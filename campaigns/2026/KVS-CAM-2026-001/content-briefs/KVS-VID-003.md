# KVS-VID-003 — Khi PIR phát hiện, server nhận gì?

## Campaign
KVS-CAM-2026-001 — Build KhuonVien Smart in Public

## Primary audience
DIY / maker / developer — secondary reach: tech-curious home & garden owner

## Pain point
Người xem hiểu sensor phát hiện chuyển động nhưng không hình dung được đoạn giữa “sensor báo” và “app/server biết”.

## Desired outcome
Sau video, người xem hiểu một physical event có thể trở thành software event để backend ghi nhận và xử lý tiếp.

## Brand pillar
- Observe Your Space
- Build & Improve
- Customizable IoT

## Objective
Cho người xem thấy trigger từ thiết bị đi vào backend như một software event, và server có thể ghi nhận/tiếp tục xử lý nó.

## Audience insight
Phần sensor thường trực quan; phần API/backend lại giống “hộp đen”. Video này mở hộp đen đó bằng log và flow thật.

## Hook
“PIR báo chuyển động rồi — server thực sự nhận được gì?”

## Key message
Khi firmware phát hiện cạnh LOW → HIGH, thiết bị gọi API trigger kèm định danh thiết bị. Backend nhận event đó để ghi nhận và quyết định bước xử lý tiếp theo.

## Proof / source
- Firmware gọi `AppApi::sendTrigger(App::getDeviceId())` khi PIR chuyển LOW → HIGH.
- Backend Rails hiện có luồng nhận trigger/event từ device.
- Hệ thống có model/log và logic phía server phục vụ automation.

## Story structure
1. Recap: PIR tạo trigger.
2. Device gửi event về backend.
3. Server nhận device/event.
4. Server ghi nhận hoặc chuyển sang logic xử lý tiếp.
5. Tease: bước tiếp theo là Action.

## Required footage
- Serial log trigger từ ESP.
- Network/API log hoặc Rails log khi request tới server.
- Một đoạn code controller/service nhận trigger, crop phần cần thiết.
- Dashboard hoặc log list cho thấy event đã được ghi nhận nếu đã verify.
- Không hiển thị token, credentials hoặc dữ liệu nhạy cảm.

## On-screen text candidates
- `PIR → ESP → API`
- `Server nhận event`
- `Physical event → Software event`
- `Observe → Decide`

## CTA
“Nhận event rồi thì server sẽ làm gì tiếp? Video sau mình thử kích hoạt một action.”

## Risks / claims to avoid
- Không claim latency realtime tuyệt đối hoặc SLA.
- Không claim server luôn nhận 100% event.
- Không phóng đại thành AI detection hay security-grade system.
- Ẩn token/secret/private identifiers.

## Handoff to Script Writer
Script 40–55 giây. Ưu tiên show log thật hơn giải thích dài. Giải thích API/backend bằng ngôn ngữ “thiết bị báo cho server biết chuyện gì vừa xảy ra” trước khi dùng jargon.