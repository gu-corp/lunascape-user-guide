# Thiết lập thông tin điều hướng

Tên và thứ tự hiển thị trong INDEX được ghi trong YAML front matter của từng tài liệu. Nếu không ghi, tài liệu vẫn được hiển thị và sử dụng tiêu đề (H1) cùng thứ tự theo tên tệp.

## Tên và thứ tự của tài liệu

Ghi như sau ở đầu tài liệu.

```yaml
---
navigation:
  title: Bắt đầu
  order: 200
---
```

| Mục | Nội dung |
|---|---|
| `navigation.title` | Tên hiển thị trong INDEX. Nếu bỏ qua, H1 được dùng; nếu cũng không có thì dùng tên tệp |
| `navigation.order` | Số nguyên quyết định thứ tự. Sắp xếp từ nhỏ đến lớn. Nếu bỏ qua, thứ tự mặc định ổn định (theo tên tệp) được áp dụng |

> **Mẹo**
>
> - Hãy đặt `order` theo bước 100 như 100, 200, 300 để sau này có thể chèn 150 vào giữa.
> - Tài liệu không bị ẩn ngay cả khi `order` bị thiếu, không hợp lệ hoặc trùng lặp.
> - Khi bạn sắp xếp lại trong INDEX, `navigation.order` được ghi tự động. Bạn không cần ghi bằng tay.

## Tên và thứ tự của thư mục

Tên và thứ tự của thư mục thuộc về front matter trong `README.md` của thư mục đó (nếu không có thì `index.md`). Trang bìa không cần có nội dung.

```yaml
---
navigation:
  title: Lập kế hoạch sản phẩm
  order: 100
---
```

Thư mục không có trang bìa sẽ hiển thị theo tên thư mục và thứ tự mặc định. Khi việc đổi tiêu đề hoặc sắp xếp lại trong INDEX cần đến, một `README.md` chỉ có front matter sẽ được tạo. Chỉ xem thì không bao giờ tạo tệp.

## Cách xử lý ở bản dịch

- Thứ tự và vai trò của thư mục (trang bìa hay chỉ dùng để cấu hình) chỉ do tài liệu ở ngôn ngữ mặc định quyết định.
- Bản dịch chỉ có thể ghi đè `navigation.title`. Khi bản gốc có nội dung, H1 của bản dịch cũng được dùng làm tên.
- Chỉ có bản dịch thì trang không tăng thêm.

## Sắp xếp và thu gọn các mục con

Ở trang bìa của thư mục, `navigation.children.sort` và `navigation.children.defaultCollapsed` được định nghĩa để chỉ định cách sắp xếp các mục con ngay bên dưới và trạng thái thu gọn ban đầu. Việc đọc và chỉnh sửa chúng trong VS Code sẽ được hỗ trợ trong thời gian tới.

## Mục liên quan

- [Thay đổi thứ tự tài liệu](../03-editing/reorder.md)
- [Thư mục gốc tài liệu và quy ước tệp](structure.md)
