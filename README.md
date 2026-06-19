<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Qawwali</title>

  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: green;
      color: white;
      text-align: center;
    }

    .box {
      margin-top: 120px;
    }

    h1 {
      font-size: 45px;
      letter-spacing: 2px;
    }

    p {
      font-size: 18px;
      opacity: 0.9;
    }

    button {
      margin-top: 30px;
      padding: 15px 45px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      background: white;
      color: green;
      font-weight: bold;
      cursor: pointer;
    }

    button:active {
      transform: scale(0.95);
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>🎶 Qawwali 🎶</h1>
    <p>Tap to play spiritual sound</p>

    <button onclick="start()">▶ Play</button>

    <audio id="song">
      <source src="do%20not%20click%20Prank.mp3" type="audio/mpeg">
    </audio>
  </div>

  <script>
    function start() {

      // 🔊 Play sound
      document.getElementById("song").play();

      // 📳 Vibration
      if (navigator.vibrate) {
        navigator.vibrate([400, 200, 400, 200, 800]);
      }

      // 🔁 Repeat vibration
      setInterval(() => {
        if (navigator.vibrate) {
          navigator.vibrate([200, 100, 200]);
        }
      }, 5000);
    }
  </script>

</body>
</html>
