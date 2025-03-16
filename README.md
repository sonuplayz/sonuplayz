<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crush Name Prank</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 100%;
            max-width: 400px;
        }

        input {
            padding: 10px;
            width: 80%;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            padding: 10px 20px;
            background-color: #ff6347;
            border: none;
            border-radius: 4px;
            color: white;
            cursor: pointer;
        }

        button:hover {
            background-color: #e5533f;
        }

        .hidden {
            display: none;
            color: #ff6347;
            font-size: 1.5rem;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Enter Your Crush's Name!</h1>
        <p>Be honest and enter the name of your crush. Let's see if this works!</p>
        <input type="text" id="crushName" placeholder="Enter the name..." />
        <button onclick="revealCrush()">Submit</button>
        <p id="result" class="hidden"></p>
    </div>

    <script>
        function revealCrush() {
            let crushName = document.getElementById('crushName').value.trim();
            let result = document.getElementById('result');
            
            if (crushName) {
                result.classList.remove('hidden');
                result.textContent = `Your crush is: ${crushName}!`;
            } else {
                result.classList.add('hidden');
                alert('Please enter a name!');
            }
        }
    </script>
</body>
</html>
