# /proc/bus
Thư mục `/proc/bus` trong hệ thống tệp Linux thường không tồn tại. Tuy nhiên, thông tin về các bus (giao diện tương tác với các thiết bị) thường được hiển thị trong thư mục `/proc/bus` thông qua các thư mục con như `/proc/bus/pci` hoặc `/proc/bus/usb`.

1. `/proc/bus/pci`:

- Chứa thông tin về các thiết bị PCI (Peripheral Component Interconnect).
- Bạn có thể tìm thấy các thông tin như địa chỉ PCI, ID của nhà sản xuất, ID của thiết bị, v.v.

2. `/proc/bus/usb`:

- Chứa thông tin về các thiết bị USB (Universal Serial Bus).
- Bạn có thể tìm thấy các thông tin như địa chỉ USB, ID của nhà sản xuất, ID của thiết bị, v.v.
Nếu bạn muốn biết thêm thông tin cụ thể về các bus cụ thể trên hệ thống của mình, bạn có thể kiểm tra nội dung của các thư mục con bên trong `/proc/bus`. Sử dụng các lệnh như ls để liệt kê nội dung của thư mục và `cat` để xem nội dung của các tệp tin trong thư mục đó.

Lưu ý rằng thông tin trong `/proc` thường là ảo và được tạo ra khi hệ thống được khởi động. Nó cung cấp một cách để truy cập và hiển thị thông tin hệ thống một cách động.