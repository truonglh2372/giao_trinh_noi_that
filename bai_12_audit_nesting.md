# GIÁO TRÌNH BÀI 12: KIỂM TRA LỖI FILE (AUDIT FILE) & XUẤT FILE NESTING SƠ CẤP

* **Thời lượng:** 3 - 4 tiếng (Lý thuyết kiểm soát lỗi + Thực hành gán nhãn, Nesting & Xuất file DXF/CNC)
* **Mục tiêu bài học:**
  * Nắm vững quy trình Audit (kiểm tra lỗi) mô hình 3D trước khi xuất xưởng để tránh rủi ro hỏng phôi ván.
  * Thành thạo các công cụ đánh nhãn (Labeling), sắp xếp sơ đồ cắt ván (Nesting) trực tiếp bằng ABF / Extension Nesting.
  * Cấu hình chính sở đồ xếp ván tối ưu tỉ lệ dừa phôi, thiết lập khoảng cách dao cắt (Toolpath clearance) và lề ván (Border margin).
  * Xuất thành công bộ file giao diện DXF / Sơ đồ sơ cấp chuẩn bị đưa sang phần mềm CAM (Aspire/Alphacam) hoặc máy CNC 1 đầu / 4 đầu.

---

## PHẦN 1: QUY TRÌNH AUDIT FILE - CHECKLIST 8 BƯỚC SỐNG CÒN (60 PHÚT)

Trước khi bấm nút Nesting, học viên bắt buộc phải quét lỗi mô hình theo đúng Checklist 8 bước sau. Sai 1 bước ở công đoạn này có thể làm hư cả tấm ván 1220 × 2440mm tại xưởng.

### Checklist 8 bước kiểm tra file (Pre-Nesting Audit Checklist):

1. **Mặt Ván Trắng (Face Direction Audit):** 
   * *Lỗi:* Tấm ván đảo mặt xám (Back Face) hướng ra ngoài.
   * *Hậu quả:* Máy CNC bị đục lỗ cam/chốt chèn ngược mặt ván.
   * *Cách khắc phục:* Chuyển View sang Style Monochrome -> Bấm **Reverse Faces** cho các mặt xám.
2. **Kiểm tra va chạm & Đè phôi (Clash Detection):** 
   * *Lỗi:* Hai tấm ván đâm xuyên qua nhau 1 - 2mm do bắt điểm sai khi dựng hình.
   * *Cách khắc phục:* Dùng công cụ **Purge / Check Solid** để phát hiện các Group bị đè nhau và dời bắt điểm chính xác.
3. **Độ dày phôi ván (Material Thickness Verification):** 
   * *Lỗi:* Dựng ván 17.5mm nhưng phôi ván thực tế nhập kho là 17mm hoặc 18mm.
   * *Cách khắc phục:* Đo lại chính xác độ dày ván thực tế bằng **Tape Measure (T)** để gán đúng thông số độ sâu đường cắt dao (Cut Depth).
4. **Trạng thái Group/Component:** 
   * *Lỗi:* Chi tiết nằm rải rác ở dạng Explode (chưa gom Group) hoặc bị Group lồng Group quá nhiều cấp (Nested Groups).
   * *Cách khắc phục:* Mở khay **Outliner**, đảm bảo mỗi tấm ván là 1 Group/Component cấp 1 duy nhất.
5. **Độ đồng phẳng của tấm ván uốn cong đã Unfold (Flatten Check):** 
   * *Lỗi:* Tấm ván cong sau khi duỗi phẳng vẫn bị vẹo nghiêng trong không gian 3D.
   * *Cách khắc phục:* Bắt điểm tấm phôi Unfold nằm phẳng tuyệt đối trên mặt phẳng XY (Z = 0).
6. **Khoảng hở cạnh & Dán chỉ PVC (Edgebanding Deductions):** 
   * *Lỗi:* Cánh tủ hay đợt gỗ chưa trừ 1mm - 2mm chỉ nẹp PVC.
   * *Cách khắc phục:* Bật chế độ khai báo nẹp chỉ trong Plugin hoặc trừ thủ công kích thước phôi.
7. **Kiểm tra vị trí lỗ Cam & Rãnh Hậu:** 
   * *Lỗi:* Lỗ cam bị nằm trùng vào lòng rãnh hậu 9mm.
   * *Cách khắc phục:* Bật chế độ hiển thị khung dây **X-Ray (Alt + Z)** để di chuyển lỗ cam lùi ra xa rãnh hậu tối thiểu 20mm.
8. **Đánh nhãn mã chi tiết (Labeling Audit):** 
   * *Lỗi:* Trùng mã chi tiết hoặc không phân loại được đâu là Tủ trên/Tủ dưới.

---

## PHẦN 2: KỸ THUẬT XẮP XẾP SƠ ĐỒ VÁN (NESTING SƠ CẤP) BẰNG ABF (90 PHÚT)

```
[Chọn cụm mô hình đã Audit] 
           ↓
[Khai báo khổ ván & Dao cắt] 
           ↓
[Bấm Run Nesting (Auto Layout)] 
           ↓
[Xử lý xoay tấm ván dọc/ngang vân gỗ] 
           ↓
[Xuất sơ đồ ván & File DXF]
```

### 1. Bảng thiết lập thông số Nesting tiêu chuẩn (Nesting Settings)

| Thông số (Parameter) | Giá trị tiêu chuẩn | Ý nghĩa kỹ thuật |
| :--- | :--- | :--- |
| **Sheet Size (Khổ ván)** | 1220 × 2440mm (hoặc 1220 × 2745mm) | Khổ ván công nghiệp chuẩn MDF/MFC nhập kho xưởng. |
| **Border Margin (Lề ván)** | 10 - 15mm | Khoảng cách an toàn từ viền ngoài tấm ván vào chi tiết cắt (tránh mép ván mẻ/cong). |
| **Part Space / Clearance (Khoảng cách giữa các chi tiết)** | 7 - 10mm | Bằng (Đường kính mũi dao cắt × 2) + 1 - 2mm độ rơ. Ví dụ: Dao 6mm đặt gap 8mm. |
| **Tool Diameter (Đường kính dao)** | 6mm (hoặc 4mm) | Đường kính mũi dao xoắn (Compress router bit) dùng để cắt đứt phôi. |
| **Grain Direction (Hướng vân gỗ)** | Cố định xoay 0° / 180° | Giữ nguyên chiều dọc vân ván MDF Melamine/Veneer. Ván đơn sắc có thể cho xoay 90°. |

---

### 2. Các bước thực hiện Nesting trên ABF Extension

#### Bước 1: Gán nhãn cho chi tiết (Labeling Parts)
1. Bôi đen toàn bộ các Module sản phẩm cần xả ván.
2. Bấm nút **Labeling (Đánh nhãn)** trên thanh công cụ ABF.
3. Plugin sẽ tự động phân tích và gắn thông số lên bề mặt từng tấm ván:
   * **Mã chi tiết:** VD: `TB_DUOI_KHOANG_CHAU - HONG_TRAI`.
   * **Kích thước phôi:** Dài x Rộng x Dày.
   * **Ký hiệu ván dán chỉ:** Hiển thị viền màu tương ứng cạnh cần dán chỉ PVC (1mm/2mm).

#### Bước 2: Thiết lập thông số khổ ván & thuật toán tính toán
1. Kích hoạt công cụ **Nesting Setup**.
2. Chọn loại ván: MDF 17.5mm, MDF 9mm, MFC 17.5mm... (Plugin sẽ tự động gom các tấm có cùng độ dày vào chung 1 nhóm xả phôi).
3. Điền các thông số khổ ván (1220 × 2440mm), Part Space (8mm), Margin (10mm).

#### Bước 3: Chạy thuật toán Nesting & Tối ưu phôi dư
1. Bấm nút **Execute Nesting (Chạy Nesting)**.
2. Phần mềm sẽ tự động trải tất cả các tấm ván 3D ra mặt phẳng 2D và xếp gọn gàng vào các tấm ván 1220 × 2440mm.
3. **Đánh giá hiệu suất phôi (Yield Rate):** Tỉ lệ xếp ván đạt từ **85% - 92%** diện tích tấm ván là tối ưu.
4. **Sắp xếp thủ công (Manual Adjust):** Nếu còn dư diện tích góc ván, dùng công cụ **Move / Rotate** của ABF để dời các tấm nhỏ (đợt di động, xà đỡ) vào lấp đầy khoảng trống.

---

## PHẦN 3: XUẤT FILE DXF / BẢN VẼ SƠ ĐỒ CẮT VÁN (45 PHÚT)

### 1. Phân xuất Layer tiêu chuẩn cho file DXF
Khi xuất từ ABF sang định dạng DXF để nạp vào phần mềm CAM, mô hình 2D sẽ được tự động tách thành các Layer màu riêng biệt:

* **Layer `CUT_OUT` (Màu đỏ):** Đường nét cắt đứt chi tiết (Sử dụng dao 6mm phay lọt lòng).
* **Layer `DRILL_CAM` (Màu xanh lá):** Các lỗ khoan mặt đục cam φ 15mm hoặc φ 8mm.
* **Layer `GROOVE` (Màu xanh dương):** Đường rãnh hèm hậu 9mm hoặc rãnh nhôm LED âm.
* **Layer `LABEL` (Màu trắng/vàng):** Đường nét khắc tên chi tiết/mã tem dán lên mặt ván bằng mũi khắc chữ V-Bit.

### 2. Quy trình xuất File
1. Chọn sơ đồ Nesting 2D hoàn chỉnh.
2. Bấm nút **Export DXF** trên thanh công cụ Plugin.
3. Chọn đường dẫn lưu Folder dự án:
   * Cấu trúc Folder lưu trữ chuẩn xưởng:
     * `01_FILE_GOC_SKETCHUP`
     * `02_FILE_DXF_NESTING` (Chứa các file `Sheet_01_MDF17.5.dxf`, `Sheet_02_MDF17.5.dxf`...)
     * `03_DANH_SACH_CAT_VAN_CUTLIST` (File Excel danh sách phôi & chỉ dán nẹp).

---

## PHẦN 4: BÀI TẬP THỰC HÀNH TẠI LỚP & XỬ LÝ LỖI NESTING (45 PHÚT)

### Bài tập thực hành tại lớp:
* **Đề bài:** Mở file tổng thể **Bộ Tủ Bếp Chữ L** (đã gán liên kết ở Bài 11):
  1. Thực hiện quy trình **Audit 8 bước** để rà soát lỗi mô hình.
  2. Khai báo thông số Nesting: Khổ ván 1220 × 2440mm, Tool 6mm, Gap 8mm, Margin 10mm.
  3. Tiến hành chạy **Nesting tự động** cho toàn bộ ván thùng 17.5mm và ván hậu 9mm.
  4. Xuất bộ file DXF chuẩn bị nạp vào phần mềm CAM.

### 3 Lỗi phổ biến khi chạy Nesting & Cách khắc phục:

1. **Chi tiết bị xếp đè lên nhau trên sơ đồ 2D:**
   * *Nguyên nhân:* Tấm ván chưa được `Make Group` chuẩn hoặc tên Group bị trùng lặp ký tự đặc biệt.
   * *Cách khắc phục:* Xóa nhãn cũ -> Bấm **Purge Unused** trong SketchUp -> Bấm **Re-label** và chạy lại Nesting.
2. **Nesting tốn quá nhiều tấm ván (Tỉ lệ lãng phí cao):**
   * *Nguyên nhân:* Do khóa cứng chiều xoay vân gỗ cho các chi tiết ẩn bên trong (như xà đỡ, chân tủ, tấm đáy âm) không cần vân.
   * *Cách khắc phục:* Vào cài đặt thuộc tính của các tấm xà/chân tủ -> Tắt thuộc tính **Lock Grain (Khóa vân)** để phần mềm tự do xoay ngang/dọc giúp xoay sở vừa khít vào các góc ván thừa.
3. **Tấm ván quá dài không xếp vừa khổ 2440mm:**
   * *Nguyên nhân:* Vách tủ áo hoặc cột lam cao 2600 - 2700mm vượt quá khổ ván chuẩn.
   * *Cách khắc phục:* Báo lỗi màu đỏ trên sơ đồ -> Tiến hành cắt đôi tấm vách thành 2 module ghép chồng hoặc chuyển thông số phôi sang khổ ván vượt khổ 1220 × 2745mm.

---
