# Xóa vật liệu (Remove color)

## Mục đích

Xóa **material** khỏi **lựa chọn hiện tại** (face front/back và material trên group/instance trong tập chọn) — trả về mặt mặc định / không còn material gán trực tiếp trên các entity được xử lý.

## Khi nào dùng

- Chuẩn bị xuất nesting / DXF cần model **sạch material** hoặc tránh nhầm mặt khi [Chọn theo vật liệu](color.md).
- Sửa nhanh một nhóm tấm đã chọn sẵn (không cần vào từng Edit Component).
- Menu chuột phải: khi có selection, **Extensions** context có mục xóa material (cùng logic `RemoveColorTool`).

## Thao tác

1. **Chọn** một hoặc nhiều object (group, component, face… trong selection SketchUp).
2. Bấm **Xóa vật liệu** trên toolbar **hoặc** dùng mục context menu plugin khi right-click selection.
3. Plugin chạy một Undo step *GG Cabinet Tools — Xóa màu*.
4. Thanh trạng thái: *Đã xóa vật liệu trên N đối tượng*.

Không mở tool tương tác — lệnh một lần trên selection.

## Phím tắt / modifier

**Không** có phím riêng trong plugin. Gán lệnh toolbar/menu qua SketchUp Shortcuts nếu cần.

## Lỗi thường gặp

- **Chọn ít nhất một đối tượng để xóa vật liệu**: selection rỗng.
- **Xóa vật liệu thất bại: …** / **Xóa màu thất bại: …**: geometry khóa, component shared, hoặc lỗi SketchUp — thử Undo, mở khóa, explode level phù hợp rồi chạy lại.

## Liên quan

- [Chọn theo vật liệu](color.md) — gom selection cùng material trước khi xóa.
- [ABF Extra Label](../05-nesting-va-gcode/abf_extra_label.md) — pipeline nesting có bước xử lý material nội bộ plugin.
- [Layer Manager](layer_manager.md) — dọn model theo tag, không theo material.
