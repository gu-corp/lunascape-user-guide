# Tạo và sắp xếp tài liệu, thư mục

Từ trình đơn mục trong INDEX, bạn có thể tạo, nhân bản, đổi tên và xóa tài liệu cũng như thư mục. Việc nhập liệu diễn ra trong một hộp thoại nhỏ ngay trong trình xem, không làm gián đoạn việc đọc.

> **Lưu ý**
>
> Các thao tác này chỉ dùng được khi không gian làm việc được tin cậy trong VS Code. Chúng không thể chạy khi đang chỉnh sửa tài liệu, khi một thao tác khác đang được xử lý, hoặc khi đối tượng có thay đổi chưa lưu.

## Tạo tài liệu hoặc thư mục

1. Mở trình đơn mục ([⋯] hoặc nhấp chuột phải) của thư mục đích.
   Để tạo ngay dưới thư mục gốc tài liệu, hãy dùng [⋯] ở cuối bên phải tiêu đề INDEX hoặc nhấp chuột phải vào vùng trống của INDEX.
2. Chọn [Tài liệu mới] hoặc [Thư mục mới].
3. Nhập tên rồi nhấn [Tạo].
   Tên tài liệu cần có phần mở rộng Markdown (`.md`, `.markdown`, `.mdx`, v.v.).

Tài liệu mới được tạo dưới dạng tài liệu ngôn ngữ mặc định (bản gốc).

## Nhân bản tài liệu

1. Mở trình đơn mục của tài liệu rồi chọn [Nhân bản].
2. Nhập tên mới rồi nhấn [Tạo].

Chỉ bản gốc được nhân bản. Các bản dịch không được nhân bản.

## Đổi tiêu đề

Thay đổi tiêu đề (H1) của tài liệu. Tên tệp không thay đổi.

1. Mở trình đơn mục của tài liệu hoặc thư mục rồi chọn [Đổi tiêu đề].
2. Nhập tiêu đề mới trên một dòng rồi nhấn [Thay đổi].

Với thư mục, tiêu đề trong `README.md` của thư mục đó sẽ được thay đổi. Khi ngôn ngữ đang hiển thị là một bản dịch, tiêu đề của tài liệu thuộc ngôn ngữ đó sẽ thay đổi.

## Đổi tên tài liệu

Thay đổi tên tài liệu hiển thị trên thanh công cụ (tên của thư mục gốc tài liệu).

1. Nhấp chuột phải vào tên tài liệu trên thanh công cụ. Bạn cũng có thể mở trình đơn này từ [⋯] ở cuối bên phải tiêu đề INDEX.
2. Chọn [Đổi tên tài liệu] rồi nhập tên mới.

Khi chưa thiết lập, tên thư mục được hiển thị nguyên như vậy.

Tên bạn đặt được ghi vào **nơi hiện đang cung cấp tên tài liệu**. Tên sẽ không được ghi vào nơi không dùng để hiển thị, để tiêu đề bạn nhìn thấy không bị bỏ qua.

| Trạng thái hiện tại | Nơi ghi |
|---|---|
| `lunascape-docs.json` có tên | Cập nhật `lunascape-docs.json` |
| Không có tên, nhưng thư mục gốc tài liệu có README | Viết lại tiêu đề (H1) của README |
| Không có cả hai | Tạo `lunascape-docs.json` và lưu tên vào đó |

Thông báo hiện ra sau khi thay đổi cho biết nơi nào đã được ghi.

> **Mẹo**
>
> Tên tài liệu được xác định theo thứ tự: tên trong `lunascape-docs.json` → tiêu đề README của thư mục gốc tài liệu → tên thư mục.

## Đổi tên tệp hoặc thư mục

1. Mở trình đơn mục rồi chọn [Đổi tên tệp] hoặc [Đổi tên thư mục].
2. Nhập tên mới rồi nhấn [Thay đổi].

Các bản dịch tương ứng (cùng đường dẫn dưới `i18n/<ngôn ngữ>/`) cũng được đổi tên cùng lúc.

## Xóa

1. Mở trình đơn mục rồi chọn [Chuyển vào thùng rác].
2. Kiểm tra nội dung thông báo xác nhận rồi chấp nhận việc di chuyển.

Đối tượng được chuyển vào thùng rác của hệ điều hành nên có thể khôi phục nếu cần. Các bản dịch không bị xóa và vẫn được giữ nguyên.

## Những tên không dùng được

- Tên bắt đầu bằng `.` (vì sẽ không hiển thị trong INDEX)
- `i18n` (dành riêng cho tệp bản dịch)
- Tên được Windows dành riêng (`CON`, `PRN`, v.v.)
- Tên kết thúc bằng dấu chấm hoặc khoảng trắng
- Ký tự điều khiển hoặc ký tự không dùng được trong tên tệp
- Tên đã có sẵn trong cùng thư mục (kể cả tên chỉ khác nhau về chữ hoa chữ thường)

> **Lưu ý**
>
> Không thể đổi tên hoặc di chuyển trang bắt đầu (thường là `README.md` ở thư mục gốc). Hãy thay đổi `startPage` trong `lunascape-docs.json` trước.

## Chủ đề liên quan

- [Thay đổi thứ tự tài liệu](reorder.md)
- [Sử dụng INDEX](../02-reading/index-panel.md)
