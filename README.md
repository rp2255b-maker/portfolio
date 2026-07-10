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
