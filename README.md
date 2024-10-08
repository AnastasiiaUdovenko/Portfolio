<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Prata&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="icon" type="image/png" href="./images/favicon.png">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Prata', serif;
            scroll-behavior: smooth;
        }
/* Common navbar styles for both desktop and mobile */
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
    width: 80px;
    height: auto;
}

/* Desktop-specific styles */
.navbar .nav-buttons {
    display: flex;
}

.navbar .nav-buttons button {
    margin: 0 5px;
    padding: 8px 16px;
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

/* Mobile-specific dropdown menu */
.navbar .nav-dropdown {
    position: relative;
    display: none; /* Hidden on desktop */
}

.navbar .dropdown-button {
    background-color: #ffffff;
    border: none;
    color: #000000;
    padding: 10px 15px;
    font-size: 1.2em;
    cursor: pointer;
    border-radius: 5px;
    transition: background-color 0.3s, color 0.3s;
}

.navbar .dropdown-button:hover {
    background-color: #cccccc;
    color: #000000;
}

.navbar .dropdown-content {
    display: none;
    position: absolute;
    right: 0;
    top: 100%;
    background-color: #ffffff;
    border-radius: 5px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
    z-index: 1001;
}

.navbar .dropdown-content button {
    display: block;
    width: 100%;
    padding: 10px;
    border: none;
    background: none;
    font-size: 1em;
    cursor: pointer;
    text-align: left;
    color: #000000;
}

.navbar .dropdown-content button:hover {
    background-color: #f0f0f0;
}

.navbar .dropdown-button:focus + .dropdown-content,
.navbar .dropdown-content:hover {
    display: block;
}

/* Mobile fullscreen dropdown menu */
.dropdown-menu {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw; /* Full viewport width */
  height: 100vh; /* Full viewport height */
  background-color: white; /* Background color */
  overflow-y: auto; /* Scroll if content overflows */
  z-index: 1000; /* Ensure it appears above other elements */
}

/* Media queries to control visibility based on screen size */

/* For desktop (screens wider than 768px) */
@media (min-width: 769px) {
    .nav-dropdown {
        display: none; /* Hide mobile dropdown on desktop */
    }

    .nav-buttons {
        display: flex; /* Show desktop buttons */
    }
}

/* For mobile (screens smaller than 768px) */
@media (max-width: 768px) {
    .nav-buttons {
        display: none; /* Hide desktop buttons on mobile */
    }

    .nav-dropdown {
        display: block; /* Show mobile dropdown on mobile */
    }
}
        body {
            margin-top: 80px;
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
            padding-top: 100px;
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
        h1 {
            font-family: 'Prata', serif;
            font-size: 54px;
            padding: 20px;
            margin: 0;
        }
        h2 {
            font-family: 'Prata', serif;
        }
        .videos {
            padding-top: 100px;
        }
        .video-list {
            align-items: end;
            grid-auto-rows: 1fr;
            list-style: none;
            padding: 0;
            margin: 20px auto;
            max-width: 1000px;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-gap: 20px;
        }
        .video-item {
            margin-bottom: 20px;
        }
        iframe {
            width: 100%;
            height: 315px;
        }
        .pictures {
            padding-top: 100px;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 10px;
            justify-content: center;
            padding: 20px;
        }
        .gallery img {
            max-width: 100%;
            max-height: 100%;
            margin: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .gallery img:hover {
            transform: scale(1.1);
        }
        .modal {
            display: none;
            justify-content: center;
            position: fixed;
            z-index: 2000;
            padding-top: 0px;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
        }
        .modal-content {
            margin: auto;
            display: block;
            max-width: 90%;
            max-height: 90%;
        }
        .close {
            color: #fff;
            position: absolute;
            top: 10px;
            right: 25px;
            font-size: 30px;
            font-weight: bold;
            cursor: pointer;
            z-index: 2001;
        }
        .pointer-left,
        .pointer-right {
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            cursor: pointer;
            z-index: 2001;
            color: white;
            font-size: 30px;
            user-select: none;
            transition: background-color 0.3s;
        }
        .pointer-left {
            left: 10px;
        }
        .pointer-right {
            right: 10px;
        }
        .pointer-left:hover,
        .pointer-right:hover {
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 50%;
        }
        .education {
            padding-top: 100px;
        }
        .education, 
        .experience {
            margin-top: 40px;
            margin-bottom: 40px;
        }
        .education .container,
        .experience .container {
            width: 80%;
            max-width: 1200px;
            margin: auto;
            padding: 0 40px;
        }
        .experience-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }
        .experience-item:hover {
            transform: translateY(-5px);
        }
        .experience-item img {
            width: 120px;
            height: auto;
            border-radius: 5px;
            margin-right: 20px;
        }
        .education p {
            font-family: 'Prata', serif;
        }
        .contact-box {
            position: relative;
            z-index: 2;
            border: 2px solid #333;
            border-radius: 10px;
            padding: 20px;
            width: 300px;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.9);
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
            margin: 0 auto;
        }
        .contact-box h3 {
            margin-top: 0;
            color: #333;
        }
        .contact-box p {
            color: #555;
        }
        .contact-box a {
            color: #4CAF50;
            text-decoration: none;
        }
        .contact-box a:hover {
            text-decoration: underline;
        }
        .contactme {
            background-image: url('./images/logoend.JPEG');
            background-size: cover;
            background-position: center;
            color: #000000;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 100px 20px;
            height: 100vh;
            position: relative;
        }
        .contactme::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1;
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
            <button onclick="document.getElementById('videos').scrollIntoView({behavior: 'smooth'})">Videos</button>
            <button onclick="document.getElementById('pictures').scrollIntoView({behavior: 'smooth'})">Pictures</button>
            <button onclick="document.getElementById('education').scrollIntoView({behavior: 'smooth'})">Education and Experience</button>
            <button onclick="document.getElementById('contactme').scrollIntoView({behavior: 'smooth'})">Contact Me</button>
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
    <div id="videos" class="videos">
        <h1 style="text-align: center;">Videos</h1>
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
                <h2>Aerial moon ~ Celebrity Cruises 2021-23</h2>
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
        <div id="pictures" class="pictures">
        <h1 style="text-align: center;">Pictures</h1>
        <div class="gallery">
  <img src="./images/hoop1.JPEG" alt="Image 1" onclick="openModal('./images/hoop1.JPEG')">
  <img src="./images/me.jpg" alt="Image 2" onclick="openModal('./images/me.jpg')">
  <img src="./images/nastiaHomepage.JPG" alt="Image 3" onclick="openModal('./images/nastiaHomepage.JPG')">
  <!-- Add more images here -->
</div>

<div id="myModal" class="modal">
  <span class="close" onclick="closeModal()">&times;</span>
  <div class="pointer-left" onclick="previousImage()">
      <i class="fas fa-chevron-left"></i>
  </div>
  <img class="modal-content" id="modalImg">
  <div class="pointer-right" onclick="nextImage()">
      <i class="fas fa-chevron-right"></i>
  </div>
</div>

<script>
  var images = ["./images/hoop1.JPEG", "./images/me.jpg", "./images/nastiaHomepage.JPG"]; // List of image sources
  var currentIndex = 0;

  function openModal(imageSrc) {
    var modal = document.getElementById('myModal');
    var modalImg = document.getElementById('modalImg');
    modal.style.display = "flex";
    modalImg.src = imageSrc;
    currentIndex = images.indexOf(imageSrc);
  }

  function closeModal() {
    var modal = document.getElementById('myModal');
    modal.style.display = "none";
  }

  function nextImage() {
    currentIndex = (currentIndex + 1) % images.length;
    document.getElementById('modalImg').src = images[currentIndex];
  }

  function previousImage() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
    document.getElementById('modalImg').src = images[currentIndex];
  }
</script>
        <div id="education" class="education">
        <h1 style="text-align: center;">Education and Experience</h1>
        <div class="container">
        
            <h2>Education</h2>
            <p>
                Anastasiia in 2021 completed the full course of the Kyiv Municipal Academy of Circus and Performing Arts. And received the diploma with honors in the field of Study Culture and Arts, Programme Subject Area Performing arts.
            </p>
        </div>

        <!-- Experience Section -->
        <div id="experience" class="experience">
            <div class="container">
                <h2>Experience</h2>
            <!-- Experience Item 1 -->
            <div class="experience-item">
                <img src="./images/hoop8.JPG" alt="Example Image">
                <div class="info">
                    <p><strong>Date:</strong> Nov 2023 - Jan 2024 </p>
                    <p><strong>Company:</strong> Cirque Musica </p> 
                    <p><strong>Description:</strong> The tour across the United States gave Anastasiia the chance to experience all the joys of bus touring, and it was pleasant for her to provide people with a Christmas mood. </p>
                </div>
            </div>
            <!-- Experience Item 2 -->
            <div class="experience-item">
                <img src="./images/show16.jpeg" alt="Example Image">
                <div class="info">
                    <p><strong>Date:</strong> Jan 2024 - Mar 2024/Jan 2022 - Jul 2023 </p>
                    <p><strong>Company:</strong> Celebrity Cruises Inc. </p>
                    <p><strong>Description:</strong> Anastasiia had the privilege of doing several contracts with Celebrity Cruises, and was apart of
                    their inaugural cast on the launch of their new ship Celebrity Beyond. She took part in
                    the creation of their shows which gave her the opportunity to work along side well
                    known producers such as Dondraico Johnson, Michelle Lynskey, Holly Palmer and
                    Michael Fatice. She was given great exposure in this process to enhance the shows with
                    multiple images, and work with multiple disciplines being hula-hoop, contortion, and
                    aerial acts. </p>
                </div>
            </div>
            <!-- Experience Item 3 -->
            <div class="experience-item">
                <img src="./images/hoop6.jpg" alt="Example Image">
                <div class="info">
                    <p><strong>Date:</strong> Dec 2021 - Jan 2022 </p>
                    <p><strong>Company:</strong> Theatre "Rizoma" </p>
                    <p><strong>Description:</strong> Anastasiia was working in Christmas show called "Alice in Wonderland “ under the production
                    of very famous artist Anatoliy Zalevskiy who known as a double gold medalist of
                    “Monte-Carlo circus festival” and “Cirque de Demain”. </p>
                </div>
            </div>
            <!-- Experience Item 4 -->
            <div class="experience-item">
                <img src="./images/neon.jpg" alt="Example Image">
                <div class="info">
                    <p><strong>Date:</strong> Jul 2021 - Oct 2021/Apr 2019 - Oct 2019 </p>
                    <p><strong>Company:</strong> Ezgi Event </p>
                    <p><strong>Description:</strong> [....]</p>
                </div>
            </div>
            <!-- Experience Item 5 -->
            <div class="experience-item">
                <img src="./images/kobzov.JPG" alt="Example Image">
                <div class="info">
                    <p><strong>Date:</strong> Mar 2017 - Sep 2018 </p>
                    <p><strong>Company:</strong> Circus "Kobzov" </p> 
                    <p><strong>Description:</strong> Anastasiia has done multiple contracts with the biggest travel circus in Ukraine as a Dance Capitan doing neon and fire performance. </p>
                </div>
            </div>
        </div>
    </div>
<div id="contactme" class="contactme">
    <div class="contact-box">
    <h3>Contact me</h3>
    <p>Email: nastia.ydovenko@gmail.com</p>
    <p>Instagram: <a style="color: black; text-decoration: underline;" href="https://www.instagram.com/anastasia__udovenko?igsh=NTF1MGMwcm51c2w2" target="_blank">anastasia__udovenko<a></p>
</div>
</div>
    <!-- Add more sections for other content if needed -->
</body>
</html>
