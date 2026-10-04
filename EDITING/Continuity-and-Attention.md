# Continuity, Geography and Eye Trace

**Purpose:** Teach how viewers build a mental map of space and track attention across cuts — screen direction, the action axis, eyelines, prop and state continuity, eye trace — and how to decide which discontinuities to accept, how to mask jumps honestly, and how reframing changes meaning.

**Applies to:** Scenes with people in space (drama, documentary, interviews), action and product sequences, and any material later reframed for other aspect ratios.

**Prerequisites:** [Cut Decisions](Cut-Decisions.md), [Shot Relationships](Shot-Relationships.md).

**Related owners:** Performance-versus-continuity choices in [Performance Editing](Performance-Editing.md); framing at acquisition in [Composition and Optics](../CAMERA/Composition-and-Optics.md); aspect-ratio versioning in [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md).

---

## 1. Why viewers need a map

Viewers continuously build a model of where people and things are, which way they face and how they relate. When the model is stable, attention is free for story. When the model breaks unintentionally, attention goes to repairing it: *Wait — who is she looking at? Which side of the room is the door?* That repair work is what people mean when they say a cut "feels wrong" without knowing why.

Continuity is therefore not about pedantic matching. It is about **protecting the viewer's map** — or breaking it on purpose.

## 2. Screen direction and the action axis

### 2.1 The axis

Between two people in conversation, or along a line of movement, there is an imaginary line — the **action axis**. If all camera positions stay on one side of it, each person keeps a consistent screen side and looking direction: Nisha always looks screen-right toward Ravi; Ravi always looks screen-left toward Nisha. This is the 180-degree convention.

### 2.2 What happens when it is crossed

Crossing the axis without preparation flips screen positions: Nisha suddenly appears to look screen-left, as if looking away from Ravi or at someone else. Viewers may briefly lose track of the relationship.

### 2.3 The convention is a tool

The 180-degree convention protects geography. It can be broken when:

- **Disorientation is the point** — a character losing control, a panic, a dream.
- **The geography is already obvious** — two people at a small table where both are always visible in context.
- **The crossing is shown** — the camera moves across the axis on screen, or a character walks across it, so the viewer sees the new orientation form.
- **A neutral shot resets it** — a shot along the axis (subjects moving directly toward or away from the camera, or a frontal two-shot) gives the viewer no left/right information, after which either side can be used.
- **An establishing or re-establishing wide shot** shows the new arrangement.

### 2.4 Movement direction

For movement (people walking, cars driving), consistent screen direction tells the viewer that motion continues toward the same goal. Reversing it can mean return, retreat, or a meeting from opposite sides. A character who walks left-to-right to leave home and right-to-left to return reads as going and coming back — a useful, near-universal convention in film grammar `[Practice]`, though some viewers and cultures may read direction with different associations; context dominates.

## 3. Eyelines

| Aspect | What to check | Failure |
|---|---|---|
| Direction | Singles of two people talking should have opposing eyeline directions | Both look the same way: they seem to look at a third person |
| Height | A seated person looking at a standing person looks up; the standing person looks down | Height mismatch makes the relationship ambiguous |
| Distance from lens | Eyelines close to the lens feel intimate; far from the lens feel observational | Mixing distances between two singles makes one person feel closer to the viewer |
| Offscreen objects | A look at something offscreen must lead to a shot of it (or a reason not to show it) | A look that is never resolved creates an unintended question |

## 4. Prop, state and time continuity

| Continuity type | Examples | Viewer sensitivity |
|---|---|---|
| Prop position and hand | Photo frame in left/right hand; cup level | High when the prop is the focus; low when attention is on faces |
| State | Wet/dry, torn/untorn, lit/unlit cigarette, door open/closed | High when state is story-relevant |
| Wardrobe and hair | Sleeves rolled, scarf on/off | Moderate |
| Light and time of day | Window light changing over a long shoot; a sunset scene shot over two hours | Moderate to high in wide shots |
| Sound continuity | Background music, a fan, traffic | Often more noticeable than picture (see [Perspective and Silence](../AUDIO/Perspective-and-Silence.md)) |
| Performance level | Emotional intensity between angles | High — this is often the real cause of "continuity" notes |

## 5. The continuity matrix

A continuity matrix tracks the state of story-relevant elements across takes and setups, so the editor knows which combinations intercut safely.

### Filled continuity matrix — Project D "The Spare Key" (hypothetical)

| Element | Master T2 | Master T4 | Nisha single T3 | Nisha single T5 | Ravi single T4 | Ravi single T5 | Insert (key) |
|---|---|---|---|---|---|---|---|
| Photo frame | Nisha's right hand throughout | Right hand → table at "You always…" | Right hand throughout | On table from "You always…" | — (offscreen) | — | Not visible |
| Key | In Ravi's right trouser pocket until reveal | Same | — | — | Pocket; hand touches it 3× | Pocket; hand touches it 2× | On table, teeth facing Nisha |
| Box of books | Half-packed | Half-packed | Visible, half-packed | Visible, more full (prop reset missed) | — | — | — |
| Ravi's sleeves | Rolled | Rolled | — | — | Rolled | Unrolled (error) | — |
| Window light | Practical lamp + streetlight | Same | Same | Same | Same | Same | — |
| Refrigerator hum | Present | Absent (switched off) | Present | Absent | Present | Absent | Absent |

**Reading the matrix:**
- Nisha T5 and Master T4 match on the photo frame (on table after "You always…") — the master T4 can be used for wides in the second half.
- Ravi T5's unrolled sleeves will mismatch any wide that shows him; use Ravi T5 only in singles and OTS shots where his arms are out of frame, or accept the mismatch if the performance justifies it (decided in [Performance Editing](Performance-Editing.md#7-worked-example-1--two-person-scene-hypothetical-project-d-the-spare-key-23976-fps)).
- The refrigerator hum is present in some takes and absent in others: the dialogue editor must build a continuous hum bed for the scene, or remove it consistently — a sound continuity decision (see [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md)).

## 6. Eye trace

### 6.1 The idea

**Eye trace** is the path a viewer's gaze is likely to follow within a shot and across cuts. Smooth cuts often place the incoming shot's focal point near where the outgoing shot left the eye, so the viewer does not have to search.

### 6.2 What attracts the eye

Without eye-tracking measurements, the editor *infers* likely gaze from well-studied attractors `[Heuristic]`:

| Attractor | Notes |
|---|---|
| Faces, especially eyes | Very strong; viewers find faces almost immediately |
| Motion | Movement against a still background pulls attention |
| Brightness and contrast | The brightest or highest-contrast area tends to draw the eye |
| Sharp focus | Sharp areas draw more than blurred ones |
| Text | Readable text pulls the eye — sometimes away from faces |
| Colour saturation | Saturated areas stand out in muted frames |
| Gaze of people in frame | Viewers tend to look where characters look |
| Graphic anchors | Lines, shapes and leading lines guide toward a point |

**Important distinction:** an editor's statement "the viewer looks at X" is an inference about likely attention based on these attractors. Actual gaze varies between viewers and can only be measured with eye-tracking. This library labels such statements as inferred.

### 6.3 Smooth transfer versus useful surprise

| Smooth transfer | Useful surprise |
|---|---|
| Incoming focal point near the outgoing one | Incoming focal point far away, motivated |
| Viewer feels guided | Viewer must search — creates a jolt, alertness, disorientation |
| Good for dialogue, demonstrations, emotional continuity | Good for shocks, reveals, comedy, a sense of chaos |

A reveal often benefits from a short search: the viewer looks where the previous shot led, finds nothing, then discovers the important thing elsewhere. A demonstration does not: a search costs comprehension.

## 7. The attention map

An attention map records the inferred focal point at the end of each outgoing shot and the start of each incoming shot, so the editor can see where the eye has to travel.

### Filled attention map — Project D, key reveal (hypothetical; inferred focal points, frame divided into a 3×3 grid: L/C/R × top/middle/bottom)

| Cut | Outgoing shot (end) | Inferred focal point | Incoming shot (start) | Inferred focal point | Eye travel | Intent |
|---|---|---|---|---|---|---|
| 1 | Ravi single, says "Dad gave it to me" | Ravi's eyes, R-top | Nisha single | Nisha's eyes, L-top | Short (opposite thirds, same height — standard two-single exchange) | Smooth |
| 2 | Nisha single, eyes drop | Nisha's eyes moving down, L-middle | Insert: key on table | Key, C-middle | Short, follows her gaze | Smooth; eyeline motivated |
| 3 | Insert: key | Key, C-middle | Wide master T4 | Nisha's face, L-middle (lamp-lit, brightest face) | Medium | Contrast: re-establish geography after insert; the eye finds the lit face |
| 4 | Wide | Nisha, L-middle | Ravi single | Ravi's eyes, R-top | Medium, motivated by her look up toward him | Smooth |

**Check:** cut 3's incoming wide places the brightest element (the lamp) beside Nisha's face; if the lamp were brighter than her face, the eye would land on the lamp. The colorist is asked to keep the lamp below the face in perceived brightness in that shot (see [Creative Grading](../COLOR/Creative-Grading.md)).

## 8. Accepting discontinuities

Every edit contains discontinuities; most go unnoticed because attention is elsewhere. Decide which to accept by asking:

1. **Where is attention at that moment?** Discontinuities outside the focal area are rarely noticed.
2. **Is the element story-relevant?** A key in the wrong hand matters; a cushion slightly moved does not.
3. **What is the performance gain?** A stronger performance often outweighs a minor mismatch.
4. **Will it be noticed at full speed, by a fresh viewer, on the target device?** Test it.

## 9. Masking a jump without random B-roll

When a jump in time or continuity must be hidden, editors often reach for "B-roll" — any shot to cover the cut. Random B-roll has costs: it interrupts, it can imply false connections, and viewers increasingly recognise it as filler.

| Masking method | When it works | Risk |
|---|---|---|
| Motivated cutaway (what the speaker is talking about, or what a character looks at) | The cutaway adds information or emotion | Must be truthful in factual work (see [Performance Editing](Performance-Editing.md)) |
| Reaction shot | A listener is present and their reaction is legitimate | In documentary, only neutral listening shots are portable |
| Angle change (second camera) | Multicamera coverage exists | Mismatched performance between angles if not simultaneous |
| Punch-in (digital reframe of the same shot) | Resolution headroom exists (e.g., UHD source in an HD timeline) | Quality loss; the "zoom" can feel arbitrary; changes body language |
| Honest jump cut | The style accepts visible edits (interviews, presenters) | In drama, reads as error unless established |
| Sound bridge across a cut to another scene | The jump coincides with a scene transition | Must not imply false causality |
| Dissolve | Time passage is the point | Implies time passing; misleading if no time passed |

## 10. Crop and reframe: meaning changes with the frame

Reframing in post (for stabilisation, punch-ins, or new aspect ratios) is not neutral.

| Reframe change | Effect on meaning |
|---|---|
| Tighter crop on a face | Increases intimacy or intensity; removes body language (hands, posture) |
| Cropping out a second person | Removes the relationship; can make someone appear alone or isolated |
| Recentering a subject | Removes lead room; can make a person appear trapped or confronting |
| Vertical crop from 16:9 | Removes horizontal context — who is beside whom, where a look is directed, product next to hand |
| Removing headroom | Increases tension; can feel claustrophobic |

**For later vertical versions:** a shot in which Nisha looks screen-right at Ravi off-frame works in 16:9 because the empty space on the right "holds" her look. In a centred 9:16 crop, her look points at the frame edge with no space; she appears to look out of the picture. Repairs include an offset crop, a different take, or a different shot (see [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md)).

## 11. Worked example — Interview with missing coverage and later vertical extraction (hypothetical, Project A)

**Situation:** for the 60-second 9:16 social excerpt, the editor uses Asha's "I stopped noticing I was tired" passage. The 16:9 A-cam frame has Asha on the left third, looking toward the interviewer on the right. The B-cam is unavailable for this answer's second half.

**Problems:**
1. A jump cut is needed to remove a 6-second digression.
2. The vertical crop needs to include her face and some look space.

**Options and choice:**

| Problem | Option | Choice and rationale |
|---|---|---|
| Jump | (a) punch-in from the UHD source at the cut; (b) honest jump cut; (c) cutaway of her hands — not available for this answer; (d) ward B-roll | **(a) in 16:9** — a modest punch-in (about 115%) masks the jump without implying anything; **(b) in 9:16** — the vertical crop is already tight, and further punch-in would lose quality; the honest jump cut fits the social contract |
| Vertical framing | Centred crop vs offset crop | **Offset crop** placing her face left of centre with look space to the right; check headroom for platform interface overlays (see [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md)) |

**Verification:** watch both versions at full speed on a phone; ask a fresh viewer whether she seems to be speaking to someone or to the camera — "to someone" confirms the look space works. Compare the edited passage against the full answer (factual context).

## 12. Counterexample and repair — the accidental axis crossing

**Hypothetical counterexample (Project D).** The over-the-shoulder shots were filmed late, after the camera had moved around the room. In the edit, the Nisha OTS (over Ravi's shoulder) places Nisha on the right of frame looking left — the same side and direction as Ravi in his single. Cutting between them, Nisha and Ravi appear to look in the same direction, as if both are looking at a third person. Test viewers ask, "Is someone else in the room?"

**Options:**

| Option | Effect | Problems |
|---|---|---|
| Flip the OTS horizontally | Restores direction | Mirrored text on the bookshelf; Ravi's hair parting and the asymmetric room become visible as wrong; generally a last resort |
| Insert a neutral shot (a frontal wide from the doorway) before the OTS | Resets geography | Requires that the shot exists (it does — the master's opening) |
| Use the crossing on a motivated movement — cut to the OTS only after Ravi walks to the window (he crosses the axis on screen in the master) | The viewer sees the new arrangement form | Restricts where the OTS can be used |
| Drop the OTS shots | Clean geography | Loses useful coverage |

**Choice:** the motivated-movement option. The OTS shots are used only after Ravi's walk to the window, which happens before the escalation. Before that, the scene uses singles and the master.

**Verification:** fresh viewers no longer ask about a third person; asked to sketch the room, they place the siblings correctly.

## 13. Micro-decisions

- When a character exits frame, cut when the leading eye or shoulder reaches the edge, or hold to an empty frame if absence matters.
- On a match-on-action, match the *speed* of movement as well as the position.
- When re-establishing geography after a cluster of close-ups, a single wide of a few seconds is usually enough.
- Check eyeline height in singles at the start of the scene; later fixes require reframing that changes headroom.
- Record "continuity accepted" decisions in markers, so later reviewers do not "fix" a deliberate choice.

## 14. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "Who is she looking at?" | Eyeline direction or height mismatch | Use matching singles; re-establish; reframe |
| "Is someone else in the room?" | Axis crossing | Neutral shot; motivated crossing; drop shot |
| "The cup keeps changing" | Prop continuity in the focal area | Choose matching takes; cutaway at the change; VFX only if necessary |
| "Where did he come from?" | Missing entrance or direction reversal | Add an entrance; keep direction |
| "The vertical version feels wrong" | Crops removed look space, relationships or product context | Recompose; alternate takes; alternate edit |
| "That cutaway feels like filler" | Random B-roll used to mask a jump | Motivated cutaway, punch-in, or honest jump |

## 15. Verification

- **Comprehension without prior familiarity:** ask a fresh viewer to describe the room and who was where.
- **Emotional plausibility with sound:** accepted continuity breaks should still be unnoticed with final sound.
- **Factual context:** for documentary, check that cutaways and reaction placements match source transcripts and full answers.
- **Every version:** run the attention and geography checks again on each aspect-ratio version.

## Dependencies

- Depends on: [Cut Decisions](Cut-Decisions.md), [Shot Relationships](Shot-Relationships.md), [Composition and Optics](../CAMERA/Composition-and-Optics.md).
- Interacts with: [Performance Editing](Performance-Editing.md), [Dialogue and Voice](../AUDIO/Dialogue-and-Voice.md), [Creative Grading](../COLOR/Creative-Grading.md), [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md).

## Confidence summary

The action axis and its reset methods, eyeline matching and continuity matrices are `[Practice]`. Eye-trace attractors are `[Heuristic]` supported by general findings on visual attention; individual gaze varies and is inferred, not measured, unless eye-tracking is used. Screen-direction associations are `[Heuristic]` and context-dependent. Examples are `[Illustrative]`.
