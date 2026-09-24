# ABF Extra Label

## Mục đích

Gắn **nhãn ABF** (`_ABF_Label`) lên **mặt trước (f_face)** mỗi tấm: **mũi tên chiều gia công** (theo trục dài tấm) và **số thứ tự** đồng bộ với cây `__ABF_Nesting`. Bước bắt buộc trước Extra Nesting nếu cần kiểm tra hướng vân/chiều phay trên sheet.

## Khi nào dùng

- Đã có (hoặc sắp có) layout **__ABF_Nesting** và cần thêm/bổ sung tấm 3D với **số tem thống nhất**.
- Tấm mới chưa có `_ABF_Label` hoặc cần **đánh số lại** toàn model / tiếp số trên selection.
- Trước **ABF Extra Nesting** — nesting bỏ qua board **chưa có nhãn**.

## Thao tác

1. **Chọn** các group/component tấm trong model (**không** cần chọn `__ABF_Nesting`; tool tự loại root nesting).
2. Chạy **ABF Extra Label** (toolbar/menu).
3. Hộp thoại **Đánh số lại?**
   - **Yes** — xóa tag `ABF_Label` và mọi geometry trên tag đó trong **cả model**, đánh số lại từ **0**.
   - **No** — xóa/chuẩn bị label chỉ trên **tấm đang chọn**, số tiếp theo từ **max index hiện có** trên nesting.
4. Tool chạy **Explode → Groups** (cùng hộp thoại tùy chọn như tool Explode riêng) rồi lọc board hợp lệ.
5. Với mỗi tấm OK: tạo group `_ABF_Label` (chỉ **edges**, phẳng trên f_face) gồm mũi tên + chữ số index.
6. Thông báo kết thúc: số tấm đã gắn / bỏ qua; đối tượng lỗi được **tự chọn** sau khi đóng hộp thoại.

Số index lấy max trên toàn cây nesting + 1 cho batch hiện tại. Chiều mũi tên = trục dài trong mặt f_face (mm world).

## Phím tắt / modifier

Không có phím tắt riêng — toàn bộ qua selection, hộp thoại Yes/No và explode confirm.

## Lỗi thường gặp

- **Chưa chọn tấm**: chọn group/component trước.
- **Component bị từ chối**: definition dùng chung — **explode thành group** trước (xem [Explode DC → Groups](explode_to_groups.md)).
- **Không phải tấm ván**: ít mặt, hai mặt lớn không song song/không congruent, cạnh không chữ nhật — sửa geometry hoặc bọc group.
- **Material bên trong**: tool có thể **dừng** nếu material trên mặt nguyên sinh bên trong — xóa màu (Remove color) rồi chạy lại.
- **Không gắn được nhãn**: đọc từng dòng lý do trong messagebox.

## Liên quan

- [Explode DC → Groups](explode_to_groups.md) — bước explode trong luồng label.
- [ABF Extra Nesting](abf_extra_nesting.md) — đưa tấm đã label lên sheet.
- [Xoay nhãn](rotate_label.md) / [Đảo nhãn](flip_label.md) — chỉnh hướng tem trên tấm 3D.
- [Tìm tấm trên nesting](find_nest_parts.md) — nhảy từ board 3D sang part trên sheet (cùng board-index).
