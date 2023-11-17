# Biến $PS1, $PATH
## $PS1
Biến `$PS1`` không phải là biến môi trường mà là biến trong shell (chẳng hạn như Bash) được sử dụng để định dạng và hiển thị dấu nhắc (prompt) của shell. Khi bạn thay đổi giá trị của $PS1, bạn có thể tùy chỉnh cách dấu nhắc xuất hiện trong terminal.

Dưới đây là một số vd:

- Hiển Thị Dấu Nhắc Đơn Giản: `PS1="\$ "`
Trong ví dụ này, dấu nhắc sẽ chỉ là dấu đô la.

- Hiển Thị Tên Người Dùng và Tên Host: `PS1="\u@\h \$ "`
Dấu nhắc sẽ hiển thị tên người dùng (`\u`), dấu `@`, tên host (`\h`) và dấu đô la.

- Hiển Thị Thư Mục Hiện Tại: `PS1="\w \$ "`
Dấu nhắc sẽ hiển thị đường dẫn đầy đủ của thư mục hiện tại (`\w`).

- Hiển Thị Thời Gian: `PS1="\t \$ "`
Dấu nhắc sẽ hiển thị thời gian hiện tại (`\t`).

- Kết Hợp Các Thông Tin: `PS1="\u@\h \w \$ "`
Dấu nhắc sẽ hiển thị tên người dùng, tên host và đường dẫn đầy đủ của thư mục hiện tại.

Lưu ý rằng nó không phải là `$PS1` mà là biến PS1. Bạn thường thấy và thay đổi giá trị của PS1 trong tệp cấu hình shell của bạn (như `.bashrc` hoặc `.bash_profile`). Để áp dụng các thay đổi ngay lập tức, bạn có thể sử dụng lệnh `source`

## $PATH
Biến `$PATH` trong Linux là một biến môi trường quan trọng, định nghĩa đường dẫn mà hệ thống sẽ tìm kiếm khi bạn nhập một lệnh vào terminal. Khi bạn nhập một lệnh, hệ thống sẽ duyệt qua các thư mục được liệt kê trong biến `$PATH` để tìm kiếm các chương trình thực thi.

Giá trị của `$PATH` được liệt kê dưới dạng một chuỗi các thư mục, cách nhau bởi dấu hai chấm (`:`). Ví dụ:

`/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/usr/sbin:/sbin`

Trong vd này, hệ thống sẽ tìm kiếm các lệnh trong các thư mục `/usr/local/bin`, `/usr/bin`, `/bin`, `/usr/local/sbin`, `/usr/sbin`, và `/sbin` theo thứ tự.

- Xem Giá Trị Của `$PATH`:
Bạn có thể xem giá trị hiện tại của biến `$PATH` bằng cách sử dụng lệnh `echo`:

`echo $PATH`

- Thay Đổi Giá Trị Của `$PATH`:
Nếu bạn muốn thêm một thư mục mới vào `$PATH`, bạn có thể sử dụng lệnh `export`:

`export PATH=$PATH:/đường/dẫn/thư/mục/mới`

Trong đó `/đường/dẫn/thư/mục/mới` là đường dẫn của thư mục mà bạn muốn thêm.

Nếu bạn muốn thực hiện thay đổi này mỗi khi bạn mở một terminal, bạn có thể thêm lệnh trên vào tệp cấu hình shell của bạn (như `.bashrc`, `.bash_profile`, hoặc tương tự).

Lưu ý rằng thứ tự của các thư mục trong `$PATH` quan trọng; hệ thống sẽ tìm kiếm lệnh theo thứ tự từ trái sang phải.


