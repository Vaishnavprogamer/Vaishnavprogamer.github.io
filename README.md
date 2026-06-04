<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Universal Food Products – Pure Coconut Oil</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Cormorant+Garamond:wght@300;400;500&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #FAF5E9;
    --warm-white: #FFF9F0;
    --gold: #C8A951;
    --deep-gold: #9B7A1E;
    --dark: #1A1208;
    --brown: #3D2B0E;
    --green: #2D4A1E;
    --light-green: #4A7A30;
    --text: #2C1F0A;
    --muted: #7A6040;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Jost', sans-serif;
    background: var(--cream);
    color: var(--text);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.2rem 5%;
    background: rgba(250, 245, 233, 0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(200,169,81,0.2);
    transition: all 0.3s;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; font-weight: 700;
    color: var(--brown);
    letter-spacing: 0.02em;
  }
  .nav-logo span { color: var(--gold); }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 0.82rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--muted); text-decoration: none; font-weight: 500;
    transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--green); color: #fff !important;
    padding: 0.55rem 1.4rem; border-radius: 2px;
    transition: background 0.3s !important;
  }
  .nav-cta:hover { background: var(--light-green) !important; color: #fff !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 8rem 5% 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 80% 50%, rgba(200,169,81,0.08) 0%, transparent 60%),
                radial-gradient(ellipse at 20% 80%, rgba(45,74,30,0.06) 0%, transparent 50%);
    pointer-events: none;
  }
  /* decorative circles */
  .hero-circle {
    position: absolute; border-radius: 50%;
    border: 1px solid rgba(200,169,81,0.15);
    pointer-events: none;
  }
  .hero-circle:nth-child(1) { width: 600px; height: 600px; right: -100px; top: 50%; transform: translateY(-50%); }
  .hero-circle:nth-child(2) { width: 420px; height: 420px; right: 60px; top: 50%; transform: translateY(-50%); }
  .hero-circle:nth-child(3) { width: 240px; height: 240px; right: 195px; top: 50%; transform: translateY(-50%); background: rgba(200,169,81,0.04); }

  .hero-text { position: relative; z-index: 2; animation: fadeUp 1s ease both; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 0.5rem;
    background: rgba(200,169,81,0.12); border: 1px solid rgba(200,169,81,0.3);
    padding: 0.4rem 1rem; border-radius: 20px;
    font-size: 0.72rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--deep-gold); font-weight: 500; margin-bottom: 1.8rem;
  }
  .hero-badge::before { content: '✦'; font-size: 0.6rem; }
  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 5vw, 5.5rem);
    line-height: 1.05; font-weight: 900;
    color: var(--dark); margin-bottom: 1.5rem;
  }
  h1 em { font-style: italic; color: var(--gold); }
  .hero-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem; color: var(--muted);
    line-height: 1.7; max-width: 480px; margin-bottom: 2.5rem;
    font-weight: 400;
  }
  .hero-btns { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    background: var(--green); color: #fff;
    padding: 0.9rem 2.2rem; border: none; border-radius: 2px;
    font-size: 0.8rem; letter-spacing: 0.12em; text-transform: uppercase;
    font-weight: 500; cursor: pointer; text-decoration: none;
    transition: all 0.3s; display: inline-block;
  }
  .btn-primary:hover { background: var(--light-green); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(45,74,30,0.3); }
  .btn-outline {
    background: transparent; color: var(--brown);
    padding: 0.9rem 2.2rem; border: 1.5px solid rgba(61,43,14,0.3); border-radius: 2px;
    font-size: 0.8rem; letter-spacing: 0.12em; text-transform: uppercase;
    font-weight: 500; cursor: pointer; text-decoration: none;
    transition: all 0.3s; display: inline-block;
  }
  .btn-outline:hover { border-color: var(--gold); color: var(--gold); }

  .hero-image-wrap {
    position: relative; z-index: 2;
    display: flex; justify-content: center; align-items: center;
    animation: fadeUp 1.2s 0.2s ease both;
  }
  .coconut-illustration {
    width: 100%; max-width: 480px;
    filter: drop-shadow(0 30px 60px rgba(61,43,14,0.15));
  }

  /* ── STATS ── */
  .stats {
    background: var(--brown);
    padding: 3rem 5%;
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 2rem;
    text-align: center;
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.5rem; font-weight: 700; color: var(--gold);
  }
  .stat-label {
    font-size: 0.75rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: rgba(255,255,255,0.6); margin-top: 0.3rem;
  }

  /* ── ABOUT ── */
  .about {
    padding: 8rem 5%;
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 6rem; align-items: center;
  }
  .about-img {
    position: relative;
  }
  .about-img-box {
    width: 100%; aspect-ratio: 4/5;
    background: linear-gradient(135deg, #e8dfc0, #c8b87a);
    border-radius: 4px;
    display: flex; align-items: center; justify-content: center;
    overflow: hidden; position: relative;
  }
  .about-img-box svg { width: 70%; opacity: 0.6; }
  .about-tag {
    position: absolute; bottom: -1.5rem; right: -1.5rem;
    background: var(--green); color: #fff;
    padding: 1.5rem 2rem; border-radius: 4px;
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-style: italic;
    box-shadow: 0 12px 32px rgba(45,74,30,0.3);
  }
  .section-eyebrow {
    font-size: 0.72rem; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); font-weight: 500; margin-bottom: 1rem;
  }
  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    line-height: 1.15; font-weight: 700;
    color: var(--dark); margin-bottom: 1.5rem;
  }
  .about p {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: var(--muted);
    line-height: 1.8; margin-bottom: 1rem;
  }
  .about-features { margin-top: 2rem; display: flex; flex-direction: column; gap: 1rem; }
  .feature-row { display: flex; align-items: center; gap: 1rem; }
  .feature-icon {
    width: 40px; height: 40px; border-radius: 50%;
    background: rgba(200,169,81,0.1); border: 1px solid rgba(200,169,81,0.3);
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem; flex-shrink: 0;
  }
  .feature-text { font-size: 0.9rem; color: var(--brown); font-weight: 500; }

  /* ── PRODUCTS ── */
  .products {
    background: var(--warm-white);
    padding: 8rem 5%;
    text-align: center;
  }
  .products h2 { margin-bottom: 0.5rem; }
  .products-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: var(--muted); margin-bottom: 4rem;
  }
  .products-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 2rem; text-align: left;
  }
  .product-card {
    background: #fff; border-radius: 4px;
    overflow: hidden;
    border: 1px solid rgba(200,169,81,0.15);
    transition: all 0.4s;
    cursor: pointer;
  }
  .product-card:hover { transform: translateY(-8px); box-shadow: 0 24px 48px rgba(61,43,14,0.12); }
  .product-img {
    height: 220px;
    display: flex; align-items: center; justify-content: center;
    font-size: 5rem;
    position: relative; overflow: hidden;
  }
  .product-img::after {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(to bottom, transparent 60%, rgba(0,0,0,0.05));
  }
  .product-body { padding: 1.8rem; }
  .product-tag {
    font-size: 0.68rem; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--gold); font-weight: 500; margin-bottom: 0.5rem;
  }
  .product-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 700; color: var(--dark); margin-bottom: 0.6rem;
  }
  .product-desc { font-size: 0.88rem; color: var(--muted); line-height: 1.6; margin-bottom: 1.2rem; }
  .product-link {
    font-size: 0.78rem; letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--green); font-weight: 500; text-decoration: none;
    display: inline-flex; align-items: center; gap: 0.4rem;
    transition: gap 0.3s;
  }
  .product-card:hover .product-link { gap: 0.7rem; }

  /* ── PROCESS ── */
  .process {
    padding: 8rem 5%;
    background: var(--cream);
  }
  .process-header { text-align: center; margin-bottom: 5rem; }
  .process-steps {
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 2rem; position: relative;
  }
  .process-steps::before {
    content: '';
    position: absolute; top: 2.5rem; left: 10%; right: 10%;
    height: 1px; background: linear-gradient(to right, transparent, var(--gold), transparent);
  }
  .step { text-align: center; position: relative; }
  .step-num {
    width: 5rem; height: 5rem; border-radius: 50%;
    background: var(--cream); border: 2px solid var(--gold);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 700; color: var(--gold);
    margin: 0 auto 1.5rem; position: relative; z-index: 1;
    font-size: 1.8rem;
  }
  .step-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-weight: 700; color: var(--dark); margin-bottom: 0.6rem;
  }
  .step-desc { font-size: 0.88rem; color: var(--muted); line-height: 1.6; }

  /* ── WHY US ── */
  .why {
    background: var(--green);
    padding: 8rem 5%;
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 6rem; align-items: center;
  }
  .why h2 { color: #fff; }
  .why .section-eyebrow { color: var(--gold); }
  .why p {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: rgba(255,255,255,0.75);
    line-height: 1.8; margin-bottom: 2rem;
  }
  .why-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .why-item {
    background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.1);
    padding: 1.5rem; border-radius: 4px;
    transition: background 0.3s;
  }
  .why-item:hover { background: rgba(255,255,255,0.12); }
  .why-icon { font-size: 1.8rem; margin-bottom: 0.8rem; }
  .why-title { font-weight: 600; color: #fff; font-size: 0.95rem; margin-bottom: 0.4rem; }
  .why-desc { font-size: 0.82rem; color: rgba(255,255,255,0.6); line-height: 1.5; }

  /* ── TESTIMONIALS ── */
  .testimonials {
    padding: 8rem 5%;
    background: var(--warm-white);
    text-align: center;
  }
  .testimonials h2 { margin-bottom: 0.5rem; }
  .test-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: var(--muted); margin-bottom: 4rem;
  }
  .test-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem; text-align: left; }
  .test-card {
    background: #fff; padding: 2.5rem; border-radius: 4px;
    border: 1px solid rgba(200,169,81,0.15);
    position: relative;
  }
  .test-quote {
    font-size: 4rem; line-height: 1; color: var(--gold);
    font-family: 'Playfair Display', serif;
    position: absolute; top: 1rem; right: 1.5rem;
    opacity: 0.3;
  }
  .test-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem; color: var(--text);
    line-height: 1.7; margin-bottom: 1.5rem;
    font-style: italic;
  }
  .test-author { display: flex; align-items: center; gap: 0.8rem; }
  .test-avatar {
    width: 42px; height: 42px; border-radius: 50%;
    background: linear-gradient(135deg, var(--gold), var(--deep-gold));
    display: flex; align-items: center; justify-content: center;
    color: #fff; font-weight: 700; font-size: 1rem;
  }
  .test-name { font-weight: 600; font-size: 0.9rem; color: var(--dark); }
  .test-role { font-size: 0.78rem; color: var(--muted); }
  .stars { color: var(--gold); font-size: 0.9rem; margin-bottom: 1rem; }

  /* ── CONTACT ── */
  .contact {
    padding: 8rem 5%;
    background: var(--cream);
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 6rem;
  }
  .contact h2 { margin-bottom: 1rem; }
  .contact-intro {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: var(--muted); line-height: 1.8; margin-bottom: 2.5rem;
  }
  .contact-details { display: flex; flex-direction: column; gap: 1.2rem; }
  .contact-item { display: flex; align-items: flex-start; gap: 1rem; }
  .contact-icon {
    width: 44px; height: 44px; border-radius: 4px;
    background: rgba(200,169,81,0.1); border: 1px solid rgba(200,169,81,0.25);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem; flex-shrink: 0;
  }
  .contact-info-label { font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--gold); margin-bottom: 0.2rem; }
  .contact-info-val { font-size: 0.92rem; color: var(--brown); }

  .contact-form { display: flex; flex-direction: column; gap: 1.2rem; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.4rem; }
  label { font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--muted); font-weight: 500; }
  input, textarea, select {
    background: #fff; border: 1.5px solid rgba(61,43,14,0.15);
    border-radius: 2px; padding: 0.85rem 1rem;
    font-family: 'Jost', sans-serif; font-size: 0.9rem;
    color: var(--text); outline: none;
    transition: border-color 0.3s;
  }
  input:focus, textarea:focus, select:focus { border-color: var(--gold); }
  textarea { resize: vertical; min-height: 120px; }

  /* ── FOOTER ── */
  footer {
    background: var(--dark);
    padding: 5rem 5% 2rem;
    color: rgba(255,255,255,0.6);
  }
  .footer-grid {
    display: grid; grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 4rem; margin-bottom: 4rem;
  }
  .footer-brand .nav-logo { color: #fff; font-size: 1.6rem; margin-bottom: 1rem; display: block; }
  .footer-brand p { font-size: 0.88rem; line-height: 1.7; max-width: 260px; }
  .footer-col h4 {
    font-size: 0.75rem; letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1.2rem; font-weight: 500;
  }
  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
  .footer-col a { font-size: 0.88rem; color: rgba(255,255,255,0.55); text-decoration: none; transition: color 0.3s; }
  .footer-col a:hover { color: var(--gold); }
  .footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.08);
    padding-top: 2rem; display: flex; justify-content: space-between; align-items: center;
  }
  .footer-bottom p { font-size: 0.82rem; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .hero, .about, .why, .contact { grid-template-columns: 1fr; gap: 3rem; }
    .hero { padding-top: 7rem; }
    .hero-image-wrap { order: -1; }
    .products-grid, .test-grid { grid-template-columns: 1fr; }
    .process-steps { grid-template-columns: 1fr 1fr; }
    .process-steps::before { display: none; }
    .stats { grid-template-columns: 1fr 1fr; }
    .footer-grid { grid-template-columns: 1fr 1fr; gap: 2.5rem; }
    .why-grid { grid-template-columns: 1fr; }
    nav { padding: 1rem 4%; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Universal <span>Food</span> Products</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#products">Products</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#contact" class="nav-cta">Contact Us</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-circle"></div>
  <div class="hero-circle"></div>
  <div class="hero-circle"></div>

  <div class="hero-text">
    <div class="hero-badge">Kerala's Finest Since 1998</div>
    <h1>Pure <em>Coconut Oil</em><br>From Nature's Heart</h1>
    <p class="hero-sub">Crafted from the finest coconuts of God's Own Country, our cold-pressed oils preserve every drop of nature's goodness for your family.</p>
    <div class="hero-btns">
      <a href="#products" class="btn-primary">Explore Products</a>
      <a href="#about" class="btn-outline">Our Story</a>
    </div>
  </div>

  <div class="hero-image-wrap">
    <!-- Coconut illustration as inline SVG -->
    <svg class="coconut-illustration" viewBox="0 0 480 520" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- Background glow -->
      <circle cx="240" cy="260" r="200" fill="rgba(200,169,81,0.06)"/>
      <circle cx="240" cy="260" r="150" fill="rgba(200,169,81,0.06)"/>

      <!-- Palm leaves -->
      <path d="M240 80 C180 120 120 100 80 60 C120 80 160 110 200 130" fill="#2D4A1E" opacity="0.8"/>
      <path d="M240 80 C300 120 360 100 400 60 C360 80 320 110 280 130" fill="#2D4A1E" opacity="0.8"/>
      <path d="M240 80 C220 40 200 20 160 10 C185 30 210 55 225 75" fill="#3A6028" opacity="0.7"/>
      <path d="M240 80 C260 40 280 20 320 10 C295 30 270 55 255 75" fill="#3A6028" opacity="0.7"/>
      <path d="M240 80 C200 60 170 30 180 0 C190 30 205 55 220 70" fill="#4A7A30" opacity="0.6"/>
      <path d="M240 80 C280 60 310 30 300 0 C290 30 275 55 260 70" fill="#4A7A30" opacity="0.6"/>

      <!-- Trunk -->
      <path d="M228 90 C224 120 220 150 222 180" stroke="#8B6914" stroke-width="8" stroke-linecap="round"/>

      <!-- Main coconut (large) -->
      <ellipse cx="240" cy="320" rx="110" ry="120" fill="#5C3D11"/>
      <ellipse cx="240" cy="310" rx="108" ry="118" fill="#7A5228"/>
      <!-- coconut texture lines -->
      <path d="M150 300 Q180 290 200 310 Q220 330 240 320 Q260 310 280 330 Q300 350 330 340" stroke="#5C3D11" stroke-width="2" fill="none" opacity="0.5"/>
      <path d="M155 330 Q185 320 205 340 Q225 360 245 350 Q265 340 285 360 Q305 380 325 370" stroke="#5C3D11" stroke-width="2" fill="none" opacity="0.5"/>
      <!-- coconut top -->
      <ellipse cx="240" cy="210" rx="60" ry="25" fill="#6B4419"/>
      <ellipse cx="240" cy="208" rx="58" ry="22" fill="#8B5E2A"/>

      <!-- Oil bottle -->
      <rect x="310" y="260" width="80" height="140" rx="8" fill="rgba(200,169,81,0.15)" stroke="rgba(200,169,81,0.4)" stroke-width="1.5"/>
      <rect x="325" y="252" width="50" height="16" rx="4" fill="rgba(200,169,81,0.3)" stroke="rgba(200,169,81,0.5)" stroke-width="1"/>
      <rect x="335" y="244" width="30" height="12" rx="3" fill="rgba(200,169,81,0.4)"/>
      <!-- oil inside bottle -->
      <rect x="314" y="330" width="72" height="68" rx="0 0 6 6" fill="rgba(200,169,81,0.25)"/>
      <!-- label -->
      <rect x="318" y="275" width="64" height="50" rx="3" fill="rgba(255,255,255,0.15)" stroke="rgba(200,169,81,0.3)" stroke-width="1"/>
      <text x="350" y="296" text-anchor="middle" font-size="7" fill="rgba(200,169,81,0.9)" font-family="serif" font-weight="bold">UNIVERSAL</text>
      <text x="350" y="307" text-anchor="middle" font-size="5.5" fill="rgba(200,169,81,0.7)" font-family="serif">COCONUT OIL</text>
      <line x1="325" y1="312" x2="375" y2="312" stroke="rgba(200,169,81,0.3)" stroke-width="0.5"/>
      <text x="350" y="322" text-anchor="middle" font-size="5" fill="rgba(200,169,81,0.6)" font-family="sans-serif">PURE &amp; NATURAL</text>

      <!-- Oil drops -->
      <ellipse cx="178" cy="420" rx="18" ry="22" fill="rgba(200,169,81,0.35)" stroke="rgba(200,169,81,0.5)" stroke-width="1"/>
      <path d="M178 398 L178 405" stroke="rgba(200,169,81,0.6)" stroke-width="1.5"/>
      <ellipse cx="148" cy="440" rx="12" ry="14" fill="rgba(200,169,81,0.25)" stroke="rgba(200,169,81,0.4)" stroke-width="1"/>

      <!-- Decorative leaves small -->
      <path d="M80 380 C100 360 130 370 140 390 C120 375 95 378 80 380Z" fill="#2D4A1E" opacity="0.6"/>
      <path d="M380 430 C400 410 420 420 415 440 C405 425 390 425 380 430Z" fill="#2D4A1E" opacity="0.5"/>
    </svg>
  </div>
</section>

<!-- STATS -->
<div class="stats">
  <div>
    <div class="stat-num">25+</div>
    <div class="stat-label">Years of Excellence</div>
  </div>
  <div>
    <div class="stat-num">500K+</div>
    <div class="stat-label">Happy Customers</div>
  </div>
  <div>
    <div class="stat-num">12+</div>
    <div class="stat-label">Product Variants</div>
  </div>
  <div>
    <div class="stat-num">100%</div>
    <div class="stat-label">Natural & Pure</div>
  </div>
</div>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-img reveal">
    <div class="about-img-box">
      <svg viewBox="0 0 300 350" fill="none" xmlns="http://www.w3.org/2000/svg">
        <!-- Factory/farm illustration -->
        <rect x="50" y="180" width="200" height="130" rx="4" fill="#8B6914" opacity="0.4"/>
        <rect x="70" y="160" width="60" height="20" rx="2" fill="#8B6914" opacity="0.5"/>
        <rect x="170" y="150" width="60" height="30" rx="2" fill="#8B6914" opacity="0.5"/>
        <!-- Chimney -->
        <rect x="85" y="120" width="20" height="42" fill="#6B4E15" opacity="0.4"/>
        <rect x="185" y="110" width="20" height="42" fill="#6B4E15" opacity="0.4"/>
        <!-- Smoke -->
        <circle cx="95" cy="110" r="8" fill="white" opacity="0.3"/>
        <circle cx="90" cy="98" r="6" fill="white" opacity="0.2"/>
        <circle cx="97" cy="88" r="5" fill="white" opacity="0.15"/>
        <!-- Palm trees -->
        <line x1="30" y1="310" x2="30" y2="200" stroke="#5C3D11" stroke-width="5"/>
        <path d="M30 200 C10 180 0 160 20 150" stroke="#2D4A1E" stroke-width="6" fill="none"/>
        <path d="M30 200 C50 180 60 160 40 150" stroke="#2D4A1E" stroke-width="6" fill="none"/>
        <path d="M30 200 C0 190 -5 170 15 165" stroke="#3A6028" stroke-width="5" fill="none"/>
        <line x1="270" y1="310" x2="270" y2="200" stroke="#5C3D11" stroke-width="5"/>
        <path d="M270 200 C250 180 240 160 260 150" stroke="#2D4A1E" stroke-width="6" fill="none"/>
        <path d="M270 200 C290 180 300 160 280 150" stroke="#2D4A1E" stroke-width="6" fill="none"/>
        <!-- Ground -->
        <rect x="0" y="300" width="300" height="50" fill="#6B8F3A" opacity="0.3"/>
        <text x="150" y="260" text-anchor="middle" font-size="36" opacity="0.4">🥥</text>
      </svg>
    </div>
    <div class="about-tag">"Purity you<br>can taste"</div>
  </div>
  <div class="reveal">
    <div class="section-eyebrow">Our Story</div>
    <h2>Rooted in Kerala's<br>Coconut Heritage</h2>
    <p>Universal Food Products was founded in 1998 in the heart of Kerala with one simple mission — to bring the purest, most authentic coconut oil to every home.</p>
    <p>From our state-of-the-art factory to your kitchen, we ensure every bottle of oil retains the full nutritional richness and natural aroma that only Kerala's finest coconuts can offer.</p>
    <div class="about-features">
      <div class="feature-row">
        <div class="feature-icon">🌴</div>
        <div class="feature-text">Sourced from certified organic coconut farms in Kerala</div>
      </div>
      <div class="feature-row">
        <div class="feature-icon">🧪</div>
        <div class="feature-text">FSSAI certified & lab-tested for purity</div>
      </div>
      <div class="feature-row">
        <div class="feature-icon">♻️</div>
        <div class="feature-text">Eco-friendly, sustainable packaging</div>
      </div>
      <div class="feature-row">
        <div class="feature-icon">🏆</div>
        <div class="feature-text">Award-winning quality since 2005</div>
      </div>
    </div>
  </div>
</section>

<!-- PRODUCTS -->
<section class="products" id="products">
  <div class="section-eyebrow reveal">Our Range</div>
  <h2 class="reveal">Nature Bottled to Perfection</h2>
  <p class="products-sub reveal">Every variant crafted for a purpose — cooking, beauty, wellness.</p>
  <div class="products-grid">
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#FFF8E7,#F5E6B0)">🫙</div>
      <div class="product-body">
        <div class="product-tag">Bestseller</div>
        <div class="product-name">Cold Pressed Virgin Coconut Oil</div>
        <div class="product-desc">Extracted without heat to retain maximum nutrients, antioxidants, and natural coconut aroma. Ideal for cooking and skincare.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#E8F5E0,#C8E8A8)">🌿</div>
      <div class="product-body">
        <div class="product-tag">Premium</div>
        <div class="product-name">Refined Edible Coconut Oil</div>
        <div class="product-desc">Refined, bleached, and deodorized for a neutral taste and high smoke point. Perfect for everyday South Indian cooking.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#FFF0F5,#F8C8D8)">✨</div>
      <div class="product-body">
        <div class="product-tag">Beauty Range</div>
        <div class="product-name">Coconut Hair & Skin Oil</div>
        <div class="product-desc">Infused with natural herbs, our beauty oil nourishes hair from root to tip and leaves skin deeply moisturized and glowing.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#E8EFF8,#B8D0F0)">🍪</div>
      <div class="product-body">
        <div class="product-tag">Bulk Supply</div>
        <div class="product-name">Coconut Oil for Bakeries</div>
        <div class="product-desc">High-grade coconut oil specially processed for bakeries and confectioneries. Available in bulk packaging for commercial use.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#F5F0E8,#E0D0A0)">🌰</div>
      <div class="product-body">
        <div class="product-tag">Traditional</div>
        <div class="product-name">Wood-Pressed Coconut Oil</div>
        <div class="product-desc">Extracted using the ancient chekku / ghani method. Full-bodied flavour with all traditional nutrients intact.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
    <div class="product-card reveal">
      <div class="product-img" style="background:linear-gradient(135deg,#E8F8F5,#A8E8D8)">💧</div>
      <div class="product-body">
        <div class="product-tag">New Launch</div>
        <div class="product-name">Coconut Water Vinegar</div>
        <div class="product-desc">Fermented from pure coconut water, rich in probiotics. A health-boosting condiment and natural remedy for digestion.</div>
        <a href="#contact" class="product-link">Enquire Now →</a>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process" id="process">
  <div class="process-header">
    <div class="section-eyebrow reveal">How We Make It</div>
    <h2 class="reveal">From Grove to Bottle</h2>
  </div>
  <div class="process-steps">
    <div class="step reveal">
      <div class="step-num">🌴</div>
      <div class="step-title">Harvest</div>
      <div class="step-desc">Hand-picked mature coconuts from trusted organic farms across Kerala's coastal belt.</div>
    </div>
    <div class="step reveal">
      <div class="step-num">🔨</div>
      <div class="step-title">Press & Extract</div>
      <div class="step-desc">Cold-pressed or wood-pressed using traditional methods to preserve all nutrients.</div>
    </div>
    <div class="step reveal">
      <div class="step-num">🧪</div>
      <div class="step-title">Test & Filter</div>
      <div class="step-desc">Rigorous quality testing at every stage. Only the purest oil makes it through.</div>
    </div>
    <div class="step reveal">
      <div class="step-num">📦</div>
      <div class="step-title">Pack & Deliver</div>
      <div class="step-desc">Hygienically sealed in eco-friendly bottles and delivered fresh to your doorstep.</div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section class="why">
  <div class="reveal">
    <div class="section-eyebrow">Why Choose Us</div>
    <h2>The Universal Food<br>Promise</h2>
    <p>We don't just make coconut oil — we uphold a tradition of purity, quality, and care that has earned the trust of families across India for over two decades.</p>
    <a href="#contact" class="btn-primary" style="display:inline-block">Get in Touch</a>
  </div>
  <div class="why-grid reveal">
    <div class="why-item">
      <div class="why-icon">🌱</div>
      <div class="why-title">100% Natural</div>
      <div class="why-desc">No additives, preservatives, or chemicals. Just pure coconut goodness.</div>
    </div>
    <div class="why-item">
      <div class="why-icon">🏭</div>
      <div class="why-title">Modern Factory</div>
      <div class="why-desc">ISO certified facility with state-of-the-art processing equipment.</div>
    </div>
    <div class="why-item">
      <div class="why-icon">🚚</div>
      <div class="why-title">Pan-India Delivery</div>
      <div class="why-desc">Fast, reliable shipping to all major cities and towns across India.</div>
    </div>
    <div class="why-item">
      <div class="why-icon">💰</div>
      <div class="why-title">Wholesale Pricing</div>
      <div class="why-desc">Competitive rates for bulk orders. Special pricing for distributors.</div>
    </div>
    <div class="why-item">
      <div class="why-icon">📜</div>
      <div class="why-title">FSSAI Certified</div>
      <div class="why-desc">All products comply with FSSAI food safety standards.</div>
    </div>
    <div class="why-item">
      <div class="why-icon">🤝</div>
      <div class="why-title">Farmer Partnership</div>
      <div class="why-desc">Direct partnership with 200+ coconut farmers, ensuring fair trade.</div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="testimonials">
  <div class="section-eyebrow reveal">Testimonials</div>
  <h2 class="reveal">Loved Across India</h2>
  <p class="test-sub reveal">What our customers and partners say about us.</p>
  <div class="test-grid">
    <div class="test-card reveal">
      <div class="test-quote">"</div>
      <div class="stars">★★★★★</div>
      <div class="test-text">The cold pressed virgin coconut oil from Universal Food Products is exceptional. You can smell the freshness the moment you open the bottle. Nothing compares to it!</div>
      <div class="test-author">
        <div class="test-avatar">L</div>
        <div>
          <div class="test-name">Lakshmi Nair</div>
          <div class="test-role">Home Cook, Thrissur</div>
        </div>
      </div>
    </div>
    <div class="test-card reveal">
      <div class="test-quote">"</div>
      <div class="stars">★★★★★</div>
      <div class="test-text">We've been sourcing bulk coconut oil from them for our bakery chain for 3 years. Consistent quality, timely delivery, and excellent pricing. Highly recommended!</div>
      <div class="test-author">
        <div class="test-avatar">R</div>
        <div>
          <div class="test-name">Rajan Pillai</div>
          <div class="test-role">Owner, Royal Bakeries, Kochi</div>
        </div>
      </div>
    </div>
    <div class="test-card reveal">
      <div class="test-quote">"</div>
      <div class="stars">★★★★★</div>
      <div class="test-text">I use their hair oil daily — my hair has never been this healthy. I switched from branded products and I'll never go back. Pure, natural, and affordable!</div>
      <div class="test-author">
        <div class="test-avatar">P</div>
        <div>
          <div class="test-name">Priya Menon</div>
          <div class="test-role">Beauty Blogger, Trivandrum</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="reveal">
    <div class="section-eyebrow">Get In Touch</div>
    <h2>Let's Work<br>Together</h2>
    <p class="contact-intro">Whether you're a retailer, distributor, or a family looking for bulk orders — we'd love to hear from you.</p>
    <div class="contact-details">
      <div class="contact-item">
        <div class="contact-icon">📍</div>
        <div>
          <div class="contact-info-label">Address</div>
          <div class="contact-info-val">Universal Food Products, Industrial Area,<br>Ernakulam, Kerala – 682 001</div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">📞</div>
        <div>
          <div class="contact-info-label">Phone</div>
          <div class="contact-info-val">+91 98470 00000</div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">✉️</div>
        <div>
          <div class="contact-info-label">Email</div>
          <div class="contact-info-val">info@universalfoodproducts.in</div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">🕐</div>
        <div>
          <div class="contact-info-label">Working Hours</div>
          <div class="contact-info-val">Mon – Sat: 9:00 AM – 6:00 PM</div>
        </div>
      </div>
    </div>
  </div>

  <div class="contact-form reveal">
    <div class="form-row">
      <div class="form-group">
        <label>Full Name</label>
        <input type="text" placeholder="Your name">
      </div>
      <div class="form-group">
        <label>Phone</label>
        <input type="tel" placeholder="+91 XXXXX XXXXX">
      </div>
    </div>
    <div class="form-group">
      <label>Email</label>
      <input type="email" placeholder="your@email.com">
    </div>
    <div class="form-group">
      <label>Enquiry Type</label>
      <select>
        <option>Select enquiry type</option>
        <option>Retail Purchase</option>
        <option>Wholesale / Bulk Order</option>
        <option>Distributorship</option>
        <option>Export Enquiry</option>
        <option>General Query</option>
      </select>
    </div>
    <div class="form-group">
      <label>Message</label>
      <textarea placeholder="Tell us about your requirements..."></textarea>
    </div>
    <button class="btn-primary" onclick="alert('Thank you! We will contact you shortly.')">Send Enquiry</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <span class="nav-logo">Universal <span>Food</span> Products</span>
      <p>Kerala's trusted coconut oil manufacturer since 1998. Pure, natural, and crafted with care for over two decades.</p>
    </div>
    <div class="footer-col">
      <h4>Products</h4>
      <ul>
        <li><a href="#">Virgin Coconut Oil</a></li>
        <li><a href="#">Refined Edible Oil</a></li>
        <li><a href="#">Hair & Skin Oil</a></li>
        <li><a href="#">Wood Pressed Oil</a></li>
        <li><a href="#">Coconut Vinegar</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Company</h4>
      <ul>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Our Process</a></li>
        <li><a href="#">Quality Assurance</a></li>
        <li><a href="#">Careers</a></li>
        <li><a href="#">News</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Connect</h4>
      <ul>
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Instagram</a></li>
        <li><a href="#">WhatsApp</a></li>
        <li><a href="#">YouTube</a></li>
        <li><a href="#">LinkedIn</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2024 Universal Food Products. All rights reserved. | FSSAI Lic. No. 12345678901234</p>
    <p>Made with ❤️ in Kerala</p>
  </div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(el => observer.observe(el));

  // Nav scroll effect
  window.addEventListener('scroll', () => {
    const nav = document.querySelector('nav');
    nav.style.boxShadow = window.scrollY > 50 ? '0 4px 24px rgba(61,43,14,0.08)' : 'none';
  });
</script>
</body>
</html>
