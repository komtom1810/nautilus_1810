## 1.Command `type`
Lệnh `type` trong hệ thống Linux được sử dụng để hiển thị thông tin về loại của một lệnh cụ thể. Nó giúp xác định liệu một lệnh là một lệnh nội bộ (built-in), một lệnh ngoại vi (external command), hoặc một alias.

**Cú pháp cơ bản:** 
`type [options] name`

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