Trong Linux, đường dẫn tương đối và đường dẫn tuyệt đối là hai khái niệm quan trọng khi làm việc với hệ thống tệp và thư mục.

## 1.Đường dẫn Tương đối:

- **Đặc điểm:** Đường dẫn tương đối là đường dẫn được xác định dựa trên vị trí hiện tại.
- **Ví dụ:** Giả sử bạn đang ở trong thư mục **/home/user/** và muốn truy cập tệp **document.txt** trong thư mục **/home/user/documents/**. Đường dẫn tương đối trong trường hợp này là:
 cd documents
 cat document.txt
**Lưu ý:** Đường dẫn tương đối sẽ thay đổi tùy thuộc vào vị trí hiện tại của bạn trong hệ thống tệp.
## 2.Đường dẫn Tuyệt đối:

- **Đặc điểm:** Đường dẫn tuyệt đối là đường dẫn đầy đủ từ thư mục gốc (root).
- **Ví dụ:** Nếu bạn muốn truy cập tệp **document.txt** trong thư mục **/home/user/documents/**, có thể sử dụng đường dẫn tuyệt đối như sau:
 cat /home/user/documents/document.txt
- **Lưu ý:** Đường dẫn tuyệt đối không phụ thuộc vào vị trí hiện tại của bạn.

Lựa chọn giữa đường dẫn tương đối và tuyệt đối phụ thuộc vào ngữ cảnh sử dụng. Đối với các tác vụ nâng cao tính linh hoạt và di động, đường dẫn tương đối có thể là lựa chọn tốt, trong khi đường dẫn tuyệt đối thường được sử dụng trong các tác vụ cần độ chính xác cao.

