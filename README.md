# QUANTO-TEMPO-FALTA
No HTML
<DOCTYPE html>
<html lang= "pt-br">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-widht, initial-scale=1.0">
   <title>Quantos dias faltam?</title>
   <link rel="stylesheet" href="style.css">
<head>
<body>
   <h1>Quantos dias faltam <span> ? </span></h1>
   <p id="dias_restantes"></p>
   <script src="main.js"></script>
</body>   
</html>

No CSS
@import
url (`https://fonts.googleapis.com/css2?family=Chakra+Petch&display=swap`);

:root{
   --cor-de-fundo:#1E1E1E;
   --branco:#FFFFFF;
   --verde:#6FFF57;
}
body{
   background-color:var(--cor de fundo);
   color:var(--branco);
   text-aling:center;
   font-family: `Chakra Petch`;
}

h1 span{
   color:var(--verde)
}

#dias_restantes{
   color:var(--verde);
   font-size:50px;
}

No main.js
const dataAtual = new Date();
let dataObjetivo = prompt("Data final ANO-MES-DIA
Exemplo: 2024-04-10");

dataObjetivo = new Date (dataObjetivo + "T23:59:59");
let diasQueFaltam = Math.floor ((dataObjetivo -
dataAtual) / 86400000);

document.querySelector("#dias_restantes").textContent = diasQueFaltam;