# Sơ đồ, công thức toán hoặc hình ảnh không hiển thị

## Hình TikZ hiển thị dưới dạng mã nguồn đã thu gọn

- Bản phân phối của tiện ích mở rộng không kèm theo công cụ dựng hình TikZ. Đây là cách hiển thị bình thường.
- Để phát triển và đánh giá, hãy cài `node-tikzjax` 1.0.5 ngay trong thư mục gốc của không gian làm việc đáng tin cậy và đặt cài đặt `lunascapeDocEditor.tikz.runtime` thành `workspace`.
- Bản xem trên trình duyệt Web không dựng hình TikZ.

## Công thức toán hiển thị dưới dạng văn bản thường

- Kiểm tra ký hiệu phân cách. Công thức trong dòng dùng `$...$` hoặc `\(...\)`, công thức riêng dòng dùng `$$...$$` hoặc `\[...\]`.
- Dấu `$` nằm trong mã nội dòng hoặc trong khối mã không tạo thành công thức toán.
- Cách viết giống số tiền như `$5 and $10` không được xem là công thức toán.
- Công thức quá lớn hoặc có nhiều lệnh macro khai triển sẽ không được dựng khi vượt quá giới hạn (`maxSize: 50`, `maxExpand: 1000`). Hãy chia nhỏ công thức.

## Sơ đồ báo "không thể dựng hình"

- Thông báo lỗi của Mermaid, Vega-Lite, WaveDrom và các công cụ khác cho biết vấn đề về cú pháp. Hãy xem mã nguồn trong màn hình soạn thảo bằng [Markdown].
- Vega-Lite: nhúng dữ liệu vào `data.values` hoặc `datasets`. Không dùng được dữ liệu từ URL bên ngoài và mốc hình ảnh.
- WaveDrom: viết theo đúng chuẩn JSON. Không dùng được dạng JavaScript (khóa không có dấu ngoặc kép và tương tự).
- Penrose: chỉ dùng `@preset set-theory` ở đầu và các câu lệnh được cho phép (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- "SVG được tạo có chứa tham chiếu không an toàn" / "SVG được tạo vượt quá giới hạn": sơ đồ tham chiếu đến tài nguyên bên ngoài hoặc sơ đồ quá lớn sẽ không hiển thị. Hãy giảm bớt nội dung hoặc bỏ các tham chiếu.

## Hình ảnh không hiển thị

- Đường dẫn hình ảnh được chỉ định theo đường dẫn tương đối tính từ tài liệu. Hình ảnh nằm ngoài thư mục gốc tài liệu sẽ không hiển thị.
- Thuộc tính `width` của `<img>` chỉ nhận giá trị số (`width="360"`).

## Sơ đồ không hiển thị trên trang web đã xuất

Các thư viện dựng hình của TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob và Penrose được tải khi hiển thị. Hãy đặt kèm thư mục `vendor/` cùng với trang web đã xuất.

## Chủ đề liên quan

- [Viết công thức toán](../03-editing/math.md)
- [Vẽ sơ đồ và biểu đồ](../03-editing/diagrams.md)
- [Điều chỉnh kích thước hình ảnh](../03-editing/images.md)
