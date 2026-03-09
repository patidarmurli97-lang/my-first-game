<!DOCTYPE html>

<html>
<head>
<title>Car Racing Game</title>
<style>
body{
margin:0;
background:#333;
overflow:hidden;
}

#game{
width:400px;
height:600px;
background:#555;
margin:auto;
position:relative;
overflow:hidden;
border:4px solid white;
}

#car{
width:50px;
height:100px;
background:red;
position:absolute;
bottom:20px;
left:175px;
border-radius:10px;
}

.obstacle{
width:50px;
height:100px;
background:yellow;
position:absolute;
top:-120px;
border-radius:10px;
}

#score{
color:white;
text-align:center;
font-size:20px;
margin-top:10px;
} </style>

</head>

<body>

<h2 id="score">Score: 0</h2>

<div id="game">
<div id="car"></div>
</div>

<script>

let car = document.getElementById("car");
let game = document.getElementById("game");
let scoreText = document.getElementById("score");

let carPosition = 175;
let score = 0;

document.addEventListener("keydown", function(e){

if(e.key === "ArrowLeft" && carPosition > 0){
carPosition -= 25;
}

if(e.key === "ArrowRight" && carPosition < 350){
carPosition += 25;
}

car.st

