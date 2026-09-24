# Khấu (cross halving join)

## Mục đích

Tạo **vùng cross halving join** (tag / group `ABF_CrossHalvingJoin`) trên các tấm ván được chọn, để CNC khấu chữ thập giữa hai (hoặc nhiều) tấm giao nhau. Tool bật xem **X-ray** và **màu theo tag** trong lúc làm; preview vector dịch trên mặt tấm trước khi nhấp.

## Khi nào dùng

- Hai tấm **giao nhau vuông góc** (hoặc quan hệ pháp tuyến f_face song song/vuông góc theo quy tắc tool) cần **khấu half-lap / cross** trên CNC.
- Cần chỉnh **offset mm**, **kéo dãn hai đầu (khử dao)**, tên tag trên HUD trước khi tạo vùng.
- Làm việc trên **nhiều tấm** đã chọn — mỗi lần click trên mặt tấm tạo vùng cho cặp liên quan.

## Thao tác

1. **Chọn ít nhất hai** group/component **tấm ván** (plugin nhận cặp mặt f/b song song, cùng diện tích).
2. Bật **Khấu** (cross halving join) trên toolbar.
3. Tool isolate selection và bật chế độ xem hỗ trợ; đọc hướng dẫn trên status: di chuột lên **mặt tấm** để xem vector dịch chuyển.
4. (Tùy chọn) Click chip HUD: **Tag**, **Offset (mm)**, **Dãn Khử Dao (mm)** — giá trị **mm world**, có thể đồng bộ cài đặt tài khoản.
5. **Click** mặt tấm cần tạo vùng khấu — plugin tạo group/face trên tag đã cấu hình.
6. Lặp trên mặt khác nếu cần; **Esc** thoát tool (khôi phục hiển thị view trước đó).

## Phím tắt / modifier

Tool **không** dùng Shift/Ctrl cho thao tác tạo khấu chính. Điều chỉnh qua **HUD chip** và **click mặt**.

| Thao tác | Cách làm |
|--------|----------|
| Đổi offset / stretch / tag | Click chip HUD, nhập giá trị |
| Hủy tool | **Esc** |

## Lỗi thường gặp

- **“Chọn ít nhất hai nhóm/component ván…”**: chưa đủ hai tấm hợp lệ trong selection khi khởi chạy.
- **“… không phải dạng tấm ván”**: object thiếu cặp mặt song song cùng diện tích — dùng [Vẽ ván](../01-ve-va-chinh-hinh/board_draw.md) hoặc chuẩn hóa tấm.
- **“… không căn theo trục”**: pháp tuyến f_face không song song/vuông góc trục Z world — xoay/căn tấm [Xoay](../02-xoay-can-chinh/rotate.md) / [Align](../02-xoay-can-chinh/align.md).
- **“Các tấm … pháp tuyến f_face …”**: hai tấm không thỏa quan hệ song song/vuông góc từng cặp — kiểm tra hướng lắp.
- **Cảnh báo chồng lấn group**: vùng khấu mới trùng group `ABF_CrossHalvingJoin` cũ — xóa hoặc đổi vị trí trước khi tạo lại.

## Liên quan

- [Tạo mộng](tenon_helper.md) — join dạng mộng–mortise.
- [Cam lock](cam_lock.md) — liên kết phụ kiện, không khấu thể tích.
- [Unsolid Trim](unsolid_trim.md) — boolean cắt khối sau thiết kế.
- [Khử dao (CNC relief)](../04-danh-dau-cnc/cnc_relief.md) — liên quan tham số “dãn” khử dao trên HUD khấu.
