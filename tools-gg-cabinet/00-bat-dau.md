# Bắt đầu với GG Cabinet Tools

## Cài đặt extension

1. Lấy file cài đặt **`.rbz`** theo kênh phân phối của bạn (tải từ trang chủ / email hướng dẫn).
2. Trong SketchUp: **Window → Extension Manager** (hoặc **Preferences → Extensions** tùy phiên bản).
3. Chọn **Install Extension…**, trỏ tới file `.rbz`, xác nhận cài.
4. **Khởi động lại SketchUp** nếu được yêu cầu sau khi cài.
5. Kiểm tra extension **GG Cabinet Tools** đã bật trong Extension Manager.

Sau khi cập nhật plugin bằng tool [Cập nhật / Khôi phục](06-tien-ich/update.md), bạn cũng cần **khởi động lại SketchUp** để mọi file core mới được nạp đúng.

## Đăng nhập & license

Hầu hết lệnh trên toolbar chính chạy qua **`run_if_signed_in`**: nếu chưa đăng nhập, plugin mở hộp thoại **Đăng nhập — GG Cabinet Tools** thay vì chạy tool.

1. Bấm bất kỳ tool nào (hoặc mở [Settings](06-tien-ich/settings.md)) — hộp thoại đăng nhập hiện ra khi cần.
2. Tab **Đăng nhập**: email + mật khẩu, hoặc **Đăng nhập bằng Google** (trình duyệt hệ thống mở riêng — hoàn tất đăng nhập ở đó rồi quay lại SketchUp).
3. Tab **Đăng ký**: tạo tài khoản mới; **xác minh email** trước khi đăng nhập lần đầu (plugin nhắc trên banner nếu chưa xác minh).
4. Cần internet: nếu mất mạng, thông báo *Không có kết nối mạng* xuất hiện khi đăng nhập.
5. **Đăng xuất**: trong Settings → **Đăng xuất**, hoặc menu **Extensions → GG Cabinet Tools** (mục cuối).

Tool **Cập nhật / Khôi phục** nằm toolbar riêng và **không** chặn đăng nhập — dùng được khi cần sửa bản plugin kể cả khi phiên hết hạn.

## Toolbar & menu

### Toolbar chính (tùy chỉnh được)

- Bật thanh công cụ: **View → Toolbars → GG Cabinet Tools**.
- Thứ tự icon mặc định theo danh sách trong plugin; tài khoản **admin** thêm cuối toolbar: AI Render, Dựng hình AI, Entity dump (3 kiểu).
- **Sắp xếp / ẩn icon**: mở [Settings](06-tien-ich/settings.md) → mục **Icon thanh công cụ** — kéo thả, bỏ chọn để ẩn, **Lưu**. Thay đổi chỉ áp dụng sau **khởi động lại SketchUp** (plugin báo rõ trên màn hình).
- **Phím tắt SketchUp**: trong Settings có **Copy tên** / hướng dẫn gán phím trong **Window → Preferences → Shortcuts**, tìm **Extensions → GG Cabinet Tools** — plugin không gán sẵn phím cho từng tool.

### Toolbar Cập nhật (luôn có)

- Thanh riêng: **GG Cabinet Tools: Cập nhật / Khôi phục** — xem [update.md](06-tien-ich/update.md).

### Menu Extensions

**Extensions → GG Cabinet Tools** liệt kê gần như toàn bộ tool (tiện gán phím tắt). Mục admin (AI, entity dump) chỉ có khi tài khoản là admin.

## Đơn vị & tọa độ (mm world)

- Plugin tính **kích thước và khoảng cách trong hệ tọa độ world** của model (bounding box sau transform, chiều dài cạnh, offset placement, v.v.).
- Các tool hiển thị kích thước (ví dụ [Hover dimensions](06-tien-ich/hover_dimensions.md)) dùng `Sketchup.format_length` trên giá trị world — nên đặt **đơn vị model là mm** trong SketchUp (**Window → Model Info → Units**) để VCB và nhãn HUD khớp cách làm việc của giáo trình.
- Khi nhập số trên **VCB** (Measurements), coi giá trị là **mm world** trừ khi tool đó ghi chú khác (ví dụ góc độ).

## Lộ trình học gợi ý

Xem [README](README.md#lộ-trình-học-gợi-ý): vẽ tấm → căn/xoay → ghép mộng → marking CNC → nesting & G-code → tiện ích. Nhóm [07-admin](07-admin/) chỉ dành tài khoản admin, không bắt buộc cho thợ sản xuất.

## Liên quan nhanh

- [Settings](06-tien-ich/settings.md) — ngôn ngữ, Pro, phiên bản plugin, layout toolbar.
- [Cập nhật plugin](06-tien-ich/update.md) — tải bản mới hoặc khôi phục bản cũ.
- [Kho mô hình](06-tien-ich/warehouse.md) — `.skp` và vật liệu trên máy / đồng bộ cloud.
