<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tee, Will You Be My Valentine? 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #ff6b9d 0%, #c471ed 50%, #f093fb 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Floating hearts background */
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.4);
            transform: rotate(45deg);
            animation: float 6s infinite;
        }

        .heart:before,
        .heart:after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.4);
            border-radius: 50%;
        }

        .heart:before {
            left: -10px;
        }

        .heart:after {
            top: -10px;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(45deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(45deg);
                opacity: 0;
            }
        }

        .container {
            background: white;
            padding: 60px 40px;
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(255, 105, 180, 0.4);
            text-align: center;
            max-width: 500px;
            width: 90%;
            position: relative;
            z-index: 10;
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .emoji {
            font-size: 80px;
            margin-bottom: 20px;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-20px);
            }
            60% {
                transform: translateY(-10px);
            }
        }

        h1 {
            background: linear-gradient(135deg, #ff1744 0%, #c471ed 50%, #ff6b9d 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-size: 2.5em;
            margin-bottom: 20px;
            line-height: 1.2;
            font-weight: bold;
        }

        .message {
            color: #555;
            font-size: 1.2em;
            margin-bottom: 40px;
            line-height: 1.6;
        }

        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        button {
            padding: 15px 40px;
            font-size: 1.2em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .yes-btn {
            background: linear-gradient(135deg, #ff1744 0%, #ff6b9d 100%);
            color: white;
        }

        .yes-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 20px rgba(255, 23, 68, 0.5);
        }

        .no-btn {
            background: #e0e0e0;
            color: #666;
            position: absolute;
            transition: all 0.3s ease;
        }

        .no-btn:hover {
            background: #d0d0d0;
        }

        .celebration {
            display: none;
            animation: fadeIn 1s ease-in;
        }

        .celebration h2 {
            background: linear-gradient(135deg, #ff1744 0%, #c471ed 50%, #ff6b9d 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-size: 2em;
            margin: 20px 0;
        }

        .celebration p {
            color: #555;
            font-size: 1.3em;
            margin: 10px 0;
        }

        .hearts-explosion {
            font-size: 40px;
            margin: 20px 0;
            animation: pulse 1s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }

        @media (max-width: 600px) {
            .container {
                padding: 40px 20px;
            }
            h1 {
                font-size: 2em;
            }
            .message {
                font-size: 1em;
            }
            button {
                padding: 12px 30px;
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <!-- Floating hearts background -->
    <script>
        // Create floating hearts
        for (let i = 0; i < 20; i++) {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDelay = Math.random() * 6 + 's';
            heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
            document.body.appendChild(heart);
        }
    </script>

    <div class="container">
        <div id="question">
            <div class="emoji">💝</div>
            <h1>Tee, Will You Be My Valentine?</h1>
            <p class="message">
                Every moment with you is special, and I can't imagine Valentine's Day without you by my side. 
                You make every day brighter! 🌟
            </p>
            <div class="buttons">
                <button class="yes-btn" onclick="sayYes()">Yes! 💕</button>
                <button class="no-btn" id="noBtn" onmouseover="runAway()" onclick="runAway()">No</button>
            </div>
        </div>

        <div id="celebration" class="celebration">
            <div class="hearts-explosion">💕💖💗💓💝💞🌹</div>
            <h2>Yay! 🎉</h2>
            <p>Tee, you just made me the happiest person!</p>
            <p>Can't wait to spend Valentine's Day with you! 💑</p>
            <div class="hearts-explosion">💕💖💗💓💝💞🌹</div>
        </div>
    </div>

    <script>
        let noBtnClicks = 0;

        function sayYes() {
            document.getElementById('question').style.display = 'none';
            document.getElementById('celebration').style.display = 'block';
            
            // Create confetti effect
            for (let i = 0; i < 50; i++) {
                createConfetti();
            }
        }

        function runAway() {
            const noBtn = document.getElementById('noBtn');
            const container = document.querySelector('.container');
            
            noBtnClicks++;
            
            // Get viewport dimensions
            const viewportWidth = window.innerWidth;
            const viewportHeight = window.innerHeight;
            
            // Generate random position anywhere on the screen
            const randomX = Math.random() * (viewportWidth - 150);
            const randomY = Math.random() * (viewportHeight - 60);
            
            noBtn.style.position = 'fixed';
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
            
            // Make the button text change after a few attempts
            if (noBtnClicks === 3) {
                noBtn.textContent = "You can't catch me! 😜";
            } else if (noBtnClicks === 5) {
                noBtn.textContent = "Still no? 🥺";
            } else if (noBtnClicks === 8) {
                noBtn.textContent = "Please? 💔";
            }
        }

        function createConfetti() {
            const confetti = document.createElement('div');
            confetti.innerHTML = ['💕', '💖', '💗', '💓', '💝', '💞', '🌹', '⭐', '❤️'][Math.floor(Math.random() * 9)];
            confetti.style.position = 'fixed';
            confetti.style.left = Math.random() * 100 + '%';
            confetti.style.top = '-50px';
            confetti.style.fontSize = (Math.random() * 20 + 20) + 'px';
            confetti.style.animation = `float ${Math.random() * 3 + 3}s linear`;
            confetti.style.zIndex = '1000';
            document.body.appendChild(confetti);
            
            setTimeout(() => {
                confetti.remove();
            }, 6000);
        }
    </script>
</body>
</html>
