# GIÁO TRÌNH BÀI 3: LÀM CHỦ NHÓM CÔNG CỤ HIỆU CHỈNH & DỰNG HÌNH 3D (EDITING & 3D TOOLS)

* **Thời lượng:** 2.5 - 3 tiếng (Lý thuyết + Thực hành tạo hình 3D + Bài tập dựng tấm ván/module tủ)
* **Mục tiêu bài học:**
  * Biến các hình phẳng 2D (ở Bài 2) thành phôi ván, khối tủ 3D chuẩn kích thước sản xuất.
  * Thành thạo các thao tác nhân bản mảng (Linear Array), xoay đối tượng (Rotate), co kéo chuẩn kích thước (Scale).
  * Làm chủ công cụ **Follow Me** để chạy phào chỉ tân cổ điển, tay nắm âm, bo viền 3D.
  * Hiểu rõ cơ chế khóa trục và bắt điểm 3D tuyệt đối khi lắp ráp các tấm ván.

---

## PHẦN 1: CHI TIẾT CÁC CÔNG CỤ DỰNG HÌNH & HIỆU CHỈNH 3D (75 PHÚT)

### 1. Công cụ Push/Pull (Phím tắt: P) - Đùn khối & Tạo độ dày ván
* **Công dụng:** Biến mặt phẳng 2D thành khối 3D (đùn độ dày ván 17.5mm, 12mm, 9mm...), đục lỗ khoét rãnh âm dương.
* **Thao tác thực hành:**
  1. Bấm phím **P**.
  2. Click chọn mặt phẳng 2D.
  3. Rê chuột theo hướng muốn đùn khối.
  4. Gõ độ dày phôi ván (VD: `17.5`) -> Nhấn **Enter**.
* **Mẹo sản xuất & Phím tắt đúp chuột:**
  * **Đúp chuột trái (Double Click):** Lặp lại đúng khoảng cách Push/Pull của lần thao tác trước (Rất nhanh khi đùn hàng loạt tấm ván có cùng độ dày).
  * **Giữ phím Ctrl + Push:** Đùn khối tạo thành một mặt phẳng mới (tạo nấc/chia đợt).
  * **Đục lỗ / Phay rãnh:** Push mặt phẳng chạm đến mặt đối diện (On Edge / On Face) để đục thủng hoàn toàn lỗ khoét hộc kéo, lỗ dây điện hoặc rãnh cắm hậu tủ.

---

### 2. Công cụ Move / Copy (Phím tắt: M) - Di chuyển & Nhân bản mảng
* **Công dụng:** Dịch chuyển đối tượng, lắp ráp các tấm ván, nhân bản mảng (chia đợt tủ, dãy lam vách).
* **Thao tác di chuyển chuẩn xác (Bắt điểm):**
  1. Chọn đối tượng (đã Make Group/Component).
  2. Bấm phím **M**.
  3. Click chọn **điểm mút/góc phôi (Endpoint)** làm điểm gốc.
  4. Kết hợp phím mũi tên (→, ←, ↑) để khóa trục di chuyển -> Snap vào góc phôi mục tiêu.
* **Thao tác Copy & Nhân bản mảng (Linear Array):**
  * **Copy đơn:** Bấm **M** -> Nhấn phím **Ctrl** (xuất hiện dấu `+` bên cạnh con trỏ) -> Kéo đối tượng ra vị trí mới.
  * **Copy nhân mảng (Phép nhân `*` hoặc `x`):** Copy tấm ván ra khoảng cách `100mm` -> Gõ `5*` hoặc `5x` -> Enter (Sẽ tự tạo thêm 5 tấm ván khoảng cách `100mm`).
  * **Copy chia đều (Phép chia `/`):** Copy tấm ván từ đầu tủ đến cuối tủ (khoảng cách `2000mm`) -> Gõ `/4` -> Enter (Sẽ tự chia đều không gian thành 4 khoảng bằng nhau - Dùng chia đợt tủ áo, tủ giày cực nhanh).

---

### 3. Công cụ Rotate (Phím tắt: Q) - Xoay & Sao chép xoay
* **Công dụng:** Xoay lật vị trí tấm ván (từ ván nằm ngang thành ván đứng), xoay cánh tủ mở, xoay mảng vách lam tròn.
* **Thao tác thực hành:**
  1. Chọn đối tượng -> Bấm phím **Q**.
  2. Đặt thước đo góc (Protractor) lên mặt phẳng muốn xoay (Ấn mũi tên để khóa mặt phẳng thước: Đỏ, Xanh lá, Xanh dương).
  3. Click điểm tâm xoay -> Click điểm định hướng thứ nhất -> Rê chuột xoay góc -> Gõ số góc (VD: `90`) -> Enter.
* **Mẹo Copy xoay:** Bấm **Q** -> Nhấn **Ctrl** -> Xoay góc 45° -> Gõ `3*` -> Enter (Tạo mảng xoay tròn đối xứng).

---

### 4. Công cụ Scale (Phím tắt: S) - Co kéo & Lật đối xứng (Mirror)
* **Công dụng:** Thay đổi kích thước phôi ván, biến đổi tỷ lệ, lật đối xứng ván hông trái thành hông phải.
* **Thao tác co kéo:**
  1. Bấm phím **S** -> Xuất hiện các nút kéo màu xanh (Handles).
  2. **Kéo nút trung tâm (Center handle):** Co kéo 1 chiều (VD: Kéo dài/ngắn chiều cao hông tủ) mà không làm biến dạng độ dày ván.
* **Thao tác Lật đối xứng (Mirror bằng Scale):**
  * Chọn đối tượng -> Bấm **S** -> Click vào nút xanh trung tâm theo hướng muốn lật -> Kéo ngược về phía đối diện -> Gõ `-1` -> Enter.

---

### 5. Công cụ Follow Me - Quét biên dạng 3D theo đường dẫn
* **Công dụng:** Chạy phào chỉ tân cổ điển, soi nẹp tay nắm âm, chạy đường soi bo tròn cạnh bàn/quầy bar.
* **Thao tác thực hành (Cách chuẩn nhất 100% không lỗi):**
  1. Vẽ đường dẫn (Path) - Dùng Line hoặc Arc (VD: Khung chữ nhật của cánh tủ tân cổ điển).
  2. Vẽ biên dạng 2D (Profile) vuông góc với điểm đầu đường dẫn (VD: Mặt cắt phào chỉ 2D).
  3. **Bước 1:** Bấm phím **Space** chọn (highlight) toàn bộ đường dẫn trước.
  4. **Bước 2:** Chọn công cụ **Follow Me**.
  5. **Bước 3:** Click vào mặt phẳng biên dạng 2D -> Biên dạng sẽ tự động chạy kín theo đường dẫn 3D.

---

## PHẦN 2: QUY TRÌNH DỰNG TẤM VÁN CHUẨN SẢN XUẤT (30 PHÚT)

Mọi sản phẩm nội thất CNC đều được cấu thành từ các tấm ván đơn lẻ được lắp ráp lại. Học viên cần tuân thủ **Quy trình 4 bước dựng tấm ván chuẩn**:

```
[Bước 1: Vẽ mặt phẳng 2D (R)] 
      ↓
[Bước 2: Đùn độ dày ván (P: 17.5mm)] 
      ↓
[Bước 3: Đảo mặt trắng ra ngoài (Reverse Faces)] 
      ↓
[Bước 4: Đóng khối ngay lập tức (Make Group / Component)]
```

> **CẢNH BÁO CNC:** Tấm ván sau khi đùn khối 3D **BẮT BUỘC** phải `Make Group` hoặc `Make Component` ngay lập tức. Nếu không đóng khối, các tấm ván khi xếp đè lên nhau sẽ bị dính liền nét (Sticky Geometry), làm hỏng file và không thể xuất file Nesting CNC.

---

## PHẦN 3: BÀI TẬP THỰC HÀNH TẠI LỚP (45 PHÚT)

### Bài tập 1: Lắp ráp Module Tủ Hộc Kéo 3 Tầng chuẩn kích thước
* **Kích thước tủ:** Ngang `500mm`, Sâu `450mm`, Cao `650mm`.
* **Thực hành:**
  1. Dùng **R** và **P** dựng tấm đáy ván 17.5mm. Make Group.
  2. Dựng 2 tấm hông, tấm hậu (9mm). Make Group từng tấm.
  3. Dùng **M + Ctrl** (Copy) và phép chia `/` để chia đều 3 khoảng lồng hộc kéo.
  4. Dùng **S (Scale -1)** để lật hông tủ trái thành hông tủ phải.

### Bài tập 2: Dựng Cánh Tủ Tân Cổ Điển bằng Follow Me
* **Thực hành:**
  1. Vẽ khung cánh tủ kích thước `400mm x 800mm`.
  2. Dùng **F (Offset)** lùi vào `60mm` tạo pano.
  3. Dựng biên dạng soi chỉ 15mm × 10mm ở góc khung.
  4. Sử dụng **Follow Me** để quét chạy chỉ chạy quanh pano cánh tủ.

---
