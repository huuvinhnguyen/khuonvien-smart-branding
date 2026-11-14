# IOS-001 — SwiftUI State Management: What Actually Matters?

**Status:** Draft V1 — review needed; not filmed, edited, or published  
**Date:** 2026-11-14  
**Channel:** Personal LinkedIn (English)  
**Format:** 9:16, 60–90 seconds, English voice-over + English subtitles, optional no-face recording  
**Audience:** iOS engineers, tech leads, recruiters in Japan/internationally

## Goal
Show practical Senior iOS reasoning: a user action, a network request, and a real device's confirmed state are different things. Use KhuonVien Smart as an illustrative demo; **verify current code and actual device behavior before making implementation claims**.

## Core idea
A switch tap is a user intent, not proof the physical device changed state. Explicitly model idle, sending, confirmed and failed states; decide whether optimistic updates are appropriate and how to reconcile with the device's actual state.

## Voice-over V1 (English; ~70–85 sec)
"Most SwiftUI bugs aren't really about the view. They're about state.

Imagine a smart-home app. You tap a switch to turn on a light. The button changes immediately—but what if the network request fails? Is the light actually on?

That's why I separate user intent from confirmed device state.

The interface can show that a command is in progress, then update when the system confirms the result. If the request fails or times out, it should show a clear error and offer a safe way to retry.

In SwiftUI, the important question isn't just which property wrapper to use. It's who owns the state, what triggers a change, and what happens when asynchronous results arrive.

For KhuonVien Smart, this is a useful real-world scenario to demonstrate and test.

Good state management makes an app more predictable—not just more reactive."

## On-screen text / EDL
| Time | Visual / shot | On-screen text |
|---|---|---|
| 00:00–00:08 | SwiftUI switch UI close-up | Most SwiftUI bugs are about STATE |
| 00:08–00:23 | Diagram: tap → request → device confirmation | A tap ≠ a confirmed device state |
| 00:23–00:39 | UI states mock/demo: sending, confirmed, failed | Intent → Loading → Confirmed / Failed |
| 00:39–00:57 | SwiftUI/Xcode screen with state owner highlighted; blur secrets | Who owns the state? |
| 00:57–01:15 | iPhone and physical device in same frame, real demo if available | Predictable. Testable. Reliable. |

Timing is provisional; adjust to actual recorded voice-over. Do not present mocked failure states as real production behavior.

## Demo checklist (before recording)
- [ ] Inspect actual KhuonVien Smart iOS/Flutter implementation and identify state owner (do not assume SwiftUI is used in the current screen).
- [ ] Confirm whether app uses optimistic or device-confirmed UI updates.
- [ ] Reproduce successful ON/OFF action with physical device and visible phone.
- [ ] Check real timeout/error behavior; use a labeled conceptual diagram if it cannot be reproduced.
- [ ] Verify the explanation matches the actual architecture; do not claim unimplemented states.
- [ ] Hide keys, IPs, customer information and other secrets.
- [ ] Record English subtitles and verify terminology.

## Draft LinkedIn caption
"SwiftUI makes reactive interfaces easier to build, but state ownership is still an engineering decision. In an IoT app, a tap isn't the same as a confirmed device action. How do you handle pending commands, failures, and reconciliation in your apps? #SwiftUI #iOSDevelopment #SoftwareArchitecture #IoT"

## Next action
Review actual implementation and refine script; only then approve filming. No publication scheduled.
