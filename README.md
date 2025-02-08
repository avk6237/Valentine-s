# Valentine-s

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #ffebf0;
            color: #d63384;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        }
        .hidden {
            display: none;
        }
        button {
            background-color: #ff4081;
            color: white;
            border: none;
            padding: 10px 15px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 15px;
        }
        button:hover {
            background-color: #d63384;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Hey, Gorgeous ❤️</h1>
        <p>I've got something super important to ask you...</p>
        <button onclick="nextStep(1)">Click to Continue</button>

        <div id="step1" class="hidden">
            <h2>Did you know?</h2>
            <p>Every day with you is like Valentine's Day...</p>
            <button onclick="nextStep(2)">Awww, tell me more!</button>
        </div>

        <div id="step2" class="hidden">
            <h2>But something is missing...</h2>
            <p>It’s February 14th soon, and I need to ask you something VERY important.</p>
            <button onclick="nextStep(3)">OMG, what is it?!</button>
        </div>

        <div id="step3" class="hidden">
            <h2>Drumroll, please... 🥁</h2>
            <p>Okay, here we go...</p>
            <button onclick="nextStep(4)">I'm ready!</button>
        </div>

        <div id="step4" class="hidden">
            <h2>Will You Be My Valentine? 💖</h2>
            <button onclick="answer('yes')">Yes! 💘</button>
            <button onclick="answer('no')" style="background-color: #ccc;">No? 😭</button>
        </div>

        <div id="yes-answer" class="hidden">
            <h2>Yay! 🎉</h2>
            <p>Best decision ever! I can't wait to spend Valentine's Day with you! ❤️</p>
            <p>Now, let’s plan something amazing together!</p>
            <button onclick="window.location.href='https://www.google.com/search?q=best+valentine%27s+date+ideas'">Plan Our Date!</button>
        </div>

        <div id="no-answer" class="hidden">
            <h2>Ouch... 💔</h2>
            <p>Wait... Are you sure? 😢</p>
            <button onclick="nextStep(4)">Let me think again...</button>
        </div>
    </div>

    <script>
        function nextStep(step) {
            document.querySelectorAll('.container div').forEach(div => div.classList.add('hidden'));
            document.getElementById('step' + step).classList.remove('hidden');
        }

        function answer(choice) {
            document.querySelectorAll('.container div').forEach(div => div.classList.add('hidden'));
            if (choice === 'yes') {
                document.getElementById('yes-answer').classList.remove('hidden');
            } else {
                document.getElementById('no-answer').classList.remove('hidden');
            }
        }
    </script>

</body>
</html>
