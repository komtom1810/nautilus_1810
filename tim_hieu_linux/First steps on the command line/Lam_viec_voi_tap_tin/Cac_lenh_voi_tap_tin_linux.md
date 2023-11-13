# Các lệnh với tập tin linux

## 1.Lệnh file
Lệnh **file** trong Linux được sử dụng để xác định loại nội dung của một tệp tin. Nó kiểm tra dữ liệu trong tệp và xuất ra một mô tả của loại nội dung, ví dụ như văn bản ASCII, hình ảnh JPEG, tệp tin nhị phân, v.v. Dưới đây là cú pháp cơ bản của lệnh file:
file tên_tệp

Một số tùy chọn thường được sử dụng:
- **Hiển thị thông tin chi tiết:**
file -i tên_tệp. 
Kết quả sẽ bao gồm loại MIME của tệp.

- **Hiển thị thông tin với tên tệp đầy đủ:**
file -b tên_tệp. 
Kết quả sẽ không chứa tên tệp mà chỉ là thông tin về loại nội dung.

- **Kiểm tra nhiều tệp:**
file tệp1 tệp2 tệp3. 
Lệnh này kiểm tra nhiều tệp cùng một lúc.

Lệnh **file** là một công cụ hữu ích khi muốn biết loại nội dung của một tệp tin mà không cần mở nó

## 2.Lệnh touch
Lệnh **touch** trong Linux được sử dụng để tạo mới một tệp mới hoặc cập nhật thời gian sửa đổi của một tệp đã tồn tại mà không cần thay đổi nội dung của tệp. Dưới đây là cú pháp cơ bản của lệnh **touch**:
touch tên_tệp

Nếu tệp đã tồn tại, lệnh touch sẽ cập nhật thời gian sửa đổi của tệp mà không làm thay đổi nội dung của nó. Nếu tệp không tồn tại, nó sẽ tạo một tệp mới.

Một số tùy chọn phổ biến:
- **Tạo nhiều tệp cùng một lúc:**
touch tệp1 tệp2 tệp3

- **Cập nhật thời gian truy cập và thời gian sửa đổi của tệp:**
touch -a tên_tệp. 
Tùy chọn -a sẽ cập nhật thời gian truy cập của tệp.

- **Tạo tệp mới với nội dung mẫu:**
touch tên_tệp && echo "Nội dung mẫu" > tên_tệp. 
Lệnh trên sẽ tạo một tệp mới và điền nội dung mẫu vào đó.

## 3.Lệnh cp
Lệnh **cp** trong Linux được sử dụng để sao chép tệp và thư mục từ một vị trí đến vị trí khác. Dưới đây là cú pháp cơ bản của lệnh **cp**:
cp [tùy_chọn] nguồn đích

Dưới đây là một số tùy chọn thường được sử dụng với lệnh **cp**:
- **Sao chép tệp đến một thư mục:**
cp tệp nguồn_thư_mục

- **Sao chép nhiều tệp đến một thư mục:**
cp tệp1 tệp2 tệp3 nguồn_thư_mục

- **Sao chép thư mục và nội dung của nó đến một thư mục khác:**
cp -r thư_mục nguồn_thư_mục. 
Tùy chọn **-r** hoặc **-R** là để sao chép thư mục và nội dung của nó (recursively).

- **Ghi đè tệp mà không cần xác nhận (force):**
cp -f nguồn đích

- **Hiển thị thông báo khi ghi đè (interactive):**
cp -i nguồn đích

- **Sao chép tất cả các tệp, bao gồm cả những tệp ẩn (all):**
cp -a nguồn đích. 
Tùy chọn **-a* thường được sử dụng để duy trì tất cả các thông tin về tệp, bao gồm cả quyền và ngày tạo.

## 4.Lệnh mv
Lệnh **mv** trong Linux được sử dụng để di chuyển hoặc đổi tên tệp và thư mục. Dưới đây là cú pháp cơ bản của lệnh **mv**:
mv [tùy_chọn] nguồn đích

- **Di chuyển tệp đến một thư mục khác:**
mv tên_tệp nguồn_thư_mục

- **Di chuyển thư mục và nội dung của nó đến một thư mục khác:**
mv thư_mục nguồn_thư_mục. 
Tùy chọn -r hoặc -R là để di chuyển thư mục và nội dung của nó (recursively).

- **Di chuyển nhiều tệp đến một thư mục:**
mv tệp1 tệp2 tệp3 nguồn_thư_mục

- **Di chuyển và đổi tên tệp hoặc thư mục:**
mv tên_cũ tên_mới

- **Ghi đè tệp mà không cần xác nhận (force):**
mv -f nguồn đích

- **Hiển thị thông báo khi ghi đè (interactive):**
mv -i nguồn đích

- **Ghi đè tệp mà có thông báo, nếu không thì tạo bản sao (backup):**
mv -b nguồn đích

## 5.Lệnh rm
Lệnh **rm** trong Linux được sử dụng để xóa tệp tin hoặc thư mục. Dưới đây là cú pháp cơ bản của lệnh **rm**:
rm [tùy_chọn] tên_tệp_/_thư_mục

Một số tùy chọn phổ biến:
- **Xóa một tệp:**
rm tên_tệp

- **Xóa nhiều tệp cùng một lúc:**
rm tệp1 tệp2 tệp3

- **Xóa thư mục và nội dung của nó:**
rm -r tên_thư_mục.
Tùy chọn -r hoặc -R là để xóa thư mục và nội dung của nó (recursively).

- **Xóa mà không hiển thị thông báo xác nhận (force):**
rm -f tên_tệp_/_thư_mục

- **Hiển thị thông báo xác nhận trước khi xóa (interactive):**
rm -i tên_tệp_/_thư_mục

- **Xóa tệp và tạo bản sao (backup) trước khi xóa:**
rm -b tên_tệp

- **Xóa tất cả các tệp trong thư mục hiện tại (chú ý: rất nguy hiểm):**
rm *

Lưu ý rằng lệnh **rm** không di chuyển tệp vào thùng rác mà ngay lập tức xóa chúng. Hãy chắc chắn rằng bạn sử dụng lệnh **rm** một cách cẩn thận, đặc biệt là khi sử dụng tùy chọn **-r** để xóa thư mục và nội dung của nó, vì thao tác này không thể đảo ngược và sẽ mất hết dữ liệu.

