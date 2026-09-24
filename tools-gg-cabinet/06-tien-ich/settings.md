# Cài đặt (Settings)

## Mục đích

**Cài đặt plugin & quản lý phiên bản**: đăng nhập/đăng xuất, ngôn ngữ, nâng cấp Pro, mã khuyến mãi, **chuyển phiên bản plugin** trên máy, và **tùy chỉnh icon toolbar** (thứ tự / ẩn hiện).

## Khi nào dùng

- Lần đầu dùng hoặc hết phiên — mở Settings để **đăng nhập**.
- Muốn **ẩn bớt icon** toolbar cho gọn màn hình.
- Thử bản plugin cũ hơn / mới hơn từ danh sách phiên bản trên server (khác với toolbar [Cập nhật](update.md) chuyên dụng).
- Nâng **Pro** hoặc nhập **mã khuyến mãi**.

## Thao tác

1. Bấm **Settings** trên toolbar hoặc **Extensions → GG Cabinet Tools** (mục Settings).
2. Nếu chưa đăng nhập: hộp thoại **Đăng nhập** mở trước; sau khi đăng nhập Settings mở lại.
3. Trong dialog **GG Cabinet Tools — Cài đặt**:
   - Xem **phiên bản hiện tại**, trạng thái **Pro** (số ngày còn lại / vĩnh viễn).
   - **Ngôn ngữ**: chọn locale plugin (Vi / En).
   - **Nâng Pro** / thanh toán: làm theo bước QR / hướng dẫn trong dialog.
   - **Mã khuyến mãi**: nhập mã → **Áp dụng** (cần mạng).
   - Bảng **phiên bản**: xem changelog, **Chuyển** sang bản khác — sau khi chuyển plugin nhắc **khởi động lại SketchUp**.
   - **Icon thanh công cụ**: kéo sắp xếp, bỏ chọn **Hiện** để ẩn icon → **Lưu** hoặc **Khôi phục mặc định**. Cả hai đều yêu cầu **restart SketchUp** để toolbar vẽ lại.
   - **Copy tên** / **Gán phím tắt**: copy tên lệnh menu để tìm trong **Window → Preferences → Shortcuts** dưới **Extensions → GG Cabinet Tools**.
   - **Đăng xuất**: kết thúc phiên trên máy này.

Layout toolbar đã lưu **đồng bộ user_config** lên server khi đăng nhập (ẩn/hiện, thứ tự).

## Phím tắt / modifier

Settings là dialog — **không** có phím trong plugin. Gán phím mở Settings qua menu Extensions nếu cần.

## Lỗi thường gặp

- Tool khác báo cần đăng nhập: mở Settings hoặc bất kỳ tool nào để hiện dialog auth; kiểm tra **email đã xác minh** sau đăng ký.
- **Không có kết nối mạng** khi đăng nhập / đổi phiên bản / promo.
- **Chuyển phiên bản** tải lỗi: xem message tải thất bại — thử lại hoặc dùng [Cập nhật / Khôi phục](update.md).
- Đã **Lưu toolbar** nhưng icon chưa đổi: chưa restart SketchUp — làm đúng như dòng trạng thái *Đã lưu — khởi động lại SketchUp để áp dụng*.

## Liên quan

- [Bắt đầu](../00-bat-dau.md) — cài extension, mm world, hai toolbar.
- [Cập nhật plugin](update.md) — toolbar riêng tải/khôi phục bản plugin.
- [Kho](warehouse.md) — cần đăng nhập & quota từ user config.
