<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AgroTec Sustentável</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:#f4f7f2;
    color:#333;
}

header{
    background:#2e7d32;
    padding:15px 5%;
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
}

nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    color:white;
    font-size:1.5rem;
    font-weight:bold;
}

nav ul{
    display:flex;
    list-style:none;
    gap:20px;
}

nav a{
    color:white;
    text-decoration:none;
    transition:.3s;
}

nav a:hover{
    color:#c8e6c9;
}

.hero{
    height:100vh;
    background:linear-gradient(rgba(0,0,0,.4), rgba(0,0,0,.4)),
    url('https://images.unsplash.com/photo-1500937386664-56d1dfef3854');
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:white;
}

.hero-content h1{
    font-size:3rem;
    margin-bottom:20px;
}

.btn{
    display:inline-block;
    margin-top:20px;
    padding:12px 25px;
    background:#4caf50;
    color:white;
    text-decoration:none;
    border-radius:8px;
}

section{
    padding:80px 10%;
}

h2{
    color:#2e7d32;
    margin-bottom:20px;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:25px;
    border-radius:12px;
    box-shadow:0 4px 10px rgba(0,0,0,.1);
}

.galeria{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
    gap:20px;
}

.galeria img{
    width:100%;
    border-radius:10px;
}

.simulador{
    background:white;
    padding:30px;
    border-radius:12px;
    max-width:500px;
}

input{
    width:100%;
    padding:12px;
    margin:10px 0;
}

button{
    background:#2e7d32;
    color:white;
    border:none;
    padding:12px 20px;
    cursor:pointer;
    border-radius:8px;
}

footer{
    background:#1b5e20;
    color:white;
    text-align:center;
    padding:20px;
}
</style>
</head>
<body>

<header>
<nav>
<div class="logo">AgroTec</div>

<ul>
<li><a href="#sobre">Sobre</a></li>
<li><a href="#comedouro">Comedouro</a></li>
<li><a href="#compostagem">Compostagem</a></li>
<li><a href="#beneficios">Benefícios</a></li>
<li><a href="#simulador">Simulador</a></li>
<li><a href="#galeria">Galeria</a></li>
</ul>
</nav>
</header>

<section class="hero">
<div class="hero-content">
<h1>Agro Forte, Futuro Sustentável</h1>
<p>Tecnologia, automação e sustentabilidade transformando o campo.</p>
<a href="#sobre" class="btn">Conheça o Projeto</a>
</div>
</section>

<section id="sobre">
<h2>Sobre o Projeto</h2>
<p>
O AgroTec Sustentável apresenta soluções inovadoras para automação rural,
reduzindo desperdícios e aumentando a produtividade.
</p>
</section>

<section id="comedouro">
<h2>🐔 Comedouro Automático</h2>
<div class="card">
<p>
O sistema monitora o nível de ração e realiza abastecimento automático,
garantindo alimentação contínua dos animais.
</p>
</div>
</section>

<section id="compostagem">
<h2>♻ Compostagem Inteligente</h2>
<div class="card">
<p>
Transforme resíduos orgânicos em adubo natural de forma sustentável.
</p>
</div>
</section>

<section id="beneficios">
<h2>Benefícios</h2>

<div class="cards">

<div class="card">
<h3>🌱 Sustentabilidade</h3>
<p>Redução do desperdício.</p>
</div>

<div class="card">
<h3>⚙ Automação</h3>
<p>Mais eficiência no manejo.</p>
</div>

<div class="card">
<h3>🐄 Bem-estar Animal</h3>
<p>Alimentação regular e segura.</p>
</div>

<div class="card">
<h3>♻ Compostagem</h3>
<p>Produção de adubo orgânico.</p>
</div>

</div>
</section>

<section id="simulador">
<h2>Simulador Rural</h2>

<div class="simulador">
<label>Quantidade de animais</label>
<input type="number" id="animais">

<button onclick="calcular()">Calcular</button>

<h3 id="resultado"></h3>
</div>
</section>

<section id="galeria">
<h2>Galeria</h2>

<div class="galeria">
<img src="https://images.unsplash.com/photo-1500595046743-cd271d694d30">
<img src="https://images.unsplash.com/photo-1464226184884-fa280b87c399">
</div>
</section>

<footer>
Projeto AgroTec Sustentável © 2026
</footer>

<script>
function calcular(){
    let animais = document.getElementById("animais").value;

    if(animais === ""){
        alert("Digite uma quantidade.");
        return;
    }

    let racao = animais * 0.5;

    document.getElementById("resultado").innerHTML =
    "Consumo estimado: " + racao + " kg de ração por dia";
}
</script>

</body>
</html>
