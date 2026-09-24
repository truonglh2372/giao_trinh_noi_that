# Deep Push

## Mục đích

Dịch một mặt theo pháp tuyến trong group/component — Tab đảo chiều, VCB nhập khoảng cách mm

## Khi nào dùng

- Đẩy/tụt một mặt **bên trong** group hoặc component (hộc, rãnh, bậc) mà không vào Edit Component thủ công.
- Cần offset mm chính xác theo pháp tuyến mặt (world).
- Lặp lại cùng một offset: double-click mặt khi đã có lần push trước (macro).

## Thao tác

1. Chọn **Push từ bên ngoài đối tượng** trên toolbar.
2. Di chuột lên mặt thuộc group/component; preview highlight mặt đang hover.
3. **Click** mặt để khóa — chuyển sang chế độ kéo dọc pháp tuyến.
4. Kéo chuột theo hướng mong muốn, **hoặc** gõ khoảng cách trên VCB (mm), **hoặc** click lần nữa để chốt.
5. Tool tự thoát sau khi chốt (một thao tác undo).
6. **Double-click** mặt (khi đã lưu offset lần trước) để lặp lại cùng offset mm lên mặt đang trỏ.
7. Thanh trạng thái: *Di chuột lên mặt — nhấp khóa, kéo hoặc nhập mm, nhấp để xác nhận*.

## Phím tắt / modifier

- **Tab** (khi đã khóa mặt, nhiều mặt tham chiếu đo): đổi mặt dùng làm chuẩn đo khoảng cách trên dim (cycle measure face).
- **VCB:** nhập offset mm (dương/âm theo hướng kéo hiện tại).
- Chip **X-ray** trên HUD (nếu có): bật/tắt X-ray trong lúc tool chạy để nhìn mặt khuất.

## Lỗi thường gặp

- **Không bám được mặt:** mặt không thuộc group/component hợp lệ, hoặc bị che — bật X-ray trên HUD.
- **Offset sai chiều:** kéo ngược hướng hoặc nhập số âm trên VCB; kiểm tra dim preview trước khi click chốt.
- **Double-click không lặp:** chưa từng chốt một deep push thành công trong phiên làm việc (macro rỗng).

## Liên quan

- [Dịch vertex](move_vertices.md) — chỉnh điểm thay vì cả mặt.
- [Trim cạnh biên tấm](board_trim.md) — thu mép s-face board.
- [Contour](contour.md) — tạo khối dọc đường thay vì đẩy một face.
