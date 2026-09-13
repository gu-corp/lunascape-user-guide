# Thay đổi quy tắc kiểm tra

Bạn có thể thay đổi mức thông báo (lỗi, cảnh báo, thông tin) của từng mục kiểm tra, hoặc không dùng mục đó nữa. Các thay đổi được lưu vào `docs-lint.config.json` trong thư mục gốc tài liệu và được chia sẻ với cả nhóm.

## Thay đổi mức thông báo

1. Nhấn [Công cụ tài liệu] trên thanh công cụ, rồi mở thẻ [Kiểm tra].
2. Nhấn [Xem và thay đổi quy tắc].
   Danh sách các mục kiểm tra sẽ mở ra ngay trong thẻ đó. Mỗi mục hiển thị mục đích của nó và nguồn của cài đặt hiện tại (Project, Profile, Pack, Default).
3. Chọn mức thông báo cho mục bạn muốn thay đổi.
4. Nhấn [Lưu và kiểm tra lại].
   Cài đặt được lưu và toàn bộ thư mục gốc tài liệu được kiểm tra lại với cài đặt mới.

| Lựa chọn | Ý nghĩa |
|---|---|
| [Cài đặt chuẩn (…)] | Xóa phần ghi đè và trở về cài đặt chuẩn, được xác định lần lượt theo hồ sơ, Standard Pack rồi giá trị mặc định |
| [Không dùng] | Không kiểm tra mục này |
| [Thông tin] / [Cảnh báo] / [Lỗi] | Báo cáo ở mức thông báo này |

> **Lưu ý**
>
> - Việc lưu đòi hỏi một không gian làm việc đáng tin cậy.
> - Chỉ mức thông báo của từng mục được lưu. Các tùy chọn riêng của mỗi mục vẫn được giữ nguyên. Bản thân Standard Pack và hồ sơ không được thay đổi ở màn hình này.
> - Nếu `docs-lint.config.json` bị thay đổi từ bên ngoài ngay trước khi lưu, việc lưu sẽ bị hủy. Hãy tải lại trạng thái mới nhất rồi thử lại.
> - Nếu chưa có `docs-lint.config.json`, tệp này sẽ được tạo khi bạn lưu.

## Chỉnh sửa trực tiếp tệp cài đặt

- Nhấn [Mở cài đặt chi tiết] để mở `docs-lint.config.json` trong VS Code.
- Mở [Nguồn quy tắc và cài đặt tài liệu] rồi nhấn [Chỉnh sửa cài đặt tài liệu] để mở `lunascape-docs.json` trong VS Code. Standard Pack và hồ sơ được chọn tại đây.

Cả hai tệp đều có gợi ý nhập liệu và phần mô tả nhờ JSON Schema đi kèm phần mở rộng.

## Standard Pack và hồ sơ

Standard Pack là một chuẩn tài liệu, tập hợp các loại tài liệu cần có, cách phân chương, thuật ngữ và mẫu. Bạn chọn nó bằng `documentStandards` trong `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Pack đi kèm `builtin:gu-corp-software` có các hồ sơ `base`, `web-application`, `api-service`, `regulated-financial-product` và `smart-contract`.

## Mục liên quan

- [Kiểm tra tài liệu](check.md)
- [Cài đặt dự án](project-configuration.md)
