# Quản lý layer (Layer Manager)

## Mục đích

Quản lý **tag/layer** SketchUp trong phạm vi lựa chọn hoặc cả model: tìm tag, bật/tắt hiển thị, **focus** (chỉ xem tag đang chọn), **highlight** viền geometry, đổi màu tag, gán tag lên selection, xóa geometry hoặc gỡ tag.

## Khi nào dùng

- Model nhiều tag `ABF_*` / tag CNC — cần **lọc nhanh** tag có trong selection hoặc toàn model.
- Kiểm tra tấm trên một tag: highlight + focus thay vì ẩn tay từng tag trong Tags panel.
- Gán tag chuẩn cho tấm vừa vẽ, hoặc **dọn tag** (chuyển geometry sang tag khác / xóa tag).

## Thao tác

1. (Tuỳ chọn) **Chọn** group/component — danh sách tag ưu tiên tag xuất hiện trong vùng chọn; không chọn thì làm việc với **context hiện tại** hoặc toàn model tùy chế độ tìm.
2. Mở **Quản lý layer** từ toolbar hoặc menu.
3. **Ô tìm tag**: gõ để lọc; placeholder *Tìm trong mọi tag của model...* khi bật chế độ xem toàn model.
4. **Hiện tất cả tag**: toggle — bật thì liệt kê mọi tag model (không đổi vùng chọn); tắt thì quay lại tag trong selection/context.
5. Trên từng dòng tag:
   - **Mắt**: hiện/ẩn tag trong model.
   - **Tên tag**: click để **chọn container** trên tag đó (top-level có geometry thuộc tag).
   - **Màu**: color picker — màu tag (đồng bộ máy khác nếu đã đăng nhập).
   - **Highlight** (đèn pin): viền geometry thuộc tag (trừ Untagged/Layer0 khi bật hàng loạt).
   - **Focus**: checkbox — chỉ hiển thị tag được focus (có thể nhiều tag).
   - **Gán tag** (icon tag): gán tag này lên selection; **Ctrl + click** = gán **đệ quy** cả geometry lồng bên trong.
   - **Gỡ tag** (thùng rác): chuyển geometry sang tag khác hoặc xóa tag (hộp thoại xác nhận).
   - **Xóa geometry trên tag** (×): xóa entity trên tag đó (có xác nhận).
6. **Lưu tag mới / gán từ ô tìm**: nhập tên tag vào ô tìm → lưu — hộp thoại *Lưu tag* hỏi gán lên selection, tuỳ chọn **gán recursively** và **đổi tên instance theo tên tag**.
7. Chọn nhiều dòng (checkbox cột đầu) → **xóa tag hàng loạt** nếu dialog có nút tương ứng.
8. Đóng dialog: trạng thái highlight/focus/màu **lưu local** và **đẩy lên server** khi đã đăng nhập (đồng bộ máy khác).

Highlight chạy bằng tool overlay trong viewport; dùng nút **Reactivate** trong dialog nếu viền không cập nhật sau khi đổi model.

## Phím tắt / modifier

| Thao tác | Modifier |
|--------|-----------|
| Gán tag đệ quy (geometry con) | **Ctrl** khi bấm nút gán tag trên dòng |
| Phím tắt riêng trong dialog Layer Manager | **Không** — gán qua menu Extensions nếu cần |

## Lỗi thường gặp

- **Không tìm thấy layer/tag nào**: không có tag trong selection/context (thử bật *Hiện tất cả tag* hoặc chọn object trước).
- **Chọn đối tượng để gán tag** / **Nhập tên tag vào ô tìm kiếm**: thiếu selection hoặc tên trống khi lưu.
- **Tag đã tồn tại**: tên trùng tag có sẵn — đổi tên hoặc chọn tag cũ trên list.
- Focus/highlight “lẫn” sau đó: tắt focus checkbox hoặc đóng dialog (plugin khôi phục hiển thị tag).

## Liên quan

- [Isolate](isolate.md) — ẩn mọi thứ trừ selection, không theo tag.
- [Chọn theo vật liệu](color.md) — lọc theo material, không theo tag.
- [Marking](../04-danh-dau-cnc/marking.md) — tạo geometry trên tag line/pocket CNC.
- [G-code Manager](../05-nesting-va-gcode/gcode.md) — preset layer/toolpath gắn với tag DB.
