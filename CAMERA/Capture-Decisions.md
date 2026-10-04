# Capture Decisions: Frame Rate, Shutter, Exposure and Devices

**Purpose:** Teach the technical capture choices that determine what post-production can do — capture rate versus timeline rate, shutter and motion blur, exposure and dynamic range, focus reliability, light flicker, white balance and the audio dependencies of picture choices — with resource-aware guidance for phones, mirrorless cameras and controlled productions.

**Applies to:** Every shoot.

**Prerequisites:** [Composition and Optics](Composition-and-Optics.md), [Decision Method](../FOUNDATIONS/Decision-Method.md) (frame/time conversions).

**Related owners:** Project frame-rate and timecode conventions in [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md); retiming in [Retiming and Virtual Motion](Retiming-and-Virtual-Motion.md); colour pipeline in [Color Management](../COLOR/Color-Management.md); lighting in [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md).

---

## 1. Capture rate versus timeline rate

| Term | Meaning |
|---|---|
| Capture (sensor) rate | How many frames per second the camera records |
| Timeline (project) rate | The rate at which the edit plays and the master is delivered |
| Playback interpretation | How a clip recorded at one rate plays on a timeline at another |

If capture rate equals timeline rate, motion plays in real time. If capture rate is higher and the clip is interpreted at the timeline rate, motion plays slower (for example, 59.94 fps interpreted on a 23.976 fps timeline plays at 40% speed). Treatment of mismatched rates is covered in [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#5-mixed-rate-footage); here the point is to **decide before shooting** which moments may need slow motion and capture them at a suitable rate.

| Planned use | Capture rate (for a 23.976 or 25 fps timeline) | Notes |
|---|---|---|
| Real time | Same as timeline | Default |
| Gentle slow motion (around 40–50%) | About 2× timeline rate (e.g., 50 or 59.94 fps) | Good for emotional emphasis; modest light needs |
| Strong slow motion (around 20%) | About 4–5× (e.g., 100–120 fps) | Product pours, splashes; needs more light; flicker risk |
| Extreme slow motion | Specialised high-speed cameras | Specialist work |
| Speed ramps (real time to slow) | High rate, interpreted with variable speed in post | Plan the ramp; capture at the highest rate needed |

## 2. Shutter, motion blur and the "180-degree" convention

**Shutter angle** expresses exposure time as a fraction of the frame interval: angle = 360° × frame rate × exposure time. A 180° shutter exposes each frame for half the frame interval: 1/48 s at 24 fps, 1/50 s at 25 fps, about 1/60 s at 29.97 fps.

The 180-degree convention produces motion blur that many viewers associate with film-like motion `[Practice]`. It is a reference, not a law:

| Shutter choice | Motion character | Use when | Risk |
|---|---|---|---|
| ~180° | Familiar, smooth motion blur | Most narrative and documentary | — |
| Narrower (e.g., 90°, 45°) | Crisper frames, staccato motion | Action, sport, war-like intensity; frames for VFX tracking or slow-motion extraction | Strobing on pans; looks "jittery" |
| Wider (e.g., 270°–360°) | More blur, dreamy or smeared | Low light; deliberate softness | Smearing of detail; less sharp stills |
| Exposure fixed to avoid light flicker (Section 6) | Near 180° | Under mains-powered lighting | — |

**Slow motion and shutter:** for footage captured at 119.88 fps, the maximum exposure is 1/119.88 s; a 180° equivalent is about 1/240 s. Each frame has little blur, so slowed motion looks crisp. If the same footage is used in real time (converted), motion looks staccato because the blur is too short for 23.976 fps viewing.

## 3. Exposure and dynamic range

### 3.1 The goal

Exposure is not "making the image look bright". It is **placing the scene's tonal range within the camera's recording range** so that the important information — usually faces, the product, key highlights — is recorded with detail and low noise, and so that the colorist has the latitude the look requires.

### 3.2 Log, raw and display profiles

| Recording | What it is | Exposure approach | Post consequence |
|---|---|---|---|
| Display-referred profile (e.g., a standard Rec.709-like picture profile) | Image looks finished in camera | Expose for the look; highlights clip earlier | Less latitude; faster workflow |
| Log profile | Compresses a wider dynamic range into the recording; looks flat | Expose per the manufacturer's guidance for that curve, typically protecting highlights while keeping shadows above noise | Requires an input transform (see [Color Management](../COLOR/Color-Management.md)); more latitude |
| Raw | Sensor data with minimal processing | Similar to log; more flexibility in white balance and ISO in post | Larger files; more post processing |

**Log needs bit depth.** Recording log in 8-bit increases the risk of banding when the grade expands the compressed tones; 10-bit or higher is preferred for log where available `[Practice]`.

### 3.3 Exposure tools on set

- **Waveform:** brightness distribution across the frame; shows clipping and crushed shadows.
- **False colour:** maps brightness ranges to colours; quick check of skin and highlights.
- **Zebras:** stripes above a threshold; set to the profile in use.
- **Histogram:** overall distribution; less spatial information.

Know whether the tool is reading the **log signal** or the **monitoring LUT** image — thresholds differ. Middle grey and skin placements vary between log curves; use the manufacturer's documentation for the specific curve.

### 3.4 What cannot be fixed later

- **Clipped highlights** in the recording have no detail to recover (see [Footage Assessment](../OPERATIONS/Footage-Assessment.md#6-triage-for-damaged-missing-or-weak-material)).
- **Severely underexposed shadows** lifted in post bring up noise and compression artefacts.
- **Wrong white balance** in display-referred recordings is partly correctable; extreme errors leave casts that cannot be fully neutralised without affecting skin.

## 4. Focus reliability

| Situation | Risk | Practice |
|---|---|---|
| Shallow depth of field on moving subjects | Focus misses | Stop down a little; mark positions; rehearse; use focus assist |
| Autofocus on faces | Hunting; jumping to the background when the subject turns | Lock or use face/eye tracking tested on the actual subject; avoid in critical takes if unreliable |
| Macro product shots | Tiny depth of field | Test focus at the exact feature; consider focus stacking only for stills |
| Phones | Autofocus hunting; focus breathing; computational artefacts | Lock focus and exposure; avoid digital zoom |
| Handheld documentary | Distance changes constantly | Wider field of view, slightly deeper focus; zone focusing |

Check focus at full magnification during or after critical takes. A focus miss seen on a small monitor is often invisible until the grade.

## 5. White balance and mixed light

- Set white balance manually; automatic white balance can shift mid-shot when the frame content changes.
- Under mixed sources (window daylight plus tungsten practicals), choose a balance that renders skin as intended and lets other sources render warm or cool deliberately (see [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md)).
- Record a grey or white reference at the start of each setup, under the key light, to help the colorist.
- Raw recording allows white balance changes in post; log and display profiles bake it in to varying degrees.

## 6. Light flicker

Many light sources powered by mains electricity vary in brightness at twice the mains frequency: **100 Hz** where mains is 50 Hz (e.g., India, Europe) and **120 Hz** where it is 60 Hz (e.g., North America). Incandescent lamps flicker little because the filament retains heat; fluorescent tubes, some discharge lamps and many inexpensive LED fixtures (especially dimmed LEDs using pulse-width modulation) can flicker strongly. When the camera's exposure does not contain a whole number of light cycles, frames receive different amounts of light — visible as flicker, pulsing or rolling bands (with rolling-shutter sensors).

| Mains | Light cycle | Flicker-safe exposure times (whole cycles) | Notes |
|---|---|---|---|
| 50 Hz | 1/100 s | 1/50, 1/100, 1/33.3, … | At 25 fps, 1/50 s (180°) is safe; at 23.976/24 fps, use 1/50 s (≈172.6°–172.8°) instead of 1/48 s |
| 60 Hz | 1/120 s | 1/60, 1/120, … | At 29.97/30 fps, 1/60 s (≈180°) is safe; at 24 fps, 1/60 s (144°) or 1/120 s |

**High frame rates under mains lighting:** exposures shorter than one light cycle (e.g., 1/240 s at 119.88 fps) cannot contain a whole cycle, so non-flicker-free sources will flicker. Use flicker-free fixtures (or sources with high-frequency drivers), daylight, or plan deflicker in post — and test.

**PWM-dimmed LEDs and screens** can flicker at frequencies unrelated to mains. Always test with the actual fixtures at the actual settings.

## 7. Devices: phones, mirrorless cameras, controlled production

| Context | Strengths | Constraints | Key practices |
|---|---|---|---|
| Smartphone | Always available; discreet; computational processing; good in daylight | Small sensor (noise in low light, deep focus); variable frame rate; aggressive processing (sharpening, noise reduction, HDR tone mapping); fixed apertures; heat | Use an app or mode that locks frame rate, shutter, ISO, focus and white balance; avoid digital zoom; record in the best available codec; external mic for sound |
| Mirrorless / consumer cinema cameras | Large sensors; interchangeable lenses; log profiles; good value | Overheating in some models; rolling shutter; recording limits; menu complexity | Test record times; know the log workflow; manage batteries and media |
| Controlled production (cinema cameras, crew) | Full control; high dynamic range; timecode; robust recording | Cost; size; crew | Standard procedures: camera reports, test days, look management |

### Stabilisation, rolling shutter, autofocus and digital zoom

| Feature | Benefit | Constraint |
|---|---|---|
| In-body stabilisation | Smoother handheld | Can produce "floaty" drift; edge warping with wide lenses |
| Electronic stabilisation | Smoother; available on phones | Crops the frame; motion-blurred frames look smeared when stabilised ("blurry but stable"); edge warping |
| Gimbal | Very smooth movement | Floating feel; setup time; balancing |
| Rolling shutter | Standard on most CMOS sensors | Skew on fast pans, wobble ("jello") with vibration, partial-frame flashes |
| Autofocus | Convenience | Hunting; wrong subject |
| Digital zoom | Framing flexibility | Resolution loss; noise; often irreversible in the recording |

## 8. Audio dependencies of picture choices

Picture decisions affect sound: a wide shot pushes the boom farther away; camera fans and lens motors are audible in quiet rooms; a gimbal operator's footsteps are recorded; high-frame-rate modes often record no audio. Plan:

- Lav mics when wide shots prevent close booms.
- Wild sound (sound recorded without picture) for high-frame-rate shots.
- Quiet camera settings (fan modes) in interviews.
- Scratch audio on every camera for sync.
- Timecode alignment with the recorder (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#6-sync-and-dual-system-audio)).

## 9. Worked example 1 — LED practical flicker (hypothetical, Project D, 23.976 fps in a 50 Hz region)

**Situation:** the project's base shutter is 1/48 s (180° at 23.976 fps). On the first lighting test, a warm LED table lamp in frame shows faint pulsing on the monitor; the background ceiling LED panel shows slow rolling bands.

**Diagnosis:** at 50 Hz mains, many LED sources flicker at 100 Hz. 1/48 s contains about 2.08 light cycles — not a whole number — so frames receive slightly different light. The rolling bands come from the panel's driver frequency interacting with the rolling shutter.

**Options:**

| Option | Effect | Trade-off |
|---|---|---|
| Change shutter to 1/50 s (≈172.6°) | Contains exactly two 100 Hz cycles; mains-related flicker eliminated | Motion blur reduced by about 4% — imperceptible in practice |
| Replace the table lamp with an incandescent bulb of similar colour | Removes flicker from the practical | Different colour and dimming behaviour; heat |
| Turn off the ceiling panel; light the background with a flicker-free fixture | Removes rolling bands | Needs a fixture and power |
| Deflicker in post | Partial fix | Time; artefacts; cannot fix rolling bands well |

**Choice:** 1/50 s shutter for all scenes lit by practicals, plus switching off the ceiling panel and lighting the background with a flicker-free LED fixture. The camera report notes the shutter change. **Verification:** record 10 seconds of each lighting setup and review at 100% on a large monitor, including a frame-by-frame check of the lamp's brightness; repeat after dimmer changes.

## 10. Worked example 2 — High-frame-rate product pour (hypothetical, Project B, 23.976 fps timeline)

**Plan:** the pour and the drink beat may use slow motion at around 20–40% speed; the reveal is in real time.

| Decision | Choice | Rationale |
|---|---|---|
| Capture rate for the pour | 119.88 fps (≈20% when interpreted at 23.976) | Allows strong slow motion and a ramp from 100% to 20% |
| Shutter | 1/240 s (≈180° at 119.88) | Crisp droplets |
| Light | Flicker-free continuous fixtures, about 2–3 stops more output than for real-time shooting | Short exposure; flicker-free required |
| Real-time version | Also capture the pour at 23.976 fps, 1/48 s | If slow motion is not used, real-time motion blur looks natural |
| Audio | No sync audio at 119.88; record pour sounds separately (wild) | Sound design (see [Sound Design](../AUDIO/Sound-Design.md)) |
| Reflections | Brushed steel; large diffusion and black flags | See [Practical Setups](../LIGHTING/Practical-Setups.md) |

**Verification:** review a test at the intended playback speed; check for flicker frame by frame; check droplet sharpness; confirm the slow-motion shot can be ramped without interpolation (see [Retiming and Virtual Motion](Retiming-and-Virtual-Motion.md)).

## 11. Counterexample and repair — the auto phone B-cam

**Hypothetical counterexample (Project A, an earlier shoot day).** The phone B-cam is left in its default camera app: automatic exposure, white balance and focus, HDR processing on, variable frame rate. During the interview, a nurse walks past the window; the phone's exposure dips and recovers; white balance shifts warmer when Asha leans into the lamp light; focus briefly jumps to the background. The editor finds the B-cam nearly unusable for cutting.

**Diagnosis:** automatic modes respond to frame content, creating changes unrelated to the scene; VFR causes sync drift.

**Repair:**
- **Next session:** use a camera app or mode that locks exposure, ISO, white balance, focus and a constant frame rate of 25 fps; disable HDR video processing; set shutter to 1/50 s (flicker-safe at 50 Hz).
- **Existing footage:** conform to constant frame rate; use only the stable sections; grade with keyframed corrections over the exposure dip (the dip is short; a correction works if no clipping occurred); avoid the focus-jump section.

**Verification:** a 2-minute test recording with someone walking past a window; check exposure stability and sync at the start, middle and end.

## 12. Micro-decisions

- Write the shutter, frame rate, ISO/EI, white balance, lens and profile in a camera report for every setup.
- Shoot a few seconds of a grey card or white reference under key light per setup.
- Record a few seconds before and after every take (handles).
- In log, monitor through the intended viewing LUT, but judge clipping on the log signal.
- Turn off in-camera sharpening and noise reduction where the profile allows, for more controllable post.
- Check for flicker with every new light source or dimmer change.

## 13. Failure signatures and corrections

| Symptom in post | Capture cause | Prevention |
|---|---|---|
| Flicker or rolling bands | Exposure time vs light cycle; PWM sources | Flicker-safe shutter; flicker-free fixtures; testing |
| Banding in the grade | 8-bit log; heavy compression | 10-bit; better codec; expose properly |
| Noisy shadows | Underexposure | Expose for the scene's important tones; add light |
| Clipped windows or skin | Overexposure; exposure judged on the LUT | Judge on log/waveform; protect highlights |
| Staccato slow-mo used at real time | Short shutter at high rate | Capture real-time version too |
| Jello/wobble | Rolling shutter with vibration | Stabilise physically; avoid fast pans |
| Unstable phone footage | Auto modes | Lock settings |

## 14. Verification before wrap

- Review critical takes at 100% for focus and noise.
- Check flicker on all light sources at the chosen shutter.
- Confirm frame rates and timecode settings match the project convention.
- Confirm clean plates, wild sound and reference charts were captured.

## Dependencies

- Depends on: [Composition and Optics](Composition-and-Optics.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md).
- Feeds: [Retiming and Virtual Motion](Retiming-and-Virtual-Motion.md), [Color Management](../COLOR/Color-Management.md), [Correction and Shot Matching](../COLOR/Correction-and-Shot-Matching.md), [Compositing and Integration](../VFX/Compositing-and-Integration.md).
- Light: [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md).

## Confidence summary

Shutter-angle arithmetic, mains-flicker frequencies and flicker-safe exposure times are technical facts. The association of ~180° shutter with familiar motion is `[Practice]`; deviations are `[Preference]`. Profile-specific exposure targets are deliberately not given; they must come from manufacturer documentation for the curve in use. Device characteristics are general `[Practice]`; specific models vary. Examples are `[Illustrative]`.
