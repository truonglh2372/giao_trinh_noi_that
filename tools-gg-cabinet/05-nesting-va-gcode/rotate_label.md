# Xoay nhãn

## Mục đích

Xoay **nhãn ABF** (`_ABF_Label`) **90°** trên mặt phẳng tấm cho **các tấm đang chọn** — chỉnh hướng chữ/mũi tên cho khớp chiều vân hoặc cách đọc tem trên bàn CNC.

## Khi nào dùng

- Sau **ABF Extra Label**, mũi tên hoặc số nằm **ngang/dọc** không đúng ý (tấm vuông, xoay model).
- Trước **Extra Nesting** nếu muốn grain trên sheet khớp hướng nhãn 3D (Extra Nesting giữ hướng polygon theo nhãn/trục dài).
- Trong **Nesting Editor** có nút tương đương trên part đã nest — tool toolbar này dùng trên **board 3D gốc**.

## Thao tác

1. Trong model 3D, **chọn** một hoặc nhiều tấm (group/component) đã có `_ABF_Label`.
2. Chạy **Xoay nhãn** trên toolbar hoặc menu.
3. Mỗi lần chạy xoay nhãn **90°** trên mặt f_face (cùng tâm nhãn).
4. Lặp lại lệnh nếu cần 180° / 270°.

Góc xoay áp dụng trong **world space** trên mặt phẳng tấm.

## Phím tắt / modifier

Không có phím tắt riêng — mỗi click toolbar/menu = một bước 90°.

Trong **Nesting Editor**, HUD có **Xoay tem 90°** trên part đã chọn trên sheet (cùng ý nghĩa, khác ngữ cảnh 2D nest).

## Lỗi thường gặp

- **Không đổi gì**: tấm chưa có `_ABF_Label` — chạy [ABF Extra Label](abf_extra_label.md) trước.
- **Chọn nhầm đối tượng**: chỉ tấm chứa nhãn bên trong definition được xử lý.

## Liên quan

- [Đảo nhãn](flip_label.md) — chuyển nhãn sang **mặt đối diện** tấm.
- [ABF Extra Label](abf_extra_label.md) — tạo nhãn ban đầu.
- [Nesting Editor](nesting_editor.md) — xoay tem trên part đã đặt trên sheet.
