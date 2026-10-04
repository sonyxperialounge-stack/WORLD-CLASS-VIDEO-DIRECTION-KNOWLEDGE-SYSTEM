# Generated Media: Failure Modes and Quality Control

**Purpose:** Teach how to inspect generated and AI-altered images and video — the characteristic failures (changing identities, hands and objects, temporal flicker, inconsistent light, unphysical camera motion, invented text, stereotypes, false factual implications) — and a QC procedure that separates a convincing preview from a production-ready, truthful, rights-cleared asset.

**Applies to:** Generated stills, generated video shots, AI-extended frames, AI-altered footage, storyboards and concept frames.

**Prerequisites:** [Assistance and Control](Assistance-and-Control.md).

**Related owners:** Disclosure and rights in [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md); generative fills in footage in [Repair and Finishing](../VFX/Repair-and-Finishing.md#4-generative-fills-removals-and-inserts); synthetic audio in [Voice and Music QC](../AI-AUDIO/Voice-and-Music-QC.md).

---

## 1. Plausible is not true

Generated imagery is optimised to look plausible. Plausibility is a property of appearance; truth is a property of the relationship between an image and the world. A generated shot of "a rural health clinic at night" can be convincing and still be false as evidence of any real clinic. In factual work, this gap is the central risk. In fiction and advertising, the risks are different — consistency, quality, implied claims, stereotypes, rights — but plausibility still is not quality.

## 2. Characteristic failure modes

| Failure | What it looks like | Why it happens (generally) | Where it matters most |
|---|---|---|---|
| Identity drift | A face, body or costume changes subtly between frames or shots | Models do not maintain a persistent identity unless constrained | Any shot with people; continuity across shots |
| Hands and fine anatomy | Extra or fused fingers; impossible joints; hands merging with objects | Complex, variable structures | Close-ups; product handling |
| Object instability | Objects change shape, count or position; labels morph | Weak temporal constraints | Product shots; props |
| Temporal flicker / shimmer | Textures crawl; details pop in and out | Frame-to-frame inconsistency | Video at full speed; large displays |
| Inconsistent light | Shadows point different ways; highlights don't match sources | No physical light model | Integration with live action |
| Unphysical camera movement | Parallax wrong; geometry warps as the camera moves; "floating" motion | Approximate scene understanding | Moving shots; inserts in edited sequences |
| Invented text | Signs, labels and screens with gibberish or plausible but wrong words | Text rendering limits; hallucination | Any visible text; especially factual or branded |
| Stereotype reinforcement | Generic, clichéd depictions of places, communities, professions, genders | Patterns in training data | Social representation; NGO and educational work |
| Factual implication | An image that implies a real event, person, location or scientific fact | Plausible depiction | Documentary, news, health, education |
| Watermarks or recognisable elements | Fragments of logos, artworks, or recognisable likenesses | Training data echoes | Rights, brand safety |

## 3. QC procedure for generated visuals

Run in order; stop and reject at the first failure that cannot be repaired cheaply.

| Step | Check | Method | Pass criterion |
|---|---|---|---|
| 1. Purpose and contract | Is generated imagery permitted for this use and genre? | Approval matrix ([Assistance and Control](Assistance-and-Control.md#5-the-approval-matrix)) | Permitted, with conditions recorded |
| 2. Temporal playback | Flicker, shimmer, morphing | Full speed on a large display and on the target device, several viewings | No visible instability at normal viewing |
| 3. Frame inspection | Hands, faces, objects, edges, text | Step through key frames at 100% | No anatomical or object errors in visible areas |
| 4. Identity and continuity | Same person/object across frames and shots | Side-by-side comparison | Consistent |
| 5. Geometry and physics | Perspective, parallax, gravity, scale | Watch camera moves; compare with plates | Plausible for the shot |
| 6. Light | Direction, softness, colour match surrounding footage | Compare with adjacent shots | Consistent |
| 7. Text | All visible text correct, intended and approved | Read every sign, label, screen | Correct or removed |
| 8. Representation | Stereotypes, dignity, cultural accuracy | Review by people with relevant knowledge | No stereotyping or misrepresentation |
| 9. Factual review | Does the image imply facts? Are they true? Is it labelled? | Subject-matter reviewer; disclosure decision | No false implication; disclosure as required |
| 10. Rights and provenance | Tool terms; recognisable elements; provenance records; content credentials if used | Producer; legal for commercial use | Terms permit; log complete |
| 11. Delivery conditions | Encoded output, all aspect ratios | Encoded review | Artefacts not exposed by compression or crops |

## 4. Preview versus production-ready

| | Preview | Production-ready |
|---|---|---|
| Purpose | Answer a creative question | Appear in a deliverable |
| Standards | Direction and feel | All QC steps pass |
| Labelling | "CONCEPT — not for delivery" | Approved version with log entry |
| Typical uses | Storyboards, look tests, pitch frames, temp inserts | Backgrounds, stylised inserts, effects elements in permitted contexts |

**Risk:** previews presented to clients can set expectations the shoot cannot meet ("the generated frame had perfect sunset light; why doesn't the footage?"). Label previews and explain their role.

## 5. Worked example 1 — Storyboard exploration (hypothetical, Project D)

**Use:** the director generates concept frames to explore lighting moods for the night interior: "pools of warm lamp light, darkness between two people".

**Value:** the frames help the crew discuss pool sizes, the darkness between characters, and the streetlight accent. Two frames become lighting references.

**Problems observed:** the frames show an apartment with architectural features unlike the real location; one frame shows a third figure in the background; light sources in some frames are physically implausible.

**Handling:** frames labelled "concept"; used only to discuss function (pool size, contrast), translated into the real location's possibilities by the cinematographer (see [Practical Setups](../LIGHTING/Practical-Setups.md#3-worked-example-2--night-interior-with-practical-fixtures-hypothetical-project-d-the-spare-key-23976-fps-150-s)); never shown to the cast as "what it will look like".

## 6. Worked example 2 — Rejecting generated B-roll in an explainer (hypothetical, Project C)

**Proposal:** a producer suggests generating a shot of "bacteria being trapped in a ceramic filter, microscope view" for realism.

**Assessment:**
- **Factual implication:** a photoreal "microscope" image implies real microscopy of this filter. It would be invented evidence.
- **Scientific accuracy:** generated "bacteria" may be wrong in shape, scale or behaviour; the advisor cannot verify generated details.
- **Contract:** educational content requires accuracy and clear signalling of what is real.

**Decision:** reject. Use the clearly diagrammatic animation (labelled "not to scale"; see [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md#4-worked-example-1--a-complex-process-visualisation-hypothetical-project-c-clear-water)). If real microscopy imagery is wanted, license real footage from a credible source with provenance.

## 7. Worked example 3 — QC of a generated background (hypothetical, Project B)

From the comparison in [Assistance and Control](Assistance-and-Control.md#8-worked-example-2--a-generated-product-background-hypothetical-project-b-916-social-variant), the generated background option is run through QC:

| Step | Result |
|---|---|
| Temporal playback | Countertop texture shimmer visible on a 27-inch display — **fail** |
| Light | Background window reflection on a kettle implies light from the right; product key from left — **fail** |
| Text | A blurred cereal box shows pseudo-letters — would need removal |
| Representation, factual | Not relevant (designed environment) — pass |
| Rights | Tool terms permit commercial use on the current plan (checked and saved) — pass |

**Outcome:** rejected in favour of the conventional extension; logged as a preview that informed composition.

## 8. Counterexample and repair — stereotyped generated imagery in an NGO film

**Hypothetical counterexample.** A small NGO, lacking footage for a fundraising film about a rural school programme, uses generated images: "children in an Indian village classroom". The results show dusty, broken classrooms, all children barefoot in identical clothing, a generic "village" with architecture from no particular region, and a chalkboard with pseudo-Hindi letters that are not real words. A supporter from the region points out that the images look nothing like the actual schools, which have painted walls and uniforms; the fake script is noticed immediately by Hindi readers.

**Diagnosis:** stereotype reinforcement (poverty imagery), factual misrepresentation of real places served by the programme, invented text, and undisclosed generation in a factual appeal.

**Repair:**
1. Remove generated images.
2. Obtain real footage or photographs from the programme's schools with consent (photos taken by staff are acceptable with releases).
3. If illustration is needed while real footage is gathered, use clearly illustrated (non-photoreal) artwork, labelled, with community review.
4. Add a policy to the approval matrix: no photoreal generated depictions of real communities in factual or fundraising contexts.

**Verification:** review by staff and community members; Hindi readers confirm all visible text.

## 9. Micro-decisions

- Read every piece of text in generated imagery, even background text.
- Watch generated video on a large display; shimmer often hides on small screens.
- Compare generated inserts with the shots before and after them, not in isolation.
- Save the generation record (prompt, tool, version, seed or settings if available, date, terms) with the asset.
- When a generated element survives into a deliverable, decide and record disclosure before lock.

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Viewers sense "something off" | Temporal or physical inconsistency | QC at full speed; reject or replace |
| Text errors noticed by readers | Invented text | Remove or replace with designed text |
| Community objects to depiction | Stereotypes; misrepresentation | Real material; community review |
| Client expects generated look on set | Previews not labelled | Labelling; expectation setting |
| Rights challenge | Terms not checked; recognisable elements | Check terms; remove; log |
| Factual complaint | Generated imagery implied real events | Remove; correct; disclose |

## 11. Verification

- Against original sources and real references.
- Against project intent and genre contract.
- Rights and provenance records complete.
- Temporal playback at full speed on large and small displays.
- Final delivery conditions: encoded, all aspect ratios.

## Dependencies

- Depends on: [Assistance and Control](Assistance-and-Control.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md).
- Related: [Repair and Finishing](../VFX/Repair-and-Finishing.md), [Compositing and Integration](../VFX/Compositing-and-Integration.md), [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md).

## Confidence summary

The plausible-versus-true distinction and the QC procedure are `[Practice]`. Failure modes are `[Heuristic]` descriptions of common behaviour in current generative tools; specific tools may improve or behave differently. Policies on stereotyped and factual imagery are `[Practice]` grounded in documentary and NGO communication ethics. Examples are `[Illustrative]`.
