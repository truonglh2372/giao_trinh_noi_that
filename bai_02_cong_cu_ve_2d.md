# GIÁO TRÌNH BÀI 2: LÀM CHỦ NHÓM CÔNG CỤ VẼ 2D CƠ BẢN (DRAWING TOOLS)

* **Thời lượng:** 2 - 3 tiếng (Gồm lý thuyết + thực hành thao tác nhập kích thước chuẩn + bài tập ứng dụng)
* **Mục tiêu bài học:**
  * Làm chủ các công cụ vẽ nét, vẽ hình học cơ bản: Line, Rectangle, Circle, Arc, Offset.
  * Thành thạo kỹ thuật **khóa trục** (mũi tên) và **nhập kích thước chuẩn mm** vào ô Measurements (VCB).
  * Hiểu rõ cơ chế quản lý số cạnh (Segments) của đường tròn/cung tròn để tối ưu file khi CNC.
  * Ứng dụng vẽ trực tiếp các mặt cắt phôi ván, biên dạng tay nắm âm và mặt bằng tủ chuẩn kích thước.

---

## PHẦN 1: NGUYÊN TẮC NHẬP KÍCH THƯỚC & KHÓA TRỤC TRONG SKETCHUP (20 PHÚT)

### 1. Quy tắc nhập kích thước vào ô Measurements (VCB)
* **Không click chuột vào ô Measurements:** Chỉ cần chọn công cụ -> Click điểm đầu -> Di chuyển chuột theo hướng muốn vẽ -> **Gõ trực tiếp số kích thước từ bàn phím** -> Nhấn **Enter**.
* **Dấu phân cách kích thước:** 
  * Khi nhập hình chữ nhật hoặc tọa độ 2 chiều, dùng dấu phẩy `,` (ví dụ: `600,800`).
  * *Lưu ý:* Nếu cài đặt Windows dùng dấu phẩy làm dấu thập phân thì dùng dấu chấm phẩy `;`.

### 2. Nguyên tắc khóa trục (Axis Locking) khi vẽ 2D
Để nét vẽ chuẩn xác 100%, tuyệt đối không vẽ "tự do" trong không gian 3D mà phải khóa theo các hướng trục:
* **Mũi tên Sang Phải (→):** Khóa theo **Trục Đỏ (Red Axis - X)**.
* **Mũi tên Sang Trái (←):** Khóa theo **Trục Xanh Lá (Green Axis - Y)**.
* **Mũi tên Lên (↑):** Khóa theo **Trục Xanh Dương (Blue Axis - Z)**.
* **Mũi tên Xuống (↓):** Khóa song song hoặc vuông góc với đường gióng/cạnh có sẵn.

---

## PHẦN 2: CHI TIẾT TỪNG CÔNG CỤ VẼ 2D (60 PHÚT)

### 1. Công cụ Line (Phím tắt: L) - Vẽ đoạn thẳng
* **Công dụng:** Vẽ các đoạn thẳng, nét đơn, khung phôi ván hoặc hình dáng tự do.
* **Thao tác thực hành:**
  1. Bấm phím **L**.
  2. Click chọn điểm bắt đầu.
  3. Rê chuột theo hướng mong muốn (chú ý đường nét đổi màu Đỏ/Xanh để biết đang song song với trục).
  4. Gõ độ dài (VD: `1200`) -> Nhấn **Enter**.
* **Mẹo sản xuất:** Khi các đoạn thẳng khép kín tạo thành một mặt phẳng (Face), mặt phẳng đó sẽ tự xuất hiện. Nếu mặt không kín, hãy kiểm tra xem có nét nào bị hở hoặc vẽ chéo trục không.

---

### 2. Công cụ Rectangle (Phím tắt: R) - Vẽ hình chữ nhật / Hình vuông
* **Công dụng:** Dựng mặt cắt thùng tủ, cánh tủ, tấm ván MDF/MFC nhanh chóng.
* **Thao tác thực hành:**
  1. Bấm phím **R**.
  2. Click chọn điểm góc thứ nhất.
  3. Kéo chuột theo hướng chéo.
  4. Gõ `Dài,Rộng` (VD: `800,600`) -> Nhấn **Enter**.
* **Rotated Rectangle (Hình chữ nhật xoay):**
  * Dùng khi muốn vẽ tấm ván đặt nghiêng hoặc các mặt hông tủ bị xéo góc.
  * Click điểm 1 -> Click điểm 2 (Xác định chiều dài và góc nghiêng) -> Kéo chuột nhập chiều rộng -> Nhấn **Enter**.

---

### 3. Công cụ Circle (Phím tắt: C) & Polygon (S)(cũ drop) - Vẽ đường tròn & Đa giác
* **Công dụng:** Vẽ lỗ khoan đợt di động, lỗ khoét bản lề âm, khoét lỗ dây điện, chân bàn tròn.
* **Thao tác thực hành:**
  1. Bấm phím **C**.
  2. **QUAN TRỌNG (Cài đặt số cạnh):** Trước khi click điểm tâm, nhìn xuống ô VCB sẽ thấy số cạnh mặc định (thường là `24`).
     * Nếu vẽ lỗ khoan nhỏ (phi 5, phi 35, cam chốt): Gõ `12s` hoặc `16s` -> Enter (giúp giảm nhẹ file).
     * Nếu vẽ mặt bàn tròn lớn cần mịn mượt: Gõ `48s` hoặc `64s` -> Enter.
  3. Click chọn tâm -> Kéo chuột nhập **Bán kính (Radius)** (VD: Khoét lỗ bản lề phi 35mm -> gõ bán kính `17.5`) -> Nhấn **Enter**.

---

### 4. Nhóm công cụ Arc (Phím tắt: A) - Vẽ cung tròn & Bo góc
* **Các dạng cung tròn hay dùng:**
  * **2-Point Arc (A):** Vẽ cung tròn qua 2 điểm (Rất hay dùng để bo góc tủ, vẽ vách trang trí uốn cong).
  * **3-Point Arc:** Vẽ cung tròn đi qua 3 điểm định trước.
* **Cách bo góc (Fillet) chuẩn xác bằng 2-Point Arc:**
  1. Bấm phím **A**.
  2. Click chọn điểm thứ 1 trên cạnh thứ nhất.
  3. Click chọn điểm thứ 2 trên cạnh thứ hai (sao cho đường cung xuất hiện màu **Xanh Tím - Magenta**, báo hiệu tiếp tuyến - Tangent to Edge).
  4. **Double click (click kép)** chuột trái: Cung tròn sẽ tự cắt bỏ góc nhọn và bo tròn hoàn hảo.

---

### 5. Công cụ Offset (Phím tắt: F) - Tạo đường song song / Độ dày ván
* **Công dụng:** Tạo độ dày khung tủ, phào chỉ, tạo khe hở nẹp chỉ, vẽ viền pano cánh tủ.
* **Thao tác thực hành:**
  1. Bấm phím **F**.
  2. Click chọn mặt phẳng hoặc chọn các đoạn đường cần Offset.
  3. Di chuyển chuột vào trong hoặc ra ngoài.
  4. Gõ khoảng cách Offset (VD: Tạo độ dày ván `17.5` hoặc khoảng lùi cánh `2`) -> Nhấn **Enter**.

---

## PHẦN 3: BÀI TẬP THỰC HÀNH TẠI LỚP (45 PHÚT)

### Bài tập 1: Vẽ mặt bằng chi tiết Tủ Bếp Dưới (Tỷ lệ 1:1)
* **Yêu cầu:** 
  * Dùng **R** vẽ khung tổng thể tủ bếp: Dài `3200mm`, Rộng `600mm`.
  * Dùng **F** (Offset) lùi vào `20mm` làm hậu và mặt cánh.
  * Dùng **L** chia các khoang tủ: Khoang chậu rửa (`800mm`), Khoang giá bát/dao thớt (`400mm`), Khoang bếp từ (`800mm`), Khoang hộc kéo (`600mm`).

### Bài tập 2: Vẽ mặt cắt biên dạng Tay Nắm Âm Gỗ (Mặt cắt 2D CNC)
* **Yêu cầu:** 
  * Dùng **R** vẽ phôi ván kích thước `17.5mm x 100mm`.
  * Dùng **L**, **A (2-Point Arc)** và **F** để vẽ biên dạng tay nắm móc J hoặc móc U âm cánh tủ áo.
  * Sử dụng kỹ thuật click kép đường Arc để bo tròn góc R3mm/R5mm mịn mượt cho mũi dao CNC đi qua.

---

## PHẦN 4: NGUYÊN TẮC CNC CẦN LƯU Ý KHI VẼ 2D

1. **Tránh tạo quá nhiều Segments không cần thiết:** Đường tròn/cung tròn có quá nhiều cạnh (`>100s`) sẽ khiến phần mềm CAM (Aspire/ABF) bị giật khi xuất đường dao và làm máy CNC chạy bị khựng, nhấp nhô.
2. **Khép kín mặt phẳng trước khi đùn 3D:** Một hình 2D phải khép kín hoàn toàn và hiển thị mặt phẳng (không bị thủng) thì mới có thể đùn khối 3D (Push/Pull) ở Bài 3.
3. **Luôn giữ mặt màu trắng hướng về phía quan sát:** Nếu vẽ hình 2D xong bị màu xám/tím, bấm chuột phải -> chọn **Reverse Faces** ngay từ bước 2D.

---
