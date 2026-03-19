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
  
<html>
<head>
  <title>Game Hub</title>

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
      text-align: center;
      font-size: 22px;
      font-weight: bold;
      box-shadow: 0 0 10px #0f0;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
      gap: 15px;
      padding: 20px;
    }

    .card {
      background: #1e293b;
      border-radius: 12px;
      padding: 15px;
      text-align: center;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 0 10px #000;
    }

    .card:hover {
      transform: scale(1.05);
      background: #334155;
      box-shadow: 0 0 15px #0f0;
    }

    .icon {
      font-size: 40px;
    }

    canvas {
      display: block;
      margin: 20px auto;
      border: 2px solid #0f0;
      border-radius: 10px;
      background: black;
    }

    #backBtn {
      display: none;
      margin: 10px;
      padding: 10px;
      background: red;
      border: none;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>

<body>

<header>🎮 Game Hub</header>

<button id="backBtn" onclick="goHome()">⬅ Back</button>

<div id="menu" class="grid">

  <div class="card" onclick="startSnake()">
    <div class="icon">🐍</div>
    <p>Snake</p>
  </div>

  <div class="card" onclick="startFlappy()">
    <div class="icon">🐤</div>
    <p>Flappy</p>
  </div>

  <div class="card" onclick="startPong()">
    <div class="icon">🏓</div>
    <p>Pong</p>
  </div>

  <div class="card" onclick="startBreakout()">
    <div class="icon">🧱</div>
    <p>Breakout</p>
  </div>

</div>

<canvas id="gameCanvas" width="500" height="400"></canvas>

<script>
const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");
let gameLoop;

function showGame() {
  document.getElementById("menu").style.display = "none";
  document.getElementById("backBtn").style.display = "inline-block";
}

function goHome() {
  clearInterval(gameLoop);
  document.getElementById("menu").style.display = "grid";
  document.getElementById("backBtn").style.display = "none";
  ctx.clearRect(0,0,500,400);
}

// 🐍 Snake
function startSnake() {
  showGame();
  let snake=[{x:200,y:200}], dx=20, dy=0;
  let food={x:100,y:100};
  document.onkeydown=e=>{
    if(e.key==="ArrowUp"){dx=0;dy=-20;}
    if(e.key==="ArrowDown"){dx=0;dy=20;}
    if(e.key==="ArrowLeft"){dx=-20;dy=0;}
    if(e.key==="ArrowRight"){dx=20;dy=0;}
  };
  gameLoop=setInterval(()=>{
    ctx.fillStyle="black"; ctx.fillRect(0,0,500,400);
    let head={x:snake[0].x+dx,y:snake[0].y+dy};
    snake.unshift(head);
    if(head.x===food.x&&head.y===food.y){
      food={x:Math.floor(Math.random()*25)*20,y:Math.floor(Math.random()*20)*20};
    } else snake.pop();
    ctx.fillStyle="lime"; snake.forEach(s=>ctx.fillRect(s.x,s.y,20,20));
    ctx.fillStyle="red"; ctx.fillRect(food.x,food.y,20,20);
  },100);
}

// 🐤 Flappy
function startFlappy() {
  showGame();
  let y=200, v=0;
  document.onclick=()=>v=-8;
  gameLoop=setInterval(()=>{
    ctx.fillStyle="skyblue"; ctx.fillRect(0,0,500,400);
    v+=0.5; y+=v;
    ctx.fillStyle="yellow"; ctx.fillRect(50,y,20,20);
    if(y>380){clearInterval(gameLoop); alert("Game Over");}
  },30);
}

// 🏓 Pong
function startPong() {
  showGame();
  let ball={x:250,y:200,dx:4,dy:4};
  let paddle={x:200};
  document.onmousemove=e=>paddle.x=e.clientX-50;
  gameLoop=setInterval(()=>{
    ctx.fillStyle="black"; ctx.fillRect(0,0,500,400);
    ball.x+=ball.dx; ball.y+=ball.dy;
    if(ball.x<0||ball.x>500) ball.dx*=-1;
    if(ball.y<0) ball.dy*=-1;
    if(ball.y>380 && ball.x>paddle.x && ball.x<paddle.x+100) ball.dy*=-1;
    if(ball.y>400){clearInterval(gameLoop); alert("Game Over");}
    ctx.fillStyle="lime"; ctx.beginPath();
    ctx.arc(ball.x,ball.y,10,0,6.28); ctx.fill();
    ctx.fillStyle="cyan"; ctx.fillRect(paddle.x,390,100,10);
  },20);
}

// 🧱 Breakout
function startBreakout() {
  showGame();
  let ball={x:250,y:200,dx:3,dy:-3};
  let paddle={x:200};
  let bricks=[];
  for(let i=0;i<5;i++){
    for(let j=0;j<8;j++){
      bricks.push({x:j*60+10,y:i*20+30,alive:true});
    }
  }
  document.onmousemove=e=>paddle.x=e.clientX-50;
  gameLoop=setInterval(()=>{
    ctx.fillStyle="black"; ctx.fillRect(0,0,500,400);
    bricks.forEach(b=>{
      if(b.alive){
        ctx.fillStyle="orange";
        ctx.fillRect(b.x,b.y,50,15);
        if(ball.x>b.x && ball.x<b.x+50 && ball.y>b.y && ball.y<b.y+15){
          b.alive=false; ball.dy*=-1;
        }
      }
    });
    ball.x+=ball.dx; ball.y+=ball.dy;
    if(ball.x<0||ball.x>500) ball.dx*=-1;
    if(ball.y<0) ball.dy*=-1;
    if(ball.y>400){clearInterval(gameLoop); alert("Game Over");}
    if(ball.y>380 && ball.x>paddle.x && ball.x<paddle.x+100) ball.dy*=-1;
    ctx.fillStyle="lime"; ctx.beginPath();
    ctx.arc(ball.x,ball.y,10,0,6.28); ctx.fill();
    ctx.fillStyle="cyan"; ctx.fillRect(paddle.x,390,100,10);
  },20);
}
</script>

</body>
</html>
