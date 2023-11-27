# Tìm hiểu các cứ pháp, sử dụng cơ bản với vi, vim
## I.Vi(Visual instrument)
Lệnh `vi` trong Linux là một trình soạn thảo văn bản mạnh mẽ và phổ biến. Nó được sử dụng để chỉnh sửa và tạo nội dung trong các tệp tin văn bản. `vi` là một phần của nhiều hệ điều hành UNIX và các hệ điều hành dựa trên UNIX như Linux.

Để sử dụng `vi`, bạn có thể mở một tệp tin hoặc tạo một tệp tin mới bằng cách sử dụng cú pháp sau: `vi tên_tệp_tin`.

Sau khi bạn nhập lệnh trên, `vi` sẽ mở tệp tin có tên được chỉ định. Nếu tệp tin không tồn tại, `vi` sẽ tạo một tệp tin mới với tên được chỉ định.

- **`vi` hoạt động ở ba chế độ chính:**

    + **Chế độ Lệnh (Command Mode):** Chế độ mặc định khi bạn mở `vi`. Bạn có thể thực hiện các lệnh như di chuyển, xóa, và lưu trữ tệp tin từ chế độ này.

    + **Chế độ Chèn (Insert Mode):** Bạn có thể chuyển sang chế độ này bằng cách nhấn `i` trong chế độ lệnh. Trong chế độ này, bạn có thể nhập văn bản vào tệp tin.

    + **Chế độ Hiển thị (Visual Mode):** Bạn có thể bắt đầu chế độ này bằng cách nhấn `v` trong chế độ lệnh. Nó cho phép bạn chọn và thực hiện các thao tác trên dãy văn bản.

- **Một số thao tác cơ bản:**

1. **Chuyển giữa các chế độ:**

- `i`: Chuyển sang chế độ chèn.
- `Esc`: Chuyển từ chế độ chèn hoặc hiển thị về chế độ lệnh.

2. **Lưu và thoát:**

- `:w`: Lưu tệp tin (trong chế độ lệnh).
- `:q`: Thoát khỏi vi (nếu không có thay đổi).
- `:wq` hoặc `ZZ`: Lưu và thoát.
- `:q!`: Thoát mà không lưu thay đổi.

3. **Di chuyển con trỏ và xóa văn bản:**

- `h`, `j`, `k`, `l`: Di chuyển con trỏ sang trái, xuống, lên, và sang phải tương ứng.
- `x`: Xóa ký tự dưới con trỏ.
- `dd`: Xóa dòng hiện tại.
- `D`: Xóa từ vị trí con trỏ tới cuối dòng.

4. **Thực hiện thao tác trên nhiều dòng (Visual Mode):**

- Nhấn `v` để bắt đầu chế độ hiển thị.
- Di chuyển con trỏ để chọn văn bản.
- `d`: Xóa văn bản đã chọn.
- `y`: Sao chép văn bản đã chọn.

5. **Tìm kiếm và thay thế:**

- `/từ_khóa`: Tìm kiếm từ khóa xuôi.
- `?từ_khóa`: Tìm kiếm từ khóa ngược.
- `n`: Di chuyển đến kết quả tìm kiếm tiếp theo.
- `N`: Di chuyển đến kết quả tìm kiếm trước đó.
- `:s/từ_khóa1/từ_khóa2/g`: Thay thế từ khóa1 bằng từ khóa2 trên dòng hiện tại.
- `:%s/từ_khóa1/từ_khóa2/g`: Thay thế từ khóa1 bằng từ khóa2 trên toàn bộ tệp tin.


Đây chỉ là một số lệnh và thao tác cơ bản của `vi`. Nếu bạn muốn biết thêm chi tiết, bạn có thể đọc tài liệu bằng cách gõ `man vi` hoặc vimtutor để bắt đầu một hướng dẫn tương tác. 

## II.Vim(Vi Improved) 

1. **`vim` là phiên bản nâng cao của `vi`:** `vim` (Vi Improved) được phát triển dựa trên `vi` để cung cấp nhiều tính năng mạnh mẽ và cải thiện hiệu suất. `vim` giữ lại tất cả các tính năng của `vi` và thêm vào đó nhiều tính năng mới, làm cho nó trở thành một trình soạn thảo văn bản linh hoạt và mạnh mẽ hơn.

2. **Tính năng mở rộng của vim:** Một số tính năng quan trọng được thêm vào vim bao gồm hỗ trợ màu sắc, giao diện đồ họa, quay lại lịch sử chỉnh sửa, kiểm tra chính tả, hỗ trợ các ngôn ngữ lập trình, và nhiều lựa chọn thích ứng khác.

3. **Chế độ chèn trực quan (vim):** `vim` cung cấp một chế độ chèn trực quan giúp dễ dàng di chuyển và chọn văn bản, giúp người dùng soạn thảo văn bản một cách thuận lợi hơn.

4. **Giao diện người dùng (`vim`):** `vim` hỗ trợ giao diện người dùng dòng lệnh và giao diện đồ họa (gVim), trong khi `vi` thường chỉ có giao diện người dùng dòng lệnh.

5. **Tùy chọn cấu hình (`vim`):** `vim` cung cấp nhiều tùy chọn cấu hình linh hoạt, cho phép người dùng tùy chỉnh hầu hết các khía cạnh của trình soạn thảo theo ý muốn.

6.**Tương thích ngược (`vim`):** `vim` thường có khả năng tương thích ngược với các lệnh và tùy chọn của `vi`, điều này có nghĩa là nó có thể sử dụng một số lệnh và tùy chọn của `vi` mà không có vấn đề lớn.

Khi sử dụng `vim`, người dùng có thể tận dụng nhiều tính năng mạnh mẽ mà `vi` không cung cấp. Tuy nhiên, `vi` vẫn là một trình soạn thảo văn bản tiêu biểu trên hệ thống UNIX và có sẵn trên hầu hết các hệ điều hành Linux mà không cần cài đặt thêm.