# Lunascape Docs là gì

Lunascape Docs là công cụ giúp bạn dùng nguyên trạng các tài liệu Markdown đặt trong kho lưu trữ Git như một “trang web bản đặc tả”. Không cần build trước, không cần máy chủ tài liệu hay cơ sở dữ liệu chuyên dụng.

## Những việc có thể làm

| Mục đích | Tính năng chính |
|---|---|
| Đọc | INDEX (mục lục), liên kết trong nội dung, đường dẫn phân cấp, quay lại/tiến tới, mục lục trong trang, tìm kiếm lọc |
| Xem | Bảng, khối mã, tự động khớp kích thước hình ảnh, công thức toán KaTeX, sơ đồ Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, thu gọn bảng quản lý tài liệu |
| Viết | Chuyển đổi giữa chỉnh sửa trực quan và chỉnh sửa mã nguồn Markdown; tạo, nhân bản, đổi tên, sắp xếp lại từ INDEX |
| Xác minh | Kiểm tra tài liệu bằng docs-lint, xác nhận tài liệu, chương, thuật ngữ bắt buộc theo Standard Pack, tạo tài liệu từ mẫu |
| Dịch | Tạo bản dịch đề xuất cho từng trang hoặc hàng loạt. Xem lại rồi mới lưu <!-- ai-only --> |
| Dùng từ AI | Công cụ đặc tả chỉ đọc mà các tác nhân trong VS Code có thể tham chiếu <!-- ai-only --> |

## Môi trường sử dụng

| Môi trường | Mục đích |
|---|---|
| Tiện ích mở rộng VS Code | Xem, chỉnh sửa, kiểm tra và dịch kho lưu trữ trên máy của bạn. Đây là trọng tâm của phần trợ giúp này |
| Phiên bản trình duyệt web | Xem tài liệu trên GitHub (công khai và riêng tư), bản nháp lưu trên thiết bị, xem thư mục cục bộ |
| Tiện ích mở rộng Chromium | Mở phiên bản trình duyệt web trong một thẻ của trình duyệt |

## Nguyên tắc cơ bản

- **Markdown là bản gốc.** Tài liệu vẫn là các tệp Markdown được quản lý bằng Git. Lunascape Docs không chuyển đổi chúng sang định dạng khác để lưu giữ.
- **Người dùng tự lưu.** Nội dung đã chỉnh sửa chỉ được ghi vào tệp khi bạn nhấn [Lưu]. Việc staging và commit trong Git không được thực hiện tự động.
- **Tài liệu được xử lý trên thiết bị.** Tài liệu không được gửi ra bên ngoài để xem hoặc chỉnh sửa. Chỉ khi dịch, nơi nhận và nội dung gửi đi mới được hiển thị trước, và tài liệu chỉ được gửi sau khi bạn chấp thuận.
- **Bản dịch được đặt trong `i18n/<言語>/`.** Tài liệu ở ngôn ngữ mặc định giữ nguyên vị trí; bản dịch được đặt với cùng đường dẫn tương đối trong `i18n/en/` và các thư mục tương tự.
- **AI chỉ dừng ở mức đề xuất.** Bản dịch đề xuất được lưu sau khi bạn xem lại phần khác biệt. Tài liệu không bao giờ bị âm thầm viết lại. <!-- ai-only -->

## Chủ đề liên quan

- [Tên và chức năng của các phần trên màn hình](screen.md)
- [Cài đặt tiện ích mở rộng](install.md)
- [Thao tác cơ bản](../02-reading/README.md)
