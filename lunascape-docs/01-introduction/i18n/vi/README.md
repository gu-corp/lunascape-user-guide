# Lunascape Docs là gì

Lunascape Docs là công cụ dùng các tài liệu Markdown đặt trong kho lưu trữ Git như một "trang bản đặc tả", nguyên trạng. Không cần bước dựng sẵn, không cần máy chủ tài liệu, không cần cơ sở dữ liệu riêng.

## Những việc có thể làm

| Mục đích | Tính năng chính |
|---|---|
| Đọc | INDEX (mục lục), liên kết trong nội dung, đường dẫn phân cấp, lùi lại – tiến tới, mục lục trong trang, tìm kiếm lọc |
| Xem | Bảng, khối mã, ảnh tự vừa khung, công thức toán KaTeX, sơ đồ Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, bảng quản lý tài liệu dạng thu gọn |
| Viết | Chuyển đổi giữa soạn thảo trực quan và soạn thảo mã nguồn Markdown; tạo, nhân bản, đổi tên, sắp xếp lại từ INDEX |
| Kiểm chứng | Kiểm tra tài liệu bằng docs-lint, xác nhận tài liệu, chương và thuật ngữ bắt buộc theo Standard Pack, tạo từ mẫu |
| Dịch | Tạo bản dịch đề xuất cho từng trang hoặc hàng loạt. Xem lại rồi mới lưu <!-- ai-only --> |
| Dùng từ AI | Công cụ bản đặc tả chỉ đọc, dành cho tác nhân của VS Code tham chiếu <!-- ai-only --> |

## Các môi trường sử dụng được

| Môi trường | Công dụng |
|---|---|
| Tiện ích mở rộng VS Code | Xem, sửa, kiểm tra và dịch kho lưu trữ trên máy của bạn. Đây là trọng tâm của phần trợ giúp này |
| Bản trình duyệt web | Xem tài liệu trên GitHub (công khai hoặc riêng tư), giữ bản nháp trong thiết bị, xem thư mục cục bộ |
| Tiện ích mở rộng Chromium | Mở bản trình duyệt web trong một thẻ của trình duyệt |
| Trình duyệt Lunascape | Dự kiến tích hợp cùng mô hình tài liệu này |

## Cách hiểu cơ bản

- **Markdown là bản gốc.** Tài liệu vẫn là các tệp Markdown được quản lý bằng Git. Lunascape Docs không chuyển đổi sang định dạng khác rồi giữ lại bản đó.
- **Việc lưu do người dùng thực hiện.** Nội dung đã sửa chỉ được ghi vào tệp khi bạn nhấn [Lưu]. Lunascape Docs không tự động đưa vào vùng staging hay commit của Git.
- **Tài liệu được xử lý trong thiết bị.** Việc xem hay sửa không gửi tài liệu ra bên ngoài. Chỉ khi dịch, nơi nhận và nội dung mới được hiển thị trước, rồi gửi đi sau khi bạn chấp thuận.
- **Bản dịch được đặt trong `i18n/<ngôn ngữ>/`.** Tài liệu bằng ngôn ngữ mặc định vẫn nằm nguyên chỗ; bản dịch nằm ở cùng đường dẫn tương đối trong `i18n/en/` và tương tự.
- **AI chỉ dừng ở mức đề xuất.** Bản dịch đề xuất chỉ được lưu sau khi bạn xem lại khác biệt. Tài liệu không bị sửa đổi một cách âm thầm. <!-- ai-only -->

## Mục liên quan

- [Tên gọi và chức năng các phần của màn hình](screen.md)
- [Cài đặt tiện ích mở rộng](install.md)
- [Thao tác cơ bản](../02-reading/README.md)
