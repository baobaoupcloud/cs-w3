---
title : "Thuật toán sắp xếp"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
Thuật toán sắp xếp được sử dụng để sắp xếp lại một danh sách các phần tử bằng những phép so sánh giữa các phần tử. Có nhiều thuật toán sắp xếp khác nhau, mỗi thuật toán có những ưu điểm và hạn chế riêng. Chúng ta sẽ khám phá ba thuật toán sắp xếp sau: ***sắp xếp chọn, sắp xếp nổi bọt và sắp xếp trộn***.

#### Sắp xếp chọn
Thuật toán sắp xếp chọn hoạt động bằng cách tìm phần tử nhỏ nhất trong phần chưa được sắp xếp của mảng và hoán đổi nó với phần tử chưa được sắp xếp đầu tiên. Lặp lại cho đến khi mảng được sắp xếp hoàn toàn.

Chúng ta có thể biểu diễn một mảng như sau:

![flowchart](https://raw.githubusercontent.com/baobaoupcloud/cs-w3/main/static/images/3.sortingalgorithms/sorting1.png)

Thuật toán sắp xếp chọn trong đoạn mã giả như sau:

```bash
For i from 0 to n–1
    Find smallest number between numbers[i] and numbers[n-1]
    Swap smallest number with numbers[i]
```
Cho i từ 0 đến n-1
> Tìm số nhỏ nhất giữa số[i] và số [n-1]

> Hoán đổi số nhỏ với với số[i]

\
Độ phức tạp thuật toán là O(n²), Ω(n²). Thuật toán này dễ hiểu và dễ thực hiện. Tuy nhiên, nó không hiệu quả cho các tập dữ liệu lớn, đặc biệt khi dữ liệu gần như đã được sắp xếp.

#### Sắp xếp nổi bọt
Thuật toán sắp xếp này hoạt động bằng cách liên tục hoán đổi các phần tử để “nổi bọt” các phần tử lớn hơn lên cuối.

Mã giả cho sắp xếp nổi bọt như sau:

```bash
Repeat n-1 times
    For i from 0 to n–2
        If numbers[i] and numbers[i+1] out of order
            Swap them
    If no swaps
        Quit
```
```
Lặp lại n-1 lần
Cho i từ 0 đến n-2
    Nếu số[i] và số[i+1] không theo thứ tự
        Hoán đổi chúng
 Nếu không hoán đổi
    Thoát
```
Đối với cách sắp xếp này, độ phức tạp thuật toán là O(n²) cho trường hợp xấu nhất và Ω(n) cho trường hợp tốt nhất. Sắp xếp nổi bọt là một cách tiếp cận đơn giản. Nó hiệu quả cho các tập dữ liệu nhỏ hoặc dữ liệu gần như đã được sắp xếp. Tuy nhiên, thuật toán này tương đối chậm và không phù hợp cho các mảng lớn.

#### Sắp xếp trộn (Merge sort)
Sắp xếp trộn là thuật toán sắp xếp theo phương pháp ***chia để trị***. Nó hoạt động bằng cách chia mảng đầu vào thành các mảng con nhỏ hơn và sắp xếp những mảng con đó, sau đó hợp nhất chúng lại với nhau để có được mảng đã sắp xếp.

Mã giả cho thuật toán như sau:

```bash
If only one number
    Quit
Else
    Sort left half of number
    Sort right half of number
    Merge sorted halves
```
```
Nếu chỉ có một số
    Thoát
Khác
    Sắp xếp nửa bên trái
    Sắp xếp nửa bên phải
    Trộn 2 nửa đã sắp xếp
```

Ví dụ, với danh sách số sau:

`6 3 4 1`

Đầu tiên, thuật toán hỏi, “đây có phải là một số không?” Câu trả lời là “không,” vì vậy thuật toán tiếp tục.

Bước hai, chia các số làm hai nửa (hoặc gần nhất có thể) và sắp xếp nửa bên trái của các số.

`6 3 | 4 1`

Bước ba, xem xét các số bên trái và hỏi, “đây có phải là một số không?” Vì câu trả lời là không, nó sẽ chia các số bên trái làm đôi.

`6 | 3`

Bước bốn, xem xét lần nữa, “đây có phải là một số không?” Câu trả lời là có! Vì vậy, nó sẽ dừng lại nhiệm vụ này và quay lại nhiệm vụ trước đó:

`6 3 | 4 1`

Bước năm, sắp xếp các số bên trái.

`3 6 | 4 1`

Bây giờ, sau khi nửa bên trái đã được sắp xếp. Quá trình tương tự từ bước 3-5 sẽ diễn ra cho các số bên phải. Kết quả sẽ là:

`3 6 | 1 4`

Cả hai nửa bây giờ đã được sắp xếp. Cuối cùng, thuật toán sẽ trộn cả hai bên. Nó sẽ xem xét số đầu tiên ở bên trái và số đầu tiên ở bên phải. Đặt số nhỏ hơn lên trước, sau đó là số nhỏ thứ hai. Thuật toán sẽ lặp lại điều này cho tất cả các số và trả về kết quả:

`1 3 4 6`

Sắp xếp trộn đã hoàn thành, và chương trình dừng lại.

Sắp xếp trộn là một thuật toán sắp xếp rất hiệu quả với trường hợp xấu nhất là O(n log n). Trường hợp tốt nhất vẫn là Ω(n log n) vì thuật toán vẫn phải duyệt qua từng vị trí trong danh sách.

\
Tóm lại, ***Sắp xếp trộn*** thường là lựa chọn tốt nhất cho các tập dữ liệu lớn nhờ vào hiệu suất của nó, nhưng nó yêu cầu thêm không gian để lưu trữ các mảng con đã được hợp nhất. ***Sắp xếp chọn và sắp xếp nổi bọt*** dễ triển khai hơn nhưng không phù hợp cho các đầu vào lớn.

\
Và đó là kết thúc của tuần 3 ^^