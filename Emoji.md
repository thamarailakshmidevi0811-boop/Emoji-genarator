<html>
<head>
    <title>Emoji Generator</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">
        <h1>Emoji Generator</h1>

        <div id="emoji"></div>

        <button onclick="generateEmoji()">Generate Emoji</button>

        <p id="message">Click the button to get a new emoji!</p>
    </div>

    <script src="script.js"></script>

</body>
</html>
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background: #ffeef5;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: white;
    width: 350px;
    padding: 30px;
    text-align: center;
    border-radius: 20px;
    box-shadow: 0 5px 15px #ccc;
}

h1 {
    color: #ff69b4;
}

#emoji {
    font-size: 80px;
    margin: 25px;
}

button {
    background: #ff69b4;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 10px;
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background: #ff1493;
}

#message {
    color: #555;
    margin-top: 20px;
}
const emojis = [
  "😍",
  "😊",
  "🙄",
  "❤️",
  "👍",
];

function generateEmoji() {

    let randomNumber =
        Math.floor(Math.random() * emojis.length);

    document.getElementById("emoji").innerHTML =
        emojis[randomNumber];

    document.getElementById("message").innerHTML =
        "Your random emoji is ready! ";
}
