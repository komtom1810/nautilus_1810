# Mã hóa mật khẩu
Mật khẩu trong Linux, bao gồm cả Ubuntu, được lưu trữ dưới dạng bản mã hóa trong tệp `/etc/shadow`. Hệ thống sử dụng một thuật toán băm (hashing algorithm) để bảo vệ mật khẩu người dùng. Phổ biến nhất là sử dụng thuật toán băm SHA-512 hoặc SHA-256.

Khi bạn tạo hoặc thay đổi mật khẩu cho một người dùng, hệ thống sẽ tự động áp dụng thuật toán băm và lưu trữ mật khẩu đã được băm trong `/etc/shadow`. Dưới đây là một số cách thực hiện việc này:

1. Sử dụng lệnh `passwd`:
`sudo passwd username`

Khi chạy lệnh này, hệ thống sẽ yêu cầu bạn nhập mật khẩu mới và sau đó lưu trữ mật khẩu đã được băm.

2. Sử dụng lệnh `useradd`:

Khi bạn tạo một người dùng mới, mật khẩu của họ cũng sẽ được băm tự động:

`sudo useradd -m username`

`sudo passwd username`

3. Sử dụng chương trình Openssl:

Để mã hóa mật khẩu bằng OpenSSL, bạn có thể sử dụng lệnh sau:

`openssl passwd -1 "your_password"`

Trong đó, "your_password" là mật khẩu bạn muốn mã hóa. OpenSSL sẽ sử dụng thuật toán MD5 để mã hóa mật khẩu trong ví dụ trên.

Nếu bạn muốn sử dụng một thuật toán mã hóa khác, bạn có thể thay thế `-1` bằng các tùy chọn khác nhau. Dưới đây là một số ví dụ:

Sử dụng SHA-256:

`openssl passwd -6 "your_password"`

Sử dụng SHA-512:

`openssl passwd -5 "your_password"`

Sau khi chạy lệnh, bạn sẽ nhận được một chuỗi mã hóa mật khẩu, và bạn có thể sử dụng nó để lưu trữ hoặc so sánh với mật khẩu đã nhập sau này.