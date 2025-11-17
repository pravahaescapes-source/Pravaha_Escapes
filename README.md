<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Escape Travel & Corporate Retreats</title>

  <!-- GOOGLE FONTS -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />

  <style>
    body {
      margin: 0;
      font-family: "Poppins", sans-serif;
      background: #fafafa;
      color: #333;
      scroll-behavior: smooth;
    }

    /* BRAND COLORS */
    :root {
      --primary: #ff8c00;
      --dark: #222;
      --light: #ffffff;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: var(--light);
      padding: 15px 10%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      z-index: 1000;
    }
    nav h1 { margin: 0; color: var(--primary); font-size: 1.5rem; font-weight: 700; }
    nav ul {
      list-style: none;
      display: flex;
      gap: 25px;
      margin: 0;
    }
    nav a {
      text-decoration: none;
      color: var(--dark);
      font-weight: 600;
    }
    nav a:hover {
      color: var(--primary);
    }

    /* HERO */
    .hero {
      margin-top: 80px;
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
        url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1200&q=80') center/cover;
      height: 100vh;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
    }

    .hero h1 { font-size: 3rem; }
    .btn { padding: 12px 25px; background: var(--primary); color: white; border-radius: 8px; text-decoration: none; display: inline-block; margin-top: 15px; }

    /* SECTION */
    section { padding: 80px 10%; }
    h2 { font-size: 2rem; text-transform: uppercase; margin-bottom: 20px; }
    .highlight { color: var(--primary); }

    /* ANIMATION */
    .reveal { opacity: 0; transform: translateY(40px); transition: 0.9s ease; }
    .reveal.active { opacity: 1; transform: translateY(0px); }

    /* CARD GRID */
    .card-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px,1fr)); gap: 25px; }
    .card { background: white; border-radius: 14px; padding: 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
    .card img { width: 100%; border-radius: 10px; }

    /* GALLERY */
    .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; }
    .gallery img { width: 100%; border-radius: 12px; box-shadow: 0 3px 8px rgba(0,0,0,0.1); }

    /* TESTIMONIALS */
    .testimonial { background: #fff; padding: 25px; border-radius: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }

    /* CONTACT */
    .contact-box { max-width: 450px; margin: auto; background: white; padding: 25px; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
    input, textarea { width: 100%; padding: 10px; margin-top: 10px; border-radius: 8px; border: 1px solid #ccc; }
    button { padding: 12px; background: var(--primary); color: white; border: none; border-radius: 8px; margin-top: 15px; width: 100%; font-size: 1rem; }

    /* FOOTER */
    footer { text-align: center; padding: 20px; background: var(--dark); color: white; }

    /* WHATSAPP BUTTON */
    .whatsapp {
      position: fixed;
      bottom: 25px;
      right: 25px;
      background: #25d366;
      padding: 15px;
      border-radius: 50%;
      color: white;
      font-size: 25px;
      text-decoration: none;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
      z-index: 999;
    }
  </style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <h1>Escape</h1>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#events">Events</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#testimonials">Testimonials</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO SECTION -->
<div class="hero" id="home">
  <div class="reveal">
    <h1>Escape The Ordinary</h1>
    <p>Your Corporate & Weekend Travel Partner</p>
    <a class="btn" href="#events">Explore Events</a>
  </div>
</div>

<!-- ABOUT -->
<section id="about" class="reveal">
  <h2>About <span class="highlight">Us</span></h2>
  <p>We create weekend getaways, corporate offsites, marathons, cycling tours, and burnout recovery programs for Pune & Mumbai. B2B + B2C experiences curated for joy and wellness.</p>
</section>

<!-- EVENTS -->
<section id="events" class="reveal">
  <h2>Upcoming <span class="highlight">Events</span></h2>
  <div class="card-container">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=600&q=80" />
      <h3>Kalsubai Sunrise Trek</h3>
      <p>Experience Maharashtra’s highest peak.</p>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1526498460520-4c246339dccb?auto=format&fit=crop&w=600&q=80" />
      <h3>Corporate Offsite</h3>
      <p>Team bonding games + nature + wellness.</p>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1520975698519-59cde193b6cf?auto=format&fit=crop&w=600&q=80" />
      <h3>Pottery Workshop</h3>
      <p>Relax your mind & boost creativity.</p>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section id="gallery" class="reveal">
  <h2>Photo <span class="highlight">Gallery</span></h2>
  <div class="gallery">
    <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=800&q=80" />
    <img src="https://images.unsplash.com/photo-1469474968028-56623f02e42e?auto=format&fit=crop&w=800&q=80" />
    <img src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=800&q=80" />
    <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80" />
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials" class="reveal">
  <h2>What <span class="highlight">Clients Say</span></h2>
  <div class="card-container">
    <div class="testimonial">
      <p>“Amazing energy! Our corporate offsite was perfectly organized.”</p>
      <b>— Deloitte Team</b>
    </div>
    <div class="testimonial">
      <p>“Best sunrise trek experience ever, very safe and fun.”</p>
      <b>— Sneha</b>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="reveal">
  <h2>Contact <span class="highlight">Us</span></h2>
  <div class="contact-box">
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="4" placeholder="Message"></textarea>
      <button>Send</button>
    </form>
  </div>
</section>

<!-- WHATSAPP BUTTON -->
<a class="whatsapp" href="https://wa.me/91XXXXXXXXXX">💬</a>

<!-- FOOTER -->
<footer>
  © 2025 Escape Travel & Corporate Retreats
</footer>

<!-- ANIMATION SCRIPT -->
<script>
  window.addEventListener('scroll', () => {
    document.querySelectorAll('.reveal').forEach(sec => {
      const top = sec.getBoundingClientRect().top;
      if (top < window.innerHeight - 100) sec.classList.add('active');
    });
  });
</script>

</body>
</html>
