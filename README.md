<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Zufällige Zitate</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #89f7fe, #66a6ff);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      color: #222;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 450px;
      animation: fadeIn 0.8s ease-in-out;
    }
    h1 {
      font-size: 26px;
      margin-bottom: 20px;
      color: #333;
    }
    p {
      font-size: 20px;
      margin: 20px 0;
      color: #444;
      min-height: 60px;
    }
    button {
      background: #007BFF;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 18px;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    button:hover {
      background: #0056b3;
      transform: scale(1.05);
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(-20px);}
      to {opacity: 1; transform: translateY(0);}
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Zufälliges Zitat</h1>
    <p id="quote">Klicke auf den Button, um ein Zitat zu sehen!</p>
    <button onclick="newQuote()">Neues Zitat</button>
  </div>

  <script>
    const quotes = [
      "Der beste Weg, die Zukunft vorherzusagen, ist, sie zu erschaffen. – Peter Drucker",
      "Auch der weiteste Weg beginnt mit einem ersten Schritt. – Konfuzius",
      "Phantasie ist wichtiger als Wissen, denn Wissen ist begrenzt. – Albert Einstein",
      "Mut steht am Anfang des Handelns, Glück am Ende. – Demokrit",
      "Man entdeckt keine neuen Erdteile, ohne den Mut zu haben, alte Küsten aus den Augen zu verlieren. – André Gide",
      "Das Leben ist zu kurz, um sich über Kleinigkeiten zu ärgern.",
      "Sei du selbst die Veränderung, die du dir wünschst für diese Welt. – Mahatma Gandhi",
      "Erfolg ist die Summe kleiner Bemühungen, die jeden Tag wiederholt werden."
    ];

    function newQuote() {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      document.getElementById('quote').textContent = quotes[randomIndex];
    }
  </script>
</body>
</html>
