```html
<!DOCTYPE html>
<html>
<head>
<title>Game Klik Koin</title>
<style>
body{
font-family:Arial;
text-align:center;
background:#222;
color:white;
}

#coin{
font-size:80px;
cursor:pointer;
margin-top:50px;
}

button{
padding:10px 20px;
font-size:16px;
margin-top:20px;
}
</style>
</head>

<body>

<h1>Game Klik Koin</h1>
<p>Poin kamu: <span id="score">0</span></p>

<div id="coin">🪙</div>

<button onclick="resetGame()">Reset</button>

<script>
let score = 0;

document.getElementById("coin").onclick = function(){
score++;
document.getElementById("score").innerText = score;
}

function resetGame(){
score = 0;
document.getElementById("score").innerText = score;
}
</script>

</body>
</html>
```
<!DOCTYPE html>
<html>
<head>
    <title>Game Klik Uang</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            background: #222;
            color: white;
            padding-top: 50px;
        }
        button {
            padding: 20px 40px;
            font-size: 20px;
            background: #FFD700;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.1s;
        }
        button:active {
            transform: scale(0.95);
        }
        #score {
            font-size: 40px;
            font-weight: bold;
            color: #00FF00;
        }
        p {
            font-size: 18px;
        }
    </style>
</head>

<body>

    <h1>Game Klik Dapat Uang</h1>
    <p>Poin Kamu: <span id="score">0</span></p>

    <button onclick="klik()">Klik Dapat Poin!</button>

    <script>
        let score = 0;
        const target = 10; // Target poin untuk menang

        function klik(){
            score = score + 1;
            document.getElementById("score").innerText = score;
            
            // Logika sederhana: Memberi peringatan jika mencapai target
            if (score === target) {
                alert("Selamat! Kamu berhasil mendapatkan 10 poin!");
                score = 0; // Reset score
                document.getElementById("score").innerText = score;
            }
        }
    </script>

</body>
</html>
