# In nhãn

## Mục đích

In **tem nhãn** cho các tấm/part trong **`__ABF_Nesting`**: số tem, tên, vật liệu, QR (ID/tên), thương hiệu — xuất **máy in** và thường kèm **PDF tem** theo tỉ lệ cài đặt.

## Khi nào dùng

- Sau nesting, cần **dán tem** lên tấm cắt hoặc giao xưởng.
- Đối chiếu **số trên tem** với `_ABF_Label` / board-index trên tấm 3D.
- In **một phần** danh sách — tìm theo số tem, tên, vật liệu.

## Thao tác

1. Model phải có **`__ABF_Nesting`** với part đã đặt (sau ABF hoặc Extra Nesting).
2. Chạy **In nhãn** trên toolbar hoặc menu.
3. Dialog **In Tem Nhãn**:
   - Chọn **mẫu tem** / mẫu phụ, **tỉ lệ tem**, rộng/cao (mm), **QR** (ID tấm / tên tấm).
   - **Tên thương hiệu**, **tiêu đề**, **Note** nếu cần.
   - Danh sách tem theo sheet — **tìm** theo số tem, tên, vật liệu (Enter).
4. **Lưu cài đặt** để giữ template cho lần sau.
5. **In Tem** — chọn máy in và khổ giấy **khớp tỉ lệ** tem; luồng gợi ý **xuất kèm PDF**.
6. **PDF** — xuất file tem không qua máy in.

Nếu chưa có tem: chạy nesting trước rồi mở lại dialog.

Trong **Nesting Editor**, có thể in tem cho **part đang chọn** (HUD In tem) — cùng dữ liệu, phạm vi selection nhỏ hơn.

## Phím tắt / modifier

- **Enter** trong ô tìm — lọc danh sách tem (theo placeholder dialog).

Không có phím tắt global khác trong plugin cho in trực tiếp.

## Lỗi thường gặp

- **Chưa có tem nào**: chưa có nesting — chạy pipeline nest trước.
- **Module in nhãn không có**: bản cài thiếu component — liên hệ admin/bản plugin đầy đủ.
- **Thiếu thư viện QR**: cài đủ dependency hoặc tắt QR trong cài đặt nếu cho phép.
- **TOP/BOT chặn** (cùng gate với DXF/G-code): sửa layout sheet trước khi in hàng loạt.

## Liên quan

- [ABF Extra Label](abf_extra_label.md) — số tem trên tấm 3D.
- [Nesting Editor](nesting_editor.md) — in tem part chọn.
- [Tìm tấm trên nesting](find_nest_parts.md) — đối chiếu số tem ↔ part.
- [Xuất Nesting DXF](nesting_dxf.md) / [G-code](gcode.md) — cùng giai đoạn xuất sản xuất.
