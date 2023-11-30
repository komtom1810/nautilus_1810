# Command groupadd, groupdel, usermod, groupmod, gpasswd, newgrp, vigr

## 1. Groupadd
Lệnh `groupadd` là một lệnh được sử dụng để tạo một nhóm mới. Khi bạn tạo một nhóm mới, bạn có thể gán các người dùng cụ thể vào nhóm đó để quản lý quyền truy cập vào các tài nguyên chia sẻ.

Cú pháp cơ bản của lệnh `groupadd` như sau:
`sudo groupadd [tùy_chọn] tên_nhóm`

Trong đó:

- `[tùy_chọn]` là một hoặc nhiều tùy chọn đi kèm với lệnh. Một số tùy chọn phổ biến bao gồm:
- `-c`: Để thêm mổ tả hoặc comment về nhóm
- `-g` GID: Xác định Group ID (GID) của nhóm mới.
- `-r`: Tạo một nhóm hệ thống (system group).
- `-f`: Bắt buộc sử dụng, thậm chí khi tên nhóm đã tồn tại.
- `tên_nhóm` là tên của nhóm bạn muốn tạo.

VD, để tạo một nhóm có tên là "nhanvien" với Group ID là 1001, bạn có thể sử dụng lệnh:
`sudo groupadd -g 1001 nhanvien`

## 2. Groupdel
Lệnh groupdel được sử dụng để xóa một nhóm người dùng khỏi hệ thống. Cú pháp cơ bản của lệnh này như sau:
`sudo groupdel tên_nhóm`

Trong đó:

`tên_nhóm`: Tên của nhóm mà bạn muốn xóa.

VD, để xóa nhóm có tên "nhanvien" bạn có thể sử dụng:

`sudo groupdel nhanvien`

Lệnh này sẽ xóa nhóm "developers" khỏi hệ thống. Hãy chắc chắn rằng bạn có đặc quyền quản trị hệ thống để thực hiện lệnh này.

Lưu ý rằng việc xóa nhóm chỉ xóa thông tin về nhóm từ tệp `/etc/group`. Nếu có người dùng nằm trong nhóm đó, họ sẽ không bị xóa và vẫn tồn tại trên hệ thống.

## 3. Usermod
Lệnh `usermod` trong hệ thống Unix/Linux được sử dụng để sửa đổi thông tin người dùng trong hệ thống. Cú pháp cơ bản của lệnh này là:

`sudo usermod [tùy_chọn] tên_người_dùng`

Trong đó:

- `[tùy_chọn]` là một hoặc nhiều tùy chọn được sử dụng để thực hiện các thay đổi cụ thể.
- `tên_người_dùng` là tên người dùng mà bạn muốn sửa đổi.

**Một số tùy chọn phổ biến của lệnh `usermod` bao gồm:**

- `-c "mô_tả"`: Thêm mô tả hoặc comment về người dùng.
- `-g tên_nhóm`: Đặt nhóm chính cho người dùng.
- `-G tên_nhóm1,tên_nhóm2`: Thêm người dùng vào các nhóm bổ sung (phân tách bằng dấu phẩy).
- `-aG tên_nhóm`: Thêm người dùng vào nhóm mà không loại bỏ khỏi các nhóm khác.

VD, để thêm người dùng "ducanh" vào nhóm "nhanvien," bạn có thể sử dụng:

`sudo usermod -aG nhanvien ducanh`

Lệnh này sẽ thêm người dùng "ducanh" vào nhóm "nhanvien" mà không làm mất đi các nhóm khác mà "ducanh" đang thuộc vào.

## 4. Groupmod
Lệnh `groupmod` trong hệ thống Unix/Linux được sử dụng để sửa đổi thông tin của một nhóm người dùng. Cú pháp cơ bản của lệnh này là:

`sudo groupmod [tùy_chọn] tên_nhóm`

Trong đó:

- `[tùy_chọn]` là một hoặc nhiều tùy chọn được sử dụng để thực hiện các thay đổi cụ thể.
- `tên_nhóm` là tên của nhóm mà bạn muốn sửa đổi.

Một số tùy chọn phổ biến của lệnh groupmod bao gồm:

- `-g GID`: Đặt Group ID (GID) cho nhóm.
- `-n tên_mới`: Đặt tên mới cho nhóm.

VD, để đổi tên của nhóm từ "nhanvien" thành "giamdoc," bạn có thể sử dụng:

`sudo groupmod -n giamdoc nhanvien`

Lệnh này sẽ thay đổi tên của nhóm từ "nhanvien" thành "giamdoc" trong hệ thống.

Lưu ý rằng để thay đổi thông tin của một nhóm, bạn cần có đặc quyền quản trị hệ thống.

## 5.Gpasswd
Lệnh `gpasswd` trong hệ thống Unix/Linux được sử dụng để quản lý các thông tin mật khẩu và thành viên của một nhóm. Cú pháp cơ bản của lệnh này là:

`gpasswd [tùy_chọn] tên_nhóm`

Trong đó:

- `[tùy_chọn]` là một hoặc nhiều tùy chọn được sử dụng để thực hiện các thay đổi cụ thể.
- `tên_nhóm` là tên của nhóm mà bạn muốn quản lý.
Một số tùy chọn phổ biến của lệnh gpasswd bao gồm:

- `-a` tên_người_dùng: Thêm một người dùng vào nhóm.
- `-d` tên_người_dùng: Xóa một người dùng khỏi nhóm.
- `-A` tên_người_dùng: Chỉ định người dùng có quyền quản lý nhóm (administrator).
- `-M` người_dùng1,người_dùng2: Đặt danh sách các thành viên mới của nhóm.

VD, để thêm người dùng "ducanh" vào nhóm "nhanvien" bằng lệnh `gpasswd`, bạn có thể sử dụng:

`sudo gpasswd -a ducanh nhanvien`

Lệnh này sẽ thêm người dùng "ducanh" vào nhóm "nhanvien." Lưu ý rằng việc quản lý nhóm này thường được thực hiện bởi người dùng có quyền quản trị hệ thống.

## 6. Newgrp
Lệnh `newgrp` được sử dụng để thay đổi nhóm mặc định của người dùng khi họ đang làm việc trong một phiên làm việc (shell session). Khi bạn chạy `newgrp` mà không có tùy chọn và chỉ cung cấp tên của một nhóm, bạn sẽ chuyển sang làm việc trong nhóm đó.

Cú pháp cơ bản của lệnh `newgrp` là:

`newgrp tên_nhóm`

Trong đó:

- `tên_nhóm` là tên của nhóm mà bạn muốn chuyển sang làm việc.
VD, để chuyển sang làm việc trong nhóm "giamdoc," bạn có thể sử dụng:

`newgrp giamdoc`

Khi bạn sử dụng `newgrp` mà không có tùy chọn, nó sẽ yêu cầu mật khẩu của nhóm để xác nhận quyền truy cập. Người dùng chỉ có thể sử dụng `newgrp` để chuyển đổi sang các nhóm mà họ đã tham gia.

Lưu ý rằng việc sử dụng `newgrp` chỉ ảnh hưởng đến phiên làm việc hiện tại và sẽ trở lại nhóm mặc định của người dùng sau khi phiên làm việc kết thúc.

## 7. vigr
Lệnh `vigr` được sử dụng để chỉnh sửa tệp `/etc/group` bằng trình soạn thảo văn bản `vi`. Tệp `/etc/group` chứa thông tin về các nhóm người dùng trên hệ thống.

Cú pháp cơ bản của lệnh vigr là:

`sudo vigr`

Lệnh này mở tệp `/etc/group` trong trình soạn thảo vi với đặc quyền quản trị hệ thống (`sudo`). Bạn có thể thêm, sửa đổi hoặc xóa các dòng trong tệp để thay đổi thông tin nhóm.

Khi bạn kết thúc việc chỉnh sửa trong vigr, các thay đổi sẽ được lưu vào tệp `/etc/group`. Nhớ luôn thận trọng khi chỉnh sửa các tệp cấu hình hệ thống, và thường xuyên tạo sao lưu trước khi thực hiện bất kỳ thay đổi quan trọng nào.






















