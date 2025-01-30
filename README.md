# vale
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi Valentín?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffe6e6;
        }
        h1 {
            color: #ff4081;
        }
        .container {
            margin-top: 50px;
        }
        .gato {
            width: 300px;
            height: auto;
            border-radius: 10px;
            margin: 10px;
        }
        .btn {
            background-color: #ff4081;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 5px;
            font-size: 20px;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #d81b60;
        }
        .hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Quieres ser mi Valentín? 💖</h1>
        <img src="https://media.tenor.com/NYWWmG6YvE4AAAAC/cute-cat.gif" class="gato" alt="Gato tierno">
        <br>
        <button class="btn" onclick="mostrarMensaje()">¡Sí, obvio! 😻</button>
    </div>
    <div class="hearts" id="hearts"></div>
    <script>
        function mostrarMensaje() {
            alert("¡Yay! Sabía que dirías que sí! 💕😻");
            soltarCorazones();
        }
        function soltarCorazones() {
            let heartsContainer = document.getElementById("hearts");
            for (let i = 0; i < 20; i++) {
                let heart = document.createElement("div");
                heart.innerHTML = "❤️";
                heart.style.position = "absolute";
                heart.style.left = Math.random() * 100 + "vw";
                heart.style.top = Math.random() * 100 + "vh";
                heart.style.fontSize = Math.random() * 30 + 10 + "px";
                heartsContainer.appendChild(heart);
                setTimeout(() => heart.remove(), 2000);
            }
        }
    </script>
</body>
</html>
