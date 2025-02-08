<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;700&display=swap');
        
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffcccc;
            font-family: 'Poppins', sans-serif;
        }
        .container {
            text-align: center;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #ff4d4d;
            font-family: 'Great Vibes', cursive;
            font-size: 40px;
        }
        .heart {
            color: red;
            font-size: 50px;
            animation: heartbeat 1s infinite alternate;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            100% { transform: scale(1.2); }
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            margin: 10px;
            font-family: 'Poppins', sans-serif;
        }
        .yes {
            background-color: #ff4d4d;
            color: white;
        }
        .no {
            background-color: #ccc;
            color: black;
            position: absolute;
        }
    </style>
</head>
<body>
    <div class="container" id="main-container">
        <h1>Will you be my Valentine? ❤️</h1>
        <div class="heart">❤️</div>
        <div class="buttons">
            <button class="yes" onclick="showCelebration()">Yes</button>
            <button class="no" onmouseover="moveButton()">No</button>
        </div>
    </div>
    
    <script>
        function moveButton() {
            let button = document.querySelector('.no');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }

        function showCelebration() {
            document.body.innerHTML = `
                <div style="text-align: center; padding: 50px; background-color: #ffcccc; height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; font-family: 'Poppins', sans-serif;">
                    <h1 style="color: #ff4d4d; font-family: 'Great Vibes', cursive; font-size: 50px;">I LOVE YOU GUNNU ❤️</h1>
                    <h2 style="font-weight: 400;">I WILL ALWAYS BE WITH YOU TILL THIS UNIVERSE'S ENERGY DIES</h2>
                    <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Celebrating Cat" style="width: 200px;">
                    <img src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif" alt="Dancing Cat" style="width: 200px;">
                </div>
            `;
        }
    </script>
</body>
</html>
