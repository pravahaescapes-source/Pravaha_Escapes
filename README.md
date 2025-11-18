<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Prāvaha Escapes — Travel & Corporate Retreats</title>
  <meta name="description" content="Prāvaha Escapes — curated weekend treks, corporate offsites, wellness retreats and experiential workshops across Mumbai & Pune. Flow. Breathe. Belong." />

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --gold: #d5b16a;
      --soft-green: #6fa88d;
      --deep-green: #1b4e44;
      --navy: #0a2a43;
      --muted: #6b7280;
      --card: #ffffff;
      --bg: #fbfbfb;
      --glass: rgba(255,255,255,0.8);
    }

    /* Reset */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: 'Poppins', system-ui, sans-serif;
      background:linear-gradient(180deg,#ffffff 0%,#fbf9f5 100%);
      color:var(--navy);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      scroll-behavior:smooth;
    }
    a{color:inherit;text-decoration:none}

    /* NAV */
    nav{
      position:fixed;
      top:0;
      left:0;
      right:0;
      height:72px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:0 6%;
      background:rgba(255,255,255,0.85);
      backdrop-filter: blur(6px);
      border-bottom:1px solid rgba(10,42,67,0.04);
      z-index:1200;
    }
    .brand-wrap{display:flex;align-items:center;gap:14px}
    .brand-logo{height:50px; width:auto; display:block; border-radius:8px; object-fit:contain}
    .brand-text{
      display:flex;flex-direction:column;line-height:1;
    }
    .brand-title{
      font-family:'Playfair Display', serif;
      color:var(--navy);
      font-size:20px;
      font-weight:700;
      letter-spacing:0.6px;
    }
    .brand-sub{font-size:12px;color:var(--muted);font-weight:600}

    /* nav links */
    .nav-links{display:flex;gap:20px;align-items:center}
    .nav-links a{font-weight:600;color:var(--navy);padding:8px 6px;border-radius:8px}
    .nav-links a:hover{color:var(--gold)}
    .nav-links a.active{color:var(--gold);box-shadow:inset 0 -3px 0 var(--gold);}

    /* mobile */
    .hamburger{display:none;background:transparent;border:0;font-size:22px;cursor:pointer}
    .mobile-menu{display:none;position:fixed;top:72px;left:0;right:0;background:var(--card);padding:14px 6%;box-shadow:0 8px 30px rgba(10,42,67,0.12);}

    /* HERO */
    .hero{
      margin-top:72px;
      min-height:80vh;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding:48px 6%;
      background-image: linear-gradient(180deg, rgba(10,42,67,0.18), rgba(10,42,67,0.0)), url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1600&q=80');
      background-size:cover;
      background-position:center;
      color: #fff;
    }
    .hero-inner{max-width:980px}
    .hero h1{
      font-family:'Playfair Display', serif;
      font-size:48px;
      line-height:1.02;
      margin:0 0 12px;
      text-shadow: 0 6px 22px rgba(10,42,67,0.35);
      letter-spacing:0.4px;
    }
    .hero p.lead{
      margin:0 0 18px;
      font-size:18px;
      color:rgba(255,255,255,0.92);
      opacity:0.95;
    }
    .hero .cta-group{display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
    .btn{
      background:var(--gold);
      color:var(--navy);
      padding:12px 18px;
      border-radius:10px;
      font-weight:700;
      box-shadow:0 8px 18px rgba(15,23,42,0.12);
    }
    .btn.secondary{
      background:transparent;border:1px solid rgba(255,255,255,0.18);color:#fff;
    }

    /* SECTIONS */
    section{padding:72px 6%;}
    section .section-head{display:flex;justify-content:space-between;align-items:center;gap:12px}
    h2{font-family:'Playfair Display',serif;font-size:22px;margin:0;color:var(--navy)}
    .muted{color:var(--muted)}

    /* GRID / CARDS */
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-top:18px}
    .card{background:var(--card);border-radius:14px;padding:18px;box-shadow:0 6px 20px rgba(10,42,67,0.06);transition:transform .18s ease}
    .card:hover{transform:translateY(-6px)}
    .card img{width:100%;height:180px;object-fit:cover;border-radius:10px}

    /* Gallery */
    .gallery{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
    .gallery img{width:100%;height:160px;object-fit:cover;border-radius:10px;cursor:pointer;box-shadow:0 4px 12px rgba(10,42,67,0.06)}

    /* Testimonials */
    .test-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
    .testimonial{padding:20px;border-radius:12px;background:linear-gradient(180deg,#fff,#fff);box-shadow:0 6px 18px rgba(10,42,67,0.04)}

    /* Contact */
    .contact-box{max-width:520px;margin:0 auto;background:var(--card);padding:22px;border-radius:12px;box-shadow:0 8px 26px rgba(10,42,67,0.06)}
    input,textarea,select{width:100%;padding:10px;border-radius:8px;border:1px solid #e6e6e6;margin-top:10px;font-size:15px}
    .note{font-size:13px;color:var(--muted);margin-top:8px}

    /* Footer */
    footer{padding:28px 6%;background:linear-gradient(180deg,var(--navy),#052034);color:#fff;text-align:center;border-top:1px solid rgba(255,255,255,0.03)}
    footer a{color:var(--gold);font-weight:700}

    /* WhatsApp floating */
    .whatsapp{
      position:fixed;right:20px;bottom:20px;z-index:1300;background:#25d366;color:#fff;padding:14px;border-radius:50%;font-size:20px;box-shadow:0 10px 30px rgba(10,42,67,0.18);display:flex;align-items:center;justify-content:center
    }

    /* responsive */
    @media (max-width:1000px){
      .grid-3{grid-template-columns:repeat(2,1fr)}
      .gallery{grid-template-columns:repeat(3,1fr)}
    }
    @media (max-width:760px){
      nav{padding:0 4%}
      .nav-links{display:none}
      .hamburger{display:block}
      .mobile-menu{display:none}
      .grid-3{grid-template-columns:1fr}
      .gallery{grid-template-columns:repeat(2,1fr)}
      .test-grid{grid-template-columns:1fr}
      .hero h1{font-size:34px}
    }

    /* reveal animation */
    .reveal{opacity:0;transform:translateY(20px);transition:all .7s cubic-bezier(.2,.9,.2,1)}
    .reveal.active{opacity:1;transform:none}
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="brand-wrap">
      <!-- Upload your logo as 'logo.png' into same folder -->
      <img src="logo.png" alt="Prāvaha Escapes logo" class="brand-logo" onerror="this.style.display='none'">
      <div class="brand-text">
        <div class="brand-title">Prāvaha Escapes</div>
        <div class="brand-sub">Flow. Breathe. Belong.</div>
      </div>
    </div>

    <div style="display:flex;align-items:center;gap:14px">
      <div class="nav-links" id="navLinks">
        <a href="#home" data-target="home">Home</a>
        <a href="#about" data-target="about">About</a>
        <a href="#events" data-target="events">Our Escapes</a>
        <a href="#gallery" data-target="gallery">Gallery</a>
        <a href="#testimonials" data-target="testimonials">Testimonials</a>
        <a href="#contact" data-target="contact">Contact</a>
      </div>

      <button class="hamburger" id="hamburger" aria-label="Open menu">☰</button>
    </div>
  </nav>

  <!-- mobile menu -->
  <div class="mobile-menu" id="mobileMenu" aria-hidden="true">
    <a href="#home">Home</a><br/>
    <a href="#about">About</a><br/>
    <a href="#events">Our Escapes</a><br/>
    <a href="#gallery">Gallery</a><br/>
    <a href="#testimonials">Testimonials</a><br/>
    <a href="#contact">Contact</a>
  </div>

  <!-- HERO -->
  <header class="hero" id="home">
    <div class="hero-inner reveal">
      <h1>Weekend escapes & corporate retreats crafted with care</h1>
      <p class="lead">We design short treks, wellness retreats and experiential workshops that help teams reset — without the hassle.</p>
      <div class="cta-group">
        <a class="btn" href="#events">View Escapes</a>
        <a class="btn secondary" href="#contact">Request a Quote</a>
      </div>
    </div>
  </header>

  <!-- ABOUT -->
  <section id="about" class="reveal">
    <div class="section-head">
      <h2>About <span class="muted">Prāvaha Escapes</span></h2>
      <div class="muted">Trusted & curated experiences across Maharashtra</div>
    </div>
    <p style="margin-top:16px;color:var(--deep-green);max-width:900px">
      Prāvaha Escapes combines experienced guides and corporate facilitators to create meaningful offsites, wellness weekends and active adventures. We focus on safety, sustainability and measurable outcomes — from leadership sprints to cold-plunge recovery sessions.
    </p>
  </section>

  <!-- EVENTS -->
  <section id="events" class="reveal">
    <div class="section-head">
      <h2>Our <span class="muted">Escapes</span></h2>
      <div class="muted">Small groups — Expert guides</div>
    </div>

    <div class="grid-3" style="margin-top:18px">
      <article class="card">
        <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=900&q=80" alt="Trek">
        <h3 style="margin-top:12px">Kalsubai Sunrise Trek</h3>
        <p class="muted">Sunrise summit, camp breakfast and team reflection session.</p>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1526498460520-4c246339dccb?auto=format&fit=crop&w=900&q=80" alt="Corporate offsite">
        <h3 style="margin-top:12px">Corporate Offsite — Reset</h3>
        <p class="muted">Custom agendas: strategy sprints, team games, and guided facilitation.</p>
      </article>

      <article class="card">
        <img src="https://images.unsplash.com/photo-1520975698519-59cde193b6cf?auto=format&fit=crop&w=900&q=80" alt="Pottery">
        <h3 style="margin-top:12px">Pottery & Creativity Day</h3>
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
    <div class="gallery" style="margin-top:18px">
      <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=1000&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1469474968028-56623f02e42e?auto=format&fit=crop&w=1000&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=1000&q=80" alt="">
      <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1000&q=80" alt="">
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section id="testimonials" class="reveal">
    <div class="section-head">
      <h2>What <span class="muted">Clients Say</span></h2>
      <div class="muted">Real feedback from teams & individuals</div>
    </div>

    <div class="test-grid" style="margin-top:18px">
      <div class="testimonial">
        <p>“Prāvaha organised an unforgettable offsite — logistics, facilitation and follow-up were handled seamlessly.”</p>
        <div style="margin-top:8px;font-weight:700">— Product Team, Fintech</div>
      </div>

      <div class="testimonial">
        <p>“The cold-plunge recovery session was transformative — perfect mix of science and calm.”</p>
        <div style="margin-top:8px;font-weight:700">— Rahul S.</div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="reveal">
    <div class="section-head">
      <h2>Contact</h2>
      <div class="muted">Tell us about your team — we’ll respond within 24 hours</div>
    </div>

    <div style="margin-top:18px">
      <div class="contact-box">
        <!-- Replace the action URL with your Formspree endpoint (or use your backend) -->
        <form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST">
          <label class="muted">Name</label>
          <input type="text" name="name" required placeholder="Your name">
          <label class="muted">Work Email</label>
          <input type="email" name="email" required placeholder="you@company.com">
          <label class="muted">Phone</label>
          <input type="tel" name="phone" placeholder="+91 9xxxxxxxxx">
          <label class="muted">Message</label>
          <textarea name="message" rows="5" placeholder="Dates, team size, goals..."></textarea>

          <div style="display:flex;gap:10px;margin-top:12px">
            <button class="btn" type="submit">Send Enquiry</button>
            <a class="btn" href="mailto:hello@pravaha.example" style="background:transparent;color:var(--navy);border:1px solid #e6e6e6">Email Us</a>
          </div>

          <div class="note" id="formNote">We will contact you within 24 hours.</div>
        </form>
      </div>
    </div>
  </section>

  <!-- WhatsApp quick chat -->
  <a class="whatsapp" href="https://wa.me/91XXXXXXXXXX?text=Hello%20Pravaha%20Escapes%2C%20I%20am%20interested%20in%20your%20corporate%20offsite%20packages.">
    <span aria-hidden="true">💬</span>
  </a>

  <!-- Footer -->
  <footer>
    <div style="max-width:1100px;margin:0 auto;padding:18px 6%;">
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
        <div style="font-weight:700;color:var(--gold)">Prāvaha Escapes</div>
        <div class="muted" style="color:rgba(255,255,255,0.84)">© <span id="year"></span> Prāvaha Escapes — Flow. Breathe. Belong.</div>
        <div><a href="https://instagram.com/YOUR_INSTAGRAM" target="_blank" rel="noopener">Instagram</a></div>
      </div>
    </div>
  </footer>

  <!-- LIGHT SCRIPT: mobile menu, reveal, form handling, active nav -->
  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Mobile menu toggle
    const hamburger = document.getElementById('hamburger');
    const mobileMenu = document.getElementById('mobileMenu');
    let menuOpen = false;
    hamburger.addEventListener('click', () => {
      menuOpen = !menuOpen;
      mobileMenu.style.display = menuOpen ? 'block' : 'none';
      mobileMenu.setAttribute('aria-hidden', !menuOpen);
    });
    // hide mobile menu on link click
    mobileMenu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => {
      mobileMenu.style.display = 'none'; menuOpen = false;
    }));

    // Reveal on scroll
    const revealEls = document.querySelectorAll('.reveal');
    const obs = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) { e.target.classList.add('active'); obs.unobserve(e.target); }
      });
    }, {threshold: 0.12});
    revealEls.forEach(el => obs.observe(el));

    // Active nav link using IntersectionObserver
    const sections = document.querySelectorAll('section, header#home');
    const navLinks = document.querySelectorAll('.nav-links a');
    const sectionObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const id = entry.target.id;
          navLinks.forEach(a => {
            a.classList.toggle('active', a.getAttribute('href') === '#' + id);
          });
        }
      });
    }, {threshold:0.35});
    sections.forEach(s => sectionObserver.observe(s));

    // Form handling (client-side feedback)
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', (e) => {
      // If you're using Formspree replace action with your endpoint; we will show sending message for UX
      const note = document.getElementById('formNote');
      note.textContent = "Sending...";
      // let browser handle POST — Formspree will respond
      setTimeout(()=>{ note.textContent = "Thanks! Your enquiry has been sent."; form.reset(); }, 900);
    });

    // Smooth scroll behavior for nav clicks (close mobile menu)
    document.querySelectorAll('a[href^="#"]').forEach(a => {
      a.addEventListener('click', (ev) => {
        // allow default anchor behavior only for same-page anchors
        if (a.getAttribute('href').startsWith('#')) {
          // close mobile menu
          if (menuOpen) { mobileMenu.style.display='none'; menuOpen=false; }
        }
      });
    });
  </script>
</body>
</html>
