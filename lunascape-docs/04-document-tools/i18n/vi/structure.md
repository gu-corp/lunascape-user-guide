# Thư mục gốc tài liệu và quy ước tệp

Đây là các quy tắc Lunascape Docs dùng để tìm tài liệu và dựng INDEX. Bản thân hệ thống tệp chính là bản gốc, nên không cần sổ đăng ký hay cấu hình biên dịch nào.

## Thư mục gốc tài liệu

- Thư mục `docs` gần nhất, hoặc thư mục có đặt `lunascape-docs.json`, sẽ trở thành thư mục gốc tài liệu.
- Nếu đặt `lunascape-docs.json`, thư mục không nhất thiết phải mang tên `docs`.
- Khi mở một tệp Markdown không thuộc thư mục gốc tài liệu nào, thư mục chứa tệp đó được hiển thị như một thư mục gốc tài liệu tạm thời.

## Các tệp hiển thị trong INDEX

- Các tệp `.md`, `.markdown` và `.mdx` được hiển thị. Tệp mới luôn xuất hiện, kể cả khi không có front matter hay thông tin điều hướng.
- Các thư mục bắt đầu bằng `.`, `node_modules` và các thư mục chỉ định trong `ignoredDirectories` (mặc định là `99-archive`) không được hiển thị.
- Mọi thứ nằm dưới `i18n/` được xem là bản dịch và không hiển thị riêng trong INDEX.

## Trang bìa của thư mục

- Tệp `README.md` có nội dung (hoặc `index.md` nếu không có README) là trang bìa của thư mục đó. Nhấn vào tên thư mục trong INDEX sẽ mở trang bìa.
- Tệp `README.md` chỉ có front matter mà không có nội dung được xem là "bộ mô tả chỉ dùng để cấu hình" và không hiển thị như một trang. Hãy dùng cách này khi chỉ cần đặt tiêu đề hoặc thứ tự cho thư mục.
- Khi có cả `README.md` và `index.md`, `README.md` được ưu tiên.

## Ngôn ngữ mặc định và bản dịch

- Tài liệu bằng ngôn ngữ mặc định (bản gốc) được giữ nguyên tại chỗ.
- Bản dịch được đặt trong `i18n/<ngôn ngữ>/` cùng thư mục với bản gốc, với cùng tên tệp. Nếu dựng lại cấu trúc thư mục bên dưới `i18n/` thì sẽ không được nhận diện.
- Đó là vị trí duy nhất để phân giải bản dịch. Cùng tệp đó đặt ở nơi khác sẽ là tệp mồ côi, không được xem là bản dịch của bất kỳ tài liệu nào.

```text
docs/
  lunascape-docs.json
  README.md                  ← trang bìa của thư mục gốc (trang bắt đầu)
  i18n/en/README.md          ← bản tiếng Anh của trang đó
  01-product/
    README.md                ← trang bìa của thư mục
    requirements.md
    i18n/en/README.md        ← bản tiếng Anh của hai tài liệu trên
    i18n/en/requirements.md
  99-archive/                ← mặc định bị loại khỏi INDEX
```

## Về `_meta.json`

Tệp `_meta.json` của Nextra không được dùng cho điều hướng. Các tệp hiện có không bị sửa đổi cũng không bị xóa. Trong tương lai, chúng sẽ chỉ được xử lý bằng chức năng nhập/xuất tường minh.

## Xem thêm

- [Thiết lập thông tin điều hướng](navigation-metadata.md)
- [Cấu hình dự án](project-configuration.md)
- [Chuyển thư mục gốc tài liệu](../02-reading/roots.md)
