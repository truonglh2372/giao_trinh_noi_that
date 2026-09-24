# Tạo mộng

## Mục đích

Tạo **lưỡi mộng (tenon)** và tùy chọn **lỗ mộng (mortise)** trên các tấm ván tiếp xúc, phục vụ gia công CNC. Tool hiển thị mũi tên anchor trên mặt cạnh tấm; nhấp để tạo mộng theo thông số HUD (số slot, chiều dài, độ sâu, offset mép, tag, v.v.). Có thể mở **Thiết lập mộng** trên toolbar để chỉnh tham số mặc định và đồng bộ tài khoản.

## Khi nào dùng

- Ghép **tấm vuông góc** hoặc **mặt bên tiếp xúc** cần mộng–mortise chuẩn ABF.
- Cần **nhiều mộng** trên một cạnh ghép (slot), với offset mép và chiều dài theo mm world.
- Làm mộng **ngàm / móc câu** (tùy preset trong thiết lập) cho liên kết đặc biệt.

Chọn tấm **trước** khi vào tool hoặc pick tấm trong tool (tool có thể isolate tấm đang làm).

## Thao tác

1. (Khuyến nghị) Mở **Thiết lập mộng** để kiểm tra số mộng, chiều dài (mm), độ sâu (mm), offset mép (mm), tag layer, đường kính dao, tùy chọn cắt mortise.
2. Bật **Tạo mộng** trên toolbar.
3. **Chọn tấm** (group/component ván) nếu chưa chọn — tool nhận dạng tấm qua cặp mặt f/b.
4. Di chuột lên **mặt cạnh** có mũi tên anchor; preview slot hiển thị vị trí mộng.
5. **Click** mũi tên tại slot cần tạo.
6. Giữ **Shift** / **Ctrl** nếu cần mở rộng phạm vi (xem modifier).
7. Sau thao tác, kiểm tra thông báo nếu có mộng không gộp được vào tấm hoặc bị bỏ qua.

Chiều dài tiếp xúc, offset và kích thước mộng tính trong **tọa độ world (mm)**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Tạo thêm mộng ở **mặt đối diện** cùng tấm (cặp face song song) | Giữ **Shift**, rê preview, rồi click |
| Tạo **tất cả slot** trên face (hoặc trên cả cặp face khi Shift) | Giữ **Ctrl** khi click |
| Chỉnh tham số nhanh trên HUD | Click chip (Số lượng, Chiều dài, Độ sâu, Offset, …) |
| Thoát / hủy pick | **Esc**; click vùng trống có thể trở về bước chọn tấm |

**Tab** không dùng trong luồng tạo mộng cơ bản (khác với Cam lock).

## Lỗi thường gặp

- **Không thấy mũi tên**: tấm không phải dạng ván plugin (thiếu cặp mặt f/b), hoặc cạnh tiếp xúc quá ngắn so với ngưỡng tối thiểu (ví dụ vùng contact dưới ~30 mm world → có thể không tạo slot).
- **Slot đã dùng**: anchor xám / không click được — slot trùng vị trí đã tạo (dung sai ~0,5 mm).
- **“Tạo mộng chưa trọn vẹn”**: một phần mộng không tạo được hoặc không merge vào tấm — kiểm tra geometry tấm, độ sâu, và tên tấm trong thông báo.
- **Mortise không cắt**: tắt cắt mortise trong thiết lập hoặc không tìm thấy tấm đối diện coplanar/tiếp xúc đúng.
- **Mộng tự “bóp” ngắn**: chiều dài cạnh ghép gần ngưỡng ladder (30 / 50 mm…) — tool chọn chiều mộng an toàn theo contact thực tế world.

## Liên quan

- [Cam lock / liên kết ngang](cam_lock.md) — đánh dấu ốc cam, không cắt hình mộng.
- [Khấu (cross halving)](khau.md) — vùng khấu chữ thập cho CNC.
- [Unsolid Trim](unsolid_trim.md) — cắt khối sau khi đã có geometry ghép.
- [Thiết lập mộng](../06-tien-ich/settings.md) — nếu mục nằm trong Settings; hoặc lệnh toolbar **Chiều dài, độ sâu, số slot, offset mép** (`toolbar_tenon_settings`).
- [Đánh dấu CNC](../04-danh-dau-cnc/marking.md) — marking profile khác với mộng.
