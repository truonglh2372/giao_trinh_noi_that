# Giáo trình SketchUp & CNC Nội thất

Bộ giáo trình dạy học viên online dựng hình nội thất bằng SketchUp và đưa file sang sản xuất CNC (ván công nghiệp MDF / MFC / Picomat). Nội dung được hệ thống từ khóa học: công cụ nền tảng → dựng module tủ → gán liên kết → nesting → CAM Aspire → vận hành máy.


## Tra cứu tool GG Cabinet Tools

Hướng dẫn từng tool trên toolbar plugin (thao tác, phím tắt, lỗi thường gặp) — dùng kèm khi học Giai đoạn 3–4:

- **[Giáo trình sử dụng tool — GG Cabinet Tools](https://github.com/truonglh2372/gg_cms/blob/main/docs/user-guide/README.md)**

## Mục lục

### Giai đoạn 1 — Nền tảng SketchUp

1. [Bài 1: Giao diện, thao tác camera và thiết lập template chuẩn](bai_01_giao_dien_camera_template.md)
2. [Bài 2: Làm chủ nhóm công cụ vẽ 2D cơ bản](bai_02_cong_cu_ve_2d.md)
3. [Bài 3: Làm chủ nhóm công cụ hiệu chỉnh và dựng hình 3D](bai_03_cong_cu_hieu_chinh_3d.md)
4. [Bài 4: Quản lý mô hình chuyên nghiệp (Groups, Components, Tags, Outliner)](bai_04_quan_ly_group_component_tag.md)

### Giai đoạn 2 — Dựng hình nội thất

5. [Bài 5: Dựng hình chi tiết module tủ bếp dưới](bai_05_module_tu_bep_duoi.md)
6. [Bài 6: Dựng hình module tủ bếp trên và tủ áo kịch trần](bai_06_tu_bep_tren_tu_ao.md)
7. [Bài 7: Dựng hình đồ rời và vách ngăn decor](bai_07_do_roi_vach_decor.md)
8. [Bài 8: Dựng bộ lam vách ngăn phòng khách và phòng bếp](bai_08_lam_vach_ngan.md)
9. [Bài 9: Dựng các chi tiết uốn cong và bo tròn sản xuất](bai_09_uon_cong_bo_tron.md)
10. [Bài 10: Dựng module tủ bếp và tủ áo tiêu chuẩn CNC](bai_10_module_tu_chuan_cnc.md)

### Giai đoạn 3 — Liên kết và nesting

11. [Bài 11: Phân tích liên kết và gán tự động bằng plugin (ABF / GG Cabinet)](bai_11_lien_ket_abf.md)
12. [Bài 12: Kiểm tra lỗi file (Audit) và xuất file nesting sơ cấp](bai_12_audit_nesting.md)

### Giai đoạn 4 — CAM và vận hành CNC

13. [Bài 13: Thao tác phần mềm CAM Vectric Aspire và xuất G-Code](bai_13_aspire_gcode.md)
14. [Bài 14: Quy trình vận hành máy CNC và xử lý sự cố tại xưởng](bai_14_van_hanh_may_cnc.md)

## Cách học

Đi lần lượt từ Bài 1. Mỗi bài có mục tiêu, thời lượng, thao tác từng bước và bài tập. Đơn vị làm việc xuyên suốt là **millimet (mm)** trong hệ tọa độ thế giới của SketchUp.

| Giai đoạn | Kỹ năng đầu ra |
| --- | --- |
| 1 | Template mm, phím tắt xưởng, vẽ 2D/3D, Group/Component, mặt trắng Front Face |
| 2 | Tủ bếp, tủ áo, đồ rời, lam vách, đồ cong, module sẵn sàng CNC |
| 3 | Cam chốt, bản lề, rãnh hậu, audit 8 bước, nesting DXF |
| 4 | Toolpath Aspire, Post Processor, vận hành máy, xử lý sự cố |

## Cấu trúc file

```text
giao_trinh_noi_that/
├── README.md
├── bai_01_giao_dien_camera_template.md
├── bai_02_cong_cu_ve_2d.md
├── bai_03_cong_cu_hieu_chinh_3d.md
├── bai_04_quan_ly_group_component_tag.md
├── bai_05_module_tu_bep_duoi.md
├── bai_06_tu_bep_tren_tu_ao.md
├── bai_07_do_roi_vach_decor.md
├── bai_08_lam_vach_ngan.md
├── bai_09_uon_cong_bo_tron.md
├── bai_10_module_tu_chuan_cnc.md
├── bai_11_lien_ket_abf.md
├── bai_12_audit_nesting.md
├── bai_13_aspire_gcode.md
└── bai_14_van_hanh_may_cnc.md
```
