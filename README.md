# Tây Nguyên Roadbook

Web app tĩnh cho hành trình xe máy từ TP.HCM đến Đà Nẵng qua Tây Nguyên (lịch tham khảo 28/11–03/12/2026). Gợi ý điểm dừng, lưu tiến độ cục bộ và mở từng chặng bằng Google Maps.

## Triển khai miễn phí bằng GitHub Pages

1. Tạo repository mới trên GitHub (Public).
2. Upload **toàn bộ các tệp trong thư mục này vào thư mục gốc của repository**, không đặt trong một thư mục con.
3. Vào **Settings → Pages → Build and deployment**; ở **Source** chọn `Deploy from a branch`.
4. Chọn nhánh `main`, thư mục `/(root)` rồi **Save**.
5. Chờ GitHub Pages triển khai; mở URL dạng `https://<username>.github.io/<repo>/`.
6. Trên iPhone, mở URL bằng Safari → Chia sẻ → Thêm vào Màn hình chính.

## File chính

- `index.html`: giao diện và logic hành trình.
- `manifest.webmanifest`: thông tin PWA.
- `service-worker.js`: cache file ứng dụng cơ bản.
- `icon.svg`: biểu tượng ứng dụng.
- `.nojekyll`: bỏ qua xử lý Jekyll khi GitHub Pages phục vụ tệp tĩnh.

## Lưu ý an toàn

Google Maps được mở bằng liên kết điều hướng, **không có API tối ưu tuyến thời gian thực**. Ứng dụng không xác minh tự động cao tốc, đường cấm xe máy, sạt lở, mưa lũ hay ùn tắc. Kiểm tra tuyến trên Google Maps bằng chế độ xe máy nếu khả dụng và tuân theo biển báo thực tế. Các con số km là ước tính.

Đây là bản mã nguồn chưa được thử GPS thực địa trên iPhone. Tiến độ lưu bằng `localStorage` của trình duyệt, không đồng bộ giữa thiết bị.
