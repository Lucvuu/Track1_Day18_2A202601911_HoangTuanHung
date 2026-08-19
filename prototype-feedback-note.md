# Prototype Feedback Note

**Người tổng hợp:** Hoàng Tuấn Hưng — 2A202601911
**Nhóm:** Đường Bốn Mùa Xuân
**Case:** VLearn – AI Support Radar
**Prototype:** https://claude.ai/code/artifact/fce7227a-a027-47b1-9282-2ebf58048e26

**Nguồn dữ liệu:** 12 phản hồi thật do Lực thu thập (repo `Track1_Day18_2A202602008_VuTheLuc/prototype-feedback-note.md`), cộng thêm 1 phản hồi thật thu thập riêng cho repo này (mục 10 bên dưới). Phần OBSERVED/INTERPRETED/pattern dưới đây là **cách tôi tự đọc và diễn giải cùng bộ dữ liệu đó** — không phải một phiên tôi tự facilitate, vì tôi không trực tiếp thu thập 12 phản hồi gốc.

## 1. Hình thức thu thập feedback

Nhóm thu được phản hồi từ **12 người ngoài nhóm**. Tester tự mở prototype, trải nghiệm cả ba phương án **A/B/C**, sau đó trả lời:

1. Chọn A, B hay C?
2. Vì sao chọn phương án đó?
3. Điểm khó chịu hoặc khó hiểu nhất là gì?

Các phản hồi được gửi lại qua tin nhắn, không có facilitator ngồi cạnh quan sát trực tiếp quá trình thao tác.

## 2. Giới hạn phương pháp

Đây là hình thức **async self-report**, vì vậy tôi chỉ sử dụng những gì tester trực tiếp báo lại.

Không có dữ liệu đủ để kết luận về:

* First action.
* Chỗ tester dừng hoặc do dự.
* Evidence nào được đọc hoặc bỏ qua.
* Thời gian hoàn thành.
* Cách tester sử dụng recovery trong quá trình thao tác.

Do đó tôi không suy đoán thêm các hành vi không được quan sát trực tiếp.

## 3. Kết quả tổng hợp

Phân bố lựa chọn của 12 tester:

* **Option A:** 3/12
* **Option B:** 5/12
* **Option C:** 4/12

Option B được chọn nhiều nhất trong mẫu hiện tại, nhưng kết quả này không được xem là bằng chứng rằng B là solution tốt nhất hoặc đã validated.

## 4. OBSERVED

Từ các phản hồi thực tế:

* 5 tester chọn B.
* 4 tester chọn C.
* 3 tester chọn A.
* Tester chọn B thường nhắc tới việc AI hỗ trợ giảm tải nhưng Coach vẫn giữ quyền quyết định.
* Tester chọn A đồng thời nhắc đến nhược điểm phải thao tác nhiều hoặc khó scale khi lớp đông.
* Tester chọn C đánh giá cao tốc độ và tính chủ động nhưng đặt câu hỏi về false positive, monitoring và khả năng AI hiểu sai tín hiệu.
* Nhiều tester muốn hiểu rõ hơn vì sao AI đưa một nhóm vào mức High/Medium/Low Priority.
* Có tester đề xuất hiển thị trực tiếp nút hoặc thông tin **"Why?"** cạnh priority.

## 5. INTERPRETED

Từ các phản hồi trên, tôi tạm diễn giải:

### Option A

A tạo cảm giác kiểm soát và an toàn cao vì AI chỉ hoạt động khi Coach yêu cầu.

Tuy nhiên, việc cả ba tester chọn A đều đề cập đến thao tác thủ công hoặc khả năng khó scale cho thấy trade-off của A được người dùng cảm nhận tương đối rõ.

### Option B

B được nhiều tester mô tả là mức cân bằng giữa:

> **Automation và Human Control**

AI có thể chủ động chuẩn bị thông tin nhưng Coach vẫn kiểm tra và quyết định trước khi có tác động tới learner.

Tuy nhiên, nếu Review Queue quá dài hoặc priority thiếu giải thích thì B vẫn có thể tạo thêm cognitive load.

### Option C

C hấp dẫn với những người ưu tiên tốc độ và muốn AI hỗ trợ chủ động hơn trong lớp đông.

Ngược lại, đây cũng là option tạo ra nhiều câu hỏi nhất liên quan đến:

* False positive.
* AI check-in nhầm.
* Quyền riêng tư và monitoring.
* Learner có biết mình đang được theo dõi không.
* AI có thể hiểu sai một tín hiệu như thời gian dừng checkpoint.

Điều này cho thấy khi AI agency tăng thì nhu cầu về transparency, consent và recovery cũng tăng theo.

## 6. Pattern nổi bật

Pattern đáng chú ý nhất không phải chỉ là B có số lượt chọn cao nhất, mà là:

> **Tester muốn AI giúp giảm attention cost nhưng vẫn muốn hiểu evidence và giữ khả năng kiểm soát quyết định.**

Một pattern khác là sự thiếu minh bạch của priority.

Các câu hỏi như:

* "High Priority được tính như thế nào?"
* "AI dựa vào tín hiệu gì?"
* "Có thể xem Why? ngay không?"

xuất hiện nhiều lần và nên được đưa sang iteration tiếp theo.

## 7. DECIDED / NEXT CHANGE

Từ phần feedback tôi tổng hợp, thay đổi nên được ưu tiên là:

> **Giữ cơ chế Review Queue nhưng bổ sung evidence summary và uncertainty ngay trên từng priority card.**

Ví dụ:

### Group 07 — 3 signals worth checking

* Checkpoint incomplete
* Repeated attempts ×4
* Related help queries ×3

`Why?` · `Review` · `Dismiss`

Thay đổi này nhằm giúp Coach hiểu ngay tại sao AI đưa một case lên queue mà không cần tin vào một nhãn High/Medium/Low đơn thuần.

Quyết định cuối cùng của cả nhóm được tổng hợp trong [`group-feedback-synthesis.md`](group-feedback-synthesis.md).

## 8. STILL UNPROVEN

Sau vòng feedback này, các vấn đề sau vẫn chưa được chứng minh:

1. Các learning signals hiện tại có đủ chính xác để dự đoán learner đang mắc hay không.
2. Cách giải thích priority nào đủ rõ nhưng không làm giao diện quá tải.
3. False positive ở Option C nên được recovery theo cơ chế nào ngoài Undo/Stop.
4. Learner có cần được thông báo hoặc cho phép opt-out khỏi behavioral monitoring hay không.
5. Coach có thực sự thường xuyên bỏ sót learner cần support trong lớp học thật không.
6. Bottleneck chính nằm ở detection hay ở khả năng hành động sau detection.
7. Vì feedback là async self-report, chưa biết hành vi thực tế của tester trong quá trình sử dụng prototype.
8. Chưa thể kết luận B tốt hơn A/C chỉ từ phân bố 5/12, 4/12 và 3/12.

## 9. Reflection

Qua vòng feedback, tôi nhận thấy việc tăng AI agency không chỉ là vấn đề thêm automation.

AI càng chủ động thì hệ thống càng phải làm rõ:

* AI đang dựa vào evidence nào.
* AI chắc chắn đến đâu.
* Con người có quyền sửa hoặc từ chối ở đâu.
* Khi AI sai thì recovery như thế nào.

Do đó, iteration tiếp theo nên tập trung vào **evidence transparency, uncertainty và human control** trước khi tiếp tục tăng mức tự động hóa.

---

## 10. Phản hồi thật thu thập riêng cho repo này

Ngoài 12 phản hồi ở trên, có thêm 1 phản hồi thật thu thập riêng (bởi Lực thay tôi, vì tôi đang nằm viện không tự facilitate được) — cùng phương pháp async self-report, chưa nằm trong 12 người ở trên.

**Người trả lời:** 1 người ngoài nhóm. Tự mở link prototype, tự dùng cả A/B/C, tự báo lại qua tin nhắn.

**Lựa chọn:** B — AI Review Queue

**Lý do:** cân bằng nhất giữa tự động hóa và quyền kiểm soát; AI gom tín hiệu nhưng Coach vẫn xem evidence trước khi quyết định. A an toàn nhưng thủ công; C nhanh nhưng AI chủ động quá nhiều nên dè chừng hơn trong bối cảnh học tập.

**Điểm khó chịu nhất:** khó tin mức Priority nếu không biết ngay vì sao AI xếp mức đó — muốn thấy 2–3 evidence chính ngay trên card thay vì phải bấm sâu vào màn hình khác.

Đây là phản hồi thật thứ 13 độc lập cùng nêu đúng vấn đề "chưa rõ priority tính từ đâu" — khớp với pattern ở mục 5–6 phía trên.

---

## Phụ lục — Mock / Dry-run (tài liệu tham khảo, không tính vào Gate 4)

Trước khi có phản hồi thật, tôi tự đóng vai tester để luyện format ghi feedback. **Đây là template dùng chung với Lực** (repo `Track1_Day18_2A202602008_VuTheLuc` cũng có bản gần giống, chỉ đổi tên) — không phải hai lần luyện độc lập ra trùng nhau ngẫu nhiên.

**Loại feedback:** Mock/Synthetic — không phải người ngoài nhóm.

**Preferred option (mock):** B — AI Review Queue, cùng lý do cân bằng automation/control.

**Main friction (mock):** chưa rõ vì sao AI xếp một nhóm vào High Priority nếu không hiển thị evidence ngay trên giao diện — dự đoán đúng pattern mà dữ liệu thật ở trên xác nhận.
