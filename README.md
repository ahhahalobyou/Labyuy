<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Superman Jump Game</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Superman Jump Game</h1>
    <div id="game-container">
        <img src="superman.png" id="superman">
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    text-align: center;
    font-family: Arial, sans-serif;
}

#game-container {
    width: 300px;
    height: 400px;
    border: 2px solid black;
    position: relative;
    margin: auto;
    overflow: hidden;
}

#superman {
    width: 50px;
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    transition: bottom 0.3s;
}
let superman = document.getElementById("superman");

document.addEventListener("click", function() {
    superman.style.bottom = "200px"; // Tumalon si Superman
    setTimeout(() => {
        superman.style.bottom = "0"; // Babalik sa lupa
    }, 300);
});
