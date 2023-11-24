# Điều hướng input, output, error 
Trong hệ điều hành Unix/Linux, bạn có thể thực hiện điều hướng (redirect) đầu vào, đầu ra và đầu ra lỗi của các tiến trình bằng cách sử dụng các toán tử redirection.

Dưới đây là một số cách thường sử dụng:

## 1. Điều Hướng Đầu Ra (stdout):
- `>`: Ghi đè nội dung vào một tệp. Nếu tệp không tồn tại, nó sẽ được tạo mới.

`command > output.txt`

- `>>`: Ghi thêm nội dung vào cuối một tệp mà không ghi đè lên nội dung đã có.

`command >> output.txt`

## 2. Điều Hướng Đầu Vào (stdin):
- `<`: Đọc nội dung từ một tệp và sử dụng làm đầu vào cho lệnh.

`command < input.txt`

## 3. Điều Hướng Đầu Ra Lỗi (stderr):
- `2>`: Ghi đè nội dung lỗi vào một tệp.

`command 2> error.txt`

- `2>>`: Ghi thêm nội dung lỗi vào cuối một tệp mà không ghi đè lên nội dung đã có.

`command 2>> error.txt`

- `&>` hoặc `>&2`: Ghi cả đầu ra và đầu ra lỗi vào một tệp.

`command &> output_and_error.txt`

- `|&`: Chuyển hướng cả stdout và stderr sang một tiến trình khác thông qua pipe.

`command 2>&1 | another_command`

## 4. Sử Dụng /dev/null:
- `/dev/null`: Là một thiết bị đặc biệt trong Unix/Linux không lưu trữ dữ liệu, nó có thể được sử dụng để loại bỏ đầu ra hoặc đầu ra lỗi mà không lưu lại chúng.

`command > /dev/null`    # Loại bỏ stdout

`command 2> /dev/null`   # Loại bỏ stderr

Những toán tử redirection giúp bạn kiểm soát nơi đầu vào và đầu ra của các lệnh, làm cho quá trình quản lý dữ liệu và thông tin trở nên linh hoạt và mạnh mẽ.