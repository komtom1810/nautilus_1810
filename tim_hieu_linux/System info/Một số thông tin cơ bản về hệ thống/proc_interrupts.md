# /proc/interrupts
Tệp `/proc/interrupts` trong hệ thống tệp Linux chứa thông tin về số lượng ngắt (interrupts) được sinh ra bởi các thiết bị phần cứng trên hệ thống. Đây là một tệp tin ảo được tạo ra động khi bạn đọc nó, cung cấp cái nhìn tổng quan về tình trạng interrupt của hệ thống tại thời điểm đó.

Có thể xem nội dung của tệp `/proc/interrupts` bằng các lệnh như `cat`, `more`, hoặc `less`. VD:

`cat /proc/interrupts`

Kết quả như sau:

![](https://forum.openwrt.org/uploads/default/original/2X/4/4a0d30cfc4caf170c9e5dd975c8ba059d2043245.png)

- Các cột trong kết quả thường thể hiện thông tin như sau:

+ **CPU0, CPU1, ...:** Các cột này thể hiện số lượng interrupts được xử lý bởi từng CPU.
+ **IRQ (Interrupt Request):** Số và loại interrupt.
+ **Edge/Level:** Kiểu kích thích (edge hoặc level).
+ **Device:** Tên thiết bị gây ra interrupt.
Thông tin này có thể hữu ích để theo dõi và đánh giá tình trạng hoạt động của các thiết bị phần cứng và xác định xem có sự cạnh tranh nào không.