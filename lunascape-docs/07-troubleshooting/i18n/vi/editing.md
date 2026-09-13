# Không thể chỉnh sửa, lưu hoặc sắp xếp lại

## Không có nút [Chỉnh sửa]

- [Nút chỉnh sửa] trong [Cài đặt hiển thị] đang tắt. Hãy bật nút đó, hoặc dùng [⋯] → [Chỉnh sửa] ở góc trên bên phải của nội dung, hoặc menu mục trong INDEX → [Chỉnh sửa].
- Trường hợp `editor.showEditButton` trong `lunascape-docs.json` là `false` cũng tương tự.
- Không thể chỉnh sửa khi đang hiển thị Trợ giúp. Hãy đóng Trợ giúp.

## Không thể chuyển sang chế độ hiển thị trực quan

「Tài liệu này chứa cú pháp MDX nên không thể chuyển sang màn hình chỉnh sửa thông thường」: tài liệu chứa cú pháp riêng của MDX (thành phần, `import`, v.v.) chỉ được chỉnh sửa ở chế độ hiển thị Markdown để giữ nguyên cú pháp đó.

## Không thể chỉnh sửa trực tiếp công thức toán hoặc sơ đồ

Chế độ hiển thị trực quan chỉ hiển thị kết quả kết xuất. Hãy nhấn [Markdown] trong màn hình chỉnh sửa và sửa mã nguồn.

## Không thể sắp xếp lại hoặc kéo thả

- Không thể sắp xếp lại khi đang lọc, khi đang chỉnh sửa tài liệu, hoặc khi một thao tác INDEX khác đang được xử lý.
- Khi không gian làm việc chưa được tin cậy, các thao tác tạo, sắp xếp và xóa đều không dùng được. Hãy tin cậy không gian làm việc trong VS Code.
- 「INDEX đã được cập nhật. Hãy kéo lại một lần nữa」: một thay đổi khác vừa được áp dụng. Hãy thực hiện lại thao tác.
- Không thể di chuyển trang bắt đầu (tệp `README.md` ở thư mục gốc).

## Hiển thị 「Có thay đổi chưa được lưu」

Tệp đích đang được chỉnh sửa trong trình soạn thảo của VS Code. Hãy lưu hoặc hủy bỏ các thay đổi trước, rồi thử lại.

## Không thể đổi tên

Không thể dùng những tên sau.

- Tên bắt đầu bằng `.`, tên `i18n`, tên dành riêng của Windows (như `CON`)
- Tên kết thúc bằng dấu chấm hoặc khoảng trắng, tên chứa ký tự điều khiển hoặc ký tự không dùng được trong tên tệp
- Tên đã có trong cùng một thư mục (kể cả tên chỉ khác nhau về chữ hoa chữ thường)
- Tên tài liệu không có phần mở rộng của Markdown

## Đã lưu nhưng Git không hiện thay đổi hoặc không được commit

Lunascape Docs chỉ ghi vào tệp, không thực hiện staging hay commit trong Git. Hãy kiểm tra trong khung nhìn quản lý mã nguồn của VS Code và commit khi cần.

## Xem thêm

- [Chỉnh sửa tài liệu](../03-editing/README.md)
- [Tạo và sắp xếp tài liệu, thư mục](../03-editing/organize.md)
- [Thay đổi thứ tự của tài liệu](../03-editing/reorder.md)
