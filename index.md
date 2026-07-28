---
layout: default
title: Home
---
Welcome to my portfolio! My name is Param Shah, I am a current graduate student at University of Texas at Austin studying Electrical Engineering with a focus on power electronics. Here are some of projects I've got to work on, past and present.

Use the menu links above to explore my work and history.

<!-- Homepage Centerpiece Carousel (Scaled Down) -->
<div class="home-gallery" id="home-carousel-gallery">
  <button class="home-carousel-btn home-prev-btn" onclick="moveHomeSlide(-1)">❮</button>
  <button class="home-carousel-btn home-next-btn" onclick="moveHomeSlide(1)">❯</button>
  
  <img class="home-slide active" src="/Photos/Home_image3.jpeg" alt="Featured Portfolio Display 1">
  <img class="home-slide" src="/Photos/Home_image2.jpeg" alt="Featured Portfolio Display 2">
  <img class="home-slide" src="/Photos/Home_image.jpg" alt="Featured Portfolio Display 3">
</div>

<!-- ========================================================= -->
<!-- HOMEPAGE SPECIFIC CAROUSEL STYLES                         -->
<!-- ========================================================= -->
<style>
  .home-gallery {
    width: 100%;
    max-width: 480px;    /* Scaled down from 800px to take up less screen space */
    margin: 2rem auto;
    position: relative;
    overflow: hidden;
    background: transparent; 
    border: none !important; 
    box-shadow: none !important; 
  }
  
  .home-slide {
    display: none;
    width: 100%;
    height: auto;         /* Preserves exact original image proportions */
    object-fit: contain;  /* Guarantees no cropping ever occurs */
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
    padding: 10px 14px;  /* Slightly smaller buttons to match scaled layout */
    cursor: pointer;
    font-size: 1.2rem;   /* Adjusted arrow size */
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
  
  .home-prev-btn { left: 10px; }
  .home-next-btn { right: 10px; }
</style>

<!-- ========================================================= -->
<!-- HOMEPAGE LIGHTWEIGHT CAROUSEL ENGINE                      -->
<!-- ========================================================= -->
<script>
  function moveHomeSlide(direction) {
    const gallery = document.getElementById('home-carousel-gallery');
    const slides = gallery.getElementsByClassName('home-slide');
    let activeIndex = 0;

    for (let i = 0; i < slides.length; i++) {
      if (slides[i].classList.contains('active')) {
        activeIndex = i;
        break;
      }
    }

    slides[activeIndex].classList.remove('active');

    let newIndex = activeIndex + direction;
    if (newIndex >= slides.length) { newIndex = 0; }
    if (newIndex < 0) { newIndex = slides.length - 1; }

    slides[newIndex].classList.add('active');
  }
</script>
