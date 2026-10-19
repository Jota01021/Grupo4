
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presióname, bebé 💋</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ffe0eb, #fff4bd, #f7d5ff);
      overflow: hidden;
    }

    .contenedor {
      text-align: center;
      padding: 25px;
    }

    h1 {
      color: #d63384;
      font-size: clamp(28px, 8vw, 42px);
      margin-bottom: 35px;
      text-shadow: 2px 2px 0 white;
    }

    .boton {
      width: min(80vw, 330px);
      min-height: 190px;
      border: 5px solid #ff5c9a;
      border-radius: 35px;
      background: linear-gradient(145deg, #ff8fbd, #ffcae0);
      color: #8b1249;
      font-size: clamp(25px, 7vw, 34px);
      font-weight: 900;
      box-shadow: 0 12px 0 #d94c83, 0 18px 30px #d94c8344;
      cursor: pointer;
      transition: transform 0.12s, box-shadow 0.12s;
    }

    .boton:active {
      transform: translateY(9px) scale(0.97);
      box-shadow: 0 3px 0 #d94c83;
    }

    .corazon {
      font-size: 48px;
      margin-bottom: 15px;
    }

    p {
      color: #8b3560;
      font-size: 16px;
      margin-top: 30px;
    }

    .flotante {
      position: fixed;
      font-size: 25px;
      opacity: 0.7;
      pointer-events: none;
    }

    .uno { top: 10%; left: 9%; }
    .dos { top: 20%; right: 10%; }
    .tres { bottom: 15%; left: 12%; }
    .cuatro { bottom: 10%; right: 12%; }
  </style>
</head>

<body>
  <span class="flotante uno">💗</span>
  <span class="flotante dos">✨</span>
  <span class="flotante tres">💕</span>
  <span class="flotante cuatro">💋</span>

  <main class="contenedor">
    <div class="corazon">💖</div>
    <h1>Oye, tú... 🥺</h1>

    <button class="boton" id="boton">
      Presióname,<br>bebé 💋
    </button>

    <p>✨ Toca aquí, no tengas miedo ✨</p>

    <audio id="sonido" preload="auto">
      <source src="pollo-ara.mp3" type="audio/mpeg">
    </audio>
  </main>

  <script>
    const boton = document.getElementById("boton");
    const sonido = document.getElementById("sonido");

    boton.addEventListener("click", () => {
      sonido.currentTime = 0;

      sonido.play().catch(() => {
        alert("No se pudo reproducir el audio. Revisa que pollo-ara.mp3 esté en el repositorio.");
      });
    });
  </script>
</body>
</html>
