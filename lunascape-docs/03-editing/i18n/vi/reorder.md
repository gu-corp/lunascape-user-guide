# Thay đổi thứ tự tài liệu

Thứ tự hiển thị trong INDEX có thể thay đổi bằng cách kéo và thả hoặc bằng bàn phím. Thứ tự đã thay đổi được lưu vào front matter của tài liệu dưới dạng `navigation.order`.

## Sắp xếp bằng cách kéo và thả

1. Kéo một tài liệu hoặc thư mục trong INDEX.
2. Thả vào trước hoặc sau một mục cùng cấp, hoặc thả lên một thư mục.
   Trong cùng một cấp, thứ tự sẽ thay đổi. Khi thả vào một thư mục khác, mục đó sẽ được chuyển vào thư mục ấy.

## Sắp xếp bằng bàn phím hoặc menu

- Đặt tiêu điểm vào một mục trong INDEX rồi nhấn `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Chọn [Di chuyển lên một bậc] / [Di chuyển xuống một bậc] trong menu của mục.

## Nội dung được lưu

- Khi sắp xếp trong cùng một cấp, `navigation.order` trong front matter của bản gốc sẽ được cập nhật. Với thư mục, giá trị này được ghi vào `README.md` của thư mục đó. Nếu thư mục chưa có `README.md`, một `README.md` chỉ gồm front matter sẽ được tạo.
- Khi di chuyển sang thư mục khác, bản gốc và các bản dịch tương ứng được di chuyển cùng nhau. Trước khi di chuyển, một xác nhận về ảnh hưởng đến các liên kết tương đối sẽ hiện ra.
- Không thực hiện thao tác staging hay commit của Git.

> **Lưu ý**
>
> - Không thể sắp xếp khi đang lọc, khi đang chỉnh sửa tài liệu, và trong không gian làm việc không đáng tin cậy.
> - Khi hiện thông báo "INDEX đã được cập nhật", đó là lúc vừa có một thay đổi khác được áp dụng. Hãy thực hiện lại thao tác.
> - Trang bắt đầu không thể di chuyển sang thư mục khác.

> **Gợi ý**
>
> Nếu đặt `navigation.order` theo bước 100 như 100, 200, 300 thì sau này dễ chèn thêm vào giữa. Chi tiết xem [Thiết lập thông tin điều hướng](../04-document-tools/navigation-metadata.md).

## Xem thêm

- [Tạo và sắp xếp tài liệu và thư mục](organize.md)
- [Thiết lập thông tin điều hướng](../04-document-tools/navigation-metadata.md)
