# REEL — static movie UI study

Một bài thực hành giao diện duyệt phim, gồm HTML, CSS và JavaScript trong
`index.html`. Tên repository là **St4**; thương hiệu minh họa trong giao diện là REEL.

## Phạm vi thực tế

- Hero, hàng thẻ phim cuộn ngang, thể loại, trang chi tiết và vùng player minh họa.
- Toggle ô tìm kiếm, tab hồ sơ, nút cuộn hàng và quay lại đầu trang.
- Skeleton tải ban đầu và bố cục responsive.

Danh sách/tên phim, năm và tiến độ xem là dữ liệu minh họa trong JavaScript.
Nhãn điểm IMDb tĩnh/ngẫu nhiên trước đây được thay bằng nhãn minh họa trong đợt audit;
giao diện không có nguồn đánh giá người dùng.
Nút player chỉ đổi trạng thái hiển thị; **không phát video**.
Chưa có backend, tìm kiếm dữ liệu, đăng nhập, thanh toán hoặc lưu lịch sử xem.

## Chạy thử

Mở `index.html` bằng trình duyệt. Để phục vụ qua HTTP, dùng một static server, ví dụ
nếu đã cài Python:

```powershell
python -m http.server 8080 --bind 127.0.0.1
```

Mở `http://127.0.0.1:8080`. Không có bước build hoặc dependency npm.
Chưa xác minh một URL public demo cho repo này; không gắn nhãn streaming service.

## Cấu trúc và kiểm tra

`index.html` chứa token màu, CSS, markup và script tạo dữ liệu giả.
Kiểm tra thủ công cần gồm màn hình 390 px/desktop, bàn phím, toggle tìm kiếm,
tab hồ sơ, nút cuộn và lỗi khi nguồn ảnh/font bên ngoài không truy cập được.
Kết quả audit ngày 04/11/2026 nằm trong [docs/verification.md](docs/verification.md).

## Nguồn và giấy phép

Ảnh hiện được tham chiếu bằng URL Unsplash; font tải từ Google Fonts.
Chưa có bảng nguồn từng ảnh/tác giả hoặc LICENSE cho toàn bộ code.
Không xem đây là giấy phép phân phối lại ảnh, phim, poster hoặc thương hiệu.
Đợt audit giữ nguyên tài nguyên và comment hiện có, không thêm ảnh stock hoặc video mới.
