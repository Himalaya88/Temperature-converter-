# Temperature-converter-
This is the first task of my internship, the name of its project is Temperature Converter 
Temperature converter 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f4f4f4;
        }

        .container {
            background-color: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        select {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
            appearance: none;
        }

        button {
            background-color: #007bff;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #0062cc;
        }

        #result {
            margin-top: 20px;
            font-size: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <input type="number" id="degrees" placeholder="Enter degrees">
        <select id="type">
            <option value="fahrenheit">Fahrenheit</option>
            <option value="celsius">Celsius</option>
        </select>
        <button onclick="convertTemperature()">Convert</button>
        <div id="result"></div>
    </div>

    <script>
        function convertTemperature() {
            const degrees = parseFloat(document.getElementById("degrees").value);
            const type = document.getElementById("type").value;
            let result;

            if (type === "fahrenheit") {
                result = (degrees - 32) * (5 / 9);
                document.getElementById("result").textContent = result.toFixed(2) + " °C";
            } else {
                result = (degrees * (9 / 5)) + 32;
                document.getElementById("result").textContent = result.toFixed(2) + " °F";
            }
        }
    </script>
</body>
</html>
