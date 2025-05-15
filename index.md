---
layout: base
title: Student Home 
description: Home Page
image: /images/mario_animation.png
hide: true
---

<!-- 
<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 10px;
        padding: 20px;
    }
    
    .box {
        background-color: #f0f0f0;
        border: 1px solid #ccc;
        padding: 10px;
        text-align: center;
        position: relative;
        text-decoration: none;
        color: black;
        transition: background-color 0.3s;
    }

    .box:hover {
        background-color: #e0e0e0;
    }

    .dropdown-text {
        display: none;
        position: absolute;
        top: 100%;
        left: 50%;
        transform: translateX(-50%);
        background-color: white;
        border: 1px solid #ccc;
        padding: 5px;
        z-index: 1;
        white-space: nowrap;
    }

    .box:hover .dropdown-text {
        display: block;
    }
</style>

<div class="grid-container">
    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-1" class="box">
        Variables
        <div class="dropdown-text">
            > Store data values
            <br>
            > Holding information
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-2" class="box">
        Data Abstraction
        <div class="dropdown-text">
            > Simplify data
            <br>
            > Make programs easier to understand
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-3" class="box">
        Mathematical Expressions
        <div class="dropdown-text">
            > Operations involving numbers
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-4" class="box">
        Strings
        <div class="dropdown-text">
            > Text with quotes
            <br>
            > Can be used to output words
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-5" class="box">
        Boolean Expressions
        <div class="dropdown-text">
            > True or False
            <br>
            > Decision making
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-6" class="box">
        Conditionals
        <div class="dropdown-text">
            > If or else statements
            <br>
            > Takes user input
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-7" class="box">
        Nested Conditionals
        <div class="dropdown-text">
            > Conditionals in conditionals
            <br>
            > Adds complexity
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-8" class="box">
        Iteration
        <div class="dropdown-text">
            > Repeat code multiple times
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-9" class="box">
        List Operations
        <div class="dropdown-text">
            > Modifying list elements
        </div>
    </a>

    <a href="https://rbojja23.github.io/rohan_2025/2024/09/05/Sprint2A-PopCornHAcks_IPYNB_2_.html#section3-10" class="box">
        Mongols Game!
        <div class="dropdown-text">
            > Using all the concepts
        </div>
    </a>
</div>



<section id="section3-1">
    <h2>Variables</h2>
    <p>Content for Variables section...</p>
</section>

<section id="section3-2">
    <h2>Data Abstraction</h2>
    <p>Content for Data Abstraction section...</p>
</section>

<section id="section3-3">
    <h2>Mathematical Expressions</h2>
    <p>Content for Mathematical Expressions section...</p>
</section>

<section id="section3-4">
    <h2>Strings</h2>
    <p>Content for Strings section...</p>
</section>

<section id="section3-5">
    <h2>Boolean Expressions</h2>
    <p>Content for Boolean Expressions section...</p>
</section>

<section id="section3-6">
    <h2>Conditionals</h2>
    <p>Content for Conditionals section...</p>
</section>

<section id="section3-7">
    <h2>Nested Conditionals</h2>
    <p>Content for Nested Conditionals section...</p>
</section>

<section id="section3-8">
    <h2>Iteration</h2>
    <p>Content for Iteration section...</p>
</section>

<section id="section3-9">
    <h2>List Operations</h2>
    <p>Content for List Operations section...</p>
</section>

<section id="section3-10">
    <h2>Mongols Game!</h2>
    <p>Content for the Mongols Game section...</p>
</section>






<!-- Liquid:  statements -->

<!-- Include submenu from _includes to top of pages -->
{% include nav/home.html %}
<!--- Concatenation of site URL to frontmatter image  --->
{% assign sprite_file = site.baseurl | append: page.image %}
<!--- Has is a list variable containing mario metadata for sprite --->
{% assign hash = site.data.mario_metadata %}  
<!--- Size width/height of Sprit images --->
{% assign pixels = 256 %}

<!--- HTML for page contains <p> tag named "Mario" and class properties for a "sprite"  -->



<title>Cookie Clicker!</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 30px;
    background-color: white;
  }
  .dark-mode {
    background-color: black;
    color: white;
  }
  .fade-rotate {
    animation: fadeInRotate 2s ease-in-out;
  }
  @keyframes fadeInRotate {
    from {
      opacity: 0;
      transform: rotate(-15deg);
    }
    to {
      opacity: 1;
      transform: rotate(0deg);
    }
  }
</style>

<h1 class="fade-rotate">Cookie Clicker!</h1>
<img id="cookie" onclick="cookiePress()" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f1/2ChocolateChipCookies.jpg/250px-2ChocolateChipCookies.jpg">
<h3 id="counter">Counter:</h3>
<h3 id="rate">Cookie Rate:</h3>
<h3 id="grandma-list">Grandma Army: </h3>
<div>
  <button onclick="grandmaPress()" id="grandma-btn">Grandma Power</button>
</div>
<button id="toggle-dark-mode">Toggle Dark Mode</button>

<script>
  // Data storage using a list to track purchases
  let purchaseHistory = [];

  // Initialize localStorage if not set
  if (localStorage.getItem("counter_value") === null) {
    localStorage.setItem("counter_value", 0);
    localStorage.setItem("cookie_rate", 1);
  }

  function cookiePress() {
    let counter_storage = Number(localStorage.getItem("counter_value"));
    let cookie_rate = Number(localStorage.getItem("cookie_rate"));

    localStorage.setItem("counter_value", counter_storage + cookie_rate);
    document.getElementById("counter").innerHTML = `Counter: ${counter_storage + cookie_rate}`;

    let audio = new Audio('https://www.myinstants.com/media/sounds/minecraft_click.mp3');
    audio.play();
  }

  // Student-developed procedure with parameter, sequencing, selection, iteration
  function purchaseUpgrade(upgradeName, rateIncrease, cost) {
    let currentCookies = Number(localStorage.getItem("counter_value"));
    let currentRate = Number(localStorage.getItem("cookie_rate"));

    if (currentCookies >= cost) {
      localStorage.setItem("cookie_rate", currentRate + rateIncrease);
      localStorage.setItem("counter_value", currentCookies - cost);

      // Track upgrade in the list
      purchaseHistory.push(upgradeName);

      // Update visuals
      document.getElementById("rate").innerHTML = `Cookie Rate: ${currentRate + rateIncrease}`;
      document.getElementById("counter").innerHTML = `Counter: ${currentCookies - cost}`;

      // Update grandma army display
      updateGrandmaArmy();
    }
  }

  // Procedure call (used by button)
  function grandmaPress() {
    purchaseUpgrade("Grandma", 5, 10);
  }

  // Iteration and string generation based on list content
  function updateGrandmaArmy() {
    let numGrandmas = purchaseHistory.filter(x => x === "Grandma").length;
    let armyString = "👵".repeat(numGrandmas);
    document.getElementById("grandma-list").innerHTML = `Grandma Army: ${armyString}`;
  }

  // Page load logic (output and state restoration)
  window.onload = function() {
    let counter_storage = localStorage.getItem("counter_value");
    let cookie_rate = localStorage.getItem("cookie_rate");

    document.getElementById("counter").innerHTML = `Counter: ${counter_storage}`;
    document.getElementById("rate").innerHTML = `Cookie Rate: ${cookie_rate}`;

    updateGrandmaArmy();
  };

  // Dark mode toggle
  document.getElementById('toggle-dark-mode').addEventListener('click', () => {
    document.body.classList.toggle('dark-mode');
  });
</script>




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
