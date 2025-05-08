# Birthday---love-
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday My Love</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: radial-gradient(circle at center, #fff0f5 0%, #ffe4e1 100%);
      overflow: hidden;
    }
    .welcome-screen, .slideshow {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
      padding: 20px;
    }
    .welcome-screen {
      background: linear-gradient(to top left, #ffb6c1, #ffe4e1);
    }
    .welcome-screen h1 {
      font-size: 2.8rem;
      color: #fff;
      text-shadow: 2px 2px 4px #ff69b4;
    }
    .start-btn {
      padding: 14px 30px;
      margin-top: 30px;
      font-size: 1.3rem;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 4px 6px rgba(0,0,0,0.2);
      transition: all 0.3s ease;
    }
    .start-btn:hover {
      background-color: #ff1493;
      transform: scale(1.05);
    }
    .slideshow {
      display: none;
      background-color: #fff0f5;
      flex-direction: column;
    }
    .slide {
      display: none;
      padding: 20px;
    }
    .slide.active {
      display: block;
    }
    .slide img {
      max-width: 90%;
      border-radius: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .slide p {
      font-size: 1.4rem;
      color: #444;
      margin-top: 15px;
      background-color: #fff;
      padding: 12px;
      border-radius: 15px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    .next-btn {
      margin-top: 25px;
      padding: 12px 28px;
      font-size: 1rem;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 20px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="welcome-screen">
    <h1>Happy Birthday My Love 💗🌎🫀</h1>
    <button class="start-btn" onclick="startSlideshow()">Tap to Begin 💫</button>
  </div>  <div class="slideshow">
    <div class="slide active">
      <img src="your-photo-1.jpg" alt="Photo 1" />
      <p>From the first smile to the first kiss 😚💗 — it all began here...</p>
    </div>
    <div class="slide">
      <img src="your-photo-2.jpg" alt="Photo 2" />
      <p>Every moment with you has been a beautiful memory 🧿🫂</p>
    </div>
    <div class="slide">
      <img src="your-photo-3.jpg" alt="Photo 3" />
      <p>Through ups and downs, we stood strong together 💕🌈</p>
    </div>
    <div class="slide">
      <img src="your-photo-4.jpg" alt="Photo 4" />
      <p>Here’s to 4 magical years and a forever to go 🌹🫶</p>
    </div>
    <button class="next-btn" onclick="nextSlide()">Next ➡️</button>
  </div>  <script>
    let currentSlide = 0;
    const slides = document.querySelectorAll('.slide');

    function startSlideshow() {
      document.querySelector('.welcome-screen').style.display = 'none';
      document.querySelector('.slideshow').style.display = 'flex';
    }

    function nextSlide() {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }
  </script></body>
</html>
