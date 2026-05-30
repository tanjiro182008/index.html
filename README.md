<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sukuna Chess Academy</title>

<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&display=swap" rel="stylesheet">

<style>

*{

margin:0;

padding:0;

box-sizing:border-box;

font-family:'Cinzel',serif;

scroll-behavior:smooth;

}

body{

background:linear-gradient(-45deg,#ffffff,#f8f8f8,#fffdf4,#ffffff);

background-size:400% 400%;

animation:bgMove 15s ease infinite;

color:#111;

overflow-x:hidden;

}

@keyframes bgMove{

0%{background-position:0% 50%;}

50%{background-position:100% 50%;}

100%{background-position:0% 50%;}

}

/* Floating Chess Pieces */

.chess{

position:fixed;

font-size:70px;

color:rgba(212,175,55,.12);

pointer-events:none;

animation:float 15s linear infinite;

z-index:-1;

}

@keyframes float{

0%{

transform:translateY(120vh) rotate(0deg) scale(.8);

opacity:0;

}

20%{opacity:1;}

80%{opacity:1;}

100%{

transform:translateY(-120vh) rotate(720deg) scale(1.2);

opacity:0;

}

}

.c1{left:5%;animation-duration:12s;}

.c2{left:18%;animation-duration:18s;}

.c3{left:35%;animation-duration:14s;}

.c4{left:55%;animation-duration:16s;}

.c5{left:75%;animation-duration:13s;}

.c6{left:92%;animation-duration:20s;}

header{

height:100vh;

display:flex;

justify-content:center;

align-items:center;

text-align:center;

position:relative;

}

.hero{

animation:heroFloat 5s ease-in-out infinite;

}

@keyframes heroFloat{

0%,100%{transform:translateY(0);}

50%{transform:translateY(-15px);}

}

.hero h1{

font-size:5rem;

color:#d4af37;

animation:glow 3s ease-in-out infinite alternate;

}

@keyframes glow{

from{

text-shadow:0 0 10px rgba(212,175,55,.3);

}

to{

text-shadow:

0 0 20px rgba(212,175,55,.9),

0 0 40px rgba(212,175,55,.7),

0 0 60px rgba(212,175,55,.5);

}

}

.typing{

font-size:1.2rem;

margin-top:20px;

color:#444;

overflow:hidden;

white-space:nowrap;

border-right:3px solid #d4af37;

width:0;

margin-inline:auto;

animation:

typing 6s steps(50,end) infinite,

blink .7s infinite;

}

@keyframes typing{

0%{width:0}

50%{width:100%}

80%{width:100%}

100%{width:0}

}

@keyframes blink{

50%{border-color:transparent;}

}

.btn{

display:inline-block;

margin-top:35px;

padding:15px 35px;

background:#d4af37;

color:white;

text-decoration:none;

border-radius:50px;

font-weight:bold;

overflow:hidden;

position:relative;

transition:.4s;

}

.btn::before{

content:'';

position:absolute;

top:0;

left:-100%;

width:100%;

height:100%;

background:linear-gradient(

90deg,

transparent,

rgba(255,255,255,.7),

transparent

);

transition:.8s;

}

.btn:hover::before{

left:100%;

}

.btn:hover{

transform:translateY(-5px) scale(1.05);

}

section{

padding:90px 10%;

}

.title{

text-align:center;

font-size:3rem;

color:#d4af37;

margin-bottom:50px;

}

.grid{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(280px,1fr));

gap:25px;

}

.card{

background:rgba(255,255,255,.8);

backdrop-filter:blur(10px);

padding:30px;

border-radius:20px;

border:1px solid rgba(212,175,55,.2);

box-shadow:0 10px 25px rgba(0,0,0,.08);

animation:cardFloat 6s ease-in-out infinite;

transition:.4s;

}

.card:hover{

transform:translateY(-10px) scale(1.03);

box-shadow:0 15px 40px rgba(212,175,55,.3);

}

.card:nth-child(2){animation-delay:1s;}

.card:nth-child(3){animation-delay:2s;}

.card:nth-child(4){animation-delay:3s;}

@keyframes cardFloat{

0%,100%{transform:translateY(0);}

50%{transform:translateY(-8px);}

}

.card h3{

color:#d4af37;

margin-bottom:15px;

}

.stats{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(200px,1fr));

gap:25px;

}

.stat{

background:white;

padding:30px;

border-radius:20px;

text-align:center;

box-shadow:0 10px 20px rgba(0,0,0,.08);

animation:pulse 3s infinite;

}

@keyframes pulse{

0%,100%{

transform:scale(1);

}

50%{

transform:scale(1.05);

}

}

.stat h2{

font-size:3rem;

color:#d4af37;

}

footer{

padding:40px;

text-align:center;

background:#f5f5f5;

color:#666;

}

/* Golden Particles */

.particles::before{

content:"";

position:fixed;

inset:0;

pointer-events:none;

background:

radial-gradient(circle at 20% 30%, rgba(212,175,55,.3) 2px, transparent 3px),

radial-gradient(circle at 80% 20%, rgba(212,175,55,.3) 2px, transparent 3px),

radial-gradient(circle at 40% 80%, rgba(212,175,55,.3) 2px, transparent 3px),

radial-gradient(circle at 60% 60%, rgba(212,175,55,.3) 2px, transparent 3px);

animation:sparkle 10s linear infinite;

}

@keyframes sparkle{

0%{transform:translateY(0);}

100%{transform:translateY(-120px);}

}

@media(max-width:768px){

.hero h1{

font-size:3rem;

}

.typing{

font-size:.9rem;

}

}

</style>

</head>

<body>

<div class="particles"></div>

<div class="chess c1">♔</div>

<div class="chess c2">♕</div>

<div class="chess c3">♖</div>

<div class="chess c4">♘</div>

<div class="chess c5">♗</div>

<div class="chess c6">♙</div>

<header>

<div class="hero">

<h1>SUKUNA CHESS ACADEMY</h1>

<p class="typing">Master Strategy • Learn Tactics • Dominate The Board</p>

<a href="#tutorials" class="btn">Start Learning</a>

</div>

</header>

<section>

<h2 class="title">Chess Tutorials</h2>

<div class="grid">

<div class="card">

<h3>♟ Control The Center</h3>

<p>Occupy central squares to maximize your pieces and gain space.</p>

</div>

<div class="card">

<h3>♞ Develop Pieces</h3>

<p>Bring knights and bishops out quickly before attacking.</p>

</div>

<div class="card">

<h3>♔ King Safety</h3>

<p>Castle early and keep your king protected throughout the game.</p>

</div>

<div class="card">

<h3>♕ Tactical Forks</h3>

<p>Attack multiple targets at once to win material efficiently.</p>

</div>

<div class="card">

<h3>♖ Pins & Skewers</h3>

<p>Master powerful tactical motifs used by strong players.</p>

</div>

<div class="card">

<h3>♛ Checkmate Patterns</h3>

<p>Learn ladder mates, back-rank mates and smothered mates.</p>

</div>

</div>

</section>

<section>

<h2 class="title">Chess Statistics</h2>

<div class="stats">

<div class="stat"><h2>64</h2><p>Squares</p></div>

<div class="stat"><h2>32</h2><p>Pieces</p></div>

<div class="stat"><h2>16</h2><p>Pieces Per Side</p></div>

<div class="stat"><h2>1</h2><p>King To Protect</p></div>

</div>

</section>

<footer>

© 2026 Sukuna Chess Academy • Strategy • Tactics • Victory

</footer>

</body>

</html>
