# Xuất Nesting DXF

## Mục đích

Xuất **mỗi sheet nesting** (mặt **trên** và mặt **dưới** `-bottom`) ra **một file DXF riêng** — chuyển layout `__ABF_Nesting` sang CAM/phần mềm khác hoặc lưu trữ bản vẽ flat.

## Khi nào dùng

- Máy CNC hoặc phần mềm **không dùng G-code Manager** của plugin nhưng nhận DXF.
- Cần **archive** từng sheet theo vật liệu/khổ sau khi chỉnh nest.
- Sau [Nesting Editor](nesting_editor.md) / [ABF Extra Nesting](abf_extra_nesting.md) khi layout đã chốt.

## Thao tác

1. Đảm bảo model có **`__ABF_Nesting`** với sheet tên dạng `…-sheet-N` và `…-sheet-N-bottom`.
2. Chạy **Xuất Nesting DXF** trên toolbar hoặc menu.
3. Hộp thoại chọn **thư mục** lưu (save panel).
4. Plugin ghi **một DXF per sheet** (trên và dưới tách file).
5. Nếu kiểm tra TOP/BOT bật trong pipeline xuất, sửa lệch trước khi export thành công.

Tọa độ trong DXF theo layout nesting **world** (sheet phẳng trong model).

## Phím tắt / modifier

Không có phím tắt riêng.

## Lỗi thường gặp

- **Không tìm thấy sheet nesting**: chưa có group sheet đúng pattern `…-sheet-N`.
- **Không tạo được thư mục**: quyền ghi đường dẫn — chọn folder khác.
- **Chặn xuất TOP/BOT**: part bottom lệch hoặc thiếu cặp — xem thông báo và sửa trên [Nesting Editor](nesting_editor.md).

## Liên quan

- [G-code Manager](gcode.md) — xuất G-code trực tiếp từ cùng nesting.
- [In nhãn](label_print.md) — cùng nguồn part trên sheet.
- [ABF Extra Nesting](abf_extra_nesting.md) — tạo/bổ sung sheet và part.
