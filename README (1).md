<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mensaje Especial</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    h1 {
      font-size: 2rem;
      margin: 20px;
      color: #ff69b4;
    }
    .message {
      font-size: 1.5rem;
      font-weight: bold;
      margin: 20px;
    }
    .buttons {
      margin-top: 20px;
    }
    .button {
      font-size: 1rem;
      padding: 10px 20px;
      margin: 10px;
      color: white;
      background-color: #4CAF50;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
    }
    .button.no {
      background-color: #f44336;
    }
    img {
      max-width: 300px;
      height: auto;
    }
  </style>
</head>
<body>
  <h1>Un Mensaje para Ti MI FUTURA ESPOSITA 💓</h1>
  
  <img id="gif" src="https://i.imgur.com/JHTocYe.gif" alt="Oso pidiendo perdón">

  <div class="message" id="message">¿ME PERDONAS MI AMORCITA HERMOSA??</div>
  
  <div class="buttons" id="buttons">
    <a href="#" id="yesButton" class="button">Sí</a>
    <a href="#" id="noButton" class="button no">No</a>
  </div>

  <script>
    const messageElement = document.getElementById('message');
    const gifElement = document.getElementById('gif');
    const buttonsElement = document.getElementById('buttons');

    const states = {
      initial: {
        gif: "https://i.imgur.com/JHTocYe.gif",
        message: "¿ME PERDONAS MI AMORCITA HERMOSA??",
      },
      yes: {
        gif: "https://i.imgur.com/a5aJQvU.gif",
        message: "Gracias mi amorcito, te amo y te amaré siempre 💖",
      },
      no: {
        gif: "https://i.imgur.com/wXq6hIn.gif",
        message: "¿Segura?",
      },
    };

    document.getElementById('yesButton').addEventListener('click', (event) => {
      event.preventDefault();
      updateState("yes");
    });

    document.getElementById('noButton').addEventListener('click', (event) => {
      event.preventDefault();
      updateState("no");
    });

    function updateState(state) {
      gifElement.src = states[state].gif;
      messageElement.textContent = states[state].message;

      if (state === "yes") {
        buttonsElement.style.display = "none"; // Oculta los botones
      } else {
        buttonsElement.style.display = "block"; // Muestra los botones
      }
    }
  </script>
</body>
</html>
