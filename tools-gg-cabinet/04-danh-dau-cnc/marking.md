# Marking (đánh dấu CNC)

## Mục đích

Đánh dấu **đường cắt line** (layer `ABF_LINE_CUT`) hoặc **vùng pocket** (layer `ABF_POCKET`) trên mặt tấm để downstream nesting và G-code nhận đúng toolpath. Tool tạo geometry marking dưới dạng group con trong tấm, theo preset (line, area, hình tùy chỉnh).

## Khi nào dùng

- Cần **rãnh, đường cắt nội bộ, pocket LED, khoét tay nắm** trên mặt phay trước khi chạy pipeline ABF / nesting.
- Muốn **lặp cùng một kiểu mark** nhiều lần — dùng preset trên HUD hoặc lưu preset trong Cài đặt Marking.
- Mark **hình 2D tùy chỉnh** (profile từ face/edge hoặc group phẳng) dọc cạnh tấm, có thể chia **nhiều điểm neo** trên một cạnh.

## Thao tác

1. Bật tool **Đánh dấu CNC** trên toolbar.
2. Trên HUD: chọn **Line** hoặc **Area** (hai nút đầu), rồi chọn **preset** (cột chip bên dưới). Biểu tượng **bánh răng** mở **Cài đặt Marking** (offset, layer, ring, đánh mặt sau, giới hạn preview phức tạp, thứ tự preset).
3. **Rê chuột** lên cạnh hoặc mặt tấm ván — preview wireframe hiện theo offset (mm world).
4. **Click** cạnh để khóa cạnh; chỉnh offset bằng **kéo chuột** hoặc gõ **mm trên VCB** (Measurements), rồi **click** lần nữa để **commit** group marking.
5. Click **vùng trống** (không trúng tấm) khi đang khóa cạnh → **hủy khóa** mà không đặt mark.
6. Preset **hình tùy chỉnh**: chọn edge/face trong model, bấm **Lưu hình** trên HUD để thêm preset; hoặc cấu hình trong dialog Cài đặt (xoay 90° CCW/CW, preview).
7. Kết quả nằm trong tấm với tên/layer theo preset; dùng **Thống kê cấu kiện** nếu cần kiểm tra loại mark.

Mọi offset, rộng area, lùi đầu cạnh trong tool đều tính bằng **mm trong tọa độ world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Chuyển Line ↔ Area | Click chip **Line** / **Area** trên HUD |
| Chọn preset | Click chip preset trên HUD |
| Nhập offset (mm world) | VCB khi cạnh đã khóa — commit ngay sau khi nhập |
| Chế độ Area: đổi neo offset (giữa cạnh / centroid / …) | **Tab** khi đang khóa cạnh hoặc hover cạnh (preset area/custom) |
| Marker dạng **điểm** (hình/group): số điểm neo dọc cạnh | VCB **`/N`** (ví dụ `/5`) hoặc chip **Điểm neo** trên HUD |
| Marker dạng điểm: xem trước / đặt **tất cả** neo cùng lúc | Giữ **Shift** trên cạnh đã khóa, rồi click |
| Marker dạng điểm: đặt **một** neo (khi đã arm `/N`) | Snap tới neo, click (cạnh vẫn khóa để đặt tiếp) |
| Bật/tắt nhãn kích thước trên preview | Chip **Dim** trên HUD |
| Thoát tool | **Esc** |

Preset bật **Ring (khép kín)** tự tạo chuỗi khép kín khi khóa cạnh; không dùng Shift cho ring.

Thanh trạng thái khi vào tool: rê lên cạnh tấm, click để tạo nhóm con marking.

## Lỗi thường gặp

- **Preview biến mất / không commit**: biên quá phức tạp (vượt giới hạn segments/góc nhọn trong Cài đặt) — đơn giản hóa hình hoặc nới giới hạn (admin).
- **Lưu hình thất bại**: chưa chọn edge hoặc face hợp lệ trong model.
- **Mark lệch mặt**: bật **Đánh mặt sau** trong preset nếu cần đặt trên mặt đối diện.
- **Layer không ra G-code**: kiểm tra tên layer trong preset khớp mapping trong Quản lý G-code.

## Liên quan

- [Dán cạnh (edge band)](edge_band.md) — đánh dấu cạnh dán, không phải pocket/line CNC.
- [Khử dao (CNC relief)](cnc_relief.md) — vòng tròn relief tại góc, khác marking line/pocket.
- [Intersect Mark](intersect_mark.md) — mark tiết diện giao giữa hai tấm tiếp xúc.
- [ABF Extra Label](../05-nesting-va-gcode/abf_extra_label.md) → [Nesting](../05-nesting-va-gcode/abf_extra_nesting.md) — sau khi mark, cần nhãn và nesting sheet.
