# Synthetic Voice and Generated Music: Quality, Consent and Rights

**Purpose:** Teach how to evaluate and control synthetic speech and generated music — pronunciation, delivery, continuity, structure, editability — and how to keep three separate questions apart: whether the tool permits the use, whether the person whose voice is involved consented, and whether the result is presented truthfully.

**Applies to:** Text-to-speech narration, voice cloning, synthetic localisation drafts, generated score and songs, temp and final use.

**Prerequisites:** [Generation and Layering](Generation-and-Layering.md), [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md), [Music Selection](../AUDIO/Music-Selection.md).

**Ownership boundaries:** Consent and disclosure formalities are owned by [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md); approval gates for AI tasks by [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md).

**Note on products:** capabilities, voice libraries, licence terms, data retention and commercial-use permissions vary by provider and change frequently. Verify the current terms of any specific service before use; this chapter does not certify any product.

---

## 1. Where synthetic voice fits

| Use | Typical acceptability | Key risks |
|---|---|---|
| Scratch/temp narration for timing an edit or animatic | High | Temp attachment; accidentally shipped |
| Draft localisation to test duration | High as a test | Mistaken for final; mispronunciation |
| Final narration with a licensed synthetic voice | Depends on brief, audience and contract | Lifeless delivery; trust; disclosure expectations |
| Accessibility features (e.g., described video drafts) | Useful with review | Accuracy; tone |
| Voice cloning of a consenting person (e.g., a presenter's own voice for corrections) | Only with informed, specific, documented consent | Scope creep; misuse; authenticity |
| Impersonation of a real person without consent | Not acceptable | Deception; legal and reputational harm |
| Synthetic speech presented as a real person's recorded words in factual work | Not acceptable without disclosure, and often not acceptable at all | Fabricated testimony |

**Do not use impersonation as a default technique.** Even when a voice "sounds like" a type (a doctor, a news anchor), consider whether it creates false authority (see [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md#53-warm-voice-versus-credible-content)).

## 2. Three separate questions

| Question | Who answers | Evidence |
|---|---|---|
| **Generation permission:** Does the tool's licence permit this use (commercial, broadcast, paid ads, territory, term)? Who owns the output? Is input data retained or used for training? | Producer, legal, from the provider's current terms | Saved copy/date of terms; account/licence tier |
| **Performer consent:** If a real person's voice is used, cloned or imitated, did they give informed consent for *this* use — scope, duration, languages, edits, compensation, withdrawal? | The person, documented by the producer | Signed consent specific to synthetic use |
| **Factual authenticity:** Will the audience understand what they are hearing? Is synthetic speech presented as a recording of someone saying it? | Director/editor, with disclosure rules from the commissioner or platform | Disclosure decision recorded; label or credit if required |

A "yes" to one does not imply "yes" to the others. A tool may permit commercial use of a voice clone, but the cloned person may not have consented to the specific line; the person may consent, but presenting the line as unscripted testimony would still mislead.

## 3. Evaluating synthetic voice

| Dimension | What to check | Common failure |
|---|---|---|
| Pronunciation | Names, places, technical terms, numbers, abbreviations, loanwords in mixed-language speech | "kidney" stressed oddly; Hindi loanwords anglicised; "100 mL" read as "one hundred em ell" |
| Language and accent | Matches audience expectation; consistent within the piece | Accent drift between generations |
| Emotional delivery | Intent and emphasis match meaning | Uniform cheerfulness; stress on the wrong word |
| Breaths | Present at plausible phrase boundaries, or deliberately absent | Breathless delivery; breaths in odd places |
| Pacing | Room for picture and comprehension | Too fast for demonstration steps |
| Phrase continuity | Lines generated separately sound like the same performance | Pitch, energy or tone jumps between lines |
| Consistency | Regenerating a line yields a compatible take | Different "mood" each time |
| Artefacts | Clicks, metallic tone, glitches, garbled syllables, unexpected sounds | Subtle garble on uncommon words |
| Intelligibility | Clear on phone speakers at low volume | Over-processed sibilance |

**Control techniques (tool-dependent):** phonetic spellings or pronunciation dictionaries; punctuation and line breaks to shape phrasing; generating whole paragraphs rather than isolated lines for continuity; selecting among multiple takes; editing breaths and pauses manually afterwards.

## 4. Evaluating generated music

| Dimension | What to check | Common failure |
|---|---|---|
| Structural drift | Does the piece maintain coherent form, or wander? | Sections that do not relate; tempo or key drift |
| Transitions | Do sections connect musically? | Abrupt or smeared changes |
| Motifs | Is there a recognisable idea that can return? | No identity; or a motif that resembles an existing work too closely |
| Stems | Can layers be separated for editing and mixing? | Single mixed file only; separation tools introduce artefacts |
| Endings | A real ending, not a fade or an abrupt stop | Endings are a frequent weakness |
| Editability | Clear bars and phrases for cutting to picture | Ambiguous timing; inconsistent tempo |
| Audio quality | Noise, artefacts, distortion, unstable timbre | Warble, smeared transients |
| Unexpected content | Vocal-like sounds, words, recognisable melodies | Accidental lyrics or imitation |
| Licensing and terms | Commercial use; ownership; content-identification conflicts on platforms | Unclear rights; platform claims |

**Ownership uncertainty:** in some jurisdictions, copyright protection for material generated without meaningful human authorship is limited or uncertain. That can affect exclusivity (others may generate similar material) and enforcement. This is a practical caution, not legal advice; consult the rights owner document and counsel for commercial work.

## 5. Artefact and rights checklist before approval

Every synthetic voice or generated music asset must pass this checklist before it can appear in an approved version. Record results in the AI-use log.

| # | Check | Pass criterion | Method |
|---|---|---|---|
| 1 | Clicks and pops | None audible | Headphones at raised gain; waveform inspection at transitions |
| 2 | Warble / metallic tone | None noticeable at normal level | Headphones and speakers |
| 3 | Noise floor | Consistent; no pumping | Listen in pauses |
| 4 | Unexpected speech or vocal sounds | None | Headphones at raised gain through the whole file |
| 5 | Repeated patterns | No obvious loops unless intended | Listen through; check for identical phrases |
| 6 | Sync | Speech aligned with picture/text; music edits on phrase | Full-speed playback with picture |
| 7 | Intelligibility | Every word understood on phone speakers at low volume | Listener test |
| 8 | Pronunciation | Names and terms correct, verified by a fluent speaker | Glossary check |
| 9 | Resemblance | No close resemblance to a specific existing recording, composition or identifiable person's voice (unless licensed/consented) | Listening by someone familiar with the genre; platform content-ID pre-check where available |
| 10 | Generation permission | Current terms permit this use; saved and dated | Producer check |
| 11 | Performer consent | Documented for any real person's voice | Consent file |
| 12 | Disclosure | Decision recorded; label/credit applied if required | Director/producer |
| 13 | Provenance record | Tool, version, prompt/settings, date, operator logged | AI-use log |

## 6. Worked example 1 — Synthetic narration in the explainer workflow (hypothetical, Project C)

**Plan:** use synthetic narration in both languages for the animatic, to time animation and edit before human narrators record.

| Stage | Synthetic voice role | Decision |
|---|---|---|
| Animatic | Temp narration in English and Hindi | Accepted: fast; reveals that the Hindi mechanism section runs longer |
| Picture lock candidate | Temp still in place | Risk: team grows used to the synthetic cadence |
| Final | Human narrators (female in both languages, per [Localization](../TEXT-ACCESSIBILITY/Localization.md#10-worked-example-2--bilingual-labels-and-narration-hypothetical-project-c-english--hindi)) | Chosen: warmth, trust with a mixed-literacy audience, correct pronunciation of local terms, natural emphasis |

**Observed synthetic-voice issues (hypothetical):** the Hindi voice pronounces "कैंडल" with an unnatural stress; numbers in the chart narration are read too fast; every sentence has the same intonation contour.

**Why not ship the synthetic voice?** The brief's success depends on trust and comprehension among viewers who may be sceptical of technology; a human narrator's natural emphasis on "no soap" and pauses after steps proved more effective in a small test (hypothetical). Cost of human narration fits the budget. **Boundary:** for a frequently updated internal training library with dozens of short modules and no trust-sensitive audience, a licensed synthetic voice with careful pronunciation control might be the right choice — disclosed per the organisation's policy.

**Temp risk control:** the temp narration files are named `TEMP-SYNTH-VO-DO-NOT-SHIP` and placed on a track coloured red; the QC checklist includes "no temp synthetic VO in timeline".

## 7. Worked example 2 — Generated score sketch versus library track (hypothetical, Project A)

**Plan:** a generated sketch (brief 3 in [Generation and Layering](Generation-and-Layering.md#example-brief-3--score-sketch-hypothetical-project-a-animatic-only)) tests whether a late cue helps the ending.

**Evaluation of the sketch (hypothetical):**

| Dimension | Observation |
|---|---|
| Structure | Mostly stable; a slight tempo drift at 45 s |
| Transitions | The harmonic change is smooth |
| Ending | Fades rather than resolving — weak |
| Artefacts | Faint warble on piano notes |
| Stems | Not available |
| Rights | Tool terms permit commercial use for paid accounts; ownership language unclear for this jurisdiction |

**Decision:** the sketch answers the creative question — the late cue works in the fresh-viewer test. For the final, the team licenses a library cue matching the functional description (with stems and a real ending), rather than using the sketch, because of the weak ending, artefacts, lack of stems and ownership uncertainty. The sketch is logged as temp only.

## 8. Counterexample and repair — cloning the founder for a legal fix

**Hypothetical counterexample.** After the Arc brand film is locked, legal requires one of Dev's lines to change from "Arc keeps you healthy" to "Arc helps you notice your habits." The founder is travelling. An editor uses a voice-cloning tool trained on the interview audio to generate the new line in Dev's voice and edits it in, covering the mouth with a cutaway. The producer discovers this at QC.

**Diagnosis:**
- **Performer consent:** Dev never consented to synthetic use of their voice.
- **Factual authenticity:** the brand film presents Dev speaking in an interview; a synthetic line is presented as their recorded words.
- **Generation permission:** the tool's terms require the account holder to have rights to the voice — not met.

**Repair:**
1. Remove the synthetic line immediately; quarantine the generated file; record the incident in the AI-use log.
2. Name the conflict to the decision owner (the producer and brand lead): the fix cannot ship as made.
3. Options: (a) a remote pickup — Dev records the new line on a phone in a quiet room, using a simple guide (see [Recording and Cleanup](../AUDIO/Recording-and-Cleanup.md)); (b) restructure the edit to remove the claim entirely; (c) if Dev, fully informed, prefers a synthetic line and documents consent, disclose according to the commissioner's and platform's policy — still a weaker choice for a film whose value is the founder's authenticity.
4. Chosen: (a), with careful matching of room tone and EQ; a cutaway covers the slight perspective difference.

**Verification:** Dev approves the line; legal approves the wording; the dialogue editor confirms the pickup matches; QC confirms no synthetic voice remains.

## 9. Micro-decisions

- Name all synthetic temp files clearly and keep them on visibly coloured tracks.
- Generate long passages in one pass for voice continuity, then edit.
- Keep a pronunciation glossary shared between synthetic and human sessions.
- Save the provider's terms (with date) alongside generated assets.
- Before approval, listen to every synthetic file in full on headphones; problems hide in the middle.

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "Phone-menu" narration | Uniform synthetic intonation | Human narrator; or careful phrasing control and editing |
| Mispronounced names/terms | No pronunciation control | Phonetic spellings; glossary; fluent review |
| Music wanders | Structural drift | Edit to stable sections; licensed alternative |
| Platform claim on generated music | Resemblance or shared generated material | Replace; check terms; document |
| Temp synthetic VO shipped | No naming/QC control | Naming convention; QC checklist item |
| Synthetic speech of a real person without consent | Process failure | Remove; consent policy; escalation |

## 11. Verification

- Complete the [artefact and rights checklist](#5-artefact-and-rights-checklist-before-approval) for every asset.
- Fresh-listener tests for intelligibility and trust where the voice carries content.
- Confirm consent and disclosure records before lock.

## Dependencies

- Depends on: [Generation and Layering](Generation-and-Layering.md), [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md), [Music Selection](../AUDIO/Music-Selection.md), [Music Editing](../AUDIO/Music-Editing.md).
- Governance: [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).
- Gate: [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

The separation of permission, consent and authenticity is `[Practice]` in responsible media production. Evaluation dimensions are `[Practice]`-based; specific failure patterns are `[Heuristic]` and tool-dependent. Statements about copyright in AI-generated output are deliberately cautious and jurisdiction-dependent — not legal advice. Examples are `[Illustrative]`.
