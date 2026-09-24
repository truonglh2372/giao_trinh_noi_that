# Xoay đối tượng (Rotate)

## Mục đích

Xoay group hoặc component đã chọn **90°** quanh trục world **X (đỏ), Y (xanh lá), Z (xanh dương)**. Tool hiển thị ghost màu theo từng trục; click ghost hoặc dùng phím mũi tên để xoay. **Ctrl** bật/tắt copy (xoay bản gốc, để lại bản duplicate tại chỗ cũ).

## Khi nào dùng

- Xoay nhanh tấm hoặc chi tiết **90° / 180°** cho đúng hướng lắp (đứng/ngang, đổi cạnh dài).
- Chỉnh hướng **nhiều object cùng lúc** trong selection.
- Cần bản sao tại vị trí cũ sau khi xoay (copy mode).

## Thao tác

1. **Chọn** group/component cần xoay.
2. Bật tool **Xoay đối tượng** trên toolbar.
3. **Rê chuột** lên ghost preview (đỏ = X, lá = Y, dương = Z) hoặc dùng phím mũi tên (xem bảng modifier).
4. Tùy chọn: bật **Ctrl** để copy (dấu **+**).
5. **Click** ghost của trục muốn xoay, hoặc bấm mũi tên để xoay ngay quanh trục tương ứng.

Góc xoay cố định **90°** mỗi thao tác; trục luôn là **trục world**, không phải trục local của component.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Xoay 90° quanh trục Z | **↑** hoặc **↓** |
| Xoay 90° quanh trục Y | **←** |
| Xoay 90° quanh trục X | **→** |
| Đảo chiều xoay (ngược 90°) | Giữ **Shift** khi bấm mũi tên hoặc click ghost |
| Bật/tắt copy (giữ bản tại chỗ cũ) | **Ctrl** (sticky) |
| Hủy tool | **Esc** |

## Lỗi thường gặp

- **Không thấy ghost**: selection rỗng hoặc không phải group/component; chọn lại rồi bật tool.
- **Xoay “lệch” so với tấm**: tool xoay quanh **tâm bbox world** của selection, không quanh góc tấm — dùng [Align](align.md) hoặc SketchUp Move sau xoay nếu cần căn góc.
- **Instance definition chung**: mọi instance cùng definition đều đổi — **Make Unique** nếu chỉ sửa một cái.
- **Nhầm với Xoay nhãn**: [Xoay nhãn](../05-nesting-va-gcode/rotate_label.md) chỉ xoay nhãn nesting trên tấm, không xoay cả khối.

## Liên quan

- [Căn đối tượng (Align)](align.md) — snap mép/mặt sau khi đã đúng hướng.
- [Mirror](mirror.md) — lật đối xứng qua mặt/điểm.
- [Precise Scale](precise_scale.md) — đổi kích thước không xoay.
- [Xoay nhãn](../05-nesting-va-gcode/rotate_label.md) — xoay nhãn ABF trên tấm (luồng nesting).
