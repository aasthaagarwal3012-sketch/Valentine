# Valentine
<!DOCTYPE html>
<html>
<head>
    <title>For Kshitij ❤️</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to right, #ff9a9e, #fecfef);
            text-align: center;
            color: white;
            overflow-x: hidden;
        }

        h1 {
            margin-top: 40px;
            font-size: 40px;
            animation: glow 2s infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px white; }
            to { text-shadow: 0 0 20px red; }
        }

        .letter {
            background: rgba(255,255,255,0.2);
            padding: 20px;
            margin: 30px auto;
            width: 80%;
            border-radius: 15px;
            backdrop-filter: blur(5px);
        }

        .gift-btn {
            padding: 15px 30px;
            font-size: 18px;
            background: white;
            color: #ff4b5c;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: 0.3s;
        }

        .gift-btn:hover {
            transform: scale(1.1);
        }

        .hidden-gift {
            display: none;
            margin-top: 20px;
            font-size: 22px;
        }

        .flower {
            position: fixed;
            top: -10px;
            font-size: 24px;
            animation: fall linear infinite;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh);
            }
        }
    </style>
</head>

<body>

    <h1>Happy Valentine's Day ❤️</h1>

    <div class="letter">
        <h2>My Love 💌</h2>
        <p>
            It has been 1.5 beautiful years with you.
            Every laugh, every silly fight, every late night talk,
            every memory — I cherish all of it.
            You are my comfort, my happiness, and my favorite person.
            Thank you for choosing me every single day.
        </p>
        <p>
            I love you more than words can explain ❤️
        </p>
    </div>

    <button class="gift-btn" onclick="showGift()">Click to Open Your Gift 🎁</button>

    <div class="hidden-gift" id="gift">
        🌹 100 Virtual Roses for You 🌹 <br><br>
        🍫 Unlimited Chocolates <br><br>
        💍 A Promise to Stay With You <br><br>
        ❤️ My Whole Heart Forever ❤️
    </div>

    <script>
        function showGift() {
            document.getElementById("gift").style.display = "block";
        }

        // Floating flowers
        function createFlower() {
            const flower = document.createElement("div");
            flower.classList.add("flower");
            flower.innerHTML = "🌸";
            flower.style.left = Math.random() * 100 + "vw";
            flower.style.animationDuration = Math.random() * 3 + 3 + "s";
            document.body.appendChild(flower);

            setTimeout(() => {
                flower.remove();
            }, 6000);
        }

        setInterval(createFlower, 300);
    </script>

</body>
</html>
