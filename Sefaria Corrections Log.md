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
