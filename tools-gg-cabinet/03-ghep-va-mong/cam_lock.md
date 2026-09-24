# Liên kết ngang (Cam lock)

## Mục đích

Tạo **đánh dấu liên kết ngang** (ốc cam / dowel / vít tùy chế độ trong thiết lập) trên tấm ván tiếp xúc: vẽ **vòng tròn** (edges) trên mặt f/b, **không cắt hình khối**. Tấm khóa cam được chọn; tấm đối diện (pin) được nhận tự động. Layer mặc định gồm `ABF-CamLock`, `ABF-CamPin`, và các layer dowel/vít nếu bật.

## Khi nào dùng

- Lắp **khóa cam Euro**, **dowel**, hoặc **vít** cần vị trí khoan chuẩn trên mặt tấm.
- Ghép **tấm đứng–ngang**, **hồi–đáy** với cùng quy trình anchor như mộng nhưng chỉ marking CNC.
- Chỉnh **số slot**, offset mép, đường kính D15/D10 (cam/pin) trong dialog thiết lập Cam lock.

## Thao tác

1. Mở **Thiết lập Cam lock** (nếu cần đổi mode: cam / dowel / vít, đường kính, số slot, offset mm, layer).
2. Bật **Tạo liên kết ngang** trên toolbar.
3. **Chọn tấm khóa cam** (tấm có mặt s tiếp xúc tấm đối diện).
4. Di chuột lên mặt cạnh có **anchor** (tương tự tool mộng); preview vị trí đánh dấu.
5. **Click** anchor tại slot cần đánh dấu.
6. Dùng **Shift** / **Ctrl** / **Tab** theo nhu cầu (modifier).
7. Trong **edit mode** (sửa connection đã tạo): **Delete** xóa connection; **Tab** lật mặt đánh dấu; **Ctrl** (thả phím) đảo chân trên tấm pin (một số mode cam cố định hướng).

Khoảng cách offset và đường kính trong thiết lập là **mm world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Đánh dấu thêm **mặt đối diện** cùng tấm | Giữ **Shift** khi click |
| Đánh dấu **tất cả slot** trên face (và mở rộng tương tự khi Shift) | Giữ **Ctrl** khi click |
| Lật mặt đánh dấu trên tấm khóa cam (khi đang marking) | **Tab** |
| Edit connection: lật mặt đánh dấu | **Tab** (trong edit mode) |
| Edit connection: đảo chân pin | **Ctrl** (on key up; không áp dụng mọi mode cam) |
| Xóa connection đang sửa | **Delete** / **Backspace** (trong edit mode) |
| Thoát | **Esc** |

## Lỗi thường gặp

- **Không thấy anchor**: chưa chọn đúng tấm khóa cam, hoặc không có cạnh tiếp xúc hợp lệ với tấm đối diện.
- **Thiếu vòng tròn trên tấm pin**: tấm đối diện không được nhận — kiểm tra tiếp xúc mặt, tấm có cùng chuẩn ván plugin.
- **Slot trùng**: vị trí đã đánh dấu (dung sai ~0,5 mm) — chọn slot khác hoặc xóa connection cũ (edit mode).
- **Tab / Ctrl “không làm gì”**: đang không ở edit mode hoặc connection loại cam cố định hướng — chỉ Tab lật mặt khi tool cho phép.

## Liên quan

- [Tạo mộng](tenon_helper.md) — cùng UX anchor/mũi tên, có cắt geometry.
- [Khấu (cross halving)](khau.md) — join khác, tag `ABF_CrossHalvingJoin`.
- [Intersect Mark](../04-danh-dau-cnc/intersect_mark.md) — đánh dấu tiết diện giao nhau.
- [G-code Manager](../05-nesting-va-gcode/gcode.md) — layer ABF-CamLock / CamPin trong lối cắt.
