---
layout: default
title: Projects
permalink: /projects/
---
<!-- Project Section CSS Wrapper -->
<style>
  .project-container {
    display: flex;
    gap: 2.5rem;
    margin-bottom: 4rem;
    align-items: flex-start;
  }
  .project-gallery {
    flex: 1;
    min-width: 320px;
    max-width: 450px;
    position: relative;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    background: #fdfdfd;
  }
  .carousel-slide {
    display: none;
    width: 100%;
    aspect-ratio: 4/3;
    object-fit: contain;
  }
  .carousel-slide.active {
    display: block;
  }
  .carousel-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(0, 0, 0, 0.6);
    color: white;
    border: none;
    padding: 12px 16px;
    cursor: pointer;
    font-size: 1.25rem;
    font-weight: bold;
    border-radius: 4px;
    transition: background 0.2s;
    user-select: none;
    z-index: 10;
  }
  .carousel-btn:hover { background: rgba(0, 0, 0, 0.85); }
  .prev-btn { left: 10px; }
  .next-btn { right: 10px; }
  
  .project-info {
    flex: 1.2;
  }
  .project-info h2 { margin-top: 0; color: #111; }
  .tech-tag {
    display: inline-block;
    background: #eaecef;
    color: #24292e;
    padding: 0.2rem 0.6rem;
    font-size: 0.8rem;
    border-radius: 3px;
    margin-right: 0.5rem;
    font-family: monospace;
  }

  /* Responsive Mobile Collapse */
  @media (max-width: 768px) {
    .project-container {
      flex-direction: column;
      gap: 1.5rem;
    }
    .project-gallery {
      max-width: 100%;
      width: 100%;
    }
  }
</style>



<!-- ========================================================= -->
<!-- Project 1: Motor Drive for Electric Bike                               -->
<!-- ========================================================= -->

<div class="project-container">
  
  <!-- Left Side: Multi-Media Carousel (Images + Video) -->
  <div class="project-gallery" id="media-carousel-gallery">
    <button class="carousel-btn prev-btn" onclick="moveSlide('media-carousel-gallery', -1)">❮</button>
    <button class="carousel-btn next-btn" onclick="mediaMoveSlide('media-carousel-gallery', 1)">❯</button>
    
    <!-- Slide 1: The Autoplay/Looping Video -->
    
    <video class="carousel-slide active" autoplay loop muted playsinline preload="metadata">
      <source src="/Photos/MotorDriveVid.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>

    <!-- Slide 2: Regular Image -->
    
    <img class="carousel-slide" src="/Photos/MotorDrivePCB.png" alt="Project Image 1">
    
  </div>

  <!-- Right Side: Descriptive Content -->
  <div class="project-info">
    <h2> PMSM Motor Drive</h2>
    <div>
      <span class="tech-tag">C++</span>
      <span class="tech-tag">Hardware Integration and Validation</span>
      <span class="tech-tag">Motor Drives</span>
      <span class="tech-tag">Control of Power Electronics</span>
    </div>
    <p style="margin-top: 1rem;">
      Brought up and validated PMSM motor drive while interfacing IPM (Intelligent Power Module) and Hall Effect sensors. Implemented closed loop controls 
      using a TI C2000 MCU to control speed of motor with a throttle input. 
    </p>
  </div>
</div>


<!-- ========================================================= -->
<!-- PROJECT 2: Boost Converter                                -->
<!-- ========================================================= -->

<div class="project-container">
  
  <!-- Left Side: Clickable Image Carousel -->
  <div class="project-gallery" id="boost-converter-gallery">
    <button class="carousel-btn prev-btn" onclick="moveSlide('boost-converter-gallery', -1)">❮</button>
    <button class="carousel-btn next-btn" onclick="moveSlide('boost-converter-gallery', 1)">❯</button>
    
    <img class="carousel-slide active" src="/Photos/CADBoostConverter.png" alt="CAD of Boost Converter">
    <img class="carousel-slide" src="/Photos/PCB_board.jpg" alt="Front of PCB">
    <img class="carousel-slide" src="/Photos/BoostWaveforms.png" alt="Waveforms of Boost Converter">
  </div>

  <!-- Right Side: Descriptive Content -->
  <div class="project-info">
    <h2>Boost Converter</h2>
    <div>
      <span class="tech-tag">PCB Layout</span>
      <span class="tech-tag">Inductor Design</span>
      <span class="tech-tag">EMI/EMC Mitigation</span>
      <span class="tech-tag">C++</span>
    </div>
    <p style="margin-top: 1rem;">
      Boost converter used to step up 24 volts to 48 volts to power an electric bike. KiCAD was used for the PCB schematic and layout and a TI C2000 MCU was used to configure the gate drivers, MOSFETs, and dead time. Inductor was designed using the KG method, comparing the geometric constraints to the core properties of the inductor.  
    </p>
    <p>
    </p>
  </div>
</div>

<!-- ========================================================= -->
<!-- PROJECT 3: Mechanical Scribing Machine                    -->
<!-- ========================================================= -->

<div class="project-container">
  
  <!-- Left Side: Clickable Image Carousel -->
  <div class="project-gallery" id="scribing-machine-gallery">
    <button class="carousel-btn prev-btn" onclick="moveSlide('scribing-machine-gallery', -1)">&#10094;</button>
    <button class="carousel-btn next-btn" onclick="moveSlide('scribing-machine-gallery', 1)">&#10095;</button>
    
    <img class="carousel-slide active" src="/Photos/GAUSS.png" alt="Mechanical Scribing Machine Front Profile">
    <img class="carousel-slide" src="/Photos/Gauss_annotated.png" alt="Mechanical Scribing Machine CAD Blueprint Diagram">
  </div>

  <!-- Right Side: Descriptive Content -->
  <div class="project-info">
    <h2>Mechanical Scribing Machine for Perovskite Solar Cells</h2>
    <div>
      <span class="tech-tag">Hardware Design and Integration</span>
      <span class="tech-tag">CAD Modeling</span>
      <span class="tech-tag">Control Systems</span>
    </div>
    <p style="margin-top: 1rem;">
      <!-- Insert your detailed project description here. Explain the mechanical engineering requirements, 
      the purpose of scribing layers in Perovskite solar cells, and how your prototype or 
      CAD configuration solves precision manufacturing challenges. -->
      This system is used to perform three scribes, each cutting through three different materials, that are crucial to the manufacturing of perovskite solar            cells. My team and I retrofitted a CNC machine and added our custom-built Z axis assembly that enables the user to perscribe specific amounts of force with a .5 gram percision and 150 micron positional tolerence. 
    </p>
    <p>
      <!-- Highlight your primary contributions, key dimensions, structural components, 
      or performance data yielded by this specific mechanical module build. -->
      Led the hardware integration of the CNC machine, custom Z axis assembly, load cells, amplifiers, and user application script. 
      
    </p>
  </div>
</div>



<!-- ========================================================= -->
<!-- SMART VIDEO-AWARE JAVASCRIPT CAROUSEL ENGINE              -->
<!-- ========================================================= -->
<script>
  function mediaMoveSlide(galleryId, direction) {
    const gallery = document.getElementById(galleryId);
    const slides = gallery.querySelectorAll('.carousel-slide');
    let activeIndex = 0;

    // Find the currently active slide index
    for (let i = 0; i < slides.length; i++) {
      if (slides[i].classList.contains('active')) {
        activeIndex = i;
        break;
      }
    }

    // If the current slide is a video, pause it before switching away
    if (slides[activeIndex].tagName === 'VIDEO') {
      slides[activeIndex].pause();
    }

    // Remove active class from old slide
    slides[activeIndex].classList.remove('active');

    // Calculate new target index safely (loop around edges)
    let newIndex = activeIndex + direction;
    if (newIndex >= slides.length) { newIndex = 0; }
    if (newIndex < 0) { newIndex = slides.length - 1; }

    // Reveal new target slide
    slides[newIndex].classList.add('active');

    // If the new slide is a video, reset its timeline and play it automatically
    if (slides[newIndex].tagName === 'VIDEO') {
      slides[newIndex].currentTime = 0;
      slides[newIndex].play().catch(error => {
        console.log("Autoplay context prevented video start:", error);
      });
    }
  }

  // Bind the new media-aware logic to old buttons if needed
  function moveSlide(galleryId, direction) {
    mediaMoveSlide(galleryId, direction);
  }
</script>

<!-- ========================================================= -->
<!-- LIGHTWEIGHT MULTI-CAROUSEL JAVASCRIPT ENGINE              -->
<!-- ========================================================= -->
<script>
  function moveSlide(galleryId, direction) {
    const gallery = document.getElementById(galleryId);
    const slides = gallery.getElementsByClassName('carousel-slide');
    let activeIndex = 0;

    // Find currently active image index
    for (let i = 0; i < slides.length; i++) {
      if (slides[i].classList.contains('active')) {
        activeIndex = i;
        break;
      }
    }

    // Hide old active image
    slides[activeIndex].classList.remove('active');

    // Calculate new target index safely loop around boundaries
    let newIndex = activeIndex + direction;
    if (newIndex >= slides.length) { newIndex = 0; }
    if (newIndex < 0) { newIndex = slides.length - 1; }

    // Reveal new target image
    slides[newIndex].classList.add('active');
  }
</script>
