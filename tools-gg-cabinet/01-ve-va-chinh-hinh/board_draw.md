# Vẽ ván

## Mục đích

Vẽ một tấm ván hoàn chỉnh như vẽ rectangle — mặc định dày 17.5 mm, trên mặt phẳng world đang khóa

## Khi nào dùng

- Cần tấm ván mới (chiều dài × rộng × dày) nhanh, đúng mm world, không vẽ tay từng face.
- Muốn phủ trọn một mặt phẳng có sẵn (mặt tường, mặt khối tham chiếu).
- Bước đầu của luồng tạo tủ: ván thùng, vách, kệ, nẹp phẳng.

## Thao tác

1. Trên toolbar, chọn **Vẽ ván**.
2. **Cách A — hai góc chéo:** click góc thứ nhất, kéo chuột, click góc đối diện (hai góc là đường chéo của hình chữ nhật; mặt phẳng ván bám theo hai góc đó).
3. **Cách B — phủ mặt:** double-click vào một mặt phẳng để tạo ván phủ trọn mặt đó.
4. Trong lúc kéo, xem trước khung và khối ván; thả chuột hoặc click lần hai để hoàn tất (một thao tác undo).
5. Độ dày mặc định hiện trên chip HUD **Độ dày**; click chip để đổi (mm), giá trị được nhớ cho lần sau.
6. Thanh trạng thái (toolbar): click góc thứ nhất, kéo, click góc đối diện; mũi tên ghim mặt phẳng world, Xuống/Shift nhả ghim; Tab lật chiều dày; VCB nhập `600;400`.

## Phím tắt / modifier

- **Mũi tên (↑ ← →):** ghim mặt phẳng ván theo mặt phẳng world (X/Y/Z); giữ ghim cho đến khi nhả.
- **Mũi tên Xuống** hoặc **Shift (thả phím):** bỏ ghim mặt phẳng — mặt phẳng lại theo hai góc rectangle.
- **Tab:** lật chiều độ dày (ván mọc sang phía còn lại của mặt phẳng).
- **VCB:** nhập kích thước hai cạnh theo mm, dạng `600;400` (cạnh thứ hai có thể bỏ trống nếu đang kéo tay).
- **Enter:** chốt ván khi đang ở bước kéo góc thứ hai.

## Lỗi thường gặp

- **Không thấy preview:** góc suy luận trùng hoặc mặt phẳng suy biến — di chuột xa hơn, bám snap cạnh/điểm, hoặc ghim mặt phẳng bằng mũi tên.
- **Ván dày sai phía:** bấm **Tab** trước khi chốt.
- **Kích thước lệch:** nhập lại trên VCB (`600;400`) khi đang kéo; mọi kích thước hiển thị là mm trong world.

## Liên quan

- [Trim cạnh biên tấm](board_trim.md) — chỉnh mép s-face sau khi vẽ.
- [Cắt ngang](cross_cut.md) — cắt ván theo cạnh.
- [Deep Push](deep_push.md) — đẩy mặt trong group/component.
- Nhóm tiếp theo: [Align](../02-xoay-can-chinh/align.md) — căn ván vào face/edge.
