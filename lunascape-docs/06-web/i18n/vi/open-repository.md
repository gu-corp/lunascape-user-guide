# Mở kho lưu trữ GitHub

Trên bản web và trong Lunascape, bạn có thể mở và đọc trực tiếp kho lưu trữ GitHub mà không cần nhân bản. Với kho lưu trữ công khai, bạn không cần đăng nhập.

## Mở từ màn hình

1. Nhấn [Mở tài liệu] (biểu tượng thư mục) trên thanh công cụ. Màn hình “Mở tài liệu” mở ra.
2. Ở cột bên trái, chọn nơi cần mở.

   | Nơi | Nội dung hiển thị |
   |---|---|
   | Tất cả | Tất cả các mục bên dưới. Các mục mở gần đây được xếp lên đầu |
   | Mở gần đây | Các kho lưu trữ và thư mục bạn đã mở |
   | Đề xuất | Các hướng dẫn sử dụng mà trang giới thiệu |
   | Kho lưu trữ GitHub | Các kho lưu trữ bạn có thể đọc, khi bạn đã đăng nhập bằng GitHub |
   | Máy tính này | Các thư mục trên thiết bị này. Trong Lunascape, các kho lưu trữ đã nhân bản cũng được liệt kê ở đây |

3. Nhấn [Mở] ở hàng muốn mở. Nhập vào ô [Lọc theo tên tài liệu hoặc tên kho lưu trữ] ở phía trên để lọc các hàng.

Với kho lưu trữ không có trong danh sách, hãy chỉ định qua [Nhập owner/repo để mở] ở cột bên trái.

> **Mẹo**
>
> - Các kho lưu trữ GitHub hiển thị trong danh sách là những kho đã cài GitHub App “Lunascape Docs” và bạn có quyền đọc. Nếu không thấy kho lưu trữ, hãy nhờ chủ sở hữu kho lưu trữ thêm App.

## Xác nhận vị trí của tài liệu

Biểu tượng nhỏ ở phía bên trái thanh công cụ (chip vị trí) cho biết tài liệu bạn đang đọc nằm ở đâu.

| Biểu tượng | Vị trí |
|---|---|
| Biểu tượng GitHub | Đang đọc từ GitHub. Tài liệu không được lưu trên thiết bị này |
| Máy tính | Thư mục trên thiết bị này do Lunascape quản lý. Tên nhánh Git và số tệp đã thay đổi cũng được hiển thị |
| Thư mục | Thư mục trên thiết bị này |

Nhấn vào biểu tượng để xem vị trí, trạng thái và các thao tác có thể thực hiện từ đó (như [Xem trên GitHub], [Sao chép liên kết]).

## Nhân bản kho lưu trữ trong Lunascape

Trong Lunascape, bạn có thể nhân bản kho lưu trữ GitHub về thiết bị này, rồi chỉnh sửa và commit bằng Git.

- Trên màn hình “Mở tài liệu”, nhấn [Nhân bản] ở hàng của kho lưu trữ.
- Khi đang đọc kho lưu trữ mở từ GitHub, nhấn chip vị trí rồi nhấn [Nhân bản vào máy tính này]. Khi nhân bản xong, cùng tài liệu đó sẽ mở từ bản trên thiết bị này.

Kho lưu trữ đã nhân bản được ghi “Có trên máy tính này” trong danh sách, và [Mở trên máy tính này] được xếp trước.

## Mở bằng URL

Địa chỉ có dạng ghi liền kho lưu trữ và vị trí của tài liệu. Đường dẫn là vị trí bên trong kho lưu trữ, nên có cùng thứ tự với URL của GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Chỉ định | Cách viết |
|---|---|
| Chỉ kho lưu trữ (nhánh mặc định) | `/github/owner/repo` |
| Tài liệu bên trong kho lưu trữ | `/github/owner/repo/docs/01-product/vision.md` |
| Chỉ định nhánh hoặc thẻ | Thêm `?ref=v1.2.0` vào cuối |

Khi chuyển trang, địa chỉ cũng thay đổi theo. Nhấn [Chia sẻ tài liệu này] trên thanh công cụ để gửi liên kết của trang đang đọc. Bạn cũng có thể dùng nút [Quay lại] [Tiến tới] của trình duyệt.

Dạng `?source=` cũ vẫn mở được như trước. Sau khi mở, địa chỉ sẽ được chuyển sang dạng mới.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Lưu ý**
>
> - Khi chưa đăng nhập, sẽ có giới hạn sử dụng GitHub API (60 lần mỗi giờ). Với kho lưu trữ có nhiều tài liệu hoặc khi xem nhiều lần, hãy [Đăng nhập bằng GitHub].
> - Tên nhánh có chứa `/` (như `feature/xxx`) có thể chỉ định bằng `?ref=` trong dạng địa chỉ ở trên. Dạng `?source=` không ghi được các tên nhánh này.
> - Tài liệu được tải bằng quyền GitHub của người xem. Người không có quyền đọc sẽ không thấy tài liệu.

## Mở tài liệu từ thư mục trên máy

Nhấn [Mở tài liệu] trên thanh công cụ, rồi chọn thư mục trên thiết bị qua [Mở tài liệu từ thư mục trên máy] ở cột bên trái. Tệp được xử lý bên trong trình duyệt và không được gửi ra bên ngoài. Tính năng này dùng được trên các trình duyệt hỗ trợ chọn thư mục (Chrome, Edge, v.v.).

## Mục liên quan

- [Xem kho lưu trữ không công khai](private-repository.md)
- [Không mở được hoặc không đăng nhập được bản web](../07-troubleshooting/web.md)
