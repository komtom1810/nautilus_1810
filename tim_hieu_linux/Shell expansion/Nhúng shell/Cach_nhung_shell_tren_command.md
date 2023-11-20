# Cách nhúng shell command: ${} và ''
Khi muốn nhúng một lệnh shell vào trong biểu diễn ${...} và đồng thời sử dụng dấu ' ' để bảo vệ các ký tự đặc biệt và tránh việc thực hiện một số thao tác mà bạn muốn giữ nguyên trong chuỗi, có thể kết hợp cả hai.

Dưới đây là một số vd:

1. Gán Kết Quả của Lệnh vào Biến:

`current_date="${date}"`

`echo "Current date: ${current_date}"`

Trong vd này, lệnh `date`csẽ được thực hiện và kết quả sẽ được gán vào biến `current_date`, sử dụng cả `${...}` và dấu `''`.

2. Sử Dụng Kết Quả của Lệnh Trong Chuỗi:

`echo "Number of files in the current directory: $('ls' | wc -l)"`

Trong vd này, lệnh `ls` được bảo vệ bằng dấu `''`, giúp tránh việc thực hiện các thay đổi không mong muốn trong kết quả của nó.

3. Thực Hiện Phép Tính Bằng Kết Quả của Lệnh:

`result="$(( $('echo' '5 + 3') ))"`

`echo "The result is: ${result}"`

Lệnh `echo` được bảo vệ bằng dấu `''`, giữ nguyên chuỗi và tránh việc thực hiện phép tính trong nó.

4. Sử Dụng Biểu Diễn Chuỗi Trong Lệnh `sed`:

`input="Hello World"`

`output="$('echo' '${input}' | sed 's/Hello/Hi/')"`

`echo "Output: ${output}"`

Trong vd này, chuỗi `${input}` được bảo vệ bằng dấu `' '`, giúp tránh việc thực hiện các thay đổi không mong muốn trong chuỗi.

Lưu ý rằng việc sử dụng dấu `''` có thể hữu ích khi bạn muốn bảo vệ chuỗi chứa các ký tự đặc biệt và tránh việc chúng bị đánh giá trước khi sử dụng. Tuy nhiên, đôi khi bạn vẫn cần sử dụng `${...}` để đánh giá các biểu thức và biến bên trong chuỗi.





