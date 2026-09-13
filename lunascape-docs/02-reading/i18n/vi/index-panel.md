# Sử dụng INDEX

INDEX ở bên trái màn hình là cây thư mục và tài liệu nằm trong thư mục gốc tài liệu.

## Lọc

1. Nhập một từ vào ô [Lọc tài liệu] phía trên INDEX.
2. Chỉ những mục có tên tài liệu khớp mới được hiển thị. Xóa nội dung đã nhập để trở lại như cũ.

> **Lưu ý**
>
> Trong khi đang lọc, bạn không thể sắp xếp lại bằng cách kéo và thả.

## Mở và đóng thư mục

- Nhấn vào mũi tên bên trái tên thư mục, hoặc nhấn vào tên của thư mục không có trang bìa, để mở hoặc đóng thư mục đó.
- Với thư mục có trang bìa (tệp `README.md` hoặc `index.md` có nội dung), nhấn vào tên sẽ mở trang bìa. Nếu chỉ muốn mở hoặc đóng, hãy dùng [Mở thư mục] / [Đóng thư mục] trong menu của mục.
- Trạng thái mở hay đóng của thư mục được ghi nhớ riêng cho từng người dùng và không được ghi vào các tệp do Git quản lý.

## README và trang bìa của thư mục

`README.md` là tệp mô tả nội dung của thư mục đó.

- Với thư mục có README, nhấn vào tên thư mục sẽ hiển thị README đó.
- Với thư mục không có README, tài liệu nằm trên cùng bên trong sẽ được hiển thị.
- Tiêu đề (H1) của README trở thành tên của thư mục đó trong INDEX.

README không bắt buộc phải có. Để thêm sau, hãy chọn [Tạo README] trong menu của thư mục (chỉ hiển thị với thư mục chưa có README).

## Hiện hoặc ẩn INDEX

- Dùng biểu tượng bên trái trong phần hiển thị cột trên thanh công cụ để hiện hoặc ẩn INDEX. Biểu tượng bên phải dùng để hiện hoặc ẩn "Trên trang này".
- Khi màn hình hẹp, INDEX bắt đầu ở trạng thái đóng. Nhấn [Mở INDEX] (ba vạch ngang) hiển thị bên trái [Quay lại] thì INDEX sẽ mở ra và phủ lên nội dung. INDEX đóng lại khi bạn nhấn [×] bên trong INDEX, nhấn vào nền, nhấn `Esc`, hoặc chuyển sang tài liệu khác. Trạng thái mở tạm thời này không làm thay đổi cài đặt của màn hình rộng.
- Ở thư mục gốc tài liệu chỉ có một tài liệu được hiển thị, INDEX tự động đóng lại trong lần đầu tiên. Bạn có thể mở lại bằng biểu tượng hiển thị cột. Có thể tắt hành vi này bằng [Tự động ẩn khi chỉ có một tài liệu] trong [Cài đặt hiển thị].

## Sử dụng menu của mục

Nhấn [⋯] hiện ra khi bạn rê chuột lên một mục trong INDEX, hoặc nhấn chuột phải vào mục đó, để mở menu của mục. Các mục được sắp xếp theo thứ tự sau.

| Nhóm | Mục |
|---|---|
| Thao tác thường dùng | [Mở thư mục] / [Đóng thư mục], [Mở INDEX] (mở trang bìa của thư mục), [Chỉnh sửa], [Đổi tiêu đề], [Mở trong VS Code], [Sao chép đường dẫn] |
| Tạo và sắp xếp | [Tạo README] (chỉ với thư mục chưa có README), [Tài liệu mới], [Thư mục mới], [Nhân bản], [Đổi tên tệp] / [Đổi tên thư mục], [Di chuyển lên một bậc], [Di chuyển xuống một bậc] |
| Xóa | [Chuyển vào thùng rác] |

- Để tạo ngay dưới thư mục gốc tài liệu, hãy nhấn [⋯] ở cuối bên phải tiêu đề của INDEX, hoặc nhấn chuột phải vào phần trống của INDEX, rồi chọn [Tài liệu mới] hoặc [Thư mục mới]. Cùng menu đó còn có [Đổi tên tài liệu], và nếu thư mục gốc tài liệu chưa có README thì có thêm [Tạo README]. Nhấn chuột phải vào tên tài liệu hiển thị trên thanh công cụ cũng mở ra menu này.
- Trong menu, dùng `↑` `↓` để di chuyển và `Home` `End` để nhảy tới mục đầu và mục cuối. Khi đóng bằng `Esc`, tiêu điểm trở về vị trí trước khi mở menu.

> **Lưu ý**
>
> Các mục tạo, sắp xếp và xóa chỉ hiển thị khi không gian làm việc được tin cậy trong VS Code. Chúng cũng không dùng được trong khi đang chỉnh sửa tài liệu hoặc khi một thao tác INDEX khác đang được xử lý.

## Thay đổi cách hiển thị

Từ [Cài đặt hiển thị], bạn có thể thay đổi việc hiển thị tên tệp, biểu tượng tài liệu và thư mục, số lượng mục trong thư mục, đường kẻ phân cấp và mật độ hiển thị. Xem chi tiết tại [Thay đổi cài đặt hiển thị](display-settings.md).

## Xem thêm

- [Tạo và sắp xếp tài liệu và thư mục](../03-editing/organize.md)
- [Thay đổi thứ tự tài liệu](../03-editing/reorder.md)
