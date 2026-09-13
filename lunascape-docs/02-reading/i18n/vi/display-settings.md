# Thay đổi cài đặt hiển thị

Từ [Cài đặt hiển thị] (bánh răng) trên thanh công cụ, mỗi người dùng có thể thay đổi cách hiển thị của INDEX và việc hiện nút chỉnh sửa.

1. Nhấn [Cài đặt hiển thị] trên thanh công cụ.
2. Bật/tắt các mục muốn thay đổi. Thay đổi được áp dụng ngay lập tức.
3. Nhấn [Cài đặt hiển thị] một lần nữa, hoặc nhấn ra ngoài bảng, để đóng lại.

## Các mục có thể cài đặt

| Phân loại | Mục | Chức năng |
|---|---|---|
| Ngôn ngữ tài liệu | (trạng thái hiện tại) | Hiển thị ngôn ngữ mặc định của dự án và ngôn ngữ đang hiển thị. [Đặt ngôn ngữ của dự án…] mở phần cài đặt ngôn ngữ của dự án |
| Nội dung | [Tên tệp] | Hiển thị tên tệp thay cho tên tài liệu |
| | [Biểu tượng tài liệu] | Hiển thị biểu tượng ở mục tài liệu |
| | [Biểu tượng thư mục] | Hiển thị biểu tượng ở mục thư mục |
| | [Số mục trong thư mục] | Hiển thị số tài liệu có trong thư mục |
| | [Đường dẫn hướng phân cấp] | Hiển thị đường kẻ chỉ dẫn cấp bậc |
| | [Tự động ẩn khi chỉ có một tài liệu] | Ở thư mục gốc tài liệu chỉ có 1 tài liệu, tự động đóng INDEX trong lần đầu tiên |
| | [Thu gọn thông tin tài liệu] | Thu gọn bảng quản lý ở đầu tài liệu thành dòng “Thông tin tài liệu”. Khi tắt, bảng được hiển thị nguyên vẹn |
| | [Mật độ hiển thị] | Chọn khoảng cách dòng của INDEX từ [Chuẩn] / [Thu gọn] |
| | [Nút chỉnh sửa] | Hiển thị [Chỉnh sửa] ở góc dưới bên phải của nội dung |
| Thao tác | [Khôi phục mặc định của dự án] | Xóa toàn bộ thay đổi của người dùng và trở về cài đặt của dự án |
| | [Mở cài đặt tiện ích mở rộng] | Mở phần cài đặt của Lunascape Docs trong màn hình cài đặt của VS Code |

> **Mẹo**
>
> - Cài đặt hiển thị được lưu theo từng người dùng và từng thư mục gốc tài liệu, không ghi vào các tệp do Git quản lý.
> - Cài đặt được ưu tiên theo thứ tự “cài đặt hiển thị của người dùng → cài đặt VS Code → `lunascape-docs.json` → mặc định của sản phẩm”. Giá trị mặc định dùng chung cho nhóm được quyết định bằng `tree` và `editor` trong `lunascape-docs.json`.

## Chuyển đổi phối màu

Nhấn nút chuyển chủ đề (mặt trời／mặt trăng) trên thanh công cụ để chuyển đổi giữa nền trắng và phối màu của VS Code. Phối màu khi mở được quyết định bằng cài đặt `lunascapeDocEditor.appearance` (`light` hoặc `auto`).

## Mục liên quan

- [Sử dụng INDEX](index-panel.md)
- [Cài đặt dự án](../04-document-tools/project-configuration.md)
- [Danh sách cài đặt VS Code](../08-reference/settings.md)
