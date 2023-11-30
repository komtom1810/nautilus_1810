# File /etc/login.defs
Tệp `/etc/login.defs` là một tệp cấu hình trên hệ thống Linux, chứa các cài đặt và quy tắc liên quan đến quá trình đăng nhập và quản lý tài khoản người dùng. Cụ thể, nó chứa các thông số mặc định cho việc quản lý mật khẩu và quản lý tài khoản.

Dưới đây là một số cài đặt thông thường mà bạn có thể tìm thấy trong tệp `/etc/login.defs`:

- `PASS_MAX_DAYS`: Số ngày tối đa giữa các lần thay đổi mật khẩu.
- `PASS_MIN_DAYS`: Số ngày tối thiểu giữa các lần thay đổi mật khẩu.
- `PASS_WARN_AGE`: Số ngày trước khi hệ thống bắt đầu cảnh báo về việc sắp hết hạn mật khẩu.
- `UID_MIN và UID_MA`X: Giới hạn dưới và trên của dải UID có sẵn cho người dùng.
- `GID_MIN và GID_MAX`: Giới hạn dưới và trên của dải GID có sẵn cho nhóm.
- `LOGIN_RETRIES`: Số lần thử đăng nhập không thành công trước khi tài khoản bị khoá.

- `ENCRYPT_METHOD`: Phương pháp mã hóa mật khẩu được sử dụng. Điều này có thể là "DES", "MD5", "SHA256", hoặc "SHA512", tùy thuộc vào phiên bản của hệ điều hành.

Lưu ý rằng tùy thuộc vào phiên bản và cấu hình cụ thể của hệ thống bạn đang sử dụng, các cài đặt có thể thay đổi. Để xem nội dung của tệp `/etc/login.defs`, bạn có thể mở nó bằng trình soạn thảo văn bản như `nano` hoặc `vi`.