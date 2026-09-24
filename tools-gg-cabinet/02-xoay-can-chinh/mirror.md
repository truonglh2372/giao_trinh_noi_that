# Đối xứng (Mirror)

## Mục đích

Mirror (đối xứng) group hoặc component đã chọn **qua mặt phẳng** của một face, **qua một điểm** (đỉnh hoặc trung điểm cạnh), hoặc **qua cạnh** (lật dọc theo cạnh đó). Preview bbox nét đứt cho thấy vị trí sau mirror; ô vuông đánh dấu tâm mirror. **Ctrl** bật/tắt giữ lại bản gốc (nhân bản mirror).

## Khi nào dùng

- Tạo ** cánh đối xứng**, tấm lật mặt, chi tiết gương so với mặt phân giữa.
- Mirror qua **mặt tấm ván** hoặc **mặt phẳng tham chiếu** trong model.
- Cần **giữ bản cũ** và thêm bản mirror (chế độ copy) khi lắp đối xứng hai bên.

## Thao tác

1. **Chọn** một hoặc nhiều group/component cần mirror (selection trước khi bật tool).
2. Bật tool **Đối xứng** trên toolbar.
3. **Rê chuột**:
   - lên **face** → mirror qua mặt phẳng chứa face đó;
   - lên **đỉnh** hoặc **trung điểm cạnh** → đối xứng qua điểm (spin quanh điểm);
   - lên **cạnh** → mirror dọc theo cạnh (flip along edge).
4. Quan sát preview bbox và marker mirror; bật **Ctrl** nếu muốn **giữ bản gốc** (dấu **+** khi copy bật).
5. **Click** để thực hiện mirror.

Transform áp dụng trong **tọa độ world**; kích thước bbox sau mirror vẫn đo bằng **mm world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Bật/tắt giữ bản gốc (nhân bản mirror) | **Ctrl** (sticky; không cần giữ khi click) |
| Hủy tool | **Esc** |

Không có phím mũi tên riêng cho Mirror trong plugin; hướng mirror do face/edge/điểm dưới con trỏ quyết định.

## Lỗi thường gặp

- **Không có preview**: chưa chọn group/component hợp lệ, hoặc con trỏ không nằm trên face/cạnh/điểm có thể pick.
- **Mirror sai phía**: đổi target (face/edge khác) hoặc mirror qua mặt phẳng rõ ràng hơn; kiểm tra normal face (mặt trước/sau tấm).
- **Mất bản gốc**: bật **Ctrl** (copy) trước click nếu cần cả hai bên.
- **Component dùng chung definition**: mirror có thể ảnh hưởng mọi instance cùng definition — cân nhắc **Make Unique** trong SketchUp nếu chỉ một instance cần đổi.

## Liên quan

- [Căn đối tượng (Align)](align.md) — đặt sát mép/mặt thay vì lật đối xứng.
- [Xoay](rotate.md) — xoay 90° quanh trục world.
- [Mirror trong ghép mộng](../03-ghep-va-mong/cam_lock.md) — Tab/Ctrl trong tool Cam lock (ngữ cảnh khác, chỉ đánh dấu liên kết).
