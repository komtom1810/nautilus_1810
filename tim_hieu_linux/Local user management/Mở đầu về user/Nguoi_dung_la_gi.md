# Người dùng là gì? Các loại người dùng trên hệ thống

## Người dùng là gì?
Trong hệ thống Linux, "người dùng" là một khái niệm quan trọng, đại diện cho người sử dụng cụ thể của hệ thống. Mỗi người dùng có một tên đăng nhập (username) và một ID người dùng (user ID hoặc UID) duy nhất.

Dưới đây là một số điểm chính về người dùng trong Linux:

1. **Tên đăng nhập (Username):** Là một chuỗi ký tự đặc biệt được gán cho mỗi người dùng. Tên đăng nhập thường được sử dụng để đăng nhập vào hệ thống.

2. **ID người dùng (User ID - UID):** Là một số duy nhất được gán cho mỗi người dùng. UID 0 thường được dành cho người dùng root, có quyền hạn tối đa trên hệ thống.

3. **Nhóm người dùng (User Group):** Mỗi người dùng thuộc một hoặc nhiều nhóm người dùng. Nhóm người dùng có thể chia sẻ quyền hạn và tài nguyên với nhiều người dùng.

4. **Mật khẩu (Password):** Mỗi người dùng có một mật khẩu, được sử dụng để xác thực người dùng khi đăng nhập vào hệ thống.

5. **Thư mục người dùng (Home Directory):** Mỗi người dùng có một thư mục người dùng riêng, thường được đặt trong /home. Thư mục này chứa các tệp tin và thư mục cá nhân của người dùng.

6. **Quyền hạn (Permissions):** Mỗi người dùng được gán một tập hợp các quyền hạn để truy cập và thực hiện các hoạt động trên hệ thống.

7. **Shell:** Là môi trường dòng lệnh mà người dùng sử dụng để tương tác với hệ thống. Nó quyết định giao diện người dùng khi họ đăng nhập.

## Các loại người dùng trên hệ thống
Trong hệ thống Linux, có nhiều loại người dùng với các quyền hạn và trách nhiệm khác nhau. Dưới đây là một số loại người dùng phổ biến:

1. **Người dùng Root (root):** Root là người dùng có quyền hạn tối cao trên hệ thống. Người dùng root có thể thực hiện mọi thao tác trên hệ thống, bao gồm cả việc thay đổi cấu hình, cài đặt phần mềm, và quản lý người dùng khác.

2. **Người dùng Hệ Thống (system):** Những người dùng này được tạo ra để chạy các dịch vụ và tiến trình hệ thống. Thông thường, chúng không có quyền đăng nhập và sử dụng các quyền hạn hạn chế.

3. **Người dùng Bình Thường (regular):** Đây là người dùng thông thường có quyền hạn giới hạn. Họ có thể làm việc trên hệ thống, chạy các ứng dụng, và thực hiện các thao tác thông thường, nhưng không có quyền thực hiện các thao tác quan trọng như cấu hình hệ thống hay quản lý người dùng.

4. **Người dùng Có Quyền (privileged):** Đây là nhóm người dùng được cấp quyền đặc biệt thông qua việc thêm vào nhóm như sudo (superuser do) để có quyền thực hiện các lệnh với quyền root mà không cần đăng nhập trực tiếp với tài khoản root. Những người dùng này có thể sử dụng lệnh sudo để thực hiện các thao tác đặc quyền.

5. **Người Dùng Vô Hình (nologin):** Đây là người dùng được sử dụng để cấm đăng nhập. Thông thường, họ không có mật khẩu và môi trường đăng nhập của họ được đặt là /usr/sbin/nologin để ngăn chặn đăng nhập trực tiếp.

6. **Người Dùng Guest (guest):** Thường được sử dụng cho các phiên người dùng không đăng nhập vào hệ thống mà chỉ có quyền truy cập tạm thời.

Các người dùng có thể thuộc nhiều nhóm khác nhau để xác định quyền hạn của họ. Quyền hạn cụ thể được quản lý thông qua hệ thống quyền (permissions) và cơ chế quyền kiểm soát truy cập (access control).





