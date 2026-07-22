# Wiki Log

## [2026-04-29] note | Wiki initialized
- Created `CLAUDE.md` schema
- Created directory skeleton (`raw/`, `wiki/`)
- Ready for first ingest

## [2026-05-01] ingest | Desnica 1950 — Istorija kotarskih uskoka 1646–1684, sveska I
- Source page: [[Desnica-1950-Kotarski-Uskoci-I]]
- Raw file: `raw/articles/desnica1.txt` (~15,303 lines, 399 numbered documents)
- **Approach**: full-breadth ingest per user instruction "every surname even one mention, especially with place attestation."
- **Pages created or substantially updated**:
  - 1 source page
  - 12 person pages (Janko Mitrović, Stojan Janković, Zaviša Janković, Janja Janković, Ilija Mitrović, Vukadin Mitrović, Petar/Ilija/Filip/Smoljan Smiljanić, Vuk Mandušić, Tadija Vrančić; updates to Stipan Sorić, Cvijan Šarić)
  - 6 events: Battle of Ribnik 1648 (with the canonical 14-harambaša roster), Battle of Zečevo I 1648 (updated existing Zečevo place), Battle of Zečevo II 1666, Conquest of Klis 1648, Cetina rotta 1666, Bribir ambush 1668, Vrana uprising 1683–84, Grusi krajiški statut 1654
  - 2 family pages: Janković-Mitrović household, Smiljanić household
  - ~85 surname pages — every surname mentioned, including single-mention with place. Major lineages: Mitrović, Smiljanić, Sorić, Mandušić, Vrančić, Šarić, Posedarski (Benja-Posedarski), Bortulačić, Močivuna, Pivljanin-Nikolić, Sinobad, Atlagić, Filipović, Durakbegović, Crnica. Single-mention bearers documented with place links: Tadić, Knežević, Vukčević, Rorčić, Tomičić, Miković, Miljanić, Dobrić, Letica, Ivetković, Šušić, Marković, Milić, Mihaljević/Miljević, Glumac, Pletikosić, Punoš, Mirković, Roić, Bobričić, Magačić, Bogdanović, Đerverščović, Grabović, Vićasić, Bušanić, Milović, Milković, Vukobratović, Krešović, Lukin, Dragojl, Kovilović, Nižić, Čipić, Mihelić, Omeljić, Vukdrašinović, Bogetić, Lovrić, Pauković, Šutić, Tintić, Rešinčić, Dragović, Nakić, Mirčetić, Klarić, Gečić, Vlastelica, Soppe, Begna, Civaleli, Detrico, Calcina, Cassio, Pasini, Fanfogna, Harlić, Bućević, Pugnić, Cheuro, Karsolov, Jelušić, Kolić, Capelletto, Garković, Milatović, Katalinić, Banić, Halaburić, Grubišić, Cernizza/Crnica, Renessi, Vlasto, Zarcanin, Kosulović, Lalić, Miagostović, Mistakieli, Stipčević, Busović, Gabrieli, Vuković, Kapuano, Krivelari, Sinčević, Kužinović, Kučić, Marininić, Crekat, Gargurica, Petković, Čačić, Salihagić, Firdusović, Čengić, Vidimlić, Bojičić, Bjedov, Kordić, Jokić, Bogavac, Stojanović, Banenović, Bačić, Radić, Vlatković, Matak, Škulić, Valičić, Ugarković, Dundović, Radobilić, Jović, Vlaković, Lilić, Sikirić, Garkinić, Stiljić, Barićević, Kovač, Šarić, Klanaz, Pačić... (full list above).
  - ~22 place pages created or expanded: Žegar, Posedarje, Udbina, Gorica, Vinjerac (Castel Venier), Otres, Ribnik, Vučjak, Zečevo, Mokro Polje, Knin (updates to existing). Many Bukovica/Velebit-Podgorje villages also linked.
  - **Total**: ~70+ new pages, ~30+ updates to existing pages.
- **Critical genealogical correction recorded** on [[Smiljanic|Smiljanić]] surname page and [[Petar-Smiljanic-b????-Udbina]] person page: per Desnica's footnote on doc. 20, the Smiljanići originated in **[[Udbina]], NOT [[Smiljan-Lika|Smiljan]]** — overrides legend.
- **Notable pre-existing pages substantially expanded with Desnica material**: [[Stipan-Soric-b????-Gorica]] (Candian War career, death at Ribnik, posthumous relic-cult); [[Cvijan-Saric-b????-Sibenik]] (full multi-decade career with sons Iuan/Žorži/Jovan); [[Posedarski]] (full 17th c. genealogy of Frano-Žorži-Frano cycle); [[Filipovic|Filipović]] (Bosnian beg-line); [[Bunjevac]] (Nikola Bunjevac of Otres 1662 added as concrete bearer); [[Brajnovic|Brajnović]] (Petropolje + Zadar branches); various single-mention surname pages (Bačić, Skulić, Vlatković, Grubić, Brajnović, Dević, Smiljanic — all updated with new bearers).
- **Migration roster docs digested**: doc. 39 (1648 Ribnik 14-harambaša roster — origin → settlement, the canonical document); doc. 70 (1653 power-of-attorney with 20+ harambaše with origin villages); doc. 84 (1654 Sv. Zulijan 37-name list of šibenski pravoslavni Morlachi); docs. 199 (1671 Dračevac re-settlement of 43 souls in 20 households); doc. 358 (1683 Lazar Dragović's 1500-family roster of Skradin–Vrana area); doc. 381 (1684 Donà's 30+ village-capitano roster); doc. 397 (1684 Tepšinci/Parčići uskakanje, 615 fighters / 5307 souls).
- **Open questions / lint candidates**:
  - **Stojan Janković's first wife**: variously *Vinka* and *Vuka* in this corpus; Desnica's footnote on doc. 211 acknowledges this.
  - **Bartul Banenović** "Germano del carambassà Elia Smiglianich" — *Germano* could mean "(first) cousin" or "kinsman"; precise relation unclear.
  - **Smoljan Smiljanić's paternal patronymic** — sometimes given as "Mihalevich" (doc. 103). Either this records his father's surname (unattested) or marks a Mihaljević line distinct from the Drniš Mihaljević.
  - **Ilija Mitrović sentence 1680**: precedes Vrana uprising; Desnica's footnotes treat his role as fully documented but interpretively complex.
  - **Janko Mitrović's brothers**: Stojan's 1670 supplica names Janko, Giovanni, Stefan, Pavle, Andrija — but only Janko and (probably) Vukadin appear in the pay-records.
  - **Cvijan Šarić's death-date**: still alive 1668-10-06 (doc. 162); pay had passed to son Jovan in 1662; the 1660 Evlija Çelebi attestation describes him in his prime.
  - **Senate's name-confusion in doc. 215** (1675-08-24): "Cianco suo frello" of Stojan Janković — but Stojan had no actual brother named Janko (Desnica's fn: probably patronymic for Zaviša or Ilija).
  - Doc. 397 (Tepšinci/Parčići) ends the volume; the *uskakanje* outcomes are in Sveska II.
- **Updated**: [[index]]
- **Status check next session**: `comm -23 raw/ vs wiki/sources/*.md location_in_raw` will now show **only `desnica2.txt`** as pending.

## [2026-04-29] ingest | Šarić 2024 — Osmanski Vlasi Istre na izvornoj Tromeđi
- Source page: [[Saric-2024-Vlasi-Istre]]
- Raw file: `raw/articles/saric-marko-vlasi-istrije-na-izvornoj-tromedi.txt` (~26k words, 3128 lines)
- **Approach**: breadth-first / index-card pages per CLAUDE.md "Page depth" convention
- Pages created (303 total):
  - 1 source
  - 7 events: Ottoman Conquest 1522–27, Vlach Migration to Istria 1518–23, Vlach Return to Klis 1528–30, Venetian-Ottoman War 1537–40, Vlasi Istre Migration to Venice 1538, Cyprus War 1570–73, Pazin Peasant Revolt 1570
  - 98 places: regions, jurisdictions (Tromeđa, Vilajet Hrvati, sandžaci), cities, ~40 villages
  - 77 surnames: 12 substantive Vlach lineages (Poropat, Gleđevac, Ružić, Najčinović, Milovanić, Rudelić, Frletić, Prejić, Šiljanović, Krmpotić, Milohanić, Mušković), plus 26 footnote-list continuity surnames, 14 starešina/Vlach-group hubs, and 24 Croatian/Habsburg/Venetian/Ottoman / clergy lines
  - 120 persons: ~32 Vlach starešine 1528–1550, families of Najčinović/Gleđevac/Frletić/Prejić/Poropat (~25), ~12 late-period persons, 6 Catholic clergy, 7 noble defectors/converts, 6 Habsburg captains, 16 Venetian officials, 9 Ottoman officials
- **Open questions / lint candidates** for future review:
  - "Petar, sin Jančića" (Ostrovica 1530) and Petar Najčinović (Dobruča Vas) — likely same person, marked confidence: medium; may want to merge.
  - Stjepan Posedarski as both 1519 chaplain and as Muslim convert — possibly two distinct men.
  - Many register-only persons have only patronymic; surnames inferred from patronymic stems (e.g. "sin Milovana" → Milovanić). Treat as provisional until cross-referenced.
  - "Ivaniš sin Mirka" (joint Donje/Gornje Miranje timar with Ivaniš Poropat) — not yet given own Person page; mentioned only in body of Ivaniš Poropat.
  - Footnote-list continuity surnames have no concrete bearers in this source; pages exist as placeholders.
- **Updated**: [[index]]
- **Status check next session**: `comm -23` of `raw/` vs `wiki/sources/*.md` `location_in_raw:` should now show 0 pending.

## [2026-05-01] ingest | Desnica 1951 — Istorija kotarskih uskoka 1684–1749, sveska II
- Source page: [[Desnica-1951-Kotarski-Uskoci-II]]
- Raw file: `raw/articles/desnica2.txt` (~17,973 lines, 392 numbered documents)
- **Period**: 6 May 1684 – 9 April 1749
- **Approach**: full-breadth ingest per user instruction "every surname captured even if mentioned once, with as much info and context as possible." User confirmed expanding farther than the desnica1 pass.
- **Extraction**: 4 parallel agents read the source in chunks (1–3600, 3600–7200, 7200–10800, 10800–14400, 14400–end) and produced structured entity inventories totaling ~700 person-mentions and ~370 surname-mentions across chunks (with substantial cross-chunk overlap).
- **Pages created or substantially updated** (this session):
  - 1 source page: [[Desnica-1951-Kotarski-Uskoci-II]]
  - **+169 person pages** (people count rose from 203 → 372): Janković family extensions (Antonia Reci, Janko, Marija/Marietta, Liberal, Magdalena, Nikola, Konstantin, Frane Peraica), Filippo Mitrović of Obrovac, Marija Mitrović = Vučen Stojisavljević's wife, Vučen Stojisavljević, Petar Mitrović-Stojisavljević, Lazaro Smiljanić, Maria Bolić-Smiljanić; the Kotari capi extras (dr. Antun Bortulačić); Venetian provveditori (Mocenigo, Donà, Pasqualigo, Valier, Cornaro, Molin (Alessandro and Antonio), Dolfin, Vendramin, Riva, Zane, Diedo, Mocenigo II) and ~40 Venetian/Italian noble surnames as simple records (Loredan, Gritti, Memo, Grimani, Barbarigo, Ruzzini, Marcello, Soranzo, Foscarini, Quirini, Bollani, Spolverino, Pizzamano, dal Borro, Civran, Corner...); Ottoman Knin/Sinj/Bihać families (Atlagić — Mehmed pasha + son + nephew Alibeg, Mandić — Šain-aga + Hasan-aga + Šakija-aga, Pašić of Ripač, Idris-aga of Bihać, Kumalić, Durakbegović expansions); harambase / serdari (Boža Milković, Lazaro Cona, Vukon Cvitanović, Filippo Tintor, Stipan Goreta, Palikuća, Žinović, Vučić Oluić, Ostoja Gagić, Rade Tepšić, Vukosav Kosić, Jovan Sudarović, Pietro/Dimitri/Jovan Sinobad, Mehrem Komanija, Mihael Milinović, Mattio Strmić, vojvoda Ivan Marušić, pop Pavao Žuljević, Mitar/Petar/Bajo/Vuko/Zuane Nikolić of Kotor, Nicolò Corponese, Nikola Blagojević, Jovan Božić, Marco Podgorica, Frane Gaeta, Stipan Garković, Pietro Tartaglia, Razzetini, Geliseo, Casotti, Manzecchi, Pavle Vukčević); Vrana harambase 1684 (Mirčetić, Vučić, Đekić, Mattio Pop, Lepur, Najerlović, Pančić, Bajčić, Parišić, fra Grgur Šutić, Ilija Radašinović); single-mention Žegar/Razanci/Radovin Morlachs (Mihajlo Radmilović, Marko Matak, Ivan Brkljača, Giacomo Bistrić, Mattio Boljač); Avramović brothers; Vukašin Rošić of Čitluk Lički; Vuko Vojkorsić; Hajra/Kosa Lakić; Zelel-aga Babahmetović; the chunk-3 lineages (Đurić brothers, Pirić, Zorić, Prešević, Vidović, Budisalić, Cesare Casanova, Pietro Calčina, Vid Petrović, Ilija Nanić, pop Petar Jagodić-Kuridža (rich page), Mattio Žabetić, Tomaso Tubić, Marlatić); chunk-4 figures (Mede Miljković, Jurašin Vučina, Radoš and Sava Kresović, Modre, Doge Silvestro Valier, Pisani, Contarini, Califfi).
  - **+8 events**: [[Sinj-Battle-1685]], [[Lika-Settlement-Census-1685]], [[Sinj-Conquest-1686]], [[Jankovic-Regiment-Authorisation-1686]], [[Stojan-Jankovic-Death-Duvno-1687]], [[Knin-Conquest-1688]], [[Kotari-Pertinenze-Reform-1689]], [[Bortulacic-Murder-Vrana-1692]], [[Bjelaj-Migration-1692]], [[Bukovica-Revolt-1704]] (10 created).
  - **+4 surname pages**: [[Nanic]], [[Zelic]], [[Radmilovic]] (Žegar footnote stubs per Desnica's 1951 editorial note + document body context); [[Vukcevic]] updated with 1951 footnote and 1684 Budin feud context.
  - **Updated existing major figures**: [[Stojan-Jankovic-b1635-Zegar]] (full Desnica II timeline 1684-1687, including children's deaths, regiment authorisation, Bribir defence, death at Duvno); [[Smoljan-Smiljanic-b????-Bukovica]] (1684–1686 timeline, wife Marica, son Lazar, daughter Margarita); [[Simun-Bortulacic-b????-Zadar]] (extension to 1692-01-16 murder at Vrana); [[Zavisa-Jankovic-b????-Zegar]] (Obrovac kapitan years, 1693–1696 raids attestation, 1697 pay raise, Spanish Succession redeployment); [[Ilija-Mitrovic-b????-Zegar]] (1684 terminacija, 1685 stipend petition, 1693 death; Peraica identity contested-flag note).
- **User directives applied**:
  1. Confirmed: Stojan Janković = Stojan Mitrović (same person).
  2. Burials recorded literally (e.g., "buried at Sv. Ilija in rito greco") with no religious-identity inference.
  3. Two Obrovacs / two Starigrads / two Poljicas / two Plavnos treated as distinct places with disambiguation notes.
  4. [[Plavno]] treated as distinct from [[Plavna]] with cross-reference note "may be the same place".
  5. Lapac complaint (doc 126) recorded on Stojan's page as fact, no resolution.
  6. Iljanović letter (doc 139) recorded on Stojan's page as fact + flagged as State-Inquisitor-suspicious.
  7. Marin Michiel kept distinct from existing [[Marin-Cavalli-b????-Venice]].
  8. Žegar footnote surnames (Zelić, Radmilović, Vukčević, Nanić) recorded with one-line note "still present in Žegar today (1951)" + source link, plus document-body bearers where attested.
- **Open questions / lint candidates**:
  - **"Peraica" identity**: Ilija "Peraica" of the March 1685 Cetina migration killed by corsair fusta off Rogoznica (Aug-Sept 1685) is treated as DISTINCT from Ilija Mitrović of Žegar (who died of natural causes 1693 per chunk-3 attestation). The original chunk-1 agent conflated them — flagged on [[Ilija-Mitrovic-b????-Zegar]].
  - **Iljanović letter (30 July 1686)**: claimant Matija Iljanović of Vienna asserts descent from "signori de Illyanova" of Gabela/Hum/Hercegovina; flagged by Cornaro and Inquisitors as Ragusan intrigue. Page TODO.
  - **Lapac complaint (1 Feb 1686)**: anonymous Morlach accusations of extortion by Janković + Bortulačić; recorded on both pages, no resolution in source.
  - **Janko Janković son of Stojan**: died 23 Aug 1685, distinct from Stojan's father Janko Mitrović (d. 1659). Pages disambiguated.
  - **Marin Michiel**: capitano + provveditor estraordinario commissario 1685, NOT [[Marin-Cavalli-b????-Venice]] — separate page created.
  - **Two Bortulačićs in Zadar**: kavalier Šimun (capo de Morlacchi, murdered 1692) and dr. Antun (his brother, lawyer, drafted petitions). Both have pages.
  - **Magdalena Janković** (d. 13 May 1684): source records "sepolta nella chiesa di sant'Elia essendo di rito greco" — literal record only, no religion inference per user directive.
  - **War of Spanish Succession redeployments (post-1701)**: Zaviša Janković and Lazar Smiljanić deployed to Italy; recorded on pages but no dedicated event page yet.
- **Coverage gaps (deferred to future passes)**:
  - **Surname pages**: ~150–200 NEW surnames mentioned in extracts but not yet given dedicated Surname pages. The information is captured on Person pages and via source citations, but the surname-hub pattern is not fully populated for this source. Priority candidates for next pass: Cona, Cvitanović, Tintor, Goreta, Palikuća, Žinović, Karalija, Oluić, Gagić, Tepšić, Kosić, Sudarović, Marušić, Žuljević, Strmić, Milinović, Komanija, Korponež, Marinović, Nuncović, Iljanović, Pašić, Bastić, Kumalić, Mandić, Salomonić, Podgorica, Pierantonii, Grizogono, Cloder, Bardi, Cassio (existing — needs extension), Lantana, Tori, Sorini, Spachioto, Alberti (place-page exists), Gioachini, Manzecchi; Venetian Cornaro, Loredan, Gritti, Memo, Grimani, Barbarigo, Vendramin, Ruzzini, Civran (existing — needs extension), Marcello, Soranzo, Foscarini, Quirini, Bollani, Spolverino, Pizzamano, dal Borro; chunk-3/4: Stojisavljević (existing — needs extension), Califfi, Calčina, Žabetić, Tubić, Marlatić, Jagodić, Spiro, Petrović (Vid), Obradović of Bruvno, Canagetti, Vojnović, Erizzo, Paulucci.
  - **Place pages**: ~60–80 NEW places mentioned but not yet given pages. Priority candidates: Lantana, Belgrade, Vienna, Banja Luka, Cattaro/Kotor, Ulcinj, Cetinje, Pastrovići, Budva, Zaostrog, Vrgorac, Imotski, Makarska, Gabela, Norin, Forte Opus, Zadvarje (Duare), Omiš (Almissa), Prolog, Solin (Salona), Hercegnovi, Velim, Daslina, Slosella, Vrpolje, Novigrad (Dalmatia), Karlobag, Krka river, Biljane, Nadin, Poličnik, Malpaga, Grahovo, Vienna, Karlovac, Buda, Sarajevo, Duvno, Bribir, Skradin (existing — needs extension), Split, Trogir, Kaštela, S. Simeone Zadar (contrada), Sv. Ilija Zadar (Greek-rite church), Sv. Šime Zadar, Bilišani, Boričevac, Ripač, Lapac, Bjelaj, Vakuf (Kulen Vakuf), Srb, Komić, Medak, Rebac, Parčići, Olib (1701 sale), Bruvno (where Vid Petrović killed 1707).
  - **Events**: a few additional events worth dedicated pages — Bjelaj/Vakuf raid 1685, Lika joint raid 1685, Lapac raid 1686, two Livno raids 1686, Bosnian Pasha Kotari raid Nov 1686, Pastrovići siege relief 1686, Knin millworks raid 1686, Rama Franciscan migration Oct 1687, Skoplje migration Nov 1687, Bosnian pasha April 1688 raid, Vrlika capitulation Sept 1688, Brochno-Goranci migration 1693–94, Mostar/Rusić migration 1692, War of Spanish Succession deployments, 1707 Bruvno (Vid Petrović killed), Olib sale 1701, Rákóczi mission of Vojnović 1706, Papal anti-pirate recruitment 1717, Sinobad death at Glamoč 1715.
  - **Reason for partial coverage**: parallel writing agents launched in this session (4 in parallel, one per chunk) hit Anthropic API rate limits (resets 8:30pm Europe/Zagreb) before completing the surname/place/event sweeps. Person pages were highest priority and got through. Plan: resume Surname/Place/Event sweeps in a follow-up session.
- **Updated**: [[index]] (sources, events sections; persons + surnames counts updated).
- **Status check next session**: `raw/` vs `wiki/sources/*.md` `location_in_raw:` should show 0 pending. The follow-up work is *within* desnica2 (surname/place/event sweep), not a new ingest.

## [2026-05-01] note | desnica2 sweep continuation — paused mid-pass
- After 8:30pm rate-limit reset, four parallel agents resumed the sweep.
- **Completed in this continuation**:
  - Surnames chunks 1+2 agent finished: **+165 new surname pages, +13 existing updates** (persons-side total 239 → ~405).
  - Events agent finished: **+38 new event pages** (31 → 79). Includes Knin-Battle-1684, Glamoč-Grahovo-Campaign-1684, Vrana-Capi-Petition-1684, Sinj-Attempt-Marcello-1684, Cetina-Migration-Peraica-1685, Mikiel-Knin-Reconnaissance-1685, Kaštela-Attack-1685, Lika-Migration-May-1685, Crna-Gora-Defection-1685, Zadvarje-Siege-1685, Bjelaj-Vakuf-Raid-1685, Lika-Joint-Raid-1685, Lapac-Raid-1686, Livno-Raid-First-1686, Livno-Raid-Second-1686, Glamoč-Engagement-1686, Pastrovići-Siege-Relief-1686, Sinj-Siege-Turkish-1686, Knin-Millworks-Raid-1686, Bosnian-Pasha-Kotari-Raid-1686 (Nov 1686 major raid), Coron-Conquest-1685, Esztergom-Battle-1685, Neuhäusel-Capture-1685, Atlagić-Bosnian-Pasha-Appointment-1687, Atlagić-Poison-Attempt-1687, Sinj-Relief-1687, Patriarch-Peć-Cetinje-Plan-1686, Zaviša-Rebac-Raid-1687, Ilija-Bilaj-Raid-1687, Varcar-Vakuf-Raid-1687, Rama-Franciscan-Migration-1687, Skoplje-Migration-1687, Zagreb-Bishop-Robbery-1688, Bosnian-Pasha-April-1688-Raid, Kanjiža-Raid-1688, Vrlika-Capitulation-1688, Brochno-Goranci-Migration-1693-94, Mostar-Rusić-Migration-1692, Mitrović-Sinobad-Reconciliation-1692, Mostar-Mokro-Polje-Raid-1696, Patriarch-Crnojević-Teodosije-1693, Vid-Petrović-Banditry-1702-1707, War-of-Spanish-Succession-Deployments, Olib-Sale-1701, Border-Demarcation-Grimani-1699-1701, Sinobad-Death-Glamoč-1715, Papal-Anti-Pirate-Recruitment-1717, Rákóczi-Mission-Vojnović-1706.
  - Places agent partial: places sweep advanced to ~346 (was 158); was stopped mid-pass; covered most chunks 1–3 places.
  - Surnames chunks 3+4 agent partial: stopped mid-pass; surname total reached 470 (was 239); chunk-3 mostly done, chunk-4 partially.
- **Stopped by user mid-pass — resume needed**:
  - **Surnames chunks 3+4 agent** stopped after partial chunk-4 work. Need to finish chunk-4 surnames not yet written. Final chunk-4 surnames known to be missing: check Califfi, Calčina, Žabetić, Tubić, Marlatić, Jagodić-Kuridža, Spiro, Petrović (Vid haiduk), Obradović (Bruvno branch), Canagetti, Vojnović, Erizzo, Paulucci, Pisani (extension), Diedo, Sfakioto, Marlatić, Modre, Vučina, Kresović (extension with Modro casale dispute), Stojisavljević (extension), Miljković (extension if not the same as existing Milkovic).
  - **Places agent** stopped while still working on chunks 3+4 places + cross-chunk dedup. Likely missing: some chunk-4 places (Bruvno, Olib, Modro/Modrino selo, Pozzi, Mt Prolog locations) and disambiguation/cross-link finish for Plavno vs Plavna, Obrovac na Cetini vs Obrovac na Zrmanji, the two Starigrads, two Poljicas, Sv-Ilija-Zadar (church) and Sv-Šime-Zadar (church) standalone entries.
- **Counts at pause**: People 372 · Surnames 470 · Places 346 · Events 79 · Sources 4 = 1,271 wiki pages (up from 623 pre-ingest).
- **Next session plan**:
  1. Finish chunk-4 surnames (~20–30 remaining).
  2. Finish chunk-3+4 places + disambiguation pages.
  3. Re-update index.md sections (surname + place lists got far past the 200-line truncation point — index will need pagination or category sub-pages soon).
  4. Lint pass: cross-check the chunk-1 agent's "Peraica" conflation, the parallel records of single-mention persons across chunks, and the disambiguation cross-references.

## [2026-05-02] note | desnica2 sweep — completed
- Resumed from 2026-05-01 pause. Items closed:
  1. **Chunk-4 surnames written**: Califfi, Žabetić, Tubić, Marlatić, Jagodić-Kuridža, Spiro, Vojnović, Paulucci, Diedo, Sfakioto, Stojisavljević, Obradović, Petrović (Vid haiduk). +13 surname pages (470 → 483).
  2. **Remaining places written**: Modro (Modrino selo, Bukovica), Pozzi (Venetian state prison). +2 places (346 → 348).
  3. **Index.md re-updated**: counts refreshed to 4 sources / 79 events / 348 places / 483 surnames / 372 persons / 2 families = 1,288 wiki pages. Events section reorganised into sub-categories (Battles & sieges, Raids, Migrations, Politics & long aftermath, Holy League) so all 70+ Morean War event pages are linkable from the index.
  4. **Peraica conflation lint resolved**:
    - [[Ilija-Peraica-b????-Cetina]] extended with death (Aug-Oct 1685, Rogoznica), brother link, and explicit disambiguation note vs. Ilija Mitrović of Žegar.
    - [[Frane-Peraica-b????-Zegar]] extended with disambiguation note (filename "-Zegar" is a legacy artifact; Peraica clan was Cetina-based, not Žegar).
    - [[Stojan-Jankovic-b1635-Zegar]] timeline entry corrected: 1685-09 Peraica death now links to Ilija Peraica (Cetina) not Frane.
    - [[Ilija-Mitrovic-b????-Zegar]] death updated to 1693 natural causes per chunk-3 attestation; "Peraica identity contested" footnote retained.
- **Final ingest counts (Desnica II totals)**:
  - +1 source page
  - +169 person pages (203 → 372)
  - +247 surname pages (236 → 483) — every surname mentioned in extracts was given a page; 13 existing pages received Desnica II extension sections
  - +190 place pages (158 → 348) — including disambiguation pages for two Obrovacs, two Starigrads, two Poljicas, two Plavnos, plus separate church pages (Sv. Ilija Zadar, Sv. Šime Zadar, Sv. Stošija Zadar)
  - +58 event pages (21 → 79)
  - **Net total**: ~665 new wiki pages, ~50 existing-page updates.
- **All 392 documents of Desnica II are now indexed via at least one entity page**. Single-mention surnames recorded with place attestation per user directive. The Janković-Mitrović cluster, the four 1684 capi, the Atlagić/Mandić/Pašić Ottoman families, the 1687 Janković death, the 1688 Knin conquest, the 1689 Pertinenze reform, the 1692 Bortulačić murder, the 1704 Bukovica revolt, and the long pop Jagodić imprisonment-to-1746 narrative are all written up with timelines and cross-references.
- **Updated**: [[index]] (full event sub-categorisation; counts).
- **Status check next session**: 0 pending sources in `raw/`; the entire desnica2 ingest is closed.

## [2026-07-19] lint | Hygiene pass — link integrity, confidence backfill, filename normalisation
Full-wiki hygiene sweep (no new source ingested). Scope: fix broken links, backfill required frontmatter, normalise filenames.

- **Broken wikilinks: 199 → 0.**
  - Stripped erroneous `.md` suffix from 10 wikilinks (incl. a stray self-link to index).
  - Created ~247 previously-unlinked target pages as thin index-cards (schema breadth-first default), each cited to one of the 4 sources; no dates/relationships invented:
    - Places: +~101 (Krmpote-migration villages, Ravni-kotari toponyms, Venetian exonyms cross-linked to modern-name pages: Cattaro→Kotor, Cherso→Cres, Cliuno→Livno, Spalato→Split, Pago→Pag, etc.).
    - Surnames: +37 hub stubs (mostly Bunjevac/Vlach muster-roll families, cited to Šarić 2008).
    - People: +52 stubs, confidence low/medium.
    - Events: +4 (Candian-War-1645-1669, Drnis-Rebellion-1608, Lika-Raid-1685, Saric-Sibenik-Pravoslavni-Morlaci-1654).
  - Residual new-outbound-link stubs created by hand: [[Crete]], [[Piva]], [[Ivan-Devic-b????]]. Fixed `Modro-Selo`→`Modro-selo` case-mismatch links (3 files).
- **Confidence backfill: 103 Person pages were missing `confidence:`; all now set** (99 low, 4 medium — graded by evidence: single-secondary-source → low, two secondary works → medium). Wiki-wide confidence now: 184 high / 85 medium / 157 low / 0 speculative.
- **Filename normalisation (ASCII rule):** 6 files had diacritics/spaces.
  - 5 were accidental duplicates of existing ASCII pages (links inconsistently spelled the same entity) — merged & stub deleted, links repointed with alias to preserve display: `Ravni Kotari`→[[Ravni-Kotari]], `Pađen`→[[Padjene]], `Vučjak`→[[Vucjak]], `Habsburška Istra`→[[Habsburska-Istra]], `Mletačka Istra`→[[Mletacka-Istra]].
  - 1 clean rename: `Žorži-Posedarski-d1679-Zadar`→[[Zorzi-Posedarski-d1679-Zadar]].
- **index.md:** removed 3 duplicate `(updated)` changelog lines (Knin, Mokro-Polje, Posedarski — already in main sections); added hygiene-pass count notes.

### Open questions / needs your decision
- **Possible Person merges (NOT merged — schema requires your confirmation):**
  - [[Andelo-Emo-b????-Venice]] ⇔ existing [[Angelo-Emo-b????-Venice]] (Anđelo = Angelo).
  - [[Anto-Matkovic-b????-Temisvar|Anto-Matkovic-b????]] ⇔ [[Anto-Matkovic-b????-Temisvar]].
  - [[Culina-sin-Milica-b????-Bjeline|Culina-sin-Milica-b????]] ⇔ [[Culina-sin-Milica-b????-Bjeline]].
  - [[Dmitar-Nikolic-b????-Plav|Mitar-Nikolic-b????-Plav]] ⇔ [[Dmitar-Nikolic-b????-Plav]].
  - [[Pietro-Sinobad-b????-Posedarje|Perica-Sinobad-b????-Budin]] ⇔ [[Pietro-Sinobad-b????-Posedarje]].
  - [[Radan-Matic-b????-Budin|Radan-Matic-b????-Brgud]] ⇔ [[Radan-Matic-b????-Budin]].
- **Possible Place merges (thin exonym/spelling stubs kept for now, cross-linked):** Biograd-na-Moru⇔Biograd, Cuculovaci⇔Cucullovaci, Krk (Sandžak Krka)⇔Krka, Novigrad⇔Novigrad-Dalmatia, Sv-Juraj⇔Sv-Juraj-Senj, Glamoc-Polje⇔Glamocko-Polje.
- **Confidence drift:** 184 Person pages still marked `high` while the wiki rests on only 4 sources; per schema `high` = multiple primary sources agree. Recommend an audit to down-grade single-source `high` pages to `medium` (not auto-changed — schema requires flagging first).
- **Plav vs Piva:** `[[Plav|Piva]]` on [[Pivljanin-Nikolic]] likely means Piva (Montenegro), not the town of Plav; both pages now exist — confirm intended referent.

## [2026-07-19] lint | Person merges (from hygiene-pass merge candidates)
Resolved 5 of the 6 flagged same-person duplicates (user-approved). Each: content folded into the canonical page, all inbound links repointed, duplicate deleted. 0 broken links after. People 426 → 421.

- **fra Anto Matković (1582, Temišvar school):** merged `Anto-Matkovic-b????` → kept [[Anto-Matkovic-b????-Temisvar]].
- **Ćulina/Čulina, sin Milića (knez, Lika timar 1528–30):** merged `Culina-sin-Milica-b????` → kept [[Culina-sin-Milica-b????-Bjeline]].
- **Dmitar/Mitar Nikolić-Pivljanin (brother of Bajo Pivljanin, m. Janja Janković 1675):** merged `Mitar-Nikolic-b????-Plav` → kept [[Dmitar-Nikolic-b????-Plav]] (folded in the 1683–84 rebellion / doc 376 detail).
- **Pietro/Perica Sinobad (kapetan di Budin, killed at Brgud 1684):** merged `Perica-Sinobad-b????-Budin` → kept [[Pietro-Sinobad-b????-Posedarje]].
- **Radan Matić (Ilija Mitrović's Budin drug / killer of Perica Sinobad):** merged `Radan-Matic-b????-Brgud` → kept [[Radan-Matic-b????-Budin]] (Budin = base, Brgud = murder site); confidence raised low → medium; identity noted as **inferential** (no single doc equates the two names).

- **NOT merged (kept separate, per user):** [[Andelo-Emo-b????-Venice]] (provveditore 1716, doc 379) vs [[Angelo-Emo-b????-Venice]] (Conte of Zadar 1684, doc 33) — same Emo patrician surname but 32 yrs apart and different offices; treated as distinct Emo-family officeholders.
- **Still open:** place-name duplicates (Biograd-na-Moru⇔Biograd, Novigrad⇔Novigrad-Dalmatia, Krk⇔Krka, Sv-Juraj⇔Sv-Juraj-Senj, Glamoc-Polje⇔Glamocko-Polje, Cuculovaci⇔Cucullovaci) — not yet reconciled. Confidence-drift audit (184 `high` on 4 sources) also still pending.

## [2026-07-21] ingest | Dundović 1610 Zadar census — Pakoštane (pilot)
- Source page: [[Dundovic-1610-Zadar-Census]] (primary transcription, Museo Correr; raw: raw/transcriptions/dundovic-1610-zadar-census.txt)
- Policy: full explosion — one Person page per named household head. Keep BOTH Croatized + original Venetian name forms (given_name_variants + surname_variants). No Family pages (source names only heads). Confidence: low.
- Pakoštane (village 1 of 18): 19 Person pages added (household heads); Place roster added to [[Pakostane]]; 13 new surname pages; [[Punos]] updated (+Marko).
- New frontmatter field introduced: `given_name_variants` (parallels surname_variants) — pending formalization in CLAUDE.md.
- Open questions:
  - Low-confidence normalizations (Veziljević, Zojić, Škilić, Ajazović, Pročić, Bašković, Piližarić) to be reconciled against the forthcoming Jelić 1608 census (scholar-Croatized).
  - Remaining 17 villages pending (Biograd, Sv. Filip i Jakov, Turanj, Sukošan, Bibinje, Dračevac, Ražanac, Posedarje, Ljubač, Gruhe, Bokanjac, Puntamika, Diklo, Bartulac, Petrčane, Kožino, Punta Ljupča).

## [2026-07-21] ingest | Dundović 1610 Zadar census — COMPLETE (all 18 villages)
- Source: [[Dundovic-1610-Zadar-Census]] (primary transcription, Museo Correr)
- Method: full explosion via 18 parallel per-village subagents (one shared spec), then central surname/index merge.
- Added: ~621 household-head Person pages; ~380 new Surname hubs; 50 existing Surname pages gained 1610 bearers; 6 new Place pages; all 18 village Place pages carry a 1610 roster. No Family pages (source names only heads). Confidence: low throughout.
- Both name forms kept (given_name_variants + surname_variants); Venetian→Croatian normalization tentative, to be reconciled against the forthcoming Jelić 1608 census.
- Fixes during merge: split [[Dracevac-Zadarski|Dračevac Zadarski (Malpaga)]] out of [[Dracevac|Dračevac kod Jasenica]] (54 people re-pointed); corrected 4 given-name stragglers (Matthio→Matija, Giacomo→Jakov ×2, Lorenzo→Lovre); annotated 12 byname/descriptor surname pages.
- Integrity: 0 broken person-links across surnames/ and places/. One surname-less head (Peruzza, Biograd na Moru) left without a hub.
- OPEN — needs decision:
  - [[Biograd-na-Moru]] vs [[Biograd-na-Moru|Biograd]] are duplicate place pages for the same town (Zaravecchia) — merge pending user approval (deletion/merge).
  - Low-confidence surname normalizations await the Jelić 1608 reconciliation pass.

## [2026-07-22] note | Timelines for 8 Vlasi Istre persons (Šarić 2024)
- Added `## Timeline` (with verbatim Croatian source quotes) + `## Sources` to 8 existing Person pages, all drawn from [[Saric-2024-Vlasi-Istre]]:
  - [[Tomas-Ruzic-b????-Sibenik]], [[Petar-Najcinovic-b????-Dobruca-Vas]], [[Murat-beg-Gajdic-b????-Sibenik]], [[Petar-Prejic-b????]], [[Bogdan-Prejic-b????]], [[Petar-Milovanic-b????-Medvidja]], [[Zakman-Gledjevac-b????-Karin]], [[Andrija-Frletic-b????-Dracevac]]
- No new pages, no frontmatter changes; enrichment of already-ingested source. Quotes cite original-language passages for provenance.
