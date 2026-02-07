<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Rose Day My Wife</title>

<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(to bottom right, #ff4b6e, #7b001c);
        font-family: 'Segoe UI', sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        color: #fff;
    }

    /* Floating roses */
    .rose {
        position: absolute;
        font-size: 26px;
        animation: floatUp 9s linear infinite;
        opacity: 0.7;
    }

    @keyframes floatUp {
        0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
        50% { opacity: 0.8; }
        100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }

    /* Falling petals */
    .petal {
        position: absolute;
        top: -10vh;
        font-size: 20px;
        animation: fall linear infinite;
        opacity: 0.8;
    }

    @keyframes fall {
        0% {
            transform: translateX(0) translateY(0) rotate(0deg);
        }
        100% {
            transform: translateX(60px) translateY(120vh) rotate(360deg);
        }
    }

    /* Gift */
    .gift {
        font-size: 80px;
        cursor: pointer;
        animation: bounce 1.5s infinite;
    }

    @keyframes bounce {
        0%,100% { transform: translateY(0); }
        50% { transform: translateY(-15px); }
    }

    .hint {
        margin-top: 10px;
        font-size: 18px;
        color: #ffe6ea;
    }

    /* Card */
    .card {
        display: none;
        background: rgba(255,255,255,0.15);
        backdrop-filter: blur(12px);
        padding: 45px;
        border-radius: 25px;
        text-align: center;
        box-shadow: 0 0 40px rgba(0,0,0,0.4);
        max-width: 460px;
        animation: fadeIn 1.5s ease;
        z-index: 2;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: scale(0.9); }
        to { opacity: 1; transform: scale(1); }
    }

    h1 {
        font-size: 36px;
        margin-bottom: 10px;
    }

    h2 {
        font-size: 25px;
        color: #ffe6ea;
        margin-bottom: 20px;
    }

    p {
        font-size: 18px;
        line-height: 1.7;
    }

    .heart {
        font-size: 42px;
        animation: pulse 1.3s infinite;
        margin: 20px 0;
    }

    @keyframes pulse {
        0%,100% { transform: scale(1); }
        50% { transform: scale(1.25); }
    }

    .signature {
        font-size: 17px;
        color: #ffe6ea;
    }
</style>
</head>

<body>

<script>
    // Floating roses
    for (let i = 0; i < 25; i++) {
        let r = document.createElement("div");
        r.className = "rose";
        r.innerHTML = "🌹";
        r.style.left = Math.random() * 100 + "vw";
        r.style.animationDelay = Math.random() * 9 + "s";
        r.style.fontSize = (22 + Math.random() * 18) + "px";
        document.body.appendChild(r);
    }

    // Falling petals
    for (let i = 0; i < 40; i++) {
        let p = document.createElement("div");
        p.className = "petal";
        p.innerHTML = "🌸";
        p.style.left = Math.random() * 100 + "vw";
        p.style.animationDuration = (6 + Math.random() * 6) + "s";
        p.style.animationDelay = Math.random() * 6 + "s";
        p.style.fontSize = (16 + Math.random() * 14) + "px";
        document.body.appendChild(p);
    }

    function openGift() {
        document.getElementById("giftBox").style.display = "none";
        document.getElementById("card").style.display = "block";
    }
</script>

<!-- Gift -->
<div id="giftBox" style="text-align:center; z-index:2;">
    <div class="gift" onclick="openGift()">🎁</div>
    <div class="hint">Click the gift, my love ❤️</div>
</div>

<!-- Message -->
<div class="card" id="card">
    <h1>Happy Rose Day 🌹</h1>
    <h2>My Wife, Kausar Qureshi</h2>

    <p>
        My love,<br><br>
        You are the most precious rose<br>
        in the garden of my life.<br><br>
        With you, every moment blooms<br>
        with love, warmth, and happiness.
    </p>

    <div class="heart">❤️</div>

    <div class="signature">
        Forever yours,<br>
        <strong>Anwar Ansari</strong>
    </div>
</div>

</body>
</html>
