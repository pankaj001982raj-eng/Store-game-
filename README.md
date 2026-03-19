# Store-game-
Hi
<!DOCTYPE html>
<html>
<head>
  <title>Store Simulator</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #222;
      color: white;
    }
    button {
      padding: 10px;
      margin: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>

<h1>🛒 My Store Simulator</h1>

<h2>Money: $<span id="money">0</span></h2>
<h2>Items Sold: <span id="items">0</span></h2>

<button onclick="sellItem()">Sell Item ($10)</button>
<button onclick="upgrade()">Upgrade Store ($100)</button>

<script>
let money = 0;
let items = 0;
let multiplier = 1;

function sellItem() {
  money += 10 * multiplier;
  items++;
  update();
}

function upgrade() {
  if (money >= 100) {
    money -= 100;
    multiplier++;
    alert("Store Upgraded! Profit Increased 🚀");
  } else {
    alert("Not enough money!");
  }
  update();
}

function update() {
  document.getElementById("money").innerText = money;
  document.getElementById("items").innerText = items;
}
</script>

</body>
</html>
