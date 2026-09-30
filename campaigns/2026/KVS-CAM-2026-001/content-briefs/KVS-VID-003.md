# KVS-VID-003 — Khi PIR phát hiện, server nhận gì?

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Objective
Cho người xem thấy trigger từ thiết bị đi vào backend như một software event, và server có thể ghi nhận/tiếp tục xử lý nó.

## Audience insight
Người xem thường hiểu phần cảm biến nhưng khó hình dung đoạn giữa ‘cảm biến kêu’ và ‘app/dashboard biết’. Video này mở hộp đen đó.

## Hook
“PIR báo chuyển động rồi — server thực sự nhận được gì?”

## Key message
Khi firmware phát hiện cạnh LOW → HIGH, thiết bị gọi API trigger kèm định danh thiết bị. Backend nhận event đó để ghi nhận và quyết định bước xử lý tiếp theo. Không cần biến nó thành một hệ thống phức tạp để hiểu flow cốt lõi.

## Proof / source
- Firmware gọi `AppApi::sendTrigger(App::getDeviceId())` khi PIR chuyển LOW → HIGH.
- Backend Rails hiện có luồng nhận trigger/event từ device.
- Hệ thống có các model/device log và các action phía server phục vụ automation.

## Story structure
1. Recap: PIR tạo trigger.
2. Device gửi event về backend.
3. Server nhận device/event.
4. Server ghi nhận hoặc chuyển sang logic xử lý tiếp.
5. Tease: video sau là Action.

## Required footage
- Serial log trigger từ ESP.
- Network/API log hoặc Rails log khi request tới server.
- Một đoạn code controller/service nhận trigger, crop phần cần thiết.
- Dashboard hoặc log list cho thấy event đã được ghi nhận.
- Không hiển thị token, IP riêng, secret, credentials, internal IDs nếu nhạy cảm.

## On-screen text candidates
- `PIR → ESP → API`
- `Server nhận event`
- `Device ID + Trigger`
- `Physical event → Software event`

## CTA
“Nhận event rồi thì server sẽ làm gì tiếp? Video sau mình thử kích hoạt một action.”

## Risks / claims to avoid
- Không claim latency realtime tuyệt đối hoặc SLA.
- Không claim server luôn nhận 100% event.
- Không phóng đại thành ‘AI detection’ hay security-grade system.
- Ẩn IP/token/secret/private identifiers.

## Handoff to Script Writer
Script 40–55 giây. Ưu tiên show log thật hơn giải thích dài. Mỗi technical term phải có visual proof hoặc wording đủ đơn giản để người không code vẫn theo được.
