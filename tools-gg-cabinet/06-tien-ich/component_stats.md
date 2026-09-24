# Thống kê cấu kiện (Component Stats)

## Mục đích

Đọc dữ liệu **tấm thật** trong model và **nesting** (`__ABF_Nesting`) để lập **dự toán chi phí**: phụ kiện liên kết, dán cạnh, danh sách tấm, chi phí khác; chỉnh đơn giá / hệ số; **lưu vào model**; **xuất Excel** (.xls).

## Khi nào dùng

- Sau [ABF Extra Nesting](../05-nesting-va-gcode/abf_extra_nesting.md) hoặc nesting nội bộ — cần bảng khối lượng + báo giá.
- Cập nhật dán cạnh / marking trên tấm rồi **làm mới thống kê** (Refresh) để số liệu tấm khớp model hiện tại.
- Tạo **đối tượng thống kê** 3D trong model để in / trình bày (cần có selection trước).

## Thao tác

1. Mở **Thống kê cấu kiện** từ toolbar hoặc menu (cần **đăng nhập**).
2. Dialog mở với tab **Cấu kiện** và **Phụ kiện**; bảng nhóm: phụ kiện liên kết, đối tượng thống kê, chỉ dán cạnh, tấm, chi phí khác.
3. **Cập nhật lại thống kê theo nesting hiện tại** (Refresh): plugin hỏi có **tạo lại** theo nesting mới hay giữ bản đã lưu — chọn theo nhu cầu.
4. Sửa **đơn giá**, **hệ số**, thêm/xóa dòng (**Thêm dòng** / **Xoá dòng**), đơn vị (cái, tấm, m…).
5. **Lưu vào model**: ghi attribute dictionary `GG_ComponentStats` — khi đóng dialog có thể hỏi lưu trước khi thoát.
6. **Xuất ra Excel**: chọn đường dẫn lưu file (mặc định tên gợi ý `thong_ke`).
7. **Khoá thống kê** / **Mở khoá**: khoá cần đã lưu model; mở khoá nhập **mật khẩu tài khoản**. Khi khoá, không lưu/cập nhật cho tới khi mở khoá.
8. **Tạo đối tượng thống kê**: chọn object trong model trước; đặt tên, kiểu (theo số lượng / theo chiều dài), đơn vị, đơn giá, hệ số — tạo geometry thống kê trong scene.

Số lượng tấm / chi tiết lấy từ **board thật** (ABF is-board) và sheet từ nesting; chỉnh dán cạnh trên tấm rồi Refresh để cột dán cạnh cập nhật.

## Phím tắt / modifier

Plugin **không** gán phím riêng cho dialog thống kê. Gán qua **Extensions → GG Cabinet Tools** nếu cần.

## Lỗi thường gặp

- **Hãy chọn đối tượng trong model trước khi tạo đối tượng thống kê**: chưa có selection khi bấm Tạo.
- **Thống kê đang bị khoá**: mở khoá trước khi lưu/cập nhật.
- **Phải lưu thống kê vào model trước khi khoá**.
- **Sai mật khẩu tài khoản** khi mở khoá.
- **Xuất Excel lỗi** / **Tạo đối tượng thống kê lỗi**: ghi chi tiết `%s` — thử lưu model, kiểm tra quyền ghi thư mục xuất.
- Bảng tấm trống: chưa có nesting / chưa có tấm ABF hợp lệ — hoàn tất luồng [Explode DC → Groups](../05-nesting-va-gcode/explode_to_groups.md) và nesting trước.

## Liên quan

- [Nesting Editor](../05-nesting-va-gcode/nesting_editor.md), [ABF Extra Label](../05-nesting-va-gcode/abf_extra_label.md) — nguồn dữ liệu nesting & nhãn.
- [Marking](../04-danh-dau-cnc/marking.md) — marker ảnh hưởng nhóm phụ kiện / logic quét.
- [In nhãn](../05-nesting-va-gcode/label_print.md) — in tem sau khi đã thống kê tấm.
