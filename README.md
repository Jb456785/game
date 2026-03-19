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
    <!DOCTYPE html>
<html>
<head>
  <title>Game Portal</title>

  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: #0f172a;
      color: white;
    }

    header {
      background: #020617;
      padding: 15px;
      font-size: 20px;
      text-align: center;
      font-weight: bold;
    }

    .container {
      padding: 20px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
    }

    .card {
      background: #1e293b;
      padding: 20px;
      border-radius: 12px;
      text-align: center;
      transition: 0.2s;
    }

    .card:hover {
      transform: scale(1.05);
      background: #334155;
    }

    button {
      margin-top: 10px;
      padding: 8px;
      border: none;
      background: #22c55e;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }

    #gameArea {
      margin-top: 20px;
      text-align: center;
    }
  </style>
</head>

<body>

<header>🎮 Game Portal</header>

<div class="container">

  <div class="grid">

    <div class="card">
      <h3>Clicker</h3>
      <button onclick="clicker()">Play</button>
    </div>

    <div class="card">
      <h3>Reaction</h3>
      <button onclick="reaction()">Play</button>
    </div>

    <div class="card">
      <h3>Guess</h3>
      <button onclick="guess()">Play</button>
    </div>

    <div class="card">
      <h3>Math Quiz</h3>
      <button onclick="math()">Play</button>
    </div>

    <div class="card">
      <h3>Fast Click</h3>
      <button onclick="fast()">Play</button>
    </div>

    <div class="card">
      <h3>Timer</h3>
      <button onclick="timer()">Play</button>
    </div>

    <div class="card">
      <h3>Color Pick</h3>
      <button onclick="color()">Play</button>
    </div>

    <div class="card">
      <h3>Coin Flip</h3>
      <button onclick="coin()">Play</button>
    </div>

    <div class="card">
      <h3>Counter</h3>
      <button onclick="counter()">Play</button>
    </div>

    <div class="card">
      <h3>Spam Button</h3>
      <button onclick="spam()">Play</button>
    </div>

  </div>

  <div id="gameArea"></div>

</div>

<script>
function clicker() {
  let score = 0;
  gameArea.innerHTML =
    '<button onclick="score++">Click</button><h2 id="s">0</h2>';
  setInterval(()=>{s.innerText=score},100);
}

function reaction() {
  gameArea.innerHTML =
    '<button id="b" style="background:red">Wait</button>';
  let start;
  setTimeout(()=>{
    b.style.background="green";
    start=Date.now();
  },2000);
  b.onclick=()=>alert(Date.now()-start+" ms");
}

function guess() {
  let n=Math.floor(Math.random()*10)+1;
  let g=prompt("1-10?");
  alert(g==n?"Win":"Lose: "+n);
}

function math() {
  let a=Math.floor(Math.random()*10);
  let b=Math.floor(Math.random()*10);
  let ans=prompt(a+" + "+b);
  alert(ans==a+b?"Correct":"Wrong");
}

function fast() {
  let c=0;
  gameArea.innerHTML =
    '<button onclick="c++">FAST</button><h2 id="f">0</h2>';
  setInterval(()=>{f.innerText=c},100);
  setTimeout(()=>alert("Score: "+c),5000);
}

function timer() {
  let t=0;
  gameArea.innerHTML='<h2 id="t">0</h2>';
  setInterval(()=>{t++;document.getElementById("t").innerText=t},1000);
}

function color() {
  let pick=prompt("Type green");
  alert(pick=="green"?"Win":"Lose");
}

function coin() {
  alert(Math.random()<0.5?"Heads":"Tails");
}

function counter() {
  let c=0;
  gameArea.innerHTML =
    '<button onclick="c++">+</button><h2 id="c">0</h2>';
  setInterval(()=>{document.getElementById("c").innerText=c},100);
}

function spam() {
  alert("😂");
}
</script>

</body>
</html>
🔥 Now your site feels like:

🎮 A real game platform

🧩 Grid layout like actual game sites

⚡ Smooth hover effects

🕹️ 10 playable games

💻 Clean + professional look

🔗 Your link (example)

After publishing on GitHub Pages:

https://yourusername.github.io/games
😈 Want it EVEN CRAZIER?

I can upgrade you to:

🐍 Real Snake game

🐤 Flappy Bird clone

🧱 Breakout / Pong

🎨 Neon glowing “hacker” UI

🎮 Game icons like real sites

Just say:
👉 “add snake and flappy bird”
    '<iframe src="' + url + '"></iframe>';
}
</script>

</body>
</html>
