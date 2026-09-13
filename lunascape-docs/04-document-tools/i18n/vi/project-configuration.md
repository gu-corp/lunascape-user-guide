# Cấu hình dự án

`lunascape-docs.json` nằm ngay dưới thư mục gốc tài liệu là phần cài đặt của thư mục gốc tài liệu, được chia sẻ trong nhóm. Tệp này được quản lý bằng Git.

## Tạo và chỉnh sửa tệp cài đặt

- Trên thanh công cụ, nhấn [Công cụ tài liệu] → thẻ [Kiểm tra] → [Nguồn quy tắc và cài đặt tài liệu] → [Chỉnh sửa cài đặt tài liệu] để mở tệp trong VS Code. Nếu chưa có tệp, tệp ban đầu sẽ được tạo vào lúc này.
- Tên tệp `lunascape-docs.json` được tự động liên kết với JSON Schema đi kèm, nên bạn sẽ thấy gợi ý nhập liệu và phần mô tả cho từng mục. Không cần viết `$schema`.

## Ví dụ cài đặt

```json
{
  "id": "product-docs",
  "title": "Tài liệu sản phẩm",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Giải thích các mục

| Mục | Nội dung | Mặc định |
|---|---|---|
| `id` | Khóa dùng để lưu cài đặt hiển thị của từng người dùng. Khi muốn giữ nguyên cài đặt dù thư mục bị di chuyển, hãy đặt một ID cố định | Đường dẫn của thư mục |
| `title` | Tên hiển thị ở ngoài cùng bên trái thanh công cụ và trong danh sách thư mục gốc tài liệu. Tên này không đổi khi chuyển ngôn ngữ hiển thị | Tiêu đề của README/index ở thư mục gốc, nếu không có thì là tên thư mục |
| `indexTitle` | Tiêu đề của INDEX | `INDEX` |
| `startPage` | Tài liệu được mở đầu tiên (đường dẫn tương đối tính từ thư mục gốc tài liệu) | `README.md` |
| `appearance` | Phối màu. `light` (luôn sáng) hoặc `auto` (theo chủ đề của VS Code) | `light` |
| `defaultLocale` | Ngôn ngữ mặc định (ngôn ngữ của bản gốc). Chỉ định bằng thẻ ngôn ngữ BCP 47 (`ja`, `en`, `zh-Hant`...). Đây là nguồn để dịch | Chưa đặt (suy đoán từ nội dung để hiển thị) |
| `fallbackLocale` | Ngôn ngữ được hiển thị đầu tiên cho người đọc có môi trường không khớp với bất kỳ ngôn ngữ được hỗ trợ nào. Hãy chỉ định một ngôn ngữ có trong `locales` | Chưa đặt (dùng `defaultLocale`) |
| `locales` | Danh sách ngôn ngữ được hỗ trợ, bao gồm cả `defaultLocale`. Đây là các mục trong trình đơn ngôn ngữ và là các ngôn ngữ đích khi dịch | Chỉ `defaultLocale` |
| `ignoredDirectories` | Tên các thư mục bị loại khỏi INDEX, tìm kiếm và kiểm tra. Khi được chỉ định, giá trị này thay thế giá trị mặc định | `["99-archive"]` |
| `tree` | Giá trị mặc định cho cách hiển thị INDEX. Người dùng có thể ghi đè bằng cài đặt hiển thị | Như ví dụ ở trên |
| `editor.defaultMode` | Chế độ hiển thị khi chỉnh sửa, dùng cho đến khi người dùng tự chuyển. `visual` hoặc `source` | `visual` |
| `editor.showEditButton` | Có hiển thị [Chỉnh sửa] ở góc dưới bên phải nội dung hay không | `true` |
| `documentStandards.pack` | Standard Pack dùng cho việc kiểm tra tài liệu và mẫu. `builtin:<tên>`, hoặc đường dẫn tương đối tính từ thư mục gốc tài liệu | Không có |
| `documentStandards.profile` | Tên hồ sơ do Pack định nghĩa | Không có |
| `translation.enabled` | Bật việc tạo bản dịch đề xuất và dịch hàng loạt | `true` |
| `translation.contextFiles` | Các tệp Markdown bản gốc (đường dẫn tương đối tính từ thư mục gốc tài liệu) được chuyển sang khi dịch để tham khảo thuật ngữ và văn phong | `[]` |
| `translation.maxContextCharacters` | Giới hạn tổng số ký tự của các tài liệu tham khảo (tối đa 1048576) | `49152` |
| `description` | Mô tả một dòng về bộ tài liệu. Được hiển thị trên thẻ ở trang chủ của kho lưu trữ. Giống `title`, có thể viết dưới dạng chuỗi hoặc đối tượng theo từng ngôn ngữ | Không có |

## Cho biết tài liệu nằm ở đâu trong kho lưu trữ

`lunascape-docs.json` đặt ngay dưới kho lưu trữ có thể chứa **bản đồ của kho lưu trữ** thay vì cài đặt của chính thư mục đó. Khi bạn viết một trong 3 mục sau, tệp sẽ trở thành bản đồ và bản thân thư mục đó không còn là thư mục gốc tài liệu.

| Mục | Nội dung | Mặc định |
|---|---|---|
| `defaultFolder` | Thư mục chứa tài liệu (đường dẫn tương đối tính từ thư mục ngay dưới kho lưu trữ). Thư mục được trỏ tới không cần tệp cài đặt riêng | Không có (dùng `docs`) |
| `roots` | Danh sách các bộ tài liệu khi có nhiều bộ (đường dẫn tương đối tính từ thư mục ngay dưới kho lưu trữ, theo thứ tự hiển thị). Khi đó, thư mục ngay dưới kho lưu trữ trở thành trang chủ | Không có |
| `excludes` | Các thư mục bị loại khỏi việc tìm thư mục gốc tài liệu (đường dẫn tương đối tính từ thư mục ngay dưới kho lưu trữ). Được cộng thêm vào các mục loại trừ mặc định như `node_modules` | `[]` |
| `home.cards` | Có hiển thị thẻ của các bộ tài liệu bên dưới README của trang chủ hay không. Đặt `false` khi bạn tự viết liên kết trong README | `true` |

Thư mục gốc tài liệu được xác định theo thứ tự sau. Xét lần lượt từ trên xuống, mục tìm thấy đầu tiên sẽ được dùng.

1. Thư mục bạn chỉ định bằng cài đặt hoặc bằng lệnh
2. Nơi mà `defaultFolder` hoặc `roots` trong `lunascape-docs.json` ngay dưới kho lưu trữ trỏ tới
3. Thư mục có `lunascape-docs.json` (nếu có từ hai thư mục như vậy trở lên dưới cùng một thư mục cha, thì thư mục cha đó là trang chủ)
4. Thư mục `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Chính thư mục ngay dưới kho lưu trữ

> **Mẹo**
>
> Nếu không viết gì thì mục 4 sẽ hoạt động, nên một kho lưu trữ thông thường chỉ có một `docs/` vẫn hoạt động như trước. Chỉ khi muốn đặt tên thư mục là `manual`, bạn mới cần viết `defaultFolder`.

### Ví dụ về bản đồ

```json
{
  "title": "Trợ giúp Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Thứ tự ưu tiên của cài đặt

Các mục liên quan đến hiển thị được ưu tiên theo thứ tự sau.

1. Cài đặt hiển thị của người dùng (bảng [Cài đặt hiển thị])
2. Cài đặt của VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Giá trị mặc định của sản phẩm

Riêng ngôn ngữ (`defaultLocale`, `fallbackLocale`, `locales`) là ngoại lệ: `lunascape-docs.json` mới là bản gốc. Bạn không thể ghi đè ngôn ngữ của dự án bằng cài đặt cá nhân của VS Code.

> **Lưu ý**
>
> Bạn cũng có thể chỉ định Standard Pack trong `docs-lint.config.json` bằng mục `standard`. Khi cả hai nơi cùng có, `docs-lint.config.json` được ưu tiên.

## Chủ đề liên quan

- [Thay đổi quy tắc kiểm tra](rules.md)
- [Thay đổi cài đặt hiển thị](../02-reading/display-settings.md)
- [Danh sách cài đặt VS Code](../08-reference/settings.md)
