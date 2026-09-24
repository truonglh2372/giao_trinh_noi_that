# Giáo trình sử dụng tool — GG Cabinet Tools

Tài liệu tiếng Việt cho **user cuối**. Đủ mọi tool trên toolbar: mục đích,
thao tác, phím tắt/modifier và lỗi thường gặp (bám tooltip/status `vi.yml` và
hành vi tool). Chi tiết có thể chỉnh thêm khi tool đổi.

Spec: [`docs/superpowers/specs/2026-09-24-user-guide-tools-design.md`](../superpowers/specs/2026-09-24-user-guide-tools-design.md).

## Bắt đầu

- [Bắt đầu](00-bat-dau.md) — cài đặt, đăng nhập, toolbar, đơn vị mm
- [Mẫu bài tool](_template.md)

## Lộ trình học gợi ý

1. [Vẽ & chỉnh hình](#01-vẽ--chỉnh-hình)
2. [Xoay / căn / scale](#02-xoay--căn--scale)
3. [Ghép & mộng](#03-ghép--mộng)
4. [Đánh dấu CNC](#04-đánh-dấu-cnc)
5. [Nesting & G-code](#05-nesting--g-code)
6. [Tiện ích](#06-tiện-ích)
7. [Admin](#07-admin-chỉ-admin) (không bắt buộc)

## 01. Vẽ & chỉnh hình

- [Vẽ ván](01-ve-va-chinh-hinh/board_draw.md)
- [Contour](01-ve-va-chinh-hinh/contour.md)
- [Tạo mặt](01-ve-va-chinh-hinh/make_face.md)
- [Deep Push](01-ve-va-chinh-hinh/deep_push.md)
- [Dịch vertex](01-ve-va-chinh-hinh/move_vertices.md)
- [Trim cạnh biên tấm](01-ve-va-chinh-hinh/board_trim.md)
- [Cắt ngang](01-ve-va-chinh-hinh/cross_cut.md)
- [Uốn cong](01-ve-va-chinh-hinh/bend.md)
- [Trải phẳng (Unfold)](01-ve-va-chinh-hinh/unfold.md)

## 02. Xoay / căn / scale

- [Align](02-xoay-can-chinh/align.md)
- [Mirror](02-xoay-can-chinh/mirror.md)
- [Xoay](02-xoay-can-chinh/rotate.md)
- [Precise Scale](02-xoay-can-chinh/precise_scale.md)
- [Scale](02-xoay-can-chinh/dumb_scale.md)

## 03. Ghép & mộng

- [Tạo mộng](03-ghep-va-mong/tenon_helper.md)
- [Cam lock / liên kết ngang](03-ghep-va-mong/cam_lock.md)
- [Khấu (cross halving)](03-ghep-va-mong/khau.md)
- [Unsolid Trim](03-ghep-va-mong/unsolid_trim.md)
- [Unsolid Outer Shell](03-ghep-va-mong/unsolid_outer_shell.md)

## 04. Đánh dấu CNC

- [Marking](04-danh-dau-cnc/marking.md)
- [Dán cạnh (edge band)](04-danh-dau-cnc/edge_band.md)
- [Khử dao (CNC relief)](04-danh-dau-cnc/cnc_relief.md)
- [Intersect Mark](04-danh-dau-cnc/intersect_mark.md)

## 05. Nesting & G-code

- [Explode DC → Groups](05-nesting-va-gcode/explode_to_groups.md)
- [ABF Extra Label](05-nesting-va-gcode/abf_extra_label.md)
- [Xoay nhãn](05-nesting-va-gcode/rotate_label.md)
- [Đảo nhãn](05-nesting-va-gcode/flip_label.md)
- [Tìm tấm trên nesting](05-nesting-va-gcode/find_nest_parts.md)
- [Nesting Editor](05-nesting-va-gcode/nesting_editor.md)
- [ABF Extra Nesting](05-nesting-va-gcode/abf_extra_nesting.md)
- [G-code Manager](05-nesting-va-gcode/gcode.md)
- [Xuất Nesting DXF](05-nesting-va-gcode/nesting_dxf.md)
- [In nhãn](05-nesting-va-gcode/label_print.md)

## 06. Tiện ích

- [Isolate](06-tien-ich/isolate.md)
- [Layer Manager](06-tien-ich/layer_manager.md)
- [Thống kê cấu kiện](06-tien-ich/component_stats.md)
- [Warehouse](06-tien-ich/warehouse.md)
- [Settings](06-tien-ich/settings.md)
- [Chọn theo vật liệu](06-tien-ich/color.md)
- [Xóa vật liệu](06-tien-ich/remove_color.md)
- [Hover dimensions](06-tien-ich/hover_dimensions.md)
- [Đổi tên instance](06-tien-ich/instance_rename.md)
- [Cập nhật plugin](06-tien-ich/update.md)

## 07. Admin (chỉ admin)

> Các tool dưới đây **chỉ hiện cho tài khoản admin**.

- [AI Render](07-admin/ai_render.md)
- [AI Model](07-admin/ai_model.md)
- [Entity dump (console)](07-admin/entity_dump.md)
- [Entity dump (txt)](07-admin/entity_dump_txt.md)
- [Entity dump (JSON)](07-admin/entity_dump_json.md)
