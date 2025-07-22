<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Modeling Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #0a0a0a;
      color: #fff;
      font-family: 'Inter', sans-serif;
      padding: 40px 20px;
    }

    header {
      text-align: center;
      margin-bottom: 40px;
    }

    header img {
      max-width: 120px;
      border-radius: 8px;
      margin: 20px 0;
    }

    .subtext {
      font-size: 1.1rem;
      color: #ccc;
      margin: 10px 0;
    }

    header h1 {
      font-size: 4.2rem;
      font-weight: 700;
      color: #fff;
      margin-top: 10px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      margin-top: 40px;
    }

    .item {
      background-color: #111;
      border: 1px solid #333;
      padding: 10px 10px 0 10px;
      display: flex;
      flex-direction: column;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;

      /* Subtle white neon glow */
      box-shadow:
        0 0 5px 1px rgba(255, 255, 255, 0.5),
        0 0 12px 2px rgba(255, 255, 255, 0.3);
    }

    .item:hover {
      transform: scale(1.02);
      box-shadow:
        0 0 8px 2px rgba(255, 255, 255, 0.7),
        0 0 18px 4px rgba(255, 255, 255, 0.4);
    }

    .image-container {
      aspect-ratio: 1 / 1;
      width: 100%;
      background: #000;
      border-radius: 6px;
      overflow: hidden;
      padding: 10px;
    }

    .image-container img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      display: block;
    }

    .caption {
      margin-top: 10px;
      padding-bottom: 10px;
      font-size: 1rem;
      color: #aaa;
      text-align: center;
    }

    .coming-soon {
      margin-top: 60px;
      padding: 80px 20px 40px; /* adjusted bottom padding for subtext */
      border: 2px dashed #333;
      text-align: center;
      font-size: 2rem;
      color: #666;
      background-color: #111;
      position: relative;
    }

    .coming-soon-subtext {
      margin-top: 15px;
      font-size: 1.2rem;
      font-style: italic;
      color: #555;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 2.8rem;
      }

      .coming-soon {
        font-size: 1.5rem;
        padding: 60px 20px 30px;
      }

      .coming-soon-subtext {
        font-size: 1rem;
      }
    }

    /* Lightbox overlay */
    .lightbox-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(10, 10, 10, 0.9);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 9999;
    }

    .lightbox-overlay.active {
      display: flex;
    }

    .lightbox-content {
      position: relative;
      max-width: 90vw;
      max-height: 90vh;
      background: #111;
      border-radius: 10px;
      box-shadow:
        0 0 15px 5px rgba(255, 255, 255, 0.8);
      padding: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .lightbox-content img {
      max-width: 100%;
      max-height: 80vh;
      border-radius: 6px;
      object-fit: contain;
      background: #000;
    }

    .lightbox-caption {
      margin-top: 12px;
      color: #ccc;
      font-size: 1.2rem;
      text-align: center;
    }

    .lightbox-close {
      position: absolute;
      top: 10px;
      right: 10px;
      background: transparent;
      border: none;
      color: #ccc;
      font-size: 2rem;
      cursor: pointer;
      user-select: none;
      transition: color 0.2s ease;
    }

    .lightbox-close:hover {
      color: white;
    }
  </style>
</head>
<body>

  <header>
    <div class="subtext">• Hello! I am a modeler/builder 🧱🔨 •</div>
    <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/q_auto:good,f_auto,fl_progressive/v1753164241/jlquc0grsjhp3wd0t3jj.jpg" alt="Logo" />
    <h1>Welcome!</h1>
    <div class="subtext">• Explore my 3D creations made in Blender •</div>
  </header>

  <section class="gallery">

    <div class="item" data-caption="Terminal" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159723/d6qcdgrysmfvge5t0dg1.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159723/d6qcdgrysmfvge5t0dg1.jpg" alt="Terminal" />
      </div>
      <div class="caption">Terminal</div>
    </div>

    <div class="item" data-caption="Cash Register" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159910/fqg9rosa12rjprvifsis.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159910/fqg9rosa12rjprvifsis.jpg" alt="Cash Register" />
      </div>
      <div class="caption">Cash Register</div>
    </div>

    <div class="item" data-caption="Freddy" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159952/o3s6qthigmujzn8s7v22.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753159952/o3s6qthigmujzn8s7v22.jpg" alt="Freddy" />
      </div>
      <div class="caption">Freddy</div>
    </div>

    <div class="item" data-caption="Camp Fazbear Exit" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753160083/bezapvhvm1k3spbfwfs0.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753160083/bezapvhvm1k3spbfwfs0.jpg" alt="Camp Fazbear Exit" />
      </div>
      <div class="caption">Camp Fazbear Exit</div>
    </div>

    <div class="item" data-caption="Camp Fazbear Exit Door v2" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753161996/c5wwxmhrampr4upmf1xm.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753161996/c5wwxmhrampr4upmf1xm.jpg" alt="Camp Fazbear Exit Door v2" />
      </div>
      <div class="caption">Camp Fazbear Exit Door v2</div>
    </div>

    <div class="item" data-caption="Diamond Holder" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753162024/lnealdtfbpjqvm8pyl7u.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753162024/lnealdtfbpjqvm8pyl7u.jpg" alt="Diamond Holder" />
      </div>
      <div class="caption">Diamond Holder</div>
    </div>

    <div class="item" data-caption="Golden Vault" data-src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753162041/nfqckugatpxm6iooiz0b.jpg">
      <div class="image-container">
        <img src="https://res.cloudinary.com/dtjjgiitl/image/upload/v1753162041/nfqckugatpxm6iooiz0b.jpg" alt="Golden Vault" />
      </div>
      <div class="caption">Golden Vault</div>
    </div>

  </section>

  <div class="coming-soon">
    COMING SOON
    <div class="coming-soon-subtext">
      (Bling Freddy's Golden Bank Map)
    </div>
  </div>

  <!-- Lightbox markup -->
  <div class="lightbox-overlay" id="lightbox">
    <div class="lightbox-content">
      <button class="lightbox-close" id="lightbox-close" aria-label="Close">&times;</button>
      <img src="" alt="" id="lightbox-img" />
      <div class="lightbox-caption" id="lightbox-caption"></div>
    </div>
  </div>

  <script>
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const lightboxCaption = document.getElementById('lightbox-caption');
    const lightboxClose = document.getElementById('lightbox-close');

    document.querySelectorAll('.item').forEach(item => {
      item.addEventListener('click', () => {
        const src = item.getAttribute('data-src');
        const caption = item.getAttribute('data-caption');
        lightboxImg.src = src;
        lightboxImg.alt = caption;
        lightboxCaption.textContent = caption;
        lightbox.classList.add('active');
        document.body.style.overflow = 'hidden'; // prevent background scroll
      });
    });

    function closeLightbox() {
      lightbox.classList.remove('active');
      document.body.style.overflow = ''; // restore scroll
      lightboxImg.src = '';
      lightboxCaption.textContent = '';
    }

    lightboxClose.addEventListener('click', closeLightbox);

    // Clicking outside image closes lightbox
    lightbox.addEventListener('click', (e) => {
      if (e.target === lightbox) {
        closeLightbox();
      }
    });

    // Escape key closes lightbox
    window.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && lightbox.classList.contains('active')) {
        closeLightbox();
      }
    });
  </script>
<script>
  window.onload = function() {
    window.scrollTo(0, 0);
  };
</script>

</body>
</html>
