---
layout: page
title: Rohan Bojja Student Webpage
permalink: /about/
---

<link href="https://fonts.googleapis.com/css2?family=Caveat:wght@600&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Raleway:wght@700&display=swap" rel="stylesheet">
<style>
    /* Page Styling */
    body {
        background: linear-gradient(135deg, #0f2027, #2c5364, #88d3ce);
        color: white;
        font-family: 'Caveat', 'Courier New', monospace;
        text-align: center;
        margin: 0;
    }

    h1 {
        margin-top: 50px;
        font-family: 'Raleway', sans-serif;
        font-size: 4em;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    }

    .description-box {
        margin: 30px auto;
        padding: 10px;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 15px;
        width: 70%;
        max-width: 500px;
        font-size: 1.8em;
        font-family: 'Raleway', sans-serif;
    }

    .icon-container {
        display: flex;
        justify-content: space-evenly;
        margin-top: 30px;
        gap: 10px;
    }

    .icon-item {
        width: 150px;
        transition: transform 0.3s ease;
    }

    .icon-item:hover {
        transform: scale(1.1);
    }

    .flag-container {
        display: flex;
        justify-content: space-around;
        margin-top: 20px;
    }

    .flag-item {
        width: 150px;
        transition: transform 0.3s ease;
    }

    .flag-item:hover {
        transform: scale(1.1);
    }

    img {
        width: 100%;
        height: auto;
        border-radius: 10px;
    }
</style>

<h1>Rohan Bojja Student Webpage</h1>

<!-- Introduction -->
<div class="description-box">
    Hi! I am Rohan Bojja. Enjoy my website!
</div>

<!-- Icon Section (Basketball, Badminton, Science, Coding) -->
<div class="icon-container">
    <div class="icon-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Basketball.png" alt="Basketball" title="Basketball">
    </div>
    <div class="icon-item">
        <img src="https://png.pngtree.com/png-clipart/20201216/original/pngtree-badminton-ball-pie-combination-cartoon-clipart-png-image_5701340.jpg" alt="Badminton Image">
    </div>
    <div class="icon-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Base_pair_GC.svg/282px-Base_pair_GC.svg.png" alt="Science" title="Science">
    </div>
    <div class="icon-item">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/C_Hello_World_Program.png/290px-C_Hello_World_Program.png" alt="Coding" title="Coding">
    </div>
</div>

<!-- Flag Section -->
<div class="flag-container" id="flagContainer">
    <!-- JavaScript will insert flag images here -->
</div>

<script>
    // Connect to the HTML div container
    var container = document.getElementById("flagContainer");

    // Define an array of flag data
    var living_in_the_world = [
        {"flag": "https://upload.wikimedia.org/wikipedia/en/thumb/4/41/Flag_of_India.svg/255px-Flag_of_India.svg.png", "greeting": "Namaste", "description": "Indian Flag"},
        {"flag": "https://upload.wikimedia.org/wikipedia/en/thumb/a/a4/Flag_of_the_United_States.svg/255px-Flag_of_the_United_States.svg.png", "greeting": "Hello", "description": "American Flag"}
    ];

    // Dynamically insert the flags into the container
    living_in_the_world.forEach(function(item) {
        var flagItem = document.createElement("div");
        flagItem.classList.add("flag-item");
        flagItem.innerHTML = `<img src="${item.flag}" alt="${item.description}" title="${item.greeting}">`;
        container.appendChild(flagItem);
    });
</script>


