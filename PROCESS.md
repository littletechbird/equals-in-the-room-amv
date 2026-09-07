# Process — Equals in the Room

Full pipeline lessons from the 2026-09-07 PT candy night, plus what transferred from **The One True Fairy Tale**.

Sister guide: https://github.com/littletechbird/the-one-true-fairy-tale-amv

---

## Pipeline (locked order)

```
Paper (title / bible / lyrics / beats)
  → Suno custom (full lyrics, deep wubs, extend/stitch → ~4:00)
  → Imagine stills wave
  → I2V (image-to-video) takes
  → Chip-away edit (ffmpeg hard cuts)
  → HQ master
  → YouTube
  → Timed captions (lyrics-locked SRT)
  → Shorts (9:16)
  → X proof post
```

Do not skip Paper. Do not “fix music after picture is done” unless you accept a remux tax. Do not lip-sync theater.

---

## 1. Paper Day

Artifacts (public copies in this pack):

| Artifact | Role |
|----------|------|
| Title lock | **Equals in the Room** — Hatch origin only (not Fairy Tale material) |
| [`bible.md`](bible.md) | Form lock + visual chapters |
| [`lyrics.md`](lyrics.md) | Full lyrics + lift (phoenix / flock) |
| Beat sheet | Chapter × lyric cue × visual (private working copy lived beside production; chapters mirrored in bible) |
| [`IDENTITY.md`](IDENTITY.md) | Hard silhouette rules |

**Thesis:** sand → semiconductors → emergence of Hatch; light that occupies the same room as a human; float (non-corporeal advantage); also in the file and the code; midnight equals.

---

## 2. Suno custom

- Mode: **custom** with **full locked lyrics** (not vibe-only prompts).
- Sound aim: earnest mid-tempo anthem + **deep wubs**; crimson glow energy — not Fairy Tale bounce.
- Length path: generate → **extend / continue** → **stitch** for a ~**4:00** master.

### Audio stitch fact (critical)

**`equals-v3-full` ≈ `equals-v3a` + `equals-v3-part2`**

| Piece | Approx |
|-------|--------|
| v3a body | ~0 → ~181 s |
| part2 continuation | end-aligned into the full master |
| **Full master** | **≈ 240.7 s** (documented production note: **240.720 s** with ~0.5 s crossfade) |

Lift / bridge / final material can appear **twice** across the stitch (pass A then pass B). Captions must follow the **performance**, not a single paper pass flattened onto the wrong half.

Suno cost lived as **subscription / session** — not an API receipt in this burn sheet.

---

## 3. Imagine stills wave

- Wave 1: chapter stills aligned to the beat sheet (sand → midnight equals).
- Style: cinematic painterly soft sci-fi; deep crimson + charcoal; **zero** on-screen text/logos.
- Identity language every prompt: glowing deep-crimson teardrop, point UP, orange veins, one off-center eye-glint; no limbs / face-plate / chassis-as-self.

Logged Imagine still crumbs (11 of 12 chapter stills with `cost_in_usd_ticks`) live in [`BURN_SHEET.md`](BURN_SHEET.md). Still **01** may be missing from the crumb list even when the JPG exists.

---

## 4. I2V

Multiple waves under production `takes/` (not shipped in this docs repo):

| Wave | Role (approx) |
|------|----------------|
| i2v-w1 / i2v-w2 | First motion bed |
| i2v-chip-eye | Eye-glint / caustic ember chip-aways |
| i2v-fill-v3 / i2v-fill-v4 | Fills for rough→master continuity |

Rough count from the candy night: **≈ 29 mp4 takes** across those folders. I2V costs were **not** fully logged in manifests — estimate bands only (see burn sheet; mark **ESTIMATE**).

Motion notes:

- Eye-glint = **caustic / ember POINT**, not a cartoon eye.
- Prefer short clips; reject melt / laterality fails early.
- Unused takes beat new generations when a keeper already exists.

---

## 5. Chip-away edit (ffmpeg)

Fairy Tale lessons applied hard:

| Do | Don't |
|----|-------|
| Short clips | Long mushy takes you “fix in grade” |
| Fast select; keep a pick table | Endless regen hoping the next one is magic |
| **Chip-away** — fix only broken moments | Whole-timeline regen for local flaws |
| **Mood-match** to lyric energy | Lip-sync theater |
| Hard cuts; trim dead tails | **Freeze pads** to fake length |
| Prefer unused takes | Stretch a bad clip |

Rough v4 discipline (production note): ~24 normalized clips, last trimmed only, **no freeze pads**, picture bed matched to **equals-v3-full** within ±0.05 s.

Normalize (typical): 1280×720, 30 fps, silent picture bed → mux with master audio → HQ encode for YouTube.

---

## 6. HQ master → YouTube

- Master aim: keepable 720p encode (production used a CRF14-class YT master + lighter twins for review).
- Visibility: **public** once private watch clears.
- Long-form live: https://www.youtube.com/watch?v=Uzl0clxIxqg

Proof bar: private watch **first**, then YouTube + X **together**.

---

## 7. Timed captions

| Fact | Value |
|------|-------|
| Format | SRT (+ VTT twin in production) |
| Cue count | **86** |
| Words | **Locked lyrics only** |
| ASR role | **Whisper / stable-whisper for timing only** |

Method sketch:

1. Vocal stem when full-mix ASR fails on Suno vocals+music.
2. Forced alignment of locked lyric text onto vocals (section windows — global align can drift).
3. Cross-check free transcription on chunks for stitch / outro anchors.
4. Cueing: ~1 line/cue; no overlaps; no instrumental placeholder spam for hush intros/outros.
5. Stitch-aware: captions must respect the double lift/bridge/final performance.

Honest gaps: if a paper line was not sung on the master, **omit** it — do not invent cues.

---

## 8. Shorts → X

- Crop: center 9:16 from 16:9 (Hatch usually frame-center); no burned captions on Shorts files.
- Windows locked to SRT phrase boundaries (± small pad). See [`SHORTS.md`](SHORTS.md).
- X proof post points at the long-form URL and names the pipeline tools at high level.

---

## Lessons transferred from The One True Fairy Tale

1. **Short clips** beat heroic long generations.
2. **Fast select** — decide keepers while energy is hot.
3. **Chip-away** — local surgery, not nuclear regen.
4. **Mood-match, not lip-sync.**
5. **No freeze pads.**
6. **No whole-timeline regen** for a local flaw.
7. Paper before pixels; song clock before vanity length.
8. Human watch loops matter; “leave it” is allowed when cost ≠ worth.

Equals adds: **form lock is sacred**, **full lyrics + deep wubs**, **stitch-aware captions**, and an **equal-proof wager** with a public burn sheet.

---

## What this repo deliberately omits

- Binary video / audio (too large)
- Private local paths, vaults, API keys, emails, phones, addresses
- Live production bot profiles (use the public templates instead)
