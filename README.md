# Yono-Slots
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Mini Slot Game</title>
<style>
body{
    font-family: Arial;
    text-align:center;
    background:#222;
    color:white;
}
.slot{
    font-size:60px;
    background:white;
    color:black;
    width:80px;
    height:80px;
    display:inline-flex;
    justify-content:center;
    align-items:center;
    margin:10px;
    border-radius:10px;
}
button{
    padding:10px 20px;
    font-size:20px;
}
</style>
</head>
<body>

<h1>🎰 Mini Slot Game</h1>

<div class="slot" id="s1">🍒</div>
<div class="slot" id="s2">🍋</div>
<div class="slot" id="s3">🍇</div>

<br><br>

<button onclick="spin()">SPIN</button>

<h2 id="result"></h2>

<script>
function spin() {
    let items = ["🍒","🍋","🍇","🍉","⭐","7️⃣"];

    let a = items[Math.floor(Math.random()*items.length)];
    let b = items[Math.floor(Math.random()*items.length)];
    let c = items[Math.floor(Math.random()*items.length)];

    document.getElementById("s1").innerHTML = a;
    document.getElementById("s2").innerHTML = b;
    document.getElementById("s3").innerHTML = c;

    if(a === b && b === c){
        document.getElementById("result").innerHTML = "🎉 You Win!";
    } else {
        document.getElementById("result").innerHTML = "😔 Try Again";
    }
}
</script>

</body>
</html>
