<!DOCTYPE html>
<html>
<head>
<title>Be My Valentine 💖</title>

<style>
body {
  margin: 0;
  overflow: hidden;
  text-align: center;
  font-family: Arial, sans-serif;
  background: linear-gradient(to right, #ff758c, #ff7eb3);
  color: white;
}

h1 {
  margin-top: 120px;
  font-size: 38px;
}

p {
  font-size: 20px;
}

button {
  font-size: 20px;
  padding: 12px 30px;
  margin: 20px;
  border: none;
  border-radius: 25px;
  cursor: pointer;
  transition: 0.3s;
}

#yes {
  background-color: white;
  color: #ff4d6d;
}

#yes:hover {
  transform: scale(1.1);
}

#no {
  background-color: #ff4d6d;
  color: white;
  position: absolute;
}

/* Floating hearts */
.heart {
  position: absolute;
  color: white;
  font-size: 20px;
  animation: float 5s linear infinite;
}

@keyframes float {
  0% { transform: translateY(100vh); opacity: 1; }
  100% { transform: translateY(-10vh); opacity: 0; }
}
</style>
</head>

<body>

<h1>Will You Be My Valentine? 💖</h1>
<p>You are my today, my tomorrow, and my forever ❤️</p>

<button id="yes" onclick="yesClick()">Yes, Always 💕</button>
<button id="no" onmouseover="moveButton()">No 🙈</button>

<!-- Romantic Music (royalty-free sample link) -->
<audio autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_115b9b7e6c.mp3?filename=romantic-love-112194.mp3" type="audio/mpeg">
</audio>

<script>
function yesClick() {
  document.body.innerHTML = "<h1>YAYYYY 💍💖<br>You just made me the happiest person alive! ❤️</h1>";
}

function moveButton() {
  var button = document.getElementById("no");
  var x = Math.random() * (window.innerWidth - 100);
  var y = Math.random() * (window.innerHeight - 50);
  button.style.left = x + "px";
  button.style.top = y + "px";
}

// Floating hearts generator
setInterval(function() {
  var heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (Math.random() * 20 + 10) + "px";
  document.body.appendChild(heart);

  setTimeout(function() {
    heart.remove();
  }, 5000);
}, 300);
</script>

</body>
</html>
