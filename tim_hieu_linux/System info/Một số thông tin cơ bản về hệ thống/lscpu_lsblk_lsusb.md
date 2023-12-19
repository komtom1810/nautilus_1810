# lscpu, lsblk, lsusb
## lscpu
Lệnh `lscpu` là một tiện ích dòng lệnh trong hệ điều hành Linux được sử dụng để hiển thị thông tin về CPU (Central Processing Unit) trên hệ thống của bạn. Khi bạn chạy lệnh `lscpu` từ dòng lệnh, nó sẽ cung cấp một bản tóm tắt về thông số kỹ thuật của CPU.

VD sử dụng lscpu: `lscpu`

Kết quả như sau:

![](https://linuxhint.com/wp-content/uploads/2021/04/1-5.jpg)

- Một số thông tin quan trọng mà `lscpu` có thể cung cấp bao gồm:

+ **Architecture:** Kiến trúc của CPU (ví dụ: x86_64).
+ **CPU op-mode(s):** Chế độ hoạt động của CPU (32-bit, 64-bit).
+ **CPU(s):** Số lượng CPU trên hệ thống.
+ **Core(s) per socket:** Số lượng lõi per socket.
+ **Thread(s) per core:** Số lượng luồng per lõi.
+ **Model name:** Tên và mô hình của CPU.
+ **CPU MHz:** Tốc độ xung nhịp của CPU.
+ **L1d cache, L1i cache, L2 cache, L3 cache:** Kích thước của các cấp bộ nhớ cache.
+ **Virtualization:** Hỗ trợ ảo hóa (ví dụ: VT-x cho Intel, AMD-V cho AMD).
Thông tin từ lscpu có thể hữu ích để đánh giá khả năng và cấu hình của CPU trên hệ thống Linux của bạn.

## lsblk
Lệnh `lsblk` là một tiện ích dòng lệnh trong hệ điều hành Linux được sử dụng để liệt kê thông tin về các thiết bị lưu trữ block trên hệ thống của bạn. Khi bạn chạy lệnh `lsblk` từ dòng lệnh, nó sẽ hiển thị một bảng tóm tắt về các ổ đĩa, phân vùng và thiết bị khác trên hệ thống.

VD sử dụng `lsblk`: `lsblk`
Kết quả:

![](https://linuxopsys.com/wp-content/uploads/2022/06/lsblk-list-06-2022-03.png)

- Một số thông tin quan trọng mà `lsblk` có thể cung cấp bao gồm:

+ **NAME:** Tên thiết bị.
+ **MAJ:MIN:** Số hiệu thiết bị major và minor.
+ **RM:** Loại thiết bị (removable hay không).
+ **SIZE:** Dung lượng của thiết bị.
+ **RO:** Cho biết thiết bị có thể đọc-only hay không.
+ **TYPE:** Loại thiết bị (disk, part - phân vùng).
+ **MOUNTPOINT:** Điểm mount của thiết bị nếu có.

Thông tin từ `lsblk` giúp bạn có cái nhìn tổng quan về cấu trúc ổ đĩa và phân vùng trên hệ thống của bạn, và nó thường được sử dụng để kiểm tra sự kết nối và sử dụng của các thiết bị lưu trữ block.

## lsusb
Lệnh `lsusb` là một tiện ích dòng lệnh trong hệ điều hành Linux được sử dụng để liệt kê thông tin về các thiết bị USB kết nối với hệ thống của bạn. Khi bạn chạy lệnh `lsusb` từ dòng lệnh, nó sẽ hiển thị danh sách các thiết bị USB và chi tiết về chúng.

VD sử dụng `lsusb`: `lsusb`

Kết quả:

![](https://media.geeksforgeeks.org/wp-content/uploads/20190421121309/Screenshot-from-2019-04-21-11-42-47.png)

- Mỗi dòng thông tin thường chứa các phần như sau:

+ **Bus:** Số bus USB.
+ **Device:** Số thiết bị trên bus.
+ **ID:** Mã sản phẩm và mã nhà sản xuất của thiết bị USB.

Thông tin từ `lsusb` rất hữu ích để kiểm tra xem các thiết bị USB đã được nhận diện đúng cách hay không, và cung cấp thông tin chi tiết về chúng như nhà sản xuất và mã sản phẩm.




