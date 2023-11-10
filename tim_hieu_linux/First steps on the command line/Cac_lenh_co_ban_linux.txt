# Các lệnh cơ bản trong linux:

## 1.Lệnh pwd
Trong Linux, **lệnh `pwd` (Print Working Directory)** được sử dụng để hiển thị đường dẫn đầy đủ của thư mục làm việc hiện tại. Khi bạn nhập `pwd` trong terminal, hệ thống sẽ trả về đường dẫn tuyệt đối của thư mục mà bạn đang làm việc.
Ví dụ: 
$ pwd
/home/username

Trong ví dụ trên, pwd hiển thị đường dẫn tuyệt đối của thư mục làm việc hiện tại là "/home/username".

## 2.Lệnh cd
**Lệnh `cd` (Change Directory)** trong Linux được sử dụng để di chuyển giữa các thư mục (directories). Bạn có thể sử dụng `cd` để chuyển đến một thư mục cụ thể hoặc di chuyển đến một vị trí tương đối trong hệ thống tệp.
Cú pháp sử dụng:
cd [đường_dẫn]

Nếu không cung cấp đường_dẫn, cd sẽ di chuyển bạn đến thư mục người dùng home (thường là /home/tên_người_dùng).

Ví dụ:

1. Di chuyển đến thư mục con bằng đường dẫn tương đối:
cd Documents

2. Di chuyển đến một đường dẫn tuyệt đối:
cd /path/to/directory

3. Di chuyển lên một thư mục:
cd ..

4. Di chuyển đến thư mục home của người dùng:
cd

## Lệnh mkdir
- **Lệnh mkdir (Make Directory)** trong Linux được sử dụng để tạo thư mục mới. Bạn có thể sử dụng mkdir để tạo một thư mục trong thư mục hiện tại hoặc tạo một thư mục với đường dẫn tuyệt đối.
Cú pháp sử dụng:
mkdir tên_thư_mục

Nếu muốn tạo thư mục với đường dẫn tuyệt đối:
mkdir /path/to/new_directory

- Lệnh **mkdir -p** trong Linux được sử dụng để tạo thư mục cùng với các thư mục cha (parent directories) nếu chúng không tồn tại. Nếu cần tạo một cây thư mục đầy đủ với các thư mục cha mà không cần phải kiểm tra từng thư mục cha có tồn tại hay không, tùy chọn -p là lựa chọn hữu ích.
Cú pháp sử dụng:
 mkdir -p đường_dẫn
Ví dụ:
mkdir -p /parents/child1/child2

Nếu **/parents/child1/** không tồn tại, lệnh trên sẽ tạo cả hai thư mục **/parents/** và **/parents/child1/** trước khi tạo thư mục **child2**.
Lựa chọn **-p** giúp tránh được lỗi khi cố tạo một thư mục trong một cấu trúc thư mục mà một số thư mục cha có thể chưa tồn tại.

## Lệnh rmdir
- Lệnh **rmdir** trong Linux được sử dụng để xóa các thư mục trống (thư mục không chứa tệp hoặc thư mục con). Lệnh này không thể xóa thư mục nếu nó chứa các tệp hoặc thư mục con.

Cú pháp sử dụng:
rmdir tên_thư_mục
Ví dụ: 
rmdir empty_directory

Nếu thư mục empty_directory không chứa bất kỳ tệp hoặc thư mục con nào, nó sẽ bị xóa.

Lưu ý rằng nếu thư mục không trống (có chứa nội dung), bạn sẽ nhận được một thông báo lỗi từ lệnh rmdir. Để xóa một thư mục và nội dung của nó, bạn có thể sử dụng lệnh rm -r (lưu ý rằng điều này cần phải thận trọng vì nó sẽ xóa tất cả nội dung bên trong thư mục).

- Lệnh **rmdir -p** trong Linux được sử dụng để xóa các thư mục cấp cao (parent directories) trống rỗng. Tùy chọn **-p** cho phép bạn xóa thư mục cấp cao nếu nó trống rỗng sau khi xóa thư mục cụ cụ thể. Nếu thư mục cấp cao trống rỗng sau khi xóa một thư mục cụ thể, thì thư mục cấp cao đó cũng sẽ bị xóa.

Cú pháp sử dụng:
rmdir -p thư_mục

Trong đó, **thư_mục** là thư mục bạn muốn xóa, và **-p** là tùy chọn cho phép xóa các thư mục cấp cao trống rỗng.

Ví dụ:
rmdir -p /parent/child1/child2

Nếu /parent/child1/child2 trống rỗng sau khi thư mục cuối cùng được xóa, thì cả đường dẫn /parent/child1/child2 cũng sẽ bị xóa.

Lưu ý rằng lệnh **rmdir** chỉ xóa thư mục nếu nó trống rỗng. Nếu thư mục chứa các tệp hoặc thư mục con, bạn có thể sử dụng lệnh **rm -r** để xóa thư mục và nội dung bên trong nó.

## Lệnh ls
- Lệnh ls trong Linux được sử dụng để liệt kê các tệp và thư mục trong thư mục hiện tại hoặc thư mục được chỉ định. Dưới đây là một số cú pháp cơ bản của lệnh **ls**:
### 1.Liệt kê các tệp và thư mục trong thư mục hiện tại:
ls

### 2.Liệt kê chi tiết với thông tin về quyền, kích thước, ngày tạo và tên tệp:
ls -l

### 3.Liệt kê tất cả các tệp và thư mục, kể cả các tệp và thư mục ẩn (bắt đầu bằng dấu chấm):
ls -a

### 4.Liệt kê tất cả các tệp và thư mục chi tiết, kể cả các tệp và thư mục ẩn:
ls -al

### 5.liệt kê tất cả các tệp và thư mục trong thư mục hiện tại, bao gồm cả các tệp và thư mục ẩn
ls -ah



