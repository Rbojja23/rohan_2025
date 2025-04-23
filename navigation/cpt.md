<!-- Minimalist Random Quote Generator -->
<html>
<head>
  <style>
    body {
      background-color: #121212;
      color: #fff;
      font-family: 'Courier New', monospace;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .quote-container {
      text-align: center;
      max-width: 600px;
      margin: 20px;
      padding: 20px;
      border: 1px solid #444;
      border-radius: 8px;
    }
    .quote {
      font-size: 1.5em;
      margin-bottom: 10px;
    }
    .author {
      font-size: 1em;
      color: #aaa;
    }
    button {
      background-color: white;
      color: black;
      border: none;
      padding: 10px 20px;
      font-size: 1em;
      cursor: pointer;
      margin-top: 20px;
      border-radius: 5px;
      transition: 0.3s;
    }
    button:hover {
      background-color: #333;
      color: white;
    }
  </style>
</head>

<body>
  <div class="quote-container">
    <div id="quote" class="quote">Click to generate inspiration.</div>
    <div id="author" class="author"></div>
    <button onclick="generateQuote()">Inspire Me ✨</button>
  </div>

  <script>
    // LIST of quotes with authors
    const quotes = [
      { text: "Be yourself; everyone else is already taken.", author: "Oscar Wilde" },
      { text: "The only way to do great work is to love what you do.", author: "Steve Jobs" },
      { text: "Life is what happens when you’re busy making other plans.", author: "John Lennon" },
      { text: "If you tell the truth, you don't have to remember anything.", author: "Mark Twain" },
      { text: "Do what you can, with what you have, where you are.", author: "Theodore Roosevelt" }
    ];

    // PROCEDURE: generates a random quote and updates the HTML
    function generateQuote() {
      const index = Math.floor(Math.random() * quotes.length); // SELECTION
      const selected = quotes[index];

      // Output to page
      document.getElementById("quote").innerText = `"${selected.text}"`;
      document.getElementById("author").innerText = `- ${selected.author}`;

      // Add a fade effect (ITERATION)
      let opacity = 0;
      let fade = setInterval(() => {        // ITERATION
        document.querySelector('.quote-container').style.opacity = opacity;
        opacity += 0.05;                    // SEQUENCING
        if (opacity >= 1) clearInterval(fade);
      }, 30);
    }
  </script>
</body>
</html>
