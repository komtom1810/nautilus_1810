# Các toán tử điều khiển khi thực hiện command
## 1. **`;` (semicolon):** Dùng để kết thúc một lệnh và bắt đầu lệnh mới:

`command1 ; command2`

## 2. **`&&` (AND logic operator):** Dùng để thực hiện lệnh 2 chỉ khi lệnh 1 thành công:

`command1 && command2`

## 3. **`||` (OR logic operator):** Dùng để thực hiện lệnh 2 chỉ khi lệnh 1 thất bại:

`command1 || command2`

## 4. **`&` (ampersand):** Dùng để chạy một lệnh nền (background). Lệnh sau `&` sẽ thực hiện ngay cùng một lúc mà không chờ lệnh trước kết thúc:

`command &`

## 5. **`|` (pipe):** Dùng để chuyển đầu ra của lệnh trước thành đầu vào của lệnh sau:

`command1 | command2`

## 6. **`$?`**: 
Toán tử `$?` là một biến đặc biệt chứa mã thoát của lệnh thực thi gần đây nhất. Mã thoát này là giá trị trả về của một lệnh khi nó kết thúc thực thi. 

Khi bạn chạy một lệnh trong Linux, giá trị trả về của lệnh đó sẽ được lưu trong biến $?. Nếu lệnh thực thi thành công, giá trị của $? sẽ là 0. Ngược lại, nếu có lỗi xảy ra, $? sẽ chứa một giá trị không phải 0 để biểu thị lỗi cụ thể. 

ví dụ:

`ls non_existent_directory`

`echo "Exit code: $?"`

 # Kết quả sẽ là Exit code: 2, vì lệnh ls thất bại với mã thoát 2

`cp existing_file new_directory/`

`echo "Exit code: $?"`

  # Kết quả sẽ là Exit code: 0, vì lệnh cp thành công

Trong ví dụ trên, sau mỗi lệnh, `echo "Exit code: $?"` được sử dụng để hiển thị mã thoát của lệnh trước đó.

## 7. **`#`** 

Dấu `#` thường được sử dụng với các ý nghĩa khác nhau tùy thuộc vào ngữ cảnh. Dưới đây là một số ý nghĩa phổ biến: 
- Dấu `#` trong Dòng Lệnh:
Khi sử dụng trong dòng lệnh, `#` thường được sử dụng để bắt đầu một dòng comment. Mọi thứ sau `#` trong dòng lệnh được xem là comment và không được thực thi.

`# Đây là một comment trong shell script`

`echo "Hello, World!"`

- Dấu `#` trong Prompt của Superuser:
Khi bạn đăng nhập với quyền root (superuser), prompt có thể chứa `#` thay vì `$`. Điều này chỉ ra rằng bạn đang làm việc với quyền hạn cao.

`root@hostname:~#`

- Dấu `#` trong Shebang:
Trong các tệp lệnh shell script, `#` thường được sử dụng trong shebang để chỉ định loại shell được sử dụng.

`#!/bin/bash`

- Dấu `#` trong Regular Expressions:
Trong các biểu thức chính quy (regular expressions), `#` có thể được sử dụng để đại diện cho chính nó.

`grep "^#" filename`

`# Sẽ khớp với các dòng bắt đầu bằng #`

Những ý nghĩa này của dấu `#` tương ứng với những ngữ cảnh sử dụng khác nhau trong hệ thống Linux và các ứng dụng khác.









