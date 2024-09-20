---
layout: page 
title: Fun
search_exclude: true
permalink: /fun/
---
<audio id="backgroundMusic" src="Travis%20Scott%20-%20HIGHEST%20IN%20THE%20ROOM%20%28Lyrics%29.mp3" loop autoplay></audio>

<html lang="en">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pong Game</title>
    <style>
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }
        canvas {
            background: #000;
            display: block;
            margin: 20px auto;
        }
    </style>

    <canvas id="pong" width="800" height="600"></canvas>

    <script>
        const canvas = document.getElementById("pong");
        const context = canvas.getContext("2d");

        // Create the paddles and ball
        const user = { x: 0, y: canvas.height / 2 - 50, width: 10, height: 100, color: "#FFF", score: 0 };
        const com = { x: canvas.width - 10, y: canvas.height / 2 - 50, width: 10, height: 100, color: "#FFF", score: 0 };
        const ball = { x: canvas.width / 2, y: canvas.height / 2, radius: 10, speed: 5, velocityX: 5, velocityY: 5, color: "#05EDFF" };

        // Draw rectangle (paddles)
        function drawRect(x, y, w, h, color) {
            context.fillStyle = color;
            context.fillRect(x, y, w, h);
        }

        // Draw circle (ball)
        function drawCircle(x, y, r, color) {
            context.fillStyle = color;
            context.beginPath();
            context.arc(x, y, r, 0, Math.PI * 2, false);
            context.closePath();
            context.fill();
        }

        // Draw text (score)
        function drawText(text, x, y, color) {
            context.fillStyle = color;
            context.font = "35px Arial";
            context.fillText(text, x, y);
        }

        // Render the game
        function render() {
            // Clear the canvas
            drawRect(0, 0, canvas.width, canvas.height, "#000");
            // Draw user and computer paddles
            drawRect(user.x, user.y, user.width, user.height, user.color);
            drawRect(com.x, com.y, com.width, com.height, com.color);
            // Draw the ball
            drawCircle(ball.x, ball.y, ball.radius, ball.color);
            // Draw scores
            drawText(user.score, canvas.width / 4, canvas.height / 5, "#FFF");
            drawText(com.score, 3 * canvas.width / 4, canvas.height / 5, "#FFF");
        }

        // Collision detection
        function collision(b, p) {
            p.top = p.y;
            p.bottom = p.y + p.height;
            p.left = p.x;
            p.right = p.x + p.width;

            b.top = b.y - b.radius;
            b.bottom = b.y + b.radius;
            b.left = b.x - b.radius;
            b.right = b.x + b.radius;

            return p.left < b.right && p.top < b.bottom && p.right > b.left && p.bottom > b.top;
        }

        // Reset the ball
        function resetBall() {
            ball.x = canvas.width / 2;
            ball.y = canvas.height / 2;
            ball.speed = 5;
            ball.velocityX = -ball.velocityX;
        }

        // Move the paddles
        function movePaddles(event) {
            let rect = canvas.getBoundingClientRect();
            user.y = event.clientY - rect.top - user.height / 2;
        }

        canvas.addEventListener("mousemove", movePaddles);

        // Update: Move the ball, check for collisions
        function update() {
            // Move the ball
            ball.x += ball.velocityX;
            ball.y += ball.velocityY;

            // Simple AI for computer paddle
            com.y += (ball.y - (com.y + com.height / 2)) * 0.1;

            // Ball collision with top and bottom walls
            if (ball.y + ball.radius > canvas.height || ball.y - ball.radius < 0) {
                ball.velocityY = -ball.velocityY;
            }

            // Check collision with paddles
            let player = (ball.x < canvas.width / 2) ? user : com;
            if (collision(ball, player)) {
                let collidePoint = (ball.y - (player.y + player.height / 2));
                collidePoint = collidePoint / (player.height / 2);

                let angleRad = (Math.PI / 4) * collidePoint;

                let direction = (ball.x < canvas.width / 2) ? 1 : -1;
                ball.velocityX = direction * ball.speed * Math.cos(angleRad);
                ball.velocityY = ball.speed * Math.sin(angleRad);

                ball.speed += 0.5;
            }

            // Update score if ball goes off screen
            if (ball.x - ball.radius < 0) {
                com.score++;
                resetBall();
            } else if (ball.x + ball.radius > canvas.width) {
                user.score++;
                resetBall();
            }
        }

        // Game loop
        function game() {
            update();
            render();
        }

        // Loop every 50 ms (20 fps)
        const framePerSecond = 50;
        setInterval(game, 1000 / framePerSecond);
    </script>
</body>
</html>
