# Thực hiện command dưới quyền sudo
Để thực hiện một lệnh dưới quyền sudo, bạn có thể sử dụng cú pháp sau:
`sudo lệnh [tùy_chọn]`

Trong đó:

- `sudo`: Là lệnh để chạy một lệnh với quyền root hoặc quyền của một người dùng khác có quyền `sudo`.
- `lệnh`: Là lệnh mà bạn muốn thực hiện với quyền `sudo`.
- `[tùy_chọn]`: Là các tùy chọn có thể đi kèm với lệnh(`-h`,`-V`,`-v`,`-l`,`-k`)
    

Ví dụ:

1. Để cài đặt một gói phần mềm bằng `apt` trên Ubuntu, bạn có thể sử dụng:

`sudo apt-get install tên_gói`

2. Sử dụng `visudo` và nhóm `sudoers`

Trong một số phiên bản Linux hiện đại, người dùng được thêm vào tệp `sudoers` để cấp đặc quyền. Việc này được thực hiện bằng lệnh `visudo`

- Sử dụng lệnh visudo để chỉnh sửa file cấu hình: `sudo visudo`
- Thao tác này sẽ mở `/etc/sudoers` để chỉnh sửa. Để thêm người dùng và cấp đầy đủ đặc quyền sudo

Khi bạn chạy lệnh `sudo`, bạn có thể được yêu cầu nhập mật khẩu người dùng hiện tại của bạn để xác thực. Sau khi nhập mật khẩu đúng, lệnh sẽ được thực hiện với quyền `sudo`.

Lưu ý: Để sử dụng `sudo`, bạn cần được thêm vào danh sách người dùng có quyền sudo trong tệp cấu hình `/etc/sudoers`. Sử dụng lệnh `visudo` để chỉnh sửa tệp này một cách an toàn.






