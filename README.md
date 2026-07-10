# portfolio
my design portpolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ritesh — UI/UX Designer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;0,9..144,900;1,9..144,500&family=Space+Grotesk:wght@400;500;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#17131F;
    --paper:#FFFCF7;
    --sun:#FFC53D;
    --coral:#FF5A5F;
    --cobalt:#2F5CFF;
    --grape:#8A3FFC;
    --mint:#00C2A8;
    --line: rgba(23,19,31,0.12);
    --radius: 22px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{animation-duration:0.001ms !important; transition-duration:0.001ms !important;}
  }
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  a{color:inherit;}
  h1,h2,h3{font-family:'Fraunces',serif; margin:0; line-height:1.02;}
  .eyebrow{
    font-family:'Space Grotesk',sans-serif;
    text-transform:uppercase;
    letter-spacing:0.14em;
    font-size:0.72rem;
    font-weight:500;
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{
    content:''; width:20px; height:2px; background:currentColor; display:inline-block;
  }
  :focus-visible{
    outline:3px solid var(--cobalt);
    outline-offset:3px;
    border-radius:4px;
  }
  .wrap{max-width:1180px; margin:0 auto; padding:0 32px;}

  /* ---------- NAV ---------- */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(255,252,247,0.85);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  nav.wrap{
    display:flex; align-items:center; justify-content:space-between;
    padding-top:18px; padding-bottom:18px;
  }
  .brand{
    font-family:'Space Grotesk',sans-serif;
    font-weight:700; font-size:1.05rem;
    text-decoration:none;
    display:flex; align-items:center; gap:10px;
  }
  .brand .dot{width:12px; height:12px; border-radius:50%; background:var(--coral);}
  .navlinks{display:flex; gap:28px; list-style:none; margin:0; padding:0;}
  .navlinks a{
    font-family:'Space Grotesk',sans-serif; font-size:0.9rem; font-weight:500;
    text-decoration:none; position:relative; padding-bottom:4px;
  }
  .navlinks a::after{
    content:''; position:absolute; left:0; bottom:0; width:0; height:2px;
    background:var(--cobalt); transition:width 0.25s ease;
  }
  .navlinks a:hover::after{width:100%;}
  .navlinks{align-items:center;}
  @media (max-width:720px){ .navlinks{display:none;} }

  /* ---------- HERO ---------- */
  .hero{
    position:relative;
    padding:96px 0 70px;
    overflow:hidden;
  }
  .blob{
    position:absolute; border-radius:50%; filter:blur(2px); opacity:0.85;
    animation: drift 14s ease-in-out infinite;
  }
  @keyframes drift{
    0%,100%{ transform:translateY(0) rotate(0deg); }
    50%{ transform:translateY(-16px) rotate(6deg); }
  }
  .b1{ width:220px; height:220px; background:var(--sun); top:-60px; right:-40px; }
  .b2{ width:120px; height:120px; background:var(--mint); bottom:10px; right:180px; animation-delay:-4s;}
  .b3{ width:70px; height:70px; background:var(--coral); top:120px; right:340px; animation-delay:-8s;}

  .hero h1{
    font-size:clamp(2.6rem, 7vw, 5.6rem);
    font-weight:900;
    max-width:11ch;
    position:relative; z-index:2;
  }
  .hero h1 em{
    font-style:italic; font-weight:500; color:var(--grape);
  }
  .hero .sub{
    max-width:520px; margin-top:26px; font-size:1.08rem; line-height:1.6; color:rgba(23,19,31,0.75);
    position:relative; z-index:2;
  }
  .hero-cta{ display:flex; gap:16px; margin-top:38px; flex-wrap:wrap; position:relative; z-index:2;}
  .btn{
    font-family:'Space Grotesk',sans-serif; font-weight:500; font-size:0.95rem;
    padding:14px 26px; border-radius:100px; text-decoration:none;
    display:inline-flex; align-items:center; gap:8px;
    transition:transform 0.2s ease, box-shadow 0.2s ease;
    border:2px solid var(--ink);
  }
  .btn:hover{ transform:translateY(-3px); }
  .btn-solid{ background:var(--ink); color:var(--paper); }
  .btn-solid:hover{ box-shadow:6px 6px 0 var(--sun); }
  .btn-outline{ background:transparent; color:var(--ink); }
  .btn-outline:hover{ box-shadow:6px 6px 0 var(--cobalt); }

  /* squiggle underline */
  .squiggle{ display:block; margin-top:6px; }

  /* ---------- SWATCH RAIL ---------- */
  .swatch-rail{
    display:flex; gap:10px; margin:56px 0 0; flex-wrap:wrap; position:relative; z-index:2;
  }
  .swatch{
    font-family:'Space Grotesk',sans-serif; font-size:0.82rem; font-weight:500;
    padding:9px 18px; border-radius:100px; text-decoration:none; color:var(--ink);
    border:2px solid transparent;
    transition:transform 0.15s ease, border-color 0.15s ease;
  }
  .swatch:hover{ transform:translateY(-2px); border-color:var(--ink); }
  .sw-1{background:var(--sun);} .sw-2{background:var(--coral); color:var(--paper);}
  .sw-3{background:var(--cobalt); color:var(--paper);} .sw-4{background:var(--grape); color:var(--paper);}

  /* ---------- WORK ---------- */
  section{ padding:90px 0; }
  .section-head{ margin-bottom:48px; }
  .section-head h2{ font-size:clamp(1.9rem,4vw,2.9rem); font-weight:600; margin-top:14px; }

  .project{
    display:grid; grid-template-columns: 1fr 1fr; gap:48px; align-items:center;
    padding:48px 0; border-top:1px solid var(--line);
  }
  .project:last-child{ border-bottom:1px solid var(--line); }
  .project-media{
    aspect-ratio: 4/3; border-radius:var(--radius); position:relative; overflow:hidden;
    display:flex; align-items:center; justify-content:center;
    transition:transform 0.35s ease;
  }
  .project:hover .project-media{ transform:rotate(-1deg) scale(1.02); }
  .project-media span{
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:1rem; opacity:0.55;
  }
  .p-1 .project-media{ background:linear-gradient(155deg, var(--sun), #ffe28f); }
  .p-2 .project-media{ background:linear-gradient(155deg, var(--coral), #ff9a9d); }
  .p-3 .project-media{ background:linear-gradient(155deg, var(--cobalt), #9db2ff); }
  .p-4 .project-media{ background:linear-gradient(155deg, var(--grape), #d4b8ff); }

  .project-tag{
    font-family:'Space Grotesk',sans-serif; font-size:0.72rem; font-weight:700;
    text-transform:uppercase; letter-spacing:0.1em;
    padding:5px 12px; border-radius:100px; display:inline-block; margin-bottom:14px;
  }
  .p-1 .project-tag{ background:var(--sun); }
  .p-2 .project-tag{ background:var(--coral); color:var(--paper); }
  .p-3 .project-tag{ background:var(--cobalt); color:var(--paper); }
  .p-4 .project-tag{ background:var(--grape); color:var(--paper); }

  .project h3{ font-size:clamp(1.5rem,3vw,2.1rem); font-weight:600; }
  .project p{ margin:16px 0 20px; color:rgba(23,19,31,0.72); line-height:1.65; max-width:46ch; }
  .project-link{
    font-family:'Space Grotesk',sans-serif; font-weight:500; font-size:0.92rem;
    text-decoration:none; display:inline-flex; align-items:center; gap:8px;
    border-bottom:2px solid var(--ink); padding-bottom:2px;
  }
  .project-link:hover{ gap:12px; transition:gap 0.2s ease; }

  @media (max-width:820px){
    .project{ grid-template-columns:1fr; }
    .project:nth-child(even){ direction:rtl; }
    .project:nth-child(even) > *{ direction:ltr; }
  }

  /* ---------- ABOUT ---------- */
  .about-grid{
    display:grid; grid-template-columns: 0.9fr 1.3fr; gap:60px; align-items:start;
  }
  .about-card{
    aspect-ratio:1/1.1; border-radius:var(--radius);
    background:
      radial-gradient(circle at 30% 30%, var(--mint), transparent 60%),
      radial-gradient(circle at 70% 70%, var(--grape), transparent 60%),
      var(--ink);
    position:relative;
  }
  .about-card::after{
    content:'R'; position:absolute; bottom:20px; left:24px;
    font-family:'Fraunces',serif; font-style:italic; font-size:2.4rem; color:var(--paper);
  }
  .about p{ font-size:1.1rem; line-height:1.75; color:rgba(23,19,31,0.8); max-width:56ch; }
  .about p + p{ margin-top:18px; }
  .pills{ display:flex; flex-wrap:wrap; gap:10px; margin-top:32px; }
  .pill{
    font-family:'Space Grotesk',sans-serif; font-size:0.85rem; font-weight:500;
    padding:8px 16px; border-radius:100px; border:1.5px solid var(--ink);
  }
  @media (max-width:820px){ .about-grid{ grid-template-columns:1fr; } }

  /* ---------- CONTACT ---------- */
  footer{
    background:var(--ink); color:var(--paper); padding:90px 0 40px; position:relative; overflow:hidden;
  }
  .contact-head{ position:relative; z-index:2; }
  .contact-head .eyebrow{ color:var(--sun); }
  footer h2{
    font-size:clamp(2.2rem,6vw,4.2rem); font-weight:600; margin-top:16px; max-width:14ch;
  }
  .email-link{
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:clamp(1.3rem,3vw,1.8rem);
    color:var(--paper); text-decoration:none; display:inline-flex; align-items:center; gap:14px;
    margin-top:36px; border-bottom:3px solid var(--sun); padding-bottom:6px;
  }
  .foot-bottom{
    display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:16px;
    margin-top:80px; padding-top:24px; border-top:1px solid rgba(255,252,247,0.15);
    font-family:'Space Grotesk',sans-serif; font-size:0.85rem; color:rgba(255,252,247,0.6);
  }
  .foot-links{ display:flex; gap:20px; list-style:none; padding:0; margin:0; }
  .foot-links a{ text-decoration:none; color:rgba(255,252,247,0.85); }
  .foot-links a:hover{ color:var(--sun); }
</style>
</head>
<body>

<header>
  <nav class="wrap">
    <a href="#top" class="brand"><span class="dot"></span> Ritesh</a>
    <ul class="navlinks">
      <li><a href="#work">Work</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#contact" class="btn btn-solid" style="padding:9px 20px; font-size:0.85rem;">Say hello</a></li>
    </ul>
  </nav>
</header>

<main id="top">
  <section class="hero">
    <div class="blob b1" aria-hidden="true"></div>
    <div class="blob b2" aria-hidden="true"></div>
    <div class="blob b3" aria-hidden="true"></div>
    <div class="wrap">
      <p class="eyebrow">UI/UX Designer — Based in Mumbai</p>
      <h1>I design interfaces that feel <em>alive.</em></h1>
      <svg class="squiggle" width="180" height="20" viewBox="0 0 180 20" fill="none" aria-hidden="true">
        <path d="M2 15C20 2 38 2 56 15C74 28 92 2 110 15C128 28 146 2 164 15" stroke="#2F5CFF" stroke-width="4" stroke-linecap="round"/>
      </svg>
      <p class="sub">Four years turning messy problems into interfaces people actually enjoy using — for health tech, fintech, and a couple of things I can't talk about yet.</p>
      <div class="hero-cta">
        <a href="#work" class="btn btn-solid">See the work →</a>
        <a href="#contact" class="btn btn-outline">Let's talk</a>
      </div>
      <div class="swatch-rail">
        <a href="#p1" class="swatch sw-1">MedVault App</a>
        <a href="#p2" class="swatch sw-2">Sunrise Bank</a>
        <a href="#p3" class="swatch sw-3">Loop Fitness</a>
        <a href="#p4" class="swatch sw-4">Scheme Finder</a>
      </div>
    </div>
  </section>

  <section id="work">
    <div class="wrap">
      <div class="section-head">
        <p class="eyebrow">Selected work</p>
        <h2>Four projects, four problems worth solving.</h2>
      </div>

      <div class="project p-1" id="p1">
        <div class="project-media"><span>Cover image</span></div>
        <div>
          <span class="project-tag">Healthcare · Mobile</span>
          <h3>MedVault — a family medicine tracker</h3>
          <p>Redesigned a cluttered medicine-scanning flow into a calm, single-tap experience for families managing multiple members' prescriptions and reminders.</p>
          <a href="#" class="project-link">View case study →</a>
        </div>
      </div>

      <div class="project p-2" id="p2">
        <div class="project-media"><span>Cover image</span></div>
        <div>
          <span class="project-tag">Fintech · Web</span>
          <h3>Sunrise Bank — onboarding redesign</h3>
          <p>Cut account opening time from 11 minutes to under 3 by rethinking form density, error states, and progressive disclosure across 6 screens.</p>
          <a href="#" class="project-link">View case study →</a>
        </div>
      </div>

      <div class="project p-3" id="p3">
        <div class="project-media"><span>Cover image</span></div>
        <div>
          <span class="project-tag">Wellness · Mobile</span>
          <h3>Loop Fitness — habit-first design system</h3>
          <p>Built a component library and motion language for a habit-tracking app, focused on making streaks feel rewarding without turning into guilt.</p>
          <a href="#" class="project-link">View case study →</a>
        </div>
      </div>

      <div class="project p-4" id="p4">
        <div class="project-media"><span>Cover image</span></div>
        <div>
          <span class="project-tag">Civic · Web</span>
          <h3>Scheme Finder — government benefits, simplified</h3>
          <p>Turned dense eligibility documents for public welfare schemes into a plain-language, filterable directory used by over 40,000 people in its first month.</p>
          <a href="#" class="project-link">View case study →</a>
        </div>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="wrap about-grid about">
      <div class="about-card" role="img" aria-label="Portrait placeholder"></div>
      <div>
        <p class="eyebrow">About</p>
        <h2 style="font-size:clamp(1.9rem,4vw,2.9rem); font-weight:600; margin:14px 0 24px;">Design is just clarity, made visible.</h2>
        <p>I'm a product designer who started in illustration and got pulled into UI because I liked watching people actually use the things I made. I care most about the unglamorous parts — empty states, error messages, the fifth screen nobody demos.</p>
        <p>Outside of client work, I run a small newsletter on color theory in interfaces, and I'm slowly teaching myself to bind books by hand.</p>
        <div class="pills">
          <span class="pill">Product Design</span>
          <span class="pill">Design Systems</span>
          <span class="pill">Figma</span>
          <span class="pill">Motion &amp; Prototyping</span>
          <span class="pill">Accessibility</span>
          <span class="pill">Illustration</span>
        </div>
      </div>
    </div>
  </section>
</main>

<footer id="contact">
  <div class="wrap contact-head">
    <p class="eyebrow">Get in touch</p>
    <h2>Got a project worth designing well? Let's make it.</h2>
    <a href="mailto:hello@ritesh.design" class="email-link">hello@ritesh.design ↗</a>

    <div class="foot-bottom">
      <span>© 2026 Ritesh. All rights reserved.</span>
      <ul class="foot-links">
        <li><a href="#">Dribbble</a></li>
        <li><a href="#">LinkedIn</a></li>
        <li><a href="#">Instagram</a></li>
      </ul>
    </div>
  </div>
</footer>

</body>
</html>
