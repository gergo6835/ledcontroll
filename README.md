<!DOCTYPE html>
<html>
<head>
    <title>ESP32 LED Control</title>
    <script>
        function toggleLED(state) {
            fetch("https://a-te-firebase-projekted.firebaseio.com/led.json", {
                method: "PUT",
                body: JSON.stringify({ "state": state }),
                headers: { "Content-Type": "application/json" }
            });
        }
    </script>
</head>
<body>
    <h1>ESP32 LED Control</h1>
    <button onclick="toggleLED('ON')">LED ON</button>
    <button onclick="toggleLED('OFF')">LED OFF</button>
</body>
</html>
