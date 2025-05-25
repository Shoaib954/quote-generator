# quote-generator
first project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Quote Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f3f3f3;
      padding: 2rem;
    }
    #quote-box {
      background: #fff;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      margin-bottom: 1rem;
      min-height: 80px;
      font-size: 1.25rem;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    button {
      background: #007bff;
      color: #fff;
      border: none;
      padding: 0.7rem 1.2rem;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
    }
    button:hover {
      background: #0056b3;
    }
  </style>
</head>
<body>

  <h1>Random Quote Generator</h1>
  <div id="quote-box">Click the button to generate a quote!</div>
  <button id="generate-btn">Generate Quote</button>

  <script>
    const quotes = [
      "The best way to predict the future is to create it.",
      "Life is 10% what happens to us and 90% how we react to it.",
      "The only limit to our realization of tomorrow is our doubts of today.",
      "Do what you can, with what you have, where you are.",
      "Success usually comes to those who are too busy to be looking for it.",
      "Don't watch the clock; do what it does. Keep going.",
      "Keep your face always toward the sunshine—and shadows will fall behind you.",
      "You are never too old to set another goal or to dream a new dream."
    ];

    const quoteBox = document.getElementById('quote-box');
    const btn = document.getElementById('generate-btn');

    btn.addEventListener('click', () => {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      quoteBox.textContent = quotes[randomIndex];
    });
  </script>

</body>
</html>
