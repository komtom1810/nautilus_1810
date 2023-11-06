# Sự khác nhau giữa nat và nat custom
Trong môi trường VMware, có hai chế độ NAT chính: NAT (Network Address Translation) và NAT Custom (Custom NAT). Dưới đây là sự khác nhau giữa chúng:

## 1/NAT (Network Address Translation):
- **Mặc định của VMware:** NAT là một chế độ mạng ảo mà VMware tự động cung cấp. Nó cho phép máy ảo kết nối với mạng ngoại vi thông qua máy chủ VMware và thực hiện chuyển đổi địa chỉ (NAT) để cho phép truy cập internet hoặc các máy tính trong mạng ngoại vi.
- **Không cần tùy chỉnh đặc biệt:** NAT không yêu cầu nhiều tùy chỉnh cụ thể từ người dùng và thường hoạt động tốt với cấu hình mạng mặc định của VMware.

## 2/NAT Custom (Custom NAT):
- **Yêu cầu tùy chỉnh:** NAT Custom cho phép bạn tùy chỉnh nhiều cài đặt mạng hơn so với NAT mặc định. Bạn có thể cấu hình địa chỉ IP ảo, cổng chuyển đổi (port forwarding), quản lý các luật tường lửa, và thay đổi nhiều cài đặt mạng khác để đáp ứng nhu cầu cụ thể của mạng của bạn.
- **Kiểm soát nhiều hơn:** NAT Custom cung cấp sự kiểm soát cao hơn và linh hoạt hơn đối với cách máy ảo của bạn kết nối với mạng ngoại vi và tương tác với internet. Bạn có thể cấu hình NAT Custom để đáp ứng các yêu cầu riêng của mạng hoặc ứng dụng cụ thể.

**Kết luận**, NAT là chế độ mạng ảo mặc định trong VMware với các cài đặt tiêu chuẩn, trong khi NAT Custom cho phép bạn tùy chỉnh nhiều cài đặt hơn để đáp ứng nhu cầu cụ thể của mạng hoặc ứng dụng của bạn. Chọn chế độ nào phù hợp với bạn phụ thuộc vào yêu cầu cụ thể của mạng và mục tiêu sử dụng của bạn.