# Gateway của 3 kiểu mạng(Bridged, Host-only, NAT):
## 1/Bridge
- Trong môi trường VMware, khi cấu hình một card mạng ở chế độ bridged (bridge network), gateway của card mạng bridged sẽ phụ thuộc vào cấu hình mạng nơi máy ảo VMware đang chạy. Thường thì gateway của card mạng bridged trong VMware sẽ là gateway mạng của mạng local mà máy ảo đang được kết nối thông qua chế độ bridged.

- Ví dụ, nếu máy ảo VMware đang chạy trên một máy tính trong mạng cục bộ của bạn và được cấu hình để sử dụng một card mạng ở chế độ bridged, thì gateway của card mạng bridged sẽ là địa chỉ IP của router hoặc gateway mạng cục bộ của bạn. Điều này cho phép máy ảo truy cập vào các mạng khác hoặc internet thông qua thiết bị định tuyến của mạng cục bộ đó.

## 2/Host-only
- Trong môi trường VMware, khi cấu hình một card mạng ở chế độ "Host-Only" (chế độ chỉ hoạt động trong mạng nội bộ của máy ảo và máy chủ VMware), gateway của card mạng host-only thường sẽ có địa chỉ IP của máy chủ VMware (VMware host) chứ không phải là một gateway tiêu chuẩn ngoài mạng.

- Máy chủ VMware sẽ đóng vai trò như một gateway ảo cho máy ảo chạy trong môi trường host-only. Nó cung cấp kết nối giữa các máy ảo trong cùng mạng host-only và không có kết nối với mạng ngoài hoặc internet. Thông thường, địa chỉ IP của máy chủ VMware sẽ là địa chỉ gateway mặc định cho máy ảo trong mạng host-only.

## 3/NAT
- Trong môi trường VMware, khi cấu hình một card mạng ở chế độ NAT (Network Address Translation), gateway của card mạng NAT thường sẽ là một địa chỉ IP ảo được quản lý bởi VMware.

- Mạng NAT trong VMware cho phép máy ảo truy cập internet thông qua máy chủ VMware, và máy chủ VMware sẽ thực hiện chuyển đổi địa chỉ (NAT) để cho phép gửi và nhận dữ liệu qua mạng ngoại vi. Gateway của card mạng NAT thường là địa chỉ IP của máy chủ VMware hoặc một địa chỉ IP ảo trên máy chủ VMware, mà VMware sử dụng để định tuyến gói tin giữa máy ảo và internet hoặc mạng ngoại vi.
