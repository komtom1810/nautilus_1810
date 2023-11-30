# Shadow file: /etc/shadow
File `/etc/shadow` trong Linux lưu trữ các thông tin về mật khẩu của người dùng. Thay vì chứa mật khẩu trực tiếp như trong file `/etc/passwd`, file `/etc/shadow` chứa một bản mã hóa của mật khẩu cùng với các thông tin bảo mật khác.

Cấu trúc của mỗi dòng trong file `/etc/shadow` thường sẽ có dạng như sau:

`username:password:last_change:min_age:max_age:warn_days:inactive_days:expire_date:reserved`

Trong đó:

- `username`: Tên người dùng.
- `password`: Bản mã hóa của mật khẩu.
- last_change: Ngày thay đổi mật khẩu lần cuối (tính bằng số ngày kể từ ngày 1/1/1970).
- `min_age`: Số ngày tối thiểu mà người dùng phải giữ mật khẩu trước khi có thể đổi nó.
- `max_age`: Số ngày tối đa mà mật khẩu có thể được sử dụng.
- `warn_days`: Số ngày trước khi mật khẩu hết hạn mà hệ thống sẽ bắt đầu cảnh báo người dùng.
- `inactive_days`: Số ngày mà một tài khoản có thể không hoạt động trước khi bị vô hiệu hóa.
- `expire_date`: Ngày mật khẩu hết hạn (tính bằng số ngày kể từ ngày 1/1/1970).
- `reserved`: Trường dữ liệu dự phòng (được sử dụng cho mục đích tương lai).

Lưu ý rằng `password` được lưu dưới dạng bản mã hóa và không thể đọc được. Chỉ có các công cụ quản trị hệ thống hoặc người dùng có quyền đặc quyền mới có thể truy cập và sửa đổi file `/etc/shadow`.





