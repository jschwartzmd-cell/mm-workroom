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


---

## 2026-10-11 — Nishmas Kol Chai — Layers, Legends, and the Question of Authorship

- **fn2 (Pesachim 117b/118a)** — **VERIFIED** amud split (mishnah on the fourth cup 117b; "מאי ברכת השיר" 118a). **CORRECTED/pinned**: Nishmas is Rabbi Yochanan's answer, Yehalelucha is Rav Yehuda's; wording added to note.
- **fn3 (Berachos 59)** — **CORRECTED**: 59a → **59b**. The phrase is Rabbi Yochanan's closing of the rain thanksgiving ("אילו פינו מלא שירה כים וכו'", Gemara has no initial vav); Rav Yehuda's formula is "מודים אנחנו לך על כל טיפה וטיפה". 59a (thunder/lightning) lacks it. Body: "(59b ...)" added.
- **fn4 (Berachos 60b)** — **VERIFIED**: מתיר אסורים, זוקף כפופים, פוקח עורים, מלביש ערומים, המעביר חבלי שינה מעיני are there; המשיח אלמים / המפענח נעלמים / סומך נופלים are not in the Gemara's list (noted).
- **fn9 (Bereishis 25:21)** — **VERIFIED** verse text added.
- **fn10 (Berachos 26b; Bereishis 24:63)** — **VERIFIED** (baraita supporting R. Yosei b. R. Chanina; Avraham/Yitzchak/Yaakov with verses). **Machzor Vitry located**: Order of Shabbat §161 "פתרון נשמת" (as numbered on Sefaria): "וכתוב בו יצחק ורבקה ... אין עניין יצחק ורבקה לכאן ... דהא יצחק אבינו תיקן תפילת המנחה". **UNCERTAIN**: the Rav's "later couple" conclusion is not in that text (body now says "as the Rav reports it").
- **fn14 (Avos 1; Berachos 48a)** — **VERIFIED** Avos 1:6/1:8/1:10 pairs; Berachos 48a (Yannai, מלכתא, "שמעון בן שטח אחוה"). **CORRECTED** note: the Gemara does not name the queen Shlomtzion or the king "Alexander Jannaeus".
- **fn17 (Shulchan Aruch OC 580)** — **CORRECTED**: locus is **580:2**; wording is "לא נודע איזה היא הצרה שאירע בו", not "ולא נודע על מה" (header + body fixed); no Rema/Ezra/Shimon Kipa in that text. Baruch Ta'am gloss not on Sefaria: UNCERTAIN.
- **fn1 (SA/Mishnah Berurah OC 52)** — SA 52 is a single se'if (with Rema). **VERIFIED** MB 52:5 (Shabbos: obligated in Nishmas; minimum "ב"ש ותהלה לדוד ונשמת וישתבח") and 52:6. **UNCERTAIN**: "must say Nishmas after davening" not found in MB 52 (52:9 = Torah blessings/אלהי נשמה); flag kept and extended; body prefaced "According to the Rav".
- **fn23 (Beitzah 16a; Taanis 27b)** — **CORRECTED** quote: Beitzah 16a (Resh Lakish) "נשמה יתירה נותן הקדוש ברוך הוא באדם ערב שבת, ולמוצאי שבת נוטלין אותה הימנו"; Taanis 27b "נשמה יתירה ניתנה בו באדם בערב שבת". Old quote ("ניתנה לאדם בערב שבת") was a hybrid.
- **fn24 (Tur OC 281; Devarim 5:15)** — **CORRECTED/located**: Tur OC 281 "ואחר השירה מוסיפין נשמת שיש בו מענין יציאת מצרים, לכך סמכוהו אצל השירה וחותמין בישתבח": the Tur ties **Nishmas** (not Shabbos) to Yetzias Mitzrayim. Body re-worded; Devarim 5:15 VERIFIED; flag tightened.
- **fn26 (Mishnah Yadayim 3:5)** — **VERIFIED**: Rabbi Akiva, "שכל הכתובים קודש ושיר השירים קודש קדשים"; the Rav's "Gemara" is a Mishnah. Rokeach part not checkable.
- **fn5 (Chida, Simchas HaRegel)** — index **VERIFIED** (Chida, Haggadah commentary, c. 1758-82, Livorno 1782); passage text not retrievable: **UNCERTAIN**.
- **fn28 (Yesod VeShoresh HaAvodah)** — index VERIFIED (R. Alexander Ziskind, c. 1769-81, pub. 1782); Third Gate (שער השיר) = Pesukei DeZimra; Nishmas/simchah passage **UNCERTAIN** (not located).
- **fn18, fn19, fn21, fn22 (Machzor Vitry Peter passage; Sefer Chasidim; Avodah piyut; Nishmas daily)** — **UNCERTAIN**: not located in Sefaria's Machzor Vitry (Order of Shabbat §§155-168, Laws of Shabbat, Order of Yom Kippur §354 has only a rubric "אתה כוננת") nor, for Sefer Chasidim, found; flags extended.
- **Not checkable on Sefaria / skip-rule**: fn6 (Algazi), fn7 (Gaonic siddurim not indexed as texts), fn8, fn11 (Rokeach not indexed), fn12, fn13, fn15, fn16, fn20 (New Testament), fn25, fn27, fn29.
- **Total:** 8 corrections (fn3, fn14 note, fn17, fn23, fn24, fn2 attribution pin, fn1 body attribution, fn10 body attribution), 9 verified (fn2, fn4, fn9, fn10, fn14, fn17 locus, fn23, fn24 Devarim, fn26), ~8 UNCERTAIN, ~12 not checkable/skipped. Modified: final MM/2026-10-11 — Nishmas Kol Chai — Layers, Legends, and the Question of Authorship.html.


### 2026-10-11 addendum — reconciled to Sofer.ai transcript

- **fn25 (Tosafos Pesachim 118a, d"h רבי יוחנן אמר נשמת כל חי)** — **LOCATED/VERIFIED** on Sefaria (Tosafot on Pesachim 118a:1): "וקורא נשמת כל חי ברכת השיר לפי שבשבתות אומרים אותו אחר פסוקי דזמרה"; "רבינו חיים כהן לא היה חותם ביהללוך כי אם בנשמת לבדו". The Rav (Sofer) says "Tosafos in Pesachim" holds it was said in Chazal's time while Gaonic siddurim say only yechidim; **UNCERTAIN/flagged**: the Tosafos text does not say so explicitly (only the Shabbos practice). The Plaud-based attribution (Tosafos = individuals only) was reversed per Sofer.
- **fn3 (Shulchan Aruch OC 221)** — **VERIFIED/added**: the Rav's "a whole siman" = Orach Chaim 221 (ברכת הודאת הגשמים): 221:1 + Rema (custom not to recite today); 221:2 "מודים אנחנו לך ה' אלהינו על כל טפה וטפה". Siman number is the editor's identification (flagged).
- **fn1 (Mishnah Berurah 52:5)** — **RE-CHECKED**: text "עוד כתב דבשבת מחוייב לומר נשמת והיא נקראת [בפסחים קי"ח] ברכת השיר" (the Rav's Pesachim 118 reference matches); still **no** statement that a skipped Nishmas is said after davening. Sofer shows the Rav attributes that to the Mishnah Berurah; flag kept (UNCERTAIN).
- **fn2 (Pesachim)** — pinned to the Rav's own daf: 118a (Sofer: "קי"ח ע"א"); 117b Mishnah remains the editor's.
- **fn4 (Berachos 60b)** — Rav's daf given in Sofer as "ס׳ ס״א" (60-61); content previously VERIFIED at 60b; flag updated, no new text check.
- **fn26 (Yadayim 3:5)** — Sofer: the Rav says "Mishnah" (not "Gemara"); Mishnah previously VERIFIED, wording only.
- **fn6 (Algazi)** — Sefaria search (name API) returned no topic for Yisrael Yaakov Algazi / Yom Tov Algazi: **not checkable**; Sofer: Rav says "the Maharit Algazi's son", name "רב יעקב ישראל אלגאזי"; family relation flagged for verification.
- **fn17 (SA OC 580:2 / Baruch Ta'am)** — no change to the Sefaria text; Sofer shows the Rav's "ולא נודע למה" is a paraphrase and that "מצאתי כתב יד" is the Baruch Ta'am's phrase (not the Rav seeing a manuscript); Baruch Ta'am is father-in-law (not father) of the Tzanzer Rav per the Rav. Gloss still not on Sefaria: UNCERTAIN.
- **Not checkable / unchanged**: fn5, fn7, fn8, fn10-fn16, fn18-fn22 (as in the earlier entry), fn27-fn29. Modified: final MM/2026-10-11 — Nishmas Kol Chai — Layers, Legends, and the Question of Authorship.html.

## Backfill entry — 2025-09-14 (run 2026-10-12)

### 2025-09-14 — Machnisei Rachamim and the Question of Intermediaries
Method note: WebFetch against Sefaria (v3 texts API, name/index APIs; search-wrapper returned "Unsupported HTTP method" and was not usable). Corrections applied in place to the final MM HTML (body + notes). One WebFetch (Nimukei Yosef on Bava Batra 116a, name API) was rate-limited (HTTP 429) and not retried; the Nimukei Yosef text, Mahari Bruna passage, Ramban's Toras Hashem Temimah (not on Sefaria), Maharit Asad (not on Sefaria; Sefaria's "Maharit" is Yosef Trani), Igros Moshe and R. Yaakov bar Yakar's commentary were not located and left UNCERTAIN. No Hebrew twin exists for this date.
- **fn2 (Rambam AZ 2:1–2; Yesodei HaTorah 1:6)** — **CORRECTED**: Dor Enosh is **Hil. Avodah Zarah 1:1** (stars/spheres as servants who minister before Him); AZ **2:1** VERIFIED (essence of the prohibition: serving any creature, angel included, even knowing God is true God); YT 1:6 VERIFIED but is knowledge of God's *existence* (Shemos 20:2) + prohibition of another god (20:3), not "Oneness". Added the actual source of the quoted "ואין לזולתו ראוי להתפלל": 5th principle, Rambam on Mishnah Sanhedrin 10 (Intro to Perek Chelek) — VERIFIED (intermediaries forbidden).
- **fn3 (Yerushalmi Berachos 9:1)** — VERIFIED ("flesh and blood has a protector… cry neither to Michael nor to Gabriel, but to Me, and I shall answer immediately"; only these lines checked).
- **fn4 / fn6 (Ramban, Toras Hashem Temimah)** — UNCERTAIN (not located; derashah not on Sefaria); caveats added: wording is the lecturer's paraphrase; structure/edition details are from the write-up, unverified.
- **fn5 (Shabbos 12b)** — text VERIFIED (R. Yochanan: whoever asks needs in Aramaic, the ministering angels do not attend to him; the sick person is different; same in Sotah 33a). **CORRECTED** characterization: it is not a prohibition of asking angels and not the Ramban's source; the lecturer raised it as a kashya. Body line rewritten accordingly. Cross-ref Sanhedrin 38b (Rav Idit, "do not exchange Me for him") VERIFIED, noted as not cited by the lecturer.
- **fn7 (Chasam Sofer OC 166)** — locus VERIFIED (responsum on Machnisei Rachamim, addressed to R. Meir av beis din of Yarmut; relies on the Maharal; "מכניסי רחמים דרכי להאריך בנפילת אפים"). **CORRECTED**: it cites the Ramban *on the Torah* (Bereishis 25:22, "ותלך לדרוש") not the derashah, and concludes the piyyut may be omitted following the Maharal; "does not change the public nusach", Rav Amram and "nobody noticed" are the lecturer's report, not located in OC 166.
- **fn8 (Maharal)** — **CORRECTED/pinned** to **Netivot Olam, Netiv HaAvodah ch. 12**; VERIFIED: objects to "הכניסו רחמינו", allows an instruction-to-appointed-angels reading, prefers the future "מכניסי רחמים יכניסו רחמינו" so that the address to God is unmistakable (the lecturer's "command" noted as his presentation).
- **fn9 (Seder Rav Amram)** — **CORRECTED** (general knowledge, not on Sefaria): "Ashkenazi-style" is anachronistic; it is a Babylonian geonic siddur. Presence of Machnisei Rachamim in it and the Chasam Sofer link: UNCERTAIN (caveat added).
- **fn10 / fn11 (Maharit Asad), fn12 (Igros Moshe)** — UNCERTAIN (not on Sefaria); fn11 "chillul Hashem" gloss noted as not in the lecturer's account (removed in Sefer Edition).
- **fn13 (Taanis 23b; Bava Basra 116a)** — BB 116a VERIFIED (R. Pinchas bar Chama; Mishlei 16:14). **CORRECTED** Taanis 23b: it concerns Chanan HaNechba (Choni's grandson), to whom schoolchildren were sent, not Choni himself.
- **fn14 (Nimukei Yosef)** — author/dates **CORRECTED/VERIFIED** via Sefaria index: Yosef ibn Habib (Habiba), c. 1330–1410, on the Rif; the Ein Yaakov alternative dropped; body "late 1300s" → "c. 1330–1410". The passage on the French custom: UNCERTAIN (not retrieved).
- **fn15 (R. Yaakov bar Yakar)** — UNCERTAIN (not on Sefaria); seat (Worms vs Mainz) flagged for verification; Rashi/Siddur Rashi/Machzor Vitri claims marked unverified.
- **fn16 (Berachos 18b)** — VERIFIED ("even in death called living").
- **fn17 (Mahari Bruna)** — **CORRECTED** via Sefaria index: Yisrael ben Chaim of Brno, 15th c., student of the **Mahari Weil** (not the Terumas HaDeshen), responsa c. 1430–1480, 111 simanim; passage not located (UNCERTAIN).
- **Body (Shiur Review/transcript)**: "ספרדים" → **"ספרים"** (the sefarim say the Safriel gematria; 381 = 381 checked); garbled "בתחפיסה" → **"בדווקא"** (Editorial; enhanced text).
- **Not located (Sefaria):** Oseh HaShalom practice (SA/Rema OC 582 do not mention it); Mahari Bruna siman; Zevadyah/Midas HaRachamim loci.
- **Total:** 8 corrections (fn2, fn5, fn7, fn8, fn13, fn14, fn17, plus fn9 label from general knowledge) + 2 body fixes (ספרים, בדווקא); 9 confirmations (fn3 Yerushalmi, fn2 AZ 2:1/YT 1:6/Rambam 5th principle, fn5 Shabbos 12b text, fn7 OC 166 locus + practice, fn8 Netiv HaAvodah 12, fn13 BB 116a, fn16 Berachos 18b, Sanhedrin 38b, Gen 25:22/Job 22:28 cross-refs); ~10 preserved/flagged. Modified: final MM/2025-09-14 — Machnisei Rachamim and the Question of Intermediaries.html (backup: tmpbuild/pre_2025-09-14.html). Sefer Edition: book-rewrites/2025-09-14 — Machnisei Rachamim and the Question of Intermediaries — Sefer Edition.html (+ styled.docx).

## Backfill entry — 2025-09-28 (Batch 8, run 2026-10-12)

### 2025-09-28 — The Cholera Epidemic and רבי ישראל סלנטר's Decision on יום כיפור
Method note: WebFetch against Sefaria (texts API v3; search-wrapper returned "Unsupported HTTP method" and was not usable). Corrections applied in place to the final MM HTML (body + notes); no Hebrew twin exists for this date. No Sofer.ai docx for this date. Chasam Sofer cholera responsum, Ketzos/Akiva Eger kiddush position, Biur Halachah, Gedolim fun Unzer Zeit, Almanori, Emes LeYaakov not retrievable and left UNCERTAIN.
- **fn3 (Devarim 4:15; Rambam Rotzeach 11; Berachos 32b)** — VERIFIED Berachos 32b cites ונשמרתם מאד לנפשתיכם (Devarim 4:15). **CORRECTED**: Rambam, Hil. Rotzeach UShemiras HaNefesh **11:4** grounds the duty in **Devarim 4:9** (השמר לך ושמור נפשך מאד), not 4:15; "pikuach nefesh overrides" rests on וחי בהם (Yoma 85b, VERIFIED "ולא שימות בהם").
- **fn4 (SA OC 618; MB 618:21)** — VERIFIED locus (10 seifim). **CORRECTED**: seif 1 = patient vs. physician, 2–5 conflicting physicians/doubt, 6 non-expert physician, **7 = the measures (about two-thirds of a medium egg, pause of the time to eat four eggs; drink כמלא לוגמיו)**, 8 urgent need, 10 Ya'aleh VeYavo in Birkas HaMazon; the "ככותבת הגסה" measure is not in 618:7. MB 618:21 VERIFIED (patient tests his own tolerance; Chasam Sofer ח"ו סי' ט"ז, 9 minutes = time to eat a peras); Chasam Sofer Collected Responsa 16 VERIFIED to state "חצי מיל שהוא ט' מינוטין" (dated Slichos 5594, a different question).
- **fn5 (Ketzos HaChoshen on kiddush when YK falls on Shabbos)** — UNCERTAIN (not located; audio reads "kiveh eger", possibly Rabbi Akiva Eger). VERIFIED instead: Magen Avraham 618:10 (sick person who ate need not make kiddush — berachah levatalah) and Mishnah Berurah 618:29 ("קידוש בודאי אין לו לעשות", discusses Ya'aleh VeYavo/Retzei); passage appears to run against the position cited. Note rewritten; flag kept.
- **fn6 (Gedolim fun Unzer Zeit; eyewitness)** — UNCERTAIN (work not located). **CORRECTED** (per audio, Shiur Review): surname **שטראשון** (Strashun), not שטרויסון (6 places); "ראש שטרויסון" → הרש"ש (Shmuel Strashun); unsupported "cited in The Making of a Gadol ad loc." hedged.
- **fn8 (MB / Biur Halachah on the story)** — UNCERTAIN: MB 618:21 and 618:29 contain no reference to Salanter or cholera; Biur Halachah not retrievable. **CORRECTED**: unsupported claims ("Chofetz Chaim's strong language … stands behind", "firsthand weight") removed.
- **fn9 (Yerushalmi Yoma 8:5; Beis Yosef OC 328)** — VERIFIED. **CORRECTED** quote order: הזריז משובח, והנשאל מגונה, והשואל הרי זה שופך דמים (variant reading noted); Beis Yosef on "הנשאל הרי זה מגונה" cites ה"ר ישראל (סימן קנ"ו): the rav should have informed his townspeople in advance — matches the lecturer's explanation.
- **fn10 (Sotah 21b; Rambam Shabbos 2:3)** — VERIFIED Mishnah Sotah 3:4 and Sotah 21b (drowning woman example; the extension to asking a rav is the lecturer's). **CORRECTED**: Rambam Shabbos 2:3 says "ואסור להתמהמה" — the words השואל / שופך דמים are not there (they are SA OC 328:2).
- **fn11 (Tur OC 328)** — VERIFIED ("הנשאל הרי זה מגונה והשואל הרי זה שופך דמים … וחי בהם ולא שימות בהם"); SA OC 328:2 also verified.
- **fn12 (Chasam Sofer, Pressburg cholera 1836)** — UNCERTAIN (not located; OC 157 and 158 checked — other subjects). Lecturer's year/pregnant-woman reasoning preserved as reported; "Verify exact siman" replaced by a "Not located" statement.
- **fn1, fn2, fn7, fn13 (Making of a Gadol; Mekor Baruch; Almanori; Emes LeYaakov)** — non-Sefaria; flags kept. **CORRECTED** fn1: unsupported author dates (1930–2018) removed; fn2: unsupported sentence on modern scholarship (Etkes) removed.
- **Body (Shiur Review / Editorial)**: **CORRECTED** the Hebrew year תר״ח → **תר״ט** (autumn 1848 = 5609; 7 places); **CORRECTED** the elder dayan (רבי יחזקאל לנדא הכהן, anachronistic and a duplicate of "ר׳ איצל הכהן") → **רבי איצל הכהן** with the identification marked unresolved; "ערב יום כיפור" → "in the days before יום כיפור" (talk of 28 Sept 2025 was four days before YK); Baruch Ber Leibowitz "of Kamenetz" added.
- **Total:** 13 corrections (fn3, fn4, fn6, fn8, fn9, fn10, fn1, fn2, תר״ט, dayan name, Strashun, ערב, Kamenetz), 7 confirmations (Berachos 32b, Yoma 85b, SA 618, MB 618:21/29 + MA 618:10, Yerushalmi Yoma 8:5 + Beis Yosef 328, Sotah 21b/Mishnah 3:4, Tur/SA 328), 6 UNCERTAIN (fn5 Ketzos/Akiva Eger, fn6 Gedolim fun Unzer Zeit, fn8 MB/BH, fn12 Chasam Sofer, fn7 Almanori, fn13 Emes LeYaakov). Modified: final MM/2025-09-28 — The Cholera Epidemic and רבי ישראל סלנטר's Decision on יום כיפור.html (backup at ~/tmpbuild/pre_2025-09-28.html). Sefer Edition: book-rewrites/2025-09-28 — The Cholera Epidemic and רבי ישראל סלנטר's Decision on יום כיפור — Sefer Edition.html (+ — styled.docx).

## Backfill entry — 2025-10-19 (Batch 8, run 2026-10-12)

### 2025-10-19 — Siyum Shemoneh Esrei: Yihyu Leratzon, Elokai Netzor, and the Machlokes of Pressburg
Method note: WebFetch against Sefaria (texts API v3; search-wrapper unusable). The source HTML was checked against the cleaned recording transcript as well; several errors inherited from the AI summary (Sandalfon, Zohar, Rema MiPano, "tradition" for "legend", "until all their thoughts") were removed. Corrections applied in place to the final MM HTML (body + notes). Hebrew-twin: none. Backup: tmpbuild/pre_2025-10-19.html.
- **fn1 (Chut HaMeshulash)** — UNCERTAIN (book not on Sefaria). **CORRECTED**: the earlier draft's name/dates for the author could not be verified and were removed; "by a grandson of the Chasam Sofer" kept as the speaker's report. Body: "Rabbeinu Baruch" removed; Pressburg account hedged as single-source (the speaker found it nowhere else).
- **fn2 (Koheles 4:12; Ketubos 62b)** — VERIFIED Ketubos 62b (Rami bar Chama cites the verse of R. Oshaya bar R. Chama bar Bisa, third generation). **CORRECTED**: an earlier draft made Bava Metzia 85a the primary source; reversed. BM 85a (R. Yochanan, Yeshayahu 59:21) is the parallel.
- **fn3 (Berachos 4b, 9b; Tehillim 51:17, 19:15)** — **CORRECTED** loci: placement argued at 9b (not 31a); the nineteen-chapter count resolved by counting chapters 1-2 as one; Hashem Sefasai Tiftach as extension of the tefillah. VERIFIED.
- **fn4 (Rashba, Berachos 17a)** — **CORRECTED**: the position that Yihyu Leratzon precedes Elokai Netzor is the **Rabad's**, cited by the Rashba on 17a (not Rashba's own, and not "Chiddushei HaRashba 31"). The Rashba's own conclusion is UNCERTAIN.
- **fn5 (Rema, SA OC 122:1; Biur HaGra)** — **CORRECTED**: "Rema MiPano" (summary error) replaced with the **Rema's gloss on SA OC 122:1** (VERIFIED: custom of Elokai Netzor before Yihyu, interrupting for Kaddish/Kedushah). Gra's position (Elokai Netzor inside the Amidah) UNCERTAIN: Biur HaGra OC 122 does not mention Elokai Netzor; flag added.
- **fn6 (Mishnah Berurah 122:3)** — VERIFIED ("tov lomar Yihyu Leratzon kodem hatachanunim ve'acharehem"). **CORRECTED** attribution: the two-reasons explanation and "tarti d'sasri" are the speaker's, not located in MB.
- **fn7 (Avudraham)** — UNCERTAIN (location not retrievable); Elokai Netzor said by individuals preserved as the speaker's report; flag kept.
- **fn8 (Berachos 16b-17a)** — VERIFIED list of personal prayers. **CORRECTED**: list of amoraim and sequence (R. Elazar, R. Yochanan, R. Zeira, R. Chiya, Rav, Rebbi, Rav Safra; R. Alexandri, Rava, Mar bereih d'Ravina, Rav Sheshes); wording of Mar's prayer ("...hafer atzasam vekalkel machashavtam," not "until all their thoughts"); the Gemara gives no reason his prayer became standard.
- **fn9 (Berachos 54a; Mishnah Berachos 9:1)** — VERIFIED Mishnah and Rava/lion blessing. **CORRECTED**: locus 54a (not 54b); the compound blessing at each place (ba'aravos u'vagamal); he "went inside" the wall (not "flew"); epithet "melumad b'nissim" not located (flag); geography of Mechoza (Tigris near Ctesiphon, not Mosul) noted as outside Sefaria.
- **fn10 (Berachos 30b-31a; Tosafos; Rema OC 560:2, EH 65:3)** — VERIFIED: Mar made a wedding for his son, broke a cup worth 400 zuzei; Rav Ashi's white-glass cup; Tosafos "mikan nahagu leshaber zechuchis b'nisu'in". **CORRECTED**: the zecher l'churban reason is not in Tosafos; it comes via SA OC 560:2 and the Rema (OC 560:2; EH 65:3) as the custom.
- **fn11 (Tehillim 137:5)** — VERIFIED.
- **fn12 (Tehillim 20:8)** — VERIFIED; Radak there confirms the chariots/Name contrast.
- **fn13 (Radak)** — **CORRECTED** locus: Radak on **Tehillim 19:15** (imrei fi vs. hegyon libi, unspoken thoughts), not 20:8. VERIFIED.
- **fn14 (SA OC 122)** — VERIFIED in outline (se'if 1-3; Rema; MB 122:3).
- **fn15 (Shelah)** — UNCERTAIN: direct attribution of the segulah to the Shelah not located; flag kept.
- **fn16 (Shem Ephraim)** — UNCERTAIN (not located); Sefaria confirms Rashi on Shoftim 20 contains parenthetical passages; flag kept.
- **fn17 (Rashi on Micah 6:9)** — VERIFIED parenthetical passage (venoshiyah yireh shemecha ... hatorah matzilo migehinom). **CORRECTED**: the summary's "sefer Mechlal" / "Tereisar" titles removed; Micah in Trei Asar.
- **fn18 (Siddur Amsterdam 1699)**, **fn19 (Yaavetz)** — UNCERTAIN (not retrievable); flags kept.
- **fn20 (Or HaChaim, Parshas Haazinu)** — **CORRECTED**: summary's "Zohar HaKadosh" (with a Zohar locus that was internally inconsistent) replaced by the speaker's "Or HaChaim HaKadosh" (hedged "I think"); UNCERTAIN, not located in Or HaChaim on Devarim 32.
- **fn21 (Arizal on naming at the bris)**, **fn22 (Bnei Yissaschar / Agra D'Pirka)** — UNCERTAIN (not retrievable); flags kept.
- **Misc.** VERIFIED: Berachos 9b (David, 18 chapters), Bava Basra 165a (avak lashon hara), Mishnah Makkos 3:16, Yeshayahu 42:21. Gematria arithmetic checked: HaShalom = Oseh = Safriel = 381 (not Sandalfon = 280).
- **Total:** 13 corrections (fn1, fn2, fn3, fn4, fn5, fn6, fn8, fn9, fn10, fn13, fn17, fn20, body "Rabbeinu Baruch"/Pressburg hedge), 14 confirmations (Ketubos 62b, Berachos 9b, Tehillim 19:15/20:8/51:17/137:5, Koheles 4:12, Mishnah Berachos 9:1, SA OC 122, MB 122:3, Rema EH 65:3, Mishnah Makkos 3:16, Rashi Micah, Rashi Shoftim parentheses), ~10 preserved/flagged (Gra's position, Rashba's conclusion, Avudraham, Shelah, Shem Ephraim, Amsterdam 1699, Yaavetz, Or HaChaim, Arizal, Bnei Yissaschar, Chofetz Chaim remark, Mechoza geography). Modified: final MM/2025-10-19 — Siyum שמונה עשרה — יהיו לרצון, אלוקי נצור, and the מחלוקת of Pressburg.html. Sefer Edition: book-rewrites/2025-10-19 — Closing the Amidah — Yihyu Leratzon, Elokai Netzor, and the Pressburg Controversy — Sefer Edition.html.

---

## Backfill entry — 2025-10-27 (run 2026-10-18)

### 2025-10-27 — The Depth of Kavanah at the Close of the Amidah: Elokai Netzor, the Four Lema'an-Phrases, and the Three Steps Back
Method note: WebFetch against Sefaria (texts API v3). The source HTML was checked against the cleaned recording transcript and the AI summary; several errors inherited from the summary (truncated Tehillim 19:15, "Rabbah" for Rava, a fabricated blessing and Divine quotation, "midrash" for haggadah, the "lifted 1493" expulsion claim, the wrong Hebrew date) were removed. Corrections applied in place to the final MM HTML (body + notes). Hebrew-twin: none. Backup: tmpbuild/pre_2025-10-27.html.
- **fn1 (Seder HaYom, Tehillim 19:15)** — VERIFIED the count for the full verse (ten words, opening and closing yud, ten yuds if the Name is spelled out). **CORRECTED**: the seven-word truncated quotation restored to the whole verse; the Yigdal identification (summary's, not in the audio), Ein Zeitim and the ten sefiros link removed. Venice 1599 and the Seder HaYom remark UNCERTAIN (not located).
- **fn2 (Rav Amram Gaon)** — UNCERTAIN (placement not retrievable); flag kept as the lecturer's report.
- **fn3 (Avudraham)** — **CORRECTED**: concluding blessing wording hedged (not asserted); "reserved for yechidim" and the dating to the early printers removed as unverified. UNCERTAIN (passage not located).
- **fn4 (Berachos 16b-17a)** — VERIFIED list of personal prayers and Mar's text. **CORRECTED**: the list and sequence of sages; the last word of Mar's prayer is mirmah (not sheker); v'nafshi ke'afar comes partway through, the prayer ends Hashem Tzuri v'Go'ali; the Gemara gives no reason his prayer became standard.
- **fn5 (Gra / Zohar)** — UNCERTAIN (not located); Bereishis 13:16 and 28:14 verified as the dust promises. Zohar attribution kept as the lecturer's hedged report ("I think").
- **fn6 (Maharsha, Berachos 17a)** — UNCERTAIN. The comment as retrieved reads the phrase as continuing the preceding petition; the lecturer's reading was not found there.
- **fn7 (R. Simcha Bunim of Peshischa)** — VERIFIED Sanhedrin 37a (the world was created for me) and Bereishis 18:27. **CORRECTED**: R. Bunim was a leader of the Peshischa school and the Kotzker's teacher, not "founder of Peshischa and rebbe of Kotzk".
- **fn8 (Kli Yakar, Bereishis 28:14)** — VERIFIED that it speaks of dust and Avraham's humility. UNCERTAIN: the dust-and-stars pairing as the lecturer presents it not found; locus unconfirmed.
- **fn9 (Beis Yosef, OC 122)** — VERIFIED Yirmeyahu 14:7 (asei lema'an shemecha). **CORRECTED**: haggadah, not "midrash"; the four things, R. Akiva and R. Eliezer are not in the paragraph (given as the lecturer's report); the unverified verse list removed.
- **fn10 (Chasam Sofer, Noach)** — UNCERTAIN (acronym teaching not found in the text retrieved); kept as reported by his students.
- **fn11 (Bereishis 9:13; Chagigah 16a)** — VERIFIED (rainbow; Chagigah 16a with Yechezkel 1:28).
- **fn12 (Berachos 32b)** — VERIFIED. **CORRECTED**: the gates of prayer are locked per Eichah 3:8; the gates of tears (singular dim'ah) are open per Tehillim 39:13; the body's illogical proof from Eichah 3:44 repaired.
- **fn13 (Eichah 3:44)** — VERIFIED. **CORRECTED**: the claim that it is Rashi's proof-text for the Gemara removed.
- **fn14 (Yoma 53a-b)** — VERIFIED (Mishnah; derivation from Shlomo; maamados and teacher leaving sideways; R. Elazar and R. Yochanan; Rava and Rav Yosef; the blessing yehei ra'ava deteirum reishach akulei karka; three steps at the end of prayer, R. Yehoshua ben Levi in the name of R. Alexandri, Abaye and Rava). **CORRECTED**: Rava, not Rabbah, throughout; the fabricated blessing ("head of all Israel, head of Mechoza") and Divine quotation removed; the claim that "Yoma does not mention the number three" is false and was reversed; the blood-on-the-threshold and Mechoza glosses UNCERTAIN (lecturer's).
- **fn15 (Mishnah Taanis 4:2; Taanis 27a)** — VERIFIED.
- **fn16 (yaal kegam)** — UNCERTAIN (the six exceptions not enumerated). **CORRECTED**: the unverified list and daf references and the Rabbah confusion removed; "two or three hundred" kept as the lecturer's estimate.
- **fn17 (Sanhedrin 96a, Nebuchadnezzar)** — VERIFIED in outline (Baladan, letter to Hizkiyahu, scribe, Gabriel, reward). **CORRECTED**: the Gemara has four steps, not three; the Divine "quotation" ("three steps ... three kings") is not in the passage and was removed; the lecturer's three-steps link and the Beis HaMikdash link attributed to him and to a Rabbi Kalish (unconfirmed).
- **fn18 (Beis Yosef OC 123; R. Yitzchak Abuhav)** — VERIFIED that the Beis Yosef cites "rabbeinu hagadol Mahari"a" for the three mil from Sinai. **CORRECTED**: "expulsion order lifted in 1493" and "led a delegation to Portugal" removed; the biographical narrative otherwise kept as the lecturer's. UNCERTAIN: identification of the Mahari"a with R. Yitzchak Abuhav, the Toledo and King Joao details.
- **fn19 (Shabbos 88b)** — VERIFIED (twelve mil at each utterance; souls departing and revived with the dew of resurrection; Rashi on Shemos 20:15 gives twelve). **CORRECTED**: the invented Hebrew quotation removed; the lecturer's difficulty (three vs twelve) preserved as his own; Mechilta parallel UNCERTAIN.
- **fn20 (Magen Avraham; SA OC 123:1, 102:4)** — VERIFIED SA OC 123:1 (three steps in one bow; left, right; bow) and the Rema's gloss; OC 102:4 (four amos). **CORRECTED**: the unsupported remark about not returning to one's place before the Shatz's repetition removed. UNCERTAIN: the Magen Avraham passage on leaving facing the Aron not located.
- **Body-only.** **CORRECTED**: Hebrew date and weekday (27 Oct 2025 was a Monday, 5 Cheshvan 5786, not 26 Tishrei / Sunday); typos (ח״ח, "Hr Sinai", "sופר", "Reb Moshe" in the Volozhin story, the Mar heading שקר).
- **Misc.** VERIFIED: Hebcal date conversion; Bereishis 18:27; Tehillim 37:11. First-blessing remark (SA OC 101:1 with the Rema) given as cited, not re-fetched.
- **Total:** 18 corrections (fn1, fn3, fn4, fn7, fn9, fn12, fn13, fn14, fn16, fn17, fn18, fn19, fn20, and 5 body-only: date/weekday, Yoma "three" claim, Rabbah to Rava, typos, "midrash" to haggadah), about 17 confirmations, 9 UNCERTAIN/flagged (Seder HaYom, Rav Amram, Avudraham, Gra/Zohar, Maharsha, Kli Yakar pairing, Chasam Sofer, Magen Avraham, Abuhav identification). Modified: final MM/2025-10-27 — The Depth of כוונה in שמונה עשרה.html. Sefer Edition

## Backfill entry — 2025-11-02 (run 2026-10-18)

### 2025-11-02 — Tachanun: The Confession, the Fall on the Face, and the Custom of Omitting It
Method note: WebFetch against Sefaria (v3 texts API; name/index APIs; search-wrapper not used). Corrections applied in place to the final MM HTML (body + notes); the source was also checked against the cleaned recording transcript and the AI summary. Several fetches failed or returned only a summary (Zohar III 222a / I 58b, Ba'er Heitev on SA OC 131, Ritva on Bava Metzia [not on Sefaria], Baal HaTurim on Gen 3:6 [no text], Numbers 16:45, Tur OC 131 returned a summary only), so those items were left UNCERTAIN. Minchas Elazar, Divrei Chaim, the Radoshitzer story, Igros Moshe, the Chazon Ish story, the Chida's account and the Chofetz Chaim are not searchable on Sefaria. Hebrew-twin: none (the "- Copy.html" was ignored). Backup: tmpbuild/pre_2025-11-02.html.
- **Callout (NASA / Armstrong)** — **CORRECTED**: "first space mission" → "first spacewalk, as the message put it" (the recording says spacewalk); the year 1969 was supplied by a listener, now stated; claims left as relayed (unverifiable).
- **fn1 (Zohar III Balak 222a; I 58b; Shaar HaKavanos)** — UNCERTAIN (could not be opened); loci were the write-up's, not the speaker's; the Balak/222a pairing is internally doubtful (flagged, not asserted).
- **fn2 / body (Tur and SA OC 131–134; Arizal "three or four hundred years"; "17th century")** — SA OC 131:1, 131:2 (sitting), 131:4–7, 131:5 (selichos and vidui on a fast day with a bris) VERIFIED. **CORRECTED**: Tur 131 as consulted describes nefilas apayim (Rambam, Rav Natronai, Rav Hai) but does not mention a vidui/Ashamnu before it; the speaker's report that the Tur notes some kehillos is UNCERTAIN and hedged in body and note; the unsupported "Lamenatzeach/Eretz Yisrael distinctions", "simanim 131–134" and "17th century" removed; Arizal dated 1534–1572 against the speaker's round figure.
- **fn3 (Chida)** — UNCERTAIN (work not located); the speaker did not know who the sage was (now stated).
- **fn4 + body (kol hakoeis ke'ilu oved avodah zarah)** — **CORRECTED**: not Shabbos 105b/R. Avin and not Zohar I 27b. The wording is the **Rambam, Hilchos De'os 2:3** ("the early Sages said": anyone who becomes angry is like one who worships idols) — VERIFIED. Shabbos 105b VERIFIED as related only (baraita: tearing garments/breaking vessels in anger = like an idolater; R. Avin on Tehillim 81:10 = the strange god is the evil inclination). Not in Nedarim 22b. Body "The גמרא says" → "The saying of חז״ל is".
- **fn5 (Yesod VeShoresh HaAvodah)** — Nechemiah 9:33 VERIFIED. UNCERTAIN: the midrash's location (write-up's "in his treatment of nefilas apayim" was its own addition, removed), the author's dates (1730–1794 marked unverified), ArtScroll translation (speaker: "I think"). Work exists on Sefaria; passage not searchable.
- **fn6 (Devarim 9:18, 9:25)** — VERIFIED; **CORRECTED** "other crisis moments": both verses retell the same forty days after the calf.
- **fn7 + body (Bamidbar 16:22, 16:45)** — 16:22 VERIFIED (they fell on their faces and said "O God, Source of the breath of all flesh"). **CORRECTED** body: it is **Moshe and Aharon**, not Klal Yisrael (speaker's wording noted); "were forgiven through the falling" marked as the speaker's inference.
- **fn8 + body (Bava Metzia 59b; Mishnah Kelim 5:10; Sanhedrin 68a; Gittin 56b)** — all VERIFIED. **CORRECTED**: the oven was cut into rings with **sand** between them (Kelim 5:10), not "cement"; carob tree/walls detail (walls leaned, neither fell nor straightened); **R. Akiva** volunteered to bring R. Eliezer the news (not merely "joined" the Sages); the Sages' visit and "we are sorry" is the speaker's paraphrase, the Gemara (Sanhedrin 68a) has them visit him ill and R. Yehoshua lift the ban at his death; calendar error: **"thirtieth, not thirty-first"** removed (there is no 31st day; BM 59b: she mistook a full month for a deficient one); R. Yochanan ben Zakkai is not in the BM 59b episode (the ban is led by Rabban Gamliel; Yavne request in Gittin 56b VERIFIED) — framing marked as the speaker's.
- **fn9 (Devarim 30:12; Shemos 23:2)** — VERIFIED; **CORRECTED**: the "acharei rabim lehatot" explanation is **R. Yirmeya's**, not R. Yehoshua's.
- **fn10 (Ritva; Beis Yosef)** — **CORRECTED**: the **Beis Yosef (OC 131) cites Talmidei HaRashba** on BM 59b ("kol yoma lo hava shavka leih limipal al apeih" → no speaking between tefillah and tachanun), not the Ritva; the reshus point is attributed to "the Rishonim" without a name, not to the Ritva. Ritva on Bava Metzia not located on Sefaria (UNCERTAIN).
- **fn11 (Chofetz Chaim)** — **CORRECTED**: Rashi on Bereishis 21:12 VERIFIED but says only that Avraham was inferior to Sarah in prophecy; BM 59a VERIFIED (R. Chelbo; "if your wife is short, bend down and whisper") — neither is a source for the principle; "Shmiras HaLashon" unsupported; removed. The Chofetz Chaim's own source: UNCERTAIN, kept as the speaker's report.
- **fn12 + body (Beis Yosef OC 131; Brisk vs. Vilna)** — **CORRECTED**: the retrieved Beis Yosef does not mention Brisk/Vilna; the speaker said "Bar Heitam" (possibly the Ba'er Heitev — fetch failed; UNCERTAIN), the summary turned it into "Beis Yosef". Rema on SA 131:4 VERIFIED (at Mincha tachanun is said even in the presence of the child); Mishnah Berurah 131:33 VERIFIED for Purim Katan.
- **fn13 (Minchas Elazar)** — not on Sefaria, UNCERTAIN; unsupported superlative ("one of the most quoted poskim") removed.
- **fn14 + body (Divrei Chaim; "נורא עלימה מלך")** — UNCERTAIN; body **CORRECTED** to the **Noam Elimelech** (R. Elimelech of Lizhensk), an identification by date (21 Adar) from a garbled recording; flagged as such.
- **fn15 (Radoshitzer)** — UNCERTAIN; speaker did not identify him; the write-up's identification marked as such. Body: arithmetic noted (5 weeks × 70–80/day ≈ 2,450–2,800, not 5,000).
- **fn16 (days tachanun is omitted)** — VERIFIED SA OC 131:4–7 (Tu B'Av, Tu BiShvat, Rosh Chodesh, Chanukah, Purim, Lag BaOmer, erev YK/RH, Nisan, Tisha B'Av, YK to Sukkos, Rema: Sivan to Shavuos). **CORRECTED**: the speaker's "all of Tishrei after Sukkos" is not in SA 131 (which has YK to Sukkos) — UNCERTAIN, hedged; Shushan Purim/Adar I items removed from the note except Purim Katan (MB 131:33).
- **fn17 (Igros Moshe)** — UNCERTAIN (no responsum given by the speaker); quoted paraphrase marked as such. **fn18 (Chazon Ish)** — UNCERTAIN (oral tradition; dates 1878–1953 not verified).
- **Body (yored, retort, Litvaks/Ashkenazim, Zalman Meltzer, קבלת עולים)** — **CORRECTED**: "יורד" → "יורד מנכסיו"; the visitor's unintelligible retort removed; "Litvaks do; Ashkenazim who follow the SA" → "Litvaks do, and others"; "מלמדי זלמן… his grandson" removed as unsupported (recording unclear); "קבלת עולים" (unintelligible) removed; yahrzeit fast VERIFIED as SA YD 402:12 (main text, not the Rema).
- **Not located / not relied on:** the Baal HaTurim aside on Chavah striking Adam; the Babylonian yeshivos saying tachanun on Chanukah/Purim; Brisk/Vilna dispute.
- **Total:** 17 corrections (callout, fn2, fn4, fn6, fn7/body Korach, fn8/body oven+Akiva+calendar+ban, fn9, fn10, fn11, fn12/body Brisk-Vilna, fn13, fn14/body Noam Elimelech, fn16, body Arizal dates, body yored/retort/arithmetic, body Litvaks/Zalman Meltzer/kabbalas olim, fn5), ~19 confirmations (BM 59a/59b, Mishnah Kelim 5:10, Sanhedrin 68a, Gittin 56b, Rambam Deos 2:3, Shabbos 105b text, Tehillim 81:10, Nechemiah 9:33, Devarim 9:18/9:25/30:12, Shemos 23:2, Bamidbar 16:22, SA OC 131:1/2/4–7, Rema 131:4, MB 131:33, Beis Yosef 131, SA YD 402:12, Rashi Bereishis 21:12), ~13 UNCERTAIN/preserved with flags (fn1 Zohar loci, Tur vidui claim, fn3 Chida, fn5 midrash locus, Ritva, Chofetz Chaim, Minchas Elazar, Divrei Chaim, Radoshitzer, Ba'er Heitev/Bar Heitam, Igros Moshe, Chazon Ish, Tishrei-after-Sukkos). Modified: final MM/2025-11-02 — שיעור על תחנון.html (backup: tmpbuild/pre_2025-11-02.html). Sefer Edition: book-rewrites/2025-11-02 — Tachanun — The Confession, the Fall on the Face, and the Custom of Omitting It — Sefer Edition.html (+ — styled.docx).

## Backfill entry — 2025-11-10 (run 2026-10-18)

### 2025-11-10 — תחנון, נפילת אפים, and the Origins of והוא רחום

Method: every note-academic flag and Sefaria-indexed citation was checked against the Sefaria v3 texts API (WebFetch); non-Sefaria sources (Zohar locus where unreachable, Rivash, Levush, Kol Bo/Rokeach, Gra/Maaseh Rav, Hanover/Epstein/Emden dates) were not fabricated. Hanover, Kitzur Shelah (1683) and Emden dates were cross-checked against secondary (Wikipedia) sources only. No Hebrew twin exists for this date.

- CORRECTED — Body date: recording dated 10 Nov 2025 = י״ט חשון (not 11 Cheshvan); header and footer fixed.
- UNCERTAIN — fn1 Zohar locus (Nefilas Apayim / Tehillim 25 danger): could not be located; flagged.
- VERIFIED — fn2 Rosh Hashanah 17b (Yochanan; Moshe; Thirteen Attributes; tallis).
- CORRECTED — fn3 Maharsha (Chidushei Agados, RH 17b): quote verified; white garment is טלית לבנה, rewritten with the verified wording.
- VERIFIED — Psalms 104:2 (עוטה אור כשלמה).
- CORRECTED — fn4: Tur (OC 131) citing Rav Natronai, Aruch HaShulchan, and Berachos 27b verified; Rambam 5:13 and Rosh dropped as unsupported; "שלחן ערוך" corrected to ערוך השלחן; "Rav Heschel" replaced with "a participant".
- UNCERTAIN — fn4 Rivash responsum (that Nefilas Apayim is optional): not located.
- VERIFIED — fn5 Genesis 22:24 (ומעכה / תחש list); UNCERTAIN — Baal Shem Tov acronym source.
- UNCERTAIN — fn6 Levush (different chapter): not located.
- VERIFIED — Bava Metzia 59b (R. Eliezer fell on his face; Rabban Gamliel).
- CORRECTED — fn7: "seated" changed to "without falling"; VERIFIED Aruch HaShulchan; Berachos 27b (Maariv optional).
- VERIFIED — fn8 II Samuel 24:13–15.
- CORRECTED — fn9: חרם wording changed to קול קורא; verse corrected to ויאמר דוד אל גד; 1683 dating added as secondary note.
- UNCERTAIN — fn10 publication details of the cited work: marked unverified.
- CORRECTED — fn11 gematria: reported as lecturer's figure; arithmetic note (1643 vs 814) added.
- CORRECTED — fn12: "ויהי נועם" section replaced with "ויאמר דוד אל גד"; fully rewritten.
- CORRECTED — fn13: Hanover biography corrected; Epstein's name corrected to יחיאל, dating hedged (1683).
- CORRECTED — fn14 rewritten; "Mishnah Berurah" changed to "(as heard) מעשה רב"; "Siddur Bnei Yissaschar" changed to an unidentified Italian kabbalist's work (possibly משנת חסידים). UNCERTAIN — both identifications are inferences.
- VERIFIED — Shabbos 129b; CORRECTED — fn15 (BK 82a) and fn16 (Ketubos/Shabbos 129b) rewritten.
- CORRECTED — Section VI: קיצץ בנטיעות (Chagigah 14b VERIFIED) replaces "מקצת בנטיעת"; SA OC 131:3 night rule and OC 134 cited, with note that SA presupposes tachanun at Mincha.
- UNCERTAIN — fn17 Kol Bo siman 11 does not contain the story; Rokeach not located.
- VERIFIED — fn18 Isaiah.
- CORRECTED — fn19 rewritten (Sanhedrin 95b has no Hezekiah prayer); VERIFIED 2 Kings 19:35.
- CORRECTED — Azriel letters sentence rewritten; note added that the Hezekiah stanza words are reconstructed from an indistinct source.

Total: 20 CORRECTED, 12 VERIFIED, 8 UNCERTAIN (approximate tally by bullet; some bullets combine statuses).

Modified: final MM/2025-11-10 — תחנון, נפילת אפים, and the Origins of והוא רחום.html (in place; backup tmpbuild/pre_2025-11-10.html). No Hebrew twin. Footnotes 1–19 contiguous and matched.

## 2026-10-18 — Kel Odon — The Silent Angels, the Hefsek Debate, and Dancing on Shabbos

- **fn3 (Tosafos Sanhedrin 37b d"h מכנף הארץ זמירות שמענו; Yeshayahu 6:2)** — **CORRECTED**: the Rav says the six-wing verse is in Yechezkel; Yechezkel 1:6 gives four wings (VERIFIED), Yeshayahu 6:2 gives six. Tosafos (Vilna, opening lines) VERIFIED: "וכל כנף הוא אומר שירה אחת ביום בששת ימי החול"; speaks of the חיות. **UNCERTAIN**: the Rav's "I want to hear my children" detail not located in the part retrieved.
- **fn4 (Chullin 91b)** — **VERIFIED** (editor's cross-reference): angels do not say shirah above until Israel say it below; order differs from the Rav's picture, flagged.
- **fn5 (Bereishis Rabbah 1:3; Tehillim 104:3-4)** — **VERIFIED** R. Yochanan: second day (Tehillim 104:3-4); **CORRECTED**: R. Chanina gives the **fifth** day, not "the fourth" (body and Section VIII annotated). **UNCERTAIN**: which Rashi "implies" Monday (Rashi on Bereishis 1:1, 1:7 do not state it); "before the world" not located.
- **fn6 (Berachos 4b)** — **CORRECTED**: 4a → **4b** (Michael one flight, Gavriel two; Tosefta adds Eliyahu four, Angel of Death eight). Question itself not preserved on the recording.
- **fn8 (Rambam, Order of Prayer, end of Sefer Ahavah)** — **VERIFIED** in outline: Shabbos has נשמת, ישתבח, then יוצר אור ובורא חשך; the additions do not appear in the text retrieved.
- **fn9 (Tur OC 281)** — **CORRECTED/narrowed**: the Tur's sentence names only לאל אשר שבת for Toledo ("ובטוליטולא אין אומרים אותו"; Ashkenaz and France say it, Rav Amram also wrote it); אל אדון is not mentioned. **UNCERTAIN** as to the Rav's inclusion of אל אדון.
- **fn13 (Shulchan Aruch OC 54:3)** — **VERIFIED**: speaking between Yishtabach and Yotzer; "returns from the battle lines". Siman is the editor's identification.
- **fn15 (Or Zarua; Magen Avraham; Rema SA OC 281:1; Mishnah Berurah 281:3)** — **VERIFIED** Rema 281:1 "מלבד אם לא אמר לאל אשר שבת וכו' מחזירין אותו" and MB 281:3 (make-up after the Shemoneh Esrei without a berachah, limited to לאל אשר שבת; Chayei Adam: do not skip it to pray with the tzibbur). **CORRECTED** (flag split): the Rav's extension to אל אדון and his "skip it, yes" are contrary to MB/Chayei Adam. **UNCERTAIN**: Or Zarua and Magen Avraham wordings not located.
- **fn16 (Shulchan Aruch OC 138:1, Rema)** — **VERIFIED**: "להתחיל בדבר טוב ולסיים בדבר טוב" is in the Rema's gloss; Mechaber is the three-verse rule.
- **fn17 (Vayikra 5:26; Maor VaShemesh)** — **VERIFIED** verse and the acrostic ל-א-ש-מ-ה-ב-ה (checked letter by letter); Maor VaShemesh author/dates (R. Kalonymus Kalman Epstein, c. 1817-23, pub. 1842) VERIFIED on Sefaria. **UNCERTAIN**: the custom (Apter Rav) not located.
- **fn18 (Bereishis 22:24; Imrei Noam)** — **VERIFIED** verse and both acrostics (תחש = תקעו חודש שופר; מעכה = מלוך על כל העולם). **UNCERTAIN**: Imrei Noam passage; Rav calls the author "a son of the Ropshitzer", likely a grandson (hedged, unverified).
- **fn19 (Megillah 23a; Esther 1:14)** — **CORRECTED**: the Gemara derives the seven readers of Shabbos from the seven who saw the king's face (רואי פני המלך), not from sarisim; seven-sarisim wording was the congregant's.
- **fn21 (Avodah Zarah 8a; Bereishis Rabbah 22:13)** — **CORRECTED** (as the Rav's understanding): Avodah Zarah 8a does not state Adam's teshuvah or mention Shabbos; Bereishis Rabbah 22:13 (Adam says מזמור שיר ליום השבת after Cain's repentance) VERIFIED as cross-reference.
- **fn22 (Shulchan Aruch OC 339:3)** — **VERIFIED**: אין מספקין ואין מטפחין ואין מרקדין; Rema notes the practice of clapping and dancing and permitting authorities.
- **Not checkable / unchanged (UNCERTAIN, not located on Sefaria)**: fn1 (recap), fn2 (R. Chaim Vital), fn7 (Rav Saadia's siddur), fn10 (Sefer HaIttim), fn11 (Sefer HaPardes; attribution to Rashi flagged), fn12 (Beis Yosef), fn14 (Shir HaMaalos aside), fn20 (Zohar passage), fn23 (Landa hakdama / Talner tish), fn24 (Wolfson, personal testimony), fn25 (Rokeach; Rema 281:1 "להאריך ולהנעים" noted as parallel).
- **Total:** 8 corrections (fn3, fn5, fn6, fn9, fn15 narrowing, fn19, fn21, fn18 hedge) plus Sofer-over-Plaud exclusions (Sefer HaEshkol, Yad HaMelekh, R. Yehoshua Horowitz, named participants), ~13 verified (fn3 Tosafos, fn4, fn5 R. Yochanan, fn8, fn13, fn15 Rema/MB, fn16, fn17, fn18 verse/acrostics, fn22, plus Isaiah 6:2, Ezekiel 1:6, Gen 22:24), ~11 UNCERTAIN, ~11 not checkable. Modified: final MM/2026-10-18 — Kel Odon — The Silent Angels, the Hefsek Debate, and Dancing on Shabbos.html.
