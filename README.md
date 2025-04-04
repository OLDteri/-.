```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blood Flowers | Official Site</title>
    <link href="https://fonts.googleapis.com/css2?family=UnifrakturMaguntia&family=Cinzel+Decorative&family=EB+Garamond&display=swap" rel="stylesheet">
    <style>
        /* Базовые стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0708;
            color: #fff;
            font-family: 'EB Garamond', serif;
            overflow-x: hidden;
            min-height: 100vh;
            position: relative;
        }

        /* Анимированный цветочный фон */
        .flower-background {
            position: fixed;
            width: 100vw;
            height: 100vh;
            z-index: -1;
            pointer-events: none;
            overflow: hidden;
        }

        .flower-particle {
            position: absolute;
            opacity: 0.1;
            animation: float 20s infinite linear;
            filter: drop-shadow(0 0 5px #ff003c);
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100vh) rotate(360deg); }
        }

        /* Стили для навигации */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem;
            background: linear-gradient(to bottom, 
                rgba(10,7,8,0.9) 0%,
                rgba(10,7,8,0.7) 100%);
            z-index: 1000;
            display: flex;
            justify-content: center;
            gap: 3rem;
            backdrop-filter: blur(5px);
        }

        .nav-link {
            color: #c72c41;
            font-family: 'Cinzel Decorative', cursive;
            text-decoration: none;
            font-size: 1.2rem;
            position: relative;
            transition: 0.3s;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #c72c41;
            transition: 0.3s;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        /* Герой-секция */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            text-align: center;
            padding: 2rem;
            position: relative;
        }

        .hero h1 {
            font-family: 'UnifrakturMaguntia', cursive;
            font-size: 5rem;
            color: #c72c41;
            text-shadow: 0 0 20px rgba(199,44,65,0.5);
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.5rem;
            letter-spacing: 3px;
        }

        /* Секция с музыкой */
        .music-section {
            padding: 4rem 2rem;
            background: rgba(10,7,8,0.9);
        }

        .album-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .album-card {
            background: rgba(25,15,18,0.8);
            border-radius: 10px;
            padding: 1.5rem;
            transition: 0.3s;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(199,44,65,0.3);
        }

        .album-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 30px rgba(199,44,65,0.2);
        }

        .album-cover {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 5px;
            margin-bottom: 1rem;
        }

        /* Кастомный аудио-плеер */
        .custom-player {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            background: rgba(10,7,8,0.9);
            padding: 1rem;
            backdrop-filter: blur(10px);
            border-top: 1px solid #c72c41;
        }

        audio {
            width: 100%;
            max-width: 600px;
            margin: 0 auto;
            display: block;
        }

        audio::-webkit-media-controls-panel {
            background: rgba(25,15,18,0.9);
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .navbar {
                gap: 1.5rem;
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Анимированные цветы -->
    <div class="flower-background">
        <!-- Добавьте больше частиц с разными задержками -->
        <div class="flower-particle" style="left:10%; animation-delay:0s">🌹</div>
        <div class="flower-particle" style="left:30%; animation-delay:5s">🥀</div>
        <div class="flower-particle" style="left:50%; animation-delay:10s">🌷</div>
        <div class="flower-particle" style="left:70%; animation-delay:15s">💮</div>
        <div class="flower-particle" style="left:90%; animation-delay:20s">🌺</div>
    </div>

    <nav class="navbar">
        <a href="#home" class="nav-link">Главная</a>
        <a href="#music" class="nav-link">Музыка</a>
        <a href="#about" class="nav-link">О нас</a>
    </nav>

    <section class="hero" id="home">
        <h1>BLOOD FLOWERS</h1>
        <p>Gothic Rock • Darkwave • Vampire Metal</p>
    </section>

    <section class="music-section" id="music">
        <div class="album-grid">
            <div class="album-card">
                <h3>Crimson Bloom (2024)</h3>
                <img src="https://i.imgur.com/4T7Xh3j.jpg" alt="Crimson Bloom" class="album-cover">
                <audio controls>
                    <source src="crimson-bloom.mp3" type="audio/mpeg">
                    Ваш браузер не поддерживает аудио элемент.
                </audio>
            </div>
            
            <div class="album-card">
                <h3>Thorn Symphony (2022)</h3>
                <img src="https://i.imgur.com/9wYVbQk.jpg" alt="Thorn Symphony" class="album-cover">
                <audio controls>
                    <source src="thorn-symphony.mp3" type="audio/mpeg">
                    Ваш браузер не поддерживает аудио элемент.
                </audio>
            </div>
        </div>
    </section>

    <div class="custom-player">
        <audio id="main-player" controls>
            <source src="current-track.mp3" type="audio/mpeg">
        </audio>
    </div>

    <script>
        // Генерация цветочных частиц
        function createFlowerParticles() {
            const container = document.querySelector('.flower-background');
            const flowers = ['🌹', '🥀', '🌷', '💮', '🌺'];
            
            for(let i = 0; i < 20; i++) {
                const flower = document.createElement('div');
                flower.className = 'flower-particle';
                flower.style.left = Math.random() * 100 + '%';
                flower.style.animationDelay = Math.random() * 20 + 's';
                flower.textContent = flowers[Math.floor(Math.random() * flowers.length)];
                container.appendChild(flower);
            }
        }

        // Инициализация
        document.addEventListener('DOMContentLoaded', () => {
            createFlowerParticles();
        });
    </script>
</body>
</html>