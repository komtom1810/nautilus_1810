# Các biến $HISTFILE, $HISTSIZE, $HISTFILESIZE
Trong môi trường Linux, có một số biến liên quan đến lịch sử lệnh trong shell. Dưới đây là một số biến thường được sử dụng:

1. `$HISTFILE`

Biến này xác định tên của tệp chứa lịch sử lệnh. Mặc định thường là `~/.bash_history`.

2. `$HISTSIZE`

Biến này xác định số lượng lệnh được giữ trong lịch sử. Nếu bạn đặt `$HISTSIZE` thành một giá trị cụ thể, chỉ số lệnh trong lịch sử sẽ được giữ không vượt quá giá trị này.

`HISTSIZE=100`

3. `$HISTFILESIZE`

Biến này giới hạn số lượng lệnh được lưu trong tệp lịch sử (`$HISTFILE`). Khi số lệnh vượt quá giá trị của `$HISTFILESIZE`, các lệnh cũ sẽ bị xóa.

`HISTFILESIZE=200`

