# Aman-Mathew
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Digital Clock</title>
  <style>
    body {
      background-color: black;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      font-family: 'Courier New', Courier, monospace;
      margin: 0;
    }
    .clock {
      font-size: 5rem;
      padding: 2rem;
      border: 4px solid rgb(221, 223, 221);
      border-radius: 10px;
      
    }
  </style>
</head>
<body>
  <div class="clock" id="clock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      let hours = now.getHours().toString().padStart(2, '0');
      let minutes = now.getMinutes().toString().padStart(2, '0');
      let seconds = now.getSeconds().toString().padStart(2, '0');
      document.getElementById('clock').textContent = ${hours}:${minutes}:${seconds};
    }

    setInterval(updateClock, 1000);
    updateClock(); // initial call to display immediately
  </script>
</body>
</html>
