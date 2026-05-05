<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Só pra te lembrar ❤️</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    background:linear-gradient(to bottom,#fff8f2,#ffeef2);
    font-family:'Patrick Hand', cursive;
    overflow-x:hidden;
    color:#222;
}

/* LOADING */

.loader{
    position:fixed;
    inset:0;
    background:#fff7f7;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    z-index:99999;
    transition:1s;
}

.loader h1{
    font-size:3rem;
    color:#ff4d6d;
    animation:pulse 1.5s infinite;
}

.loader p{
    margin-top:15px;
    font-size:1.3rem;
}

@keyframes pulse{
    0%,100%{
        transform:scale(1);
    }
    50%{
        transform:scale(1.1);
    }
}

/* CURSOR */

.cursor-heart{
    position:fixed;
    pointer-events:none;
    font-size:20px;
    animation:heartFade 1s linear forwards;
    z-index:99999;
}

@keyframes heartFade{
    to{
        transform:translateY(-40px) scale(0);
        opacity:0;
    }
}

/* FUNDO */

.hearts{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
    overflow:hidden;
}

.heart{
    position:absolute;
    color:#ff4d6d;
    animation:up linear infinite;
    opacity:.4;
}

@keyframes up{
    from{
        transform:translateY(100vh);
    }
    to{
        transform:translateY(-120vh);
    }
}

/* ESTRELAS */

.stars{
    position:fixed;
    inset:0;
    z-index:0;
    pointer-events:none;
}

.star{
    position:absolute;
    width:3px;
    height:3px;
    background:white;
    border-radius:50%;
    animation:blink 2s infinite;
}

@keyframes blink{
    0%,100%{
        opacity:.2;
    }
    50%{
        opacity:1;
    }
}

/* TOPO */

.hero{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    position:relative;
    z-index:2;
    padding:20px;
}

.hero h1{
    font-size:5rem;
    color:#ff4d6d;
    animation:float 4s ease-in-out infinite;
}

.hero p{
    margin-top:20px;
    font-size:2rem;
    max-width:700px;
}

.scroll{
    position:absolute;
    bottom:30px;
    font-size:1.3rem;
    animation:float 2s infinite;
}

/* HISTÓRIA */

.story{
    width:100%;
    max-width:1000px;
    margin:auto;
    position:relative;
    z-index:2;
}

/* PAINÉIS */

.panel{
    margin-bottom:40px;
    opacity:0;
    transform:translateY(80px);
    transition:1s;
    position:relative;
}

.panel.show{
    opacity:1;
    transform:translateY(0);
}

/* IMAGENS */

.panel img{
    width:100%;
    display:block;
    border-radius:25px;
    box-shadow:0 15px 40px rgba(0,0,0,.15);
    transition:.5s;
}

.panel img:hover{
    transform:scale(1.02);
}

/* GLOW */

.panel::before{
    content:"";
    position:absolute;
    inset:-10px;
    background:linear-gradient(45deg,#ff4d6d,#ffb6c1,#ff4d6d);
    z-index:-1;
    filter:blur(25px);
    opacity:.25;
    border-radius:30px;
}

/* FINAL */

.final{
    text-align:center;
    padding:100px 20px;
    position:relative;
    z-index:2;
}

.final h1{
    font-size:4rem;
    color:#ff4d6d;
    margin-bottom:25px;
    animation:heartbeat 1.5s infinite;
}

.final p{
    font-size:2rem;
    line-height:1.8;
}

@keyframes heartbeat{
    0%,100%{
        transform:scale(1);
    }
    25%{
        transform:scale(1.05);
    }
    50%{
        transform:scale(1);
    }
    75%{
        transform:scale(1.08);
    }
}

@keyframes float{
    0%,100%{
        transform:translateY(0);
    }
    50%{
        transform:translateY(-10px);
    }
}

/* BOTÕES */

.controls{
    position:fixed;
    bottom:20px;
    right:20px;
    display:flex;
    flex-direction:column;
    gap:15px;
    z-index:999;
}

.btn{
    width:65px;
    height:65px;
    border:none;
    border-radius:50%;
    background:#ff4d6d;
    color:white;
    font-size:25px;
    cursor:pointer;
    box-shadow:0 10px 25px rgba(0,0,0,.2);
    transition:.3s;
}

.btn:hover{
    transform:scale(1.1) rotate(10deg);
}

/* CONTADOR */

.counter{
    margin-top:40px;
    font-size:2rem;
    color:#ff4d6d;
}

/* RESPONSIVO */

@media(max-width:768px){

    .hero h1{
        font-size:2.8rem;
    }

    .hero p{
        font-size:1.3rem;
    }

    .final h1{
        font-size:2.5rem;
    }

    .final p{
        font-size:1.2rem;
    }

    .btn{
        width:55px;
        height:55px;
        font-size:20px;
    }
}

</style>
</head>

<body>

<!-- LOADING -->
<div class="loader" id="loader">
    <h1>❤️ Carregando amor... ❤️</h1>
    <p>Preparando uma surpresa especial ✨</p>
</div>

<!-- ESTRELAS -->
<div class="stars"></div>

<!-- CORAÇÕES -->
<div class="hearts"></div>

<!-- TOPO -->
<section class="hero">

    <h1>Só pra te lembrar ❤️</h1>

    <p>
        Que independente do tempo,
        dos problemas ou da correria...
        você continua sendo uma das melhores partes da minha vida.
    </p>

    <div class="counter" id="counter"></div>

    <div class="scroll">
        ↓ role para continuar ↓
    </div>

</section>

<!-- HISTÓRIA -->
<div class="story">

    <div class="panel">
        <img src="1.png">
    </div>

    <div class="panel">
        <img src="2.png">
    </div>

    <div class="panel">
        <img src="3.png">
    </div>

    <div class="panel">
        <img src="4.png">
    </div>

</div>

<!-- FINAL -->
<section class="final">

    <h1>❤️ Eu te amo ❤️</h1>

    <p>
        Obrigado por existir.<br>
        Obrigado por cada abraço,<br>
        cada risada,<br>
        cada momento nosso. ✨
    </p>

</section>

<!-- BOTÕES -->
<div class="controls">

    <button class="btn" onclick="toggleMusic()">
        🎵
    </button>

    <button class="btn" onclick="window.scrollTo({top:0,behavior:'smooth'})">
        ⬆
    </button>

</div>

<!-- MÚSICA -->
<audio id="music" loop>
    <source src="musica.mp3" type="audio/mp3">
</audio>

<script>

/* LOADING */

window.onload = ()=>{

    setTimeout(()=>{

        document.getElementById('loader').style.opacity = '0';

        setTimeout(()=>{

            document.getElementById('loader').style.display='none';

        },1000);

    },2500);
};

/* CORAÇÕES */

const hearts = document.querySelector('.hearts');

for(let i=0;i<60;i++){

    const heart = document.createElement('div');

    heart.classList.add('heart');

    heart.innerHTML = '❤';

    heart.style.left = Math.random()*100+'vw';

    heart.style.fontSize =
    (Math.random()*25+10)+'px';

    heart.style.animationDuration =
    (Math.random()*8+5)+'s';

    hearts.appendChild(heart);
}

/* ESTRELAS */

const stars = document.querySelector('.stars');

for(let i=0;i<120;i++){

    const star = document.createElement('div');

    star.classList.add('star');

    star.style.left = Math.random()*100+'vw';

    star.style.top = Math.random()*100+'vh';

    star.style.animationDelay =
    Math.random()*3+'s';

    stars.appendChild(star);
}

/* APARECER */

const panels = document.querySelectorAll('.panel');

function reveal(){

    panels.forEach(panel=>{

        const top = panel.getBoundingClientRect().top;

        if(top < window.innerHeight - 100){

            panel.classList.add('show');
        }
    });
}

window.addEventListener('scroll',reveal);

reveal();

/* MÚSICA */

const music = document.getElementById('music');

function toggleMusic(){

    if(music.paused){

        music.play();

    }else{

        music.pause();
    }
}

/* CURSOR COM CORAÇÃO */

document.addEventListener('mousemove',(e)=>{

    const heart = document.createElement('div');

    heart.classList.add('cursor-heart');

    heart.innerHTML = '❤';

    heart.style.left = e.clientX+'px';

    heart.style.top = e.clientY+'px';

    document.body.appendChild(heart);

    setTimeout(()=>{

        heart.remove();

    },1000);
});

/* CONTADOR */

const startDate = new Date("2024-01-01");

function updateCounter(){

    const now = new Date();

    const diff = now - startDate;

    const days = Math.floor(diff / (1000*60*60*24));

    document.getElementById('counter').innerHTML =
    `✨ ${days} dias guardando memórias juntos ✨`;
}

updateCounter();

</script>

</body>
</html>
