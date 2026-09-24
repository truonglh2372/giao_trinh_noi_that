# AI Render

> **Chỉ admin** — tool này không hiện trên toolbar user thường.

## Mục đích

**AI Render** — biến **góc nhìn hiện tại** trong SketchUp thành **ảnh render** nội thất/kiến trúc (AI), với prompt, chip mô tả, kiểm soát bám layout model, và tuỳ chọn gửi kèm dữ liệu scene / bản vẽ nét.

## Khi nào dùng

- Demo nhanh phương án cho khách từ model SketchUp (không thay V-Ray/Enscape chính thức).
- Thử material / ánh sáng / phong cách phòng qua prompt thay vì dựng ảnh tay.
- Admin kiểm thử pipeline render server (Gemini / Replicate) trên tài khoản có quota.

## Thao tác

1. Đăng nhập tài khoản **admin** — icon **AI Render** xuất hiện cuối toolbar chính và trong menu Extensions.
2. Dựng **camera** trong SketchUp (tab **Trực tiếp** / Live: xoay view — preview canh khung).
3. Mở **AI Render** → dialog **AI Render**:
   - **Chụp góc nhìn hiện tại** — tạo/chọn cảnh làm input (*Trước* / *Bản nét* nếu bật line-art).
   - **Mô tả**, **Chip prompt** (thư viện chip tích cực/loại trừ), **Mô tả loại trừ**.
   - **Phong cách**, **Ánh sáng**, **Loại phòng**, **Giữ bố cục** (cao = bám geometry), **Kích thước ảnh**, **Nhà cung cấp**, **Seed**, **Số ảnh**.
   - Tuỳ chọn: **Gửi kèm dữ liệu model**; **Gửi kèm bản vẽ nét** cùng góc nhìn.
   - **Sửa prompt** / xem *Prompt gửi cho AI* — tắt chip, sửa tay, **Tạo lại** từ thiết lập.
4. **Render** — chờ kết quả tab **Sau** / lịch sử phiên.
5. **Lưu ảnh** ra disk khi hài lòng.

Cần cửa sổ model mở và cảnh đã chụp trước khi render.

## Phím tắt / modifier

Dialog HTML — **không** có phím tắt riêng trong plugin cho AI Render. Gán lệnh menu admin qua SketchUp Shortcuts nếu cần.

## Lỗi thường gặp

- **Chưa chọn cảnh nào — bấm Chụp…**
- **Không chụp được góc nhìn — hãy mở một cửa sổ model**
- **Phiên đăng nhập đã hết hạn — đăng nhập lại để render**
- **Tài khoản đã hết lượt render**
- **Dịch vụ render chưa sẵn sàng** / **Không kết nối được… — kiểm tra mạng**
- **Dịch vụ không trả về ảnh nào** / **Render thất bại**
- User thường **không thấy tool** — đúng thiết kế; chỉ role admin.

## Liên quan

- [Dựng hình bằng AI](ai_model.md) — dựng geometry từ bản vẽ, không chỉ ảnh.
- [Settings](../06-tien-ich/settings.md) — đăng nhập / phiên.
- [Bắt đầu](../00-bat-dau.md) — admin toolbar order.
