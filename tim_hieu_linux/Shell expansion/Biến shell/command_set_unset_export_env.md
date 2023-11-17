# Command set, unset, export, env 
## 1. Set
Lệnh `set` trong hệ thống Linux thường được sử dụng để cài đặt và xem các tùy chọn shell, môi trường, và các cấu hình khác. Dưới đây là một số tùy chọn thường được sử dụng với lệnh set:

- Hiển Thị Tất Cả Các Biến Môi Trường: `set`
- Hiển Thị Các Tùy Chọn Của Shell: `set -o`
- Bật/Tắt Một Tùy Chọn Cụ Thể:

`set -o option_name  # Bật một tùy chọn`

`set +o option_name  # Tắt một tùy chọn`

VD: `set -o vi`  # Bật chế độ vi

- Thiết Lập Biến Môi Trường: 
`set variable_name=value`

VD: `set MY_VARIABLE="Hello, World"`
 
Lưu ý rằng việc sử dụng `set` để đặt các biến môi trường chỉ ảnh hưởng đến phiên làm việc hiện tại. Để thực hiện thay đổi có thể được sử dụng trong các phiên làm việc tiếp theo, bạn có thể muốn thêm các lệnh này vào tệp cấu hình shell như ``.bashrc` hoặc `.bash_profile` (đối với Bash).

## 2.Unset
Lệnh `unset` trong Linux được sử dụng để xóa giá trị của một biến. Khi bạn sử dụng `unset`, biến sẽ không còn tồn tại trong môi trường làm việc hiện tại.

Dưới đây là cách sử dụng `unset`:

`unset variable_name`

Trong đó, variable_name là tên của biến bạn muốn xóa. Ví dụ:

`my_variable="Hello, World"`

`echo $my_variable`  # In giá trị của biến

`unset my_variable`

`echo $my_variable`  # Sẽ không in gì cả vì biến đã bị xóa

Lưu ý rằng `unset` chỉ xóa giá trị của biến trong shell hiện tại. Nếu bạn muốn xóa biến môi trường (biến tồn tại trong các phiên làm việc tiếp theo), bạn có thể sử dụng lệnh `export -n` hoặc chỉ cần sử dụng `unset` trong môi trường hiện tại và không sử dụng `export`.

## 3.Export
Lệnh `export` trong Linux được sử dụng để gắn giá trị cho một biến môi trường. Biến môi trường là các biến có thể được sử dụng bởi các quá trình con được tạo bởi quá trình hiện tại. Khi một biến được "export", nó trở thành một biến môi trường.

Cú pháp cơ bản của export là:

`export VARIABLE_NAME=value`

VD: `export MY_VARIABLE="Hello, World"`

Ngoài ra, để xem danh sách các biến môi trường đã được export, bạn có thể sử dụng lệnh `env` hoặc `printenv`

## 4.Env
Lệnh `env`` trong Linux được sử dụng để hiển thị danh sách các biến môi trường hiện tại hoặc chạy một chương trình với môi trường được chỉ định.

- Hiển Thị Danh Sách Biến Môi Trường: `env`
Lệnh trên sẽ hiển thị danh sách các biến môi trường hiện tại, bao gồm tên biến và giá trị của chúng.

- Chạy Chương Trình với Môi Trường Được Chỉ Định:
`env MY_VARIABLE="Hello, World" echo $MY_VARIABLE`

Trong vd này, chương trình echo sẽ được chạy với môi trường được chỉ định, bao gồm biến môi trường MY_VARIABLE có giá trị là "Hello, World".

- Hiển Thị Giá Trị Của Một Biến Môi Trường Cụ Thể:

`env | grep VARIABLE_NAME`

VD: `env | grep PATH`

Lệnh trên sẽ hiển thị giá trị của biến môi trường PATH.

`env` là một công cụ mạnh mẽ khi bạn muốn kiểm tra, chỉnh sửa hoặc chạy một chương trình với một môi trường cụ thể.








