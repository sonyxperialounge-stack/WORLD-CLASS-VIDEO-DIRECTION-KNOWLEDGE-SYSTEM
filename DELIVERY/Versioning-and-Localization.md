# Versioning and Localization Workflow

**Purpose:** Teach how to plan, build, name and verify multiple versions — durations, aspect ratios, languages, caption types, audio variants, graphics and end cards — from a single source of truth; how series inherit specifications; and how to run localization as a re-edit, not just a text swap.

**Applies to:** Any piece delivered in more than one version.

**Prerequisites:** [Platform and Format Strategy](Platform-and-Format-Strategy.md), [Localization](../TEXT-ACCESSIBILITY/Localization.md) (language and script behaviour).

**Owns:** The version matrix, version naming and the localization workflow. Linguistic practice is owned by [Localization](../TEXT-ACCESSIBILITY/Localization.md); export settings by [Quality Control and Export](Quality-Control-and-Export.md).

---

## 1. The version matrix

The version matrix is the single source of truth for what is being delivered. Every version has a row; every row has a parent master and a status.

| Column | Content |
|---|---|
| Version ID | Unique, used in file names |
| Duration | Target and actual |
| Aspect ratio | 16:9, 9:16, 1:1, … |
| Language | Audio and on-screen text languages |
| Caption type | Closed (sidecar/embedded), open (burned-in), none |
| Audio variant | Full mix, music-and-effects, dialogue-free, loudness profile |
| Graphics variation | Which graphic package/layout |
| End card | Which end card or CTA |
| Delivery profile | Reference to the export specification (see [Quality Control and Export](Quality-Control-and-Export.md)) |
| Approval status | Draft / in review / approved / delivered / superseded |
| Parent master | The approved master this version derives from |

### Filled version matrix — Project B "Arc" (hypothetical)

| ID | Duration | Ratio | Language | Captions | Audio | Graphics | End card | Profile | Status | Parent |
|---|---|---|---|---|---|---|---|---|---|---|
| ARC-BF90-169-EN | 1:30 | 16:9 | EN | Closed (sidecar) + open version for social | Full mix (stereo) | Brand film package | Brand film card | WEB-MASTER-169 | Approved | — (master) |
| ARC-SP30-169-EN | 0:30 | 16:9 | EN | Open + closed | Full mix | Spot package | Spot card + URL | PREROLL-169 | Approved | — (master) |
| ARC-SP15-916-EN | 0:15 | 9:16 | EN | Open (upper zone) | Full mix, muted-first design | Vertical package | Vertical card | SOCIAL-916 | In review | ARC-SP30-169-EN v07 |
| ARC-BMP06-169-EN | 0:06 | 16:9 | EN | Open | Product tone + music button | Bumper package | Logo + URL | PREROLL-169 | Draft | ARC-SP30-169-EN v07 |
| ARC-SP30-169-ME | 0:30 | 16:9 | — | None | Music & effects only | Spot package, textless | Textless | MEZZ-169 | Approved | ARC-SP30-169-EN v07 |

### Filled version matrix — Project C "Clear Water" (hypothetical)

| ID | Duration | Ratio | Language | Captions | Audio | Graphics | End card | Profile | Status | Parent |
|---|---|---|---|---|---|---|---|---|---|---|
| CW-05-169-HI | ≈5:10 | 16:9 | Hindi VO, Hindi text | Hindi closed captions | Hindi mix | Hindi package | Helpline card (Hindi) | CHANNEL-169 | Approved | — (master) |
| CW-05-169-EN | ≈4:50 | 16:9 | English VO, English text | English closed captions | English mix | English package | Helpline card (English) | CHANNEL-169 | Approved | — (master, shares picture edit with HI except timing adjustments) |
| CW-60-916-HI | 1:00 | 9:16 | Hindi | Hindi open | Hindi mix | Vertical package | Short card | SOCIAL-916 | In review | CW-05-169-HI v04 |
| CW-60-916-EN | 1:00 | 9:16 | English | English open | English mix | Vertical package | Short card | SOCIAL-916 | In review | CW-05-169-EN v04 |
| CW-05-169-TXL | ≈5:10 | 16:9 | — | — | M&E | Textless picture | — | MEZZ-169 | Approved | CW-05-169-HI v04 |

Note that the Hindi and English versions differ in duration (illustrative): the localization is a re-edit (Section 4).

## 2. Naming that prevents stale exports

Stale exports — an earlier version delivered or reviewed by mistake — are among the most common delivery failures.

**Convention:** `PROJECT-DELIVERABLE-RATIO-LANG_vNN_STATUS_YYYYMMDD.ext`, e.g., `ARC-SP15-916-EN_v03_APPROVED_20261012.mp4`.

**Rules** `[Practice]`:
- Version numbers only increase; never reuse a number.
- Status in the name reflects the matrix; superseded files move to a `SUPERSEDED/` folder immediately (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#3-naming-and-folder-structure)).
- The matrix records the exact file name delivered for each version.
- Review links show the version name in the title and burned-in on screen.

## 3. Series and recurring formats

For a series, continuity across episodes is a delivery constraint. A **series specification** records:

| Element | Inherited from the spec |
|---|---|
| Graphics | Templates, lower thirds, chapter cards, end cards |
| Typography | Roles, fonts (licensed), sizes per ratio |
| Music identity | Theme, stings, sound logo; licence covering the series |
| Grade | Look reference, LUTs/transforms, skin and brand colour targets |
| Caption styling | Font, size, position rules, style guide |
| Audio | Loudness profile per destination; stem layout |
| Delivery | Profiles and naming |

Later episodes inherit rather than reinvent; changes to the spec are versioned and applied deliberately (not drifted into).

## 4. Localization is a re-edit

Translating words is only part of localization. A localized version must be checked as a film in its own right.

| Factor | Effect | Workflow response |
|---|---|---|
| Reading time | Captions and on-screen text may need more or less time | Re-time captions; extend shots from handles |
| Text expansion/contraction | Layouts overflow or look empty | Design headroom; adapt copy |
| Script and font shaping | Rendering failures; different vertical space | Test tools and fonts (see [Localization](../TEXT-ACCESSIBILITY/Localization.md#3-devanagari-in-practice)) |
| Voice cadence | Narration duration and rhythm differ | Re-time picture to narration, or adapt the script; never speed up narration unnaturally |
| Currency, units, dates | Must match local conventions where appropriate | Approved conversions only |
| Cultural connotations | Imagery, gestures, colours, humour | Review by a cultural/linguistic reviewer |
| Adaptation approval | Changed wording needs approval | Subject-matter and client approval per language |
| Factual meaning | Must be preserved | Advisor reviews each language |
| Stereotypes | New audiences surface assumptions | Review; adjust examples |

### Re-checking the edit when narration duration differs

When the translated narration runs longer or shorter, the picture edit must respond:

| Situation | Options |
|---|---|
| Narration longer | Extend shots from handles; add a cutaway; adapt the script for brevity; never compress speech unnaturally |
| Narration shorter | Shorten shots; hold for comprehension pauses; keep music phrasing intact (see [Music Editing](../AUDIO/Music-Editing.md)) |
| Sync points (narration referring to an action) | Re-align picture to the new narration timing |

## 5. Worked example 1 — Hindi/English educational localization (hypothetical, Project C)

**Approach:** parallel production rather than "translate after". The script is written in English and Hindi in parallel, reviewed by the advisor in both languages, and recorded by two narrators. The picture edit is built on the Hindi narration (the primary audience), then adapted for English.

| Step | Action | Check |
|---|---|---|
| 1 | Parallel scripts; glossary agreed ("candle" → "कैंडल") | Advisor approval per language |
| 2 | Animatic with synthetic temp narration in both languages | Duration differences found (mechanism section longer in Hindi) |
| 3 | Picture edit to the recorded Hindi narration | Comprehension pauses kept |
| 4 | English version: same shots, re-timed; some holds shortened; one cutaway removed | Music re-edited at phrase boundaries |
| 5 | Graphics: both language packages from the same templates; text-length limits enforced | Devanagari rendering test |
| 6 | Captions: authored per language from the final scripts; re-timed to each recording | Checked on encoded files |
| 7 | Late factual change (see [Constraints and Priorities](../FOUNDATIONS/Constraints-and-Priorities.md#change-impact-map--filled-example-hypothetical-project-c-clear-water)) applied to both | Matrix updated; old exports superseded |

**Verification:** each version watched independently by a fluent viewer on a low-cost phone; recall test of steps per language; advisor sign-off per language.

## 6. Worked example 2 — Building cutdowns from a master (hypothetical, Project B)

**Rule:** cutdowns derive from the **approved** master version (recorded in the parent column). When the master changes (e.g., the late cut change in [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md#8-worked-example-2--multi-specialist-brand-job-with-a-late-cut-change-hypothetical-project-b-23976-fps)), every derived version is flagged "check" in the matrix until reviewed.

| Version | Derivation | Specific checks |
|---|---|---|
| 15 s vertical | Alternate edit using vertical framings | Interface collisions; ring legibility; captions upper zone |
| 6 s bumper | Locked-off ring reveal + logo | Ring lights within the first seconds; logo hold; music button |
| M&E (textless) | Master without VO/captions/text | For future adaptation; no dialogue leaks |

## 7. Counterexample and repair — the stale caption file

**Hypothetical counterexample.** For Project C's English version, the delivery folder contains the approved video (v04) and a caption file from v03 (before the factual change). The channel publishes them together. The captions say "removes 99% of bacteria" while the narration says "reduces most bacteria when maintained". Viewers relying on captions receive the superseded — and unsupported — claim.

**Diagnosis:** caption files were not tracked in the version matrix; naming didn't tie captions to video versions; QC checked the video but not the sidecar.

**Repair:**
1. Replace the caption file with the v04 captions immediately; notify the channel.
2. Add caption files (per language) as matrix columns with their own version IDs tied to the video version.
3. QC checks sidecars against the final audio on the destination player.

**Verification:** captions match narration on the published page; matrix shows caption versions aligned with video versions.

## 8. Micro-decisions

- Record the parent master's exact version for every derived version.
- When any master changes, flag all children for review.
- Keep textless versions and M&E mixes for future localization.
- Name caption and subtitle files with the same version ID as their video.
- Put the version ID on screen (slate or burn-in) in review copies.

## 9. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Stale version delivered | Naming and folder discipline | Matrix, naming, SUPERSEDED folder |
| Localized version feels rushed | Narration duration not accommodated | Re-edit to narration |
| Graphics overflow in translation | No text-length planning | Templates with headroom; copy adaptation |
| Inconsistent episodes | No series spec | Write and inherit the spec |
| Captions mismatch audio | Sidecars not versioned | Version captions with video |

## 10. Verification

- Each version verified independently on representative devices and on encoded outputs.
- Caption and graphic collisions checked per version.
- Audio and CTA changes checked per version.
- Matrix reconciled with delivered files before signoff.

## Dependencies

- Depends on: [Platform and Format Strategy](Platform-and-Format-Strategy.md), [Localization](../TEXT-ACCESSIBILITY/Localization.md), [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md).
- Feeds: [Quality Control and Export](Quality-Control-and-Export.md), [Audio Delivery](Audio-Delivery.md).

## Confidence summary

The version matrix, naming discipline and series specifications are `[Practice]`. Localization-as-re-edit is `[Practice]` in professional localization. Durations and version sets are `[Illustrative]`.
