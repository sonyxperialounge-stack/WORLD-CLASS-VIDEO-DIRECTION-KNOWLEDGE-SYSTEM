# Repair, Cleanup and Finishing

**Purpose:** Teach invisible cleanup and repair — removing distractions, privacy masking, stabilisation fixes — how to decide what is worth fixing, how to evaluate generative fills and removals for consistency and truth, and how finishing (conform, online, versions) brings the picture to a deliverable state.

**Applies to:** Any project with cleanup needs, privacy requirements or a separate finishing stage.

**Prerequisites:** [Compositing and Integration](Compositing-and-Integration.md).

**Ownership boundaries:** Consent, privacy policy and disclosure rules are owned by [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md); handoffs and interchange by [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md); export and QC by [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

---

## 1. What invisible cleanup covers

| Task | Examples |
|---|---|
| Distraction removal | Boom mic dipping into frame, crew reflections, a modern sign in a period scene, a stray cable, a passing stranger in a product shot |
| Brand/logo removal | Unlicensed logos on clothing, products, screens |
| Sensor and lens defects | Dust spots, dead/hot pixels, lens flares in the wrong place |
| Rig removal | Wires, stands, stabiliser parts |
| Stabilisation cleanup | Edges revealed by stabilisation; warping artefacts |
| Privacy masking | Faces, documents, screens, vehicle plates, name boards |
| Beauty and continuity fixes | Small blemishes (with consent), continuity errors in props |

## 2. Deciding whether to fix

Not every imperfection deserves work. Decide by viewer benefit, cost and truth:

| Question | Fix if… | Leave if… |
|---|---|---|
| Is it visible at full speed on the target display? | Yes | Only visible when frame-stepping at high magnification |
| Does it draw attention from the story? | Yes (e.g., a bright reflection near a face) | It sits outside the focal area, briefly |
| Is it a legal/privacy/rights issue? | Always | — |
| Does fixing change the meaning or truth of the image? | Only with disclosure or not at all in factual work | — |
| Is there a cheaper editorial fix? | — | A different take or a slight reframe solves it |
| What is the cost relative to the piece's value? | Proportionate | Disproportionate to a fleeting, minor issue |

## 3. Cleanup methods

| Method | How | Good for | Limit |
|---|---|---|---|
| Clean plate patch | Replace the area with the same region from a clean plate | Static camera; planned cleanups | Needs a clean plate; lighting must match |
| Clone/paint | Copy nearby texture over the object, frame by frame or tracked | Small, static areas | Repetition patterns; temporal instability |
| Planar-tracked patch | Paint a patch on one frame and track it on a planar surface | Removing signs or marks on walls, floors, screens | Non-planar or deforming surfaces |
| 3D projection | Project a painted frame onto a 3D reconstruction of the scene | Moving cameras with parallax | Requires a camera solve and geometry |
| Temporal fill (borrowing from other frames) | Use frames where the background is visible | Moving objects revealing background | Needs background visibility in other frames |
| Generative fill / inpainting | A model synthesises plausible content for the area | Complex textures; large areas; when other methods fail | Invents content; temporal consistency; factual truth (Section 4) |

## 4. Generative fills, removals and inserts

Generative tools can remove objects or fill areas with plausible content in images and video, and can insert synthetic elements. Evaluate output on five criteria:

| Criterion | What to check | Typical failure |
|---|---|---|
| Temporal consistency | Does the fill stay stable across frames? | Shimmering, crawling texture; content changing frame to frame |
| Identity | Are people's faces and bodies unchanged where they should be? | Subtle changes to faces, hands, clothing near the edit |
| Geometry | Do lines, perspective and structures continue correctly? | Bent lines; impossible architecture; mismatched perspective |
| Texture | Does the fill match grain, sharpness and material? | Smooth patches; wrong pattern scale |
| Factual truth | Does the change alter what the image documents? | Erasing a person, a sign, evidence; adding content that was not there |

**Rules for factual work** `[Practice]`:
- Do not erase evidence (people, objects, text) whose presence matters to the truth of the scene.
- Do not imply documentary authenticity for altered images without appropriate disclosure.
- Prefer blurring or masking (which reads as an edit) over seamless removal when privacy is the goal.
- **Preserve reversible originals** (untouched source media and the pre-fill version), and **document material changes** in a change log: what was changed, why, by whom, with which tool, and whether disclosed.

See [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md) for broader generated-media checks.

## 5. Privacy masking

Privacy masking protects identifiable people and information where consent is absent or not appropriate.

| Method | Strength | Weakness |
|---|---|---|
| Heavy blur | Common; reads as protective | Light blur can sometimes be partially reversed or still reveal identity; blur may be insufficient for small, high-contrast text |
| Pixelation / mosaic | Clear signal of masking | Coarse mosaics of faces can still reveal identity to people who know the person; small block sizes are weak |
| Solid shape / bar | Strongest | Visually heavy |
| Cropping or choosing other shots | No visible mask | Not always possible |

**Robust masking practice:**
- Use strong masking (heavy blur or coarse mosaic, or solid) sized to the feature; test whether the person is still recognisable to someone who knows them.
- Track across every frame where the feature is visible — including entrances and exits, partial visibility, reflections in windows, mirrors and screens.
- Mask audio identity too: names spoken aloud, distinctive voices (see [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md#6-worked-example-1--dialogue-edit-decision-log-hypothetical-project-a-25-fps)).
- Check every version and aspect ratio: reframes can reveal previously off-frame details or shift masks.
- Keep unmasked originals secure; access-control them (see [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md)).

## 6. Worked example 1 — A modest distracting-object cleanup (hypothetical, Project D)

**Shot:** the wide master of the flat at night. The window behind Ravi reflects a crew member and a lighting stand in the glass for about 6 seconds as the camera slowly pushes in.

**Options:**

| Option | Effort | Result |
|---|---|---|
| A. Use a different take without the reflection | None | Take 2 has the reflection too; take 4 lacks it but has weaker performance |
| B. Planar-track the window and patch with the clean plate | Moderate | The clean plate (shot at wrap) was recorded locked-off at the start position, so it does not follow the push-in; usable only with additional re-projection work |
| C. Planar-track the window; build a patch from the frame at the start of the push where the reflection is absent (the crew member stepped in later); track it over the window through the push; add grain; match the streetlight glow | Moderate | Convincing if the window glass is planar and the reflection region is small |
| D. Darken the window region to make the reflection invisible | Low | Changes the streetlight look; the window becomes a dead black area |

**Choice:** C. The window is planar, the move is slow, and the needed patch area is small. Grain and the streetlight's slight shimmer are matched.

**Verification:** full-speed playback on a large display; frame inspection at the window edges; check that Ravi's head, which crosses part of the window, is correctly in front of the patch (roto the head edge).

## 7. Worked example 2 — Privacy masking in observational footage (hypothetical, Project A)

**Shot:** a 12-second handheld shot of Asha at the nurses' station; behind her, a whiteboard lists patients' names and bed numbers; a patient's face is briefly visible in a doorway.

**Decisions:**
- **Whiteboard:** names must not be legible. Planar-track the board and apply heavy blur sized so that no letters can be read at any resolution, including on a large projection; confirm the blur does not reveal names at frame edges as the camera moves.
- **Patient face:** no consent. Options: cut the shot shorter (the face appears in the last 2 seconds) — chosen; the shot still works at 10 seconds.
- **Reflections:** check the glass of a cabinet behind Asha — a reflection shows part of the whiteboard; blurred as well.
- **Log entry:** "SH-112: whiteboard blurred (privacy); shot trimmed to exclude unconsented patient; reflection blurred."

**Verification:** the producer reviews the shot at full resolution and on the projection copy; a staff member who knows the patients confirms nothing identifying remains.

## 8. Counterexample and repair — the generative removal that erased evidence

**Hypothetical counterexample.** In a documentary about a protest, an editor uses a generative tool to remove a police vehicle parked in the background of an interview shot, because it "distracted from the interviewee". The removal is seamless. A viewer who was present recognises the location and notes online that the vehicle was there; the film is accused of hiding the police presence.

**Diagnosis:** a generative removal changed what the image documents. The vehicle's presence was part of the factual context.

**Repair:**
1. Restore the original shot (preserved original).
2. If the vehicle is genuinely distracting, choose a different framing (punch-in), a different take, or accept it.
3. Publish a correction according to the commissioner's policy if the film was already released.
4. Update the project's AI-use and change logs; add a rule: no generative removal in factual footage without editorial approval and disclosure (see [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md)).

**Verification:** editorial review of all cleanup shots against originals.

## 9. Finishing

Finishing brings the edit to a deliverable master.

| Stage | What happens | Key checks |
|---|---|---|
| Conform | The offline edit is rebuilt with full-quality media (via interchange such as EDL/XML/AAF — see [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md)) | Every shot matches the offline reference (side-by-side or difference check); retimes and reframes correct |
| VFX integration | Approved renders replace plates | Correct versions; frame ranges; colour pipeline |
| Grade | Colour work on the conformed timeline | See COLOR chapters |
| Graphics and captions | Final graphics; burned-in text where required | Text versions; fonts; spelling |
| Final render | Master files at the mezzanine/master specification | Correct format, colour tags, frame rate |
| Versions | Derived deliverables (aspect ratios, languages, durations) | Version matrix (see [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md)) |
| QC | Technical and editorial checks | See [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md) |

**Conform check:** compare the conformed timeline with the offline reference export frame by frame or via a difference overlay; mismatches (wrong take, slipped frames, missing retimes) are common after interchange.

## 10. Micro-decisions

- Request clean plates on set for any shot that may need cleanup.
- Keep cleanups as separate layers/versions so they can be revised.
- Record each cleanup and privacy decision in a change log.
- Check masks after every grade and reframe change.
- In privacy masking, test legibility at the largest display size the piece will be shown on.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Patch "swims" | Tracking drift; texture mismatch | Re-track; match grain; shorten patch duration |
| Repeating texture | Clone patterns | Vary sources; use larger patches |
| Mask slips revealing faces/text | Track lost on fast moves | Keyframe; enlarge mask; frame-by-frame review |
| Generative fill flicker | Temporal inconsistency | Different method; stabilise; avoid |
| Factual misrepresentation | Removal or insertion changed meaning | Restore; disclose; review policy |
| Conform mismatch | Interchange error | Difference check; manual fix |

## 12. Verification

- Edge stability and texture match at full speed and frame by frame.
- Privacy: legibility tests at maximum display size; all versions.
- Truth: comparison with originals for every material change; change log complete.
- Final encoded playback in every version.

## Dependencies

- Depends on: [Compositing and Integration](Compositing-and-Integration.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).
- Feeds: [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md), [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md).
- Generated media: [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md).

## Confidence summary

Cleanup methods, privacy-masking robustness and conform checks are `[Practice]`. The evaluation criteria for generative fills are `[Practice]` adapted to fast-changing tools. Rules against undisclosed factual alteration are `[Practice]` consistent with widely held journalistic and documentary ethics; specific codes vary by organisation. Examples are `[Illustrative]`.
