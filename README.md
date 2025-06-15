# index.html
<!DOCTYPE html>
<html>
<head>
  <title>Track Your Package</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background: #f5f5f5; }
    .tracker-box { background: white; padding: 20px; max-width: 400px; margin: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    input, button { padding: 10px; width: 100%; margin-top: 10px; border-radius: 5px; border: 1px solid #ccc; }
    #result { margin-top: 20px; }
  </style>
</head>
<body>
  <div class="tracker-box">
    <h2>Track Your Package</h2>
    <input type="text" id="trackingNumber" placeholder="Enter your tracking number">
    <button onclick="trackPackage()">Track</button>
    <div id="result"></div>
  </div>

  <script>
    const data = {
      "C123456": "In transit. Expected delivery: June 18, 2025.",
      "C789101": "Delivered on June 14, 2025.",
      "C111213": "Out for delivery today."
    };

    function trackPackage() {
      const number = document.getElementById("trackingNumber").value.trim();
      const result = data[number] || "Tracking number not found. Please check again.";
      document.getElementById("result").innerText = result;
    }
  </script>
</body>
</html>
