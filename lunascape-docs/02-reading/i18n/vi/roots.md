# Chuyển đổi thư mục gốc tài liệu

Thư mục gốc tài liệu là thư mục cao nhất của một bộ tài liệu. INDEX, bộ lọc, kiểm tra và bản dịch đều hoạt động theo từng thư mục gốc tài liệu.

## Cách tìm thư mục gốc tài liệu

Lunascape Docs đi ngược lên các thư mục cha từ tệp Markdown đang mở và lấy thư mục gần nhất khớp với một trong các điều kiện sau làm thư mục gốc tài liệu.

- Thư mục có `lunascape-docs.json` (không phụ thuộc vào tên thư mục)
- Thư mục có tên `docs` (bạn có thể thêm tên khác bằng cài đặt `lunascapeDocEditor.rootDirectoryNames`)

Khi bạn chạy "Lunascape Docs: Mở trình xem bản đặc tả", thư mục gốc tài liệu trong cài đặt `lunascapeDocEditor.root` (mặc định là `docs`) sẽ được mở.

## Chuyển sang thư mục gốc tài liệu khác

Khi không gian làm việc có nhiều thư mục gốc tài liệu, tên thư mục gốc tài liệu ở ngoài cùng bên trái thanh công cụ sẽ trở thành một danh sách thả xuống.

1. Nhấn vào tên thư mục gốc tài liệu ở ngoài cùng bên trái thanh công cụ.
2. Chọn một thư mục gốc tài liệu trong danh sách.
   Trang bắt đầu của thư mục gốc tài liệu đã chọn sẽ hiển thị và INDEX được chuyển theo.

> **Gợi ý**
>
> Tên hiển thị trong danh sách được xác định theo thứ tự sau. Tên này không thay đổi khi bạn chuyển ngôn ngữ hiển thị.
>
> 1. `title` trong `lunascape-docs.json`
> 2. `navigation.title` của `README.md` ở thư mục gốc, nếu không có thì lấy H1 của tệp đó
> 3. `navigation.title` của `index.md` ở thư mục gốc, nếu không có thì lấy H1 của tệp đó
> 4. Tên thư mục (với thư mục `docs` tiêu chuẩn thì lấy tên thư mục cha của nó)

## Mở tệp Markdown không thuộc thư mục gốc tài liệu nào

Khi bạn mở một tệp Markdown không nằm trong thư mục gốc tài liệu, thư mục chứa tệp đó sẽ được hiển thị như một thư mục gốc tài liệu tạm thời. INDEX sẽ liệt kê các tệp Markdown trong thư mục đó và các thư mục con bên dưới.

- Nhấn [Lên thư mục trên] trên thanh công cụ để mở rộng phạm vi hiển thị đến thư mục cha trong không gian làm việc.
- Ở chế độ hiển thị này, bạn không dùng được cài đặt ngôn ngữ của dự án và dịch hàng loạt. Hãy đặt một tệp `lunascape-docs.json` vào thư mục đó để biến nó thành thư mục gốc tài liệu, khi đó các chức năng này sẽ dùng được.

## Luôn mở một thư mục gốc tài liệu cố định

Nếu bạn đặt cài đặt `lunascapeDocEditor.rootMode` thành `fixed`, thì dù bạn mở tệp Markdown nào, thư mục gốc tài liệu trong `lunascapeDocEditor.root` cũng luôn được mở.

## Chủ đề liên quan

- [Thư mục gốc tài liệu và quy ước tệp](../04-document-tools/structure.md)
- [Cấu hình dự án](../04-document-tools/project-configuration.md)
- [Danh sách cài đặt VS Code](../08-reference/settings.md)
