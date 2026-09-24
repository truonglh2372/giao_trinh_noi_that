# ABF Extra Nesting

## Mục đích

Thêm **các tấm 3D đã chọn** (thường đã có `_ABF_Label`) vào cây **`__ABF_Nesting` hiện có**: trích outline mặt cắt (kèm lỗ), **tự xếp (pack)** bằng thuật toán nesting, **tràn sang sheet mới** khi hết chỗ. Giữ cấu trúc sheet/part ABF (`_ABF_cuttingLines`, pocket, mark square, label trên sheet).

## Khi nào dùng

- Layout ABF đã có nhưng cần **bổ sung tấm lẻ** không qua generator gốc.
- Sau [ABF Extra Label](abf_extra_label.md) — board đã có số tem và mũi tên grain.
- Trước [Nesting Editor](nesting_editor.md) để tinh chỉnh vị trí tay.

## Thao tác

1. **Chọn** các group **tấm** cần thêm (component nên đã explode → group).
2. Chạy **ABF Extra Nesting**.
3. Nếu có **material trên mặt bên trong** tấm, hộp thoại hỏi Yes/No:
   - **Yes** — xóa material các đối tượng đó, **dừng** lượt nest, chọn sẵn tấm để bạn kiểm tra.
   - **No** — bỏ qua các tấm đó trong nest.
4. Nhập **margin (mm)** khi được hỏi (mỗi lần chạy — khoảng cách pack, quy đổi đúng mm world).
5. Tool tìm sheet **cùng vật liệu/màu**, pack part; index part mới = **max index trên sheet + 1**, tên dạng `__<n>. <tên>`.
6. Tấm có mark chỉ trên **mặt sau** có thể có thêm outline trên sheet **`-bottom`** (mirror theo quy ước lật tấm).
7. Kết thúc: thông báo **đã xếp bao nhiêu / tổng số chọn**; liệt kê tấm **bỏ qua** (chưa label, không phải board, geometry lỗi, không vừa sheet, không khớp sheet, …). Đóng hộp thoại → **tự chọn** tấm thất bại.

Extra Nesting **không explode** model — không chọn `__ABF_Nesting` làm nguồn explode.

## Phím tắt / modifier

Không có phím tắt — selection + input margin + hộp thoại kết quả.

Tùy chọn nesting: **Cho phép xoay 90° để vừa khít** (trong cài đặt nesting liên quan, nếu bật cho pack).

## Lỗi thường gặp

- **Chưa có nhãn**: gắn label trước — xem danh sách `Board chưa gắn nhãn`.
- **Component**: explode → group ([Explode DC → Groups](explode_to_groups.md)).
- **Không nhận board**: bọc group thừa, geometry lỗi — sửa hoặc unwrap.
- **Không vừa sheet / không có sheet màu**: kiểm tra tên vật liệu sheet `__<color>-sheet-N` trong model.
- **Mark không lên sheet**: instance mark thiếu `"ABF"` trong tên — đổi tên trên board gốc.
- **Preflight dừng hẳn**: có đối tượng không nest được trong selection — sửa hết rồi chạy lại (không đặt board nào nếu preflight fail).

## Liên quan

- [ABF Extra Label](abf_extra_label.md) — bước trước khuyến nghị.
- [Explode DC → Groups](explode_to_groups.md) — chuẩn group.
- [Nesting Editor](nesting_editor.md) — chỉnh sau pack.
- [Tìm tấm trên nesting](find_nest_parts.md) — kiểm tra part theo board-index.
- [Thống kê cấu kiện](../06-tien-ich/component_stats.md) — đọc nesting hiện tại.
