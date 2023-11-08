# Hướng dẫn Cài Đặt Hệ Điều Hành LINUX trên PC và Máy Ảo 

# 1.Có nên cài đặt hệ điều hành Linux không?
- Hệ điều hành Linux là hệ điều hành **mã nguồn mở**, có thể tải được mã nguồn của các phần mềm có sẵn, nghiên cứu chạy nhiều chương trình và cách vận hành của chương trình theo ý của mình
- **Có độ an toàn cao**, vì bạn sử dụng các phần mềm từ kho dữ liệu chính thức nên sẽ không xảy ra trường hợp dính mã độc hại
- Có thể chạy được trên hầu như các đời máy từ cấu hình cao đến cấu hình thấp, tối thiểu là RAM 512MB
- Hỗ trợ tốt cho các lập trình viên, coder vì Linux hỗ trợ nhiều cho nhiều ngôn ngữ như C, C++, Java, Python,…
- Là hệ điều hành mã nguồn mở nên Linux hoàn toàn **miễn phí**

# 2.Hướng dẫn cài đặt hệ điều hành LINUX trên PC và máy ảo
Hệ điều hành Linux chia ra nhiều phiên bản/bản phân phối hệ điều hành khác nhau như: **Ubuntu, Debian, CentOS,…** Tại bài viết này, LANIT sẽ hướng dẫn bạn cách cài đặt 2 hệ điều hành phổ biến nhất là CentOS và Ubuntu.

# 2.1Hướng dẫn cài đặt hệ điều hành CentOS 7
**CentOS** là một hệ điều hành nguồn mở dựa trên mã nguồn **Red Hat Enterprise Linux** và được xây dựng trên nhân Linux, được giới thiệu lần đầu tiên vào năm 2004. Đây là phần mềm ổn định với mức độ bảo mật cao và nhiều tùy chọn bảng điều khiển khác nhau.

CentOS được sử dụng rộng rãi trong các doanh nghiệp bởi sở hữu tính ổn định, bảo mật cao và nhiều tùy chọn bảng điều khiển của nó. Không chỉ vậy, CentOS được phát triển bởi một cộng đồng các lập trình viên chuyên nghiệp, góp phần nâng cấp bản phân phối Linux thông qua việc tạo nội dung wiki, hỗ trợ kỹ thuật và tìm các bản sửa lỗi.

Phần cấu hình cài đặt của CentOS 7.x tương thích với Red Hat Enterprise 7.x. CentOS 7 được ra mắt và ngày 7 tháng 7 năm 2014 và được hỗ trợ cho đến hết tháng 6 năm 2024.

**_Các bước cài đặt CentOS 7_**
**Bước 1:** Tải file iso của CentOS 7. Tải file iso CentOS 7.9 từ các link trong link tải dưới đây:
_http://isoredirect.centos.org/centos/7/isos/x86_64/_
**Bước 2: Đối với PC hoặc laptop:**
Sau khi tải file iso của CentOS 7.9, dùng phần mềm Rufus để burn file đó vào USB hoặc đĩa CD của bạn để có thể cài đặt. phần mềm Rufus chạy trên các hệ điều hành Window. Sau đó cắm USB hoặc đĩa CD của bạn vào máy cần cài và cài đặt
![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.png)
Sau đó, bạn ấn Start để burn file iso vào USB hoặc đĩa CD của bạn.

**Đối Với máy chủ ảo:**
Cài đặt hệ điều hành CentOS 7.9 trên máy ảo được tạo bởi công nghệ ảo hóa VMWARE trên Vmware vsphere hypervisor 7 (ESXi 7).
- Tạo 1 máy ảo và kèm tài nguyên bạn muốn trên máy chủ Vmware.
- Sau đó, Tải file iso cần cài đặt vào phần CD/DVD Drive 1.
![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.1-1024x275.png)
- Mở máy ảo VPS lên và cài đặt.
Sau khi xong các bước chuẩn bị, mở máy lên và bắt đầu cài đặt. Chọn Install CentOS 7.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.2.png)

Chọn ngôn ngữ mà bạn muốn cài đặt.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.3-1024x796.png)

Đây là màn hình mặc định cho những cấu hình cơ bản. Đầu tiên chọn Date & Time.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.4-1024x796.png)

Chọn khu vực bản muốn trên bản đồ hoặc bạn có thể chọn khu vực trong phần Region và chọn thành phố trong phần City. Sau đó chọn Done:

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.5-1024x796.png)

Chọn INSTALLATION DESTINATION để chọn phân vùng cài lên hệ điều hành. Bạn có thể chọn tự động tạo cá phân vùng trong phần “Automatically configure partitioning”.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.6-1024x710.png)

Hoặc tuỳ chọn trong phần “I will configure partitioning”. Bạn có thể tùy chọn định dạng của ổ cứng và dung lượng của từng phần vùng.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.7-1024x796.png)

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.8-1024x796.png)

Sau khi cài đặt xong bạn chọn “Done” rồi chọn “Accept Changes” để hoàn thành cài đặt:

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.9-1024x796.png)

Chọn phần “NETWORK & HOSTNAME” để cài đặt mạng cho máy. Chọn “Configure” để cấu hình card mạng:

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.10-1024x720.png)

Bạn có thể chọn DHCP là giao thức quản lý máy chủ tự động phân cấp IP hoặc Manual là để tự cấu hình IP cho máy. Sau khi cấu hình xong “Save” lại.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.11-1024x720.png)

Tiếp theo bật card mạng và chỉnh sửa tên của máy trong phần “Host name”. Sau đó, chọn “Done” để hoàn thành.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.12-1024x746.png)

Ấn chọn “Begin Installation” để bắt đầu cài đặt.

Trong phần “ROOT PASSWORD” để cài đặt mật khẩu cho máy. Phần “USER CREATION” để tạo thêm user mà bạn muốn. User mặc định của hệ điều hành là “root”.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.13-1024x746.png)

Sau đó chờ hệ điều hành được cài xong bạn chọn vào Reboot khởi động lại máy và vào hệ điều hành.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.14-1024x689.png)

Đây là giao diện của hệ điều hành centos bản “Minimal”.

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.1.15-1024x571.png)

Như vậy là bạn đã cài đặt xong hệ điều hành CentOS 7.

# 2.2.Cài đặt hệ điều hành Ubuntu 22.04 Live Server
Ubuntu 22.04 được ra mắt ngày 21 tháng 4 năm 2022 và được hỗ trợ đến hết tháng 4 năm 2027.

**_Các bước cài đặt:_**

- Tải file iso ubuntu 22.04 live server theo link: [Link](https://cdimage.ubuntu.com/releases/22.04/release/)
- Phần chuẩn bị file iso và USB boot cho máy PC và máy ảo đều giống với hệ điều hành CentOS.
- Sau khi bật máy và chọn “Try or Install Ubuntu Server” để bắt đầu cài đặt.
- Chọn ngôn ngữ và kiểu bàn phím bạn muốn. Click “Done” để tiếp tục.
- Chọn phiên bản Ubuntu Server mặc định. 
- Cấu hình card mạng có sẵn của máy, có thể theo 2 chế độ là DHCP hoặc Manual. Sau khi cấu hình xong chọn Done để tiếp tục.
- **_Chú ý:_** Trong cấu hình theo kiểu Manual (tĩnh) của Subnet, bạn cần gõ cả dải IP và subnet mask ( như hình dưới).

![Alt](https://lanit.com.vn/wp-content/uploads/2023/01/2.2.6-1024x186.png)

Sau đó tiếp tục chọn “Done” đến phần cấu hình phân vùng ổ cứng cài đặt hệ điều hành.

- Chọn ổ cứng bạn sẽ cài đặt hệ điều hành lên đó, có thể tuỳ chọn ở cứng là LVM group hoặc định dạng thường bằng cách sử dụng nút cách( Space) để chọn/bỏ chọn. Sau đó click “Done” để tiếp tục.
- Chọn “Done” và click chọn “Continue” để tiếp tục.
- Điền hostname, user và mật khẩu bạn muốn đặt cho máy. Sau đó chọn “Done”
- Tích chọn cài đặt “Install OpenSSH Server” để server cài thêm giao thức SSH bạn có thể truy cập từ 1 máy khác vào máy.
- Sau đó bạn tiếp tục chọn Done để tới phần tự động cài đặt hệ điều hành, hệ điều hành cài xong bạn chọn “REBOOT NOW”, khởi động lại máy và sử dụng hệ điều hành.
- Dưới đây là giao diện của hệ điều hành Ubuntu 22.04 live server: