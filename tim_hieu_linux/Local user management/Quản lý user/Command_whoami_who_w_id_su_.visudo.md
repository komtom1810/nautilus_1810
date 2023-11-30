# Command: whoami, who, w, id, su, visudo
## 1. Whoami
Lệnh whoami được sử dụng để hiển thị tên đăng nhập của người dùng hiện tại. Khi chạy lệnh này trong terminal, nó sẽ trả về tên đăng nhập của bạn.

VD: `whoami` 

Kết quả có thể là tên đăng nhập của bạn trên hệ thống, chẳng hạn như: `your_username`

## 2.who
Lệnh `who` được sử dụng để hiển thị thông tin về người dùng đang đăng nhập vào hệ thống. Khi bạn chạy lệnh này trong terminal, nó sẽ liệt kê tất cả các người dùng hiện đang đăng nhập, bao gồm tên đăng nhập, địa chỉ IP, thời gian đăng nhập và nơi đăng nhập (nếu có).

Ví dụ: `who`

Kết quả như sau:

`username1  pts/0        2023-11-20 10:00 (192.168.1.100)`

`username2  pts/1        2023-11-20 10:15 (192.168.1.101)`

Ở đây:

- `username1` và `username2` là tên đăng nhập của người dùng.

- `pts/0` và `pts/1` là các phiên đăng nhập tương ứng với terminal.

- `2023-11-27 10:00` là thời gian đăng nhập.

- `(192.168.1.100)` và `(192.168.1.101)` là địa chỉ IP của người dùng.

## 3.w
Lệnh `w` được sử dụng để hiển thị thông tin chi tiết về người dùng hiện đang đăng nhập và các tiến trình đang chạy. Khi chạy lệnh này trong terminal, nó sẽ cung cấp thông tin như tên đăng nhập, thời gian làm việc, thời gian hệ thống đang chạy, và các tiến trình hiện đang thực thi.

VD: `w`

Kết quả như sau:

 `10:47:49 up 1 day,  2:30,  2 users,  load average: 0.08, 0.15, 0.20`

`USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT`

`user1    :0       :0               09:17   ?xdm?  1:22   0.01s /usr/lib/gdm3/gdm-x-session --run-script env GNOME_S`

`user2    pts/0    :1.0             10:00   25:44   0.10s  0.10s /bin/bash`

Ở đây:

- `USER`: Tên đăng nhập của người dùng.
- `TTY`: Terminal nơi người dùng đang đăng nhập.
- `FROM`: Nguồn đăng nhập hoặc địa chỉ IP.
- `LOGIN`@: Thời gian đăng nhập.
- `IDLE`: Thời gian người dùng không hoạt động.
- `JCPU`: Tổng thời gian CPU sử dụng (đơn vị: phút).
- `PCPU`: Thời gian CPU sử dụng gần đây (đơn vị: phút).
- `WHAT`: Các tiến trình đang chạy cho người dùng.

## 4.id
Lệnh `id` trong Linux được sử dụng để hiển thị thông tin về user và group IDs của người dùng hiện tại hoặc của người dùng được chỉ định. Khi bạn chạy lệnh này trong terminal, nó sẽ trả về UID (User ID), GID (Group ID), và các thông tin về các nhóm mà người dùng thuộc.

**Hiển thị thông tin về người dùng hiện tại:** `id`

Kết quả như sau:

`uid=1000(username) gid=1000(username) groups=1000(username),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),116(lpadmin),126(sambashare)`

Ở đây:

- `uid=1000`: User ID là 1000.
- `gid=1000`: Group ID là 1000.
- `groups=1000,4,24,27,30,46,116,126`: Các nhóm mà người dùng thuộc.

## 5.su
Lệnh `su` trong Linux được sử dụng để chuyển đổi người dùng (switch user) hoặc thực thi lệnh dưới quyền của một người dùng khác mà không cần đăng xuất khỏi phiên làm việc hiện tại.

**Chuyển đổi đến người dùng khác:** `su - ten_nguoi_dung`

VD: `su - ducanh`

Sau khi nhập lệnh, bạn sẽ được yêu cầu nhập mật khẩu của người dùng mới (trong trường hợp ví dụ là ducanh). Nếu mật khẩu đúng, bạn sẽ chuyển đến phiên làm việc của người dùng đó.

**Thực thi lệnh dưới quyền của người dùng khác:**
`su -c "lenh_can_thuc_hien" ten_nguoi_dung`

VD: `su -c "ls /root" ducanh`

Lệnh này sẽ thực hiện `ls /root` dưới quyền của người dùng `ducanh`.

Lưu ý rằng nếu bạn sử dụng `su` mà không chỉ định người dùng cụ thể, nó sẽ mặc định chuyển đến người dùng root:

`su -`

Sau khi nhập lệnh, bạn sẽ được yêu cầu nhập mật khẩu của root để chuyển đến phiên làm việc root.

## 6.sudo
Lệnh `sudo` trong Linux được sử dụng để thực hiện các lệnh với quyền hạn superuser (hoặc của một người dùng khác) mà người dùng hiện tại không có.

Cú pháp cơ bản của lệnh sudo là: `sudo lenh_can_thuc_hien`

VD: `sudo apt-get update`
Trong ví dụ trên, `sudo` được sử dụng để thực hiện lệnh `apt-get update` với quyền hạn superuser. Khi bạn chạy lệnh này, hệ thống sẽ yêu cầu bạn nhập mật khẩu để xác thực quyền hạn.

Nếu người dùng có quyền thực hiện lệnh `sudo`, họ sẽ được thêm vào nhóm sudo trong file `/etc/sudoers`. 

Lệnh `sudo su -` được sử dụng để chuyển đến tài khoản root trên hệ thống Linux. Khi bạn chạy lệnh này, nó sẽ yêu cầu bạn nhập mật khẩu của người dùng hiện tại để xác thực quyền hạn, và sau đó chuyển đến tài khoản root.

Sau khi nhập mật khẩu, bạn sẽ thấy dấu nhắc của root (`root@yourhostname:/home/yourusername#`). Bạn đang ở trong môi trường làm việc của tài khoản root và có thể thực hiện các lệnh với đặc quyền tối cao.

Lưu ý rằng việc sử dụng `sudo su -` để đăng nhập trực tiếp vào tài khoản root không được khuyến khích vì có thể tạo ra một số vấn đề liên quan đến an toàn và quản lý. Thay vào đó, thường thì sử dụng `sudo` để thực hiện các lệnh đặc quyền mà không cần đăng nhập trực tiếp vào tài khoản root.

## 7.visudo
Lệnh `visudo` trong Linux được sử dụng để chỉnh sửa và kiểm tra cấu hình file `/etc/sudoers`. File này quy định các quyền hạn và cấu hình sudo (superuser do) trên hệ thống.

`sudo visudo`

Khi bạn chạy lệnh này, nó sẽ mở file `/etc/sudoers` trong một trình soạn thảo văn bản an toàn (thường là `vi` hoặc `nano`) và kiểm tra cú pháp của file trước khi lưu thay đổi. Nếu có lỗi cú pháp, `visudo` sẽ thông báo cho bạn và không lưu thay đổi, giữ cho file `/etc/sudoers` không bị hỏng.

Lưu ý rằng chỉnh sửa file `/etc/sudoers` trực tiếp bằng trình soạn thảo thông thường không được khuyến khích vì có thể dẫn đến lỗi cú pháp và khả năng không thể đăng nhập hoặc sử dụng `sudo`. Sử dụng `visudo` giúp đảm bảo an toàn khi chỉnh sửa file sudoers.

