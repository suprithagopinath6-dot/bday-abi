<!DOCTYPE html>
<html>
<head>
  <title>Happy Birthday Esther 🎂</title>
  <style>
    body {
      background: linear-gradient(to right, pink, lavender);
      text-align: center;
      font-family: Arial, sans-serif;
      overflow: hidden;
      margin: 0;
      height: 100vh;
    }
    h1 {
      font-size: 50px;
      animation: glow 1.5s infinite alternate;
      margin-top: 100px;
    }
    @keyframes glow {
      from { color: hotpink; }
      to { color: purple; }
    }
    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: #ff69b4;
      opacity: 0.8;
      top: -10px;
      animation: fall 5s linear infinite;
    }
    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(360deg);
      }
    }
  </style>
</head>
<body>

<h1>🎉 Happy Birthday Esther 🎉</h1>
<p>You are special 💖</p>

<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<script>
  // Create confetti
  function createConfetti() {
    const confetti = document.createElement('div');
    confetti.classList.add('confetti');
    confetti.style.left = Math.random() * window.innerWidth + 'px';
    confetti.style.backgroundColor = `hsl(${Math.random()*360}, 100%, 50%)`;
    confetti.style.width = Math.random()*10+5+'px';
    confetti.style.height = Math.random()*10+5+'px';
    confetti.style.animationDuration = Math.random()*3+2+'s';
    document.body.appendChild(confetti);
    setTimeout(() => { confetti.remove(); }, 5000);
  }
  setInterval(createConfetti, 100);
</script>

</body>
</html>
