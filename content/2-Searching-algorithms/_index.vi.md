---
title : "Thuật toán tìm kiếm"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
**Thuật toán tìm kiếm** là quy trình tìm một phần tử cụ thể trong một tập hợp dữ liệu.

Chúng ta sẽ đi qua hai thuật toán tìm kiếm thường dùng: ***tìm kiếm tuyến tính*** và ***tìm kiếm nhị phân***.

#### Tìm kiếm tuyến tính (Linear search)
Trong thuật toán này, để tìm một mục cụ thể, mỗi phần tử trong tập hợp sẽ được kiểm tra theo thứ tự cho đến khi tìm thấy mục mong muốn hoặc đi qua toàn bộ danh sách. Độ phức tạp thuật toán là O(n). Thuật toán này phù hợp cho các danh sách có kích thước nhỏ hoặc chưa được sắp xếp.

Dưới đây là đoạn mã giả (pseudocode) mô tả thuật toán tìm kiếm tuần tự để tìm số 50 sau các cánh cửa tủ khóa:

```bash
For i from 0 to n-1
    If 50 is behind doors[i]
        Return true
Return false
```
Cho i từ 0 đến n-1
    Nếu 50 ở sau cánh cửa[i]
        Trả về giá trị đúng
Trả về giá trị sai

#### Tìm kiếm nhị phân (Binary search)
Thuật toán này chỉ áp dụng cho các danh sách đã được sắp xếp. Nó liên tục chia danh sách thành hai nửa và so sánh phần tử ở giữa danh sách với phần tử mục tiêu, sau đó thu hẹp khoảng tìm kiếm sang nửa trái hoặc nửa phải dựa trên kết quả so sánh. Độ phức tạp thuật toán là O(log n). Thuật toán này rất hiệu quả khi tìm kiếm trong các danh sách đã được sắp xếp lớn.

Dưới đây là đoạn mã giả mô tả thuật toán tìm kiếm nhị phân để tìm số 50 sau các cánh cửa tủ khóa:

```bash
If no doors left
    Return false
If 50 is behind middle door
    Return true
Else if 50 < middle door
    Search left half
Else if 50 > middle door
    Search right half
```
Nếu không còn cánh cửa nào
>    Trả về giá trị sai

Nếu 50 ở sau cánh cửa
>    Trả về giá trị đúng

Khác nếu 50 < cánh cửa ở giữa
>   Tìm nửa bên trái

Khác nếu 50 > cánh cửa ở giữa
>   Tìm nửa bên phải

