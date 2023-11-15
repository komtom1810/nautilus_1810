# Các kiểu command: external or builtin commands, alias
## 1.External commands
External commands trong Linux là các lệnh không được tích hợp trực tiếp vào shell mà chúng được triển khai dưới dạng các tập tin thực thi độc lập hoặc là các chương trình nằm trong các thư mục đã được thiết lập trong biến môi trường PATH. Dưới đây là một số external commands phổ biến:
- **`ls`:** Liệt kê các tệp tin và thư mục trong một thư mục.
- **`cp`:** Sao chép tệp tin hoặc thư mục từ một vị trí đến một vị trí khác.
- **`mv`:** Di chuyển hoặc đổi tên tệp tin hoặc thư mục.
- **`rm`:** Xóa tệp tin hoặc thư mục.
- **`mkdir`:** Tạo một thư mục mới.
- **`rmdir`:** Xóa một thư mục trống.
- **`cat`:** Hiển thị nội dung của một hoặc nhiều tệp tin.
- **`grep`:** Tìm kiếm một chuỗi trong tệp tin hoặc đầu ra của một lệnh.
- **`chmod`:** Thay đổi quyền truy cập của tệp tin hoặc thư mục.
- **`ps`:** Hiển thị trạng thái của các tiến trình đang chạy.
- **`df`:** Hiển thị thông tin về không gian đĩa còn trống.
- **`ifconfig`:** Hiển thị và quản lý cấu hình của các giao diện mạng.
- **`ping`:** Gửi các gói tin ICMP để kiểm tra kết nối mạng
.
.
.

## 2.Built-in commands
Built-in commands trong Linux là các lệnh được tích hợp sẵn trong shell, chúng được thực hiện bởi shell mà không cần tạo một tiến trình riêng biệt. Dưới đây là một số built-in commands phổ biến:
- **`cd`:** Thay đổi thư mục làm việc hiện tại.
- **`pwd`:** In ra đường dẫn của thư mục làm việc hiện tại.
- **`echo`:** In ra một chuỗi hoặc giá trị của biến.
- **`export`:** Đặt giá trị cho biến môi trường.
- **`alias`:** Tạo một bí danh (alias) cho một lệnh dài và phức tạp.
- *`unset`:** Loại bỏ một biến môi trường.
- **`history`:** Hiển thị lịch sử các lệnh đã nhập.
- **`exit`:** Thoát khỏi môi trường shell hoặc kết thúc một script.
- **`source hoặc .`:** Đọc và thực hiện các lệnh từ một tệp script trong ngữ cảnh hiện tại của shell.
- **`type`:** Hiển thị thông tin về loại lệnh (internal command, external command, alias).
- **`help`:** Hiển thị trợ giúp về các built-in commands.
.
.
.

## 3.Alias commands
Trong Linux, lệnh **alias** được sử dụng để tạo bí danh (alias) cho các lệnh dài hoặc phức tạp, hoặc thậm chí để tạo các biến môi trường ngắn gọn. Alias giúp tiết kiệm thời gian và công sức khi nhập các lệnh dài thường xuyên. Dưới đây là cách sử dụng lệnh **alias**:
**Cú pháp cơ bản:**
**`alias alias_name='command'`**
Ví dụ:
- **Tạo alias để thực hiện ls -l khi nhập ll:**
`alias ll='ls -l'`. 
Bây giờ, khi gõ ll và nhấn Enter, nó sẽ thực hiện lệnh ls -l.
- **Tạo alias để di chuyển đến thư mục cụ thể:**
`alias mycd='cd /path/to/my/directory'`. 
Khi gõ mycd và nhấn Enter, nó sẽ đưa bạn đến thư mục đã được đặt trước.
- **Tạo alias với tham số:**
`alias greetme='echo Hello'`. 
Bây giờ, khi bạn gõ `greetme DucAnh` và nhấn Enter, nó sẽ in ra `Hello DucAnh`.
- **Xóa alias:**
`unalias ll1`'. 
Lệnh này sẽ xóa alias ll đã tạo trước đó.
- **Hiển thị danh sách các alias đang tồn tại:**
`alias`. 
Lệnh này sẽ hiển thị tất cả các alias đang được định nghĩa.

**Lưu ý:**
Alias thường chỉ tồn tại trong phiên làm việc hiện tại. Để giữ alias tồn tại giữa các phiên làm việc, bạn có thể thêm lệnh tạo alias vào tệp cấu hình shell của bạn (ví dụ: `~/.bashrc` hoặc `~/.bash_profile`).

Nếu bạn muốn sử dụng alias ngay lập tức mà không phải mở một phiên làm việc mới, bạn có thể chạy lệnh `source ~/.bashrc` (hoặc tương tự tùy thuộc vào tên tệp cấu hình shell của bạn).




