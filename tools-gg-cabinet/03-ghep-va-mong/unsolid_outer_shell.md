# Hàn tấm (Outer shell)

## Mục đích

**Outer shell** (hàn / vỏ ngoài) gộp nhiều group/component solid thành **một khối vỏ** như lệnh Outer Shell native SketchUp Pro. Plugin boolean trên bản sao **chỉ mesh**, bỏ qua group lồng (nhãn, edge band…), rồi gộp kết quả vào **khối gốc** và **chuyển** group con từ các khối bị “ăn” vào khối gốc. Thao tác **im lặng** khi lỗi.

## Khi nào dùng

- **Hàn** hai tấm hoặc nhiều khối chồng nhau thành một solid ngoài (tủ kín, khối composite).
- Cần outer shell khi tấm vẫn có **ABF_Label** hoặc con khác bên trong.
- Sau hàn, tiếp tục chỉnh bằng [Unsolid Trim](unsolid_trim.md) hoặc export nesting.

## Thao tác

1. Bật **Outershell** (Hàn tấm) trên toolbar.

**Cách A — selection sẵn**

- Chọn **hai hoặc nhiều** group/component solid.
- Bật tool → plugin **outer shell một lần** (khối đầu selection làm base), giữ lại base trong selection, status mời chọn khối tiếp.

**Cách B — pick từng khối**

1. Status: **Chọn khối đầu tiên** — click group/component **1** (con trỏ vòng **1**).
2. Status: **Chọn khối tiếp theo để gộp** — click khối **2**, **3**, … Mỗi lần click gộp thêm vào base; base vẫn được chọn.
3. **Esc** kết thúc tool (dừng pick, xóa status).

Khối bị gộp (modifier) bị **xóa** sau khi thành công; nested group bên trong chuyển sang base.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Kết thúc chế độ pick | **Esc** |

Không có Shift/Ctrl trong tool Outer shell.

## Lỗi thường gặp

- **Không gộp, không thông báo**: cần **SketchUp Pro** và `outer_shell` solid; một trong các khối **không manifold** sau khi tách mesh — sửa lỗi face, khe hở.
- **Tooltip nói “nhiều hơn 2 đối tượng”**: thực tế tool chấp nhận **≥ 2** khối (pre-selection hoặc pick nhiều lần); với đúng 2 tấm vẫn hàn được khi chọn cả hai trước khi chạy.
- **Mất một tấm trong model**: modifier bị consume — giữ bản sao hoặc undo (Ctrl+Z) nếu hàn nhầm.
- **Nhãn lệch**: nested đã reparent vào base — kiểm tra transformation; undo nếu cần.

## Liên quan

- [Unsolid Trim](unsolid_trim.md) — cắt thay vì hàn.
- [Deep Push](../01-ve-va-chinh-hinh/deep_push.md) — tạo khối trước khi hàn.
- [Explode DC → Groups](../05-nesting-va-gcode/explode_to_groups.md) — chuẩn hóa trước nesting sau khi hàn.
