# Điều chỉnh kích thước ảnh

Ảnh chèn vào tài liệu sẽ tự động vừa với chiều rộng nội dung và chiều cao màn hình. Với ảnh cần hiển thị ở một kích thước nhất định, bạn có thể chỉ định chiều rộng.

## Cách tự động điều chỉnh

- Ảnh Markdown thông thường (`![mô tả](./images/screen.png)`) được thu nhỏ để vừa với chiều rộng nội dung. Ảnh không bao giờ được phóng to hơn kích thước gốc.
- Ảnh chụp màn hình dạng dọc được giới hạn ở 72% chiều cao màn hình hoặc 720px, tùy giá trị nào nhỏ hơn.

## Chỉ định chiều rộng trong màn hình chỉnh sửa

1. Nhấn [Chỉnh sửa] và chọn ảnh trong chế độ hiển thị trực quan.
2. Chọn chiều rộng từ [Kích thước ảnh] trên thanh công cụ.
3. Nhấn [Lưu].

| Tùy chọn | Chiều rộng |
|---|---|
| [Tự động] | Không chỉ định (tự động điều chỉnh) |
| [Nhỏ (360px)] | 360px |
| [Vừa (560px)] | 560px |
| [Lớn (760px)] | 760px |
| [Chiều rộng nội dung (920px)] | 920px |
| [Tùy chọn…] | Số nguyên bất kỳ từ 16 đến 4096px |

## Chỉ định chiều rộng bằng Markdown

Hãy đặt giá trị số cho thuộc tính `width` của thẻ HTML `img`. Cách viết này cũng hiển thị như vậy trên GitHub và trong MDX.

```html
<img src="./images/screen.png" alt="Màn hình cài đặt" width="360" />
```

> **Lưu ý**
>
> - `width` chỉ nhận giá trị số, không kèm `px` hay `%`. Dù bạn chỉ định giá trị lớn hơn chiều rộng nội dung, ảnh vẫn hiển thị vừa với chiều rộng nội dung.
> - Đường dẫn ảnh được tính tương đối so với tài liệu. Ảnh nằm ngoài Thư mục gốc tài liệu sẽ không hiển thị.

## Xem thêm

- [Chỉnh sửa tài liệu](README.md)
- [Sơ đồ, công thức toán hoặc ảnh không hiển thị](../07-troubleshooting/rendering.md)
