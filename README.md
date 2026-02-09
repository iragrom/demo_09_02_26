<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Космос: Бесконечная Тайна</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            color: #ffffff;
            overflow-x: hidden;
            min-height: 100vh;
        }
        .hero {
            height: 100vh;
            background-image: url('https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
        }
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 20px;
        }
        h1 {
            font-size: 4rem;
            margin: 0 0 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            animation: glow 2s ease-in-out infinite alternate;
        }
        @keyframes glow {
            from { text-shadow: 2px 2px 4px rgba(0,0,0,0.8), 0 0 20px #00d4ff; }
            to { text-shadow: 2px 2px 4px rgba(0,0,0,0.8), 0 0 30px #00d4ff, 0 0 40px #00d4ff; }
        }
        .subtitle {
            font-size: 1.5rem;
            margin: 0 0 40px;
            opacity: 0.9;
        }
        .content {
            max-width: 1000px;
            margin: 0 auto;
            padding: 80px 20px;
            line-height: 1.8;
        }
        h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
            color: #00d4ff;
        }
        p {
            font-size: 1.2rem;
            margin-bottom: 25px;
            text-align: justify;
        }
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            animation: twinkle 2s infinite;
        }
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    
    <section class="hero">
        <div class="hero-content">
            <h1>🌌 Космос</h1>
            <p class="subtitle">Бесконечная тайна Вселенной ждет тебя</p>
        </div>
    </section>

    <section class="content">
        <h2>Открываем тайны Вселенной</h2>
        <p>Космос — это не просто пустота между звездами. Это грандиозный океан, полный чудес: от пылающих галактик до черных дыр, поглощающих свет. Представь: наша Земля — лишь песчинка в бесконечности, а Млечный Путь — одна из миллиардов галактик.</p>
        
        <h2>Путешествие к звездам</h2>
        <p>Каждая звезда — это солнце, подобное нашему, с планетами, возможно, населёнными жизнью. Телескопы вроде "Джеймса Уэбба" раскрывают нам картины Большого Взрыва, случившегося 13,8 миллиарда лет назад. Космос шепчет секреты: тёмная материя, многомерные миры, параллельные реальности.</p>
        
        <h2>Твое место во Вселенной</h2>
        <p>Смотри в ночное небо — ты часть этой симфонии. Космос вдохновляет мечтателей, ученых и художников. Может, следующий прорыв сделаешь ты? 🌟</p>
    </section>

    <script>
        // Анимированные звезды
        function createStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 2 + 's';
                starsContainer.appendChild(star);
            }
        }
        createStars();
    </script>
</body>
</html>
