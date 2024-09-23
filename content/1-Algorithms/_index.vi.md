---
title : "Thuật toán"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Thuật toán** có thể được ví như một hộp đen nhận đầu vào và tạo ra đầu ra.

Trong tuần này, chúng ta sẽ xem cách một thuật toán hoạt động khi giải quyết một vấn đề. Thuật toán có thể được thiết kế ngày càng hiệu quả, tới mức nhất định. Chúng ta sẽ tập trung vào thiết kế thuật toán và cách đo lường hiệu quả của chúng. Chúng ta sẽ đánh giá hiệu suất của các thuật toán qua **độ phức tạp của thuật toán**.

Độ phức tạp của thuật toán (time complexity) xem xét số lần mỗi câu lệnh được thực thi. Nó không phải là thời gian thực tế cần để thực thi một đoạn mã cụ thể, vì điều đó phụ thuộc vào các yếu tố khác như ngôn ngữ lập trình, phần mềm điều hành, sức mạnh xử lý, v.v.

Để diễn đạt độ phức tạp của một thuật toán, chúng ta sử dụng kí hiệu `O`. Nó thể hiện mức độ tăng lên của số lần thực thi giải thuật tương ứng với lượng đầu vào `n`.

Ví dụ, nếu thời gian chạy của một thuật toán tăng "theo kích thước của đầu vào", chúng ta sẽ nói rằng nó là `O(n)`.

Hoặc độ phức tạp thuật toán `O(log n)` có nghĩa là thời gian giảm với một độ lớn tỉ lệ nghịch với đầu vào n. Thuật toán này không cần phải xử lý tất cả các đầu vào, vì chúng thường hoạt động bằng cách loại bỏ lượng lớn đầu vào ở mỗi bước.

Ngoài ra chúng ta cũng cần quan tâm đến trường hợp tốt nhất của một thuật toán với ký hiệu Omega Ω. Chẳng hạn như `Ω(n)` có nghĩa là thuật toán cần n bước trong trường hợp tốt nhất.