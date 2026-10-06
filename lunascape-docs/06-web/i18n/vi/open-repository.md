# Mở kho lưu trữ GitHub

Trên phiên bản Web, bạn có thể mở và đọc trực tiếp kho lưu trữ GitHub mà không cần sao chép kho lưu trữ về máy. Với kho lưu trữ công khai, bạn không cần đăng nhập.

## Mở từ màn hình

1. Nhấn [Mở tài liệu] (biểu tượng thư mục) trên thanh công cụ. Màn hình “Mở tài liệu” sẽ mở ra.
2. Ở cột bên trái, chọn nơi cần mở.

   | Vị trí | Nội dung hiển thị |
   |---|---|
   | Tất cả | Tất cả các mục bên dưới. Các mục mở gần đây được xếp lên đầu |
   | Mở gần đây | Các kho lưu trữ và thư mục bạn đã mở trước đây |
   | Đề xuất | Các hướng dẫn sử dụng mà trang web giới thiệu |
   | Kho lưu trữ GitHub | Khi bạn đã đăng nhập GitHub, các kho lưu trữ bạn có thể đọc |
   | Máy tính này | Các thư mục trên thiết bị này |

3. Nhấn [Mở] ở hàng muốn mở. Nhập vào ô [Lọc theo tên tài liệu hoặc tên kho lưu trữ] ở phía trên để lọc các hàng.

Với kho lưu trữ không có trong danh sách, hãy chỉ định qua [Nhập owner/repo để mở] ở cột bên trái.

> **Mẹo**
>
> - Các kho lưu trữ GitHub xuất hiện trong danh sách là những kho đã cài GitHub App “Lunascape Docs” và bạn có quyền đọc. Nếu không thấy kho lưu trữ cần mở, hãy nhờ chủ sở hữu kho lưu trữ thêm App này.

## Kiểm tra vị trí của tài liệu

Biểu tượng nhỏ ở phía bên trái thanh công cụ (chip vị trí) cho biết tài liệu bạn đang đọc nằm ở đâu.

| Biểu tượng | Vị trí |
|---|---|
| Biểu tượng GitHub | Đang đọc từ GitHub. Tài liệu không được lưu trên thiết bị này |
| Thư mục | Thư mục trên thiết bị này |

Nhấn vào biểu tượng để xem vị trí, trạng thái và các thao tác có thể thực hiện từ đó ([Xem trên GitHub], [Sao chép liên kết], v.v.).

## Mở bằng URL

Địa chỉ được tạo bằng cách ghép nguyên vị trí của kho lưu trữ và tài liệu. Đường dẫn là vị trí bên trong kho lưu trữ, nên có cùng thứ tự với URL trên GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Chỉ định | Cách viết |
|---|---|
| Chỉ kho lưu trữ (nhánh mặc định) | `/github/owner/repo` |
| Tài liệu bên trong kho lưu trữ | `/github/owner/repo/docs/01-product/vision.md` |
| Chỉ định nhánh hoặc thẻ | Thêm `?ref=v1.2.0` vào cuối |

Khi chuyển trang, địa chỉ cũng thay đổi theo. Nhấn [Chia sẻ tài liệu này] trên thanh công cụ để gửi liên kết của trang đang đọc. Bạn cũng có thể dùng [Quay lại] [Tiến tới] của trình duyệt.

Dạng `?source=` trước đây vẫn mở được như cũ. Sau khi mở, địa chỉ sẽ được chuyển sang dạng mới.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Lưu ý**
>
> - Khi chưa đăng nhập, giới hạn sử dụng GitHub API (60 lần mỗi giờ) sẽ được áp dụng. Với kho lưu trữ có nhiều tài liệu hoặc khi đọc nhiều lần, hãy [Đăng nhập bằng GitHub].
> - Tên nhánh có chứa `/` (như `feature/xxx`) có thể chỉ định bằng `?ref=` trong dạng địa chỉ ở trên. Không thể viết tên nhánh này bằng dạng `?source=`.
> - Tài liệu được tải bằng quyền GitHub của người xem. Người không có quyền đọc sẽ không thấy tài liệu.

## Mở tài liệu từ thư mục trên máy

Nhấn [Mở tài liệu] trên thanh công cụ, rồi chọn một thư mục trên thiết bị qua [Mở tài liệu từ thư mục trên máy] ở cột bên trái. Tệp được xử lý bên trong trình duyệt và không bị gửi ra bên ngoài. Tính năng này dùng được trên các trình duyệt hỗ trợ chọn thư mục (Chrome, Edge, v.v.).

## Chủ đề liên quan

- [Xem kho lưu trữ riêng tư](private-repository.md)
- [Không mở được hoặc không đăng nhập được trên phiên bản Web](../07-troubleshooting/web.md)
