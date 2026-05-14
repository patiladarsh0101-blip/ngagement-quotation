<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Adarsh Patil Cinematography — Luxury Engagement Packages</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400;1,600&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Poppins:wght@300;400;500;600&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg-primary: #0a0a0a;
    --bg-secondary: #111111;
    --bg-tertiary: #1a1a1a;
    --gold-primary: #d4af37;
    --gold-light: #f5d77a;
    --gold-dark: #caa64b;
    --gold-muted: rgba(212, 175, 55, 0.15);
    --text-primary: #ffffff;
    --text-secondary: #d9d9d9;
    --text-muted: #888888;
    --glass-bg: rgba(255,255,255,0.03);
    --glass-border: rgba(212, 175, 55, 0.2);
  }

  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg-primary);
    color: var(--text-primary);
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
    cursor: none;
  }

  /* CUSTOM CURSOR */
  .cursor {
    width: 12px; height: 12px;
    background: var(--gold-primary);
    border-radius: 50%;
    position: fixed; top: 0; left: 0;
    pointer-events: none; z-index: 9999;
    transition: transform 0.15s ease;
    mix-blend-mode: difference;
  }
  .cursor-ring {
    width: 40px; height: 40px;
    border: 1px solid rgba(212,175,55,0.5);
    border-radius: 50%;
    position: fixed; top: 0; left: 0;
    pointer-events: none; z-index: 9998;
    transition: transform 0.35s cubic-bezier(0.23,1,0.32,1), width 0.3s, height 0.3s, border-color 0.3s;
  }
  body:hover .cursor-ring { border-color: var(--gold-primary); }

  /* SCROLL PROGRESS */
  .scroll-progress {
    position: fixed; top: 0; left: 0;
    height: 2px; background: linear-gradient(90deg, var(--gold-dark), var(--gold-light), var(--gold-dark));
    z-index: 9000; width: 0%;
    transition: width 0.1s linear;
    box-shadow: 0 0 8px var(--gold-primary);
  }

  /* LOADING SCREEN */
  .loader {
    position: fixed; inset: 0;
    background: #050505;
    z-index: 99999;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    transition: opacity 0.8s ease, visibility 0.8s ease;
  }
  .loader.hidden { opacity: 0; visibility: hidden; }
  .loader-logo {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.2rem, 3vw, 1.8rem);
    color: var(--gold-primary);
    letter-spacing: 0.3em;
    text-transform: uppercase;
    margin-bottom: 2rem;
    opacity: 0;
    animation: fadeInUp 1s 0.3s forwards;
  }
  .loader-bar-wrap {
    width: 200px; height: 1px;
    background: rgba(212,175,55,0.2);
    position: relative; overflow: hidden;
  }
  .loader-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--gold-dark), var(--gold-light));
    width: 0%;
    animation: loadBar 2s 0.5s ease forwards;
    box-shadow: 0 0 10px var(--gold-primary);
  }
  .loader-text {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.3em;
    color: var(--text-muted);
    margin-top: 1rem;
    text-transform: uppercase;
    opacity: 0;
    animation: fadeInUp 1s 0.6s forwards;
  }
  @keyframes loadBar { to { width: 100%; } }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    z-index: 1000;
    padding: 1.2rem 4rem;
    display: flex; align-items: center; justify-content: space-between;
    background: linear-gradient(180deg, rgba(5,5,5,0.95) 0%, transparent 100%);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(212,175,55,0.08);
    transition: all 0.4s ease;
  }
  nav.scrolled {
    background: rgba(8,8,8,0.97);
    border-bottom-color: rgba(212,175,55,0.15);
    padding: 0.9rem 4rem;
  }
  .nav-brand {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    color: var(--gold-primary);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    line-height: 1.3;
  }
  .nav-brand span {
    display: block;
    font-size: 0.55rem;
    font-family: 'Montserrat', sans-serif;
    color: var(--text-muted);
    letter-spacing: 0.35em;
    font-weight: 400;
    margin-top: 2px;
  }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--text-secondary);
    text-decoration: none;
    transition: color 0.3s;
    position: relative;
  }
  .nav-links a::after {
    content: ''; position: absolute; bottom: -4px; left: 0;
    width: 0; height: 1px;
    background: var(--gold-primary);
    transition: width 0.3s ease;
  }
  .nav-links a:hover { color: var(--gold-light); }
  .nav-links a:hover::after { width: 100%; }
  .nav-cta {
    background: transparent;
    border: 1px solid var(--gold-primary);
    color: var(--gold-primary) !important;
    padding: 0.5rem 1.2rem;
    border-radius: 1px;
    transition: all 0.3s ease !important;
  }
  .nav-cta:hover { background: var(--gold-primary); color: #000 !important; }
  .nav-cta::after { display: none !important; }

  /* HERO */
  .hero {
    min-height: 100vh;
    position: relative;
    display: flex; align-items: center; justify-content: center;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 30%, rgba(212,175,55,0.08) 0%, transparent 60%),
      radial-gradient(ellipse 60% 80% at 80% 70%, rgba(212,175,55,0.04) 0%, transparent 50%),
      linear-gradient(160deg, #050505 0%, #0d0d0d 40%, #0a0806 100%);
  }
  .hero-noise {
    position: absolute; inset: 0;
    opacity: 0.03;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    background-size: 200px;
  }
  .hero-grid {
    position: absolute; inset: 0;
    background-image: linear-gradient(rgba(212,175,55,0.04) 1px, transparent 1px),
                      linear-gradient(90deg, rgba(212,175,55,0.04) 1px, transparent 1px);
    background-size: 60px 60px;
    mask-image: radial-gradient(ellipse at center, black 30%, transparent 80%);
  }
  .hero-particles { position: absolute; inset: 0; overflow: hidden; }
  .particle {
    position: absolute;
    width: 2px; height: 2px;
    background: var(--gold-primary);
    border-radius: 50%;
    animation: float linear infinite;
    opacity: 0;
  }

  .hero-content {
    position: relative; z-index: 10;
    text-align: center;
    padding: 0 2rem;
    max-width: 900px;
    animation: heroReveal 1.5s 2.8s ease forwards;
    opacity: 0;
  }
  .hero-eyebrow {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.5em;
    text-transform: uppercase;
    color: var(--gold-primary);
    margin-bottom: 1.5rem;
    display: flex; align-items: center; justify-content: center; gap: 1rem;
  }
  .hero-eyebrow::before, .hero-eyebrow::after {
    content: ''; flex: 1; max-width: 60px;
    height: 1px; background: linear-gradient(90deg, transparent, var(--gold-primary));
  }
  .hero-eyebrow::after { background: linear-gradient(270deg, transparent, var(--gold-primary)); }
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.5rem, 6vw, 5.5rem);
    font-weight: 400;
    line-height: 1.1;
    color: var(--text-primary);
    margin-bottom: 1.5rem;
    letter-spacing: -0.01em;
  }
  .hero-title em {
    font-style: italic;
    color: var(--gold-light);
    display: block;
  }
  .hero-subtitle {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1rem, 2.5vw, 1.4rem);
    color: var(--text-secondary);
    font-weight: 300;
    line-height: 1.7;
    max-width: 600px; margin: 0 auto 3rem;
    font-style: italic;
  }
  .hero-divider {
    width: 80px; height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold-primary), transparent);
    margin: 0 auto 2.5rem;
  }
  .btn-primary {
    display: inline-flex; align-items: center; gap: 0.8rem;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.7rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: #000;
    background: linear-gradient(135deg, var(--gold-dark), var(--gold-light), var(--gold-dark));
    background-size: 200% 100%;
    border: none; padding: 1rem 2.5rem;
    cursor: none;
    text-decoration: none;
    position: relative; overflow: hidden;
    transition: all 0.4s ease;
    box-shadow: 0 0 30px rgba(212,175,55,0.25), 0 0 60px rgba(212,175,55,0.1);
  }
  .btn-primary:hover {
    background-position: right center;
    box-shadow: 0 0 50px rgba(212,175,55,0.4), 0 0 100px rgba(212,175,55,0.15);
    transform: translateY(-2px);
  }
  .btn-primary::before {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(255,255,255,0.2), transparent);
    opacity: 0; transition: opacity 0.3s;
  }
  .btn-primary:hover::before { opacity: 1; }
  .hero-scroll {
    position: absolute; bottom: 2.5rem; left: 50%;
    transform: translateX(-50%);
    display: flex; flex-direction: column;
    align-items: center; gap: 0.5rem;
    opacity: 0;
    animation: heroReveal 1s 3.5s forwards;
  }
  .hero-scroll span {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.55rem; letter-spacing: 0.35em;
    text-transform: uppercase; color: var(--text-muted);
  }
  .scroll-line {
    width: 1px; height: 50px;
    background: linear-gradient(180deg, var(--gold-primary), transparent);
    animation: scrollPulse 2s ease-in-out infinite;
  }

  /* SECTIONS COMMON */
  section { padding: 7rem 2rem; }
  .section-eyebrow {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.6rem; letter-spacing: 0.5em;
    text-transform: uppercase; color: var(--gold-primary);
    text-align: center; margin-bottom: 1rem;
    display: flex; align-items: center; justify-content: center; gap: 1rem;
  }
  .section-eyebrow::before, .section-eyebrow::after {
    content: ''; width: 40px; height: 1px;
    background: var(--gold-primary); opacity: 0.4;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 4vw, 3rem);
    font-weight: 400; text-align: center;
    color: var(--text-primary);
    margin-bottom: 1rem;
  }
  .section-title em { font-style: italic; color: var(--gold-light); }
  .section-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem; font-style: italic;
    color: var(--text-muted); text-align: center;
    margin-bottom: 4rem;
  }

  /* PACKAGES */
  #packages { background: var(--bg-secondary); }
  .packages-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem; max-width: 1200px; margin: 0 auto;
    align-items: start;
  }
  .package-card {
    position: relative;
    background: var(--glass-bg);
    border: 1px solid var(--glass-border);
    border-radius: 2px;
    padding: 2.5rem 2rem;
    backdrop-filter: blur(20px);
    transition: all 0.5s cubic-bezier(0.23,1,0.32,1);
    overflow: hidden;
  }
  .package-card::before {
    content: ''; position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold-primary), transparent);
    opacity: 0; transition: opacity 0.4s;
  }
  .package-card::after {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse at 50% 0%, rgba(212,175,55,0.06) 0%, transparent 60%);
    opacity: 0; transition: opacity 0.4s;
    pointer-events: none;
  }
  .package-card:hover { transform: translateY(-8px); border-color: rgba(212,175,55,0.4); box-shadow: 0 30px 80px rgba(0,0,0,0.5), 0 0 40px rgba(212,175,55,0.08); }
  .package-card:hover::before { opacity: 1; }
  .package-card:hover::after { opacity: 1; }

  .card-featured {
    border-color: rgba(212,175,55,0.35);
    background: rgba(212,175,55,0.04);
    transform: scale(1.03);
    box-shadow: 0 20px 60px rgba(0,0,0,0.4), 0 0 40px rgba(212,175,55,0.1);
  }
  .card-featured:hover { transform: scale(1.03) translateY(-8px); }
  .card-royal {
    background: linear-gradient(160deg, rgba(212,175,55,0.06) 0%, rgba(10,10,10,0.9) 40%);
    border-color: rgba(212,175,55,0.3);
  }
  .card-royal-glow {
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 50% 100%, rgba(212,175,55,0.08) 0%, transparent 60%);
    pointer-events: none;
  }
  @keyframes royalGlow {
    0%, 100% { opacity: 0.4; }
    50% { opacity: 1; }
  }
  .card-royal::before { animation: royalGlow 3s ease-in-out infinite; opacity: 0.6; }

  .badge {
    display: inline-flex; align-items: center; gap: 0.4rem;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.55rem; letter-spacing: 0.25em;
    text-transform: uppercase;
    padding: 0.35rem 0.9rem;
    margin-bottom: 1.5rem;
    border-radius: 1px;
  }
  .badge-popular {
    background: var(--gold-primary); color: #000; font-weight: 600;
  }
  .badge-offer {
    background: rgba(212,175,55,0.12); color: var(--gold-light);
    border: 1px solid rgba(212,175,55,0.3);
  }
  .badge-royal {
    background: linear-gradient(135deg, var(--gold-dark), var(--gold-primary));
    color: #000; font-weight: 700;
  }

  .pkg-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.75rem; letter-spacing: 0.3em;
    color: var(--gold-primary); opacity: 0.6;
    margin-bottom: 0.5rem;
    font-style: italic;
  }
  .pkg-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem; font-weight: 400;
    color: var(--text-primary); margin-bottom: 0.3rem;
  }
  .pkg-subtitle {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.95rem; font-style: italic;
    color: var(--gold-muted); color: rgba(212,175,55,0.6);
    margin-bottom: 1.5rem;
  }
  .pkg-divider {
    width: 40px; height: 1px;
    background: linear-gradient(90deg, var(--gold-primary), transparent);
    margin-bottom: 1.5rem;
  }
  .pkg-features { list-style: none; margin-bottom: 2rem; }
  .pkg-features li {
    font-family: 'Poppins', sans-serif;
    font-size: 0.8rem; color: var(--text-secondary);
    padding: 0.5rem 0;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    display: flex; align-items: center; gap: 0.7rem;
    font-weight: 300;
  }
  .pkg-features li:last-child { border-bottom: none; }
  .pkg-features .feat-icon { font-size: 0.9rem; min-width: 1.2rem; }

  .pkg-price-wrap { margin-top: auto; }
  .pkg-original {
    font-family: 'Poppins', sans-serif;
    font-size: 0.85rem; color: var(--text-muted);
    text-decoration: line-through;
    margin-bottom: 0.3rem;
  }
  .pkg-final {
    font-family: 'Playfair Display', serif;
    font-size: 2.2rem; color: var(--gold-light);
    font-weight: 400;
    text-shadow: 0 0 30px rgba(245,215,122,0.4);
    line-height: 1;
    margin-bottom: 0.3rem;
  }
  .pkg-save {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.6rem; letter-spacing: 0.2em;
    color: #4ade80; text-transform: uppercase;
  }
  .pkg-desc {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.95rem; font-style: italic;
    color: var(--text-muted); line-height: 1.6;
    margin-top: 1.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .pkg-cta {
    display: block; text-align: center;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.65rem; letter-spacing: 0.3em;
    text-transform: uppercase; text-decoration: none;
    margin-top: 1.5rem;
    padding: 0.9rem;
    border: 1px solid var(--glass-border);
    color: var(--gold-light);
    transition: all 0.3s ease; cursor: none;
  }
  .pkg-cta:hover { background: var(--gold-primary); color: #000; border-color: var(--gold-primary); }
  .pkg-cta-gold {
    background: linear-gradient(135deg, var(--gold-dark), var(--gold-light));
    color: #000; border-color: transparent;
    font-weight: 600;
    box-shadow: 0 0 20px rgba(212,175,55,0.25);
  }
  .pkg-cta-gold:hover { box-shadow: 0 0 40px rgba(212,175,55,0.5); color: #000; }

  /* ALBUMS */
  #albums { background: var(--bg-primary); }
  .albums-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.5rem; max-width: 1000px; margin: 0 auto;
  }
  .album-card {
    position: relative;
    background: var(--glass-bg);
    border: 1px solid var(--glass-border);
    padding: 2rem;
    transition: all 0.4s cubic-bezier(0.23,1,0.32,1);
    overflow: hidden;
    cursor: none;
  }
  .album-card::before {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(160deg, rgba(212,175,55,0.05) 0%, transparent 60%);
    opacity: 0; transition: opacity 0.4s;
  }
  .album-card:hover { transform: translateY(-6px); border-color: rgba(212,175,55,0.4); box-shadow: 0 20px 50px rgba(0,0,0,0.4); }
  .album-card:hover::before { opacity: 1; }
  .album-icon {
    font-size: 2.5rem; margin-bottom: 1rem;
    filter: drop-shadow(0 0 10px rgba(212,175,55,0.3));
  }
  .album-photos {
    font-family: 'Montserrat', sans-serif;
    font-size: 0.6rem; letter-spacing: 0.3em;
    text-transform: uppercase; color: var(--gold-primary);
    margin-bottom: 0.3rem;
  }
  .album-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; color: var(--text-primary);
    margin-bottom: 1rem;
  }
  .album-price {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem; color: var(--gold-light);
    text-shadow: 0 0 20px rgba(245,215,122,0.3);
  }
  .album-badge {
    position: absolute; top: 1rem; right: 1rem;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.5rem; letter-spacing: 0.2em;
    text-transform: uppercase;
    background: var(--gold-primary); color: #000;
    padding: 0.25rem 0.7rem; font-weight: 600;
  }

  /* ADD-ONS */
  #addons { background: var(--bg-secondary); }
  .addons-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 1.2rem; max-width: 1100px; margin: 0 auto;
  }
  .addon-card {
    background: rgba(255,255,255,0.02);
    border: 1px solid rgba(212,175,55,0.12);
    padding: 1.8rem;
    transition: all 0.4s ease;
    position: relative; overflow: hidden;
    cursor: none;
  }
  .addon-card::after {
    content: ''; position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold-primary), transparent);
    opacity: 0; transition: opacity 0.4s;
  }
  .addon-card:hover { border-color: rgba(212,175,55,0.3); background: rgba(212,175,55,0.03); transform: translateY(-4px); }
  .addon-card:hover::after { opacity: 1; }
  .addon-icon { font-size: 2rem; margin-bottom: 0.8rem; display: block; }
  .addon-title {
    font-family: 'Playfair Display', serif;
    font-size: 1rem; color: var(--text-primary);
    margin-bottom: 0.3rem;
  }
  .addon-price {
    font-family: 'Poppins', sans-serif;
    font-size: 0.8rem; color: var(--gold-light);
    font-weight: 500;
  }
  .addon-note {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.85rem; font-style: italic;
    color: var(--text-muted); margin-top: 0.3rem;
  }

  /* QUOTE SECTION */
  .quote-section {
    position: relative;
    padding: 8rem 2rem;
    background: var(--bg-primary);
    text-align: center; overflow: hidden;
  }
  .quote-bg {
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 70% 60% at 50% 50%, rgba(212,175,55,0.06) 0%, transparent 70%);
  }
  .quote-particles { position: absolute; inset: 0; overflow: hidden; }
  .quote-mark {
    position: absolute; top: 3rem; left: 50%;
    transform: translateX(-50%);
    font-family: 'Playfair Display', serif;
    font-size: 15rem; line-height: 1;
    color: rgba(212,175,55,0.04);
    pointer-events: none; user-select: none;
    font-style: italic;
  }
  .quote-text {
    position: relative; z-index: 2;
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.5rem, 4vw, 2.8rem);
    font-style: italic;
    color: var(--gold-light);
    line-height: 1.5;
    max-width: 800px; margin: 0 auto 2rem;
    text-shadow: 0 0 60px rgba(212,175,55,0.2);
  }
  .quote-author {
    position: relative; z-index: 2;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.6rem; letter-spacing: 0.4em;
    text-transform: uppercase; color: var(--text-muted);
    display: flex; align-items: center; justify-content: center; gap: 1rem;
  }
  .quote-author::before, .quote-author::after {
    content: ''; width: 40px; height: 1px;
    background: rgba(212,175,55,0.3);
  }

  /* FOOTER */
  footer {
    background: #050505;
    border-top: 1px solid rgba(212,175,55,0.1);
    padding: 4rem 4rem 2rem;
  }
  .footer-top {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center; gap: 3rem;
    padding-bottom: 3rem;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    margin-bottom: 2rem;
  }
  .footer-brand {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; color: var(--gold-primary);
    letter-spacing: 0.1em;
  }
  .footer-brand p {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.85rem; font-style: italic;
    color: var(--text-muted); margin-top: 0.5rem;
    letter-spacing: 0.05em; font-weight: 300;
  }
  .footer-logo-center {
    width: 60px; height: 60px;
    border: 1px solid rgba(212,175,55,0.2);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    color: var(--gold-primary); font-size: 1.5rem;
  }
  .footer-contact { text-align: right; }
  .footer-contact-links {
    display: flex; gap: 1rem; justify-content: flex-end; flex-wrap: wrap;
  }
  .contact-btn {
    display: inline-flex; align-items: center; gap: 0.5rem;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.65rem; letter-spacing: 0.2em;
    text-transform: uppercase; text-decoration: none;
    padding: 0.7rem 1.2rem;
    border: 1px solid rgba(212,175,55,0.25);
    color: var(--text-secondary);
    transition: all 0.3s ease; cursor: none;
  }
  .contact-btn:hover { border-color: var(--gold-primary); color: var(--gold-light); background: rgba(212,175,55,0.05); }
  .contact-btn.whatsapp:hover { border-color: #25d366; color: #25d366; }
  .contact-btn.instagram:hover { border-color: #e1306c; color: #e1306c; }
  .footer-bottom {
    display: flex; align-items: center; justify-content: space-between;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-copy {
    font-family: 'Poppins', sans-serif;
    font-size: 0.65rem; color: var(--text-muted);
    letter-spacing: 0.1em;
  }
  .footer-tagline {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.85rem; font-style: italic;
    color: rgba(212,175,55,0.4);
  }

  /* ANIMATIONS */
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes heroReveal {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes float {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 1; }
    90% { opacity: 1; }
    100% { transform: translateY(-100px) translateX(var(--drift)); opacity: 0; }
  }
  @keyframes scrollPulse {
    0%, 100% { opacity: 0.3; transform: scaleY(1); }
    50% { opacity: 1; transform: scaleY(1.2); }
  }
  @keyframes shimmer {
    0% { background-position: -200% 0; }
    100% { background-position: 200% 0; }
  }
  @keyframes borderGlow {
    0%, 100% { box-shadow: 0 0 5px rgba(212,175,55,0.1), 0 0 20px rgba(212,175,55,0.05); }
    50% { box-shadow: 0 0 20px rgba(212,175,55,0.3), 0 0 60px rgba(212,175,55,0.1); }
  }

  /* REVEAL ON SCROLL */
  .reveal {
    opacity: 0; transform: translateY(40px);
    transition: opacity 0.8s cubic-bezier(0.23,1,0.32,1), transform 0.8s cubic-bezier(0.23,1,0.32,1);
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  /* MUSIC TOGGLE */
  .music-btn {
    position: fixed; bottom: 2rem; right: 2rem;
    width: 48px; height: 48px;
    background: rgba(10,10,10,0.9);
    border: 1px solid rgba(212,175,55,0.3);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    cursor: none; z-index: 500;
    color: var(--gold-primary); font-size: 1rem;
    transition: all 0.3s ease;
    backdrop-filter: blur(10px);
  }
  .music-btn:hover { border-color: var(--gold-primary); box-shadow: 0 0 20px rgba(212,175,55,0.2); }
  .music-btn.playing { animation: borderGlow 2s ease-in-out infinite; }

  /* MOBILE NAV */
  .hamburger {
    display: none;
    flex-direction: column; gap: 5px;
    cursor: none; padding: 5px;
  }
  .hamburger span {
    width: 24px; height: 1px;
    background: var(--gold-primary);
    display: block; transition: all 0.3s;
  }

  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    nav.scrolled { padding: 0.8rem 1.5rem; }
    .nav-links { display: none; }
    .hamburger { display: flex; }
    .nav-links.open {
      display: flex; flex-direction: column;
      position: fixed; top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(5,5,5,0.98);
      align-items: center; justify-content: center;
      gap: 2.5rem; z-index: 999;
      backdrop-filter: blur(20px);
    }
    .nav-links.open a { font-size: 1rem; letter-spacing: 0.15em; }
    section { padding: 5rem 1.2rem; }
    .packages-grid { grid-template-columns: 1fr; }
    .card-featured { transform: scale(1); }
    .card-featured:hover { transform: translateY(-8px); }
    .footer-top { grid-template-columns: 1fr; text-align: center; }
    .footer-contact { text-align: center; }
    .footer-contact-links { justify-content: center; }
    .footer-bottom { flex-direction: column; text-align: center; }
    .footer-logo-center { margin: 0 auto; }
    .cursor, .cursor-ring { display: none; }
    body { cursor: auto; }
    a, button { cursor: pointer; }
    .btn-primary, .pkg-cta, .contact-btn, .music-btn { cursor: pointer; }
  }

  @media (max-width: 480px) {
    .hero-title { font-size: 2rem; }
    .packages-grid { gap: 1.5rem; }
    .addons-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- CURSOR -->
<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- SCROLL PROGRESS -->
<div class="scroll-progress" id="scrollProgress"></div>

<!-- LOADER -->
<div class="loader" id="loader">
  <div class="loader-logo">Adarsh Patil</div>
  <div class="loader-bar-wrap"><div class="loader-bar"></div></div>
  <div class="loader-text">Crafting your cinematic experience</div>
</div>

<!-- MUSIC TOGGLE -->
<button class="music-btn" id="musicBtn" title="Toggle ambient music">♪</button>
<audio id="ambientAudio" loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-9.mp3" type="audio/mpeg">
</audio>

<!-- NAV -->
<nav id="navbar">
  <div class="nav-brand">
    Adarsh Patil
    <span>Cinematography & Videography</span>
  </div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#packages">Packages</a></li>
    <li><a href="#albums">Albums</a></li>
    <li><a href="#addons">Add-Ons</a></li>
    <li><a href="#footer" class="nav-cta">Contact</a></li>
  </ul>
  <div class="hamburger" id="hamburger">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-noise"></div>
  <div class="hero-grid"></div>
  <div class="hero-particles" id="heroParticles"></div>

  <div class="hero-content">
    <div class="hero-eyebrow">Engagement Packages 2025</div>
    <h1 class="hero-title">
      Luxury Engagement
      <em>Experiences</em>
    </h1>
    <div class="hero-divider"></div>
    <p class="hero-subtitle">
      Crafting timeless memories with cinematic storytelling, emotions & elegance.
    </p>
    <a href="#packages" class="btn-primary">
      <span>✦</span>
      View Packages
      <span>✦</span>
    </a>
  </div>

  <div class="hero-scroll">
    <span>Scroll</span>
    <div class="scroll-line"></div>
  </div>
</section>

<!-- PACKAGES -->
<section id="packages">
  <div class="section-eyebrow">Our Offerings</div>
  <h2 class="section-title reveal">Engagement <em>Packages</em></h2>
  <p class="section-sub reveal">Three curated experiences — each crafted with intention and elegance.</p>

  <div class="packages-grid">

    <!-- PACKAGE 01 -->
    <div class="package-card reveal reveal-delay-1">
      <div class="badge badge-offer">✦ Special Offer</div>
      <div class="pkg-num">Package 01</div>
      <h3 class="pkg-title">Classic Moments</h3>
      <p class="pkg-subtitle">Simple & Elegant Coverage</p>
      <div class="pkg-divider"></div>
      <ul class="pkg-features">
        <li><span class="feat-icon">📸</span> Traditional Photography</li>
        <li><span class="feat-icon">🖼</span> Professional Photo Editing</li>
      </ul>
      <div class="pkg-price-wrap">
        <div class="pkg-original">₹13,000</div>
        <div class="pkg-final">₹10,000</div>
        <div class="pkg-save">✓ Save ₹3,000</div>
      </div>
      <p class="pkg-desc">"Perfect for couples who want simple, elegant and beautifully captured engagement memories."</p>
      <a href="#footer" class="pkg-cta">Book Now</a>
    </div>

    <!-- PACKAGE 02 -->
    <div class="package-card card-featured reveal reveal-delay-2">
      <div class="badge badge-popular">★ Most Popular</div>
      <div class="pkg-num">Package 02</div>
      <h3 class="pkg-title">Signature Celebration</h3>
      <p class="pkg-subtitle">Emotional & Cinematic Experience</p>
      <div class="pkg-divider"></div>
      <ul class="pkg-features">
        <li><span class="feat-icon">📸</span> Traditional Photography</li>
        <li><span class="feat-icon">📷</span> Candid Photography</li>
        <li><span class="feat-icon">🎬</span> Cinematic Videography</li>
        <li><span class="feat-icon">🖼</span> Professional Photo Editing</li>
        <li><span class="feat-icon">🎞</span> Cinematic Video Editing</li>
        <li><span class="feat-icon">📱</span> 1 Instagram Reel Included</li>
      </ul>
      <div class="pkg-price-wrap">
        <div class="pkg-original">₹36,000</div>
        <div class="pkg-final">₹32,000</div>
        <div class="pkg-save">✓ Save ₹4,000</div>
      </div>
      <p class="pkg-desc">"A perfect blend of emotions, candid moments and cinematic storytelling."</p>
      <a href="#footer" class="pkg-cta pkg-cta-gold">Book Now — Most Popular</a>
    </div>

    <!-- PACKAGE 03 -->
    <div class="package-card card-royal reveal reveal-delay-3">
      <div class="card-royal-glow"></div>
      <div class="badge badge-royal">♛ Royal Experience</div>
      <div class="pkg-num">Package 03</div>
      <h3 class="pkg-title">Royal Engagement</h3>
      <p class="pkg-subtitle">Luxury Cinematic Storytelling</p>
      <div class="pkg-divider"></div>
      <ul class="pkg-features">
        <li><span class="feat-icon">📸</span> Traditional Photography</li>
        <li><span class="feat-icon">📷</span> Candid Photography</li>
        <li><span class="feat-icon">🎥</span> Traditional Videography</li>
        <li><span class="feat-icon">🎬</span> Cinematic Videography</li>
        <li><span class="feat-icon">🖼</span> Premium Photo Editing</li>
        <li><span class="feat-icon">🎞</span> Cinematic Film Editing</li>
        <li><span class="feat-icon">📀</span> Traditional Video Editing</li>
        <li><span class="feat-icon">📱</span> 2 Instagram Reels Included</li>
        <li><span class="feat-icon">☁️</span> Online Gallery Access</li>
      </ul>
      <div class="pkg-price-wrap">
        <div class="pkg-original">₹50,000</div>
        <div class="pkg-final">₹44,000</div>
        <div class="pkg-save">✓ Save ₹6,000</div>
      </div>
      <p class="pkg-desc">"Crafted for couples who desire a luxurious and unforgettable engagement experience."</p>
      <a href="#footer" class="pkg-cta">Book the Royal Experience</a>
    </div>

  </div>
</section>

<!-- ALBUMS -->
<section id="albums">
  <div class="section-eyebrow">Preserve the Memories</div>
  <h2 class="section-title reveal">Premium <em>Album Collection</em></h2>
  <p class="section-sub reveal">Heirloom-quality albums crafted for generations.</p>

  <div class="albums-grid">
    <div class="album-card reveal reveal-delay-1">
      <div class="album-icon">📖</div>
      <div class="album-photos">100 Photos</div>
      <h3 class="album-title">Classic Album</h3>
      <div class="album-price">₹5,000</div>
    </div>
    <div class="album-card reveal reveal-delay-2">
      <div class="album-badge">Most Preferred</div>
      <div class="album-icon">📔</div>
      <div class="album-photos">150 Photos</div>
      <h3 class="album-title">Signature Album</h3>
      <div class="album-price">₹7,000</div>
    </div>
    <div class="album-card reveal reveal-delay-3">
      <div class="album-icon">📚</div>
      <div class="album-photos">250 Photos</div>
      <h3 class="album-title">Luxury Album</h3>
      <div class="album-price">₹10,000</div>
    </div>
  </div>
</section>

<!-- ADD-ONS -->
<section id="addons">
  <div class="section-eyebrow">Enhance Your Experience</div>
  <h2 class="section-title reveal">Optional <em>Add-Ons</em></h2>
  <p class="section-sub reveal">Elevate your coverage with bespoke cinematic extras.</p>

  <div class="addons-grid">
    <div class="addon-card reveal reveal-delay-1">
      <span class="addon-icon">🚁</span>
      <div class="addon-title">Drone Coverage</div>
      <div class="addon-price">₹6,000 Per Day</div>
      <div class="addon-note">Aerial cinematic perspectives</div>
    </div>
    <div class="addon-card reveal reveal-delay-2">
      <span class="addon-icon">🎞</span>
      <div class="addon-title">Same Day Edit</div>
      <div class="addon-price">₹5,000 Extra</div>
      <div class="addon-note">Cinematic film, ready same day</div>
    </div>
    <div class="addon-card reveal reveal-delay-3">
      <span class="addon-icon">✨</span>
      <div class="addon-title">AI Memory Film</div>
      <div class="addon-price">Separate charges apply</div>
      <div class="addon-note">AI-crafted cinematic memory reel</div>
    </div>
    <div class="addon-card reveal reveal-delay-4">
      <span class="addon-icon">📱</span>
      <div class="addon-title">Extra Instagram Reel</div>
      <div class="addon-price">₹2,000 Per Reel</div>
      <div class="addon-note">Share your story beautifully</div>
    </div>
  </div>
</section>

<!-- QUOTE SECTION -->
<div class="quote-section">
  <div class="quote-bg"></div>
  <div class="quote-particles" id="quoteParticles"></div>
  <div class="quote-mark">"</div>
  <blockquote class="quote-text reveal">
    Every engagement has a story…<br>
    We capture it with emotions, elegance<br>
    & timeless cinematic memories.
  </blockquote>
  <div class="quote-author reveal reveal-delay-1">
    Adarsh Patil Cinematography
  </div>
</div>

<!-- FOOTER -->
<footer id="footer">
  <div class="footer-top">
    <div class="footer-brand">
      Adarsh Patil<br>Cinematography and Videography
      <p>Crafting cinematic memories, one frame at a time.</p>
    </div>
    <div class="footer-logo-center">✦</div>
    <div class="footer-contact">
      <div class="footer-contact-links">
        <a href="https://www.instagram.com/iamadarshpatil?igsh=ZHR0M2s2Ynp6ZHRl&utm_source=qr" class="contact-btn instagram" target="_blank">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          Instagram
        </a>
        <a href="https://wa.me/917744882930" class="contact-btn whatsapp" target="_blank">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
          WhatsApp
        </a>
        <a href="tel:+917744882930" class="contact-btn">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
          +91 77448 82930
        </a>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">
      © 2025 Adarsh Patil Cinematography and Videography. All rights reserved.
    </div>
    <div class="footer-tagline">
      Crafted with love & cinematic artistry ✦
    </div>
  </div>
</footer>

<script>
// LOADER
window.addEventListener('load', () => {
  setTimeout(() => {
    document.getElementById('loader').classList.add('hidden');
  }, 2600);
});

// CURSOR
const cursor = document.getElementById('cursor');
const cursorRing = document.getElementById('cursorRing');
let mouseX = 0, mouseY = 0, ringX = 0, ringY = 0;

document.addEventListener('mousemove', e => {
  mouseX = e.clientX; mouseY = e.clientY;
  cursor.style.transform = `translate(${mouseX - 6}px, ${mouseY - 6}px)`;
});

function animateRing() {
  ringX += (mouseX - ringX - 20) * 0.12;
  ringY += (mouseY - ringY - 20) * 0.12;
  cursorRing.style.transform = `translate(${ringX}px, ${ringY}px)`;
  requestAnimationFrame(animateRing);
}
animateRing();

document.querySelectorAll('a, button, .package-card, .album-card, .addon-card').forEach(el => {
  el.addEventListener('mouseenter', () => {
    cursorRing.style.width = '60px';
    cursorRing.style.height = '60px';
    cursor.style.transform += ' scale(1.5)';
  });
  el.addEventListener('mouseleave', () => {
    cursorRing.style.width = '40px';
    cursorRing.style.height = '40px';
  });
});

// SCROLL PROGRESS
const progressBar = document.getElementById('scrollProgress');
window.addEventListener('scroll', () => {
  const scrollTop = document.documentElement.scrollTop;
  const scrollHeight = document.documentElement.scrollHeight - window.innerHeight;
  progressBar.style.width = (scrollTop / scrollHeight * 100) + '%';

  // NAV
  const nav = document.getElementById('navbar');
  nav.classList.toggle('scrolled', scrollTop > 50);
});

// REVEAL ON SCROLL
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) entry.target.classList.add('visible');
  });
}, { threshold: 0.1 });
reveals.forEach(el => observer.observe(el));

// PARTICLES - HERO
function createParticles(container, count) {
  for (let i = 0; i < count; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random() * 3 + 1;
    const x = Math.random() * 100;
    const drift = (Math.random() - 0.5) * 200 + 'px';
    const duration = Math.random() * 15 + 10;
    const delay = Math.random() * 15;
    p.style.cssText = `
      left: ${x}%; bottom: -10px;
      width: ${size}px; height: ${size}px;
      --drift: ${drift};
      animation-duration: ${duration}s;
      animation-delay: ${delay}s;
      opacity: ${Math.random() * 0.6 + 0.2};
    `;
    container.appendChild(p);
  }
}
createParticles(document.getElementById('heroParticles'), 50);
createParticles(document.getElementById('quoteParticles'), 30);

// MOBILE NAV
const hamburger = document.getElementById('hamburger');
const navLinks = document.getElementById('navLinks');
hamburger.addEventListener('click', () => {
  navLinks.classList.toggle('open');
});
navLinks.querySelectorAll('a').forEach(a => {
  a.addEventListener('click', () => navLinks.classList.remove('open'));
});

// MUSIC
const musicBtn = document.getElementById('musicBtn');
const audio = document.getElementById('ambientAudio');
let playing = false;
audio.volume = 0.15;

musicBtn.addEventListener('click', () => {
  if (playing) {
    audio.pause();
    musicBtn.textContent = '♪';
    musicBtn.classList.remove('playing');
  } else {
    audio.play().catch(() => {});
    musicBtn.textContent = '♫';
    musicBtn.classList.add('playing');
  }
  playing = !playing;
});

// SMOOTH SCROLL
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    e.preventDefault();
    const target = document.querySelector(a.getAttribute('href'));
    if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
  });
});
</script>
</body>
</html>
