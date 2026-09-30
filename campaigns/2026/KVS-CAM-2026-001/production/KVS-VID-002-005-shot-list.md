# KVS-VID-002–005 Production Shot List

## Goal
Quay một batch footage đủ dùng cho 4 video tiếp theo, ưu tiên footage thật, dễ quay, có thể tái sử dụng giữa các video.

## Existing footage that can be reused
- Garden / animal movement: `IMG_8731.mp4`, `IMG_7890.mp4`, `IMG_5629.mp4`
- PIR / prototype / buzzer: `IMG_8830.mp4`, `IMG_8832.mp4`, `IMG_8828.jpeg`, `IMG_2291ACF1-D1DE-4C89-A967-4BD5639DAC4D.jpeg`
- PIR dashboard history: `66327107d37c47f382787127f497a4bb.mp4`

Do not reuse any frame that exposes private IDs, IPs, tokens, credentials or unrelated private UI.

## Missing footage to shoot

### A. PIR sensor behavior
Use for: KVS-VID-002, KVS-VID-003

1. Wide shot: PIR installed in the real garden context — 5–8s
2. Medium shot: person walks across PIR field — 5–8s
3. Close-up: PIR module / sensor lens — 4–6s
4. Device reaction shot: ESP serial / indicator / physical device at the moment motion is triggered — 5–8s
5. Optional controlled demo: enter frame, trigger, leave frame, trigger again — 10–15s

### B. Device → server event
Use for: KVS-VID-003

6. Screen recording of backend receiving one trigger event — 8–12s
7. Screen recording of the relevant Rails log/API request line — 5–8s
8. Optional code shot showing LOW→HIGH logic and `sendTrigger(...)` — 5–8s

Rules:
- Blur/hide device IDs, IPs, auth data, tokens.
- Show only the minimum technical detail needed to prove the flow.

### C. Server → action
Use for: KVS-VID-004

9. Wide/medium shot of buzzer or relay device before action — 4–6s
10. Action shot: buzzer activates or relay changes state — 5–8s
11. Screen recording of action command/event in backend or MQTT-related UI/log — 6–10s
12. Optional side-by-side / sequential proof shot: trigger → backend → action — 8–12s

Important claim guardrail:
Do not imply exact causality between a visible PIR movement and a buzzer sound unless that exact run is verified on camera. Safer framing: the system can use a received event to trigger an action such as buzzer/relay.

### D. Dashboard / history
Use for: KVS-VID-005

13. Clean screen recording of motion history list — 8–12s
14. Scroll/filter by time if available — 8–12s
15. Detail shot of one history row/event — 5–8s
16. Wider dashboard overview — 5–8s

Rules:
- Keep only real fields that currently exist.
- Do not imply advanced analytics, object classification, reliability, or notification features unless actually implemented and shown.

## Batch shooting order
To minimize setup changes:

1. Garden context + PIR movement shots
2. PIR/device closeups
3. Buzzer/relay action shots
4. Backend/API/log screen recordings
5. Dashboard/history screen recordings

## Camera / capture settings
- Vertical 9:16 whenever possible
- 1080×1920 target
- 30 fps
- Lock exposure/focus if practical
- Keep each useful take at least 5 seconds
- Leave 1–2 seconds before and after the action for editing
- Avoid digital zoom and fast camera movement
- Capture natural device sound for action shots

## Minimum acceptable production package
If time is limited, capture these 8 items first:

1. PIR installed in garden
2. Person crossing PIR field
3. PIR/device close-up
4. One clean backend trigger event recording
5. One code/log proof shot
6. Buzzer/relay activation shot
7. Motion history screen recording
8. Dashboard overview

## File naming
Recommended:
- `KVS-VID-002_PIR-Wide_T01.mp4`
- `KVS-VID-002_PIR-Close_T01.mp4`
- `KVS-VID-003_Server-Trigger_T01.mp4`
- `KVS-VID-004_Buzzer-Action_T01.mp4`
- `KVS-VID-005_History_T01.mp4`

For shared shots use:
- `KVS-BATCH-002-005_<shot-name>_T01.mp4`

## Handoff to Editor
Production is ready for Editor when:
- each of the 4 videos has enough visual proof for its core message;
- missing shots are explicitly noted;
- sensitive technical data is hidden;
- filenames are recognizable;
- raw files are uploaded to the campaign raw-footage folder;
- the Production task includes the Drive folder/link and any caveats.
