# Contour (Tạo khối theo đường)

## Mục đích

Biến đường vẽ trên một mặt phẳng thành khối solid chạy dọc theo đường

## Khi nào dùng

- Cần nẹp, thanh, profile đặc biệt dọc theo polyline/arc trên một mặt phẳng (mặt ván, mặt tham chiếu).
- Đường gốc giữ nguyên; khối mới nằm trong group riêng cạnh đường.
- Bổ sung chi tiết không muốn vẽ push/pull thủ công từng đoạn.

## Thao tác

1. (Tuỳ chọn) Chọn sẵn cạnh/đường — tool sẽ preview ngay khi mở.
2. Chọn **Tạo khối theo đường** trên toolbar.
3. Di chuột lên đường cần tạo khối; preview dải (band) hiện dọc theo cả chuỗi cạnh liền nhau trên cùng một run.
4. Trên HUD: chỉnh **Dày** (độ cao vuông góc mặt phẳng, mm) và **Rộng** (bề rộng trong mặt phẳng, mm).
5. **Tab** để chọn ô HUD đang nhận số trên VCB; gõ mm, hoặc gõ cả hai một lần dạng `3x6` (dày × rộng).
6. Click (thả chuột trên đường) để tạo khối solid.
7. Hướng dẫn trên màn hình: *Di chuột lên đường cần tạo khối · Tab đổi dày/rộng · gõ "3x6" để đặt cả hai*; khi đã có preview: *Nhấp để tạo khối · Tab đổi dày/rộng · gõ số cho ô đang chọn*.

## Phím tắt / modifier

- **Tab:** chuyển focus giữa chip **Dày** và **Rộng** (số VCB áp vào chip đang focus).
- **VCB:** số mm dương; hoặc `3x6` cho cả dày và rộng (mm world).
- **Esc:** thoát tool.

## Lỗi thường gặp

- **Không có preview:** đường không nằm trên một mặt phẳng ổn định (path cong ra khỏi mặt phẳng) — vẽ lại trên một face phẳng hoặc tách run ngắn hơn.
- **Khối lệch hướng:** kiểm tra mặt phẳng gốc (face chứa cạnh) trước khi click.
- **Sai kích thước:** mặc định thường 3 mm dày × 6 mm rộng; đổi trên HUD trước khi click.

## Liên quan

- [Vẽ ván](board_draw.md) — tấm phẳng cơ bản.
- [Tạo mặt](make_face.md) — khép cạnh thành mặt trước khi contour phức tạp.
- [Deep Push](deep_push.md) — đẩy mặt sau khi đã có khối.
