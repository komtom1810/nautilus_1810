# ~/.bashrc
`~/.bashrc` là một tệp cấu hình dành cho Bash (Bourne Again SHell), một loại shell phổ biến trong các hệ thống Unix và Unix-like. Tệp này thường nằm trong thư mục home của người dùng và có tên đầy đủ là `.bashrc`. Ký hiệu `~` đại diện cho thư mục chính của người dùng.

Trong môi trường Linux và các hệ điều hành tương tự, khi bạn đăng nhập vào một phiên dòng lệnh, Bash sẽ thực thi các lệnh trong tệp `.bashrc`. Điều này cho phép bạn tùy chỉnh môi trường làm việc của mình bằng cách đặt các biến môi trường, alias, và thậm chí là thực hiện các lệnh cụ thể.

## Dưới đây là một số lệnh bạn có thể sử dụng để thực hiện các thao tác cơ bản trên tệp `.bashrc`:

- **Mở tệp `.bashrc` để chỉnh sửa:** `nano ~/.bashrc`

Điều này mở tệp `.bashrc` trong trình soạn thảo văn bản Nano. Bạn cũng có thể thay thế `nano` bằng trình soạn thảo văn bản ưa thích của bạn như `vi`, `vim`, hoặc `gedit`.

- **Thêm alias hoặc biến môi trường:**

`export MY_VARIABLE="Hello, World!"`

`alias ll="ls -l"`

Đây là ví dụ về cách thêm một biến môi trường và một alias. Bạn có thể thêm những đoạn mã này vào tệp `.bashrc` để sử dụng chúng trong phiên làm việc Bash của bạn.

## Một số công việc phổ biến mà người dùng thường thực hiện trong tệp `.bashrc` bao gồm:

1. **Đặt biến môi trường:** Cấu hình các biến môi trường như `PATH`, `PS1` (prompt), và các biến khác.

2. **Alias:** Tạo các "biệt danh" cho các lệnh dài và phức tạp hơn để dễ sử dụng hơn.

3. **Cài đặt các lệnh tự động chạy:** Chạy các lệnh tự động khi bạn mở một phiên dòng lệnh.

4. **Cài đặt màu sắc cho dòng lệnh:** Tùy chỉnh màu sắc cho các phần khác nhau của dòng lệnh để làm cho nó dễ đọc hơn.

Vui lòng lưu ý rằng các thay đổi trong tệp `.bashrc` sẽ chỉ áp dụng cho phiên làm việc hiện tại và các phiên làm việc mới, không phải cho các phiên làm việc hiện tại. Đối với các thay đổi có hiệu lực ngay lập tức, bạn có thể chạy lệnh `source ~/.bashrc` hoặc mở một phiên làm việc mới.