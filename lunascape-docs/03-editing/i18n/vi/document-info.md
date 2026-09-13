# Hiển thị thông tin tài liệu

“Bảng quản lý tài liệu” (bảng gồm mã tài liệu, phiên bản, ngày cập nhật, trạng thái…) đặt ở đầu tài liệu sẽ được gộp lại và hiển thị thành một dòng “thông tin tài liệu” nhỏ khi đọc. Bản thân Markdown vẫn là một bảng thông thường, nên vẫn đọc được bình thường trên GitHub.

## Điều kiện để được hiển thị

Đặt một bảng hai cột như sau ngay sau tiêu đề (H1).

```markdown
# Bản định nghĩa yêu cầu chức năng

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Điều kiện là bảng có dòng “文書ID” và có nhiều mục quản lý.
- Bảng đặt dưới tiêu đề `## 文書管理` hoặc `## Document information` cũng được nhận diện.
- Bảng nằm giữa phần nội dung và bảng “mục/nội dung” thông thường sẽ không được chuyển đổi.

## Cách hiển thị

- Khi đọc, chỉ hiển thị “trạng thái” và “ngày cập nhật” bằng cỡ chữ nhỏ.
- Nhấn vào dòng đó để hiển thị tất cả các mục.
- Khi in, tất cả các mục đều được hiển thị.
- Trong màn hình chỉnh sửa, bảng hiển thị như một bảng thông thường và có thể chỉnh sửa trực tiếp.

> **Mẹo**
>
> Nếu muốn luôn hiển thị dưới dạng bảng mà không thu gọn, hãy tắt [Thu gọn thông tin tài liệu] trong [Cài đặt hiển thị].

## Chủ đề liên quan

- [Chỉnh sửa tài liệu](README.md)
- [Thay đổi cài đặt hiển thị](../02-reading/display-settings.md)
