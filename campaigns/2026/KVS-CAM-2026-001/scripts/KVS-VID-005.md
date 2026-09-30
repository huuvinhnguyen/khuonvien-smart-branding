# KVS-VID-005 — Xem lịch sử chuyển động trên dashboard

## Objective
Cho thấy phần Data/Observe của hệ thống: event từ thế giới thật có thể được xem lại trên dashboard thay vì chỉ tồn tại ở log.

## Target length
45–55 giây, dọc 9:16.

## Core message
Khi event được ghi nhận đúng cách, dashboard giúp quan sát lại khi nào có sự kiện, tần suất và xu hướng cơ bản theo thời gian.

## Hook
**“Một lần phát hiện chuyển động thì dễ thấy. Nhưng nếu muốn biết cả ngày đã xảy ra bao nhiêu lần thì sao?”**

## Script / EDL

### 0:00–0:05 — Hook
**Visual:** dashboard/history list hoặc chart có dữ liệu thật.
**VO:** “Một lần phát hiện chuyển động thì dễ thấy. Nhưng nếu muốn biết cả ngày đã xảy ra bao nhiêu lần thì sao?”
**On-screen:** `Không chỉ thấy event — cần xem lại được`

### 0:05–0:13 — Why history matters
**Visual:** PIR ngoài vườn → dashboard.
**VO:** “Lúc đó log terminal không còn đủ tiện. Mình cần một chỗ để xem lại event theo thời gian.”
**On-screen:** `Event → History`

### 0:13–0:22 — Dashboard view
**Visual:** quay dashboard thực tế, highlight danh sách hoặc biểu đồ.
**VO:** “Dashboard giúp mình nhìn các event đã ghi nhận và kiểm tra chúng xảy ra vào thời điểm nào.”
**On-screen:** `Thời gian • Thiết bị • Sự kiện`

### 0:22–0:32 — Patterns
**Visual:** scroll/zoom theo giờ hoặc ngày nếu UI có hỗ trợ thật.
**VO:** “Khi có đủ dữ liệu, mình có thể bắt đầu nhìn pattern đơn giản: giờ nào có nhiều activity hơn, thiết bị nào phát hiện thường xuyên hơn.”
**On-screen:** `Observe → Pattern`

### 0:32–0:41 — Data quality caveat
**Visual:** một event record + cảnh PIR.
**VO:** “Nhưng số liệu chỉ có ý nghĩa khi cách mình định nghĩa và lưu event nhất quán. Một trigger PIR chưa tự động có nghĩa là một đối tượng cụ thể.”
**On-screen:** `Data cần đúng ngữ cảnh`

### 0:41–0:49 — Learning loop
**Visual:** diagram Sensor → Device → Server → Action → Data → Improve.
**VO:** “Đó là vòng lặp mình muốn cho KhuonVien Smart: quan sát, hiểu hệ thống đang làm gì, rồi cải thiện rule tiếp theo.”
**On-screen:** `Observe → Learn → Improve`

### 0:49–0:55 — CTA
**Visual:** montage cả series.
**VO:** “Bạn muốn mình đào sâu phần nào tiếp: cảm biến, automation hay dashboard?”
**On-screen:** `Bạn muốn xem phần nào tiếp?`

## Required footage
- Dashboard/history thật có event hợp lệ.
- Một record/event close-up.
- View theo giờ/ngày nếu UI thực sự hỗ trợ.
- Cảnh PIR ngoài vườn để nối physical event với data.

## Proof/source
Use only current dashboard/history functions that are visibly available in the product at filming time. If motion history schema is still evolving, frame the screen as a prototype/experiment.

## Claims to avoid
- Không nói dashboard phân biệt người/thú nếu chưa có classifier.
- Không suy ra “motion duration” nếu backend chỉ có rising-edge events.
- Không nói chart/history là hoàn chỉnh nếu feature còn đang phát triển.
- Không dùng số liệu demo như dữ liệu thực tế nếu chưa xác minh.

## Handoff
Next owner: Production.
Before recording, prepare a small set of verified test events so the dashboard is readable and privacy-safe.