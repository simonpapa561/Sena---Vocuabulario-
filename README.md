<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Glosario Interactivo IA</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --black:#1d1d1f;
  --white:#fff;
  --gray-50:#fbfbfd;
  --gray-100:#f5f5f7;
  --gray-200:#e8e8ed;
  --gray-300:#d2d2d7;
  --gray-400:#86868b;
  --gray-600:#515154;
  --gray-800:#1d1d1f;
  --blue:#0071e3;
  --mat-algo:#0071e3;
  --mat-tgs:#1c8c4e;
  --mat-agil:#c0392b;
  --nav-h:52px;
  --r:18px;
  --font:-apple-system,BlinkMacSystemFont,'Inter','Helvetica Neue',Helvetica,Arial,sans-serif;
  --ease:cubic-bezier(0.4,0,0.2,1);
}
html{scroll-behavior:smooth;}
body{
  background:var(--gray-50);
  color:var(--black);
  font-family:var(--font);
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  overflow-x:hidden;
  font-size:17px;
  line-height:1.47059;
  letter-spacing:-0.022em;
}
::selection{background:#0071e3;color:#fff;}
::-webkit-scrollbar{width:6px;}
::-webkit-scrollbar-track{background:#f5f5f7;}
::-webkit-scrollbar-thumb{background:#d2d2d7;border-radius:3px;}

/* NAV */
nav{
  position:fixed;top:0;left:0;width:100%;height:var(--nav-h);
  background:rgba(255,255,255,0.8);
  backdrop-filter:saturate(180%) blur(20px);
  -webkit-backdrop-filter:saturate(180%) blur(20px);
  border-bottom:1px solid rgba(0,0,0,0.12);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 22px;z-index:9000;
}
.nav-logo{
  font-size:21px;font-weight:600;
  letter-spacing:0.004em;
  color:var(--black);text-decoration:none;
  display:flex;align-items:center;gap:8px;flex-shrink:0;
}
.nav-logo-icon{
  width:30px;height:30px;background:var(--black);
  border-radius:8px;display:flex;align-items:center;justify-content:center;
  flex-shrink:0;
}
.nav-logo-icon svg{width:16px;height:16px;fill:#fff;}
.nav-pills{
  display:flex;gap:2px;
  background:rgba(0,0,0,0.05);
  border-radius:980px;padding:3px;
  position:absolute;left:50%;transform:translateX(-50%);
}
.nav-pill{
  padding:6px 16px;border-radius:980px;
  font-size:13px;font-weight:400;letter-spacing:-0.01em;
  color:var(--gray-600);cursor:pointer;border:none;background:transparent;
  transition:all 0.22s var(--ease);white-space:nowrap;
  font-family:var(--font);
}
.nav-pill.active,.nav-pill:hover{
  background:#fff;color:var(--black);
  box-shadow:0 1px 4px rgba(0,0,0,0.12),0 2px 8px rgba(0,0,0,0.06);
}
.nav-right{
  display:flex;align-items:center;gap:10px;flex-shrink:0;
}
.nav-search{
  display:flex;align-items:center;gap:8px;
  background:rgba(0,0,0,0.06);
  border-radius:980px;padding:6px 14px;
  border:1px solid transparent;
  transition:all 0.22s var(--ease);min-width:200px;
}
.nav-search:focus-within{
  background:#fff;
  border-color:var(--gray-300);
  box-shadow:0 0 0 3px rgba(0,113,227,0.2);
}
.nav-search svg{width:14px;height:14px;stroke:var(--gray-400);stroke-width:2;fill:none;flex-shrink:0;}
.nav-search input{
  border:none;background:transparent;outline:none;
  font-size:14px;color:var(--black);width:100%;
  font-family:var(--font);letter-spacing:-0.01em;
}
.nav-search input::placeholder{color:var(--gray-400);}

/* HERO */
.hero{
  padding-top:calc(var(--nav-h) + 80px);
  padding-bottom:100px;
  text-align:center;
  background:#fff;
  padding-left:24px;padding-right:24px;
  border-bottom:1px solid var(--gray-200);
}
.hero-eyebrow{
  font-size:14px;font-weight:400;letter-spacing:0.01em;
  color:var(--blue);margin-bottom:10px;
  display:flex;align-items:center;justify-content:center;gap:6px;
}
.hero-eyebrow .dot{width:6px;height:6px;border-radius:50%;background:#22c55e;display:inline-block;}
.hero-title{
  font-size:clamp(48px,7vw,80px);
  font-weight:700;
  letter-spacing:-0.025em;
  line-height:1.05;
  color:var(--black);
  margin-bottom:16px;
}
.hero-title-blue{color:var(--blue);}
.hero-sub{
  font-size:clamp(17px,2vw,21px);
  font-weight:400;
  color:var(--gray-600);
  max-width:520px;
  margin:0 auto 40px;
  line-height:1.47059;
  letter-spacing:-0.022em;
}
.hero-stats{
  display:flex;gap:40px;justify-content:center;
  margin-bottom:44px;
}
.stat-n{
  font-size:40px;font-weight:700;letter-spacing:-0.03em;
  color:var(--black);line-height:1;
}
.stat-l{font-size:14px;color:var(--gray-400);margin-top:4px;font-weight:400;}
.hero-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;}
.btn-blue{
  padding:12px 24px;
  background:var(--blue);color:#fff;
  border:none;border-radius:980px;
  font-size:15px;font-weight:400;letter-spacing:-0.01em;
  cursor:pointer;font-family:var(--font);
  transition:all 0.22s var(--ease);
  display:inline-flex;align-items:center;gap:6px;
}
.btn-blue:hover{background:#0077ed;transform:scale(1.01);}
.btn-blue:active{transform:scale(0.98);}
.btn-outline{
  padding:12px 24px;
  background:transparent;color:var(--blue);
  border:1.5px solid var(--blue);
  border-radius:980px;font-size:15px;font-weight:400;letter-spacing:-0.01em;
  cursor:pointer;font-family:var(--font);transition:all 0.22s var(--ease);
}
.btn-outline:hover{background:rgba(0,113,227,0.05);}

/* SECTION */
.section-wrap{padding:0 24px 80px;max-width:1200px;margin:0 auto;}
.section-header{
  text-align:center;
  padding:72px 0 48px;
}
.eyebrow{
  font-size:12px;font-weight:600;letter-spacing:0.08em;
  text-transform:uppercase;margin-bottom:10px;
}
.section-title{
  font-size:clamp(32px,4vw,52px);
  font-weight:700;letter-spacing:-0.025em;
  line-height:1.07143;
  color:var(--black);margin-bottom:12px;
}
.section-desc{
  font-size:17px;color:var(--gray-600);
  max-width:480px;margin:0 auto;
  line-height:1.47059;letter-spacing:-0.022em;
}

/* FILTER BAR */
.filter-bar{
  display:flex;align-items:center;gap:8px;
  background:rgba(0,0,0,0.05);
  border-radius:12px;padding:10px 16px;
  border:1px solid transparent;
  transition:all 0.22s var(--ease);
  max-width:440px;margin:0 auto 36px;
}
.filter-bar:focus-within{background:#fff;border-color:var(--gray-300);box-shadow:0 0 0 3px rgba(0,113,227,0.15);}
.filter-bar svg{width:15px;height:15px;stroke:var(--gray-400);stroke-width:2;fill:none;flex-shrink:0;}
.filter-bar input{flex:1;border:none;background:transparent;outline:none;font-size:15px;font-family:var(--font);color:var(--black);letter-spacing:-0.01em;}
.filter-bar input::placeholder{color:var(--gray-400);}

/* GRID */
.cards-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(290px,1fr));
  gap:0;
  border-radius:var(--r);
  overflow:hidden;
  border:1px solid var(--gray-200);
}
.term-card{
  background:#fff;
  padding:28px 24px;
  cursor:pointer;
  transition:background 0.18s var(--ease);
  position:relative;
  border-right:1px solid var(--gray-200);
  border-bottom:1px solid var(--gray-200);
}
.term-card:hover{background:var(--gray-50);}
.card-icon{font-size:28px;margin-bottom:16px;display:block;line-height:1;}
.card-term{
  font-size:19px;font-weight:600;
  letter-spacing:-0.022em;
  color:var(--black);margin-bottom:6px;
  line-height:1.21053;
}
.card-hint{
  font-size:14px;color:var(--gray-400);
  line-height:1.42857;letter-spacing:-0.01em;
  margin-bottom:20px;
}
.card-footer{display:flex;align-items:center;justify-content:space-between;gap:8px;}
.card-badge{
  font-size:11px;font-weight:500;letter-spacing:0.04em;
  text-transform:uppercase;padding:4px 10px;border-radius:980px;flex-shrink:0;
}
.badge-algo{background:rgba(0,113,227,0.1);color:var(--mat-algo);}
.badge-tgs{background:rgba(28,140,78,0.1);color:var(--mat-tgs);}
.badge-agil{background:rgba(192,57,43,0.1);color:var(--mat-agil);}
.card-cta{
  font-size:14px;font-weight:400;
  color:var(--blue);
  display:flex;align-items:center;gap:3px;
  white-space:nowrap;
  transition:gap 0.18s var(--ease);
}
.term-card:hover .card-cta{gap:6px;}
.card-cta svg{width:14px;height:14px;stroke:currentColor;stroke-width:2;fill:none;flex-shrink:0;}

/* BG alternates */
.bg-white{background:#fff;}
.bg-gray{background:var(--gray-50);}

/* ABOUT */
.about-section{
  background:var(--black);color:#fff;
  padding:100px 24px;text-align:center;
}
.about-section .section-title{color:#fff;}
.about-section .section-desc{color:rgba(255,255,255,0.6);}
.about-section .eyebrow{color:rgba(255,255,255,0.4);}
.chips{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin-top:36px;}
.chip{
  padding:8px 18px;
  border:1px solid rgba(255,255,255,0.2);
  border-radius:980px;font-size:14px;
  color:rgba(255,255,255,0.7);
  transition:all 0.18s var(--ease);
}
.chip:hover{background:rgba(255,255,255,0.08);color:#fff;}

/* FOOTER */
footer{
  background:#f5f5f7;
  border-top:1px solid var(--gray-200);
  padding:32px 24px;
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:12px;
}
.footer-logo{font-size:17px;font-weight:600;letter-spacing:-0.022em;color:var(--black);}
.footer-txt{font-size:13px;color:var(--gray-400);}

/* MODAL */
.modal-overlay{
  position:fixed;inset:0;
  background:rgba(0,0,0,0.4);
  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);
  z-index:9999;
  display:flex;align-items:center;justify-content:center;
  padding:20px;
  opacity:0;pointer-events:none;
  transition:opacity 0.25s var(--ease);
}
.modal-overlay.open{opacity:1;pointer-events:all;}
.modal{
  background:#fff;
  border-radius:20px;
  max-width:580px;width:100%;
  max-height:88vh;
  overflow-y:auto;
  box-shadow:0 32px 80px rgba(0,0,0,0.22),0 2px 8px rgba(0,0,0,0.1);
  transform:translateY(24px) scale(0.97);
  transition:transform 0.3s cubic-bezier(0.34,1.2,0.64,1);
}
.modal-overlay.open .modal{transform:translateY(0) scale(1);}
.modal-top{
  padding:24px 24px 0;
  display:flex;align-items:flex-start;gap:14px;
}
.modal-icon-wrap{
  width:52px;height:52px;border-radius:14px;
  background:var(--gray-100);
  display:flex;align-items:center;justify-content:center;
  font-size:26px;flex-shrink:0;
}
.modal-meta{flex:1;}
.modal-materia{
  font-size:11px;font-weight:600;letter-spacing:0.08em;
  text-transform:uppercase;margin-bottom:4px;
}
.modal-term-name{
  font-size:28px;font-weight:700;
  letter-spacing:-0.025em;line-height:1.07143;color:var(--black);
}
.modal-close{
  width:32px;height:32px;border-radius:50%;
  background:var(--gray-100);border:none;
  cursor:pointer;display:flex;align-items:center;justify-content:center;
  flex-shrink:0;transition:background 0.18s;
}
.modal-close:hover{background:var(--gray-200);}
.modal-close svg{width:14px;height:14px;stroke:var(--gray-600);stroke-width:2;fill:none;}
.modal-body{padding:24px;}
.def-block{margin-bottom:20px;}
.def-label{
  font-size:11px;font-weight:600;letter-spacing:0.06em;
  text-transform:uppercase;
  margin-bottom:8px;
  display:flex;align-items:center;gap:6px;
}
.def-label::after{content:'';flex:1;height:1px;background:var(--gray-200);}
.def-text{
  font-size:16px;line-height:1.65;
  color:var(--gray-800);letter-spacing:-0.015em;
}
.def-example{
  background:var(--gray-50);border-radius:12px;
  padding:14px 16px;
  font-size:15px;line-height:1.55;
  color:var(--gray-600);
  border-left:3px solid var(--gray-300);
  letter-spacing:-0.01em;
}
.kw-row{display:flex;flex-wrap:wrap;gap:6px;}
.kw{
  padding:5px 12px;border-radius:980px;
  background:var(--gray-100);font-size:13px;
  color:var(--gray-600);font-weight:400;
}

/* Reveal */
.reveal{opacity:0;transform:translateY(20px);transition:opacity 0.5s var(--ease),transform 0.5s var(--ease);}
.reveal.visible{opacity:1;transform:translateY(0);}
.d1{transition-delay:0.05s;}.d2{transition-delay:0.1s;}.d3{transition-delay:0.15s;}
.no-results{text-align:center;padding:48px 24px;color:var(--gray-400);font-size:15px;}

@media(max-width:768px){
  nav{padding:0 16px;}
  .nav-pills{display:none;}
  .hero{padding-left:16px;padding-right:16px;}
  .hero-stats{gap:24px;}
  .stat-n{font-size:32px;}
  .section-wrap{padding:0 16px 60px;}
  .cards-grid{grid-template-columns:1fr;}
  footer{flex-direction:column;align-items:center;text-align:center;}
}
</style>
</head>
<body>

<nav>
  <a class="nav-logo" href="#">
    <div class="nav-logo-icon">
      <svg viewBox="0 0 16 16"><path d="M8 1L15 4.5V11.5L8 15L1 11.5V4.5Z"/></svg>
    </div>
    GlosarioIA
  </a>
  <div class="nav-pills">
    <button class="nav-pill active" onclick="goTo('sec-algo',this)">Algoritmos</button>
    <button class="nav-pill" onclick="goTo('sec-tgs',this)">T. de Sistemas</button>
    <button class="nav-pill" onclick="goTo('sec-agil',this)">Met. Ágiles</button>
  </div>
  <div class="nav-right">
    <div class="nav-search">
      <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <input id="globalSearch" type="text" placeholder="Buscar término…" oninput="globalFilter(this.value)">
    </div>
  </div>
</nav>

<section class="hero">
  <div class="hero-eyebrow"><span class="dot"></span> Powered by Claude AI &middot; 3 materias</div>
  <h1 class="hero-title">Glosario<br><span class="hero-title-blue">Interactivo</span></h1>
  <p class="hero-sub">Haz clic en cualquier tarjeta para ver la definición completa, un ejemplo práctico y palabras clave.</p>
  <div class="hero-stats">
    <div><div class="stat-n">28</div><div class="stat-l">Términos</div></div>
    <div><div class="stat-n">3</div><div class="stat-l">Materias</div></div>
    <div><div class="stat-n">IA</div><div class="stat-l">Definiciones</div></div>
  </div>
  <div class="hero-btns">
    <button class="btn-blue" onclick="goTo('sec-algo',null)">
      Explorar términos
      <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
    </button>
    <button class="btn-outline" onclick="goTo('about',null)">Como funciona</button>
  </div>
</section>

<div class="bg-white" id="sec-algo">
  <div class="section-wrap">
    <div class="section-header reveal">
      <div class="eyebrow" style="color:var(--mat-algo);">01 — Algoritmos</div>
      <h2 class="section-title">Fundamentos de<br>Algoritmos</h2>
      <p class="section-desc">Los pilares del pensamiento algoritmico y el ciclo de vida de un programa.</p>
    </div>
    <div class="filter-bar reveal">
      <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <input type="text" placeholder="Filtrar en Algoritmos…" oninput="filterSection('grid-algo',this.value)">
    </div>
    <div class="cards-grid" id="grid-algo"></div>
  </div>
</div>

<div class="bg-gray" id="sec-tgs">
  <div class="section-wrap">
    <div class="section-header reveal">
      <div class="eyebrow" style="color:var(--mat-tgs);">02 — Teoria General de Sistemas</div>
      <h2 class="section-title">Teoria General<br>de Sistemas</h2>
      <p class="section-desc">Como los sistemas se estructuran, interactuan y evolucionan en su entorno.</p>
    </div>
    <div class="filter-bar reveal">
      <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <input type="text" placeholder="Filtrar en T. de Sistemas…" oninput="filterSection('grid-tgs',this.value)">
    </div>
    <div class="cards-grid" id="grid-tgs"></div>
  </div>
</div>

<div class="bg-white" id="sec-agil">
  <div class="section-wrap">
    <div class="section-header reveal">
      <div class="eyebrow" style="color:var(--mat-agil);">03 — Metodologias Agiles</div>
      <h2 class="section-title">Metodologias<br>Agiles</h2>
      <p class="section-desc">Marcos modernos para entregar software de calidad de manera iterativa.</p>
    </div>
    <div class="filter-bar reveal">
      <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <input type="text" placeholder="Filtrar en Met. Agiles…" oninput="filterSection('grid-agil',this.value)">
    </div>
    <div class="cards-grid" id="grid-agil"></div>
  </div>
</div>

<section class="about-section" id="about">
  <div style="max-width:680px;margin:0 auto;">
    <div class="eyebrow" style="color:rgba(255,255,255,0.4);">Como funciona</div>
    <h2 class="section-title" style="color:#fff;margin-bottom:12px;">Definiciones con<br>inteligencia artificial</h2>
    <p class="section-desc" style="color:rgba(255,255,255,0.6);max-width:480px;margin:0 auto;">Cada tarjeta contiene una definicion academica completa con ejemplo practico y palabras clave contextuales generadas con Claude AI.</p>
    <div class="chips">
      <div class="chip">Definicion completa</div>
      <div class="chip">Ejemplo practico</div>
      <div class="chip">Palabras clave</div>
      <div class="chip">Claude AI</div>
      <div class="chip">Busqueda en tiempo real</div>
      <div class="chip">Nivel academico</div>
    </div>
  </div>
</section>

<footer>
  <div class="footer-logo">GlosarioIA</div>
  <div class="footer-txt">2025 &middot; Glosario Interactivo</div>
  <div class="footer-txt">Definiciones por <strong style="color:var(--black);">Claude AI</strong></div>
</footer>

<div class="modal-overlay" id="overlay" onclick="closeOnBg(event)">
  <div class="modal" id="modal">
    <div class="modal-top">
      <div class="modal-icon-wrap" id="mIcon"></div>
      <div class="modal-meta">
        <div class="modal-materia" id="mMateria"></div>
        <div class="modal-term-name" id="mTerm"></div>
      </div>
      <button class="modal-close" onclick="closeModal()">
        <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>
      </button>
    </div>
    <div class="modal-body" id="mBody"></div>
  </div>
</div>

<script>
const DEFS = {
  'Algoritmo':{
    def:'Un algoritmo es un conjunto finito, ordenado y preciso de instrucciones que permiten resolver un problema o realizar una tarea especifica. Cada paso debe ser claro, ejecutable y conducir a un resultado en un tiempo finito. Los algoritmos son la base de toda la programacion y el pensamiento computacional.',
    ejemplo:'Para ordenar una lista de calificaciones de mayor a menor, el algoritmo compara pares de numeros repetidamente y los intercambia hasta que la lista queda completamente ordenada.',
    kws:['instrucciones','pasos','logica','problema','solucion','finito','computacion']
  },
  'Entrada':{
    def:'La entrada es el conjunto de datos o informacion que un programa o algoritmo recibe para comenzar su procesamiento. Sin datos de entrada, el sistema no tiene informacion sobre que operar. Los datos de entrada pueden provenir del usuario, de archivos, de sensores o de bases de datos.',
    ejemplo:'En una calculadora, cuando el usuario escribe los numeros 8 y 3, esos valores son la entrada que el programa procesara para devolver un resultado.',
    kws:['datos','input','usuario','informacion','variables','parametros','lectura']
  },
  'Proceso':{
    def:'El proceso es la fase central del algoritmo donde los datos de entrada son transformados, analizados o calculados mediante operaciones logicas y matematicas para producir un resultado. Esta etapa incluye todas las instrucciones, condiciones, ciclos y calculos que conforman la logica del programa.',
    ejemplo:'En un programa que calcula el promedio de un estudiante, el proceso suma todas las notas y divide el total entre la cantidad de materias evaluadas.',
    kws:['transformacion','calculo','operaciones','logica','ciclos','condiciones','procesamiento']
  },
  'Salida':{
    def:'La salida es el resultado final que genera un algoritmo o programa tras haber procesado los datos de entrada. Representa la respuesta o producto del sistema, que puede mostrarse en pantalla, guardarse en un archivo, enviarse a otro sistema o activar un dispositivo externo.',
    ejemplo:'Despues de calcular el promedio de un estudiante, el programa muestra en pantalla el mensaje "Tu promedio es: 8.5", que constituye la salida del proceso.',
    kws:['resultado','output','respuesta','visualizacion','impresion','retorno','producto']
  },
  'Planificacion':{
    def:'La planificacion en programacion es la etapa previa al desarrollo donde se analiza el problema, se definen los objetivos, se disena la estructura del algoritmo y se establece el flujo de trabajo. Incluye la elaboracion de diagramas de flujo, pseudocodigo y la identificacion de entradas, procesos y salidas.',
    ejemplo:'Antes de programar una aplicacion para registrar inventario, el desarrollador dibuja un diagrama de flujo que muestra como se ingresaran los productos, como se actualizaran las existencias y que reportes generara.',
    kws:['diseno','analisis','diagrama de flujo','pseudocodigo','objetivos','estructura','organizacion']
  },
  'Edicion':{
    def:'La edicion es el proceso de escribir el codigo fuente del programa en un lenguaje de programacion especifico, siguiendo la logica disenada durante la planificacion. Esta etapa se realiza en un editor de codigo o entorno de desarrollo integrado (IDE) y requiere conocer la sintaxis del lenguaje elegido.',
    ejemplo:'Un programador escribe en Python el codigo de una funcion que calcula el area de un circulo, utilizando el IDE Visual Studio Code con resaltado de sintaxis.',
    kws:['codigo fuente','IDE','sintaxis','lenguaje de programacion','escritura','editor','instrucciones']
  },
  'Ejecutar y Compilar':{
    def:'Compilar es el proceso de traducir el codigo fuente escrito por el programador a codigo maquina que el procesador puede entender y ejecutar. Ejecutar significa correr el programa compilado para que realice las tareas programadas. En lenguajes interpretados como Python, ambas etapas ocurren simultaneamente.',
    ejemplo:'Al presionar Ejecutar en un IDE de Java, el compilador traduce el codigo a bytecode, la JVM lo interpreta y el programa comienza a funcionar mostrando resultados en pantalla.',
    kws:['compilador','codigo maquina','interprete','bytecode','ejecucion','JVM','traduccion']
  },
  'Corregir':{
    def:'Corregir, tambien llamado depuracion o debugging, es el proceso de identificar, analizar y eliminar errores (bugs) en el codigo de un programa. Estos errores pueden ser sintacticos, logicos o de tiempo de ejecucion. Un debugger permite ejecutar el programa paso a paso para localizar el problema.',
    ejemplo:'Al detectar que una funcion retorna valores incorrectos, el programador usa el debugger de su IDE para revisar el valor de las variables en cada paso y descubre que uso el operador incorrecto.',
    kws:['debugging','bug','error','depuracion','logico','sintactico','correccion']
  },
  'Documentar':{
    def:'Documentar es el proceso de registrar de manera clara y organizada el funcionamiento, la estructura y el proposito de un programa o algoritmo. Una buena documentacion incluye comentarios en el codigo, manuales de usuario, descripciones de funciones y guias de instalacion, facilitando el mantenimiento y la colaboracion.',
    ejemplo:'Un desarrollador agrega comentarios en cada funcion de su codigo explicando que hace, que parametros recibe y que valor retorna, ademas de redactar un archivo README con instrucciones de uso.',
    kws:['comentarios','README','manual','docstring','mantenimiento','legibilidad','descripcion']
  },
  'Sistema Abierto':{
    def:'Un sistema abierto es aquel que intercambia continuamente materia, energia e informacion con su entorno externo. Esta interaccion constante permite al sistema adaptarse, aprender y evolucionar en respuesta a cambios del exterior. La mayoria de los sistemas biologicos, sociales y organizacionales son sistemas abiertos.',
    ejemplo:'Una empresa es un sistema abierto porque recibe insumos del exterior (capital, empleados, materias primas), los procesa internamente y devuelve al entorno productos, servicios e impuestos.',
    kws:['interaccion','entorno','adaptacion','intercambio','evolucion','feedback','organismo']
  },
  'Sistema Cerrado':{
    def:'Un sistema cerrado es aquel que no intercambia materia ni informacion con su entorno exterior; opera de forma aislada e independiente. En la practica, los sistemas totalmente cerrados son teoricos, ya que todos los sistemas reales intercambian al menos energia con el medio.',
    ejemplo:'Un reloj mecanico clasico, una vez dado cuerda, opera internamente sin recibir nuevas entradas del exterior; sus engranajes funcionan de manera autonoma hasta que se agota la energia almacenada.',
    kws:['aislado','autonomo','independiente','sin intercambio','teorico','energia','autosuficiente']
  },
  'Entorno':{
    def:'El entorno es todo aquello que rodea a un sistema y con lo cual puede interactuar. Comprende el conjunto de elementos externos que influyen en el comportamiento del sistema sin pertenecer a el. Un cambio en el entorno puede generar respuestas de adaptacion dentro del sistema.',
    ejemplo:'Para un sistema educativo, el entorno incluye factores como las politicas gubernamentales, la economia, los avances tecnologicos y las tendencias culturales que influyen en como se imparte la educacion.',
    kws:['exterior','contexto','ambiente','influencia','factores externos','limite','ecosistema']
  },
  'Entrada (Input)':{
    def:'En la Teoria General de Sistemas, la entrada (input) es cualquier recurso, dato, energia o materia que ingresa al sistema desde su entorno para ser procesado. Las entradas son los ingredientes que el sistema necesita para funcionar y producir sus salidas.',
    ejemplo:'En un sistema de manufactura, las entradas son las materias primas, la energia electrica, la mano de obra y los disenos tecnicos que el sistema transforma en productos terminados.',
    kws:['recursos','datos','materia prima','insumos','importacion','flujo','recepcion']
  },
  'Proceso (Process)':{
    def:'El proceso es la transformacion interna que realiza el sistema sobre sus entradas para generar salidas. Es el nucleo funcional del sistema donde se aplican reglas, operaciones y mecanismos que convierten los insumos en productos o resultados.',
    ejemplo:'En un sistema hospitalario, el proceso incluye la evaluacion medica, el diagnostico, el tratamiento y la recuperacion del paciente, transformando la entrada (paciente enfermo) en salida (paciente curado).',
    kws:['transformacion','operaciones','mecanismo','conversion','tratamiento','funcion','nucleo']
  },
  'Salida (Output)':{
    def:'La salida (output) es el producto, resultado o consecuencia que genera el sistema tras procesar sus entradas. Las salidas pueden ser bienes, servicios, informacion, energia o residuos que el sistema devuelve al entorno. La calidad de las salidas refleja la eficiencia del sistema.',
    ejemplo:'En un sistema educativo, las salidas son los egresados formados, el conocimiento generado, las publicaciones academicas y los profesionales que se integran al mercado laboral.',
    kws:['producto','resultado','exportacion','bienes','servicios','eficiencia','retorno']
  },
  'Retroalimentacion (Feedback)':{
    def:'La retroalimentacion es el mecanismo mediante el cual el sistema recibe informacion sobre sus propias salidas para ajustar o corregir su comportamiento. El feedback negativo reduce la desviacion del sistema respecto a su objetivo, mientras que el positivo amplifica los cambios.',
    ejemplo:'Un termostato que detecta que la temperatura bajo por debajo de lo configurado y activa la calefaccion es un ejemplo clasico de retroalimentacion negativa que mantiene el sistema en equilibrio.',
    kws:['control','regulacion','ajuste','homeostasis','feedback negativo','feedback positivo','correccion']
  },
  'Sistema Natural':{
    def:'Un sistema natural es aquel que existe y se forma sin intervencion humana, creado por procesos de la naturaleza. Estos sistemas siguen leyes fisicas, quimicas y biologicas que los regulan. Son generalmente complejos, interdependientes y autorregulados.',
    ejemplo:'El sistema solar, los ecosistemas forestales, el ciclo del agua y el sistema circulatorio del ser humano son ejemplos de sistemas naturales que funcionan sin diseno humano.',
    kws:['naturaleza','biologico','ecosistema','organico','autorregulado','espontaneo','evolucion']
  },
  'Sistema Artificial':{
    def:'Un sistema artificial es el creado, disenado y construido por el ser humano con un proposito especifico. Estos sistemas son el resultado de la planificacion intencional y suelen estar orientados a satisfacer necesidades humanas o resolver problemas concretos.',
    ejemplo:'Una computadora, una red de transporte publico, un sistema de irrigacion y una base de datos son sistemas artificiales disenados por personas para funcionar de manera eficiente.',
    kws:['disenado','construido','intencional','tecnologico','ingenieria','proposito','creado']
  },
  'Sistema Social':{
    def:'Un sistema social es aquel conformado por personas, grupos e instituciones que interactuan entre si mediante normas, valores, comunicacion y estructuras de poder. Los sistemas sociales emergen de las relaciones humanas y evolucionan con el tiempo segun los cambios culturales y contextuales.',
    ejemplo:'Una universidad es un sistema social compuesto por estudiantes, docentes, administrativos y directivos, que interactuan mediante reglamentos, roles definidos y procesos academicos.',
    kws:['sociedad','instituciones','normas','cultura','interaccion','grupos','relaciones']
  },
  'Sistema Tecnologico':{
    def:'Un sistema tecnologico es el conjunto de herramientas, tecnicas, dispositivos y conocimientos organizados para lograr un objetivo productivo o de servicio. Combina componentes fisicos (hardware) y logicos (software) junto con procedimientos y personas que los operan.',
    ejemplo:'Internet es un sistema tecnologico que integra servidores, cables de fibra optica, protocolos de comunicacion y millones de dispositivos para permitir el intercambio global de informacion.',
    kws:['tecnologia','hardware','software','herramientas','innovacion','digital','infraestructura']
  },
  'Sinergia':{
    def:'La sinergia es el principio que establece que el resultado obtenido por la accion conjunta de los componentes de un sistema es mayor que la simple suma de sus resultados individuales. En sistemas, significa que la colaboracion e integracion generan un valor adicional que ningun elemento podria producir solo.',
    ejemplo:'Un equipo de futbol donde cada jugador cumple su rol especifico logra victorias que no podrian alcanzar individualmente, ya que la coordinacion genera un rendimiento superior al de cada jugador por separado.',
    kws:['cooperacion','totalidad','integracion','emergencia','valor anadido','colectivo','complementariedad']
  },
  'Totalidad':{
    def:'El principio de totalidad establece que un sistema debe analizarse como un todo integrado y no como la suma de sus partes aisladas. Los cambios en cualquier componente afectan a todo el sistema, y las propiedades del conjunto no pueden deducirse simplemente estudiando cada elemento por separado.',
    ejemplo:'Estudiar el cuerpo humano solo organo por organo no permite entender como funciona el organismo completo; la salud del cuerpo depende de la interaccion integral de todos sus sistemas.',
    kws:['holismo','globalidad','integracion','interdependencia','emergencia','conjunto','perspectiva']
  },
  'Inter-relacion':{
    def:'La inter-relacion describe los vinculos, conexiones y dependencias que existen entre los diferentes componentes de un sistema. Estas relaciones determinan como fluye la informacion, la energia o la materia entre las partes y como los cambios en un elemento repercuten en los demas.',
    ejemplo:'En un sistema de produccion, si el departamento de compras no provee materiales a tiempo, la produccion se detiene, lo que retrasa las entregas al cliente; todas las areas estan inter-relacionadas.',
    kws:['conexion','dependencia','vinculo','flujo','comunicacion','red','interdependencia']
  },
  'Metodologias Agiles':{
    def:'Las metodologias agiles son enfoques de desarrollo de software basados en la entrega iterativa e incremental de valor, la colaboracion constante con el cliente y la capacidad de adaptarse rapidamente a los cambios. Surgieron como respuesta a los metodos tradicionales rigidos y quedaron plasmadas en el Manifiesto Agil de 2001.',
    ejemplo:'Un equipo de desarrollo entrega una version funcional de su aplicacion cada dos semanas, incorporando el feedback del cliente en cada ciclo en lugar de esperar meses para mostrar un producto terminado.',
    kws:['iterativo','incremental','adaptacion','colaboracion','Manifiesto Agil','sprint','valor']
  },
  'SCRUM':{
    def:'SCRUM es un marco de trabajo agil que organiza el desarrollo en ciclos cortos llamados sprints (1 a 4 semanas). Define roles claros (Product Owner, Scrum Master, Equipo de Desarrollo) y ceremonias especificas (Sprint Planning, Daily Scrum, Sprint Review, Retrospectiva) para maximizar la productividad y transparencia del equipo.',
    ejemplo:'Un equipo de cinco desarrolladores trabaja en sprints de dos semanas: el lunes planifican las tareas del sprint, cada dia realizan una reunion de 15 minutos y al final del sprint presentan el incremento al cliente.',
    kws:['sprint','Product Owner','Scrum Master','daily','backlog','retrospectiva','ceremonias']
  },
  'Entregables':{
    def:'En el contexto agil, los entregables son los productos funcionales o incrementos de valor que el equipo entrega al cliente al final de cada sprint o iteracion. A diferencia de los proyectos tradicionales, los entregables agiles son parciales pero funcionales, permitiendo obtener retroalimentacion temprana y continua.',
    ejemplo:'Al final del segundo sprint, el equipo entrega un modulo de autenticacion completamente funcional que el cliente puede probar y aprobar, aunque la aplicacion completa aun no este terminada.',
    kws:['incremento','producto funcional','sprint','valor','retroalimentacion','entrega parcial','validacion']
  },
  'Sprint':{
    def:'Un sprint es el ciclo de trabajo basico en SCRUM, con una duracion fija de entre 1 y 4 semanas, durante el cual el equipo desarrolla un conjunto especifico de funcionalidades seleccionadas del Product Backlog. Al finalizar cada sprint se obtiene un incremento potencialmente entregable del producto.',
    ejemplo:'Durante un sprint de dos semanas, el equipo se compromete a desarrollar las funcionalidades de busqueda y filtrado de una tienda en linea, al termino del cual estas caracteristicas funcionan correctamente.',
    kws:['ciclo','iteracion','tiempo fijo','planificacion','SCRUM','incremento','compromisos']
  },
  'Backlog':{
    def:'El backlog (o Product Backlog) es una lista ordenada y priorizada de todas las funcionalidades, mejoras, correcciones y tareas que se desea implementar en el producto. Es gestionado por el Product Owner y representa la unica fuente de trabajo para el equipo de desarrollo; evoluciona constantemente.',
    ejemplo:'El backlog de una app de delivery incluye historias de usuario como "el cliente puede rastrear su pedido en tiempo real", "el restaurante puede actualizar su menu" y "el repartidor recibe notificaciones", ordenadas por prioridad de negocio.',
    kws:['lista de tareas','priorizacion','Product Owner','historias de usuario','refinamiento','planificacion','gestion']
  },
  'XP - Programacion Extrema':{
    def:'XP (Extreme Programming) es una metodologia agil centrada en mejorar la calidad del software y la capacidad de respuesta ante cambios en los requisitos. Sus practicas clave incluyen el desarrollo guiado por pruebas (TDD), la programacion en pares, la integracion continua y las entregas frecuentes de pequenos incrementos.',
    ejemplo:'Dos programadores trabajan juntos en la misma computadora (pair programming): uno escribe el codigo y el otro lo revisa en tiempo real, alternando roles periodicamente, lo que reduce errores y mejora la calidad del codigo.',
    kws:['TDD','pair programming','integracion continua','refactorizacion','pruebas','calidad','iteraciones cortas']
  },
  'RAD - Desarrollo Rapido':{
    def:'RAD (Rapid Application Development) es una metodologia de desarrollo de software que prioriza la velocidad de entrega mediante el uso de prototipado rapido, ciclos de desarrollo cortos y la participacion activa del usuario durante todo el proceso. Reduce el tiempo de desarrollo al minimizar la planificacion formal y centrarse en iteraciones rapidas.',
    ejemplo:'Para desarrollar un sistema de facturacion urgente, el equipo construye un prototipo basico en una semana, lo presenta al cliente, recoge su feedback, lo refina y repite el ciclo hasta obtener el sistema final en pocas semanas.',
    kws:['prototipado','velocidad','iteracion','usuario activo','entrega rapida','ciclos cortos','adaptacion']
  }
};

const TERMS = {
  algo:[
    {term:'Algoritmo',icon:'🔢',hint:'Secuencia finita de instrucciones para resolver un problema'},
    {term:'Entrada',icon:'📥',hint:'Datos que recibe un algoritmo o programa'},
    {term:'Proceso',icon:'⚙️',hint:'Transformacion de los datos de entrada'},
    {term:'Salida',icon:'📤',hint:'Resultado generado tras el procesamiento'},
    {term:'Planificacion',icon:'📋',hint:'Diseno y analisis previo a la codificacion'},
    {term:'Edicion',icon:'✏️',hint:'Escritura del codigo fuente del programa'},
    {term:'Ejecutar y Compilar',icon:'▶️',hint:'Traducir y correr el programa'},
    {term:'Corregir',icon:'🐛',hint:'Depuracion y eliminacion de errores'},
    {term:'Documentar',icon:'📝',hint:'Registrar el funcionamiento del codigo'},
  ],
  tgs:[
    {term:'Sistema Abierto',icon:'🔓',hint:'Intercambia materia e informacion con su entorno'},
    {term:'Sistema Cerrado',icon:'🔒',hint:'Opera de forma aislada sin intercambio exterior'},
    {term:'Entorno',icon:'🌐',hint:'Todo lo que rodea e influye en el sistema'},
    {term:'Entrada (Input)',icon:'⬇️',hint:'Recursos que ingresan al sistema desde el exterior'},
    {term:'Proceso (Process)',icon:'🔄',hint:'Transformacion interna de las entradas'},
    {term:'Salida (Output)',icon:'⬆️',hint:'Producto generado por el sistema'},
    {term:'Retroalimentacion (Feedback)',icon:'🔁',hint:'Informacion de retorno para ajustar el sistema'},
    {term:'Sistema Natural',icon:'🌿',hint:'Existe sin intervencion del ser humano'},
    {term:'Sistema Artificial',icon:'🤖',hint:'Disenado y construido por personas'},
    {term:'Sistema Social',icon:'👥',hint:'Formado por personas e instituciones que interactuan'},
    {term:'Sistema Tecnologico',icon:'💻',hint:'Integra herramientas y tecnicas con un proposito'},
    {term:'Sinergia',icon:'✨',hint:'El todo produce mas que la suma de las partes'},
    {term:'Totalidad',icon:'🎯',hint:'El sistema debe analizarse como un conjunto integrado'},
    {term:'Inter-relacion',icon:'🔗',hint:'Vinculos y dependencias entre componentes'},
  ],
  agil:[
    {term:'Metodologias Agiles',icon:'🚀',hint:'Enfoques iterativos e incrementales de desarrollo'},
    {term:'SCRUM',icon:'🏉',hint:'Marco agil basado en sprints y roles definidos'},
    {term:'Entregables',icon:'📦',hint:'Productos funcionales al final de cada sprint'},
    {term:'Sprint',icon:'⏱️',hint:'Ciclo fijo de trabajo en SCRUM'},
    {term:'Backlog',icon:'📋',hint:'Lista priorizada de tareas del producto'},
    {term:'XP - Programacion Extrema',icon:'⚡',hint:'Agil centrado en calidad y pruebas continuas'},
    {term:'RAD - Desarrollo Rapido',icon:'🏎️',hint:'Prototipado rapido y ciclos de entrega cortos'},
  ]
};

const BADGE_CLASS={algo:'badge-algo',tgs:'badge-tgs',agil:'badge-agil'};
const BADGE_LABEL={algo:'Algoritmos',tgs:'T. de Sistemas',agil:'Met. Agiles'};
const BADGE_COLOR={algo:'var(--mat-algo)',tgs:'var(--mat-tgs)',agil:'var(--mat-agil)'};

function renderAll(){
  ['algo','tgs','agil'].forEach(key=>{
    const grid=document.getElementById('grid-'+key);
    TERMS[key].forEach((t,i)=>{
      const card=document.createElement('div');
      card.className='term-card reveal d'+((i%3)+1);
      card.dataset.search=t.term.toLowerCase();
      card.innerHTML=`
        <span class="card-icon">${t.icon}</span>
        <div class="card-term">${t.term}</div>
        <div class="card-hint">${t.hint}</div>
        <div class="card-footer">
          <span class="card-badge ${BADGE_CLASS[key]}">${BADGE_LABEL[key]}</span>
          <span class="card-cta">Ver definicion
            <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
          </span>
        </div>`;
      card.addEventListener('click',()=>openModal(t,key));
      grid.appendChild(card);
    });
  });
  initReveal();
}

function findDef(termName){
  if(DEFS[termName]) return DEFS[termName];
  const k=Object.keys(DEFS).find(k=>k.toLowerCase()===termName.toLowerCase());
  return k?DEFS[k]:null;
}

function openModal(t,key){
  document.getElementById('mIcon').textContent=t.icon;
  document.getElementById('mMateria').textContent=BADGE_LABEL[key];
  document.getElementById('mMateria').style.color=BADGE_COLOR[key];
  document.getElementById('mTerm').textContent=t.term;
  const body=document.getElementById('mBody');
  const def=findDef(t.term);
  if(def){
    const c=BADGE_COLOR[key];
    body.innerHTML=`
      <div class="def-block">
        <div class="def-label" style="color:${c};">Definicion</div>
        <p class="def-text">${def.def}</p>
      </div>
      <div class="def-block">
        <div class="def-label" style="color:${c};">Ejemplo practico</div>
        <div class="def-example">${def.ejemplo}</div>
      </div>
      <div class="def-block">
        <div class="def-label" style="color:${c};">Palabras clave</div>
        <div class="kw-row">${def.kws.map(k=>`<span class="kw">${k}</span>`).join('')}</div>
      </div>`;
  } else {
    body.innerHTML=`<div style="padding:24px 0;text-align:center;color:var(--gray-400);font-size:15px;">Definicion no disponible.</div>`;
  }
  document.getElementById('overlay').classList.add('open');
  document.body.style.overflow='hidden';
}

function closeModal(){
  document.getElementById('overlay').classList.remove('open');
  document.body.style.overflow='';
}
function closeOnBg(e){if(e.target===document.getElementById('overlay'))closeModal();}
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeModal();});

function filterSection(gridId,q){
  const grid=document.getElementById(gridId);
  const val=q.toLowerCase().trim();
  let any=false;
  grid.querySelectorAll('.term-card').forEach(c=>{
    const show=!val||c.dataset.search.includes(val);
    c.style.display=show?'':'none';
    if(show)any=true;
  });
  let nr=grid.nextElementSibling;
  if(nr&&nr.classList.contains('no-results'))nr.remove();
  if(!any&&val){
    const el=document.createElement('div');
    el.className='no-results';
    el.textContent='Sin resultados para "'+q+'"';
    grid.after(el);
  }
}
function globalFilter(q){['algo','tgs','agil'].forEach(k=>filterSection('grid-'+k,q));}

function goTo(id,btn){
  if(btn){
    document.querySelectorAll('.nav-pill').forEach(p=>p.classList.remove('active'));
    btn.classList.add('active');
  }
  document.getElementById(id).scrollIntoView({behavior:'smooth',block:'start'});
}

function initReveal(){
  const obs=new IntersectionObserver(entries=>{
    entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target);}});
  },{threshold:0.08});
  document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
}

renderAll();
</script>
</body>
</html>
