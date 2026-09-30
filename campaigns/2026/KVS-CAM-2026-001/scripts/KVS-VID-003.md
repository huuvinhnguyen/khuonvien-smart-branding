# KVS-VID-003 — Khi PIR phát hiện, server nhận gì?

## Objective
Cho người xem thấy event từ thiết bị đi vào backend như thế nào, tập trung vào bằng chứng thật thay vì mô tả mơ hồ.

## Target length
45–55 giây, dọc 9:16.

## Core message
PIR chỉ tạo trigger ở device; ESP gửi request/event lên backend, backend nhận và xử lý theo logic hệ thống.

## Hook
**“PIR vừa báo chuyển động — server thật sự nhận được gì?”**

## Script / EDL

### 0:00–0:04 — Hook
**Visual:** cảnh PIR detect + cắt nhanh sang backend log.
**VO:** “PIR vừa báo chuyển động — server thật sự nhận được gì?”
**On-screen:** `PIR → Server: có gì bên trong?`

### 0:04–0:11 — Event leaves device
**Visual:** ESP/PIR + serial log `sending trigger`.
**VO:** “Ở device, khi PIR chuyển LOW sang HIGH, ESP gọi API trigger với device ID.”
**On-screen:** `sendTrigger(deviceId)`

### 0:11–0:19 — Server receives
**Visual:** Rails log/request log hoặc endpoint thật, crop phần nhạy cảm.
**VO:** “Backend nhận request, xác định thiết bị gửi sự kiện và chạy logic xử lý phía server.”
**On-screen:** `Device event → Backend`

### 0:19–0:29 — What the backend should know
**Visual:** diagram đơn giản: device ID / event type / received time.
**VO:** “Về mặt dữ liệu, mình cần tối thiểu biết thiết bị nào gửi, loại sự kiện gì và server nhận lúc nào.”
**On-screen:** `Device • Event • Time`

### 0:29–0:39 — Why backend matters
**Visual:** backend/dashboard + action path.
**VO:** “Điểm quan trọng là từ đây motion không còn chỉ là tín hiệu điện. Nó trở thành một software event để mình có thể lưu, kiểm tra hoặc kích hoạt action.”
**On-screen:** `Physical event → Software event`

### 0:39–0:47 — Proof
**Visual:** request log thật + dashboard/event record nếu có.
**VO:** “Mình ưu tiên nhìn log thật và record thật để biết hệ thống đang chạy đúng đến đâu.”
**On-screen:** `Proof > Assumption`

### 0:47–0:53 — CTA
**Visual:** Server → Relay/Buzzer.
**VO:** “Video tiếp theo: từ event này, server có thể kích hoạt relay hoặc buzzer như thế nào?”
**On-screen:** `Tiếp theo: Server → Action`

## Required footage
- PIR/ESP trigger thực tế.
- Serial log có `sending trigger`.
- Rails/backend request log thực tế.
- Dashboard hoặc DB/event record nếu đã có.
- Diagram đơn giản, không lộ IP/token/device secret.

## Proof/source
- Firmware gọi `AppApi::sendTrigger(App::getDeviceId())` ở rising edge.
- Backend KhuonVien đã có API/device processing; chỉ dùng trường dữ liệu nào đã xác minh trên log/code thật khi quay.

## Claims to avoid
- Không bịa payload nếu chưa quay/fetch code endpoint chính xác.
- Không nói server lưu toàn bộ motion history nếu implementation hiện tại chưa xác minh.
- Không hứa realtime/latency cụ thể.
- Che IP, token, cookie, credential và identifier nhạy cảm.

## Handoff
Next owner: Production.
Before filming server screen, verify the current endpoint/log fields and redact sensitive data.