# Tìm tấm trên nesting

## Mục đích

Từ **tấm 3D gốc** (đã có **board-index** ABF), **tìm và chọn** mọi **part tương ứng** trên cây `__ABF_Nesting` — cả sheet **trên** và **-bottom** — rồi zoom camera nhìn layout nesting.

## Khi nào dùng

- Đã nest xong, cần **nhảy nhanh** từ chi tiết trong tủ sang vị trí trên sheet cắt.
- Kiểm tra tấm **có lên sheet** hay bị bỏ sót sau Extra Nesting.
- Đối chiếu **số tem** trên tấm 3D với part `__<n>. <tên>` trên sheet.

## Thao tác

1. Trong model 3D, **chọn** một hoặc nhiều tấm đã từng qua **ABF Extra Label** (attribute `ABF` / `board-index` trên instance).
2. Chạy **Tìm tấm trong nesting sheet** (toolbar/menu).
3. Tool thu thập index từ selection, quét `__ABF_Nesting`, chọn mọi part group có **cùng board-index**.
4. Camera chuyển **nhìn từ trên** (top), **zoom** vừa khung **cả root nesting** để thấy part trong bối cảnh sheet.
5. Thanh trạng thái báo số part đã chọn (top + bottom).

Liên kết index do Extra Nesting ghi khi đặt part — cùng số với nhãn trên tấm 3D.

## Phím tắt / modifier

Không có phím tắt riêng.

## Lỗi thường gặp

- **“Chọn board gốc (đã có board-index)”**: tấm chưa label hoặc chưa có attribute — chạy [ABF Extra Label](abf_extra_label.md).
- **“Không tìm thấy nesting”**: model chưa có group `__ABF_Nesting`.
- **“Không tìm thấy part”**: tấm chưa được nest hoặc index không khớp — chạy lại [ABF Extra Nesting](abf_extra_nesting.md) hoặc kiểm tra selection đúng tấm gốc.

## Liên quan

- [ABF Extra Label](abf_extra_label.md) — gán board-index / số tem.
- [ABF Extra Nesting](abf_extra_nesting.md) — đặt part lên sheet.
- [Nesting Editor](nesting_editor.md) — HUD **Tìm board 3D** (chiều ngược: từ part nest → board nguồn).
