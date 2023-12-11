Trong hệ điều hành Linux, quản lý quyền hạn là một phần quan trọng của bảo mật hệ thống. Các quyền hạn này quyết định ai được phép thực hiện các hành động nào trên hệ thống. Dưới đây là một số khái niệm và cơ bản về quyền hạn trong Linux:

1. Nhóm **User (hay còn gọi là người dùng)** là tài khoản dùng để đăng nhập vào hệ thống. Mỗi User sẽ chứa một mã **UID (Unique identification number)** hay mã xác định danh tính duy nhất, từ đó hệ thống có thể phân biệt được các người dùng với nhau.

Tất cả các thông tin về các User trong hệ thống được lưu tại địa chỉ `/etc/passwd` còn mật khẩu thì sẽ được hash (mã băm - mã hoá một chiều) và lưu tại `/etc/shadow`

- Dựa vào quyền hạn truy cập thì User được chia theo 2 loại chính:

    + **Superuser/root/administrator** : Loại User có quyền hạn cao nhất. Có khả năng truy cập vào mọi file có trong hệ thống.

    + **Normal user**: Là loại User thường, bị giới hạn một số quyền (Ta có thể tuỳ chọn các quyền mà user này có thể làm).

2. Nhóm **(Group)**: Người dùng có thể được tổ chức thành các nhóm. Mỗi nhóm có một **GID (Group ID)** duy nhất. Việc tổ chức người dùng thành nhóm giúp quản lý quyền hạn dễ dàng hơn.

- Trong linux, tất cả các file, tài nguyên đều có 3 loại quyền chính:

    + **READ (Đọc)**: Quyền đọc cho phép bạn mở file và xem nội dung của nó. Trong trường hợp thư mục thì bạn có thể xem các thành phần con trong nó.

    + **WRITE (Viết)**: Quyền viết hay ghi cho phép bạn thay đổi nội dung của file. Trong trường hợp thư mục thì bạn có thể thay đổi vị trí, xoá, thêm các thành phần con trong nó

    + **EXECUTE (Thực thi)**: Quyền thực thi cho phép bạn chạy file.

3. **Quyền Hạn Owner, Group, và Others:**

- **Owner (chủ sở hữu):** Người dùng tạo ra tệp hoặc thư mục, thường là người tạo ra nó.
- **Group (nhóm):** Nhóm chủ sở hữu của tệp hoặc thư mục.
- **Others (người khác):** Tất cả những người dùng không phải là chủ sở hữu hoặc không thuộc nhóm chủ sở hữu.

4. **Sử dụng chmod để Thay Đổi Quyền Hạn:**

- `chmod`: chmod là viết tắt của `change mode` dùng để thay đổi quyền của một thư mục hay file trên Linux.

    + Phần quyền bằng số:
Cú pháp: `chmod <permissions-number> <filename>`

![](https://images.viblo.asia/b9741f62-bb9f-492c-8bf1-8a865193edc5.png)

Permissions-number về cơ bản sẽ có 3 chữ số một số với ý nghĩa số thứ nhất là quyền của user, số thứ 2 là quyền của group, số thứ 3 là quyền của other. Ý nghĩa của từng chữ số ở đây:

| Số     | Ký hiệu     | Ý nghĩa              | 
| :----- | :---------- | :------------------  | 
| 0      | ---         | Không có quyền       | 
| 1      | --x         | Thực thi             | 
| 2      | -w-         | Ghi                  | 
| 3      | -wx         | Thực thi + Ghi       |
| 4      | r--         | Đọc                  |
| 5      | r-x         | Đọc + Thực thi       |
| 6      | rw-         | Đọc + Ghi            |
| 7      | rwx         | Đọc + Ghi + Thực thi |

vD: cần phân quyền cho một file có tên là `file1` quyền `rwxrw-r--`. Nó có nghĩa là user có tất cả quyền đọc, ghi, thực thi. Group có quyền đọc và ghi và other thì chỉ có quyền đọc. Để làm điều này ta cần tính quyền cho từng chủ sở hữu.

user: r + w +x = 4 + 2 + 1 = 7

group: r + w = 4 + 2 = 6

other: r = 4 = 4

- Vậy quyền của cả file sẽ là `764`, sau đó sử dụng lệnh sau để phân quyền:

`chmod 764 file1`

- Ngoài ra bạn cũng có thể tham khảo thêm câu lệnh

`chmod u=rwx,g=rw,o=r <filename>`

5. **Sử dụng chown và chgrp để Thay Đổi Chủ Sở Hữu và Nhóm:**

- `chown`: Là lệnh để thay đổi chủ sở hữu của tệp hoặc thư mục.
- `chgrp`: Là lệnh để thay đổi nhóm chủ sở hữu của tệp hoặc thư mục.

- Để thay đổi được bạn cần phải có quyền `sudo`.

    + Để thay đổi user: `sudo chown <username> <filename>`

    + Để thay đổi group: `sudo chgrp <groupname> <filename>`

    + Để thay đổi cả user và group:`sudo chown <username>:<groupname> <filename>`

6. **Quyền Truy Cập Các Tài Nguyên Hệ Thống:**

- Ngoài quyền trên tệp và thư mục, có cả quyền truy cập và thực hiện các hành động đặc biệt đối với các tài nguyên hệ thống khác như thiết bị, socket, pipe, và quyền thực thi.

7. **File Access Control Lists (ACLs):**

- ACLs: Là một cơ chế mở rộng để cung cấp kiểm soát quyền hạn chi tiết hơn đối với tệp và thư mục.

Tất cả những khái niệm này tạo nên một hệ thống quản lý quyền hạn mạnh mẽ trong Linux, giúp đảm bảo bảo mật và kiểm soát truy cập đối với tài nguyên hệ thống.