<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Love</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: black;
      color: white;
      text-align: center;
    }
    .screen {
      display: none;
      height: 100vh;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding: 30px;
    }
    #welcome {
      display: flex;
      background: url('bg-placeholder.jpg') no-repeat center center/cover;
    }
    #poemPage {
      background-color: #111;
    }
    h1, p {
      margin: 10px 0;
    }
    .button {
      padding: 12px 24px;
      font-size: 1.2em;
      background: #ff3366;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 20px;
    }
    .slideshow {
      padding: 40px 20px;
      display: none;
    }
    .slide {
      margin-bottom: 50px;
      animation: fadeIn 2s ease-in-out;
      display: none;
    }
    .slide img, .slide video {
      max-width: 90%;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(255,255,255,0.3);
    }
    .poetry {
      font-size: 1.2em;
      margin-top: 20px;
      font-style: italic;
    }
    audio {
      display: none;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>

<!-- Welcome Screen -->
<div class="screen" id="welcome">
  <h1>Happy Birthday My Love!!!💗</h1>
  <p>Tap to begin your memorable journey 🫂❤️</p>
  <button class="button" onclick="showPoem()">Let's Begin 🥹</button>
</div>

<!-- Poem Page -->
<div class="screen" id="poemPage">
  <h1>Happy Birthday Mine!!!❤️🌎</h1>
  <p>You grow like a river, calm yet strong,<br>
     Carving dreams, singing life's song.<br>
     You shine like the stars in the endless sky,<br>
     Lighting my world, lifting me high.</p>
  <p>I hope we stay together like roots and tree,<br>
     Bound by love, wild and free.<br>
     Today and forever, come what may,<br>
     I choose you more with every day.</p>
  <p><strong>Happy Birthday My Forever Home 🫀🧿</strong></p>
  <button class="button" onclick="startSlideshow()">Start Our 4-Year Journey</button>
</div>

<!-- Slideshow Page -->
<div class="screen slideshow" id="slideshow">
  <audio id="bg-music" autoplay loop>
    <source src="ye-tune-kya-kiya.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <!-- Photo Slide 1 -->
  <div class="slide">
    <img src="photoo1.jpg" alt="Memory 1">
    <p class="poetry">"Year 1: From friendship’s first spark, you lit up my dark."</p>
  </div>
  <!-- Photo Slide 2 -->
  <div class="slide">
    <img src="photo2.jpg" alt="Memory 2">
    <p class="poetry">"Year 2: Laughter, late nights, and dreams we drew.🫀🫂"</p>
  </div>
  <!-- Photo Slide 3 -->
  <div class="slide">
    <img src="photo3.jpg" alt="Memory 3">
    <p class="poetry">"Year 3: Weathered storms, held each other true.🫂"</p>
  </div>
  <!-- Photo Slide 4 -->
  <div class="slide">
    <img src="photo4.jpg" alt="Memory 4">
    <p class="poetry">"Year 4: From smiles to memories that feel brand new.❤️"</p>
  </div>
  <!-- Photo Slide 5 -->
  <div class="slide">
    <img src="photo5.jpg" alt="Memory 5">
    <p class="poetry">"New beginnings, side by side, together we thrive 😌🫂."</p>
  </div>
  <!-- Photo Slide 6 -->
  <div class="slide">
    <img src="photo6.jpg" alt="Memory 6">
    <p class="poetry">"In every laugh, in every tear, you've been my guiding light.💗😚"</p>
  </div>
  <!-- Photo Slide 7 -->
  <div class="slide">
    <img src="photo7.jpg" alt="Memory 7">
    <p class="poetry">"No distance too far, no hurdle too tall, your love conquers it all.🧿🫂"</p>
  </div>
  <!-- Photo Slide 8 -->
  <div class="slide">
    <img src="photo8.jpg" alt="Memory 8">
    <p class="poetry">"With you, the world feels just right, you’re my moonlight.🌝🫂"</p>
  </div>
  <!-- Photo Slide 9 -->
  <div class="slide">
    <img src="photo9.jpg" alt="Memory 9">
    <p class="poetry">"Through thick and thin, I’ll always stand by you.❤️🤝🏻"</p>
  </div>
  <!-- Photo Slide 10 -->
  <div class="slide">
    <img src="photo10.jpg" alt="Memory 10">
    <p class="poetry">"Here's to forever, one moment at a time 🌎🫀"</p>
  </div>

  <!-- Video Slide -->
<div class="slide">
  <video controls width="100%" height="auto">
    <source src="video1.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p class="poetry">"Our beautiful journey, captured in time, every moment sublime."</p>
</div>


<script>
  function showPoem() {
    document.getElementById('welcome').style.display = 'none';
    document.getElementById('poemPage').style.display = 'flex';
  }

  function startSlideshow() {
    document.getElementById('poemPage').style.display = 'none';
    document.getElementById('slideshow').style.display = 'block';
    document.getElementById('bg-music').play();
    
    // Start Slideshow
    let currentSlide = 0;
    const slides = document.querySelectorAll('.slide');
    const totalSlides = slides.length;

    function showNextSlide() {
      slides[currentSlide].style.display = 'none';
      currentSlide = (currentSlide + 1) % totalSlides;
      slides[currentSlide].style.display = 'block';
    }
    if (slides[currentSlide].querySelector('video')) {
  document.getElementById('bg-music').pause(); // Pause music on video slide
} else {
  document.getElementById('bg-music').play(); // Resume otherwise
    }

    // Start showing the first slide and set interval to change slides
    slides[currentSlide].style.display = 'block';
    setInterval(showNextSlide, 4000); // Change slides every 4 seconds
  }

  // Show welcome screen on load
  window.onload = function() {
    document.getElementById('welcome').style.display = 'flex';
  }
</script>

</body>
</html>
