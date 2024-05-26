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
        .navbar {
            height: 80px;
            background-color: #000000;
            color: #ffffff;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
        }
        .navbar .logo img {
            width: 80px; /* Adjust the width of the logo image */
            height: auto;
        }
        body {
            margin-top: 80px;
        }
        .navbar .nav-buttons {
            display: flex;
        }
        .navbar .nav-buttons button {
            margin: 0 5px;
            padding: 8px 16px; /* Decreased padding around buttons */
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
        .full-screen-image {
            background-image: url('./images/nastiaHomepage.JPG');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #ffffff;
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
        <div class="logo">
            <img src="./images/logo.jpg" alt="Your Logo">
        </div>
        <div class="nav-buttons">
            <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">About Me</button>
            <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">Videos</button>
            <button>Section 2</button>
            <button>Section 3</button>
            <button>Section 4</button>
        </div>
    </div>
    <div class="full-screen-image"></div>
    <div id="about" class="about">
        <h1>About Me</h1>
        <div class="container">
            <div class="left">
                <div class="image">
                    <img src="./images/me.jpg" alt="me">
                </div>
            </div>
            <div class="right">
                <div class="text">
                    <div class="text-content">
                        <p>Hello! My name is Anastasiia Udovenko, and I was born on October 23, 2002, in the charming town of Novomoskovsk, Ukraine. My journey into the world of performance arts began early. At the age of six, I started school, where I quickly discovered a passion for choreography and drawing, attending additional classes to hone my skills.</p>
                        <p>A year later, my fascination with the circus led me to join the children's circus studio "Melange-art" in Novomoskovsk. This experience was transformative, and in 2016, as part of a talented group of neon jugglers, I had the thrilling opportunity to become a finalist on "Ukraine’s Got Talent. Kids."</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
         <h1>Videos</h1>
    <ul class="video-list">
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/pCsbirQaViY">
                <h2>Promo</h2>
                <iframe src="https://www.youtube.com/embed/pCsbirQaViY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/Js4RHO5j7SQ">
                <h2>Hula hoop - Contortion act</h2>
                <iframe src="https://www.youtube.com/embed/Js4RHO5j7SQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/2j2YWaLqeIo">
                <h2>"Wizards in Winter" ~ Cirque Musica 2023</h2>
                <iframe src="https://www.youtube.com/embed/2j2YWaLqeIo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/D0NNIQ0eBkc">
                <h2>Aerial moon ~ Celebrity Cruises 2021-2023</h2>
                <iframe src="https://www.youtube.com/embed/D0NNIQ0eBkc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/db67Y0X9ZKk">
                <h2>Contortion ~ Celebrity Cruises 2021-2023</h2>
                <iframe src="https://www.youtube.com/embed/db67Y0X9ZKk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/iknI4urKxaY">
                <h2>Aerial Lyra experience</h2>
                <iframe src="https://www.youtube.com/embed/iknI4urKxaY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/P8M5aoNRzi0">
                <h2>Silks experience</h2>
                <iframe src="https://www.youtube.com/embed/P8M5aoNRzi0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/FvP84u08ppQ">
                <iframe src="https://www.youtube.com/embed/FvP84u08ppQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/KBQjVvvkk0Q">
                <h2>"Bad Girl" hula hoop ~ Celebrity Cruises 2021-2023</h2>
                <iframe src="https://www.youtube.com/embed/KBQjVvvkk0Q" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
        <li class="video-item">
            <a class="video-link" href="https://www.youtube.com/embed/PM0cf7knRHY">
                <h2>"Champagne Supernova" ~ Celebrity Cruises 2021-2023</h2>
                <iframe src="https://www.youtube.com/embed/PM0cf7knRHY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </li>
     </ul>   
    <!-- Add more sections for other content if needed -->
</body>
</html>
