# Tạo mặt

## Mục đích

Tạo mọi mặt có thể từ các cạnh và đường cong đang chọn

## Khi nào dùng

- Cạnh đã khép kín hoặc gần khép nhưng chưa có face (import DXF, explode, cắt lỗi).
- Cần “vá” mặt phẳng trước khi push/pull, deep push, hoặc contour.
- Chỉ xử lý **cạnh/curve ở selection top-level** — không đụng geometry bên trong group/component đang chọn.

## Thao tác

1. Dùng công cụ Select, chọn một hoặc nhiều **Edge** / **Curve** (có thể chọn cả cung — tool lấy đủ cạnh của curve).
2. Chọn **Tạo mặt** trên toolbar (hoặc menu tương ứng).
3. Plugin chạy một bước undo; status bar báo số mặt đã tạo, hoặc hộp thoại nếu không tạo được.
4. Thanh trạng thái khi chạy: *Chọn cạnh/đường cong rồi chạy để tạo mặt cho chúng*.

## Phím tắt / modifier

- Không có chế độ tool tương tác — chỉ cần selection rồi chạy lệnh.

## Lỗi thường gặp

- **“Chọn ít nhất một cạnh…”:** chưa chọn edge/curve, hoặc chỉ chọn group/component (bên trong không được quét).
- **“Không tạo được mặt nào”:** cạnh không khép thành vòng phẳng kín — kiểm tra khe hở, cạnh không đồng phẳng, hoặc thiếu một đoạn.
- **Tạo ít mặt hơn mong đợi:** chỉ các vòng hợp lệ mới thành face; sửa topology rồi chạy lại.

## Liên quan

- [Vẽ ván](board_draw.md) — tạo ván không cần make face.
- [Contour](contour.md) — cần đường trên mặt phẳng rõ ràng.
- [Deep Push](deep_push.md) — thường cần mặt kín trong group.
