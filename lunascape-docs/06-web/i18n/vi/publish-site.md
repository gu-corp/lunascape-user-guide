# Xuất bản tài liệu của bạn lên Web

Bạn có thể xuất bản tài liệu trong kho lưu trữ của mình thành một trang web trên GitHub Pages hoặc bất kỳ dịch vụ lưu trữ tĩnh nào. Có hai cách. Các bước này dành cho nhà phát triển có thể clone kho lưu trữ Lunascape Docs và dùng được `npm`.

## Cách 1: Đặt hai tệp của trình xem

Chỉ triển khai phần thân trình xem (`index.html` và `lsdoc.js`) và để nó tải tài liệu từ GitHub. Bản thân tài liệu không nằm trong trang web, nên cách này an toàn với cả kho lưu trữ riêng tư (người đọc đăng nhập bằng GitHub).

1. Chạy lệnh sau trong kho lưu trữ Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` và `lsdoc.js` được tạo ra trong `dist/viewer/`.
2. Đặt hai tệp đó vào `docs/` của kho lưu trữ bạn muốn xuất bản.
3. Bật GitHub Pages.

Thư mục gốc tài liệu được hiển thị sẽ được xác định theo thứ tự sau.

1. Cài đặt `source` trong `index.html`
2. `repository` ghi trong `lunascape-docs.json` ở cùng thư mục
3. Suy đoán từ URL `*.github.io` và cấu trúc nhánh

## Cách 2: Xuất một trang tĩnh có kèm tài liệu

Xuất trình xem cùng với các tệp tài liệu và lưu trữ kết quả nguyên trạng.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Kết quả gồm toàn bộ trình xem, các tài liệu dưới `docs/`, tệp danh mục `lunascape-docs-manifest.json` và `.nojekyll`. Đặt thư mục kết quả lên S3 hoặc GitHub Pages là xuất bản được. Về ví dụ tự động xuất bản bằng GitHub Actions, xem `examples/workflows/publish-docs-pages.yml` trong kho lưu trữ.

> **Lưu ý**
>
> - **Đừng xuất tài liệu của kho lưu trữ riêng tư rồi đặt lên GitHub Pages.** GitHub Pages ngoài Enterprise Cloud thì ai cũng xem được. Nếu cần xuất bản hạn chế, hãy dùng cách 1 và để người đọc đăng nhập bằng GitHub.
> - Mở trực tiếp `index.html` bằng `file://` sẽ không chạy, vì trình duyệt cấm tải các tệp lân cận và cấm thực thi ES module theo cách đó. Khi muốn kiểm tra tại chỗ, hãy dùng bản VS Code hoặc một máy chủ HTTP.
> - Các thư viện vẽ của TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob và Penrose được tải khi hiển thị. Với trang đã xuất, hãy đặt kèm cả thư mục `vendor/`.

## Mục liên quan

- [Những gì bản Web làm được](README.md)
- [Xem kho lưu trữ riêng tư](private-repository.md)
