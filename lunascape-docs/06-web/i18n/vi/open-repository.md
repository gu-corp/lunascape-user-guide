# Mở kho lưu trữ GitHub

Ở bản Web, bạn mở tài liệu bằng cách chỉ định một kho lưu trữ GitHub. Với kho lưu trữ công khai thì không cần đăng nhập.

## Mở từ màn hình

1. Mở <https://docs.lunascape.org/>.
2. Nhấn [Mở tài liệu] (biểu tượng thư mục) trên thanh công cụ.
3. Nhập kho lưu trữ vào [Nhập trực tiếp kho lưu trữ] rồi nhấn [Mở].
   Khi đã đăng nhập GitHub, bạn cũng có thể chọn từ danh sách ở [Chọn từ các kho lưu trữ đọc được].

> **Gợi ý**
>
> - Biểu tượng GitHub ở bên cạnh sẽ mở tài liệu bạn đang đọc trên github.com. Đó không phải là thao tác mở tài liệu.

## Mở bằng URL

Địa chỉ là dạng xếp liền vị trí của kho lưu trữ và của tài liệu. Đường dẫn là vị trí bên trong kho lưu trữ, nên có thứ tự giống với URL của GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Chỉ định | Cách viết |
|---|---|
| Chỉ kho lưu trữ (nhánh mặc định) | `/github/owner/repo` |
| Tài liệu bên trong kho lưu trữ | `/github/owner/repo/docs/01-product/vision.md` |
| Chỉ định nhánh hoặc thẻ | Thêm `?ref=v1.2.0` vào cuối |

Khi bạn chuyển trang thì địa chỉ cũng thay đổi. Nhấn [Chia sẻ tài liệu này] trên thanh công cụ để gửi liên kết đến trang bạn đang đọc. Nút [Quay lại] và [Tiến tới] của trình duyệt cũng dùng được.

Dạng `?source=` trước đây vẫn mở được như từ trước tới nay. Sau khi mở, địa chỉ sẽ được viết lại theo dạng mới.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Lưu ý**
>
> - Khi chưa đăng nhập, giới hạn sử dụng GitHub API (60 lần mỗi giờ) sẽ được áp dụng. Với kho lưu trữ có nhiều tài liệu hoặc khi xem đi xem lại, hãy [Đăng nhập bằng GitHub].
> - Tên nhánh có chứa `/` (như `feature/xxx`) có thể chỉ định bằng `?ref=` theo dạng địa chỉ ở trên. Dạng `?source=` không viết được.
> - Tài liệu được tải bằng quyền GitHub của chính người xem. Người không có quyền đọc sẽ không thấy tài liệu.

## Mở tài liệu từ thư mục trên máy

Nhấn [Mở tài liệu] trên thanh công cụ, rồi từ [Mở tài liệu từ thư mục trên máy] ở bên dưới danh sách, chọn một thư mục trong máy. Tệp được xử lý ngay trong trình duyệt và không được gửi ra bên ngoài. Tính năng này dùng được trên các trình duyệt hỗ trợ chọn thư mục (Chrome, Edge và các trình duyệt khác).

## Mục liên quan

- [Xem kho lưu trữ riêng tư](private-repository.md)
- [Không mở được hoặc không đăng nhập được ở bản Web](../07-troubleshooting/web.md)
