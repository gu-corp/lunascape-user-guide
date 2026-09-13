# Viết công thức toán

Công thức toán được viết theo ký hiệu TeX và được kết xuất trên thiết bị của bạn bằng KaTeX. Không sử dụng mạng.

## Cách viết

| Loại | Ký hiệu phân cách | Ví dụ |
|---|---|---|
| Công thức nội dòng (trong câu) | `$...$` hoặc `\(...\)` | `Quan hệ giữa khối lượng và năng lượng được biểu diễn bằng $E = mc^2$.` |
| Công thức hiển thị (trên dòng riêng) | `$$...$$` hoặc `\[...\]` | Xem bên dưới |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Không cần khoảng trắng trước và sau ký hiệu phân cách. Công thức nằm sát chữ tiếng Nhật, như `値は$V=-H$である`, vẫn được nhận diện.
- Ký tự `$` bên trong mã nội dòng hoặc khối mã không được xem là công thức toán mà hiển thị nguyên văn.
- Cách viết giống số tiền như `$5 and $10` không được xem là công thức toán.

## Chỉnh sửa

Ở chế độ hiển thị trực quan, công thức toán được hiển thị dưới dạng đã kết xuất. Để thay đổi nội dung, hãy nhấn [Markdown] trong màn hình chỉnh sửa và sửa mã nguồn. Khi lưu từ chế độ hiển thị trực quan, mã nguồn TeX và dạng ký hiệu phân cách ban đầu (`$` hay `\(`) vẫn được giữ nguyên.

> **Lưu ý**
>
> - Vì lý do an toàn, KaTeX hoạt động với `trust: false` và có giới hạn về kích thước (`maxSize: 50`) cũng như số lần khai triển macro (`maxExpand: 1000`). Công thức vượt quá các giới hạn này sẽ không được kết xuất.
> - Trong tài liệu đã có, `tikzpicture` được viết bên trong `$$...$$` hoặc `\[...\]` sẽ được nhận diện là sơ đồ TikZ chứ không phải công thức toán.

## Chủ đề liên quan

- [Viết sơ đồ và biểu đồ](diagrams.md)
- [Sơ đồ, công thức toán hoặc hình ảnh không hiển thị](../07-troubleshooting/rendering.md)
