# Tạo tài liệu từ mẫu

Trong tab [Tạo] của Công cụ tài liệu, bạn có thể chọn một mẫu, xem trước nội dung rồi tạo tài liệu mới.

1. Nhấn [Công cụ tài liệu] trên thanh công cụ và mở tab [Tạo].
2. Nhấn [Tạo từ mẫu] và chọn một mẫu.
3. Điền các mục nhập (tiêu đề, tóm tắt, v.v.). Các mục bắt buộc được đánh dấu "Bắt buộc".
4. Nhập nơi lưu bằng đường dẫn tương đối tính từ Thư mục gốc tài liệu (ví dụ: `03-design/api.md`).
5. Nhấn [Xem trước] và kiểm tra phần Markdown được tạo ra.
6. Nhấn [Tạo với nội dung này].
   Tài liệu được tạo và hiển thị trong trình xem. Sau đó, toàn bộ Thư mục gốc tài liệu sẽ được kiểm tra.

## Các mẫu có thể chọn

| Mẫu | Nội dung |
|---|---|
| Tài liệu một trang | Tạo một bản đặc tả ngắn, ghi chú hoặc tài liệu giải thích độc lập trong một tệp |
| Bản đặc tả・Hướng dẫn sử dụng・Trợ giúp | Tạo một tệp với bố cục chương mục tổng quát, dùng được cho bản đặc tả, hướng dẫn sử dụng và trợ giúp |
| Mẫu của Standard Pack | Khi Standard Pack được chọn trong `lunascape-docs.json`, các loại tài liệu dùng được với hồ sơ đó (bản đặc tả yêu cầu, bản thiết kế, v.v.) sẽ được bổ sung |

> **Lưu ý**
>
> - Việc tạo tài liệu cần một Không gian làm việc đáng tin cậy.
> - Các tệp hiện có sẽ không bị ghi đè. Nếu nơi lưu đã có tài liệu trùng tên thì không thể tạo được.
> - Nơi lưu cần có phần mở rộng `.md` hoặc `.mdx`. Không thể tạo bên dưới `i18n` (nơi chứa các bản dịch).
> - Sau khi thay đổi nội dung nhập, hãy nhấn [Xem trước] một lần nữa rồi mới tạo.

> **Gợi ý**
>
> Với dự án chưa có thư mục tài liệu, bạn có thể tạo bộ tài liệu đầu tiên bằng "Lunascape Docs: Tạo tài liệu từ mẫu" trong Bảng lệnh. Xem [Tạo tài liệu lần đầu](../01-introduction/first-documents.md).

## Xem thêm

- [Sử dụng Công cụ tài liệu](README.md)
- [Thay đổi quy tắc kiểm tra](rules.md)
