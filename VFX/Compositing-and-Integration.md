# Compositing and Integration

**Purpose:** Teach how to decide whether a visual effect is needed; the physical and photographic cues that make composited elements belong in a shot; alpha and edge fundamentals; acquisition planning that makes effects cheaper; how virtual backgrounds and LED volumes turn post problems into on-set decisions; and how to evaluate composites honestly.

**Applies to:** Screen replacements, keying, rotoscoping, tracking, object integration, set extensions and stylised composites.

**Prerequisites:** [Color Management](../COLOR/Color-Management.md), [Composition and Optics](../CAMERA/Composition-and-Optics.md), [Capture Decisions](../CAMERA/Capture-Decisions.md).

**Companion chapter:** [Repair and Finishing](Repair-and-Finishing.md) (invisible cleanup, privacy masking, generative removals, finishing and handoffs). Graphic overlays and data graphics are in [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md).

---

## 1. Is an effect needed?

| Question | Why it matters |
|---|---|
| What is the narrative function? | Effects that do not serve the story are cost without return |
| Does it improve visual clarity? | Some effects clarify (a readable screen); others distract |
| Is there a practical alternative? | Shooting it for real, choosing another angle, a prop, or an edit may be cheaper and more convincing |
| What will it cost (time, money, schedule risk)? | Effects often delay finishing |
| Is the source suitable? | Motion blur, noise, compression, missing tracking information or poor keying conditions raise cost sharply |
| What is the ethical implication? | In factual work, altering images can misrepresent reality; disclosure may be required |

**Practical before digital** `[Heuristic]`: for many problems — a screen that should show content, a sign that should be removed, a reflection — solving it on set (playing content on the screen, covering the sign, flagging the reflection) costs less than compositing.

## 2. Kinds of compositing work

| Work | Description | Typical difficulty drivers |
|---|---|---|
| Invisible cleanup | Removing unwanted elements (rigs, logos, reflections) | Movement, parallax, texture, duration (see [Repair and Finishing](Repair-and-Finishing.md)) |
| Screen replacement | Replacing a device screen's content | Reflections, fingers over the screen, motion blur, screen angle, moiré |
| Object integration | Adding a CG or photographed object into a scene | Lighting match, shadows, contact, perspective |
| Keying | Extracting a subject from a coloured background (green/blue screen) | Spill, hair, motion blur, uneven screen lighting, compression |
| Rotoscoping | Hand-drawing mattes frame by frame (or with assisted tools) | Hair, motion blur, fast movement |
| Tracking | Following motion (2D points, planar surfaces, 3D camera solves) | Lack of features, motion blur, lens distortion, rolling shutter |
| Stabilisation cleanup | Fixing edges and artefacts after stabilisation | Revealed edges, warping |
| Stylised composites | Deliberately non-realistic combinations | Coherence with the piece's style |

## 3. What makes an element belong in a shot

Masking an element precisely is not integration. An element belongs when it shares the shot's **space, light, optics and medium**.

| Factor | What to match | Typical failure |
|---|---|---|
| Coordinate space | Composite in linear light (scene-referred) where possible, so blending, blur and light behave physically | Edges and glows look wrong when compositing in display-referred gamma |
| Lens distortion | Undistort the plate for tracking/compositing, then re-distort | Elements slide at frame edges |
| Perspective | Element matches vanishing points and camera height | Element looks "stuck on" or tilted |
| Parallax | Element moves correctly relative to foreground/background as the camera moves | Floating or sliding |
| Scale | Correct size relative to known objects | Toy-like or giant |
| Lighting | Direction, softness, colour and intensity match | Element lit from a different side; too bright |
| Shadow and contact | Element casts and receives shadows; contact points darken (occlusion) | Floating; no weight |
| Reflections | Shiny surfaces reflect the environment; the element appears in reflections where it should | "Missing" reflections betray a fake |
| Occlusion | Foreground objects pass in front correctly (requires roto/depth) | Element in front of things it should be behind |
| Edge behaviour | Edge softness, light wrap (background light bleeding onto edges), no fringes | Hard cutout look; halos |
| Depth of field | Element blurred to match its distance from the focal plane | Sharp element in a soft plane |
| Grain/noise | Matching noise structure and level | Clean element over noisy plate |
| Shutter/motion blur | Matching blur for movement | Crisp element in a blurred move |
| Colour pipeline | Same working space and output transform as the plate (see [Color Management](../COLOR/Color-Management.md)) | Colour mismatch; double transforms |

### Alpha, premultiplication and fringes

An **alpha channel** describes each pixel's opacity. Images with alpha are stored either **straight** (colour values independent of alpha) or **premultiplied** (colour already multiplied by alpha). Compositing a premultiplied image as if it were straight (or vice versa) produces **dark or light halos** at semi-transparent edges. Other fringe causes:

- **Spill:** coloured light from a green/blue screen contaminating edges and hair — corrected by despill.
- **Edge erosion or expansion** in keys — over-choking leaves dark lines; under-choking leaves background colour.
- **Colour operations on premultiplied images** without unpremultiplying first — brightening edges incorrectly.
- **Display-referred blending** — edges look harsh or dirty.

Knowing which convention each render and each tool uses is a handoff requirement (Section 7).

## 4. Planning effects at acquisition

| Planning item | Purpose |
|---|---|
| Clean plates | The same shot without the subject/object, for cleanup and background reconstruction |
| Tracking markers | Features for trackers on plain surfaces (e.g., small markers on a phone screen or green screen), placed so they are easy to remove |
| Lens information | Focal length, focus distance, sensor mode; lens grid charts for distortion |
| Reference light | Grey and chrome spheres, colour charts, or HDR environment captures for lighting CG |
| Measurements | Distances, sizes, camera height and tilt |
| Handles | Extra frames before and after the used section |
| Even screen lighting | For keys: evenly lit green/blue screen, subject separated from it to reduce spill |
| Shutter and frame rate | Consistent with integration needs; avoid unnecessary motion blur on tracked elements if precise tracking is critical |

**Effects that must be planned before picture lock:** shots that need substantial compositing should have their duration and handles fixed early; VFX work on shots that later change length is wasted. Some effects (e.g., an inserted screen showing information the story depends on) must be approved in content before the edit can be locked.

### Virtual backgrounds, LED volumes and in-camera effects

When a production composites against a virtual background, shoots in an LED volume (actors in front of large LED walls displaying a rendered environment), or creates effects in camera, the following become **acquisition decisions** rather than post repairs:

| Factor | Why it is decided on set |
|---|---|
| Perspective and parallax | The background must be rendered from the tracked camera's position; errors are baked into the shot |
| Lighting relationship | The LED wall lights the actors; its colour and brightness must work for skin and the scene |
| Shutter and frame rate | LED panel refresh and camera shutter must be synchronised to avoid scanlines and flicker |
| Colour pipeline | The wall's content, the panels' colour behaviour and the camera's capture must be calibrated together |
| Focus and moiré | Focusing on or near the wall can reveal the pixel grid as moiré |

Fixing these afterwards is costly and often impossible; test on the stage before shooting.

## 5. Evaluating composites: full speed versus frame inspection

| Inspection | Purpose | Trap |
|---|---|---|
| Full-speed playback | How viewers will perceive it; reveals flicker, sliding, temporal instability | Subtle edge issues may pass unnoticed — and may not matter |
| Frame inspection | Diagnose edges, fringes, track errors | A perfect still may flicker in motion; a slightly imperfect frame may be invisible at speed |
| Encoded and reframed review | Compression and resizing can reveal matte edges, banding and halos; vertical crops change what's visible | Approving on uncompressed playback only |

**Microscopic work:** distinguish defects worth fixing (visible at full speed on the target display, or in the vertical crop, or after compression) from those that require frame-stepping at 400% to find. Spend time on what viewers can perceive.

## 6. Worked example 1 — Phone screen replacement (hypothetical, Project B "Arc")

**Shot:** a hand holds a phone showing the Arc app's progress screen; the phone tilts slightly as the person glances at it; the screen was shot with a plain dark-grey display and small tracking markers (on-set plan), because the approved final UI was not ready.

**Process:**
1. **Track** the screen with a planar tracker using the markers and screen corners; check for drift during the tilt.
2. **Undistort** the plate if lens distortion affects the screen corners.
3. **Render the approved UI** (from the client's design system) at a resolution appropriate to the screen's size in frame, in the working colour space (see [Color Management](../COLOR/Color-Management.md#5-a-complex-mixed-camera-workflow-hypothetical-project-b-arc)).
4. **Insert** the UI with matching perspective; animate it to match the real ring's behaviour (see [Animation Grammar](../MOTION-DESIGN/Animation-Grammar.md#8-worked-example-1--the-arc-lid-ring-and-claim-text-hypothetical-project-b-23976-fps)).
5. **Screen look:** match screen brightness relative to the scene (screens are emissive; not so bright that they clip); add subtle pixel-structure softness so it looks like a display, not a sticker.
6. **Reflections:** extract the real screen's reflections (the room and the person's face faintly visible in the dark screen) and layer them over the new UI at appropriate strength.
7. **Occlusion:** roto the thumb where it overlaps the screen edge.
8. **Remove markers** (they are covered by the UI or cleaned).
9. **Motion blur and grain:** match the plate's blur during the tilt and its grain.
10. **Legal check:** the UI content (progress values, text) is approved, accurate and consistent with the product's real behaviour — a technical substitution that does not misrepresent function (see [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md#23-brand-film-and-advertisement)).

**Verification:** full-speed playback on a phone and a large display; frame inspection of the thumb edge and screen corners; encoded review; brand and legal approval of UI content.

## 7. Compositing checklist and render handoff assumptions

### Compositing checklist (use per shot)

| # | Check | Pass |
|---|---|---|
| 1 | Plate interpretation and working colour space confirmed | ☐ |
| 2 | Lens distortion handled (undistort/redistort) | ☐ |
| 3 | Track stable through the whole shot, including handles | ☐ |
| 4 | Perspective and scale correct | ☐ |
| 5 | Lighting direction, softness and colour match | ☐ |
| 6 | Shadows and contact present where needed | ☐ |
| 7 | Reflections handled (in the element and in the scene) | ☐ |
| 8 | Occlusion correct | ☐ |
| 9 | Edges: no fringes/halos; correct premultiplication; light wrap where appropriate | ☐ |
| 10 | Depth of field matched | ☐ |
| 11 | Motion blur matched | ☐ |
| 12 | Grain/noise matched | ☐ |
| 13 | Full-speed review on target display | ☐ |
| 14 | Encoded and reframed (all aspect ratios) review | ☐ |
| 15 | Content approval (facts, UI, claims) and disclosure decision where relevant | ☐ |

### Render handoff assumptions (fill per project)

**Filled example (hypothetical, Project B):**

| Item | Agreement |
|---|---|
| Plate delivery | Image sequences from camera originals, conformed with handles of 12 frames (≈ 0.5 s at 23.976 fps) each side |
| Colour | Plates delivered in the scene-referred working space (linear for compositing); renders returned in the same space; no output transform baked in |
| Bit depth / format | 16-bit half-float image sequences for plates and renders |
| Alpha | Renders premultiplied; stated in the file naming and delivery note |
| Resolution | Plate resolution maintained (no reformat); reframes happen in the conform |
| Naming | `ARC_SH040_comp_v003` (shot, task, version); version increments only, never overwritten |
| Frame range | Timecode/frame numbers matching the plate including handles |
| Notes | Each delivery includes a note: what changed, known issues |
| Review | Composites reviewed as encoded proxies *and* in the conform at full quality |

## 8. Worked example 2 — A stylistic effect with justified non-realism (hypothetical, Arc 90-second brand film)

**Moment:** Dev describes sketching the first idea at the kitchen table at night. The film shows the real sketchbook page; then the pencil lines of the sketch lift off the paper and draw themselves in the air above the table, forming the outline of the bottle, before the shot cuts to the workshop.

**Why non-realism is justified:** the moment depicts an idea becoming a design — an interior, imaginative process. The style is hand-drawn and flat (pencil-texture lines), clearly not presented as a physical event.

**Integration choices (even for stylised work):**
- The lines are anchored to the page with accurate tracking — the stylisation is in what they are, not in sloppy attachment.
- Light: the lines are not lit by the scene (they are graphic), but a faint warm glow on the page as they lift ties them to the lamp-lit kitchen.
- Grain: the lines receive the plate's grain so they sit in the same medium.
- Disclosure: not needed — the effect is self-evidently imaginative and the brand film's contract is persuasive storytelling, not documentation.

**Verification:** fresh viewers describe the moment as "the idea taking shape"; nobody asks whether it really happened.

## 9. Counterexample and repair — the floating keyed presenter

**Hypothetical counterexample.** A training video places a presenter, shot on a green screen, into a 3D-rendered office. The presenter has a dark outline around the hair, a green tinge on the shoulders, is lit from the left while the virtual office's window is on the right, and appears to float — no shadow on the floor, feet slightly sliding as the virtual camera moves.

**Diagnosis:**

| Symptom | Cause |
|---|---|
| Dark outline | Premultiplied key treated as straight, plus over-choked edges |
| Green tinge | No despill |
| Wrong light direction | Studio lighting not designed for the virtual set |
| Floating | No contact shadow; no ambient occlusion |
| Sliding feet | Virtual camera moves without matching the real camera's (static) perspective — no camera track |

**Repair:**
1. Correct premultiplication handling; soften the edge erosion; add light wrap.
2. Despill green; restore natural hair colour.
3. Rotate the virtual office so its window is on the presenter's key side (cheaper than reshooting).
4. Add a soft contact shadow and subtle floor reflection consistent with the virtual floor.
5. Lock the virtual camera (the real camera was static) or reshoot with a tracked camera if movement is essential.

**Verification:** full-speed playback; viewers no longer comment on "green screen look"; frame inspection of hair edges after encoding.

## 10. Micro-decisions

- Shoot a few seconds of every effects shot without the subject (clean plate), from the same camera position.
- Record lens and camera data on every effects setup.
- Name every render with shot, task and version; never overwrite.
- Review composites in the edit context, not only in isolation; a shot that is fine alone may jar against its neighbours.
- Keep stylised effects consistent in their rules (how lines move, how glows behave) throughout the piece.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Halo/fringe | Premultiplication or edge matte error | Correct alpha handling; refine edges |
| Floating element | Missing shadow/contact; parallax error | Add contact; re-track |
| Sliding | Poor track; lens distortion ignored | Re-track; undistort |
| Pasted-on look | Lighting, grain, blur or DoF mismatch | Match photographic properties |
| Colour mismatch | Pipeline inconsistency | Same working space; check transforms |
| Edge visible only after upload | Compression reveals matte | Review encoded; improve matte |

## 12. Verification

- Edge stability at full speed and frame by frame.
- Contact and perspective plausibility.
- Source/working/output colour relationship confirmed.
- Render versions tracked; the conform uses the approved version.
- Final encoded playback in every version and aspect ratio.

## Dependencies

- Depends on: [Color Management](../COLOR/Color-Management.md), [Capture Decisions](../CAMERA/Capture-Decisions.md), [Composition and Optics](../CAMERA/Composition-and-Optics.md).
- Companion: [Repair and Finishing](Repair-and-Finishing.md).
- Related: [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md), [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md), [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md).

## Confidence summary

Integration factors, alpha/premultiplication behaviour and acquisition planning are `[Practice]` and technical fact. LED-volume considerations are `[Practice]`; specifics depend on equipment and must be tested. "Practical before digital" is a `[Heuristic]`. Examples are `[Illustrative]`.
