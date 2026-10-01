# KVS-VID-002 — PIR phát hiện chuyển động như thế nào?

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Primary audience
Home & garden owner — tech-curious

## Pain point
Muốn biết khi có chuyển động trong vườn/khuôn viên nhưng không hiểu cảm biến thực sự phát hiện gì và dễ nhầm PIR với camera/AI nhận diện.

## Desired outcome
Sau video, người xem hiểu PIR chỉ tạo ra tín hiệu chuyển động và đó là điểm bắt đầu để KhuonVien biến một sự kiện ngoài đời thành automation.

## Brand pillar
- Observe Your Space
- Practical Automation
- Build & Improve

## Objective
Giải thích ngắn gọn cách PIR tham gia vào flow KhuonVien và làm rõ rằng PIR phát hiện thay đổi bức xạ hồng ngoại trong vùng quan sát, không xác định chính xác người hay vật.

## Audience insight
Người xem thường thấy cảm biến PIR trong đèn/camera nhưng không biết nó thực sự gửi gì và vì sao một tín hiệu HIGH/LOW đã đủ để bắt đầu một workflow automation.

## Hook
“Cảm biến này có thật sự biết có người đi vào vườn không?”

## Key message
PIR không “nhận diện ai”. Trong prototype hiện tại, firmware đọc trạng thái PIR và chỉ gửi trigger khi trạng thái chuyển từ LOW → HIGH. Đây là bước đầu tiên trong flow **Sự kiện → Thiết bị → Tự động hóa**.

## Proof / source
- Firmware hiện tại đọc `digitalRead(pinPir2)`.
- Chỉ gọi `AppApi::sendTrigger(App::getDeviceId())` khi `pirState && !previousPirState`.
- Polling hiện tại khoảng 500 ms.

## Story structure
1. Problem: muốn biết khi có chuyển động trong vườn.
2. Experiment: dùng PIR.
3. Explain: LOW → HIGH = trigger edge.
4. Result: trigger được gửi về hệ thống.
5. Lesson: sensor tạo tín hiệu; device/server mới quyết định xử lý tiếp thế nào.

## Required footage
- Cận cảnh module PIR đang dùng.
- Người/vật đi qua vùng cảm biến.
- Serial log có dòng `PIR detected, sending trigger`.
- Một shot code/firmware ngắn, crop chỉ phần LOW → HIGH logic.
- Nếu có thể: LED/indicator hoặc dashboard phản hồi sau trigger.

## On-screen text candidates
- `PIR không nhận diện người`
- `LOW → HIGH = Trigger`
- `Sensor → Device`
- `Sự kiện ngoài đời → Event phần mềm`

## CTA
“Video sau mình sẽ cho xem trigger này đi vào server như thế nào.”

## Risks / claims to avoid
- Không nói PIR biết “người”, “trộm”, “chó” hay object identity.
- Không claim độ chính xác, khoảng cách, latency hoặc reliability nếu chưa đo.
- Không nói mọi PIR đều hoạt động giống hệt implementation hiện tại.

## Handoff to Script Writer
Viết script 35–50 giây, giọng Friendly + Practical + Technical but accessible. Mở bằng vấn đề thực tế, không mở bằng tên linh kiện. Phải dùng wording chính xác: PIR phát hiện thay đổi bức xạ hồng ngoại/chuyển động trong vùng cảm biến; prototype hiện tại gửi trigger ở cạnh LOW → HIGH.