# Trim cạnh biên tấm

## Mục đích

Trim các mặt cạnh (s-face) của board vào trong N mm (mặc định 1 mm, đổi bằng ± trên HUD / VCB) — click board, Shift+click 1 s-face, hoặc Trim selection

## Khi nào dùng

- Thu mép cạnh ván (s-face) vào trong vài mm — bù dao, clearance, hoặc chuẩn bị liên kết.
- Trim một cạnh cụ thể hoặc toàn bộ cạnh board tùy chế độ.
- Áp preset offset/mode từ bánh răng cài đặt.

## Thao tác

1. Chọn **Trim cạnh biên tấm** trên toolbar (view chuyển X-ray để nhìn s-face mỏng).
2. Trên HUD: chip **Offset** (mm), toggle **1 mặt / tất cả mặt**, preset chips, nút **Trim selection** (icon giữa trên), bánh răng **Preset**.
3. **Click** lên board: trim tất cả s-face ngoài của board đó với offset đang chọn.
4. **Shift+click** gần một s-face: chỉ trim **một** mặt cạnh đó (Shift giữ cũng đảo preview ngay).
5. Chọn nhiều board trong model → bấm **Trim selection** để trim hết board hợp lệ trong selection.
6. Gõ offset trên **VCB** (mm dương) hoặc click chip Offset để nhập hộp thoại.
7. Thanh trạng thái toolbar: *Click board để trim hết s-face · Shift+click 1 s-face · nút Trim trim mọi board đã chọn · VCB/± đổi mm*.

## Phím tắt / modifier

- **Shift (giữ):** ép chế độ trim **một** s-face (preview và toggle HUD phản ánh ngay).
- **VCB:** nhập offset trim mm (0.1–100 mm sau clamp).
- **Toggle Faces** trên HUD: đổi mặc định 1 mặt / tất cả (trừ khi đang giữ Shift).

## Lỗi thường gặp

- **“Không phải board” / highlight đỏ:** đối tượng không nhận dạng là board GG — kiểm tra cấu trúc group/ván.
- **Không hover được s-face:** giữ X-ray; zoom sát mép; thử Shift+click đúng cạnh cần trim.
- **Trim selection bỏ qua vài tấm:** chỉ board hợp lệ được xử lý; phần còn lại được báo và highlight.

## Liên quan

- [Vẽ ván](board_draw.md) — tạo board trước khi trim.
- [Cắt ngang](cross_cut.md) — cắt tách ván thay vì thu mép.
- [Dán cạnh](../04-danh-dau-cnc/edge_band.md) — đánh dấu cạnh dán sau trim.
