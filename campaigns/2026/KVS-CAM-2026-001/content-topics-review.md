# KhuonVien Smart — Content Topics Review

> Checklist để duyệt các topic content mới sau khi tạm gác KVS-VID-003 → KVS-VID-005.

## Review status

- [x] KVS-VID-006 — Đi ngang → đèn hoặc buzzer bật
  - Hook: “Chỉ cần đi ngang qua đây, chuyện gì xảy ra?”
  - Visual: người đi qua → PIR detect → relay/buzzer chạy.
  - Mục tiêu: demo trực quan, không cần giải thích nhiều.
  - Độ khó quay: thấp.
  - Ưu tiên: Rất cao.

- [ ] KVS-VID-007 — PIR có phân biệt người và chó không?
  - Hook: “PIR có biết đây là người hay chó không?”
  - Nội dung: PIR không nhận diện đối tượng; chỉ phát hiện thay đổi bức xạ hồng ngoại.
  - Visual: người đi qua / thú đi qua / cảm biến.
  - Mục tiêu: educational, dễ hiểu.
  - Ưu tiên: Cao.

- [ ] KVS-VID-008 — Một PIR điều khiển nhiều thiết bị
  - Hook: “Một cảm biến có thể bật cùng lúc bao nhiêu thiết bị?”
  - Visual: PIR → đèn + buzzer + thiết bị khác.
  - Mục tiêu: cho thấy khả năng fan-out và tính linh hoạt của KhuonVien.
  - Ưu tiên: Rất cao.

- [ ] KVS-VID-009 — Quên tắt thiết bị ngoài vườn
  - Hook: “Ra khỏi nhà rồi mới nhớ chưa tắt thiết bị thì sao?”
  - Visual: điện thoại → app → relay OFF.
  - Mục tiêu: gắn IoT với vấn đề thực tế.
  - Ưu tiên: Cao.

- [ ] KVS-VID-010 — Thiết bị còn online không?
  - Hook: “Làm sao biết ESP ngoài vườn còn sống hay đã mất kết nối?”
  - Nội dung: giải thích last_seen / heartbeat bằng ngôn ngữ đơn giản.
  - Visual: device online → mất Wi-Fi → trạng thái thay đổi.
  - Mục tiêu: kỹ thuật nhưng thực tế.
  - Ưu tiên: Trung bình–cao.

- [ ] KVS-VID-011 — Hẹn giờ bật thiết bị
  - Hook: “6 giờ sáng mỗi ngày tự bật bơm trong 10 phút được không?”
  - Visual: đặt lịch → tới giờ → relay bật → tự tắt.
  - Mục tiêu: demo automation có giá trị sử dụng ngay.
  - Ưu tiên: Rất cao.

- [ ] KVS-VID-012 — Điều khiển thiết bị trong 10 giây
  - Hook: “Từ điện thoại đến thiết bị ngoài vườn chỉ cần thế này.”
  - Visual: mở app → nhấn ON → thiết bị chạy.
  - Format: 15–25 giây, ưu tiên TikTok/Reels.
  - Mục tiêu: demo ngắn, dễ xem.
  - Ưu tiên: Cao.

- [ ] KVS-VID-013 — Một bug IoT mình vừa gặp
  - Hook: “Con ESP này chạy lần đầu ngon, lần sau lại im luôn.”
  - Format: Bug → nguyên nhân → cách test → fix.
  - Có thể dùng case buzzer/cooldown, Wi-Fi hoặc MQTT.
  - Mục tiêu: Build in Public, tăng credibility với maker/developer.
  - Ưu tiên: Cao.

- [ ] KVS-VID-014 — PIR false trigger ngoài trời
  - Hook: “PIR ngoài vườn có tự báo nhầm không?”
  - Visual: test thực tế với người đi ngang, cây lay, thay đổi môi trường.
  - Mục tiêu: test thật, không phóng đại độ chính xác.
  - Ưu tiên: Cao.

- [ ] KVS-VID-015 — KhuonVien thực sự đang xây cái gì?
  - Hook: “KhuonVien không chỉ là app bật tắt thiết bị.”
  - Visual: Sensor → ESP → Server → App → Action.
  - Message: Observe → Decide → Act.
  - Mục tiêu: brand explainer / video ghim.
  - Ưu tiên: Rất cao.

- [x] KVS-VID-016 — Điều khiển bóng đèn bằng Wi‑Fi
  - Status: SCHEDULED.
  - Flow: Command → Wi‑Fi → ESP → Relay → Light.

- [x] KVS-VID-017 — Bật đèn bằng điện thoại
  - Hook: “Bóng đèn này, mình có thể bật ngay trên điện thoại.”
  - Visual: iPhone/KhuonVien app → Switch ON/OFF → bóng đèn thật.
  - Message: Mobile → Switch → Light.
  - Mục tiêu: chứng minh trải nghiệm mobile điều khiển thiết bị thật.
  - Status: READY FOR PRODUCTION.
  - Ưu tiên: Rất cao.

- [ ] KVS-VID-018 — Khi bấm ON trên app, phía sau xảy ra chuyện gì?
  - Flow dự kiến: Mobile → API → Backend → MQTT → Switch.
  - Mục tiêu: technical follow-up cho KVS-VID-017.

## Suggested first batch

Đề xuất duyệt và sản xuất trước:

- [ ] KVS-VID-006 — Demo trực quan — PAUSED / HOLD
- [ ] KVS-VID-008 — Một sensor → nhiều action
- [ ] KVS-VID-011 — Automation theo lịch
- [ ] KVS-VID-015 — Brand explainer

## Review rule

- Tick `[x]` khi topic được duyệt.
- Topic đã duyệt mới chuyển sang Content Planner / Script Writer.
- Topic chưa duyệt giữ nguyên ở backlog.
- KVS-VID-003 → KVS-VID-005 hiện đang tạm gác, không đưa vào production.
