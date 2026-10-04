# Quality Control and Export

**Purpose:** Teach how to define delivery profiles, distinguish masters from distribution copies, run staged quality control — including flash and pattern risk — and sign off deliverables with evidence, so that "the export finished" is never mistaken for "the piece is checked".

**Applies to:** Every deliverable.

**Prerequisites:** [Versioning and Localization](Versioning-and-Localization.md), [Audio Delivery](Audio-Delivery.md), [Color Management](../COLOR/Color-Management.md).

**Owns:** Delivery profiles, the staged QC process, the flash/pattern QC gate and signoff. Destination loudness is owned by [Audio Delivery](Audio-Delivery.md); rights evidence by [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

---

## 1. Delivery profiles

A delivery profile is the written specification of a deliverable. It should be copied from the destination's current documentation (or agreed with the client) and stored with the project.

| Field | Examples of what to specify | Why it matters |
|---|---|---|
| Destination | Platform, broadcaster, distributor, client archive | Determines everything else |
| Container | MOV, MP4, MXF | Compatibility |
| Video codec and profile | A mezzanine codec (e.g., an intra-frame professional codec) or a distribution codec (e.g., H.264/H.265 at a stated profile) | Quality, size, compatibility |
| Resolution and aspect ratio | 1920×1080, 3840×2160, 1080×1920; pixel aspect ratio | Display; cropping |
| Frame rate and scan | 23.976p, 25p, 29.97p; progressive | Motion; compatibility |
| Bit depth and chroma subsampling | 10-bit 4:2:2 for masters; 8-bit 4:2:0 common for distribution | Banding; colour fidelity |
| Colour tags and range | Primaries, transfer function, matrix; full or legal range | How players display it |
| HDR metadata (if HDR) | Mastering display, content light levels, dynamic metadata per the HDR system | HDR display behaviour |
| Bitrate strategy | Constant vs variable; target and maximum | Quality vs size |
| Audio | Layout, sample rate, bit depth, loudness target and method, true-peak limit | Compliance (see [Audio Delivery](Audio-Delivery.md)) |
| Captions/subtitles | Format, embedded or sidecar, languages, burned-in variants | Accessibility; platform support |
| Slate, leaders, black | Required head/tail elements | Broadcast and archive specs |
| Naming and metadata | File naming convention; embedded metadata | Tracking; ingestion |

### Filled profiles (hypothetical; exact values must come from current destination specs)

| Profile ID | Use | Container / codec | Picture | Audio | Captions | Notes |
|---|---|---|---|---|---|---|
| MEZZ-169 | Archive master, source for all distribution | MOV, professional intra-frame codec, 10-bit 4:2:2 | 1920×1080 (UHD for Arc), project frame rate, BT.709 tags, legal range | 48 kHz/24-bit, stereo + stems as separate files | Sidecar files per language | Textless and texted versions |
| WEB-MASTER-169 | Upload to video platforms and players | MP4, H.264 high profile, high bitrate | 1920×1080, project rate, BT.709 tags | AAC stereo at a high bitrate; loudness per [Audio Delivery](Audio-Delivery.md) | Sidecar (platform-supported format) | Platform re-encodes |
| SOCIAL-916 | Vertical feeds | MP4, H.264 | 1080×1920, project rate | AAC stereo | Open captions burned in | Check current platform specs for length/size |
| CHANNEL-169 | Public-health channel website | MP4, H.264 | 1920×1080 | AAC stereo | Sidecar captions per language | Check the channel's player caption support |
| PREROLL-169 | Pre-roll placements | Per ad platform spec | Per spec | Per spec | Open captions | Ad platform specs vary |

## 2. Master versus distribution copy

| | Mezzanine / master | Distribution copy |
|---|---|---|
| Purpose | Highest practical quality; source for future versions; archive | Efficient delivery to viewers or platforms |
| Compression | Light (intra-frame or high-bitrate) | Heavy (long-GOP, lower bitrate) |
| Bit depth / chroma | 10-bit or higher, 4:2:2 or 4:4:4 | Often 8-bit 4:2:0 |
| Edits from it | Safe | Avoid re-encoding repeatedly (generation loss) |

Make distribution copies from the master, not from other distribution copies.

### Render and encoding artefacts to look for

| Artefact | Cause | Check |
|---|---|---|
| Banding in gradients | 8-bit encoding; heavy grade; low bitrate | Skies, dark backgrounds, vignettes |
| Macro-blocking | Low bitrate; noise and grain; fast motion | Dark scenes, water, grain |
| Mosquito noise / ringing | Compression around sharp edges | Text and graphics edges |
| Gamma/contrast shift | Colour tags or player interpretation | Compare in target players |
| Range mismatch | Full/legal mismatch | Milky or crushed blacks |
| Frame rate conversion artefacts | Export at a different rate than the timeline | Motion judder |
| Audio drift | Sample-rate or frame-rate mismatch | Sync at end of programme |
| Caption loss | Unsupported caption format; stripped on export | Captions present in output |

## 3. Staged QC

QC is staged so that problems are caught where they are cheapest to fix. Each stage has pass criteria and a failure route.

| Stage | Checks | Pass criterion | Failure action |
|---|---|---|---|
| 1. Source and edit | Every shot is the intended take; no flash frames; no gaps; no offline media; correct version | Timeline review at full speed; frame-step at cuts | Fix in edit |
| 2. Picture, colour, VFX | Shot matching; no clipping errors from transforms; VFX approved versions; no artefacts; masks intact | Full-speed review on calibrated display; checklist | Return to colour/VFX |
| 2a. Flash and pattern risk (gate) | Rapid flashes, saturated red flashes, high-contrast regular patterns, strobing, rapid cuts between very different luminance levels | Automated PSE-type analysis where the destination requires or the content is at risk, plus human review; destination requirement identified | Re-edit, reduce contrast/frequency, or (only where permitted) a warning — see Section 4 |
| 3. Sound and sync | Dialogue intelligibility; no clicks; sync at start, middle, end; loudness and true peak per spec | Listening pass; meter readings recorded | Return to mix |
| 4. Text, language, accessibility | Spelling, names, numbers; caption accuracy and timing; translations reviewed; readability on devices; no information by colour alone | Checklists per language | Return to graphics/captions/localization |
| 5. Rights and disclosure | Register complete; licences match version uses; disclosures present; privacy masking in every version | Register reviewed against version matrix | Remove/replace/clear |
| 6. Export | File matches the delivery profile (codec, resolution, rate, tags, range, audio layout, captions) | Media-information inspection | Re-export |
| 7. Encoded playback | The actual delivered file played in target players/devices, start to finish | Full playback; spot checks | Re-export or fix upstream |
| 8. Version reconciliation | Every deliverable in the version matrix exists, with correct names, parents and sidecars | Matrix and folder reconciled | Fix naming, re-export |
| 9. Archive and restore | Masters, projects, documents archived; restore tested | Restore test passed | Repair archive |

## 4. Flash and pattern risk

Flashing images and certain regular patterns can trigger seizures in people with photosensitive epilepsy. This is a **final-output QC gate**, separate from creative choices about strobe or flicker.

**Reference guidance (verified 2026-10-04; see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md)):**

| Source | Summary | Status |
|---|---|---|
| W3C WCAG 2.2, Success Criterion 2.3.1 "Three Flashes or Below Threshold" (Level A) | Content should not flash more than three times in any one-second period, unless the flashes are below the general flash and red flash thresholds; the definitions involve luminance change, saturated red, and the area of the screen affected | `[Requirement]` for web content claiming WCAG conformance |
| ITU-R BT.1702 (current version BT.1702-3, 2023), "Guidance for the reduction of photosensitive epileptic seizures caused by television" | International guidance for television | `[Practice]`/`[Requirement]` where adopted by broadcasters; document title and version verified, content not reproduced here |
| UK broadcast regulation (Ofcom) | UK broadcasters must take precautions to reduce the risk from flashing images; automated testing is widely used | Reported via secondary sources; verify the current Ofcom guidance before claiming compliance |

**Practice:**
- Identify the destination's requirement (broadcasters often specify automated PSE testing; online platforms may not).
- Run automated analysis where required or where content is at risk (strobes, lightning, rapid cuts between black and white, flashing graphics, high-contrast stripes or checkerboards in motion).
- Review flagged sections with a human; consider area of screen, frequency, contrast and red saturation.
- Prefer re-editing (fewer flashes per second, lower contrast, smaller flashing area, slower alternation) over warnings. Warnings do not make content safe and may not satisfy destination requirements.
- Re-check after any change to the affected section and after encoding.

## 5. Signoff gate

A deliverable is approved only when a signoff record exists:

| Field | Content |
|---|---|
| Deliverable ID and file name | From the version matrix |
| QC stages passed | With dates and reviewers |
| Evidence | Meter readings; media-information report; flash analysis report (if applicable); caption check notes; rights register reference |
| Known limitations | Anything accepted with reason (e.g., "minor focus softness at 00:02:13 accepted for performance") |
| Approver | Name, role, date |

**Reject/rework route:** a failed stage returns the deliverable to the owning department with the failure noted in the review log (see [Review and Revisions](../OPERATIONS/Review-and-Revisions.md)); after the fix, the stage — and any later stage affected — is repeated.

**An export that completed successfully is not a checked deliverable.** Export software confirms only that a file was written.

## 6. Worked example 1 — Small-team QC (hypothetical, Project A)

**Team:** the editor (who also graded and mixed), the producer, a bilingual reviewer.

| Stage | Who | Notes (hypothetical) |
|---|---|---|
| Edit | Editor | One flash frame found at a cut and fixed |
| Picture | Editor + producer on a calibrated monitor | B-cam match accepted; projection check scheduled |
| Flash/pattern | Editor | Low risk content; fluorescent flicker not present (25 fps, 1/50 s); no strobing; automated check not required by the online destination — noted |
| Sound | Editor | Readings recorded for web master; projection copy checked in the screening room |
| Text/language | Bilingual reviewer | Two subtitle line breaks improved; one name corrected |
| Rights | Producer | Register complete; masking verified in the 9:16 excerpt |
| Export | Editor | Media-information report matches profiles |
| Encoded playback | Producer | Watched full film on the series page player and a phone; captions on |
| Versions | Producer | Matrix reconciled |
| Archive | Editor | Restore test on the nonprofit's machine |

## 7. Worked example 2 — Multi-specialist QC (hypothetical, Project B)

| Stage | Owner | Specific checks |
|---|---|---|
| Edit | Editor | Conform matches offline reference (difference check) |
| Picture/VFX | Colorist, VFX lead | Screen-replacement shot reviewed encoded; ring colour vs brand spec |
| Flash/pattern | Finishing | The montage includes a quick light flicker effect on the alarm; automated analysis passes; human review confirms |
| Sound | Mixer | Readings recorded per deliverable; stems null-tested |
| Text | Motion designer, legal | Claim wording approved; captions per version |
| Rights | Producer | Music licence covers all placements and term; Dev's release; UI approval |
| Export | Finishing | Profiles matched; caption sidecars named with version IDs |
| Encoded playback | Producer, brand lead | Ad platform preview tools; phones; muted and unmuted |
| Versions | Producer | All five versions reconciled; superseded files moved |

## 8. Counterexample and repair — the strobing launch reel

**Hypothetical counterexample.** The festival app launch reel's peak (0:22–0:38) cuts between white-flash frames and dark crowd shots on every beat at 120 BPM (two alternations per second), with additional strobing stage lights in the footage. The reel is approved creatively and exported. Before the event screening, an accessibility reviewer runs a flash analysis: several segments exceed three flashes per second at large screen area and high contrast.

**Diagnosis:** a creative strobe choice combined with strobing source footage produced flash rates beyond accepted thresholds; flash risk was not treated as a QC gate.

**Repair options:**

| Option | Effect |
|---|---|
| Reduce flash frequency — white flashes only on every second bar | Lower rate; retains energy |
| Reduce contrast — flashes to mid-grey rather than full white; darken strobing light areas | Lower luminance change |
| Reduce area — flashes as a smaller graphic element rather than full frame | Below area threshold |
| Remove strobing footage sections or replace with non-strobing shots | Removes source risk |

**Choice:** combine reduced frequency and contrast, and replace the most strobing shots. Re-run analysis until it passes; human review.

**Verification:** analysis report attached to the signoff; the reel still reads as energetic in a fresh-viewer check.

## 9. Micro-decisions

- Keep media-information reports for every delivered file.
- Watch the very first and last seconds of every export (leaders, black, cut-offs, end cards).
- Check captions on the platform after upload, not only in the file.
- Recheck true peak after the final encode.
- Don't QC on the same display the work was done on only; include consumer devices.
- Record "not applicable" decisions explicitly (e.g., "no PSE test required by destination; content low risk; reviewed").

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Platform rejects file | Profile mismatch | Re-check current spec; re-export |
| Looks different in players | Colour tags/range | Correct tags; test players |
| Captions missing online | Unsupported format; not uploaded | Correct format; upload; verify |
| Late discovery of flash risk | Gate skipped | Run analysis earlier; re-edit |
| Wrong version delivered | Matrix not reconciled | Reconcile; naming discipline |
| Archive unusable | No restore test | Test restore |

## 11. Verification

- Every stage's pass criterion met, with evidence recorded.
- Encoded files played in real target conditions.
- Flash/pattern gate passed or documented as not applicable with reason.
- Signoff recorded; limitations stated.

## Dependencies

- Depends on: [Versioning and Localization](Versioning-and-Localization.md), [Audio Delivery](Audio-Delivery.md), [Color Management](../COLOR/Color-Management.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md), [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md).
- Gate used by: [Master Checklist](../MASTER-CHECKLIST.md).

## Confidence summary

Staged QC, master/distribution distinctions and signoff with evidence are `[Practice]`. WCAG 2.3.1 wording and ITU-R BT.1702-3's title and date were verified; Ofcom specifics are reported via secondary sources and must be checked. Delivery profiles shown are `[Illustrative]` templates — values must come from current destination documents.
