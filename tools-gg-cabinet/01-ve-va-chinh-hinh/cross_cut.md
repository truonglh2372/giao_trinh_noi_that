# Cắt ngang

## Mục đích

Cắt object thành 2 phần theo đường vuông góc cạnh được chọn

## Khi nào dùng

- Chia ván/khối thành hai phần bằng mặt cắt vuông góc một cạnh (cắt ngang theo nhịp).
- Cần kerf/độ rộng đường cắt mm (mặc định thường 3 mm) và đặt vị trí cắt theo mm dọc cạnh.
- Chia **N phần bằng nhau** trên cùng một cạnh (VCB dạng `/N`).

## Thao tác

1. Chọn **Cắt ngang** trên toolbar.
2. Di chuột lên **cạnh** của solid/group cần cắt; preview đường cắt cam và dim hiện theo vị trí con trỏ.
3. Trên HUD, click chip **Width** nếu cần đổi **độ rộng kerf** (mm).
4. **VCB:**
   - Gõ số mm: offset từ đầu cạnh (gần v0); cùng khoảng cách cũng snap từ đầu kia.
   - Gõ `/N` (N ≥ 2): chia cạnh thành N phần bằng nhau (nhiều đường cắt preview).
5. **Tab:** đổi mốc đo offset trên VCB — **Gần (mm) / Giữa (mm) / Xa (mm)** (cạnh kerf gần, tâm, hoặc xa so với điểm tham chiếu).
6. **Click** trên cạnh (không trúng chip HUD) để thực hiện cắt (một bước undo).
7. Thanh trạng thái: *Di chuột lên cạnh — nhập chiều rộng cắt, nhấp để cắt*.

## Phím tắt / modifier

- **Tab:** xoay vòng neo đo offset (near / centroid / far) trên VCB.
- **VCB:** mm offset hoặc `/N` chia đều.
- Snap: kim cương cyan trên preview — vị trí cắt hút vào các điểm snap.

## Lỗi thường gặp

- **Click không cắt:** chưa hover đúng cạnh trên solid hợp lệ, hoặc click trúng chip HUD.
- **Vị trí cắt lệch:** đổi neo **Tab** (Gần/Giữa/Xa) rồi gõ lại mm.
- **Kerf quá hẹn/rộng:** chỉnh chip Width (mm) trước khi click.

## Liên quan

- [Vẽ ván](board_draw.md) — tạo tấm cần cắt.
- [Trim cạnh biên tấm](board_trim.md) — chỉnh mép, không tách khối.
- [Unsolid Trim](../03-ghep-va-mong/unsolid_trim.md) — trim boolean phức tạp hơn.
