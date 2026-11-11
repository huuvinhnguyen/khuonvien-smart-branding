# KVS-VID-017 — Điều khiển switch thật từ app KhuonVien iOS / Flutter

## Status
READY FOR PRODUCTION

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Goal
Chứng minh trực quan app mobile KhuonVien trên **iOS và Flutter** có thể điều khiển switch và làm bóng đèn thật ON/OFF.

## Core message
**App → API → Device → Relay → Light**

Video ưu tiên proof-of-action và UX thật. Không đi sâu backend/MQTT trong video này; technical follow-up dành cho KVS-VID-018.

## Target
- 25–35 giây
- Vertical 9:16
- Reels / TikTok / YouTube Shorts
- Proof chính: iOS ON/OFF thiết bị thật; bổ sung Flutter cross-platform proof

## Voice-over V1

Bóng đèn này, mình có thể bật ngay trên điện thoại.

Đây là switch mình vừa tích hợp vào app KhuonVien.

Thử bật nhé.

Đèn đã bật.

Và tắt.

Một thao tác trên app trở thành một hành động thật trên thiết bị.

Đây là một phần mình đang xây cho KhuonVien.

## EDL V1

| Time | Visual / Shot | Voice-over | On-screen text |
| --- | --- | --- | --- |
| 0:00–0:03 | Bóng đèn OFF, đưa iPhone có app KhuonVien vào khung | Bóng đèn này, mình có thể bật ngay trên điện thoại. | Bật đèn bằng điện thoại? |
| 0:03–0:07 | Close-up app, mở thiết bị Switch | Đây là switch mình vừa tích hợp vào app KhuonVien. | KhuonVien → Switch |
| 0:07–0:11 | Ngón tay nhấn ON; ưu tiên thấy cả điện thoại và đèn | Thử bật nhé. | ON |
| 0:11–0:14 | Đèn sáng thật, giữ 1–2 giây | Đèn đã bật. | 💡 ON |
| 0:14–0:18 | Nhấn OFF trên mobile | Và tắt. | OFF |
| 0:18–0:21 | Đèn tắt; giữ âm thanh thật | — | 💡 OFF |
| 0:21–0:26 | Split-screen/replay app → đèn | Một thao tác trên app trở thành một hành động thật trên thiết bị. | Mobile → Switch → Light |
| 0:26–0:30 | App + thiết bị/đèn + end card | Đây là một phần mình đang xây cho KhuonVien. | KhuonVien — Build in Public |

## Production must-have

1. Bóng đèn OFF trước thao tác.
2. iPhone mở đúng màn hình Switch của KhuonVien.
3. Một shot duy nhất thấy **cả điện thoại và bóng đèn**: tap ON → đèn sáng thật.
4. Tap OFF → đèn tắt thật.
5. Screen recording app để dùng B-roll.
6. Close-up relay/thiết bị nếu thuận tiện.
7. Giữ 2–3 giây trước/sau mỗi action.

## Production rule

Shot 0:07–0:14 là proof shot quan trọng nhất. Không speed-up để giả cảm giác phản hồi nhanh. Nếu latency chưa được benchmark thì không dùng claim “realtime”, “instant” hay số mili-giây.

## Technical guardrails

- Chỉ mô tả luồng đã xác minh.
- Không để token, IP, password hoặc dữ liệu nhạy cảm xuất hiện.
- Không claim production-grade/realtime nếu chưa đo.
- Video này tập trung UX Mobile → thiết bị thật, không cần giải thích backend/MQTT.

## Next content

**KVS-VID-018 — Khi bấm ON trên app, phía sau thực sự xảy ra chuyện gì?**

Dự kiến: Mobile → API → Backend → MQTT → Switch.


## Hướng dẫn quay thực tế — V2 (2026-11-11)

### Chuẩn bị trước khi bấm quay (5–10 phút)
- iPhone đã đăng nhập app KhuonVien, mở đúng Switch/relay có thể bật tắt bóng đèn thử nghiệm.
- Bóng đèn, nguồn và thiết bị relay được lắp an toàn trong hộp/đế cách điện; **không chạm dây điện lưới hoặc đấu nối khi đang cấp điện**. Nếu chưa có bộ thử nghiệm an toàn, nhờ người có chuyên môn lắp.
- Chuẩn bị một điện thoại thứ hai hoặc máy quay để quay cả iPhone và bóng đèn; giá đỡ cố định, ánh sáng đủ thấy màn hình không bị cháy sáng.
- Kiểm tra Wi-Fi, quyền điều khiển, đèn OFF lúc bắt đầu; thử ON/OFF 2 lần **trước khi quay** để chắc chắn hoạt động.
- Bật Không làm phiền, giấu thông báo và thông tin cá nhân, chỉnh độ sáng màn hình khoảng 60–80% tùy điều kiện; không lộ IP/token/chip ID nhạy cảm.

### Danh sách cảnh quay theo thứ tự ưu tiên
1. **Take A — proof shot liên tục, bắt buộc:** Máy quay cố định 9:16, thấy đồng thời màn hình iPhone, ngón tay và bóng đèn. Quay từ khi đèn OFF, giữ 3 giây → chạm ON → đợi đèn sáng thật → giữ 3 giây → chạm OFF → đợi đèn tắt → giữ 3 giây. **Không cắt giữa lúc chạm và lúc đèn đổi trạng thái.** Quay 2–3 take để chọn take rõ nhất.
2. **Take B — cận cảnh app:** Quay màn hình iPhone từ màn hình Switch, thao tác ON rồi OFF; có thể dùng iOS Screen Recording để dựng xen kẽ. Ẩn thông báo.
3. **Take C — toàn cảnh thiết bị:** Quay bóng đèn và hộp switch/relay đã được che chắn, 5–7 giây; không mở hộp đang có điện.
4. **Take D — outro:** Quay app + bóng đèn trong cùng khung 4–5 giây để đặt dòng “KhuonVien — Build in Public”.

### Lời dẫn dễ đọc, 25–30 giây
- 0–3s: “Bóng đèn này, mình bật được ngay trên điện thoại.”
- 3–7s: “Đây là công tắc mình đang tích hợp vào ứng dụng KhuonVien.”
- 7–14s: “Mình bấm bật. Đèn sáng thật.”
- 14–21s: “Giờ bấm tắt. Đèn cũng tắt theo.”
- 21–30s: “Từ một thao tác trên điện thoại đến thiết bị ngoài đời. Mình sẽ tiếp tục chia sẻ cách KhuonVien hoạt động.”

### Checklist bàn giao Editor
- [ ] Có take A liên tục, rõ tay chạm và đèn đổi trạng thái thật.
- [ ] Có take B màn hình app và take C thiết bị, không lộ thông tin nhạy cảm.
- [ ] Video gốc dọc 9:16, âm thanh sạch; giữ file gốc, không chỉnh tốc độ proof shot.
- [ ] Đặt tên `KVS-VID-017_A_proof_01.mp4`, `KVS-VID-017_B_app_01.mp4`, `KVS-VID-017_C_device_01.mp4`.
- [ ] Tải file lên thư mục media chiến dịch trên Drive; dán link vào task ClickUp KVS-VID-017.
- [ ] Chỉ chuyển Production → Editor khi proof shot đã đạt; nếu lỗi Wi-Fi/relay thì ghi rõ và quay lại, không giả lập kết quả.


---

# Script / EDL V3 — iOS + Flutter cross-platform proof (2026-11-12)

## Hook
**“App tự làm có điều khiển được thiết bị thật không?”**

## 0:00–0:03 — Hook / Proof first

**Visual**
- Cùng khung hình có điện thoại và bóng đèn/relay thật.
- Bóng đèn đang OFF.
- Tay chuẩn bị chạm ON trên app.

**VO**
“App tự làm có điều khiển được thiết bị thật không?”

**On-screen**
`App → thiết bị thật?`

**Edit note**
- Không mở đầu bằng logo, terminal hoặc code.
- 3 giây đầu phải thấy được cả app và thiết bị thật.

## 0:03–0:08 — KhuonVien iOS

**Visual**
- Close-up app KhuonVien trên iPhone.
- Mở màn hình switch/device.
- Label nhỏ: `iOS`.

**VO**
“Đây là app KhuonVien mình đang phát triển trên iOS.”

**On-screen**
`KhuonVien iOS`

## 0:08–0:14 — ON → real action

**Visual**
- Shot liên tục thấy tay chạm ON và bóng đèn.
- Relay/đèn phản ứng thật.
- Giữ nguyên timing thực tế.

**VO**
“Mình bật switch trên app, lệnh được gửi tới thiết bị và relay bật bóng đèn.”

**On-screen**
`App → API → Device → Relay ON`

**Audio**
- Giữ tiếng relay click nếu thu được.
- Duck nhạc nền đúng khoảnh khắc action.

**Edit note**
- Đây là proof shot quan trọng nhất.
- Không speed-up hoặc cắt che latency.

## 0:14–0:19 — OFF → verify control

**Visual**
- Chạm OFF.
- Bóng đèn tắt.
- Có thể thêm close-up relay/device.

**VO**
“Bấm OFF, thiết bị nhận lệnh và bóng đèn tắt.”

**On-screen**
`OFF → Device → Light OFF`

## 0:19–0:25 — Flutter proof

**Visual**
- Chuyển sang app Flutter trên Android/thiết bị thật.
- Show cùng switch.
- Thực hiện một action ngắn ON hoặc OFF.
- Match cut vị trí nút switch nếu dựng được.

**VO**
“Cùng flow này hiện cũng đã chạy được trên phiên bản Flutter.”

**On-screen**
`iOS ✅   Flutter ✅`

**Edit note**
- Chỉ dùng câu này khi Flutter đã verify physical action.
- Nếu mới verify UI thì đổi VO thành: “Cùng flow này đang được triển khai trên Flutter.”

## 0:25–0:31 — Brand value

**Visual**
- Wide shot điện thoại + switch/ESP/relay + bóng đèn.
- Overlay flow tối giản.

**VO**
“Đây là cách mình đang xây KhuonVien: kết nối phần mềm với những hành động thật quanh nhà và khu vườn.”

**On-screen**
`Software → Real-world action`

**End card**
`KhuonVien — Build in Public`

## 0:31–0:34 — Optional CTA

**On-screen**
`Tiếp theo: app → nhiều thiết bị?`

**VO**
“Video sau mình thử điều khiển nhiều thiết bị từ cùng một app.”

---

# Full Voice-over V3

“App tự làm có điều khiển được thiết bị thật không?

Đây là app KhuonVien mình đang phát triển trên iOS.

Mình bật switch trên app, lệnh được gửi tới thiết bị và relay bật bóng đèn.

Bấm OFF, thiết bị nhận lệnh và bóng đèn tắt.

Cùng flow này hiện cũng đã chạy được trên phiên bản Flutter.

Đây là cách mình đang xây KhuonVien: kết nối phần mềm với những hành động thật quanh nhà và khu vườn.”

---

# Subtitle copy V3

1. App tự làm có điều khiển được thiết bị thật không?
2. Đây là app KhuonVien trên iOS.
3. Bật switch trên app.
4. Lệnh được gửi tới thiết bị.
5. Relay bật bóng đèn thật.
6. Bấm OFF → bóng đèn tắt.
7. iOS ✅ Flutter ✅
8. KhuonVien: Software → Real-world action.

---

# Production shot list V3

## Must-have
1. Wide shot có cả điện thoại và bóng đèn/thiết bị thật.
2. Close-up app KhuonVien iOS.
3. Một take liên tục: iOS tap ON → đèn sáng thật.
4. Một take liên tục: iOS tap OFF → đèn tắt thật.
5. Flutter/Android shot cùng switch.
6. Một physical action được trigger từ Flutter nếu đã verify.
7. End shot toàn hệ thống: app + device + relay/light.
8. Screen recording iOS và Flutter nếu có.

## Nice-to-have
9. Close-up relay click.
10. ESP/switch device LED phản ứng.
11. Split-screen app / physical light.
12. Backend/API log thật tối đa 0.5–1 giây.
13. Match cut iOS ↔ Flutter trên cùng nút switch.

---

# Editor notes V3

## Pace
- 0:00–0:03: hook nhanh.
- 0:03–0:08: app context.
- 0:08–0:19: payoff ON/OFF.
- 0:19–0:25: cross-platform proof.
- 0:25–0:31: brand value.
- CTA tối đa 2–3 giây nếu cần.

## Priority
Proof shot quan trọng hơn screen recording hoặc code. Người xem phải thấy **tap trên app → thiết bị thật đổi trạng thái**.

## Technical guardrails
- Chỉ claim iOS/Flutter đã điều khiển thiết bị thật nếu đã verify physical action.
- Không claim “instant”, “real-time”, “zero latency” nếu chưa benchmark.
- Không speed-up footage để che latency.
- Không claim local control nếu flow thực tế đi qua backend/API/MQTT.
- Mô tả trung tính: “lệnh được gửi tới thiết bị” khi không cần giải thích transport.
- Không để token, JWT, IP, Wi-Fi password hoặc dữ liệu nhạy cảm xuất hiện.

---

# Suggested caption V3

Từ app KhuonVien trên iOS, mình đã có thể bật/tắt một switch thật và thấy relay điều khiển bóng đèn ngoài đời.

Điểm mình muốn chứng minh ở video này không phải giao diện đẹp đến đâu, mà là flow thật:

`App → API → Device → Relay → Light`

Cùng chức năng cũng đã chạy trên Flutter.

Mình đang build KhuonVien theo hướng từng bước kết nối phần mềm với những việc thật quanh nhà và khu vườn.

#KhuonVien #IoT #iOS #Flutter #ESP32 #Automation #SmartHome #BuildInPublic

---

# Cover V3

**BẤM TRÊN APP  
ĐÈN BẬT THẬT?**

Small label:
`iOS + Flutter → Switch`

---

# Handoff V3

**Next owner: Production**

Production cần bàn giao:
1. iOS ON → đèn bật thật.
2. iOS OFF → đèn tắt thật.
3. Flutter điều khiển cùng switch trên thiết bị thật.
4. Wide shot app + thiết bị trong cùng context.
5. Screen recordings nếu có.
6. Raw footage giữ nguyên timing để Reviewer kiểm tra action thật.
