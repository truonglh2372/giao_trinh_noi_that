# Căn đối tượng (Align)

## Mục đích

Align (căn) group hoặc component bằng cách đưa **đỉnh gần nhất** của đối tượng tới điểm bám trên face, cạnh, trung điểm cạnh hoặc đỉnh mục tiêu. Preview màu cyan cho thấy vị trí trước khi xác nhận. Có thể nhân bản sau khi căn hoặc chia đều nhiều bản sao dọc theo quãng từ vị trí cũ tới vị trí mới.

## Khi nào dùng

- Đặt tấm ván, khuôn, phụ kiện **sát mép hoặc mặt** của tấm khác mà không đo tay từng lần.
- Căn nhanh vào **gốc tọa độ (0,0,0)** hoặc **trục X / Y / Z** khi rê chuột vào vùng trống (không có hình học dưới con trỏ).
- Sau khi căn một chi tiết, **nhân bản đều** nhiều bản (kệ, thanh đỡ lặp) bằng lệnh `/n` trên thanh Measurements.

## Thao tác

1. Bật tool **Căn đối tượng theo face hoặc edge** trên toolbar (hoặc menu tương ứng).
2. **Chọn đối tượng cần căn**: click vào group/component (hoặc chọn sẵn rồi bật tool — tool sẽ nhận selection).
3. **Rê chuột** tới face, cạnh, trung điểm hoặc đỉnh đích; preview cyan cập nhật theo điểm bám (màu cam đánh dấu điểm snap).
4. Tùy chọn: xoay preview, đổi mặt dày bám (Tab), nhập số mm trên VCB để dịch preview, bật chế độ nhân bản (Ctrl).
5. **Click** để commit — đối tượng (và bản sao nếu bật nhân bản) được đặt đúng vị trí.
6. **Giai đoạn array** (sau khi đã căn): gõ **`/n`** trên thanh Measurements (ví dụ `/3`) để xem trước `n` bản sao chia đều giữa vị trí ban đầu và vị trí đã căn; **click** để tạo thật; **Esc** để thoát, chỉ giữ bản đã căn.

Mọi khoảng cách hiển thị hoặc nhập trên VCB là **mm trong hệ tọa độ world** của model.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Xoay preview 90° quanh trục Z | Phím **↑** |
| Xoay preview 90° quanh trục Y | Phím **←** |
| Xoay preview 90° quanh trục X | Phím **→** |
| Đảo chiều xoay (90° ngược) | Giữ **Shift** khi bấm mũi tên |
| Chuyển mặt dày bám (mặt trước → giữa → mặt sau tấm) | **Tab** (Shift + Tab: ngược chiều); chỉ có hiệu lực với đối tượng dạng tấm ván |
| Bật/tắt nhân bản khi căn (giữ bản cũ, đặt bản mới) | **Ctrl** (bật/tắt dạng sticky; dấu **+** cạnh con trỏ khi bật) |
| Dịch preview theo mm | VCB: gõ số (mm world) |
| Xem trước nhân bản chia đều sau căn | VCB: **`/n`** (n = số bản sao thêm) |
| Hủy tool | **Esc** |

## Lỗi thường gặp

- **Không thấy preview**: đảm bảo đã chọn đúng group/component (không phải face lẻ trong edit context), và con trỏ nằm trên hình học hoặc vùng snap trục/gốc.
- **Tab không đổi mặt dày**: đối tượng không được nhận dạng là tấm ván (không có cặp mặt song song); chỉ snap theo đỉnh gần nhất trên mặt phẳng đã chọn.
- **`/n` không phản hồi**: chỉ dùng sau khi đã **click commit** lần căn đầu; gõ đúng dạng `/số` trên VCB.
- **Căn lệch so với ý muốn**: điểm bám là **đỉnh gần nhất** tới target, không phải tâm bbox — thử xoay preview (mũi tên) hoặc Tab đổi mặt dày trước khi click.

## Liên quan

- [Mirror](mirror.md) — đối xứng qua mặt hoặc điểm thay vì dịch snap.
- [Xoay](rotate.md) — xoay 90° quanh tâm bbox khi không cần bám face.
- [Precise Scale](precise_scale.md) — chỉnh kích thước bằng trượt đỉnh bbox, không dịch snap.
- [Scale theo trục](dumb_scale.md) — đặt nhanh rộng/cao/sâu chung cho nhiều đối tượng.
- [Vẽ ván](../01-ve-va-chinh-hinh/board_draw.md) — tạo tấm ván trước khi căn ghép.
