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

## Weekly entries (going forward)

New entries added each Sunday by the automated scheduled task. Format for each week:

```
### YYYY-MM-DD — [Shiur title]
- **fnN (topic)** — CORRECTED / VERIFIED / UNCERTAIN. [detail]
- **Total:** X corrections, Y confirmations, Z flags preserved.
```

*First automated entry will be for the 2026-09-06 shiur (or whichever week has the next new shiur).*
