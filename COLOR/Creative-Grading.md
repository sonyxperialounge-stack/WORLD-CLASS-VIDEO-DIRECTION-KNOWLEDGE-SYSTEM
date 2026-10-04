# Creative Grading: Designing the Image

**Purpose:** Teach the difference between correcting light and designing it in post; how palette, contrast structure, highlight behaviour, saturation distribution, colour separation and attention combine into a look; how to treat skin with fidelity while allowing stylised departures; and when an invisible grade or an expressive one is right.

**Applies to:** Any project after technical correction.

**Prerequisites:** [Color Management](Color-Management.md), [Correction and Shot Matching](Correction-and-Shot-Matching.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md).

**Companion:** [Texture and Post Relighting](Texture-and-Post-Relighting.md) (local shaping, grain, halation and other texture tools).

---

## 1. Correcting light versus designing light

| | Correction | Creative grading |
|---|---|---|
| Goal | Technical coherence: consistent exposure, balance, matching | Meaning and feeling: how the world of the piece looks |
| Question | "Is this image consistent and accurate to the intended light?" | "What should this image make the viewer notice and feel?" |
| Reference | The scene's light; neutral references; the other shots | The brief, the story, the references by function |
| Success | Nobody notices inconsistencies | The look supports the story — and may or may not be noticed |

Both are design decisions, but correction answers to the material while creative grading answers to the brief. A creative grade built on uncorrected shots becomes a collection of fixes.

## 2. The components of a look

A "look" is not a preset name. It is a set of integrated decisions:

| Component | Decisions | Effect |
|---|---|---|
| Palette | Which hues dominate; which are suppressed; accent colours | World identity; mood; brand |
| Contrast structure | Overall contrast; where the midtones sit; shadow density; highlight brightness | Weight, drama, softness, clarity |
| Highlight behaviour | Hard clip vs gentle roll-off; colour of highlights | Filmic softness, digital crispness, warmth, coolness |
| Saturation distribution | Which tonal ranges and hues are saturated (e.g., saturated midtones, desaturated shadows) | Richness vs restraint; where colour draws attention |
| Colour separation | Hue difference between subject and background, between skin and environment | Depth; clarity; focus |
| Attention | Brightness, saturation and contrast concentrated on the subject | Guides the eye (see [Continuity and Attention](../EDITING/Continuity-and-Attention.md#6-eye-trace)) |

These are interdependent: raising contrast also raises perceived saturation; cooling shadows changes how skin in shadow looks; brightening the subject's area reduces background attention.

## 3. Invisible versus expressive grades

| | Invisible grade | Expressive grade |
|---|---|---|
| Viewer awareness | Not noticed; the image looks "natural" | Noticed as a deliberate world |
| Fits | Observational documentary, testimony, instructional content, many corporate and news contexts | Music videos, fashion, stylised brand work, genre fiction, subjective sequences |
| Risk | Can look flat or "uncorrected" if confused with no grade | Can overwhelm the content; can misrepresent reality in factual work |

An invisible grade is still a grade: it balances, shapes attention, and makes the image feel truthful. It is right for observational realism because a visible stylisation signals interpretation where the contract promises observation. The same restraint is wrong for strongly expressive work, where a neutral grade makes the piece feel unfinished or generic.

**Factual work caution:** grading can change perceived facts — making a place look dirtier, a crowd look more menacing, a face look more ill. In documentary, grade to represent the scene as experienced, not to argue a point.

## 4. Skin fidelity and departures

Viewers are highly sensitive to skin rendering. Principles:

- **Fidelity first:** keep skin plausible for the person and the light (see [Correction and Shot Matching](Correction-and-Shot-Matching.md#3-scopes-as-diagnostic-aids)).
- **Contextual cast is legitimate:** lamplight warms, moonlight-convention cools, neon colours. Skin carrying the scene's light reads as being *in* the scene.
- **Stylised departure** is acceptable when it serves the scene and remains respectful — e.g., a music video drenched in red light — but avoid careless complexion distortion.
- **Cultural assumptions:** do not "lighten" darker skin as an aesthetic default, or push all skin toward one ideal. Different complexions need different exposure and contrast to show richness and detail. Check with people familiar with how subjects want to be represented.
- **Brand colour requirements:** product colours may need to be accurate; skin and product may pull the grade in different directions. Isolate the product for accuracy if necessary.

### Criteria for a skin departure that serves the scene

1. The departure is motivated by the scene's light or the piece's stated style.
2. It is consistent across shots of the scene.
3. The person remains recognisable and is not made to look ill, aged or "other" unintentionally.
4. Skin detail and density are preserved (not waxy or grey).
5. A reviewer familiar with the subject agrees it represents them acceptably.

## 5. LUTs and instinct in creative work

A creative LUT can establish a look quickly and consistently. Risks: it was made for different footage; it fixes decisions that should vary by scene; its strength overwhelms skin. Practice `[Practice]`:

- Place a creative LUT after correction and before final trims, at partial strength if needed.
- Adjust per scene around it; don't force every shot through it unchanged.
- Build looks from understood operations (contrast, hue shifts, saturation by range) when possible, so they can be adjusted.

## 6. Worked example 1 — A restrained documentary grade (hypothetical, Project A "Second Shift")

**Brief:** truthful, respectful, unhurried; no beautification of fatigue; night should feel like night, dawn like relief.

| Scene | Hypothetical input (after correction) | Decision | Rationale |
|---|---|---|---|
| Day interview | Window-lit, soft, slightly warm, natural contrast | Very light grade: gentle contrast; skin warm-natural; background shelf slightly darker via a soft vignette-like window | Intimacy and focus without style |
| Night ward | Fluorescent green tint (corrected), noisy shadows, warm desk lamp | Keep a slight cool-neutral overall, lamp warm; let shadows be dark but retain detail in faces and hands; do not remove all green — a hint keeps the institutional feel | Truthful to the place; avoid a "thriller" teal or a cosy amber |
| Emergency | Handheld, mixed light, motion blur | No added stylisation; consistency priority | Factual contract; avoid dramatising |
| Dawn | Blue window light rising, generator stops | Allow the cool dawn to read; skin slightly warmer than the window | Relief through light change, not through saturation |
| End card | Graphic over a dark frame | Graphic colours verified on output | Brand of the nonprofit |

**Before/after decision description (hypothetical):** before grading, the night ward looks greenish, flat and noisy; after correction and the light grade, it looks like a dim institutional ward at night with a warm lamp at the nurses' station, faces readable, shadows dark but not crushed; noise reduced moderately and texture kept (see [Texture and Post Relighting](Texture-and-Post-Relighting.md)).

**Rejected alternative:** a desaturated, crushed "gritty documentary" look — it would editorialise exhaustion and make Asha's world look more grim than she describes it.

**Verification:** compare the grade to the director's and Asha's memory of the place (if she reviews the film); watch on a phone and projector; ensure the film's emotional arc (night → dawn) is perceptible in light without being forced.

## 7. Worked example 2 — A stylised brand scene (hypothetical, Project B "Arc" 30-second spot)

**Brief:** calm confidence; warm-neutral studio; the lid ring's glow is the hero.

| Component | Decision |
|---|---|
| Palette | Warm-neutral whites and soft greys; muted wood tones; the ring's brand colour is the strongest saturated accent in the frame |
| Contrast | Moderate contrast with clean, slightly lifted (not milky) blacks; highlights roll off gently on the steel |
| Saturation distribution | Low saturation in backgrounds; natural skin; saturation reserved for the ring |
| Separation | Product slightly brighter and cleaner than background; background slightly warmer |
| Attention | A subtle local brightness boost around the lid in the reveal shot |
| Morning montage | Slightly cooler and busier, so the warm calm of the product moment contrasts |
| Brand colour | Ring colour measured against the brand specification on the SDR output; isolated and protected from global adjustments |

**Before/after (hypothetical):** before, the studio looks clinically white and the ring's colour slightly clipped in one channel; after, the studio feels warm and calm, the ring reads as a precise, glowing accent without clipping, and the montage's cooler tone makes the product moment feel like arriving somewhere calm.

**Verification:** brand lead approves product and ring colour on calibrated display and on representative phones; fresh viewers describe the spot with words like "calm" and "clean".

## 8. Counterexample and repair — the preset that distorted skin

**Hypothetical counterexample.** A short documentary about a fishing village uses a popular teal-and-orange creative preset across all footage. The sea becomes saturated teal; skin becomes orange; the villagers' darker complexions turn an unnatural copper; shadows go cyan. A community screening produces uncomfortable laughter; a villager says, "We don't look like that."

**Diagnosis:** a stylised preset from a different genre contract applied to factual material; complexion distortion; skin used as an aesthetic element rather than a person's appearance.

**Repair:**
1. Remove the preset; return to the corrected baseline.
2. Build a restrained look: natural skin rendered with density; the sea's colour as recorded (it was grey-green on the overcast days, blue on sunny ones); shadows neutral.
3. Keep a gentle palette consistency across days (slight warmth) without imposing hues.
4. Review with community members.

**Verification:** villagers confirm they look like themselves; the film still looks consistent and finished.

## 9. Scope compliance is not taste

A grade can be within all technical limits — no clipping, legal range, consistent skin — and still be wrong for the film. Conversely, an expressive grade may deliberately push into deep blacks or strong colours. Scopes verify technical boundaries; the brief and the story verify taste. The [Creative Coherence and Taste](../FOUNDATIONS/Creative-Coherence-and-Taste.md) chapter discusses how to evaluate whether the grade belongs to the whole piece.

## 10. Micro-decisions

- Grade the hero shot of each scene to the look first, then propagate and adjust.
- Make looks from adjustable operations; save versions.
- Check the look at the start, middle and end of the programme on a fresh day.
- Watch the grade with sound; sound changes how images feel.
- Check graphics and captions after the grade; contrast may change.
- When a client asks for "more cinematic", ask which component: contrast, palette, highlights, darkness? (See [Review and Revisions](../OPERATIONS/Review-and-Revisions.md).)

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "Looks like a filter" | Preset/LUT applied without adaptation | Build look from adjustable operations; reduce strength |
| Orange skin, teal everything | Aggressive complementary look | Protect skin; reduce hue shifts |
| Product colour wrong | Global look affects brand colour | Isolate and protect |
| Night looks like day | Over-correction to "visible" | Restore darkness with readable faces |
| Grade fights story | Look from a different genre | Re-derive from brief and contract |
| Inconsistent look across scenes | Look applied per shot without hierarchy | Scene hero shots; consistent nodes/layers |

## 12. Verification

- In motion, at full speed, across scene cuts.
- After resizing and encoding (compression changes gradients and saturation).
- With sound and story intact.
- On calibrated and consumer displays.
- Skin reviewed by people familiar with the subjects where possible.

## Dependencies

- Depends on: [Color Management](Color-Management.md), [Correction and Shot Matching](Correction-and-Shot-Matching.md), [Reference Analysis](../FOUNDATIONS/Reference-Analysis.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md).
- Companion: [Texture and Post Relighting](Texture-and-Post-Relighting.md).
- Coherence: [Creative Coherence and Taste](../FOUNDATIONS/Creative-Coherence-and-Taste.md).

## Confidence summary

Look components and their interactions are `[Practice]`. Invisible-versus-expressive guidance by genre is a `[Heuristic]`. Skin fidelity principles and avoiding complexion distortion are `[Practice]` with ethical grounding. Specific looks are `[Preference]` and `[Illustrative]`.
