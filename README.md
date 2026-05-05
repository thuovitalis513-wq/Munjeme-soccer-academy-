# Munjeme-soccer-academy-
Professional 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Munjeme Soccer Academy</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow:wght@300;400;600;700&family=Barlow+Condensed:wght@700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0D1B3E;
    --navy-dark: #080F23;
    --navy-mid: #112248;
    --navy-card: #0f1e40;
    --gold: #F5C518;
    --gold-dark: #C49A0A;
    --teal: #1A6B5A;
    --white: #F5F5F0;
    --muted: #7a8aaa;
  }
  * { margin:0; padding:0; box-sizing:border-box; }
  body { font-family:'Barlow',sans-serif; background:var(--navy-dark); color:var(--white); overflow-x:hidden; }

  /* ── NAV ── */
  nav {
    position:fixed; top:0; width:100%; z-index:100;
    display:flex; align-items:center; justify-content:space-between;
    padding:0 5%; height:72px;
    background:rgba(8,15,35,0.97);
    backdrop-filter:blur(14px);
    border-bottom:2px solid rgba(245,197,24,0.25);
  }
  .nav-logo { display:flex; align-items:center; gap:12px; text-decoration:none; }
  .nav-logo img { height:52px; width:auto; object-fit:contain; }
  .nav-logo-text { font-family:'Bebas Neue',sans-serif; font-size:1.25rem; letter-spacing:2px; color:var(--white); line-height:1.1; }
  .nav-logo-text span { color:var(--gold); display:block; font-size:0.68rem; letter-spacing:4px; font-family:'Barlow',sans-serif; font-weight:600; }
  .nav-links { display:flex; gap:2rem; list-style:none; }
  .nav-links a { color:var(--muted); text-decoration:none; font-size:0.82rem; letter-spacing:1.5px; text-transform:uppercase; font-weight:600; transition:color .2s; }
  .nav-links a:hover { color:var(--gold); }
  .nav-cta { background:var(--gold); color:var(--navy-dark); padding:9px 22px; border-radius:2px; font-weight:700; font-size:0.8rem; letter-spacing:1px; text-transform:uppercase; border:none; cursor:pointer; transition:background .2s,transform .2s; font-family:'Barlow Condensed',sans-serif; }
  .nav-cta:hover { background:#fff; transform:translateY(-1px); }

  /* ── HERO ── */
  .hero { min-height:100vh; display:flex; flex-direction:column; justify-content:center; align-items:flex-start; padding:0 8%; position:relative; overflow:hidden; }
  .hero-bg { position:absolute; inset:0; background: radial-gradient(ellipse 70% 60% at 75% 45%, rgba(26,107,90,0.22) 0%,transparent 65%), radial-gradient(ellipse 50% 50% at 15% 75%, rgba(245,197,24,0.07) 0%,transparent 60%), var(--navy-dark); }
  .hero-pattern { position:absolute; inset:0; background-image: repeating-linear-gradient(0deg,transparent,transparent 59px,rgba(245,197,24,0.03) 60px), repeating-linear-gradient(90deg,transparent,transparent 59px,rgba(245,197,24,0.03) 60px); pointer-events:none; }
  .hero-shield { position:absolute; right:3%; top:50%; transform:translateY(-50%); opacity:0.035; z-index:0; pointer-events:none; }
  .hero-badge { font-family:'Barlow Condensed',sans-serif; font-size:0.78rem; letter-spacing:4px; text-transform:uppercase; color:var(--gold); background:rgba(245,197,24,0.1); border:1px solid rgba(245,197,24,0.35); padding:6px 18px; border-radius:100px; margin-bottom:1.5rem; position:relative; z-index:1; animation:fadeUp .7s ease both; display:flex; align-items:center; gap:10px; }
  .hero-badge img { height:26px; width:auto; }
  .hero h1 { font-family:'Bebas Neue',sans-serif; font-size:clamp(3.5rem,10vw,9rem); line-height:.9; letter-spacing:2px; position:relative; z-index:1; animation:fadeUp .7s .15s ease both; }
  .hero h1 .line-gold { color:var(--gold); display:block; }
  .hero-sub { margin-top:1.5rem; font-size:1.05rem; color:var(--muted); max-width:480px; line-height:1.7; position:relative; z-index:1; animation:fadeUp .7s .3s ease both; }
  .hero-actions { margin-top:2.5rem; display:flex; gap:1rem; flex-wrap:wrap; position:relative; z-index:1; animation:fadeUp .7s .45s ease both; }
  .btn-primary { background:var(--gold); color:var(--navy-dark); padding:14px 36px; border:none; border-radius:2px; font-family:'Barlow Condensed',sans-serif; font-size:1rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; cursor:pointer; transition:all .2s; }
  .btn-primary:hover { background:#fff; transform:translateY(-2px); }
  .btn-ghost { background:transparent; color:var(--white); padding:14px 36px; border:1px solid rgba(255,255,255,.2); border-radius:2px; font-family:'Barlow Condensed',sans-serif; font-size:1rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; cursor:pointer; transition:all .2s; }
  .btn-ghost:hover { border-color:var(--gold); color:var(--gold); }
  .hero-stats { position:absolute; right:8%; bottom:12%; display:flex; gap:3rem; animation:fadeUp .7s .6s ease both; z-index:1; }
  .stat { text-align:center; }
  .stat-num { font-family:'Bebas Neue',sans-serif; font-size:3rem; color:var(--gold); line-height:1; }
  .stat-label { font-size:0.72rem; color:var(--muted); letter-spacing:1px; text-transform:uppercase; }

  /* ── SECTION HEADER ── */
  .section-header { text-align:center; padding:0 5% 3rem; }
  .section-tag { font-family:'Barlow Condensed',sans-serif; font-size:0.75rem; letter-spacing:4px; text-transform:uppercase; color:var(--gold); display:block; margin-bottom:.8rem; }
  .section-title { font-family:'Bebas Neue',sans-serif; font-size:clamp(2.5rem,5vw,4rem); letter-spacing:2px; }

  /* ── TEAMS ── */
  #teams { padding:100px 5%; background:var(--navy-dark); }
  .teams-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(300px,1fr)); gap:2px; background:rgba(245,197,24,0.07); border:1px solid rgba(245,197,24,0.07); }
  .team-card { background:var(--navy-card); position:relative; overflow:hidden; cursor:pointer; transition:transform .3s,box-shadow .3s; }
  .team-card:hover { transform:translateY(-6px); box-shadow:0 20px 60px rgba(245,197,24,0.12); z-index:2; }
  .team-card:hover .card-overlay { opacity:1; }
  .card-img-wrap { width:100%; height:240px; background:var(--navy-mid); position:relative; overflow:hidden; }
  .card-img-wrap img { width:100%; height:100%; object-fit:cover; transition:transform .5s; display:block; }
  .team-card:hover .card-img-wrap img { transform:scale(1.06); }
  .card-placeholder { width:100%; height:100%; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:.5rem; background:linear-gradient(135deg,#0a1428,#0f1e3a); }
  .card-placeholder svg { opacity:.18; }
  .card-placeholder span { font-size:.72rem; color:var(--muted); letter-spacing:2px; text-transform:uppercase; }
  .card-age-badge { position:absolute; top:14px; left:14px; background:var(--gold); color:var(--navy-dark); font-family:'Barlow Condensed',sans-serif; font-size:.78rem; font-weight:900; letter-spacing:1px; padding:4px 12px; text-transform:uppercase; }
  .card-body { padding:1.5rem; }
  .card-category { font-size:.68rem; letter-spacing:3px; color:var(--gold); text-transform:uppercase; font-weight:600; margin-bottom:.4rem; }
  .card-name { font-family:'Barlow Condensed',sans-serif; font-size:1.5rem; font-weight:900; line-height:1.1; margin-bottom:.6rem; }
  .card-desc { font-size:.86rem; color:var(--muted); line-height:1.6; margin-bottom:1.2rem; }
  .card-meta { display:flex; gap:1.5rem; }
  .card-meta-item { text-align:center; }
  .meta-val { font-family:'Barlow Condensed',sans-serif; font-size:1.2rem; font-weight:700; color:var(--white); display:block; }
  .meta-key { font-size:.62rem; color:var(--muted); letter-spacing:1px; text-transform:uppercase; }
  .card-overlay { position:absolute; inset:0; background:rgba(245,197,24,0.04); border:2px solid var(--gold); opacity:0; transition:opacity .3s; pointer-events:none; }
  .card-btn { display:inline-block; margin-top:1rem; background:transparent; border:1px solid rgba(245,197,24,0.4); color:var(--gold); padding:7px 18px; font-size:.73rem; letter-spacing:2px; text-transform:uppercase; font-weight:600; cursor:pointer; transition:all .2s; font-family:'Barlow',sans-serif; }
  .card-btn:hover { background:var(--gold); color:var(--navy-dark); }

  /* ── ABOUT ── */
  #about { padding:100px 8%; display:grid; grid-template-columns:1fr 1fr; gap:6rem; align-items:center; background:var(--navy); }
  .about-text .section-tag,.about-text .section-title { text-align:left; }
  .about-text .section-title { margin-bottom:1.5rem; }
  .about-text p { color:var(--muted); line-height:1.8; margin-bottom:1rem; }
  .about-features { margin-top:2rem; display:flex; flex-direction:column; gap:1rem; }
  .feature { display:flex; align-items:flex-start; gap:1rem; padding:1rem; background:var(--navy-card); border-left:3px solid var(--gold); }
  .feature-icon { width:36px; height:36px; flex-shrink:0; background:rgba(245,197,24,0.1); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:1rem; }
  .feature-text strong { display:block; margin-bottom:.2rem; font-size:.95rem; }
  .feature-text span { font-size:.82rem; color:var(--muted); }
  .pitch-svg-wrap { width:100%; aspect-ratio:1; background:var(--navy-card); border:1px solid rgba(245,197,24,0.1); display:flex; align-items:center; justify-content:center; overflow:hidden; position:relative; }
  .pitch-bg { position:absolute; inset:0; background:linear-gradient(135deg,#0a1e1a 0%,#081510 100%); }

  /* ── CONTACT ── */
  #contact { padding:100px 8%; background:var(--navy-dark); }
  .contact-info-bar { display:flex; justify-content:center; gap:2.5rem; flex-wrap:wrap; margin-bottom:3rem; }
  .contact-info-item { display:flex; align-items:center; gap:.8rem; font-size:.9rem; color:var(--muted); }
  .ci-icon { width:40px; height:40px; background:rgba(245,197,24,0.1); border:1px solid rgba(245,197,24,0.2); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:1.1rem; flex-shrink:0; }
  .ci-label { font-size:.65rem; letter-spacing:2px; text-transform:uppercase; color:var(--gold); display:block; margin-bottom:2px; }
  .contact-info-item a { color:var(--muted); text-decoration:none; transition:color .2s; }
  .contact-info-item a:hover { color:var(--gold); }
  .contact-form { max-width:640px; margin:0 auto; display:flex; flex-direction:column; gap:1rem; }
  .form-row { display:grid; grid-template-columns:1fr 1fr; gap:1rem; }
  .form-group { display:flex; flex-direction:column; gap:.4rem; }
  .form-group label { font-size:.72rem; letter-spacing:2px; text-transform:uppercase; color:var(--muted); }
  .form-group input,.form-group select,.form-group textarea { background:var(--navy-card); border:1px solid rgba(255,255,255,0.07); color:var(--white); padding:12px 16px; font-family:'Barlow',sans-serif; font-size:.95rem; border-radius:2px; transition:border-color .2s; outline:none; }
  .form-group input:focus,.form-group select:focus,.form-group textarea:focus { border-color:var(--gold); }
  .form-group textarea { resize:vertical; min-height:120px; }
  .form-group select option { background:var(--navy-card); }
  .form-submit { background:var(--gold); color:var(--navy-dark); padding:14px; border:none; border-radius:2px; font-family:'Barlow Condensed',sans-serif; font-size:1rem; font-weight:700; letter-spacing:3px; text-transform:uppercase; cursor:pointer; transition:all .2s; margin-top:.5rem; }
  .form-submit:hover { background:#fff; }

  /* ── FOOTER ── */
  footer { background:var(--navy); border-top:2px solid rgba(245,197,24,0.15); padding:2.5rem 8%; }
  .footer-inner { display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:1.5rem; }
  .footer-logo { display:flex; align-items:center; gap:12px; }
  .footer-logo img { height:48px; width:auto; }
  .footer-logo-text { font-family:'Bebas Neue',sans-serif; font-size:1.25rem; letter-spacing:2px; line-height:1.1; }
  .footer-logo-text span { color:var(--gold); font-size:.68rem; display:block; letter-spacing:4px; font-family:'Barlow',sans-serif; font-weight:600; }
  .footer-copy { font-size:.78rem; color:var(--muted); }
  .footer-links { display:flex; gap:1.5rem; }
  .footer-links a { font-size:.78rem; color:var(--muted); text-decoration:none; transition:color .2s; }
  .footer-links a:hover { color:var(--gold); }
  .footer-contact { margin-top:1.5rem; padding-top:1.5rem; border-top:1px solid rgba(245,197,24,0.08); display:flex; gap:3rem; flex-wrap:wrap; }
  .footer-contact-item { font-size:.82rem; color:var(--muted); }
  .footer-contact-item strong { color:var(--gold); display:block; font-size:.65rem; letter-spacing:2px; text-transform:uppercase; margin-bottom:3px; font-family:'Barlow Condensed',sans-serif; }
  .footer-contact-item a { color:var(--muted); text-decoration:none; }

  /* ── MODAL ── */
  .modal-bg { display:none; position:fixed; inset:0; z-index:200; background:rgba(0,0,0,0.88); backdrop-filter:blur(8px); align-items:center; justify-content:center; padding:5%; }
  .modal-bg.open { display:flex; }
  .modal { background:var(--navy-card); max-width:640px; width:100%; border:1px solid rgba(245,197,24,0.2); position:relative; animation:modalIn .3s ease; max-height:90vh; overflow-y:auto; }
  .modal-img { width:100%; height:260px; object-fit:cover; display:block; }
  .modal-img-placeholder { width:100%; height:200px; background:linear-gradient(135deg,#0a1428,#0f1e3a); display:flex; align-items:center; justify-content:center; flex-direction:column; gap:.5rem; }
  .modal-body { padding:2rem; }
  .modal-tag { font-size:.68rem; letter-spacing:3px; color:var(--gold); text-transform:uppercase; font-weight:600; }
  .modal-title { font-family:'Bebas Neue',sans-serif; font-size:2.5rem; letter-spacing:2px; margin:.3rem 0 1rem; }
  .modal-desc { color:var(--muted); line-height:1.7; margin-bottom:1.5rem; }
  .modal-close { position:absolute; top:1rem; right:1rem; background:rgba(0,0,0,.6); border:none; color:var(--white); width:36px; height:36px; border-radius:50%; cursor:pointer; font-size:1.1rem; display:flex; align-items:center; justify-content:center; transition:background .2s; }
  .modal-close:hover { background:var(--gold); color:var(--navy-dark); }
  .modal-stats { display:flex; gap:2rem; padding:1rem 0; border-top:1px solid rgba(255,255,255,0.06); }
  .upload-section { margin-top:1.5rem; }
  .upload-label { font-size:.72rem; letter-spacing:2px; text-transform:uppercase; color:var(--muted); display:block; margin-bottom:.5rem; }
  .upload-area { border:1px dashed rgba(245,197,24,.3); padding:1.5rem; text-align:center; cursor:pointer; transition:border-color .2s,background .2s; position:relative; }
  .upload-area:hover { border-color:var(--gold); background:rgba(245,197,24,.04); }
  .upload-area input[type="file"] { position:absolute; inset:0; opacity:0; cursor:pointer; }
  .upload-area p { font-size:.85rem; color:var(--muted); }
  .upload-area span { font-size:.75rem; color:var(--gold); }
  .upload-preview { display:flex; flex-wrap:wrap; gap:.5rem; margin-top:.75rem; }
  .upload-preview img { width:70px; height:70px; object-fit:cover; border:1px solid rgba(245,197,24,.2); }
  .edit-field { width:100%; background:var(--navy-mid); border:1px solid rgba(255,255,255,.07); color:var(--white); padding:8px 12px; font-family:'Barlow',sans-serif; font-size:.9rem; margin-top:.3rem; border-radius:2px; outline:none; }
  .edit-field:focus { border-color:var(--gold); }
  .save-btn { margin-top:1rem; background:var(--gold); color:var(--navy-dark); border:none; padding:10px 24px; font-family:'Barlow Condensed',sans-serif; font-size:.9rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; cursor:pointer; transition:background .2s; }
  .save-btn:hover { background:#fff; }

  @keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }
  @keyframes modalIn { from{opacity:0;transform:scale(.95) translateY(20px)} to{opacity:1;transform:scale(1) translateY(0)} }

  @media(max-width:768px){
    .hero-stats{display:none}
    #about{grid-template-columns:1fr;gap:3rem}
    .about-visual{display:none}
    .form-row{grid-template-columns:1fr}
    .nav-links{display:none}
    .contact-info-bar{gap:1.2rem}
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#home">
    <img src="/mnt/user-data/uploads/4749.png" alt="Munjeme Soccer Academy Logo">
    <div class="nav-logo-text">Munjeme <span>Soccer Academy</span></div>
  </a>
  <ul class="nav-links">
    <li><a href="#teams">Teams</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Join Us</a></li>
  </ul>
  <button class="nav-cta" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Register Now</button>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-pattern"></div>
  <svg class="hero-shield" width="580" height="680" viewBox="0 0 200 220" fill="none">
    <path d="M100 5 L185 35 L185 110 C185 160 145 200 100 215 C55 200 15 160 15 110 L15 35 Z" fill="white"/>
  </svg>
  <div class="hero-badge">
    <img src="/mnt/user-data/uploads/4749.png" alt="">
    Munjeme Soccer Academy
  </div>
  <h1>Developing<span class="line-gold">Champions</span>Of Tomorrow</h1>
  <p class="hero-sub">From grassroots to elite performance — we develop players, build character, and forge champions at every age group. Proudly based at Ak Magugu Primary School.</p>
  <div class="hero-actions">
    <button class="btn-primary" onclick="document.getElementById('teams').scrollIntoView({behavior:'smooth'})">View Our Teams</button>
    <button class="btn-ghost" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Register a Player</button>
  </div>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num" id="cnt-players">0</div><div class="stat-label">Players</div></div>
    <div class="stat"><div class="stat-num" id="cnt-trophies">0</div><div class="stat-label">Trophies</div></div>
    <div class="stat"><div class="stat-num" id="cnt-coaches">0</div><div class="stat-label">Coaches</div></div>
  </div>
</section>

<!-- TEAMS -->
<section id="teams">
  <div class="section-header">
    <span class="section-tag">Age Groups</span>
    <h2 class="section-title">Our Teams</h2>
  </div>
  <div class="teams-grid" id="teamsGrid"></div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-text">
    <span class="section-tag">Who We Are</span>
    <h2 class="section-title">More Than A Club</h2>
    <p>Munjeme Soccer Academy is a community-driven football academy committed to the holistic development of young players. From the youngest Under 9s to our Senior team, we deliver structured, high-quality coaching at every stage.</p>
    <p>Our philosophy centers on technical mastery, tactical intelligence, and building confident, resilient athletes — all from our home at Ak Magugu Primary School.</p>
    <div class="about-features">
      <div class="feature">
        <div class="feature-icon">🦁</div>
        <div class="feature-text"><strong>Pride of the Lions</strong><span>We play with the heart of a lion — fearless, disciplined, and united</span></div>
      </div>
      <div class="feature">
        <div class="feature-icon">📈</div>
        <div class="feature-text"><strong>Structured Pathway</strong><span>Clear progression from U9 through to Senior level</span></div>
      </div>
      <div class="feature">
        <div class="feature-icon">🤝</div>
        <div class="feature-text"><strong>Values-First Culture</strong><span>Respect, discipline, and teamwork above all else</span></div>
      </div>
    </div>
  </div>
  <div class="about-visual">
    <div class="pitch-svg-wrap">
      <div class="pitch-bg"></div>
      <svg width="90%" viewBox="0 0 400 280" fill="none" style="position:relative;z-index:1">
        <rect x="10" y="10" width="380" height="260" rx="2" stroke="rgba(245,197,24,0.4)" stroke-width="2" fill="none"/>
        <line x1="200" y1="10" x2="200" y2="270" stroke="rgba(245,197,24,0.4)" stroke-width="1.5"/>
        <circle cx="200" cy="140" r="40" stroke="rgba(245,197,24,0.4)" stroke-width="1.5" fill="none"/>
        <circle cx="200" cy="140" r="3" fill="rgba(245,197,24,0.9)"/>
        <rect x="10" y="80" width="70" height="120" stroke="rgba(245,197,24,0.35)" stroke-width="1.5" fill="none"/>
        <rect x="10" y="108" width="28" height="64" stroke="rgba(245,197,24,0.35)" stroke-width="1.5" fill="none"/>
        <rect x="320" y="80" width="70" height="120" stroke="rgba(245,197,24,0.35)" stroke-width="1.5" fill="none"/>
        <rect x="362" y="108" width="28" height="64" stroke="rgba(245,197,24,0.35)" stroke-width="1.5" fill="none"/>
        <circle cx="80" cy="100" r="8" fill="rgba(245,197,24,0.75)"/>
        <circle cx="80" cy="180" r="8" fill="rgba(245,197,24,0.75)"/>
        <circle cx="150" cy="70" r="8" fill="rgba(245,197,24,0.75)"/>
        <circle cx="150" cy="140" r="8" fill="rgba(245,197,24,0.75)"/>
        <circle cx="150" cy="210" r="8" fill="rgba(245,197,24,0.75)"/>
        <circle cx="320" cy="100" r="8" fill="rgba(26,107,90,0.9)"/>
        <circle cx="320" cy="180" r="8" fill="rgba(26,107,90,0.9)"/>
        <circle cx="250" cy="70" r="8" fill="rgba(26,107,90,0.9)"/>
        <circle cx="250" cy="140" r="8" fill="rgba(26,107,90,0.9)"/>
        <circle cx="250" cy="210" r="8" fill="rgba(26,107,90,0.9)"/>
      </svg>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-header">
    <span class="section-tag">Get In Touch</span>
    <h2 class="section-title">Register Your Player</h2>
  </div>

  <div class="contact-info-bar">
    <div class="contact-info-item">
      <div class="ci-icon">📍</div>
      <div><span class="ci-label">Location</span>Ak Magugu Primary School</div>
    </div>
    <div class="contact-info-item">
      <div class="ci-icon">📞</div>
      <div><span class="ci-label">Phone</span><a href="tel:0768424376">0768 424 376</a></div>
    </div>
    <div class="contact-info-item">
      <div class="ci-icon">✉️</div>
      <div><span class="ci-label">Email</span><a href="mailto:vitalisthuo153@gmail.com">vitalisthuo153@gmail.com</a></div>
    </div>
  </div>

  <form class="contact-form" onsubmit="handleSubmit(event)">
    <div class="form-row">
      <div class="form-group"><label>Player First Name</label><input type="text" placeholder="John" required></div>
      <div class="form-group"><label>Player Last Name</label><input type="text" placeholder="Smith" required></div>
    </div>
    <div class="form-row">
      <div class="form-group"><label>Date of Birth</label><input type="date" required></div>
      <div class="form-group">
        <label>Age Group</label>
        <select required>
          <option value="">Select team</option>
          <option>Under 9</option><option>Under 11</option><option>Under 13</option>
          <option>Under 15</option><option>Under 18</option><option>Senior Team</option>
        </select>
      </div>
    </div>
    <div class="form-group"><label>Parent / Guardian Email</label><input type="email" placeholder="parent@email.com" required></div>
    <div class="form-group"><label>Phone Number</label><input type="tel" placeholder="0768 424 376"></div>
    <div class="form-group"><label>Additional Information</label><textarea placeholder="Previous experience, position preference, or any questions..."></textarea></div>
    <button type="submit" class="form-submit">Submit Registration</button>
  </form>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">
      <img src="/mnt/user-data/uploads/4749.png" alt="Munjeme Soccer Academy">
      <div class="footer-logo-text">Munjeme <span>Soccer Academy</span></div>
    </div>
    <div class="footer-copy">© 2026 Munjeme Soccer Academy. All rights reserved.</div>
    <div class="footer-links">
      <a href="#teams">Teams</a><a href="#about">About</a><a href="#contact">Contact</a>
    </div>
  </div>
  <div class="footer-contact">
    <div class="footer-contact-item"><strong>Location</strong>Ak Magugu Primary School</div>
    <div class="footer-contact-item"><strong>Phone</strong><a href="tel:0768424376">0768 424 376</a></div>
    <div class="footer-contact-item"><strong>Email</strong><a href="mailto:vitalisthuo153@gmail.com">vitalisthuo153@gmail.com</a></div>
  </div>
</footer>

<!-- MODAL -->
<div class="modal-bg" id="modal" onclick="closeModalOnBg(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div id="modalImgArea"></div>
    <div class="modal-body">
      <div class="modal-tag" id="mTag"></div>
      <div class="modal-title" id="mTitle"></div>
      <div class="modal-desc" id="mDesc"></div>
      <div class="modal-stats" id="mStats"></div>
      <div class="upload-section">
        <span class="upload-label">Team Photos</span>
        <div class="upload-area">
          <input type="file" accept="image/*" multiple onchange="handleUpload(event)">
          <p>📷 Click to upload team photos</p>
          <span>JPG, PNG, WEBP supported</span>
        </div>
        <div class="upload-preview" id="uploadPreview"></div>
      </div>
      <div class="upload-section" style="margin-top:1.2rem">
        <span class="upload-label">Edit Team Details</span>
        <input class="edit-field" id="editCoach" placeholder="Head Coach name">
        <input class="edit-field" id="editPlayers" placeholder="Number of players" type="number" style="margin-top:.5rem">
        <textarea class="edit-field" id="editBio" placeholder="Team bio / description" rows="3" style="margin-top:.5rem;resize:vertical"></textarea>
        <button class="save-btn" onclick="saveDetails()">Save Changes</button>
      </div>
    </div>
  </div>
</div>

<script>
const teams = [
  {id:0,label:"Under 9",tag:"Youth · Beginners",name:"Under 9 Squad",desc:"The foundation of our academy. We focus on fun, fundamental movement, and a love for the beautiful game.",players:14,coach:"TBA",trophies:0,img:"",bio:""},
  {id:1,label:"Under 11",tag:"Youth · Development",name:"Under 11 Squad",desc:"Building core skills — passing, receiving, and positional awareness in a nurturing, competitive environment.",players:16,coach:"TBA",trophies:1,img:"",bio:""},
  {id:2,label:"Under 13",tag:"Youth · Intermediate",name:"Under 13 Squad",desc:"Tactical concepts are introduced as players begin to understand the game on a deeper level.",players:18,coach:"TBA",trophies:2,img:"",bio:""},
  {id:3,label:"Under 15",tag:"Youth · Advanced",name:"Under 15 Squad",desc:"High-intensity training, league competition, and individual development plans for each player.",players:20,coach:"TBA",trophies:3,img:"",bio:""},
  {id:4,label:"Under 18",tag:"Youth · Elite",name:"Under 18 Squad",desc:"Our bridge to senior football. Players are prepared for professional trials and higher-level competition.",players:22,coach:"TBA",trophies:4,img:"",bio:""},
  {id:5,label:"Senior",tag:"Senior · First Team",name:"Senior Team",desc:"The pinnacle of the academy. A competitive senior side proudly representing Munjeme Soccer Academy.",players:25,coach:"TBA",trophies:6,img:"",bio:""}
];
let currentTeam=null;

function renderTeams(){
  document.getElementById('teamsGrid').innerHTML=teams.map(t=>`
    <div class="team-card" onclick="openModal(${t.id})">
      <div class="card-img-wrap">
        ${t.img?`<img src="${t.img}" alt="${t.name}">`:`<div class="card-placeholder"><svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="1"><circle cx="12" cy="12" r="10"/><path d="M12 2a10 10 0 0 1 0 20M2 12h20M12 2c-2.8 2.8-4 6-4 10s1.2 7.2 4 10M12 2c2.8 2.8 4 6 4 10s-1.2 7.2-4 10"/></svg><span>Add Photo</span></div>`}
        <div class="card-age-badge">${t.label}</div>
      </div>
      <div class="card-body">
        <div class="card-category">${t.tag}</div>
        <div class="card-name">${t.name}</div>
        <div class="card-desc">${t.bio||t.desc}</div>
        <div class="card-meta">
          <div class="card-meta-item"><span class="meta-val">${t.players}</span><span class="meta-key">Players</span></div>
          <div class="card-meta-item"><span class="meta-val">${t.trophies}</span><span class="meta-key">Trophies</span></div>
          <div class="card-meta-item"><span class="meta-val">${t.coach}</span><span class="meta-key">Coach</span></div>
        </div>
        <div class="card-btn">View Team →</div>
      </div>
      <div class="card-overlay"></div>
    </div>`).join('');
}

function openModal(id){
  currentTeam=id; const t=teams[id];
  document.getElementById('mTag').textContent=t.tag;
  document.getElementById('mTitle').textContent=t.name;
  document.getElementById('mDesc').textContent=t.bio||t.desc;
  document.getElementById('mStats').innerHTML=`<div class="modal-stat"><span class="meta-val">${t.players}</span><span class="meta-key">Players</span></div><div class="modal-stat"><span class="meta-val">${t.trophies}</span><span class="meta-key">Trophies</span></div><div class="modal-stat"><span class="meta-val">${t.coach}</span><span class="meta-key">Head Coach</span></div>`;
  document.getElementById('modalImgArea').innerHTML=t.img?`<img class="modal-img" src="${t.img}" alt="${t.name}">`:`<div class="modal-img-placeholder"><svg width="56" height="56" viewBox="0 0 24 24" fill="none" stroke="rgba(245,197,24,0.25)" stroke-width="1.2"><circle cx="12" cy="12" r="10"/><path d="M12 2a10 10 0 0 1 0 20M2 12h20M12 2c-2.8 2.8-4 6-4 10s1.2 7.2 4 10M12 2c2.8 2.8 4 6 4 10s-1.2 7.2-4 10"/></svg><span style="font-size:.72rem;color:#666;margin-top:.5rem;letter-spacing:2px;text-transform:uppercase">Add Team Photo</span></div>`;
  document.getElementById('editCoach').value=t.coach!=='TBA'?t.coach:'';
  document.getElementById('editPlayers').value=t.players;
  document.getElementById('editBio').value=t.bio||'';
  document.getElementById('uploadPreview').innerHTML='';
  document.getElementById('modal').classList.add('open');
}
function closeModal(){document.getElementById('modal').classList.remove('open');}
function closeModalOnBg(e){if(e.target===document.getElementById('modal'))closeModal();}

function handleUpload(e){
  Array.from(e.target.files).forEach(file=>{
    const url=URL.createObjectURL(file);
    if(currentTeam!==null)teams[currentTeam].img=url;
    const img=document.createElement('img'); img.src=url;
    document.getElementById('uploadPreview').appendChild(img);
    document.getElementById('modalImgArea').innerHTML=`<img class="modal-img" src="${url}" alt="Team photo">`;
  });
  renderTeams();
}

function saveDetails(){
  if(currentTeam===null)return;
  const coach=document.getElementById('editCoach').value.trim();
  const players=parseInt(document.getElementById('editPlayers').value)||teams[currentTeam].players;
  const bio=document.getElementById('editBio').value.trim();
  teams[currentTeam].coach=coach||'TBA';
  teams[currentTeam].players=players;
  teams[currentTeam].bio=bio;
  document.getElementById('mDesc').textContent=bio||teams[currentTeam].desc;
  document.getElementById('mStats').innerHTML=`<div class="modal-stat"><span class="meta-val">${players}</span><span class="meta-key">Players</span></div><div class="modal-stat"><span class="meta-val">${teams[currentTeam].trophies}</span><span class="meta-key">Trophies</span></div><div class="modal-stat"><span class="meta-val">${teams[currentTeam].coach}</span><span class="meta-key">Head Coach</span></div>`;
  renderTeams();
  const btn=document.querySelector('.save-btn');
  btn.textContent='✓ Saved!'; btn.style.background='#1A6B5A'; btn.style.color='#fff';
  setTimeout(()=>{btn.textContent='Save Changes';btn.style.background='';btn.style.color='';},1800);
}

function handleSubmit(e){
  e.preventDefault();
  const btn=e.target.querySelector('.form-submit');
  btn.textContent='✓ Registration Received!'; btn.style.background='#1A6B5A'; btn.style.color='#fff';
  setTimeout(()=>{btn.textContent='Submit Registration';btn.style.background='';btn.style.color='';e.target.reset();},3000);
}

function animateCounter(el,target,suffix=''){
  let n=0; const step=Math.ceil(target/40);
  const t=setInterval(()=>{n+=step;if(n>=target){n=target;clearInterval(t);}el.textContent=n+suffix;},40);
}

window.addEventListener('load',()=>{
  renderTeams();
  setTimeout(()=>{
    animateCounter(document.getElementById('cnt-players'),115,'+');
    animateCounter(document.getElementById('cnt-trophies'),16);
    animateCounter(document.getElementById('cnt-coaches'),12);
  },600);
});
</script>
</body>
</html>
