# Sử dụng từ AI

Tiện ích mở rộng đăng ký Language Model Tool chỉ đọc `lunascape_getDocsSpecification` với VS Code. Khi được hỏi về các tính năng, cài đặt hoặc quy ước tài liệu của Lunascape Docs, tác nhân VS Code tương thích có thể dùng công cụ này để lấy nội dung của phần trợ giúp này (bản đặc tả chung).

## Cách dùng

Trong khung trò chuyện của VS Code, hãy đặt câu hỏi kèm `#lunascapeDocs`, hoặc hỏi về cài đặt và cấu trúc tài liệu của Lunascape Docs.

```text
#lunascapeDocs Làm thế nào để bật bản dịch tiếng Anh trong lunascape-docs.json?
```

## Tham số của công cụ

| Tham số | Nội dung |
|---|---|
| `topic` | Chương cần lấy. `all`, `usage` (thao tác cơ bản), `structure` (thư mục gốc tài liệu và quy ước tệp), `editing` (chỉnh sửa tài liệu), `configuration` (cài đặt dự án), `security` (bảo mật và ranh giới ghi), `ai` (sử dụng từ AI) |
| `locale` | Ngôn ngữ của phần trợ giúp (thẻ ngôn ngữ của phần trợ giúp đi kèm, ví dụ `ja`, `en`). Nếu bỏ qua, công cụ dùng ngôn ngữ hiển thị của VS Code; nếu không có thì trả về phần trợ giúp tiếng Nhật |

> **Lưu ý**
>
> - Công cụ không gửi nội dung tài liệu ra bên ngoài.
> - Công cụ không trả về tên không gian làm việc hay đường dẫn cục bộ.
> - Công cụ không thay đổi tệp.
> - Ngay cả khi không có `AGENTS.md`, bạn vẫn dùng được từ các tác nhân VS Code tương thích. Công cụ không tự động được chia sẻ với các ứng dụng AI khác không dùng API công cụ của tiện ích mở rộng.

## Xem thêm

- [Hiển thị trợ giúp](../02-reading/help.md)
- [Bảo mật và ranh giới ghi](security.md)
