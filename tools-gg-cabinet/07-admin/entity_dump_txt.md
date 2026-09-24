# Entity dump (TXT)

> **Chỉ admin** — tool này không hiện trên toolbar user thường.

## Mục đích

**Xuất dump lựa chọn ra file văn bản** (.txt) — cùng family thông tin với dump console, tiện đính kèm ticket / diff ngoại tuyến. Kích thước trong file dùng **mm** (bounds, cạnh, điểm transform).

## Khi nào dùng

- Gửi cấu trúc model cho dev không cần chia sẻ `.skp` đầy đủ.
- Lưu snapshot selection trước/sau thao tác phá hủy.
- Đọc bằng editor text khi Ruby Console khó copy.

## Thao tác

1. **Admin** + **chọn** entity cần dump.
2. Bấm **Xuất lựa chọn ra TXT** (toolbar hoặc menu admin).
3. Hộp thoại **GG Entity Console Dump — Xuất ra TXT**:
   - **Tên file xuất (không đuôi)** — mặc định gợi ý từ model/selection.
4. Chọn **thư mục** lưu (hộp chọn folder hệ thống).
5. File ghi dạng `{tên}_{YYYYMMDD_HHMMSS}.txt` — message *Đã xuất:* kèm đường dẫn; mở thư mục trong file manager OS.

## Phím tắt / modifier

**Không** có phím plugin.

## Lỗi thường gặp

- **Chưa chọn gì. Hãy chọn một hoặc nhiều đối tượng rồi chạy lại.**
- **Tên file không hợp lệ.**
- **Xuất thất bại** — quyền ghi thư mục, đường dẫn quá dài, disk đầy.
- **Thư mục không tồn tại** (khi dùng đường dẫn tay ở flow khác).

## Liên quan

- [Entity dump (console)](entity_dump.md) — xem nhanh không tạo file.
- [Entity dump (JSON)](entity_dump_json.md) — machine-readable.
- [Component Stats](../06-tien-ich/component_stats.md) — báo cáo user, không phải debug dump.
