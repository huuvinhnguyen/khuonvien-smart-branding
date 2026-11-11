# KVS-VID-017 — Bật đèn bằng điện thoại

## Status
READY FOR PRODUCTION

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Goal
Chứng minh trực quan app mobile KhuonVien có thể điều khiển switch và làm bóng đèn thật ON/OFF.

## Core message
**Mobile → Switch → Light**

Không đi sâu API/MQTT trong video này. Technical follow-up dành cho KVS-VID-018.

## Target
- 25–30 giây
- Vertical 9:16
- Reels / TikTok / YouTube Shorts

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
