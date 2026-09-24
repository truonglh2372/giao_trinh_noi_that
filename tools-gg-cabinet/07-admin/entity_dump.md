# Entity dump (console)

> **Chỉ admin** — tool này không hiện trên toolbar user thường.

## Mục đích

**In thông tin lựa chọn ra Ruby Console** — class, bounds, thuộc tính, transform; kích thước dài diện tích xuất kèm **mm / mm²** (quy đổi từ model SketchUp).

## Khi nào dùng

- Debug nhanh entity user gửi kèm bug report (admin / dev).
- So sánh bounds instance vs kích thước [Hover dimensions](../06-tien-ich/hover_dimensions.md) hiển thị.
- Kiểm tra attribute dictionary (ABF, marking…) trước khi xuất file.

## Thao tác

1. Tài khoản **admin**.
2. **Chọn** một hoặc nhiều entity trong model (group, component, face, edge…).
3. Bấm **Dump ra Ruby Console** (toolbar hoặc **Extensions → GG Cabinet Tools**).
4. Mở **Window → Ruby Console** — đọc block:
   - `=== GG Entity Console Dump v… ===`
   - Chi tiết từng entity (indent cây)
   - `=== End of dump ===`

Selection rỗng: console in *Selection is empty. Please select one or more entities and run again.*

Context menu admin (nếu bật): mục *GG: Dump lựa chọn ra Console*.

## Phím tắt / modifier

**Không** có phím plugin. Gán menu admin qua Shortcuts nếu cần.

## Lỗi thường gặp

- **Chưa chọn gì** (message box bản TXT/JSON; console bản tiếng Anh tương đương).
- User thường **không có** lệnh — gate `run_if_admin`.
- Console trống: chưa mở Ruby Console hoặc chọn entity ngoài active context.

## Liên quan

- [Entity dump (txt)](entity_dump_txt.md) — cùng nội dung, lưu file.
- [Entity dump (JSON)](entity_dump_json.md) — cấu trúc đệ quy cho script.
- [Marking](../04-danh-dau-cnc/marking.md) — attribute GG_Marking trên marker.
