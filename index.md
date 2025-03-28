---
layout: base
title: Student Home 
description: Home Page
image: /images/mario_animation.png
hide: true
---


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


<p id="mario" class="sprite"></p>

<style>
  .fade-rotate {
    animation: fadeInRotate 2s forwards;
  }

  @keyframes fadeInRotate {
    0% { opacity: 0; transform: rotate(0deg); }
    100% { opacity: 1; transform: rotate(360deg); }
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
  
<!--- Embedded Cascading Style Sheet (CSS) rules, 
        define how HTML elements look 
--->
<style>

body.dark-mode {
  background-color: black;
  color: white;
}

a {
  color: blue;
}

body.dark-mode a {
  color: white;
}

.page-header {
  background-color: #f5f5f5;
  color: black;
}

body.dark-mode .page-header {
  background-color: black;
  color: white;
}

.btn {
  background-color: #eeeeee;
  color: black;
  border: 2px solid black;
}

body.dark-mode .btn {
  background-color: black;
  color: white;
  border: 2px solid white;
}

/* Dark mode styles for code blocks, tables, etc. */
body.dark-mode code {
  background-color: #333333;
  color: white;
}

body.dark-mode pre {
  background-color: #333333;
  color: white;
  border-color: #555555;
}

body.dark-mode blockquote {
  color: white;
  border-left-color: #555555;
}

body.dark-mode hr {
  background-color: #555555;
}

body.dark-mode table {
  border-color: #555555;
}

body.dark-mode th, body.dark-mode td {
  border-color: #555555;
}

body.dark-mode .site-footer {
  border-top-color: #555555;
}

  /*CSS style rules for the id and class of the sprite...
  */
  .sprite {
    height: {{pixels}}px;
    width: {{pixels}}px;
    background-image: url('{{sprite_file}}');
    background-repeat: no-repeat;
  }

  /*background position of sprite element
  */
  #mario {
    background-position: calc({{animations[0].col}} * {{pixels}} * -1px) calc({{animations[0].row}} * {{pixels}}* -1px);
  }
</style>

<script>
  function shopbtn(){
    rate = 1
    btn = docuemnt.getElementById("btn")
    rate += 2
  }
</script>

<!--- Embedded executable code--->
<script>
  ////////// convert YML hash to javascript key:value objects /////////

  var mario_metadata = {}; //key, value object
  {% for key in hash %}  
  
  var key = "{{key | first}}"  //key
  var values = {} //values object
  values["row"] = {{key.row}}
  values["col"] = {{key.col}}
  values["frames"] = {{key.frames}}
  mario_metadata[key] = values; //key with values added

  {% endfor %}

  ////////// game object for player /////////

  class Mario {
    constructor(meta_data) {
      this.tID = null;  //capture setInterval() task ID
      this.positionX = 0;  // current position of sprite in X direction
      this.currentSpeed = 0;
      this.marioElement = document.getElementById("mario"); //HTML element of sprite
      this.pixels = {{pixels}}; //pixel offset of images in the sprite, set by liquid constant
      this.interval = 100; //animation time interval
      this.obj = meta_data;
      this.marioElement.style.position = "absolute";
    }

    animate(obj, speed) {
      let frame = 0;
      const row = obj.row * this.pixels;
      this.currentSpeed = speed;

      this.tID = setInterval(() => {
        const col = (frame + obj.col) * this.pixels;
        this.marioElement.style.backgroundPosition = `-${col}px -${row}px`;
        this.marioElement.style.left = `${this.positionX}px`;

        this.positionX += speed;
        frame = (frame + 1) % obj.frames;

        const viewportWidth = window.innerWidth;
        if (this.positionX > viewportWidth - this.pixels) {
          document.documentElement.scrollLeft = this.positionX - viewportWidth + this.pixels;
        }
      }, this.interval);
    }

    startWalking() {
      this.stopAnimate();
      this.animate(this.obj["Walk"], 3);
    }

    startRunning() {
      this.stopAnimate();
      this.animate(this.obj["Run1"], 6);
    }

    startPuffing() {
      this.stopAnimate();
      this.animate(this.obj["Puff"], 0);
    }

    startCheering() {
      this.stopAnimate();
      this.animate(this.obj["Cheer"], 0);
    }

    startFlipping() {
      this.stopAnimate();
      this.animate(this.obj["Flip"], 0);
    }

    startResting() {
      this.stopAnimate();
      this.animate(this.obj["Rest"], 0);
    }

    stopAnimate() {
      clearInterval(this.tID);
    }
  }

  const mario = new Mario(mario_metadata);

  ////////// event control /////////

  window.addEventListener("keydown", (event) => {
    if (event.key === "ArrowRight") {
      event.preventDefault();
      if (event.repeat) {
        mario.startCheering();
      } else {
        if (mario.currentSpeed === 0) {
          mario.startWalking();
        } else if (mario.currentSpeed === 3) {
          mario.startRunning();
        }
      }
    } else if (event.key === "ArrowLeft") {
      event.preventDefault();
      if (event.repeat) {
        mario.stopAnimate();
      } else {
        mario.startPuffing();
      }
    }
  });

  //touch events that enable animations
  window.addEventListener("touchstart", (event) => {
    event.preventDefault(); // prevent default browser action
    if (event.touches[0].clientX > window.innerWidth / 2) {
      // move right
      if (currentSpeed === 0) { // if at rest, go to walking
        mario.startWalking();
      } else if (currentSpeed === 3) { // if walking, go to running
        mario.startRunning();
      }
    } else {
      // move left
      mario.startPuffing();
    }
  });

  //stop animation on window blur
  window.addEventListener("blur", () => {
    mario.stopAnimate();
  });

  //start animation on window focus
  window.addEventListener("focus", () => {
     mario.startFlipping();
  });

  //start animation on page load or page refresh
  document.addEventListener("DOMContentLoaded", () => {
    // adjust sprite size for high pixel density devices
    const scale = window.devicePixelRatio;
    const sprite = document.querySelector(".sprite");
    sprite.style.transform = `scale(${0.2 * scale})`;
    mario.startResting();
  });

</script>

<script>
  // counter_value = 0;
  if (localStorage.getItem("counter_value") === null) {
    localStorage.setItem("counter_value", 0);
    localStorage.setItem("cookie_rate", 1);
  }

  function cookiePress(){
    // counter_value = Number(counter_value) + 1
    counter_storage = localStorage.getItem("counter_value");
    cookie_rate = localStorage.getItem("cookie_rate");
    localStorage.setItem("counter_value", Number(counter_storage) + Number(cookie_rate));

    counter = document.getElementById("counter");
    counter.innerHTML = `Counter: ${Number(counter_storage) + Number(cookie_rate)}`

    var audio = new Audio('assets/crunch.mp3');
    audio.play();
  }

  function grandmaPress(){
    var grandma_increase = 100;
    var grandma_price = 10;
    counter_storage = localStorage.getItem("counter_value");
    cookie_rate = localStorage.getItem("cookie_rate");
    localStorage.setItem("cookie_rate", Number(cookie_rate) + grandma_increase);

    if (Number(counter_storage) > grandma_price) {
      rate = document.getElementById("rate");
      counter = document.getElementById("counter");

      rate.innerHTML = `Cookie Rate: ${Number(cookie_rate) + grandma_increase}`;

      localStorage.setItem("counter_value", Number(counter_storage) - grandma_price);
      counter.innerHTML = `Counter: ${Number(counter_storage) - grandma_price}`
      grandma_number = (Number(cookie_rate) + grandma_increase - 1)/5
      grandmaArmy_string = "👵".repeat(grandma_number);
      document.getElementById("grandma-list").innerHTML = `Grandma Army: ${grandmaArmy_string}`
    }
  }

  window.onload = function() {
    var counter_storage = localStorage.getItem("counter_value");
    var cookie_rate = localStorage.getItem("cookie_rate");
    document.getElementById("counter").innerHTML = `Counter: ${counter_storage}`;
    document.getElementById("rate").innerHTML = `Cookie Rate: ${cookie_rate}`;

    var grandma_increase = 5;
    grandma_number = (Number(cookie_rate) + grandma_increase - 1)/5
    grandmaArmy_string = "👵" + int(grandma_number);
    document.getElementById("grandma-list").innerHTML = `Grandma Army: ${grandmaArmy_string}`
  };
</script>


<button id="toggle-dark-mode">Toggle Dark Mode</button>

<script>
  const toggleDarkMode = () => {
    document.body.classList.toggle('dark-mode');
  };

  document.getElementById('toggle-dark-mode').addEventListener('click', toggleDarkMode);
</script>