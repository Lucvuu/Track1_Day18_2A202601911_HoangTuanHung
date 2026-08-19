# AI Support Log

## Thông tin

* **Họ và tên:** Hoàng Tuấn Hưng
* **Mã học viên:** 2A202601911
* **Nhóm:** Đường Bốn Mùa Xuân
* **Case:** VLearn – AI Support Radar
* **Day:** Track 1 – Day 18: Multiple Prototypes & Human–AI Design

## 1. AI đã hỗ trợ những gì?

Trong Day 18, tôi sử dụng AI để:

* Phân tích yêu cầu và các checkpoint của bài lab.
* Kết nối evidence Day 17 với Hypothesis Problem của Day 18.
* Hỗ trợ tách **Observed Evidence** và **Interpretation**.
* Gợi ý cách tạo ba solution option khác nhau về mức AI agency.
* Hỗ trợ xây dựng:
  * Option A – User-led / Coach Query
  * Option B – Co-created / AI Review Queue
  * Option C – Proactive AI Agent
* Kiểm tra việc A/B/C có thực sự khác nhau về mechanism hay chỉ khác UI.
* Gợi ý Human–AI Design theo:
  * Expectation
  * Role & Agency
  * Evidence & Uncertainty
  * Control & Recovery
* Hỗ trợ xây dựng test task, feedback structure và cách tổng hợp trade-off.
* Hỗ trợ rà soát nội dung prototype và tài liệu nộp bài.

## 2. Điểm AI đề xuất chưa phù hợp

Một số output ban đầu của AI chưa hoàn toàn phù hợp với bài lab:

* Có lúc AI đi sang solution quá sớm trước khi evidence Day 17 được kiểm tra đầy đủ.
* Một số cách diễn đạt khiến problem mạnh hơn mức evidence thực tế hỗ trợ.
* Có phương án ban đầu thay đổi cả user flow nên việc so sánh A/B/C chưa công bằng.
* AI có xu hướng đề xuất nhiều tính năng hơn mức cần thiết cho một micro-prototype.
* Feedback do AI mô phỏng chỉ có thể dùng để dry-run, không thể coi là evidence từ tester thật.

## 3. Tôi đã tự kiểm tra và chỉnh sửa

Tôi cùng nhóm đã:

* Kiểm tra lại evidence Day 17 trước khi giữ Hypothesis Problem.
* Không coi hypothesis là fact hoặc validation.
* Giữ cùng target user là **Instructor/Lab Coach** cho cả ba option.
* Giữ nguyên situation, task, desired outcome và data fixture.
* Chỉ thay đổi mức độ phân quyền giữa Human và AI.
* Giữ quyền quyết định cuối cùng cho Coach.
* Bổ sung các cơ chế kiểm soát như:
  * Review
  * Dismiss
  * Undo
  * Stop / Global Pause
  * Audit Log
* Không sử dụng output của AI như user evidence.

## 4. AI giúp ích nhất ở đâu?

AI hữu ích nhất trong việc giúp tôi hệ thống hóa các yêu cầu của bài lab và nhìn rõ sự khác biệt giữa:

> **thay đổi giao diện**

và

> **thay đổi Human–AI interaction mechanism.**

AI cũng giúp nhóm nhận diện các vấn đề cần xem xét như:

* automation bias;
* false positive;
* explainability;
* uncertainty;
* human control;
* recovery khi AI sai.

## 5. Những phần tôi và nhóm tự quyết định

AI không thay thế quyết định của nhóm trong các phần:

* Chọn evidence Day 17.
* Chốt Hypothesis Problem.
* Chọn ba solution options.
* Xác định trade-off cần test.
* Thiết kế prototype.
* Đánh giá feedback tester thật.
* Chốt Next Change.
* Xác định Still Unproven.

AI được sử dụng như công cụ hỗ trợ reasoning và rà soát, không phải nguồn evidence.

## 6. Reflection

Qua Day 18, tôi nhận thấy AI có thể hỗ trợ rất nhanh trong việc mở rộng ý tưởng và cấu trúc reasoning, nhưng mọi output vẫn cần được đối chiếu với evidence và rubric.

Nếu không kiểm tra kỹ, AI có thể khiến nhóm:

* solutionize quá sớm;
* biến assumption thành fact;
* tạo ba option khác giao diện nhưng giống mechanism;
* hoặc đưa ra claim mạnh hơn evidence.

Vì vậy, cách sử dụng AI phù hợp nhất là:

> **AI hỗ trợ mở rộng và kiểm tra reasoning; con người chịu trách nhiệm về evidence, quyết định và kết luận cuối cùng.**
