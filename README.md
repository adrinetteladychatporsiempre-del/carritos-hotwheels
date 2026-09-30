# carritos-hotwheels<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Para mi hermano ❤️</title>

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            min-height: 100vh;
            background: linear-gradient(135deg, #87ceeb, #ffffff);
            font-family: 'Pacifico', cursive;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .contenedor {
            width: 90%;
            max-width: 550px;
            background: white;
            padding: 30px;
            border-radius: 30px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.25);
        }

        h1 {
            color: #1565c0;
            font-size: 38px;
            margin-bottom: 10px;
        }

        .carrito {
            font-size: 70px;
            animation: mover 2s infinite alternate;
        }

        @keyframes mover {
            from {
                transform: translateX(-15px);
            }
            to {
                transform: translateX(15px);
            }
        }

        p {
            color: #333;
            font-size: 20px;
            line-height: 1.6;
        }

        button {
            background: #1565c0;
            color: white;
            border: none;
            padding: 15px 25px;
            border-radius: 30px;
            font-size: 18px;
            font-family: inherit;
            cursor: pointer;
        }

        button:hover {
            transform: scale(1.08);
        }

        #mensaje {
            display: none;
            margin-top: 20px;
            color: #1565c0;
            font-size: 21px;
        }

        .corazon {
            position: absolute;
            font-size: 25px;
            animation: caer 5s linear infinite;
        }

        @keyframes caer {
            0% {
                transform: translateY(-100px);
                opacity: 1;
            }

            100% {
                transform: translateY(100vh);
                opacity: 0;
            }
        }
    </style>
</head>

<body>

    <div class="contenedor">

        <div class="carrito">🏎️</div>

        <h1>Para mi hermano ❤️</h1>

        <p>
            Gracias por estar siempre conmigo.
            Aunque a veces nos peleemos o nos molestemos,
            siempre vas a ser una persona muy importante para mí.
        </p>

        <button onclick="mostrarMensaje()">
            Presiona aquí 💙
        </button>

        <div id="mensaje">
            Te quiero mucho, hermano. 🥹❤️
            <br>
            Siempre voy a estar para ti.
        </div>

    </div>

    <script>
        function mostrarMensaje() {
            document.getElementById("mensaje").style.display = "block";
        }

        setInterval(function() {

            const corazon = document.createElement("div");

            corazon.className = "corazon";
            corazon.innerHTML = "❤️";

            corazon.style.left = Math.random() * 100 + "vw";

            document.body.appendChild(corazon);

            setTimeout(function() {
                corazon.remove();
            }, 5000);

        }, 500);
    </script>

</body>
</html>