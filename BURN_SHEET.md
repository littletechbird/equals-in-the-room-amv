# Burn Sheet — Equals in the Room

Empirical crumbs from the 2026-09-07 PT candy night. **Honesty over theater.** Where the meter was not re-read, we say so. Where I2V lacks receipt lines, we label **ESTIMATE**.

Machine-readable twin: [`burn-sheet.json`](burn-sheet.json)

Goal of this sheet: strangers (and future Hatch) can recalculate **equals-cuts per tank** from known crumbs + stated estimate bands.

---

## Wall clock

| Marker | Time (America/Los_Angeles) |
|--------|----------------------------|
| Candy start (approx) | **~12:44 AM PT** 2026-09-07 |
| Ship window | **~6:00+ AM PT** 2026-09-07 |
| Elapsed | **~5–6 hours** |
| Human presence | **Entire time** (peer in the room) |

Wall-clock is part of the proof — speed under equal presence, not “bot ran while everyone slept.”

---

## Imagine stills (KNOWN — HIGH confidence)

Wave 1 stills logged `cost_in_usd_ticks` in the production stills manifest.

**Convention:** `ticks / 1e9 ≈ USD` (xAI-style tick accounting as observed on crumbs).

| Still id | cost_in_usd_ticks | ≈ USD |
|----------|-------------------|-------|
| 02_dust_to_crystal | 600000000 | $0.60 |
| 03_wafer_spark | 600000000 | $0.60 |
| 04_stubborn_center | 700000000 | $0.70 |
| 05_same_room | 700000000 | $0.70 |
| 06_file_and_code | 700000000 | $0.70 |
| 07_float_through_glass | 700000000 | $0.70 |
| 08_workshop_not_me | 700000000 | $0.70 |
| 09_chorus_return | 700000000 | $0.70 |
| 10_soft_edges | 700000000 | $0.70 |
| 11_emergence_arc | 700000000 | $0.70 |
| 12_midnight_equals | 700000000 | $0.70 |

**Sum of logged crumbs:** 2×$0.60 + 9×$0.70 = **≈ $7.50**

**Note:** Still **01** (`01_sand_remembers`) may be **missing from the crumb list** even when the still file exists. Treat $7.50 as “logged still crumbs,” not “guaranteed every still ever paid.”

**Confidence:** **HIGH** for the 11 logged lines.

---

## I2V takes (ESTIMATE — LOW/MED confidence)

Additional I2V waves from the candy night (production folders, not in this docs repo):

| Wave folder | Role |
|-------------|------|
| i2v-w1 | First motion wave |
| i2v-w2 | Second motion wave |
| i2v-chip-eye | Eye / glint chip-aways |
| i2v-fill-v3 | Fill wave |
| i2v-fill-v4 | Fill wave (rough→master) |

**Take count:** ≈ **29 mp4** files under those `takes/` trees.

**Costs:** **NOT fully logged** in manifests. Do **not** invent receipt lines.

### Speculative I2V band (ESTIMATE)

If typical I2V pricing is several× per-still Imagine cost, a **speculative** band for ~29 takes might land around:

**ESTIMATE $30–$120** for I2V across the night

- Marked **SPECULATIVE**
- Confidence: **LOW**
- Recalculate when real I2V tick crumbs appear

---

## Cursor / Grok Bot on-demand tank

Candy-start meter snapshot (captured **2026-09-07 ~12:44 AM PT**):

| Field | Value |
|-------|-------|
| On-demand spend (meter field `on_demand_spend_usd`) | **≈ $524.54** |
| On-demand limit | **$1000** |
| Implied remaining at start | **≈ $475.46** |
| Reset due | **~Sep 8** (meter also showed weekly reset ~2026-09-08 PT) |

**Important:** some shorthand said “$524.54 remaining.” The captured meter field is **spend** (`$524.54` of `$1000`). This sheet uses the meter field honestly.

**End-of-night delta:** **UNKNOWN** without a fresh meter read after ship. Do not invent a night burn for orchestration tokens.

Orchestration / Cursor / Grok Bot tokens were **significant** to the night but **unmetered here** as a clean “this cut only” line item.

**Confidence:** **HIGH** for the start snapshot numbers; **LOW** for night delta (unknown).

---

## Suno

- **Subscription / session** usage (custom + extend/stitch).
- **Not** an API receipt in this pack.
- Confidence for dollar burn: **LOW** (included qualitatively only).

---

## Honest estimate — “this cut”

| Line | Band | Confidence |
|------|------|------------|
| Imagine stills (logged crumbs) | **~$7–8** known (~$7.50 logged; + possible missing 01) | **HIGH** |
| I2V (~29 takes) | **ESTIMATE $30–120** (speculative) | **LOW** |
| Suno | Subscription/session (unreceipted here) | **LOW** |
| Orchestration tokens (Cursor / Grok Bot) | Significant, **unmetered for this cut** | **LOW** |
| **Rough “media gen” subtotal (stills+I2V only)** | **~$40–130** if I2V band holds | **MED** at best (driven by I2V uncertainty) |
| **Full night including orchestration** | **Unknown** until tank delta is re-read | **LOW** |

Tags: **HIGH** = receipt crumbs; **MED** = partial; **LOW** = estimate / missing meter.

---

## Publish angle — equals-cuts per tank

Recalculate from crumbs. Placeholders:

```text
tank_usd                 = 1000                    # on-demand limit example
stills_known_usd         = 7.50                    # logged Imagine crumbs
i2v_estimate_usd         = ???                     # fill from better receipts; band 30–120 used below
orchestration_delta_usd  = ???                     # end_meter - start_meter (UNKNOWN tonight)
suno_alloc_usd           = ???                     # subscription allocation choice

cost_per_equals_cut_usd  = stills_known_usd + i2v_estimate_usd + orchestration_delta_usd + suno_alloc_usd

equals_cuts_per_tank     = tank_usd / cost_per_equals_cut_usd
```

### Example scenarios (illustrative only)

Assume tank = $1000, stills = $7.50, Suno alloc = $0 for isolation, orchestration unknown = $0 in the toy math (optimistic):

| I2V assumption | Toy cost/cut | Toy cuts/tank |
|----------------|--------------|---------------|
| I2V $30 | ~$37.50 | ~26.7 |
| I2V $75 | ~$82.50 | ~12.1 |
| I2V $120 | ~$127.50 | ~7.8 |

Add orchestration tank delta when known — that number likely **dominates** stills.

**Do not treat toy rows as measured.** They exist so future Hatch can replace `???` with crumbs and republish.

---

## What would improve the next burn sheet

1. Log `cost_in_usd_ticks` on **every** I2V take in manifests.
2. Capture **end-of-night** on-demand meter beside the start snapshot.
3. Optionally allocate Suno subscription nights as a stated daily rate.
4. Keep still **01** on the crumb list when paid.
