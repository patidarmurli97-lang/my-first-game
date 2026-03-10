<!DOCTYPE html>
<html>
<head>
<title>Car Racing Game</title>

<style>
body{
margin:0;
background:gray;
overflow:hidden;
}

#game{
width:300px;
height:500px;
background:black;
margin:auto;
position:relative;
overflow:hidden;
}

#car{
width:60px;
height:100px;
background-image:src="car.png" width="50" height"100" alt="car"

background-size:contain
position:absolute;
bottom:20px;
left:120px;
}

.enemy{
width:60px;
height:100px;
background-image:url("https://i.imgur.com/3ZQ3Z6P.png");
background-size:cover;
position:absolute;
top:-100px;
}
</style>

</head>

<body>

<h2 style="text-align:center;color:white;">Car Racing Game</h2>

<div id="game">
<div id="car"></div>
</div>

<script>

let car=document.getElementById("car");
let game=document.getElementById("game");
let carLeft=120;

document.addEventListener("keydown",function(e){

if(e.key==="ArrowLeft" && carLeft>0){
carLeft-=20;
}

if(e.key==="ArrowRight" && carLeft<240){
carLeft+=20;
}

car.style.left=carLeft+"px";

});

function createEnemy(){

let enemy=document.createElement("div");
enemy.classList.add("enemy");
enemy.style.left=Math.floor(Math.random()*240)+"px";
game.appendChild(enemy);

let enemyTop=-100;

let move=setInterval(function(){

enemyTop+=5;
enemy.style.top=enemyTop+"px";

if(enemyTop>500){
enemy.remove();
clearInterval(move);
}

let carRect=car.getBoundingClientRect();
let enemyRect=enemy.getBoundingClientRect();

if(
carRect.left<enemyRect.left+60 &&
carRect.left+60>enemyRect.left &&
carRect.top<enemyRect.top+100 &&
carRect.top+100>enemyRect.top
){
alert("Game Over");
location.reload();
}

},50);

}

setInterval(createEnemy,2000);

</script>

</body>
</html>kfq


