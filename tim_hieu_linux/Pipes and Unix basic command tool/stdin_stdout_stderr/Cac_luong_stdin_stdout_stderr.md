# Các luồng stdin,stdout,stderr
Trong Unix/Linux, có ba luồng (hoặc dòng) tiêu chuẩn mà mọi tiến trình có thể sử dụng để giao tiếp với môi trường xung quanh:

## 1. Standard Input (stdin):
- **Biểu tượng:`0`** 
- **Mô tả:** Là luồng đầu vào tiêu chuẩn. Thông thường, nó được kết nối với bàn phím, nhưng bạn cũng có thể chuyển hướng nó từ một tệp hoặc bất kỳ nguồn nào khác.
## 2. Standard Output (stdout):
- **Biểu tượng:`1`** 
- **Mô tả:** Là luồng đầu ra tiêu chuẩn. Kết quả của một chương trình thường được xuất ra luồng này. Mặc định, nó được kết nối với màn hình console, nhưng bạn có thể chuyển hướng nó đến một tệp hoặc luồng khác.
## 3. Standard Error (stderr):
- **Biểu tượng:`2`**
- **Mô tả:** Là luồng lỗi tiêu chuẩn. Nó được sử dụng để xuất thông báo lỗi và thông tin debug. Như stdout, stderr cũng có thể được chuyển hướng đến một tệp hoặc luồng khác.

Các luồng này thường được sử dụng trong việc đọc từ và ghi vào từ các tiến trình, làm cho quá trình tương tác với hệ thống và với nhau trở nên linh hoạt và mạnh mẽ.