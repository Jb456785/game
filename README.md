<!DOCTYPE html>
<html>
<head>
  <title>My Game Hub</title>
  <style>
    body {
      font-family: Arial;
      background: #111;
      color: white;
      text-align: center;
    }

    h1 {
      margin-top: 20px;
    }

    .game-box {
      display: inline-block;
      background: #222;
      padding: 20px;
      margin: 15px;
      border-radius: 10px;
      width: 200px;
    }

    button {
      padding: 10px;
      border: none;
      background: limegreen;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }

    iframe {
      margin-top: 20px;
      width: 90%;
      height: 400px;
      border: none;
      border-radius: 10px;
    }
  </style>
</head>

<body>

<h1>🎮 My Game Hub</h1>
<p>Play games below 👇</p>

<!-- GAME 1 -->
<div class="game-box">
  <h3>Clicker Game</h3>
  <button onclick="startClicker()">Play</button>
</div>

<!-- GAME 2 -->
<div class="game-box">
  <h3>Color Game</h3>
  <button onclick="startColor()">Play</button>
</div>

<!-- GAME 3 -->
<div class="game-box">
  <h3>Snake Game</h3>
  <button onclick="loadGame('https://playsnake.org/')">Play</button>
</div>

<!-- GAME SCREEN -->
<div id="gameArea"></div>

<script>
function startClicker() {
  document.getElementById("gameArea").innerHTML = `
    <h2>Click Game</h2>
    <button onclick="score++">Click Me</button>
    <h3 id="score">0</h3>
  `;
  let score = 0;
  setInterval(() => {
    let el = document.getElementById("score");
    if (el) el.innerText = score;
  }, 100);
}

function startColor() {
  document.getElementById("gameArea").innerHTML = `
    <h2>Click the right color!</h2>
    <button style="background:red" onclick="lose()">Red</button>
    <button style="background:green" onclick="win()">Green</button>
  `;
}

function win() {
  alert("You win!");
}

function lose() {
  alert("You lost!");
}

function loadGame(url) {
  document.getElementById("gameArea").innerHTML =
    '<iframe src="' + url + '"></iframe>';
}
</script>

</body>
</html>
