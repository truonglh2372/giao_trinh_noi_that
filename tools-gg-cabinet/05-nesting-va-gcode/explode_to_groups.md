# Explode DC → Groups

## Mục đích

**Explode dynamic component** và chuyển mọi component trong selection thành **group**, chuẩn bị model cho ABF Extra Label / nesting (pipeline yêu cầu group, không dùng chung component definition). Tùy chọn gộp group con (`abf_autocombine`), gán layer (`abf_layer`), dọn ẩn/thuộc tính DC.

## Khi nào dùng

- Model từ **Dynamic Component** hoặc component thư viện — cần **make unique / explode** trước khi gắn nhãn ABF.
- **ABF Extra Label** tự gọi bước explode tương tự; chạy tay khi muốn chuẩn hóa selection trước các tool khác.
- Trước **ABF Extra Nesting** khi board vẫn là component instance dùng chung definition.

## Thao tác

1. **Chọn** một hoặc nhiều group/component (không chọn root `__ABF_Nesting` khi explode thủ công cho label — Extra Label tự lọc root đó).
2. Chạy **Explode DC → Groups** trên toolbar hoặc menu.
3. Hộp thoại **Explode → Groups**:
   - **Xóa đối tượng ẩn** — dọn geometry ẩn trong quá trình explode.
   - **Xóa thuộc tính dynamic** — bỏ DC attributes sau explode.
   - **Xóa prefix ID** — dọn prefix ID theo quy ước plugin.
4. **OK** để chạy; **Hủy** để không đổi model.
5. Plugin explode/chuyển component → group, áp dụng **abf_autocombine** (outer shell gộp group con nếu bật trong luồng) và **abf_layer** gán tag.

Extra Nesting **không** tự explode — board phải đã là group trước khi nest thêm.

## Phím tắt / modifier

Không có phím tắt riêng trong plugin cho lệnh này — thao tác qua toolbar/menu và hộp thoại xác nhận.

## Lỗi thường gặp

- **“Hãy chọn group/component trước”**: selection rỗng.
- **Lỗi Explode → Groups**: geometry phức tạp hoặc DC lỗi — thử explode từng phần nhỏ hơn.
- **Nesting báo “chỉ nest Group”**: chạy lại explode trên component còn sót.

## Liên quan

- [ABF Extra Label](abf_extra_label.md) — explode nội bộ trước khi vẽ `_ABF_Label`.
- [ABF Extra Nesting](abf_extra_nesting.md) — yêu cầu group, không explode nesting root.
- [Nesting Editor](nesting_editor.md) — chỉnh layout sau khi đã có `__ABF_Nesting`.
