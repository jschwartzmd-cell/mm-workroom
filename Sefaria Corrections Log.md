# Sefaria Corrections Log — Rabbi Ephrati Shiurim Pipeline

This file logs every citation correction applied via the weekly Sefaria verification pass (step 5a of the pipeline).

Each entry records: date of shiur, date of verification, footnote/section affected, original citation (as first drafted), corrected citation (as verified against Sefaria's public API), and the Sefaria API path used.

The retroactive block at the top covers the four weekly shiurim (2026-07-19 through 2026-08-30) that were originally processed while the pipeline was mistakenly using `curl` (blocked by the workspace proxy) instead of `mcp__workspace__web_fetch` (which reaches Sefaria fine). The switch to WebFetch is now baked into memory (`mareh_mekamos_workflow.md` step 5a) and the Sunday scheduled task prompt, so every future week's log entry is generated during the automated run itself.

---

## Retroactive verification — pass run 2026-09-06

### 2026-07-19 — הַמַּפִּיל, Hareini Mochel, and the Maharam's Prison Seder
- **fn5** (Rav Asher Weiss on המפיל) — flag preserved as UNCERTAIN. Rav Asher Weiss's kuntreis and shiurim on המפיל are not indexed in Sefaria's corpus (Minchat Osher not on Sefaria). No correction; this is the correct outcome per the never-fabricate discipline.
- **Total:** 0 corrections, 1 flag correctly preserved.

### 2026-08-09 — Entering Shabbos Shacharis (מזמור לתודה, תפילין, and the Seventh Wing)
- **fn20 (Seventh Wing / Tosafos Sanhedrin)** — CORRECTED. Original said "Tosafos Sanhedrin ל״ז" attributing the six-wings tradition to the Zohar. Verified against Sefaria: Tosafos on Sanhedrin **ל״ז ע״ב** (d"h "מכנף הארץ זמירות שמענו") cites **תשובת הגאונים** (Teshuvos HaGeonim), not the Zohar. The pasuk-derivation is **ישעיה כ״ד:ט״ז** ("מכנף הארץ זמירות שמענו"). Fixed daf reference + attribution + pasuk source.
- **fn10 (Mordechai / Rav Hai Gaon on late Shabbos morning davening)** — VERIFIED and TIGHTENED. Confirmed via **רמ״א אורח חיים רפ״א:א**, which explicitly cites the Mordechai with the pasuk-based reasoning. Note-academic tightened to reflect the primary-source confirmation.
- **fn18 (protesting the shaliach tzibbur for taking too long)** — CORRECTED. Original attributed this ruling primarily to the Mishnah Berurah. Actually the ruling is **רמ״א אורח חיים רפ״א:א in the name of the אור זרוע**, with the MB as secondary codification on the same siman. Reattributed.
- **Uncertain (preserved as-is):** fn6 (Maharsha/Semag two-witnesses derivation on Berachos 14), fn11 (Maharil on kohanim sleeping later Shabbos morning), fn12 (Radvaz teshuvah defending Rav Hai then repudiating — specific siman unlocatable), fn14/fn15 (alternative interpretations of late-Shabbos-davening — no specific attribution), fn26 (David-before-Achish-was-on-Shabbos — no explicit source in standard commentaries).
- **Total:** 3 corrections, 3 confirmations, 6 flags correctly preserved.

### 2026-08-16 — Toledo's שמחתי, Adam HaRishon's Sunrise, and the Nishmas Rebuttal
- **fn9 + body §V (Divrei HaYamim / Dovid HaMelech)** — CORRECTED. Original quoted **"יָדֶיךָ דָּמִים מָלֵאוּ"** attributed to דברי הימים א' כ״ב:ח. That phrase is actually from **ישעיהו א':ט״ו** (Yeshayahu rebuking corrupt worshippers) — wrong pasuk, wrong context. The correct DH I 22:8 pasuk about Dovid reads: **"דָּמִים לָרֹב שָׁפַכְתָּ… לֹא תִבְנֶה בַיִת לִשְׁמִי"**. Replaced both body and fn9.
- **Verified as accurate (no edit needed):** ישעיהו ו':ב (שש כנפים לאחד, fn3); תהילים קכ״ב:א (שמחתי באמרים לי, fn6); תהילים קל״ו:כ״ה (נותן לחם לכל בשר, fn12).
- **Uncertain (preserved as-is):** fn4 (Tur — no specific siman cited); fn5 (Siddur Rabbeinu Shlomo miGarmisa — manuscript-era, appropriate); fn7 (Sefer HaManhig sole-source claim); fn11 (Rav Avraham HaYarchi biographical); fn14 (Napoleon nigun folk attribution); fn17 (Ritva on AZ, exact location); fn20 (Shimon Kefa legend); fn21 (Machzor Vitry — paraphrase acknowledged).
- **Total:** 1 correction, 3 confirmations, 8 flags correctly preserved.

### 2026-08-30 — The Rosh HaShanah Tefillah (Malchiyos, Zichronos, Shofaros)
- **fn4 (Rabba's baraita on the formulas for Malchiyos/Zichronos/Shofaros)** — CORRECTED. Original cited **RH 32a**. The three formulas (`כדי שתמליכוני עליכם`, `כדי שיעלה זכרונכם לפני לטובה`, `ובמה בשופר`) are on **RH ל״ד ע״ב**. Fixed the daf reference.
- **fn5 (R' Akiva vs R' Yochanan ben Nuri machloikes on placement of Malchiyos)** — CORRECTED. Original cited RH 34b. The machloikes is in **Mishnah Rosh HaShanah 4:5** (appearing on daf 32a in Bavli). Fixed to Mishnah RH 4:5.
- **Verified as accurate (no edit needed):** Mishnah RH 4:5 (fn3); RH 32a on ten pesukim per section (fn7); RH 16b on three sefarim / תלויים ועומדים (fn10); RH 32b on no Hallel (fn12); Nechemiah 8:10 (fn13); Tehillim 2:11 (fn15); Avos 1:14 (fn17).
- **Uncertain (preserved as-is per policy — chassidishe/oral/off-Sefaria):** fn1 (Nadvorna Rebbe story); fn2 (Amnon of Mainz / ונתנה תוקף authorship); fn6 (Yerushalmi RH 4:6 regional practice); fn8 (Rav's introductions specific attribution); fn9 (Chaslavich Kroining Nacht from Rav Soloveitchik); fn11 (R' Chaim Shmuel Levit noose formulation); fn14 (Pri Chadash mishloach manos on RH — specific siman); fn16 (Zohar 3:101a); fn18 (Michtav MeEliyahu specific volume); fn19 (Reb Zusha/Reb Elimelech story).
- **Total:** 2 corrections, 7 confirmations, 10 flags correctly preserved.

### Retroactive-pass summary
- **6 real citation corrections applied** across the 4 shiurim
- **~13 references confirmed as accurate** (upgraded from note-academic to verified)
- **~25 flags correctly preserved as uncertain** (chassidishe maasiyos, oral mesorah, sources not indexed on Sefaria)
- **Modified files pushed to `Rabbi-Efratti-Shiurim` repo:** commit `5f713ad` (shiur HTMLs + DOCXs)
- **Sefer Edition rewrites propagated in a separate pass** — same day, pushed to `mm-workroom` repo.

---

## Retroactive backfill pass — Sefer Edition shiurim (Batches 1-5, ran 2026-09-06)

Full Sefaria verification pass on all 25 backfill shiurim originally processed before verification was baked into the pipeline. Sefaria verification is now the 4th agent in the Sefer Edition pipeline (see `sefer_edition_project.md`), so future batches include it inline.

### Batch 1 — 2024-06-23 through 2024-08-13

#### 2024-06-23 — Ana B'Ko'ach
- **Total:** 0 corrections, 0 confirmations, 1 preserved (kabbalistic mesorah).

#### 2024-07-04 — Nishmas Kol Chai
- **fnX (Kiddushin)** — CORRECTED. Original cited Kiddushin 69b; correct daf is **Kiddushin 69a**.
- **fnY (Shir HaShirim Rabbah)** — CORRECTED. Original cited SHR 2:23; correct location is **Shir HaShirim Rabbah 2:9**.
- **Total:** 2 corrections, 14 confirmations, 0 preserved. Modified: both original + Sefer Edition.

#### 2024-08-04 — Sof Pesukei D'Zimra
- **Total:** 0 corrections, 4 confirmations, 0 preserved.

#### 2024-08-11 — [shiur]
- **Total:** 0 corrections, 4 confirmations, 0 preserved.

#### 2024-08-13 — [shiur]
- **fnZ (Yirmiyahu pasuk range)** — CORRECTED. Original cited Yirmiyahu 31:15-16; correct range is **31:15-17**.
- **Total:** 1 correction, 6 confirmations, 0 preserved. Modified: both files.

### Batch 2 — 2024-08-18 through 2024-09-08

#### 2024-08-18 — מִזְמוֹר לְתוֹדָה · צִיצִית · יְהִי כְבוֹד · אַשְׁרֵי
- **Total:** 0 corrections, 0 confirmations, 4 preserved (Rimzei Elul obscure sefer, Aderes biography, Vilna Gaon oral hagiographic, Friedlander forgery-history).

#### 2024-08-25 — אַשְׁרֵי — פֶּתַח לְעוֹלָם הַבָּא
- **Total:** 0 corrections, 8 confirmations (Berachos 4b muvtach, Berachos 32b chassidim harishonim, all Tehillim pesukim, Shemos 15:19), 12 preserved (Rishonim/Acharonim/halachic citations not directly re-checked).

#### 2024-09-01 — סוֹף פְּסוּקֵי דְּזִמְרָה
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2024-09-02 — אֱמוּנָה בְּבִיאַת הַמָּשִׁיחַ
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2024-09-08 — אָז יָשִׁיר · יִשְׁתַּבַּח · כִּסֵּא שְׁלֹמֹה הַמֶּלֶךְ
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

### Batch 3 — 2024-09-22 through 2025-01-01

#### 2024-09-22 — בָּרְכוּ — מקורות, כח ומעשה
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2024-09-29 — סְלִיחוֹת — חסד ואמת לפני יום הדין
- **fn1 (Brisker Rav mashal)** — PRESERVED. Oral Brisker drashos; not on Sefaria.
- **Total:** 0 corrections, 0 confirmations, 1 preserved.

#### 2024-12-25 — כֵּיצַד נַעֲשׂוּ הַחַשְׁמוֹנָאִים לִמְלָכִים
- **Total:** 0 corrections, 0 confirmations, 0 preserved (already integrated prior editorial corrections; no note-academic flags remaining).

#### 2024-12-29 — בָּרוּךְ שֵׁם כְּבוֹד מַלְכוּתוֹ לְעוֹלָם וָעֶד
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2025-01-01 — מַדּוּעַ אֵין מַסֶּכֶת חֲנוּכָּה
- **Total:** 0 corrections, 0 confirmations, 5 preserved (Apter Rav oral; Chasam Sofer via Chut HaMeshulash indirect; Cassius Dio; Engelman modern critical edition; Bircas HaShalom Chassidic).

### Batch 4 — 2025-01-05 through 2025-02-09

#### 2025-01-05 — יְדִיד נֶפֶשׁ
- **Total:** 0 corrections, 0 confirmations, 4 preserved (Sefer HaMefoar digital archive, Elazar Azkari autograph MS at JTS, Tzfas mekubalim oral, Prague museum artifacts).

#### 2025-01-12 — Seder Kriat Shema and Its Halachot
- **fn22/fn23 (Mahar"i Beirav biography)** — VERIFIED. Dates 1474–1546, Spain→Fez→Tlemçen→Safed, 1538 semichah renewal opposed by Ralbach, ordained Beis Yosef→Alshich→Chaim Vital confirmed.
- **fn28 (Rashbash / HaMagdef)** — UNCERTAIN. HaLevi/HaLorki relationship is "friend/correspondent" per JE, not clearly formal teacher; preserved as-is.
- **Total:** 0 corrections, 2 confirmations, 1 preserved.

#### 2025-01-26 — The Hidden History of Birkat Emet V'Yatziv
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2025-02-02 — Birkat Emet V'Yatziv — Origins, Nusach, Semichat Geulah
- **fn10 (Rav Yaakov Moshe Charlap bio)** — VERIFIED. 1882–1951, Mercaz HaRav, talmid muvhak of Rav Kook, Mei Marom, connection to R' Yehoshua Leib Diskin's beis din confirmed.
- **Total:** 0 corrections, 1 confirmation, 0 preserved.

#### 2025-02-09 — The Origins and Development of Shemoneh Esrei
- **fn4 (Prof. Avraham Ofir Shemesh academic)** — PRESERVED. Non-Sefaria academic source.
- **Total:** 0 corrections, 0 confirmations, 1 preserved.

### Batch 5 — 2025-02-16 through 2025-03-16

#### 2025-02-16 — The Origins of Shemoneh Esrei — Words of the Malachim
- **Total:** 0 corrections, 0 confirmations, 0 preserved (no flags).

#### 2025-02-23 — The Three-Part Structure of Shemoneh Esrei and Birkat Avot
- **fn5 (Ketzos HaChoshen / Terumas HaDeshen brotherly pair + Vilna Gaon haskamah)** — CORRECTED. There is no 18th-century Terumas HaDeshen by a Heller brother; Aryeh Leib's elder brother Yehuda Kahana Heller authored **Kuntras HaSfeikos** (customarily printed with Ketzos). Terumas HaDeshen (at fn4) is the medieval R' Yisrael Isserlein. The Gra all-night-haskamah anecdote could not be verified; removed. Note rewritten.
- **fn16 (Sadigura Rebbe)** — PRESERVED. Oral Chassidic.
- **Total:** 1 correction, 0 confirmations, 1 preserved. Modified: original file.

#### 2025-03-02 — Repetition of Words in Chazanus
- **fn15 (Leon of Modena — Sur MeRa / anti-gambling dialogue)** — UNCERTAIN. Core biographical claims verified (age 13, Amsterdam 1692, Eldad/Meidad from Bamidbar 11); "סוד ישרים" alternate title unverifiable via Sefaria (Sefaria doesn't host the work). Preserved as flagged.
- **Total:** 0 corrections, 0 confirmations, 1 preserved.

#### 2025-03-09 — Purim Falling on Erev Shabbos Kodesh
- **Total:** 0 corrections, 0 confirmations, 7 preserved (RZNG private letter, Gur Imrei Emes oral, kabbalistic Arizal without specific locus, x2 in Sefer Edition).

#### 2025-03-16 — Magen Avraham — The Soul of the First Berachah
- **fn23 Sefer Edition (Rema on shituf)** — CORRECTED. Original cited "Rema, Choshen Mishpat 425" (capital cases). The Rema's shituf ruling is at **Orach Chaim 156**. Fixed.
- **fn17 (Ramban / chazir drasha)** — UNCERTAIN preserved; classical printed source is Or HaChaim on Vayikra 11:7, "shem chazir" drasha circulates without clean rishonic pin.
- **Others (Etz HaDa'as Tov, Rav Baruch Ber oral, Mateh Tov kavvanah)** — PRESERVED.
- **Total:** 1 correction, 0 confirmations, 4 preserved. Modified: Sefer Edition file.

### Backfill-pass summary
- **4 real citation corrections applied** across the 25 shiurim (2 in 2024-07-04, 1 in 2024-08-13, 1 in 2025-02-23, 1 in 2025-03-16 = 5 individual fixes across 4 shiurim)
- **~29 references confirmed as accurate**
- **~45 flags correctly preserved as uncertain** (chassidishe/oral/off-Sefaria/academic-secondary)
- **~9 of 25 shiurim had zero note-academic flags** (Sefer Edition rewrites had already stripped them)
- Sefaria verification now baked into Sefer Edition pipeline as 4th agent for all future batches

---

## Weekly entries (going forward)

New entries added each Sunday by the automated scheduled task. Format for each week:

```
### YYYY-MM-DD — [Shiur title]
- **fnN (topic)** — CORRECTED / VERIFIED / UNCERTAIN. [detail]
- **Total:** X corrections, Y confirmations, Z flags preserved.
```

### 2026-09-06 — The Final Mincha, אֲחוֹת קְטַנָּה, and the Chofetz Chaim's Primordial Oath
- **fn1 (Berakhot 12a, hakol holech achar hachitum)** — VERIFIED. Gemara at 12a explicitly.
- **fn5 (Megillah 31b, tikhleh shanah)** — VERIFIED verbatim (Abaye / Reish Lakish).
- **fn8 (Tehillim 24:3-4)** — VERIFIED verbatim.
- **fn9 (Niddah 30b, mashbi'in oso / tehi tzaddik)** — VERIFIED. R' Simlai drasha with all elements.
- **fn10 (Chofetz Chaim application to Ps 24)** — CORRECTED/TIGHTENED. Niddah 30b itself explicitly cites Ps 24:4 as the pasuk describing one who kept the oath — flag rewritten to note the linkage is in Chazal; Chofetz Chaim's chiddush is the practical Rosh HaShanah avodah drawn out.
- **fn12 (Devarim 20:8; Sotah 44a)** — VERIFIED both. Pasuk + R' Yosei HaGelili's mei-averos she-b'yado.
- **fn15 (Berakhot 34a — no bakashos)** — VERIFIED verbatim. SA OC 112:1 also verified — communal bakashos ARE permitted, supporting the first teretz in the shiur.
- **fn20 (SA OC 582:5, forgot Zochreinu)** — VERIFIED.
- **fn21 (Taanit 25b, R' Akiva)** — VERIFIED verbatim.
- **fn24 (II Samuel 6:14/16, David mekharker)** — VERIFIED (v.14 mekharker, v.16 mefazez u-mekharker).
- **Preserved as UNCERTAIN** (out of scope: chassidishe/oral/kabbalistic/non-Sefaria): fn2, fn3, fn4, fn6, fn7, fn11, fn13, fn14, fn16, fn17, fn18, fn19, fn22, fn23.
- **Total:** 1 correction/tightening, 11 confirmations, 13 preserved. Modified: original shiur HTML.

---

*Weekly entries continue below.*

---

## Retroactive backfill pass — Batch 6 (ran 2026-09-06)

Verified inline during 4-agent Sefer Edition pipeline (Sefaria verify integrated as agent #3, per updated pipeline).

### 2025-03-23 — HaKel HaGadol HaGibor v'HaNorah, the Two Bows, and Birkat Gevurot
- **Sefaria pass:** 0 corrections, 1 verification (Yoma 69b sugya of Yirmiyahu/Daniel/Anshei Knesses HaGedolah verbatim confirmed), 3 preserved (Satanov historical, R' Aharon Kotler oral mesorah, Rav Fisher/Rav Auerbach oral teshuvos).

### 2025-03-30 — Kedushah — The Daily Mitzvah of Kiddush Hashem
- **Sefaria pass:** 0 corrections, 0 verifications, 5 preserved (all historical/biographical: First Crusade, ShUM, Saadia–Ben Meir calendar dispute, Rabbeinu Kalonymus HaZakein, Rav Pirkoi ben Baboi).

### 2025-04-06 — Preparing for Pesach — Bedikat Chametz and Bi'ur Chametz
- **Sefaria pass:** 0 corrections, 0 verifications, 2 preserved (mechiras chametz historical development, R' Itzele Charif anecdote).

### 2025-05-04 — Atah Kadosh, the Kuzari, and Atah Chonen
- **Sefaria pass:** 0 corrections, 2 spot-verifications (Nedarim 41a; Rashi on Vayikra 19:2), 6 preserved (Kuzari, Cairo Genizah, Raavad, Rizhiner, Rav Yonah of Vizhnitz, Rav Avli Posweller, Nieto/Breuer).

### 2025-05-18 — Atah Chonen, Hashiveinu, and the Path of Teshuvah
- **Sefaria pass:** 0 corrections, 0 verifications, 4 preserved (Rabbi Ephraim Zalman Margolios bio, Cairo Genizah manuscript recovery, Rav Noach Weinberg bio, Bobover Rebbe's oral pre-Holocaust account).

### Batch 6 summary
- 0 corrections, 3 verifications, 20 preserved (all correctly per skip-rule: chassidishe/oral/biographical/non-Sefaria).

---

## Weekly entry — 2026-09-07 (extra Monday shiur, Labor Day)

### 2026-09-07 — Kaf-Hei Elul, Rosh HaShanah on Shabbos, and the Piyutim Machloikes
- **fn1 (RH 11a, R' Eliezer בתשרי נברא העולם)** — VERIFIED.
- **fn2 (Rashi Bereishis 1:1, בשביל ישראל)** — VERIFIED (BR 1:4 + VR 36:4).
- **fn3 (Nechemiah 6:15, 52 days כ"ה אלול)** — VERIFIED verbatim.
- **fn5 (R' Akiva Ta'anit 25b)** — VERIFIED.
- **fn6 (SA OC 288:1 fasting on Shabbos)** — VERIFIED.
- **fn7 (SA OC 89:3 no eating before davening)** — VERIFIED.
- **fn9 (SA OC 288:2 area on crying on Shabbos)** — VERIFIED.
- **fn12 (SA OC 583:2 sleeping on RH)** — VERIFIED locus (formulation quoted is really MB/MA on the siman).
- **fn14 (MB 583)** — VERIFIED locus.
- **fn16 (SA OC 592:3 hefsek by shofar)** — VERIFIED.
- **fn17 (SA YD 228 hataras nedarim)** — VERIFIED.
- **fn18 (מסירת מודעא)** — **CORRECTED** from YD 210:5 → **SA YD 211:1-2** (211 has the "כל הנדרים שאני עתיד לידור" formula with Rama attaching to Kol Nidrei; 210 is on aligning heart/lips + dream vows).
- **fn22 (Rosh via Tur OC 68)** — VERIFIED.
- **Preserved UNCERTAIN** (chassidishe/kabbalistic/oral/non-Sefaria): fn4 (Zohar end of Balak, כ"ה אלול), fn8 (modern coffee psak), fn10 (Arizal on RH tears), fn11 (Reishis Chochma), fn13 (Arizal/Gra sleep after חצות), fn15 (Arizal Ps. 47 x7), fn19 (chassidishe minhag המלך הקדוש), fn20 (piyutim gzeiros framing), fn21 (Rav Hai teshuvah locus), fn23 (Gra מעשה רב), fn24 (Maharil), fn25 (הקליר legends).
- **Total:** 1 correction (fn18 YD 210→211), 10 confirmations, 14 preserved. Modified: original shiur HTML.

---

## Backfill entry — 2025-07-27 (Batch 8, run 2026-10-05)

### 2025-07-27 — Tefillat Nachem and Modim
Method note: the two note-academic flags (fn15 Shlomo Simchi, fn16 R' Yonasan Eibeschutz) are in skip-domains (modern composer; oral/chassidishe maaseh) and were left UNCERTAIN. Because several unflagged standard-canon citations carried material errors, they were also spot-checked via mcp__workspace__web_fetch and corrected in place.
- **fn1 (Yerushalmi Berachos 4:3, Rav Muna rule)** — VERIFIED (R' Avdima d'Tzipori asks R' Mana; rule quoted). Name corrected Avdimi -> **Avdima** (דצפורין); parallel **Yerushalmi Taanis 2:2** added, where R' Mana cites the rule in the name of Rav Yirmiyah in the name of Rav.
- **fn2 (Rav Saadia, "ein hefsed b'amiraso")** — UNCERTAIN; phrase not located. Beis Yosef OC 557 (citing Abudraham) records Rav Saadia as saying Nachem only at Mincha. Flag added; claim left.
- **fn3 (AZ 7b-8a me'ein ha-bracha)** — **CORRECTED** to **AZ 8a** (Rav Yehuda b. Shmuel b. Sheilat in the name of Rav), via Beis Yosef OC 557.
- **fn4 (Rif, Taanis)** — VERIFIED (Rif and Rosh at end of Taanis, per Beis Yosef/Taz).
- **fn5 (Tur and Taz: forgot -> Shema Koleinu)** — **CORRECTED**: this is the **Taz's own ruling** (557:1, "ולענ"ד", no menachem Tziyon chasimah); the Tur does not give it. Body text adjusted; Beis Yosef's Hoda'ah (R' Gershom) noted.
- **fn6 (SA OC 557 / Rama)** — VERIFIED locus; **CORRECTED** characterization: Mechaber's wording is unqualified; Rama's gloss cites **Rokeach and Avudraham** (and Maharil: one who ate says Nachem in Birkas HaMazon).
- **fn7 (Yirmeyahu 52:12-13; Melachim II 25:8-9)** — VERIFIED. Body corrected: Nevuchadnezzar -> **Nevuzaradan** (servant of N.) as the agent.
- **fn8 (Taanis 29a process)** — **CORRECTED**: fire set on the ninth **סמוך לחשכה** (near nightfall), not "after midday"; seventh and eighth = eating/desecration (ואכלו וקלקלו בו). "אוכלין ושותין ומקרקרין" is the speaker's paraphrase, not Gemara. Restraint into the tenth is not in this passage (flag added).
- **fn9 (R' Yochanan, Taanis 29a)** — VERIFIED verbatim.
- **fn10 (BK 22a-23a, chitzav/mamono)** — VERIFIED for 22a.
- **fn11 (BK 16a, spine/snake)** — VERIFIED locus; **CORRECTED** quote to actual baraisa text (שדרו של אדם לאחר שבע שנים נעשה נחש, והני מילי דלא כרע במודים).
- **fn12 (Tosafos BK 16a, luz bone)** — **CORRECTED**: main Tosafos = middah k'neged middah (Rav Sheishes, Berachos 12b); the luz-bone proposal and its rejection appear in the printed **גליון** ("ויש מפרשים"), not in Tosafos proper. Body and note revised.
- **fn13 (Tehillim 35:10)** — VERIFIED (text via Yerushalmi Berachos 4:3, R' Simon: bowing through all vertebrae); parallel added.
- **fn14 (MB 113)** — SA OC 113:7 VERIFIED (כורע בברוך, זוקף בשם); MB back-condition wording UNCERTAIN, flag added.
- **fn15, fn16** — UNCERTAIN, preserved (skip-rule: modern composer; chassidishe/oral maaseh).
- **Total:** 8 corrections (fn1 name, fn3, fn5, fn6, fn7/body, fn8, fn11, fn12), 6 confirmations (fn1 locus, fn4, fn9, fn10, fn13, fn14 SA), 4 preserved/flagged (fn2, fn14 MB, fn15, fn16). Modified: final MM/2025-07-27 — Tefillat Nachem and Modim.html.

### 2025-07-31 — Al Naharot Bavel — A Study of Tehillim 137
- **fn1 (Malbim on Tehillim 137:1, 2, 7, 8)** — VERIFIED (settled/Jer 29:5; aravim as sweet; gemul as act from love/hatred). **CORRECTED** characterization: gemul repaid "b'sinah v'nekamah" (not "rather than vengeance"); the "aru aru ad hayesod" inner-yesod reading is the speaker's extension (Malbim 137:7: Edom aided the destruction). Noted: Malbim dates the mizmor to year 1 after Koresh.
- **fn4 (Yirmiyahu 29:5-7)** — VERIFIED. Midrash Eichah (atrocities) — UNCERTAIN, not located, preserved.
- **fn5 (Radak 137:2)** — VERIFIED.
- **fn6 (Alshich)** — UNCERTAIN (not located on Sefaria; aphoristic wording may be the speaker's); preserved.
- **fn7 (Midrash Tehillim 137)** — VERIFIED march/ship/loads/tohu vavohu/angels/mashal/thumbs/tilei tilim. **CORRECTED** body + note: "tanchumin shel hevel ... al tachishu" is not the midrash; actual: "תנחומין הללו שאתם מנחמים אותי ניאוצין הן לפני" + Yeshayahu 22:4 "אל תאיצו לנחמני"; queen's retort "ריקה" (not ריקן); verse glossed is "ותוללינו שמחה" (not "ושואלינו"); loads were sand-filled sacks made of books (not "stones"). "ומקרקרין" not found in this midrash (speaker's gloss).
- **fn8 (BB 60b)** — VERIFIED locus, R. Yehoshua, "ein gozrin gezeirah", afar mikleh on chasan. **CORRECTED** list: bread (menachos), fruit (bikkurim), water (nisuch hamayim) → silent; oil/chavitei kohen gadol is not in the passage.
- **fn9 (SA OC 1)** — SA OC 1:3 VERIFIED for the general churban-grief obligation; **CORRECTED**: the Al Naharos Bavel minhag is MB 1:11 citing the Shelah ("at every meal"; Shir HaMaalos on Shabbos and no-Tachanun days), not the Mechaber. Body adjusted.
- **fn10 (Perfidy)** — skip-rule (modern work); preserved, flag kept.
- **fn11 (Kotel 1967)** — skip-rule (oral/modern); preserved. Added note: "Har HaBayis b'yadeinu" is conventionally attributed to Mota Gur, Rav Goren blew the shofar.
- **fn2 (Simchas Torah 5784)** — skip-rule (speaker's own); preserved.
- **Total:** 6 corrections (fn1 characterization, fn7 quote/retort/verse/loads, fn8 foods, fn9 source, plus fn11 attribution note), 5 confirmations (fn1, fn4, fn5, fn7, fn8), 4 preserved/flagged (Alshich, Eichah, Perfidy, Kotel). Modified: final MM/2025-07-31 — Al Naharot Bavel — A Study of Tehillim 137.html.

---

## Backfill entry — 2025-07-20 (Batch 8, run 2026-10-05)

### 2025-07-20 — Shema Koleinu: The Culmination of Our Petitions
Method note: mcp__workspace__web_fetch against Sefaria (texts API). Aruch HaShulchan, Bach, Iyun Tefillah and Zohar were not retrievable and were left UNCERTAIN (flags added). Corrections applied in place to the final MM HTML (body + notes); fn19 (Rashi) added.
- **fn1 (Megillah 17b)** — **CORRECTED** to **17b-18a**: Hoshea 3:5 then Yeshayahu 56:7 ("בית תפילתי") are on 18a; body reworded (David comes -> tefillah comes). Tur 119 and Beis Yosef 119:1 give the same rationale.
- **fn2 (Tur OC 118, 1,800)** — locus VERIFIED, **CORRECTED** attribution: the Tur cites the מדרש דורשי רשומות (not the Zohar) in Boneh Yerushalayim, in support of ולירושלים עירך; no mention of אב הרחמן in 118 or 119. The ש-vs-א conclusion is the speaker's application, flagged. Editorial arithmetic: 19 initials = 1,799 (+1 kollel); with א for ש = 1,500.
- **fn3 (Shaar HaKavanos)** — UNCERTAIN (flag added).
- **fn4 (Taanis 25b)** — VERIFIED (before sunrise / after sunset; both meshalim). Gemara's own answer (משיב הרוח / מוריד הגשם) added.
- **fn5 (AZ 7b-8a)** — **CORRECTED** to **8a**; **be'arai/bekviyus is NOT in the Gemara** (removed; attributed to Taz/AH as presented).
- **fn6 (SA OC 119)** — VERIFIED 119:1-2 (Rabbeinu Yonah, Rama); MB 119:4 viduy/parnasah verified; "majority permits daily" unverified, flagged.
- **fn7 (Taz 119)** — UNCERTAIN: 119:1 has Rabbeinu Yonah's four categories and "בקשה שלו תהיה טפילה", but no be'arai/bekviyus prohibition located.
- **fn8 (MB 119)** — **CORRECTED**: verified s"k 3, 4, 12; the Taz-machloket description and the Kedusha warning not located in 119 (cross-ref siman 122), flagged.
- **fn9 (AH 119)**, **fn13 (Bach)**, **fn11 (Iyun Tefillah)**, **fn14 (Zohar: 1,800 / Rav Yeiva Saba)** — UNCERTAIN; Zohar Vayishlach locus for specifying the sin found via MB 119:2 (Pri Chadash).
- **fn10 (Yaavetz/Landsofer)** — UNCERTAIN; caution added (Yaavetz = Altona/Emden; Prague drasha points to Landsofer).
- **fn12 (Tehillim 37:25)** — VERIFIED.
- **fn19 (new, Rashi Bereishis 30:8)** — **CORRECTED**: "חיבור" is Menachem ben Saruk's reading cited by Rashi; Rashi's own is persistent wrestling (נתעקשתי והפצרתי).
- **Preserved UNCERTAIN (non-Sefaria):** fn15 (R' Yaakov Yosef), fn16 (Brisker Rav), fn17 (Baal Shem Tov), fn18 (R' Schorr); Editorial: "השיבנו בחיים / בא נשלום" possible transcription artifacts (noted in Sefer Edition).
- **Total:** 5 corrections (fn1, fn2 attribution, fn5, fn8, Rashi), 5 confirmations (fn4, fn6 SA, fn12, MB 119:4, Megillah verses), ~12 preserved/flagged. Modified: final MM/2025-07-20 — Shema Koleinu — The Culmination of Our Petitions.html. Sefer Edition: book-rewrites/2025-07-20 — Shema Koleinu — The Culmination of Our Petitions — Sefer Edition.html.

---

## Backfill entry — 2025-08-24 (Batch 8, run 2026-10-05)

### 2025-08-24 — Birkat Modim and Nesias Kapayim
Method note: mcp__workspace__web_fetch against Sefaria (texts API; search-wrapper returned "Unsupported HTTP method" and was not usable). Corrections applied in place to the final MM HTML (body + notes). Ran/Ri Migash, Yerushalmi, Torat Chaim, Beis Yosef, Mishnah Berurah, Avudraham were not retrievable and left UNCERTAIN.
- **fn1 (Sotah 40a, Modim DeRabbanan)** — VERIFIED locus and Rav Pappa's "recite all of them". **CORRECTED** list of formulators: Rav, Shmuel, R. Simai, the sages of Neharde'a in his name, Rav Acha bar Yaakov (not R. Shimon bar Menasya). "ברוך א-ל ההודאות" / "אתה הוא ה' אלהינו" are siddur composite wording, not attributed to individual amoraim in the sugya; body line 104 corrected to the actual Rav / Shmuel formulations.
- **fn2 (Yerushalmi Berachos 2:4, body bows)** — UNCERTAIN (not located); flag added.
- **fn3 (Torat Chaim; Tehillim 150:6)** — UNCERTAIN (Torat Chaim not located); flag added.
- **fn4 (Vayikra Rabbah 9:7)** — VERIFIED (R. Pinchas / R. Levi / R. Yochanan in name of R. Menachem of Galya; korbanos and tefillos/hoda'ah). **CORRECTED** SA locus: **OC 51:9** (all *songs* batel except Mizmor LeTodah, hence said to a melody), not korbanos/tefillos; body adjusted. "Modim" = hoda'ah is the speaker's application.
- **fn5 (Ran, "al she'anu modim lach")** — UNCERTAIN: recording reads "...megash" (Ri Migash?), not located on Sefaria; flag added.
- **fn6 (Rambam SM Aseh 26; Chinuch 378)** — VERIFIED. **CORRECTED**: "בכל מקום, בכל זמן, בכל יום" is not the Chinuch's wording (practiced every day and at all times; body/notes changed to בכל יום ובכל זמן); the "three mitzvos aseh" are R. Yehoshua ben Levi, **Sotah 38b** (non-ascending kohen transgresses three), not the Chinuch; speaker's "fulfills three" is the converse.
- **fn7 (Rambam, Hil. Tefillah ch. 15)** — **CORRECTED** to **ch. 14:1-2** (no nesias kapayim at Mincha: people already ate, perhaps wine, a drunk may not duchen; fast-day Mincha decree; Mincha near sunset like Ne'ilah). Rambam does not call it avodah here; avodah = Sotah 38b.
- **fn8 (Mishnah Tamid 5:1, 7)** — VERIFIED / **CORRECTED**: Tamid 5:1 = three blessings incl. Birkas Kohanim as prayer (Lishkas HaGazis); Tamid **7:2** = kohanim on the Ulam steps, one blessing in the Mikdash, Name as written, hands above head. "Baalei maamados in the azarah" not in these mishnayos (removed; speaker was hedging). Body quote "וידבר ה' אל משה... ויברך את העם" replaced by **Vayikra 9:22** (וישא אהרן את ידיו אל העם ויברכם), the Sotah 38b source for avodah.
- **fn9 (Rema OC 128:44)** — VERIFIED (Ashkenaz custom, Yom Tov only, only at Musaf; livelihood on Shabbos too; Yom Kippur incl. Ne'ilah/Shacharis in some places). **CORRECTED**: Hebrew "quote" was a paraphrase (removed); dibbur/machshavah (Yeshayahu 58:13) is the speaker's elaboration, not in the Rema. "נשבת גמר" (Editorial) not recoverable; omitted in Sefer Edition.
- **fn10 (Beis Yosef 128)** — UNCERTAIN (not retrieved); Aruch HaShulchan 128:64 verifies daily duchening in EY, Egypt, Asia.
- **fn11 (Aruch HaShulchan OC 128)** — locus pinned to **128:64**, VERIFIED "כאילו בת קול יצא שלא להניח לנו לישא כפים". **CORRECTED**: AH records an unnamed tradition ("ומקובלני") of **two** great men of earlier generations, each in his own place; he names neither the Gra nor Reb Chaim and mentions no jail or fire (those are the speaker's/oral tradition; flag added). Body re-worded.
- **fn12 (Lubavitcher Rebbe sicha on Baal HaTanya)**, **fn15 (9/11 beis din)**, **fn16 (Rav Noach Shimonowitz)**, **fn18 (Baal Shem Tov families)**, **fn19 (Rav Elyashiv)**, **fn20 (Pinsk)** — skip-rule (oral/modern/chassidish); preserved, flags kept. fn15 flag extended per Editorial (roster/page count unverified).
- **fn13/fn14 (Sheilas Margolios; Rav Frank)** — **CORRECTED** attribution per the recording (Shiur Review): **R' Efraim Zalman Margolios (of Brody)**, not Rabbi Reuven Margoliot; body "Rabbi Margoliot" changed. Title/work not located on Sefaria: UNCERTAIN, flag added.
- **Body (Editorial)**: garbled "שטעט יקי" resolved from recording ("a yekish shtot, a German city") to יעקישע שטאט.
- **Total:** 9 corrections (fn1, fn4 SA locus, fn6, fn7, fn8, fn9, fn11, fn13/14 author, body Yekkish), 5 confirmations (fn1 locus, fn4 VR, fn6 Rambam/Chinuch, fn9 Rema, fn11 AH quote), ~11 preserved/flagged. Modified: final MM/2025-08-24 — Birkat Modim and Nesias Kapayim.html. Sefer Edition: book-rewrites/2025-08-24 — Birkat Modim and Nesias Kapayim — Sefer Edition.html.


---

## Backfill entries — Batch 7 (ran 2026-10-05; Sefaria pass completed earlier in session)

### 2025-05-25 — Refaeinu and Barech Aleinu
- **CORRECTED**: Megillah 17a → **17b**; Maharam captivity numbers corrected. Modified: final MM/2025-05-25 html.

### 2025-05-26 — Mitzvat Yishuv Eretz Yisrael
- Rambam Melachim/Ishus citations pinned; shalosh shevuos added; Megillas Esther author resolved. No flags found.

### 2025-06-15 — Teka B'Shofar in a Time of War
- **CORRECTED**: fn3, fn7 (Chazon Ish → Chofetz Chaim at Mir), fn10, Hebrew agreement. Pirkei d'R. Eliezer 31 / Megillah 17b VERIFIED. Modified: final MM/2025-06-15 html.

### 2025-06-22 — Hashivah Shofteinu and Birkat HaMinim
- **FLAGGED**: fn14 Yerushalmi Sukkah vs. Sotah 9:13 possible miscitation (warrants final pin).

### 2025-06-29 — Birkat HaMinim and Birkat Al HaTzaddikim
- **FLAGGED**: fn25 Terumot 1:1 vs. Chagigah 3:1; fn7 Tehillim 75:11 variant (warrants final pin).

## Backfill entry — 2025-07-06 (Batch 8, run 2026-10-05)

### 2025-07-06 — Birkat Yerushalayim and Tzemach David
- **fn3 (Tur OC 118)** — VERIFIED; 1,800 count is the darshei reshumos', not Zohar; removed unconfirmed "siman 236".
- **fn7 (Tosefta Berakhot 3:25)** — **CORRECTED**: only David+Jerusalem combination permitted; Yerushalmi tightened to 4:3; unsupported "later split" dropped.
- **fn12 (Yoma 10a)** — VERIFIED (Rome/Persia dispute); Megillah 6 parallel dropped.
- **fn13 (Sanhedrin 98b)** — **CORRECTED**: Menachem is a "some say" opinion, not a school.
- Confirmed: Megillah 17b, Pesachim 54a. Not re-fetched: fn15 Shabbat 31a.
- **UNCERTAIN (non-Sefaria)**: fn6, 11, 17, 21, 22 (Rashi Taanis/third Mikdash, Vital cave, Gra kavanah, acrostic, Hirsch quote). Sefer Edition: Hirsch childhood example attributed to Rav Schwab (Hirsch d. 1888) — editorial note.
