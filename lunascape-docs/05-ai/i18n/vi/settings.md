# Cài đặt AI

Chọn AI và mô hình sẽ nhận công việc của bạn. Màn hình này dùng các danh sách thả xuống riêng, không dùng ô chọn nhanh của VS Code.

1. Nhấn [Công cụ tài liệu] → thẻ [AI] → [Cài đặt AI…].
2. Chọn [Nhà cung cấp].
   Những mục máy này không dùng được sẽ hiện ở trạng thái không chọn được, kèm lý do.
3. Chọn [Mô hình]. Các lựa chọn thay đổi theo từng nhà cung cấp.
4. Đóng màn hình. Lựa chọn được lưu theo từng người dùng và dùng lại cho lần sau.

## Nhà cung cấp

| Nhà cung cấp | Dạng | Cách phát hiện |
|---|---|---|
| Claude Code | Phiên | Có lệnh `claude` hay không |
| Codex | Phiên | Có lệnh `codex` hay không |
| Mô hình ngôn ngữ của VS Code | API | Mô hình đã đăng ký với VS Code Language Model API |
| Anthropic API | API | Khóa API đã đăng ký |
| API tương thích OpenAI | API | Khóa API và điểm cuối đã đăng ký |

Nhà cung cấp **dạng phiên** tự đọc và ghi tệp, đồng thời tự chạy kiểm tra tài liệu. Kết quả được ghi thẳng vào cây làm việc và được xem lại bằng khác biệt của Git.

Nhà cung cấp **dạng API** trả về Markdown của một tài liệu, và phần mở rộng hiển thị khác biệt trước khi lưu.

## Đăng ký khóa API

Anthropic API và API tương thích OpenAI dùng được sau khi đăng ký khóa API.

1. Chọn nơi đăng ký ở [Nhà cung cấp]. Ô nhập khóa API sẽ hiện ra.
2. Nhập [Khóa API]. Với API tương thích OpenAI, nhập thêm [Điểm cuối] (ví dụ: `https://api.openai.com/v1`).
3. Nhấn [Lưu]. Dòng chữ “Đã đăng ký khóa” sẽ hiện ra.

> **Lưu ý**
>
> - Khóa được lưu trong SecretStorage của VS Code và không hiện lại lần nữa. Khóa cũng không được ghi vào `settings.json` hay vào tài liệu nào. Bạn có thể xóa bằng [Xóa khóa].
> - Danh sách mô hình được lấy từ từng dịch vụ bằng khóa đã đăng ký. Trong lúc chưa lấy được, danh sách đã biết sẽ hiển thị.
> - Nhà cung cấp dạng API chỉ chạy được “Dịch trang này” và “Soát lỗi trang này”. Việc duyệt qua nhiều tài liệu và tạo tài liệu hãy chạy bằng nhà cung cấp dạng phiên.

> **Mẹo**
>
> Nếu không tìm thấy nhà cung cấp nào, hãy cài đặt Claude Code hoặc Codex, hoặc đăng ký một khóa API. Mở lại [Cài đặt AI…] thì chúng sẽ được phát hiện.

## Chủ đề liên quan

- [Giao việc cho AI](README.md)
- [Danh sách cài đặt VS Code](../08-reference/settings.md)
