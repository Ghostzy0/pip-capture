# Pip Capture

A local macOS inbox for voice, imported audio and text. Keep the original recording, edit a note, organise it with folders and tags, then return to the source or export your work.

**Experimental source only:** Core 0.1.0-alpha.4 and Plus 0.2.0-alpha.4 are unreleased candidates; binaries are withheld. Bounded native text-save/reopen cases are recorded for Neutral Core, Pip Core, Neutral Plus, Pip Plus and the separate Replica candidate; scenarios differ by edition. Pip Plus also has bounded Markdown export, text import/source recall, tag/search filtering, favourite and appearance-persistence evidence. Broader workflows remain unqualified. See [test evidence](TESTING.md), [custom draft PR5](https://github.com/Ghostzy0/pip-capture/pull/5) and [Replica draft PR3](https://github.com/Ghostzy0/pip-capture-replica/pull/3); current exact-head CI status is tracked in PR5.

No account, telemetry or hosted core service. Microphone recording needs macOS consent; recording acceptance remains unverified. Local transcription needs separately installed whisper.cpp and compatible weights; neither is downloaded automatically. Full Mem/Voicenotes equivalence is not claimed.

The version-only candidates identify the shared editor-save correction: Core `0.1.0-alpha.4` (build 4), Plus remains `0.2.0-alpha.4` (build 4), and Replica `0.1.0-alpha.3` (build 3). Published Core/Plus alpha.3 and Replica alpha.2 tags remain unchanged. The Replica source pin and static verifier are prepared in its separate draft.

## Four app variants

The canonical primary-reference Neutral Core recreation is being separated into [Capture Replica](https://github.com/Ghostzy0/pip-capture-replica). Its signed-in reference/layout fidelity remains incomplete. The neutral Core configuration here is retained as an original comparison for reproducibility; it is not proof of a faithful Voicenotes recreation.

All four use one local engine and the same note format. Separate app IDs and storage folders let them coexist without rewriting each other's library.

| Variant | Appearance | Scope | Storage folder in Application Support |
| --- | --- | --- | --- |
| Capture Neutral Core | Native neutral | Core workflows | Capture Neutral Core |
| Capture Neutral Plus | Native neutral | Core + compact recorder and tag filter | Capture Neutral Plus |
| Pip Capture | Paper/Oat Pip | Same Core workflows | Pip Capture |
| Pip Capture Plus | Paper/Oat Pip | Same Plus additions | Pip Capture Plus |

Core: text/audio import, explicit record/pause/resume/save/discard, editable notes and timed transcript corrections, original audio/timestamps, folders/tags/favourites/search, quoted source recall/highlights, Markdown/audio export, recoverable trash/drafts and explicit retention preview. Plus adds collapsible controls inside the main window and a selectable tag filter. No floating idle recorder, cloud service or new data format.

The additional `baseline/` directory preserves a licensed WhisperNotes snapshot at `05d12535863757943a7e243edd2df7cea1d86f84`, with declared safety and packaging repairs. It is a provenance comparison, separate from these four variants, with narrower functionality. See [provenance](UPSTREAM.md) and [notices](THIRD_PARTY_NOTICES.md). This is our original implementation; Mem/Voicenotes source is not included.

## Build and run

Requires Apple Silicon macOS 14 or later and full Xcode with command line tools selected. Verified host/build results are in [TESTING](TESTING.md); other architectures are unverified.

```sh
git clone https://github.com/Ghostzy0/pip-capture.git
cd pip-capture
swift test --jobs 2
./scripts/build.sh all
open 'build/Pip Capture.app'
# Or build one variant: neutral-core, neutral-plus, pip-core, pip-plus
./scripts/build.sh pip-core
# Optional independent upstream-derived comparison:
(cd baseline && swift test --jobs 2)
./scripts/build-baseline.sh
open 'build/Capture Baseline.app'
```

The scripts produce ad-hoc signed local bundles. They are **not Developer ID signed or notarised**. Use macOS's per-app approval if required; never disable Gatekeeper globally. Packages are only published when their exact build passed the stated checks. No weights or speech runtime are bundled.

[AI setup](docs/AI-SETUP.md) includes a short copyable prompt, exact speech installation commands and verification. Build artifacts, weights and recordings are excluded from Git. Xcode download and optional speech weights require network/storage; daily text capture/library/export works offline.

## Everyday use

Choose **New note** to write; press **Save changes** to commit. Unsaved edits survive switching captures and are saved before a normal quit; failed saves cancel quitting. Choose **Record → Start recording** to request microphone access. Pause/resume, then save or explicitly discard. Imports retain the original bytes. Transcribe only after choosing trusted local speech files in Settings. Check names, numbers and negation against the original audio. Playback and timestamp buttons navigate the source.

Folder names and comma-separated tags are edited in the note. Search finds saved note text/titles/tags/folders; **Find in sources** searches source excerpts and links back to the capture. This is deterministic text retrieval. Highlights quote selected saved sentences. Generative summaries, semantic answers, speaker diarisation, live transcription, cloud sync and mobile apps are not implemented.

**Recently deleted** keeps notes/audio until you explicitly delete permanently. Restore reverses a move. Retention is off by default: Settings can preview captures unchanged for 30 days and move only reviewed matches to Recently deleted. Nothing is deleted on a timer. Exports are separate copies and remain after deleting the app's copy.

## Storage, permissions and recovery

Each variant uses its own folder from the table above under `~/Library/Application Support/`. It contains `library.json`, `audio/` and unfinished `drafts/`. Baseline uses its own `Pip Capture Baseline` directory and app ID. No app silently imports the other's data. Back up the entire directory with the app closed. Data is local plaintext protected by normal OS account/file permissions; app-level encryption is not provided. Exports are separate files; check the privacy of the folder you choose.

The microphone permission is requested only from Start recording. Denial leaves text/import/export usable; permit the selected app in System Settings → Privacy & Security → Microphone if desired. No Accessibility/Screen Recording permission is required for the Pip core. A malformed/incompatible library blocks writes and preserves its bytes; open storage, keep a backup, then repair/restore it. Unfinished recording drafts appear for explicit recovery. A source file missing from disk does not erase its note.

## Status and help

[FAQ](docs/FAQ.md) covers privacy, variants and migration limits. [Workflows](docs/WORKFLOWS.md) explains capture, local transcription, export and recovery.

Read [CHANGELOG](CHANGELOG.md), [TESTING](TESTING.md), [PARITY](PARITY.md), [security](SECURITY.md) and [contributing](CONTRIBUTING.md). Setup trouble: check full Xcode selection, writable disk space, compatible speech weights, the chosen executable, and microphone consent. Keep source data backed up before testing an alpha upgrade.

Maintained by [Ghostzy0](https://github.com/Ghostzy0). Code is [MIT](LICENSE); upstream and font notices are preserved separately. [WhisperNotes](https://github.com/reidemeister94/whisper-notes) is the open-source foundation reference; [Mem](https://get.mem.ai/features/voice) and [Voicenotes](https://help.voicenotes.com/en/articles/11161004-how-to-use-voicenotes-on-mac) are independent workflow references. No affiliation or endorsement is implied.

Temporary transcription copies are created in the Pip library's `work/` directory and removed when a job finishes. After an app crash, Settings can explicitly clear marked work copies whose creating process has ended; originals/notes are kept. The optional file-fed CLI uses a private OS temporary `pip-capture-asr-UUID` directory and can leave one after a hard crash. Inspect/remove that exact derived directory only when no matching job is active. Never treat an exported recording as automatically deleted by library retention.
