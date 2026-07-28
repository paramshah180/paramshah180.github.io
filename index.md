---
layout: default
title: Home
---
Welcome to my portfolio! My name is Param Shah, I am a current graduate student at University of Texas at Austin studying Electrical Engineering with a focus on power electronics. Here are some of projects I've got to work on, past and present.

Use the menu links above to explore my work and history.

---
layout: default
title: Home
---

<!-- Welcome Introduction -->
<h1 style="margin-top: 0; color: #ffffff;">Welcome to My Portfolio</h1>
<p style="font-size: 1.1rem; color: var(--text-muted); margin-bottom: 2.5rem;">
  Explore my engineering projects, hardware designs, and technical documentation using the menu links above.
</p>

<!-- Homepage Centerpiece Carousel -->
<div class="home-gallery" id="home-carousel-gallery">
  <button class="home-carousel-btn home-prev-btn" onclick="moveHomeSlide(-1)">❮</button>
  <button class="home-carousel-btn home-next-btn" onclick="moveHomeSlide(1)">❯</button>
  
  <img class="home-slide active" src="/Photos/Home_image.jpg" alt="Featured Portfolio Display 1">
  <img class="home-slide" src="/Photos/Home_image2.jpg" alt="Featured Portfolio Display 2">
  <img class="home-slide" src="/Photos/Home_image3.jpg" alt="Featured Portfolio Display 3">
</div>

<!-- ========================================================= -->
<!-- HOMEPAGE SPECIFIC CAROUSEL STYLES                         -->
<!-- ========================================================= -->
<style>
  .home-gallery {
    width: 100%;
    max-width: 800px;
    margin: 2rem auto;
    position: relative;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
    background: #161b26;
    border: 1px solid var(--border-color);
  }
  
  .home-slide {
    display: none;
    width: 100%;
    aspect-ratio: 16/9; /* Modern widescreen format */
    object-fit: cover;   /* Ensures images fill the frame cleanly */
  }
  
  .home-slide.active {
    display: block;
  }
  
  .home-carousel-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(11, 15, 25, 0.7);
    color: white;
    border: 1px solid var(--border-color);
    padding: 14px 18px;
    cursor: pointer;
    font-size: 1.5rem;
    font-weight: bold;
    border-radius: 4px;
    transition: all 0.2s ease-in-out;
    user-select: none;
    z-index: 10;
  }
  
  .home-carousel-btn:hover {
    background: var(--accent-brown);
    border-color: var(--accent-brown-hover);
    box-shadow: 0 0 10px rgba(139, 90, 43, 0.5);
  }
  
  .home-prev-btn { left: 15px; }
  .home-next-btn { right: 15px; }
</style>

<!-- ========================================================= -->
<!-- HOMEPAGE LIGHTWEIGHT CAROUSEL ENGINE                      -->
<!-- ========================================================= -->
<script>
  function moveHomeSlide(direction) {
    const gallery = document.getElementById('home-carousel-gallery');
    const slides = gallery.getElementsByClassName('home-slide');
    let activeIndex = 0;

    // Locate active image index
    for (let i = 0; i < slides.length; i++) {
      if (slides[i].classList.contains('active')) {
        activeIndex = i;
        break;
      }
    }

    // Hide old active image
    slides[activeIndex].classList.remove('active');

    // Calculate new index wrapping around boundaries
    let newIndex = activeIndex + direction;
    if (newIndex >= slides.length) { newIndex = 0; }
    if (newIndex < 0) { newIndex = slides.length - 1; }

    // Reveal target image
    slides[newIndex].add('active');
    slides[newIndex].classList.add('active');
  }
</script>
