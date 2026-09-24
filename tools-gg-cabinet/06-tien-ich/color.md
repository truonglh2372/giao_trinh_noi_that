# Chọn theo vật liệu (Color)

## Mục đích

Chọn **mọi group/component** trong model đang **mang trực tiếp** cùng một vật liệu (material) với mặt bạn click — lọc nhanh theo màu/texture phủ trên instance, không chọn ancestor chỉ “chứa” con có material đó.

## Khi nào dùng

- Model nhiều tấm cùng **melamine / veneer** — cần đổi tag, scale, hoặc xuất nhóm cùng loại.
- Sau khi gán material mẫu, chọn hàng loạt để [Xóa vật liệu](remove_color.md) hoặc chỉnh tay trong SketchUp.
- Kiểm tra tấm cùng vật liệu trước nesting (không thay thế [Layer Manager](layer_manager.md)).

## Thao tác

1. Bấm icon **Chọn theo màu vật liệu** (tooltip: *Chọn component để chọn tất cả cùng vật liệu*).
2. Con trỏ đổi sang dạng picker (icon PICKER).
3. **Click** lên face của group/component (hoặc mặt có material kế thừa dọc pick path):
   - Plugin lấy material **mặt visible** (front/back theo hướng camera); nếu mặt trống thì material **kế thừa** từ group/instance trên đường pick.
4. Selection trong model được **thay bằng** danh sách mọi group/instance có **trực tiếp** material đó (quét đệ quy `model.entities`, innermost owner).
5. Thanh trạng thái báo *Đã chọn N đối tượng có cùng vật liệu*.
6. Thoát tool: **Esc** (SketchUp hủy tool hiện tại).

Tool **không** tự gán material mới — chỉ chọn. (Áp dụng material hàng loạt, nếu có trong build khác, sẽ báo lỗi riêng.)

## Phím tắt / modifier

| Thao tác | Phím |
|--------|------|
| Thoát tool picker | **Esc** |
| Phím tắt bật tool | Gán qua menu **Extensions → GG Cabinet Tools** (không có sẵn) |

## Lỗi thường gặp

- **Click không chọn gì**: face không có material và không kế thừa — thử click mặt có texture hoặc instance đã gán material.
- **Thiếu tấm mong đợi**: material nằm trên **face con** nhưng instance ngoài không mang material trực tiếp — tool chỉ khớp owner trực tiếp; dùng Layer Manager hoặc chọn tay.
- **Áp dụng / xóa vật liệu thất bại** (nếu dùng thao tác khác sau chọn): geometry khóa hoặc trong component definition read-only.

## Liên quan

- [Xóa vật liệu](remove_color.md) — xóa material trên selection hiện tại (menu ngữ cảnh cũng có).
- [Warehouse](warehouse.md) — tab vật liệu V-Ray.
- [Board draw](../01-ve-va-chinh-hinh/board_draw.md) — tạo tấm trước khi gán material.
