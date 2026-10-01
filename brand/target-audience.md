# KhuonVien Target Audience v1

## Audience strategy

KhuonVien phục vụ nhiều kiểu người dùng khác nhau, nhưng **mỗi nội dung chỉ nên nói với một audience chính**.

Ưu tiên hiện tại:

1. **Home & garden owner**
2. **DIY / maker / developer**
3. **Small farm / small property operator**

Đây là giả thuyết Brand Foundation v1 và phải tiếp tục được kiểm chứng bằng analytics, comment và hành vi người xem.

---

## Primary audience 1 — Home & garden owner

### Who they are

Người có nhà, sân, vườn hoặc một không gian nhỏ cần chăm sóc và muốn giảm những việc lặp lại như:

- tưới cây;
- bật/tắt bơm, đèn hoặc thiết bị;
- kiểm tra trạng thái từ xa;
- phát hiện một sự kiện trong khuôn viên;
- theo dõi chuyện gì đã xảy ra khi không có mặt.

Họ không nhất thiết quan tâm ESP32, MQTT hay backend hoạt động thế nào.

### Core pain points

- Không biết chuyện gì đang xảy ra khi không có mặt.
- Phải đi kiểm tra hoặc bật/tắt thủ công nhiều việc nhỏ.
- Các thiết bị hoạt động rời rạc.
- Automation hiện tại quá phức tạp hoặc khó hiểu.
- Muốn hệ thống linh hoạt hơn các thiết bị smart-home cố định.

### Jobs to be done

- Biết trạng thái hiện tại của khuôn viên.
- Nhận biết một sự kiện quan trọng.
- Tự động thực hiện một hành động đơn giản.
- Xem lại lịch sử khi cần.
- Thay đổi rule mà không cần hiểu toàn bộ hệ thống kỹ thuật.

### What makes them stop scrolling

- Một vấn đề rất quen thuộc.
- Before / after automation.
- Thiết bị thật đang chạy trong vườn/nhà.
- Kết quả nhìn thấy được ngay.
- “Trước đây phải làm bằng tay, giờ hệ thống tự làm.”

### Best content formats

- Problem → automation → result.
- Demo thực tế 20–60 giây.
- Before / after.
- Một ngày hệ thống tự xử lý việc gì.
- Một lỗi thực tế và cách cải thiện.

### Language

Ưu tiên:

- bơm;
- tưới;
- đèn;
- cảm biến;
- chuyển động;
- cảnh báo;
- lịch sử;
- tự bật / tự tắt.

Hạn chế jargon kỹ thuật nếu không cần thiết.

---

## Primary audience 2 — DIY / maker / developer

### Who they are

Người quan tâm:

- ESP32 / ESP8266;
- sensor;
- MQTT;
- firmware;
- backend;
- mobile app;
- automation architecture.

Họ muốn xem một hệ thống IoT **end-to-end** hoạt động ngoài môi trường thật, không chỉ là demo trên bàn.

### Core pain points

- Prototype thường chỉ dừng ở việc đọc sensor hoặc bật relay.
- Khó nối device → server → app → action → history thành một hệ thống rõ ràng.
- Tutorial thường bỏ qua lỗi vận hành thực tế.
- Muốn hiểu trade-off thay vì chỉ copy code.

### Jobs to be done

- Hiểu architecture.
- Xem implementation thực tế.
- Học từ bug và refactor.
- Hiểu cách firmware, backend và mobile phối hợp.
- Tìm ý tưởng để áp dụng cho project riêng.

### What makes them stop scrolling

- Architecture đơn giản nhưng thực tế.
- Debugging thật.
- Log / dashboard / code liên kết với hardware thật.
- Một quyết định kỹ thuật có trade-off rõ ràng.
- “Tại sao mình thiết kế flow này như vậy?”

### Best content formats

- Architecture breakdown.
- Dev log.
- Debugging story.
- Firmware → API → database → app flow.
- Lessons learned.

### Language

Có thể dùng thuật ngữ kỹ thuật như PIR, ESP32, MQTT, relay, API, worker, database… nhưng phải giải thích đủ để tech-curious vẫn theo được.

---

## Secondary audience — Small farm / small property operator

### Who they are

Người quản lý:

- vườn nhỏ;
- farm nhỏ;
- khu đất;
- khuôn viên có một số thiết bị cần theo dõi hoặc điều khiển.

Họ chưa cần một nền tảng công nghiệp lớn nhưng bắt đầu thấy việc vận hành thủ công tốn thời gian.

### Core pain points

- Phải kiểm tra thiết bị trực tiếp.
- Khó biết hệ thống đã chạy hay chưa.
- Có nhiều tác vụ lặp lại.
- Giải pháp công nghiệp có thể quá phức tạp hoặc quá lớn cho nhu cầu hiện tại.

### Jobs to be done

- Theo dõi trạng thái từ xa.
- Tự động hóa tác vụ lặp lại.
- Ghi lịch sử hoạt động.
- Biết khi có sự kiện bất thường.
- Thử automation nhỏ trước khi đầu tư hệ thống lớn hơn.

### Best content formats

- Case thực tế tại vườn.
- Theo dõi bơm / tưới / cảm biến.
- Một automation nhỏ tiết kiệm một thao tác lặp lại.
- Nhật ký vận hành và cải tiến.

---

## Audience overlap

Một use case có thể hấp dẫn nhiều audience, nhưng góc kể phải khác nhau.

Ví dụ cùng một hệ thống PIR:

### Home & garden owner
> Có chuyển động trong vườn khi mình không ở đó thì làm sao biết?

### Maker / developer
> PIR gửi event lên Rails backend và chống duplicate event như thế nào?

### Small property operator
> Có thể lưu lại các lần xuất hiện chuyển động để xem pattern theo thời gian không?

---

## Communication rule

Trước khi Script Writer bắt đầu một content item, Content Planner phải ghi rõ:

- **Primary audience**
- **Pain point**
- **Desired outcome**
- **Knowledge level**

Không viết video ngắn vừa giải thích cho người phổ thông vừa đi sâu code cho developer.

---

## Knowledge levels

### Non-technical

Dùng:

**Event → Action → Result**

Tránh jargon.

### Tech-curious

Có thể dùng tên sensor/device và mô tả server/app ở mức đơn giản.

### Developer / maker

Có thể đi sâu:

**Device → MQTT/API → Backend → Database → Automation → App**

---

## Current assumptions to validate

Brand Foundation v1 giả định rằng Home & Garden Owner là audience public-facing quan trọng nhất.

Các tín hiệu cần theo dõi:

- audience nào xem hết video nhiều hơn;
- chủ đề nào tạo comment hỏi thêm;
- nội dung practical hay technical tạo follow tốt hơn;
- use case nào khiến người xem mô tả vấn đề của chính họ;
- người xem có hiểu KhuonVien làm gì mà không cần giải thích thêm hay không.

Analytics phải được dùng để điều chỉnh audience priority thay vì coi tài liệu này là cố định.