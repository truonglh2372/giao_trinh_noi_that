# GIÁO TRÌNH BÀI 9: DỰNG CÁC CHI TIẾT UỐN CONG & BO TRÒN SẢN XUẤT

* **Thời lượng:** 3 - 4 tiếng (Lý thuyết kết cấu thi công uốn cong + Thực hành dựng hình + Kỹ thuật xả phẳng/Unfold xuất CNC)
* **Mục tiêu bài học:**
  * Master kỹ thuật dựng hình 3D cho các sản phẩm mềm mại, bo cong hiện đại: Quầy bar cong, vách bo góc R, cánh tủ cong, kệ góc bo tròn.
  * Hiểu rõ 2 phương pháp thi công đồ cong thực tế tại xưởng: **Xẻ rãnh lưng ván (Kerf bending)** và **Cắt xương khung ghép ván mỏng (Ribs framework + Flex-ply/MDF 3mm)**.
  * Thành thạo kỹ thuật xả phẳng mặt cong (Unfold / Flatten Surface) để xuất phôi ván CNC chuẩn xác 100%.

---

## PHẦN 1: TƯ DUY KẾT CẤU & BÁN KÍNH BO CONG TRONG THI CÔNG (45 PHÚT)

### 1. Quy chuẩn bán kính uốn cong (Radius R)
* **Bo góc nhẹ (R50 - R150mm):** Thường ứng dụng cho góc tủ, góc bàn, đợt trang trí. Có thể dùng gỗ MDF nẹp bo block đặc hoặc soi rãnh xẻ lưng ván.
* **Uốn cong bán kính vừa (R150 - R500mm):** Cánh tủ cong, quầy lễ tân bo góc, vách ốp cong. Phương pháp xẻ rãnh lưng ván MDF 17.5mm (mỗi rãnh cách nhau 10 - 15mm, sâu 14mm) hoặc ép 2 lớp MDF 6mm.
* **Uốn cong bán kính lớn (R > 500mm):** Vách uốn sóng, quầy bar cong bán nguyệt. Sử dụng kết cấu **Xương CNC (Ribs)** kết hợp dán ốp ván mỏng Flex-ply / MDF 3mm - 6mm.

### 2. Tư duy dựng 3D cho đồ cong chuẩn sản xuất CNC
* **Không vẽ "khối đặc" đại khái:** Trong sản xuất, bề mặt cong được ghép từ bộ xương định hình bên trong và lớp vỏ bọc bên ngoài. Vẽ trên 3D đúng kết cấu thi công giúp tính toán chính xác số lượng ván và vị trí chạy dao CNC.

---

## PHẦN 2: THỰC HÀNH DỰNG CÁC MÔ HÌNH CONG SẢN XUẤT (90 PHÚT)

### Bài tập 1: Dựng Kệ Đợt Góc Bo Tròn & Cánh Tủ Cong (Góc R200mm)
1. **Dựng Khung Tủ Bo Góc:**
   * Dùng **Rectangle (R)** vẽ phôi 600 × 400mm.
   * Dùng **2-Point Arc (A)** tạo cung tròn R200mm tại góc tủ. Double-click để cắt bo góc.
   * Dùng **Offset (F)** lùi vào 17.5mm tạo độ dày thùng tủ.
   * Dùng **Push/Pull (P)** đùn cao 800mm. **Make Group**.
2. **Dựng Cánh Tủ Cong Lọt Lòng:**
   * Vẽ cung tròn bám theo đường cong R200 của thùng tủ.
   * Dùng **Offset (F)** lùi 17.5mm tạo độ dày cánh cong.
   * Đùn cao cánh, trừ khoảng hở hèm cánh 2mm (sát trần/đáy). **Make Component**.

---

### Bài tập 2: Dựng Quầy Bar Cong Lái Bán Nguyệt (Kết cấu Xương CNC)
Hệ quầy bar kích thước L2200 × W800 × H1050mm bo cong 180° đầu quầy.

#### Bước 1: Dựng Khung Xương Định Hình CNC (Ribs Framework)
1. Dùng **Arc (A)** và **Line (L)** vẽ mặt bằng chân quầy bar hình chữ U bo cong tròn 2 đầu.
2. Dùng **Offset (F)** tạo tấm xương đáy dày 17.5mm.
3. Dùng **Move (M) + Ctrl** copy tấm xương đáy lên top (đỉnh quầy) và chia đều các tấm xương sườn đứng dọc theo đường cong (khoảng cách 300 - 400mm/xương).
4. Tạo mộng âm dương trên các tấm xương sườn để máy CNC xẻ rãnh sập tự động. **Make Group** từng tấm xương.

#### Bước 2: Dựng Bề Mặt Vỏ Bọc Cong (Skin Flex-ply)
1. Dùng **Arc** bám theo viền ngoài bộ xương -> Đùn **P** lên chiều cao quầy 1050mm.
2. Cho độ dày lớp vỏ là 6mm (2 lớp MDF 3mm ép đè).
3. Gán Map gỗ/vải/da ốp bề mặt.

#### Bước 3: Mô Phỏng Soi Rãnh Xẻ Lưng Ván (Kerf Bending Simulation)
1. Trên mặt sau của tấm ván cong 17.5mm, vẽ các đường soi rãnh song song rộng 4mm (bằng đường kính mũi dao CNC 4mm), sâu 14mm.
2. Khoảng cách giữa các đường xẻ rãnh (Pitch): 10mm - 12mm tùy theo độ cong R.

---

## PHẦN 3: KỸ THUẬT XẢ PHẲNG BỀ MẶT CONG (UNFOLD SURFACE) XUẤT CNC (45 PHÚT)

Khi thiết kế tấm ván uốn cong trên 3D, mặt ván sẽ ở dạng cong tròn. Tuy nhiên, máy CNC chỉ cắt trên phôi ván phẳng 1220 × 2440mm. Học viên phải duỗi phẳng (Unfold) tấm ván cong ra mặt phẳng 2D.

### Quy trình Xả phẳng chuẩn xác:
1. **Sử dụng Plugin Unfold (Flattery / Curviloft / ABF Unfold):**
   * Chọn bề mặt cong của cánh tủ/vách cong.
   * Kích hoạt công cụ **Unfold / Flatten**.
   * Plugin sẽ tự động tính toán tổng độ dài cung tròn (Arc Length) và trải phẳng tấm ván ra dạng 2D phẳng tuyệt đối.
2. **Kiểm tra Kích thước Phôi Phẳng (Cut-list Validation):**
   * Chuẩn đường kính phôi phẳng = Chu vi đoạn cung cong (L = (π × R × a / 180)).
   * Cộng thêm 10 - 20mm biên độ chừa lề (Stock allowance) cho thợ xưởng xén lề sau khi uốn dán thực tế.
3. **Gán nhãn & Xuất file:**
   * Đặt tên tấm phôi phẳng trong Outliner: `PHOI_VAN_CONG_MDF6MM`.
   * Chuyển qua lớp **Untagged**, chuẩn bị gán liên kết sập xương cho bài Nesting CNC.

---

## PHẦN 4: BÀI TẬP THỰC HÀNH TẠI LỚP & NGUYÊN TẮC THI CÔNG CONG (30 PHÚT)

### Bài tập thực hành tại lớp:
* **Đề bài:** Dựng mô hình 3D hoàn chỉnh cho một **Đảo Bếp Bo Cong 2 Đầu** kích thước 2000 × 900 × 860mm:
  * Bán kính bo cong 2 đầu góc R300mm.
  * Có hộc kéo âm ở mặt thẳng, phần bo cong làm cánh mở cong lọt lòng.
  * Thực hiện xả phẳng 2 tấm cánh cong ra bản vẽ 2D kích thước cắt ván.

### 4 Nguyên tắc vàng khi làm Đồ Cong CNC:
1. **Số lượng phân đoạn (Segments) trong SketchUp:** Khi vẽ cung tròn Arc uốn cong để xả phôi CNC, phải gõ số cạnh `36s` hoặc `48s` để đường cong mượt, tránh tình trạng xả phẳng ra bị gấp khúc, sai kích thước phôi.
2. **Trừ hao độ dày dán chỉ & Lớp keo:** Bề mặt uốn cong dán nhiều lớp ván mỏng sẽ bị nở nhẹ 0.5 - 1mm do keo nẹp (keo Pur/EVA). Cần tính độ rơ chân khe sập.
3. **Quy tắc dán chỉ mặt cong:** Cánh tủ cong chỉ dán chỉ được trên máy dán chỉ cầm tay hoặc máy dán chỉ cong tự động. Khai báo chỉ dán 1mm đầy đủ trên các viền cong.
4. **Mặt trắng Front Face:** Đảm bảo cả tấm ván cong 3D và tấm ván đã Unfold 2D đều hiển thị **Mặt Trắng** hướng ra ngoài.

---
