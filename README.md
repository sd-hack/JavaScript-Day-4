# JavaScript-Day-4
<!DOCTYPE html>
<html>
<head>
  <title>Tony’s Café Receipt</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      padding: 30px;
    }
    .bill {
      background: white;
      padding: 20px;
      width: 300px;
      border-radius: 8px;
    }
    h2 {
      text-align: center;
    }
  </style>
</head>

<body>

  <div class="bill">
    <h2>🧾 Tony’s Café</h2>
    <p id="receipt"></p>
  </div>

  <script>
    // 1. Order details (fill your data)
    let customerName = "Sanket";
    let itemName = "LATTE coffee";
    let price = 120;
    let quantity = 2;

    // 2. Format item name using string methods
    let formattedItem =
      itemName.charAt(0).toUpperCase() + itemName.slice(1).toLowerCase();

    // 3. Calculate total
    let total = price * quantity;

    // BONUS: 10% service charge
    let serviceCharge = total * 0.10;
    let finalAmount = total + serviceCharge;

    // Show receipt on page
    document.getElementById("receipt").innerHTML =
      "Customer: " + customerName + "<br>" +
      "Item: " + formattedItem + "<br>" +
      "Price: ₹" + price + "<br>" +
      "Quantity: " + quantity + "<br><br>" +
      "Total: ₹" + total + "<br>" +
      "Service Charge (10%): ₹" + serviceCharge.toFixed(2) + "<br>" +
      "<b>Final Amount: ₹" + finalAmount.toFixed(2) + "</b>";
  </script>

</body>
</html>
