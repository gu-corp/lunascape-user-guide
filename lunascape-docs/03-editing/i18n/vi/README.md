# Chỉnh sửa tài liệu

Bạn có thể chỉnh sửa tài liệu ngay trong trình xem. Màn hình chỉnh sửa có chế độ "hiển thị trực quan" cho phép sửa đúng như những gì bạn thấy, và chế độ "hiển thị mã nguồn Markdown"; một nút duy nhất dùng để chuyển đổi giữa hai chế độ.

## Bắt đầu chỉnh sửa

Nhấn một trong các mục sau. Tất cả đều mở cùng một màn hình chỉnh sửa.

- [Chỉnh sửa] ở góc dưới bên phải nội dung
- [⋯] (Thao tác khác) ở góc trên bên phải nội dung → [Chỉnh sửa]
- Menu mục trong INDEX → [Chỉnh sửa]

## Chỉnh sửa

1. Chỉnh sửa trực tiếp nội dung.
   Trên thanh công cụ ở phía trên màn hình chỉnh sửa, bạn có thể dùng định dạng đoạn văn (nội dung, tiêu đề 1–4, trích dẫn, mã), [In đậm], [In nghiêng], [Danh sách dấu đầu dòng], [Danh sách đánh số], [Liên kết], [Chèn bảng], [Kích thước ảnh], [Hoàn tác], [Làm lại].
2. Khi muốn chỉnh sửa trực tiếp mã nguồn Markdown, hãy nhấn [Markdown].
   Nhấn lần nữa để quay lại hiển thị trực quan. Chế độ hiển thị dùng lần cuối sẽ được ghi nhớ và khôi phục khi bạn nhấn [Chỉnh sửa] lần sau.
3. Nhấn [Lưu].
   Nội dung được ghi vào tệp Markdown và màn hình trở về chế độ xem. Khi muốn dừng lại, hãy nhấn [Hủy].

> **Lưu ý**
>
> - Thao tác lưu chỉ ghi vào tệp. Việc staging hay commit của Git không được thực hiện tự động.
> - Công thức toán và các sơ đồ như Mermaid, TikZ, Vega-Lite được hiển thị ở dạng đã kết xuất trong chế độ hiển thị trực quan. Để thay đổi nội dung của chúng, hãy chuyển sang [Markdown].
> - Tài liệu chứa cú pháp riêng của MDX (thành phần, `import` v.v.) chỉ được chỉnh sửa ở chế độ hiển thị Markdown, nhằm giữ nguyên cú pháp đó.
> - Front matter (phần cài đặt nằm giữa các dòng `---` ở đầu tệp) vẫn được giữ nguyên khi bạn chỉnh sửa ở chế độ hiển thị trực quan.

> **Gợi ý**
>
> - Nhấn [Mở trong VS Code] để mở tệp bằng trình soạn thảo văn bản thông thường. Khi bạn lưu trong trình soạn thảo văn bản, màn hình của trình xem cũng tự động được cập nhật.
> - Khi không muốn hiển thị nút [Chỉnh sửa], hãy tắt [Nút chỉnh sửa] trong [Cài đặt hiển thị]. Để ẩn nút này cho toàn bộ dự án, hãy đặt `editor.showEditButton` trong `lunascape-docs.json` thành `false`.
> - Chế độ hiển thị mở đầu tiên (trực quan hoặc Markdown) có thể thay đổi bằng cài đặt `lunascapeDocEditor.editor.defaultMode` hoặc `editor.defaultMode` trong `lunascape-docs.json`.

## Chủ đề liên quan

- [Tạo và sắp xếp tài liệu, thư mục](organize.md)
- [Điều chỉnh kích thước ảnh](images.md)
- [Viết công thức toán](math.md)
- [Vẽ sơ đồ và biểu đồ](diagrams.md)
