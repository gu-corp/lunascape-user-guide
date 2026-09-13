# Đọc bằng ngôn ngữ khác

Tài liệu nào có bản dịch thì bạn có thể đổi ngôn ngữ để đọc từ menu ngôn ngữ (hình quả địa cầu) trên thanh công cụ.

## Chuyển đổi ngôn ngữ

1. Nhấn menu ngôn ngữ trên thanh công cụ.
   Menu hiển thị ngôn ngữ của trang đang xem và căn cứ xác định ngôn ngữ đó (đường dẫn của bản dịch, tự động phát hiện, hoặc ngôn ngữ mặc định của dự án).
2. Chọn ngôn ngữ bạn muốn đọc.
   Bản dịch của cùng tài liệu đó sẽ mở ra. Ngôn ngữ đã chọn được ghi nhớ; tài liệu bạn mở lần sau cũng hiển thị bằng ngôn ngữ đó nếu có bản dịch.

Danh sách ngôn ngữ cho biết tài liệu này có bản dịch sang ngôn ngữ đó hay không.

| Hiển thị | Ý nghĩa |
|---|---|
| Đã dịch | Bản dịch đã có và có thể mở được |
| Chưa dịch | Ngôn ngữ này được dự án hỗ trợ, nhưng tài liệu này chưa có bản dịch |
| Cần cập nhật | Bản dịch đã có, nhưng tài liệu gốc đã thay đổi sau khi dịch |

> **Lưu ý**
>
> - Thao tác chọn ngôn ngữ chỉ mở bản dịch đã có sẵn. Thao tác này không tạo bản dịch và cũng không tạo tệp. Để tạo bản dịch, hãy dùng [Tạo và quản lý bản dịch…] trong cùng menu đó.
> - Khi ngôn ngữ của trang đang xem được xác định là khác với ngôn ngữ mặc định của dự án, một cảnh báo sẽ hiện ra. Cấu hình không bao giờ bị ghi đè.

## Ngôn ngữ hiển thị đầu tiên

Khi bạn mở một tài liệu, ngôn ngữ hiển thị đầu tiên được quyết định theo thứ tự sau.

1. Ngôn ngữ mà chính bạn đã chọn trước đó tại thư mục gốc tài liệu này. Lựa chọn của bạn được lưu lại (ngay cả khi bạn chọn ngôn ngữ mặc định, đó cũng được lưu như một lựa chọn).
2. Ngôn ngữ hiển thị của VS Code (với bản trình duyệt Web là thiết lập ngôn ngữ của trình duyệt). Ngôn ngữ được hỗ trợ nào trùng khớp sẽ được chọn tự động. Ngôn ngữ có kèm vùng (như `en-US`) cũng khớp với ngôn ngữ cơ sở (`en`).
3. Ngôn ngữ dự phòng của dự án (`fallbackLocale` trong `lunascape-docs.json`).
4. Ngôn ngữ mặc định của dự án.

> **Gợi ý**
>
> - Khi ngôn ngữ được chọn tự động, ngôn ngữ hiện tại trong menu ngôn ngữ sẽ hiển thị nhãn «Tự động chọn». Đưa con trỏ lên nhãn đó để xem lý do.
> - `fallbackLocale` là ngôn ngữ hiển thị cho những độc giả có môi trường sử dụng ngôn ngữ không khớp với bất kỳ ngôn ngữ nào được hỗ trợ. Với một dự án có bản gốc là tiếng Nhật và có bản tiếng Anh, nếu đặt `"en"` thì độc giả ở môi trường tiếng Tây Ban Nha chẳng hạn sẽ được mở bản tiếng Anh. Khi không đặt, ngôn ngữ mặc định sẽ được dùng.

## Nơi đặt bản dịch

Tài liệu bằng ngôn ngữ mặc định vẫn để nguyên chỗ cũ, còn bản dịch được đặt trong **`i18n/<ngôn ngữ>/` thuộc cùng thư mục**, với cùng tên tệp.

```text
docs/
  README.md                  ← ngôn ngữ mặc định (ví dụ: tiếng Nhật)
  i18n/en/README.md          ← bản tiếng Anh của tài liệu đó
  guide/
    setup.md
    i18n/en/setup.md         ← bản tiếng Anh của tài liệu đó
```

> **Lưu ý**
>
> - Cách dựng lại cấu trúc thư mục bên dưới `i18n/` (`i18n/en/guide/setup.md`) sẽ không được nhận diện. Thư mục `i18n/` luôn phải nằm cùng thư mục với tài liệu mà nó dịch.
> - Bản dịch chỉ được tìm ở duy nhất một nơi này. Nếu bạn đặt thêm bản dịch của cùng tài liệu đó vào `i18n/` của thư mục cha, sẽ không có chuyện «bên nào được ưu tiên»: bản ở thư mục cha trở thành tệp mồ côi, không xuất hiện trong menu ngôn ngữ lẫn trong sổ quản lý (và cũng không bị xóa tự động). Đừng đặt cùng một bản dịch ở hai nơi.

## Khi đọc bằng bản trình duyệt Web

Bản trình duyệt Web cũng chuyển đổi ngôn ngữ theo cách tương tự nếu có bản dịch. Khi bạn muốn đọc bằng ngôn ngữ chưa có bản dịch, có thể dùng chức năng dịch trang của trình duyệt. Mã nguồn, công thức toán và sơ đồ được loại khỏi phạm vi dịch.

## Chủ đề liên quan

- [Giao việc cho AI](../05-ai/README.md)
- [Những việc có thể giao](../05-ai/tasks.md)
- [Thay đổi cài đặt hiển thị](../02-reading/display-settings.md)
