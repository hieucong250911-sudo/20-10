
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy 20/10 🌷</title>
<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  overflow-x: hidden;
  font-family: Arial, sans-serif;
  color: #88445f;
  background: linear-gradient(135deg, #ffe1eb, #fff7fa, #fbd6e7);
}

.card {
  width: 100%;
  max-width: 440px;
  padding: 30px 22px;
  text-align: center;
  background: rgba(255,255,255,.88);
  border: 1px solid white;
  border-radius: 26px;
  box-shadow: 0 12px 45px #c75c8825;
  position: relative;
  z-index: 1;
}

.bouquet { font-size: 54px; }

h1 {
  color: #d85d8c;
  font-size: 34px;
  margin: 14px 0;
}

p { line-height: 1.8; }

button {
  margin-top: 12px;
  padding: 14px 22px;
  border: none;
  border-radius: 30px;
  color: white;
  background: linear-gradient(120deg, #ed8db0, #d85d8c);
  font-size: 16px;
  cursor: pointer;
}

#letter {
  display: none;
  margin-top: 24px;
  padding: 18px;
  border-radius: 18px;
  background: #fff0f5;
  line-height: 1.9;
  animation: appear .8s ease;
}

footer {
  margin-top: 22px;
  color: #bd8198;
  font-size: 12px;
}

.flower {
  position: fixed;
  top: -35px;
  pointer-events: none;
  animation: fall linear forwards;
  z-index: 0;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(360deg);
  }
}

@keyframes appear {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>
</head>

<body>
<main class="card">
  <div class="bouquet">💐🌷💗</div>
  <h1>Happy 20/10</h1>
  <p>Gửi ngàn lời yêu thương đến những bông hoa của lớp mình 🌸</p>
  <p>Chúc cô giáo và 29 bạn nữ luôn vui vẻ, hạnh phúc và tỏa sáng theo cách riêng!</p>

  <button onclick="openLetter()">💌 Mở phong thư</button>

  <section id="letter">
    <h2>Gửi những bông hoa tuyệt vời 🌷</h2>
    Chúc cô và các bạn nữ có một ngày 20/10 thật vui vẻ,
    luôn mạnh khỏe, tự tin, học tập thật tốt và gặp nhiều
    điều may mắn. Cảm ơn mọi người đã góp phần làm cho
    lớp mình trở nên đặc biệt hơn mỗi ngày. 💗
    <p>Chúc mừng ngày Phụ nữ Việt Nam!</p>
    <div style="font-size:32px">🌸💖🌸</div>
  </section>

  <footer>Made with 💗 for 20/10</footer>
</main>

<script>
function openLetter() {
  document.getElementById("letter").style.display = "block";
}

function makeFlower() {
  const flower = document.createElement("div");
  flower.className = "flower";
  flower.textContent = ["🌸", "🌷", "💗", "🌼"][
    Math.floor(Math.random() * 4)
  ];
  flower.style.left = Math.random() * 100 + "vw";
  flower.style.fontSize = (16 + Math.random() * 15) + "px";
  flower.style.animationDuration = (5 + Math.random() * 4) + "s";
  document.body.appendChild(flower);
  setTimeout(() => flower.remove(), 9500);
}

setInterval(makeFlower, 650);
</script>
</body>
</html>
