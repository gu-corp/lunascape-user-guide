# Các tác vụ có thể giao

Chọn từ [Tác vụ] trong tab [AI]. Mỗi tác vụ có chỉ dẫn được giao và bước kiểm tra sau đó khác nhau.

| Tác vụ | Nội dung | Điều kiện cần | Loại API |
|---|---|---|---|
| Dịch trang này | Dịch tài liệu đang hiển thị sang ngôn ngữ đã chọn | Đang mở tài liệu cần dịch, ngôn ngữ đích | ○ |
| Dịch gộp phần chưa dịch | Lần lượt dịch các tài liệu chưa dịch và cần cập nhật của ngôn ngữ đã chọn | Ngôn ngữ đích | Chỉ loại phiên |
| Hiệu đính trang này | Kiểm tra và sửa thuật ngữ, văn phong cùng bố cục chương mục mà tiêu chuẩn tài liệu yêu cầu | Đang mở tài liệu cần hiệu đính | ○ |
| Tạo tài liệu mới | Tạo tài liệu mới theo tiêu chuẩn tài liệu và mẫu | Chủ đề (có thể bỏ qua) | Chỉ loại phiên |

## Những gì có trong chỉ dẫn

| Mục | Nội dung |
|---|---|
| 1 | Vị trí của thư mục gốc tài liệu. Chỉ dẫn không thay đổi bất cứ thứ gì bên ngoài phạm vi này |
| 2 | Ngôn ngữ mặc định (bản gốc) và nơi đặt bản dịch (thư mục `i18n/<ngôn ngữ>/` nằm cùng chỗ với tài liệu) |
| 3 | `navigation.order` chỉ thuộc về bản gốc, và bản dịch chỉ được phép ghi đè `navigation.title` |
| 4 | Không thay đổi ID yêu cầu, liên kết, mã, Mermaid, TeX và cấu trúc front matter |
| 5 | Tiêu chuẩn tài liệu và bảng thuật ngữ (`terminology` trong `docs-lint.config.json`) |
| 6 | Khi xong thì chạy kiểm tra tài liệu, báo cáo các tệp đã thay đổi và không thực hiện thao tác Git nào |

> **Mẹo**
>
> Đối tượng của "Dịch gộp phần chưa dịch" được tạo từ sổ ghi, mỗi lần tối đa 200 tài liệu. Nếu nhiều hơn, hãy chạy lại nhiều lần.

## Mục liên quan

- [Giao việc cho AI](README.md)
- [Sổ ghi và bản ghi](ledger.md)
