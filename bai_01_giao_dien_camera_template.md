# GIÁO TRÌNH BÀI 1: GIAO DIỆN, THAO TÁC CAMERA & THIẾT LẬP TEMPLATE CHUẨN

* **Thời lượng:** 2 - 3 tiếng (Gồm lý thuyết + thực hành thao tác trực tiếp)
* **Mục tiêu bài học:**
  * Thành thạo thao tác góc nhìn, điều khiển camera không giật lag, không mất phương hướng.
  * Thiết lập giao diện làm việc tối ưu với bộ phím tắt dành riêng cho làm sản xuất CNC.
  * Tự tạo và lưu **Template mẫu chuẩn xưởng** (đơn vị mm, Style nét mỏng, hiển thị màu mặt ván) giúp tiết kiệm 90% thời gian chuẩn bị file sau này.

---

## PHẦN 1: LÝ THUYẾT & TƯ DUY NỀN TẢNG (30 PHÚT)

### 1. Tư duy làm việc trong SketchUp Sản Xuất CNC
* **Độ chính xác tuyệt đối (100%):** Trong vẽ kiến trúc/diễn họa, sai số 1-2cm có thể chấp nhận. Nhưng trong dựng hình CNC sản xuất, sai số **1mm** cũng sẽ làm hỏng toàn bộ liên kết cam chốt, hở chỉ dán hoặc kẹt hộc kéo.
* **Hệ tọa độ 3 trục (X, Y, Z):**
  * **Trục đỏ (Red - X):** Chiều ngang (Chiều dài tấm ván/chiều rộng tủ).
  * **Trục xanh lá (Green - Y):** Chiều sâu (Chiều sâu tủ/mặt bàn).
  * **Trục xanh dương (Blue - Z):** Chiều cao (Chiều cao tủ/vách).

---

## PHẦN 2: THỰC HÀNH CẤU HÌNH GIAO DIỆN & PHÍM TẮT (45 PHÚT)

### Bước 1: Bật các thanh công cụ (Toolbars) cần thiết
Vào **View -> Toolbars** và tích chọn các thanh công cụ sau:
1. **Large Tool Set:** Thanh công cụ vẽ chính (nằm bên trái màn hình).
2. **Views:** Các góc nhìn chiếu bằng, chiếu đứng, chiếu cạnh.
3. **Styles:** Chuyển đổi chế độ hiển thị (X-Ray, Shaded With Textures, Hidden Line).
4. **Tags (Layer cũ):** Quản lý ẩn/hiện chi tiết.
5. **Measurements (Value Control Box - VCB):** Khung nhập kích thước (kéo xuống góc dưới bên phải).

### Bước 2: Thiết lập hệ thống Phím tắt (Shortcuts) chuẩn xưởng
Vào **Window -> Preferences -> Shortcuts**. Tìm và gán các phím tắt tối ưu sau:
* `Make Group`: Gán phím **G** (hoặc **Alt + G**)
* `Make Component`: Gán phím **Shift + G** (hoặc **G**)
* `Parallel Projection` (Góc nhìn song song không biến dạng): Gán phím **F2**
* `Perspective` (Góc nhìn phối cảnh): Gán phím **F3**
* `Hide Rest of Model` (Ẩn các đối tượng ngoài Group đang chỉnh sửa): Gán phím **I** (Rất quan trọng khi soi liên kết bên trong tủ)
* `Hide` (Ẩn đối tượng): Gán phím **H**
* `Unhide All` (Hiện lại tất cả): Gán phím **Shift + H**

---

## PHẦN 3: LÀM CHỦ THAO TÁC CAMERA & QUY TẮC MẶT VÁN (45 PHÚT)

### 1. Thao tác chuột & Điều khiển Camera
* **Xoay góc nhìn (Orbit - Phím tắt O hoặc Giữ con lăn chuột):** Xoay không gian 3D xung quanh tâm quan sát.
* **Di chuyển góc nhìn (Pan - Giữ Shift + Giữ con lăn chuột):** Trượt màn hình sang trái, phải, lên, xuống.
* **Phóng to/Thu nhỏ (Zoom - Lăn con lăn chuột):** Phóng to/thu nhỏ tại đúng vị trí con trỏ chuột đang chỉ vào.
* **Zoom Extents (Ctrl + Shift + E):** Phóng to toàn bộ mô hình vừa vặn màn hình (Cứu nguy khi bị trôi/mất hút góc nhìn).

### 2. Phân biệt Parallel Projection & Perspective
* **Perspective (Phối cảnh 3D):** Các đường thẳng hội tụ về điểm xăm. Dùng để xem tổng thể không gian nội thất, render ảnh.
* **Parallel Projection (Chiếu song song):** Không có điểm xăm, các đường thẳng song song giữ nguyên tỷ lệ. **BẮT BUỘC dùng chế độ này khi kiểm tra mặt cắt, xả phẳng ván và kiểm tra liên kết CNC.**

### 3. Quy tắc Mặt Trắng (Front Face) & Mặt Xám (Back Face)
* Trong SketchUp, mỗi bề mặt 3D luôn có 2 mặt: **Mặt Trắng (Mặt thật/Front)** và **Mặt Xám/Tím (Mặt trái/Back)**.
* **Quy tắc CNC:** Tất cả các bề mặt ván hướng ra ngoài phải là **Mặt Trắng**. Nếu để mặt xám hướng ra ngoài, khi xuất file qua ABF/Nesting sẽ bị **ngược mặt khoan lỗ cam** hoặc **lỗi không nhận diện được chỉ dán cạnh**.
* **Thao tác đảo mặt:** Chuột phải vào mặt xám -> Chọn **Reverse Faces**.

---

## PHẦN 4: THIẾT LẬP VÀ LƯU TEMPLATE CHUẨN XƯỞNG SẢN XUẤT (30 PHÚT)

Thực hiện lần lượt các bước sau để tạo một file Template hoàn chỉnh:

1. **Thiết lập đơn vị đo (Units):**
   * Vào **Window -> Model Info -> Units**.
   * Format: Chọn **Decimal / Millimeters (mm)**.
   * Precision (Độ chính xác): Chọn **0mm** (Không để số thập phân để tránh bị lẻ kích thước phôi).
   * Tích chọn **Enable length snapping**: Đặt là **1mm**.

2. **Tối ưu Style hiển thị (Style mượt nhẹ file):**
   * Vào **Window -> Default Tray -> Styles -> Edit**.
   * Phần **Edge Settings**: Bỏ tích *Profiles*, bỏ tích *Endpoints*, bỏ tích *Jitter*. (Chỉ giữ lại *Edges*). Việc này giúp đường nét mảnh, màn hình chạy nhẹ mượt gấp 3 lần khi vẽ công trình lớn.

3. **Cấu hình Shadow & Fog (Tắt hiệu ứng nặng máy):**
   * Tắt hoàn toàn **Shadows** (Bóng đổ) và **Fog** (Sương mù) để tránh giật lag khi dựng hình nhiều chi tiết.

4. **Xóa nhân vật mặc định (Người mẫu scale):**
   * Bấm phím **Space** (Select) -> Click chọn hình người mặc định trên màn hình -> Nhấn **Delete**.

5. **Lưu file làm Template Mặc định (Save As Template):**
   * Vào **File -> Save As Template...**
   * Name: Đặt tên `Template_NOI_THAT_CNC_MM`
   * File Name: `Template_NOI_THAT_CNC_MM.skp`
   * Tích chọn ô: **Set as default template** (Đặt làm mẫu mặc định).
   * Bấm **Save**. Từ nay về sau, mỗi khi mở SketchUp lên, phần mềm sẽ tự động áp dụng đúng môi trường chuẩn này!

---

## BÀI TẬP THỰC HÀNH TẠI LỚP / VỀ NHÀ

1. **Thực hành thao tác phím:**
   * Luyện tập chuyển đổi liên tục giữa phím **F2** (Parallel) và **F3** (Perspective).
   * Luyện tập ấn **I** để ẩn các đối tượng xung quanh và ấn **I** lần nữa để hiện lại.
2. **Thực hành tạo Template:**
   * Tự tay cài đặt toàn bộ thông số đơn vị mm, phím tắt, Style nét mỏng và lưu thành Template mang tên cá nhân học viên.
   * Đóng hoàn toàn SketchUp và mở lại để kiểm tra xem Template cá nhân đã tự động kích hoạt chưa.

---
