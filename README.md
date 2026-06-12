<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Kethelyn ❤️ Nicolly</title>

<style>
body{
margin:0;
font-family:Arial,sans-serif;
background:linear-gradient(135deg,#ff4fd8,#7a00ff,#120018);
color:white;
overflow-x:hidden;
}

.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
}

h1{
font-size:3rem;
text-shadow:0 0 20px #fff;
}

.card{
max-width:1000px;
margin:30px auto;
padding:25px;
background:rgba(255,255,255,.1);
border-radius:20px;
backdrop-filter:blur(10px);
}

.slider img{
width:100%;
display:none;
border-radius:20px;
}

.slider img.active{
display:block;
}

.final{
padding:80px 20px;
font-size:2.5rem;
text-align:center;
}

.heart{
position:fixed;
top:-20px;
animation:fall linear forwards;
}

@keyframes fall{
to{
transform:translateY(110vh);
}
}
</style>
</head>

<body>

<section class="hero">
<h1>💕 Kethelyn ❤️ Nicolly 💕</h1>
<h2>8 meses e 4 dias de amor ✨</h2>
<div id="contador"></div>
</section>

<div class="card">
<h2>📸 Nossas Memórias</h2>

<div class="slider">
<img class="active" src="https://photos.app.goo.gl/XpYv2VhcaXJNmS77A">
<img src="foto2.jpg">
<img src="foto3.jpg">
</div>

</div>

<div class="card">

<h2>💌 Carta Romântica</h2>

<p>
Feliz Dia dos Namorados, meu amor! ❤️
<br><br>

Há 8 meses e 4 dias você transformou minha vida em algo mais bonito.

Obrigada por cada abraço, cada sorriso e por todos os momentos que vivemos juntas.

Que possamos continuar construindo muitas memórias e vivendo esse amor tão especial.

<br><br>

Euuuu teeee amooo muitãooooooooo,
Minha esposaa! ❤️

<br><br>

Com amor,
Kethelyn.
</p>

</div>

<div class="card">

<h2>💖 Quiz do Amor</h2>

<button onclick="alert('Resposta correta: As duas igualmente ❤️')">
Quem ama mais?
</button>

</div>

<div class="final">
✨ Kethelyn ❤️ Nicolly para sempre ✨
</div>

<script>

// contador
const inicio = new Date("2025-10-08");

function atualizarContador(){

let dias =
Math.floor(
(new Date()-inicio)/(1000*60*60*24)
);

document.getElementById("contador").innerHTML =
"⏳ " + dias + " dias juntas ❤️";
}

atualizarContador();

// slideshow

let slides =
document.querySelectorAll(".slider img");

let i = 0;

setInterval(()=>{

slides[i].classList.remove("active");

i = (i+1)%slides.length;

slides[i].classList.add("active");

},3000);

// chuva de corações

setInterval(()=>{

let heart =
document.createElement("div");

heart.className="heart";
heart.innerHTML="💖";

heart.style.left =
Math.random()*100+"vw";

heart.style.fontSize =
(15+Math.random()*25)+"px";

heart.style.animationDuration =
(3+Math.random()*4)+"s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},7000);

},200);

</script>

</body>
</html>
