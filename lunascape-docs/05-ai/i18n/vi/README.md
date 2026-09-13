# Giao tác vụ cho AI

Lunascape Docs không gọi mô hình ngôn ngữ. Sản phẩm chuẩn bị **ngữ cảnh, công cụ và bước kiểm chứng**, còn việc dịch, hiệu đính và soạn thảo thì giao cho AI mà bạn đang dùng.

## Ý tưởng

| Những gì sản phẩm chuẩn bị | Nội dung |
|---|---|
| Ngữ cảnh | Các quy ước của tài liệu (nơi đặt bản dịch, front matter, chuẩn tài liệu, bảng thuật ngữ) và vị trí của tài liệu cần xử lý |
| Công cụ làm việc | Sổ ghi các mục chưa dịch và cần cập nhật, việc đọc và ghi tài liệu, việc tạo tài liệu từ mẫu |
| Kiểm tra sau khi làm | Kiểm chứng bằng docs-lint, mức độ bao phủ và khác biệt về độ mới |

Câu lệnh không chứa nội dung của tài liệu. AI tự đọc tệp, tự ghi và tự kiểm chứng.

## Giao tác vụ

1. Nhấn [Công cụ tài liệu] trên thanh công cụ rồi mở thẻ [AI].
2. Chọn tác vụ muốn giao trong [Tác vụ].
3. Nhập các mục cần thiết (ngôn ngữ đích, chủ đề).
4. Nhấn [Giao tác vụ này].
   Một cửa sổ dòng lệnh của VS Code mở ra và AI bạn đã chọn nhận câu lệnh rồi bắt đầu làm việc.

> **Mẹo**
>
> Phiên làm việc của Claude Code luôn đi kèm công cụ làm việc (máy chủ MCP `lunascape-docs`). Phiên đó có thể tự lấy danh sách mục chưa dịch và cần cập nhật, tự chạy docs-lint và tự ghi lại độ mới sau khi dịch.

## Kiểm tra kết quả

| Dạng nhà cung cấp | Nơi kết quả đến |
|---|---|
| Dạng phiên (Claude Code, Codex) | Ghi thẳng vào cây làm việc. **Hãy kiểm tra bằng khác biệt của Git** |
| Dạng API (mô hình ngôn ngữ của VS Code, Anthropic, tương thích OpenAI) | Trả về đề xuất cho từng tài liệu một. Kiểm tra bằng [Mở khác biệt] rồi ghi bằng [Lưu] |

### Kiểm tra đề xuất của dạng API

Khi chạy với dạng API, đề xuất sẽ đến thẻ [AI].

1. Nhấn [Mở khác biệt] và đối chiếu với nội dung hiện tại.
2. Nếu thấy ổn, nhấn [Lưu]. Với bản dịch thì độ mới cũng được ghi lại. Nếu muốn bỏ, nhấn [Hủy bỏ].
   Để dừng giữa chừng việc tạo nội dung, nhấn [Dừng].

> **Lưu ý**
>
> - Lunascape Docs không bao giờ đưa vào vùng chờ hay tạo commit trong Git. Hãy luôn kiểm tra thay đổi bằng khác biệt.
> - Không thể giao tác vụ trong không gian làm việc chưa được tin cậy, cũng như khi đang xem tạm một thư mục nằm ngoài thư mục gốc tài liệu.

## Chủ đề liên quan

- [Các tác vụ có thể giao](tasks.md)
- [Cài đặt AI](settings.md)
- [Sổ ghi và bản ghi](ledger.md)
