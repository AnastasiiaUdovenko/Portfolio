<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Prata&display=swap" rel="stylesheet">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Prata', serif;
            scroll-behavior: smooth;
        }
        .container {
            width: 100%;
        }
        .navbar {
            width: 100%;
            background-color: #000000;
            color: #ffffff;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        .navbar .logo {
            font-size: 1.5em;
        }
        .navbar .nav-buttons {
            display: flex;
        }
        .navbar .nav-buttons button {
            margin: 0 10px;
            padding: 10px 20px;
            font-size: 1em;
            cursor: pointer;
            font-family: 'Prata', serif;
            color: #000000;
            background-color: #ffffff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s, color 0.3s;
        }
        .navbar .nav-buttons button:hover {
            background-color: #cccccc;
            color: #000000;
        }
        .section {
            padding: 100px 20px 20px 20px; /* Add padding to compensate for fixed navbar */
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .left {
            background-color: #f0f0f0;
            text-align: center;
        }
        .left img {
            max-width: 80%;
            height: auto;
        }
        .left .caption {
            margin-top: 20px;
            font-size: 2em;
        }
        .right {
            background-color: #000000;
            color: #ffffff;
        }
        .right .content {
            color: #ffffff;
        }
        .right .buttons {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .right .buttons button {
            margin: 20px;
            padding: 20px 40px;
            font-size: 2em;
            cursor: pointer;
            font-family: 'Prata', serif;
            color: #000000;
            background-color: #ffffff;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s, color 0.3s;
        }
        .right .buttons button:hover {
            background-color: #cccccc;
            color: #000000;
        }
        .about {
            background-color: #ffffff;
            color: #000000;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 100px; /* Add padding to compensate for fixed navbar */
        }
        .about .container {
            display: flex;
            flex-direction: row;
            width: 80%;
        }
        .about .left {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            margin-right: 20px;
        }
        .about .image {
            overflow: hidden;
            margin-bottom: 30px;
            height: 70vh;
        }
        .about img {
            width: auto;
            height: 100%;
            margin-top: 30px;
        }
        .about .right {
            flex: 2;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .about .text {
            width: 100%;
            text-align: center;
            margin-left: 20px;
        }
        .about .text-content {
            padding: 0 20px;
            font-size: 1.1em;
            margin-top: 60px;
        }
        .about .text-content p {
            line-height: 1.6;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <div class="logo">My Logo</div>
        <div class="nav-buttons">
            <button onclick="document.getElementById('portfolio').scrollIntoView({behavior: 'smooth'})">Portfolio</button>
            <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">About Me</button>
            <button onclick="document.getElementById('section3').scrollIntoView({behavior: 'smooth'})">Section 3</button>
            <button onclick="document.getElementById('section4').scrollIntoView({behavior: 'smooth'})">Section 4</button>
            <button onclick="document.getElementById('section5').scrollIntoView({behavior: 'smooth'})">Section 5</button>
        </div>
    </div>
    <div class="container">
        <div id="portfolio" class="section">
            <div class="left">
                <img src="your-image.jpg" alt="Your Picture">
                <div class="caption">Anastasiia Udovenko</div>
            </div>
            <div class="right">
                <div class="buttons">
                    <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">About Me</button>
                    <button onclick="document.getElementById('section3').scrollIntoView({behavior: 'smooth'})">Section 3</button>
                    <button onclick="document.getElementById('section4').scrollIntoView({behavior: 'smooth'})">Section 4</button>
                    <button onclick="document.getElementById('section5').scrollIntoView({behavior: 'smooth'})">Section 5</button>
                </div>
            </div>
        </div>
        <div id="about" class="section about">
            <h1>About Me</h1>
            <div class="container">
                <div class="left">
                    <div class="image">
                        <img src="./images/headshot.JPG" alt="Headshot">
                    </div>
                </div>
                <div class="right">
                    <div class="text">
                        <div class="text-content">
                            <p>Hello! My name is Anastasiia Udovenko, and I was born on October 23, 2002, in the charming town of Novomoskovsk, Ukraine. My journey into the world of performance arts began early. At the age of six, I started school, where I quickly discovered a passion for choreography and drawing, attending additional classes to hone my skills.</p>
                            <p>A year later, my fascination with the circus led me to join the children's circus studio "Melange-art" in Novomoskovsk. This experience was transformative, and in 2016, as part of a talented group of neon jugglers, I had the thrilling opportunity to become a finalist on "Ukraine’s Got Talent. Kids."</p>
                            <p>From 2017 to 2018, I expanded my horizons by working as a juggler and ballet dancer with the renowned Ukrainian circus "Kobzov." This period was incredibly enriching and solidified my love for the circus arts.</p>
                            <p>In 2018, I took a significant step in my professional development by enrolling in the Kiev Municipal Academy of Circus and Performing Arts. I successfully graduated as a Junior Specialist and, in 2021, embarked on a Bachelor's degree. My studies have been comprehensive, covering juggling, contortion with hoops, acting, pantomime, and both classical and modern choreography.</p>
                            <p>This is just the beginning of my adventure in the performing arts, and I am excited to see where this journey takes me next!</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="section3" class="section right">
            <div class="content">
                <h1>Section 3</h1>
                <p>Content for section 3.</p>
            </div>
        </div>
        <div id="section4" class="section right">
            <div class="content">
                <h1>Section 4</h1>
                <p>Content for section 4.</p>
            </div>
        </div>
        <div id="section5" class="section right">
            <div class="content">
                <h1>Section 5</h1>
                <p>Content for section 5.</p>
            </div>
        </div>
    </div>
</body>
</html>
