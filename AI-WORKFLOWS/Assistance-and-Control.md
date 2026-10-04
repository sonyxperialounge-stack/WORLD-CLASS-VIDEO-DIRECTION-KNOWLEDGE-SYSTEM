# AI Assistance and Human Control

**Purpose:** Teach how to classify AI-assisted tasks in production by intent and evidence, where automation is a useful first pass and where it must not decide, how to keep work reversible, how to handle client data, how to write useful briefs for AI tools, and how to run an approval matrix that keeps humans accountable.

**Applies to:** Transcription, logging, assembly, restoration, masking, translation, captions, storyboards, generated media and review assistance — any AI involvement in a project.

**Prerequisites:** [Decision Method](../FOUNDATIONS/Decision-Method.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

**Owns:** The AI approval matrix and AI-use log. Quality control of generated images and video is in [Generated Media QC](Generated-Media-QC.md); synthetic audio in [Generation and Layering](../AI-AUDIO/Generation-and-Layering.md) and [Voice and Music QC](../AI-AUDIO/Voice-and-Music-QC.md).

**Note on products:** AI services change capabilities, prices, data-retention and training policies, and commercial terms frequently. This chapter is tool-independent. Before using a named service with project material, check its current terms; record the check.

---

## 1. Classify the task before choosing a tool

| Task class | Typical use | Input requirements | Likely failure modes | Human acceptance gate |
|---|---|---|---|---|
| Transcription and search | Make speech searchable; draft transcripts | Clean audio; language/dialect settings; name list | Misheard names, numbers, technical terms; negation errors; code-switching; speaker confusion; invented words in unclear passages | Verify every line used in the edit, captions or quotes |
| Logging and tagging | Describe shots; detect faces, objects, scenes | Representative media | Wrong labels; missed context; privacy-sensitive detection | Spot-check; never use as rights clearance |
| Rough assembly | Suggest selects or a first cut from transcripts | Transcripts; story intent | Stitching sentences into claims; ignoring performance and pauses; choosing fluent over truthful | Editor rebuilds with full-context review — the human method is the paper edit (see [Paper Edit and Assembly](../OPERATIONS/Paper-Edit-and-Assembly.md)) |
| Restoration and enhancement | Denoise, upscale, deblur, dialogue isolation | Source media | Invented detail; artefacts; altered faces or speech | Comparison with source; no invented evidence |
| Masking and segmentation | Isolate subjects; rotoscoping assistance | Media | Edge errors; temporal flicker; missed frames | Frame-by-frame check on critical masks |
| Translation drafts | First-pass translation of scripts, subtitles | Source text; context; glossary | Literalism; wrong gender forms; terminology errors; tone | Translator and fluent reviewer (see [Localization](../TEXT-ACCESSIBILITY/Localization.md)) |
| Caption drafts | Timed captions from speech | Final audio; style rules | Accuracy, timing, line breaks; sound labels missing | Caption editor verification |
| Storyboard and look exploration | Concept frames; mood references | Brief | Generic imagery; stereotypes; implied promises the shoot cannot deliver | Director review; labelled as exploration |
| Generated media (images, video, audio) | Backgrounds, inserts, temp elements, final elements | Brief; references; rights | Artefacts; identity changes; factual misrepresentation; rights uncertainty | [Generated Media QC](Generated-Media-QC.md) |
| Review assistance | Spellcheck, continuity flags, QC alerts | Exports | False positives/negatives | Human QC remains the gate |

## 2. Where automation helps — and where it must not decide

**Useful as a first pass:** finding words in hours of interview; drafting transcripts and captions; flagging possible technical issues; producing many rough options for exploration; accelerating rotoscoping; drafting translations to test duration.

**Must not decide:**

| Decision | Why |
|---|---|
| Meaning of testimony | Automatic selection cannot judge whether an edit preserves what a person meant |
| Emotional emphasis | Which moment carries a story is an editorial judgement tied to the brief and the contract |
| Consent and privacy | Detection is not permission; only people and documents establish consent |
| Factual truth | A plausible output is not evidence |
| Accessibility compliance | Captions must be verified by people; tools can misrepresent speech |
| Representation of people and communities | Stereotype and dignity judgements require human review, ideally by people with relevant lived experience |

## 3. Reversible assistance versus destructive or deceptive alteration

| Reversible assistance | Destructive or deceptive alteration |
|---|---|
| A transcript used to find a moment; the edit uses the original audio | Replacing a spoken word with a synthetic one in testimony |
| A denoised copy alongside the original | Overwriting original media with "enhanced" versions |
| A generated storyboard frame labelled as concept | A generated image presented as documentation |
| A mask that can be adjusted | A generative removal of evidence without record |

**Practice** `[Practice]`:
- Keep original media untouched; AI outputs are derived media in separate folders with clear names.
- Version every AI-assisted output; record tool, version, settings, operator and date in an **AI-use log**.
- Preserve the ability to reject: never build so much on a generated element that removing it is impossible late in the schedule.

## 4. Data handling: do not assume uploads are allowed

Client footage, unreleased products, interviews with private individuals and medical settings carry confidentiality obligations. Before uploading anything to a third-party AI service:

| Check | Why |
|---|---|
| Contract and NDA terms | Many forbid sharing material with third parties |
| Consent scope | Subjects may have consented to filming for a specific film, not to processing by external services |
| Service terms on retention and training | Some services retain inputs or may use them to improve models; terms vary by plan and change |
| Data location | Some clients and jurisdictions restrict cross-border data transfer |
| Sensitive categories | Health, minors, location, identity documents |

**Alternatives by capability:** where uploads are not permitted, use tools that run locally on project machines, or vendor offerings with contractual guarantees appropriate to the project — verified, not assumed. Where neither exists, do the task conventionally.

## 5. The approval matrix

The approval matrix lists each AI-assisted task in the project with its permitted scope and its human gate. It is agreed early and updated when a new use appears.

### Filled approval matrix (hypothetical, Projects A, B and C)

| Task | Sensitive input? | Permitted transformation | Required reviewer | Error signals | Verification |
|---|---|---|---|---|---|
| A: Hindi interview transcription | Yes — private individual, medical setting | Local transcription tool only (hospital agreement prohibits external upload); transcript as search aid | Bilingual assistant editor | Misheard medical terms; English code-switching rendered as nonsense; negation | Every quoted or captioned line checked against audio |
| A: Dialogue noise reduction | Yes | Derived copies; originals kept | Editor/mixer | Warble; altered words | Matched-loudness A/B against original |
| A: Generative removal or fill | Yes | **Not permitted** in observational footage | Director | — | — |
| A: Privacy blur assistance (face tracking) | Yes | Tracking assistance; human-checked masks | Producer | Lost tracks; missed reflections | Frame review of every masked shot |
| B: Phone screen UI | No (approved product UI) | Compositing of approved UI; no generated UI | Brand lead, legal | Wrong values; inconsistent behaviour | Comparison with approved build |
| B: Generated background for a social variant | No (product only) | Background generation behind real product footage; product pixels untouched | Director, brand lead, legal | Artefacts; implied claims; lighting mismatch | [Generated Media QC](Generated-Media-QC.md) checklist |
| B: Synthetic voice | Founder's voice | **Not permitted** without explicit written consent and disclosure decision | Producer | — | — |
| C: Translation draft for timing | No | Draft only; not used for recording | Translator, reviewer | Gender forms; terminology | Translator rewrites; reviewer approves |
| C: Caption drafts | No | Draft; human-edited | Caption editor | Timing, accuracy | Checked on encoded files |
| C: Generated B-roll of "contaminated water under a microscope" | — | **Not permitted** — factual imagery must be real or clearly labelled diagrammatic animation | Advisor | — | — |

## 6. Writing useful AI briefs

| Element | Content | Example (Project B background) |
|---|---|---|
| Intent | What the output must achieve | "A calm, warm-neutral morning kitchen behind the real product shot for the 9:16 social variant" |
| Context | Where it will be used; surrounding shots | "Follows the morning montage; precedes the end card" |
| References by function | What to take from references, not "make it like X" | "Soft window light from the left; uncluttered surfaces; muted wood" |
| Constraints | Technical and brand limits | "Matches 23.976 fps plate; soft focus to match f/2.8 depth; no brand logos; no people" |
| Positive requirements | What must be present | "Window on the left consistent with the plate's key; background slightly warmer than product" |
| Prohibited changes | What must not happen | "Product pixels untouched; no added text; no other bottles; no health-related imagery" |
| Acceptance conditions | Measurable or checkable criteria | "No visible artefacts at full speed on phone and 27-inch display; lighting direction matches; legal approves" |

### Iterate from observed defects, not adjectives

Weak iteration: "More realistic. More premium. More cinematic." Strong iteration names the observed defect and the change: "The window light in the background comes from the right; the product's key is from the left — move the background's window to the left." "The countertop texture shimmers frame to frame — reduce texture detail or use a still background with a subtle parallax move."

### Preview versus production-ready

A generated **preview** answers a creative question (is this direction worth pursuing?). A **production-ready** asset meets technical, rights, consistency and truth requirements. Many generated outputs are excellent previews and poor production assets. Label previews clearly and keep them out of deliverable timelines.

## 7. Worked example 1 — Interview-assisted logging (hypothetical, Project A)

**Workflow:**

| Step | Who/what | Output | Human control |
|---|---|---|---|
| 1. Local automatic transcription of 70 minutes of Hindi with English medical terms | Local tool on the edit machine | Draft transcript with timestamps | Status marked "unverified" |
| 2. Assistant editor reviews and corrects the transcript in passes, prioritising sections flagged in the director's live log (see [Interview Craft](../STORY/Interview-Craft.md#9-follow-up-listening-and-live-logging)) | Bilingual assistant | Corrected transcript; uncertain passages marked | Corrections against audio |
| 3. Search for themes (fatigue, daughter, Sunita) | Editor using transcript search | Candidate moments | Editor watches each candidate in full context |
| 4. Performance assessment | Editor and director watching | Selects with ratings | Entirely human — pauses, tone, truth |
| 5. Context check | Editor | Each select linked to full answer | Human |
| 6. Caption basis | Caption editor | Captions from the verified transcript, re-timed | Verified on encoded file |

**What stays human-controlled:** selection, meaning, emphasis, consent decisions, captions' final text.

**When conventional is preferable:** the 4-second pause and the self-correction were found by the director's live log, not by search — transcripts do not record silence or tone. For the most important passages, watching beats searching.

**Hypothetical transcript error caught:** "मैं थकी नहीं थी" (I was not tired) transcribed as "मैं थकी थी" (I was tired) — a negation dropped in a noisy passage. Caught in step 2; would have reversed meaning in captions.

## 8. Worked example 2 — A generated product background (hypothetical, Project B, 9:16 social variant)

**Situation:** the studio kitchen set was framed for 16:9; the vertical variant of one product shot lacks background above the product. Options:

| Option | Description | Assessment |
|---|---|---|
| A. Reframe only | Crop tighter | Product too large; ring's glow loses context |
| B. Reshoot the vertical framing | Half-day pickup | Highest quality; cost and schedule |
| C. Extend the background with conventional compositing (photographed plates of the same set) | Use stills of the set shot during the shoot | Good if stills exist (they do, partially) |
| D. Generate the missing background area, keeping product pixels untouched | Fast | Needs QC; legal check that nothing implies claims |

**Comparison method:** produce C and D for the same shot; review both side by side at full speed on phones and a large display; check the [Generated Media QC](Generated-Media-QC.md) checklist for D.

**Result (hypothetical):** D has a subtle shimmer in the countertop texture across frames and a window reflection inconsistent with the product's highlights; C is stable. **Choice: C.** D remains a preview that guided the composition of C.

**When generation would have been chosen:** if no set stills existed and the background were a static, low-detail wall — a simple case where temporal consistency is easier — after QC and approval.

## 9. Counterexample and repair — the automated highlight clip

**Hypothetical counterexample.** For the 60-second social excerpt of Project A, a junior editor uses an automated "highlights" feature that picks the "most engaging" sentences from the transcript and assembles them. The output joins "I stopped noticing" (from one answer) with "the hospital doesn't care" (a paraphrase the tool generated from a different, more nuanced answer: "sometimes it feels like nobody up there sees us"). The clip is posted to a review link; the nonprofit's communications lead loves it.

**Diagnosis:**
- The tool stitched answers and paraphrased testimony — fabricated speech in captions and a misleading claim about the hospital.
- No human context check; no approval matrix entry for automated assembly.
- Risk to Asha's employment and to the organisation's credibility.

**Repair:**
1. Withdraw the clip from the review link; inform the producer.
2. Rebuild the excerpt manually from verified selects with full-context checks (see [Performance Editing](../EDITING/Performance-Editing.md#interview-compression-what-is-permissible)).
3. Add "automated assembly" to the approval matrix as "exploration only; never for review or publication".
4. Asha reviews the new excerpt.

**Verification:** every line in the excerpt matches the original audio and meaning; Asha approves; the producer signs off.

## 10. Micro-decisions

- Mark every AI-derived file name with a suffix (e.g., `_AIDRAFT`, `_AIDENOISE`) and keep them in derived folders.
- Log each AI use in the AI-use log at the time of use, not afterwards.
- Never allow an AI-generated transcript line into captions without listening to it.
- Keep generated previews out of the main timeline or on clearly coloured tracks.
- When unsure whether an upload is allowed, don't upload; ask the producer.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Quotes don't match audio | Unverified transcripts | Verify against audio |
| Testimony misrepresented | Automated assembly or paraphrase | Manual rebuild; context checks |
| Confidential material leaked/at risk | Uploads without checking terms | Data policy; local tools; incident report |
| Generated asset fails late | Too much built on it | Keep ability to reject; parallel conventional option |
| Endless iteration | Adjective-based prompting | Defect-based iteration; stop criteria |
| Disclosure missed | No AI-use log | Log; review before lock |

## 12. Verification

- Output checked against original sources (audio, footage, documents).
- Check against project intent and the brief.
- Rights and terms confirmed and recorded.
- Temporal playback for any visual AI output.
- Final delivery conditions (encoded files, all versions).
- Do not recommend AI for a stage merely because it is available; record when conventional methods were chosen and why.

## Dependencies

- Depends on: [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md), [Footage Assessment](../OPERATIONS/Footage-Assessment.md).
- Companion: [Generated Media QC](Generated-Media-QC.md).
- Related: [Localization](../TEXT-ACCESSIBILITY/Localization.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Repair and Finishing](../VFX/Repair-and-Finishing.md), [Voice and Music QC](../AI-AUDIO/Voice-and-Music-QC.md).

## Confidence summary

Task classification, human gates, reversible workflows and data-handling checks are `[Practice]` in responsible production. Failure modes are `[Heuristic]` summaries of common behaviour in current tools, which change quickly. No product capability or term is asserted. Examples are `[Illustrative]`; the Hindi transcript example should be reviewed by a fluent speaker before reuse.
