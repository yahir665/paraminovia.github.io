<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Ti ❤️</title>
    <style>
        body {
            background-color: #ffebef;
            text-align: center;
            font-family: 'Arial', sans-serif;
            padding: 20px;
            color: #d63384;
            position: relative;
            overflow: hidden;
        }

        h1 {
            font-size: 3rem;
            margin-top: 50px;
        }

        p {
            font-size: 1.5rem;
            margin: 20px auto;
            width: 80%;
        }

        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: floatUp 3s linear infinite;
        }

        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }

        .btn {
            background-color: #d63384;
            color: blue;
            padding: 10px 20px;
            border: none;
            border-radius: 20px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn:hover {
            background-color: #b52e6e;
        }
    </style>
</head>
<body>

    <h1>💖 Para la persona más especial 💖</h1>
    <p>Si estás leyendo esto, es porque te quiero decir que te amoo un monton mi princesita ❤️😍 y siempre seras la mejor 
        abogadiosa ❤️😍 en verdad te amo un monton amor eres toda mi vida entera ❤️😍 </p>
    <button class="btn" onclick="mostrarMensaje()">Haz clic aquí</button>

    <script>
        function mostrarMensaje() {
            alert("Eres mi persona favorita ❤️");
        }

        function crearCorazon() {
            const heart = document.createElement("div");
            heart.innerHTML = "❤️";
            heart.classList.add("heart");
            document.body.appendChild(heart);

            const size = Math.random() * 20 + 10 + "px";
            heart.style.fontSize = size;

            heart.style.left = Math.random() * 100 + "vw";
            heart.style.top = "100vh";

            setTimeout(() => {
                heart.remove();
            }, 3000);
        }

        setInterval(crearCorazon, 500);
    </script>

</body>
</html>
