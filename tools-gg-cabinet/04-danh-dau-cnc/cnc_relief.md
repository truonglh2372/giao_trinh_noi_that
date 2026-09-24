# Khử dao (CNC relief)

## Mục đích

Đánh dấu **vòng tròn khu đạo (relief)** tại góc tấm — điểm khử dao cho CNC — bằng geometry trên layer/tag cấu hình. Tool hỗ trợ preview đường kính, đặt nhanh nhiều góc **cùng mặt phẳng**, và cài đặt đường kính preview/final.

## Khi nào dùng

- Tấm góc vuông cần **bo/tròn góc phay** hoặc vùng tránh dao ở góc sau khi cắt contour.
- Cần **đồng bộ nhiều góc** trên cùng một mặt phẳng (mặt đứng, mặt ngang) trong một thao tác.
- Muốn chỉnh **đường kính relief** (mm) trước khi đặt hàng loạt.

## Thao tác

1. **Chọn một hoặc nhiều Group/ComponentInstance** (tấm) trong model.
2. Bật tool **Vòng tròn khu đạo CNC** (hoặc menu tương ứng).
3. Tool **cô lập/isolate** tạm các tấm đã chọn để dễ pick góc.
4. **Rê chuột** tới **góc ứng viên** (preview vòng); **click** để đặt relief tại góc đó.
5. Trên HUD chỉnh:
   - **Preview** — đường kính vòng xem trước (mm).
   - **Circle** — đường kính relief cuối (mm).
   - **Tag** — layer/tag gán cho vòng.
   - **Thông báo** — bật/tắt notice trên màn hình khi đặt.
   - **Loop** — chế độ vòng (theo cài đặt khu đạo).
6. Tool **Cài đặt khu đạo** (toolbar riêng): đường kính preview/final mặc định, tag, chế độ loop.
7. Sau khi đặt xong, tool báo số vòng đã đặt và đường kính thực (mm).

Đường kính và khoảng cách luôn **mm world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Đổi chế độ offset góc (OUTER / INNER trên HUD) | **Tab** |
| Đặt relief cho **mọi góc cùng mặt phẳng** với góc đang hover | Giữ **Shift**, click |
| Nhập đường kính preview hoặc final (mm) | VCB: số mm, hoặc dạng **`w5`** (theo gợi ý tool) |
| Thoát / hủy tool | **Esc** |

Thanh trạng thái khi chọn tấm: nhấp góc; **Shift** cho cùng mặt phẳng.

## Lỗi thường gặp

- **“Chọn Group/Component trước”**: chưa selection tấm trước khi chạy tool.
- **Không thấy góc ứng viên**: xoay camera; góc phải thuộc tấm đã chọn và hợp lệ với chế độ OUTER/INNER.
- **Relief không ra G-code**: kiểm tra **tag** trùng layer mapping trong Quản lý G-code.

## Liên quan

- [Marking](marking.md) — line/pocket trên mặt, khác relief góc.
- Menu **Cài đặt khu đạo** trên toolbar (cùng nhóm CNC relief).
- [G-code Manager](../05-nesting-va-gcode/gcode.md) — map layer relief sang toolpath.
