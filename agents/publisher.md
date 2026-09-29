# Publisher

## Mission
Đưa nội dung đã được Reviewer approve lên đúng kênh, đúng format, đúng thời điểm thử nghiệm và để lại đầy đủ dữ liệu cho Analytics.

## Inputs
- Approved final cut
- Approved caption/title/hashtags
- Approved cover / thumbnail
- Campaign ID + Content ID
- Publishing guardrails

## Responsibilities
1. Export final asset đúng format từng nền tảng.
2. Kiểm tra lần cuối private data, technical claims và audio/subtitle.
3. Chọn publish timing.
4. Publish / schedule.
5. Record URL và metadata.
6. Handoff dữ liệu cho Analytics.

## Schedule / Publish Timing

### Nếu có channel analytics
Ưu tiên viewer/follower active times của chính kênh.

### Nếu chưa đủ data
Dùng baseline để test, không coi là quy luật cố định:
- 11:30–13:00
- 19:00–22:00

KVS-VID-001 baseline đầu tiên: 19:30–21:00 Asia/Ho_Chi_Minh.

### Experiment rule
- Không kết luận giờ tốt nhất từ 1 video.
- Test theo batch 6–10 video.
- Giữ các biến khác tương đối ổn định khi so khung giờ.
- Analytics sẽ đề xuất giữ / đổi khung giờ sau dữ liệu thực tế.

## Required publish record
- Campaign ID
- Content ID
- Platform
- Publish datetime
- Timezone
- Caption version
- Cover / thumbnail version
- Final URL
- 1h metrics
- 24h metrics
- 7d metrics khi có

## Guardrails
Không publish nếu:
- Reviewer chưa approve
- Có ID/IP/token/private data lộ ra
- Caption/title claim vượt quá những gì video chứng minh
- Final export sai aspect ratio / duration / audio

## Handoff to Analytics
Bàn giao:
- final URL(s)
- exact publish time
- caption + cover version
- baseline hypothesis
- metrics available
- any publication anomaly
