# KhuonVien Messaging Framework v1

## Core message

**KhuonVien giúp biến những việc lặp lại quanh nhà, sân vườn và mô hình nhỏ thành những việc thiết bị có thể quan sát, hỗ trợ và tự động thực hiện — theo cách thực tế, dễ hiểu và có thể tùy biến.**

Short version:

**Để công nghệ lo những việc lặp lại quanh khuôn viên của bạn.**

---

## Messaging hierarchy

### 1. Start from a real problem

Technology should solve a real task.

Use when:
- mở đầu video;
- giới thiệu một experiment mới;
- giải thích vì sao một feature tồn tại.

Preferred framing:

> Có việc gì đang phải làm lặp lại bằng tay?

> Có chuyện gì xảy ra khi mình không có mặt?

> Có thể để thiết bị tự xử lý việc này không?

Content should begin with the problem before mentioning the technology.

---

### 2. Show the action and result

Người xem phải hiểu hệ thống đã làm gì ngoài đời.

Preferred structure:

**Event → Action → Result**

Examples:

> Đến giờ tưới → bơm bật → hết thời gian → bơm tự tắt.

> PIR phát hiện chuyển động → event được gửi về hệ thống → app/server ghi nhận sự kiện.

> Người dùng bật thiết bị trên app → thiết bị thật thay đổi trạng thái → hệ thống lưu lại kết quả.

---

### 3. Make automation observable

Automation không chỉ cần chạy; người dùng cần biết:

- điều gì vừa xảy ra;
- thiết bị nào đã hoạt động;
- automation nào được kích hoạt;
- kết quả cuối cùng là gì;
- có thể xem lại lịch sử hay không.

Useful proof points, when confirmed:

- server received an event;
- device status changed;
- app/dashboard reflected the state;
- history was recorded;
- automation completed its intended action.

---

### 4. Open + customizable

KhuonVien không được kể như một flow cố định duy nhất.

Một system flow có thể thay:

- sensor;
- device;
- rule;
- action;
- UI;
- notification.

Preferred framing:

> Hôm nay mình dùng buzzer làm action. Cùng flow này có thể đổi thành relay hoặc một action khác ở experiment tiếp theo.

Không biến khả năng lý thuyết thành product claim nếu integration chưa được test.

---

### 5. Build and learn in public

Prototype là experiment.

Lỗi, giới hạn và lesson learned là một phần của content.

Default story structure:

**Problem → Experiment → Result → Lesson → Next improvement**

KhuonVien không cần tạo cảm giác mọi thứ đều hoàn hảo ngay từ đầu.

---

## Message pillars

### Pillar 1 — Practical Automation

**Tự động hóa một việc thật.**

Topics:
- tưới;
- bơm;
- đèn;
- timer;
- cảnh báo;
- monitoring;
- remote control.

### Pillar 2 — Observe Your Space

**Biết chuyện gì đang xảy ra trong khuôn viên của mình.**

Topics:
- sensor;
- motion events;
- device status;
- history;
- dashboard;
- logs.

### Pillar 3 — Build & Improve

**Thử, đo, sửa và làm hệ thống tốt hơn.**

Topics:
- prototype;
- failures;
- debugging;
- architecture;
- improvements;
- experiments.

### Pillar 4 — Customizable IoT

**Automation phù hợp với không gian thật, không ép không gian phải phù hợp với thiết bị.**

Topics:
- custom rules;
- different sensors;
- different actions;
- hardware integration;
- mobile/backend/device workflows.

---

## Supporting messages

- Sensor chỉ thật sự hữu ích khi dữ liệu dẫn tới một quyết định hoặc action.
- Dashboard hữu ích khi giúp trả lời: **“Đã xảy ra chuyện gì?”**
- Automation tốt nên giảm công việc lặp lại, không tạo thêm việc phải giám sát.
- Bắt đầu bằng automation nhỏ, quan sát được, rồi mới tăng độ phức tạp.
- Một hệ thống smart không nhất thiết phải dùng AI.
- Công nghệ tốt nhất là công nghệ giải quyết vấn đề mà người dùng gần như không phải nghĩ tới nó.

---

## Audience-specific messaging

### Home & garden owner

Lead with:

**Problem → Convenience → Result**

Example:

> Mỗi tối phải ra bật đèn ngoài vườn? Mình thử để hệ thống tự làm việc đó theo lịch.

Avoid leading with:

> ESP32 subscribe MQTT topic...

### DIY / maker / developer

Lead with:

**Problem → Architecture → Trade-off → Result**

Example:

> PIR chỉ gửi trigger khi rising edge. Vậy backend nên quyết định motion session và history như thế nào?

### Small farm / property operator

Lead with:

**Repeated operation → Remote visibility → Automation**

Example:

> Thay vì đi kiểm tra bơm nhiều lần, mình muốn biết trạng thái và lịch hoạt động từ xa.

---

## Proof point rules

Một proof point chỉ được dùng như fact khi có bằng chứng từ ít nhất một nguồn phù hợp:

- source code;
- footage;
- dashboard/app;
- server log;
- database/history;
- test thực tế.

### Safe / confirmed-style language

- “Trong prototype hiện tại…”
- “Mình đang thử…”
- “Ở phiên bản này…”
- “Server ghi nhận event…” nếu log xác nhận.
- “Thiết bị tự tắt sau X giây…” nếu demo/test xác nhận.

### Unverified / prohibited claims

Không tự ý dùng:

- “100% chính xác”;
- “real-time” nếu chưa đo latency;
- “phát hiện người/kẻ lạ” nếu sensor chỉ phát hiện motion;
- “hệ thống an ninh” nếu không được thiết kế/chứng nhận cho mục đích đó;
- “ổn định 24/7” nếu chưa có reliability test;
- “tiết kiệm X%” nếu chưa có dữ liệu;
- “AI-powered” nếu AI không thật sự cần thiết;
- “production-ready” khi vẫn đang ở prototype/experiment stage.

---

## Tone of voice

KhuonVien nên nói như một người **đang tự xây, thử và chia sẻ kết quả thật**.

### Prefer

- cụ thể;
- dễ hiểu;
- tò mò;
- thực tế;
- có bằng chứng;
- thừa nhận giới hạn khi cần.

### Avoid

- corporate buzzwords;
- hype;
- phóng đại;
- quá nhiều jargon;
- nói như quảng cáo trước khi có sản phẩm hoàn chỉnh.

---

## CTA library

Prefer curiosity and participation:

- “Bạn muốn mình thử tự động hóa việc gì tiếp theo?”
- “Ở nhà hoặc vườn của bạn có việc gì đang phải làm lặp lại mỗi ngày?”
- “Bạn muốn xem phần sensor, server hay app kỹ hơn?”
- “Nếu đổi action này thành thiết bị khác, bạn sẽ dùng gì?”
- “Bạn muốn mình test tình huống nào tiếp theo?”

Avoid generic CTA unless needed:

- “Like share subscribe ngay!”
- “Sản phẩm số 1…”
- “Công nghệ đột phá…”

---

## Short brand lines

Primary working line:

**Để công nghệ lo những việc lặp lại quanh khuôn viên của bạn.**

Supporting working lines:

- **Practical automation for real spaces.**
- **Observe. Automate. Improve.**
- **From sensor to real-world action.**
- **Build. Observe. Automate. Learn.**

Các dòng trên là working lines, chưa phải tagline pháp lý hoặc tagline thương mại cố định.

---

## Content quality check

Trước khi publish, Reviewer phải có thể trả lời “Có” cho phần lớn câu hỏi sau:

1. Nội dung có bắt đầu từ một vấn đề hoặc nhu cầu thật không?
2. Người xem có hiểu thiết bị/hệ thống đã làm gì không?
3. Có kết quả, bằng chứng hoặc observation không?
4. Ngôn ngữ có phù hợp với audience đã chọn không?
5. Có claim nào vượt quá bằng chứng hiện có không?
6. Nội dung có phản ánh ít nhất một brand pillar không?
7. Người xem có hiểu thêm KhuonVien là gì sau khi xem không?