# Dịch vertex

## Mục đích

Quét chọn vertex và dịch theo trục world (Tab xoay Z/X/Y, Ctrl bỏ khóa); snap, VCB hoặc điểm thứ 2 để định khoảng cách

## Khi nào dùng

- Chỉnh mép, làm phẳng, dịch nhẹ đỉnh/điểm trên ván hoặc khối (mm world).
- Cần thấy vertex bên trong board — tool bật X-ray và tô màu theo tag khi chạy, khôi phục view khi thoát.
- Hạn chế trong phạm vi selection model (nếu đã chọn group/face trước, chỉ quét vertex trong vùng đó).

## Thao tác

1. Chọn **Dịch vertex** trên toolbar.
2. **Quét (drag)** hộp chọn quanh các vertex cần dịch; vertex chọn được tô màu.
3. **Click** (không kéo) sau khi đã có vertex: đặt **điểm đầu mũi tên** (snap cạnh, midpoint, trục, vertex khác…).
4. Di chuột để xem mũi tên preview dọc trục đang khóa; **click** điểm đích **hoặc** gõ mm trên VCB **hoặc** **Enter** để chốt theo preview hiện tại.
5. **Esc** lần một: hủy bước dịch, quay lại chọn vertex; **Esc** khi đang chọn: thoát tool.
6. Hướng dẫn: *Quét chọn các vertex · click để chọn điểm đầu mũi tên*; khi đang dịch: *Di chuột (↑←→ khoá trục, ↓ hoặc Ctrl bỏ khoá, Tab đổi trục) · VCB/điểm 2 · Enter để xong*.

## Phím tắt / modifier

- **Tab:** xoay vòng khóa trục world **Z → X → Y** (khi đang dịch).
- **↑ / ← / →:** ghim trục **Z / X / Y** tương ứng.
- **↓:** bỏ ghim phím — trục lại bám hướng gần con trỏ nhất.
- **Ctrl:** bật/tắt **tự do** (không khóa trục; di trên mặt phẳng song song màn hình qua điểm đầu).
- **VCB:** khoảng cách mm dọc theo hướng mũi tên.
- **Enter:** chốt dịch.

## Lỗi thường gặp

- **Quét không chọn được điểm:** tăng vùng quét, bật X-ray sẵn có của tool, zoom gần mép ván.
- **Dịch lệch trục:** kiểm tra chip/hướng mũi tên; dùng **Tab** hoặc mũi tên để khóa đúng trục world.
- **Snap không ăn:** click gần endpoint/midpoint; điểm hồng là điểm đầu đã chọn.

## Liên quan

- [Deep Push](deep_push.md) — dịch cả mặt theo pháp tuyến.
- [Trim cạnh biên tấm](board_trim.md) — thu mép đồng loạt thay vì kéo từng vertex.
- Nhóm tiếp: [Precise Scale](../02-xoay-can-chinh/precise_scale.md) — scale có kiểm soát.
