# Prototype Feedback Note

**Trạng thái: MOCK / DRY-RUN — không phải feedback từ tester thật, không tính vào Gate 4.** Hưng tự đóng vai tester để luyện format trước khi test thật; phần "Still Unproven" bên dưới tự ghi rõ điều này. Nếu không kịp test người thật trước hạn nộp, giữ nguyên trạng thái mock này, không đổi nhãn.

Phần thật (facilitate với người ngoài nhóm): **chưa có.** Xem [group-feedback-synthesis.md](group-feedback-synthesis.md) cho 12 phản hồi thật đã thu thập trong repo chung của Lực.

---

## Thông tin

* **Họ và tên:** Hoàng Tuấn Hưng
* **Mã học viên:** 2A202601911
* **Nhóm:** Đường Bốn Mùa Xuân
* **Case:** VLearn – AI Support Radar
* **Day:** Track 1 – Day 18
* **Loại feedback:** Mock/Synthetic feedback dùng để dry-run trước khi test thật

## 1. Test Context

Tester được đặt vào vai **Lab Coach** đang theo dõi nhiều learner/nhóm cùng lúc và cần xác định nhóm nào nên được hỗ trợ trước.

Tester trải nghiệm cả ba phương án:

* **Option A – Coach Query:** Coach chủ động yêu cầu AI kiểm tra.
* **Option B – AI Review Queue:** AI chủ động tổng hợp tín hiệu, Coach review và quyết định.
* **Option C – Proactive Agent:** AI chủ động hơn và có thể thực hiện một số hành động rủi ro thấp trong phạm vi được cho phép.

Ba option sử dụng cùng context, task và data fixture để đảm bảo việc so sánh tập trung vào **mức độ AI agency**.

## 2. Observed

Qua phần dry-run:

* Option B tạo cảm giác cân bằng nhất giữa automation và human control.
* Người dùng vẫn muốn xem evidence trước khi đồng ý với recommendation của AI.
* Option A dễ hiểu và an toàn nhưng yêu cầu Coach thực hiện nhiều thao tác hơn.
* Option C giúp giảm attention cost nhưng gây lo ngại về false positive và việc AI can thiệp quá sớm.
* Mức **High / Medium / Low Priority** chưa đủ minh bạch nếu không hiển thị lý do ngay trên giao diện.

## 3. Preferred Option

### Option B – AI Review Queue

Option B được ưu tiên vì AI có thể chủ động chuẩn bị danh sách những trường hợp đáng chú ý nhưng **Coach vẫn giữ quyền quyết định cuối cùng**.

Phương án này giảm thao tác so với Option A nhưng không trao quá nhiều quyền cho AI như Option C.

## 4. Main Friction

Điểm gây khó hiểu nhất là:

> Coach chưa biết rõ tại sao AI đưa một learner hoặc nhóm vào mức High Priority.

Nếu AI chỉ hiển thị priority mà không có evidence, người dùng có thể quá tin hoặc hoàn toàn không tin recommendation.

Ngoài ra, với Option C, vẫn có lo ngại AI có thể chủ động check-in nhầm learner không thực sự cần hỗ trợ.

## 5. Interpretation

Tôi tạm diễn giải rằng người dùng chấp nhận AI chủ động hỗ trợ, nhưng vẫn muốn giữ quyền kiểm tra và quyết định cuối cùng.

Trade-off chính là:

> **AI càng chủ động thì hệ thống càng phải minh bạch về evidence, uncertainty và khả năng sửa sai.**

## 6. Next Change

Thay đổi được đề xuất:

> **Giữ cơ chế AI Review Queue của Option B nhưng hiển thị evidence summary ngay trên từng priority card.**

Ví dụ:

**Group 07 — 3 signals worth checking**

* Checkpoint incomplete
* Repeated attempts ×4
* Related help queries ×3

`View details`

Điều này giúp Coach hiểu nhanh lý do AI đưa ra recommendation mà không cần mở quá nhiều màn hình.

_(Ghi chú đối chiếu: pattern này trùng với phát hiện độc lập từ 12 phản hồi thật trong repo của Lực — 4/12 người cũng vướng đúng chỗ "chưa rõ priority tính từ đâu". Hai nguồn khác nhau cùng chỉ ra một chỗ, đáng để ưu tiên sửa thật.)_

## 7. Still Unproven

Những điều vẫn chưa được chứng minh:

* Tín hiệu từ VLAB/checkpoint có đủ chính xác để nhận biết learner đang mắc hay không.
* Coach có thực sự thường xuyên bỏ sót learner cần hỗ trợ trong lớp học thật hay không.
* Bottleneck chính nằm ở detection hay ở khả năng hành động sau khi phát hiện.
* Learner có chấp nhận việc AI phân tích hành vi học tập và chủ động can thiệp hay không.
* Option B có thực sự giảm cognitive load trong lớp đông hay không.
* Mock feedback hiện tại chưa thể được coi là validation từ tester thật.

## 8. Reflection

Qua quá trình thiết kế và dry-run, tôi nhận thấy một hệ thống Human–AI tốt không chỉ cần AI phát hiện nhanh mà còn phải giúp người dùng hiểu **AI đang dựa vào dữ liệu nào, mức độ chắc chắn ra sao và có thể sửa AI như thế nào**.

Iteration tiếp theo nên ưu tiên transparency và human control thay vì tăng thêm automation.
