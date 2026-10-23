# Test evidence

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
| Real local file-fed speech |In progress | No recognition quality claim before result inspection |
| Clean public checkout |Pending | Source export review alone is insufficient |

The42-test suite includes original-audio preservation, corrected/original transcript separation, old-index compatibility, malformed-index preservation, safe atomic storage, concurrent writers, purge rollback/restart, draft recovery, retention/edit races, source-linked recall, worker cancellation/timeout/stale-result rejection, AVFoundation conversion, and safe crash-workspace cleanup. Cleanup preserves live speech children, uncertain launch states, reused/unknown PIDs, unmarked directories and symlinks. Edition tests cover isolated identities and composable Plus filters; Core ignores extras.

The pinned WhisperNotes original compiled in13.59s and passed127 original tests; its original packaging assertion failed on nested SwiftPM resources. The declared comparison repairs packaging and adds containment/collision/mirror-error tests. It preserves original source bytes and licence notices; this is not a claim that the original script passed.

Three independent technical/UI/release reviews found and drove fixes. A later independent Plus source review found active-recording presentation and filter-empty copy issues; final corrected source passed the42-test package checkpoint. Source review is distinct from rendered/native acceptance.

Reference Mem/Voicenotes workflows remain documented rather than account-tested. Official Voicenotes2.3.7 was observed only at Welcome/sign-in; no signup or terms were accepted. Complete competitor equivalence, human transcription accuracy, network isolation tracing, full VoiceOver, macOS14/Intel and stable release readiness remain unverified.

## Pinned speech integration

whisper.cpp231638a0717b7822784297e5980965ffcec05810 and MIT ggml-small.bin SHA2561be3a9b2063867b937e64e2ec7483364a79917e157fa98c5d94b5c1fffea987b ran locally with Metal. Same16kHz mono WAV in all three paths; input SHA256ef708e53b4096be5ee2faa90c064fe7fd2a201ff7a37f9695ee9fff99ce01fe2 remained unchanged. Direct and Pip text matched exactly in this fixture; review retained Alice Morgan, negation, £19.50, meeting number2,10:30 and Friday correctly. Pip produced two valid timestamped segments. The optional comparison RealEngineTests also passed when configured with the same files.

| Invocation | Wall seconds | Reported maximum RSS bytes |
| --- | ---: | ---: |
| 05-direct-engine |32.06 |895336448 |
| 06-packaged-pip-cli |20.32 |902447104 |
| 07-baseline-real-engine-test |9.15 |893190144 |

Metrics are raw `/usr/bin/time -l` invocation reports on a shared host. Warmup, concurrency and different thread defaults prevent comparative speed claims. Wrapper CPU time is not a full child/GPU energy measurement. Energy and real microphone resource use remain unmeasured. Child jobs finished and the shared model hash was unchanged.
