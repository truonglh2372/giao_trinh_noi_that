# Cô lập đối tượng (Isolate)

## Mục đích

Ẩn mọi thứ trong model **trừ** nhóm/component (và nhánh chứa) bạn đang chọn, để tập trung chỉnh sửa hoặc trình bày một cụm chi tiết.

## Khi nào dùng

- Model đông chi tiết, cần nhìn rõ **một tủ / một cụm tấm** đang làm.
- Sau [Nesting Editor](../05-nesting-va-gcode/nesting_editor.md) hoặc ghép mộng, cần kiểm tra một nhánh mà không xóa geometry.
- Bổ sung cho [Đổi tên instance](instance_rename.md) (nút cô lập trong dialog rename) — Isolate trên toolbar cô lập theo **selection hiện tại** trong model.

## Thao tác

1. **Chọn** một hoặc nhiều group/component (face/edge lẻ được quy về **container cha** chứa chúng).
2. Bấm icon **Cô lập đối tượng** trên toolbar hoặc menu **Extensions → GG Cabinet Tools**.
3. Plugin ẩn các container gốc khác; selection được giữ lại trên phần còn visible.
4. Muốn trả model về như cũ: **Edit → Undo** (hoặc **Ctrl+Z**) — thao tác ghi trong Undo với tên *GG Cabinet Tools — Cô lập lựa chọn* / *Khôi phục sau cô lập*.

Geometry **lẻ** (face/edge không nằm trong group) **không** được coi là đối tượng cô lập riêng; tool ưu tiên container.

## Phím tắt / modifier

| Thao tác | Ghi chú |
|--------|---------|
| Hoàn tác cô lập | **Ctrl+Z** (Undo SketchUp) — gợi ý trên thanh trạng thái sau khi chạy |
| Phím tắt riêng cho lệnh Isolate | **Không** — gán qua **Window → Preferences → Shortcuts** nếu cần (menu Extensions → GG Cabinet Tools) |

## Lỗi thường gặp

- **“Chọn ít nhất một đối tượng để cô lập”**: chưa chọn group/component hợp lệ.
- **Cô lập thất bại** (message `%s`): hiếm — thử Undo, kiểm tra model có container bị khóa/ lỗi; chạy lại sau khi thoát edit context.
- **Vẫn thấy chi tiết khác**: có thể cùng nằm trong container được giữ; cô lập theo **cây gốc model**, không tách geometry bên trong một group đang giữ.

## Liên quan

- [Layer Manager](layer_manager.md) — ẩn/hiện theo tag thay vì cô lập selection.
- [Đổi tên instance](instance_rename.md) — cô lập các tấm đang chọn trong list rename.
- [Find nest parts](../05-nesting-va-gcode/find_nest_parts.md) — tìm tấm trên nesting thay vì ẩn phần còn lại.
