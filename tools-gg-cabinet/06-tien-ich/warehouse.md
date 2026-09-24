# Kho (Warehouse)

## Mục đích

**Kho GG Cabinet Tools**: duyệt và quản lý **mô hình `.skp`**, **vật liệu V-Ray**, và **asset** trên máy; khi đã đăng nhập, đồng bộ với cloud theo tài khoản (upload/download, giới hạn dung lượng theo gói).

## Khi nào dùng

- Chèn module tủ / phụ kiện chuẩn từ thư viện `.skp` thay vì vẽ lại.
- Áp dụng hoặc quản lý **vật liệu V-Ray** tập trung (tab Vật liệu).
- Đồng bộ kho giữa máy bàn và laptop (Pro/admin có hạn mức cao hơn free).

## Thao tác

1. **Đăng nhập** (nếu chưa — mở Kho sẽ nhảy hộp thoại đăng nhập trước).
2. Mở **Kho** từ toolbar hoặc menu **Extensions → GG Cabinet Tools**.
3. Tab **Mô hình**:
   - **Tìm kiếm** theo tên trong danh sách.
   - **Làm mới** danh sách sau khi copy file `.skp` vào thư mục kho.
   - **Đổi thư mục mô hình** nếu thư viện nằm ổ khác (chọn thư mục gốc).
   - Chọn mô hình để **đặt vào model** (thao tác trong dialog — import/instance theo UI tab).
   - **Xóa** mô hình khỏi máy (xác nhận *Xóa "%s" khỏi máy này?*) — không nhầm với xóa trên cloud nếu có đồng bộ.
4. Tab **Vật liệu V-Ray** / **Asset**: duyệt, áp dụng hoặc quản lý tài nguyên tương ứng (thông báo lỗi/giai đoạn hiển thị trong dialog nếu thiếu file).
5. Khi có mạng và đã đăng nhập: plugin **đồng bộ manifest** với server (tự chạy sau đăng nhập / theo chu kỳ watcher) — upload file mới, tải bản cloud mới hơn local.

Giới hạn dung lượng (file đơn / tổng kho) lấy từ cấu hình user trên server — free thấp hơn Pro/admin; upload vượt cap bị chặn trước khi gửi API.

## Phím tắt / modifier

**Không** có phím tắt riêng trong plugin cho dialog Kho. Gán lệnh menu **Kho** qua SketchUp Shortcuts nếu cần.

## Lỗi thường gặp

- **Không tìm thấy mô hình**: thư mục kho sai hoặc chưa có `.skp` — **Đổi thư mục** / copy file rồi **Làm mới**.
- **Đang tải…** lâu: danh sách lớn hoặc đang sync cloud — đợi, kiểm tra mạng.
- Upload/sync thất bại: vượt **dung lượng** gói hoặc mất kết nối — xem dung lượng trong Settings / user config, thử lại khi có mạng.
- Vật liệu V-Ray không áp dụng: thiếu proxy/texture — đọc thông báo lỗi cụ thể trên tab Vật liệu.

## Liên quan

- [Settings](settings.md) — đăng nhập, gói Pro, dung lượng kho.
- [Chọn theo vật liệu](color.md) — chọn nhanh object cùng material trong model đang mở.
- [Bắt đầu](../00-bat-dau.md) — cài extension & đăng nhập.
