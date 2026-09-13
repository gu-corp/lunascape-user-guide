# Tài liệu không hiển thị

## Hiển thị thông báo "Không tìm thấy Markdown hoặc thư mục docs có thể mở"

- Không gian làm việc không có thư mục `docs`, hoặc dùng tên khác với `docs`.
  - Đặt tệp `lunascape-docs.json` vào thư mục đó thì thư mục sẽ được nhận là thư mục gốc tài liệu, bất kể tên là gì.
  - Hoặc thêm tên thư mục vào cài đặt `lunascapeDocEditor.rootDirectoryNames`.
- Nếu chưa có tài liệu nào, hãy tạo bằng "Lunascape Docs: Tạo tài liệu từ mẫu".
- Cũng có cách mở tệp Markdown trong trình soạn thảo rồi chạy "Lunascape Docs: Mở trong trình xem bản đặc tả".

## Tài liệu không xuất hiện trong INDEX

- Kiểm tra phần mở rộng có phải là `.md`, `.markdown` hoặc `.mdx` không.
- Các thư mục sau không được hiển thị: thư mục bắt đầu bằng `.`, `node_modules`, và thư mục chỉ định trong `ignoredDirectories` (mặc định là `99-archive`).
- Bản dịch nằm dưới `i18n/` không hiển thị riêng trong INDEX. Hãy chuyển sang chúng từ trình đơn ngôn ngữ.
- Khi tệp vừa thêm không hiển thị, hãy nhấn [Tải lại].
- Có thể bạn đang xem một thư mục gốc tài liệu khác. Hãy kiểm tra tên thư mục gốc tài liệu ở ngoài cùng bên trái thanh công cụ.

## Nhấn vào thư mục nhưng không hiển thị gì

Tệp `README.md` của thư mục đó là "bộ mô tả chỉ dùng để cấu hình", chỉ có front matter mà không có phần nội dung. Hãy mở thư mục trong INDEX và chọn một tài liệu bên trong.

## Mở nhầm thư mục gốc tài liệu

- Khi cài đặt `lunascapeDocEditor.rootMode` là `fixed`, `lunascapeDocEditor.root` luôn được mở.
- Với `auto`, thư mục gốc tài liệu gần nhất với tệp Markdown đang mở sẽ được chọn. Bạn có thể chuyển bằng danh sách thả xuống ở ngoài cùng bên trái thanh công cụ.

## Tên thư mục gốc tài liệu khác với mong đợi

Tên được quyết định theo thứ tự: `title` trong `lunascape-docs.json` → `navigation.title` của `README.md` ở gốc → H1 của tệp đó → `index.md` → tên thư mục. Nếu muốn cố định, hãy đặt `title`.

## INDEX biến mất

- Ở thư mục gốc tài liệu chỉ có 1 tài liệu, INDEX tự động đóng trong lần đầu. Bạn có thể mở lại bằng biểu tượng hiển thị cột trên thanh công cụ. Có thể tắt bằng [Tự động ẩn khi chỉ có một tài liệu] trong [Cài đặt hiển thị].
- Khi màn hình hẹp, hãy mở bằng [Mở INDEX] (ba vạch ngang) ở bên trái [Quay lại].

## Nhấn vào liên kết nhưng không mở

- "Không tìm thấy đích của liên kết": tệp đích không tồn tại. Bạn có thể kiểm tra liên kết nội bộ bằng [Kiểm tra] trong Công cụ tài liệu.
- "Đã không mở liên kết không an toàn hoặc không được hỗ trợ": không mở các liên kết nằm ngoài thư mục gốc tài liệu, hoặc dùng lược đồ khác `https://` và `mailto:`.

## Ngôn ngữ hiển thị khác với mong muốn

- Hãy kiểm tra ngôn ngữ của trang đang xem và căn cứ xác định ngôn ngữ đó trong trình đơn ngôn ngữ.
- Ngôn ngữ hiển thị đã chọn lần trước được ghi nhớ. Hãy chọn lại ngôn ngữ mặc định trong trình đơn ngôn ngữ.
- Khi cài đặt cá nhân `lunascapeDocEditor.locale` được thiết lập, bản dịch của ngôn ngữ đó sẽ được ưu tiên.

## Liên quan

- [Chuyển thư mục gốc tài liệu](../02-reading/roots.md)
- [Thư mục gốc tài liệu và quy ước tệp](../04-document-tools/structure.md)
