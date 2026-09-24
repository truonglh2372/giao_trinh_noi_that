# Trải phẳng (Unfold)

## Mục đích

Trải mặt cong (các face liền kề) thành tấm 2D để cắt rãnh CNC

## Khi nào dùng

- Ván cong / strip nhiều face liền kề cần **layout 2D** cho rãnh zigzag, pocket, xương giữ, đường giữ (hold).
- Sau khi uốn hoặc model mặt cong trong ngưỡng góc strip (cài trong cài đặt Unfold).
- **Gói Pro:** tool chỉ chạy khi tài khoản Pro (plugin báo nếu không đủ quyền).

## Thao tác

1. Chọn **Trải phẳng** trên toolbar.
2. Di chuột lên **một mặt** của board cong; preview xanh lá = các cạnh strip sẽ trải; viền cam đậm = mặt seed.
3. Trên HUD:
   - Chọn **POCKET** hoặc **ZIGZAG** (chế độ rãnh / đường chạy dao).
   - Bật/tắt **Outer / Inner / Mid / Union** (xương ngoài, trong, giữa, union) theo nhu cầu CNC.
   - **Bánh răng:** mở hộp thoại cài đặt (ngưỡng góc strip, offset giữ mm, đường kính dao mm, độ dày ván mm, tên group ABF_*, v.v.).
4. **Click** mặt khi preview strip đủ (ít nhất hai face liền kề trong ngưỡng) để trải và tạo các group rãnh + giữ trong model.
5. Hướng dẫn: *Di chuột lên một mặt — các face liền kề trong ngưỡng góc sẽ được trải khi nhấp*.
6. Thanh trạng thái: *Di chuột lên mặt; nhấp để trải strip và tạo nhóm rãnh + giữ*.

## Phím tắt / modifier

- Tool không dùng phím modifier chính — tham số mm chỉnh trên HUD / dialog **Trải phẳng / Unfold** (đường kính dao, offset giữ, độ dày ván, offset xương giữa, v.v., đơn vị mm trong world).
- Click chip HUD để đổi chế độ; không gõ phím tắt riêng ngoài VCB SketchUp (nếu chip mở prompt số).

## Lỗi thường gặp

- **Preview không mở rộng strip:** góc giữa các face vượt **ngưỡng góc strip** — tăng góc trong cài đặt hoặc tách model.
- **Click không trải:** strip < 2 face; seed không thuộc board hợp lệ.
- **Thiếu marking/curve:** plugin có thể báo không đủ marking hoặc strip quá hẹp — kiểm tra [Marking](../04-danh-dau-cnc/marking.md) và tham số độ rộng xương/độ dày ván (mm).
- **Không mở được tool:** cần gói Pro.

## Liên quan

- [Uốn cong](bend.md) — tạo mặt cong trước unfold.
- [Marking](../04-danh-dau-cnc/marking.md) — marking liên quan strip hẹp.
- [Nesting Editor](../05-nesting-va-gcode/nesting_editor.md) — xếp tấm 2D sau trải phẳng.
- Nhóm tiếp: [Ghép & mộng](../03-ghep-va-mong/tenon_helper.md).
