# Branding Workflow

## Main flow
Brand Manager → Content Planner → Script Writer → Production → Editor → Reviewer → Publisher → Analytics

## Handoff rule
Mỗi handoff phải có:
- Campaign / Content ID
- Inputs đã dùng
- Output hiện tại
- Open questions
- Next owner

## Video production workflow đã kiểm chứng

### 1. Plan
- Chốt campaign brief.
- Chốt content brief.
- Chốt script và EDL trước khi dựng.

### 2. Build final visual timeline trước
- Dựng một video timeline hoàn chỉnh từ source gốc.
- Với KVS-VID-001: target 52s, 1080×1920, 30fps.
- Không để raw clip rời rạc cùng tồn tại trên Canva final page nếu không cần.

### 3. Voice
- Tạo voiceover trong Descript.
- Voice có thể ngắn hơn visual timeline; target thực tế 45–50s cho video 52s.
- Không cố kéo voice bằng khoảng lặng quá dài.
- Ưu tiên câu ngắn, tự nhiên, dễ TTS.

### 4. Canva assembly
- Chỉ giữ:
  1. Final cut video
  2. Final voice layer
- Xóa raw clips cũ khỏi page.
- Luôn kiểm tra duration của từng asset trước commit.
- Asset dài bất thường có thể kéo total duration toàn design.
- Không dùng audio như layer 1×1/opacity 0 vì playback không ổn định.

### 5. Review before commit
Kiểm tra:
- total duration
- voice timing
- buzzer/ambient có át voice không
- private data / IDs
- technical claims
- CTA
- subtitle readability

### 6. Commit
Chỉ commit Canva sau khi preview đúng.

### 7. Schedule / Publish Timing
Publisher phải chọn thời điểm đăng thay vì publish ngẫu nhiên.

Ưu tiên theo thứ tự:
1. Dùng analytics thật của từng kênh để xem follower/viewer active times.
2. Nếu kênh chưa đủ dữ liệu, dùng baseline test ban đầu:
   - Trưa: 11:30–13:00
   - Tối: 19:00–22:00
3. Không kết luận “giờ vàng” từ 1 video. Chia batch 6–10 video để test các khung giờ.
4. Record chính xác thời gian publish cho từng platform.
5. Analytics dùng dữ liệu 1h / 24h / 7d để đề xuất khung giờ tiếp theo.

Với kênh mới, KVS-VID-001 dùng baseline đầu tiên: 19:30–21:00 (Asia/Ho_Chi_Minh), sau đó Analytics xác nhận hoặc thay đổi.

### 8. Publish record
Publisher phải lưu:
- platform
- publish datetime + timezone
- caption version
- cover / thumbnail version
- final URL
- 1h metrics
- 24h metrics
- notes nếu có sự cố publish

## Lesson learned từ KVS-VID-001
- Một raw clip 107s đã kéo video gần 2 phút.
- Voice v1 30s không khớp timeline 52s.
- Voice v2 ~48s phù hợp hơn.
- Final page nên tối giản: final cut + voice.
- Publish timing phải được coi là một biến thử nghiệm, không phải một “giờ vàng” cố định.
