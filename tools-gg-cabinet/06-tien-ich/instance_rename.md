# Đổi tên instance (Instance rename)

## Mục đích

Đổi tên **instance** group/component với **thư viện tên** (tìm fuzzy), chế độ **Prefix** / **Suffix**, **Clear ID** đầu tên; đồng bộ danh sách tên lên server khi đăng nhập. UI là **HtmlDialog** — gõ chữ không kích hoạt phím tắt tool SketchUp.

## Khi nào dùng

- Chuẩn hóa tên tấm trước [In nhãn](../05-nesting-va-gcode/label_print.md) / nesting.
- Áp prefix dự án (VD `A1_`) hoặc suffix vật liệu hàng loạt trên selection.
- Tìm tấm trong list rename theo **số tem hoặc tên**, rồi **chọn trong model** hoặc **cô lập** các tấm trong list.

## Thao tác

1. (Tuỳ chọn) Chọn trước group/component trong model — selection SketchUp là nguồn chính; dialog hiển thị số đối tượng đang chọn.
2. Bấm **Đổi tên instance** trên toolbar hoặc menu.
3. Dialog **Đổi tên** mở (900×620, có thể resize):
   - Cột trái: danh sách instance đang chọn (#, tên); ô **Tìm theo số tem hoặc tên** (Enter).
   - Ba vùng **Đổi tên** / **Prefix** / **Suffix**: gõ để lọc gợi ý từ thư viện; chip đã lưu bên phải (kéo thả sắp xếp, × để xóa khỏi thư viện).
4. Chọn object thêm/bớt: click trong model; **Shift + click** thêm/bớt selection (SketchUp chuẩn) — HUD dialog cập nhật số chọn.
5. Áp tên:
   - **Tab**: áp **dòng gợi ý đang highlight** trong dropdown.
   - **Enter**: dùng **nguyên văn** chữ đang gõ (và lưu vào thư viện nếu là tên mới).
   - **↑ / ↓**: chọn dòng gợi ý.
6. **Clear ID**: xóa prefix ID đầu tên theo quy ước plugin (Undo riêng).
7. Nút **Chọn trong model** / **Cô lập** (list): thao tác trên subset đang chọn trong bảng rename.
8. **Esc** (hoặc đóng dialog): thoát; thư viện prefix/suffix lưu local, tên sync server nền.

Tên (`names`) merge với `/api/instance_names` khi có mạng; prefix/suffix chỉ local JSON cạnh config.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Thêm/bớt selection trong model | **Shift + click** |
| Chọn gợi ý dropdown | **↑** / **↓** |
| Áp gợi ý highlight | **Tab** |
| Áp chữ đang gõ | **Enter** |
| Thoát | **Esc** / đóng dialog |

Toolbar status cũ ghi *Click chọn (Shift thêm), Tab áp — Esc thoát* — vẫn đúng cho selection + phím trong dialog.

## Lỗi thường gặp

- **Danh sách trống** (*— chưa có đối tượng trong danh sách —*): chưa chọn group/component.
- **— không khớp —**: tìm trong list không ra — kiểm tra số tem / chính tả.
- Tên server không về: offline — vẫn dùng thư viện local; đăng nhập lại để sync.
- Gõ không vào ô: click focus vào ô rename trong dialog (dialog cố ý nuốt phím để tránh shortcut SketchUp).

## Liên quan

- [Layer Manager](layer_manager.md) — tuỳ chọn đổi tên instance khi gán tag.
- [Isolate](isolate.md) — cô lập theo selection toolbar.
- [Find nest parts](../05-nesting-va-gcode/find_nest_parts.md) — tìm tấm theo nesting.
