# AI Usage Log

## 1. Công cụ AI

- **Tên công cụ:** ChatGPT (OpenAI).

## 2. Mục đích sử dụng

Sử dụng AI nhằm hỗ trợ phân tích giao diện thương mại điện tử, đề xuất cách trình bày giá gốc/giá khuyến mãi/tỷ lệ giảm, thiết kế bố cục responsive, tạo giao diện mẫu bằng HTML5 và CSS3, và giải thích ý nghĩa những chỉnh sửa trong mã nguồn.

## 3. Prompt đã sử dụng

Các prompt chính (trích theo nội dung trao đổi):

> **Prompt 1 – Khảo sát website:** “Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website UNIQLO VN – https://www.uniqlo.com/vn/vi/. Hãy giúp tôi lập bảng phân tích các khu vực: trang chủ, danh mục sản phẩm, chi tiết sản phẩm, tìm kiếm, giỏ hàng ... Không khẳng định những tính năng chưa được kiểm chứng. Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI.”

> **Prompt 2 – Đề xuất cải tiến:** “Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3. Tôi muốn cải tiến khu vực: cải tiến cách hiển thị giá gốc, giá khuyến mãi và tỷ lệ giảm giá ... Hãy đề xuất bố cục giao diện, các thành phần HTML, cách tổ chức CSS, cách hiển thị trên máy tính và điện thoại, và những điểm cần kiểm tra về khả năng sử dụng. Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.”

> **Prompt 3 – Tạo giao diện:** “Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3 ... có tối thiểu 4 sản phẩm mẫu ... CSS được tách thành file riêng ... không sử dụng backend hoặc cơ sở dữ liệu.”

> **Prompt 4 – Giải thích CSS:** “body{margin:0;font-family:inter,Helvetica,sans-serif;background:var(--background);color:var(--ink);line-height:1.55} muốn đổi phông inter làm sao” và “hướng dẫn thay phông chữ inter hoặc roboto”.

> **Prompt 5 – Giải thích chỉnh sửa cá nhân:** “Trong file CSS .hero background:#fff9eb. Trong file HTML class=\"hero-circle\">SALE<br><strong>UP TO<br>30%</strong> ... giải thích vai trò đã sửa (thay đổi màu và số)”.

## 4. Kết quả AI đề xuất

- Phân tích một số khu vực chính của website tham khảo theo góc nhìn BA/UX.
- Đề xuất thẻ sản phẩm gồm hình ảnh, tên, giá khuyến mãi nổi bật, giá gốc có gạch ngang, nhãn giảm giá và số tiền tiết kiệm.
- Tạo `index.html`, `style.css` và ảnh minh họa SVG cho bốn sản phẩm; bố cục thay đổi theo kích thước màn hình.
- Giải thích vai trò của class CSS, `background`, `font-family`, `<div>`, `<br>`, `<strong>`, `<del>`, Grid và media queries.
- Gợi ý kiểm tra giá, khả năng đọc, hành vi thao tác và giao diện trên điện thoại.

## 5. Kiểm tra và điều chỉnh

**Điều chỉnh đã yêu cầu và đưa vào mã:**

- Đổi nền khu vực banner `.hero` sang `#fff9eb` để có màu vàng kem nhạt.
- Nội dung trong `hero-circle` thể hiện chương trình `SALE UP TO 30%`.
- Nền vòng tròn dùng màu trắng để phân biệt với nền banner sau khi đổi màu.

**Những điểm cần tự kiểm tra trên trình duyệt trước khi nộp:**

- Đủ bốn sản phẩm và ảnh tương ứng hiển thị đúng.
- Giá khuyến mãi, giá gốc, phần trăm giảm và số tiền tiết kiệm khớp nhau (phần trăm có thể làm tròn).
- Nhãn `UP TO 30%` không vượt mức giảm của các sản phẩm minh họa.
- Mục `Xem thông tin` có thể mở/đóng.
- Ở màn hình máy tính và điện thoại, chữ và giá không bị tràn hoặc che khuất.
- File CSS được tải; màu banner mới hiển thị đúng.

**Phần chưa sử dụng:** Không triển khai backend, cơ sở dữ liệu, giỏ hàng thực tế, thanh toán trực tuyến hoặc tính giá động bằng JavaScript. Các nội dung trên chỉ là giao diện minh họa.

## 6. Phần tôi hiểu và có thể giải thích

| Thành phần | Vai trò |
|---|---|
| `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>` | Phân chia các khu vực có ý nghĩa của trang HTML5. |
| `<article class="product-card">` | Đại diện cho một sản phẩm trong danh sách. |
| `<img>` | Hiển thị ảnh minh họa sản phẩm, có `alt` mô tả. |
| `<strong class="current-price">` | Nhấn mạnh giá khuyến mãi đang áp dụng. |
| `<del>` | Gạch ngang giá cũ đã được thay thế. |
| `.hero { background: #fff9eb; }` | Đặt màu nền vàng kem nhạt cho banner. |
| `.hero-circle` | Định dạng khu vực biểu thị chương trình SALE thành hình tròn. |
| `<br>` và `<strong>` | Ngắt dòng và nhấn mạnh nội dung `UP TO 30%`. |
| `font-family` | Chọn phông chữ cho giao diện; dự án hiện sử dụng Arial và Helvetica dự phòng. |
| `<details>` và `<summary>` | Mở/đóng thông tin sản phẩm bằng HTML, không dùng JavaScript. |

