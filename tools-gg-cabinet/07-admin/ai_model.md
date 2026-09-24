# Dựng hình bằng AI (AI Model)

> **Chỉ admin** — tool này không hiện trên toolbar user thường.

## Mục đích

**Dựng hình bằng AI từ bản vẽ** — đưa mặt bằng/mặt đứng/ảnh tham chiếu, mô tả yêu cầu; AI **chỉ thêm** geometry mới (model hiện có được bảo vệ, không sửa/xóa).

## Khi nào dùng

- Thử nhanh dựng **khung kiến trúc** từ PDF/ảnh mặt bằng (chế độ Kiến trúc).
- Dựng **món nội thất** từ ảnh (chế độ Nội thất).
- Admin debug agent dựng hình, API key, thư viện đối tượng server.

## Thao tác

1. Tài khoản **admin** — mở **Dựng hình bằng AI** từ toolbar hoặc menu.
2. Dialog **Dựng hình bằng AI**:
   - **Bản vẽ**: kéo thả mặt bằng, mặt đứng, mặt cắt; **Thêm bản vẽ** / **Bỏ bản vẽ này**.
   - **Yêu cầu** (prompt), **Chế độ** Kiến trúc / Nội thất.
   - Kiến trúc: **Cao tường (mm)**, **Cos cửa (mm)** — kích thước nhập theo **mm world** khi agent đặt geometry.
   - **Mô hình AI**, **API key** (lưu **local** `config.json`, không gửi server lưu trữ).
   - **Bắt đầu dựng** — theo dõi **Nhật ký**, **Lượt**, trạng thái (Sẵn sàng / Đang dựng… / Xong / Lỗi / Đã dừng).
3. Nếu **Bản vẽ không nói rõ**: panel hỏi — trả lời hoặc tick **Cho phép AI ước lượng nhịp**; không dựng khi còn câu hỏi chưa trả lời.
4. **Dừng** khi cần; giới hạn số lượt có thể dừng sớm (*Đã dừng vì chạm giới hạn số lượt*).

Thư viện component server bắt buộc cho agent — nếu **Không tải được thư viện đối tượng từ máy chủ**, chưa có gì để dựng.

## Phím tắt / modifier

**Không** có phím tắt plugin. Gán menu admin qua SketchUp Shortcuts nếu cần.

## Lỗi thường gặp

- **Không tải được thư viện đối tượng…**
- **Dừng khi còn tường chưa dựng** — thiếu thông tin nhịp trên bản vẽ.
- Trạng thái **Lỗi** / **Đã dừng** — xem Nhật ký; kiểm tra API key (**chưa có** trên provider đang chọn).
- **Đang chờ bạn trả lời** — trả lời panel câu hỏi trước khi tiếp tục.
- User không admin: không thấy lệnh.

## Liên quan

- [AI Render](ai_render.md) — render ảnh từ view, không dựng khối.
- [Entity dump (JSON)](entity_dump_json.md) — xuất cấu trúc model sau dựng thử.
- [Vẽ ván](../01-ve-va-chinh-hinh/board_draw.md) — workflow tấm chuẩn sản xuất.
