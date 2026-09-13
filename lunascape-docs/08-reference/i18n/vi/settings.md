# Danh sách cài đặt VS Code

Tìm "Lunascape Docs" trong phần cài đặt của VS Code (`⌘,` / `Ctrl+,`) để thay đổi các mục sau. Tất cả đều là cài đặt riêng của từng người dùng và không được lưu vào tài liệu của dự án.

## Thư mục gốc tài liệu

| Cài đặt | Giá trị | Mặc định | Chức năng |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` tự động chọn thư mục gốc tài liệu gần nhất với tệp Markdown đang mở; nếu tệp không thuộc thư mục gốc nào thì mở tạm thời thư mục cha. `fixed` luôn mở thư mục gốc tài liệu được chỉ định ở `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Mảng chuỗi | `["docs"]` | Tên các thư mục được tự động phát hiện là thư mục gốc tài liệu ở chế độ `auto`. Thư mục có `lunascape-docs.json` luôn được phát hiện, bất kể tên gọi. Nếu `lunascape-docs.json` ngay dưới kho lưu trữ có `defaultFolder` hoặc `roots` thì các giá trị đó được ưu tiên |
| `lunascapeDocEditor.root` | Đường dẫn | `docs` | Thư mục gốc tài liệu tương đối với không gian làm việc, dùng cho chế độ `fixed` hoặc khi mở bằng lệnh |
| `lunascapeDocEditor.startPage` | Đường dẫn | `README.md` | Trang bắt đầu, tính tương đối với thư mục gốc tài liệu |
| `lunascapeDocEditor.title` | Chuỗi | `Lunascape Docs` | Ghi đè tiêu đề của thẻ tài liệu. Cài đặt này không ảnh hưởng đến tên hiển thị khi chọn thư mục gốc tài liệu |
| `lunascapeDocEditor.ignoredDirectories` | Mảng chuỗi | `["99-archive"]` | Tên các thư mục bị loại khỏi INDEX |

## Hiển thị

| Cài đặt | Giá trị | Mặc định | Chức năng |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` dùng nền trắng, `auto` theo bảng màu của VS Code |
| `lunascapeDocEditor.locale` | Thẻ ngôn ngữ | Không có | Ngôn ngữ tài liệu riêng của bạn, được ưu tiên hiển thị khi có sẵn. Cài đặt này không thay đổi ngôn ngữ bản gốc của dự án |
| `lunascapeDocEditor.documentMetadata.compact` | Giá trị luận lý | `true` | Thu gọn bảng quản lý tài liệu ngay sau H1 thành một dòng "Thông tin tài liệu" |
| `lunascapeDocEditor.tree.showFileNames` | Giá trị luận lý | `false` | Hiển thị tên tệp thay cho tên tài liệu trong INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Giá trị luận lý | `false` | Hiển thị biểu tượng tài liệu trong INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Giá trị luận lý | `false` | Hiển thị biểu tượng thư mục trong INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Giá trị luận lý | `false` | Hiển thị số mục nằm ngay dưới mỗi thư mục trong INDEX |
| `lunascapeDocEditor.tree.showGuides` | Giá trị luận lý | `true` | Hiển thị đường dẫn hướng phân cấp trong INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Khoảng cách dòng của INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Giá trị luận lý | `true` | Đóng INDEX một lần đầu tiên khi chỉ có một tài liệu |

## Chỉnh sửa

| Cài đặt | Giá trị | Mặc định | Chức năng |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Chế độ hiển thị khi chỉnh sửa lúc bạn chưa chuyển đổi. Chế độ hiển thị dùng lần cuối được ưu tiên hơn |
| `lunascapeDocEditor.editor.showEditButton` | Giá trị luận lý | `true` | Hiển thị [Chỉnh sửa] ở góc dưới bên phải của nội dung |

## Sơ đồ

| Cài đặt | Giá trị | Mặc định | Chức năng |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Môi trường chạy để vẽ TikZ. `bundled` dùng môi trường chạy đã được phê duyệt đi kèm (không có trong bản phân phối hiện tại), `workspace` dùng `node-tikzjax` 1.0.5 nằm ngay dưới không gian làm việc đáng tin cậy (chỉ dành cho phát triển và đánh giá), `disabled` không vẽ |

## Cài đặt không còn được khuyến nghị

| Cài đặt | Dùng thay thế |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` trong `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` trong `lunascape-docs.json` |

Cài đặt riêng của người dùng không thể ghi đè ngôn ngữ của dự án.

## Chủ đề liên quan

- [Thay đổi cài đặt hiển thị](../02-reading/display-settings.md)
- [Cấu hình dự án](../04-document-tools/project-configuration.md)
