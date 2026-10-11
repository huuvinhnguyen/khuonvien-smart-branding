# KVS-VID-003 — Khi PIR phát hiện, server nhận gì?

## Status
READY FOR PRODUCTION

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Primary audience
DIY / maker / developer — secondary reach: tech-curious home & garden owner

## Target length
45–55 giây, dọc 9:16.

## Core message
PIR chỉ tạo trigger ở device. Khi firmware phát hiện cạnh LOW → HIGH, ESP gửi event/request về backend. Server nhận event đó, xác định thiết bị gửi và tiếp tục xử lý theo logic hệ thống. Đây là bước biến một chuyển động ngoài đời thành một software event có thể quan sát và tự động hóa.

## Hook
**“PIR vừa báo chuyển động — server thật sự nhận được gì?”**

## Script / EDL

### 0:00–0:04 — Hook
**Visual:** cảnh PIR detect thật, cut rất nhanh sang terminal/backend log vừa xuất hiện request.

**VO:** “PIR vừa báo chuyển động — server thật sự nhận được gì?”

**On-screen:** `PIR → Server: có gì bên trong?`

**Edit note:** 2 cut trong 4 giây đầu. Có thể dùng sound effect ngắn khi chuyển từ PIR sang log. Không mở đầu bằng code.

---

### 0:04–0:11 — Event leaves the device
**Visual:** PIR + ESP, rồi serial log `PIR detected, sending trigger`. Chèn crop ngắn đoạn firmware gọi `sendTrigger`.

**VO:** “Ở device, khi PIR chuyển từ LOW sang HIGH, ESP xem đó là một event mới và gọi API trigger lên server.”

**On-screen:** `LOW → HIGH = sendTrigger(deviceId)`

**Code proof:**
```cpp
if (pirState && !previousPirState) {
  Serial.println("PIR detected, sending trigger");
  AppApi::sendTrigger(App::getDeviceId());
}
```

**Edit note:** code chỉ xuất hiện 1–2 giây; highlight `sendTrigger`, không để người xem phải đọc cả block.

---

### 0:11–0:19 — Backend receives the request
**Visual:** Rails/backend request log thật. Zoom/crop vào method/path/status hoặc log liên quan tới trigger. Che IP, token, cookie, credential và identifier không cần thiết.

**VO:** “Backend nhận request, biết thiết bị nào vừa gửi sự kiện, rồi chuyển event đó vào logic xử lý phía server.”

**On-screen:** `Device event → Backend`

**Optional lower-third:** `ESP → API → Rails`

**Edit note:** nếu log có HTTP 200, có thể highlight ngắn `200 OK` như proof request đã tới server; không suy diễn rằng toàn bộ downstream action đã thành công chỉ từ 200.

---

### 0:19–0:28 — What the server needs to know
**Visual:** graphic đơn giản ba ô: Device / Event / Time. Nếu code/log thật có các field tương ứng thì dùng field thật; nếu chưa verify, chỉ dùng conceptual labels.

**VO:** “Tối thiểu, phía server cần biết event đến từ thiết bị nào, chuyện gì vừa xảy ra và thời điểm server nhận được nó.”

**On-screen:** `Device • Event • Time`

**Edit note:** đây là phần giải thích khái niệm. Không bịa JSON payload hay field name chưa xác minh trong source/log.

---

### 0:28–0:38 — Physical event becomes software event
**Visual:** motion/PIR ở trái → arrow → backend/event ở giữa → các action khả dĩ ở phải: log / relay / buzzer. Dùng graphic đơn giản, không mô phỏng quá nhiều.

**VO:** “Từ đây, motion không còn chỉ là tín hiệu điện ở cảm biến. Nó trở thành một software event để KhuonVien có thể ghi nhận, kiểm tra hoặc dùng cho automation tiếp theo.”

**On-screen:** `Physical event → Software event`

**Secondary text:** `Observe → Decide → Act`

**Edit note:** nếu việc lưu history chưa được verify cho đúng event này, dùng wording “có thể ghi nhận” thay vì khẳng định “đã lưu history”.

---

### 0:38–0:46 — Show proof, not assumption
**Visual:** quay lại request log thật. Nếu có record/dashboard tương ứng đã verify cùng event thì show tiếp. Nếu chưa có record thật, chỉ giữ backend log.

**VO:** “Mình ưu tiên nhìn log thật và record thật, vì như vậy mới biết chính xác flow đang chạy tới đâu.”

**On-screen:** `Proof > Assumption`

**Edit note:** nếu không chứng minh được causal chain giữa log và dashboard record thì không dựng như thể chúng là cùng một event.

---

### 0:46–0:53 — CTA / Series handoff
**Visual:** graphic `PIR → ESP → Server → Relay/Buzzer`, highlight phần `Server → Action`.

**VO:** “Nhận được event rồi, server sẽ làm gì tiếp? Video sau mình thử kích hoạt relay hoặc buzzer từ chính flow này.”

**On-screen:** `Tiếp theo: Server → Action`

**End card:** `KhuonVien — Build in Public`

---

## Full voice-over

“PIR vừa báo chuyển động — server thật sự nhận được gì?

Ở device, khi PIR chuyển từ LOW sang HIGH, ESP xem đó là một event mới và gọi API trigger lên server.

Backend nhận request, biết thiết bị nào vừa gửi sự kiện, rồi chuyển event đó vào logic xử lý phía server.

Tối thiểu, phía server cần biết event đến từ thiết bị nào, chuyện gì vừa xảy ra và thời điểm server nhận được nó.

Từ đây, motion không còn chỉ là tín hiệu điện ở cảm biến. Nó trở thành một software event để KhuonVien có thể ghi nhận, kiểm tra hoặc dùng cho automation tiếp theo.

Mình ưu tiên nhìn log thật và record thật, vì như vậy mới biết chính xác flow đang chạy tới đâu.

Nhận được event rồi, server sẽ làm gì tiếp? Video sau mình thử kích hoạt relay hoặc buzzer từ chính flow này.”

## Subtitle copy

1. PIR vừa báo chuyển động — server thật sự nhận được gì?
2. Khi PIR chuyển LOW → HIGH, ESP xem đó là một event mới.
3. ESP gọi API trigger lên server.
4. Backend nhận request và xác định thiết bị gửi sự kiện.
5. Server tiếp tục đưa event vào logic xử lý.
6. Tối thiểu cần biết: Device • Event • Time.
7. Motion lúc này đã trở thành một software event.
8. Event đó có thể được ghi nhận, kiểm tra hoặc dùng cho automation.
9. Mình ưu tiên log thật và record thật — Proof > Assumption.
10. Tiếp theo: Server → Relay/Buzzer.

## Production shot list

### Must-have
1. PIR thật phát hiện chuyển động.
2. ESP/PIR trong cùng frame hoặc một cut cho thấy hardware đang chạy.
3. Serial log có dòng `PIR detected, sending trigger`.
4. Firmware crop có `AppApi::sendTrigger(App::getDeviceId())`.
5. Rails/backend request log thật khi trigger tới server.
6. Graphic đơn giản `PIR → ESP → API → Server`.
7. Graphic kết `Server → Relay/Buzzer`.

### Nice-to-have
8. Endpoint/controller/service nhận trigger đã crop an toàn.
9. Record/database/dashboard tương ứng với event nếu causal chain đã verify.
10. Shot màn hình server trước/sau request để tăng cảm giác “proof”.

## Screen-record checklist
- Font terminal đủ lớn để đọc trên điện thoại.
- Chỉ giữ 1–3 dòng log quan trọng trong crop.
- Ẩn IP public nếu không cần thiết.
- Ẩn token, Authorization header, cookie, session, password, secret key.
- Ẩn identifier nhạy cảm nếu có.
- Không để notification/email/chat riêng tư lọt vào screen recording.
- Dùng dummy/blur nếu phải quay phần cấu hình.

## Editing notes
- Format: 1080 × 1920, 9:16.
- Hook phải xong trong 4 giây đầu.
- Nhịp cut khoảng 1.5–3 giây/cảnh ở đoạn đầu.
- Code không nên chiếm màn hình quá 2 giây mỗi lần.
- Subtitle tối đa khoảng 2 dòng; ưu tiên từ khóa ngắn.
- Highlight các từ: `LOW → HIGH`, `sendTrigger`, `Backend`, `Software event`.
- Không dùng animation kiểu “AI scanning”.
- Nhạc nền nhỏ hơn VO rõ rệt.
- Sound effect chỉ dùng để nhấn transition PIR → log và Server → Action.
- End card 1–1.5 giây là đủ.

## Suggested on-screen visual language
- `PIR → ESP → API → Server`
- `LOW → HIGH = New Event`
- `Device • Event • Time`
- `Physical event → Software event`
- `Proof > Assumption`
- `Server → Relay/Buzzer`

## Verified technical source
Firmware rising-edge flow:

```cpp
bool pirState = digitalRead(pinPir2) == HIGH;
if (pirState && !previousPirState) {
  Serial.println("PIR detected, sending trigger");
  AppApi::sendTrigger(App::getDeviceId());
}
previousPirState = pirState;
delay(500);
```

This video should only show backend fields, payload shape, response data, persistence behavior, or downstream actions that have been verified from current code/logs.

## Claims to avoid
- Không nói PIR nhận diện người/chó/mèo.
- Không nói trigger là motion-start/motion-end; current flow là rising-edge event.
- Không bịa JSON payload hoặc API field chưa xác minh.
- Không nói server lưu toàn bộ motion history nếu implementation chưa verify.
- Không claim realtime tuyệt đối, latency cụ thể hoặc SLA.
- Không claim 100% event delivery.
- Không gọi đây là hệ thống an ninh.
- Không suy ra relay/buzzer đã chạy chỉ vì request trả HTTP 200.

## Caption draft — Facebook / TikTok

PIR phát hiện chuyển động rồi — nhưng phía server thực sự nhận được gì?

Trong prototype KhuonVien, khi tín hiệu PIR chuyển từ LOW → HIGH, ESP tạo một event mới và gửi trigger về backend. Từ đây, một chuyển động ngoài đời đã trở thành software event để hệ thống có thể quan sát và xử lý tiếp.

Mình ưu tiên show log thật và flow thật thay vì chỉ mô tả trên sơ đồ.

Video tiếp theo: từ event này, server kích hoạt relay hoặc buzzer như thế nào?

#KhuonVien #IoT #ESP32 #PIR #Rails #Automation #SmartGarden

## Suggested cover text
**PIR báo chuyển động  
SERVER NHẬN GÌ?**

Small label: `ESP → API → Rails`

## Handoff
**Next owner: Production**

Before filming:
1. Trigger PIR thật.
2. Capture serial log.
3. Capture the matching Rails/backend request.
4. Verify which fields are actually received.
5. Redact sensitive data.
6. If a matching DB/dashboard record exists, verify causal link before using it.
