# Track 1 — Day 18: Multiple Prototypes & Human–AI Design

**Người nộp:** Hoàng Tuấn Hưng — 2A202601911
**Nhóm:** Đường Bốn Mùa Xuân

| Thành viên | Mã học viên |
| --- | --- |
| Vũ Thế Lực | 2A202602008 |
| Hoàng Tuấn Hưng | 2A202601911 |
| Nguyễn Thị Nam Phương | 2A202601720 |
| Đỗ Thị Thanh Loan | 2A202601654 |

## Lab Information

- **Track:** Track 1 — AI Product
- **Day:** Day 18
- **Case:** C — AI Support Radar (VLearn)

## Hypothesis Problem

> Khi một phiên lab đông học viên đang diễn ra hoặc vừa kết thúc, Lab Coach gặp khó khăn trong việc xác định learner nào đang thực sự mắc kẹt và cần được ưu tiên hỗ trợ vì tín hiệu hiện tại nằm rải rác giữa quan sát tại lớp, tiến độ checkpoint/VLAB và việc learner tự lên tiếng, dẫn đến nguy cơ một số learner được phát hiện hoặc hỗ trợ muộn trong khi thời gian của coach bị phân tán.

Chi tiết evidence và cách nhóm đi tới hypothesis này ở [cp1-evidence-continuity.md](cp1-evidence-continuity.md).

## Ba Solution Options

- **Option A — Coach Query:** coach chọn phạm vi rồi mới yêu cầu AI phân tích. AI không tự tạo queue hay liên hệ learner.
- **Option B — AI Review Queue:** AI tự gom tín hiệu thành queue kèm priority, coach duyệt trước khi có hành động nào chạm tới learner.
- **Option C — Proactive Agent:** AI được tự gửi check-in rủi ro thấp trong giới hạn policy, có thể trước cả khi coach mở tab; coach có undo, opt-out, audit log.

Prototype chạy được tại [prototype/index.html](prototype/index.html) (mở trực tiếp bằng trình duyệt). Chi tiết cơ chế từng option ở [prototype-link.md](prototype-link.md), phân quyền Human–AI đầy đủ ở [human-ai-decision-table.md](human-ai-decision-table.md).

## Đóng góp của tôi trong nhóm

_(Bản nháp dựa trên nội dung commit "Redesign prototype UI" của Hưng — Hưng đọc lại và sửa cho đúng ý mình trước khi nộp, phần này cần chính Hưng xác nhận.)_

Phần tôi phụ trách là thiết kế lại giao diện của cả ba prototype sau khi bản đầu (A/B của Lực, C của Loan) đã chạy được nhưng khó nắm tình hình: mọi khối dùng chung một kiểu khung nên không có phân cấp, không màn nào tóm tắt được tình hình lớp ngay khi mở lên.

Việc tôi làm:
- Thêm một dải "situation strip" 4 ô ở đầu mỗi option, tóm số liệu suy ra từ data fixture có sẵn (không thêm dữ liệu mới). Riêng Option A, dải này chỉ hiện sau khi coach bấm quét, để không phá cơ chế "AI chưa phân tích gì cho tới khi được yêu cầu" mà Lực đã thiết kế.
- Đổi Option A sang layout master-detail, Option B và C có một "decision rail" dính bên cạnh khi xem chi tiết case.
- Đổi evidence từ 4 dòng liệt kê dọc thành lưới 2 cột; checkpoint card có thanh tiến độ; audit log của Option C đổi thành dạng timeline.
- Tách các đoạn văn dài thành bullet để đọc nhanh hơn — chỉ đổi cách xuống dòng, không đổi chữ, có viết smoke test riêng để kiểm việc này không làm trôi nội dung gốc.
- Thêm chế độ sáng/tối, mặc định theo cài đặt hệ điều hành, có nút chuyển và nhớ lựa chọn qua localStorage (có bọc try/catch cho trường hợp trình duyệt chặn).
- Thêm một lớp trang trí (glow, gradient nhẹ) tách riêng ở cuối file CSS, không chạm vào giá trị evidence hay khối uncertainty — để tín hiệu không bị đọc nhầm thành kết luận.

Đã tự kiểm bằng smoke test (jsdom) và audit contrast trên Chrome thật ở cả hai theme trước khi đưa vào repo chung.

## Prototype Feedback

Xem [group-feedback-synthesis.md](group-feedback-synthesis.md) — tổng hợp chung của nhóm từ 12 phản hồi thật (thu thập bởi Lực, xem chi tiết phương pháp trong file đó).

`prototype-feedback-note.md` của riêng tôi: _(để trống — tôi chưa tự facilitate một phiên test riêng; sẽ bổ sung nếu có thời gian trước hạn nộp)._

## AI Support Log

_(Để Hưng tự viết — mình (Lực) không viết thay được phần này, vì đây là lời của chính người dùng AI, không phải người khác suy đoán hộ.)_

## Trạng thái Gate

- [x] Gate 1 — Evidence Continuity
- [x] Gate 2 — Meaningful Options
- [x] Gate 3 — Human Control
- [ ] Gate 4 — Test-ready (12 phản hồi là tự báo cáo qua tin nhắn, không có facilitator quan sát trực tiếp)
- [x] Gate 5 — Learning, not praise
