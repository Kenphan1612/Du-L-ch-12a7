# Du-L-ch-12a7
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Soha Travel - Du Lịch Cần Thơ & Cà Mau</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="logo">
            <img src="logo.png" alt="Soha Travel">
        </div>
        <nav>
            <ul>
                <li><a href="#home">Trang chủ</a></li>
                <li><a href="#about">Giới thiệu</a></li>
                <li><a href="#services">Dịch vụ</a></li>
                <li><a href="#contact">Liên hệ</a></li>
            </ul>
        </nav>
    </header>

    <!-- Banner Section -->
    <section id="home" class="banner">
        <h1>Chào mừng đến với Soha Travel</h1>
        <p>Khám phá Cần Thơ và Cà Mau cùng Soha Travel</p>
        <a href="#about" class="btn">Xem thêm</a>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>Chương trình du lịch Cần Thơ - Cà Mau</h2>
        <p>Trải nghiệm chuyến du lịch khám phá các danh lam thắng cảnh từ Cần Thơ đến Cà Mau.</p>
        <ul>
            <li>Tham quan Vườn Quốc Gia Mũi Cà Mau</li>
            <li>Khám phá hệ sinh thái rừng đước</li>
            <li>Check-in tại cột mốc Tọa độ Quốc Gia GPS 0001</li>
        </ul>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2>Dịch vụ của chúng tôi</h2>
        <div class="service">
            <h3>Vận chuyển</h3>
            <p>Xe đưa đón suốt tuyến theo lịch trình.</p>
        </div>
        <div class="service">
            <h3>Ăn uống</h3>
            <p>Cung cấp bữa sáng và bữa chính.</p>
        </div>
        <div class="service">
            <h3>Vé tham quan</h3>
            <p>Miễn phí tất cả các vé tham quan trong chương trình.</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Liên hệ với chúng tôi</h2>
        <p>Số điện thoại: 0939 108 999</p>
        <p>Email: info@sohatravel.net</p>
        <p>Địa chỉ: B2-22 Nguyễn Văn Quang, Cần Thơ</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Soha Travel. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* style.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    display: flex;
    justify-content: space-between;
    padding: 10px 20px;
}

header nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
}

header nav ul li {
    margin-left: 20px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.banner {
    background-image: url('banner.jpg');
    background-size: cover;
    background-position: center;
    height: 400px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    text-align: center;
}

.banner h1 {
    font-size: 3em;
}

.banner p {
    font-size: 1.5em;
}

section {
    padding: 20px;
    margin: 20px 0;
}

#about, #services, #contact {
    background-color: #f4f4f4;
    padding: 40px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}
// script.js
document.addEventListener("DOMContentLoaded", function() {
    // Smooth scroll effect
    const links = document.querySelectorAll("nav ul li a");
    for (const link of links) {
        link.addEventListener("click", smoothScroll);
    }

    function smoothScroll(event) {
        event.preventDefault();
        const targetId = event.currentTarget.getAttribute("href").substring(1);
        const targetElement = document.getElementById(targetId);
        window.scrollTo({
            top: targetElement.offsetTop,
            behavior: "smooth"
        });
    }
});
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'];
    $email = $_POST['email'];
    $message = $_POST['message'];

    $to = "info@sohatravel.net";
    $subject = "Liên hệ từ khách hàng: $name";
    $body = "Tên: $name\nEmail: $email\nTin nhắn: $message";
    
    mail($to, $subject, $body);

    echo "Cảm ơn bạn đã liên hệ!";
}
?>
