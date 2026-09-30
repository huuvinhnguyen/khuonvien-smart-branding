# KVS-VID-004 — Từ server kích hoạt relay/buzzer ra sao?

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Objective
Giải thích bước Action trong flow: backend sau khi nhận event có thể kích hoạt một hành động như buzzer hoặc relay thông qua command/MQTT/API trong prototype hiện tại.

## Audience insight
Người xem dễ hiểu cảm biến và dashboard, nhưng phần ‘server ra lệnh cho thiết bị thật’ thường là điểm tạo cảm giác automation rõ nhất.

## Hook
“Server nhận được chuyển động rồi — làm sao để nó bật một thiết bị thật?”

## Key message
Automation không dừng ở việc ghi log. Backend có thể phát command để một device khác thực hiện action, ví dụ buzzer hoặc relay. Đây là prototype đang thử nghiệm, không phải hệ thống an ninh hoàn thiện.

## Proof / source
- Hệ thống hiện có MQTT topics/action cho relay/buzzer.
- Backend có service/job liên quan đến bật/tắt relay và duration.
- KVS-VID-001 đã dùng buzzer như action minh họa, nhưng không nên khẳng định causal timing nếu chưa verify từng shot.

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
- Nếu có: đồng thời quay device + log để chứng minh chuỗi sự kiện.
- Một diagram đơn giản: `Event → Rule → Command → Action`.

## On-screen text candidates
- `Event → Rule → Action`
- `Server gửi command`
- `Action: Buzzer / Relay`
- `Automation = quyết định + hành động`

## CTA
“Video sau mình sẽ xem toàn bộ lịch sử event này trên dashboard.”

## Risks / claims to avoid
- Không nói hệ thống security-grade, fail-safe hoặc production-ready.
- Không claim exact latency nếu chưa đo.
- Không claim buzzer/relay luôn được kích hoạt bởi đúng event đang hiển thị nếu footage không chứng minh được causal chain.
- Không hiển thị broker credentials, token hoặc private network data.

## Handoff to Script Writer
Script 40–55 giây, nhấn mạnh ‘event → rule → command → action’. Giữ ngôn ngữ prototype/build-in-public và show proof thật thay vì nói quá nhiều.
