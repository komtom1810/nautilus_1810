# Banner login 
Để chỉnh sửa banner login khi đăng nhập vào hệ thống Linux, bạn thường cần chỉnh sửa một trong các tệp cấu hình sau đây:

1. `/etc/issue`:

- Mở tệp `/etc/issue` bằng trình soạn thảo văn bản, ví dụ:

`sudo nano /etc/issue`

- Chèn nội dung bạn muốn hiển thị. Ví dụ:

`Welcome to My Linux System`

`System status: Online`

- Lưu và đóng tệp.

2. `/etc/issue.net`:

- Một số hệ thống sử dụng tệp `/etc/issue.net` để hiển thị banner login khi đăng nhập từ xa (remote login). Thực hiện tương tự như `/etc/issue`.

`sudo nano /etc/issue.net`

3. `/etc/motd`:

- Tệp `/etc/motd` chứa thông điệp hiển thị sau khi người dùng đăng nhập thành công.

`sudo nano /etc/motd`

4. `/etc/update-motd.d/`:

- Thư mục `/etc/update-motd.d/` có thể chứa các tệp thực thi để tạo nội dung động cho banner login. Các tệp trong thư mục này được thực thi mỗi khi có người dùng đăng nhập.

- Chỉnh sửa các tệp trong thư mục này nếu bạn muốn tạo nội dung động.

- Ví dụ, bạn có thể sửa đổi tệp `/etc/update-motd.d/10-help-text`:

`sudo nano /etc/update-motd.d/10-help-text`

5. `/etc/pam.d/login`:

Một số hệ thống sử dụng PAM (Pluggable Authentication Modules) để quản lý quá trình đăng nhập. Bạn có thể thêm dòng sau vào tệp `/etc/pam.d/login` để hiển thị banner:

`session    optional     pam_exec.so /etc/motd`

Lưu ý rằng việc chỉnh sửa `/etc/pam.d/login` có thể yêu cầu sự cẩn trọng, và bạn nên tạo sao lưu trước khi thực hiện.

Sau khi thay đổi, bạn có thể đăng nhập lại hoặc mở một cửa sổ terminal mới để xem banner login đã được cập nhật. Lưu ý rằng một số thay đổi có thể yêu cầu quyền quản trị (sudo).





