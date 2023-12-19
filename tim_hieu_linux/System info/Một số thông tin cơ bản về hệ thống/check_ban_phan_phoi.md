# Check bản phân phối
Để kiểm tra bản phân phối Linux (Linux distribution) mà bạn đang sử dụng từ dòng lệnh, bạn có thể sử dụng một số lệnh khác nhau tùy thuộc vào bản phân phối cụ thể của bạn. Dưới đây là một số cách phổ biến:

1. **Lệnh lsb_release:** `lsb_release -a`

- Kết quả:

![](https://beebom.com/wp-content/uploads/2022/11/Screenshot-from-2022-11-18-09-37-16.jpg?w=640)

2. **Đọc tệp /etc/os-release:** `cat /etc/os-release`

- Kết quả có chứa thông tin như `NAME`, `VERSION`, và `ID`.

![](https://itslinuxfoss.com/wp-content/uploads/2022/11/lsb_release-Linux-Command-Explained-9.png)

3. **Đọc tệp /etc/issue:** `cat /etc/issue`

Kết quả có chứa thông tin về tên bản phân phối và phiên bản.

4. **Kiểm tra tệp /etc/redhat-release:** `cat /etc/redhat-release`
Đối với các bản phân phối dựa trên Red Hat (như CentOS hoặc Fedora), thông tin có thể hiển thị trong tệp này.

5. **Kiểm tra uname:** `uname -a`
Kết quả có thể chứa thông tin về hạt nhân Linux và phiên bản.

6. **Kiểm tra /proc/version:** `cat /proc/version`
Tệp này cung cấp thông tin về hạt nhân Linux và bản phân phối.

![](https://linuxhint.com/wp-content/uploads/2022/10/The-proc-File-System-3.png)

Mỗi trong số các lệnh này có thể cung cấp thông tin về bản phân phối Linux và phiên bản của nó. Chọn lệnh phù hợp với hệ thống bạn đang sử dụng.





