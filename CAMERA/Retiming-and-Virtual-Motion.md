# Retiming, Speed Ramps and Virtual Camera Motion

**Purpose:** Teach how to change the speed of recorded time — slow motion, fast motion, ramps — and how to create or modify camera movement in post — reframing, stabilisation, 2.5D parallax, virtual cameras — with honest limits on what interpolation and flat images can supply.

**Applies to:** Edit and finishing stages for any footage; planning at acquisition.

**Prerequisites:** [Capture Decisions](Capture-Decisions.md) (capture rate and shutter), [Motivated Movement](Motivated-Movement.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#5-mixed-rate-footage).

**Related owners:** Motion curves and easing in [Animation Grammar](../MOTION-DESIGN/Animation-Grammar.md); photoreal integration in [Compositing and Integration](../VFX/Compositing-and-Integration.md); generated motion in [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md).

---

## 1. What retiming is for

Changing speed changes how viewers perceive an action:

| Purpose | Speed change | Example |
|---|---|---|
| Make a fast action readable | Slow motion | Water stream entering a bottle; a hand catching a falling object |
| Emphasise a moment's significance | Slow motion, often brief | A look; a product moment |
| Compress time | Fast motion, time-lapse, speed-up | A filter emptying over hours |
| Create energy and transition | Speed ramps | Ramp from real time into slow for an impact, then back |
| Convey subjective time | Slow or variable speed | A character's shock |
| Smooth an unstable or awkward moment | Slight slow-down | Rare; risky in factual work |

**A dramatic acceleration does not automatically create excitement.** Speed ramps became a fashionable shorthand for energy; overused, they erase the action they were meant to emphasise (the important moment happens during the fast part) or become a distraction that announces "edited". The test is always: *after the ramp, can the viewer describe what happened, and does it feel more important than before?*

## 2. Capture-rate headroom

Real slow motion requires frames that were captured. A clip shot at the timeline rate (e.g., 25 fps) slowed to 50% must invent half of its frames; one shot at 50 fps can play at 50% using real frames.

| Captured at | Timeline | Clean slow motion available (real frames) |
|---|---|---|
| 25 fps | 25 fps | None (100% only) |
| 50 fps | 25 fps | Down to 50% |
| 59.94 fps | 23.976 fps | Down to 40% |
| 119.88 fps | 23.976 fps | Down to 20% |

Below the captured headroom, frames must be synthesised (Section 3).

### Shutter and blur in retimed footage

The motion blur recorded in each frame depends on the capture shutter (see [Capture Decisions](Capture-Decisions.md#2-shutter-motion-blur-and-the-180-degree-convention)). A slow-motion clip shot with a short shutter looks crisp when slowed. If part of a ramp returns to real time, the same short shutter makes real-time motion look staccato. Remedies: add synthetic motion blur during real-time portions (with care), choose a slightly longer shutter as a compromise if the ramp is planned, or capture real-time and slow-motion passes separately.

## 3. Methods of retiming and their artefacts

| Method | How it works | Good for | Artefacts |
|---|---|---|---|
| Frame sampling (repeat/drop) | Repeats or skips whole frames | Speeds that divide evenly; deliberately stepped looks | Stutter when slowing beyond headroom |
| Frame blending | Mixes adjacent frames | Small speed changes; dreamy effects | Ghosting/double images |
| Optical flow / motion-compensated interpolation | Estimates motion vectors and synthesises in-between frames | Smooth slow motion of simple motion | Warping around occlusions (things passing in front of others), edges, hands and fingers, spinning wheels, water, hair, transparent or reflective objects, motion blur |
| Machine-learning frame interpolation | Learned models synthesise frames | Often better than classic optical flow on complex motion | Plausible but invented details; temporal shimmer; face and hand deformation; still fails on complex occlusion |

**Factual work caution:** synthesised frames contain invented image content. In documentary or evidential contexts, heavy interpolation can create details that never existed (a hand position, a facial expression). Use real frames or modest retiming; disclose stylisation where it changes perception (see [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md)).

## 4. Designing a speed ramp

1. **Identify the moment of emphasis** — the frame range that must be seen clearly.
2. **Keep that moment within the slow section**, with time to read it.
3. **Place ramp transitions in less important parts** of the action (the approach, the follow-through).
4. **Shape the ramp curve**: abrupt ramps feel percussive; eased ramps feel fluid. Match to the piece's motion grammar (see [Animation Grammar](../MOTION-DESIGN/Animation-Grammar.md)).
5. **Plan sound**: production audio cannot simply be slowed (pitch drops; artefacts). Options: silence during the slow section, designed sound (a whoosh into slow, a low sustained tone), time-stretched ambience, or music carrying the moment. Re-sync sound at the end of the ramp.
6. **Check total duration**: ramps change length; music and captions downstream must be re-checked.

## 5. Post-production camera movement

### 5.1 Reframing and digital moves

Cropping into a higher-resolution source allows reframing, punch-ins and digital pushes or pans.

| Consideration | Detail |
|---|---|
| Crop budget | The amount you can crop before quality falls below delivery needs: e.g., a UHD (3840×2160) source can be cropped to about 50% width for an HD (1920×1080) delivery without upscaling. Compression, noise and lens sharpness also limit useful crop |
| Digital push ≠ dolly | A digital push magnifies the image uniformly — no parallax. It resembles a zoom, not a camera moving through space |
| Body language and context | Reframing removes context (see [Continuity and Attention](../EDITING/Continuity-and-Attention.md#10-crop-and-reframe-meaning-changes-with-the-frame)) |
| Motion blur | Digital moves add no natural motion blur; fast digital moves need synthetic blur to look camera-like |

### 5.2 Stabilisation

Stabilisation tracks motion and counter-moves the frame, cropping edges.

| Problem | Cause | Mitigation |
|---|---|---|
| Edge warping / wobble | Rolling shutter skew corrected imperfectly; lens distortion; parallax not modelled | Lower strength; rolling-shutter correction; accept some motion |
| "Floating" drift | Over-smoothing removes intended movement | Use smoothing that preserves intentional moves |
| Blurred frames in a stable image | Motion blur recorded during shake remains when the shake is removed | Less stabilisation on blurred sections; cut around them |
| Crop loss | Stabilisation requires margin | Plan resolution headroom |

### 5.3 2.5D parallax from stills

A "2.5D" move separates a still image into layers (foreground, subject, background) and moves them at different speeds to simulate camera movement through space. Depth maps (manual or AI-estimated) can automate layering.

**Limits — a flat still cannot supply unseen geometry:**
- When a foreground layer moves, the background behind it must be revealed; that area was never photographed. It must be painted or generated (inventing image content).
- Depth maps make errors at hair, glass, fine detail and edges, producing stretching and tearing.
- Large moves expose flatness: objects behave like cardboard cut-outs.
- Lighting and reflections stay fixed while perspective appears to change — subtly wrong.

Use small moves, mask edges carefully, and in factual work disclose or avoid invented areas in evidential images.

### 5.4 Virtual cameras

Fully 3D virtual cameras (in 3D animation, game engines or projected 3D reconstructions) can perform any move. To sit with live action they must respect the same lens behaviour, motion blur, depth of field, grain and acceleration characteristics as the real camera. A virtual move with infinitely smooth, robotic acceleration and perfect sharpness reveals itself next to handheld footage — synthetic-camera inconsistency.

## 6. Worked example 1 — The product pour ramp (hypothetical, Project B "Arc", 23.976 fps timeline)

**Material:** pour into Arc captured at 119.88 fps with a 1/240 s shutter (see [Capture Decisions](Capture-Decisions.md#10-worked-example-2--high-frame-rate-product-pour-hypothetical-project-b-23976-fps-timeline)); real-time pass at 23.976 fps also captured.

**Options:**

| Option | Description | Evaluation |
|---|---|---|
| A. Real time only | The 23.976 pass | Clean, honest; the pour is quick and less sensory |
| B. Ramp: real time → 20% for the stream entering → real time | Classic ramp | The stream is beautiful; ramp transitions risk looking showy; real-time portions from 119.88 footage look staccato (short shutter) |
| C. Continuous 40% slow motion of the pour (no ramp) | Calm, sensory | Fits "calm confidence"; no staccato problem because the whole shot is slow |
| D. Cut from real-time hand (23.976 pass) to a 20% slow insert of the stream | Two shots; a cut instead of a ramp | Avoids ramp artefacts; combines natural blur with sensory slow insert |

**Choice:** **D** for the 30-second spot (precise, calm, sensory without spectacle); **C** for the 90-second brand film's slower rhythm. B rejected: it reads as a fashionable effect at odds with the brand stance, and the real-time portions look staccato.

**Sound:** the slow insert uses a designed, softened pour sound rather than slowed production audio; the real-time hand shot uses Foley.

**Verification:** full-speed playback with music; ask fresh viewers to describe the product's personality; compare with option B in an A/B.

## 7. Worked example 2 — A still-image move with limited geometry (hypothetical, Project A)

**Material:** a scanned 1990s photograph of the district hospital ward from the hospital's archive (licensed for use; alteration permitted for "reasonable cropping and movement" per the agreement — confirmed in [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md)).

**Intent:** a brief historical reference — "the ward has looked like this for decades" — under Asha's line about how little has changed.

| Option | Effect | Evaluation |
|---|---|---|
| A. Static hold | Honest, archival | Fine; slightly abrupt in an otherwise moving film |
| B. Slow digital push (≈5% over 6 s) | Gentle attention, like leaning in | Honest — no invented content; resolution sufficient |
| C. 2.5D parallax (separate the nurse in foreground from the beds behind) | Dimensional, "documentary style" | Requires painting the area behind the nurse; depth errors at her hair; invents image content in a historical photo |

**Choice:** **B.** The move adds gentle emphasis without inventing image content. **Disclosure:** none needed for a simple push; a 2.5D treatment with painted areas would warrant at least internal documentation and, depending on the commissioner's standards, disclosure.

**Verification:** inspect the push at 100% on the final resolution for grain/scan artefacts magnified by the move; confirm the archive agreement covers movement.

## 8. Counterexample and repair — the unnecessary speed ramp

**Hypothetical counterexample.** In an early cut of Project A, the editor ramps the handheld follow during the 3 a.m. emergency: real time → 30% slow motion as Asha reaches the bed → real time. The footage was shot at 25 fps, so the slow section uses optical-flow interpolation. In review: the slow section shows warping around Asha's hands and the IV stand; the emergency feels "like a music video"; a staff reviewer says it looks staged.

**Diagnosis:**
- The ramp imposed a stylistic convention on observational material (contract breach; see [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md)).
- No capture headroom: interpolation invented frames, producing visible artefacts — and invented image content in a factual scene.
- The emphasis the ramp sought was already present in the real-time action.

**Repair:** remove the ramp; restore real-time footage. To emphasise the moment honestly, hold the shot a beat longer at her arrival at the bed and let the production sound (her instruction) carry it. Simpler, truer and stronger.

**Verification:** staff reviewer and fresh viewers watch the repaired version; the scene should feel urgent and real, with no "edited" sensation.

## 9. Micro-decisions

- Before ramping, mark the exact frames of the important action; keep them within the slow section.
- Render retimes at full quality and review at 100%; preview renders hide interpolation artefacts.
- When interpolating, check hands, faces, edges and occlusions frame by frame.
- Add motion blur to digital moves proportional to their speed; none for very slow moves.
- Keep a record of every retime (clip, speed, method) for conform and VFX handoffs (see [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md)).
- In vertical versions, recheck digital moves: the crop may push the subject out of frame mid-move.

## 10. Failure signatures and corrections

| Symptom | Cause | Correction |
|---|---|---|
| Warping, rubbery edges | Interpolation beyond headroom | Reduce slow-down; cut around the problem; capture higher next time |
| Ghosting | Frame blending | Use optical flow or real frames |
| Staccato real-time motion | Short shutter footage at real speed | Add blur; use a real-time pass |
| Floating stabilised shot | Over-smoothing | Lower strength; preserve intentional moves |
| Cardboard 2.5D | Large moves; flat layers | Smaller moves; better depth separation; or avoid |
| Ramp feels gimmicky | Style without purpose | Remove or replace with a cut or a hold |

## 11. Verification

- Full-speed playback, then frame inspection of interpolated sections and edges.
- Action comprehension: can viewers describe what happened?
- Perspective plausibility of digital and virtual moves.
- Format variants: check moves in every aspect ratio.
- Sound synchronisation after ramps.

## Dependencies

- Depends on: [Capture Decisions](Capture-Decisions.md), [Motivated Movement](Motivated-Movement.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md).
- Interacts with: [Animation Grammar](../MOTION-DESIGN/Animation-Grammar.md), [Compositing and Integration](../VFX/Compositing-and-Integration.md), [Sound Design](../AUDIO/Sound-Design.md).
- Disclosure: [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

## Confidence summary

Capture headroom arithmetic and the dolly/digital-push distinction are technical facts. Interpolation artefact patterns are `[Practice]` observations; ML interpolation quality changes quickly. The caution about ramps as fashion is a `[Heuristic]`. Crop budget numbers are arithmetic; usable crop also depends on lens and compression. Examples are `[Illustrative]`.
