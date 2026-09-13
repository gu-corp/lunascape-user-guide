# Kiểm tra tài liệu

Với docs-lint, bạn có thể kiểm tra cấu trúc tiêu đề, liên kết hỏng, thiếu tài liệu hoặc chương bắt buộc, thuật ngữ không thống nhất, tính nhất quán của ID yêu cầu và nhiều điểm khác. Việc kiểm tra luôn áp dụng cho toàn bộ thư mục gốc tài liệu.

## Chạy kiểm tra

1. Nhấn [Công cụ tài liệu] trên thanh công cụ rồi mở thẻ [Kiểm tra].
2. Nhấn [Kiểm tra thư mục gốc tài liệu].
   Bạn cũng có thể chạy bằng lệnh “Lunascape Docs: Kiểm tra thư mục gốc tài liệu” trong bảng lệnh.
3. Xem danh sách kết quả.

## Đọc kết quả

- Dùng [Tài liệu này] / [Tất cả] ở phía trên danh sách để chuyển phạm vi hiển thị. Bản thân phạm vi kiểm tra thì luôn là toàn bộ thư mục gốc tài liệu.
- Các mục phát hiện có 4 mức: “lỗi”, “cảnh báo”, “thông tin” và “gợi ý”. Nút [Công cụ tài liệu] trên thanh công cụ hiển thị số lượng lỗi và cảnh báo.
- Nhấn vào một mục phát hiện để mở đúng vị trí trong nguồn Markdown bằng trình soạn thảo của VS Code.
- Những mục liên quan đến toàn bộ thư mục gốc tài liệu (ví dụ thiếu tài liệu kiểm thử) được hiển thị dưới mục “Toàn bộ thư mục gốc tài liệu” và không có vị trí cụ thể.
- Các mục phát hiện này cũng xuất hiện trong bảng “Sự cố” của VS Code.

## Các mục được kiểm tra

Nhấn [Xem và thay đổi quy tắc] để xem danh sách các mục kiểm tra đang bật và mục đích của từng mục. Các mục chính như sau.

| Mục | Nội dung |
|---|---|
| Cấu trúc tiêu đề | Có đúng một H1 và các cấp tiêu đề không bị nhảy cóc hay không |
| Liên kết nội bộ | Tài liệu được liên kết có tồn tại và không ra ngoài thư mục gốc tài liệu hay không |
| Ngôn ngữ của khối mã | Khối mã có chỉ định tên ngôn ngữ hay không |
| Thư mục và tài liệu bắt buộc | Đã có đủ các thư mục và tài liệu mà hồ sơ của Standard Pack yêu cầu hay chưa |
| Chương bắt buộc của tài liệu | Mỗi loại tài liệu có đủ các chương bắt buộc hay không |
| Thống nhất thuật ngữ | Phát hiện cách diễn đạt cần tránh và khuyến khích dùng thuật ngữ được đề xuất |
| Cách đặt tên và trùng lặp ID yêu cầu | ID yêu cầu có theo quy tắc đặt tên và không bị định nghĩa hai lần hay không |
| Tính nhất quán tham chiếu ID yêu cầu | ID yêu cầu được thiết kế, kiểm thử, bảng tình trạng tham chiếu có thực sự tồn tại hay không |
| Đối ứng giữa yêu cầu và kiểm thử | ID yêu cầu có được tham chiếu từ tài liệu kiểm thử hay không |

Những mục được bật phụ thuộc vào Standard Pack và hồ sơ đã chọn trong `lunascape-docs.json`, cũng như `docs-lint.config.json`.

> **Lưu ý**
>
> - Khi bạn thay đổi tài liệu hoặc cài đặt, kết quả lần trước sẽ chuyển thành “cần kiểm tra lại”. Kết quả không tự động được xem là đạt. Hãy nhấn lại [Kiểm tra thư mục gốc tài liệu].
> - Các thay đổi chưa lưu không được đưa vào kiểm tra. Hãy lưu trước.
> - Việc kiểm tra chạy ngay trên máy và cho kết quả xác định. Kết quả đánh giá hay bản dịch của AI không bao giờ lẫn vào kết quả kiểm tra.

## Mục liên quan

- [Thay đổi quy tắc kiểm tra](rules.md)
- [Cấu hình dự án](project-configuration.md)
- [Kiểm tra, tạo hoặc dịch không hoạt động](../07-troubleshooting/tools.md)
