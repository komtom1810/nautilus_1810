# Command user management
## 1./etc/passwd
File `/etc/passwd` trong Linux chứa thông tin về các tài khoản người dùng trên hệ thống. Mỗi dòng trong file này đại diện cho một người dùng và chứa các thông tin cụ thể về tài khoản. Dưới đây là cấu trúc của mỗi dòng trong file `/etc/passwd`:

`username:password:UID:GID:GECOS:home_directory:shell`

Trong đó:

- `username`: Tên đăng nhập của người dùng.
- `password`: Mật khẩu đã được băm (đối với hệ thống hiện đại, thường được giữ trống hoặc thay thế bằng "x").
- `UID`: User ID, số nguyên đại diện cho người dùng.
- `GID`: Group ID, số nguyên đại diện cho nhóm của người dùng.
- `GECOS`: Thông tin chung về người dùng (tên đầy đủ, số điện thoại, v.v.).
- `home_directory`: Đường dẫn đến thư mục người dùng.
- `shell`: Đường dẫn đến shell mặc định cho người dùng.

Lưu ý rằng mật khẩu thực sự không được lưu trực tiếp trong file `/etc/passwd` mà thay vào đó được lưu trong file `/etc/shadow` với bảo mật cao hơn. File `/etc/passwd` chỉ chứa dấu chấm (x) để chỉ ra rằng mật khẩu được lưu trữ trong file `/etc/shadow`.

## 2.useradd và file cấu hình /etc/default/useradd
## 2.1 useradd
Lệnh `useradd` trong Linux được sử dụng để thêm một tài khoản người dùng mới vào hệ thống. Khi bạn chạy lệnh này, nó sẽ tạo một tài khoản mới với các thiết lập mặc định, bao gồm cả UID (User ID) và GID (Group ID), cũng như tạo thư mục người dùng mặc định.

Cú pháp cơ bản của lệnh `useradd` là:

`sudo useradd [OPTIONS] username`

VD:

sudo useradd ducanh2

Trong đó:

- `ducanh2` là tên đăng nhập của người dùng mới.

Một số tùy chọn phổ biến có thể được sử dụng với lệnh `useradd`:

- `-c`: Chú thích hoặc thông tin về người dùng.
- `-m`: Tạo thư mục người dùng.
- `-g`: Chỉ định GID (Group ID).
- `-G`: Chỉ định danh sách các nhóm phụ khác nhau mà người dùng thuộc vào.
- `-s`: Chỉ định loại shell mặc định cho người dùng.
Ví dụ sử dụng một số tùy chọn:

`sudo useradd -m -s /bin/bash -g users -G sudo ducanh2`

Trong VD này, lệnh tạo một người dùng mới có tên là `ducanh2` với thư mục người dùng được tạo (`-m`), shell mặc định là Bash (`-s /bin/bash`), thuộc nhóm chính là `users` (`-g users`), và thuộc nhóm phụ là `sudo` (`-G sudo`).

## File cấu hình /etc/default/useradd
Tệp `/etc/default/useradd` chứa các cấu hình mặc định cho lệnh useradd. Bạn có thể mở nó bằng một trình soạn thảo văn bản để xem nó:

`sudo vi /etc/default/useradd`

Bên cạnh việc sử dụng `cat` hoặc `vi` để hiển thị tệp tin này, bạn cũng có thể sử dụng `useradd -D`. Khi bạn chạy lệnh này, nó sẽ hiển thị các tùy chọn mặc định hiện tại được sử dụng bởi `useradd`. Nếu bạn muốn thay đổi các tùy chọn này, bạn có thể sử dụng cùng lệnh với các tùy chọn khác.

VD: `sudo useradd -D`

Kết quả như sau:

`makefile`

`Copy code`

`GROUP=100`

`HOME=/home`

`INACTIVE=-1`

`EXPIRE=`

`SHELL=/bin/sh`

`SKEL=/etc/skel`

`CREATE_MAIL_SPOOL=no`

Ở đây:

- `GROUP=100`: GID (Group ID) mặc định cho người dùng mới.
- `HOME=/home`: Thư mục người dùng mặc định.
- `INACTIVE=-1`: Số ngày không hoạt động trước khi tài khoản bị khóa.
- `EXPIRE=`: Ngày hết hạn tài khoản (nếu có).
- `SHELL=/bin/sh`: Shell mặc định cho người dùng mới.
- `SKEL=/etc/skel`: Thư mục mẫu chứa các tệp mẫu được sao chép vào thư mục người dùng mới.
- `CREATE_MAIL_SPOOL=no`: Tạo thư mục gói thư (mail spool) cho người dùng mới hay không.

## 3. userdel
Lệnh `userdel` trong Linux được sử dụng để xóa một tài khoản người dùng khỏi hệ thống. Khi bạn chạy lệnh này, nó sẽ xóa tài khoản người dùng cũng như các tệp tin và thư mục liên quan đến tài khoản đó.

Cú pháp cơ bản của lệnh `userdel` là:
`sudo userdel [OPTIONS] username`

VD: `sudo userdel ducanh2`

Trong đó:

- `ducanh2` là tên đăng nhập của người dùng cần xóa.

Một số tùy chọn phổ biến:

- `-r`: Xóa cả thư mục người dùng và thư mục spool mail (nếu có). Nếu bạn không sử dụng tùy chọn này, chỉ tài khoản người dùng sẽ bị xóa, nhưng thư mục người dùng và mail spool không bị xóa.

VD sử dụng tùy chọn `-r`:
`sudo userdel -r john`

Lưu ý rằng trước khi xóa một tài khoản người dùng, bạn nên đảm bảo rằng không có quy trình nào đang chạy dưới tên người dùng đó và làm sao để đảm bảo dữ liệu quan trọng không bị mất đi.

## 4.usermod
Lệnh `usermod` trong Linux được sử dụng để sửa đổi thông tin của một tài khoản người dùng đã tồn tại. Bạn có thể sử dụng `usermod` để thay đổi các thông số như UID (User ID), GID (Group ID), thư mục người dùng, shell mặc định, và nhiều tùy chọn khác.

Cú pháp cơ bản của lệnh `usermod` là:
`sudo usermod [OPTIONS] username`

VD:
`sudo usermod -s /bin/bash -G sudo ducanh`

Trong đó:

- `-s /bin/bash`: Thay đổi shell mặc định của người dùng thành Bash.
- `-G sudo`: Thêm người dùng vào nhóm sudo.

Một số tùy chọn phổ biến:

- `-u UID`: Đặt User ID (UID) cho người dùng.
- `-g GID`: Đặt Group ID (GID) cho người dùng.
- `-d home_directory`: Đặt thư mục người dùng.

VD sử dụng các tùy chọn khác:
`sudo usermod -u 1001 -g users -d /home/newhome ducanh`
Trong ví dụ này:

- `-u 1001`: Đặt User ID (UID) thành 1001.
- `-g users`: Đặt Group ID (GID) thành users.
- `-d /home/newhome`: Đặt thư mục người dùng thành `/home/newhome`.
Lưu ý rằng để thực hiện các thay đổi trên tài khoản, bạn cần có quyền root hoặc sử dụng sudo.

## 5./etc/skel 
Thư mục `/etc/skel` trong Linux chứa các tệp và thư mục mẫu được sao chép vào thư mục người dùng mới khi tài khoản người dùng được tạo. Cụ thể, khi sử dụng lệnh `useradd` để tạo một tài khoản mới, nội dung của thư mục `/etc/skel` sẽ được sao chép vào thư mục người dùng mới, tạo ra một môi trường người dùng khởi đầu với các tệp và thư mục mẫu.

VD, nếu bạn có một tệp có tên là `.bashrc` trong thư mục `/etc/skel`, nó sẽ được sao chép vào thư mục người dùng mới với tên là `.bashrc`, cung cấp một cấu hình mặc định cho shell của người dùng.

Thường thì, thư mục `/etc/skel` chứa các tệp mẫu như `.bashrc`, `.bash_profile`, và các tệp khác liên quan đến cấu hình môi trường người dùng.

Bạn có thể kiểm tra nội dung của thư mục `/etc/skel` bằng cách sử dụng lệnh ls:
`ls /etc/skel`

Lưu ý rằng nếu bạn muốn thay đổi cấu trúc môi trường mặc định cho các tài khoản người dùng mới, bạn có thể chỉnh sửa thư mục `/etc/skel` hoặc thay đổi tệp mẫu trong đó.

## 6.user login shell:/bin/bash và /usr/sbin/nologin
Nếu bạn thấy rằng trường shell của một người dùng là `/bin/bash` khi kiểm tra tệp `/etc/passwd`, điều này chỉ đơn giản là cho biết rằng người dùng đó được đặt làm môi trường làm việc với Bash khi họ đăng nhập vào hệ thống.

VD , nếu kết quả của lệnh `grep` hoặc `awk` giống như sau:

ducanh:x:1000:1000:ducanh:/home/ducanh:/bin/bash
Trong đó, /bin/bash là đường dẫn đến shell của người dùng ducanh. Khi ducanh đăng nhập vào hệ thống, hệ thống sẽ sử dụng Bash làm môi trường làm việc của em.

Nếu bạn thấy rằng trường shell của một người dùng là `/usr/sbin/nologin` khi kiểm tra tệp /etc/passwd, điều này chỉ đơn giản là cho biết rằng người dùng đó không được phép đăng nhập vào hệ thống thông qua môi trường dòng lệnh.

Shell `/usr/sbin/nologin` thường được sử dụng để "tắt" tài khoản người dùng mà không cần xóa hoặc vô hiệu hóa tài khoản đó. Khi một người dùng cố gắng đăng nhập với shell nologin, họ sẽ nhận được một thông báo như "This account is currently not available" và sau đó đăng xuất ngay lập tức.

