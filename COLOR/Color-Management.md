# Color Management: Interpretation, Pipelines and Monitoring

**Purpose:** Teach the order in which an expert examines footage before correcting it, the concepts that make colour predictable across cameras, software and displays (scene- and display-referred processing, input and output transforms, working spaces, tone and gamut mapping), how to set up a simple and a complex pipeline, what monitoring can and cannot tell you, and how to avoid the classic interpretation mistakes.

**Applies to:** Every project whose images pass through more than one device — which is every project.

**Prerequisites:** [Capture Decisions](../CAMERA/Capture-Decisions.md) (log, raw, display profiles); [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md) (documenting colour assumptions).

**Owns:** The colour pipeline. Correction technique is in [Correction and Shot Matching](Correction-and-Shot-Matching.md); creative looks in [Creative Grading](Creative-Grading.md); destination colour specifications and tags in [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

---

## 1. The first look: image, waveform, vectorscope — or something else?

The original question — *what should an expert look at first?* — has a sequenced answer:

1. **Confirm interpretation.** What is this footage (camera, profile/log curve, colour space, bit depth, range)? What transform is currently applied to display it? Is that the right one? Most "bad footage" in the first hour is misinterpreted footage.
2. **Evaluate the image under intended monitoring.** On a display set to the intended standard, in appropriate ambient light, look at the picture as a viewer would: does it look plausible, are faces natural, is there obvious clipping or noise?
3. **Use scopes to investigate.** Waveform and RGB parade for exposure, black and white levels, channel balance and clipping; vectorscope for hue and saturation, including skin relative to the skin-tone reference line; histograms and false colour as supplementary tools.
4. **Compare shots.** Put shots side by side (or in a gallery) to judge continuity.

No single scope replaces perceptual judgement. Scopes measure signals; they do not know what the scene was or what the story needs. Perception, in turn, is fooled by adaptation, surround and uncalibrated displays. Use both.

## 2. Core concepts

| Concept | Meaning | Why it matters |
|---|---|---|
| Raw | Sensor data before debayering and most processing | White balance and exposure interpretations can be set in post |
| Log encoding | A curve that stores a wide scene range in the recording's code values; looks flat on a normal display | Needs a transform to be viewed correctly; preserves latitude |
| Scene-referred | Values proportional (or log-related) to light in the scene | Grading operations behave more like physical light adjustments (e.g., exposure changes behave consistently) |
| Display-referred | Values intended for a specific display's characteristics (e.g., Rec.709/BT.1886 SDR) | What the viewer finally sees; grading here is direct but less physically consistent |
| Input transform | Converts a camera's encoding (log curve and gamut) into the working space | Must match the actual camera and profile |
| Working space | The colour space in which grading happens (camera-native, a wide-gamut log space, or a standard like ACEScct) | Consistency across mixed sources |
| Output (display rendering) transform | Converts working-space values into display values (tone mapping and gamut mapping) | Determines highlight roll-off, contrast and how wide-gamut colours are rendered |
| Tone mapping | Compressing scene luminance range into display range | Highlight and shadow behaviour |
| Gamut mapping | Bringing colours outside the display's gamut inside it | Saturated lights, LEDs, neon; avoids hard clipping or hue shifts |
| Data levels: full vs legal (video) range | Whether code values span the full range or a "legal" subset (e.g., 64–940 in 10-bit for video range) | Mismatches lift blacks or crush/clip |
| Metadata tags | Colour primaries, transfer characteristic, matrix coefficients, range | Players decide how to display a file partly from tags |

### A LUT is not a pipeline

A Look-Up Table (LUT) maps input values to output values. A manufacturer's "log-to-Rec.709" LUT combines an input interpretation, a tone mapping and an output encoding into one fixed operation. It can be part of a pipeline, but it lacks flexibility: it assumes a specific input, it may clip values outside its range, it cannot adapt to another display standard, and stacking corrections before or after it behaves differently. A pipeline defines explicit input, working and output stages, so grading happens in a predictable space and the output can be changed for different deliverables (SDR, HDR).

## 3. Display standards (stable references)

| Standard | Use | Note |
|---|---|---|
| ITU-R BT.709 primaries with BT.1886 display EOTF | HD SDR video mastering | BT.1886 describes a reference display response (approximately a 2.4 power function in a dim reference environment) |
| sRGB | Computer displays and web graphics | Different transfer function (approximately 2.2) and viewing assumptions than BT.1886 |
| DCI-P3 / P3-D65 | Digital cinema (DCI white) / many HDR masters (D65 white) | Wider gamut than BT.709 |
| ITU-R BT.2020 primaries | UHD and HDR containers | Very wide gamut; masters often occupy only part of it |
| ITU-R BT.2100 (PQ and HLG transfer functions) | HDR | PQ (also SMPTE ST 2084) is absolute luminance-referenced; HLG is relative and designed for broadcast compatibility |

These standards are stable references, but destination delivery requirements (which standard, which tags, which mastering display) must be verified per destination (see [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md)).

## 4. A simple colour-managed workflow (hypothetical, Project A "Second Shift")

**Sources:** A-cam mirrorless in a manufacturer log profile, 10-bit; phone B-cam in its standard (display-referred) profile, conformed to constant frame rate; a few scanned archive photographs; graphics.
**Delivery:** SDR, BT.709/BT.1886, 1920×1080, for web, social and projection.
**Grading by:** the editor, in the NLE's colour tools, on a calibrated external monitor set to BT.709/BT.1886.

| Stage | Setting | Notes |
|---|---|---|
| Input (A-cam) | Manufacturer log curve and gamut → working space | Use the exact curve/gamut the camera recorded |
| Input (phone) | Rec.709-like display-referred → working space via an inverse display transform (or graded directly in display space if the tool prefers) | Phone processing varies; treat as display-referred |
| Working space | A wide-gamut log working space provided by the software (or the camera-native log space) | Grade exposure and white balance consistently |
| Output | Working space → BT.709/BT.1886 with a tone mapping that rolls off highlights softly | One output transform for all shots |
| Graphics | Designed in sRGB-like display space, brought in as display-referred; checked under the output | Brand colours verified on the output |
| Archive photos | Display-referred; scanned in a known profile | Avoid applying log transforms to them |
| Export tags | BT.709 primaries, BT.709 transfer tag, BT.709 matrix, correct range | Players depend on tags |

**Why this setup:** one output transform makes every source land in the same display world; the log footage keeps its latitude; the phone footage is treated honestly as already "baked".

**Verification:** a test export played on the target web player, a phone and the projection setup; compare against the grading monitor. Check that blacks are not lifted (range mismatch) and that the image does not appear lighter or darker than intended (player interpretation differences — some players and operating systems apply different display transforms to BT.709-tagged video, which can change apparent contrast; test on target players).

## 5. A complex mixed-camera workflow (hypothetical, Project B "Arc")

**Sources:** studio cinema camera recording raw; the founder interview on a mirrorless camera in log; a few phone clips from Dev's archive; CG renders of the app UI for screen replacement; motion graphics; high-frame-rate clips in a different codec.
**Delivery:** SDR masters for social and pre-roll; an HDR deliverable is requested as an option for the product page's video player (exact specification to be confirmed with the platform).

| Stage | Choice | Rationale |
|---|---|---|
| Working space | A scene-referred wide-gamut space — for example an ACES-based pipeline (grading in a log working encoding such as ACEScct, compositing in a linear space such as ACEScg) or the grading software's own wide-gamut managed space | Consistent maths across cameras and CG; both SDR and HDR outputs from one grade |
| Inputs | Camera-specific input transforms for each camera/profile; phone clips treated as display-referred with an inverse output transform | Each source interpreted correctly |
| CG UI renders | Rendered in a linear working space matching the compositing pipeline, delivered as high-bit-depth image sequences | Avoids display-referred CG being double-transformed |
| Graphics | Created in display space; brand colours specified with values for the output and checked on both SDR and HDR outputs | Brand compliance |
| Output transforms | SDR BT.709/BT.1886 for social and pre-roll; HDR (e.g., PQ with P3-D65 mastering primaries in a BT.2020 container) only if the destination specification confirms it | One grade, multiple outputs — with trims |
| HDR monitoring | Only on a display capable of the HDR mastering requirements; no HDR grading on an uncharacterised laptop | HDR decisions need appropriate monitoring |
| SDR trim | Adjustments to the SDR output after the HDR grade (or vice versa) | Tone mapping does not automatically produce a perfect SDR version |

**About ACES:** ACES (Academy Color Encoding System) is an open framework for colour management. Its version 2.0, released in 2025 with new output transforms including improved gamut mapping, is implemented in tools such as OpenColorIO configurations; implementations and default settings differ between applications and versions. Do not assume two applications labelled "ACES" render identically — test round-trips (see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md)).

**Verification:** a round-trip test before the main grade: a frame from each camera through input → working → output in the grading system and in the compositing system, compared side by side; CG UI composite rendered and compared under both outputs; brand colours measured on the outputs.

## 6. Monitoring: what can be assessed, and on what

| Display situation | What it can support | What it cannot |
|---|---|---|
| Calibrated reference or professional monitor in a controlled, dim environment | Critical colour and contrast decisions; matching; final approval | Every viewer's experience |
| Good consumer display, calibrated, in a controlled room | Most SDR decisions with care | HDR mastering; subtle colour approval |
| Uncalibrated laptop or phone | Composition, story, rough exposure; how many viewers might see it | Accurate colour; reliable shadow detail; HDR judgements |
| Phone/tablet "consumer check" | Translation check: does it still work for real viewers? | Correct colour reference |

**Ambient light** affects perception: a bright room makes a display look darker and less contrasty, leading graders to lift blacks; a dark room does the opposite. Grade in a consistent, appropriate surround; then check on consumer devices.

**Calibration limits:** calibration aligns a display to a target within its capabilities; it cannot give a narrow-gamut or low-brightness display wide-gamut or HDR capability. Calibration also drifts; recalibrate periodically.

**HDR honesty:** do not promise correct HDR from an uncharacterised laptop display. HDR grading requires a display that can show the target peak luminance and gamut with known behaviour.

## 7. Classic interpretation mistakes

| Mistake | Symptom | Cause | Fix |
|---|---|---|---|
| Wrong input transform | Colours odd; skin magenta or green; contrast wrong | Wrong camera, log curve or gamut selected | Confirm metadata and camera reports; select the correct transform |
| Double transform | Extremely contrasty, oversaturated image with crushed shadows and clipped highlights | A log-to-display transform applied twice (e.g., in a LUT on the clip *and* in the project's output; or baked into proxies and then applied again) | Remove one; trace every transform in the chain |
| Missing transform | Flat, grey image graded "by hand" into contrast | Log footage graded as if it were display-referred | Apply the correct input/output transform; regrade |
| Range mismatch (full vs legal) | Lifted, milky blacks or crushed blacks; clipped whites | File's range tag or interpretation doesn't match its data | Correct interpretation or tag; check export settings |
| Transform clipping vs source clipping | Highlights clip in the image but the log signal has detail | The output transform or a LUT clips, not the camera | Use a transform with highlight roll-off; adjust before the transform |
| Tag mismatch at export | Exported file looks different in players than in the grading system | Wrong primaries/transfer/matrix tags or player interpretation | Correct tags; test in target players |

### Clipping caused by transforms versus source capture

Check on the **log or raw signal** (before transforms) whether highlights contain detail. If they do and the displayed image clips, the problem is in the transform or grade — recoverable. If the source itself is clipped (all channels at maximum), no transform can recover detail (see [Footage Assessment](../OPERATIONS/Footage-Assessment.md#6-triage-for-damaged-missing-or-weak-material)).

## 8. Counterexample and repair — the double transform

**Hypothetical counterexample.** An editor's proxies for Project D were created with the camera manufacturer's log-to-Rec.709 LUT baked in. Later, the colorist relinks to the camera originals and the project's colour management also applies an input and output transform. Meanwhile, the editor had added the same manufacturer LUT as an effect on some clips "to match the proxies". In the grading room, those clips appear wildly contrasty and saturated; others look normal. The colorist initially tries to fix the contrasty clips with curves.

**Diagnosis:** a double transform on the clips with the LUT effect — log converted to display once by the LUT, then treated as log by the pipeline and converted again.

**Repair:**
1. Stop grading. Trace every transform per clip: clip effects, project colour management, timeline LUTs, monitor LUTs.
2. Remove the LUT effects from the clips; rely on the project's input/output transforms.
3. Confirm that all clips now look consistent before grading.
4. Document the pipeline in the project notes (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#73-proxy-color)).

**Verification:** a gallery comparison of all shots before any correction — consistent baseline. A waveform check that formerly crushed shadows now show detail.

## 9. Micro-decisions

- Write the pipeline on one page: inputs per camera, working space, output(s), monitoring standard, export tags.
- Use the camera's metadata *and* the camera report to confirm log curves; metadata can be missing after transcoding.
- Keep the monitoring LUT separate from the grade; never bake a monitoring LUT into deliverables.
- Grade at a consistent monitor brightness and room light.
- Before delivery, play the actual exported file in the actual target players.
- Name LUT files with their intended input and output (e.g., `CamLog_to_709_Look_A_v2.cube`).

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "Looks different on YouTube/phone" | Tags; player interpretation; ambient differences | Correct tags; test on targets; accept some variation |
| Inconsistent look across cameras | Inconsistent input transforms | Per-camera input transforms into one working space |
| Harsh highlight clipping | Output transform or LUT without roll-off | Different transform; adjust before transform |
| Neon/LED colours shift hue or posterise | Gamut mapping issues | Better gamut mapping; reduce saturation in the working space |
| Graphics colours don't match brand | Graphics passed through wrong transform | Treat graphics as display-referred; verify on output |

## 11. Verification

- Shot-to-shot baseline consistency before grading.
- Scope checks on the source signal (clipping, range).
- Round-trip tests across applications in complex pipelines.
- Exported files checked in destination players and devices.
- Illustrative guidance separated from verified destination requirements (HDR, broadcast) — see [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Dependencies

- Depends on: [Capture Decisions](../CAMERA/Capture-Decisions.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md).
- Feeds: [Correction and Shot Matching](Correction-and-Shot-Matching.md), [Creative Grading](Creative-Grading.md), [Texture and Post Relighting](Texture-and-Post-Relighting.md), [Compositing and Integration](../VFX/Compositing-and-Integration.md), [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Pipeline concepts and display standards (BT.709, BT.1886, BT.2020, BT.2100, ST 2084) are established technical references. ACES 2.0's 2025 release was verified (see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md)); application-specific behaviour is not claimed. The first-look sequence and the interpretation-mistake catalogue are `[Practice]`. Monitoring guidance is `[Practice]`. Player interpretation differences are a known `[Practice]` concern whose specifics change with software versions — test rather than assume. Examples are `[Illustrative]`.
