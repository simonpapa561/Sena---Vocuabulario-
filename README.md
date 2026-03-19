<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Glosario Interactivo IA</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@300;400;600;700&family=Syne:wght@400;600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --black:#000;--white:#fff;
  --gray-50:#f9f9f9;--gray-100:#f2f2f2;--gray-200:#e8e8e8;--gray-400:#999;--gray-600:#555;--gray-800:#222;
  --blue:#0071e3;--blue-dark:#0060c0;
  --accent-1:#6366f1;--accent-2:#8b5cf6;--accent-3:#06b6d4;
  --mat-1:#0071e3;--mat-2:#1d4ed8;
  --mat-tgs:#059669;--mat-tgs-2:#047857;
  --mat-agil:#dc2626;--mat-agil-2:#b91c1c;
  --font-display:'Syne',sans-serif;
  --font-body:'DM Sans',sans-serif;
  --nav-h:64px;
  --radius-card:20px;
  --shadow-card:0 2px 20px rgba(0,0,0,0.08);
  --shadow-hover:0 12px 40px rgba(0,0,0,0.15);
  --transition:all 0.35s cubic-bezier(0.4,0,0.2,1);
}
html{scroll-behavior:smooth;}
body{background:var(--white);color:var(--black);font-family:var(--font-body);-webkit-font-smoothing:antialiased;overflow-x:hidden;}
::selection{background:var(--blue);color:#fff;}
::-webkit-scrollbar{width:6px;}
::-webkit-scrollbar-track{background:#f1f1f1;}
::-webkit-scrollbar-thumb{background:#ccc;border-radius:3px;}

/* ── NAV ── */
nav{
  position:fixed;top:0;left:0;width:100%;height:var(--nav-h);
  background:rgba(255,255,255,0.85);
  backdrop-filter:saturate(180%) blur(20px);
  -webkit-backdrop-filter:saturate(180%) blur(20px);
  border-bottom:1px solid rgba(0,0,0,0.07);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 40px;z-index:1000;
  transition:var(--transition);
}
.nav-logo{
  font-family:var(--font-display);font-size:18px;font-weight:800;
  letter-spacing:-0.03em;color:var(--black);text-decoration:none;
  display:flex;align-items:center;gap:8px;
}
.nav-logo span{
  display:inline-block;width:28px;height:28px;background:var(--black);
  border-radius:8px;display:flex;align-items:center;justify-content:center;
}
.nav-logo span svg{width:14px;height:14px;fill:#fff;}
.nav-pills{display:flex;gap:4px;background:var(--gray-100);border-radius:50px;padding:4px;}
.nav-pill{
  padding:7px 18px;border-radius:50px;font-size:13px;font-weight:500;
  color:var(--gray-600);cursor:pointer;border:none;background:transparent;
  transition:var(--transition);white-space:nowrap;font-family:var(--font-body);
}
.nav-pill.active,.nav-pill:hover{background:#fff;color:var(--black);box-shadow:0 1px 6px rgba(0,0,0,0.1);}
.nav-search{
  display:flex;align-items:center;gap:8px;
  background:var(--gray-100);border-radius:50px;padding:8px 16px;
  border:1px solid transparent;transition:var(--transition);
}
.nav-search:focus-within{background:#fff;border-color:var(--gray-200);box-shadow:0 2px 12px rgba(0,0,0,0.08);}
.nav-search svg{width:15px;height:15px;stroke:var(--gray-400);flex-shrink:0;}
.nav-search input{border:none;background:transparent;outline:none;font-size:14px;color:var(--black);width:160px;font-family:var(--font-body);}
.nav-search input::placeholder{color:var(--gray-400);}

/* ── HERO ── */
.hero{
  padding-top:var(--nav-h);
  min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;
  text-align:center;
  background:radial-gradient(ellipse 80% 60% at 50% 0%,rgba(99,102,241,0.07) 0%,transparent 70%),
             radial-gradient(ellipse 60% 40% at 80% 80%,rgba(6,182,212,0.05) 0%,transparent 60%),
             var(--white);
  padding-left:40px;padding-right:40px;padding-bottom:80px;
  position:relative;overflow:hidden;
}
.hero::before{
  content:'';position:absolute;top:0;left:0;right:0;height:1px;
  background:linear-gradient(90deg,transparent,rgba(99,102,241,0.3),rgba(6,182,212,0.3),transparent);
}
.hero-badge{
  display:inline-flex;align-items:center;gap:6px;
  background:var(--gray-100);border:1px solid var(--gray-200);
  border-radius:50px;padding:6px 14px;font-size:12px;font-weight:500;
  color:var(--gray-600);margin-bottom:32px;
  animation:fadeDown 0.7s ease both;
}
.hero-badge .dot{width:6px;height:6px;border-radius:50%;background:#22c55e;animation:pulse 2s infinite;}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.4;}}
.hero-title{
  font-family:var(--font-display);
  font-size:clamp(52px,9vw,100px);
  font-weight:800;letter-spacing:-0.04em;line-height:0.95;
  color:var(--black);margin-bottom:24px;
  animation:fadeDown 0.7s ease 0.1s both;
}
.hero-title .accent-word{
  background:linear-gradient(135deg,var(--accent-1),var(--accent-3));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
}
.hero-sub{
  font-size:clamp(16px,2vw,20px);color:var(--gray-600);font-weight:400;
  max-width:560px;line-height:1.6;margin-bottom:48px;
  animation:fadeDown 0.7s ease 0.2s both;
}
.hero-stats{
  display:flex;gap:48px;justify-content:center;margin-bottom:60px;
  animation:fadeDown 0.7s ease 0.3s both;
}
.stat{text-align:center;}
.stat-n{font-family:var(--font-display);font-size:40px;font-weight:800;letter-spacing:-0.03em;color:var(--black);}
.stat-l{font-size:13px;color:var(--gray-400);font-weight:400;margin-top:2px;}
.hero-btns{display:flex;gap:12px;justify-content:center;animation:fadeDown 0.7s ease 0.4s both;}
.btn-primary{
  padding:14px 32px;background:var(--black);color:#fff;
  border:none;border-radius:50px;font-size:15px;font-weight:500;
  cursor:pointer;font-family:var(--font-body);
  transition:var(--transition);display:flex;align-items:center;gap:8px;
}
.btn-primary:hover{background:var(--gray-800);transform:translateY(-2px);box-shadow:0 8px 25px rgba(0,0,0,0.2);}
.btn-secondary{
  padding:14px 32px;background:transparent;color:var(--black);
  border:1.5px solid var(--gray-200);border-radius:50px;font-size:15px;font-weight:500;
  cursor:pointer;font-family:var(--font-body);transition:var(--transition);
}
.btn-secondary:hover{border-color:var(--gray-400);transform:translateY(-2px);}
.hero-scroll{
  position:absolute;bottom:32px;left:50%;transform:translateX(-50%);
  display:flex;flex-direction:column;align-items:center;gap:8px;animation:fadeDown 0.7s ease 0.6s both;
}
.hero-scroll span{font-size:11px;color:var(--gray-400);letter-spacing:0.12em;text-transform:uppercase;}
.scroll-line{width:1px;height:32px;background:linear-gradient(to bottom,var(--gray-400),transparent);animation:scrollAnim 1.8s ease infinite;}
@keyframes scrollAnim{0%,100%{transform:scaleY(1);opacity:0.6;}50%{transform:scaleY(0.5);opacity:1;}}
@keyframes fadeDown{from{opacity:0;transform:translateY(-16px);}to{opacity:1;transform:translateY(0);}}

/* ── MATERIAS BANNER ── */
.materias-bar{
  background:var(--black);padding:0 40px;overflow:hidden;
  border-top:1px solid rgba(255,255,255,0.08);
  border-bottom:1px solid rgba(255,255,255,0.08);
}
.materias-track{
  display:flex;gap:0;
  animation:marquee 30s linear infinite;
  width:max-content;
}
.materia-item{
  padding:18px 48px;font-family:var(--font-display);font-size:13px;font-weight:600;
  letter-spacing:0.1em;text-transform:uppercase;color:rgba(255,255,255,0.5);
  border-right:1px solid rgba(255,255,255,0.1);white-space:nowrap;
  display:flex;align-items:center;gap:10px;
}
.materia-item .mi-dot{width:6px;height:6px;border-radius:50%;}
@keyframes marquee{from{transform:translateX(0);}to{transform:translateX(-50%);}}

/* ── SECTIONS ── */
.section{padding:100px 40px;max-width:1200px;margin:0 auto;}
.section-header{text-align:center;margin-bottom:64px;}
.section-eyebrow{
  font-size:12px;font-weight:600;letter-spacing:0.15em;text-transform:uppercase;
  margin-bottom:16px;display:inline-flex;align-items:center;gap:8px;
}
.section-eyebrow::before,.section-eyebrow::after{content:'';flex:1;height:1px;background:currentColor;opacity:0.25;width:24px;}
.section-title{
  font-family:var(--font-display);font-size:clamp(36px,5vw,60px);
  font-weight:800;letter-spacing:-0.03em;line-height:1;margin-bottom:16px;
}
.section-desc{font-size:17px;color:var(--gray-600);max-width:480px;margin:0 auto;line-height:1.6;}

/* ── GRID ── */
.cards-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(280px,1fr));
  gap:16px;
}

/* ── CARD ── */
.term-card{
  background:var(--white);
  border:1px solid var(--gray-200);
  border-radius:var(--radius-card);
  padding:28px;
  cursor:pointer;
  transition:var(--transition);
  position:relative;overflow:hidden;
  box-shadow:var(--shadow-card);
}
.term-card::before{
  content:'';position:absolute;inset:0;
  opacity:0;transition:opacity 0.35s;border-radius:var(--radius-card);
}
.term-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-hover);border-color:transparent;}
.term-card:hover::before{opacity:1;}

/* Materia colores */
.mat-algo::before{background:linear-gradient(135deg,rgba(0,113,227,0.06),rgba(29,78,216,0.06));}
.mat-algo:hover{border-color:rgba(0,113,227,0.2);}
.mat-algo .card-icon-bg{background:rgba(0,113,227,0.1);color:var(--mat-1);}
.mat-algo .card-tag{background:rgba(0,113,227,0.1);color:var(--mat-1);}
.mat-algo .card-num{color:var(--mat-1);}

.mat-tgs::before{background:linear-gradient(135deg,rgba(5,150,105,0.06),rgba(4,120,87,0.06));}
.mat-tgs:hover{border-color:rgba(5,150,105,0.2);}
.mat-tgs .card-icon-bg{background:rgba(5,150,105,0.1);color:var(--mat-tgs);}
.mat-tgs .card-tag{background:rgba(5,150,105,0.1);color:var(--mat-tgs);}
.mat-tgs .card-num{color:var(--mat-tgs);}

.mat-agil::before{background:linear-gradient(135deg,rgba(220,38,38,0.06),rgba(185,28,28,0.06));}
.mat-agil:hover{border-color:rgba(220,38,38,0.2);}
.mat-agil .card-icon-bg{background:rgba(220,38,38,0.1);color:var(--mat-agil);}
.mat-agil .card-tag{background:rgba(220,38,38,0.1);color:var(--mat-agil);}
.mat-agil .card-num{color:var(--mat-agil);}

.card-top{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:20px;}
.card-icon-bg{
  width:44px;height:44px;border-radius:12px;
  display:flex;align-items:center;justify-content:center;
  font-size:20px;flex-shrink:0;
}
.card-num{font-family:var(--font-display);font-size:13px;font-weight:700;opacity:0.5;}
.card-term{
  font-family:var(--font-display);font-size:22px;font-weight:800;
  letter-spacing:-0.02em;line-height:1.1;margin-bottom:10px;color:var(--black);
}
.card-hint{font-size:13px;color:var(--gray-400);line-height:1.4;margin-bottom:20px;}
.card-footer{display:flex;align-items:center;justify-content:space-between;}
.card-tag{font-size:11px;font-weight:600;padding:4px 10px;border-radius:50px;letter-spacing:0.05em;}
.card-arrow{
  width:32px;height:32px;border-radius:50%;
  background:var(--gray-100);border:none;cursor:pointer;
  display:flex;align-items:center;justify-content:center;
  transition:var(--transition);flex-shrink:0;
}
.term-card:hover .card-arrow{background:var(--black);color:#fff;}
.card-arrow svg{width:14px;height:14px;stroke:currentColor;stroke-width:2;fill:none;transition:var(--transition);}

/* ── MODAL ── */
.modal-overlay{
  position:fixed;inset:0;background:rgba(0,0,0,0.5);
  backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);
  z-index:2000;display:flex;align-items:center;justify-content:center;
  padding:20px;opacity:0;pointer-events:none;transition:opacity 0.3s ease;
}
.modal-overlay.open{opacity:1;pointer-events:all;}
.modal{
  background:#fff;border-radius:28px;max-width:600px;width:100%;
  max-height:85vh;overflow-y:auto;
  box-shadow:0 40px 100px rgba(0,0,0,0.25);
  transform:scale(0.94) translateY(20px);
  transition:transform 0.35s cubic-bezier(0.34,1.56,0.64,1);
}
.modal-overlay.open .modal{transform:scale(1) translateY(0);}
.modal-header{padding:32px 32px 0;display:flex;align-items:flex-start;justify-content:space-between;gap:16px;}
.modal-icon{
  width:56px;height:56px;border-radius:16px;
  display:flex;align-items:center;justify-content:center;font-size:26px;flex-shrink:0;
}
.modal-close{
  width:36px;height:36px;border-radius:50%;background:var(--gray-100);
  border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;
  flex-shrink:0;transition:var(--transition);
}
.modal-close:hover{background:var(--gray-200);}
.modal-close svg{width:16px;height:16px;stroke:var(--gray-600);stroke-width:2;fill:none;}
.modal-meta{flex:1;}
.modal-tag{font-size:11px;font-weight:600;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:6px;}
.modal-term{font-family:var(--font-display);font-size:30px;font-weight:800;letter-spacing:-0.03em;line-height:1.1;}
.modal-body{padding:24px 32px 32px;}
.modal-loading{
  display:flex;flex-direction:column;align-items:center;gap:16px;padding:32px 0;
}
.loader{
  width:36px;height:36px;border-radius:50%;
  border:2px solid var(--gray-200);border-top-color:var(--black);
  animation:spin 0.8s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg);}}
.loader-text{font-size:14px;color:var(--gray-400);}
.modal-content-area{}
.modal-section{margin-bottom:24px;}
.modal-section:last-child{margin-bottom:0;}
.modal-section-title{
  font-size:11px;font-weight:600;letter-spacing:0.1em;text-transform:uppercase;
  color:var(--gray-400);margin-bottom:10px;
  padding-bottom:8px;border-bottom:1px solid var(--gray-100);
}
.modal-definition{
  font-size:16px;line-height:1.7;color:var(--gray-800);
}
.modal-example{
  background:var(--gray-50);border-radius:12px;padding:16px;
  font-size:14px;line-height:1.6;color:var(--gray-600);
  border-left:3px solid var(--gray-200);
}
.modal-keywords{display:flex;flex-wrap:wrap;gap:8px;}
.kw-pill{
  padding:6px 12px;border-radius:50px;font-size:12px;font-weight:500;
  background:var(--gray-100);color:var(--gray-600);
}
.modal-error{
  text-align:center;padding:24px 0;
  font-size:15px;color:var(--gray-600);
}
.modal-error .err-icon{font-size:36px;margin-bottom:12px;}
.retry-btn{
  margin-top:12px;padding:10px 24px;background:var(--black);color:#fff;
  border:none;border-radius:50px;font-size:14px;cursor:pointer;
  font-family:var(--font-body);transition:var(--transition);
}
.retry-btn:hover{opacity:0.85;}

/* ── ABOUT STRIP ── */
.about-strip{
  background:var(--black);color:#fff;
  padding:100px 40px;text-align:center;position:relative;overflow:hidden;
}
.about-strip::before{
  content:'GLOSARIO';
  position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);
  font-family:var(--font-display);font-size:200px;font-weight:800;
  color:rgba(255,255,255,0.03);letter-spacing:-0.05em;white-space:nowrap;pointer-events:none;
}
.about-inner{position:relative;z-index:1;max-width:700px;margin:0 auto;}
.about-strip .section-title{color:#fff;}
.about-strip .section-desc{color:rgba(255,255,255,0.5);}
.about-chips{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin-top:40px;}
.chip{
  padding:10px 20px;border:1px solid rgba(255,255,255,0.15);border-radius:50px;
  font-size:13px;font-weight:500;color:rgba(255,255,255,0.7);
  transition:var(--transition);cursor:default;
}
.chip:hover{background:rgba(255,255,255,0.08);color:#fff;}

/* ── FOOTER ── */
footer{
  border-top:1px solid var(--gray-200);padding:40px;
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:16px;
}
.footer-logo{font-family:var(--font-display);font-size:16px;font-weight:800;letter-spacing:-0.02em;}
.footer-copy{font-size:13px;color:var(--gray-400);}
.footer-credit{font-size:13px;color:var(--gray-400);}
.footer-credit strong{color:var(--black);}

/* ── SEARCH FILTER ── */
.search-filter-bar{
  max-width:480px;margin:0 auto 48px;
  display:flex;align-items:center;gap:10px;
  background:var(--gray-100);border-radius:50px;
  padding:10px 20px;border:1px solid transparent;
  transition:var(--transition);
}
.search-filter-bar:focus-within{background:#fff;border-color:var(--gray-200);box-shadow:0 4px 20px rgba(0,0,0,0.08);}
.search-filter-bar svg{width:16px;height:16px;stroke:var(--gray-400);flex-shrink:0;}
.search-filter-bar input{flex:1;border:none;background:transparent;outline:none;font-size:15px;font-family:var(--font-body);}
.search-filter-bar input::placeholder{color:var(--gray-400);}
.no-results{text-align:center;padding:48px;color:var(--gray-400);font-size:15px;}

/* ── RESPONSIVE ── */
@media(max-width:768px){
  nav{padding:0 20px;}
  .nav-pills{display:none;}
  .hero-stats{gap:28px;}
  .section{padding:64px 20px;}
  .cards-grid{grid-template-columns:1fr;}
  .about-strip{padding:64px 20px;}
  footer{flex-direction:column;align-items:center;text-align:center;padding:32px 20px;}
}

/* ── REVEAL ── */
.reveal{opacity:0;transform:translateY(24px);transition:opacity 0.6s ease,transform 0.6s ease;}
.reveal.visible{opacity:1;transform:translateY(0);}
.reveal-delay-1{transition-delay:0.08s;}
.reveal-delay-2{transition-delay:0.16s;}
.reveal-delay-3{transition-delay:0.24s;}
</style>
</head>
<body>

<!-- ── NAV ── -->
<nav>
  <a class="nav-logo" href="#">
    <span>
      <svg viewBox="0 0 14 14"><path d="M7 1L13 4V10L7 13L1 10V4Z"/></svg>
    </span>
    GlosarioIA
  </a>
  <div class="nav-pills">
    <button class="nav-pill active" onclick="scrollToSection('algo')">Algoritmos</button>
    <button class="nav-pill" onclick="scrollToSection('tgs')">T. de Sistemas</button>
    <button class="nav-pill" onclick="scrollToSection('agil')">Met. Ágiles</button>
  </div>
  <div class="nav-search">
    <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input id="globalSearch" type="text" placeholder="Buscar término..." oninput="filterGlobal(this.value)">
  </div>
</nav>

<!-- ── HERO ── -->
<section class="hero" id="top">
  <div class="hero-badge"><span class="dot"></span> Powered by Claude IA · 3 materias</div>
  <h1 class="hero-title">Glosario<br><span class="accent-word">Interactivo</span></h1>
  <p class="hero-sub">Haz clic en cualquier tarjeta y la IA generará una definición completa, ejemplo y palabras clave al instante.</p>
  <div class="hero-stats">
    <div class="stat"><div class="stat-n">28</div><div class="stat-l">Términos</div></div>
    <div class="stat"><div class="stat-n">3</div><div class="stat-l">Materias</div></div>
    <div class="stat"><div class="stat-n">IA</div><div class="stat-l">Definiciones</div></div>
  </div>
  <div class="hero-btns">
    <button class="btn-primary" onclick="scrollToSection('algo')">
      Explorar términos
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </button>
    <button class="btn-secondary" onclick="scrollToSection('about')">¿Cómo funciona?</button>
  </div>
  <div class="hero-scroll">
    <span>Scroll</span>
    <div class="scroll-line"></div>
  </div>
</section>

<!-- ── MARQUEE ── -->
<div class="materias-bar">
  <div class="materias-track" id="marqueeTrack"></div>
</div>

<!-- ── SECCIÓN ALGORITMOS ── -->
<div style="background:var(--white);padding:80px 0 0;" id="algo">
<div class="section">
  <div class="section-header reveal">
    <div class="section-eyebrow" style="color:var(--mat-1);">01 / Algoritmos</div>
    <h2 class="section-title">Fundamentos de<br>Algoritmos</h2>
    <p class="section-desc">Los conceptos esenciales del pensamiento algorítmico y el ciclo de desarrollo.</p>
  </div>
  <div class="search-filter-bar reveal">
    <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input type="text" placeholder="Filtrar en esta sección..." oninput="filterSection('algo-grid', this.value)">
  </div>
  <div class="cards-grid" id="algo-grid"></div>
</div>
</div>

<!-- ── SECCIÓN TGS ── -->
<div style="background:var(--gray-50);padding:80px 0 0;" id="tgs">
<div class="section">
  <div class="section-header reveal">
    <div class="section-eyebrow" style="color:var(--mat-tgs);">02 / Teoría General de Sistemas</div>
    <h2 class="section-title">Teoría General<br>de Sistemas</h2>
    <p class="section-desc">Conceptos que explican cómo los sistemas interactúan con su entorno.</p>
  </div>
  <div class="search-filter-bar reveal">
    <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input type="text" placeholder="Filtrar en esta sección..." oninput="filterSection('tgs-grid', this.value)">
  </div>
  <div class="cards-grid" id="tgs-grid"></div>
</div>
</div>

<!-- ── SECCIÓN ÁGIL ── -->
<div style="background:var(--white);padding:80px 0 0;" id="agil">
<div class="section">
  <div class="section-header reveal">
    <div class="section-eyebrow" style="color:var(--mat-agil);">03 / Metodologías Ágiles</div>
    <h2 class="section-title">Metodologías<br>Ágiles</h2>
    <p class="section-desc">Marcos de trabajo modernos para el desarrollo ágil de software.</p>
  </div>
  <div class="search-filter-bar reveal">
    <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input type="text" placeholder="Filtrar en esta sección..." oninput="filterSection('agil-grid', this.value)">
  </div>
  <div class="cards-grid" id="agil-grid"></div>
</div>
</div>

<!-- ── ABOUT STRIP ── -->
<section class="about-strip" id="about">
  <div class="about-inner">
    <div class="section-header">
      <div class="section-eyebrow" style="color:rgba(255,255,255,0.4);">¿Cómo funciona?</div>
      <h2 class="section-title">IA que define<br>en tiempo real</h2>
      <p class="section-desc">Cada vez que haces clic en una tarjeta, se consulta a Claude — una IA avanzada — que genera una definición personalizada, un ejemplo práctico y palabras clave del término.</p>
    </div>
    <div class="about-chips">
      <div class="chip">⚡ Respuesta instantánea</div>
      <div class="chip">📖 Definición completa</div>
      <div class="chip">💡 Ejemplo práctico</div>
      <div class="chip">🏷️ Palabras clave</div>
      <div class="chip">🤖 Powered by Claude</div>
      <div class="chip">🎓 Enfoque académico</div>
    </div>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <div class="footer-logo">GlosarioIA</div>
  <div class="footer-copy">© 2025 · Glosario Interactivo con IA</div>
  <div class="footer-credit">Definiciones por <strong>Claude AI</strong></div>
</footer>

<!-- ── MODAL ── -->
<div class="modal-overlay" id="modalOverlay" onclick="closeModal(event)">
  <div class="modal" id="modal">
    <div class="modal-header">
      <div class="modal-icon" id="modalIcon"></div>
      <div class="modal-meta">
        <div class="modal-tag" id="modalTag"></div>
        <div class="modal-term" id="modalTerm"></div>
      </div>
      <button class="modal-close" onclick="closeModalDirect()">
        <svg viewBox="0 0 24 24"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>
      </button>
    </div>
    <div class="modal-body" id="modalBody">
      <div class="modal-loading"><div class="loader"></div><div class="loader-text">La IA está pensando...</div></div>
    </div>
  </div>
</div>

<script>
/* ═══════════════════════════════════════
   DATA
═══════════════════════════════════════ */
const DATA = {
  algo:{
    label:'Algoritmos',tag:'algo',color:'var(--mat-1)',bgClass:'mat-algo',
    tagLabel:'Algoritmos',
    terms:[
      {term:'Algoritmo',hint:'Secuencia ordenada de instrucciones',icon:'🔢'},
      {term:'Entrada',hint:'Datos que recibe un algoritmo',icon:'📥'},
      {term:'Proceso',hint:'Transformación de datos',icon:'⚙️'},
      {term:'Salida',hint:'Resultado del algoritmo',icon:'📤'},
      {term:'Planificación',hint:'Diseño previo a la solución',icon:'📋'},
      {term:'Edición',hint:'Escritura del código fuente',icon:'✏️'},
      {term:'Ejecutar y Compilar',hint:'Correr y traducir el programa',icon:'▶️'},
      {term:'Corregir',hint:'Depuración de errores',icon:'🐛'},
      {term:'Documentar',hint:'Registrar el funcionamiento del código',icon:'📝'},
    ]
  },
  tgs:{
    label:'T. General de Sistemas',tag:'tgs',color:'var(--mat-tgs)',bgClass:'mat-tgs',
    tagLabel:'T. de Sistemas',
    terms:[
      {term:'Sistema Abierto',hint:'Intercambia con su entorno',icon:'🔓'},
      {term:'Sistema Cerrado',hint:'No interactúa con el exterior',icon:'🔒'},
      {term:'Entorno',hint:'Contexto que rodea al sistema',icon:'🌐'},
      {term:'Entrada (Input)',hint:'Recursos que ingresan al sistema',icon:'⬇️'},
      {term:'Proceso (Process)',hint:'Transformación dentro del sistema',icon:'🔄'},
      {term:'Salida (Output)',hint:'Producto generado por el sistema',icon:'⬆️'},
      {term:'Retroalimentación (Feedback)',hint:'Información de retorno al sistema',icon:'🔁'},
      {term:'Sistema Natural',hint:'Existe sin intervención humana',icon:'🌿'},
      {term:'Sistema Artificial',hint:'Creado por el ser humano',icon:'🤖'},
      {term:'Sistema Social',hint:'Formado por personas e interacciones',icon:'👥'},
      {term:'Sistema Tecnológico',hint:'Basado en herramientas y técnicas',icon:'💻'},
      {term:'Sinergia',hint:'El todo es más que la suma de partes',icon:'✨'},
      {term:'Totalidad',hint:'El sistema actúa como un todo',icon:'🎯'},
      {term:'Inter-relación',hint:'Dependencia entre componentes',icon:'🔗'},
    ]
  },
  agil:{
    label:'Metodologías Ágiles',tag:'agil',color:'var(--mat-agil)',bgClass:'mat-agil',
    tagLabel:'Met. Ágiles',
    terms:[
      {term:'Metodologías Ágiles',hint:'Enfoques iterativos de desarrollo',icon:'🚀'},
      {term:'SCRUM',hint:'Marco ágil basado en sprints',icon:'🏉'},
      {term:'Entregables',hint:'Producto terminado por sprint',icon:'📦'},
      {term:'Sprint',hint:'Ciclo de desarrollo corto',icon:'⏱️'},
      {term:'Backlog',hint:'Lista priorizada de tareas',icon:'📋'},
      {term:'XP – Programación Extrema',hint:'Ágil centrado en calidad de código',icon:'⚡'},
      {term:'RAD – Desarrollo Rápido',hint:'Prototipado y entregas veloz',icon:'🏎️'},
    ]
  }
};

/* ═══════════════════════════════════════
   RENDER CARDS
═══════════════════════════════════════ */
function renderCards(){
  Object.entries(DATA).forEach(([key,mat])=>{
    const grid=document.getElementById(key+'-grid');
    mat.terms.forEach((t,i)=>{
      const num=String(i+1).padStart(2,'0');
      const card=document.createElement('div');
      card.className=`term-card ${mat.bgClass} reveal reveal-delay-${(i%3)+1}`;
      card.dataset.term=t.term.toLowerCase();
      card.innerHTML=`
        <div class="card-top">
          <div class="card-icon-bg">${t.icon}</div>
          <span class="card-num">${num}</span>
        </div>
        <div class="card-term">${t.term}</div>
        <div class="card-hint">${t.hint}</div>
        <div class="card-footer">
          <span class="card-tag">${mat.tagLabel}</span>
          <button class="card-arrow" aria-label="Ver definición">
            <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
          </button>
        </div>`;
      card.addEventListener('click',()=>openModal(t,mat));
      grid.appendChild(card);
    });
  });
  setupReveal();
}

/* ═══════════════════════════════════════
   MARQUEE
═══════════════════════════════════════ */
function buildMarquee(){
  const track=document.getElementById('marqueeTrack');
  const colors={algo:'#60a5fa',tgs:'#34d399',agil:'#f87171'};
  const items=[
    ...DATA.algo.terms.map(t=>({t:t.term,c:colors.algo})),
    ...DATA.tgs.terms.map(t=>({t:t.term,c:colors.tgs})),
    ...DATA.agil.terms.map(t=>({t:t.term,c:colors.agil}))
  ];
  const doubled=[...items,...items];
  doubled.forEach(({t,c})=>{
    const el=document.createElement('div');
    el.className='materia-item';
    el.innerHTML=`<span class="mi-dot" style="background:${c}"></span>${t}`;
    track.appendChild(el);
  });
}

/* ═══════════════════════════════════════
   MODAL
═══════════════════════════════════════ */
let currentRequest=null;

async function openModal(term,mat){
  const overlay=document.getElementById('modalOverlay');
  const icon=document.getElementById('modalIcon');
  const tag=document.getElementById('modalTag');
  const termEl=document.getElementById('modalTerm');
  const body=document.getElementById('modalBody');

  icon.textContent=term.icon;
  icon.className=`modal-icon ${mat.bgClass}`;
  icon.style.background=`rgba(0,0,0,0.06)`;

  tag.textContent=mat.tagLabel;
  tag.style.color=mat.color;
  termEl.textContent=term.term;

  body.innerHTML=`<div class="modal-loading"><div class="loader"></div><div class="loader-text">La IA está generando la definición...</div></div>`;
  overlay.classList.add('open');
  document.body.style.overflow='hidden';

  try{
    const def=await fetchDefinition(term.term,mat.label);
    renderDefinition(body,def);
  }catch(e){
    body.innerHTML=`
      <div class="modal-error">
        <div class="err-icon">⚠️</div>
        <div>No se pudo obtener la definición. Verifica tu conexión.</div>
        <button class="retry-btn" onclick="retryModal()">Reintentar</button>
      </div>`;
    body._retryData={term,mat};
  }
}

function retryModal(){
  const body=document.getElementById('modalBody');
  if(body._retryData){
    const {term,mat}=body._retryData;
    openModal(term,mat);
  }
}

async function fetchDefinition(termName,materia){
  const prompt=`Eres un docente universitario experto explicando el término "${termName}" en el contexto de la materia "${materia}".

Responde ÚNICAMENTE con un JSON válido con esta estructura exacta (sin markdown, sin backticks, sin texto extra):
{
  "definicion": "Definición clara y completa en 2-3 oraciones, en español, nivel universitario.",
  "ejemplo": "Un ejemplo concreto y práctico de 1-2 oraciones que ilustre el concepto.",
  "palabras_clave": ["palabra1","palabra2","palabra3","palabra4","palabra5"]
}`;

  const res=await fetch('https://api.anthropic.com/v1/messages',{
    method:'POST',
    headers:{'Content-Type':'application/json'},
    body:JSON.stringify({
      model:'claude-sonnet-4-20250514',
      max_tokens:1000,
      messages:[{role:'user',content:prompt}]
    })
  });

  if(!res.ok) throw new Error('API error '+res.status);
  const data=await res.json();
  const raw=data.content.map(b=>b.text||'').join('');
  const clean=raw.replace(/```json|```/g,'').trim();
  return JSON.parse(clean);
}

function renderDefinition(body,def){
  body.innerHTML=`
    <div class="modal-content-area">
      <div class="modal-section">
        <div class="modal-section-title">📖 Definición</div>
        <p class="modal-definition">${def.definicion}</p>
      </div>
      <div class="modal-section">
        <div class="modal-section-title">💡 Ejemplo práctico</div>
        <div class="modal-example">${def.ejemplo}</div>
      </div>
      <div class="modal-section">
        <div class="modal-section-title">🏷️ Palabras clave</div>
        <div class="modal-keywords">${def.palabras_clave.map(k=>`<span class="kw-pill">${k}</span>`).join('')}</div>
      </div>
    </div>`;
}

function closeModal(e){
  if(e.target===document.getElementById('modalOverlay')) closeModalDirect();
}
function closeModalDirect(){
  document.getElementById('modalOverlay').classList.remove('open');
  document.body.style.overflow='';
}
document.addEventListener('keydown',e=>{if(e.key==='Escape') closeModalDirect();});

/* ═══════════════════════════════════════
   SEARCH / FILTER
═══════════════════════════════════════ */
function filterSection(gridId,query){
  const grid=document.getElementById(gridId);
  const q=query.toLowerCase().trim();
  let any=false;
  grid.querySelectorAll('.term-card').forEach(card=>{
    const match=!q||card.dataset.term.includes(q);
    card.style.display=match?'':'none';
    if(match) any=true;
  });
  let nr=grid.nextElementSibling;
  if(nr&&nr.classList.contains('no-results')) nr.remove();
  if(!any&&q){
    const el=document.createElement('div');
    el.className='no-results';
    el.textContent='No se encontraron términos para "'+query+'"';
    grid.after(el);
  }
}

function filterGlobal(query){
  const q=query.toLowerCase().trim();
  if(!q){['algo-grid','tgs-grid','agil-grid'].forEach(id=>{
    document.getElementById(id).querySelectorAll('.term-card').forEach(c=>c.style.display='');
  });return;}
  ['algo-grid','tgs-grid','agil-grid'].forEach(id=>{
    document.getElementById(id).querySelectorAll('.term-card').forEach(card=>{
      card.style.display=card.dataset.term.includes(q)?'':'none';
    });
  });
}

/* ═══════════════════════════════════════
   SCROLL & REVEAL
═══════════════════════════════════════ */
function scrollToSection(id){
  const el=document.getElementById(id);
  if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
}

function setupReveal(){
  const obs=new IntersectionObserver(entries=>{
    entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target);}});
  },{threshold:0.1});
  document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
}

/* ═══════════════════════════════════════
   INIT
═══════════════════════════════════════ */
renderCards();
buildMarquee();
</script>
</body>
</html>
