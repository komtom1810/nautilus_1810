# Unix command tool

## 1. File
Lệnh này được sử dụng để xác định loại của một tệp tin.

**Cú pháp cơ bản:** `file [tên_tệp_tin]`

- **Xác định loại của một tệp tin:**
`file example.txt`

Kết quả có thể là như sau:

`example.txt: ASCII text`

- **Kiểm tra loại của một thư mục:**
`file /path/to/directory`

Kết quả có thể là như sau:

`/path/to/directory: directory`

- **Kiểm tra loại của một ứng dụng thực thi:**
`file /usr/bin/python3`

Kết quả có thể là như sau:

`/usr/bin/python3: ELF 64-bit LSB shared object, x86-64, ...`

## 2. Locate
Lệnh ``locate`` trong Linux được sử dụng để tìm kiếm các tệp tin và thư mục dựa trên cơ sở dữ liệu `locate`, giúp tìm kiếm nhanh chóng mà không cần quét toàn bộ hệ thống tệp và thư mục.

**Cú pháp cơ bản:**
`locate [tên_tệp_tin]`

VD:

- **Tìm kiếm một tệp tin cụ thể:**
`locate myfile.txt`

Kết quả có thể là đường dẫn đầy đủ của tệp tin nếu nó tồn tại trong cơ sở dữ liệu locate.

- **Tìm kiếm tất cả các tệp tin và thư mục có chứa một từ khóa:**
`locate keyword`

Kết quả sẽ là danh sách các đường dẫn của tất cả các tệp tin và thư mục có chứa từ khóa "keyword".

**Lưu ý:**

- `locate` sử dụng cơ sở dữ liệu được cập nhật định kỳ để thực hiện tìm kiếm nhanh chóng. Tuy nhiên, để đảm bảo rằng cơ sở dữ liệu là mới nhất, bạn có thể cần chạy lệnh `sudo updatedb` để cập nhật nó.

`sudo updatedb`

- Nếu không thấy kết quả mong muốn, hãy chắc chắn rằng tệp tin đó đã được thêm vào cơ sở dữ liệu locate bằng cách chạy `updatedb`.

- Lệnh `locate` có thể không trả về kết quả ngay lập tức sau khi bạn tạo hoặc di chuyển một tệp tin mới. Bạn có thể cần đợi đến lúc cơ sở dữ liệu `locate` được cập nhật (hoặc cập nhật nó bằng lệnh `updatedb`).

## 3. Hostnamectl
Lệnh `hostnamectl` trong Linux là một công cụ mạnh mẽ cho việc quản lý thông tin về hostname (tên máy tính) và các thuộc tính hệ thống khác. Dưới đây là một số ví dụ về cách sử dụng `hostnamectl`:

- **Hiển thị thông tin chi tiết về hệ thống:**
`hostnamectl`

- **Hiển thị tên máy tính:**
`hostnamectl --static`

- **Hiển thị tên máy tính đầy đủ (bao gồm cả tên miền nếu có):**
`hostnamectl --transient`

- **Thay đổi tên máy tính tạm thời (không giữ lại sau khi khởi động lại):**
`sudo hostnamectl set-hostname newhostname`

- **Thay đổi tên máy tính vĩnh viễn:**
`sudo hostnamectl set-hostname newhostname --static`

- **Hiển thị các thuộc tính chi tiết của hệ thống:**
`hostnamectl status`

- **Hiển thị tất cả các thuộc tính hệ thống có thể:**
`hostnamectl list-properties`

## 4. Timedatectl
Lệnh `timedatectl` trong Linux là một công cụ quản lý thời gian và ngày giờ hệ thống. Dưới đây là một số ví dụ về cách sử dụng `timedatectl`:

- **Hiển thị thời gian hệ thống:**
`timedatectl`

- **Hiển thị thông tin chi tiết về múi giờ hệ thống:**
`timedatectl status`

- **Hiển thị danh sách các múi giờ có sẵn:**
`timedatectl list-timezones`

- **Thay đổi múi giờ hệ thống:**
`sudo timedatectl set-timezone Asia/Ho_Chi_Minh`

## 5. Sleep
Lệnh `sleep` trong Linux được sử dụng để tạm thời làm cho một tiến trình ngủ (chờ) trong một khoảng thời gian cụ thể. Dưới đây là cú pháp cơ bản và một số ví dụ:

**Cú pháp cơ bản:**

`sleep [thời_gian]`

`thời_gian`: Số giây (có thể là số thập phân) hoặc chuỗi thời gian, ví dụ, "5s" cho 5 giây hoặc "2m" cho 2 phút.

**Ví dụ:**

- Ngủ trong 5 giây: `sleep 5`
- Ngủ trong 2 phút: `sleep 2m`
- Ngủ trong 1 giờ: `sleep 1h`
- Ngủ trong 0.5 giây: `sleep 0.5`
- Ngủ trong 3 giây và in ra thông báo sau khi tỉnh dậy:

`sleep 3 && echo "Đã tỉnh dậy sau 3 giây!"`

Lệnh `sleep` thường được sử dụng trong các kịch bản shell và các tình huống khi bạn muốn giữ tiến trình đang chạy ngủ trong một khoảng thời gian nhất định trước khi thực hiện các bước tiếp theo.

## 6.Tar
Lệnh `tar` trong Linux được sử dụng để tạo và quản lý các file nén (archive). Dưới đây là một số ví dụ cơ bản về cách sử dụng lệnh `tar`:

**Cú pháp cơ bản:**

`tar [tùy_chọn] [tên_tệp_archive] [đường_dẫn_tệp_đích]`

**Một số tùy chọn phổ biến:**

- `-c, --create`: Tạo một file archive mới.
- `-x, --extract`: Giải nén một file archive.
- `-v, --verbose`: Hiển thị quá trình làm việc chi tiết.
- `-f, --file`: Xác định tên của file archive.
- `-z, --gzip`: Sử dụng gzip để nén/giải nén (dùng cho các file có đuôi .tar.gz hoặc .tgz).
- `-j, --bzip2`: Sử dụng bzip2 để nén/giải nén (dùng cho các file có đuôi .tar.bz2 hoặc .tbz2).
- `-r, --append`: Thêm file vào trong một archive đã có.
- `-t, --list`: Liệt kê các file trong archive.
- `-u, --update`: Thêm các file mới hơn vào trong một archive đã có.
- `-C, --directory`: Chuyển đến thư mục trước khi thực hiện các thao tác.

**Ví dụ:**

- **Tạo một file archive từ một thư mục:**
`tar -cvf archive.tar /đường/dẫn/thư/mục`

- **Nén một file archive bằng gzip:**
`tar -cvzf archive.tar.gz /đường/dẫn/thư/mục`

- **Giải nén một file archive:**
`tar -xvf archive.tar`

- **Liệt kê nội dung của một file archive:**
`tar -tvf archive.tar`

- **Thêm một file vào trong một archive đã có:**
`tar -rvf archive.tar newfile.txt`

- **Giải nén một file archive bằng bzip2:**
`tar -xvjf archive.tar.bz2`

Lưu ý rằng các tùy chọn và định dạng có thể thay đổi tùy thuộc vào phiên bản cụ thể của lệnh `tar`. Hãy kiểm tra tài liệu hoặc sử dụng tùy chọn `man tar` để biết thêm chi tiết.


- 