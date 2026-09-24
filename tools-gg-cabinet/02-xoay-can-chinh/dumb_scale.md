# Scale theo trục (Dumb Scale)

## Mục đích

Chia tỷ lệ (scale) các group/component đã chọn theo **chiều rộng (Width), chiều sâu (Depth), chiều cao (Height)** của bounding box **world**. HUD hiển thị ba chip W / D / H; click chip để nhập kích thước mới hoặc offset **mm world** cho toàn bộ selection.

## Khi nào dùng

- Đặt **cùng một kích thước** cho nhiều chi tiết (ví dụ cùng cao 720 mm).
- Tăng/giảm một chiều **tương đối** (nhập `+10` hoặc `-5` mm) trên bbox hiện tại.
- Chỉnh nhanh module khi **scale đồng nhất** theo trục bbox là đủ (không cần trượt từng đỉnh như Precise Scale).

## Thao tác

1. **Chọn** một hoặc nhiều group/component.
2. Bật **Scale theo trục** (Dumb Scale) trên toolbar — tool chạy ngay trên selection hiện tại.
3. Trên HUD (góc màn hình), xem giá trị **Width / Depth / Height** (mm world). Nếu các đối tượng không cùng kích thước một chiều, chip hiển thị `???`.
4. **Click** chip Width, Depth hoặc Height.
5. Trong hộp nhập:
   - gõ **số dương** (ví dụ `600`) → đặt chiều đó = **600 mm world** cho mọi đối tượng trong selection;
   - gõ **`+`** hoặc **`-`** trước số (ví dụ `+2`, `-10`) → cộng/trừ **mm world** so với kích thước hiện tại.
6. Thoát tool bằng cách chọn tool khác hoặc **Esc** (theo SketchUp).

Plugin map bbox SketchUp: **width → Width**, **height → Depth**, **depth → Height** (theo convention Dumb Scale trong code).

## Phím tắt / modifier

Tool **không** đăng ký phím modifier riêng. Mọi nhập liệu qua **click chip HUD** và hộp thoại số.

| Thao tác | Cách làm |
|--------|----------|
| Đặt kích thước tuyệt đối | Nhập số mm (ví dụ `17.5`) |
| Offset theo chiều | Nhập `+mm` hoặc `-mm` |
| Hủy | **Esc** / đóng hộp nhập |

## Lỗi thường gặp

- **“Vui lòng chọn một hoặc nhiều đối tượng”** / **“… nhóm hoặc component”**: selection rỗng hoặc chỉ có face/edge — chọn group/component.
- **Chip hiển thị `???`**: các đối tượng không cùng W, D hoặc H — chọn đồng nhất hoặc chỉnh từng nhóm.
- **Chi tiết bên trong bị méo**: Dumb Scale scale cả definition — dùng [Precise Scale](precise_scale.md) nếu chỉ muốn đổi một phía bbox.
- **Lỗi Dumb Scale**: thông báo `Lỗi GG Cabinet Tools Dumb Scale` — thường do kích thước ≤ 0 hoặc geometry không scale được; kiểm tra giá trị mm nhập vào.

## Liên quan

- [Precise Scale](precise_scale.md) — trượt đỉnh, không scale đồng nhất.
- [Hover dimensions](../06-tien-ich/hover_dimensions.md) — đọc kích thước mm world trước/sau chỉnh.
- [Căn đối tượng (Align)](align.md) — đặt vị trí sau khi đã đúng kích thước.
