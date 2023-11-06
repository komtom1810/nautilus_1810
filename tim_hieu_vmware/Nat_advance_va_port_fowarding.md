# Port forwarding

Port forwarding trong mạng NAT (Network Address Translation) cho phép bạn định tuyến lưu lượng từ cổng bên ngoài của router của bạn đến một máy tính hoặc thiết bị cụ thể trong mạng nội bộ của bạn. Điều này có thể hữu ích khi bạn muốn cung cấp truy cập từ bên ngoài vào các dịch vụ hoặc ứng dụng trong mạng LAN của bạn thông qua mạng NAT. Dưới đây là cách thực hiện port forwarding trong mạng NAT:

 **1. Xác định Mục tiêu:** Xác định máy tính hoặc thiết bị trong mạng LAN của bạn mà bạn muốn định tuyến lưu lượng đến. Bạn cần biết địa chỉ IP của máy tính này và cổng mà bạn muốn định tuyến.

 **2. Truy cập Giao diện Quản trị Router:** Truy cập giao diện quản trị của router hoặc thiết bị NAT. Để làm điều này, bạn cần biết địa chỉ IP của router. Thường, bạn truy cập giao diện quản trị bằng cách nhập địa chỉ IP của router vào trình duyệt web (ví dụ: http://192.168.1.1).

 **3. Đăng nhập và Tìm cài đặt Port Forwarding:** Đăng nhập vào giao diện quản trị của router bằng tên người dùng và mật khẩu. Sau đó, tìm cài đặt port forwarding hoặc virtual server trong giao diện quản trị của router. Thường, bạn sẽ tìm thấy nó trong mục "Advanced" hoặc "Port Forwarding" của giao diện quản trị.

 **4. Cấu hình Port Forwarding:**

- Trong cài đặt port forwarding, bạn cần cung cấp thông tin sau:
- **Cổng bên ngoài (External Port):** Đây là cổng mà bạn muốn người dùng bên ngoài sử dụng để - - truy cập dịch vụ hoặc ứng dụng.
- **Cổng trong mạng LAN (Internal Port):** Đây là cổng của máy tính hoặc thiết bị trong mạng LAN mà bạn muốn định tuyến lưu lượng đến.
- **Địa chỉ IP của Mục tiêu (Internal IP Address):** Đây là địa chỉ IP của máy tính hoặc thiết bị trong mạng LAN mà bạn muốn định tuyến lưu lượng đến.
- **Giao thức (Protocol):** Chọn giao thức (TCP, UDP, hoặc cả hai) bạn muốn định tuyến.
 **5. Lưu và Kích hoạt:** Sau khi cấu hình port forwarding, lưu cài đặt và kích hoạt chúng. Sau đó, router sẽ bắt đầu định tuyến lưu lượng từ cổng bên ngoài đến máy tính hoặc thiết bị trong mạng LAN của bạn.

# Nat Advance

"Advanced Network Address Translation" (NAT) là một loại NAT cao cấp hoặc mở rộng được sử dụng trong các mạng máy tính để biến đổi địa chỉ IP và cổng (port) để điều hướng lưu lượng mạng từ bên ngoài vào mạng nội bộ. Advanced NAT cung cấp nhiều tính năng và kiểm soát mạng cao hơn so với NAT cơ bản, giúp quản lý hiệu suất và bảo mật của mạng một cách tốt hơn.

Dưới đây là một số tính năng và ứng dụng của Advanced NAT:

**1. Port Forwarding:** Advanced NAT cho phép định tuyến lưu lượng từ một cổng bên ngoài đến một cổng cụ thể trong mạng nội bộ. Điều này hữu ích khi bạn muốn cung cấp truy cập từ bên ngoài vào các dịch vụ hoặc ứng dụng cụ thể trong mạng LAN.

**2. Dynamic Port Allocation:** Advanced NAT có thể tự động cấp phát cổng cụ thể cho các kết nối mạng động. Điều này giúp giảm xung đột cổng và tối ưu hóa sử dụng tài nguyên.

**3. Load Balancing:** Advanced NAT có thể sử dụng để phân phối lưu lượng mạng đến nhiều máy chủ hoặc thiết bị dưới dạng cụm. Điều này giúp cân bằng tải trên các máy chủ và cải thiện hiệu suất.

**4. Network Address Pooling:** Advanced NAT cho phép quản lý cụm địa chỉ IP nội bộ và phân phối chúng theo cách linh hoạt.

**5. Security and Access Control:** Advanced NAT cung cấp kiểm soát quyền truy cập và bảo mật, cho phép bạn xác định ràng buộc về quyền truy cập dựa trên địa chỉ IP và cổng.

**6. VPN Support:** Advanced NAT có khả năng hỗ trợ kết nối mạng riêng ảo (VPN) và chuyển tiếp các loại lưu lượng VPN đặc biệt.

**7. Monitoring and Logging:** Advanced NAT thường đi kèm với các công cụ theo dõi và ghi log để theo dõi lưu lượng và sự kiện trong mạng.

Advanced NAT thường được sử dụng trong môi trường doanh nghiệp và trong các mạng lớn hơn, nơi quản lý và bảo mật mạng là một ưu tiên quan trọng. Các sản phẩm tường lửa và router mạng doanh nghiệp thường tích hợp Advanced NAT và cung cấp nhiều tính năng cao cấp cho quản lý mạng.




