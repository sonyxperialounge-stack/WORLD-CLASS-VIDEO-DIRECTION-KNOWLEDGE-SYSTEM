# Ingest and Preparation

**Purpose:** Teach how to bring media into a project safely and predictably — verified backups, naming, folder structure, proxies, sync, frame-rate and timecode conventions — so that every later department works from the same reliable clock and the same trusted masters.

**Applies to:** Every project, from a single phone shoot to multi-camera productions with separate audio and archive.

**Prerequisites:** [Decision Method](../FOUNDATIONS/Decision-Method.md) (units and timecode notation).

**Owns:** The project frame-rate and timecode convention, the backup and verification standard, proxy policy and sync method. Assessment of the material's creative value is in [Footage Assessment](Footage-Assessment.md); handoffs and interchange in [Production and Handoffs](Production-and-Handoffs.md).

---

## 1. Why ingest is an editorial matter

Ingest looks like clerical work. It is where the most expensive failures begin: a card formatted before its copy was verified, a variable-frame-rate phone clip that drifts out of sync, a proxy exported as the final master, a 23.976 fps timeline that silently turns 25 fps footage into slightly slow motion. None of these failures announce themselves at ingest. They surface weeks later in the grade, the mix, or — worst — after delivery.

The goal of ingest is simple to state: **every file is safe, findable, correctly interpreted and on a shared clock.**

## 2. Offload and verified backup

### 2.1 Principles

| Principle | Practice | Why |
|---|---|---|
| Never work from the only copy | Copy original media to at least two independent storage devices before formatting any card | Drives fail; cards are reused |
| Verify, do not just copy | Use copy software that computes a checksum (hash) of source and destination and compares them | A file can copy without error messages and still be corrupt |
| Keep originals unmodified | Never rename, transcode or edit inside the original media folders | Relinking, conform and archive depend on original names and metadata |
| Geographic or device separation | One copy off-site or on a separate device not connected to the edit system | Theft, fire, ransomware, a single power surge |
| Record what was done | An ingest log: card ID, date, files, sizes, checksums verified, destination paths, operator | Traceability; proves the backup existed |

### 2.2 Checksums explained

A checksum is a short value computed from every bit of a file. If the file changes by one bit, the checksum changes. Copy-verification tools compute it on the source and on each copy; matching values give strong evidence the copy is identical. Common algorithms include MD5 and the faster xxHash family; the specific algorithm matters less than consistency and the fact of verification. A file-size comparison alone is **not** verification.

### 2.3 The "3-2-1" concept

A widely used rule of thumb `[Practice]`: three copies of important data, on two different types of media or devices, one off-site. For a small team, a practical version is: the edit drive, a second backup drive kept separately, and a cloud or off-site copy of originals, project files and key exports. Projects with confidentiality requirements must check that off-site or cloud storage is permitted (see [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md)).

## 3. Naming and folder structure

A good structure lets someone who has never seen the project find any file in under a minute.

**Filled example — Project A "Second Shift" (hypothetical):**

```
SECOND-SHIFT/
  01_ORIGINAL-MEDIA/          (read-only after verification)
    2026-03-14_DAY01/
      ACAM_A001/              (card contents exactly as recorded)
      BCAM_B001/
      AUDIO_R001/
  02_DERIVED-MEDIA/
    PROXIES/
    CONFORMED-CFR/            (constant-frame-rate conversions of phone media)
    TRANSCRIPTS/
  03_PROJECT/
    EDIT/
    AUTOSAVE/
  04_AUDIO/
    MUSIC/  SFX/  VO/  STEMS/
  05_GRAPHICS/
    FONTS/  SOURCE/  RENDERS/
  06_COLOR/
  07_DELIVERABLES/
    APPROVED/  SUPERSEDED/
  08_DOCUMENTS/
    INGEST-LOG.md  RELEASES/  CLEARANCES/  PROJECT-NOTES.md
```

Rules that prevent typical failures:

- **Dates in ISO order** (YYYY-MM-DD) so folders sort chronologically.
- **No spaces or special characters** in folder names that will travel between systems.
- **Camera roll IDs** that match the slate and camera metadata.
- **Original and derived media separated** so nobody accidentally edits, deletes or archives the wrong one.
- **APPROVED versus SUPERSEDED deliverables** so a stale export is never mistaken for the current version (see [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md)).

## 4. The frame-rate and timecode convention

This is the single most important decision recorded at ingest. It must be written in `PROJECT-NOTES.md` and communicated to every collaborator — editor, motion designer, composer, caption editor, colorist, mixer.

### 4.1 What to decide

| Item | Decision | Example (Project A) | Example (Project C) |
|---|---|---|---|
| Timeline frame rate | The rate of the master and all versions | 25 fps | 29.97 fps |
| Timecode convention | Drop-frame (DF) or non-drop-frame (NDF), where applicable | Not applicable (25 fps has no DF) | NDF — chosen so that frame counts are exact in captions and music edits; the timecode will read about 0.3 s behind wall-clock time over 5 minutes, which is irrelevant for this piece |
| Treatment of off-rate sources | Conform, convert or interpret | Phone at variable rate → conform to constant 25 fps | Screen recordings at variable rate → conform to 29.97 constant |
| Start timecode of the master | A convention for programme start | 01:00:00:00 | 01:00:00:00 |
| Reference for notes | Which clock reviewers quote | Timeline timecode of the current version, with version ID | Same |

### 4.2 Drop-frame versus non-drop-frame

At 29.97 fps, there are not exactly 30 frames per second. If timecode counts 30 frame numbers per second, it slowly falls behind real time — by about 3.6 seconds per hour. **Drop-frame timecode** skips two frame *numbers* (not frames) at the start of each minute except every tenth minute, keeping the timecode within a fraction of a frame of clock time over long durations. It matters for broadcast schedules and long programmes. **Non-drop-frame** numbers every frame consecutively; it is simpler for frame arithmetic but drifts from the clock.

Neither changes the picture. The danger is **mixing them**: a caption file authored in DF against an NDF master will drift progressively; a music cue timed in NDF placed by DF timecode will land early or late. Pick one and state it.

### 4.3 Why the shared clock matters

Every later department references time:

- Review notes cite timecode ("at 01:02:14:10, the caption covers her mouth").
- The composer edits music to picture by timecode or frame.
- Caption files are timed by timecode or milliseconds.
- The colorist and mixer receive turnovers referenced to the timeline.

If these do not share the same frame rate, convention and version, notes point at the wrong frames, captions drift, and music hits land a frame or two off. State the version as well as the timecode: "v07, 01:02:14:10".

## 5. Mixed-rate footage

Footage frequently arrives at rates other than the timeline's. There are three distinct operations, often confused:

| Operation | What happens | Effect | Use when |
|---|---|---|---|
| Interpret (conform playback rate) | The edit system plays every recorded frame at the timeline rate | Motion speeds up or slows down; audio, if kept, changes speed (and pitch unless corrected) | High-frame-rate capture intended for slow motion (59.94 → 23.976 gives 40% speed) |
| Frame-rate conversion (cadence) | Frames are repeated or dropped to fit the timeline rate | Real-time motion with uneven cadence (judder) | Small amounts of off-rate B-roll where slight judder is acceptable |
| Motion-compensated / optical-flow conversion | New in-between frames are synthesised | Smoother real-time motion; risk of warping artefacts on complex motion | Off-rate material that must look smooth; check every shot |

### Common cases

| Source | Timeline | Typical treatment | Watch for |
|---|---|---|---|
| 25 fps | 23.976 fps | Interpret (≈4% slow motion, audio pitch drop) only if acceptable; otherwise convert | Speech pitch, lip sync, slightly sluggish motion |
| 29.97 fps | 25 fps | Conversion with frame blending or optical flow | Judder on pans; ghosting |
| 59.94 fps | 23.976 fps | Interpret for slow motion (≈40% speed), or convert for real-time | Shutter: 59.94 fps at 1/120 s gives crisp slow motion; at real time it looks staccato |
| 23.976 fps | 24 fps (cinema) | Usually interpreted (0.1% change) | Audio sync drift if audio is not resampled correspondingly |

Shutter and motion-blur consequences of these choices are explained in [Capture Decisions](../CAMERA/Capture-Decisions.md) and [Retiming and Virtual Motion](../CAMERA/Retiming-and-Virtual-Motion.md).

### Variable-frame-rate sources

Phones and screen-recording software often record **variable frame rate (VFR)**: the interval between frames changes depending on processing load and scene content. Many edit systems handle VFR poorly; symptoms include gradual audio drift, stutter, and frames that do not match timecode between systems.

**Practice** `[Practice]`: detect VFR at ingest (media-information tools report frame-rate mode), and transcode VFR files to constant frame rate (CFR) at the project rate into a clearly labelled derived-media folder before editing. Keep the original VFR file. Check sync at the start, middle and end of long clips after conforming.

## 6. Sync and dual-system audio

### 6.1 Methods

| Method | How it works | Confidence | Failure modes |
|---|---|---|---|
| Shared timecode (jam sync or wireless timecode) | Camera and recorder record the same time-of-day timecode | High when re-jammed regularly | Drift on some cameras over hours; wrong rate setting on recorder |
| Slate / clap | A visual and audible event aligned manually | High per clip | Missed slates; laborious |
| Audio waveform matching | Software aligns camera scratch audio to recorder audio | Medium–high | Fails with no or noisy scratch audio; VFR sources drift |
| Manual by lip | Editor aligns by eye and ear | Variable | Time-consuming; prone to one-frame errors |

### 6.2 Sync confidence and verification

Mark each synced clip with a confidence level and check method. Lip sync errors of a frame or two can be noticeable on close-ups of speech, especially when audio leads picture; viewers tend to be more tolerant of audio slightly late than early `[Heuristic]`. Check sync on close-ups at the start, middle and end of long takes. After any frame-rate conversion, re-check.

### 6.3 Dual-system specifics

- Confirm the recorder's sample rate (commonly 48 kHz for video) and its timecode frame rate match the project. A recorder set to 29.97 timecode on a 25 fps shoot breaks timecode sync.
- Keep the recorder's polyphonic or multi-track files intact; do not mix down at ingest. The dialogue editor needs isolated tracks.
- Record a brief verbal ident at the start of each recorder take (scene/take) as a backup to metadata.

## 7. Proxies

### 7.1 Proxy versus master

A **proxy** is a lighter, lower-resolution or more edit-friendly copy of a master file, used to edit smoothly on modest hardware. A **master** (camera original or a high-quality mezzanine) is what the final picture is conformed from.

| | Proxy | Master |
|---|---|---|
| Purpose | Smooth editing, remote collaboration | Final quality, grading, delivery |
| Quality | Reduced resolution, heavier compression, often display-referred color | Full resolution, original encoding, full color data |
| Risk | Exported by mistake as a deliverable | Too heavy to edit on available hardware |

### 7.2 Preventing accidental proxy export

Proxy exports reach clients surprisingly often. Defences:

- Burn a small, unobtrusive "PROXY" label into proxy media (some workflows do this at creation).
- Name proxy files with a suffix (`_PRX`) and store them in a clearly named folder.
- Before every export, check the media source setting in the edit system (proxy vs original/full-resolution).
- QC exports at 100% scale for resolution and texture; proxies look soft and blocky at full size.
- Never deliver from a timeline that has not been explicitly relinked to masters.

### 7.3 Proxy color

If proxies are created with a display LUT baked in (to make log footage look normal while editing), the edit looks graded but the masters are still log. That is fine — provided everyone knows that the proxy appearance is not the grade, and that the conform relinks to masters with the correct input transform. Document the proxy LUT in the project notes. See [Color Management](../COLOR/Color-Management.md).

## 8. Relinking

Relinking reconnects a project's clips to media files — for example, from proxies to masters, or after media moves. It succeeds when file names, reel/tape names, timecode and durations are consistent. It fails when files were renamed, when duplicate names exist (two cameras both producing `C0001.MP4`), or when derived media lacks original timecode.

Prevent failures by keeping original names, creating proxies that preserve source timecode and reel names, and giving each camera a unique roll prefix.

## 9. Metadata, transcripts and color assumptions

At ingest, record:

- **Camera metadata:** profile/log curve, color space, ISO/EI, white balance, shutter, lens where available.
- **Scene/take** from slates or logs.
- **Transcripts** for interview material, generated or human, marked with their verification status (see [Footage Assessment](Footage-Assessment.md#4-logging-versus-creative-selection)).
- **Color assumptions:** which input transform each camera needs, and which display transform is used for monitoring — so the colorist does not inherit a mystery. See [Color Management](../COLOR/Color-Management.md).

## 10. Archive and third-party ingest

Archive and third-party media get extra records: source, date received, licence reference, original format and frame rate, whether the file is already a conversion (look for judder cadence or interlacing), and any restriction on alteration. Store the licence document with the media reference. See [Footage Assessment](Footage-Assessment.md#5-archival-and-third-party-material).

## 11. Worked example 1 — Project A ingest (hypothetical)

| Step | Action | Result |
|---|---|---|
| Offload | A-cam card, phone media, recorder card copied with checksum verification to edit drive and backup drive | Verification log shows all checksums matched; ingest log updated |
| Off-site | Originals uploaded overnight to the nonprofit's approved cloud storage (confirmed permitted under the hospital agreement) | Third copy |
| Rate check | A-cam 25 fps CFR; recorder 48 kHz, timecode 25 fps; phone: variable frame rate averaging ≈ 25 fps | Phone flagged VFR |
| Conform | Phone files transcoded to CFR 25 fps into `02_DERIVED-MEDIA/CONFORMED-CFR/` | Originals preserved |
| Sync | A-cam ↔ recorder by timecode; phone ↔ A-cam by waveform | Checked at start, middle, end; phone clip B001_C009 drift < 1 frame after conform |
| Proxies | Created at reduced resolution with source timecode and names, with the camera manufacturer's log-to-display LUT applied for viewing | Documented in project notes |
| Notes | `PROJECT-NOTES.md`: 25 fps; master starts 01:00:00:00; phone conformed; proxy LUT named; Hindi transcripts unverified | Shared with the translator and caption editor |

## 12. Worked example 2 — Screen recordings and music for Project C (hypothetical)

Project C includes a 40-second segment showing a phone app that reminds users to clean their filter. The screen recording was captured with a phone's built-in recorder.

- **Finding:** the screen recording is VFR; it alternates between about 60 fps during animation and as low as about 10 fps when the screen is static.
- **Decision:** conform to CFR 29.97 fps NDF to match the timeline. Static periods duplicate frames (no visual change); animated periods drop frames (slight loss of smoothness in UI animation — acceptable).
- **Music and captions:** the composer receives a reference export with burned-in timecode (29.97 NDF) and a written note of the convention. The caption editor receives the same. Because NDF is used throughout, a cue at 01:02:10:15 means the same frame for all three.
- **Verification:** after the composer's music is laid in, the editor checks three hit points against picture; the caption file is checked on the encoded export, not only in the edit system.

## 13. Counterexample and repair — the drifting phone and the proxy master

**Hypothetical counterexample.** A small team edits an event film using phone footage imported directly (VFR) and a separate audio recorder. They edit with proxies that have a display LUT baked in. The client approves the cut. The editor exports "the final" late at night.

Problems found after delivery:
1. Lip sync drifts by about 5 frames late in a 20-minute speech clip.
2. The delivered file is 960 pixels wide and looks soft and blocky on the client's projector — it was exported from proxies.
3. The colorist, given the project later for a festival version, finds the timeline linked to proxies and the masters still in log, with no note of which LUT was used.

**Diagnosis.** VFR was never detected; proxies were never relinked; color assumptions were never documented.

**Repair.**
1. Conform phone originals to CFR; re-sync the speech using the recorder audio as master; verify at multiple points.
2. Relink the timeline to master media; confirm in the export settings that source media is full resolution.
3. Identify the proxy LUT from the proxy-creation preset; document it; give the colorist the masters with the correct input transform.
4. Re-export, QC at full size, and replace the delivered file with a clear version number. Mark the old file as superseded.

**Verification.** Full-length playback of the speech checking lip sync at intervals; inspection of the export at 100% on a large display; colorist confirms the masters' interpretation.

## 14. Micro-decisions

- Write the timeline frame rate and timecode convention on the project's first marker and in the export file names of review copies (e.g. `ARC_SPOT30_v05_23976.mp4`).
- Set the recorder's timecode rate before the first take, not after.
- Never format a card until two verified copies exist and the person formatting has seen the verification log.
- When receiving media from others, ask for the original files, not exports from their phone gallery or messaging apps, which are often re-compressed and stripped of metadata.
- Keep a short "known issues" section in the project notes (e.g. "B001_C009: brief sync check at 12:40 — OK").

## 15. Failure signatures and corrections

| Symptom | Ingest cause | Correction |
|---|---|---|
| Gradual lip-sync drift | VFR or sample-rate mismatch | Conform to CFR; check recorder sample rate; re-sync |
| Motion slightly slow and voices low-pitched | Off-rate footage interpreted at the timeline rate | Re-interpret or convert; decide intentionally |
| Captions drift over the programme | DF/NDF mismatch between caption file and master | Re-time in the project convention |
| Relink fails | Renamed files; duplicate names | Restore original names; unique roll prefixes |
| Soft, blocky deliverable | Proxy export | Relink to masters; export check |
| Colorist cannot reproduce the edit's look | Proxy LUT undocumented | Document LUT; apply correct transform |

## 16. Verification

- Ingest log shows checksum verification for every card.
- Project notes state rate, timecode convention, proxy policy, color assumptions and known issues.
- A spot check of five random clips relinks correctly from proxy to master.
- Sync is checked at three points in every long multi-source clip.

## Dependencies

- Feeds: [Footage Assessment](Footage-Assessment.md), [Production and Handoffs](Production-and-Handoffs.md), [Color Management](../COLOR/Color-Management.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Music Editing](../AUDIO/Music-Editing.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).
- Camera-side causes: [Capture Decisions](../CAMERA/Capture-Decisions.md).

## Confidence summary

Verified backups, original-media preservation, documented frame-rate/timecode conventions, CFR conforming of VFR sources and proxy safeguards are `[Practice]`. The DF/NDF arithmetic (≈3.6 s per hour difference at 29.97 fps NDF) is a technical fact. Lip-sync tolerance observations are `[Heuristic]`; tolerance varies with shot size and viewer.
