# EXO-HUB-KEY-SYSTEM
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EXO HUB | Key System</title>
    <style>
        body {
            background-color: #0a0a0a;
            color: white;
            font-family: 'Segoe UI', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background: #151515;
            padding: 40px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid #333;
            box-shadow: 0 0 20px rgba(138, 43, 226, 0.2);
        }
        h1 { color: #8a2be2; letter-spacing: 2px; }
        .key-box {
            background: #000;
            padding: 15px;
            margin: 20px 0;
            border-radius: 8px;
            font-size: 24px;
            font-weight: bold;
            border: 1px dashed #8a2be2;
        }
        button {
            background: #8a2be2;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover { background: #a052ee; }
    </style>
</head>
<body>
    <div class="container">
        <h1>EXO HUB</h1>
        <p>SYSTEM ACTIVE</p>
        <div class="key-box" id="keyDisplay">EXO-XXXXX</div>
        <button onclick="generateKey()">GENERATE NEW KEY</button>
    </div>

    <script>
        function generateKey() {
            // Sample logic para sa random key
            const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
            let result = "EXO-";
            for (let i = 0; i < 8; i++) {
                result += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            document.getElementById('keyDisplay').innerText = result;
            // Dito mo ikokonekta ang backend para i-save ang key sa database
        }
    </script>
</body>
</html>
