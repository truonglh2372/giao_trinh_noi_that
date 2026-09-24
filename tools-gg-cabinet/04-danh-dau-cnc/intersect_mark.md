# Intersect Mark (đánh dấu giao nhau)

## Mục đích

Đánh dấu **tiết diện giao nhau** nơi cạnh tấm nguồn **tiếp xúc** tấm đích (vách kệ, hồi, ngăn) — tạo marker trên tấm đích theo preset giao cắt, phục vụ gia công CNC hoặc kiểm tra khớp.

## Khi nào dùng

- Lắp **tấm đứng vào tấm ngang** (hoặc ngược lại) cần mark vị trí **cắt slot / pocket giao**.
- Nhiều điểm tiếp xúc cùng một tấm nguồn — muốn đặt mark **từng chỗ** hoặc **tất cả** mặt đích cùng lúc.
- Cần chỉnh **offset rộng** mark (mm) trước khi commit.

## Thao tác

1. Bật tool **Đánh dấu giao nhau**.
2. **Click chọn tấm nguồn** (board seed) — tool quét các tấm **đích** tiếp xúc / xuyên qua.
3. **Rê chuột** tới từng vị trí tiếp xúc; preview marker trên tấm đích đang hover.
4. **Click** để **commit** marker tại tấm đích đang hover.
5. **Double-click** tấm nguồn — đặt marker lên **tất cả** tấm đích mating của tấm đó trong một lần.
6. **Click vùng trống** (không giữ Shift) — bỏ seed hiện tại và selection, quay lại bước chọn tấm nguồn mới.
7. Chọn **preset** trên HUD (nếu có nhiều kiểu mark giao).
8. Gõ **mm** trên VCB để đổi offset rộng; giá trị được lưu cho lần sau.

Geometry đặt trên tấm đích; kích thước offset theo **mm world**.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Preview / commit lên **mọi** tấm đích (không chỉ hover) | Giữ **Shift** khi click |
| Shift + click khi chưa có marker dưới chuột | **Không** đổi seed (tránh xóa nguồn nhầm) |
| Nhập offset rộng (mm world) | VCB |
| Đặt tất cả mating của tấm nguồn | **Double-click** tấm nguồn |
| Thoát tool | **Esc** |

Thanh trạng thái: chọn tấm nguồn — rê tới chỗ tiếp xúc, nhấp để đặt dấu.

## Lỗi thường gặp

- **Không có preview**: tấm nguồn chưa chọn hoặc không có tiếp xúc hình học với tấm đích — kiểm tra tấm thật sự chạm/penetration.
- **Mark sai tấm**: chỉ commit tấm đang hover; dùng Shift nếu cần cùng lúc nhiều đích.
- **Seed “kẹt”**: click vùng trống (không Shift) để clear seed và chọn nguồn khác.

## Liên quan

- [Marking](marking.md) — mark dọc cạnh tấm đơn, không tính giao hai tấm.
- [Khấu (cross halving)](../03-ghep-va-mong/khau.md) — ghép cắt ngang; intersect mark cho tiếp xúc tổng quát hơn.
- [Tenon helper](../03-ghep-va-mong/tenon_helper.md) — workflow mộng tương tự (chọn nguồn, hover đích).
