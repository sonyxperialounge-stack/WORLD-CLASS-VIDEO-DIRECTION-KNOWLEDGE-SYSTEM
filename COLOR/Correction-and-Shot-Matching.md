# Technical Correction and Shot Matching

**Purpose:** Teach primary correction — exposure, white balance and tint, contrast, saturation, black and white relationships — in the context of scene lighting, skin and camera response; how to read scopes as diagnostic aids; how to match shots and cameras while preserving intentional lighting differences; and how to evaluate LUTs.

**Applies to:** Every graded project, from a quick single-operator pass to a full colour session.

**Prerequisites:** [Color Management](Color-Management.md) (interpretation must be correct first).

**Companion chapters:** [Creative Grading](Creative-Grading.md) (looks), [Texture and Post Relighting](Texture-and-Post-Relighting.md) (local shaping and texture).

---

## 1. Correction before creation

Correction makes images **technically coherent and consistent**: exposure placed sensibly, white balance intended, black and white levels within range, cameras matched, skin plausible. Creative grading then shapes look and emotion. Doing creative work on uncorrected shots means fighting inconsistencies forever — each shot needs a different version of the look.

**Diagnose interpretation before secondaries.** If a shot looks wrong, check the input transform and range before reaching for qualifiers, masks or hue curves (see [Color Management](Color-Management.md#7-classic-interpretation-mistakes)).

## 2. The primary controls and what they fix

| Control | What it adjusts | Observe | Common mistake |
|---|---|---|---|
| Exposure / offset | Overall brightness (ideally in a scene-referred way) | Faces and key subjects at a plausible level for the scene | Exposing every shot to the same brightness, erasing night/day differences |
| White balance / temperature | Warm–cool axis | Neutral references (white walls, grey cards) relative to intended light | Neutralising deliberate warm practicals |
| Tint | Green–magenta axis | Skin under fluorescent/LED; foliage | Ignoring tint and fixing only temperature |
| Contrast (with pivot) | Spread of tones around a midpoint | Scene's intended contrast; shadow and highlight detail | Increasing contrast until shadows crush story detail |
| Black level / lift | Darkest tones | Whether blacks are truly black, milky or crushed | Lifting blacks to "see detail" and losing density |
| White level / gain | Brightest tones | Highlights and speculars | Clipping highlights in the grade |
| Saturation | Colour intensity overall | Natural colour for the scene | Raising saturation globally, oversaturating skin and LEDs |
| Curves | Tonal and colour shaping in ranges | Specific tonal relationships | Complex curves for problems better solved by primaries |

**Order of primary operations** `[Heuristic]`: exposure and white balance first (they change everything else), then contrast and black/white relationships, then saturation. Revisit as needed; primaries interact.

## 3. Scopes as diagnostic aids

| Scope | Shows | Use it to | It does not tell you |
|---|---|---|---|
| Luma waveform | Brightness distribution across the image width | Exposure placement; clipping; crushed shadows; consistency between shots | Whether the brightness is right for the story |
| RGB parade | Each channel's waveform side by side | Colour casts (channels misaligned on neutral areas); channel clipping | Whether a cast is intended |
| Vectorscope | Hue (angle) and saturation (distance from centre) | Overall casts; saturation extremes; skin hue relative to the skin-tone reference line | Whether a person's skin is "right" — skin varies |
| Histogram | Distribution of values | Overall exposure distribution | Spatial information |
| False colour | Brightness ranges mapped to colours | Quick exposure checks on faces | Colour accuracy |

### The skin-tone line is a diagnostic aid, not a command

Many vectorscopes display a reference line along which a wide range of human skin hues tend to fall under neutral light `[Practice]`. It helps diagnose obvious casts (all faces drifting toward green). It is **not** an instruction to force every person's skin onto the line:

- Skin varies in hue and saturation between people, ethnicities, individuals and even areas of the same face.
- Lighting legitimately colours skin: warm lamplight makes skin warmer; a cool window makes it cooler. Forcing it "onto the line" removes the scene's light.
- Makeup, flush, tan and health change skin colour.

Use the line to ask a question ("Is this face greener than the light explains?"), then answer it by looking.

## 4. Shot matching

### 4.1 Method

1. **Choose a reference (hero) shot** for each scene — usually the best-exposed, most representative shot, often the master or the main interview angle.
2. **Correct the reference** to the intended baseline.
3. **Match other shots to it**, comparing side by side (split screen or gallery) and with scopes on corresponding areas (skin to skin, wall to wall, sky to sky).
4. **Match in order:** exposure → white balance/tint → contrast → saturation → specific hues.
5. **Watch in sequence** at full speed: matching is judged in time across cuts, not only in split screens.

### 4.2 Matching across cameras

Different cameras record colour differently (sensor response, processing, gamut). Even with correct input transforms, they will differ. Typical differences: skin hue rendering, saturation of reds and greens, highlight roll-off, noise texture, sharpness.

| Difference | Correction approach | Limit |
|---|---|---|
| Overall exposure and balance | Primaries | Usually fully correctable |
| Skin hue rendering | Targeted hue adjustment on skin range (secondary) | Over-adjustment creates plastic skin |
| Saturation behaviour in specific hues | Hue-vs-saturation curves | Can create banding in 8-bit sources |
| Highlight roll-off | Highlight compression; soft clip | Clipped data can't gain detail |
| Noise and sharpness | Texture matching (see [Texture and Post Relighting](Texture-and-Post-Relighting.md)) | Different sensors can't become identical |

### 4.3 Preserve intentional lighting differences

Matching does not mean making everything identical. In a scene with a warm lamp on one side and a cool window on the other, a character turning from one to the other *should* change colour. A dawn scene should be cooler than the night interior before it. Before "correcting" a difference, ask whether it is **story information** (time, place, light source) or **a technical inconsistency** (camera mismatch, auto white balance shift).

## 5. LUT evaluation

LUTs (and similar fixed transforms) can be technical (converting encodings) or creative (applying a look). Evaluate a LUT before relying on it:

| Criterion | Question | Test |
|---|---|---|
| Intended input | Which camera, curve, gamut and range does it expect? | Read its documentation/name; test on the correct source |
| Intended output | Which display standard does it produce? | Check against the output pipeline |
| Role | Technical conversion, creative look, or both combined? | Combined LUTs are hard to adjust; separate if possible |
| Exposure tolerance | Does it behave well if footage is a stop over or under? | Apply to bracketed test footage |
| Clipping | Does it clip highlights or shadows that the source contains? | Waveform before and after |
| Gamut behaviour | How does it handle saturated colours (LEDs, neon, flowers)? | Test on a saturated chart or scene |
| Strength | Can it be blended or reduced? Does it overwhelm skin? | Apply at partial strength |
| Placement | Where in the node/layer order? Corrections before or after it behave differently | Test both positions |

**LUT versus instinct:** neither automatically wins. A well-made technical LUT gives a consistent, tested starting point; uncalibrated instinct on an uncalibrated display can wander. A creative LUT applied blindly can look generic and break on some shots. Use LUTs as known transforms, and judgement to adapt.

## 6. Worked example 1 — Mixed-camera interview match (hypothetical, Project A, 25 fps)

**Sources:** A-cam (mirrorless, log, 10-bit, correct input transform) and B-cam (phone, display-referred, conformed CFR). Window-lit interview.

**Observed differences (hypothetical):**

| Aspect | A-cam (reference) | B-cam (phone) |
|---|---|---|
| Exposure | Face at an appropriate level; window soft roll-off | Face slightly brighter; the window clips earlier |
| White balance | Slightly warm, as the window light was overcast-neutral and the grade chose mild warmth | Cooler, with a slight green tint |
| Contrast | Moderate | Higher (phone processing) |
| Saturation | Natural | Higher in reds |
| Texture | Fine grain-like noise | Smoother, with sharpening halos |
| Exposure change | — | A brief exposure dip when someone passed the window (auto-exposure; see [Capture Decisions](../CAMERA/Capture-Decisions.md#11-counterexample-and-repair--the-auto-phone-b-cam)) |

**Correction steps for the B-cam:**
1. Exposure: lower slightly to match face brightness on the waveform (same area on both).
2. White balance and tint: warm slightly and remove green using the white wall and the vectorscope; compare skin side by side.
3. Contrast: reduce, with a softer highlight roll-off to approach the A-cam's window rendering (the clipped window cannot gain detail; reduce its brightness slightly so it doesn't draw attention).
4. Saturation: reduce reds selectively.
5. Exposure dip: a keyframed exposure correction over the dip.
6. Texture: reduce sharpening halos with gentle softening; add fine grain to match (see [Texture and Post Relighting](Texture-and-Post-Relighting.md)).

**Verification:** cut A → B → A at full speed in the interview; the change of angle should be noticed, the change of camera should not. Check skin on a phone and on the grading monitor.

## 7. Worked example 2 — A deliberately mixed-temperature scene (hypothetical, Project D)

**Scene:** warm practical lamps on the siblings; cool streetlight through the window as background accent (see [Practical Setups](../LIGHTING/Practical-Setups.md#3-worked-example-2--night-interior-with-practical-fixtures-hypothetical-project-d-the-spare-key-23976-fps-150-s)).

**Correction goals:**
- Skin under the lamps: warm but not orange; plausible for each actor's complexion.
- The streetlight: clearly cooler, to preserve the separation and the night.
- Consistency between Nisha's and Ravi's singles: each lit by a different lamp — some difference is truthful (two lamps), but skin rendering must not jump between cuts.

**Process:**
1. Set the white balance so the lamp-lit skin is warm but natural; do not neutralise the lamps.
2. Check the vectorscope: Nisha's and Ravi's skin hues sit close to each other but differ slightly (different complexions and lamps); the difference is accepted if it reads as different light, not different cameras.
3. Protect the cool window with a qualifier if global warming shifts it toward neutral.
4. Match Ravi's floor-lamp side to Nisha's table-lamp side in exposure so the scene does not "pump" between cuts.

**Rejected alternative:** neutralising both siblings' skin to the skin line and making the window neutral — technically "correct", but erases the night interior's warmth and the cool exterior that gives depth.

**Verification:** full-scene playback; fresh viewers asked "what time is it and where is the light coming from?" should answer "night, lamps" without prompting.

## 8. Counterexample and repair — skin and lighting mismatch

**Hypothetical counterexample.** In a corporate panel discussion shot with three cameras, the colorist matches all speakers' skin to the vectorscope skin line using a skin qualifier on every shot. One speaker with deeper skin now looks ashen and slightly grey; another, lit by a warm stage light, looks pasted into the scene because her skin is neutral while the warm light is visible on her clothes and the table.

**Diagnosis:** a diagnostic aid was used as a target; skin was corrected independently of the scene's light and individual complexions.

**Repair:**
1. Remove the skin qualifiers.
2. Correct each camera's primaries to the scene's light using neutral references in the set (a white table, a grey panel backdrop).
3. Assess each speaker's skin by eye on a calibrated display, in context; apply small skin adjustments only where a camera's rendering is wrong (e.g., a green cast on one camera), not to impose a standard hue.
4. Check deeper skin tones for density and richness, avoiding lifting into grey; check lighter skin tones for pink/orange exaggeration.

**Verification:** a reviewer familiar with the speakers confirms they look like themselves; side-by-side with the set's neutral references shows consistent light.

## 9. Micro-decisions

- Match skin first, then everything else around it; viewers forgive many colour errors before skin errors.
- Use the same area for comparisons (forehead to forehead, wall to wall).
- Set black levels deliberately per scene; a night scene can have deep blacks while an overcast exterior has softer ones.
- Leave headroom for creative grading; don't push corrections to the limits.
- Use a still store or gallery of reference frames for each scene.
- Recheck matches after the creative grade; looks can reintroduce differences.

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Faces change colour between cuts | Camera mismatch; auto white balance | Match primaries; targeted skin adjustment |
| Milky blacks | Lifted blacks; range mismatch | Correct black level; check range |
| Crushed shadows lose story detail | Too much contrast | Lower contrast; lift shadow region gently |
| Oversaturated reds/LEDs | Global saturation; camera rendering | Selective saturation; gamut mapping |
| Night scenes look like day | Exposure normalised across all shots | Restore scene-appropriate exposure |
| Skin looks "corrected", not alive | Forced to skin line | Correct to light; respect individual skin |

## 11. Verification

- Shot-to-shot continuity at full speed in sequence.
- Scope checks on corresponding areas.
- Image intent: lighting differences that carry story are preserved.
- Destination transforms: check corrections under every required output (SDR/HDR) — see [Color Management](Color-Management.md).

## Dependencies

- Depends on: [Color Management](Color-Management.md), [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md), [Capture Decisions](../CAMERA/Capture-Decisions.md).
- Companion: [Creative Grading](Creative-Grading.md), [Texture and Post Relighting](Texture-and-Post-Relighting.md).
- Feeds: [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Primary controls, scope functions and the reference-shot matching method are `[Practice]`. The skin-tone reference line's usefulness as a diagnostic and its unsuitability as a universal target are `[Practice]`. Order of operations is a `[Heuristic]`. LUT evaluation criteria are `[Practice]`. Examples are `[Illustrative]`.
