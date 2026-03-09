
<!DOCTYPE html>

<html>
<head>
<title>Click Game</title>
<style>
body{
text-align:center;
font-family:Arial;
background:#f2f2f2;
}

h1{
color:#333;
}

button{
padding:20px 40px;
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

<h1>Click Game</h1>
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
