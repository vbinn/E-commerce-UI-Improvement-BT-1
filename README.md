# E-commerce-UI-Improvement-BT-1
# MINI MODE – Giao diện website thương mại điện tử

## 1. Giới thiệu

MINI MODE là dự án giao diện cửa hàng thời trang minh họa, được xây dựng bằng HTML5 và CSS3. Trang web gồm tiêu đề, thanh điều hướng, banner khuyến mãi, danh sách bốn sản phẩm mẫu và chân trang. Nội dung tập trung vào **cách hiển thị giá bán hiện tại, giá gốc, phần trăm giảm giá và số tiền tiết kiệm** để khách hàng dễ so sánh mức giá.

Đây là bài tập giao diện tĩnh: sản phẩm và giá chỉ mang tính minh họa, không có chức năng đặt hàng hay thanh toán.

## 2. Website tham khảo

- **Tên website:** UNIQLO Việt Nam.
- **URL:** https://www.uniqlo.com/vn/vi/
- **Khu vực khảo sát:** Trang chủ, danh mục sản phẩm và trang chi tiết sản phẩm; trọng tâm là khu vực thông tin giá và nội dung khuyến mãi.

Dự án MINI MODE được thiết kế độc lập để thực hành, không sao chép giao diện hoặc sử dụng dữ liệu giá thực của UNIQLO.

## 3. Chức năng

- Hiển thị danh sách **4 sản phẩm mẫu**: áo thun, quần jeans, túi đeo chéo và áo khoác.
- Mỗi sản phẩm có ảnh minh họa, tên, giá khuyến mãi, giá gốc gạch ngang, tỷ lệ giảm giá và số tiền tiết kiệm.
- Mục **Xem thông tin** sử dụng thẻ HTML `<details>` và `<summary>` để mở/đóng mô tả; không cần JavaScript.
- Thanh điều hướng dẫn đến khu vực sản phẩm và phần giới thiệu trong cùng trang.
- Giao diện hỗ trợ nhiều kích thước màn hình nhờ CSS Grid và media queries: thường 4 cột trên màn hình rộng, 2 cột trên màn hình vừa/điện thoại và 1 cột trên màn hình rất hẹp.

## 4. Công nghệ

- **HTML5:** Tạo cấu trúc nội dung bằng `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` và các thẻ nội dung liên quan.
- **CSS3:** Quy định màu sắc, kiểu chữ, khoảng cách, bố cục Grid/Flexbox và cách hiển thị responsive.
- **SVG nội bộ:** Cung cấp bốn ảnh minh họa trong thư mục `images/`.

Không sử dụng backend, cơ sở dữ liệu, JavaScript hay thư viện giao diện bên ngoài.

## 5. Cách chạy

1. Giải nén dự án, giữ nguyên cấu trúc thư mục.
2. Mở thư mục `E-commerce-UI-Improvement-BT-1`.
3. Nhấp đúp vào `index.html` và mở bằng Chrome, Edge hoặc Firefox.
4. Kiểm tra rằng `style.css` và thư mục `images/` nằm đúng vị trí để giao diện và hình ảnh hiển thị.

Có thể dùng **F12 → Toggle device toolbar** để kiểm tra hiển thị điện thoại. Không cần XAMPP hay máy chủ web.

## 6. Cải tiến đã thực hiện

**Vấn đề nhận thấy:** Banner khuyến mãi cần có màu nền phù hợp hơn với phong cách cửa hàng và cần nêu thông tin ưu đãi rõ ràng. Ngoài ra, thông tin giá trên thẻ sản phẩm phải có thứ bậc trực quan để dễ so sánh.

**Thay đổi đã thực hiện:**

1. **CSS – màu banner:** Đổi `background` của `.hero` thành `#fff9eb` (vàng kem nhạt). Thuộc tính này thay đổi nền của khu vực giới thiệu/khuyến mãi; đồng thời dùng nền trắng cho `.hero-circle` để vòng tròn khuyến mãi vẫn phân biệt được với nền banner.
2. **HTML – nội dung ưu đãi:** Trong `<div class="hero-circle">`, thể hiện `SALE` và `UP TO 30%`. `<div>` chứa nội dung, class `hero-circle` liên kết đến CSS để tạo bố cục hình tròn, `<br>` ngắt dòng, `<strong>` nhấn mạnh mức giảm tối đa. Con số 30% là thông tin hiển thị tĩnh và phải khớp với dữ liệu ưu đãi minh họa.
3. **Hiển thị giá:** Giá bán hiện tại được nhấn mạnh, giá gốc dùng `<del>` để gạch ngang, tỷ lệ giảm được trình bày bằng nhãn và số tiền tiết kiệm được hiển thị riêng.

**Kết quả kỳ vọng:** Banner dễ nhận biết; khách hàng thấy ngay giá thực trả, giá tham chiếu và mức giảm giá. Đây là cải tiến thiết kế, chưa phải kết quả kiểm thử với người dùng thực tế.

## 7. Hỗ trợ từ AI

ChatGPT hỗ trợ phân tích khu vực của website tham khảo, đề xuất bố cục thẻ sản phẩm, tạo mã HTML5/CSS3, tổ chức giao diện responsive và giải thích các thẻ/thuộc tính quan trọng. Người thực hiện đã xác định hướng chỉnh sửa màu banner và số phần trăm trên banner; cần tự mở trang, kiểm tra ảnh, thông tin giá, chức năng mở mô tả và hiển thị trên điện thoại trước khi nộp bài.

Xem chi tiết tại [AI_USAGE.md]

## Cấu trúc thư mục

```text
E-commerce-UI-Improvement-BT-1/
├── index.html
├── style.css
├── README.md
├── AI_USAGE.md
└── images/
    ├── ao-thun.svg
    ├── hình ảnh web demo.pdf
    ├── quan-jeans.svg
    ├── tui-deo.svg
    └── ao-khoac.svg
```
