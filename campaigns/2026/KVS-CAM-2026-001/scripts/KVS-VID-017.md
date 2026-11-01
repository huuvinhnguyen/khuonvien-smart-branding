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
