<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Windi!</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #fff5f5 0%, #fff0f5 50%, #ffe5e5 100%);
            color: #333;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
        }
        
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            color: #ff6b6b;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        h2 {
            font-size: 1.5rem;
            color: #d23669;
            margin-bottom: 30px;
        }
        
        .countdown {
            background-color: rgba(255,255,255,0.8);
            border-radius: 15px;
            padding: 20px;
            margin: 30px auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            max-width: 500px;
        }
        
        .countdown-title {
            font-family: 'Dancing Script', cursive;
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: #ff6b6b;
        }
        
        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 15px;
        }
        
        .countdown-item {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .countdown-number {
            font-size: 2rem;
            font-weight: bold;
            color: #d23669;
        }
        
        .countdown-label {
            font-size: 0.9rem;
            color: #666;
        }
        
        .message-box {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            margin: 30px auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            max-width: 600px;
        }
        
        .message-box::before {
            content: """;
            font-family: 'Dancing Script', cursive;
            font-size: 5rem;
            color: rgba(255,107,107,0.2);
            position: absolute;
            top: -20px;
            left: 10px;
        }
        
        .message-box::after {
            content: """;
            font-family: 'Dancing Script', cursive;
            font-size: 5rem;
            color: rgba(255,107,107,0.2);
            position: absolute;
            bottom: -50px;
            right: 10px;
        }
        
        .message-content {
            font-size: 1.1rem;
            line-height: 1.6;
            text-align: center;
            margin-bottom: 20px;
        }
        
        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #ff6b6b;
            text-align: right;
            margin-top: 20px;
        }
        
        .game-container {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            margin: 30px auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            max-width: 600px;
        }
        
        .game-title {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #ff6b6b;
            margin-bottom: 20px;
        }
        
        .game-question {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #333;
        }
        
        .game-options {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .game-option {
            background-color: #ff6b6b;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
        }
        
        .game-option:hover {
            background-color: #d23669;
            transform: translateY(-3px);
            box-shadow: 0 5px 10px rgba(0,0,0,0.2);
        }
        
        .game-result {
            margin-top: 20px;
            font-size: 1.1rem;
            min-height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #d23669;
        }
        
        .photo-frame {
            margin: 30px auto;
            width: 200px;
            height: 200px;
            border: 10px solid white;
            border-radius: 50%;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            overflow: hidden;
            position: relative;
        }
        
        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: rgba(255,107,107,0.7);
            transform: rotate(45deg);
            animation: float 5s ease-in-out infinite;
        }
        
        .heart:before, .heart:after {
            content: '';
            width: 20px;
            height: 20px;
            background-color: rgba(255,107,107,0.7);
            border-radius: 50%;
            position: absolute;
        }
        
        .heart:before {
            top: -10px;
            left: 0;
        }
        
        .heart:after {
            top: 0;
            left: -10px;
        }
        
        @keyframes float {
            0% {
                transform: rotate(45deg) translateY(0) translateX(0);
                opacity: 1;
            }
            100% {
                transform: rotate(45deg) translateY(-500px) translateX(100px);
                opacity: 0;
            }
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .countdown-timer {
                gap: 10px;
            }
            
            .countdown-number {
                font-size: 1.5rem;
            }
            
            .game-options {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="hearts" id="hearts"></div>
    
    <div class="container">
        <header>
            <h1>Happy Birthday Windi!</h1>
            <h2>Turning 19 on July 13th, 2025</h2>
        </header>
        
        <div class="photo-frame">
            <img src="windi.jpg" alt="" />
        </div>
        
        <div class="countdown">
            <div class="countdown-title">Menuju Hari Spesialmu</div>
            <div class="countdown-timer" id="countdown">
                <div class="countdown-item">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Days</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Hours</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Minutes</div>
                </div>
                <div class="countdown-item">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Seconds</div>
                </div>
            </div>
        </div>
        
        <div class="message-box">
            <div class="message-content">
                Selamat ulang tahun ke-19, Windi! 🎉<br><br>
                happy birthday my love. i love you so much. know that i'll forever love and adore you. you are worthy of so much love and care in this world. you deserve anything and everything, im so happy with you. im so proud of you for making it to your special day. you've been through so much and im so proud of you for always being your bright positive brave self in this cruel world. i hope you spend this day with lots of love and appreciation for you. you mean the world to me.

Happy birthday baby.<br><br>
                Semoga tahun ini penuh dengan kebahagiaan, pencapaian, dan momen-momen indah untuk kita berdua.<br><br>
                Aku bangga melihatmu tumbuh menjadi gadis yang mandiri dan penuh perhatian. Selamat ulang tahun! Aku selalu di sini untukmu.<br><br>
                Dengan tulus,
            </div>
            <div class="signature" id="signature"></div>
        </div>
        
        <div class="game-container">
            <div class="game-title">Game Kejutan Ulang Tahun</div>
            <div class="game-question" id="game-question">Pilih sayang sama pacar kamu apa engak:</div>
            <div class="game-options" id="game-options">
                <button class="game-option" onclick="nextQuestion(1)">sayang aku nga?</button>
                <button class="game-option" onclick="nextQuestion(2)">ga pernah sayang</button>
                <button class="game-option" onclick="nextQuestion(3)">engak sayang</button>
                <button class="game-option" onclick="nextQuestion(4)">udah pasti jelas sayang aku banget ya</button>
            </div>
            <div class="game-result" id="game-result"></div>
        </div>
        
        <footer>
            Made with ❤️ for Windi's 19th Birthday | July 13th, 2025
        </footer>
    </div>
    
    <script>
        // Countdown timer
        function updateCountdown() {
            const birthday = new Date('July 13, 2025 00:00:00').getTime();
            const now = new Date().getTime();
            const distance = birthday - now;
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            document.getElementById('days').innerHTML = days;
            document.getElementById('hours').innerHTML = hours;
            document.getElementById('minutes').innerHTML = minutes;
            document.getElementById('seconds').innerHTML = seconds;
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
        
        // Love particles
        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const heartCount = 30;
            
            for (let i = 0; i < heartCount; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart');
                
                // Random position
                const posX = Math.random() * window.innerWidth;
                const posY = Math.random() * window.innerHeight;
                
                // Random size
                const size = Math.random() * 20 + 10;
                
                // Random animation duration
                const duration = Math.random() * 10 + 5;
                
                // Random delay
                const delay = Math.random() * 5;
                
                heart.style.left = posX + 'px';
                heart.style.top = posY + 'px';
                heart.style.width = size + 'px';
                heart.style.height = size + 'px';
                heart.style.animationDuration = duration + 's';
                heart.style.animationDelay = delay + 's';
                
                heartsContainer.appendChild(heart);
            }
        }
        
        // Signature animation
        function animateSignature() {
            const signature = document.getElementById('signature');
            const names = ["Seseorang yang menyayangimu", "Teman hidupmu", "Sahabatmu"];
            let currentIndex = 0;
            
            function rotateNames() {
                signature.style.opacity = 0;
                setTimeout(() => {
                    signature.textContent = names[currentIndex];
                    signature.style.opacity = 1;
                    currentIndex = (currentIndex + 1) % names.length;
                }, 500);
            }
            
            setInterval(rotateNames, 3000);
        }
        
        // Birthday game
        const gameQuestions = [
            {
                question: "kasih aku hadiah:",
                options: ["kirim foto yang banyak ke aku", "chat aku terus tulis alasan kamu mau sama aku", "hal kecil apa dariku yang paling kamu syukuri ada di hidupmu?", "Quality time berdua"],
                results: []
            },
            {
                question: "LOVE YOU SAYANGKU IHHH GEMESSSSSSS",
                options: ["Ini untuk gadis tercantik di dunia", "Semoga harimu menyenangkan sayang", "Aku mencintaimu lebih dari apapun", "Kamu berarti segalanya bagiku"],
                results: []
            },
            {
                question: "Selamat ulang tahun bocill",
                options: ["kamu cantik banget", "kamu imut banget", "admin ladies", "lucu gemesssss"],
                results: []
            },
            {
                question: "Apa harapanmu untuk Windi di tahun ini?",
                options: ["Semoga selalu bahagia", "Semoga sukses dalam segala hal", "Semoga kesehatan selalu menyertai", "Semoga hubungan kita semakin kuat"],
                results: []
            }
        ];
        
        const finalMessages = [
            "Semoga di umur baru ini kamu selalu dikelilingi orang-orang baik, rezeki yang lancar, dan semua doa indahmu terkabul satu per satu.",
            "Semoga setiap langkahmu ke depan selalu ditemani kebahagiaan dan aku bisa terus ada di sampingmu, mendukung apa pun impianmu.",
            "“Semoga hatimu selalu tenang, pikiranmu selalu jernih, dan hatimu selalu hangat sama cinta kita",
            "Semoga kita bisa terus sama-sama, saling menguatkan, saling sayang, dan saling jaga, sampai nanti kita rayain ulang tahunmu bareng-bareng terus."
        ];
        
        let currentQuestion = 0;
        let selectedOptions = [];
        
        function nextQuestion(option) {
            selectedOptions.push(option);
            
            if (currentQuestion < gameQuestions.length - 1) {
                currentQuestion++;
                document.getElementById('game-question').textContent = gameQuestions[currentQuestion].question;
                
                const optionsContainer = document.getElementById('game-options');
                optionsContainer.innerHTML = '';
                
                gameQuestions[currentQuestion].options.forEach((opt, index) => {
                    const button = document.createElement('button');
                    button.className = 'game-option';
                    button.textContent = opt;
                    button.onclick = function() { nextQuestion(index + 1); };
                    optionsContainer.appendChild(button);
                });
                
                document.getElementById('game-result').textContent = '';
            } else {
                // Game finished
                const randomMessage = finalMessages[Math.floor(Math.random() * finalMessages.length)];
                document.getElementById('game-result').innerHTML = `<strong>${randomMessage}</strong><br><br>Terima kasih telah memainkan game ini! aku sangat sayang banget sama kamu i love you sayangku.`;
                document.getElementById('game-options').style.display = 'none';
                
                // Reset game after 5 seconds
                setTimeout(resetGame, 5000);
            }
        }
        
        function resetGame() {
            currentQuestion = 0;
            selectedOptions = [];
            document.getElementById('game-question').textContent = gameQuestions[0].question;
            
            const optionsContainer = document.getElementById('game-options');
            optionsContainer.innerHTML = '';
            optionsContainer.style.display = 'flex';
            
            gameQuestions[0].options.forEach((opt, index) => {
                const button = document.createElement('button');
                button.className = 'game-option';
                button.textContent = opt;
                button.onclick = function() { nextQuestion(index + 1); };
                optionsContainer.appendChild(button);
            });
            
            document.getElementById('game-result').textContent = '';
        }
        
        // Initialize
        window.onload = function() {
            createHearts();
            animateSignature();
        };
    </script>
</body>
</html>

