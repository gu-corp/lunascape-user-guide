# Cài đặt tiện ích mở rộng

Tiện ích mở rộng của VS Code "Lunascape Docs Pro" được phân phối dưới dạng tệp VSIX. Tiện ích này miễn phí; chữ "Pro" cho biết đây là phiên bản có khả năng giao việc cho AI và tự cập nhật.

## Môi trường hoạt động

- VS Code 1.90 trở lên
- Các tính năng ghi tệp — tạo tài liệu, sắp xếp từ INDEX, lưu cài đặt kiểm tra, dịch — chỉ dùng được trong không gian làm việc mà bạn đã đánh dấu là "đáng tin cậy" trong VS Code.

## Cài đặt

1. Lấy tệp VSIX. Liên kết này luôn trỏ đến phiên bản mới nhất.

   [Tải xuống lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Mở khung xem tiện ích mở rộng của VS Code (`⇧⌘X` / `Ctrl+Shift+X`).
3. Từ menu `…` ở góc trên bên phải, chọn [Cài đặt từ VSIX...] rồi chỉ định tệp đã tải về.

### Cài bằng lệnh

Bạn cũng có thể làm gọn trong một dòng từ terminal. Lệnh sẽ tải về rồi cài đặt liền mạch.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Lưu ý**
> Nếu không tìm thấy `code`, hãy chạy [Shell Command: Install 'code' command in PATH] từ bảng lệnh (`⇧⌘P` / `Ctrl+Shift+P`).

## Cập nhật

Khi có phiên bản mới được phát hành, tiện ích mở rộng sẽ tự tải về và cài đặt. Khi VS Code nhắc tải lại cửa sổ, phiên bản mới sẽ được áp dụng tại thời điểm đó. Cài đặt và tài liệu của bạn vẫn được giữ nguyên.

Việc kiểm tra diễn ra mỗi ngày một lần. Nếu muốn kiểm tra ngay, hãy chạy [Lunascape Docs: Kiểm tra bản cập nhật] từ bảng lệnh (`⇧⌘P` / `Ctrl+Shift+P`).

Bạn có thể thay đổi cách hoạt động bằng cài đặt `lunascapeDocEditor.update.check`.

| Cài đặt | Cách hoạt động |
|---|---|
| Cài đặt khi có phiên bản mới được phát hành | Mặc định |
| Thông báo cho tôi, tùy mỗi lần tôi quyết định | Một thông báo hiện ra, và chỉ thay đổi khi bạn nhấn [Cập nhật] |
| Không kiểm tra | Không làm gì cả |

### Khi không cập nhật được

Nếu xuất hiện thông báo "Không thể lấy bản cập nhật: No Servers", nghĩa là phiên bản đang cài là 0.22.18 hoặc cũ hơn. Tính năng cập nhật của phiên bản đó luôn thất bại ở bước ngay sau khi tải về, nên nó không thể tự cập nhật lên bản mới. Hãy cài lại thủ công một lần theo các bước ở trên. Từ đó trở đi, tiện ích sẽ tự cập nhật.

## Kiểm tra phiên bản

Mở "Lunascape Docs Pro" trong khung xem tiện ích mở rộng để thấy phiên bản đã cài. Bạn sẽ cần thông tin này khi báo cáo sự cố.

## Xem thêm

- [Tạo tài liệu đầu tiên](first-documents.md)
- [Báo cáo sự cố](../07-troubleshooting/report.md)
