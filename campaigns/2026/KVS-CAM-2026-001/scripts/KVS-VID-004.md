# KVS-VID-004 — Từ server kích hoạt relay/buzzer ra sao?

## Objective
Giải thích phần Action trong flow KhuonVien Smart: sau khi backend có event, hệ thống có thể gửi lệnh đến thiết bị để bật relay/buzzer.

## Target length
45–55 giây, dọc 9:16.

## Core message
Một event chỉ hữu ích khi nó có thể dẫn đến action phù hợp. Trong prototype KhuonVien Smart, backend có thể điều khiển device qua MQTT/command flow đã có.

## Hook
**“Server biết có chuyển động rồi — vậy làm sao để một thiết bị ngoài vườn phản ứng?”**

## Script / EDL

### 0:00–0:04 — Hook
**Visual:** backend event → buzzer/relay bật.
**VO:** “Server biết có chuyển động rồi — vậy làm sao để một thiết bị ngoài vườn phản ứng?”
**On-screen:** `Event → Action`

### 0:04–0:12 — Decision point
**Visual:** simple rule diagram: event → condition → action.
**VO:** “Backend không nhất thiết phải bật gì ngay. Trước hết mình cần rule: sự kiện nào thì action nào.”
**On-screen:** `Event → Rule → Action`

### 0:12–0:21 — Command path
**Visual:** Rails/backend → MQTT → ESP/relay.
**VO:** “Khi rule được thỏa, backend gửi command tới device. Hệ thống hiện tại đã có luồng MQTT để điều khiển relay.”
**On-screen:** `Server → MQTT → Device`

### 0:21–0:31 — Device executes
**Visual:** relay board/buzzer thực tế bật; giữ audio click/beep nếu rõ.
**VO:** “Device nhận command rồi đổi trạng thái relay hoặc kích hoạt buzzer theo action đã chọn.”
**On-screen:** `Command received → Output ON`

### 0:31–0:40 — Keep it observable
**Visual:** MQTT log / relay state / dashboard.
**VO:** “Mình cũng muốn hệ thống ghi nhận trạng thái sau action để có thể kiểm tra thiết bị đã phản ứng như thế nào.”
**On-screen:** `Action cần quan sát được`

### 0:40–0:48 — Prototype framing
**Visual:** toàn cảnh prototype wiring.
**VO:** “Đây vẫn là prototype. Mục tiêu hiện tại là kiểm tra end-to-end flow, chưa phải khẳng định độ tin cậy thương mại.”
**On-screen:** `Prototype / Experiment`

### 0:48–0:54 — CTA
**Visual:** Sensor → Server → Action → Data.
**VO:** “Bước tiếp theo mình sẽ mở phần history để xem những event này được theo dõi như thế nào.”
**On-screen:** `Tiếp theo: Event History`

## Required footage
- Backend/action trigger screen.
- MQTT command/log thật.
- Relay hoặc buzzer thật.
- ESP/device receiving command.
- Dashboard/state nếu có.

## Verified technical source
Current KhuonVien backend/device flow includes MQTT topics and relay actions, including `<chip_id>/switchon` and `<chip_id>/switchon/relay`, plus Rails services/jobs for relay switching.

## Claims to avoid
- Không nói action chắc chắn do đúng PIR event nhìn thấy trên video nếu chưa quay cùng một end-to-end test.
- Không hứa latency, uptime hoặc reliability.
- Không gọi đây là security/alarm system certified.
- Nếu dùng buzzer chỉ xem là example action.

## Handoff
Next owner: Production.
Prefer one real end-to-end take where log timestamps make causality easy to verify.