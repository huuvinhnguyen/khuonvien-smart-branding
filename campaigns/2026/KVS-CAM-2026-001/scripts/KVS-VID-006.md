# KVS-VID-006 — Đi ngang → đèn hoặc buzzer bật

## Status
READY FOR PRODUCTION

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Primary audience
Home & garden owner / tech-curious user. Secondary: DIY / maker / developer.

## Target length
25–35 giây, dọc 9:16.

## Objective
Cho người xem hiểu ngay giá trị của KhuonVien bằng một tình huống thật: có chuyển động → PIR phát hiện → thiết bị phản ứng. Không đi sâu backend.

## Core message
Một chuyển động ngoài đời có thể trở thành một trigger để KhuonVien thực hiện một action thật, ví dụ bật đèn hoặc buzzer.

## Hook
**“Chỉ cần đi ngang qua đây, chuyện gì xảy ra?”**

---

# Script / EDL

## 0:00–0:03 — Hook / Curiosity

**Visual**
- Wide shot khu vực có PIR.
- Người bắt đầu bước vào vùng cảm biến.
- Cut cận PIR ngay trước lúc trigger.

**VO**
“Chỉ cần đi ngang qua đây, chuyện gì xảy ra?”

**On-screen**
`Đi ngang → chuyện gì xảy ra?`

**Audio**
- Nhạc nền nhẹ, giữ suspense.
- Có thể dùng riser rất ngắn trước khoảnh khắc trigger.

**Edit note**
- Không giải thích kỹ thuật ở 3 giây đầu.
- Phải thấy rõ “người đi ngang” và “PIR” trong cùng context.

---

## 0:03–0:07 — PIR detects motion

**Visual**
- Cận PIR.
- Nếu có LED/debug indicator thì show lúc trigger.
- Có thể insert 0.5–1 giây serial log thật: `PIR detected, sending trigger`.

**VO**
“Khi có chuyển động, PIR phát hiện sự thay đổi trong vùng cảm biến.”

**On-screen**
`Motion detected`

**Secondary label**
`PIR ≠ Camera`

**Edit note**
- Không dùng animation giống nhận diện người/khuôn mặt.
- Không nói PIR biết đó là người, chó hay mèo.

---

## 0:07–0:12 — Trigger becomes an action

**Visual**
- Cut từ PIR sang thiết bị action.
- Relay click / buzzer beep / đèn bật.
- Nếu dùng đèn: quay trước và sau thật rõ để thấy thay đổi.
- Nếu dùng buzzer: quay cả thiết bị và thêm waveform/icon nhỏ nếu âm thanh khó nghe trên điện thoại.

**VO**
“Trigger này được dùng để bật một action — ví dụ đèn hoặc buzzer.”

**On-screen**
`PIR → Trigger → Action`

**Audio**
- Giữ tiếng relay click / buzzer thật nếu thu được.
- Duck nhạc nền trong 0.5–1 giây đúng khoảnh khắc action xảy ra.

**Edit note**
- Đây là khoảnh khắc payoff chính của video.
- Nếu latency nhìn thấy rõ, giữ footage thật; không speed-ramp để làm phản ứng có vẻ nhanh hơn thực tế.

---

## 0:12–0:18 — Show it again, clearer

**Visual**
- Replay góc khác hoặc split-screen:
  - trái: người đi ngang + PIR
  - phải: đèn/buzzer phản ứng
- Có thể thêm arrow flow.

**VO**
“Tức là một chuyển động ngoài đời có thể biến thành một hành động tự động.”

**On-screen**
`Motion → PIR → Action`

**Edit note**
- Replay chỉ 1 lần.
- Nếu dùng split-screen, sync theo cùng một event đã quay.

---

## 0:18–0:25 — Why it matters

**Visual**
- Cảnh thực tế hơn: khu vườn / cổng / lối đi / khu vực thiết bị.
- Có thể show app/dashboard rất nhanh ở cuối nếu phù hợp, nhưng không bắt buộc.

**VO**
“Điểm mình muốn thử với KhuonVien là biến những việc lặp lại quanh nhà và khu vườn thành automation thật, dễ quan sát và dễ tùy chỉnh.”

**On-screen**
`Observe → Decide → Act`

**Edit note**
- Đây là đoạn brand value.
- Không biến video thành product ad; vẫn giữ cảm giác prototype/build in public.

---

## 0:25–0:31 — CTA / Next episode

**Visual**
- Graphic đơn giản:
  `1 PIR → ? actions`
- Cut nhanh đèn + buzzer.

**VO**
“Nhưng một PIR có thể điều khiển cùng lúc nhiều thiết bị không? Video sau mình thử luôn.”

**On-screen**
`Tiếp theo: 1 PIR → nhiều Action?`

**End card**
`KhuonVien — Build in Public`

**Edit note**
- Dẫn trực tiếp sang KVS-VID-008.
- End card 1–1.5 giây là đủ.

---

# Full Voice-over

“Chỉ cần đi ngang qua đây, chuyện gì xảy ra?

Khi có chuyển động, PIR phát hiện sự thay đổi trong vùng cảm biến.

Trigger này được dùng để bật một action — ví dụ đèn hoặc buzzer.

Tức là một chuyển động ngoài đời có thể biến thành một hành động tự động.

Điểm mình muốn thử với KhuonVien là biến những việc lặp lại quanh nhà và khu vườn thành automation thật, dễ quan sát và dễ tùy chỉnh.

Nhưng một PIR có thể điều khiển cùng lúc nhiều thiết bị không? Video sau mình thử luôn.”

---

# Subtitle copy

1. Chỉ cần đi ngang qua đây, chuyện gì xảy ra?
2. PIR phát hiện chuyển động trong vùng cảm biến.
3. Trigger được gửi để bật một action.
4. Ví dụ: đèn hoặc buzzer.
5. Motion → PIR → Action.
6. Một chuyển động ngoài đời có thể thành một hành động tự động.
7. KhuonVien: Observe → Decide → Act.
8. Tiếp theo: 1 PIR → nhiều Action?

---

# Production shot list

## Must-have
1. Wide shot khu vực lắp PIR.
2. Người đi ngang vào vùng cảm biến.
3. Close-up PIR.
4. Cảnh đèn trước khi bật.
5. Cảnh đèn bật hoặc buzzer kêu.
6. Shot có thể thấy rõ mối quan hệ giữa PIR và action.
7. End-card / graphic `Motion → PIR → Action`.

## Nice-to-have
8. Serial log thật: `PIR detected, sending trigger`.
9. Relay click close-up.
10. Split-screen cùng event: PIR / action.
11. App/dashboard 1–2 giây để cho thấy hệ thống có thể quan sát được.

---

# Recommended filming setup

- Quay 1080p hoặc 4K, 30fps.
- Ưu tiên video dọc 9:16 nếu quay riêng cho Reels/TikTok.
- Nếu quay ngang để tái sử dụng, giữ chủ thể ở vùng giữa để crop 9:16.
- Khóa exposure nếu cảnh đèn bật làm camera tự giảm sáng.
- Thu tiếng buzzer/relay thật ở khoảng cách gần.
- Quay mỗi action tối thiểu 3 take.
- Giữ 2–3 giây trước và sau trigger để editor có room cắt.
- Không quay token, IP, Wi-Fi password hoặc màn hình có dữ liệu nhạy cảm.

---

# Editor notes

## Pace
- 0:00–0:07: nhanh, 1–2 giây/cut.
- 0:07–0:18: payoff + replay rõ ràng.
- 0:18–0:31: chậm hơn một chút để truyền brand value + CTA.

## On-screen hierarchy
Primary:
- `Đi ngang → chuyện gì xảy ra?`
- `PIR → Trigger → Action`
- `Motion → PIR → Action`

Secondary:
- `PIR ≠ Camera`
- `Observe → Decide → Act`

## Sound
- Giữ tiếng action thật.
- Không che tiếng relay/buzzer bằng nhạc.
- Có thể dùng một impact nhẹ đúng lúc đèn/buzzer bật.
- Không dùng alarm/siren quá mạnh làm video giống quảng cáo hệ thống an ninh.

## Transition
- Hard cut là chính.
- Dùng arrow/simple motion graphic cho flow kỹ thuật.
- Không dùng hiệu ứng sci-fi/AI scanning.

---

# Technical guardrails

- PIR không nhận diện người, chó, mèo hay danh tính.
- Không gọi đây là hệ thống an ninh.
- Không claim khoảng cách, accuracy, false-positive rate nếu chưa đo.
- Không claim latency “tức thì” hoặc “real-time” nếu chưa benchmark.
- Không chỉnh tốc độ footage để làm action có vẻ phản ứng nhanh hơn thực tế.
- Nếu action đi qua backend/MQTT, chỉ mô tả đúng flow đã verify.
- Nếu demo dùng một action local/direct khác với production flow, phải nói rõ khi cần.

---

# Suggested caption

Chỉ cần đi ngang qua vùng PIR, KhuonVien có thể biến một chuyển động ngoài đời thành một action thật — ví dụ bật đèn hoặc buzzer.

Mình thích kiểu demo này vì không cần nói quá nhiều về backend: nhìn vào là thấy ngay Event → Action hoạt động như thế nào.

Video tiếp theo mình sẽ thử một bài khó hơn: một PIR có thể kích hoạt cùng lúc nhiều thiết bị không?

#KhuonVien #IoT #PIR #ESP32 #Automation #SmartGarden #BuildInPublic

---

# Cover

**ĐI NGANG  
ĐÈN TỰ BẬT?**

Small label:
`PIR → Action`

---

# Handoff

**Next owner: Production**

Production cần quay:
1. Một event thật từ đầu đến cuối.
2. PIR rõ trong context.
3. Action rõ bằng hình hoặc âm thanh.
4. Tối thiểu 3 take cho khoảnh khắc trigger.
5. Giữ footage raw để Reviewer kiểm tra timing thật.
