# Các command filter với pipe
Khi sử dụng pipe (`|`) trong Linux, có thể kết hợp nhiều lệnh để tạo ra một chuỗi xử lý dữ liệu. Dưới đây là một số ví dụ về việc sử dụng pipe để lọc dữ liệu:

## 1. Sử dụng `grep` và `egrep`:
- Khi kết hợp với `grep`, một công cụ tìm kiếm văn bản, bạn có thể lọc các dòng chứa một chuỗi cụ thể từ đầu ra của lệnh trước đó.
Cú pháp là:
`command | grep "pattern"`

Trong đó:
    -`command` là lệnh đầu tiên, tạo ra đầu ra.
    -`grep` là công cụ tìm kiếm văn bản.
    -`"pattern"` là chuỗi cần tìm kiếm.

- Lệnh `egrep` là một biến thể của lệnh `grep` trong hệ điều hành Linux và các hệ điều hành tương tự. `egrep` tương đương với việc sử dụng `grep -E`, và nó hỗ trợ các biểu thức chính quy mở rộng (Extended Regular Expressions).
Cú pháp là:
`egrep "pattern" filename`

Trong đó: 
    - `"pattern"` là biểu thức chính quy mà bạn muốn tìm kiếm.
    - `filename` là tên của tệp tin bạn muốn tìm kiếm trong.
    - `egrep` cho phép sử dụng các biểu thức chính quy mở rộng mà không cần escape (`\`) một số ký tự so với `grep`. Cụ thể, `egrep` hỗ trợ ký tự `+`, `?`, `|`, `()` để thực hiện các phép toán như 1 hoặc nhiều lần xuất hiện, 0 hoặc 1 lần xuất hiện, phép toán "hoặc", và nhóm biểu thức.

VD, để tìm kiếm tất cả các dòng trong một tệp tin có chứa từ "apple" hoặc "orange", bạn có thể sử dụng:

`egrep "apple|orange" filename`

## 2.Sử dụng ``cut``: 
Lệnh `cut` được sử dụng để cắt (extract) các phần của các dòng từ một tệp tin hoặc đầu vào tiêu chuẩn và hiển thị chúng trên đầu ra tiêu chuẩn. `cut` thường được sử dụng để cắt các cột từ các tệp tin văn bản, sử dụng một số tiêu chí như byte, ký tự, hoặc trường (cột).

- **Cắt theo byte hoặc ký tự:**

 `cut -b 1-5 filename`  # Cắt từ byte 1 đến byte 5

 `cut -c 1-5 filename`  # Cắt từ ký tự 1 đến ký tự 5

- **Cắt theo trường (cột) sử dụng dấu phân tách mặc định (tab):**

 `cut -f 2 filename`  # Hiển thị nội dung của trường thứ 2

Mặc định, `cut` sử dụng ký tự tab làm dấu phân tách trường. Nếu dấu phân tách là ký tự khác, bạn có thể sử dụng tùy chọn `-d` để chỉ định.

`cut -d ',' -f 2 filename`  # Sử dụng dấu ',' làm dấu phân tách và hiển thị nội dung của trường thứ 2

- **Cắt từ kết quả của lệnh khác sử dụng pipe |:**
Khi sử dụng lệnh `cut` với pipe (`|`), bạn có thể cắt các trường (cột) từ đầu ra của một lệnh trước đó. VD: 

`command1 | cut -d ',' -f 2`

Trong đó:
    - `command1` là lệnh đầu tiên, tạo ra đầu ra.
    - `cut` là lệnh cắt.
    - `-d ','` chỉ định dấu phân tách là dấu `,`. Nếu dấu phân tách khác, bạn có thể thay đổi thành ký tự hoặc chuỗi phù hợp với đầu ra của `command1`.
    - `-f 2` chỉ định hiển thị nội dung của trường thứ 2. Bạn có thể thay đổi số để chọn trường khác.

## 3.Sử dụng `tr`: 
Lệnh `tr` trong Linux được sử dụng để thực hiện các biến đổi ký tự (character translation). Khi kết hợp với pipe (`|`), nó có thể được sử dụng để thực hiện các thay đổi trên đầu ra của một lệnh trước đó.

Dưới đây là một ví dụ sử dụng `tr` với pipe:

- **Thay thế ký tự:**
`echo "hello" | tr 'l' 'L'`

Kết quả: `heLLo`

- **Xóa ký tự:**
`echo "hello" | tr -d 'l'`

Kết quả: `heo`

- **Chuyển đổi chữ thường thành chữ in hoa và ngược lại:**
`echo "Hello" | tr 'a-zA-Z' 'A-Za-z'`

Kết quả: hELLO

- **Xóa các ký tự không thuộc tập ký tự cho trước:**
`echo "a1b2c3" | tr -cd '0-9'`

Kết quả: `123`

- **Xóa các dấu cách dư thừa:**
`echo "   too    many    spaces   " | tr -s ' '`

Kết quả: `too many spaces`

## 4.Sử dụng `wc`
Lệnh `wc` được sử dụng để đếm số lượng dòng, số lượng từ, và số lượng ký tự trong một tệp tin hoặc từ đầu vào tiêu chuẩn.

Dưới đây là một số cú pháp cơ bản của lệnh `wc`:

- **Đếm số lượng dòng, từ, và ký tự trong một tệp tin:**
`wc filename`

Kết quả:
`số_lượng_dòng số_lượng_từ số_lượng_ký_tự filename`

- **Đếm từng dòng từ đầu vào tiêu chuẩn (thường là đầu ra của một lệnh trước đó):**
`command1 | wc`

Kêt quả: `số_lượng_dòng số_lượng_từ số_lượng_ký_tự`

- **Chỉ đếm số lượng dòng:**
`wc -l filename`

Kết quả sẽ chỉ hiển thị số lượng dòng.

- **Chỉ đếm số lượng từ:**
`wc -w filename`

Kết quả sẽ chỉ hiển thị số lượng từ.

- **Chỉ đếm số lượng ký tự:**
`wc -c filename`

Kết quả sẽ chỉ hiển thị số lượng ký tự.

## 5.Sử dụng sort 
Lệnh `sort` trong Linux được sử dụng để sắp xếp các dòng trong một tệp tin. Dưới đây là một số cú pháp cơ bản của lệnh `sort`:

- **Sắp xếp các dòng trong tệp tin:**
`sort filename`

Kết quả sẽ là các dòng được sắp xếp theo thứ tự từ điển.

- **Sắp xếp và hiển thị dòng duy nhất (loại bỏ các dòng trùng lặp):** 
`sort -u filename`

Kết quả sẽ là các dòng được sắp xếp và không có dòng nào lặp lại.

- **Sắp xếp và hiển thị dòng theo thứ tự ngược đảo:**
`sort -r filename`

Kết quả sẽ là các dòng được sắp xếp theo thứ tự ngược đảo.

- **Sắp xếp theo cột cụ thể (ví dụ: cột thứ 2):**
`sort -k2 filename`

Kết quả sẽ là các dòng được sắp xếp dựa trên nội dung của cột thứ 2.

- **Sắp xếp và hiển thị số liệu số theo thứ tự tăng dần hoặc giảm dần:**
`sort -n filename   # Tăng dần`

`sort -nr filename  # Giảm dần`

Kết quả sẽ là các dòng được sắp xếp dựa trên giá trị số (nếu có) trong tệp tin.

## 6.Sử dụng `sed` 
Lệnh `sed` (stream editor) trong Linux được sử dụng để thực hiện các biến đổi trên văn bản từ đầu vào (hoặc tệp tin). Nó thường được sử dụng trong các kịch bản và các ứng dụng dòng lệnh để thay đổi, thêm, hoặc xóa nội dung trong văn bản. Dưới đây là một số cú pháp cơ bản của lệnh `sed`:

- **Thay thế một chuỗi bằng chuỗi khác trên mỗi dòng:**
#Tạo một tệp tin ví dụ

`echo "Hello, world!" > example.txt`

#Thay thế "world" bằng "universe" trong tệp tin

`sed 's/world/universe/' example.txt`


Kết quả sẽ là `Hello, universe!`

- **Thay thế tất cả các xuất hiện của một chuỗi trên mỗi dòng:**

`echo "apple orange apple banana" | sed 's/apple/fruit/g'`

Kết quả sẽ là `fruit orange fruit banana`

- **Xóa dòng chứa một chuỗi cụ thể:**

`echo -e "apple\norange\nbanana" | sed '/orange/d'`

Kết quả sẽ là 
`apple`
`banana`

- **In các dòng chỉ định:**

`echo -e "one\ntwo\nthree" | sed -n '2p'`

Kết quả sẽ là `two`

## 7.Sử dụng `awk`
Lệnh `awk` trong Linux là một công cụ mạnh mẽ cho việc xử lý và hiển thị văn bản trong các kịch bản và ứng dụng dòng lệnh. Dưới đây là một số ví dụ về cách sử dụng lệnh `awk`:

- **Hiển thị một cột cụ thể từ mỗi dòng**

`echo "Name Age City" | awk '{print $2}'`

Kết quả: `Age`

- **Tính tổng của một cột số**

`echo -e "10\n20\n30" | awk '{sum += $1} END {print "Total:", sum}'`

Kết quả: `Total: 60`

- Hiển thị tên và tuổi từ một file văn bản

Name   Age

Ducanh 22

Duoc   25

`awk 'NR>1 {print $1, $2}' data.txt`

Kết quả:

`John 25`

`Jane 30`

## 8.Sử dụng `comm`
Lệnh `comm` trong Linux được sử dụng để so sánh hai tệp tin đã được sắp xếp và hiển thị các dòng chung và các dòng chỉ xuất hiện trong một hoặc cả hai tệp tin. Dưới đây là cú pháp cơ bản của lệnh `comm`:

`comm [OPTION]... FILE1 FILE2`

Trong đó:

`FILE1` và `FILE2` là hai tệp tin đã được sắp xếp trước.

Các tùy chọn thường được sử dụng:

- `-1`: Hiển thị các dòng chỉ xuất hiện trong `FILE1`.
- `-2`: Hiển thị các dòng chỉ xuất hiện trong `FILE2`.
- `-3`: Hiển thị các dòng chung của cả hai tệp tin.
- `--check-order`: Kiểm tra xem các tệp tin có được sắp xếp không.
VD:

- **Hiển thị các dòng chung**

`comm file1 file2`

- **Hiển thị các dòng chỉ xuất hiện trong file1**

`comm -23 file1 file2`

- **Hiển thị các dòng chỉ xuất hiện trong file2**

`comm -13 file1 file2`

- K**iểm tra xem các tệp tin đã được sắp xếp không**

`comm --check-order file1 file2`

Lưu ý rằng lệnh `comm` yêu cầu các tệp tin đầu vào phải được sắp xếp trước. Nếu chúng không được sắp xếp, bạn có thể sử dụng lệnh `sort` để sắp xếp chúng trước khi sử dụng `comm`.

## 9.Sử dung `diff`
Lệnh `diff` trong Linux được sử dụng để so sánh nội dung của hai tệp tin và hiển thị sự khác biệt giữa chúng. Dưới đây là một số ví dụ về cách sử dụng lệnh `diff`:

**Cú pháp cơ bản:**

`diff [tùy_chọn] tệp_tin_1 tệp_tin_2`

**Một số tùy chọn phổ biến:**

- `-u, --unified`: Hiển thị đầu ra trong định dạng thống nhất (thường được sử dụng).
- `-c, --context`: Hiển thị đầu ra trong định dạng ngữ cảnh.
- `-r, --recursive`: So sánh thư mục và nội dung của chúng.
- `-q, --brief`: Chỉ hiển thị thông báo nếu có sự khác biệt, không hiển thị đầu ra chi tiết.

**Ví dụ:**

- **So sánh hai tệp tin và hiển thị sự khác biệt:**
`diff file1.txt file2.txt`

- **So sánh hai thư mục và hiển thị sự khác biệt (đối với thư mục, bạn cần sử dụng -r):**
`diff -r directory1 directory2`

- **So sánh và hiển thị đầu ra trong định dạng thống nhất:**
`diff -u file1.txt file2.txt`

- **So sánh hai thư mục và hiển thị đầu ra trong định dạng ngữ cảnh:**
`diff -c directory1 directory2`

- **So sánh và chỉ hiển thị thông báo nếu có sự khác biệt:**
`diff -q file1.txt file2.txt`

Lệnh `diff` là một công cụ mạnh mẽ khi bạn cần xem xét sự khác biệt giữa các tệp tin hoặc thư mục, và có thể được tích hợp trong quá trình kiểm thử mã nguồn, quản lý mã nguồn, hoặc chỉ đơn giản là để xác định những thay đổi nhanh chóng.





