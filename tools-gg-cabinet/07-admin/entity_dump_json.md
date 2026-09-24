# Entity dump (JSON)

> **Chỉ admin** — tool này không hiện trên toolbar user thường.

## Mục đích

**Xuất đệ quy lựa chọn ra JSON** — cây entity với bounds **mm**, transform origin **mm**, face area **mm²**, edge length **mm**; phục vụ script kiểm tra / so sánh regression.

## Khi nào dùng

- Pipeline CI hoặc tool ngoài đọc cấu trúc selection.
- Diff hai lần dump sau thay đổi tool (marking, nesting…).
- Bổ sung TXT khi cần parse tự động.

## Thao tác

1. **Admin** — chọn entity gốc (có thể nhiều top-level; dump đệ quy con).
2. Bấm **Xuất lựa chọn ra JSON**.
3. Hộp thoại **GG Entity Console Dump — Xuất ra JSON** — nhập **tên file (không đuôi)**.
4. Chọn thư mục output → file `{tên}_{timestamp}.json`.
5. Thông báo *Đã xuất JSON:* hoặc lỗi *Xuất JSON thất bại*.

Schema do `EntityConsoleDump` v2.x định nghĩa (version trong console dump tương ứng).

## Phím tắt / modifier

**Không** có phím plugin.

## Lỗi thường gặp

- Selection rỗng / tên file invalid — giống [TXT](entity_dump_txt.md).
- JSON quá lớn: chọn subset (một group con) thay vì cả model.
- User không admin: lệnh không đăng ký trên toolbar/menu.

## Liên quan

- [Entity dump (console)](entity_dump.md)
- [Entity dump (txt)](entity_dump_txt.md)
- [Nesting Editor](../05-nesting-va-gcode/nesting_editor.md) — contract `__ABF_Nesting` khác JSON dump (xem design doc repo).
