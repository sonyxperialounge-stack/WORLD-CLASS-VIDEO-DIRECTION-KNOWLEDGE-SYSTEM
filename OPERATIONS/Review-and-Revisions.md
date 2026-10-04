# Review, Notes and Revisions

**Purpose:** Teach how to treat review notes as symptoms to diagnose rather than instructions to execute, how to resolve conflicting notes, how to annotate reviews so they are actionable, how to classify notes by type, and how to protect communication and truth when a requested change would damage them.

**Applies to:** Internal reviews, client rounds, advisor and legal reviews, subject reviews and final approvals.

**Prerequisites:** [Creative Brief](../FOUNDATIONS/Creative-Brief.md) (the intent every note is tested against), [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md) (change process).

**Owns:** The review log format and the note-translation method. The change-impact map is defined in [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md#5-the-brief-change-process).

---

## 1. Notes are symptoms

Reviewers describe experiences: "it's too slow", "it doesn't feel premium", "the music is wrong", "make the logo bigger". These notes are valuable — they report something real about how the piece felt to someone — but their proposed cures are often wrong. The expert's job is to **diagnose the cause**, propose repairs that address it, and agree an acceptance criterion.

### Translating common notes

| Note | Possible causes | Clarifying questions | Alternative repairs | Acceptance criterion |
|---|---|---|---|---|
| "Too slow" | Repetition; low information density; a section without a viewer question; long setup; music too languid; performance pauses | "Where did you first feel it?" "What were you waiting for?" | Remove repetition; move the hook earlier; restructure; adjust music; trim specific pauses — not necessarily faster cutting (see [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md)) | Reviewer no longer reports a slow point; fresh viewer comprehension unchanged or better |
| "Not premium" | Busy graphics; cheap-looking transitions; harsh highlights; inconsistent typography; music genre; audio quality; too many claims | "Which moment felt least premium?" "Show me something that feels premium to you." | Simplify graphics; refine typography; control reflections and highlight roll-off; restrain motion; reduce claims | Reviewer identifies the moment as fixed; brand lead agrees with the reference function |
| "Music is wrong" | Genre associations; energy mismatch; lyric meaning; too emotional; fights dialogue; temp attachment | "Wrong how — energy, mood, style, or it's in the way?" "What should the viewer feel here?" | Different track by function; edit structure; reduce level; remove music (see [Music Selection](../AUDIO/Music-Selection.md)) | Agreed functional description satisfied |
| "Make the logo bigger" | Brand not recognised; logo appears too briefly; logo competes with other elements; stakeholder visibility concern | "Is the concern that people won't know who made this?" | Show the brand earlier (product in hand); hold the end card longer; increase contrast; add audio brand cue; modest size increase within the design system | Brand recall in a small test; brand guidelines respected |
| "Can it be more cinematic?" | Unclear: contrast, camera movement, music, aspect ratio, pacing | "Which film or moment do you mean, and what about it?" | Depends on the functional answer (see [Reference Analysis](../FOUNDATIONS/Reference-Analysis.md)) | Agreed function addressed |
| "I don't get it" | Missing context; unclear central question; jargon | "At what point did you lose it?" | Add orientation; clarify promise; reorder | Fresh viewer explains the piece |
| "Can we add…" (new content) | Scope change | "What should it achieve, and what can it replace?" | Priority map trade-off | Approved change with price |

## 2. Categories of notes

Classify every note; each category has a different owner and handling.

| Category | Definition | Example | Handling |
|---|---|---|---|
| Technical defect | Something objectively broken | Flash frame; audio click; caption drift; clipping | Fix; no debate |
| Factual mistake | Something untrue or inaccurate | Wrong statistic; misattributed quote; wrong name spelling | Fix; verify against sources; inform subject-matter owner |
| Accessibility failure | Something that excludes viewers | Unreadable caption; information only by colour; missing sound label | Fix; required |
| Taste preference | A matter of style or feeling | "I'd prefer a warmer grade" | Weigh against brief and coherence; decide by approval owner |
| Scope change | New content, deliverable or objective | "Can we add a 9:16 version for another platform?" | Change process; priced |
| Legal/compliance | Rights, claims, regulation | "That claim isn't substantiated" | Fix; legal owns the decision |
| Ethical/representation | Misrepresentation or dignity issue | "This reaction makes her look foolish" | Investigate; fix; escalate if contested |

## 3. Resolving conflicting notes

Conflicts are normal: the brand lead wants energy; legal wants fewer claims; the founder wants their story longer; the media buyer wants a shorter opening.

**Method** `[Practice]`:
1. **Map each note to the objective it serves** (from the brief's layers: business, story, viewer experience, accessibility, delivery).
2. **Identify the approval owner** for that objective (from the brief's approvals field).
3. **Look for a repair that satisfies both causes** — conflicting *requests* often have compatible *causes*.
4. **If no compatible repair exists, the owner of the higher-priority objective decides**, informed by the trade-off stated plainly.
5. **Record the decision** in the review log.

**Hypothetical example:** the brand lead asks for "more energy" in the Arc spot; the founder asks for "more calm". Causes: the brand lead feels the montage drags (low information density); the founder feels the product moment is rushed. Compatible repair: tighten the montage by removing repetitive shots (more information density) and lengthen the hover before the reveal by half a second (more calm where it matters). Both approve.

## 4. When a requested change would damage communication or truth

Do not silently comply with a change that would misrepresent evidence, expose private information, impersonate a person without consent, remove a required accessibility feature, or make the piece fail its intent. Do not refuse without explanation either.

**Practice:**
1. **Name the conflict plainly:** "If we place this reaction after that statement, viewers will think she was reacting to it; she wasn't."
2. **Offer an honest alternative:** "We can show her listening neutrally, or keep the original order."
3. **Escalate to the responsible decision owner** (producer, legal, editorial lead) if the requester insists.
4. **Record** the exchange in the review log.

## 5. Review annotation format

Every note should be actionable without a meeting. Fields:

| Field | Content |
|---|---|
| Version / path | Exact version reviewed (e.g., `ARC_SPOT30_v05_23976.mp4`) |
| Time reference | Timecode or frame, with the version's timecode convention |
| Observed problem | What the reviewer experienced or saw |
| Desired outcome | What they want the viewer to experience |
| Category | Technical, factual, accessibility, taste, scope, legal, ethical |
| Priority | Must fix / should fix / consider |
| Proposed fix | The editor's (or reviewer's) proposed repair |
| Impact | Dependencies touched (music, captions, versions…) |
| Approval | Who approved the fix and when |
| Status | Open / in progress / done / declined (with reason) |

### Filled review log (hypothetical, Project B "Arc" 30 s, round 2, 23.976 fps)

| # | Version | TC | Observed problem | Desired outcome | Category | Priority | Proposed fix | Impact | Approval | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | v05 | 00:00:03:10 | "Feels slow at the start" | Viewer engaged from first seconds | Taste | Should | Remove two repetitive kitchen shots; start on the alarm | Music intro shortened by 1 bar; captions unaffected | Brand lead | Done |
| 2 | v05 | 00:00:17:02 | "The ring lights too fast to notice" | Ring clearly seen lighting | Taste/communication | Must | Extend hover by 12 frames; ring lights after the move settles | Music breakdown extended via pad stem; total duration kept by trimming end-card hold slightly | Brand lead, founder | Done |
| 3 | v05 | 00:00:19:00 | Claim text: "Tracks your hydration" | Legal: the bottle doesn't measure intake; the app estimates from user input and lid events | Legal | Must | Change to "Glows to show how much you've had today" (approved wording) | Text animation re-timed; vertical version updated | Legal | Done |
| 4 | v05 | 00:00:24:12 | Caption covers the ring in 9:16 | Ring visible | Accessibility/technical | Must | Move caption to the upper zone for this shot | Caption file position updated; check other shots | Producer | Done |
| 5 | v05 | 00:00:28:00 | "Make the logo bigger" | Brand recognition | Taste | Consider | Hold end card 8 frames longer; increase contrast; logo size within guideline maximum | Music tail extended | Brand lead | Done (size unchanged; hold and contrast changed) |
| 6 | v05 | whole | Audio click at 00:00:11:22 | — | Technical | Must | Crossfade fix | — | — | Done |

## 6. Review logistics

- **Watermarked, password-protected review links** with expiry for confidential projects.
- **Burned-in timecode and version name** on review exports, so notes reference exact frames.
- **Review on representative devices:** clients reviewing a phone-first piece on a laptop will judge text size and pacing differently. Ask reviewers to watch on the intended device at least once.
- **One consolidated set of notes per round** from each organisation; conflicting notes resolved by the client's designated owner before they reach the editor, where possible.
- **Limit rounds** per the brief; extra rounds follow the change process.
- **The subject may be a reviewer, where it was agreed.** A round with the person in the film is not a courtesy; it is the check that the piece still represents what they meant (see [Care of the subject who sees the cut](#care-of-the-subject-who-sees-the-cut)).

### Care of the subject who sees the cut

When the agreement provides for it, the person in the film sees their own sections before lock. This round is unlike any other: the reviewer is not judging the piece as a viewer but recognising, or failing to recognise, themselves. The situations below are not taste notes.

| Situation | What to do | Why |
|---|---|---|
| The subject disagrees with how a line reads | Compare the cut against the full answer; if the meaning changed, repair it; if it did not, explain the context they may not have seen | The objection may be an editing fault, or a missing frame of reference |
| The subject asks to be removed from a section | Treat it as a consent question, not a taste note; involve the producer and check what the release and the agreement allow | Withdrawal is the subject's to ask for; the decision is documented, not assumed |
| The subject is distressed by difficult material | Stop the review, do not press for a reaction, and let them choose when to continue | A reaction recorded for the film is not the same as a reaction caused by it |
| The context of the piece has changed since filming | Re-confirm consent against the new use (new platform, new language, new framing) | Consent given for one use does not automatically cover another |
| The subject wants a change that would damage truth | Name the conflict and offer an alternative, as in [Section 4](#4-when-a-requested-change-would-damage-communication-or-truth) | Dignity and truth are protected, not traded |

**Care continues after the form is signed** `[Practice]`: consent formalities (owned by [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md)) establish the right to use the material; they do not settle what it feels like to see yourself in it. A person filmed in a difficult moment is owed a plain account of where the piece will appear, the chance to see it first where that was agreed, and a route to raise a concern after delivery — not because the law demands it, but because the next film depends on this one being handled well.

## 7. Worked example 1 — Multi-stakeholder brand review (hypothetical, Project B)

See the filled review log above. Key techniques demonstrated:
- Note 1: "slow" translated to repetition, not faster cutting.
- Note 2: a communication failure (ring not noticed) resolved by timing, preserving duration by trading the end-card hold.
- Note 3: a legal note overriding copy; wording owned by legal.
- Note 5: "make the logo bigger" translated to recognition; solved with hold and contrast within guidelines; the brand lead agreed after seeing it.

**Verification:** a muted phone viewing of v06 by two fresh viewers who can state the benefit and the brand.

## 8. Worked example 2 — Advisor and client review of an explainer (hypothetical, Project C)

| Note | Source | Category | Handling |
|---|---|---|---|
| "The 99% claim is not supported" | Public-health advisor | Factual | Removed; chart revised (see [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md#5-worked-example-2--a-chart-with-a-revised-claim-hypothetical-project-c)); change-impact map executed |
| "Make it tighter" | Client | Taste | Diagnosed as the slow history section; history trimmed; comprehension pauses kept (see [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md#11-counterexample-and-repair--trimming-every-pause)) |
| "Hindi captions are too fast in step 3" | Hindi reviewer | Accessibility | Captions re-chunked; shot extended by 1 s from handles |
| "Can we add a section on boiling?" | Client | Scope change | Priced: 20 s of new content; agreed to add a 6-second safety line instead, approved by advisor |

## 9. Counterexample and repair — notes executed literally

**Hypothetical counterexample.** A corporate film receives notes: "too slow", "make the logo bigger", "more energy", "music is boring". The editor executes literally: cuts are shortened everywhere, the logo doubled in size and placed on every section card, transitions added, a high-energy track swapped in. The next round: "It's exhausting", "it looks cheap", "the CEO's message got lost".

**Diagnosis:** symptoms treated as prescriptions; no causes identified; the brief's intent (the CEO's message on a new safety policy) lost.

**Repair:**
1. Return to the brief's intent; restore the previous version as a baseline.
2. For each note, ask clarifying questions; identify that "slow" referred to a 40-second introduction of the company history, and "boring music" to a cue that sounded like hold music.
3. Trim the history; choose music by function; keep the logo at guideline size with a clear end card.
4. Show the new version with a short explanation of what was changed and why.

**Verification:** stakeholders confirm the message is clear; a fresh viewer states the safety policy.

## 10. Micro-decisions

- Restate each note in your own words back to the reviewer before acting ("So the issue is that the ring lights before you've noticed it?").
- Keep declined notes in the log with reasons; they often return.
- Separate "must" from "should" from "consider" in every round.
- Never fix taste notes before technical, factual and accessibility notes in the same round — the latter are non-negotiable.
- When a note implies a large change, show a quick test (an alternate version of one section) before rebuilding everything.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Endless rounds | No intent anchor; no round limits | Brief intent at the top of every review; change process |
| Contradictory changes | Notes from many people unconsolidated | Designated owner; conflict resolution |
| Version confusion | Notes against old versions | Version names and burned-in timecode |
| Damage from literal execution | Notes treated as prescriptions | Diagnose causes; propose alternatives |
| Ethical problems introduced in review | Pressure to dramatise or misrepresent | Name conflict; alternative; escalate |

## 12. Verification

- Every note has a category, status and approval.
- Fixes verified against the acceptance criterion agreed with the reviewer.
- Dependent changes executed per the change-impact map.
- The final version still meets the brief's intent (fresh-viewer check).

## Dependencies

- Depends on: [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md).
- Interacts with: all craft chapters (note causes), [Production and Handoffs](Production-and-Handoffs.md), [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md), [Interview Craft](../STORY/Interview-Craft.md#16-verification-before-picture-lock) (speaker review), [Paper Edit and Assembly](Paper-Edit-and-Assembly.md) (compression checked before review).
- Diagnostics: [Failure Modes and Repair](../DIAGNOSTICS/Failure-Modes-and-Repair.md).

## Confidence summary

Notes-as-symptoms, categorisation, conflict resolution by objective and owner, and annotation formats are `[Practice]`. The specific note translations are `[Heuristic]`: common causes, not exhaustive. Examples are `[Illustrative]`.
