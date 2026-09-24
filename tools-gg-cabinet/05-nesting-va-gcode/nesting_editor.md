# Nesting Editor (trình xếp tấm)

## Mục đích

Chỉnh **layout nesting 2D** trong `__ABF_Nesting`: kéo part trên sheet, chỉnh gap/biên (mm), pack lại, chèn part vào **slot trống**, vẽ hình phụ, gán **thứ tự cắt** / **đường cắt ngoài**, in tem, tìm board 3D. Sheet **dưới** (`-bottom`) đi theo quy ước đối xứng với sheet trên.

## Khi nào dùng

- Sau generator ABF hoặc **ABF Extra Nesting**, cần **dịch/xếp lại** tấm trên sheet cho đủ khổ hoặc tránh va.
- Muốn **nhét thêm** tấm vào khe trống cùng vật liệu mà không chạy lại toàn bộ nest.
- Chuẩn bị sản xuất: **thứ tự cắt**, outline ngoài, tem, gap/border theo máy.

## Thao tác

### Vào tool và di chuyển part

1. Bật **Nesting Editor** — camera hướng layout phẳng trên sheet.
2. **Click** part trên sheet để chọn; **kéo** để di chuyển.
3. Bật **Block** (HUD) để **chặn chồng** — part không xuyên qua part khác; khi không còn chỗ vừa, sheet có thể **đỏ** (không fit true-shape); khi khe bị chặn nhưng còn pocket khác, part có thể **nhảy** tới vị trí trống **gần con trỏ** nhất.
4. Chỉnh **Gap** (mm) — khoảng cách va chạm giữa part; **Border** (mm) — lề tới biên sheet.
5. **Opacity** — giảm độ che khuất khi xem chồng sheet.

### Pack / infill / sheet

6. **Pack** — quét chọn part trên sheet rồi pack: part vừa chọn được **ưu tiên** xếp trước trên sheet active.
7. **Infill** — chọn part (3D hoặc trên sheet tùy luồng), chèn vào **slot trống** trên các sheet **cùng vật liệu** (sheet 1 → cuối); chỉ tạo sheet mới khi hết chỗ.
8. **Sheet back / forward** — đổi thứ tự sheet active.

### Tem và liên kết 3D

9. **Xoay tem 90°**, **Lật tem**, **In tem** (part đang chọn).
10. **Tìm board 3D** — chọn part nest → chọn/zoom board nguồn trong model.

### Vẽ phụ trên sheet

11. Vẽ **đường**, **hình chữ nhật**, **tròn**; **xóa** hình phụ. Giữ **Shift** khi vẽ để **không gộp** nét liền kề (mặc định line có thể chain).

### Thứ tự cắt (cut mode)

12. Bật **Cut mode** — gán layer thứ tự gia công lên part.
13. **Zigzag** qua part để đánh số thủ công; **Auto** gán tự động; **Reset all** xóa tag thứ tự trên mọi sheet.
14. **Cài đặt** (bánh răng) — tham số nesting editor / thứ tự cắt.

### Đường cắt ngoài (outline mode)

15. Bật **Outline mode** — offset đường cắt ngoài so với biên part.
16. **Pick** cạnh → **Create** outline; **Zigzag** đánh số R_On; chỉnh **Offset** / **Extend** (mm); erase / delete all.

### Sửa biên cắt part

17. **Edit edges** — chọn cạnh trên part, kéo hoặc gõ khoảng cách (mm world trên mặt phẳng sheet).

Mọi gap, border, offset, nudge là **mm world** (layout nesting nằm phẳng theo hệ model).

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Xoay part đang chọn 90° trên sheet | **Tab** |
| Nudge part 1 mm | **Phím mũi tên** (giữ lặp = trượt liên tục) |
| Marquee chọn part | Kéo khung; **Shift** = cộng vào selection |
| Vẽ line/rect/circle tách riêng (không merge) | Giữ **Shift** khi vẽ |
| Kết thúc zigzag thứ tự cắt / outline | **Enter** (VCB có thể nhận start index) |
| Thoát tool | **Esc** |

## Lỗi thường gặp

- **Sheet đỏ khi kéo**: không còn chỗ **true-shape** vừa part (kể cả khe hình chữ L) — thử sheet khác, giảm gap, hoặc tắt Block tạm để xếp tay (cẩn thận chồng).
- **Infill báo chưa chọn part**: chọn part trước khi infill.
- **Jump “lạ”**: tool ưu tiên pocket **gần con trỏ**, không phải mọi khe trống khi đã có part chiếm chỗ.
- **Không thấy nesting**: model thiếu `__ABF_Nesting` — tạo layout trước.

## Liên quan

- [ABF Extra Nesting](abf_extra_nesting.md) — thêm tấm mới vào cây nesting.
- [Tìm tấm trên nesting](find_nest_parts.md) / HUD Find — liên kết 3D ↔ sheet.
- [Xuất Nesting DXF](nesting_dxf.md) / [G-code](gcode.md) — sau khi layout ổn (kiểm tra TOP/BOT).
- [In nhãn](label_print.md) — in tem từ dữ liệu nesting.
