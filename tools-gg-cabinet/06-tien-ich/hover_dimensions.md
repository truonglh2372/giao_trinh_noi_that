# Kích thước khi rê chuột (Hover dimensions)

## Mục đích

Tool overlay: khi **rê chuột** lên **group** hoặc **component**, hiển thị **rộng, cao, sâu** theo hệ trục local của instance (quy ra **kích thước world** trên nhãn) cùng trục XYZ màu trên viewport.

## Khi nào dùng

- Kiểm tra nhanh **kích thước tấm / module** mà không mở Entity Info hay đo tay.
- So sánh hai chi tiết song song trong assembly (rê lần lượt từng object).
- Hỗ trợ sau [Precise Scale](../02-xoay-can-chinh/precise_scale.md) hoặc [Scale](../02-xoay-can-chinh/dumb_scale.md) — xác nhận bbox world.

## Thao tác

1. Bấm **Kích thước khi rê chuột** trên toolbar hoặc menu.
2. **Rê chuột** lên group/component:
   - Ba cạnh bbox local (có scale transform) → ba nhãn dùng `Sketchup.format_length` (mm nếu model đặt mm).
   - Trục đỏ / xanh lá / xanh dương = X / Y / Z của transformation instance.
3. Rê ra vùng trống hoặc entity không phải group/component → overlay tắt.
4. **Esc** để thoát tool (hủy tool, xóa overlay).

Chỉ pick **Group** và **ComponentInstance**; face/edge lẻ không hiện kích thước.

## Phím tắt / modifier

| Thao tác | Phím |
|--------|------|
| Thoát tool | **Esc** |

Không có phím bật tool sẵn — gán qua menu Extensions nếu cần.

## Lỗi thường gặp

- **Không thấy số**: con trỏ không nằm trên group/component; hoặc instance scale ~0 trên một trục.
- **Số khác Entity Info**: plugin hiển thị **width × height × depth** của definition bounds × scale trục (local AABB), không phải khoảng cách đo tùy ý giữa hai điểm world.
- **Đơn vị lạ**: đặt model **mm** ([Bắt đầu](../00-bat-dau.md)) để khớp giáo trình.

## Liên quan

- [Dumb Scale](../02-xoay-can-chinh/dumb_scale.md) — chỉnh rộng/cao/sâu có chủ đích.
- [Board draw](../01-ve-va-chinh-hinh/board_draw.md) — tạo tấm với kích thước VCB mm world.
- [Component Stats](component_stats.md) — khối lượng / dự toán formal, không phải HUD rê chuột.
