meu-primeiro-site
│
├── index.html
├── login.html
├── perguntas.html
├── admin.html
├── style.css
└── script.js
<!DOCTYPE html>
<html>
<head>
<title>Perguntas de Jiu-Jitsu</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<h1>🥋 Fórum de Jiu-Jitsu</h1>

<p>Faça perguntas e receba respostas dos professores.</p>

<a href="login.html">
<button>Entrar</button>
</a>

<a href="perguntas.html">
<button>Ver Perguntas</button>
</a>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Login</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<h2>Login</h2>

<input type="text" id="usuario" placeholder="Usuário">

<input type="password" id="senha" placeholder="Senha">

<br><br>

<button onclick="loginAluno()">Entrar como Aluno</button>

<button onclick="loginProfessor()">Entrar como Professor</button>

<script src="script.js"></script>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
<title>Perguntas</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<h2>Faça sua pergunta</h2>

<textarea id="pergunta" placeholder="Digite sua pergunta"></textarea>

<br><br>

<button onclick="enviarPergunta()">Enviar</button>

<h3>Perguntas feitas</h3>

<ul id="listaPerguntas"></ul>

<script src="script.js"></script>

</body>
</html>
function loginAluno(){
window.location.href = "perguntas.html"
}

function loginProfessor(){
let senha = document.getElementById("senha").value

if(senha === "admin123"){
window.location.href = "admin.html"
}else{
alert("Acesso negado")
}
}

function enviarPergunta(){

let pergunta = document.getElementById("pergunta").value

let lista = document.getElementById("listaPerguntas")

let item = document.createElement("li")

item.textContent = pergunta

lista.appendChild(item)

}
body{
font-family: Arial;
text-align: center;
background: #f4f4f4;
}

textarea{
width: 300px;
height: 100px;
}

button{
padding: 10px;
margin: 5px;
}
