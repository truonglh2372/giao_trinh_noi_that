# Cập nhật plugin (Update / Khôi phục)

## Mục đích

Toolbar **riêng** *GG Cabinet Tools: Cập nhật / Khôi phục*: kiểm tra bản mới, **tải** bản cập nhật hoặc **hạ về** phiên bản cũ, **áp dụng** gói đã tải — **không yêu cầu đăng nhập** (recovery khi phiên hết hạn).

## Khi nào dùng

- Plugin báo **bắt buộc cập nhật** hoặc có bản mới trên server.
- Sau khi cập nhật lỗi — **khôi phục** bản ổn định trước đó.
- Khác với [Settings](settings.md): Update Launcher tập trung tải/cài file plugin; Settings có bảng phiên bản tương tự nhưng UX tách toolbar.

## Thao tác

1. Bật toolbar **GG Cabinet Tools: Cập nhật / Khôi phục** (View → Toolbars) nếu chưa thấy.
2. Bấm icon/menu **Cập nhật / Khôi phục** — dialog mở:
   - **Phiên bản hiện tại** / **Mới nhất** / (tuỳ chọn) **Khôi phục về**.
3. **Tải bản cập nhật** hoặc **Tải bản khôi phục** — chờ *Đang tải bản …* (có timeout mạng).
4. Khi tải xong: **Cập nhật ngay** / xác nhận *Bạn có muốn cập nhật ngay?* — plugin giải nén và thay file core.
5. **Khởi động lại SketchUp** khi được nhắc (*Đã cài bản … Hãy KHỞI ĐỘNG LẠI SketchUp để áp dụng*).
6. Popup **Có bản cập nhật** (sau ~2s nếu có bản mới): **Cập nhật ngay** hoặc **Để sau**; **Bắt buộc cập nhật** chặn tool cho tới khi cập nhật.

Dialog liệt kê changelog, nút **Tải** / **Chuyển sang** từng dòng phiên bản (xác nhận *Chuyển sang phiên bản …?*).

## Phím tắt / modifier

**Không** có phím plugin. Gán lệnh menu toolbar Update qua SketchUp Shortcuts nếu cần.

## Lỗi thường gặp

- **Tải thất bại** / **Không tải được bản cập nhật**: kiểm tra internet, firewall; thử lại.
- **Tải … không kịp trong N giây**: mạng chậm — thử lại.
- **Không giải nén được** / **Gói không phải bản plugin hợp lệ**: tải lại; không dùng file lẫn.
- **Một số tệp đang được sử dụng**: **restart SketchUp** rồi chạy cập nhật lại.
- **Gói tải về không khớp phiên bản đã chọn**: chưa thay đổi gì — tải lại đúng dòng bảng.
- **Áp dụng bản cập nhật thất bại**: đóng model, restart, thử lại.

Sau mọi cập nhật thành công: **reload extension** bằng restart SketchUp (không chỉ Save model).

## Liên quan

- [Bắt đầu](../00-bat-dau.md) — cài `.rbz` lần đầu.
- [Settings](settings.md) — chuyển phiên bản & layout toolbar trong cùng tài khoản.
- [README](../README.md) — lộ trình tool sau khi nâng bản mới.
