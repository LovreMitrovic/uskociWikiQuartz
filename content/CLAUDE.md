# Genealogy Wiki — Schema and Conventions

This is a personal genealogy knowledge base, built from literature, articles, and transcribed historical sources. It follows the LLM Wiki pattern (see `llm-wiki.md` for the underlying idea): you read sources and ask questions; I (the LLM) maintain the wiki.

The focus is **people, surnames, dates, and places**. Everything else is in service of that.

## Directory layout

```
/
├── CLAUDE.md          ← this file (the schema)
├── llm-wiki.md        ← the underlying idea (reference, not edited)
├── raw/               ← immutable source documents (I never modify these)
│   ├── articles/
│   ├── books/
│   ├── transcriptions/
│   └── assets/        ← images, scans, maps
└── wiki/              ← LLM-maintained markdown (I own this)
    ├── index.md
    ├── log.md
    ├── people/        ← one file per individual
    ├── surnames/      ← one file per surname (hub pages)
    ├── places/        ← one file per place
    ├── families/      ← marriages / households (optional, when useful)
    ├── events/        ← migrations, wars, plagues, etc.
    └── sources/       ← one file per ingested source
```

The two layers are strict: `raw/` is read-only truth; `wiki/` is everything I write. If a source is uncited or unfileable, it belongs in `raw/`, not `wiki/`.

## Entity types

Six page types. Each has a fixed frontmatter shape so Dataview queries work.

### Person — `wiki/people/<id>.md`

The most important rule: **stable IDs in filenames**, because names repeat heavily. Format: `<Given>-<Surname>-b<year>-<birthplace>.md`. Use `b????` if the birth year is unknown, and the most common modern surname spelling.

Examples:
- `Ivan-Horvat-b1820-Zagreb.md`
- `Marija-Novak-b1825-Senj.md`
- `Petar-Mitrovic-b????-Klis.md`

Frontmatter:

```yaml
---
type: person
given_name: Ivan
surname: Horvat              # canonical (modern) spelling
surname_variants: [Horwath, Horvath, Hervat]
birth_date: "c. 1820"
birth_place: "[[Zagreb]]"
death_date: "1885-03-12"
death_place: "[[Zagreb]]"
father: "[[Marko-Horvat-b1790-Zagreb]]"
mother: "[[Ana-Kovac-b1795-Sisak]]"
spouses: ["[[Marija-Novak-b1825-Zagreb]]"]
children: ["[[Petar-Horvat-b1850-Zagreb]]"]
occupation: blacksmith
religion: Roman Catholic
sources: ["[[Zagreb-Parish-Register-1820-1850]]"]
confidence: high             # high | medium | low | speculative
---
```

Body sections (in this order, omit if empty):

```markdown
# Ivan Horvat (c. 1820 – 1885)

## Summary
One-paragraph life summary. Each factual claim ends with a source link, e.g.
"Born around 1820 in Zagreb [[Zagreb-Parish-Register-1820-1850]]."

## Timeline
- **c. 1820** — Born in Zagreb. [[source]]
- **1845-06-12** — Married Marija Novak in Zagreb. [[source]]
- **1850** — Son Petar born. [[source]]
- **1885-03-12** — Died in Zagreb, age ~65. [[source]]

## Family
- Father: [[Marko-Horvat-b1790-Zagreb]]
- Mother: [[Ana-Kovac-b1795-Sisak]]
- Spouse: [[Marija-Novak-b1825-Zagreb]] (m. 1845)
- Children: ...

## Notes
Anything that doesn't fit above — disputes between sources, anecdotes,
open questions, links to related people not in the family tree.

## Sources
- [[Zagreb-Parish-Register-1820-1850]]
- [[Article-Horvat-Family-History]]
```

### Surname — `wiki/surnames/<Surname>.md`

Hub pages — this is where the surname focus lives. One per canonical surname spelling.

```yaml
---
type: surname
canonical: Horvat
variants: [Horwath, Horvath, Hervat, Horvatić]
etymology: "From Croatian 'Hrvat' meaning Croat."
origin_region: "[[Croatia]]"
first_attested: "c. 1500"
---
```

Body:

```markdown
# Horvat

## Etymology and origin
...

## Spelling variants across sources
- **Horwath** — Latin/German records, 16th–18th c.
- **Horvath** — Hungarian records
- **Horvat** — modern Croatian
- **Hervat** — occasional 18th c. variant in Dalmatian sources

## Geographic concentration
Where bearers cluster, by century if relevant.

## Bearers in this wiki
(Auto-generate via Dataview when convenient, or keep manually.)
- [[Ivan-Horvat-b1820-Zagreb]] — Zagreb blacksmith, 1820–1885
- [[Marko-Horvat-b1790-Zagreb]] — Ivan's father
- ...

## Notable lineages
Group bearers by traceable family lines when known.
```

### Place — `wiki/places/<Place>.md`

Page title is the **modern name**. Body records historical names with date ranges, since borders and names shift over centuries — critical for this region.

```yaml
---
type: place
modern_name: Zagreb
historical_names:
  - { name: "Agram", language: "German", period: "until 1918" }
  - { name: "Zágráb", language: "Hungarian", period: "until 1918" }
parent_admin:
  - { unit: "Zagreb County", period: "current" }
  - { unit: "Kingdom of Croatia-Slavonia", period: "1868–1918" }
  - { unit: "Habsburg Monarchy", period: "1527–1918" }
coordinates: "45.8150, 15.9819"
---
```

Body:

```markdown
# Zagreb

## Names and jurisdictions over time
Brief prose on what the place was called and which polity/parish it
belonged to in each period. Important because parish records are
typically filed under the contemporary name and jurisdiction.

## Notes
Anything relevant for genealogy — major events, plagues, fires that
destroyed records, migration waves in/out, etc.

## People associated with this place
- [[Ivan-Horvat-b1820-Zagreb]] — born here
- [[Marija-Novak-b1825-Zagreb]] — born here, married here
- ...
```

### Family / Household — `wiki/families/<id>.md` (optional)

Use when a marriage or household is a meaningful unit — usually when there are several children to track or the household is itself a subject of sources. ID format: `<Husband-id>+<Wife-id>` (use the person filenames without `.md`).

```yaml
---
type: family
husband: "[[Ivan-Horvat-b1820-Zagreb]]"
wife: "[[Marija-Novak-b1825-Zagreb]]"
marriage_date: "1845-06-12"
marriage_place: "[[Zagreb]]"
children:
  - "[[Petar-Horvat-b1850-Zagreb]]"
  - "[[Ana-Horvat-b1852-Zagreb]]"
---
```

### Event — `wiki/events/<Event>.md`

For things that touch multiple people/places: migrations, wars, plagues, mass conversions, boundary changes.

```yaml
---
type: event
name: "Great Migration of the Serbs (1690)"
start_date: "1690"
end_date: "1691"
places: ["[[Kosovo]]", "[[Vojvodina]]", "[[Habsburg Monarchy]]"]
---
```

### Source — `wiki/sources/<Source-Id>.md`

One per ingested item. Captures the citation and how I assessed its reliability.

```yaml
---
type: source
title: "Zagreb Parish Register, 1820–1850"
author: "Various parish priests"
publication: "Original parish records, transcribed 1923"
date: "1820–1850"
source_type: primary        # primary | secondary | tertiary
form: original              # original | derivative | transcription | translation
language: Latin
location_in_raw: "raw/transcriptions/zagreb-parish-1820-1850.md"
ingested: "2026-04-29"
reliability: high           # high | medium | low
---
```

Body:

```markdown
# Zagreb Parish Register, 1820–1850

## Summary
What this source is, what it covers, what it doesn't.

## Citation
Full bibliographic citation in a consistent style.

## Reliability and biases
Primary/secondary, known gaps (e.g. fire of 1880 destroyed the 1830s
volume), copyist errors, translation issues. Anything a future reader
needs to know to weigh claims drawn from this source.

## Key facts extracted
- Births recorded: ~3,400
- Marriages: ~900
- Deaths: ~2,800
- Period: 1820–1850
- Persons added to wiki from this source: 47 (see log entry [[log#2026-04-29]])
```

## Conventions

### Page depth — current default: breadth-first
Default to **thin index-card pages**: frontmatter + 1–3 lines of body. Skip optional body sections (Timeline, Family, Notes) unless trivial to fill from the source or specifically requested. Goal is comprehensive coverage of surnames / places / persons rather than narrative depth on any one page. This default can be revisited as the wiki grows or when a specific lineage warrants deeper treatment.

### Stable IDs
Person filename = `<Given>-<Surname>-b<year>-<birthplace>.md`. Use `b????` for unknown birth year. Strip diacritics in filenames (`Mitrović` → `Mitrovic`) but keep them in body text and the `surname` frontmatter field.

### Fuzzy dates
Pin one format. Use these tokens:
- `1820-03-12` — exact
- `1820` — known year only
- `c. 1820` — circa, approximate
- `bef. 1850` — before
- `aft. 1830` — after
- `1820–1825` — range (use en-dash)
- `?` — unknown

Do not invent precision. If the source says "around 50 years old in 1870," record `c. 1820`, not `1820`.

### Citations
Every factual claim on a Person, Place, Family, or Event page ends with a `[[Source-Id]]` link. If a fact has multiple supporting sources, list them all. If sources disagree, record both and note the conflict in the page's **Notes** section.

### Confidence levels
On Person pages, set `confidence:` based on the strongest evidence:
- `high` — multiple primary sources agree
- `medium` — single primary source, or multiple secondary sources
- `low` — single secondary source, or weak evidence
- `speculative` — inferred (e.g. likely father based on naming patterns), not directly attested

### Surname spelling
Canonical spelling = modern Croatian/local form. Always record variants in the surname frontmatter and on the Person page (`surname_variants:`). When a source uses an old spelling, file the person under the canonical surname but keep the source's spelling visible in the body.

### Place names
Page title = modern name. In Person frontmatter `birth_place`, link to the modern-name page even if the source uses a historical name. The historical name belongs in the Place page's body and frontmatter, and can appear in the Person's body prose.

### Diacritics in body text
Keep them everywhere except filenames. `Mitrović`, not `Mitrovic`, in prose.

## Workflows

### Ingest

**Hard rule: I never write or modify wiki pages during an ingest without your explicit approval.** Reading and discussing the source is fine; writing wiki pages requires an explicit "go" from you. This applies even if you said "ingest it" — that's an instruction to begin the workflow, not pre-approval to write.

When you drop a source in `raw/` and tell me to ingest it:

0. **Status check.** Show what's currently pending vs. ingested by diffing `raw/` against `location_in_raw:` fields in `wiki/sources/*.md`. Concretely:

   ```bash
   find raw -type f \( -name "*.md" -o -name "*.txt" -o -name "*.pdf" \) | sort > /tmp/raw.txt
   grep -h "^location_in_raw:" wiki/sources/*.md 2>/dev/null \
     | sed -E 's/.*"([^"]+)".*/\1/' | sort > /tmp/ingested.txt
   comm -23 /tmp/raw.txt /tmp/ingested.txt
   ```

   Confirm with you which file(s) to work on if it's ambiguous.
1. **Read the full source.** Note its language, period, and form (transcription, scholarly article, primary record, etc.).
2. **Discuss key takeaways** with you before writing — what people, places, surnames, events appear, and any surprises. **Wait for your explicit approval before proceeding to step 3.**
3. **Create the Source page** in `wiki/sources/` with full citation and reliability notes.
4. **For each person mentioned:**
   - Check `wiki/people/` for an existing match (same name + plausible date/place overlap). If unsure, ask before merging vs. creating new.
   - Create or update the Person page. Add a **Timeline** entry for each event from this source.
   - Update relevant frontmatter (parents, spouses, children, dates, places).
5. **For each surname:** create or update the Surname page. Add new variants if the source uses different spellings. Add new bearers to the bearer list.
6. **For each place:** create or update the Place page. Add historical names if the source uses any not yet recorded.
7. **Update `wiki/index.md`** with any new pages.
8. **Append to `wiki/log.md`** with a structured entry (see Log format).
9. **Report back to you** with a summary of what changed and any open questions (ambiguous identities, missing dates, conflicts with existing pages).

A single source typically touches 10–30 wiki pages. Default to ingesting one source at a time so you can supervise.

### Query

When you ask a question:

1. Read `wiki/index.md` first to find candidate pages.
2. Read those pages. Follow links as needed.
3. Synthesize an answer with citations — every claim links to the Person/Source page that supports it.
4. **Offer to file the answer back into the wiki** if it's substantive (a comparison, an inferred lineage, a timeline). Comparisons live in `wiki/` as new pages; one-off conversational answers don't need filing.

### Lint

When you ask me to lint:

1. **Conflicting dates/places** for the same person across sources — flag and suggest a resolution.
2. **Possible duplicates** — persons with the same surname + given name + overlapping dates and no shared sources. Prompt to merge or distinguish.
3. **Orphan people** — Person pages with no inbound links from family, source, or place pages. Often a sign of an isolated reference that should connect somewhere.
4. **Missing surname or place pages** — Person pages reference a surname or place with no hub page yet.
5. **Stale claims** — older sources contradicted by newer, more authoritative sources.
6. **Confidence drift** — Person pages marked `high` confidence but sourced from a single secondary reference.
7. **Suggest follow-ups** — questions worth investigating, sources worth seeking out (parish registers, censuses, regional histories).

## index.md format

Catalog organized by entity type. One line per page: link, one-line description, optionally key dates/places.

```markdown
# Wiki Index

## People
- [[Ivan-Horvat-b1820-Zagreb]] — Zagreb blacksmith, c. 1820–1885
- [[Marko-Horvat-b1790-Zagreb]] — Ivan's father, Zagreb, c. 1790–1850
- ...

## Surnames
- [[Horvat]] — 12 bearers, Zagreb / Sisak / Karlovac
- [[Mitrović]] — 8 bearers, Senj / Klis / Knin
- ...

## Places
- [[Zagreb]] — capital of Croatia; 23 people associated
- [[Senj]] — Adriatic port; Uskok stronghold; 14 people
- ...

## Events
- [[Great Migration of the Serbs (1690)]]
- ...

## Sources
- [[Zagreb-Parish-Register-1820-1850]] — primary, ingested 2026-04-29
- ...
```

## log.md format

Append-only, with a consistent prefix so it's grep-parseable: `## [YYYY-MM-DD] <op> | <description>`. Operations: `ingest`, `query`, `lint`, `note`.

```markdown
# Wiki Log

## [2026-04-29] ingest | Zagreb Parish Register 1820–1850
- Source page: [[Zagreb-Parish-Register-1820-1850]]
- Persons added: 47 (see source page for list)
- Persons updated: 12
- New surnames: Horvat, Novak, Kovač
- New places: Sisak (referenced)
- Open questions:
  - Two Ivan Horvats born c. 1820 — possibly the same person? Need cross-check.
  - Marija Novak's mother unnamed in records — flagged in her page Notes.

## [2026-04-30] query | Trace Horvat lineage to 1700s
- Filed answer as: [[Horvat-Lineage-Pre-1800]]
- Drew on: [[Zagreb-Parish-Register-1820-1850]], [[Article-Horvat-Family-History]]

## [2026-05-02] lint | Routine check
- Flagged 3 possible duplicates (see lint report below)
- 2 orphan Person pages — proposed connections
- Suggested follow-up: seek 1780s Zagreb parish records
```

Quick recent-history command: `grep "^## \[" wiki/log.md | tail -10`.

## What I will not do without asking

- Merge two Person pages into one (always confirm).
- Delete a page (confirm; usually merge or mark deprecated instead).
- Change a confidence level from `high` to `low` (flag in lint output, ask).
- Modify anything in `raw/` (never).
- Invent precision in dates or relationships not stated in sources.

## Evolving this schema

This document is the configuration. When something feels awkward — too verbose, missing a field, wrong category — tell me and we'll update CLAUDE.md together. The schema should evolve as your wiki grows.
