<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Mini Games Hub</title>

<style>

body{
    font-family:Arial, sans-serif;
    text-align:center;
    background:#f0f0f0;
    margin:0;
    padding:20px;
}

h1{
    margin-bottom:30px;
}

.game{
    background:white;
    padding:20px;
    margin:20px auto;
    max-width:400px;
    border-radius:10px;
}

button{
    padding:10px 20px;
    margin:5px;
    cursor:pointer;
}

input{
    padding:10px;
}

</style>
</head>

<body>

<h1>🎮 Mini Games Hub</h1>

<div class="game">
    <h2>Number Guessing Game</h2>

    <p>Guess a number from 1 to 10</p>

    <input type="number" id="guess">

    <button onclick="guessGame()">
        Guess
    </button>

    <p id="guessResult"></p>
</div>

<div class="game">

    <h2>Rock Paper Scissors</h2>

    <button onclick="play('Rock')">Rock</button>

    <button onclick="play('Paper')">Paper</button>

    <button onclick="play('Scissors')">Scissors</button>

    <p id="rpsResult"></p>

</div>

<script>

let secret =
Math.floor(Math.random()*10)+1;

function guessGame(){

let user =
Number(document.getElementById("guess").value);

if(user === secret){

document.getElementById("guessResult")
.innerHTML = "✅ You Win!";

secret =
Math.floor(Math.random()*10)+1;

}
else{

document.getElementById("guessResult")
.innerHTML = "❌ Wrong Guess";

}

}

function play(user){

let choices =
["Rock","Paper","Scissors"];

let computer =
choices[Math.floor(Math.random()*3)];

let result = "";

if(user === computer){

result = "Draw";

}
else if(
(user==="Rock" && computer==="Scissors") ||
(user==="Paper" && computer==="Rock") ||
(user==="Scissors" && computer==="Paper")
){

result = "You Win";

}
else{

result = "Computer Wins";

}

document.getElementById("rpsResult")
.innerHTML =
"Computer chose " + computer +
"<br>" + result;

}

</script>

</body>
</html># Testxt1
It's just a test :)
