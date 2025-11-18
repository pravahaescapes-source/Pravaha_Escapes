<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Prāvaha Escapes — Flow. Breathe. Belong.</title>
  <meta name="description" content="Prāvaha Escapes — curated weekend treks, corporate offsites and wellness retreats around Mumbai & Pune." />

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --gold:#d5b16a;
      --soft-green:#6fa88d;
      --deep-green:#1b4e44;
      --navy:#0a2a43;
      --muted:#6b7280;
      --card:#ffffff;
      --bg:#fbfbfb;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:'Poppins',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial;
      color:var(--navy);
      background:linear-gradient(180deg,#ffffff 0%,#fbf9f5 100%);
      -webkit-font-smoothing:antialiased;
    }
    a{color:inherit;text-decoration:none}

    /* NAV */
    nav{
      position:fixed;left:0;right:0;top:0;height:68px;
      display:flex;align-items:center;justify-content:space-between;padding:0 5%;
      background:rgba(255,255,255,0.88);backdrop-filter:blur(6px);z-index:1200;
      border-bottom:1px solid rgba(10,42,67,0.04);
    }
    .brand{display:flex;align-items:center;gap:12px;}
    .brand img{height:46px;width:auto;display:block;border-radius:8px}
    .brand-title{font-family:'Playfair Display',serif;font-size:18px;color:var(--navy);font-weight:700}
    .brand-sub{font-size:11px;color:var(--muted);margin-top:2px}

    .nav-links{display:flex;gap:18px;align-items:center}
    .nav-links a{font-weight:600;color:var(--navy);padding:6px 8px;border-radius:8px}
    .nav-links a:hover{color:var(--gold)}
    .nav-links a.active{color:var(--gold);box-shadow:inset 0 -3px 0 var(--gold)}

    .hamburger{display:none;background:transparent;border:0;font-size:22px;cursor:pointer}

    /* HERO */
    header.hero{
      margin-top:68px;min-height:66vh;display:flex;align-items:center;justify-content:center;
      background-image: linear-gradient(180deg, rgba(10,42,67,0.18), rgba(10,42,67,0.02)), url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1600&q=80');
      background-size:cover;background-position:center;padding:48px 5%;text-align:center;color:#fff;
    }
    .hero-inner{max-width:980px}
    .hero h1{font-family:'Playfair Display',serif;font-size:36px;line-height:1.02;margin:0 0 10px;text-shadow:0 8px 28px rgba(10,42,67,0.45)}
    .lead{font-size:16px;margin:0 0 16px;opacity:0.95}
    .cta{display:flex;gap:10px;justify-content:center;flex-wrap:wrap}
    .btn{background:var(--gold);color:var(--navy);padding:10px 16px;border-radius:10px;font-weight:700;box-shadow:0 10px 22px rgba(10,42,67,0.12)}
    .btn.secondary{background:transparent;border:1px solid rgba(255,255,255,0.16);color:#fff}

    /* SECTIONS */
    section{padding:64px 5%}
    .section-head{display:flex;justify-content:space-between;align-items:center;gap:12px}
    h2{font-family:'Playfair Display',serif;font-size:20px;margin:0}
    .muted{color:var(--muted)}

    /* GRID */
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-top:18px}
    .card{background:var(--card);border-radius:12px;padding:14px;box-shadow:0 8px 26px rgba(10,42,67,0.06);transition:transform .18s}
    .card:hover{transform:translateY(-6px)}
    .card img{width:100%;height:160px;object-fit:cover;border-radius:8px}

    /* GALLERY */
    .gallery{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-top:14px}
    .gallery img{width:100%;height:140px;object-fit:cover;border-radius:10px;box-shadow:0 4px 12px rgba(0,0,0,0.06);cursor:pointer}

    /* Testimonials */
    .test-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;margin-top:14px}
    .test{background:linear-gradient(180deg,#fff,#fff);padding:16px;border-radius:10px;box-shadow:0 6px 20px rgba(10,42,67,0.04)}

    /* Contact */
    .contact-box{max-width:620px;margin:0 auto;background:var(--card);padding:18px;border-radius:12px;box-shadow:0 8px 26px rgba(10,42,67,0.06)}
    input,textarea{width:100%;padding:10px;border-radius:8px;border:1px solid #e8e8e8;margin-top:10px;font-size:15px}
    .note{font-size:13px;color:var(--muted);margin-top:10px}

    /* Footer */
    footer{padding:28px 5%;background:linear-gradient(180deg,var(--navy),#052034);color:#fff;text-align:center;margin-top:24px}
    footer a{color:var(--gold);font-weight:700}

    /* WhatsApp */
    .whatsapp{position:fixed;right:18px;bottom:18px;background:#25d366;color:#fff;padding:14px;border-radius:50%;z-index:1300;box-shadow:0 12px 30px rgba(10,42,67,0.16);display:flex;align-items:center;justify-content:center;font-size:20px}

    /* Mobile responsive */
    @media (max-width:980px){
      .grid-3{grid-template-columns:repeat(2,1fr)}
      .gallery{grid-template-columns:repeat(3,1fr)}
      .test-grid{grid-template-columns:1fr}
    }
    @media (max-width:720px){
      .nav-links{display:none}
      .hamburger{display:block}
      .gallery{grid-template-columns:repeat(2,1fr)}
      .grid-3{grid-template-columns:1fr}
      .hero h1{font-size:28px}
      .brand-title{font-size:16px}
      header.hero{min-height:56vh;padding:36px 5%}
      .brand img{height:40px}
    }

    /* reveal animation */
    .reveal{opacity:0;transform:translateY(16px);transition:all .7s cubic-bezier(.2,.9,.2,1)}
    .reveal.active{opacity:1;transform:none}
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="brand">
      <!-- ensure your logo filename is exactly logo.png and uploaded to repo root -->
      <img src="logo.png" alt="Prāvaha Escapes logo" onerror="this.style.display='none'">
      <div>
        <div class="brand-title">Prāvaha Escapes</div>
        <div class="brand-sub">Flow. Breathe. Belong.</div>
      </div>
    </div>

    <div style="display:flex;align-items:center;gap:12px">
      <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#events">Our Escapes</a>
        <a href="#gallery">Gallery</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#contact">Contact</a>
      </div>

      <button class="hamburger" id="hamburger" aria-label="Open menu">☰</button>
    </div>
  </nav>

  <!-- MOBILE MENU (hidden by default) -->
  <div id="mobileMenu" style="display:none;position:fixed;top:68px;left:0;right:0;background:var(--card);padding:12px 5%;box-shadow:0 12px 30px rgba(10,42,67,0.12);z-index:1250">
    <a href="#home" style="display:block;padding:10px 0;border-bottom:1px solid #f1f1f1">Home</a>
    <a href="#about" style="display:block;padding:10px 0;border-bottom:1px solid #f1f1f1">About</a>
    <a href="#events" style="display:block;padding:10px 0;border-bottom:1px solid #f1f1f1">Our Escapes</a>
    <a href="#gallery" style="display:block;padding:10px 0;border-bottom:1px solid #f1f1f1">Gallery</a>
    <a href="#testimonials" style="display:block;padding:10px 0;border-bottom:1px solid #f1f1f1">Testimonials</a>
    <a href="#contact" style="display:block;padding:10px 0">Contact</a>
  </div>

  <!-- HERO -->
  <header class="hero" id="home">
    <div class="hero-inner reveal">
      <h1>Weekend escapes & corporate retreats crafted with care</h1>
      <p class="lead">Short treks, wellness retreats and experiential workshops to help teams reset and recharge — without the hassle.</p>
      <div class="cta">
        <a class="btn" href="#events">View Escapes</a>
        <a class="btn secondary" href="#contact">Request Quote</a>
      </div>
    </div>
  </header>

  <!-- ABOUT -->
  <section id="about" class="reveal">
    <div class="section-head">
      <h2>About</h2>
      <div class="muted">Curated experiences across Maharashtra</div>
    </div>
    <p style="margin-top:14px;color:var(--deep-green);max-width:900px">
      Prāvaha Escapes blends experienced guides and corporate facilitators to design meaningful offsites, wellness weekends and active escapes. We focus on safety, sustainability and outcomes — whether it’s leadership sprints, trail recovery sessions, or creative workshops.
    </p>
  </section>

  <!-- EVENTS -->
  <section id="events" class="reveal">
    <div class="section-head">
      <h2>Our Escapes</h2>
      <div class="muted">Small groups · Expert guides</div>
    </div>

    <div class="grid-3">
      <article class="card">
        <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=900&q=80" alt="">
        <h3 style="margin-top:10px">Kalsubai Sunrise Trek</h3>
        <p class="muted">Sunrise summit, camp breakfast and reflection session.</p>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1526498460520-4c246339dccb?auto=format&fit=crop&w=900&q=80" alt="">
        <h3 style="margin-top:10px">Corporate Offsite — Reset</h3>
        <p class="muted">Strategy sprints, team games and guided facilitation.</p>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1520975698519-59cde193b6cf?auto=format&fit=crop&w=900&q=80" alt="">
        <h3 style="margin-top:10px">Pottery & Creativity Day</h3>
        <p class="muted">Hands-on workshop to slow down, create and reconnect.</p>
      </article>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery" class="reveal">
    <div class="section-head">
      <h2>Gallery</h2>
      <div class="muted">Moments from our escapes</div>
    </div>
    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=1200&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1469474968028-56623f02e42e?auto=format&fit=crop&w=1200&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=1200&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1200&q=80" alt="">
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section id="testimonials" class="reveal">
    <div class="section-head">
      <h2>Testimonials</h2>
      <div class="muted">Real feedback from teams</div>
    </div>
    <div class="test-grid">
      <div class="test">
        <p>“Prāvaha organised an unforgettable offsite — logistics and facilitation were seamless.”</p>
        <div style="margin-top:8px;font-weight:700">— Product Team, Fintech</div>
      </div>
      <div class="test">
        <p>“The cold-plunge session was transformative — perfect mix of science & calm.”</p>
        <div style="margin-top:8px;font-weight:700">— Rahul S.</div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="reveal">
    <div class="section-head">
      <h2>Contact</h2>
      <div class="muted">Tell us about your team — we’ll reply in 24 hours</div>
    </div>
    <div style="margin-top:14px">
      <div class="contact-box">
        <!-- REPLACE with your Formspree endpoint or backend URL -->
        <form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST">
          <label class="muted">Name</label>
          <input type="text" name="name" required placeholder="Your name">
          <label class="muted">Work Email</label>
          <input type="email" name="email" required placeholder="you@company.com">
          <label class="muted">Phone</label>
          <input type="tel" name="phone" placeholder="+91 9xxxxxxxxx">
          <label class="muted">Message</label>
          <textarea name="message" rows="4" placeholder="Dates, team size, goals..."></textarea>

          <div style="display:flex;gap:10px;margin-top:12px">
            <button class="btn" type="submit">Send Enquiry</button>
            <a class="btn" href="mailto:hello@pravaha.example" style="background:transparent;color:var(--navy);border:1px solid #e9e9e9">Email</a>
          </div>
          <div class="note" id="formNote">We will contact you within 24 hours.</div>
        </form>
      </div>
    </div>
  </section>

  <!-- WhatsApp -->
  <a class="whatsapp" href="https://wa.me/91XXXXXXXXXX?text=Hello%20Pravaha%20Escapes%2C%20I%20am%20interested%20in%20your%20packages." aria-label="Chat on WhatsApp">💬</a>

  <!-- Footer -->
  <footer>
    <div style="max-width:1100px;margin:0 auto">
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap;padding:14px 0">
        <div style="font-weight:700;color:var(--gold)">Prāvaha Escapes</div>
        <div style="color:rgba(255,255,255,0.9)">© <span id="year"></span> Flow. Breathe. Belong.</div>
        <div><a href="https://instagram.com/YOUR_INSTAGRAM" target="_blank" rel="noopener">Instagram</a></div>
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script>
    // set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // mobile menu toggle
    const hamburger = document.getElementById('hamburger');
    const mobileMenu = document.getElementById('mobileMenu');
    let open = false;
    hamburger.addEventListener('click', () => {
      open = !open;
      mobileMenu.style.display = open ? 'block' : 'none';
      hamburger.setAttribute('aria-expanded', open);
    });

    // reveal animation
    const reveals = document.querySelectorAll('.reveal');
    const rObs = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) { e.target.classList.add('active'); rObs.unobserve(e.target); }
      });
    }, {threshold:0.12});
    reveals.forEach(r => rObs.observe(r));

    // active nav highlight using IntersectionObserver
    const navLinks = document.querySelectorAll('.nav-links a');
    const sections = document.querySelectorAll('header, section');
    const secObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const id = entry.target.id || 'home';
          navLinks.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + id));
        }
      });
    }, {threshold:0.45});
    sections.forEach(s => secObserver.observe(s));

    // contact form UX
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', (ev) => {
      const note = document.getElementById('formNote');
      note.textContent = 'Sending...';
      // real submission handled by Formspree / your backend
      setTimeout(()=>{ note.textContent = 'Thanks — we received your enquiry.'; form.reset(); }, 900);
    });

    // ensure anchor links close mobile menu
    document.querySelectorAll('a[href^="#"]').forEach(a => {
      a.addEventListener('click', () => {
        if (open) { mobileMenu.style.display='none'; open=false; }
      });
    });
  </script>
</body>
</html>
