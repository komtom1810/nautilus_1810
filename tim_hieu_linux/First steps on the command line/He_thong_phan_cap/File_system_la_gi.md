# File System Linux

Trong Linux, hệ thống tệp (filesystem) là cách tổ chức và lưu trữ dữ liệu trên ổ đĩa. Hệ thống tệp quản lý cách các tệp và thư mục được tổ chức và truy cập trong hệ điều hành. Dưới đây là một số khái niệm và thành phần quan trọng của hệ thống tệp trong Linux:

1. **Cây thư mục (Directory Tree):** Hệ thống tệp trong Linux tổ chức dữ liệu dưới dạng cây thư mục. Thư mục gốc được gọi là thư mục /, và từ đó có thể chứa nhiều thư mục con và tệp.

2. **Tệp (File):** Là một đơn vị cơ bản để lưu trữ dữ liệu. Các tệp có thể chứa văn bản, hình ảnh, chương trình thực thi, và nhiều loại dữ liệu khác.

3. **Thư mục (Directory):** Là một cách để tổ chức tệp và thư mục khác. Mỗi thư mục có thể chứa nhiều thư mục con và tệp.

4. **Đường dẫn (Path):** Mô tả vị trí của một tệp hoặc thư mục trong hệ thống tệp. Đường dẫn có thể là đường dẫn tuyệt đối (absolute path) hoặc đường dẫn tương đối (relative path).

5. **Mount Point:** Là một thư mục trong hệ thống tệp mà một hệ thống tệp khác được gắn kết (mounted) vào. Việc mount một hệ thống tệp là quá trình kết nối một ổ đĩa hoặc phân vùng vào cây thư mục của hệ thống.

6. **Hệ thống tệp thuần Linux (Linux Filesystem):** Các hệ thống tệp phổ biến trên Linux bao gồm Ext4, Ext3, và Ext2. Các hệ thống tệp này hỗ trợ các tính năng như quyền truy cập, ghi nhật ký (journaling), và phân quyền.

7. **/etc/fstab:** Là tệp tin cấu hình trong hệ thống Linux chứa thông tin về việc gắn kết các hệ thống tệp vào các mount point.

8. **Virtual File System (VFS):** Là một thành phần trong hệ thống Linux giúp hỗ trợ nhiều loại hệ thống tệp khác nhau và làm cho chúng trông giống nhau đối với các ứng dụng.

Hệ thống tệp là một phần quan trọng của hệ điều hành Linux, quản lý và tổ chức dữ liệu để đảm bảo sự hiệu quả và an toàn trong quá trình sử dụng.