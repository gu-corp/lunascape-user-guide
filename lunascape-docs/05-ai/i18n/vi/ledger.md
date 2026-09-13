# Bảng theo dõi và bản ghi

Bảng theo dõi ở phần trên của tab [AI] cho biết tình trạng bản dịch của từng ngôn ngữ được hỗ trợ. Ngay cả khi không dùng AI, bạn vẫn có thể xem những gì còn thiếu.

| Hiển thị | Ý nghĩa |
|---|---|
| Chưa dịch | Số tài liệu chưa có bản dịch |
| Cần cập nhật | Số tài liệu đã có bản dịch nhưng bản gốc mới hơn thời điểm được ghi lại |
| Đã dịch | Số bản dịch bám theo bản gốc |

Bảng theo dõi được tính bằng cách quét thư mục gốc tài liệu. Không có AI và không có mô hình ngôn ngữ nào tham gia.

## Cập nhật bản ghi bản dịch

Để xác định trạng thái “Cần cập nhật”, cần ghi lại bản gốc và bản dịch tại thời điểm dịch. AI kiểu phiên làm việc ghi thẳng vào tệp nên bản ghi không được tạo tự động.

1. Khi dịch xong và đã kiểm tra nội dung, hãy nhấn [Cập nhật bản ghi bản dịch].
2. Các bản dịch chưa có bản ghi sẽ được ghi nhận là tương ứng với bản gốc hiện tại.

Phiên làm việc của Claude Code và thao tác lưu của nhà cung cấp kiểu API sẽ tự động ghi lại (phiên làm việc được hướng dẫn dùng công cụ MCP `record_translation_freshness`). Nút này cần đến khi bạn dịch bằng Codex hoặc bằng chat của VS Code.

Từ đó trở đi, khi bạn thay đổi bản gốc, bản dịch của tài liệu đó sẽ hiển thị là “Cần cập nhật”.

> **Lưu ý**
>
> - Bản dịch đã có bản ghi thì không bị ghi đè, để không xóa mất trạng thái “Cần cập nhật”.
> - Bản ghi được lưu trong `.lunascape-docs/translation-freshness.json`. Nội dung lưu chỉ gồm đường dẫn tương đối, ngôn ngữ, mã băm của nội dung và thời điểm, không bao gồm phần thân tài liệu.

## Chủ đề liên quan

- [Công việc có thể giao](tasks.md)
- [Đọc bằng ngôn ngữ khác](../02-reading/languages.md)
