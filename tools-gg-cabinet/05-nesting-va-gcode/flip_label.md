# Đảo nhãn (lật mặt trước/sau)

## Mục đích

Chuyển **nhãn ABF** sang **mặt đối diện** của tấm (flip qua thickness), rồi **vẽ lại** `_ABF_Label` — dùng khi mặt gia công thực tế là b_face nhưng workflow vẫn cần tem trên mặt kia trước khi mirror sang sheet `-bottom`.

## Khi nào dùng

- Tấm **phay mặt sau** trong model 3D nhưng nhãn đang nằm trên f_face mặc định.
- Cần đồng bộ hướng đọc tem với cách đặt tấm trên máy (lật tấm trên bàn).
- Bổ sung cho [Xoay nhãn](rotate_label.md) khi vấn đề là **mặt** chứ không chỉ góc 90°.

## Thao tác

1. **Chọn** một hoặc nhiều tấm có `_ABF_Label`.
2. Chạy **Đảo nhãn mặt trước/sau** trên toolbar hoặc menu.
3. Plugin chuyển logic nhãn sang mặt đối diện và **tạo lại** geometry nhãn (edges phẳng, depth 0).

Lưu ý thiết kế ABF: nhãn 3D mặc định luôn trên **f_face** khi gắn lần đầu; sheet **-bottom** trong nesting mang outline mặt sau riêng. Flip label trên tấm 3D khi bạn chủ động đổi mặt mang tem trên board gốc.

## Phím tắt / modifier

Không có phím tắt riêng.

Trong **Nesting Editor**, HUD **Lật tem** áp dụng trên **part đã nest** (tem trên sheet), khác với tool này trên board 3D.

## Lỗi thường gặp

- **Không có nhãn**: chạy Extra Label trước.
- **Nesting lệch TOP/BOT**: sau khi lật/sửa nhiều part, kiểm tra cặp sheet trên–dưới trước [Xuất DXF](nesting_dxf.md) / [G-code](gcode.md) (cảnh báo TOP/BOT).

## Liên quan

- [Xoay nhãn](rotate_label.md) — xoay 90° trên cùng mặt.
- [ABF Extra Nesting](abf_extra_nesting.md) — sheet `-bottom` cho gia công mặt sau.
- [Nesting Editor](nesting_editor.md) — lật tem trên layout 2D.
