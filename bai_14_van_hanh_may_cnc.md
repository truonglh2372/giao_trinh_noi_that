# GIÁO TRÌNH BÀI 14: QUY TRÌNH VẬN HÀNH MÁY CNC & XỬ LÝ SỰ CỐ TẠI XƯỞNG

* **Thời lượng:** 3.5 - 4 tiếng (Lý thuyết vận hành + Thực hành trên máy CNC 1 đầu / 4 đầu hút chân không)
* **Mục tiêu bài học:**
  * Thành thạo quy trình vận hành máy CNC từ lúc bật nguồn đến lúc lấy phôi hoàn thiện.
  * Thiết lập gốc tọa độ X, Y, Z; kiểm tra lực hút chân không và chạy thử không tải.
  * Đọc lệnh G-Code cơ bản và mô phỏng hành trình dao trước khi cắt thật.
  * Xử lý các sự cố thường gặp: gãy mũi dao, văng phôi, mẻ chỉ Melamine, lệch tâm lỗ cam.

---

## PHẦN 1: CHUẨN BỊ MÁY & AN TOÀN XƯỞNG (45 PHÚT)

### 1. Kiểm tra trước khi chạy máy
* Bàn hút chân không sạch, không dăm ván kẹt rãnh hút.
* Ván hy sinh / tấm lót MDF còn đủ dày, phẳng, không thủng lỗ lớn.
* Mũi dao đúng loại: Compress 6mm (cắt đứt), mũi khoan φ15 / φ8 (cam, chốt), mũi thẳng 4mm hoặc 6mm (rãnh).
* Hệ hút bụi thông suốt, túi chứa chưa đầy.
* Người vận hành đeo kính bảo hộ, không để tóc/áo lỏng gần trục chính.

### 2. Bật nguồn theo thứ tự
1. Bật nguồn tổng máy CNC.
2. Bật bơm chân không (Vacuum pump).
3. Bật máy hút bụi.
4. Home máy (về gốc máy) nếu bộ điều khiển yêu cầu.
5. Kiểm tra áp suất hút và đèn báo sẵn sàng.

---

## PHẦN 2: NẠP PHÔI, BẮT GỐC VÀ CHẠY MÁY (90 PHÚT)

### 1. Nạp phôi & bắt gốc XY
1. Đưa tấm ván MDF/MFC lên bàn hút chân không.
2. Đẩy sát vào 2 xilanh / chốt định vị góc (0,0) tương ứng XY Datum đã chọn trong Aspire (góc dưới trái).
3. Bật hút chân không, kiểm tra tấm ván không nhấc được bằng tay.
4. Gạt xilanh định vị xuống (nếu máy có) để dao không va chốt khi cắt mép.

### 2. Đo gốc Z (Z-Zero)
* Đặt Auto Tool Sensor lên mặt phôi (Material Surface).
* Cho máy dò Z tự động.
* Xác nhận Z = 0 nằm trên mặt ván, khớp với Job Setup trong Aspire.

### 3. Nạp G-Code và chạy
1. Mở phần mềm điều khiển: NcStudio / Shanlong / Syntec / Mach3.
2. Load file `.nc` / `.tap` / `.txt` tương ứng Post Processor đã xuất ở Bài 13.
3. Chạy Simulation / Dry Run (chạy không tải hoặc Z nâng cao) để xem hành trình dao.
4. Đọc nhanh các lệnh:
   * `G00`: Di chuyển nhanh.
   * `G01`: Cắt thẳng.
   * `G02` / `G03`: Cung tròn.
   * `M03` / `M05`: Bật / tắt trục chính.
5. Bấm **START** khi mô phỏng không va bàn, không đi ra ngoài khổ ván.

Thứ tự gia công tại xưởng: **Khoan cam/chốt → Soi rãnh → Khắc tem → Cắt đứt phôi**.

---

## PHẦN 3: XỬ LÝ SỰ CỐ SỐNG CÒN (60 PHÚT)

### 1. Gãy mũi dao giữa chừng
1. Bấm **Pause / Stop** ngay.
2. Tắt trục chính, tháo mũi gãy, lắp mũi mới cùng đường kính.
3. Đo lại gốc Z.
4. Chạy lại từ số dòng (Block number) ngay trước vị trí gãy, không start lại từ đầu nếu phôi đã cắt một phần.

### 2. Văng phôi nhỏ
* Nguyên nhân: Chi tiết < 200 × 200mm, lực hút yếu, không gắn Tab.
* Xử lý: Dán băng dính 2 mặt, chèn Tab 1.5 × 5mm trong Aspire, hoặc cắt chi tiết nhỏ trên tấm lớn hơn rồi tách tay.

### 3. Mẻ chỉ Melamine
* Nguyên nhân: Feedrate cao, mũi mòn, cắt ngược (Conventional) trên mặt phủ.
* Xử lý: Giảm tốc độ tiến dao, đổi mũi Compress xoắn ngược, chọn **Climb** cho rãnh và cắt ngoài.

### 4. Lệch tâm lỗ cam / sai kích thước
* Kiểm tra Front Face đã đúng chưa trước khi xuất DXF.
* Đo lại độ dày phôi thực tế (17mm / 17.5mm / 18mm) và Cut Depth.
* Kiểm tra Post Processor và đơn vị mm.
* Không cắt khi Simulation cho thấy Z-Max ăn quá sâu xuống bàn hút (ví dụ cắt 18.5mm trên phôi 17.5mm).

### 5. Lệch đường cắt, xước chỉ dán
* Kiểm tra ván có bị trượt khi hút yếu.
* Kiểm tra dao có bị mòn, kẹp collet có chặt.
* Giảm tốc độ góc cua và tăng số lần pec drilling khi khoan sâu.

---

## PHẦN 4: SAU KHI CẮT & BÀI TẬP (30 PHÚT)

### 1. Lấy phôi và đối chiếu
* Tắt hút, gỡ chi tiết, đối chiếu tem nhãn với Cut-list ở Bài 12.
* Kiểm tra lỗ cam φ15, rãnh hậu 9.5 × 7mm, khe hở cánh 2mm trên sản phẩm thật.
* Ghi nhận phôi dư (offcut) để tái sử dụng.

### 2. Bài tập tại lớp
1. Nạp 1 sheet G-Code từ Bài 13 lên máy (hoặc mô phỏng nếu không có máy).
2. Thực hiện đủ quy trình: đặt phôi → hút chân không → dò Z → Simulation → Start.
3. Viết biên bản 1 sự cố giả định (gãy dao hoặc văng phôi) gồm nguyên nhân và 4 bước xử lý.

### 3. Hồ sơ giao xưởng
* File G-Code theo từng sheet.
* Sơ đồ Nesting và danh sách BOM (ván, chỉ dán, cam chốt, bản lề).
* Bản vẽ lắp ráp cho thợ.

---
