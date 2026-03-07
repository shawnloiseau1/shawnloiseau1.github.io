# shawnloiseau1.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shawn Loiseau | Operations & Logistics Leader</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    /* ─── RESET & BASE ───────────────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --bg:        #080b10;
      --surface:   #0e1117;
      --card:      #141821;
      --border:    #1e2433;
      --accent:    #00c8ff;
      --accent2:   #7b5cf0;
      --text:      #f0f4ff;
      --muted:     #8895b3;
      --line:      rgba(0,200,255,.18);
      --glow:      0 0 40px rgba(0,200,255,.15);
      --radius:    14px;
      --transition: .35s cubic-bezier(.4,0,.2,1);
    }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.7;
      overflow-x: hidden;
    }

    /* ─── SCROLLBAR ──────────────────────────────────────────────── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--accent2); border-radius: 3px; }

    /* ─── NAV ────────────────────────────────────────────────────── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1.1rem 4rem;
      background: transparent;
      border-bottom: 1px solid transparent;
      transition: var(--transition);
    }
    nav.scrolled {
      background: rgba(8,11,16,.92);
      backdrop-filter: blur(18px);
      border-bottom-color: var(--border);
      box-shadow: 0 2px 40px rgba(0,0,0,.5);
    }
    .nav-logo {
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 700; font-size: 1.15rem; letter-spacing: .02em;
      color: var(--text); text-decoration: none;
    }
    .nav-logo span { color: var(--accent); }
    .nav-links { display: flex; gap: 2.2rem; list-style: none; }
    .nav-links a {
      color: var(--muted); text-decoration: none; font-size: .88rem;
      font-weight: 500; letter-spacing: .04em; text-transform: uppercase;
      transition: color var(--transition), opacity var(--transition);
    }
    .nav-links a:hover { color: var(--accent); }
    .nav-cta {
      padding: .5rem 1.3rem;
      border: 1px solid var(--accent);
      border-radius: 6px; color: var(--accent) !important;
      transition: background var(--transition) !important;
    }
    .nav-cta:hover { background: rgba(0,200,255,.1) !important; }

    /* ─── HERO ───────────────────────────────────────────────────── */
    .hero {
      position: relative; min-height: 100vh;
      display: flex; align-items: center;
      overflow: hidden;
    }
    .hero-bg {
      position: absolute; inset: 0;
      background: url('Websitephotos/IMG_1950.JPEG') center/cover no-repeat;
      transform: scale(1.05);
      transition: transform 12s ease;
    }
    .hero-bg::after {
      content: '';
      position: absolute; inset: 0;
      background: linear-gradient(
        135deg,
        rgba(8,11,16,.92) 0%,
        rgba(8,11,16,.7) 50%,
        rgba(8,11,16,.85) 100%
      );
    }
    .hero-content {
      position: relative; z-index: 2;
      padding: 0 4rem;
      max-width: 900px;
    }
    .hero-eyebrow {
      display: inline-flex; align-items: center; gap: .6rem;
      font-size: .78rem; font-weight: 600; letter-spacing: .12em;
      text-transform: uppercase; color: var(--accent);
      margin-bottom: 1.5rem;
    }
    .hero-eyebrow::before {
      content: ''; display: block;
      width: 28px; height: 2px;
      background: var(--accent);
    }
    h1 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(3rem, 7vw, 5.5rem);
      font-weight: 800; line-height: 1.05;
      letter-spacing: -.02em; margin-bottom: 1.2rem;
    }
    h1 span { color: var(--accent); }
    .hero-subtitle {
      font-size: clamp(1.05rem, 2vw, 1.3rem);
      color: var(--muted); max-width: 580px;
      margin-bottom: 2.4rem; font-weight: 400;
    }
    .hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }
    .btn {
      display: inline-flex; align-items: center; gap: .5rem;
      padding: .85rem 2rem; border-radius: 8px;
      font-size: .9rem; font-weight: 600; cursor: pointer;
      text-decoration: none; transition: var(--transition);
      letter-spacing: .02em;
    }
    .btn-primary {
      background: var(--accent); color: var(--bg);
      box-shadow: 0 0 28px rgba(0,200,255,.35);
    }
    .btn-primary:hover {
      background: #33d4ff;
      box-shadow: 0 0 42px rgba(0,200,255,.55);
      transform: translateY(-2px);
    }
    .btn-outline {
      background: transparent;
      border: 1px solid var(--border);
      color: var(--text);
    }
    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-2px);
    }
    .hero-stats {
      position: absolute; bottom: 2.5rem; right: 4rem; z-index: 2;
      display: flex; gap: 3rem;
    }
    .stat { text-align: center; }
    .stat-number {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2.2rem; font-weight: 700;
      color: var(--accent); line-height: 1;
    }
    .stat-label { font-size: .72rem; letter-spacing: .1em; text-transform: uppercase; color: var(--muted); margin-top: .3rem; }

    /* ─── SECTION COMMON ─────────────────────────────────────────── */
    section { padding: 6rem 4rem; }
    .section-label {
      display: inline-flex; align-items: center; gap: .6rem;
      font-size: .72rem; font-weight: 700; letter-spacing: .14em;
      text-transform: uppercase; color: var(--accent);
      margin-bottom: .8rem;
    }
    .section-label::before {
      content: ''; display: block;
      width: 20px; height: 2px; background: var(--accent);
    }
    h2 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(1.9rem, 4vw, 2.8rem);
      font-weight: 700; letter-spacing: -.02em;
      line-height: 1.15; margin-bottom: 1rem;
    }
    .section-intro { color: var(--muted); max-width: 620px; font-size: 1.05rem; }

    /* ─── ABOUT ──────────────────────────────────────────────────── */
    #about { background: var(--surface); }
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem; align-items: center;
      margin-top: 3.5rem;
    }
    .about-text p { color: var(--muted); font-size: 1rem; margin-bottom: 1.1rem; }
    .about-text p strong { color: var(--text); font-weight: 600; }
    .about-highlights {
      display: grid; grid-template-columns: 1fr 1fr; gap: 1.2rem;
      margin-top: 2rem;
    }
    .highlight-item {
      padding: 1.2rem 1.4rem;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      transition: var(--transition);
    }
    .highlight-item:hover {
      border-color: var(--accent);
      box-shadow: var(--glow);
      transform: translateY(-3px);
    }
    .highlight-icon { font-size: 1.4rem; margin-bottom: .5rem; }
    .highlight-title { font-size: .82rem; font-weight: 600; color: var(--text); }
    .highlight-desc { font-size: .78rem; color: var(--muted); margin-top: .2rem; }
    .about-image-stack { position: relative; }
    .about-img-main {
      width: 100%; border-radius: var(--radius);
      object-fit: cover; height: 420px;
      border: 1px solid var(--border);
      box-shadow: 0 20px 60px rgba(0,0,0,.5);
    }
    .about-img-badge {
      position: absolute; bottom: -1.5rem; left: -1.5rem;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 1.1rem 1.5rem;
      box-shadow: 0 12px 40px rgba(0,0,0,.4);
    }
    .badge-number {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2rem; font-weight: 700; color: var(--accent); line-height: 1;
    }
    .badge-text { font-size: .75rem; color: var(--muted); margin-top: .2rem; }

    /* ─── EXPERIENCE ─────────────────────────────────────────────── */
    #experience { background: var(--bg); }
    .timeline { margin-top: 3.5rem; position: relative; padding-left: 2rem; }
    .timeline::before {
      content: ''; position: absolute;
      left: 0; top: .5rem; bottom: .5rem; width: 1px;
      background: linear-gradient(to bottom, var(--accent), var(--accent2), transparent);
    }
    .timeline-item {
      position: relative; padding: 0 0 3.5rem 2.5rem;
    }
    .timeline-item:last-child { padding-bottom: 0; }
    .timeline-dot {
      position: absolute; left: -2.05rem; top: .4rem;
      width: .85rem; height: .85rem; border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 12px var(--accent);
      border: 2px solid var(--bg);
    }
    .timeline-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 2rem 2.2rem;
      transition: var(--transition);
    }
    .timeline-card:hover {
      border-color: var(--accent);
      box-shadow: var(--glow);
      transform: translateX(4px);
    }
    .job-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: .8rem; margin-bottom: 1.2rem; }
    .job-title {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.18rem; font-weight: 700; color: var(--text);
    }
    .job-company { font-size: .88rem; color: var(--accent); font-weight: 500; margin-top: .2rem; }
    .job-location { font-size: .78rem; color: var(--muted); }
    .job-date {
      font-size: .78rem; font-weight: 600; letter-spacing: .06em;
      text-transform: uppercase; color: var(--muted);
      background: var(--surface);
      border: 1px solid var(--border);
      padding: .3rem .9rem; border-radius: 20px;
      white-space: nowrap;
    }
    .job-bullets { list-style: none; display: flex; flex-direction: column; gap: .85rem; }
    .job-bullets li {
      display: flex; gap: .8rem; font-size: .93rem; color: var(--muted);
    }
    .job-bullets li::before {
      content: '▹'; color: var(--accent);
      flex-shrink: 0; margin-top: .05rem;
    }
    .job-bullets li strong { color: var(--text); font-weight: 600; }

    /* ─── SKILLS ─────────────────────────────────────────────────── */
    #skills { background: var(--surface); }
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
      gap: 1.2rem;
      margin-top: 3.5rem;
    }
    .skill-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 1.6rem 1.8rem;
      transition: var(--transition);
      position: relative; overflow: hidden;
    }
    .skill-card::before {
      content: ''; position: absolute;
      top: 0; left: 0; right: 0; height: 2px;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      transform: scaleX(0); transform-origin: left;
      transition: transform var(--transition);
    }
    .skill-card:hover::before { transform: scaleX(1); }
    .skill-card:hover {
      border-color: rgba(0,200,255,.3);
      transform: translateY(-4px);
      box-shadow: 0 12px 40px rgba(0,0,0,.4);
    }
    .skill-icon { font-size: 1.8rem; margin-bottom: .8rem; }
    .skill-name { font-size: .95rem; font-weight: 600; color: var(--text); margin-bottom: .3rem; }
    .skill-desc { font-size: .8rem; color: var(--muted); }

    /* ─── GALLERY ────────────────────────────────────────────────── */
    #gallery { background: var(--bg); }
    .gallery-intro { margin-bottom: 3rem; }
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: auto;
      gap: 1rem;
    }
    .gallery-item {
      position: relative; overflow: hidden;
      border-radius: var(--radius);
      border: 1px solid var(--border);
      cursor: pointer;
      background: var(--card);
    }
    .gallery-item:first-child {
      grid-column: span 2;
    }
    .gallery-item img {
      width: 100%; height: 280px;
      object-fit: cover;
      display: block;
      transition: transform .6s cubic-bezier(.4,0,.2,1);
    }
    .gallery-item:first-child img { height: 360px; }
    .gallery-item:hover img { transform: scale(1.06); }
    .gallery-overlay {
      position: absolute; inset: 0;
      background: linear-gradient(
        to top,
        rgba(8,11,16,.9) 0%,
        rgba(8,11,16,.2) 60%,
        transparent 100%
      );
      opacity: 0; transition: opacity var(--transition);
      display: flex; align-items: flex-end;
      padding: 1.4rem;
    }
    .gallery-item:hover .gallery-overlay { opacity: 1; }
    .gallery-caption {
      font-size: .82rem; font-weight: 500;
      color: var(--text); line-height: 1.4;
    }
    .gallery-caption span { color: var(--accent); font-weight: 600; display: block; font-size: .72rem; letter-spacing: .08em; text-transform: uppercase; }

    /* ─── EDUCATION ──────────────────────────────────────────────── */
    #education { background: var(--surface); }
    .edu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.2rem; margin-top: 3rem;
    }
    .edu-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 1.8rem 2rem;
      transition: var(--transition);
    }
    .edu-card:hover {
      border-color: var(--accent2);
      box-shadow: 0 0 40px rgba(123,92,240,.15);
      transform: translateY(-3px);
    }
    .edu-icon { font-size: 2rem; margin-bottom: 1rem; }
    .edu-title { font-size: 1rem; font-weight: 700; color: var(--text); margin-bottom: .3rem; }
    .edu-org { font-size: .85rem; color: var(--accent); margin-bottom: .2rem; }
    .edu-detail { font-size: .8rem; color: var(--muted); }

    /* ─── CONTACT ────────────────────────────────────────────────── */
    #contact { background: var(--bg); }
    .contact-wrapper {
      margin-top: 3.5rem;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: calc(var(--radius) * 1.5);
      overflow: hidden;
      display: grid; grid-template-columns: 1fr 1fr;
    }
    .contact-info {
      padding: 3.5rem;
      background: linear-gradient(135deg, rgba(0,200,255,.06), rgba(123,92,240,.08));
      border-right: 1px solid var(--border);
    }
    .contact-info h3 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.6rem; font-weight: 700; margin-bottom: .8rem;
    }
    .contact-info p { color: var(--muted); font-size: .95rem; margin-bottom: 2rem; }
    .contact-item {
      display: flex; align-items: center; gap: 1rem;
      padding: 1rem 1.2rem;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      margin-bottom: .8rem;
      transition: var(--transition);
    }
    .contact-item:hover {
      border-color: var(--accent);
      transform: translateX(4px);
    }
    .contact-icon {
      width: 38px; height: 38px;
      border-radius: 8px;
      background: rgba(0,200,255,.1);
      border: 1px solid rgba(0,200,255,.2);
      display: flex; align-items: center; justify-content: center;
      font-size: 1rem; flex-shrink: 0;
    }
    .contact-label { font-size: .72rem; text-transform: uppercase; letter-spacing: .08em; color: var(--muted); }
    .contact-value { font-size: .92rem; font-weight: 500; color: var(--text); }
    .contact-right {
      padding: 3.5rem;
      display: flex; flex-direction: column; justify-content: center; align-items: flex-start;
      gap: 1rem;
    }
    .contact-right h3 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.4rem; font-weight: 700; margin-bottom: .4rem;
    }
    .contact-right p { color: var(--muted); font-size: .92rem; margin-bottom: 1.2rem; }
    .availability-badge {
      display: inline-flex; align-items: center; gap: .5rem;
      padding: .5rem 1.1rem;
      background: rgba(0,200,255,.08);
      border: 1px solid rgba(0,200,255,.25);
      border-radius: 20px;
      font-size: .8rem; font-weight: 600; color: var(--accent);
      margin-bottom: 1.5rem;
    }
    .availability-badge::before {
      content: '';
      width: 7px; height: 7px; border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 8px var(--accent);
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: .3; }
    }

    /* ─── FOOTER ─────────────────────────────────────────────────── */
    footer {
      background: var(--surface);
      border-top: 1px solid var(--border);
      padding: 2rem 4rem;
      display: flex; justify-content: space-between; align-items: center;
      flex-wrap: wrap; gap: 1rem;
    }
    footer p { font-size: .82rem; color: var(--muted); }
    footer span { color: var(--accent); }

    /* ─── LIGHTBOX ───────────────────────────────────────────────── */
    .lightbox {
      display: none; position: fixed; inset: 0; z-index: 999;
      background: rgba(0,0,0,.92);
      align-items: center; justify-content: center;
      backdrop-filter: blur(10px);
    }
    .lightbox.open { display: flex; }
    .lightbox img {
      max-width: 90vw; max-height: 88vh;
      border-radius: var(--radius);
      box-shadow: 0 0 80px rgba(0,0,0,.8);
    }
    .lightbox-close {
      position: fixed; top: 1.5rem; right: 2rem;
      font-size: 2rem; color: var(--muted); cursor: pointer;
      transition: color var(--transition); background: none; border: none;
    }
    .lightbox-close:hover { color: var(--accent); }

    /* ─── REVEAL ANIMATIONS ──────────────────────────────────────── */
    .reveal {
      opacity: 0; transform: translateY(28px);
      transition: opacity .65s ease, transform .65s ease;
    }
    .reveal.visible { opacity: 1; transform: none; }

    /* ─── RESPONSIVE ─────────────────────────────────────────────── */
    @media (max-width: 1024px) {
      nav { padding: 1rem 2rem; }
      .nav-links { gap: 1.4rem; }
      section { padding: 5rem 2.5rem; }
      .about-grid { grid-template-columns: 1fr; gap: 3rem; }
      .about-image-stack { order: -1; }
      .contact-wrapper { grid-template-columns: 1fr; }
      .contact-info { border-right: none; border-bottom: 1px solid var(--border); }
      footer { padding: 2rem; }
    }
    @media (max-width: 768px) {
      nav { padding: .9rem 1.5rem; }
      .nav-links { display: none; }
      .hero-content { padding: 0 1.5rem; }
      .hero-stats { display: none; }
      section { padding: 4rem 1.5rem; }
      h1 { font-size: 2.6rem; }
      .gallery-grid { grid-template-columns: 1fr; }
      .gallery-item:first-child { grid-column: span 1; }
      .gallery-item img, .gallery-item:first-child img { height: 240px; }
      footer { padding: 1.5rem; flex-direction: column; text-align: center; }
    }
  </style>
</head>
<body>

  <!-- ─── NAV ───────────────────────────────────────────────────── -->
  <nav id="navbar">
    <a href="#" class="nav-logo">S.<span>L</span></a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#gallery">Portfolio</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#contact" class="nav-cta">Contact</a></li>
    </ul>
  </nav>

  <!-- ─── HERO ──────────────────────────────────────────────────── -->
  <section class="hero" id="home">
    <div class="hero-bg" id="heroBg"></div>
    <div class="hero-content">
      <div class="hero-eyebrow">Operations &amp; Logistics Leader</div>
      <h1>Shawn<br /><span>Loiseau</span></h1>
      <p class="hero-subtitle">
        10+ years driving operational excellence across fitness technology,
        logistics, P&amp;L management, and elite team leadership.
      </p>
      <div class="hero-actions">
        <a href="#experience" class="btn btn-primary">View Experience</a>
        <a href="#contact" class="btn btn-outline">Get In Touch</a>
      </div>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-number">10+</div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat">
        <div class="stat-number">4</div>
        <div class="stat-label">Major Roles</div>
      </div>
      <div class="stat">
        <div class="stat-number">3</div>
        <div class="stat-label">Premium Brands</div>
      </div>
    </div>
  </section>

  <!-- ─── ABOUT ─────────────────────────────────────────────────── -->
  <section id="about">
    <div class="reveal">
      <div class="section-label">About Me</div>
      <h2>Built on Precision,<br />Driven by Results</h2>
    </div>
    <div class="about-grid">
      <div class="about-text reveal">
        <p>
          <strong>Results-driven Operations and Logistics Leader</strong> with over 10 years of
          progressive experience spanning the fitness industry — including high-end equipment
          installation, technical training, consultative sales, and comprehensive operational
          management with full P&amp;L oversight.
        </p>
        <p>
          Critical technical proficiency in maintaining and quality-assuring commercial fitness
          technology from premium brands like <strong>Technogym, Life Fitness, and Precor</strong>.
          Expert in leading teams, ensuring <strong>DOT and safety compliance</strong>, and
          optimizing facility performance to deliver a reliable, premium, resort-style
          member experience.
        </p>
        <p>
          Bilingual in <strong>English and Spanish</strong>, with proven ability to communicate
          effectively across all levels of an organization and with diverse client bases.
        </p>
        <div class="about-highlights">
          <div class="highlight-item">
            <div class="highlight-icon">&#9881;</div>
            <div class="highlight-title">P&amp;L Oversight</div>
            <div class="highlight-desc">Full financial performance management</div>
          </div>
          <div class="highlight-item">
            <div class="highlight-icon">&#128200;</div>
            <div class="highlight-title">KPI Tracking</div>
            <div class="highlight-desc">Scorecard &amp; performance metrics</div>
          </div>
          <div class="highlight-item">
            <div class="highlight-icon">&#128101;</div>
            <div class="highlight-title">Team Leadership</div>
            <div class="highlight-desc">Training, onboarding &amp; retention</div>
          </div>
          <div class="highlight-item">
            <div class="highlight-icon">&#9989;</div>
            <div class="highlight-title">Quality Assurance</div>
            <div class="highlight-desc">In-process &amp; final QC protocols</div>
          </div>
        </div>
      </div>
      <div class="about-image-stack reveal">
        <img
          src="Websitephotos/IMG_0754.JPEG"
          alt="Technogym dumbbell installation — Life Time Fitness"
          class="about-img-main"
        />
        <div class="about-img-badge">
          <div class="badge-number">10+</div>
          <div class="badge-text">Years in the Field</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── EXPERIENCE ────────────────────────────────────────────── -->
  <section id="experience">
    <div class="reveal">
      <div class="section-label">Work History</div>
      <h2>Key Experience</h2>
      <p class="section-intro">A track record of leadership, technical expertise, and measurable impact across top-tier organizations.</p>
    </div>
    <div class="timeline">

      <div class="timeline-item reveal">
        <div class="timeline-dot"></div>
        <div class="timeline-card">
          <div class="job-header">
            <div>
              <div class="job-title">Sales Associate, Wellness Consulting</div>
              <div class="job-company">Vitamin World</div>
              <div class="job-location">Rosemont, IL</div>
            </div>
            <div class="job-date">Nov 2023 — Present</div>
          </div>
          <ul class="job-bullets">
            <li><strong>Consultative Sales:</strong> Consistently provided exceptional customer service as a wellness consultant, offering personalized product recommendations to maximize sales and meet individual customer needs.</li>
            <li><strong>Retail Operations:</strong> Managed inventory, stocked shelves, and maintained organization and visual display of the sales floor to enhance the customer shopping experience.</li>
          </ul>
        </div>
      </div>

      <div class="timeline-item reveal">
        <div class="timeline-dot" style="background: var(--accent2); box-shadow: 0 0 12px var(--accent2);"></div>
        <div class="timeline-card">
          <div class="job-header">
            <div>
              <div class="job-title">Manager, Operational Excellence</div>
              <div class="job-company">J.B. Hunt</div>
              <div class="job-location">Melrose Park, IL</div>
            </div>
            <div class="job-date">May 2022 — Jun 2023</div>
          </div>
          <ul class="job-bullets">
            <li><strong>Operational &amp; Financial Oversight:</strong> Responsible for complete P&amp;L performance, including cost control decisions, expense management, and maximizing profitability for assigned operations.</li>
            <li><strong>Process Optimization:</strong> Trained, audited, and improved standard operating procedures to enhance daily proficiency and streamline workflow processes.</li>
            <li><strong>Leadership &amp; Compliance:</strong> Oversaw all aspects of operations, focusing on safety, compliance, employee scorecard management, and driver retention.</li>
          </ul>
        </div>
      </div>

      <div class="timeline-item reveal">
        <div class="timeline-dot"></div>
        <div class="timeline-card">
          <div class="job-header">
            <div>
              <div class="job-title">Lead Trainer &amp; Fitness Technology Specialist</div>
              <div class="job-company">Mass Movement Inc. / J.B. Hunt</div>
              <div class="job-location">Melrose Park, IL</div>
            </div>
            <div class="job-date">Aug 2019 — May 2022</div>
          </div>
          <ul class="job-bullets">
            <li><strong>Expert Equipment Training:</strong> Developed and implemented comprehensive training programs for technical staff on the assembly, installation, and SOPs for high-end fitness equipment — Technogym, Life Fitness, Precor, and Stages.</li>
            <li><strong>Quality Assurance:</strong> Led quality control protocols, testing gym equipment at all stages of production to ensure strict conformity to manufacturer specifications, directly impacting user safety and product reliability.</li>
            <li><strong>Process Improvement:</strong> Implemented continual education programs, significantly reducing installation errors and improving the efficiency of field service teams.</li>
          </ul>
        </div>
      </div>

      <div class="timeline-item reveal">
        <div class="timeline-dot" style="background: var(--accent2); box-shadow: 0 0 12px var(--accent2);"></div>
        <div class="timeline-card">
          <div class="job-header">
            <div>
              <div class="job-title">Installation &amp; Quality Control Lead</div>
              <div class="job-company">Mass Movement Inc. / J.B. Hunt</div>
              <div class="job-location">Melrose Park, IL</div>
            </div>
            <div class="job-date">Sep 2017 — Aug 2019</div>
          </div>
          <ul class="job-bullets">
            <li><strong>Field Management:</strong> Directed 4–5 member installation teams as the primary onsite customer contact, coordinating and resolving all installation and delivery issues through to completion.</li>
            <li><strong>Technical Assembly:</strong> Led the proper assembly, functional testing, and installation of complex gym equipment per manufacturer specifications and local codes — ensuring zero damage to product and customer locations.</li>
            <li><strong>Safety &amp; Logistics:</strong> Ensured safe, secure, and timely transportation of high-value goods, adhering to DOT and strict internal safety compliance standards.</li>
          </ul>
        </div>
      </div>

    </div>
  </section>

  <!-- ─── SKILLS ────────────────────────────────────────────────── -->
  <section id="skills">
    <div class="reveal">
      <div class="section-label">Capabilities</div>
      <h2>Skills &amp; Expertise</h2>
    </div>
    <div class="skills-grid">
      <div class="skill-card reveal">
        <div class="skill-icon">&#128200;</div>
        <div class="skill-name">Operational Management</div>
        <div class="skill-desc">P&amp;L oversight, KPI tracking, and full operational performance ownership</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#9881;</div>
        <div class="skill-name">Fitness Equipment Technology</div>
        <div class="skill-desc">Maintenance, QC, and installation for Technogym, Life Fitness &amp; Precor</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#128172;</div>
        <div class="skill-name">Consultative Sales</div>
        <div class="skill-desc">Customer-first approach to sales with personalized recommendations</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#128101;</div>
        <div class="skill-name">Team Leadership &amp; Training</div>
        <div class="skill-desc">Onboarding, coaching, retention, and field team management</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#9989;</div>
        <div class="skill-name">Quality Control &amp; Assurance</div>
        <div class="skill-desc">In-process and final QC protocols against manufacturer specifications</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#127760;</div>
        <div class="skill-name">Bilingual — English &amp; Spanish</div>
        <div class="skill-desc">Full professional proficiency in both languages</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#128667;</div>
        <div class="skill-name">DOT Compliance &amp; Safety</div>
        <div class="skill-desc">Transportation safety, Non-CDL Class C, and regulatory adherence</div>
      </div>
      <div class="skill-card reveal">
        <div class="skill-icon">&#128260;</div>
        <div class="skill-name">Process Optimization</div>
        <div class="skill-desc">SOP development, auditing, and continual improvement programs</div>
      </div>
    </div>
  </section>

  <!-- ─── GALLERY ───────────────────────────────────────────────── -->
  <section id="gallery">
    <div class="reveal gallery-intro">
      <div class="section-label">Portfolio</div>
      <h2>Work in the Field</h2>
      <p class="section-intro">A selection of commercial fitness facility installations showcasing technical expertise across premium brands and venues.</p>
    </div>
    <div class="gallery-grid">
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_1950.JPEG')">
        <img src="Websitephotos/IMG_1950.JPEG" alt="Technogym treadmills — Life Time Fitness" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Technogym &bull; Life Time Fitness</span>
            Treadmill row installation &amp; alignment
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0861.JPEG')">
        <img src="Websitephotos/IMG_0861.JPEG" alt="Functional training rig installation" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Functional Training Rig</span>
            Multi-station cable system setup
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0754.JPEG')">
        <img src="Websitephotos/IMG_0754.JPEG" alt="Technogym dumbbell racks — Life Time Fitness" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Technogym &bull; Life Time Fitness</span>
            Dumbbell rack installation &amp; staging
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0634.JPEG')">
        <img src="Websitephotos/IMG_0634.JPEG" alt="TRX suspension trainers and stability equipment" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Suspension &amp; Functional Training</span>
            TRX &amp; stability station configuration
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0637.JPEG')">
        <img src="Websitephotos/IMG_0637.JPEG" alt="WaterRower concept2 rowing machines" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Cardio Suite</span>
            Rowing machine installation &amp; QC
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0576.JPEG')">
        <img src="Websitephotos/IMG_0576.JPEG" alt="Hammer Strength squat racks with lifting platforms" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Hammer Strength</span>
            Power rack &amp; platform installation
          </div>
        </div>
      </div>
      <div class="gallery-item reveal" onclick="openLightbox('Websitephotos/IMG_0500.JPEG')">
        <img src="Websitephotos/IMG_0500.JPEG" alt="Life Fitness and Cybex strength machines" loading="lazy" />
        <div class="gallery-overlay">
          <div class="gallery-caption">
            <span>Life Fitness &bull; Cybex</span>
            Selectorized strength equipment setup
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── EDUCATION ─────────────────────────────────────────────── -->
  <section id="education">
    <div class="reveal">
      <div class="section-label">Education &amp; Credentials</div>
      <h2>Qualifications</h2>
    </div>
    <div class="edu-grid">
      <div class="edu-card reveal">
        <div class="edu-icon">&#127891;</div>
        <div class="edu-title">GED</div>
        <div class="edu-org">Timothy Christian High School</div>
        <div class="edu-detail">Elmhurst, IL &mdash; January 2009</div>
      </div>
      <div class="edu-card reveal">
        <div class="edu-icon">&#128667;</div>
        <div class="edu-title">Non-CDL Class C</div>
        <div class="edu-org">Commercial Driver License</div>
        <div class="edu-detail">DOT compliance &amp; safety certified</div>
      </div>
      <div class="edu-card reveal">
        <div class="edu-icon">&#127760;</div>
        <div class="edu-title">Bilingual</div>
        <div class="edu-org">English &amp; Spanish</div>
        <div class="edu-detail">Full professional proficiency</div>
      </div>
      <div class="edu-card reveal">
        <div class="edu-icon">&#9881;</div>
        <div class="edu-title">Fitness Tech Specialist</div>
        <div class="edu-org">Technogym &bull; Life Fitness &bull; Precor</div>
        <div class="edu-detail">Assembly, installation &amp; QC certification</div>
      </div>
    </div>
  </section>

  <!-- ─── CONTACT ───────────────────────────────────────────────── -->
  <section id="contact">
    <div class="reveal">
      <div class="section-label">Get In Touch</div>
      <h2>Let's Connect</h2>
    </div>
    <div class="contact-wrapper reveal" style="grid-template-columns: 1fr;">
      <div class="contact-right" style="padding: 3.5rem; align-items: center; text-align: center;">
        <div class="availability-badge">Available for New Opportunities</div>
        <h3>Ready to Make an Impact</h3>
        <p>With 10+ years of hands-on experience in operations, logistics, and fitness technology, I bring both strategic leadership and ground-level expertise to every role.</p>
        <a href="mailto:shawn.loiseau1@gmail.com" class="btn btn-primary">Send an Email</a>
      </div>
    </div>
  </section>

  <!-- ─── FOOTER ────────────────────────────────────────────────── -->
  <footer>
    <p>&copy; 2025 <span>Shawn Loiseau</span>. All rights reserved.</p>
  </footer>

  <!-- ─── LIGHTBOX ──────────────────────────────────────────────── -->
  <div class="lightbox" id="lightbox" onclick="closeLightbox()">
    <button class="lightbox-close" onclick="closeLightbox()">&times;</button>
    <img id="lightboxImg" src="" alt="" />
  </div>

  <!-- ─── SCRIPTS ───────────────────────────────────────────────── -->
  <script>
    // Nav scroll
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
      navbar.classList.toggle('scrolled', window.scrollY > 60);
    });

    // Parallax hero bg
    const heroBg = document.getElementById('heroBg');
    window.addEventListener('scroll', () => {
      const y = window.scrollY;
      heroBg.style.transform = `scale(1.05) translateY(${y * 0.25}px)`;
    });

    // Reveal on scroll
    const observer = new IntersectionObserver(
      (entries) => entries.forEach(e => {
        if (e.isIntersecting) { e.target.classList.add('visible'); observer.unobserve(e.target); }
      }),
      { threshold: 0.12 }
    );
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    // Stagger children reveals inside grids
    document.querySelectorAll('.skills-grid, .gallery-grid, .edu-grid, .about-highlights').forEach(grid => {
      grid.querySelectorAll('.reveal').forEach((el, i) => {
        el.style.transitionDelay = `${i * 0.08}s`;
      });
    });

    // Lightbox
    function openLightbox(src) {
      document.getElementById('lightboxImg').src = src;
      document.getElementById('lightbox').classList.add('open');
      document.body.style.overflow = 'hidden';
    }
    function closeLightbox() {
      document.getElementById('lightbox').classList.remove('open');
      document.body.style.overflow = '';
    }
    document.addEventListener('keydown', e => { if (e.key === 'Escape') closeLightbox(); });
  </script>
</body>
</html>
