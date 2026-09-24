# Uốn cong (Bend)

## Mục đích

Uốn cong nhóm ván thành hình cung

## Khi nào dùng

- Bo góc ván dạng tủ cong, panel có góc vuông cần thành cung (radius mm cố định).
- Làm việc trên **group/component ván** có mặt phẳng và góc vuông phù hợp preview (tool báo preview cung tại góc hover).
- Mặt phẳng không có mặt đối diện vẫn có thể uốn theo chế độ phẳng (flat) khi tool nhận góc hợp lệ.

## Thao tác

1. Chọn **Uốn cong** trên toolbar.
2. Di chuột lên **mặt phẳng** của board (group/component); preview cung và cạnh góc hiện khi trỏ gần góc vuông hợp lệ.
3. Trên **VCB** (nhãn *R(mm), Đoạn*): nhập `bán_kính, số_đoạn` — ví dụ `200,24` (mm và số segment cung).
4. **Giữ Shift** để xem trước cung **lõm** (cove); thả Shift cho cung **lồi** (theo góc concave/convex tool nhận diện).
5. **Click** để áp dụng uốn (một bước undo); di chuột sang góc khác để uốn tiếp nếu cần.
6. Hướng dẫn: *Di chuột lên mặt phẳng để xem trước — nhập bán kính,đoạn (vd: 200,24) — giữ Shift để đổi lồi/lõm — nhấp để uốn*.

## Phím tắt / modifier

- **Shift (giữ):** đảo preview lồi/lõm (cove) tại góc đang hover.
- **VCB:** `R,đoạn` — R tối thiểu 0.1 mm; đoạn ≥ 1 (số đoạn cung).
- **Esc:** thoát tool.

## Lỗi thường gặp

- **Không có preview cung:** không hover đúng board, không có góc vuông trong vùng pick, hoặc bán kính quá nhỏ so với góc — tăng R hoặc đổi góc.
- **Hình uốn gãy:** giảm số đoạn nếu đã nhập quá thấp; tăng đoạn khi R lớn.
- **Uốn sai mặt:** đảm bảo hover đúng mặt seed; kiểm tra Shift (lồi/lõm) trước khi click.

## Liên quan

- [Trải phẳng (Unfold)](unfold.md) — xử lý mặt cong sau uốn cho CNC rãnh.
- [Vẽ ván](board_draw.md) — tạo ván phẳng trước khi bend.
- [Dịch vertex](move_vertices.md) — chỉnh nhẹ sau uốn.
