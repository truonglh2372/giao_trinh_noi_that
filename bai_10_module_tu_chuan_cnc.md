# GIÁO TRÌNH BÀI 10: DỰNG MODULE TỦ BẾP & TỦ ÁO TIÊU CHUẨN CNC

* **Thời lượng:** 3.5 - 4 tiếng (Lý thuyết tiêu chuẩn sản xuất + Thực hành dựng module thực tế)
* **Mục tiêu bài học:**
  * Nắm vững các quy chuẩn kích thước ergonomics (nhân trắc học) và kết cấu thi công thực tế cho hệ Tủ Bếp & Tủ Áo ván công nghiệp (MDF/MFC/Picomat).
  * Dựng thành thạo toàn bộ kết cấu phôi ván: Thùng tủ, hậu tủ (soi rãnh/bắn âm), chân tủ, cánh chớm/cánh phủ/cánh lùa, đợt di động.
  * Tích hợp chuẩn xác hệ phụ kiện kim khí (bản lề, ray kéo hộc kéo, giá bát đĩa, tay nâng Blum, thanh treo áo).

---

## PHẦN 1: QUY CHUẨN KÍCH THƯỚC & KẾT CẤU THI CÔNG CNC (45 PHÚT)

### 1. Kích thước tiêu chuẩn sản xuất (Ergonomics)

* **Hệ Tủ Bếp:**
  * **Tủ bếp dưới:** Sâu 600mm (thùng 580mm + cánh 17.5mm + nhô đá 2.5mm), Cao 810 - 860mm (đã gồm đá 18mm và chân nhựa 100mm).
  * **Tủ bếp trên:** Sâu 350mm (thùng 330mm + cánh 17.5mm), Cao 700 - 900mm.
  * **Khoảng cách giữa bếp trên & dưới:** 600 - 650mm (ốp kính/đá).
* **Hệ Tủ Áo:**
  * **Chiều sâu tổng thể:** 600mm cho cánh mở; 650mm cho cánh lùa (trừ 70 - 80mm cho ray lùa).
  * **Chiều cao tiêu chuẩn:** Module dưới 2000 - 2200mm, Module kịch trần 400 - 600mm.

### 2. Kết cấu ghép ván thùng tủ chuẩn CNC
* **Tấm ván hông:** Phủ ngoài tấm đáy và tấm đỉnh (giúp chịu lực ép xả xuống chân tủ tốt nhất).
* **Xà ngang/Xà đỡ (Stretcher):** Tủ bếp dưới dùng xà ván 17.5mm rộng 80 - 100mm (xà nằm ngang đỡ mặt đá, xà đứng bắn Hậu).
* **Hậu tủ:** 
  * *Rãnh âm (Groove):* Ván hậu 9mm hoặc 6mm ăn sâu vào hông/đáy/xà 7mm, cách mép sau 10mm.
  * *Hậu bắn phủ/sập âm:* Bắn đè lưng hông hoặc soi hèm sập âm 9mm.
* **Khoảng hở cánh tủ (Gaps):** Khe hở giữa 2 cánh mở 2mm, khe hở cánh sát tường/sàn 3 - 5mm.

---

## PHẦN 2: THỰC HÀNH DỰNG MODULE TỦ BẾP CHUẨN CNC (90 PHÚT)

### Bài tập 1: Dựng Module Tủ Bếp Dưới (Khoang Chậu Rửa / Bếp Từ)
* **Kích thước module:** W800 x D580 x H790mm (chưa đá, chưa chân nhựa).

#### Bước 1: Dựng Đáy, Hông và Xà Đỡ
1. Dùng **Rectangle (R)** & **Push/Pull (P)** dựng tấm đáy 800 × 580 × 17.5mm. **Make Group**.
2. Dựng 2 tấm hông 580 × 772.5 × 17.5mm kẹp 2 bên tấm đáy. **Make Group** từng tấm.
3. Dựng 2 thanh xà ngang đỡ mặt đá 765 × 80 × 17.5mm (1 xà nằm phía trước, 1 xà đứng phía sau).

#### Bước 2: Tạo Rãnh Âm & Dựng Hậu Tủ 9mm
1. Vào bên trong Group tấm hông, dùng **R** và **P** tạo rãnh soi hậu rộng 9.5mm (cho ván hậu 9mm + độ rơ), sâu 7mm, cách mép sau 10mm.
2. Dựng tấm hậu 779 × 765 × 9mm lọt gọn vào rãnh sập. **Make Group**.

#### Bước 3: Dựng Hệ Cánh Mở & Chân Tủ
1. Dựng 2 cánh mở 398 × 768 × 17.5mm (đã trừ khe hở 2mm giữa 2 cánh và 2mm sát mép trên). **Make Component** cho 2 cánh.
2. Dựng chân ván nhựa/Gỗ lùi vào 50mm so với mặt thùng tủ, cao 100mm.

---

### Bài tập 2: Dựng Module Tủ Bếp Trên (Khoang Bát Đĩa Cánh Nâng Tay Nâng Blum)
* **Kích thước module:** W800 x D330 x H750mm.

1. Dựng thùng tủ: Tấm nóc, đáy, 2 tấm hông (17.5mm), hậu 9mm rãnh âm.
2. Dựng tấm đợt di động: Kích thước lọt lòng trừ 2mm chiều rộng để tháo lắp dễ dàng (763 × 300 × 17.5mm).
3. Dựng 2 cánh xẻ ngang cho tay nâng Blum F22/F25: Cánh trên và cánh dưới chia đôi chiều cao, trừ khe hở 2mm ở giữa để dán chỉ không bị cạ.

---

## PHẦN 3: THỰC HÀNH DỰNG MODULE TỦ ÁO KỊCH TRẦN (75 PHÚT)

### Cấu trúc Module Tủ Áo: W2000 x H2600 x D600mm
Bao gồm **Module Dưới (H2100mm)** và **Module Kịch Trần (H500mm)** ghép chồng lên nhau (Tách module giúp dễ vận chuyển qua cầu thang/thang máy).

```
[Module Tủ Kịch Trần H500mm]
          ↑ (Chồng khớp)
[Module Tủ Áo Chính H2100mm] -> [Hệ Hộc Kéo Âm & Thanh Treo]
```

#### Bước 1: Dựng Module Tủ Áo Chính (Dưới)
1. Dựng khung thùng tổng: Khung hông, đáy, nóc và vách đứng trung tâm chia tủ thành 2 khoang lớn (W982.5mm mỗi khoang).
2. **Thiết kế khoang treo áo dài/áo ngắn:**
   * Khoang bên trái: 1 đợt cố định + 1 thanh treo áo nhôm oval (Dựng hình trụ Ellipse 15 × 30mm).
   * Khoang bên phải: 2 đợt chia ô để đồ gấp + Khung hộc kéo âm 3 tầng.

#### Bước 2: Dựng Module Hộc Kéo Âm Tủ Áo (Drawer Box)
1. Dựng mặt hộc kéo (Drawer Front) lọt lòng hoặc phủ ngoài.
2. Dựng thùng hộc kéo: 2 thành hông, đầu/đôi hộc kéo, đáy 9mm soi rãnh.
3. **Quy tắc trừ hao ray kéo:** Trừ hao 13mm mỗi bên cho ray giảm chấn hộc kéo (Ray bi/Ray âm giảm chấn). Chiều rộng thùng hộc kéo = Lọt lòng thùng tủ trừ 26mm.

#### Bước 3: Dựng Module Kịch Trần (Thượng Tủ)
1. Dựng thùng module kịch trần độc lập W2000 × H500 × D600mm.
2. Chia 4 cánh mở kịch trần ngắn bám theo chiều dọc của cánh tủ dưới để tạo hệ đường nét thẳng tắp từ sàn đến trần.

---

## PHẦN 4: BÀI TẬP THỰC HÀNH & NGUYÊN TẮC QUAN TRỌNG (30 PHÚT)

### Bài tập thực hành tại lớp:
* **Đề bài:** Học viên dựng hoàn chỉnh **Bộ Tủ Bếp Chữ L** gồm: 1 Module góc chữ L, 1 Module chậu rửa, 1 Module bếp từ có hộc kéo gia vị và 1 Module tủ đồ khô kịch trần.
* **Yêu cầu:**
  * Toàn bộ tấm ván phải được `Make Group` hoặc `Make Component` riêng biệt.
  * Phân phân gán Tag chuẩn: `03_THUNG_TU_BEP`, `04_CANH_TU_BEP`.
  * Đặt tên chuẩn trong Outliner (`TB_DUOI_KHOANG_CHAU`, `TB_DUOI_KHOANG_BEP`).

### 4 Quy tắc CNC sống còn khi dựng Tủ Bếp & Tủ Áo:
1. **Quy tắc mặt ván trắng (Front Face):** Tất cả các tấm ván thùng, cánh, hậu bắt buộc 100% bề mặt màu trắng hướng ra ngoài/hướng quan sát để khi xuất ABF không bị khoan ngược lỗ cam.
2. **Quy tắc đặt tên ván trong Outliner:** Tên tấm ván nên ghi rõ độ dày ván (VD: `HONG_TRAI_17.5mm`, `HAU_TU_9mm`) giúp phần mềm CAM tự động phân loại chiều sâu đường cắt.
3. **Mặt khoét âm chậu rửa & bếp từ:** Trên tấm ván mặt đá hoặc xà đỡ tủ bếp, dựng sẵn nét khoét chậu/bếp để xuất bản vẽ định vị cho thợ đá/thợ kim khí.
4. **Trừ hao nẹp chỉ dán cạnh (Edgebanding Deduction):** Trong thiết kế nâng cao, nếu không dùng tính năng tự động trừ chỉ của Plugin (ABF/GG Cabinet), cần tính toán trừ 1mm hoặc 2mm chiều dài/chiều rộng phôi ván cho các cạnh có dán chỉ PVC.

---
