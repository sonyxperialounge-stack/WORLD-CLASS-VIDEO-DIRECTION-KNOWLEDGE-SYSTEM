# Master Checklist: Production and Post Gates

**Purpose:** An ordered sequence of gates from brief to archive. Each gate has observable pass criteria, the evidence to keep, and the action when it fails. The detail behind each item lives in the linked owner chapter; this checklist does not replace them.

**How to use:** copy the gates into the project tracker; mark each criterion with evidence (a file, a reading, a name and date). Small projects may merge gates, but should not skip criteria marked ★ (non-negotiable: truth, rights, accessibility, safety, data integrity).

---

## G0 — Brief

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| One-sentence intent | A third person can test it with a fresh viewer | Brief v-dated | Rewrite with the commissioner | [Creative Brief](FOUNDATIONS/Creative-Brief.md) |
| Five layers separated | Business, story, viewer, accessibility, delivery each stated | Brief | Clarify conflicts now | [Creative Brief](FOUNDATIONS/Creative-Brief.md#3-five-layers-that-must-be-separated) |
| Hinge variables | Listed with confirmation steps | Assumption register | Ask the top three | [Creative Brief](FOUNDATIONS/Creative-Brief.md#5-inferring-cautiously-from-an-incomplete-brief) |
| ★ Truths to protect | Named (facts, testimony, claims, dignity, accessibility) | Brief | Add before shooting | [Creative Brief](FOUNDATIONS/Creative-Brief.md) |
| Destinations and languages | Known well enough to plan acquisition | Draft version matrix | Plan for the likely set; flag cost of additions | [Versioning and Localization](DELIVERY/Versioning-and-Localization.md) |

## G1 — Pre-production

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Priority map | Must-haves named, with defenders; consequences stated | Priority map | Make one before committing budget | [Constraints and Priorities](FOUNDATIONS/Constraints-and-Priorities.md#3-the-priority-map) |
| References translated | Each reference labelled with function and "do not take" | Reference board | Re-analyse by function | [Reference Analysis](FOUNDATIONS/Reference-Analysis.md) |
| Shot list by beats | Each beat's must-see element has a planned shot | Shot list | Re-plan | [Composition and Optics](CAMERA/Composition-and-Optics.md#shot-lists-based-on-story-beats-not-shot-sizes) |
| Interview plan | Listening plan; sensitive areas agreed; location chosen for sound | Plan; notes of agreement | Re-plan; consult subject | [Interview Craft](STORY/Interview-Craft.md) |
| Who is interviewed | Chosen for direct experience rather than fluency; exposure risk assessed; range matches the spread in vox-pop | Selection note | Approach another subject, or re-scope the claim | [Interview Craft](STORY/Interview-Craft.md) |
| ★ Consent and rights plan | Releases, location agreements, music approach, archive needs identified | Rights register started | Resolve before shoot day | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md) |
| Capture plan | Frame rate, timecode convention, shutter (flicker-safe), profiles, HFR needs, vertical framings, VFX plates | Camera plan | Decide now | [Capture Decisions](CAMERA/Capture-Decisions.md) |
| ★ Data handling | Storage, backups, AI/cloud permissions defined | Data plan | Restrict uploads until defined | [Assistance and Control](AI-WORKFLOWS/Assistance-and-Control.md#4-data-handling-do-not-assume-uploads-are-allowed) |

## G2 — On set

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Light read and tested | Motivated directions; flicker tested at chosen shutter for each source | Test clips | Change shutter/sources | [Reading and Designing Light](LIGHTING/Reading-and-Designing-Light.md), [Capture Decisions](CAMERA/Capture-Decisions.md#6-light-flicker) |
| Exposure and focus | Critical takes checked at 100% | Notes | Re-take | [Capture Decisions](CAMERA/Capture-Decisions.md) |
| Sound | Intelligible on headphones; room tone recorded per setup | Sound report | Fix source; re-take | [Recording and Cleanup](AUDIO/Recording-and-Cleanup.md) |
| Coverage | Reactions, cutaways, handles, alternate framings, clean plates captured | Shot list ticks | Pick up before wrap | [Composition and Optics](CAMERA/Composition-and-Optics.md#5-composition-for-the-edit) |
| ★ Releases | Signed for every featured person and location | Photographed releases | Do not use material without them | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md) |
| Reports | Camera and sound reports complete | Reports | Complete before wrap | [Worksheets and Logs](TEMPLATES/Worksheets-and-Logs.md#9-camera-report-filled-example-below) |

## G3 — Ingest

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| ★ Verified backups | Two independent checksum-verified copies before any card is formatted | Ingest log | Stop; complete backups | [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md#2-offload-and-verified-backup) |
| Clock convention | Frame rate, DF/NDF, start TC, off-rate treatment documented | Project notes | Decide and document | [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md#4-the-frame-rate-and-timecode-convention) |
| VFR conformed | All VFR sources converted to CFR in derived media | Media reports | Conform | [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md#variable-frame-rate-sources) |
| Sync checked | Start, middle, end of long multi-source clips | Notes | Re-sync | [Ingest and Preparation](OPERATIONS/Ingest-and-Preparation.md#6-sync-and-dual-system-audio) |
| Colour assumptions | Input transforms and proxy LUT documented | Project notes | Document | [Color Management](COLOR/Color-Management.md) |

## G4 — Before rough cut

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Material opens | Every clip plays | Technical sweep | Re-copy / log loss | [Footage Assessment](OPERATIONS/Footage-Assessment.md#10-acceptance-gates-before-rough-cut) |
| Selects log | Hero moments with context links | Log | Complete | [Footage Assessment](OPERATIONS/Footage-Assessment.md#3-a-selection-system) |
| Paper edit | Story order drafted from transcripts and read aloud before assembly | Paper edit document | Draft before timeline assembly | [Paper Edit and Assembly](OPERATIONS/Paper-Edit-and-Assembly.md) |
| ★ Critical rights known | Featured people and archive status known | Register | Mark pending; plan alternatives | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md) |
| Transcripts flagged | Unverified transcripts labelled as such | Transcript status | Label | [Assistance and Control](AI-WORKFLOWS/Assistance-and-Control.md) |

## G5 — Story lock (structure agreed)

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Central question | Two people independently name the same question | Notes | Restructure | [Story Architecture](STORY/Story-Architecture.md#10-rough-cut-diagnostic-for-beautiful-but-shapeless-material) |
| Beat map reads as a story | Read aloud without pictures | Beat map | Re-order | [Story Architecture](STORY/Story-Architecture.md#5-the-beat-map) |
| Open questions | No unintended open questions | Ledger | Close or de-emphasise | [Story Architecture](STORY/Story-Architecture.md#4-the-open-question-ledger) |
| ★ Temporal honesty | Restructured material checked against original context | Context notes | Repair | [Story Architecture](STORY/Story-Architecture.md#6-restructuring-while-preserving-meaning) |
| Fresh-viewer comprehension | Viewers state topic early and summarise correctly | Test notes | Diagnose | [Failure Modes and Repair](DIAGNOSTICS/Failure-Modes-and-Repair.md) |

## G6 — Picture lock

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Pacing | Intensity map shows purposeful variation; no fatigue notes | Map; test notes | Repair density, not just cut rate | [Rhythm and Pacing](EDITING/Rhythm-and-Pacing.md) |
| Cuts | Full-speed review from before each key cut; no flash frames | Review notes | Re-time | [Cut Decisions](EDITING/Cut-Decisions.md#11-verification-methods-for-cuts) |
| Geography | Fresh viewer can describe space | Test | Neutral shots, re-order | [Continuity and Attention](EDITING/Continuity-and-Attention.md) |
| ★ Interview compression | Every compressed line checked against full answers; speaker review where agreed | Context log | Repair | [Performance Editing](EDITING/Performance-Editing.md#interview-compression-what-is-permissible) |
| ★ Subject review and care | Subjects shown their sections where agreed; welfare checked after difficult material; consent re-confirmed if the context changed | Review notes | Escalate to the producer; repair or re-consent | [Review and Revisions](OPERATIONS/Review-and-Revisions.md), [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md) |
| Lock signed | Named approvers and version | Signed lock | Do not start finishing | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md#2-picture-lock-is-a-process-not-a-guarantee) |
| Turnovers | Tested; handles; correct rate; references | Department confirmations | Re-export | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md#3-handoffs-what-each-department-needs) |

## G7 — Department finishing

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Graphics | Resting frames reviewed as stills; animatic timing approved; brand compliance | Stills; approvals | Redesign | [Design System](MOTION-DESIGN/Design-System.md) |
| Data honesty | Values, units, scales and sources match the source document | Reviewer sign | Correct | [Integration and Data Graphics](MOTION-DESIGN/Integration-and-Data-Graphics.md#3-data-visualisation-faithful-values-honest-motion) |
| VFX | Compositing checklist passed; encoded review | Checklist | Rework | [Compositing and Integration](VFX/Compositing-and-Integration.md#7-compositing-checklist-and-render-handoff-assumptions) |
| ★ Factual alterations | No undisclosed alteration of factual imagery; change log complete | Change log | Restore/disclose | [Repair and Finishing](VFX/Repair-and-Finishing.md#4-generative-fills-removals-and-inserts) |
| Grade | Baseline consistent before look; matches; skin reviewed; graphics re-checked | Gallery; notes | Fix interpretation first | [Color Management](COLOR/Color-Management.md), [Correction and Shot Matching](COLOR/Correction-and-Shot-Matching.md) |
| Dialogue | Intelligible at low level on phone; no over-processing | Listening notes | Back off processing; fill | [Recording and Cleanup](AUDIO/Recording-and-Cleanup.md) |
| Music | Edits musically plausible; licence covers edits | Music-only pass | Re-edit | [Music Editing](AUDIO/Music-Editing.md) |
| Mix | Full playback; mono check; readings recorded | Readings | Re-mix | [Mix Strategy](AUDIO/Mix-Strategy.md#9-the-final-mix-pass) |
| Generated assets | QC checklists passed; logged | AI-use log | Reject | [Generated Media QC](AI-WORKFLOWS/Generated-Media-QC.md), [Voice and Music QC](AI-AUDIO/Voice-and-Music-QC.md) |

## G8 — Text, language and accessibility

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| ★ Caption accuracy | Every line verified against audio by a fluent reviewer | Review notes | Correct | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md#16-verification) |
| Caption timing and placement | Readable; no cut flicker; no collisions in any version | Encoded checks | Re-time/reposition | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| Script rendering | Devanagari (and other scripts) render correctly in every tool and player | Screenshots | Change tool/font | [Localization](TEXT-ACCESSIBILITY/Localization.md) |
| Translation | Meaning reviewed; testimony reviewed by speaker where practical | Reviewer sign | Revise | [Localization](TEXT-ACCESSIBILITY/Localization.md#8-linguistic-review-workflow) |
| Readability | Text legible on the smallest target device | Device check | Resize/shorten | [Typography System](TEXT-ACCESSIBILITY/Typography-System.md) |
| No information by colour alone | Checked | Desaturated review | Add shape/labels | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md#8-audiences-and-their-needs) |

## G9 — Rights and disclosure

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| ★ Register complete | Every person, location, track, archive item, generated asset cleared for every version's use | Register vs version matrix | Clear, replace or remove | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md#15-verification-gate-before-lock-and-before-delivery) |
| ★ Privacy | Masking verified in every version and reflection | Privacy review | Fix | [Repair and Finishing](VFX/Repair-and-Finishing.md#5-privacy-masking) |
| ★ Disclosure | Decisions recorded and implemented | Log | Implement | [Rights, Consent and Disclosure](OPERATIONS/Rights-Consent-and-Disclosure.md#7-disclosure-reconstruction-alteration-and-generated-material) |

## G10 — Versions

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Matrix | Every version has parent, status and profile | Matrix | Complete | [Versioning and Localization](DELIVERY/Versioning-and-Localization.md#1-the-version-matrix) |
| Recomposition | Vertical/square versions recomposed or re-edited, not blindly cropped | Review | Re-edit | [Platform and Format Strategy](DELIVERY/Platform-and-Format-Strategy.md#2-aspect-ratios-and-versioning-strategies) |
| Localization re-edit | Picture adjusted to each narration | Review | Re-edit | [Versioning and Localization](DELIVERY/Versioning-and-Localization.md#4-localization-is-a-re-edit) |

## G11 — Export and QC

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Profiles | Each file matches its current destination specification | Media report | Re-export | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#1-delivery-profiles) |
| ★ Flash and pattern risk | Analysis where required or content is at risk; human review | Report or documented N/A | Re-edit | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#4-flash-and-pattern-risk) |
| Audio compliance | Readings meet each destination's target and method | Readings | Re-mix for destination | [Audio Delivery](DELIVERY/Audio-Delivery.md) |
| Encoded playback | Every delivered file watched in target players | Notes | Fix | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#3-staged-qc) |

## G12 — Delivery and signoff

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| Signoff record | QC stages, evidence, limitations, approver | Signoff sheet | Do not deliver | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md#5-signoff-gate) |
| Reconciliation | Delivered files match the matrix; superseded files moved | Folder vs matrix | Fix | [Versioning and Localization](DELIVERY/Versioning-and-Localization.md#2-naming-that-prevents-stale-exports) |
| Coherence | Coherence audit completed with evidence | Audit | Address material issues | [Creative Coherence and Taste](FOUNDATIONS/Creative-Coherence-and-Taste.md#5-the-coherence-audit) |

## G13 — Archive and restore

| Criterion | Pass when | Evidence | Failure action | Owner |
|---|---|---|---|---|
| ★ Archive complete | Originals, projects with dependencies, masters, documents | Archive manifest | Complete | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md#6-archive-and-restore) |
| Restore tested | A sample opened and played from the archive on another machine | Restore note | Repair archive | [Production and Handoffs](OPERATIONS/Production-and-Handoffs.md#6-archive-and-restore) |
