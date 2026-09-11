# GIÁO TRÌNH BÀI 8: DỰNG BỘ LAM VÁCH NGĂN PHÒNG KHÁCH & PHÒNG BẾP

* **Thời lượng:** 3 - 4 tiếng (Lý thuyết kết cấu thi công + Thực hành dựng 2 phom vách thực tế)
* **Mục tiêu bài học:**
  * Master kỹ thuật dựng hệ lam vách phức tạp ngăn không gian phòng khách và phòng bếp.
  * Nắm vững kết cấu lắp ráp thực tế: Khe âm dương, rãnh giấu đèn LED, mộng ghép, phào chỉ soi huỳnh cho máy CNC 1 đầu/4 đầu.
  * Dựng thành thạo 2 phong cách phổ biến nhất thị trường: **Hiện đại (tích hợp tủ TV/đợt decor/đèn LED)** và **Tân cổ điển (chạy phào chỉ/huỳnh Pano đối xứng)**.

---

## PHẦN 1: TƯ DUY KẾT CẤU & BẢN VẼ THI CÔNG HỆ LAM VÁCH (45 PHÚT)

### 1. Quy chuẩn kích thước thi công thực tế
* **Cột lam gỗ/MDF hộp:** Kích thước phổ biến 40 × 100mm, 50 × 120mm, hoặc 50 × 150mm.
* **Khoảng cách giữa các cột lam:** Mật độ tiêu chuẩn từ 80mm - 120mm (đảm bảo độ thông thoáng nhưng vẫn phân chia không gian).
* **Vách nan/Lam sóng ốp tường:** Độ dày ván 17.5mm hoặc 9mm soi rãnh, nan rộng 30 - 50mm.
* **Độ rơ liên kết CNC:** Khe sập/mộng âm dương làm rộng hơn phôi 0.2 - 0.5mm để sập vừa khi dán chỉ.

### 2. Tư duy tách lớp sản xuất CNC cho Lam Vách
* **Phần khung/Tủ kệ đế:** Dựng các thùng cabinet chịu lực bằng ván 17.5mm.
* **Phần nan lam:** Dựng dạng hộp 4 mặt ghép mộng 45 độ hoặc xẻ rãnh mộng sập CNC.
* **Phần trang trí:** Khai báo riêng nét soi hèm, rãnh dải nhôm LED âm, phào chỉ soi bằng mũi V-Bit/mũi định hình.

---

## PHẦN 2: THỰC HÀNH DỰNG HỆ LAM VÁCH HIỆN ĐẠI (80 PHÚT)

### Cấu trúc bài tập Hiện đại:
Hệ vách kích thước W3000 × H2700 × D350mm gồm: Tủ kệ TV kẹp chân, mảng vách ván ốp soi rãnh LED, và hệ cột lam đứng có đợt trang trí đâm xuyên.

```
[Khung Tủ Kệ TV Chân] -> [Vách Ốp Soi Rãnh LED] -> [Hệ Cột Lam Đứng] -> [Đợt Decor Xuyên Cột]
```

#### Bước 1: Dựng Khung Tủ Kệ TV dưới
1. Dùng **Rectangle (R)** vẽ mặt bằng tủ 2400 × 350mm. Bấm **P** đùn cao 400mm.
2. Dùng **Offset (F)** và **Line (L)** chia 3 khoang cánh mở / hộc kéo.
3. Đùn lùi hậu 9mm, tạo ván hông, tấm đợt. **Make Group** tủ đế.

#### Bước 2: Dựng Mảng Vách Ván Ốp Soi Rãnh Đèn LED Âm
1. Dùng **R** vẽ vách phẳng hậu 1200 × 2300mm, đùn dày 17.5mm.
2. Dùng **Offset (F)** hoặc **Line (L)** tạo đường soi rãnh nhôm LED âm: Rãnh rộng 22mm, đùn âm vào mặt ván (Push - **P**) sâu 10mm.
3. Gán vật liệu nhôm / dải LED phát sáng vào lòng rãnh.

#### Bước 3: Dựng Hệ Cột Lam Hộp Đứng (Tối ưu Component)
1. Dùng **R** vẽ mặt cắt cột lam 50 × 120mm, đùn cao 2300mm (bằng trần).
2. Tạo độ dày rỗng lòng (Offset 17.5mm) nếu làm lam hộp tiết kiệm ván.
3. Select toàn bộ -> Chuột phải chọn **Make Component** -> Đặt tên `COT_LAM_HIEN_DAI`.
4. Dùng **Move (M) + Ctrl** copy cột lam ra khoảng cách 150mm, gõ `6*` -> Enter để tạo dãy lam tự động.

#### Bước 4: Dựng Đợt Trang Trí Âm Xuyên Cột Lam
1. Vẽ tấm đợt 1800 × 250mm, dày 35mm kẹp đâm xuyên qua 3 cột lam.
2. Dùng công cụ **Intersect Faces (Giao cắt mặt)** để cắt âm ngàm giữ đợt gỗ và cột lam, tạo khớp nối CNC chuẩn xưởng.

---

## PHẦN 3: THỰC HÀNH DỰNG HỆ LAM VÁCH TÂN CỔ ĐIỂN (75 PHÚT)

### Cấu trúc bài tập Tân cổ điển:
Hệ vách lam phân chia phòng có vòm cong trang trí, hệ vách ốp Pano chia ô tỷ lệ vàng, chạy phào chỉ (Molding Profile) nổi và cột lam soi rãnh hạt mướp/chỉ đũa.

#### Bước 1: Dựng Khung Ô Pano Cân Bằng Tỷ Lệ Vàng
1. Dùng **R** dựng khung mảng tường chính 2000 × 2700mm.
2. Dùng **Line (L)** chia mảng tường thành 3 ô Pano đối xứng (Trái - Giữa - Phải).
3. Dùng **Offset (F)** lùi các ô Pano vào 80mm tạo đường khung chỉ.

#### Bước 2: Tạo Mặt Cắt Phào Chỉ 2D (Profile) & Chạy Follow Me
1. Vẽ biên dạng phào chỉ trang trí 2D (Profile) kích thước 35 × 20mm tại góc ô Pano.
2. Bấm phím **Space** chọn đường viền khung ô Pano (Path).
3. Chọn công cụ **Follow Me** -> Click vào mặt phẳng biên dạng phào 2D.
4. **Kết quả:** Hệ phào tân cổ điển ôm trọn ô Pano được tạo hoàn chỉnh. **Make Group** từng khung chỉ.

#### Bước 3: Dựng Cột Lam Soi Chỉ Đũa / Rãnh Âm (Fluted Column)
1. Dựng cột lam tân cổ điển 60 × 150mm, cao 2700mm.
2. Vẽ các bán nguyệt nhỏ R5mm trên mặt trước cột lam.
3. Dùng **Push/Pull (P)** đẩy âm các rãnh chạy dọc từ đỉnh cột xuống chân cột để tạo hiệu ứng cột lam soi chỉ đũa sang trọng.
4. Dùng **Follow Me** chạy đế cột (Base) và đầu cột (Capital) bo phào tân cổ điển.

#### Bước 4: Khai Báo Đường Dao CNC Soi Huỳnh Pano
1. Bật chế độ **Parallel Projection (F2)** nhìn diện đứng vách.
2. Sử dụng đường nét màu riêng biệt để phân tách nét cắt xuyên (Cut-out) và nét cho mũi soi huỳnh Pano (90° V-Bit hoặc Mũi Cầu) khi xuất sang phần mềm CAM (Aspire/Alphacam).

---

## PHẦN 4: BÀI TẬP THỰC HÀNH & NGUYÊN TẮC CNC CẦN NHỚ (40 PHÚT)

### Bài tập về nhà / Tại lớp:
* **Đề bài:** Học viên chọn 1 trong 2 mẫu mặt bằng thực tế (Do giảng viên cung cấp) để dựng hoàn chỉnh hệ lam vách ngăn phòng khách - bếp kích thước 2800 × 2600mm.
* **Yêu cầu bắt buộc:**
  1. Phân chia Tag chuẩn: `01_KHUNG_TU`, `02_COT_LAM`, `03_PHAO_CHI`, `04_VACH_OP`.
  2. Toàn bộ các mặt ván lộ ra ngoài phải là **Mặt Trắng (Front Face)**.
  3. Đặt tên chi tiết rõ ràng trong **Outliner** chuẩn bị cho bài gán liên kết ABF/GG Cabinet.

### 3 Quy tắc CNC sống còn khi dựng Lam Vách:
1. **Dán chỉ cạnh:** Cột lam hộp 4 mặt ghép mộng vát 45° không cần dán chỉ. Nhưng các cột lam xẻ tấm ván hở mép phải khai báo chỉ dán 1mm hoặc 2mm trên SketchUp.
2. **Khe tiêu âm/khe sập:** Khi dựng cột lam cắm vào âm sàn/trần hay đợt gỗ kẹp vào cột, luôn để độ rơ 0.5mm trên 3D để khi sản xuất sơn/phủ Melamine dán chỉ không bị kẹt.
3. **Giới hạn khổ ván:** Chiều cao lam 2700mm vượt quá khổ ván tiêu chuẩn (1220 × 2440mm). Do đó phải thiết kế điểm nối cột lam (chân đế/đầu cột) hoặc chọn khổ ván vượt khổ (1220 × 2745mm) khi lập trình Nesting.

---
