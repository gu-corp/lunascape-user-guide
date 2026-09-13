# Không mở được hoặc không đăng nhập được trên bản Web

## Đã đăng nhập nhưng kho lưu trữ không hiện trong danh sách

GitHub App “Lunascape Docs” chưa được cài đặt cho tài khoản đó, hoặc kho lưu trữ không nằm trong phạm vi cài đặt. Hãy nhờ chủ sở hữu kho lưu trữ hoặc quản trị viên của tổ chức cài đặt theo hướng dẫn trong [Xem kho lưu trữ riêng tư](../06-web/private-repository.md).

## Không qua được màn hình đăng nhập

- Bạn không có quyền đọc kho lưu trữ đó. Hãy nhờ chủ sở hữu kho lưu trữ cấp quyền.
- “Trang web này chưa được thiết lập đăng nhập GitHub”: trình xem do bạn tự triển khai chưa được cấu hình dịch vụ đăng nhập. Quản trị viên cần thiết lập dịch vụ đăng nhập.

## Cửa sổ bật lên để đăng nhập không mở

Trình duyệt đang chặn cửa sổ bật lên. Hãy cho phép cửa sổ bật lên cho trang web này, rồi thử lại.

## Hiển thị “Phiên đăng nhập đã hết hạn”

Phiên đăng nhập đã hết hạn. Hãy nhấn [Đăng nhập bằng GitHub] một lần nữa.

## Mở kho lưu trữ công khai thì gặp lỗi 404

- Kiểm tra cách viết `owner/repo@ref/dir`.
- Không thể chỉ định tên nhánh có chứa `/`.

## Sau một lúc thì không tải được nữa

Khi chưa đăng nhập, GitHub API có giới hạn sử dụng (60 lần mỗi giờ). Nếu hiển thị “Đã đạt giới hạn số lần”, hãy đợi một lát hoặc [Đăng nhập bằng GitHub].

## Hiển thị “Không thể hiển thị kho lưu trữ này từ trang web này”

Để mở từ trình xem do bạn tự triển khai, cần thêm URL của trang web đó vào `viewer.origins` trong tệp `lunascape-docs.json` của kho lưu trữ.

## Mở `index.html` nhưng không hiển thị gì

Mở trực tiếp bằng `file://` thì không hoạt động. Hãy mở qua máy chủ HTTP, hoặc dùng bản VS Code.

## Trang web đã xuất hiển thị “Không tìm thấy lunascape-docs-manifest.json”

Hãy triển khai nguyên vẹn toàn bộ tệp xuất ra bằng `npm run export:web`, bao gồm cả tệp manifest.

## Không lưu được bản nháp

- “Không thể mở IndexedDB”, “Đang được dùng ở tab khác”: nguyên nhân là chế độ riêng tư của trình duyệt, hoặc một tab khác đang mở cùng trang web. Hãy mở trong cửa sổ thông thường và đóng các tab khác.
- Bản nháp được lưu theo từng thiết bị và từng trình duyệt. Bản nháp không được chuyển sang thiết bị khác.

## Mục liên quan

- [Mở kho lưu trữ GitHub](../06-web/open-repository.md)
- [Lưu bản nháp](../06-web/drafts.md)
