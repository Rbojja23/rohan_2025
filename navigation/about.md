---
layout: page
title: About Us
permalink: /about/
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rohan Bojja Student Webpage</title>
    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@500&display=swap" rel="stylesheet"> <!-- Font Import -->
    <style>
        /* Styling */
        body {
            background: linear-gradient(135deg, #6e45e2, #88d3ce);
            color: white;
            font-family: 'Caveat', 'Courier New', monospace;
            text-align: center;
            margin: 0;
        }

        h1 {
            margin-top: 50px;
        }

        .flag-container {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
        }

        .flag-item {
            width: 200px;
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

        /* Description box styling */
        .description-box {
            margin: 50px auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            width: 80%;
            max-width: 600px;
            font-size: 1.5em;
        }
    </style>
</head>
<body>
    <h1>Rohan Bojja Student Webpage</h1>

    <!-- Description Box -->
    <div class="description-box">
        Hi! I am Rohan Bojja, a sophomore at Del Norte High School. I am currently a part of AP Computer Science Principles. 
        I took this class to widen my knowledge about the different aspects of coding, such as using GitHub and HTML. 
        I hope you enjoy my website!
    </div>

    <div class="flag-container" id="flagContainer">
        <!-- JavaScript will insert flag images here -->
    </div>

    <script>
        // 1. Connect to the HTML div container
        var container = document.getElementById("flagContainer");

        // 2. Define an array of flag data
        var living_in_the_world = [
            {"flag": "https://upload.wikimedia.org/wikipedia/en/thumb/4/41/Flag_of_India.svg/255px-Flag_of_India.svg.png", "greeting": "Namaste", "description": "Indian Flag"},
            {"flag": "https://upload.wikimedia.org/wikipedia/en/thumb/a/a4/Flag_of_the_United_States.svg/255px-Flag_of_the_United_States.svg.png", "greeting": "Hello", "description": "American Flag"}
        ];

        // 3. Dynamically insert the flags into the container
        living_in_the_world.forEach(function(item) {
            var flagItem = document.createElement("div");
            flagItem.classList.add("flag-item");
            flagItem.innerHTML = `<img src="${item.flag}" alt="${item.description}" title="${item.greeting}">`;
            container.appendChild(flagItem);
        });
    </script>
</body>
</html>
