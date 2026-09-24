# Cắt tấm (Unsolid Trim)

## Mục đích

**Trim** (cắt boolean) tấm **TARGET** bằng khối **CUTTER**, tương tự Trim solid của SketchUp Pro, nhưng **bỏ qua group lồng** (nhãn ABF, edge band…) khi tính boolean — mesh cắt trên bản sao sạch, rồi gộp lại vào target và **giữ nguyên** group con của target. Sau khi cắt xong, selection thường **chỉ còn CUTTER** (theo thiết kế tool).

## Khi nào dùng

- Cắt **tấm ván** theo khối cutter (khuôn, volume phụ) trong thiết kế tủ.
- Cần trim **ổn định** khi tấm có nhãn/nesting con bên trong (plugin không làm hỏng sub-group target).
- SketchUp **Pro** (cần API `trim` solid); tool **im lặng** khi lỗi — không popup.

## Thao tác

1. Bật **Trim** (Unsolid Trim) trên toolbar.
2. **Chọn CUTTER (1)**: click group/component dùng làm dao cắt, hoặc chọn một object rồi vào tool (status: chọn TARGET).
3. **Chọn TARGET (2)**: click tấm (hoặc khối) bị cắt.
4. Plugin thực hiện trim một thao tác undo; **CUTTER** được chọn lại trong selection; tool tự thoát.

**Cách nhanh**: chọn **đúng hai** group/component (CUTTER rồi TARGET theo thứ tự selection SketchUp) **trước** khi bật tool — trim chạy ngay nếu thứ tự hợp lệ.

Con trỏ hiển thị vòng tròn xanh với số **1** hoặc **2** theo bước pick.

## Phím tắt / modifier

| Thao tác | Phím / modifier |
|--------|------------------|
| Hủy tool | **Esc** |

Không có modifier Shift/Ctrl trong tool Trim.

## Lỗi thường gặp

- **Không cắt, không báo gì**: SketchUp Make hoặc không có solid trim; cutter/target **không solid** sau khi bỏ group lồng — kiểm tra manifold, khe hở, face lỗi.
- **Cắt ngược cutter/target**: luôn chọn **CUTTER trước**, **TARGET sau**; nếu dùng pre-selection hai object, thứ tự trong selection quyết định (object đầu = cutter khi tool không có thứ tự pick nội bộ).
- **Mất nhãn target**: không nên xảy ra nếu nhãn nằm trong group con target — nếu mất, kiểm tra nhãn có nằm ngoài target không.
- **Cutter biến mất khỏi model**: cutter mesh có thể bị tiêu thụ trong boolean native — giữ bản cutter ngoài model nếu cần tái sử dụng.

## Liên quan

- [Hàn tấm (Outer shell)](unsolid_outer_shell.md) — gộp khối thay vì cắt.
- [Trim cạnh biên tấm](../01-ve-va-chinh-hinh/board_trim.md) — trim 2D trên tấm ván.
- [Tạo mộng](tenon_helper.md) — join mộng thay vì boolean tự do.
