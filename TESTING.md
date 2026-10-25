# Test evidence

## Plus alpha.4 candidate — updated 25 October 2026

### Native text-save round R3 — 25 October 2026

The exact Pip Capture Plus package `98ee0141…` with Swift sources matching public draft `e683a6b` passed the tested native text workflow for synthetic title `Native-Keyboard-N25R3`: the fictional source text, including its negation, £18.40, distinct times and two tags, survived ⌘S, normal quit/reopen, and native Trash → Restore with the same fields and favourite. The app showed the saved state and disabled Save button before quit; the owned executable was absent after quit. Independent saved-evidence review agrees. This is one Plus workflow/package result only; it does not establish Core, all-variant, full fidelity, signing, downloadable-binary or release acceptance.

An export attempt showed the app's saved status and a 567-byte file in Documents while the intended owned temporary folder remained empty. The file was not read or moved after the stalled reader was cancelled before verification, so export content and destination correctness remain unverified. This is not evidence of an app export defect.

The first alpha.4 layout (clean export `a1463d602054a59fa596878ae942daa668715f84`) passed all 49 shared tests and all four package/configuration/ad-hoc-signature checks. Its native pixel review **failed** at 2400×1520: Start recording was partly clipped. A 900×650 native result was not achieved. These checks and pixels apply only to that earlier layout.

The revised layout source at public draft head `7de411a265cb4cd37a0e0f913b92545e6eee77c5` received independent source review with no blocking finding; exact-head public CI run [40125190137](https://github.com/Ghostzy0/pip-capture/actions/runs/40125190137) passed. Its previously reported 49 shared tests (zero failures/skips) and four local package/configuration/ad-hoc-signature checks are historical evidence for that source revision; they do not establish exact-source CI for later changes.

Earlier 25 October saved native frames for a Plus alpha.4 package showed the full idle Start control at 2400×1520 and 1802×1278 pixels. A later current Plus JPEG showed full Start at 1800×1276; the exact 900×650 target was not explicitly set, so none of these closes the original two-size gate. The light-mode JPEGs show the 13-point recorder caption at an estimated 6.9–7.1:1 against the sampled panel background. This is a pixel estimate with JPEG and antialiasing limits, not a full WCAG certification; dark-mode contrast is unmeasured. The earlier frames predate the keyboard-save change; the later 1800×1276 JPEG shows recorder geometry but does not exercise keyboard save.

In a separate bounded interaction, Start entered “Waiting for microphone access”; the native discard confirmation returned to the empty Inbox and the app was quit. No recording or permission grant was observed, and the app-only capture did not establish whether a separate macOS privacy overlay was visible.

The earlier native `⌘S` failure on package `fb329f11…` with Swift sources matching public draft `fa21037` repeatedly lost its changed title ([issue 6](https://github.com/Ghostzy0/pip-capture/issues/6)); that result remains tied to that package. The corrected source routes both Save actions through the current selected edit and leaves the Capture menu as the sole `⌘S` shortcut. The model regression checks synthetic title, body and favourite persistence through store reopen but does not exercise SwiftUI shortcut dispatch. The R3 native result above closes this behavior only for the tested Plus package and scenario; other editions and broader keyboard acceptance remain open.

The keyboard-save correction passed the complete local `swift test` suite: **50 tests, zero failures/skips** (25 app/audio and 25 store tests), including the selected-save regression. All four custom packages passed local configuration and strict ad-hoc-signature checks for that source revision; no checks were rerun for this documentation update. Exact-head public CI for the current source changes remains pending; the passing run at `7de411a` is historical ([PR5](https://github.com/Ghostzy0/pip-capture/pull/5)). Published Core alpha.3 and the Replica alpha.2 source pin remain unchanged; the shared-editor correction requires future Core versioning and Replica backport/pin review before their next releases. Plus alpha.4 is unreleased and binaries are withheld.

Official Voicenotes for Mac 2.3.7 build 102 was directly observed navigating Home → bundled Welcome example detail → Back to Home. This confirms those visible navigation steps only. The separate signed-in Voicenotes web observation in Brave remains version-unverified and historical; it does not establish native app parity. Only bundled example content was inspected. Reference pixels remain private and are excluded from this repository.

## 24 October 2026 candidate fixes

Core 0.1.0-alpha.3 / Plus 0.2.0-alpha.3 passed 49 shared tests, zero failures/skips (25 storage, 5 model, 12 audio/worker, 7 edition). New regressions use real temporary files with one exact unlink failure injected after a successful note commit; retries/reopen preserve one recovered note and original bytes. Distinct recordings with identical bytes stay distinct, changed drafts remain distinct, missing/corrupt recovered audio preserves the source, and older indexes without optional recovery fields load.

All 4 custom bundles and the separate replica candidate built and passed their executable configuration diagnostics and strict ad-hoc signatures on the qualification host. Plus opens a new idle recorder expanded; Replica applies its existing appearance preference. Their changed native paths still need current-package observation. Clean exported-checkout results are recorded below; no binary qualification follows from unit tests or packaging.

The previous baseline and synthetic file-fed ASR results below are retained 23 October evidence for unchanged code; they were not redundantly rerun locally. These notes do not claim microphone, VoiceOver, faithful signed-in commercial workflows, notarisation or general accuracy acceptance.

23 October2026. Qualification host: Apple Silicon arm64, macOS27.0.1, Swift6.4, full Xcode. Deployment target macOS14; older OS/Intel runtime unverified.

| Check | Executed result | Limits |
| --- | --- | --- |
| Shared storage/model/audio/edition tests |42 passed, zero failures | Synthetic temporary-directory/process fixtures; no microphone |
| Pinned upstream comparison tests |141 tests, one optional real-engine test skipped, zero failures | Additional file-fed engine result recorded separately when run |
| Four app packages |All four built; deep strict ad-hoc signatures verified | Not Developer ID signed/notarised |
| Comparison package |Built; licence notices and ad-hoc signature verified | Optional provenance comparison, not one of the four product variants |
| Earlier native Pip text workflow |Synthetic note create/edit/save, folder/tags, favourite, source quote observed | Precedes latest visible-action/folder/tag fixes and Plus controls |
| Actual microphone record/pause/resume/save |Pending | No grant changed during current qualification |
| Final four-variant native UI/accessibility |Pending | Dark/Oat, minimumwidth, keyboard, reducedmotion and VoiceOver need exact package evidence |
| Real local file-fed speech |Passed direct engine, packaged Pip CLI and comparison test with unchanged source hash |One synthetic voice/11.679s file; microphone/general accuracy separate |
| Clean public checkout |42 shared tests,141 comparison tests(one optional skip), all four and comparison packages passed |Fresh history/export; native acceptance separate |

The42-test suite includes original-audio preservation, corrected/original transcript separation, old-index compatibility, malformed-index preservation, safe atomic storage, concurrent writers, purge rollback/restart, draft recovery, retention/edit races, source-linked recall, worker cancellation/timeout/stale-result rejection, AVFoundation conversion, and safe crash-workspace cleanup. Cleanup preserves live speech children, uncertain launch states, reused/unknown PIDs, unmarked directories and symlinks. Edition tests cover isolated identities and composable Plus filters; Core ignores extras.

The pinned WhisperNotes original compiled in13.59s and passed127 original tests; its original packaging assertion failed on nested SwiftPM resources. The declared comparison repairs packaging and adds containment/collision/mirror-error tests. It preserves original source bytes and licence notices; this is not a claim that the original script passed.

Three independent technical/UI/release reviews found and drove fixes. A later independent Plus source review found active-recording presentation and filter-empty copy issues; final corrected source passed the42-test package checkpoint. Source review is distinct from rendered/native acceptance.

Most Mem/Voicenotes workflows remain documented. Direct native observation of Voicenotes for Mac 2.3.7 build 102 confirms only Home → bundled Welcome example detail → Back to Home; recording, upload/transcription and generative workflows were not exercised. Complete competitor equivalence, human transcription accuracy, network isolation tracing, full VoiceOver, macOS14/Intel and stable release readiness remain unverified.

## Pinned speech integration

whisper.cpp231638a0717b7822784297e5980965ffcec05810 and MIT ggml-small.bin SHA2561be3a9b2063867b937e64e2ec7483364a79917e157fa98c5d94b5c1fffea987b ran locally with Metal. Same16kHz mono WAV in all three paths; input SHA256ef708e53b4096be5ee2faa90c064fe7fd2a201ff7a37f9695ee9fff99ce01fe2 remained unchanged. Direct and Pip text matched exactly in this fixture; review retained Alice Morgan, negation, £19.50, meeting number2,10:30 and Friday correctly. Pip produced two valid timestamped segments. The optional comparison RealEngineTests also passed when configured with the same files.

| Invocation | Wall seconds | Reported maximum RSS bytes |
| --- | ---: | ---: |
| 05-direct-engine |32.06 |895336448 |
| 06-packaged-pip-cli |20.32 |902447104 |
| 07-baseline-real-engine-test |9.15 |893190144 |

Metrics are raw `/usr/bin/time -l` invocation reports on a shared host. Warmup, concurrency and different thread defaults prevent comparative speed claims. Wrapper CPU time is not a full child/GPU energy measurement. Energy and real microphone resource use remain unmeasured. Child jobs finished and the shared model hash was unchanged.

## Qualification patch2 / separate replica

Final Core 0.1.0-alpha.2 and Plus 0.2.0-alpha.2 source passed42shared tests. All four packages passed signature verification and their own non-UI configuration diagnostic, checking actual name/bundleID/storage/version/theme/extras flags. The separate Capture Replica 0.1.0-alpha.1 also built and passed signature/configuration checks with com.pipreps.capture.replica and its own Capture Replica storage folder. These are executable bundle checks, not native UI acceptance.

The last native slice exercised alpha1 Pip Plus tagfilter, idle recorder collapse and CmdOptionR expansion, and Pip Core tag editing/CmdS save. No microphone started. It exposed selected-row contrast under a purple macOS accent. Patch2 corrects focused/unfocused text colors in source; its final rendered contrast is pending. Computer-use disconnected while opening Settings and failed to reconnect after a reset, so neutral/replica, dark/Oat, minimumwidth and remaining assistive/native workflows remain unverified. Owned apps were stopped and no new grants were requested. Downloadable binary release is withheld pending this UI gate; source remains experimental.

One63-sample Plus navigation segment reported median0% CPU with a43.7% launch/interaction peak and maximum154144KiB RSS. This mixes startup/interaction/idle; it is not a recording/energy benchmark or efficiency claim. Core samples were interrupted and are not reported.


## Clean candidate export — 24 October 2026

A clean exported checkout at `18c8534bdf291f62a116143c5afae1a76c851f57` passed all 49 shared tests (zero failures/skips) and built all four packages. Every package passed strict ad-hoc signature verification and its executable configuration diagnostic. These checks ran on 24 October 2026; subsequent evidence-only documentation changes do not alter the tested source. Native UI, microphone, reference fidelity and downloadable binary qualification remain pending.
