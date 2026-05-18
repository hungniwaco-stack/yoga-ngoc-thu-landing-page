# Ghi chú dự án Yoga Ngọc Thư

Ngày thực hiện: 2026-05-18

## Mục tiêu

Tạo landing page online cho Yoga Ngọc Thư dựa trên nội dung trong file Word, dùng ảnh thật trong thư mục `Anh`, đưa lên GitHub Pages.

## Nguồn nội dung

- File gốc: `Yoga Võ Ngọc Thư.docx`
- File đã viết lại: `Yoga Võ Ngọc Thư - bản viết lại.docx`
- Nội dung chính:
  - Dịch vụ: Dạy Yoga Ngọc Thư
  - Thông điệp: Đánh thức năng lượng, cân bằng thân tâm
  - Khách hàng mục tiêu: phụ nữ 25-45 tuổi, dân văn phòng, mẹ sau sinh, người muốn giảm stress, giữ dáng, cải thiện sức khỏe
  - Giọng văn: gần gũi, mạnh mẽ, truyền cảm hứng
  - Các nhận định sức khỏe cần diễn đạt thận trọng bằng “hỗ trợ”, “có thể”, “tùy thể trạng”

## File đã tạo/chỉnh

- `index.html`: landing page tĩnh hoàn chỉnh
- `Anh/`: ảnh thật dùng trong landing page
- `README.md`: mô tả repo
- `.gitignore`: bỏ qua file Word và thư mục skill phụ
- `PROJECT_NOTES.md`: ghi chú này

## Landing page đã làm

Các section hiện có:

- Header/sticky nav
- Hero
- Nỗi đau khách hàng
- Lợi ích nổi bật
- Lộ trình tập
- Kết quả có thể hướng tới
- Vì sao chọn Yoga Ngọc Thư
- Thông tin đăng ký/tư vấn
- Gallery hình ảnh lớp học
- FAQ
- Final CTA
- Liên hệ
- Footer

## Ảnh đã dùng

- `Anh/05.jpg`: hero background, final CTA background, ảnh lớn gallery
- `Anh/00.jpg`: hero card và gallery
- `Anh/03.jpg`: section lợi ích
- `Anh/01.jpg`, `Anh/02.jpg`, `Anh/04.jpg`: gallery
- `Anh/chan-dung.jpg`: ảnh chân dung nguồn, tên ASCII để dùng an toàn trên web/GitHub Pages
- `Anh/chan-dung-logo.jpg`: logo tròn ở header, được crop từ `Anh/chan-dung.jpg`
- Text thương hiệu ở header đang dùng chữ in hoa: `YOGA NGỌC THƯ`, có nền pill sáng, viền xanh nhẹ và đổ bóng để nổi bật hơn.

## Thay đổi sau cùng

Đã thêm ảnh bảng hiệu luxury vào đầu trang:

- File ảnh: `Anh/bang-hieu-luxury-yoga.png`
- Nguồn ban đầu: `C:/Users/Admin/Downloads/01. Bảng hiệu - Phong cách Luxury Yoga Studio (sang trọng – thu hút) 2.png`
- Vị trí hiển thị: section đầu trang, ngay dưới header
- Ảnh bảng hiệu phải hiển thị đủ toàn bộ nội dung, dùng `height: auto` và `object-fit: contain`, không dùng `cover` để tránh cắt chữ “PHÒNG TẬP YOGA”.

Đã thêm số tư vấn/liên hệ/Zalo:

- Số điện thoại: `0918 890 212`
- Link gọi điện: `tel:0918890212`
- Link Zalo: `https://zalo.me/0918890212`
- Vị trí: hero, khối tư vấn, final CTA/liên hệ

Trước đó đã xóa form liên hệ gồm:

- Họ và tên
- Số điện thoại
- Mục tiêu chính
- Khung giờ tiện trao đổi
- Ghi chú thêm
- Nút “Gửi thông tin tư vấn”

Phần liên hệ hiện chỉ còn card thông tin Yoga Ngọc Thư và các bullet lợi ích.

## GitHub

- Tài khoản GitHub CLI đã đăng nhập: `hungniwaco-stack`
- Repo: `https://github.com/hungniwaco-stack/yoga-ngoc-thu-landing-page`
- Website public: `https://hungniwaco-stack.github.io/yoga-ngoc-thu-landing-page/`
- Nhánh deploy: `main`
- GitHub Pages source: branch `main`, path `/`

## Vercel

- Tài khoản Vercel CLI đã đăng nhập: `hungniwaco-8245`
- Vercel team/scope: `hungs-projects-fdde2488`
- Project Vercel hiện tại: `yoga-ngocthu`
- Repo GitHub đã được Vercel kết nối: `https://github.com/hungniwaco-stack/yoga-ngoc-thu-landing-page`
- Dashboard/inspect: `https://vercel.com/hungs-projects-fdde2488/yoga-ngocthu`
- Website Vercel production public chính thức: `https://yoga-ngocthu.vercel.app`
- Link cũ vẫn có thể còn hoạt động: `https://landing-page-planner.vercel.app`
- Đã tắt SSO deployment protection để domain `https://yoga-ngocthu.vercel.app` truy cập công khai.
- Lệnh deploy production thủ công: `npx vercel --prod --yes`
- `.vercel` được ignore trong Git; `.vercelignore` dùng để không upload file Word/thư mục phụ lên Vercel.

## Lưu ý lần sau

- Không hỏi lại thông tin nền của dự án nếu chỉ cần chỉnh landing page hiện tại.
- Khi chỉnh nội dung/ảnh:
  1. Sửa `index.html`
  2. Kiểm tra local hoặc URL Pages
  3. `git add index.html`
  4. `git commit -m "..."`
  5. `git push`
  6. Chờ GitHub Pages/Vercel build xong
- Nếu cần deploy Vercel thủ công sau khi sửa local, chạy `npx vercel --prod --yes`.
- Nếu trang online vẫn hiện bản cũ, dùng cache-busting như `?v=<commit>` hoặc refresh mạnh `Ctrl + F5`.
- Không đưa file `.docx` lên GitHub vì đã được ignore.
