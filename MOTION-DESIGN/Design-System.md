# Motion Design: Purpose, Hierarchy and the Design System

**Purpose:** Teach how to begin any graphic — title card, lower third, transition, chart, logo animation — from communication purpose and hierarchy rather than from a favourite effect; how to design static frames before motion; how to test timing cheaply; and how to build a design system that versions and series can inherit.

**Applies to:** All on-screen graphics in any genre.

**Prerequisites:** [Creative Brief](../FOUNDATIONS/Creative-Brief.md).

**Companion chapters:** [Animation Grammar](Animation-Grammar.md) (timing, spacing, easing, curves); [Integration and Data Graphics](Integration-and-Data-Graphics.md) (live-action integration and honest data visualisation). Type roles and text specifications are owned by [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md); caption timing by [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md).

---

## 1. Start from the job, not the effect

Every graphic exists to do one or more jobs:

| Job | Typical graphic | The question it must answer |
|---|---|---|
| Identify | Lower third, name card, location title | Who or where is this — quickly, without stealing attention? |
| Orient | Chapter card, map, timeline marker | Where are we in the piece or the world? |
| Explain | Diagram, process animation, label | How does this work? |
| Prove | Chart, data callout, comparison | What is the evidence? |
| Emphasise | Kinetic text, highlight | What matters most here? |
| Brand | Logo animation, end card, colour system | Who made this, and what do they stand for? |
| Transition | Graphic wipe, section card | A new section starts |
| Act | Call to action | What should I do now? |

A graphic designed for "make the lower third look cool" tends to fail its identify job; it pulls attention from the speaker's first words. A graphic designed for "identify Asha without competing with her face during her first sentence" leads to concrete decisions: position, size, timing, motion restraint.

## 2. Three ways in: shape-first, timing-first, footage-first

| Approach | Method | Helps when | Fails when |
|---|---|---|---|
| Shape-first | Design the static composition and system (grid, type, colour) before animating | Brand systems, information graphics, anything that must be readable and consistent | The piece's character is in motion (music-driven typography); static design may not anticipate motion needs |
| Timing-first | Start from the audio or edit rhythm; block in when elements appear and how long they hold | Music-driven graphics, title sequences, kinetic typography, anything synchronised | Readability and hierarchy get neglected; design becomes busy |
| Footage-first | Design from the live-action image — its composition, colour, light, movement | Graphics that live inside shots (labels on objects, integrated titles) | Graphics that must be consistent across very different footage |

Experienced designers often combine them: **shape-first for the system, timing-first for the sequence, footage-first for integration.** The mistake is starting with an effect (a glow, a glitch, a 3D extrusion) and searching for a job for it.

## 3. Layout fundamentals

| Principle | What it controls | Practical guidance |
|---|---|---|
| Negative space | Breathing room; emphasis by isolation | Leave space around important elements; crowding makes everything less important |
| Grouping (proximity) | Which items belong together | Name and title together; a gap separates the next group |
| Grid | Consistency and alignment across frames | Define margins and columns; snap elements to them; consistent left edges read as order |
| Scale | Importance | The most important item is usually largest; limit to two or three scale levels |
| Weight | Emphasis within type and shapes | Bold for primary, regular for secondary; avoid many weights |
| Texture | Character; relationship to footage | Subtle grain or paper texture can integrate graphics with filmic footage; can reduce legibility |
| Contrast | Legibility and hierarchy | Text must contrast with its background across all frames it covers (see [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md)) |
| Brand constraints | Colour, type, logo rules, motion rules | Know the brand's rules and their intent; push only with approval |
| Animation hierarchy | What moves first, what moves most, what stays still | Primary element moves first or most; secondary follows; background stays stable |

### What must move, what should stay, where the eye lands

For each graphic, answer three questions before animating:

1. **Where should the eye land first?** On a lower third: the name. On a chart: the key value. On an end card: the product name or the call to action.
2. **What must move?** Only what carries information in its motion — a value growing, a part assembling, an arrow showing flow. Entry and exit animations are a separate, smaller decision.
3. **What should stay stable?** Anchors: frames, labels, axes, the logo once revealed. Stable elements let the eye rest and give moving elements meaning.

A common failure is **everything moving**: every element enters with its own animation, nothing is still, and the eye has no place to land.

## 4. Static frames before motion

Design key frames as still images first ("style frames"), at final resolution, over representative footage. Static frames expose composition problems that motion hides: a weak hierarchy can look exciting in motion because the eye is busy following movement; when it stops, the viewer cannot find the information.

**Practice** `[Practice]`: every graphic's final resting state (the frame after all animation settles) should work as a well-composed still. If the resting state is weak, animation is decoration covering a problem.

### Animatic and previz before the full build

When a sequence depends on rhythm or many moving parts (a title sequence, a process animation, a data story), test it as a **timed animatic**: rough shapes or sketches timed to the audio or the edit, played at full speed. It costs hours instead of days and answers:

- Is there time to read each piece of text?
- Does the order of information make sense?
- Is the pacing right against the voice-over or music?
- Where does the eye go at each moment?

Changing timing in an animatic is cheap. Changing timing after artwork, type, effects and renders exist is expensive and tends to be resisted, so problems survive into delivery.

## 5. Element-by-element guidance

### 5.1 Title cards

- **Job:** orient or announce; sometimes set tone.
- **Decisions:** duration long enough to read twice at normal speed (readability is tested, not computed; see [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) for reading-time reasoning); over footage or over a solid; motion level appropriate to genre.
- **Failure:** cards that appear and disappear before they can be read; cards that are more elaborate than the content they introduce.

### 5.2 Lower thirds

- **Job:** identify a person (and sometimes role) without stealing attention from their speech.
- **Decisions:** position relative to face and safe areas; size relative to the platform's smallest viewing size; entry timing (often after the speaker's first phrase, so the viewer meets the person before reading about them); duration; exit.
- **Failure:** entering on the speaker's first word (competes with listening); covering the speaker's mouth or a caption area; generic templates that do not match the piece's character.

### 5.3 Graphic transitions

- **Job:** mark a section change.
- **Decisions:** whether a straight cut with a title is enough; consistency across the piece.
- **Failure:** decorative transitions that draw attention to themselves and imply meaning the content does not carry — see the "transition pack" counterexample in [Shot Relationships](../EDITING/Shot-Relationships.md#8-counterexample-and-repair--the-transition-pack).

### 5.4 Charts and diagrams

Owned in depth by [Integration and Data Graphics](Integration-and-Data-Graphics.md). In brief: faithful values, clear scales and units, honest animation.

### 5.5 Logo animation

- **Job:** brand identification and closure.
- **Decisions:** follow brand guidelines (clear space, colour, minimum size, permitted animation); the animation should express the brand's character (precise, playful, warm) through timing and spacing, not through generic effects; a sound logo, if any, coordinated with the mix.
- **Failure:** a logo animation more energetic than the film it closes; a reveal so long that the viewer has left; brand-colour shifts caused by uncontrolled colour management (see [Color Management](../COLOR/Color-Management.md)).

## 6. Building a design system

A design system is a written specification of reusable decisions so that every graphic — and every later version and episode — is consistent without being reinvented.

| Component | Contents | Owner/link |
|---|---|---|
| Grid and safe areas | Margins, columns, title-safe/action-safe zones per aspect ratio; platform interface overlay zones | [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md) |
| Colour tokens | Named colours with values in the working colour space and their intended roles (text, background, accent, data series) | [Color Management](../COLOR/Color-Management.md) for value consistency |
| Type roles | Title, name, role, label, data value, caption-style text, call to action | [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md) |
| Components | Lower third, chapter card, label, callout, end card, chart styles | This chapter |
| Motion tokens | Standard durations, easing families, stagger offsets, entry/exit behaviour | [Animation Grammar](Animation-Grammar.md) |
| Sound pairing | Whether graphics have sound; which sounds | [Sound Design](../AUDIO/Sound-Design.md) |
| Accessibility rules | Minimum contrast approach, minimum sizes, reduced-motion alternatives, no information by colour alone | [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| Variant rules | How components adapt to 9:16, 1:1, other languages | [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md) |

### Series and recurring formats

For series, the design system is a **delivery constraint**: later episodes inherit recurring graphics, typography, colour, motion and caption styling rather than reinventing them. Store project templates, fonts (with licences) and the written spec together; record version changes.

## 7. Worked example 1 — A restrained interview lower third (hypothetical, Project A "Second Shift", 25 fps, 1920×1080)

**Job:** identify Asha (name and role) in Hindi and English versions without competing with her face or the captions, and without signalling "corporate".

**Design decisions:**

| Decision | Choice | Rationale |
|---|---|---|
| Position | Left side, aligned to the grid's left margin, vertically positioned above the caption zone | Asha is framed on the left third; the lower third sits below her shoulder line, not across her face; captions occupy the bottom zone and must not collide |
| Content | Line 1: "Asha" (name). Line 2: "Night-shift nurse, District Hospital" (role) | Short; no surname by agreement (privacy); role gives context |
| Scale | Name about 1.5× role size `[Illustrative]` | Clear hierarchy with two levels only |
| Background | No box; a soft, low-opacity gradient behind text only where needed for contrast | A box would feel institutional; the window-lit background is variable, so a subtle local gradient protects contrast |
| Colour | Off-white text | Pure white looks harsh against warm skin tones in this grade |
| Language versions | Hindi version uses Devanagari for both lines; English version uses Latin; both inherit size roles, adjusting for script (see [Localization](../TEXT-ACCESSIBILITY/Localization.md)) | Consistent hierarchy across scripts |
| Entry timing | After her first phrase — about 1.5 s after she begins speaking `[Illustrative]` | Viewers meet her voice and face first |
| Motion | A simple fade with a small upward drift (a few pixels) over about 12 frames (480 ms); text fades, the gradient fades slightly earlier | Restraint suits observational documentary; the drift gives a sense of arrival without spectacle |
| Duration | About 4 s on screen `[Illustrative]`, tested by reading aloud twice | Two short lines |
| Exit | Fade over about 10 frames, no drift | Exits should be quieter than entries |

**Static frame check:** the resting frame (text fully in) is reviewed as a still over the brightest part of the interview (when the window brightens) and the darkest — legible on both.

**Verification:** watch on a phone at arm's length and on the projector at a community screening space (or a large display as proxy); ask a fresh viewer who the speaker is after the lower third exits; check no collision with captions at any point (captions are placed with knowledge of the lower-third zone; see [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md)).

**Boundary condition:** if the subject were a public official in an accountability piece, a more formal, boxed lower third with full name and title might be appropriate — the contract demands authority and precise identification.

## 8. Worked example 2 — Product claim and end card (hypothetical, Project B "Arc", 23.976 fps, 16:9 and 9:16)

**Jobs:** (1) carry the claim for muted viewers: "Glows to show how much you've had today"; (2) end card: product name, one benefit line, call to action.

**Shape-first system decisions:**
- One typeface family across all Arc materials (brand rule), two weights.
- Claim text left-aligned to a margin; never over the product.
- End card: product name largest, benefit line medium, call to action smallest but highest contrast.

**Timing-first decisions:**
- The claim appears *after* the ring lights (about 12 frames ≈ 500 ms later), so the viewer sees the evidence before reading the claim — "show, then tell".
- The claim holds through the drink beat; tested for reading time on a phone.
- End card: product name settles first; benefit line 8 frames later; call to action 8 frames after that — a staggered hierarchy that matches reading order.

**Footage-first decisions:**
- Text colour sampled from the warm-neutral studio background but darkened for contrast; avoids the brand's bright accent colour except on the call to action, where it signals interactivity.

**9:16 variant:** stacked layout; claim positioned in the upper-middle zone because the bottom of a vertical feed is often covered by interface elements (verify per platform; see [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md)).

**Verification:** muted phone test: can a viewer state the benefit? Brand and legal review the claim wording. The resting end card is checked as a still in both aspect ratios.

## 9. Counterexample and repair — motion hiding a weak composition; a no-motion alternative

**Hypothetical counterexample.** For a corporate results video, a title card shows "Q3 Highlights" with six bullet points, each flying in from a different direction with a 3D rotation, a glow and a particle trail. In motion it looks busy and expensive. In review, the CFO asks, "What were the six highlights?" Nobody in the room can say.

**Diagnosis.**
- Static resting frame: six bullets of equal size and weight, centred, with no hierarchy — weak composition.
- Motion: every element moves differently, so the eye follows motion rather than reading.
- Timing: the last bullet settles 0.5 s before the card cuts away; there is no time to read the settled state.

**Repair options:**

| Option | Result |
|---|---|
| A. Simplify motion: bullets fade in sequentially, 0.5 s apart | Better reading order; still six equal items |
| B. Redesign hierarchy: one headline number large ("Revenue up 12%"), two supporting items smaller; remaining three moved to a later card | Clear focus |
| C. **No motion at all:** a static card with the redesigned hierarchy, held long enough to read, while the CFO's voice-over states the headline | Most legible; the voice carries pace; the stillness signals seriousness |

**Choice:** **C** for the results section, with a single, subtle fade-up. In a financial context, stillness reads as confidence and accuracy; motion would add nothing to the information. **Boundary:** in a launch video for the same company's consumer product, motion could carry energy legitimately.

**Verification:** show the static version to people who did not see the first; ask for the headline. Success: they repeat it accurately.

## 10. Micro-decisions

- Align text to the same left edge across successive graphics; a few pixels' drift reads as sloppiness.
- Make entry and exit of related elements share a direction logic (enter from left, exit to left or fade) — mixed directions feel random.
- Use one accent colour for "action" items consistently across the piece.
- Avoid placing graphics where a cut will happen mid-animation, unless the graphic intentionally bridges the cut.
- Design graphics at the delivery resolution, and test at the smallest viewing size in the brief.
- Keep the resting frame on screen at least as long as the animation into it, as a starting point for reading time — then test.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "I couldn't read it" | Insufficient hold; too much text; motion during reading | Shorten text; extend hold; stop motion while text is read |
| "It looks generic" | Template used without adapting to the piece's character | Derive from the brief's emotional stance and footage |
| "It's distracting" | Graphic competes with speech or a face | Reposition; delay entry; reduce motion |
| "It looks cheap" | Inconsistent alignment, too many styles, effects without purpose | Apply a grid and system; remove effects |
| "Everything is moving" | No animation hierarchy | Define primary, secondary, static |
| "The vertical version is cramped" | Components not designed for variants | Variant rules in the design system |

## 12. Verification

- Review every resting frame as a still at final size.
- Watch the animatic, then the final, at full speed with the final audio.
- Test on the smallest target device, muted and unmuted.
- Check against caption placement and platform overlays in every version.
- Confirm brand compliance and font licensing.

## Dependencies

- Depends on: [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md).
- Companion: [Animation Grammar](Animation-Grammar.md), [Integration and Data Graphics](Integration-and-Data-Graphics.md).
- Feeds: [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md), [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md).

## Confidence summary

Purpose-first design, static-frame review and animatic testing are `[Practice]`. The three approaches (shape-, timing-, footage-first) are a teaching framework based on common studio workflows. Specific sizes, durations and offsets are `[Illustrative]` and must be tested on the target device. Preference for stillness in financial and serious contexts is a `[Heuristic]` tied to genre and audience.
