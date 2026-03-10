<!DOCTYPE html>
<html lang="es">

<head>
<meta charset="UTF-8">
<title>FUENTEVIVA GAME</title>

<style>

body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;

    font-family:Arial, Helvetica, sans-serif;

    background: linear-gradient(135deg,#6495ED,#A9A9A9);
}

.titulo{
    font-size:90px;
    color:#39ff14;

    text-shadow:
        -4px -4px 0 #000,
         4px -4px 0 #000,
        -4px 4px 0 #000,
         4px 4px 0 #000;

    transform:rotate(-3deg);
    margin-bottom:40px;
}

.panel{
    background:white;
    padding:30px;
    border-radius:15px;
    box-shadow:0 10px 25px rgba(0,0,0,0.3);
}

input{
    padding:10px;
    font-size:16px;
    border-radius:8px;
    border:1px solid #ccc;
}

button{
    padding:10px 20px;
    margin-left:10px;
    font-size:16px;
    border:none;
    border-radius:8px;
    background:#6495ED;
    color:white;
    cursor:pointer;
}

button:hover{
    background:#4f7ed6;
}

#mensaje{
    margin-top:15px;
    font-size:18px;
}

</style>
</head>

<body>

<h1 class="titulo">FUENTEVIVA GAME</h1>

<div class="panel">

<input type="text" id="nombre" placeholder="Escribe tu nombre">

<button onclick="guardarNombre()">Guardar</button>

<p id="mensaje"></p>

</div>

<script>

function guardarNombre(){

let nombre=document.getElementById("nombre").value;

localStorage.setItem("jugador",nombre);

document.getElementById("mensaje").innerText="Jugador guardado: "+nombre;

}

</script>

</body>

</html>
