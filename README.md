<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hương</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">
    <!-- Animate On Scroll Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --primary-pink: #ff758c;
            --secondary-pink: #ff7eb3;
            --glass: rgba(255, 255, 255, 0.25);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: #fff;
            overflow-x: hidden;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Màn hình chào */
        #welcome-screen {
            position: fixed;
            inset: 0;
            background: #000;
            z-index: 9999;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            transition: 1s;
        }

        #start-btn {
            padding: 15px 40px;
            font-size: 1.5rem;
            background: var(--primary-pink);
            border: none;
            border-radius: 50px;
            color: white;
            cursor: pointer;
            box-shadow: 0 0 20px var(--primary-pink);
            transition: 0.3s;
        }

        #start-btn:hover { transform: scale(1.1); }

        /* Nút điều khiển nhạc */
        .music-control {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
            background: var(--glass);
            backdrop-filter: blur(10px);
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            border: 1px solid rgba(255,255,255,0.5);
        }

        /* Container chính */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .glass-card {
            background: var(--glass);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 5rem;
            margin-bottom: 20px;
            text-shadow: 3px 3px 10px rgba(0,0,0,0.2);
        }

        #typing-text {
            font-size: 1.5rem;
            min-height: 1.6em;
        }

        /* Thư viện ảnh xịn */
        .photo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin: 50px 0;
        }

        .photo-item {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            aspect-ratio: 3/4;
            cursor: pointer;
        }

        .photo-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: 0.5s;
        }

        .photo-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.7));
            display: flex;
            align-items: flex-end;
            padding: 20px;
            opacity: 0;
            transition: 0.5s;
        }

        .photo-item:hover .photo-overlay { opacity: 1; }
        .photo-item:hover img { transform: scale(1.1); }

        /* Hiệu ứng cánh hoa bay */
        .heart {
            position: fixed;
            top: -10vh;
            pointer-events: none;
            animation: fall linear forwards;
            z-index: 99;
        }

        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }

        footer {
            text-align: center;
            padding: 100px 0 50px;
            font-size: 1.2rem;
        }
    </style>
</head>
<body>

    
    <div id="welcome-screen">
        <h2 style="margin-bottom: 20px;">Bạn có một thông điệp</h2>
        <button id="start-btn">Nhấn Vào</button>
    </div>

    <!-- Nhạc nền (Thay link MP3 của bạn vào đây) -->

    <div class="container">
        <header data-aos="zoom-in">
            <h1>Happy Women's Day</h1>
            <div class="glass-card">
                <p id="typing-text"></p>
            </div>
            <div style="margin-top: 50px; font-size: 2rem;">👇</div>
        </header>

        <!-- Thư viện ảnh -->
        <section class="photo-grid">
            <!-- Ảnh 1 -->
            <div class="photo-item" data-aos="fade-up">
                <img src="1.jpg" alt="Ảnh 1"> 
                <div class="photo-overlay"><h3>lời chúc của hùng</h3></div>
            </div>
            <!-- Ảnh 2 -->
            <div class="photo-item" data-aos="fade-up" data-aos-delay="100">
                <img src="2.jpg" alt="Ảnh 2"> 
                <div class="photo-overlay"><h3>lời chúc của a hy</h3></div>
            </div>
            <!-- Ảnh 3 -->
            <div class="photo-item" data-aos="fade-up" data-aos-delay="200">
                <img src="3.jpg" alt="Ảnh 3"> 
                <div class="photo-overlay"><h3>lời chúc của long</h3></div>
            </div>
            <!-- Ảnh 4 -->
            <div class="photo-item" data-aos="fade-up" data-aos-delay="300">
                <img src="4.jpg" alt="Ảnh 4"> 
                <div class="photo-overlay"><h3>lời chúc của hòa</h3></div>
            </div>
             <div class="photo-item" data-aos="fade-up" data-aos-delay="300">
                <img src="2.jpg" alt="Ảnh 4"> 
                <div class="photo-overlay"><h3>lời chúc của táo đuần</h3></div>
            </div>
             <div class="photo-item" data-aos="fade-up" data-aos-delay="300">
                <img src="1.jpg" alt="Ảnh 4"> 
                <div class="photo-overlay"><h3>lời chúc của tao</h3></div>
            </div>
        </section>

        <section class="glass-card" data-aos="flip-up" style="margin-top: 50px;">
            <h2>Gửi [Lại Quỳnh Hương],</h2>
            <p style="line-height: 1.8; margin-top: 20px;">
                Cảm ơn bạn vì đã xuất hiện và làm cho thế giới này trở nên dịu dàng hơn. 
                Chúc bạn không chỉ ngày 8/3 mà tất cả 364 ngày còn lại đều luôn tự tin, 
                được yêu thương và đậu nguyện vọng 1 nhaaaa❤️❤️❤️
            </p>
        </section>

        <footer>
            <p>Made with ❤️ by [Hảo 4.0]</p>
        </footer>
    </div>

    <!-- Scripts -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Khởi tạo AOS
        AOS.init({ duration: 1000, once: true });

        const music = document.getElementById('bg-music');
        const startBtn = document.getElementById('start-btn');
        const welcomeScreen = document.getElementById('welcome-screen');
        const typingText = document.getElementById('typing-text');

        const message = "Chào bạn tôi đại diện cho Gia Đình Hóa Học chúc mừng bạn ngày 8/3 vui vẻ nha";

        // Xử lý khi bắt đầu
        startBtn.addEventListener('click', () => {
            welcomeScreen.style.opacity = '0';
            setTimeout(() => {
                welcomeScreen.style.display = 'none';
                music.play();
                startTyping();
            }, 1000);
        });

        // Hiệu ứng gõ chữ
        let i = 0;
        function startTyping() {
            if (i < message.length) {
                typingText.innerHTML += message.charAt(i);
                i++;
                setTimeout(startTyping, 100);
            }
        }

        // Điều khiển nhạc
        function toggleMusic() {
            if (music.paused) music.play();
            else music.pause();
        }

        // Hiệu ứng trái tim/hoa rơi
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = ['🌸', '❤️', '✨', '💐'][Math.floor(Math.random() * 4)];
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 3 + 2 + "s";
            heart.style.fontSize = Math.random() * 20 + 10 + "px";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 300);
    </script>
</body>
</html>
