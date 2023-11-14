# Hệ thống phân cấp trong linux

Hệ thống phân cấp trong Linux là cách mà thư mục và tệp được tổ chức thành một cây thư mục, tạo nên một cấu trúc hệ thống tệp phân cấp. Dưới đây là mô tả về một số thư mục quan trọng trong hệ thống phân cấp Linux:

## 1.Thư mục gốc:
- **/ (Thư mục Gốc):** Là thư mục cao nhất trong hệ thống tệp Linux. Tất cả các thư mục và tệp tin đều nằm trong thư mục gốc. Biểu tượng là /.

## 2.Thư mục chứa các thư viện: 
- **/bin (Binary):** Chứa các tệp thực thi (chương trình nhị phân) cần thiết để khởi động hệ thống và thực hiện các tác vụ cơ bản khi hệ thống chưa được mount.
- **/sbin (System Binary):** Chứa các tệp thực thi chủ yếu dành cho quản trị hệ thống và các tác vụ hệ thống cơ bản.
- **/lib (Library):** Chứa các thư viện chia sẻ cần thiết cho các chương trình thực thi ở /bin và /sbin.
- **/opt (Optional):** Thư mục cho các ứng dụng thêm vào, không phải là một phần của phân phối hệ điều hành chính.

## 3.Thư mục cấu hình:
- **/etc (Etcetera):** Chứa các tệp cấu hình hệ thống và ứng dụng. Các tệp trong /etc thường được sửa đổi để cấu hình hệ thống.
- **/boot:** Chứa các file cần thiết để khởi động hệ thống, bao gồm cả kernel và các tệp cấu hình khởi động.

## 4.Thư mục dữ liệu:
- **/home:** Là thư mục chứa các thư mục cá nhân cho từng người dùng. Mỗi người dùng có một thư mục riêng tại /home/username.
- **/root:** Thư mục home của người quản trị hệ thống (root user).
- **/srv (Service):** Thường được sử dụng để chứa dữ liệu cho các dịch vụ cụ thể chạy trên hệ thống.
- **/media:** Thường được sử dụng làm thư mục tạm thời để gắn kết các thiết bị lưu trữ tạm thời, như USB hoặc DVD.
- **/mnt (Mount):** Thường được sử dụng làm thư mục để gắn kết các thiết bị lưu trữ tạm thời hoặc từ xa.
- **/tmp (Temporary):** Chứa các tệp tạm thời được tạo bởi các chương trình và người dùng.

## 5.Thư mục chứa trong RAM:
- **/dev (Device):** Chứa các file đại diện cho các thiết bị phần cứng trên hệ thống, ví dụ như /dev/sda là ổ đĩa đầu tiên.
- **/proc (Process):** Chứa thông tin về các tiến trình đang chạy trên hệ thống.
- **/sys (System):** Chứa thông tin về hệ thống và các thiết bị.

## 6.Thư mục tài nguyên hệ thống:
- **/usr (Unix System Resources):** Chứa các tệp nhị phân, thư viện, hình ảnh, và dữ liệu của ứng dụng.
- **/usr/bin:** Chứa các tệp thực thi (chương trình nhị phân) của ứng dụng cài đặt từ các gói.
- **/usr/include:** Chứa các tệp tiêu đề (header files) cần thiết để phát triển ứng dụng.
- **/usr/lib:** Chứa các thư viện cần thiết cho các ứng dụng nằm trong **`/usr/bin`** và **`/usr/sbin`**. Các thư mục con như **`/usr/lib32`** và **`/usr/lib64`** có thể tồn tại để hỗ trợ thư viện 32-bit và 64-bit trên các hệ thống 64-bit.
- **/usr/local:** Thư mục này thường chứa các ứng dụng và tệp cài đặt từ nguồn cài đặt hoặc từ các gói không phải là phần của hệ thống cơ bản.
- **/usr/share:** Chứa dữ liệu chia sẻ giữa các ứng dụng, chẳng hạn như tệp ngôn ngữ, hình ảnh, âm thanh, và tài nguyên khác.
- **/usr/src:** Chứa mã nguồn (source code) của kernel Linux hoặc các gói cài đặt khác.

## 7.Thư mục biến động: 
- **/var (Variable)**: Chứa dữ liệu biến đổi khi hệ thống đang chạy, chẳng hạn như các file log (/var/log), tệp tạm thời (/var/tmp),...
- **/var/log:** Chứa các file log của hệ thống và các ứng dụng. Các log này giúp theo dõi sự kiện và lỗi trong hệ thống.
- **/var/lib:** Chứa dữ liệu biến đổi của các ứng dụng và hệ thống, như cơ sở dữ liệu.
- **/var/mail:** Thường được sử dụng để lưu trữ hộp thư (mailbox) của người dùng khi họ nhận thư điện tử. 


Hệ thống phân cấp Linux này giúp tổ chức và quản lý các tệp và thư mục một cách có tổ chức, cho phép người quản trị và người sử dụng dễ dàng tìm và quản lý dữ liệu.