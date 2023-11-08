# Các cú pháp trong Markdown
# 1/Heading
- Với kiểu Setext: ta sử dụng ký tự = và - gạch chân dưới tiêu đề, sử dụng cho 2 thẻ h1và h2.
- Với kiểu AXT sử dụng ký tự # để biểu diễn các thẻ tiêu đề từ h1 tới h6.
Bạn cũng có thể sử dụng 1 thẻ đóng #
VD: # Heading 1
    # Heading 1 #

# 2/Character styles 
- Tạo chữ in đậm **example** 
- Tạo chữ in nghiêng _example_
- Tạo chữ in đậm và in nghiêng **_example_**
- Tạo chữ trong hộp `example`
- Tạo chữ gạch ngang ~~example~~
- Tạo văn bản trích dẫn > example

# 3/Lists
Để dánh dấu 1 danh sách không có thứ tự (unorder list) chúng ta sử dụng dấu - hoặc + hoặc ***** trước mỗi dòng. Để đánh dấu một danh sách có thứ tự bạn sử dụng các số thay vì các dấu như ở trên.

- Text1
- Text2

1. Text1
2. Text2

# 4/Links
- Markdown hỗ trợ 2 kiểu chèn liên kết là: inline và refences.
- Để tạo một liên kết nội tuyến, sử dụng một tập hợp các dấu ngoặc đơn ngay sau ngoặc vuông. Bên trong ngoặc đặt URL mà bạn muốn liên kết, cùng với một tiêu đề tùy chọn cho liên kết, bao bọc trong dấu ngoặc kép.
VD:
Markdown [Link](http://example.com)
Markdown [Link](../link)

Link1[Link1](1) Link2[Link2](2)
[1]: http://example1.com
[2]: http://example2.com

# 5/Images
- Hình ảnh trong Markdown tương tự như liên kết. Sự khác biệt là:

  + Các dấu ngoặc vuông phải được bắt đầu bằng một dấu chấm than
  + Và bên trong chúng có thể có một số văn bản thay thế. Mô tả về hình ảnh, nó sẽ được hiển thị nếu hình ảnh bị lỗi.
VD: Picture: ![Alt](https://i.imgur.com/Ayrum1k.jpeg)

# 6/Table 

| Number | Next number | Previous number |
| :----- | :---------- | :-------------- |
| Five   | Six         | Four            |
| Ten    | Eleven      | Nine            |
| Seven  | Eight       | Six             |
| Two    | Three       | One             |


# 7/Code và Block

Có 2 loại code có thể viết trong markdown: inline code (code trong dòng) và code block (đoạn code riêng). sử dụng lần lượt 1 ký tự và 3 ký tự `