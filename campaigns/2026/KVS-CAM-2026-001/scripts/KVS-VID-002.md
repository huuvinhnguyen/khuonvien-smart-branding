# KVS-VID-002 — PIR phát hiện chuyển động như thế nào?

## Status
READY FOR PRODUCTION

## Primary audience
Home & garden owner — tech-curious

## Target length
45–55 giây, dọc 9:16.

## Core message
PIR không “nhìn thấy” hay nhận diện người/vật như camera. Trong prototype KhuonVien hiện tại, thiết bị chỉ tạo trigger khi tín hiệu PIR chuyển từ LOW → HIGH. Đây là cách một chuyển động ngoài đời trở thành event để hệ thống xử lý tiếp.

## Hook
**“Nếu có chuyển động ngoài vườn khi mình không ở đó, cảm biến thực sự biết được gì?”**

## Script / EDL

### 0:00–0:05 — Real problem / Hook
**Visual:** góc vườn/khuôn viên, một người đi ngang; cut nhanh sang PIR.

**VO:** “Nếu có chuyển động ngoài vườn khi mình không ở đó, cảm biến này thực sự biết được gì?”

**On-screen:** `Có chuyển động ngoài vườn → hệ thống biết bằng cách nào?`

### 0:05–0:12 — Clarify
**Visual:** cận PIR, tránh làm visual giống camera nhận diện.

**VO:** “Nó không biết đó là người, chó hay mèo. PIR chỉ phát hiện sự thay đổi bức xạ hồng ngoại trong vùng cảm biến.”

**On-screen:** `PIR ≠ Camera / AI nhận diện`

### 0:12–0:20 — Device reads the signal
**Visual:** PIR nối ESP; có thể chèn đoạn code `digitalRead` rất ngắn.

**VO:** “Trong prototype KhuonVien, ESP kiểm tra trạng thái PIR khoảng mỗi nửa giây.”

**On-screen:** `PIR → ESP`

### 0:20–0:29 — Rising edge
**Visual:** animation LOW → HIGH + serial log.

**VO:** “Khi tín hiệu chuyển từ LOW sang HIGH, thiết bị xem đó là một sự kiện mới và gửi một trigger lên server.”

**On-screen:** `LOW → HIGH = 1 Trigger`

### 0:29–0:37 — Why this matters
**Visual:** HIGH giữ vài giây; animation chỉ hiện một event.

**VO:** “PIR có thể giữ trạng thái HIGH một lúc, nhưng mình không muốn thiết bị gửi cùng một event lên server liên tục.”

**On-screen:** `Không spam event khi tín hiệu vẫn HIGH`

### 0:37–0:47 — Result
**Visual:** serial log `PIR detected, sending trigger`, sau đó cut sang server/dashboard nếu có footage đã verify.

**VO:** “Vậy là một chuyển động ngoài đời đã được biến thành một event phần mềm để KhuonVien có thể ghi nhận hoặc tự động xử lý tiếp.”

**On-screen:** `Sự kiện ngoài đời → Event phần mềm`

### 0:47–0:53 — CTA / Series handoff
**Visual:** graphic đơn giản `PIR → ESP → Server`.

**VO:** “Video tiếp theo mình sẽ mở xem chính xác server nhận event này như thế nào.”

**On-screen:** `Tiếp theo: ESP → Server`

## Production shot list
1. Wide shot khu vườn/khuôn viên có người đi ngang.
2. Close-up PIR thật đang sử dụng.
3. PIR + ESP + dây kết nối.
4. Terminal serial log có `PIR detected, sending trigger`.
5. Code crop chỉ phần `pirState && !previousPirState`.
6. Optional: server/dashboard nhận event nếu causal chain đã verify.
7. Simple graphic: `PIR → ESP → Server`.

## Editing notes
- 3–5 giây đầu phải ưu tiên vấn đề ngoài đời, chưa cần nói ESP/MQTT/API.
- Không để code chiếm màn hình quá lâu; code chỉ là proof.
- Highlight `LOW → HIGH` trực quan bằng animation đơn giản.
- Nếu dashboard/server footage chưa chắc cùng một event, không dựng theo kiểu khẳng định causal chain.
- Subtitle dùng ngôn ngữ phổ thông; technical label chỉ xuất hiện khi visual hỗ trợ.

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
- Không gọi đây là hệ thống an ninh.
- Không nói trigger tương đương “motion start/motion end”; implementation hiện tại chỉ gửi rising-edge event.

## Handoff
**Next owner: Production**

Production cần quay footage PIR thật + serial-log proof. Sau khi footage đủ, handoff sang Editor.