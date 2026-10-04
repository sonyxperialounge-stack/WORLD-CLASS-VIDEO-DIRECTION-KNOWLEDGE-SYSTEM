# Production Operations and Handoffs

**Purpose:** Teach practical scope, scheduling, dependencies and signoff; what picture lock does and does not mean; how to prepare handoffs between editor, motion designer, colorist, sound team and finisher; how interchange works and fails; and how to archive a project so it can be restored.

**Applies to:** Any project with more than one person or more than one application in post — which is most projects.

**Prerequisites:** [Ingest and Preparation](Ingest-and-Preparation.md), [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md).

**Owns:** Handoff and interchange practice, lock definitions and archive. Review notes and change requests are in [Review and Revisions](Review-and-Revisions.md); final QC and export in [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

---

## 1. Scope, schedule and dependencies

A post-production schedule is a chain of dependencies. Most delays come from a dependency nobody wrote down.

| Dependency | Example | Consequence if missed |
|---|---|---|
| Approvals before work | Legal approval of claims before graphics are built | Rebuilding graphics |
| Picture lock before finishing | Colour and sound start on a locked cut | Re-conform, re-mix, re-grade |
| Content before VFX | Approved UI design before screen replacement | Re-render |
| Music licence before mix | Licence confirmed before the final music edit | Replacing music late, re-editing picture |
| Translation before localised graphics | Approved translated text before building language versions | Re-building every version |
| Captions after final picture and audio | Captions timed to the final versions | Drift and errors |
| Delivery specs before export | Current platform specs confirmed | Rejected deliveries |

### A schedule skeleton (hypothetical, Project B "Arc")

| Phase | Duration | Outputs | Gate |
|---|---|---|---|
| Pre-production | 2 weeks | Brief, priority map, shot list, version matrix draft | Brief approved |
| Shoot | 2 days | Media, sound, references, clean plates | Ingest verified |
| Offline edit | 8 days | Rough cut → fine cut (30 s, 90 s) | Round 1 & 2 notes resolved |
| Picture lock | — | Locked cuts, turnover packages | Signed lock (Section 2) |
| Parallel finishing | 6 days | Motion graphics, VFX (UI), grade, sound design, mix | Each department's internal review |
| Online/conform | 1 day | Conformed master | Conform check |
| Versions | 3 days | 15 s vertical, 6 s bumper, captions | Version QC |
| QC & delivery | 2 days | Deliverables | Signed QC sheet |

## 2. Picture lock is a process, not a guarantee

**Picture lock** means the edit's timing is agreed so that departments can work in parallel on fixed durations. It is not a guarantee that nothing will change: legal notes, factual corrections, platform changes and late client decisions happen.

What lock should mean in practice `[Practice]`:
- A signed agreement (named approvers, date, version).
- A change-control process after lock: any change goes through the [brief-change process](../FOUNDATIONS/Constraints-and-Priorities.md#5-the-brief-change-process) and is priced in time and risk.
- Departments know that post-lock changes are possible and keep their work adaptable (handles, stems, layered graphics).

## 3. Handoffs: what each department needs

### 3.1 Turnover packages

| Recipient | Needs | Common omissions |
|---|---|---|
| Motion designer | Locked reference export with burned-in timecode; durations and in/out points for each graphic; approved text; design system and fonts; safe-area and version requirements | Approved text; version variants; caption zones |
| Colorist | Conform-ready timeline (interchange) linked to masters; reference export; list of retimes, reframes and effects; camera and colour assumptions; VFX shot list | Colour pipeline notes; reframes for other aspect ratios |
| Sound (dialogue editor, sound designer, mixer) | Audio interchange (e.g., AAF/OMF-style) with handles; reference picture with timecode; production sound reports; music files and licences; notes on temp vs final elements; delivery spec | Handles; split production tracks; music stems; frame rate |
| VFX | Plates (image sequences or high-quality files) with handles; reference; lens/camera data; clean plates; colour space and pipeline agreement; render handoff assumptions (see [Compositing and Integration](../VFX/Compositing-and-Integration.md#7-compositing-checklist-and-render-handoff-assumptions)) | Handles; colour space; versioning rules |
| Finisher / online | All of the above plus final graphics, VFX renders, mix, captions; delivery specs | Fonts; plug-in dependencies; correct versions |
| Caption/translation | Final picture and audio; scripts; glossary; style guide | Final versions; names list |

### 3.2 Handles

**Handles** are extra frames before and after each used clip, included in turnovers so other departments can extend fades, transitions, sound tails or VFX. Typical requests are in the range of about half a second to a couple of seconds per side `[Illustrative]`; agree the number per project. A sound turnover without handles prevents the mixer from extending ambiences or crossfading cleanly.

## 4. Project organisation and versions

- **Working versus approved:** keep a clear distinction between working sequences (constantly changing) and approved versions (frozen, named, dated). Never edit an approved version; duplicate it.
- **Naming:** `PROJECT_DELIVERABLE_vNN_status`, e.g., `ARC_SPOT30_v07_LOCKED`. Include frame rate in review exports if multiple rates exist.
- **Relinking and proxies:** see [Ingest and Preparation](Ingest-and-Preparation.md#7-proxies).
- **Dependencies:** fonts (with licences), plug-ins, LUTs, generated assets, music files and graphics templates must be collected with the project. A project that opens with "missing font" or "missing plug-in" on another machine is not handed off.

## 5. Interchange: concepts and failure risks

Interchange formats carry an edit's structure between applications.

| Interchange type | Typically carries | Typical limits |
|---|---|---|
| EDL (edit decision list) | Simple list of events: source reel/clip name, source timecode, record timecode; basic transitions | One video track (per list); limited effects; reel-name dependence; character limits |
| XML-based timeline formats (application-specific dialects) | Multitrack edits, clip references, some effects and metadata | Effects interpreted differently or dropped; dialect differences between applications |
| AAF (Advanced Authoring Format) | Multitrack picture and audio edits, audio levels and fades (often), embedded or linked media | Effects and some automation may not survive; plug-in processing not transferred |
| OpenTimelineIO-style editorial interchange | Timeline structure in an open format, with adapters | Adapter coverage varies; effects largely not interpreted |
| Rendered references | Exact picture as approved | Not editable — the reference against which interchange is checked |

**No interchange format preserves every effect.** Expect speed changes, reframes, nested sequences, multicam clips, titles, transitions and plug-in effects to need checking or rebuilding. The rendered reference export is the truth; the interchange is a convenience.

### Interchange preparation checklist

| Step | Why |
|---|---|
| Duplicate the locked sequence and simplify it (flatten nests, collapse multicams, remove unused tracks) | Fewer interpretation errors |
| Make reel/clip names unique and consistent | Relinking in the receiving application |
| Mark or list all retimes, reframes and effects | So the receiver can rebuild |
| Export a reference video with burned-in timecode and clip names | For the conform check |
| Confirm frame rate and timecode convention in the export | Avoid drift |
| Include handles | Flexibility downstream |
| Test a short section first | Discover problems early |

## 6. Archive and restore

At delivery, archive:
- Original media (camera, sound, archive, licensed music).
- Project files from every application (edit, graphics, colour, audio) with collected dependencies (fonts, LUTs, plug-in lists with versions).
- Masters (mezzanine/master files) and deliverables.
- Documents: brief, releases, licences, version matrix, QC sheets, AI-use log, change logs.

**Restore check** `[Practice]`: after archiving, restore a sample (e.g., open the edit project from the archive on another machine, relink, and play a section). An archive that has never been restored is an assumption, not an archive.

## 7. Worked example 1 — Small-team quick turnaround (hypothetical, Project A)

**Situation:** one editor handles edit, grade and mix; a caption editor and a translator work remotely; two-week schedule.

**Operations decisions:**
- No interchange for picture (single application); captions handed off as text files against reference exports with burned-in timecode (25 fps).
- Locking: the director and nonprofit sign off a **story lock** on day 8 (structure fixed), then a **picture lock** on day 10. Between them, only trims.
- Archive: originals already on two verified drives plus approved cloud storage; final project and documents added at delivery; restore check by opening the project on the nonprofit's archive machine.
- Risk control: the editor exports a daily reference to a shared review link (password-protected), so remote collaborators always see the current version.

**What made it work:** fewer handoffs means fewer interchange failures; the schedule spent saved time on dialogue clarity and caption accuracy (see [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md#23-fast-delivery-versus-complex-finishing)).

## 8. Worked example 2 — Multi-specialist brand job with a late cut change (hypothetical, Project B, 23.976 fps)

**Situation:** after picture lock, grade and mix of the 30-second spot are complete. Legal then requires removal of a 2-second shot that shows the bottle next to a competitor-like product on a café table (an unplanned brand-safety issue). The spot must stay 30 seconds.

**Change-impact map:**

| Department | Impact | Action | Verification |
|---|---|---|---|
| Edit | 2 s gap at 0:09–0:11 | Replace with an alternate morning-montage shot from selects (same rhythm role) | Full-speed playback; rhythm unchanged |
| Music | The montage music is unaffected in duration, but a cut that landed on a downbeat now lands on a different image | Check that the replacement shot's action suits the accent | Music + picture playback |
| Sound design | Foley and effects for the removed shot must be replaced | Sound designer adds Foley for the new shot (keys on a table) | Sound-only pass; sync check |
| Mix | New effects to balance; loudness re-check | Mixer updates the section; re-measures integrated loudness and true peak | Meter readings recorded |
| Grade | New shot ungraded | Colorist grades it to match neighbours | Shot-to-shot comparison |
| VFX | None | — | — |
| Graphics/captions | Captions unaffected (no speech there); on-screen claim unaffected | Confirm | Visual check |
| Versions | The 15 s vertical uses the same section | Update the vertical; check reframe of the new shot | Version QC |
| Interchange | Colour and sound receive an updated EDL/AAF for the change, with handles | Change list with timecodes | Conform check |
| Approval | Brand lead and legal | Re-review of updated spot | Signed |

**Lesson:** a 2-second change touched seven departments. The [brief-change process](../FOUNDATIONS/Constraints-and-Priorities.md#5-the-brief-change-process) and a change list prevent "we forgot the vertical".

## 9. Counterexample and repair — the turnover without handles

**Hypothetical counterexample.** An editor exports an AAF for the sound team with no handles, at the wrong frame rate setting (29.97 instead of 23.976) because the export preset was reused from another project. The mixer cannot extend room tone under cuts, the music edits sit slightly off, and the conform drifts.

**Diagnosis:** turnover settings unchecked; no test export.

**Repair:**
1. Re-export with correct frame rate and agreed handles.
2. Provide a reference video with burned-in timecode and confirm the start timecode.
3. The mixer checks sync at several points against the reference.
4. Add turnover settings to a checklist used for every handoff.

**Verification:** sync check at start, middle and end; room tone extensions possible.

## 10. Micro-decisions

- Put the frame rate, timecode start and version in every turnover's file name or accompanying note.
- Send a reference export with burned-in timecode and clip names alongside every interchange.
- Keep a single "source of truth" document for versions (the version matrix; see [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md)).
- Ask each receiving department to confirm receipt and a successful test before the deadline day.
- Collect fonts and plug-in lists before handoff, not after a failure.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Conform doesn't match the offline | Interchange interpretation; reel names; retimes | Compare to reference; rebuild effects; fix names |
| Sound can't extend tails | No handles | Re-export with handles |
| Late change breaks a version | No change-impact map | Map dependencies; version matrix update |
| Project won't open elsewhere | Missing dependencies | Collect fonts, plug-ins, LUTs |
| Archive unusable | Never tested | Restore check |
| Stale export delivered | Unclear version naming | Naming, APPROVED/SUPERSEDED folders |

## 12. Verification

- Turnovers tested with a short section before full delivery.
- Conform checked against the reference export.
- Every department confirms receipt and test.
- Archive restore tested.
- Lock and change approvals recorded.

## Dependencies

- Depends on: [Ingest and Preparation](Ingest-and-Preparation.md), [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md).
- Feeds: [Review and Revisions](Review-and-Revisions.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md), [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md).
- Department specifics: [Color Management](../COLOR/Color-Management.md), [Mix Strategy](../AUDIO/Mix-Strategy.md), [Compositing and Integration](../VFX/Compositing-and-Integration.md), [Design System](../MOTION-DESIGN/Design-System.md).

## Confidence summary

Lock and change control, turnover contents, handles and archive restore checks are `[Practice]`. Interchange format capabilities are described generally; application support varies by version and must be tested — `[Practice]`. Schedule durations and handle lengths are `[Illustrative]`.
