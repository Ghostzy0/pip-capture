# Changelog

## Plus 0.2.0-alpha.4 candidate — updated 25 October 2026

The first alpha.4 layout failed native pixel review at 2400×1520 because Start recording was partly clipped; the earlier 900×650 result was not achieved. The revised layout moves the compact Plus footer below the flexible split view and bounds the sidebar with scrolling. On 25 October, the full idle Start control was visible in a native capture at 2400×1520; 900×650 was not run, so the two-size gate remains open. Starting recording reached “Waiting for microphone access”; the app's discard confirmation returned to the empty Inbox before quit. No recording or permission grant was observed, and the capture did not establish whether the macOS privacy overlay appeared.

The prior public draft source at `7de411a` passed 49 shared tests, four local package/configuration/signature checks, independent source review, and exact-head public CI ([PR5](https://github.com/Ghostzy0/pip-capture/pull/5)). A later saved-JPEG estimate raised a contrast concern for the 13-point recorder caption; the current source follow-up applies the shared `CaptureTheme.secondary(scheme)` token. All four local package/configuration/signature checks passed for the caption revision. Its native contrast has not been remeasured; exact-source public CI is a separate source-freeze gate tracked in PR5. The full-Start result and CI above are for the pre-caption-change package/source. Core remains 0.1.0-alpha.3. Plus 0.2.0-alpha.4 remains unreleased; no binary or full native-acceptance pass is implied.

## Core 0.1.0-alpha.3 / Plus 0.2.0-alpha.3 — 24 October 2026

Draft recovery now distinguishes a committed note from pending cleanup and keeps retry identity separate from distinct recordings. Plus resets a fresh idle recorder to expanded. Subsequent native pixel review found Start clipped below its viewport; the alpha.4 entry above tracks the correction. Replica 0.1.0-alpha.2 applies its existing Light/Dark/Device choice. These candidates passed 49 shared regressions and all package/configuration/ad-hoc signature checks. Native follow-up, publication and binary acceptance are separate. Previous source previews and their exact evidence remain in Git history.

## Qualification patch 2 — 23 October 2026

Core 0.1.0-alpha.2 / Plus 0.2.0-alpha.2 correct selected-row contrast under the macOS accent and guard Settings/About while a recording needs attention. The neutral replica surface is explicitly selected by its own package flag and data identity; it remains an incomplete primary-reference reproduction. No native microphone or full layout-fidelity pass is implied. Previous alpha1 source checkpoints remain in Git history.

## 0.2.0-alpha.2 — Plus qualification in progress

Neutral Plus and Pip Plus share two additions: collapsible recording controls inside the main window and a library tag filter. Collapsing preserves the same recording session; active state/time and Save stay visible. Tag filtering composes with text/folder/favourites/trash. Separate app/data identities preserve the Core libraries. Actual package and native acceptance are recorded in TESTING; this entry alone is not a release claim.

## 0.1.0-alpha.2 — 23 October 2026

Initial experimental Core variants (neutral and Pip), plus a separately pinned provenance comparison. Pip adds a native local text/audio inbox, source-preserving imports, real recording controls, local timestamped transcription adapter, editable notes, folders/tags/favourites/search, quoted source recall/highlights, Markdown/audio export, recoverable trash and opt-in retention preview. Paper light/dark and Oat themes use locally bundled Geist and an original geometric Pip.

The baseline preserves pinned MIT WhisperNotes with app/data isolation and a macOS SwiftPM resource packaging repair. Models and speech engines are not bundled. Full competitor parity, generative summaries, speaker diarisation, live transcript, mobile/sync, Developer ID signing and notarisation are not claimed.

Patch notes during qualification: protect source metadata when saving concurrent edits; reconcile edits before retention; clear cancelled/trashed transcription state; refuse file-fed output overwriting any source; isolate every baseline data path; preserve corrupt indexes and unfinished source files. Final passing evidence is recorded in TESTING, not inferred from these notes.
