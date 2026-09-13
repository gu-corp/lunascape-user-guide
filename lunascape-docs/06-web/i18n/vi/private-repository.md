# Xem kho lưu trữ riêng tư

Tài liệu trong các kho lưu trữ riêng tư có thể xem được sau khi bạn đăng nhập bằng GitHub, giới hạn ở những kho mà bạn có quyền đọc. Lunascape Docs không bao giờ có tài khoản hay quyền hạn riêng.

## Đăng nhập và mở

1. Mở <https://docs.lunascape.org/>.
   Khi bạn chỉ định một tài liệu riêng tư hoặc chưa đăng nhập, màn hình đăng nhập sẽ hiện ra.
2. Nhấn [Đăng nhập bằng GitHub].
   Màn hình xác thực của GitHub mở ra trong một cửa sổ bật lên.
3. Sau khi đăng nhập xong, nhấn [Mở tài liệu] trên thanh công cụ, rồi chọn kho lưu trữ muốn mở trong [Chọn từ các kho lưu trữ đọc được].

> **Mẹo**
>
> - Tên tài khoản đang đăng nhập được hiển thị trên thanh công cụ. Bạn cũng có thể [Đăng xuất] hoặc [Đăng nhập bằng tài khoản khác] từ đây.
> - Danh sách hiển thị các kho lưu trữ của những tài khoản (tổ chức hoặc cá nhân) đã cài đặt GitHub App "Lunascape Docs", giới hạn ở những kho mà bạn có quyền đọc.

## Cài đặt do chủ sở hữu kho lưu trữ thực hiện

Nếu kho lưu trữ cần tìm không hiển thị trong danh sách, chủ sở hữu kho lưu trữ hoặc quản trị viên của tổ chức phải cài đặt GitHub App "Lunascape Docs".

- Quyền được yêu cầu là Contents (đọc và ghi) và Pull requests (đọc và ghi). Quyền đọc để xem; quyền ghi để gửi yêu cầu xuất bản (Pull Request) từ Web. Lunascape Docs không bao giờ lưu trữ nội dung tài liệu.
- Đơn vị cài đặt là tài khoản (tổ chức hoặc cá nhân). Bạn thiết lập đối tượng là "All repositories" (bao gồm cả các kho lưu trữ được tạo về sau) hay chỉ những kho lưu trữ đã chọn.

| Tình huống | Các bước |
|---|---|
| Cài đặt mới cho một tài khoản tổ chức hoặc cá nhân | Thực hiện từ [trang cài đặt](https://github.com/apps/lunascape-docs/installations/new) |
| Thêm kho lưu trữ vào một tổ chức đã cài đặt | Thiết lập tại Settings của tổ chức → GitHub Apps → Lunascape Docs → Configure → Repository access |

Ngay cả khi cài đặt cho toàn bộ tổ chức, mỗi thành viên chỉ xem được những kho lưu trữ mà bản thân có quyền đọc. Và chỉ có thể gửi yêu cầu xuất bản đến những kho lưu trữ mà bản thân có quyền ghi.

> **Mẹo**
> - Khi cài đặt mới, các quyền được yêu cầu sẽ hiển thị dưới dạng danh sách trên màn hình cài đặt, và tại thời điểm nhấn "Install" là bạn đã chấp thuận. Không cần thao tác thêm.
> - Với tổ chức đã cài đặt từ trước khi có thêm quyền, quản trị viên sẽ nhận được email xác nhận, và một nút chấp thuận sẽ hiển thị ở phần trên của Settings của tổ chức → GitHub Apps → Lunascape Docs → Configure. Cho đến khi chấp thuận, tổ chức đó chỉ có thể xem, và khi gửi yêu cầu xuất bản sẽ hiện thông báo "cần được cấp quyền ghi".
> - Bạn có thể kiểm tra hiện đang cài đặt với quyền nào ngay trên màn hình Configure đó. Với tài khoản cá nhân thì tại Settings → Applications → Installed GitHub Apps.
> - Nếu lỡ bỏ kho lưu trữ khỏi đối tượng hoặc gỡ cài đặt, chỉ cần cài lại từ [trang cài đặt](https://github.com/apps/lunascape-docs/installations/new) là mọi thứ trở về như cũ. Thông báo từ chối yêu cầu xuất bản có kèm liên kết đến màn hình để sửa.
> - Nếu phía kho lưu trữ không muốn nhận yêu cầu xuất bản, hãy ghi `"publish": { "enabled": false }` trong `lunascape-docs.json`. Việc xem vẫn dùng được như thường.

## Mục liên quan

- [Mở kho lưu trữ GitHub](open-repository.md)
- [Không mở được hoặc không đăng nhập được ở bản Web](../07-troubleshooting/web.md)
