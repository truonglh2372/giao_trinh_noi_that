# Dán cạnh (edge band)

## Mục đích

Đánh dấu **cạnh cần dán melamine/PVC** trên các mặt cạnh (s-face) của tấm ván. Màu và preset (dày mm, hệ số thống kê) giúp **Thống kê cấu kiện** tính mét dán cạnh và nhóm “Chỉ dán cạnh”.

## Khi nào dùng

- Sau khi vẽ tấm, trước khi xuất bóc vật liệu / báo giá dán cạnh.
- Cần đánh dấu **hàng loạt** cạnh hở, toàn bộ cạnh bên, hoặc **xóa hết** mark cũ trên các tấm đã chọn.
- Muốn **chuẩn hóa tên/màu/dày** preset cạnh (Cạnh 0.4 mm, 2 mm, …) cho cả team.

## Thao tác

1. Bật tool **Dán cạnh** trên toolbar.
2. **Chọn tấm**: click tấm trong model, kéo khung chọn, hoặc chọn sẵn rồi bật tool. Có thể **Ctrl** (hoặc modifier copy khi kéo khung) để **cộng thêm** vào selection thay vì thay thế.
3. **Click trực tiếp cạnh** (s-face) trên tấm đang chọn → bật/tắt mark cạnh đó với **preset đang active** (màu trên preview).
4. Ba nút trên HUD (trái → phải):
   - **Cạnh hở** — mark mọi cạnh không tiếp xúc tấm khác trên các tấm đã chọn.
   - **Xóa hết** — gỡ toàn bộ mark dán cạnh trên các tấm đã chọn.
   - **Tất cả cạnh** — mark mọi cạnh bên trên các tấm đã chọn.
5. **Bánh răng** mở **Preset dán cạnh**: thêm/sửa tên, dày (mm), hệ số, màu; **Lưu** hoặc **Mặc định**.
6. Mark được ghi lên geometry tấm; nesting đọc `_ABF_edgeBanding` (nếu có trong pipeline ABF).

Khoảng cách và dày preset hiển thị theo **mm world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Thêm tấm vào selection (click hoặc khung chọn) | **Ctrl** / modifier copy (theo SketchUp) |
| Thay selection (không cộng) | Click / khung chọn **không** giữ Ctrl |
| Đổi preset mark | Chọn preset trong dialog (bánh răng) — preset active dùng cho click cạnh |
| Thoát tool | **Esc** (quay tool Select của SketchUp) |

Thanh trạng thái: click cạnh để đánh dấu, hoặc dùng 3 nút trên cùng; bánh răng = preset.

## Lỗi thường gặp

- **Không tìm thấy tấm nào**: model không có board nhận dạng được — kiểm tra tấm là group/component ván chuẩn (hai mặt lớn song song).
- **Click cạnh không phản hồi**: tấm chứa cạnh chưa nằm trong selection — click tấm trước hoặc chọn bằng khung.
- **Thống kê dán cạnh sai**: kiểm tra **hệ số** preset và mark đúng cạnh thật sự cần dán (dùng “cạnh hở” cho tủ kín).

## Liên quan

- [Marking](marking.md) — line/pocket CNC trên mặt tấm, không thay dán cạnh.
- [Thống kê cấu kiện](../06-tien-ich/component_stats.md) — đọc mark dán cạnh và nhóm chỉ dán cạnh.
- [Trim cạnh biên tấm](../01-ve-va-chinh-hinh/board_trim.md) — trim s-face trước khi mark nếu cần mép sạch.
