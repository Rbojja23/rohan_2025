---
layout: null
permalink: /retro_4/
---
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sprint 4 Retrospective Storyboard - Rohan Bojja</title>





<style>
* {
box-sizing: border-box;
font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

body {
margin: 0;
background: #0f172a;
color: #e5e7eb;
display: flex;
align-items: center;
justify-content: center;
height: 100vh;
overflow: hidden;
}

.slider-container {
width: 80vw;
height: 80vh;
position: relative;
overflow: hidden;
border-radius: 20px;
box-shadow: 0 20px 40px rgba(0,0,0,0.5);
background: #020617;
}

.slides {
display: flex;
height: 100%;
transition: transform 0.6s ease-in-out;
}

.slide {
min-width: 100%;
padding: 3rem;
display: flex;
flex-direction: column;
justify-content: center;
gap: 1.5rem;
}

.slide h1 {
font-size: 2.5rem;
color: #38bdf8;
}

.slide p {
font-size: 1.1rem;
line-height: 1.7;
max-width: 700px;
}

.image-placeholder {
width: 100%;
height: 260px;
border-radius: 16px;
background: linear-gradient(135deg, #1e293b, #020617);
display: flex;
align-items: center;
justify-content: center;
color: #94a3b8;
font-size: 1rem;
border: 1px dashed #334155;
}

.nav-btn {
position: absolute;
top: 50%;
transform: translateY(-50%);
background: rgba(15,23,42,0.9);
border: none;
color: #38bdf8;
font-size: 2rem;
padding: 0.6rem 1rem;
cursor: pointer;
border-radius: 999px;
transition: background 0.3s;
}

.nav-btn:hover {
background: rgba(56,189,248,0.2);
}

.prev {
left: 1rem;
}

.next {
right: 1rem;
}

.progress {
position: absolute;
bottom: 1rem;
left: 50%;
transform: translateX(-50%);
display: flex;
gap: 8px;
}

.dot {
width: 10px;
height: 10px;
border-radius: 50%;
background: #334155;
}

.dot.active {
background: #38bdf8;
}
</style>
</head>
<body>

<div class="slider-container">
<button class="nav-btn prev" onclick="prevSlide()">❮</button>
<button class="nav-btn next" onclick="nextSlide()">❯</button>

<div class="slides" id="slides">

<section class="slide">
<h1>Intro</h1>
<p>
This retrospective is a visual story of my journey in this class — how ideas became systems,
how failure turned into iteration, and how collaboration shaped my learning.
</p>
</section>

<section class="slide">
<h1>Ideation</h1>
<p>
I noticed that grades were not truly functional. There was no real connection between users,
grades, admin access, and frontend display. My goal became building a complete grading pipeline.
</p>
</section>

<section class="slide">
<h1>Ideation Visual</h1>
<div class="image-placeholder">Add ideation diagram / notes here</div>
</section>

<section class="slide">
<h1>Implementation</h1>
<p>
I modified the SQLite grades database to include user information, updated the Spring backend
schema, and connected everything to the frontend using GET requests to the admin table.
</p>
</section>

<section class="slide">
<h1>Implementation Visual</h1>
<div class="image-placeholder">Add database / backend screenshot here</div>
</section>

<section class="slide">
<h1>Testing & Iterations</h1>
<p>
Early iterations failed due to Spring issues and schema mismatches. Through collaboration
with Adis’s group, we debugged the problems and got the system working correctly.
</p>
</section>

<section class="slide">
<h1>Testing Visual</h1>
<div class="image-placeholder">Add debugging or error logs here</div>
</section>

<section class="slide">
<h1>Future</h1>
<p>
After validating the system, our team transitioned toward using an AWS S3 bucket.
Nikhil and I are currently working on this shift to improve scalability.
</p>
</section>

<section class="slide">
<h1>Future Visual</h1>
<div class="image-placeholder">Add AWS architecture diagram here</div>
</section>

<section class="slide">
<h1>Girls Who Code Seminar</h1>
<p>
Attending the Girls Who Code seminar expanded my understanding of the tech community
and reinforced the importance of collaboration and diverse pathways in computer science.
</p>
</section>

<section class="slide">
<h1>Seminar Visual</h1>
<div class="image-placeholder">Add seminar photo or notes here</div>
</section>

<section class="slide">
<h1>Commits & Analytics</h1>
<p>
My commit history reflects consistent effort, iteration, and problem-solving throughout
the course — turning ideas into working systems.
</p>
</section>

<section class="slide">
<h1>Commits Visual</h1>
<div class="image-placeholder">Add GitHub commits screenshot here</div>
</section>

<section class="slide">
<h1>End</h1>
<p>
This class taught me that real software development is iterative, collaborative,
and constantly evolving. This storyboard captures that journey.
</p>
</section>

</div>

<div class="progress" id="progress"></div>
</div>

<script>
let currentSlide = 0;
const slides = document.getElementById('slides');
const totalSlides = slides.children.length;
const progress = document.getElementById('progress');

for (let i = 0; i < totalSlides; i++) {
const dot = document.createElement('div');
dot.classList.add('dot');
if (i === 0) dot.classList.add('active');
progress.appendChild(dot);
}

function updateSlider() {
slides.style.transform = `translateX(-${currentSlide * 100}%)`;
[...progress.children].forEach((dot, index) => {
dot.classList.toggle('active', index === currentSlide);
});
}

function nextSlide() {
if (currentSlide < totalSlides - 1) {
currentSlide++;
updateSlider();
}
}

function prevSlide() {
if (currentSlide > 0) {
currentSlide--;
updateSlider();
}
}

document.addEventListener('keydown', (e) => {
if (e.key === 'ArrowRight') nextSlide();
if (e.key === 'ArrowLeft') prevSlide();
});
</script>
</body>
</html>
