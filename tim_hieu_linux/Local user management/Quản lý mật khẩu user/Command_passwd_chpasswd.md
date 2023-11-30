# Command passwd, chpasswd
## passwd
Lệnh `passwd` trong Linux được sử dụng để thay đổi hoặc đặt lại mật khẩu cho một người dùng cụ thể. Khi bạn chạy lệnh `passwd` mà không có thêm đối số, nó sẽ yêu cầu bạn nhập mật khẩu mới cho tài khoản của bạn.

Cú pháp cơ bản của lệnh `passwd` là: `passwd [tùy_chọn] [tên_người_dùng]`

Trong đó:

- `[tùy_chọn]`: Là một số tùy chọn có thể đi kèm với lệnh. Một số tùy chọn phổ biến bao gồm:

- `-l`: Khóa mật khẩu người dùng.
- `-u`: Mở khóa mật khẩu người dùng.
- `-d`: Xóa mật khẩu của người dùng.
- `-S`: Hiển thị trạng thái mật khẩu của người dùng.
- `[tên_người_dùng]`: Là tên người dùng cho mà bạn muốn thay đổi mật khẩu. Nếu không có tên người dùng nào được cung cấp, mật khẩu của người dùng hiện tại (đang thực hiện lệnh) sẽ được thay đổi.

Nếu bạn chạy lệnh mà không có đối số, nó sẽ thay đổi mật khẩu cho tài khoản người dùng hiện tại. Nếu bạn muốn thay đổi mật khẩu cho một người dùng khác, hãy chỉ định tên người dùng:

`passwd ducanh`  # Thay đổi mật khẩu cho người dùng có tên là "ducanh"

Khi bạn chạy lệnh này, hệ thống sẽ yêu cầu bạn nhập mật khẩu mới và sau đó xác nhận nó.

Lưu ý rằng để thực hiện các thay đổi đối với tài khoản root hoặc sử dụng lệnh `passwd` để đặt lại mật khẩu trong một số trường hợp (như khi sử dụng chế độ khôi phục), bạn có thể cần có quyền đặc quyền hoặc quyền root.

## chpasswd
Lệnh `chpasswd` trong Linux được sử dụng để thay đổi nhiều mật khẩu người dùng cùng một lúc thông qua đầu vào từ đường ống hoặc tệp văn bản. Nó cho phép bạn thay đổi mật khẩu cho nhiều người dùng một cách thuận tiện.

Cú pháp cơ bản của lệnh `chpasswd` là:
`chpasswd [options]`

Lệnh này thường được kết hợp với đầu vào từ đường ống hoặc từ tệp văn bản. Ví dụ, nếu bạn có một tệp văn bản chứa tên người dùng và mật khẩu, bạn có thể sử dụng `chpasswd` như sau:
`chpasswd < /path/to/password_file`

Trong tệp văn bản, mỗi dòng thường chứa một cặp "tên người dùng:mật khẩu", ví dụ:

`user1:password1`

`user2:password2`

Lưu ý rằng để sử dụng lệnh `chpasswd`, bạn có thể cần quyền đặc quyền hoặc quyền root tùy thuộc vào việc thay đổi mật khẩu của người dùng nào.

Lệnh này thường hữu ích trong các kịch bản tự động hóa hoặc khi bạn muốn đặt lại mật khẩu cho nhiều người dùng cùng một lúc.












