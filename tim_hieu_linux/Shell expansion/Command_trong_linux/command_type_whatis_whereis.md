# Command type,which,whatis,whereis

## 1.Command `type`
Lệnh `type` trong hệ thống Linux được sử dụng để hiển thị thông tin về loại của một lệnh cụ thể. Nó giúp xác định liệu một lệnh là một lệnh nội bộ (built-in), một lệnh ngoại vi (external command), hoặc một alias.
**Cú pháp cơ bản:**
type [options] name
**Các tùy chọn phổ biến:**
-a: Hiển thị tất cả các định nghĩa của lệnh, nếu có nhiều hơn một.
-t: Chỉ hiển thị loại lệnh (alias, function, builtin, file).
**Ví dụ:**
**Kiểm tra loại của lệnh `ls`:** `type ls`
Kết quả có thể là `ls is aliased to 'ls --color=auto'` nếu bạn đã tạo một alias cho `ls`.
**Kiểm tra loại của lệnh `cd`:** `type cd`
Kết quả có thể là `cd is a shell builtin` vì `cd` là một lệnh nội bộ.
**Kiểm tra loại của lệnh `cp`:** `type cp`
Kết quả có thể là `cp is /bin/cp` vì `cp` là một lệnh ngoại vi và nằm trong thư mục `/bin`.

## 2.Command `which`
Lệnh `which` trong hệ thống Linux được sử dụng để hiển thị đường dẫn của một lệnh cụ thể. Nó tìm kiếm trong các đường dẫn được đặt trong biến môi trường `PATH`.
**Cú pháp cơ bản:**
`which command_name`
**Ví dụ:**
**Kiểm tra đường dẫn của lệnh `ls`:** `which ls`
Kết quả có thể là `/bin/ls`, chỉ ra rằng lệnh `ls` được thực thi từ thư mục `/bin`.
Lệnh `which` hữu ích khi bạn muốn biết chính xác nơi một lệnh cụ thể được thực thi từ. Nếu lệnh không được tìm thấy, `which` sẽ không có đầu ra.

## 3.Command `whatis` 
Lệnh `whatis` trong hệ thống Linux được sử dụng để hiển thị một mô tả ngắn gọn về một lệnh cụ thể. Nó trích xuất thông tin từ cơ sở dữ liệu mô tả tài liệu `man` (manual pages).
**Cú pháp cơ bản:**
`whatis command_name`
**Ví dụ:**
**Kiểm tra mô tả của lệnh `ls`:** `whatis ls`.
Kết quả có thể là một mô tả ngắn như "list directory contents."
Lệnh `whatis` hữu ích để nhanh chóng xem mô tả ngắn về một lệnh cụ thể mà không cần mở rộng manual pages (`man`) để đọc thông tin chi tiết hơn.

## 4.command `whereis`
Lệnh `whereis` trong hệ thống Linux được sử dụng để tìm kiếm vị trí của các tệp tin thực thi, mã nguồn, và các tệp hỗ trợ của một lệnh cụ thể. Nó tìm kiếm trong các đường dẫn tiêu biểu được cấu hình cho các lệnh trong biến môi trường `PATH`.
**Cú pháp cơ bản:**
`whereis command_name`
**ví dụ:**
**Tìm kiếm vị trí của lệnh `ls`:** `whereis ls`.
Kết quả có thể là một danh sách bao gồm vị trí của tệp thực thi (`/bin/ls`), mã nguồn (`/usr/share/man/man1/ls.1.gz`), và các tệp hỗ trợ khác.
Lệnh `whereis` thường trả về thông tin về vị trí của các thành phần chính liên quan đến một lệnh nhất định. Đối với lệnh cụ thể, có thể thấy một số tệp tin thực thi, tệp hỗ trợ, và mã nguồn liên quan.
