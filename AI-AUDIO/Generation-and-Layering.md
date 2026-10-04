# Synthetic Sound: Generation Briefs, Diagnosis and Layering

**Purpose:** Teach how to specify, select, diagnose and integrate generated or synthesised sound effects, ambiences and musical sketches — what makes a sound perceptually plausible, why technically plausible output can still feel wrong, and how to layer synthetic material with recorded sound under human control.

**Applies to:** Generative audio tools, procedural and synthesised sound design, and any workflow mixing generated with recorded audio.

**Prerequisites:** [Sound Design](../AUDIO/Sound-Design.md), [Perspective and Silence](../AUDIO/Perspective-and-Silence.md).

**Companion chapter:** [Voice and Music QC](Voice-and-Music-QC.md) (synthetic voice, generated music, artefact and rights checks). Approval gates for any AI use are owned by [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md); rights and disclosure by [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

**Note on products:** generative audio tools change quickly in capability, cost, data retention and licensing terms. This chapter teaches tool-independent principles; any specific product's behaviour and terms must be checked in its current documentation before use.

---

## 1. What makes a sound perceptually identifiable

Listeners recognise a sound — and judge whether it is plausible — from a bundle of cues. A generation brief, and a diagnosis of generated output, should address each.

| Property | What the listener infers | Example cues |
|---|---|---|
| Source action | What happened (strike, scrape, roll, pour, step) | Onset shape; rhythm; continuous vs discrete |
| Material | What it's made of (wood, metal, glass, fabric, ceramic) | Resonances; decay; brightness; damping |
| Force | How hard (tap vs slam) | Level; spectral brightness; onset sharpness |
| Scale | How big | Low-frequency content; resonance pitch; decay length |
| Space | What kind of room or environment | Early reflections; reverberation; ambience |
| Distance | How far | Direct-to-reverberant ratio; high-frequency loss; level |
| Early reflections | Nearby surfaces; room size | Reflection timing and density |
| Reverberation tail | Space size and materials | Decay time; tone of the tail |
| Plausibility | Whether all cues agree | Consistency across properties |
| Organic variation | Whether it sounds performed, not mechanical | Natural differences between repetitions |

**Reconstruction versus expression.** Some sounds must reconstruct recognisable acoustic cues (a footstep on a tiled floor must sound like that). Others are deliberately impossible — a product "signature" tone, a sci-fi interface, a subjective sound of memory. For reconstruction, plausibility is judged against reality. For expression, it is judged against the piece's internal logic and the emotion intended. Both still need coherent cues: an expressive impact still needs an onset, body and tail that belong together.

## 2. Writing a generation brief

A good brief is specific about the event and its context, honest about what the model can do, and explicit about what must not appear.

| Field | Content | Why |
|---|---|---|
| Source / event | The action and object, in plain language | Identity |
| Duration | Total length; durations of parts if relevant | Most tools approximate duration; edit afterwards |
| Perspective | Close, medium, distant; mic character | Matches the shot |
| Environment | Room type, size, surfaces; indoor/outdoor | Space cues |
| Texture | Material and surface details | Specificity |
| Timing anchors | Number of events and approximate spacing, if needed | Do not expect frame accuracy; plan to edit |
| Variation | How many variants; what should differ | Material for organic editing |
| Prohibited artefacts | Music, speech, voices, clicks, reverb beyond X, background noise, crowd | Avoids common contamination |
| Output constraints | Sample rate, bit depth, mono/stereo, loudness headroom, file format | Integration |
| Intended use | Which scene; what layer role (onset, body, detail, space, tail) | Guides choice and evaluation |

**Assumptions to avoid:** that the model understands exact frame timing; that it will output separated stems or layers; that it will be consistent between generations; that output is automatically cleared for commercial use.

### Example brief 1 — Foley (hypothetical, Project D)

> **Event:** a woman walking slowly across a tiled floor in an apartment at night, wearing thin rubber-soled indoor slippers. Five steps, unhurried, slightly hesitant on the last two.
> **Duration:** about 5 seconds total; steps roughly one per second (exact timing will be edited to picture).
> **Perspective:** close-medium, as if a boom microphone is overhead about 1 metre from the feet. Mono.
> **Environment:** small living room, about 4 × 5 metres, tiled floor, painted walls, some soft furnishings (sofa, curtains); short, slightly bright room reflections; no long reverb.
> **Texture:** soft heel contact, slight slipper slap and scuff; no squeaks.
> **Variation:** 6 variants; vary weight and scuff between steps.
> **Prohibited:** music, speech, breathing, background ambience, traffic, refrigerator hum, clicks, reverb tails longer than about half a second.
> **Output:** 48 kHz, 24-bit WAV, mono, peaks below −6 dBFS.
> **Use:** body and detail layers for Nisha's footsteps in the wide master; onset will come from recorded Foley if the generated attack is weak.

### Example brief 2 — Ambience (hypothetical, Project B "Arc" studio kitchen scene)

> **Event:** quiet modern apartment kitchen in a city, early morning. Distant traffic murmur through a closed double-glazed window; faint refrigerator hum; no voices.
> **Duration:** 60 seconds, seamlessly loopable if possible (will be edited and crossfaded).
> **Perspective:** room perspective, as if recorded with a stereo pair at head height in the centre of the kitchen.
> **Environment:** medium room, hard surfaces (tile, stone countertop), some soft furnishing in the adjoining room.
> **Texture:** low, steady, calm; occasional distant bird; one distant car horn very soft around 40 seconds is acceptable.
> **Prohibited:** music, speech, recognisable phone tones or brand sounds, sirens, dogs barking, construction noise.
> **Output:** 48 kHz, 24-bit WAV, stereo; integrated loudness low enough to sit under dialogue; no limiting.
> **Use:** background bed for the morning montage; the real location had a noisy air conditioner, and this is a designed advertising environment (not documentary).

### Example brief 3 — Score sketch (hypothetical, Project A animatic only)

> **Purpose:** temporary sketch to test whether a late, sparse cue helps the ending; *not* for final use without separate approval.
> **Music:** sustained warm pads and a few soft piano notes, very slow (around 60 BPM or free time), no percussion, no melody that resolves dramatically.
> **Structure:** 0–20 s pads only; one gentle harmonic change around 20 s; 20–60 s pads with three or four isolated piano notes; natural decay ending at about 70 s.
> **Prohibited:** vocals, choir, strings swelling, drums, a recognisable melody, imitation of any specific artist or film score.
> **Output:** 48 kHz stereo WAV; separate pad and piano files if the tool supports it (likely not — plan for a single mix).
> **Use:** tested against the no-music version with fresh viewers (see [Music Selection](../AUDIO/Music-Selection.md#7-worked-example-2--a-reflective-documentary-scene-hypothetical-project-a-second-shift)).

## 3. Selecting and integrating

1. **Generate several candidates.** Expect most to fail on at least one property.
2. **Audition in context** — with picture, dialogue and ambience — not solo. A sound that is impressive alone may be wrong in the scene.
3. **Rate each candidate against the brief's properties** (identity, material, scale, space, distance, variation, artefacts).
4. **Select parts, not whole files.** Use the best step from variant 2 and the best scuff from variant 5.
5. **Edit to picture.** Place events on contact frames; trim, fade, vary.
6. **Integrate with layers** (Section 5) and match perspective (see [Perspective and Silence](../AUDIO/Perspective-and-Silence.md)).
7. **Keep originals and a record** of prompts, tool version, settings and dates — needed for rights review and reproducibility.

## 4. Why technically plausible output can feel wrong

Generated sounds often pass a first listen and fail in the scene. Diagnose *which property* fails before regenerating; repeating generation with adjectives ("more realistic") rarely fixes a specific defect.

| Symptom | Underlying defect | Typical repair |
|---|---|---|
| "Too big" or "too small" | Incorrect scale: resonance pitch and low-frequency content don't match the object | Pitch/EQ adjustment; choose another variant; layer a recorded body of the right scale |
| "Mushy" or "disconnected" | Transient (onset) and body don't belong together — e.g., a soft onset with a heavy body | Replace onset with a recorded or library transient; align |
| "In the wrong room" | Wrong acoustic distance or space baked in | Choose a drier variant and add matching room; or regenerate with a drier brief |
| "Machine-gun" | Repetition of identical events | Use different variants; vary pitch, level and timing slightly; re-sequence |
| "Wobbly" or "synthetic" timbre | Unstable spectral character within a sound (warble, phasing) | Discard; or use only stable fragments; record conventionally |
| "Cut-off" or "ghostly" tail | Unnatural decay — abrupt or smeared | Replace tail with recorded reverb/tail; fade |
| "Floating", not "in the world" | Missing contextual bed: the sound exists without the room's air | Lay ambience; add early reflections |
| "Too much detail" | Over-detailed texture, more information than the shot implies | Low-pass or reduce detail layer; choose simpler variant |

**When to stop generating:** if two or three targeted attempts fail on the same property, record it (Foley is often quick for footsteps and props) or use a library sound. Generation is one source among several, not an obligation.

## 5. Layering synthetic with recorded sound

| Principle | Practice |
|---|---|
| Layer roles | Assign onset, body, detail, space and tail (see [Sound Design](../AUDIO/Sound-Design.md#5-layering-with-complementary-roles)); a generated sound may supply one role well and others badly |
| Onset alignment | Align transients exactly; misaligned onsets "flam" (doubled attack) |
| Phase and low-end interaction | Two layers with low-frequency energy can reinforce or cancel; check in mono; high-pass one of them |
| Perspective matching | All layers must share one perspective, or the composite feels split |
| Variation | Use different variants for repeated events |
| Silence and bed continuity | Generated files may include their own noise floor; matching or replacing it avoids "noise pumping" between events |
| Nondestructive comparison | Keep the recorded-only and composite versions; compare at matched loudness |

### Organic variation defined

Organic variation is **structured difference**, not random noise. Real footsteps vary in systematic ways: heel-to-toe timing changes with speed; weight shifts alternate between feet; the surface changes near furniture; the last step before stopping is softer. Adding random pitch and level variation to identical samples sounds less mechanical but not organic. Build variation from the logic of the action.

### Sparse versus dense

Dense layering can create impressive sounds and can also hide performance and dialogue. Under dialogue, prefer fewer, cleaner layers; in non-dialogue moments with no competing focus, density can be expressive.

## 6. Worked example — A generated indoor footstep (hypothetical, Project D, 23.976 fps)

**Situation:** the wide master shot shows Nisha walking across the flat; the boom recorded her footsteps poorly (refrigerator hum, distant). The team tries generated footsteps from Example brief 1.

**First-generation results (hypothetical):**

| Variant | Observation | Defect |
|---|---|---|
| 1 | Clear steps but sound like hard shoes | Material (wrong source: shoe, not slipper) |
| 2 | Slipper character, good weight | Each step identical in onset — repetition |
| 3 | Good scuff; too much reverb | Space (too reverberant for the small room) |
| 4 | A faint voice-like murmur at 3.2 s | Prohibited artefact (unexpected speech-like sound) |
| 5 | Good weight variation, slightly bright | Usable with EQ |
| 6 | Unstable, warbly decay | Unstable timbre |

**Diagnosis before regenerating:** the core problem with most variants is *onset character* and *room*. Rather than regenerating repeatedly, the editor:
1. Records three slipper steps on a tiled floor at home with a phone held about 50 cm away, in a small room, as onset material (10 minutes' work).
2. Uses generated variants 2 and 5 for body and scuff detail (selecting different steps to avoid repetition).
3. Aligns the recorded onsets with the generated bodies; high-passes the generated layer slightly to avoid low-end build-up.
4. Adds the scene's room tone and a short, matching early-reflection reverb to the composite.
5. Places each step on the frame of foot contact; adjusts the last two steps to be softer, matching her hesitation.

**Rejected alternative:** regenerating with "more realistic, softer, less reverb" until something works — rejected as time-consuming and unpredictable.

**Verification:** watch the wide shot at full speed with dialogue and room tone; ask a listener whether the footsteps belong to the room. Inspect variant 4's artefact is not used. Record prompts, tool and version for the rights log.

## 7. Counterexample and repair — the synthetic ambience in a documentary

**Hypothetical counterexample.** For Project A's night-ward scenes, an assistant replaces the noisy location ambience with a generated "hospital ward at night" ambience: soft monitor beeps, distant announcements, a gentle air-conditioning hum. It sounds cleaner than the real ward. But the ward has no monitors and no announcement system; the generated bed misrepresents the place and contradicts the visible fans and generator.

**Diagnosis:** a generated environment was used as documentary evidence of a real place — a factual misrepresentation, not a sound-quality improvement.

**Repair:**
1. Remove the generated bed.
2. Rebuild ambience from location recordings (room tone recorded on the night; additional ambience recorded in the same ward on another night with permission).
3. Where cleanup is needed, use noise reduction on the real recordings, not replacement.
4. Note in the project's AI-use log that generated ambience was trialled and rejected for documentary scenes.

**Boundary:** in Project B's designed advertising kitchen, a generated ambience is acceptable — the contract is a designed environment, not evidence of a real place.

**Verification:** a hospital staff member reviews the night scenes' sound for authenticity.

## 8. Micro-decisions

- Ask for dry, close perspective in briefs; it is easier to add space than remove it.
- Request more variants than you need; selection is cheaper than repair.
- Normalise generated files to a common working level before comparison.
- Check generated files for hidden speech-like artefacts at low levels — listen with headphones at raised gain.
- Keep a project log of generated assets: prompt, tool, version, date, terms, where used.

## 9. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Doesn't sit in the scene | Perspective/space mismatch | Drier variant; add matching room |
| Sounds fake on repeat | Repetition | Variants; structured variation |
| Low-end mud | Layer conflict | High-pass; remove redundant body |
| Strange murmurs or tones | Generation artefacts | Discard affected segments |
| Factual misrepresentation | Generated environment used as evidence | Use real recordings in factual work |
| Rights uncertainty | Terms not checked | Verify terms; log; replace if unclear |

## 10. Verification

- In-context listening at full speed with dialogue and ambience.
- Matched-loudness comparison against recorded/library alternatives.
- Artefact scan on headphones at raised gain.
- Rights and terms recorded before approval (see [Voice and Music QC](Voice-and-Music-QC.md#5-artefact-and-rights-checklist-before-approval)).

## Dependencies

- Depends on: [Sound Design](../AUDIO/Sound-Design.md), [Perspective and Silence](../AUDIO/Perspective-and-Silence.md).
- Companion: [Voice and Music QC](Voice-and-Music-QC.md).
- Governance: [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

## Confidence summary

The perceptual properties of sound and layering principles are `[Practice]` in sound design. Diagnostic patterns for generated audio are `[Heuristic]`, based on common failure modes of current generative tools, which change quickly. Statements about tool limitations (timing precision, stems, consistency) are deliberately general and must be checked per product. Examples are `[Illustrative]`.
