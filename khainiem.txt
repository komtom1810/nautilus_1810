# Khái niệm Repository 
- Repository được hiểu là một kho lưu trữ nơi chứa các files của dự án. Các file đó có thể là code, hình ảnh, âm thanh hoặc mọi thứ liên quan đến dự án. Bạn có thể tổ chức kho lưu trữ của mình dưới nhiều hình thức khác nhau, hai loại kho lưu trữ trong Github là Local Repository và Remote Repository
  + Local Repository: là một lại repository nằm trên máy tính của bạn, repository này có nhiêm vụ đồng bộ hóa với remote repository bằng các lệnh của git.
  + Remote Repository: là một loại repository được cài đặt trên server chuyên dụng. Ví dụ như: GitHub, GitLab, Bitbucket,…
- Repository public: kho lưu trữ công khai có thể được truy cập bởi mọi người
- Repository private kho lưu trữ riêng tư chỉ có thể được truy cập bởi bạn và những người cho phép 

# Khái niệm Branch
- Branch được dùng để phân nhánh và ghi luồng của lịch sử. Bạn có thể dùng Branch để triển khai dự án theo hướng cô lập để không ảnh hưởng đến dự án chính. Tại đây cho phép bạn thử nghiệm các tính năng mới hoặc điều chỉnh, sửa lỗi project.
- Khi khởi tạo kho lưu trữ hoặc Clone, các thành viên sẽ được tạo lập một branch dùng riêng cho công việc của mình từ branch chính để không làm ảnh hưởng đến công việc của những thành viên khác. Branch riêng này sẽ chứa toàn bộ mã nguồn trong kho.
- Sau khi công việc đã hoàn thành, có thể nhập branch vừa tạo vào những branch khác khoặc repository chính bằng cách dùng lệnh Pull Request.

# Khái niệm Pull Request
Pull Request là lệnh được dùng để thông báo với mọi người rằng bạn đã đẩy những thay đổi của Branch lên Repository tổng . Khi đó, các thành viên khác có thể chấp nhận hoặc từ chối Request này. Khi lệnh này được mở, bạn và các thành viên có thể xem lại công việc và thảo luận với nhau.

# Khái niệm Fork
- Khái niệm này được hiểu là hành động tạo một dự án mới dựa trên dự án đã có sẵn. Cho phép bạn sao chép hoàn toàn một repository cũ, sau đó thay đổi hoặc chỉnh sửa một vài thứ cần thiết và lưu phiên bản mới này dưới dạng một repository độc lập hoàn toàn mới và gọi nó là dự án của riêng mình.

- Đây là tính năng giúp đẩy nhanh tiến độ của dự án. Vì là một dự án mới nên repository cũ không ảnh hưởng. Khi repository tổng được cập nhật, bạn cũng có thể áp dụng các cập nhật đó lên bản fork của bạn.

# Khái niệm Clone 
- Với tính năng gần giống như Fork, Clone cho phép tạo ra bản sao dữ liệu hoàn chỉnh của kho đang được lưu chứa trên máy chủ và tất cả lịch sử trên kho. Với Clone, có thể phục hồi bất kỳ bước nào dù đã commit. Đặc biệt, dù ổ cứng máy chủ có bị hư hỏng và không sử dụng được, vẫn có thể sử dụng Clone của máy khách bất kỳ để khôi phục lại dữ liệu máy chủ.

# Khái niệm Issue
- Github issue để theo dõi tasks và bugs

# Khái niệm commit
- Commit nghĩa là một action để Git lưu lại một snapshot của các sự thay đổi trong thư mục làm việc. Và các tập tin, thư mục được thay đổi đã phải nằm trong Staging Area. Mỗi lần commit nó sẽ được lưu lại lịch sử chỉnh sửa của code kèm theo tên và địa chỉ email của người commit. Ngoài ra trong Git bạn cũng có thể khôi phục lại tập tin trong lịch sử commit của nó để chia cho một branch khác, vì vậy bạn sẽ dễ dàng khôi phục lại các thay đổi trước đó.