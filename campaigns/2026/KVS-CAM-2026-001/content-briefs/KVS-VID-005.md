# KVS-VID-005 — Xem lịch sử chuyển động trên dashboard

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Objective
Khép lại mini-series Sensor → Device → Server → Action → Data bằng cách cho thấy event sau khi đi qua hệ thống có thể được lưu và xem lại trên dashboard theo thời gian.

## Audience insight
Người xem không chỉ muốn biết thiết bị có phản ứng hay không; họ cần thấy dữ liệu được lưu lại để quan sát pattern và hiểu chuyện gì đã xảy ra khi không có mặt.

## Hook
“Nếu mình không có ở vườn, làm sao biết lúc nào cảm biến đã phát hiện chuyển động?”

## Key message
Sau khi event được backend ghi nhận, lịch sử có thể được hiển thị trên dashboard để người dùng xem lại theo thời gian. Giá trị của hệ thống không chỉ là action tức thời mà còn là khả năng quan sát dữ liệu sau đó.

## Proof / source
- KVS-VID-001 đã có dashboard/history footage.
- Backend hiện có logic lưu event/log phục vụ việc quan sát lịch sử.
- Dashboard có thể hiển thị các event theo thời điểm; chỉ mô tả đúng những trường dữ liệu thực tế đang có.

## Story structure
1. Problem: không có mặt tại vườn.
2. Event đã được ghi nhận.
3. Dashboard hiển thị history/timestamp.
4. Người dùng xem lại theo thời gian.
5. Recap toàn series: Sensor → Device → Server → Action → Data.

## Required footage
- Dashboard history ở trạng thái sạch, dễ đọc.
- Timestamp/event list thật.
- Một shot filter/time view nếu tính năng này hiện có và đã verify.
- Montage ngắn PIR → ESP → server → buzzer/relay → dashboard.
- Crop/hide device IDs, internal identifiers hoặc dữ liệu riêng tư không cần thiết.

## On-screen text candidates
- `Lưu lịch sử phát hiện`
- `Xem lại theo thời gian`
- `Action + Data`
- `Sensor → Device → Server → Action → Data`

## CTA
“Bạn muốn mình build tiếp phần nào: notification, automation rule hay mobile app?”

## Risks / claims to avoid
- Không claim dashboard có filter/analytics cụ thể nếu chưa verify UI hiện tại.
- Không gọi đây là giám sát an ninh chuyên nghiệp.
- Không claim dữ liệu không bao giờ mất hoặc được lưu vô hạn.
- Không để lộ private IDs, IPs, tokens hoặc user data.

## Handoff to Script Writer
Script 40–55 giây, ưu tiên UI readability. Kết thúc bằng recap cả chuỗi và CTA mở cho experiment tiếp theo.
