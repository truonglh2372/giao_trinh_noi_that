# GIÁO TRÌNH BÀI 4: QUẢN LÝ MÔ HÌNH CHUYÊN NGHIỆP (DATA MANAGEMENT & TEXTURING)

* **Thời lượng:** 2.5 - 3 tiếng (Lý thuyết + Thực hành chuẩn hóa dữ liệu + Xử lý vân gỗ sản xuất)
* **Mục tiêu bài học:**
  * Hiểu sâu sự khác biệt bản chất giữa Group và Component để áp dụng đúng trong thi công tủ/vách.
  * Thành thạo quản lý cây thư mục Outliner và hệ thống Tags (Layer) giúp file siêu nhẹ, không bị giật lag khi dựng toàn bộ căn hộ.
  * Làm chủ kỹ thuật gán vật liệu, xoay hướng vân gỗ (Texture Position) chuẩn chiều cắt ván CNC.

---

## PHẦN 1: BẢN CHẤT GROUP & COMPONENT TRONG SẢN XUẤT (45 PHÚT)

### 1. Phân biệt Make Group vs Make Component

| Đặc tính | Make Group | Make Component |
| :--- | :--- | :--- |
| **Bản chất** | Đối tượng độc lập hoàn toàn. | Đối tượng liên kết hàng loạt (Instances). |
| **Khi chỉnh sửa** | Chỉnh sửa Group A, Group B **không** đổi theo. | Chỉnh sửa Component A, tất cả bản sao **tự động cập nhật**. |
| **Dung lượng file** | Nhân bản nhiều sẽ làm tăng dung lượng file. | Tối ưu dung lượng file, giúp mô hình chạy rất mượt. |
| **Ứng dụng CNC** | Tấm ván đơn lẻ có kích thước/liên kết khác nhau (Ván hông, tấm đợt di động). | Cánh tủ có cùng kích thước, đợt trang trí lặp lại, chân tủ, bản lề, cam chốt, tay nắm. |

### 2. Kỹ thuật Make Unique Component
* **Tình huống:** Tủ áo có 4 cánh tủ giống hệt nhau (Component). Tuy nhiên, cánh ngoài cùng bên trái cần soi thêm rãnh móc tay nắm âm.
* **Thao tác:** Chuột phải vào cánh tủ cần sửa -> Chọn **Make Unique**.
* **Kết quả:** Cánh tủ đó sẽ tách thành một Component độc lập hoàn toàn, khi sửa sẽ không làm ảnh hưởng đến 3 cánh còn lại.

---

## PHẦN 2: QUẢN LÝ TỆP BẰNG OUTLINER VÀ TAGS (LAYER) (45 PHÚT)

### 1. Quản lý cây thư mục Outliner (Cấu trúc cây tủ)
Khay **Outliner** (Window -> Default Tray -> Outliner) hiển thị toàn bộ sơ đồ cấu trúc của file SketchUp.

* **Quy tắc đặt tên Group/Component chuẩn xưởng:**
  * Không để tên mặc định như `Component#1`, `Group`.
  * Đặt tên rõ ràng theo cụm: `TU_BEP_DUOI` -> `KHOANG_CHAU_RUA` -> `HONG_TRAI_17.5mm`.
* **Mẹo sản xuất:** Đặt tên chi tiết chuẩn ngay từ SketchUp giúp khi xuất qua phần mềm Nesting (ABF / GG Cabinet), tem nhãn dán lên tấm ván CNC sẽ in đúng tên chi tiết, thợ xưởng dễ phân loại lắp ráp.

### 2. Quản lý Tags (Layer cũ) & Quy tắc gán Tag
Thanh **Tags** dùng để ẩn/hiện các nhóm đối tượng giúp thao tác nhanh và nhẹ máy.

* **Bộ Tags tiêu chuẩn cho công trình nội thất:**
  * `01_KIENTRUC` (Tường, dầm, sàn, cửa)
  * `02_THIETBI` (Chậu rửa, bếp từ, tủ lạnh, phụ kiện chén đĩa)
  * `03_NOITHAT_GOC` (Khung thùng tủ, đợt ván)
  * `04_CANHTU_VACH` (Hệ cánh tủ, vách ốp trang trí)
  * `05_LIENKET_CNC` (Cam chốt, chốt gỗ, rãnh hậu)
* **QUY TẮC VÀNG:** Luôn vẽ nét 2D và đùn khối ở **Untagged** (Layer 0). Chỉ gán Tag cho khối tổng Group/Component bên ngoài.

---

## PHẦN 3: GÁN VẬT LIỆU VÀ ĐỊNH VỊ CĂN CHỈNH MAP GỖ (45 PHÚT)

### 1. Gán vật liệu (Paint Bucket - Phím tắt: B)
* Bấm **B** -> Chọn màu/Texture từ bảng **Materials** -> Click trực tiếp vào mặt ván hoặc Group để phủ vật liệu.
* **Lưu ý gán vật liệu cho CNC:** Nên gán vật liệu trực tiếp vào **mặt phẳng (Face)** bên trong Group thay vì gán phủ ngoài vỏ Group, giúp phần mềm ABF/CAM nhận diện chính xác mặt dán chỉ và mặt phủ Melamine.

### 2. Xoay hướng vân gỗ chuẩn chiều cắt CNC (Texture Position)
Trong sản xuất ván công nghiệp, chiều vân gỗ quyết định chiều cắt phôi trên máy CNC (thường chiều vân dọc theo chiều dài tấm ván 1220 × 2440mm).

* **Cách kiểm tra & Xoay hướng vân gỗ 90 độ:**
  1. Click đúp chuột vào Group ván -> Chọn mặt phẳng có vân gỗ bị ngược.
  2. Chuột phải -> Chọn **Texture** -> **Position**.
  3. Xuất hiện 4 ghim màu (Pins):
     * **Ghim Đỏ (Move):** Di chuyển vị trí Map vân.
     * **Ghim Xanh Dương (Scale/Distort):** Co kéo biến dạng Map.
     * **Ghim Xanh Lá (Rotate/Scale):** Xoay hướng vân gỗ và phóng to/thu nhỏ Map.
  4. **Thao tác xoay nhanh:** Tại menu ghim -> Chuột phải -> Chọn **Rotate** -> **90** (hoặc **180/270** độ) -> Nhấn **Enter** (hoặc click ra ngoài).

---

## PHẦN 4: BÀI TẬP THỰC HÀNH TẠI LỚP (30 PHÚT)

### Bài tập: Chuẩn hóa dữ liệu cho Module Tủ Áo 3 Cánh
1. **Quản lý Component/Group:**
   * Dựng 3 cánh tủ giống nhau dạng **Component**.
   * Dùng **Make Unique** cho cánh phải để khoét ô kính trang trí.
2. **Thiết lập Outliner & Tags:**
   * Phân chia Tag: Tạo Tag `03_THUNG_TU` và `04_CANH_TU`. Gán đối tượng vào đúng Tag.
   * Đổi tên trong Outliner theo cấu trúc: `TU_AO_P.NGU` -> `CANH_MO_TRAI`.
3. **Xử lý Map vân gỗ:**
   * Gán Map gỗ sồi/gỗ óc chó cho toàn bộ tủ.
   * Kiểm tra và xoay lại hướng vân gỗ của thanh xà ngang tủ bị sai chiều vân dọc thành vân ngang chuẩn thi công.

---
