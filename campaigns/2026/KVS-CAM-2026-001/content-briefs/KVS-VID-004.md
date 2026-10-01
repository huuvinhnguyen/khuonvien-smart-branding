# KVS-VID-004 — Từ server kích hoạt relay/buzzer ra sao?

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Primary audience
DIY / maker / developer — secondary reach: Home & garden owner

## Pain point
Người xem dễ hiểu sensor và dashboard nhưng chưa thấy rõ automation tạo ra hành động vật lý như thế nào.

## Desired outcome
Sau video, người xem hiểu lõi của automation là **Event → Rule → Command → Action**, và KhuonVien không dừng ở việc hiển thị dữ liệu.

## Brand pillar
- Practical Automation
- Customizable IoT
- Build & Improve

## Objective
Giải thích bước Action trong flow: backend sau khi nhận event có thể kích hoạt một hành động như buzzer hoặc relay thông qua command/MQTT/API trong prototype hiện tại.

## Audience insight
Khoảnh khắc software làm thiết bị thật thay đổi trạng thái là nơi người xem dễ cảm nhận giá trị automation nhất.

## Hook
“Server biết có chuyển động rồi — làm sao để nó bật một thiết bị thật?”

## Key message
Automation không dừng ở việc ghi log. Backend có thể phát command để một device thực hiện action, ví dụ buzzer hoặc relay. Đây là prototype đang thử nghiệm, không phải hệ thống an ninh hoàn thiện.

## Proof / source
- Hệ thống hiện có MQTT topics/action cho relay/buzzer.
- Backend có service/job liên quan đến bật/tắt relay và duration.
- KVS-VID-001 đã dùng buzzer như action minh họa; causal timing chỉ được mô tả khi footage/log chứng minh được.

## Story structure
1. Server đã nhận event.
2. Rule/logic quyết định action.
3. Server gửi command.
4. Device thực hiện action.
5. Lesson: event → rule → action là lõi của automation.

## Required footage
- Rails log/service/action phía server.
- MQTT publish hoặc command log.
- Relay hoặc buzzer thực tế hoạt động.
- Nếu có: quay đồng thời device + log để chứng minh chuỗi sự kiện.
- Diagram đơn giản: `Event → Rule → Command → Action`.

## On-screen text candidates
- `Event → Rule → Action`
- `Server gửi command`
- `Action: Buzzer / Relay`
- `Software → hành động ngoài đời`

## CTA
“Video sau mình sẽ xem toàn bộ lịch sử event này trên dashboard.”

## Risks / claims to avoid
- Không nói hệ thống security-grade, fail-safe hoặc production-ready.
- Không claim exact latency nếu chưa đo.
- Không claim buzzer/relay được kích hoạt bởi đúng event đang hiển thị nếu footage không chứng minh causal chain.
- Không hiển thị broker credentials, token hoặc private network data.

## Handoff to Script Writer
Script 40–55 giây. Mở bằng kết quả ngoài đời, sau đó mới giải thích rule/command. Nhấn mạnh `Event → Rule → Command → Action` và ưu tiên visual proof hơn jargon.