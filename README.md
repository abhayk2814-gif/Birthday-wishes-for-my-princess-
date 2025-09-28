# Birthday-wishes-for-my-princess-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Bestie 🎂💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ffe6f0, #e6f7ff);
      overflow: hidden;
    }

    .card {
      text-align: center;
      background: white;
      padding: 35px;
      border-radius: 25px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.15);
      position: relative;
      z-index: 10;
      max-width: 550px;
      animation: pop 1s ease;
    }

    .card h1 {
      font-size: 2.5rem;
      color: #ff4da6;
      margin-bottom: 15px;
    }

    .card p {
      font-size: 1.3rem;
      margin: 10px 0;
      color: #333;
      min-height: 50px;
    }

    .heart {
      font-size: 2rem;
      color: #ff66b2;
      animation: pulse 1.5s infinite;
      margin: 15px 0;
    }

    @keyframes pop {
      0% { transform: scale(0.7); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    @keyframes pulse {
      0%,100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    /* Balloons */
    .balloon {
      position: absolute;
      bottom: -150px;
      width: 60px;
      height: 80px;
      background: pink;
      border-radius: 50%;
      animation: float 8s linear infinite;
    }
    .balloon::after {
      content: '';
      position: absolute;
      top: 80px;
      left: 28px;
      width: 4px;
      height: 50px;
      background: gray;
    }
    @keyframes float {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-110vh); opacity: 0; }
    }

    /* Confetti */
    .confetti {
      position: absolute;
      width: 8px;
      height: 14px;
      background: gold;
      top: -20px;
      animation: fall 5s linear infinite;
    }
    @keyframes fall {
      0% { transform: translateY(0) rotate(0deg); }
      100% { transform: translateY(110vh) rotate(360deg); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>🎉 Happy Birthday Bestie 🎂💖</h1>
    <p id="wish">Wishing you endless smiles, laughter, and sweet moments today 💕</p>
    <p class="heart">💖💖💖</p>
    <p style="font-size:1.1rem; color:#666;">— Made with love by Abhay ✨</p>
  </div>

  <!-- Balloons -->
  <div class="balloon" style="left:10%; background:#ff99cc; animation-duration:7s;"></div>
  <div class="balloon" style="left:25%; background:#99ccff; animation-duration:9s;"></div>
  <div class="balloon" style="left:45%; background:#ffcc99; animation-duration:11s;"></div>
  <div class="balloon" style="left:65%; background:#ccffcc; animation-duration:8s;"></div>
  <div class="balloon" style="left:85%; background:#ffb3e6; animation-duration:10s;"></div>

  <!-- Confetti & Wishes Script -->
  <script>
    // Rotating Wishes
    const wishes = [
      "🎂 May your day be filled with cake, love & laughter 💕",
      "🌸 You deserve all the happiness in the world, bestie ✨",
      "💖 Always stay the sweet, amazing person you are!",
      "🎁 I’m so lucky to have a friend like you 💫",
      "🌟 May all your dreams sparkle and come true today 💝",
      "😊 Smile big, laugh loud, and shine bright today 🎉"
    ];
    let index = 0;
    const wishText = document.getElementById("wish");

    setInterval(() => {
      index = (index + 1) % wishes.length;
      wishText.innerText = wishes[index];
    }, 3000);

    // Confetti
    function createConfetti() {
      const confetti = document.createElement("div");
      confetti.classList.add("confetti");
      confetti.style.left = Math.random() * 100 + "vw";
      confetti.style.background = ["#ff4da6","#66ccff","#ffcc00","#99ff99","#ff9966"][Math.floor(Math.random()*5)];
      confetti.style.animationDuration = (3 + Math.random()*3) + "s";
      document.body.appendChild(confetti);

      setTimeout(() => confetti.remove(), 6000);
    }
    setInterval(createConfetti, 200);
  </script>
</body>
</html>
