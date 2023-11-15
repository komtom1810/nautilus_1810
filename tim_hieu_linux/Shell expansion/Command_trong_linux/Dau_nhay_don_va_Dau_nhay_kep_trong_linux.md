# Dấu nháy đơn và dấu nháy kép trong linux
Sự khác biệt giữa dấu `'` (nháy đơn) và `"` (nháy kép) đôi khi quan trọng, vì chúng ảnh hưởng đến cách shell xử lý các ký tự bên trong chúng. Dưới đây là một số điểm quan trọng:

## 1.Xử lý Biến và Biểu thức:

- **Nháy đơn:** Mọi thứ bên trong nháy đơn được xem như một chuỗi không thay đổi (literal string). Các biến và biểu thức không được xử lý. Ví dụ:

**`fruit="apple"
echo 'The value of $fruit is $fruit'`**
Kết quả: **`The value of $fruit is $fruit`**

- **Nháy kép:** Biến và biểu thức bên trong nháy kép sẽ được đánh giá và thay thế bởi giá trị thực tế của chúng. Ví dụ:

**`fruit="apple"
echo "The value of \$fruit is $fruit"`**
Kết quả: **`The value of $fruit is apple`**

## 2.Xử lý Ký tự Escape:

- **Nháy đơn:** Ký tự escape (ví dụ: \') không có tác dụng, và ký tự backslash (\) được xem như là chính nó.
- **Nháy kép:** Ký tự escape được xử lý. Ví dụ:

**`echo "This is a single quote: '\''"`**
Kết quả: **`This is a single quote: '`**

## 3.Command Substitution:

- **Nháy đơn:** Command substitution (chèn kết quả của một lệnh vào trong một chuỗi) không hoạt động bên trong nháy đơn.
- **Nháy kép:** Command substitution hoạt động, ví dụ:

**`echo "Today is $(date)"`**
Kết quả: **`Today is [current date and time]`**

Tùy thuộc vào yêu cầu cụ thể, có thể chọn sử dụng nháy đơn hoặc nháy kép trong các tình huống khác nhau. Thông thường, nếu muốn bảo toàn đối số chính là chuỗi gốc mà không thay đổi giá trị của biến hay thực hiện command substitution, sẽ sử dụng nháy đơn. Ngược lại, nếu muốn thực hiện thay thế giá trị biến hoặc command substitution, sẽ sử dụng nháy kép.





