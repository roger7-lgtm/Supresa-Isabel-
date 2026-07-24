# Supresa-Isabel-
Te amo minha princesa 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Uma Surpresa ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,Helvetica,sans-serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ff5f9e,#ff9dc5,#ffd3e5);
overflow:hidden;
}

.container{
width:90%;
max-width:420px;
background:white;
padding:35px;
border-radius:25px;
text-align:center;
box-shadow:0 20px 40px rgba(0,0,0,.25);
position:relative;
z-index:2;
}

h1{
font-size:32px;
color:#ff2d75;
margin-bottom:15px;
}

p{
font-size:20px;
line-height:1.6;
color:#444;
margin-bottom:25px;
}

button{
padding:15px 35px;
font-size:18px;
border:none;
border-radius:50px;
cursor:pointer;
background:#ff2d75;
color:white;
transition:.3s;
}

button:hover{
transform:scale(1.05);
background:#ff0a5f;
}

.hidden{
display:none;
}

.heart{
position:absolute;
font-size:25px;
animation:fall linear infinite;
opacity:.8;
}

@keyframes fall{

0%{
transform:translateY(-100px);
opacity:0;
}

20%{
opacity:1;
}

100%{
transform:translateY(110vh);
opacity:0;
}

}
</style>
</head>

<body>

<div class="container">

<div id="inicio">

<h1>❤️ Uma surpresa...</h1>

<p>
Clique no botão abaixo.
Prometo que vale a pena.
</p>

<button onclick="abrir()">
Abrir ❤️
</button>

</div>

<div id="mensagem" class="hidden">

<h1>Eu tenho algo para dizer...</h1>

<p id="texto"></p>

<br>

<button onclick="whats()">
💬 Me responde no WhatsApp
</button>

</div>

</div>

<script>

const frase="Eu te amo mais do que qualquer palavra consegue explicar. Obrigado por fazer parte da minha vida. Você é uma das melhores coisas que já me aconteceram. ❤️";

function abrir(){

document.getElementById("inicio").classList.add("hidden");
document.getElementById("mensagem").classList.remove("hidden");

digitar(frase);

}

function digitar(texto){

let i=0;

const destino=document.getElementById("texto");

const timer=setInterval(()=>{

destino.innerHTML+=texto.charAt(i);

i++;

if(i>=texto.length){

clearInterval(timer);

}

},40);

}

function whats(){

const numero="5511999999999";

const mensagem=encodeURIComponent("Eu também te amo ❤️🥹");

window.location.href=`https://wa.me/${numero}?text=${mensagem}`;

}

function criarCoracao(){

const h=document.createElement("div");

h.className="heart";

h.innerHTML="❤️";

h.style.left=Math.random()*100+"vw";

h.style.animationDuration=(3+Math.random()*5)+"s";

h.style.fontSize=(15+Math.random()*25)+"px";

document.body.appendChild(h);

setTimeout(()=>{

h.remove();

},8000);

}

setInterval(criarCoracao,300);

</script>

</body>
</html>
