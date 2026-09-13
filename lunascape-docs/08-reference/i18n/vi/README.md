# Thông số kỹ thuật chính

## Môi trường hoạt động

| Môi trường | Yêu cầu |
|---|---|
| Tiện ích mở rộng VS Code | VS Code 1.90 trở lên. Các tính năng có ghi tệp cần Không gian làm việc đáng tin cậy |
| Bản trình duyệt Web | Chrome, Edge, Safari, Firefox phiên bản gần đây. Để xem thư mục cục bộ, cần trình duyệt hỗ trợ chọn thư mục (File System Access API) |
| Tiện ích mở rộng Chromium | Manifest V3. Không yêu cầu quyền truy cập máy chủ |

## Tài liệu được hỗ trợ

| Mục | Nội dung |
|---|---|
| Tệp | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (bảng, danh sách công việc, khối mã, gạch ngang), hình ảnh cục bộ, YAML front matter |
| MDX | Chỉ hiển thị các thành phần được cho phép. Không thực thi bất kỳ tập lệnh tùy ý nào |
| HTML | Được làm sạch bằng DOMPurify 3.4.14 trước khi hiển thị |

## Sơ đồ và công thức toán

| Loại | Tên ngôn ngữ | Ghi chú |
|---|---|---|
| Công thức toán | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Chỉ dữ liệu nhúng. Không dùng được URL bên ngoài và dấu hình ảnh |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Chỉ JSON nghiêm ngặt |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Bản phân phối hiển thị mã nguồn ở dạng thu gọn. Giới hạn đầu vào 64 KiB, 15 giây, SVG 2 MiB |
| Penrose (thử nghiệm) | `penrose` | Chỉ cấu hình sẵn `set-theory` |

## Giá trị giới hạn

| Mục | Giá trị |
|---|---|
| Kết quả kết xuất của Mẫu | 4 MiB |
| Ngữ cảnh tham chiếu của Bản dịch | Mặc định 49.152 ký tự, tối đa 1.048.576 ký tự |
| Số tài liệu cho mỗi lần dịch hàng loạt | 1.000 tài liệu |
| Chiều rộng tùy chọn của hình ảnh | 16–4096px |

## Tệp

| Tệp | Vai trò | Quản lý bằng Git |
|---|---|---|
| `lunascape-docs.json` | Cài đặt của Thư mục gốc tài liệu | Có |
| `docs-lint.config.json` | Cài đặt của Quy tắc kiểm tra | Có |
| `.lunascape-docs/translation-freshness.json` | Bản ghi độ mới của Bản dịch (chỉ gồm đường dẫn, ngôn ngữ, mã băm và thời điểm) | Có |
| Cài đặt VS Code và trạng thái không gian làm việc | Cài đặt hiển thị cá nhân, lựa chọn nhà cung cấp, trạng thái đóng/mở của INDEX | Không |

## Standard Pack đi kèm

`builtin:gu-corp-software` — hồ sơ: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Xem thêm

- [Danh sách cài đặt VS Code](settings.md)
- [Bảo mật và ranh giới lưu trữ](security.md)
