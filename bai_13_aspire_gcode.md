# GIÁO TRÌNH BÀI 13: THAO TÁC PHẦN MỀM CAM (VECTRIC ASPIRE) & XUẤT FILE G-CODE CẮT CNC

* **Thời lượng:** 3.5 - 4 tiếng (Lý thuyết lập trình đường dao CAM + Thực hành thiết lập Toolpath & Xuất G-code)
* **Mục tiêu bài học:**
  * Nắm vững giao diện công việc và quy trình lập trình cắt gọt trên phần mềm Vectric Aspire (phổ biến nhất cho xưởng gỗ CNC).
  * Import file DXF đã xuất từ ABF/SketchUp vào Aspire, kiểm tra và làm sạch Vector (Vector Validation).
  * Phân loại Layer và tự động gán đường dao (Toolpath Template): Khoan mồi, phay rãnh hậu, khoét lỗ cam, phay huỳnh Pano và cắt đứt phôi (Cut-out).
  * Chọn đúng bộ Post Processor tương thích với hệ điều hành máy CNC (NcStudio, Shanlong, Syntec, Mach3...) và xuất file G-Code (.nc, .tap, .gcode).

---

## PHẦN 1: THIẾT LẬP PHÔI VÁN & IMPORT FILE DXF VÀO ASPIRE (45 PHÚT)

### 1. Khởi tạo phôi ván trong Aspire (Job Setup)
Khi mở phần mềm Vectric Aspire, bấm **Create a new file** và thiết lập thông số phôi trùng khớp với sơ đồ Nesting từ SketchUp:

* **Job Type:** Single Sided (Gia công 1 mặt) hoặc Double Sided (Gia công 2 mặt nếu có lật ván).
* **Width (X):** 1220mm (Chiều rộng tấm ván).
* **Height (Y):** 2440mm (Chiều dài tấm ván).
* **Thickness (Z):** 17.5mm (Nhập đúng độ dày thực tế của phôi MDF/MFC).
* **Z Zero Position:** Chọn **Material Surface** (Lấy gốc Z trên mặt phôi ván) hoặc **Machine Bed** (Lấy gốc Z dưới mặt bàn hút chân không). *Tiêu chuẩn xưởng gỗ nên chọn Material Surface*.
* **XY Datum Position:** Chọn góc dưới bên trái (Bottom-Left Corner) - tương ứng với gốc tọa độ (0,0) trên bàn máy CNC.

---

### 2. Import & Kiểm tra lỗi Vector (Vector Validation)
1. **Import File DXF:** Vào `File` -> `Import` -> `Import Vectors` (hoặc phím tắt `Ctrl + I`) -> Chọn file `Sheet_01_MDF17.5.dxf`.
2. **Kiểm tra Vector hở (Open Vectors):**
   * Bôi đen toàn bộ Vector trên màn hình.
   * Chọn công cụ **Join Open Vectors** (Phím tắt `J`).
   * Nhập độ rơ tolerance 0.1mm -> Bấm **Join**. Tất cả các đường nét cắt đứt phải khép kín hoàn toàn (Closed Vectors) để tránh lỗi bỏ nét khi chạy dao.
3. **Xóa Vector trùng lặp (Delete Duplicates):**
   * Kích hoạt công cụ **Fit Curves to Vectors** hoặc **Vector Cleaner** để xóa các đường nét đè lên nhau gây cháy ván hoặc đâm dao nhiều lần.

---

## PHẦN 2: LẬP TRÌNH BỘ ĐƯỜNG DAO (TOOLPATH TEMPLATE) (90 PHÚT)

Thứ tự chạy dao CNC thực tế tại xưởng tuân theo nguyên tắc: **Khoan mặt -> Phay rãnh âm/Khắc chữ -> Cắt phôi nhỏ -> Cắt phôi lớn**.

```
[1. Drill Toolpath (Khoan Cam/Chốt)] 
                 ↓
[2. Pocket/Profile Toolpath (Soi Rãnh Hậu/Rãnh LED)] 
                 ↓
[3. V-Carve / Engraving Toolpath (Khắc Tên Tem Ván)] 
                 ↓
[4. Profile Toolpath Cut-Out (Cắt Đứt Chi Tiết)]
```

---

### 1. Đường dao 1: Khoan lỗ Cam & Lỗ Chốt Gỗ (Drilling Toolpath)
* **Layer nhận diện:** `DRILL_CAM` / `DRILL_DOWEL`.
* **Loại đường dao:** **Drilling Toolpath**.
* **Cấu hình thông số:**
  * **Start Depth (D1):** 0mm (Bắt đầu từ mặt ván).
  * **Cut Depth (C1):** 13.5mm (Độ sâu lỗ cam) hoặc 12mm (Độ sâu chốt gỗ).
  * **Select Tool:** Chọn dao đục lỗ/mũi soi (VD: Mũi khoan φ 15mm hoặc φ 8mm).
  * **Pec Drilling (Khoan nhấp):** Bật chế độ nhấp dao 4 - 5mm/lần để thoát phoi gỗ dăm, tránh gãy mũi.

### 2. Đường dao 2: Phay Rãnh Hậu & Rãnh Đèn LED (Pocket / Profile Toolpath)
* **Layer nhận diện:** `GROOVE_9MM` / `LED_SLOT`.
* **Loại đường dao:** **Pocket Toolpath** (Phay vét lòng) hoặc **Profile Toolpath** (Chạy theo nét).
* **Cấu hình thông số:**
  * **Start Depth:** 0mm.
  * **Cut Depth:** 7mm (cho rãnh hậu 9mm) hoặc 10mm (cho rãnh LED âm).
  * **Tool:** Mũi dao cắt thẳng/xoắn φ 6mm hoặc φ 4mm.
  * **Clearance Pass / Cut Direction:** Chọn **Climb (Cắt thuận)** để mặt ván Melamine không bị mẻ chỉ.

### 3. Đường dao 3: Cắt đứt chi tiết phôi ván (Profile Cut-Out Toolpath)
* **Layer nhận diện:** `CUT_OUT`.
* **Loại đường dao:** **Profile Toolpath** (Chạy bên ngoài nét - Outside).
* **Cấu hình thông số:**
  * **Start Depth:** 0mm.
  * **Cut Depth:** 17.8mm (Cắt qua độ dày ván 17.5mm thêm 0.3mm để ăn sâu nhẹ vào tấm ván hy sinh Mật độ trung bình/MDF lót sàn bàn hút).
  * **Tool:** Mũi cắt nén xoắn 2 lưỡi (Compress Bit) φ 6mm.
  * **Machine Vectors:** Chọn **Outside / Right** (Chạy phía ngoài viền chi tiết).
  * **Add Tabs / Bridges (Gắn cầu giữ phôi):** Đối với các chi tiết nhỏ (< 200 × 200mm), tích chọn **Add tabs** (dày 1.5mm, dài 5mm) để tránh hút chân không không chặt làm văng phôi va vào lưỡi dao.

---

## PHẦN 3: TỰ ĐỘNG HÓA GÁN LAYER VÀ XUẤT FILE G-CODE (60 PHÚT)

### 1. Kỹ thuật tạo Bộ khuôn đường dao tự động (Toolpath Template)
Để không phải thiết lập thông số dao thủ công cho từng sheet ván, ta dùng tính năng tự động liên kết Layer (Vector Selection Associate):

1. Trong bảng cài đặt từng Toolpath -> Bấm vào nút **Selector...** ở góc dưới.
2. Tích chọn **Automatic selection with vector of this type**.
3. Chọn đúng tên Layer tương ứng (VD: Layer `CUT_OUT` liên kết với Toolpath Cắt Đứt).
4. Bấm **Save Toolpath Template** -> Lưu file `GIA_CONG_MDF_17.5MM.vtpro`.
5. Từ các sheet sau, chỉ cần Import DXF -> Bấm **Load Toolpath Template** -> Toàn bộ đường dao tự động gán chuẩn xác 100% trong 3 giây.

---

### 2. Mô phỏng 3D (Toolpath Simulation) & Kiểm tra va chạm
1. Chọn **Preview All Toolpaths**.
2. Quan sát tốc độ chạy dao, góc đâm dao và kết quả gọt phôi 3D trên màn hình.
3. Kiểm tra xem mũi dao có ăn quá sâu xuống mặt bàn hút chân không hay không.

---

### 3. Xuất file G-Code chuẩn Post Processor cho máy CNC
1. Bấm vào biểu tượng **Save Toolpaths** (Hình đĩa mềm).
2. Tích chọn **Output all visible toolpaths to one file** (Nếu dùng máy CNC 4 đầu tự động đổi dao) hoặc xuất riêng từng đợt dao (Nếu dùng máy CNC 1 đầu thay dao thủ công).
3. **Chọn bộ Post Processor (Định dạng máy):**
   * Máy dùng cạc điều khiển NcStudio: Chọn `Ncstudio Arcs (mm) (*.nc)`.
   * Máy dùng cạc Shanlong / RichAuto A11: Chọn `G-Code Arcs (mm) (*.tap)` hoặc `AutoCAD (*.gcode)`.
   * Máy dùng hệ điều hành Syntec: Chọn `Syntec ATC Arcs (mm) (*.txt)`.
4. Bấm **Save Toolpath(s)** -> Đặt tên file `SHEET_01_MDF17.5MM.nc`.

---

## PHẦN 4: BÀI TẬP THỰC HÀNH TẠI LỚP & NGUYÊN TẮC VẬN HÀNH (45 PHÚT)

### Bài tập thực hành tại lớp:
* **Đề bài:** Học viên lấy file DXF `Sheet_01` đã xuất từ Bài 12:
  1. Nạp file vào phần mềm Vectric Aspire.
  2. Tạo Toolpath Template đầy đủ 3 đường dao: Khoan lỗ cam (13.5mm), Soi rãnh hậu (7mm), Cắt đứt phôi (17.8mm).
  3. Mô phỏng cắt 3D và kiểm tra các góc cắt.
  4. Xuất file G-Code định dạng `.nc` dành cho máy CNC cạc NcStudio.
