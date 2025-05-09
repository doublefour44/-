<!DOCTYPE html>
<html>
<head>
  <title>BBQ Village</title>
  <style>
    body { font-family: sans-serif; text-align: center; }
    .button { margin: 10px; padding: 10px 20px; font-size: 16px; }
  </style>
</head>
<body>
  <h1>BBQ Village</h1>
  <p>Мясо: <span id="meat">0</span> | Овощи: <span id="veggies">0</span> | Шашлык: <span id="bbq">0</span></p>

  <button class="button" onclick="gatherMeat()">Собрать мясо</button>
  <button class="button" onclick="gatherVeggies()">Собрать овощи</button>
  <button class="button" onclick="makeBBQ()">Жарить шашлык</button>

  <script>
    let meat = 0, veggies = 0, bbq = 0;

    function gatherMeat() {
      meat++;
      updateDisplay();
    }

    function gatherVeggies() {
      veggies++;
      updateDisplay();
    }

    function makeBBQ() {
      if (meat >= 1 && veggies >= 1) {
        meat--; veggies--;
        bbq++;
        updateDisplay();
      } else {
        alert("Нужно мясо и овощи!");
      }
    }

    function updateDisplay() {
      document.getElementById("meat").textContent = meat;
      document.getElementById("veggies").textContent = veggies;
      document.getElementById("bbq").textContent = bbq;
    }
  </script>
</body>
</html>
