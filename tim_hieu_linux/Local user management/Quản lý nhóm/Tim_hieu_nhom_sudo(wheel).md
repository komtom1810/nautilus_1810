# Tìm hiểu nhóm sudo wheel
Nhóm `sudo` hay `wheel` là một nhóm người dùng trên hệ thống Linux thường được sử dụng để quản lý quyền truy cập sudo (superuser do) cho các người dùng. Nhóm này được sử dụng để cấp quyền truy cập sudo, cho phép người dùng thực hiện các lệnh với đặc quyền root hoặc quyền người quản trị hệ thống mà không cần đăng nhập trực tiếp với tài khoản root.

1. **`sudo` Group:**

- Trong các phiên bản của hệ thống Linux như Ubuntu, thành viên của nhóm `sudo` có thể sử dụng lệnh `sudo` để thực hiện các lệnh với đặc quyền root.
- Một số hệ thống có thể sử dụng `wheel` thay vì `sudo`, nhưng cơ bản chúng đều có mục đích tương tự.
2. **`wheel` Group:**

- Trong một số hệ thống Linux như Fedora hoặc CentOS, nhóm `wheel` được sử dụng như một nhóm tương tự nhóm `sudo`.
- Các thành viên của nhóm `wheel` có quyền sử dụng sudo để thực hiện các lệnh với đặc quyền root.
Để thêm một người dùng vào nhóm `sudo` hoặc `wheel`, bạn thường cần chỉnh sửa tệp `/etc/group` hoặc sử dụng lệnh `usermod`. Ví dụ:

`sudo usermod -aG sudo tên_người_dùng`  # Trên Ubuntu hoặc Debian

hoặc

`sudo usermod -aG wheel tên_người_dùng`  # Trên Fedora hoặc CentOS

Sau khi thêm người dùng vào nhóm, họ có thể sử dụng `sudo` để thực hiện các lệnh với đặc quyền root. Lưu ý rằng đối với một số hệ thống, bạn có thể cần đăng nhập lại hoặc mở một phiên làm việc mới để các thay đổi được áp dụng.
