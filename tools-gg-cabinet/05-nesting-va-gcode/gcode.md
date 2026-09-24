# G-code Manager (quản lý G-code)

## Mục đích

Mở **Quản lý G-code**: định nghĩa **lối cắt (toolpath)**, map **layer/tag** nesting → profile / pocket / khoan / fluting, gán **công cụ cắt**, xem preview 2D, **xuất file G-code** ra thư mục máy CNC.

## Khi nào dùng

- Model đã có **`__ABF_Nesting`** với part, pocket, cutting lines đúng layer ABF.
- Cần **cấu hình lần đầu** hoặc chỉnh recipe cắt (dao, tốc độ, thứ tự) cho xưởng.
- Sau khi chỉnh layout trong [Nesting Editor](nesting_editor.md) và xác nhận **TOP/BOT** khớp (nếu gia công hai mặt).

## Thao tác

1. Chạy **Quản lý G-code** trên toolbar (menu **Tạo G-code**).
2. Tab **Lối cắt** — thêm/nhân bản/sắp xếp nhóm toolpath: Profile, Pocket, Fluting, Khoan; import/export JSON hoặc mẫu Aspire; gán tham số từng lối.
3. Tab **Layer** — map tag SketchUp (ABF_LINE_CUT, ABF_POCKET, thứ tự cắt, …) sang lối cắt; reset nếu lệch preset.
4. Tab **Công cụ cắt** — thư viện dao (đường kính, tốc độ, …) dùng trong toolpath.
5. **Preview 2D** / panel G-code — kiểm tra đường chạy trước khi post.
6. **Xuất G-code** — chọn **thư mục output**; plugin đọc nesting qua `NestingReader`, sinh file theo cấu hình.

Capture profile 2D (khi tool yêu cầu): click component biên dạng dao phẳng XY, vòng kín; **Esc** hủy.

Trước xuất, hệ thống có thể **chặn** nếu cặp sheet TOP/BOT lệch > **0,1 mm** hoặc part BOT không có TOP tương ứng — sửa layout rồi thử lại.

## Phím tắt / modifier

Dialog web — thao tác chuột và form; không có phím tắt plugin riêng ngoài **Esc** khi đang pick profile 2D.

## Lỗi thường gặp

- **Vị trí TOP/BOT không khớp — chặn xuất G-code**: căn lại part trên sheet trên/dưới hoặc nest lại.
- **Layer không cắt**: tag part không map trong tab Layer — thêm mapping tới đúng lối cắt.
- **Profile capture lỗi**: biên dạng không kín, không phẳng Z=0 local, hoặc không phải group/component 2D.
- **Không đọc được nesting**: thiếu `__ABF_Nesting` hoặc cấu trúc part bị đổi tên (phá vỡ contract ABF).

## Liên quan

- [Marking](../04-danh-dau-cnc/marking.md) / [Khử dao](../04-danh-dau-cnc/cnc_relief.md) — tạo geometry layer CNC.
- [Nesting Editor](nesting_editor.md) — thứ tự cắt, outline.
- [Xuất Nesting DXF](nesting_dxf.md) — xuất geometry cho CAM khác.
- [In nhãn](label_print.md) — cùng gate kiểm tra TOP/BOT trước xuất.
