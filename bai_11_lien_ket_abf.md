# GIÁO TRÌNH BÀI 11: PHÂN TÍCH CÁC LOẠI LIÊN KẾT & GÁN TỰ ĐỘNG BẰNG PLUGIN (ABF / GG CABINET)

* **Thời lượng:** 3 - 4 tiếng (Lý thuyết kết cấu liên kết + Thực hành gán liên kết tự động + Kiểm tra đường dao CNC)
* **Mục tiêu bài học:**
  * Hiểu rõ nguyên lý hoạt động, ưu/nhược điểm và thông số kỹ thuật của các loại liên kết gỗ công nghiệp phổ biến trên thị trường.
  * Làm chủ công cụ gán liên kết tự động (ABF extension / GG Cabinet Tools) trên SketchUp.
  * Thiết lập chính xác bán kính mũi dao CNC (mũi 3mm, 4mm, 6mm), độ sâu lỗ khoan cam, chốt gỗ và đường soi rãnh hậu.
  * Tự thiết lập và lưu bộ thư viện liên kết chuẩn (Preset) để áp dụng cho mọi dự án xưởng.

---

## PHẦN 1: PHÂN TÍCH CÁC LOẠI LIÊN KẾT TRONG NỘI THẤT HIỆN ĐẠI (60 PHÚT)

### 1. Bảng so sánh các loại liên kết phổ biến

| Loại liên kết | Nguyên lý & Cấu tạo | Ưu điểm | Nhược điểm | Ứng dụng thực tế |
| :--- | :--- | :--- | :--- | :--- |
| **Cam chốt + Chốt gỗ (Cam lock + Dowel)** | Ốc cam kẹp chốt kim loại/nhựa kết hợp chốt gỗ φ 8mm giữ định vị. | Che giấu đầu vít (không lộ vít mặt ngoài), tháo lắp dễ dàng, chắc chắn. | Cần khoan mặt + khoan cạnh (máy CNC khoan ngang hoặc máy xẻ/khoan ngang laser). | Thùng tủ áo, tủ bếp, hộc kéo, kệ trang trí cao cấp. |
| **Ốc âm dương / Chốt âm (Minifix / Rafix / Chốt âm)** | Chốt nhựa/kim loại ăn sâu vào lòng ván, siết bằng ốc xoắn. | Chịu lực xé tốt, không lộ vết liên kết mặt ngoài, thẩm mỹ cao. | Giá thành phụ kiện cao hơn cam chốt. | Đợt tủ di động, tủ kịch trần, đồ rời tháo lắp. |
| **Vít xéo / Vít bắn trực tiếp (Pocket Hole / Confirmat)** | Bắn vít nghiêng 15° hoặc bắn vít thẳng φ 4 × 50mm. | Thi công cực nhanh, chi phí phụ kiện rẻ, không cần máy khoan ngang. | Lộ đầu vít (phải dùng nút nhựa che), khó tháo lắp nhiều lần. | Các vị trí khuất: Xà đỡ tủ bếp, đáy hộc kéo, thùng tủ giá rẻ. |
| **Mộng âm dương CNC (Tenon & Mortise)** | Máy CNC tự xẻ ngàm âm trên tấm hông và mộng dương trên tấm đáy/đợt để sập vào nhau. | Định vị cực kỳ chính xác, không lo lệch ván khi ráp, kết cấu siêu bền. | Phải dùng keo dán (khó tháo rời), tốn thời gian chạy dao CNC. | Khung xương vách uốn cong, quầy bar, cabinet thi công cố định. |

---

### 2. Thông số kỹ thuật lỗ khoan CNC chuẩn xưởng
Khi lập trình trên Plugin SketchUp, phải nhập chính xác kích thước thực tế của phụ kiện kim khí:

* **Ốc Cam 15:** 
  * Lỗ mở khóa cam: Đường kính φ 15mm, độ sâu 12.5 - 13.5mm (cho ván 17.5mm).
  * Lỗ chân cam (mặt ván kề): Đường kính φ 8mm (hoặc φ 10mm tùy loại nở nhựa), độ sâu 24 - 34mm.
  * Khoảng cách từ tâm cam đến mép ván: 24mm hoặc 34mm.
* **Chốt gỗ (Wood Dowel):** Đường kính φ 8mm, chiều sâu lỗ khoan mặt 12mm, lỗ khoan cạnh 22mm.
* **Bản lề bật (Concealed Hinge):** 
  * Chén bản lề: Đường kính φ 35mm, độ sâu 11.5 - 12mm.
  * Khoảng cách tâm chén bản lề đến mép cánh (K-distance): 3 - 5mm (thường đặt 4mm).
  * Vị trí bản lề: Cách mép trên/dưới cánh tủ 100 - 120mm.

---

## PHẦN 2: THỰC HÀNH GÁN LIÊN KẾT TỰ ĐỘNG BẰNG PLUGIN (90 PHÚT)

### 1. Tổng quan giao diện Plugin (ABF / GG Cabinet Tools)
Bộ công cụ gán liên kết tự động gồm các chức năng chính:
* **Connectors / Fitting Setup:** Cấu hình thư viện liên kết.
* **Add Connectors:** Gán cam chốt, chốt gỗ lên giao điểm 2 tấm ván.
* **Hinge Setup & Placement:** Gán lỗ bản lề lên cánh tủ.
* **Slot / Groove Setup:** Tạo rãnh hậu tủ, rãnh nhôm LED.
* **Labeling / Nesting:** Đánh mã chi tiết và xả phôi.

---

### 2. Quy trình 4 bước gán liên kết tự động cho Module Tủ

```
[Bước 1: Kiểm tra va chạm & Mặt Trắng (Front Face)] 
                          ↓
[Bước 2: Thiết lập thông số Fitting Preset (Cam + Chốt gỗ / Bản lề)] 
                          ↓
[Bước 3: Chọn cụm Tủ -> Kích hoạt Gán liên kết tự động] 
                          ↓
[Bước 4: Kiểm tra trực quan & Sửa vị trí lỗi bằng tay]
```

#### Bước 1: Chuẩn hóa mô hình trước khi gán
1. Toàn bộ các tấm ván phải là **Group/Component** độc lập.
2. Kiểm tra mặt ván: Bắt buộc 100% mặt hướng ra ngoài phải là **Mặt Trắng**. (Nếu màu xám, bấm **Reverse Faces**).

#### Bước 2: Thiết lập cấu hình liên kết (Fitting Configuration)
1. Mở khay cài đặt Plugin -> Chọn mục **Cam & Dowel (Cam + Chốt)**.
2. Cài đặt quy tắc khoảng cách:
   * Chiều sâu ván < 300mm: Bố trí **2 Cam**.
   * Chiều sâu ván 300 - 600mm: Bố trí **2 Cam + 1 Chốt gỗ** ở giữa.
   * Chiều sâu ván > 600mm: Bố trí **3 Cam + 2 Chốt gỗ**.
   * Khoảng cách từ đầu tấm ván đến cam đầu tiên: 50mm.

#### Bước 3: Thao tác gán tự động
1. Bôi đen chọn toàn bộ Module Tủ Bếp / Tủ Áo.
2. Bấm nút **Gán liên kết tự động (Auto Add Fitting)** trên thanh công cụ ABF/GG Cabinet.
3. Plugin sẽ tự động phân tích các góc tiếp giáp 90° giữa tấm Hông - Đáy - Nóc - Đợt di động và bắn hệ thống lỗ khoan 3D vào mô hình trong vòng vài giây.

#### Bước 4: Gán lỗ khoét bản lề cánh tủ
1. Chọn tấm Cánh tủ và tấm Hông tủ tương ứng.
2. Chọn công cụ **Add Hinge (Thêm bản lề)**.
3. Chọn kiểu bản lề: **Trùm ngoài (Full Overlay)**, **Nửa trùm (Half Overlay)** hoặc **Lọt lòng (Inset)**.
4. Nhập số lượng bản lề (Chiều cao cánh < 1000mm: 2 bản lề; 1000 - 1800mm: 3 bản lề; > 1800mm: 4 - 5 bản lề).
5. Bấm **Apply**: Các lỗ chén bản lề φ 35mm trên cánh và lỗ vít bắt đế bản lề trên ván hông sẽ tự động tạo hình.

---

## PHẦN 3: KỸ THUẬT TẠO RÃNH HẬU VÀ XẢ RÃNH ĐÈN LED ÂM (45 PHÚT)

### 1. Tạo rãnh hậu tự động (Auto Groove/Slot)
1. Bấm chọn tính năng **Create Slot/Groove**.
2. Thiết lập thông số rãnh:
   * Width (Rộng rãnh): 9.5mm (cho ván hậu 9mm).
   * Depth (Sâu rãnh): 7mm.
   * Offset (Khoảng cách lùi từ lưng tủ): 10mm.
3. Chọn các tấm ván Hông, Đáy, Nóc -> Bấm **Generate**: Plugin sẽ tự động phay rãnh âm 9.5 × 7mm bám theo viền trong của thùng tủ.

### 2. Soi rãnh nhôm LED âm mặt ván
1. Chọn mặt phẳng ván đợt/vách trang trí cần lắp đèn LED.
2. Vẽ đường Line định vị tim đèn LED.
3. Chọn công cụ **Soi rãnh theo đường dẫn**: Nhập độ rộng rãnh 18mm (thanh nhôm LED phổ thông 17mm + 1mm độ rơ), độ sâu 10mm.
4. Bấm kích hoạt: Rãnh phay CNC sẽ xuất hiện trực tiếp trên phôi ván 3D.

---

## PHẦN 4: BÀI TẬP THỰC HÀNH TẠI LỚP & SỬA LỖI (45 PHÚT)

### Bài tập thực hành tại lớp:
* **Đề bài:** Mở file **Module Tủ Bếp Dưới (Khoang Bếp Từ + Hộc Kéo)** đã dựng ở Bài 10:
  1. Gán hệ thống Cam chốt + Chốt gỗ cho tấm hông, tấm đáy và các xà ngang.
  2. Gán 3 bộ ray hộc kéo giảm chấn tự động (tạo lỗ khoan định vị ray bi/ray âm).
  3. Tạo rãnh hậu 9.5mm cho tấm hậu.
  4. Bật chế độ ẩn vỏ tủ (dùng phím **I - Hide Rest of Model**) để kiểm tra xem các đường khoan cam có bị đâm xuyên ra mặt ngoài ván hay không.

### 5 Lỗi thường gặp & Cách xử lý khi gán liên kết:

1. **Lỗi đục ngược mặt cam (Khoan thủng mặt tiền):**
   * *Nguyên nhân:* Tấm ván bị ngược mặt xám (Back Face) hướng ra ngoài.
   * *Xử lý:* Bấm **Reverse Face** đưa mặt trắng ra ngoài -> Bấm **Update Fitting**.
2. **Cam chốt bị dính sát mép ván hoặc đâm vào rãnh hậu:**
   * *Nguyên nhân:* Khoảng cách lùi 50mm vô tình trùng với rãnh hậu lùi 10mm + 9mm.
   * *Xử lý:* Dùng công cụ **Move Fitting** di chuyển con cam lùi vào trong 20 - 30mm.
3. **Lỗi không nhận diện liên kết giữa 2 tấm ván:**
   * *Nguyên nhân:* Hai tấm ván bị hở nhau 0.1mm (không tiếp xúc phẳng) hoặc ván chưa được `Make Group`.
   * *Xử lý:* Dùng công cụ **Move (M)** kiểm tra bắt điểm (Snap) cho 2 tấm ván dính chặt vào nhau.
4. **Mũi dao CNC ăn phạm phôi do sai bán kính mũi:**
   * *Nguyên nhân:* Khai báo trong Plugin dùng mũi dao 6mm nhưng khi gán lại chọn mẫu phụ kiện yêu cầu rãnh 4mm.
   * *Xử lý:* Đồng bộ hóa bán kính mũi dao giữa Plugin trên SketchUp và phần mềm CAM (Aspire).
5. **Trùng lặp quá nhiều cam chốt tại tấm vách vách ngăn trung tâm:**
   * *Nguyên nhân:* Vách ngăn ở giữa bị gán cam từ cả 2 khoang trái và phải đâm vào cùng một độ cao.
   * *Xử lý:* Đặt vị trí cam lệch tầng (Offset Y: 20mm) giữa khoang trái và khoang phải để ốc cam không bị đụng nhau inside tấm ván 17.5mm.

---
