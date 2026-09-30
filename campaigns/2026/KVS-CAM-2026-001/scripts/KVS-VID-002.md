# KVS-VID-002 — PIR phát hiện chuyển động như thế nào?

## Objective
Giải thích dễ hiểu cách cảm biến PIR trong prototype KhuonVien Smart phát hiện chuyển động và tạo trigger cho hệ thống.

## Target length
45–55 giây, dọc 9:16.

## Core message
PIR không “nhìn thấy” người hay con vật như camera. Trong prototype hiện tại, thiết bị đọc trạng thái PIR và chỉ gửi trigger khi tín hiệu chuyển từ LOW → HIGH.

## Hook
**“Cảm biến này có biết ai đang đi ngang qua không?”**

## Script / EDL

### 0:00–0:04 — Hook
**Visual:** cận cảnh PIR + một chuyển động đi ngang vùng cảm biến.
**VO:** “Cảm biến này có biết ai đang đi ngang qua không?”
**On-screen:** `PIR có nhận diện được ai không?`

### 0:04–0:10 — Clarify the misconception
**Visual:** PIR đặt trong vườn, xen cảnh camera nếu có.
**VO:** “Không. PIR không nhận diện người, chó hay mèo. Nó chỉ báo khi phát hiện thay đổi bức xạ hồng ngoại trong vùng cảm biến.”
**On-screen:** `PIR ≠ Camera`

### 0:10–0:18 — Device logic
**Visual:** ESP + PIR, quay dây kết nối/GPIO; có thể chèn code ngắn.
**VO:** “Ở prototype của mình, ESP đọc trạng thái PIR khoảng mỗi nửa giây.”
**On-screen:** `PIR → GPIO → ESP`

### 0:18–0:27 — Rising edge
**Visual:** animation đơn giản LOW → HIGH hoặc terminal/log thực tế.
**VO:** “Khi trạng thái chuyển từ LOW sang HIGH, mình xem đó là một sự kiện mới và gửi trigger lên server.”
**On-screen:** `LOW → HIGH = Trigger`

### 0:27–0:37 — Why not send continuously
**Visual:** minh họa HIGH giữ vài giây nhưng chỉ một event được gửi.
**VO:** “Như vậy khi PIR giữ HIGH trong vài giây, thiết bị không spam server liên tục.”
**On-screen:** `1 lần chuyển trạng thái → 1 trigger`

### 0:37–0:46 — Result
**Visual:** log `PIR detected, sending trigger` + server/dashboard nhận event nếu quay được.
**VO:** “Kết quả là một chuyển động ngoài vườn được biến thành một sự kiện mà phần mềm có thể xử lý tiếp.”
**On-screen:** `Motion → Event`

### 0:46–0:52 — CTA
**Visual:** PIR → ESP → Server graphic.
**VO:** “Video tiếp theo mình sẽ mở đúng event server nhận được là gì.”
**On-screen:** `Tiếp theo: Server nhận gì?`

## Required footage
- PIR cận cảnh.
- Một người/vật đi ngang vùng cảm biến.
- ESP + dây PIR.
- Serial log thực tế.
- Nếu có thể: màn hình code chỉ đoạn LOW→HIGH trigger.

## Verified technical source
Prototype hiện tại dùng logic rising edge:

```cpp
bool pirState = digitalRead(pinPir2) == HIGH;
if (pirState && !previousPirState) {
  Serial.println("PIR detected, sending trigger");
  AppApi::sendTrigger(App::getDeviceId());
}
previousPirState = pirState;
delay(500);
```

## Claims to avoid
- Không nói PIR biết đó là người, thú, xe hay vật cụ thể.
- Không hứa độ chính xác, khoảng cách, latency hoặc chống false-positive nếu chưa đo.
- Không nói trigger tương đương “motion start/motion end”; prototype hiện tại chỉ gửi rising-edge event.

## Handoff
Next owner: Production.
Need to capture real PIR + serial-log proof before Editor.