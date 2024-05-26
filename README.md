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
                h1 {
            font-family: 'Prata', serif; /* Apply Prata font */
            font-size: 54px; /* 50% larger font size */
            padding: 20px;
            margin: 0;
            
        }
        h2 {
            font-family: 'Prata', serif; /* Apply Prata font */
        }
                .video-list {
            list-style: none;
            padding: 0;
            margin: 20px auto;
            max-width: 1000px; /* Increased max-width to accommodate two columns */
            display: grid; /* Use grid layout */
            grid-template-columns: repeat(2, 1fr);
            grid-gap: 20px; /* Add gap between grid items */
         }
        .video-item {
            margin-bottom: 20px;
        }
        iframe {
            width: 100%;
            height: 315px;
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
    z-index: 2001; /* Ensure the close button is above other elements */
  }
  .pointer-left,
  .pointer-right {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 20%;
    cursor: pointer;
    z-index: 1;
  }
  .pointer-left {
    left: 0;
  }
  .pointer-right {
    right: 0;
  }
          .education, .experience {
            margin-bottom: 40px;
        }
                .education .container,
                .experience .container {
            width: 80%; /* Adjust the width as needed */
            max-width: 1200px; /* Set maximum width */
            margin: auto; /* Center the container */
            padding: 0 40px; /* Add padding to create space from the edges */
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
        /* Apply Prata font to education text */
        .education p {
            font-family: 'Prata', serif;
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
            <button onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">Contact Me</button>
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
  <div class="pointer-left" onclick="previousImage()"></div>
  <img class="modal-content" id="modalImg">
  <div class="pointer-right" onclick="nextImage()"></div>
</div>

<script>
  var images = ["./images/hoop1.JPEG", "./images/me.jpg", "./images/nastiaHomepage.JPG"]; // List of image sources
  var currentIndex = 0;

  function openModal(imageSrc) {
    var modal = document.getElementById('myModal');
    var modalImg = document.getElementById('modalImg');
    modal.style.display = "block";
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
        <div id="experience" class="education">
        <h1 style="text-align: center;">Education and Experience</h1>
        <div class="container">
        
            <h2>Education</h2>
            <p>
                Anastasiia in 2021 completed the full course of the Kyiv Municipal Academy of Circus and Performing Arts. And received the diploma with honors in the field of Study Culture and Arts, Programme Subject Area Performing arts.
            </p>
        </div>

        <!-- Experience Section -->
        <div class="experience">
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
    <!-- Add more sections for other content if needed -->
</body>
</html>
