# Kiểm tra, tạo hoặc dịch không thành công

## Kiểm tra

### Hiển thị thông báo "Không thể sử dụng docs-lint"

- Phần mở rộng không chứa môi trường chạy docs-lint, hoặc cài đặt có vấn đề. Hãy cài đặt lại phần mở rộng.
- "Hãy tin cậy không gian làm việc này trong VS Code để tải Pack cục bộ và cài đặt một cách an toàn": để dùng Standard Pack cục bộ, cần có không gian làm việc đáng tin cậy.

### Kết quả vẫn ở trạng thái "Cần kiểm tra lại"

Khi bạn thay đổi tài liệu hoặc cài đặt, kết quả trước đó không còn hiệu lực. Hãy nhấn lại [Kiểm tra thư mục gốc tài liệu]. Những thay đổi chưa lưu sẽ không được tính đến.

### Nhấn vào một cảnh báo nhưng không mở được gì

Các mục thuộc "Toàn bộ thư mục gốc tài liệu" không gắn với một tài liệu cụ thể nên không có vị trí. Hãy kiểm tra tài liệu tương ứng theo nội dung của cảnh báo.

### Không lưu được quy tắc

- Cần có không gian làm việc đáng tin cậy.
- "Cài đặt lint đã bị thay đổi bởi một thao tác khác": tệp `docs-lint.config.json` đã bị thay đổi từ bên ngoài. Hãy tải lại trạng thái mới nhất rồi thử lại.
- Không thể chỉnh sửa các tệp cài đặt là liên kết tượng trưng hoặc nằm ngoài thư mục gốc tài liệu.

## Tạo từ mẫu

- "Bản xem trước của mẫu đã hết hạn" / "Nội dung nhập đã thay đổi": hãy nhấn [Xem trước] một lần nữa rồi mới tạo.
- "Tài liệu tại nơi lưu đã tồn tại": tệp có sẵn sẽ không bị ghi đè. Hãy chỉ định nơi lưu khác.
- Nơi lưu cần một đường dẫn tương đối tính từ thư mục gốc tài liệu và phần mở rộng `.md` / `.mdx`. Không thể tạo bên dưới `i18n`.
- "Hãy tin cậy không gian làm việc để tạo tài liệu": hãy tin cậy không gian làm việc trong VS Code.

<!-- ai-only:start -->
## Bản dịch

### Không nhấn được các nút dịch

- "Bản dịch AI chưa được bật cho thư mục gốc tài liệu này": hãy đặt `translation.enabled` trong `lunascape-docs.json` thành `true`.
- "Chưa đặt ngôn ngữ mặc định của dự án": hãy lưu ngôn ngữ mặc định theo hướng dẫn tại [Thay đổi cài đặt hiển thị](../02-reading/display-settings.md).
- "Hãy thêm ngôn ngữ đích vào các ngôn ngữ được hỗ trợ": hãy thêm ngôn ngữ đích vào `locales`.
- "Không tìm thấy bản gốc để dịch": bạn đang mở một trang bản dịch. Hãy chuyển sang trang ở ngôn ngữ mặc định.
- Không dùng được dịch hàng loạt khi thư mục chỉ được mở tạm thời. Hãy đặt một tệp `lunascape-docs.json` vào thư mục đó để biến nó thành thư mục gốc tài liệu.

### Bản dịch đề xuất bị từ chối hoặc bị yêu cầu tạo lại

- "Bản gốc đã thay đổi. Hãy tạo lại bản dịch đề xuất": bản gốc hoặc bản đích đã thay đổi sau khi bản dịch đề xuất được tạo. Hãy dịch lại.
- Nếu phản hồi của mô hình ngôn ngữ thiếu các mã hoặc định danh cần được bảo vệ thì phản hồi đó sẽ không được chấp nhận. Bạn có thể xem nội dung phản hồi trong bảng đầu ra "Lunascape Docs Bản dịch".
- "Mỗi lần dịch hàng loạt tối đa 1000 tài liệu": hãy chia phạm vi theo thư mục hoặc chọn thủ công.
<!-- ai-only:end -->

## Chủ đề liên quan

- [Kiểm tra tài liệu](../04-document-tools/check.md)
- [Tạo tài liệu từ mẫu](../04-document-tools/templates.md)
- [Giao việc cho AI](../05-ai/README.md)
