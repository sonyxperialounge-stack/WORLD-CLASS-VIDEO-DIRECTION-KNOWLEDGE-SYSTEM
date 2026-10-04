# Coverage Map

**Purpose:** Show where every requested domain, original question cluster, extension and technical-care area is covered in this library, with the evidence that the coverage is substantive (worked examples, counterexamples, verification).

**How to read:** "Examples" lists the worked examples and failure/repair cases by short name; follow the links for the actual sections. The [Quality Audit](QUALITY-AUDIT.md) records how this map was checked.

---

## 1. The seven original domains and the closing question

| # | Original domain | Canonical documents | Key evidence |
|---|---|---|---|
| 1 | The precise cut and its relationship to pacing, rhythm and emotional timing | [Cut Decisions](EDITING/Cut-Decisions.md), [Shot Relationships](EDITING/Shot-Relationships.md), [Rhythm and Pacing](EDITING/Rhythm-and-Pacing.md), [Performance Editing](EDITING/Performance-Editing.md), [Continuity and Attention](EDITING/Continuity-and-Attention.md) | Frame-level dialogue-turn comparison (5 candidates, 23.976 fps); product action timing; beat-sync counterexample and repair; outgoing/incoming relationship table; intensity maps; deliberate rule-breaking with undo tests |
| 2 | Design, motion and easing — what moves, what stays, integration with live action | [Design System](MOTION-DESIGN/Design-System.md), [Animation Grammar](MOTION-DESIGN/Animation-Grammar.md), [Integration and Data Graphics](MOTION-DESIGN/Integration-and-Data-Graphics.md), [Typography System](TEXT-ACCESSIBILITY/Typography-System.md) | Lower third and end-card examples; velocity-curve comparison; linear motion legitimised; overshoot counterexample (medical); pasted-on graphic diagnosis; no-motion alternative; honest chart revision |
| 3 | Raw sound, music, mixing and silence | [Recording and Cleanup](AUDIO/Recording-and-Cleanup.md), [Dialogue and Voice](AUDIO/Dialogue-and-Voice.md), [Music Selection](AUDIO/Music-Selection.md), [Music Editing](AUDIO/Music-Editing.md), [Sound Design](AUDIO/Sound-Design.md), [Perspective and Silence](AUDIO/Perspective-and-Silence.md), [Mix Strategy](AUDIO/Mix-Strategy.md), [Audio Delivery](DELIVERY/Audio-Delivery.md) | First-listen checklist; noisy interview chain; track evaluation matrix; 15-bar rearrangement; same-frame music/cut answer; key-reveal silence design; muddy-mix diagnosis; over-limited repair; verified loudness table |
| 4 | Synthetic and AI-assisted audio | [Generation and Layering](AI-AUDIO/Generation-and-Layering.md), [Voice and Music QC](AI-AUDIO/Voice-and-Music-QC.md) | Three complete generation briefs (Foley, ambience, score); generated footstep diagnosis and layering; synthetic narration workflow; generated score sketch; cloned-voice counterexample; artefact and rights checklist |
| 5 | Captions and on-screen text — timing, placement, typography, conflict with the image | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Typography System](TEXT-ACCESSIBILITY/Typography-System.md), [Localization](TEXT-ACCESSIBILITY/Localization.md) | Cue table with illustrative times and rate calculations; reading/action collision and repair; interchange capabilities; Devanagari rules; kinetic-caption counterexample |
| 6 | Camera motivation and movement — physical and simulated, including retiming | [Motivated Movement](CAMERA/Motivated-Movement.md), [Retiming and Virtual Motion](CAMERA/Retiming-and-Virtual-Motion.md), [Composition and Optics](CAMERA/Composition-and-Optics.md), [Capture Decisions](CAMERA/Capture-Decisions.md) | Product reveal options; documentary handheld follow; orbiting-interview counterexample; pour ramp options; still-image move limits; unnecessary-ramp repair |
| 7 | Lighting read through to colour (existing light, correction, grading, texture) | [Reading and Designing Light](LIGHTING/Reading-and-Designing-Light.md), [Practical Setups](LIGHTING/Practical-Setups.md), [Color Management](COLOR/Color-Management.md), [Correction and Shot Matching](COLOR/Correction-and-Shot-Matching.md), [Creative Grading](COLOR/Creative-Grading.md), [Texture and Post Relighting](COLOR/Texture-and-Post-Relighting.md) | Location read; window interview diagram; night practicals; first-look sequence; simple and complex pipelines; double-transform repair; skin-line counterexample; restrained vs stylised grades; texture matching |
| — | Closing question: when do correct techniques become one artistic statement? | [Creative Coherence and Taste](FOUNDATIONS/Creative-Coherence-and-Taste.md), [Failure Modes and Repair](DIAGNOSTICS/Failure-Modes-and-Repair.md), [Worked Projects](WORKED-PROJECTS/00-Overview.md) | Coherence signals table; coherence audit (filled); polished-but-empty repair; imperfect-but-working moment; isolation tests; stopping criteria |

## 2. Original question clusters

| Original inquiry | Where answered |
|---|---|
| First cue, frameworks, micro-decisions, tensions, technical versus apt choices, "invisible rules" | [Decision Method](FOUNDATIONS/Decision-Method.md) (public criteria, confidence labels); micro-decision sections in every chapter; [Creative Coherence and Taste](FOUNDATIONS/Creative-Coherence-and-Taste.md#2-technical-correctness-versus-apt-choice) |
| Exact cut, timeline/scene pacing, emotional rhythm, outgoing/incoming relationship, rule breaking | [Cut Decisions](EDITING/Cut-Decisions.md), [Shot Relationships](EDITING/Shot-Relationships.md), [Rhythm and Pacing](EDITING/Rhythm-and-Pacing.md) |
| Starting point for design, easing, what moves/stays, native integration, anticipation/overshoot/settle | [Design System](MOTION-DESIGN/Design-System.md#2-three-ways-in-shape-first-timing-first-footage-first), [Animation Grammar](MOTION-DESIGN/Animation-Grammar.md), [Integration and Data Graphics](MOTION-DESIGN/Integration-and-Data-Graphics.md) |
| First listen, track character, spectral space, silence, counterpoint, same-frame music/cut | [Dialogue and Voice](AUDIO/Dialogue-and-Voice.md#1-the-first-listen), [Music Selection](AUDIO/Music-Selection.md), [Mix Strategy](AUDIO/Mix-Strategy.md), [Perspective and Silence](AUDIO/Perspective-and-Silence.md), [Music Editing](AUDIO/Music-Editing.md#5-beat-aligned-and-offbeat-cutting) |
| Generated perceptual properties, acoustic space, plausibility, density, organic sound | [Generation and Layering](AI-AUDIO/Generation-and-Layering.md) |
| Speech/reading timing, placement conflict, typography/emotion, utility vs expressive text | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Typography System](TEXT-ACCESSIBILITY/Typography-System.md#8-worked-example-1--informative-corporate-overlay-hypothetical) |
| Motion motivation, subject/camera relationships, ramps, operator-like virtual moves | [Motivated Movement](CAMERA/Motivated-Movement.md), [Retiming and Virtual Motion](CAMERA/Retiming-and-Virtual-Motion.md) |
| Existing light, hard/soft, three-point alternatives, warm/cool; scopes/LUT/skin/invisibility | [Reading and Designing Light](LIGHTING/Reading-and-Designing-Light.md), [Practical Setups](LIGHTING/Practical-Setups.md#1-five-approaches-compared), [Correction and Shot Matching](COLOR/Correction-and-Shot-Matching.md), [Creative Grading](COLOR/Creative-Grading.md#3-invisible-versus-expressive-grades) |
| Correct techniques becoming one artistic statement | [Creative Coherence and Taste](FOUNDATIONS/Creative-Coherence-and-Taste.md), [Worked Projects](WORKED-PROJECTS/00-Overview.md) |

## 3. The 25 requested domain modules

"≥2 examples" counts distinct applied examples in the owner documents (and shared, linked examples where the prompt allows). Every module also has a failure/repair or counterexample and a verification section.

| # | Module | Owner documents | Worked examples (≥2) | Counterexample / failure-repair | Status |
|---|---|---|---|---|---|
| 01 | Creative brief, intent and audience | [Creative Brief](FOUNDATIONS/Creative-Brief.md), [Constraints and Priorities](FOUNDATIONS/Constraints-and-Priorities.md), [Reference Analysis](FOUNDATIONS/Reference-Analysis.md) | Arc brief; Second Shift brief; same "energetic" reference in interview vs ad; priority maps | Viral-style brief; even scarcity; stylish reference cost credibility | Written, reviewed |
| 02 | Interview craft and testimony | [Interview Craft](STORY/Interview-Craft.md), [Review and Revisions](OPERATIONS/Review-and-Revisions.md#care-of-the-subject-who-sees-the-cut) (subject review) | Founder interview; nervous first-time subject (unplanned opening); subject selection tests | Manufactured sound-bite and re-interview | Written, reviewed |
| 03 | Footage assessment and preparation | [Footage Assessment](OPERATIONS/Footage-Assessment.md), [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md), [Paper Edit and Assembly](OPERATIONS/Paper-Edit-and-Assembly.md) | Multicam interview; imperfect handheld event; Project A ingest; screen recordings; Project A and Project B paper edits | AI-focus promise; drifting phone and proxy master; the split that only looked safe | Written, reviewed |
| 04 | Story architecture | [Story Architecture](STORY/Story-Architecture.md), [Genre and Viewer Contract](STORY/Genre-and-Viewer-Contract.md) | Educational vs character structures; Arc rough-cut diagnostic; same footage, two contracts | Misleading reorder and truthful repair; imported retention tactics | Written, reviewed |
| 05 | Editing and cut decisions | [Cut Decisions](EDITING/Cut-Decisions.md), [Shot Relationships](EDITING/Shot-Relationships.md) | Dialogue turn micro-timeline; product action sequence; night-to-dawn transition; graphic match | Mechanical beat-synced montage; transition pack | Written, reviewed |
| 06 | Rhythm and pacing | [Rhythm and Pacing](EDITING/Rhythm-and-Pacing.md) | Quiet documentary vs kinetic launch reel (maps); slow-looking high-tension sequence; repetitive montage repair | Trimming every pause | Written, reviewed |
| 07 | Performance, continuity and eye trace | [Performance Editing](EDITING/Performance-Editing.md), [Continuity and Attention](EDITING/Continuity-and-Attention.md) | Two-person scene; interview with missing coverage; continuity matrix; attention map; vertical extraction | Spokesperson polishing; accidental axis crossing | Written, reviewed |
| 08 | Motion graphics and design | [Design System](MOTION-DESIGN/Design-System.md), [Animation Grammar](MOTION-DESIGN/Animation-Grammar.md), [Integration and Data Graphics](MOTION-DESIGN/Integration-and-Data-Graphics.md) | Restrained lower third; product claim/end card; process visualisation; chart revision | Motion hiding weak composition (no-motion alternative); medical bounce; pasted-on graphic | Written, reviewed |
| 09 | Typography and text hierarchy | [Typography System](TEXT-ACCESSIBILITY/Typography-System.md) | Corporate overlay; expressive music-video type; filled bilingual spec | Cramped lower third with glow | Written, reviewed |
| 10 | Dialogue, voice and recording | [Recording and Cleanup](AUDIO/Recording-and-Cleanup.md), [Dialogue and Voice](AUDIO/Dialogue-and-Voice.md) | Noisy location interview; budget VO; dialogue edit decision log; lifeless VO repair | Robotic interview; over-claiming authoritative voice | Written, reviewed |
| 11 | Music selection and editing | [Music Selection](AUDIO/Music-Selection.md), [Music Editing](AUDIO/Music-Editing.md) | Product-film track evaluation; reflective documentary cue; 15-bar rearrangement; cue extension | Overly emphatic cue; waveform-aligned join | Written, reviewed |
| 12 | Sound design, perspective and silence | [Sound Design](AUDIO/Sound-Design.md), [Perspective and Silence](AUDIO/Perspective-and-Silence.md) | Small intimate action (key); large stylised impact; key-reveal silence; perspective continuity | Over-designed documentary; digital silence perceived as fault | Written, reviewed |
| 13 | Mixing and loudness | [Mix Strategy](AUDIO/Mix-Strategy.md), [Audio Delivery](DELIVERY/Audio-Delivery.md) | Dialogue-heavy explainer; action montage; multi-destination explainer; brand deliverables | Muddy mix diagnosis; over-limited mix; "−14 everywhere" | Written, reviewed |
| 14 | AI audio and synthetic sound | [Generation and Layering](AI-AUDIO/Generation-and-Layering.md), [Voice and Music QC](AI-AUDIO/Voice-and-Music-QC.md) | Generated indoor footstep; synthetic narration; generated score sketch | Synthetic ambience in documentary; founder voice clone | Written, reviewed |
| 15 | Captions and accessibility | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Localization](TEXT-ACCESSIBILITY/Localization.md) | Overlapping speakers cue table; dense tutorial labels; testimony subtitles; bilingual labels | Kinetic captions as only access; machine-translated narration | Written, reviewed |
| 16 | Camera composition and optics | [Composition and Optics](CAMERA/Composition-and-Optics.md), [Capture Decisions](CAMERA/Capture-Decisions.md) | Intimate interview; product demonstration; LED flicker; HFR pour | Sharp but detached; auto phone B-cam | Written, reviewed |
| 17 | Camera motion and retiming | [Motivated Movement](CAMERA/Motivated-Movement.md), [Retiming and Virtual Motion](CAMERA/Retiming-and-Virtual-Motion.md) | Product reveal; handheld follow; pour ramp; still-image move | Orbiting interview; unnecessary ramp | Written, reviewed |
| 18 | On-set lighting | [Reading and Designing Light](LIGHTING/Reading-and-Designing-Light.md), [Practical Setups](LIGHTING/Practical-Setups.md) | Reading the interview room; reflective product; window-lit interview (diagram); night practicals | Implausible source direction; corporate three-point in a home | Written, reviewed |
| 19 | Colour management and correction | [Color Management](COLOR/Color-Management.md), [Correction and Shot Matching](COLOR/Correction-and-Shot-Matching.md) | Simple pipeline; complex mixed-camera pipeline; mixed-camera interview match; mixed-temperature scene | Double transform; skin-line forcing | Written, reviewed |
| 20 | Creative grade and image texture | [Creative Grading](COLOR/Creative-Grading.md), [Texture and Post Relighting](COLOR/Texture-and-Post-Relighting.md) | Restrained documentary grade; stylised brand scene; texture matching; motivated relighting | Teal-orange preset; beauty pass | Written, reviewed |
| 21 | VFX, compositing and finishing | [Compositing and Integration](VFX/Compositing-and-Integration.md), [Repair and Finishing](VFX/Repair-and-Finishing.md) | Phone screen replacement; stylised sketch effect; window reflection cleanup; privacy masking | Floating keyed presenter; generative removal of evidence | Written, reviewed |
| 22 | AI-assisted workflow | [Assistance and Control](AI-WORKFLOWS/Assistance-and-Control.md), [Generated Media QC](AI-WORKFLOWS/Generated-Media-QC.md) | Interview-assisted logging; generated product background; storyboard exploration; rejected B-roll | Automated highlight clip; stereotyped NGO imagery | Written, reviewed |
| 23 | Platforms, formats and localization | [Platform and Format Strategy](DELIVERY/Platform-and-Format-Strategy.md), [Versioning and Localization](DELIVERY/Versioning-and-Localization.md) | Brand film to vertical; documentary across destinations; Hindi/English localization; cutdowns | Failed crop and repair; one export for everything; stale caption file | Written, reviewed |
| 24 | Review operations and delivery | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md), [Review and Revisions](OPERATIONS/Review-and-Revisions.md), [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md), [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md) | Small-team turnaround; multi-specialist with late cut change; review logs; consent in a medical setting; QC sheets | Turnover without handles; literal notes; subscription track in paid ads; strobing launch reel | Written, reviewed |
| 25 | Taste, coherence and diagnostics | [Creative Coherence and Taste](FOUNDATIONS/Creative-Coherence-and-Taste.md), [Failure Modes and Repair](DIAGNOSTICS/Failure-Modes-and-Repair.md) | Polished but empty brand film; imperfect documentary moment; "it's not working" diagnosis; flat scene | Treating a story problem with effects | Written, reviewed |

## 4. Extensions (added scope) mapped

| Extension | Where |
|---|---|
| Brief, audience, references; resource-aware planning | [Creative Brief](FOUNDATIONS/Creative-Brief.md), [Constraints and Priorities](FOUNDATIONS/Constraints-and-Priorities.md), [Reference Analysis](FOUNDATIONS/Reference-Analysis.md) |
| Interview planning and conduct; remote interviews; modes | [Interview Craft](STORY/Interview-Craft.md) |
| Ingest, selects, archive and third-party material | [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md), [Footage Assessment](OPERATIONS/Footage-Assessment.md) |
| Story; genre contracts | [Story Architecture](STORY/Story-Architecture.md), [Genre and Viewer Contract](STORY/Genre-and-Viewer-Contract.md) |
| Assembly planning from transcripts (paper edit, radio cut, stringout) | [Paper Edit and Assembly](OPERATIONS/Paper-Edit-and-Assembly.md) |
| Performance; geography and eye trace | [Performance Editing](EDITING/Performance-Editing.md), [Continuity and Attention](EDITING/Continuity-and-Attention.md) |
| Typography; data truth | [Typography System](TEXT-ACCESSIBILITY/Typography-System.md), [Integration and Data Graphics](MOTION-DESIGN/Integration-and-Data-Graphics.md) |
| Dialogue/VO; music editing; acoustics and perspective | [Dialogue and Voice](AUDIO/Dialogue-and-Voice.md), [Music Editing](AUDIO/Music-Editing.md), [Perspective and Silence](AUDIO/Perspective-and-Silence.md) |
| Colour management; texture | [Color Management](COLOR/Color-Management.md), [Texture and Post Relighting](COLOR/Texture-and-Post-Relighting.md) |
| Compositing; LED volumes and virtual backgrounds | [Compositing and Integration](VFX/Compositing-and-Integration.md#virtual-backgrounds-led-volumes-and-in-camera-effects) |
| Accessibility and localization (including Devanagari, RTL) | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Localization](TEXT-ACCESSIBILITY/Localization.md) |
| AI controls | [Assistance and Control](AI-WORKFLOWS/Assistance-and-Control.md), [Generated Media QC](AI-WORKFLOWS/Generated-Media-QC.md) |
| Genres and formats; series continuity | [Platform and Format Strategy](DELIVERY/Platform-and-Format-Strategy.md), [Versioning and Localization](DELIVERY/Versioning-and-Localization.md#3-series-and-recurring-formats) |
| Production and handoffs; interchange | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md) |
| Rights, privacy, disclosure | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md) |
| Revisions | [Review and Revisions](OPERATIONS/Review-and-Revisions.md) |
| Technical QC, flash risk, archive | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md) |
| Integrated projects | [Worked Projects](WORKED-PROJECTS/00-Overview.md) |
| Sources | [Sources and Limitations](SOURCES-AND-LIMITATIONS.md) |
| Continuation and delivery | [Progress](PROGRESS.md), [Quality Audit](QUALITY-AUDIT.md) |

## 5. Technical areas requiring special care

| Area | Where treated | How the care requirement is met |
|---|---|---|
| Colour management (scene vs display, transforms, LUT ≠ pipeline) | [Color Management](COLOR/Color-Management.md) | Explicit concepts table; two pipelines; mistakes catalogue |
| HDR/SDR delivery | [Color Management](COLOR/Color-Management.md#6-monitoring-what-can-be-assessed-and-on-what), [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#1-delivery-profiles) | No HDR claims from uncharacterised displays; destination specs required |
| Loudness (integrated, short-term, true peak, sample peak, normalisation) | [Mix Strategy](AUDIO/Mix-Strategy.md#3-the-vocabulary-of-level-and-loudness), [Audio Delivery](DELIVERY/Audio-Delivery.md) | Vocabulary distinguished; verified figures with levels; no universal number |
| Captions (heuristics vs requirements) | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md#23-reading-time-and-reading-rate) | Verified destination examples labelled; language dependence stated |
| Exposure and motion (capture rate, timeline rate, shutter, flicker, interpolation) | [Capture Decisions](CAMERA/Capture-Decisions.md), [Retiming and Virtual Motion](CAMERA/Retiming-and-Virtual-Motion.md) | Arithmetic and assumptions stated |
| Flash and pattern risk | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#4-flash-and-pattern-risk) | QC gate; WCAG 2.3.1 verified; BT.1702-3 identified; destination check required |
| Generative AI | [Assistance and Control](AI-WORKFLOWS/Assistance-and-Control.md), [Generated Media QC](AI-WORKFLOWS/Generated-Media-QC.md), [Voice and Music QC](AI-AUDIO/Voice-and-Music-QC.md) | No product claims; terms must be checked; rights not assumed |
| Export (codec, container, bit depth, chroma, tags, range, bitrate) | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md) | Profiles from current destination documents |

## 6. Integrated worked projects requirements

| Requirement | Evidence |
|---|---|
| Truthful interview/documentary segment | [Project 1](WORKED-PROJECTS/01-Documentary-Second-Shift.md) |
| Short product/brand advertisement with horizontal/vertical adaptation | [Project 2](WORKED-PROJECTS/02-Product-Brand-Arc.md) |
| Educational/explainer with localization and accessibility complication | [Project 3](WORKED-PROJECTS/03-Explainer-Clear-Water.md) |
| Additional project (narrative drama) | [Project 4](WORKED-PROJECTS/04-Narrative-Scene-Spare-Key.md) |
| Each contains brief → acceptance (14 content items), micro-timeline, late change with dependencies, sacrifice and disconfirming test | Sections 1–17 of each project |

## 7. Required root documents

| Document | Present |
|---|---|
| [00-START-HERE](00-START-HERE.md), [README](README.md), [01-MASTER-INDEX](01-MASTER-INDEX.md), [COVERAGE-MAP](COVERAGE-MAP.md), [MASTER-CHECKLIST](MASTER-CHECKLIST.md), [FINAL-MASTER-REFERENCE](FINAL-MASTER-REFERENCE.md), [GLOSSARY](GLOSSARY.md), [QUALITY-AUDIT](QUALITY-AUDIT.md), [SOURCES-AND-LIMITATIONS](SOURCES-AND-LIMITATIONS.md), [PROGRESS](PROGRESS.md) | Yes — verified by inventory check (see [Quality Audit](QUALITY-AUDIT.md)) |
