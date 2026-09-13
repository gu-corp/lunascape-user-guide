# Bảo mật và phạm vi ghi

Các ranh giới mà Lunascape Docs đặt ra để bảo vệ tài liệu và thiết bị của bạn.

## Hiển thị

- HTML sinh ra từ Markdown và SVG sinh ra từ sơ đồ được làm sạch bằng DOMPurify 3.4.14 trước khi hiển thị.
- Mọi script tùy ý có trong MDX đều không được thực thi.
- KaTeX chạy với `trust: false`, `maxSize: 50` và `maxExpand: 1000`, không tin cậy HTML bên ngoài cũng như lệnh tùy ý.
- Các thư viện vẽ Markmap, WaveDrom, Svgbob, Vega-Lite và Penrose chỉ được nạp trong thiết bị, ở phiên bản cố định, khi có khối tương ứng. Không cho phép tham chiếu đến tài nguyên bên ngoài, HTML thô và ký pháp thực thi được; script, ảnh bên ngoài, `link`, `style` và `foreignObject` bị loại bỏ khỏi SVG được sinh ra.
- Việc vẽ TikZ không khởi chạy LaTeX của máy chủ, mà chạy tuần tự trong một worker TeX WebAssembly có hệ thống tệp trong bộ nhớ. Đầu vào, hàng đợi, bộ nhớ, thời gian chạy (15 giây) và đầu ra SVG đều có giới hạn trên, và các lệnh I/O tệp bị từ chối.

## Truy cập tài liệu và tệp

- Liên kết trong tài liệu và các thao tác tệp không thể ra ngoài thư mục gốc tài liệu.
- Các thao tác tạo, đổi tên, di chuyển và xóa từ INDEX chỉ được áp dụng sau khi phía tiện ích mở rộng xác nhận lại thư mục gốc tài liệu, phiên bản của INDEX, đường dẫn bản gốc, loại đối tượng, ranh giới liên kết tượng trưng và các tài liệu chưa lưu. Các yêu cầu thao tác từ menu cũ hoặc từ một thư mục gốc tài liệu khác sẽ không được áp dụng.
- Trong khi đang chỉnh sửa tài liệu hoặc đang áp dụng một thao tác INDEX khác, các thao tác thay đổi INDEX bị vô hiệu hóa.
- Việc tạo từ mẫu xác nhận lại độ tin cậy của không gian làm việc, thực thể của thư mục gốc tài liệu, phiên bản của INDEX, Standard Pack và nội dung được sinh ra, nơi lưu và ranh giới liên kết tượng trưng sau khi xem trước. Thao tác này không ghi đè tệp đã có, và không tạo nội dung khác với bản xem trước hay kết quả triển khai vượt quá 4 MiB.
- Khi lưu tệp cấu hình, phiên bản được kiểm tra ngay trước lúc lưu, và việc lưu sẽ bị hủy nếu phát hiện thay đổi từ bên ngoài.

## Gửi ra bên ngoài

- Tài liệu không bao giờ được gửi ra bên ngoài để xem, chỉnh sửa hay kiểm tra. Việc kiểm tra tài liệu chạy trong thiết bị một cách tất định.
- Chỉ có bản dịch (dịch trang này, dịch hàng loạt) mới gửi tài liệu đến mô hình ngôn ngữ, sau khi hiển thị trước nơi nhận và phạm vi gửi, và chỉ khi được chấp thuận rõ ràng. <!-- ai-only -->
- Bản dịch đề xuất được trình bày dưới dạng khác biệt; sau khi xác nhận lại phiên bản của bản gốc và bản dịch, đề xuất chỉ được áp dụng khi có người lưu lại một cách rõ ràng. <!-- ai-only -->
- Công cụ bản đặc tả dành cho tác nhân AI không trả về nội dung tài liệu, tên không gian làm việc hay đường dẫn cục bộ. <!-- ai-only -->

## Git

- Việc lưu chỉ ghi vào tệp. Không tính năng nào tự động staging hay commit trong Git.
- Các tệp đã có như `_meta.json` không bao giờ bị xóa hay thay đổi một cách âm thầm. Các bản dịch mồ côi cũng không bị tự động xóa hay di chuyển.

## Chủ đề liên quan

- [Bản đặc tả chính](README.md)
- [Sử dụng từ AI](ai-agents.md)
