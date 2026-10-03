# Chỉnh sửa tài liệu

Bạn có thể chỉnh sửa tài liệu ngay trong trình xem. Màn hình chỉnh sửa có "chế độ hiển thị trực quan" để chỉnh sửa theo đúng những gì bạn thấy và "chế độ hiển thị nguồn Markdown"; một nút duy nhất dùng để chuyển đổi giữa hai chế độ.

## Bắt đầu chỉnh sửa

Nhấn một trong các cách sau. Tất cả đều mở cùng một màn hình chỉnh sửa.

- [Chỉnh sửa] ở góc dưới bên phải của nội dung
- [⋯] (Thao tác khác) ở góc trên bên phải của nội dung → [Chỉnh sửa]
- Menu mục trong INDEX → [Chỉnh sửa]

## Chỉnh sửa

1. Chỉnh sửa trực tiếp nội dung.
   Trên thanh công cụ ở phần trên của màn hình chỉnh sửa, bạn có thể dùng định dạng đoạn văn (nội dung, tiêu đề 1–4, trích dẫn, mã), [In đậm], [In nghiêng], [Danh sách dấu đầu dòng], [Danh sách đánh số], [Liên kết], [Chèn bảng], [Kích thước ảnh], [Hoàn tác], [Làm lại].
2. Khi muốn chỉnh sửa trực tiếp nguồn Markdown, hãy nhấn [Markdown].
   Nhấn một lần nữa để quay lại chế độ hiển thị trực quan. Chế độ hiển thị bạn dùng lần cuối sẽ được ghi nhớ và khôi phục vào lần tiếp theo bạn nhấn [Chỉnh sửa].
3. Nhấn [Lưu] (cũng có thể lưu bằng Ctrl+S / ⌘S).
   Nội dung được ghi vào tệp Markdown và trình xem quay lại chế độ đọc. Khi muốn dừng chỉnh sửa và trở về nội dung đã lưu lần cuối, hãy nhấn [Discard edits].

## Luôn bắt đầu từ màn hình chỉnh sửa (chế độ chỉnh sửa)

Nhấn [Edit mode] trên thanh công cụ để bật lên, thì mỗi lần mở tài liệu bạn sẽ bắt đầu từ màn hình chỉnh sửa. Dùng khi bạn muốn viết liên tục như trên một cuốn sổ tay.

- Khi đang bật, dù nhấn [Lưu] thì màn hình chỉnh sửa cũng không đóng lại. [Discard edits] sẽ trở về nội dung đã lưu lần cuối, và màn hình chỉnh sửa vẫn giữ nguyên.
- Nhấn một lần nữa để tắt và quay lại chế độ đọc. Trạng thái bật/tắt được ghi nhớ theo từng người dùng.
- Không hiển thị ở thư mục gốc tài liệu không ghi được (chẳng hạn nguồn chỉ đọc trên GitHub).

## Chỉnh sửa chưa lưu

Các chỉnh sửa chưa lưu sẽ tự động được giữ lại trên thiết bị này. Chúng không bị mất ngay cả khi bạn chuyển sang tài liệu khác hay đóng tab hoặc cửa sổ.

- [Unsaved] trên màn hình chỉnh sửa cho biết có sự khác biệt so với nội dung đã lưu lần cuối.
- Lần tiếp theo mở cùng tài liệu đó, nó sẽ tiếp tục từ các chỉnh sửa đã giữ lại và thông báo cho bạn biết. Nếu tài liệu gốc đã được cập nhật sau đó, nó cũng sẽ thông báo. Bạn có thể dùng [Discard edits] để trở về nội dung mới nhất.
- Các chỉnh sửa đã giữ lại sẽ biến mất khi bạn nhấn [Lưu] hoặc [Discard edits]. Vì chưa được lưu, chúng không xuất hiện trong Git hay trong bản nháp.

> **Lưu ý**
>
> - Việc lưu chỉ ghi vào tệp. Việc staging và commit của Git không được thực hiện tự động.
> - Các sơ đồ như công thức toán, Mermaid, TikZ, Vega-Lite được hiển thị dưới dạng kết quả kết xuất trong chế độ hiển thị trực quan. Để thay đổi nội dung, hãy chuyển sang [Markdown].
> - Tài liệu chứa cú pháp riêng của MDX (như thành phần hay `import`) chỉ được chỉnh sửa ở chế độ hiển thị Markdown, để giữ nguyên cú pháp.
> - front matter (phần cài đặt được bao trong `---` ở đầu tệp) vẫn được giữ lại ngay cả khi bạn chỉnh sửa ở chế độ hiển thị trực quan.

> **Gợi ý**
>
> - Nhấn [Mở trong VS Code] để mở bằng trình soạn thảo văn bản thông thường. Khi lưu trong trình soạn thảo văn bản, phần hiển thị của trình xem cũng tự động cập nhật.
> - Khi không muốn hiển thị nút [Chỉnh sửa], hãy tắt [Nút chỉnh sửa] trong [Cài đặt hiển thị]. Để ẩn trên toàn bộ dự án, hãy đặt `editor.showEditButton` trong `lunascape-docs.json` thành `false`.
> - Chế độ hiển thị mặc định khi mở lần đầu (trực quan / Markdown) có thể thay đổi bằng cài đặt `lunascapeDocEditor.editor.defaultMode` hoặc `editor.defaultMode` trong `lunascape-docs.json`.

## Xem thêm

- [Tạo và sắp xếp tài liệu và thư mục](organize.md)
- [Điều chỉnh kích thước ảnh](images.md)
- [Viết công thức toán](math.md)
- [Vẽ sơ đồ và biểu đồ](diagrams.md)
