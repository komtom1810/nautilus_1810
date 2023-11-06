# Các chế độ hoạt động của VMware Network
# 1/Bridged
Cơ chế hoạt động của Bridged mode được mô tả như sau:
- Ở chế độ này, card mạng trên máy ảo được gắn vào VMnet0, VMnet0 này liên kết trực tiếp với card mạng vật lý trên máy thật, máy ảo lúc này sẽ kết nối internet thông qua  card mạng vật lý và có chung lớp mạng với card mạng vật lý.

![bridged](https://public.bn.files.1drv.com/y4pFlTUeJ_cAeQ3V8dLWymc0fohq2W-EwqIVcZ8ZdkU1yckAPNNiSnG9I3yduZGscDz0KLcI8XdZQCx2HvyjBnPYntfIbpX-eChU9B92yjE5_C5bTSvzl68N5mgGz7tsbEMIitTXOwGcAtfNK7MbRXycYJ3vfc1Tyjb5QNbHq1tRJhHksZyshuk3n6MdW1pI87k/briged.png?psid=1&rdrts=373837233)

- Card Bridge trên máy ảo chỉ có thể giao tiếp với card mạng thật trên máy thật.
- Card mạng Bridge này có thể giao tiếp với mạng vật lý mà máy tính thật đang kết nối.

# 2/Host-only
Cơ chế hoạt động của Host-only mode được mô tả như sau:
- Máy ảo được kết nối với VMnet có tính năng Host-only, trong trường hợp này là VMnet1 . VNnet Host-only kết nối với  một card mạng ảo tương ứng ngoài máy thật (như đã nói ở phần trên). Ở chế độ này,  các máy ảo không có kết nối vào mạng vật lý bên ngoài hay internet thông qua máy thật , có nghĩa là mạng VMnet Host-only và mạng vật lý hoàn toàn tách biệt. IP của máy ảo được cấp bởi DHCP của VMnet tương ứng. Trong nhiều trường hợp đặc biệt cần cấu hình riêng, ta có thể tắt DHCP trên VMnet và cấu hình IP bằng tay cho máy ảo.

![Host-only](https://public.sn2.livefilestore.com/y2pP5x5S-hctvRaGYnS19WRmpkhDnqGeWbKsqJrxMmcJgj4nplOWuXgZ6VmlYVVQJhr2O771zgIP0tH7WHIbdaCaAZKF_ms1PqKptl3ioj-COI/host-only.png?psid=1)

- Card Host-only chỉ có thể giao tiếp với card mạng ảo VMnet1 trên máy thật.
- Card Host-only chỉ có thể giao tiếp với các card Host-only trên các máy ảo khác.
- Card Host-only không thể giao tiếp với mạng vật lý mà máy tính thật đang kết nối.

# 3/NAT(Network Address Translation)
Cơ chế hoạt động của NAT mode được mô tả như sau:
- Ở chế độ này, card mạng của máy ảo kết nối với VMnet8, VNnet8 cho phép máy ảo đi ra mạng vật lý bên ngoài internet thông qua cơ chế NAT (NAT device). Lúc này lớp mạng bên trong máy ảo khác hoàn toàn với lớp mạng của card vật lý bên ngoài, hai mạng hoàn toàn tách biệt. IP của card mạng máy ảo sẽ được cấp bởi DHCP của VMnet8, trong trường hợp bạn muốn thiết lập IP tĩnh cho card mạng máy ảo bạn phải đảm bảo chung lớp mạng với VNnet8 thì máy ảo mới có thể đi internet.

![NAT](https://public.sn2.livefilestore.com/y2pvoXPJXGiHRiv4zknu2S7UJjcxNmiQXMNkFNlkZcSIgqKXV6631h6n3sBnQ6BTue9rr4PvO2Leemq816L5Hk_oUjUhvYzxwsoTCJ9S-3FByk/NAT.png?psid=1)
 
- Card NAT chỉ có thể giao tiếp với card mạng ảo VMnet8 trên máy thật.
- Card NAT chỉ có thể giao tiếp với các card NAT trên các máy ảo khác.
- Card NAT không thể giao tiếp với mạng vật lý mà máy tính thật đang kết nối. Tuy nhiên nhờ cơ chế NAT được tích hợp trong VMWare, máy tính ảo có thể gián tiếp liên lạc với mạng vật lý bên ngoài.


