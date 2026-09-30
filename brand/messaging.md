# Messaging Framework

## Core message
**KhuonVien Smart giúp biến những việc lặp lại quanh nhà và sân vườn thành những việc thiết bị có thể tự làm — theo cách thực tế, dễ quan sát và có thể tùy biến.**

## Message hierarchy

### 1. Practical automation
Technology should solve a real task.

Use when:
- giới thiệu một experiment mới
- mở đầu video bằng vấn đề thực tế
- giải thích vì sao một feature tồn tại

Example:
> Có chuyển động trong vườn khi mình không ở đó? Mình thử để sensor phát hiện rồi gửi sự kiện về hệ thống.

### 2. Observable system
Automation không chỉ “chạy”; người dùng cần biết điều gì đã xảy ra.

Proof points có thể dùng khi đã xác nhận:
- event được server ghi nhận
- trạng thái thiết bị có thể xem trên dashboard/app
- lịch sử sự kiện có thể được lưu và xem lại

### 3. Open + customizable
Một flow có thể thay sensor, device, rule hoặc action để phù hợp bài toán khác.

Example framing:
> Hôm nay action là buzzer; cùng flow này có thể thử với relay hoặc một action khác ở experiment sau.

Không biến ví dụ thành claim sản phẩm nếu integration chưa được kiểm chứng.

### 4. Build and learn in public
Prototype là experiment. Lỗi và lesson learned là một phần của nội dung.

Default story structure:
**Problem → Experiment → Result → Lesson**

## Supporting messages
- Sensor tạo ra dữ liệu có ý nghĩa khi nó đi được tới action.
- Dashboard hữu ích khi giúp trả lời “đã xảy ra chuyện gì?”.
- Automation tốt nên giảm công việc lặp lại, không tạo thêm việc phải giám sát.
- Bắt đầu đơn giản, đo được, rồi mới tăng độ phức tạp.

## Proof point rules
Một proof point chỉ được dùng như fact khi đã có bằng chứng trong source code, footage, dashboard, log hoặc test đã xác nhận.

### Confirmed-style language
- “Trong prototype hiện tại…”
- “Mình đang thử…”
- “Server ghi nhận event…” nếu footage/log xác nhận.
- “Action ví dụ là buzzer…” nếu đúng với experiment.

### Unverified / prohibited claims
Không tự ý dùng:
- “100% chính xác”
- “real-time” nếu chưa đo latency
- “phát hiện người/kẻ lạ” nếu sensor chỉ phát hiện motion
- “hệ thống an ninh” nếu chưa được thiết kế/chứng nhận cho mục đích đó
- “ổn định 24/7” nếu chưa có reliability test
- “tiết kiệm X%” nếu chưa có dữ liệu
- “sản phẩm hoàn thiện / production-ready” khi vẫn là prototype

## CTA library
Prefer curiosity and participation:
- “Bạn muốn mình thử tự động hóa việc gì tiếp theo?”
- “Bạn muốn xem phần sensor, server hay app kỹ hơn?”
- “Nếu đổi buzzer thành một action khác, bạn sẽ chọn gì?”

Avoid generic CTA nếu không cần:
- “Like share subscribe ngay!”
- “Sản phẩm số 1…”

## Short brand lines
- **Practical automation for real spaces.**
- **Sensor → Data → Action.**
- **Build. Observe. Automate. Learn.**

Các dòng trên là working lines, không phải tagline pháp lý/chính thức và có thể được điều chỉnh sau khi có analytics.
