<!DOCTYPE html>

<html>
<head>
<title>Simple Click Game</title>
<style>
body{
text-align:center;
font-family:Arial;
background:#f0f0f0;
}

h1{
color:#333;
}

button{
padding:15px 30px;
font-size:20px;
background:green;
color:white;
border:none;
border-radius:10px;
cursor:pointer;
}

button:hover{
background:darkgreen;
} </style>

</head>

<body>

<h1>My GitHub Game</h1>
<p>Score: <span id="score">0</span></p>

<button onclick="addScore()">Click Me</button>

<script>
let score = 0;

function addScore(){
score++;
document.getElementById("score").innerText = score;
}
</script>

</body>
</html>


