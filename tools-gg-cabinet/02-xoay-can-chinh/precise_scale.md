# Scale chính xác (Precise Scale)

## Mục đích

**Trượt đỉnh** của group/component theo hướng bounding-box world — thay vì scale đồng nhất (làm dày cả khung cửa), tool **chỉ kéo một phía** của hộp bao. Chọn cạnh hoặc mặt để định hướng, kéo handle hoặc mặt giữa, bắt dính hình học; nhập **mm world** trên VCB khi đang kéo.

## Khi nào dùng

- Chỉnh ** một chiều** (rộng, cao, sâu) của tấm hoặc module mà không méo chi tiết bên trong theo tỷ lệ Scale thông thường.
- Kéo **mặt giữa** hoặc **handle góc/cạnh** bbox để mở rộng/thu hẹp theo trục đã chọn.
- Cần **đối xứng hai đầu** khi kéo (Ctrl: trượt hai bên).

Khác với [Scale theo trục](dumb_scale.md): Precise Scale **di chuyển vertex** dọc trục; Dumb Scale **scale transform** theo W/H/D bbox.

## Thao tác

1. **Chọn** ít nhất một group hoặc component (tool báo lỗi nếu selection rỗng hoặc không phải group/component).
2. Bật **Scale chính xác** trên toolbar.
3. **Rê chuột** lên handle bbox, **mặt giữa**, hoặc **cạnh/mặt** để chọn hướng trượt — **click** để bắt đầu giữ (drag).
4. **Kéo** chuột hoặc gõ **mm** trên VCB (khoảng cách **world mm**); có thể bắt dính điểm, trung điểm, cạnh, guideline, trục world.
5. **Click** lần nữa để **xác nhận**; **Esc** hủy thao tác kéo đang mở.

Trong lúc kéo, **Tab** đổi tham chiếu đo (điểm bắt đầu/kết thúc dimension hiển thị).

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Trượt đối xứng hai phía (hai đầu bbox) | **Ctrl** (bật/tắt mỗi lần nhấn Ctrl mới; không cần giữ liên tục) |
| Đổi tham chiếu đo khi đang kéo | **Tab** |
| Nhập khoảng cách kéo | VCB: số **mm** (world) |
| Hủy lần kéo hiện tại | **Esc** |

## Lỗi thường gặp

- **“Hãy chọn ít nhất một group hoặc component”**: chọn đúng container trước khi chạy tool.
- **Không kéo được**: chưa click để “giữ” handle/mặt giữa — phải vào trạng thái drag (status bar: kéo hoặc nhập mm).
- **Kích thước lệch mong đợi**: kiểm tra đã chọn đúng **cạnh/mặt định hướng**; đo lại bằng [Hover dimensions](../06-tien-ich/hover_dimensions.md) (mm world).
- **Definition dùng chung**: trượt đỉnh trong component ảnh hưởng mọi instance — **Make Unique** nếu cần.

## Liên quan

- [Scale theo trục](dumb_scale.md) — đặt nhanh W/D/H chung cho nhiều đối tượng.
- [Dịch vertex](../01-ve-va-chinh-hinh/move_vertices.md) — chỉnh đỉnh chi tiết hơn trên mesh.
- [Vẽ ván](../01-ve-va-chinh-hinh/board_draw.md) — tạo tấm rồi chỉnh kích thước bằng Precise Scale.
