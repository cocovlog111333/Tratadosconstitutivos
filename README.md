<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Tratados Constitutivos</title>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --navy:#0a1628;--gold:#c9a84c;--gold-light:#f0d080;--blue:#1a3a6b;--blue-mid:#2255a4;
  --text:#e8eaf0;--text-muted:#9ba3b5;--card:#0f1f3d;--card2:#122347;--border:#1e3560;
}
body{font-family:'Segoe UI',system-ui,sans-serif;background:var(--navy);color:var(--text);overflow-x:hidden}
nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(10,22,40,0.92);backdrop-filter:blur(10px);border-bottom:1px solid var(--border);padding:0 2rem;display:flex;align-items:center;justify-content:space-between;height:60px}
.nav-logo{font-size:14px;font-weight:600;color:var(--gold);letter-spacing:1px}
.nav-links{display:flex;gap:1.5rem;list-style:none}
.nav-links a{color:var(--text-muted);text-decoration:none;font-size:13px;transition:color .2s}
.nav-links a:hover{color:var(--gold)}
.hero{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:6rem 2rem 4rem;position:relative;overflow:hidden}
.hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse 80% 60% at 50% 30%,#1a3a6b55 0%,transparent 70%)}
.globe-ring{position:absolute;width:600px;height:600px;border-radius:50%;border:1px solid #1e356040;top:50%;left:50%;transform:translate(-50%,-50%)}
.globe-ring:nth-child(2){width:800px;height:800px;border-color:#1e356028}
.globe-ring:nth-child(3){width:1000px;height:1000px;border-color:#1e356018}
.hero-badge{display:inline-flex;align-items:center;gap:8px;background:#1a3a6b;border:1px solid var(--blue-mid);color:var(--gold);font-size:12px;font-weight:600;letter-spacing:1.5px;padding:6px 16px;border-radius:20px;text-transform:uppercase;margin-bottom:2rem}
.hero h1{font-size:clamp(2rem,5vw,3.8rem);font-weight:700;line-height:1.1;color:#fff;margin-bottom:1rem}
.hero h1 span{color:var(--gold)}
.hero p{font-size:1.1rem;color:var(--text-muted);max-width:600px;line-height:1.7;margin-bottom:2.5rem}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap;justify-content:center}
.btn-primary{background:var(--gold);color:var(--navy);padding:12px 28px;border-radius:8px;font-weight:700;font-size:14px;text-decoration:none;transition:background .2s}
.btn-primary:hover{background:var(--gold-light)}
.btn-outline{background:transparent;color:var(--text);padding:12px 28px;border-radius:8px;font-weight:600;font-size:14px;text-decoration:none;border:1px solid var(--border);transition:border-color .2s}
.btn-outline:hover{border-color:var(--gold)}
.hero-stats{display:flex;gap:3rem;margin-top:4rem;flex-wrap:wrap;justify-content:center}
.stat{text-align:center}
.stat-num{font-size:2.2rem;font-weight:700;color:var(--gold)}
.stat-label{font-size:13px;color:var(--text-muted);margin-top:4px}
section{padding:5rem 2rem;max-width:1100px;margin:0 auto}
.section-tag{display:inline-flex;align-items:center;gap:6px;background:#1a3a6b;color:var(--gold);font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;padding:4px 14px;border-radius:20px;margin-bottom:1rem}
.section-title{font-size:clamp(1.6rem,3vw,2.4rem);font-weight:700;color:#fff;margin-bottom:.75rem}
.section-title span{color:var(--gold)}
.section-sub{color:var(--text-muted);font-size:1rem;line-height:1.7;max-width:680px;margin-bottom:3rem}
.divider{width:60px;height:3px;background:var(--gold);border-radius:2px;margin:1rem 0 2.5rem}
.def-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem}
.def-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.5rem;position:relative;overflow:hidden;transition:border-color .2s,transform .2s}
.def-card:hover{border-color:var(--gold);transform:translateY(-3px)}
.def-card::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--gold)}
.def-icon{margin-bottom:.75rem}
.def-card h3{font-size:1rem;font-weight:600;color:#fff;margin-bottom:.5rem}
.def-card p{font-size:.875rem;color:#c8d0e0;line-height:1.6}
.actors-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1.2rem}
.actor-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.25rem;text-align:center;transition:border-color .2s,transform .2s}
.actor-card:hover{border-color:var(--gold);transform:translateY(-4px)}
.actor-icon{width:64px;height:64px;margin:0 auto 1rem;display:flex;align-items:center;justify-content:center}
.actor-card h3{font-size:.95rem;font-weight:600;color:#fff;margin-bottom:.4rem}
.actor-card p{font-size:.8rem;color:#9ba3b5;line-height:1.5}
.timeline{position:relative;padding-left:2.5rem}
.timeline::before{content:'';position:absolute;left:16px;top:0;bottom:0;width:2px;background:linear-gradient(to bottom,var(--gold),var(--blue-mid))}
.t-step{position:relative;margin-bottom:2rem}
.t-dot{position:absolute;left:-2.5rem;top:4px;width:32px;height:32px;border-radius:50%;background:var(--gold);display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;color:var(--navy)}
.t-body{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:1.25rem 1.5rem}
.t-body h3{font-size:1rem;font-weight:600;color:#fff;margin-bottom:.4rem}
.t-body p{font-size:.875rem;color:#c8d0e0;line-height:1.6}
.firma-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.2rem}
.firma-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.4rem;transition:border-color .2s;display:flex;flex-direction:column;gap:.5rem}
.firma-card:hover{border-color:var(--gold)}
.firma-num{font-size:2rem;font-weight:700;color:var(--gold)}
.firma-card h3{font-size:.95rem;font-weight:600;color:#fff}
.firma-card p{font-size:.825rem;color:#9ba3b5;line-height:1.6}
.firma-icon{margin-bottom:.25rem}
.table-wrap{overflow-x:auto;border-radius:14px;border:1px solid var(--border)}
table{width:100%;border-collapse:collapse;font-size:.875rem}
thead{background:#1a3a6b}
thead th{padding:12px 16px;text-align:left;color:var(--gold);font-weight:600;letter-spacing:.5px}
tbody tr{border-top:1px solid var(--border);background:#0d1e3a}
tbody tr:hover{background:#1a3a6b33}
tbody td{padding:12px 16px;color:#c8d0e0;vertical-align:middle}
tbody td:first-child{color:#fff;font-weight:500}
.badge{display:inline-block;padding:2px 10px;border-radius:20px;font-size:11px;font-weight:600}
.badge-yes{background:#0d3320;color:#4ade80}
.badge-no{background:#3a1515;color:#f87171}
.badge-cond{background:#2a2010;color:#fbbf24}
.foros-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.2rem}
.foro-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.4rem;display:flex;gap:1rem;align-items:flex-start;transition:border-color .2s}
.foro-card:hover{border-color:var(--gold)}
.foro-icon-wrap{min-width:52px;height:52px;display:flex;align-items:center;justify-content:center}
.foro-card h3{font-size:.95rem;font-weight:600;color:#fff;margin-bottom:.35rem}
.foro-card p{font-size:.8rem;color:#9ba3b5;line-height:1.5}
.ejemplos-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:1.5rem}
.ejemplo-card{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:1.75rem;transition:border-color .2s,transform .2s}
.ejemplo-card:hover{border-color:var(--gold);transform:translateY(-4px)}
.ej-header{display:flex;align-items:center;gap:1rem;margin-bottom:1rem}
.ej-year{background:#1a3a6b;color:var(--gold);font-size:12px;font-weight:700;padding:4px 12px;border-radius:20px}
.ej-org{font-size:.85rem;color:#9ba3b5}
.ejemplo-card h3{font-size:1.05rem;font-weight:600;color:#fff;margin-bottom:.6rem}
.ejemplo-card p{font-size:.845rem;color:#9ba3b5;line-height:1.65}
.ej-tag{display:inline-flex;align-items:center;gap:6px;margin-top:1rem;background:#1a3a6b44;border:1px solid var(--border);color:var(--gold);font-size:11px;padding:3px 10px;border-radius:20px}
.ej-icon{margin-bottom:.75rem}
footer{background:#060e1c;border-top:1px solid var(--border);padding:3rem 2rem;text-align:center}
.footer-logo{font-size:1.1rem;font-weight:700;color:var(--gold);margin-bottom:.5rem}
.footer-sub{font-size:.85rem;color:#9ba3b5;margin-bottom:.25rem}
.footer-credits{display:flex;flex-wrap:wrap;justify-content:center;gap:.75rem 2rem;margin-top:1.5rem}
.credit{font-size:.8rem;color:#9ba3b5}
.credit span{color:var(--text)}
html{scroll-behavior:smooth}
@media(max-width:640px){.def-grid{grid-template-columns:1fr}.hero-stats{gap:2rem}.nav-links{display:none}}
</style>
</head>
<body>

<nav>
  <div class="nav-logo">
    <svg width="18" height="18" viewBox="0 0 24 24" fill="none" style="vertical-align:-3px;margin-right:6px"><circle cx="12" cy="12" r="10" stroke="#c9a84c" stroke-width="1.5"/><ellipse cx="12" cy="12" rx="4" ry="10" stroke="#c9a84c" stroke-width="1.5"/><line x1="2" y1="12" x2="22" y2="12" stroke="#c9a84c" stroke-width="1.5"/></svg>
    Tratados Constitutivos
  </div>
  <ul class="nav-links">
    <li><a href="#que-es">¿Qué es?</a></li>
    <li><a href="#actores">Actores</a></li>
    <li><a href="#proceso">Proceso</a></li>
    <li><a href="#firma">Firma</a></li>
    <li><a href="#diferencias">Comparativa</a></li>
    <li><a href="#foros">Foros</a></li>
    <li><a href="#ejemplos">Ejemplos</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-bg"></div>
  <div class="globe-ring"></div><div class="globe-ring"></div><div class="globe-ring"></div>
  <div style="position:relative;z-index:2">
    <div class="hero-badge">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M12 2l2.4 7.4H22l-6.2 4.5 2.4 7.4L12 17l-6.2 4.3 2.4-7.4L2 9.4h7.6z" stroke="#c9a84c" stroke-width="1.5" stroke-linejoin="round"/></svg>
      Derecho Internacional Público
    </div>
    <h1>Tratados <span>Constitutivos</span><br>&amp; Procesos de Integración</h1>
    <p>El acto jurídico fundacional por excelencia: el documento que da vida a las organizaciones internacionales, las dota de personalidad jurídica y define su estructura de gobernanza.</p>
    <div class="hero-btns">
      <a href="#que-es" class="btn-primary">Explorar contenido</a>
      <a href="#ejemplos" class="btn-outline">Ver ejemplos históricos</a>
    </div>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">6</div><div class="stat-label">Tratados paradigmáticos</div></div>
      <div class="stat"><div class="stat-num">4</div><div class="stat-label">Métodos de firma</div></div>
      <div class="stat"><div class="stat-num">5</div><div class="stat-label">Foros diplomáticos</div></div>
      <div class="stat"><div class="stat-num">1969</div><div class="stat-label">Convención de Viena</div></div>
    </div>
  </div>
</div>

<!-- QUÉ ES -->
<section id="que-es">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><path d="M4 19V6a2 2 0 012-2h12a2 2 0 012 2v13" stroke="#c9a84c" stroke-width="1.8"/><path d="M4 19a2 2 0 002 2h12a2 2 0 002-2" stroke="#c9a84c" stroke-width="1.8"/><line x1="9" y1="10" x2="15" y2="10" stroke="#c9a84c" stroke-width="1.8"/><line x1="9" y1="14" x2="13" y2="14" stroke="#c9a84c" stroke-width="1.8"/></svg>
    Fundamentos
  </div>
  <h2 class="section-title">¿Qué es un <span>Tratado Constitutivo</span>?</h2>
  <div class="divider"></div>
  <p class="section-sub">Acuerdo internacional multilateral celebrado entre Estados soberanos mediante el cual se crea una organización internacional, dotándola de personalidad jurídica propia, estructura institucional y un ordenamiento jurídico interno.</p>
  <div class="def-grid">

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><rect x="8" y="4" width="26" height="34" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><path d="M14 14h14M14 20h14M14 26h8" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round"/><path d="M30 32l4 4 6-7" stroke="#4ade80" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>
      <h3>Naturaleza jurídica</h3>
      <p>Funciona como la "ley fundamental" de la organización. Es la norma primaria y jerárquicamente superior: todos los demás actos jurídicos deben subordinarse a él.</p>
    </div>

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><circle cx="24" cy="24" r="16" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><circle cx="24" cy="24" r="6" fill="#c9a84c" opacity=".3"/><circle cx="24" cy="24" r="2.5" fill="#c9a84c"/><line x1="24" y1="8" x2="24" y2="18" stroke="#c9a84c" stroke-width="1.5"/><line x1="24" y1="30" x2="24" y2="40" stroke="#c9a84c" stroke-width="1.5"/><line x1="8" y1="24" x2="18" y2="24" stroke="#c9a84c" stroke-width="1.5"/><line x1="30" y1="24" x2="40" y2="24" stroke="#c9a84c" stroke-width="1.5"/></svg>
      </div>
      <h3>Nuevo sujeto de derecho</h3>
      <p>Crea un nuevo sujeto de derecho internacional: la organización misma, con personalidad jurídica diferenciada de la de sus Estados miembros.</p>
    </div>

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><rect x="6" y="12" width="36" height="28" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><path d="M16 12V8a2 2 0 014 0v4M28 12V8a2 2 0 014 0v4" stroke="#c9a84c" stroke-width="1.5"/><rect x="12" y="22" width="8" height="8" rx="1" fill="#c9a84c" opacity=".4"/><rect x="28" y="22" width="8" height="8" rx="1" fill="#c9a84c" opacity=".2"/><line x1="6" y1="19" x2="42" y2="19" stroke="#c9a84c" stroke-width="1.2" opacity=".5"/></svg>
      </div>
      <h3>Cuándo se utiliza</h3>
      <p>Cuando los Estados deciden institucionalizar su cooperación creando un organismo internacional permanente, ya sea para integración económica, política o seguridad.</p>
    </div>

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><path d="M24 6l4 10h10l-8 6 3 10-9-6-9 6 3-10-8-6h10z" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5" stroke-linejoin="round"/><circle cx="24" cy="24" r="5" fill="#c9a84c" opacity=".5"/></svg>
      </div>
      <h3>Marco normativo</h3>
      <p>Regulado por la Convención de Viena (1969), que en su artículo 2.1.a) define los elementos constitutivos de todo tratado internacional.</p>
    </div>

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><path d="M8 40V20l16-12 16 12v20" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5" stroke-linejoin="round"/><rect x="18" y="28" width="12" height="12" rx="1" fill="#c9a84c" opacity=".35"/><path d="M24 8v4M16 16l-3-3M32 16l3-3" stroke="#c9a84c" stroke-width="1.2" stroke-linecap="round"/></svg>
      </div>
      <h3>Permanencia</h3>
      <p>Diseñados para vigencia indefinida o de largo plazo, con mecanismos propios de enmienda que requieren mayorías calificadas o unanimidad.</p>
    </div>

    <div class="def-card">
      <div class="def-icon">
        <svg width="40" height="40" viewBox="0 0 48 48" fill="none"><circle cx="16" cy="20" r="7" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><circle cx="32" cy="20" r="7" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><path d="M6 40c0-5.5 4.5-10 10-10h16c5.5 0 10 4.5 10 10" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round"/><path d="M22 16l4 4-4 4" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>
      <h3>Adhesión abierta</h3>
      <p>Incluyen cláusulas de adhesión que permiten a otros Estados incorporarse posteriormente, ampliando la membresía de la organización.</p>
    </div>

  </div>
</section>

<!-- ACTORES -->
<section id="actores" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><circle cx="9" cy="7" r="4" stroke="#c9a84c" stroke-width="1.6"/><path d="M2 21c0-4 3-7 7-7h6c4 0 7 3 7 7" stroke="#c9a84c" stroke-width="1.6" stroke-linecap="round"/></svg>
    Participantes
  </div>
  <h2 class="section-title">¿Para quiénes y <span>por quiénes</span>?</h2>
  <div class="divider"></div>
  <p class="section-sub">Los tratados constitutivos involucran actores con roles específicos en su elaboración, firma y aplicación.</p>
  <div class="actors-grid">

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><path d="M16 36V26l12-9 12 9v10" stroke="#c9a84c" stroke-width="1.8" stroke-linejoin="round" fill="none"/><rect x="22" y="28" width="12" height="8" rx="1" stroke="#c9a84c" stroke-width="1.5" fill="none"/><path d="M20 18l-4-3M36 18l4-3" stroke="#f0d080" stroke-width="1.2" stroke-linecap="round"/><rect x="26" y="20" width="4" height="4" rx=".5" fill="#c9a84c" opacity=".5"/></svg>
      </div>
      <h3>Estados soberanos</h3>
      <p>Sujetos primarios del derecho internacional. Creadores y miembros de la organización. Deben ratificar el tratado internamente.</p>
    </div>

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><circle cx="28" cy="22" r="7" stroke="#c9a84c" stroke-width="1.8" fill="none"/><path d="M18 40c0-5.5 4.5-9 10-9s10 3.5 10 9" stroke="#c9a84c" stroke-width="1.8" stroke-linecap="round" fill="none"/><path d="M35 18l3-3M36 22h4" stroke="#f0d080" stroke-width="1.4" stroke-linecap="round"/><circle cx="37" cy="16" r="2" fill="#c9a84c" opacity=".6"/></svg>
      </div>
      <h3>Plenipotenciarios</h3>
      <p>Representantes con plenos poderes del Jefe de Estado o Canciller para negociar, adoptar y autenticar el texto.</p>
    </div>

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><rect x="14" y="20" width="28" height="18" rx="2" stroke="#c9a84c" stroke-width="1.8" fill="none"/><path d="M20 20v-2a2 2 0 014 0v2M32 20v-2a2 2 0 014 0v2" stroke="#c9a84c" stroke-width="1.5"/><line x1="14" y1="27" x2="42" y2="27" stroke="#c9a84c" stroke-width="1.2" opacity=".5"/><rect x="20" y="30" width="5" height="5" rx=".5" fill="#c9a84c" opacity=".5"/><rect x="31" y="30" width="5" height="5" rx=".5" fill="#c9a84c" opacity=".3"/></svg>
      </div>
      <h3>Parlamentos nacionales</h3>
      <p>Órganos legislativos que aprueban la ratificación del tratado en cada Estado, confiriéndole validez jurídica interna.</p>
    </div>

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><circle cx="28" cy="28" r="12" stroke="#c9a84c" stroke-width="1.8" fill="none"/><ellipse cx="28" cy="28" rx="5" ry="12" stroke="#c9a84c" stroke-width="1.2" fill="none"/><line x1="16" y1="28" x2="40" y2="28" stroke="#c9a84c" stroke-width="1.2"/><line x1="18" y1="22" x2="38" y2="22" stroke="#c9a84c" stroke-width="1" opacity=".5"/><line x1="18" y1="34" x2="38" y2="34" stroke="#c9a84c" stroke-width="1" opacity=".5"/></svg>
      </div>
      <h3>Org. internacionales</h3>
      <p>Pueden actuar como depositarios, brindar asistencia técnica o auspiciar las negociaciones diplomáticas.</p>
    </div>

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><path d="M18 38V22l10-8 10 8v16" stroke="#c9a84c" stroke-width="1.8" stroke-linejoin="round" fill="none"/><path d="M14 38h28" stroke="#c9a84c" stroke-width="1.8" stroke-linecap="round"/><rect x="24" y="28" width="8" height="10" rx="1" stroke="#c9a84c" stroke-width="1.5" fill="none"/><path d="M28 14v4" stroke="#f0d080" stroke-width="1.4" stroke-linecap="round"/></svg>
      </div>
      <h3>Cancillerías</h3>
      <p>Ministerios de Relaciones Exteriores que coordinan la posición nacional y gestionan el proceso de ratificación.</p>
    </div>

    <div class="actor-card">
      <div class="actor-icon">
        <svg width="56" height="56" viewBox="0 0 56 56" fill="none"><rect width="56" height="56" rx="28" fill="#1a3a6b"/><rect x="14" y="18" width="22" height="22" rx="2" stroke="#c9a84c" stroke-width="1.8" fill="none"/><path d="M18 26h14M18 30h10M18 34h7" stroke="#c9a84c" stroke-width="1.4" stroke-linecap="round"/><path d="M32 30l8 8" stroke="#4ade80" stroke-width="2" stroke-linecap="round"/><circle cx="38" cy="36" r="5" fill="#1a3a6b" stroke="#4ade80" stroke-width="1.5"/><path d="M36 36l1.5 1.5 3-3" stroke="#4ade80" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>
      <h3>Estudiantes y académicos</h3>
      <p>Futuros diplomáticos cuya comprensión de estos instrumentos es esencial para la práctica profesional.</p>
    </div>

  </div>
</div>
</section>

<!-- PROCESO -->
<section id="proceso">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" stroke="#c9a84c" stroke-width="1.6"/><polyline points="12 7 12 12 15 15" stroke="#c9a84c" stroke-width="1.6" stroke-linecap="round"/></svg>
    Etapas
  </div>
  <h2 class="section-title">Pasos y <span>Proceso</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La celebración de un tratado constitutivo es un proceso jurídico-diplomático complejo consagrado en la Convención de Viena (1969).</p>
  <div class="timeline">
    <div class="t-step"><div class="t-dot">1</div><div class="t-body"><h3>Iniciativa y propuesta</h3><p>Uno o varios Estados proponen la creación de una organización. Surge en cumbres presidenciales, reuniones ministeriales o foros preexistentes, precedida de "diplomacia de corredor".</p></div></div>
    <div class="t-step"><div class="t-dot">2</div><div class="t-body"><h3>Conferencia de plenipotenciarios</h3><p>Se convoca una Conferencia Diplomática formal. Los Estados participan con delegaciones acreditadas con plenos poderes para negociar y adoptar el texto.</p></div></div>
    <div class="t-step"><div class="t-dot">3</div><div class="t-body"><h3>Negociación del texto</h3><p>Los delegados negocian artículo por artículo: objetivos, estructura institucional, competencias, procedimientos de decisión y cláusulas de adhesión.</p></div></div>
    <div class="t-step"><div class="t-dot">4</div><div class="t-body"><h3>Adopción y autenticación</h3><p>Los Estados adoptan el texto final por consenso o mayoría de dos tercios. La autenticación certifica que el texto es auténtico y definitivo.</p></div></div>
    <div class="t-step"><div class="t-dot">5</div><div class="t-body"><h3>Firma del tratado</h3><p>Acto solemne mediante el cual los Estados expresan su intención de quedar vinculados. Puede ser firma definitiva, ad referéndum o rúbrica.</p></div></div>
    <div class="t-step"><div class="t-dot">6</div><div class="t-body"><h3>Ratificación interna</h3><p>El Ejecutivo somete el tratado al Parlamento. El órgano legislativo debate y vota su aprobación para depositar el instrumento de ratificación.</p></div></div>
    <div class="t-step"><div class="t-dot">7</div><div class="t-body"><h3>Depósito y entrada en vigor</h3><p>El Estado deposita su instrumento ante el depositario. El tratado entra en vigor al alcanzar el número mínimo de ratificaciones estipulado.</p></div></div>
    <div class="t-step" style="margin-bottom:0"><div class="t-dot">8</div><div class="t-body"><h3>Registro ante la ONU</h3><p>Conforme al Artículo 102 de la Carta de la ONU, el tratado debe registrarse ante la Secretaría para poder ser invocado ante órganos de la ONU.</p></div></div>
  </div>
</section>

<!-- FIRMA -->
<section id="firma" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><path d="M17 3a2.8 2.8 0 014 4L7.5 20.5 2 22l1.5-5.5z" stroke="#c9a84c" stroke-width="1.6" stroke-linejoin="round"/></svg>
    Firma
  </div>
  <h2 class="section-title">Métodos de <span>Firma</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La firma es uno de los momentos más solemnes de la diplomacia multilateral. Existen cuatro modalidades reconocidas por el derecho internacional.</p>
  <div class="firma-grid">

    <div class="firma-card">
      <div class="firma-icon">
        <svg width="44" height="44" viewBox="0 0 44 44" fill="none"><rect x="4" y="6" width="28" height="32" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M10 16h16M10 21h16M10 26h10" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round"/><path d="M26 32c2-3 6-4 8-2s0 6-3 5" stroke="#f0d080" stroke-width="1.5" stroke-linecap="round"/><path d="M30 36l-3 2 1-3" stroke="#f0d080" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>
      <div class="firma-num">01</div>
      <h3>Firma definitiva</h3>
      <p>Expresa el consentimiento pleno del Estado. Cuando no se requiere ratificación posterior, la firma sola es suficiente para vincular al Estado.</p>
    </div>

    <div class="firma-card">
      <div class="firma-icon">
        <svg width="44" height="44" viewBox="0 0 44 44" fill="none"><rect x="4" y="6" width="28" height="32" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M10 16h16M10 21h16M10 26h10" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round" opacity=".5"/><path d="M24 34c2-3 6-4 8-2s0 6-3 5" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-dasharray="3 2"/><circle cx="36" cy="12" r="6" fill="#1a3a6b" stroke="#f0d080" stroke-width="1.4"/><path d="M33 12h6M36 9v6" stroke="#f0d080" stroke-width="1.4" stroke-linecap="round"/></svg>
      </div>
      <div class="firma-num">02</div>
      <h3>Firma ad referéndum</h3>
      <p>Firma provisional sujeta a confirmación posterior. Expresa la intención del Estado de someterse al proceso de ratificación.</p>
    </div>

    <div class="firma-card">
      <div class="firma-icon">
        <svg width="44" height="44" viewBox="0 0 44 44" fill="none"><rect x="4" y="6" width="28" height="32" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M10 16h16M10 21h16M10 26h10" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round" opacity=".4"/><text x="23" y="38" font-size="12" fill="#c9a84c" font-family="serif" font-style="italic" font-weight="bold">RF</text></svg>
      </div>
      <div class="firma-num">03</div>
      <h3>Rúbrica (initialing)</h3>
      <p>Firma de las iniciales del representante. Autentica el texto pero no expresa consentimiento de obligarse. Común en etapas de negociación.</p>
    </div>

    <div class="firma-card">
      <div class="firma-icon">
        <svg width="44" height="44" viewBox="0 0 44 44" fill="none"><circle cx="22" cy="22" r="16" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><circle cx="22" cy="22" r="3" fill="#c9a84c"/><line x1="22" y1="6" x2="22" y2="14" stroke="#c9a84c" stroke-width="1.4"/><line x1="22" y1="30" x2="22" y2="38" stroke="#c9a84c" stroke-width="1.4"/><line x1="6" y1="22" x2="14" y2="22" stroke="#c9a84c" stroke-width="1.4"/><line x1="30" y1="22" x2="38" y2="22" stroke="#c9a84c" stroke-width="1.4"/><path d="M14 14l5 5M25 25l5 5M30 14l-5 5M14 30l5-5" stroke="#f0d080" stroke-width="1.2" stroke-linecap="round"/></svg>
      </div>
      <div class="firma-num">04</div>
      <h3>Protocolo multilateral</h3>
      <p>Verificación de plenos poderes → orden alfabético → declaraciones en el acto → acta final. Proceso formal para tratados con múltiples signatarios.</p>
    </div>

  </div>
</div>
</section>

<!-- DIFERENCIAS -->
<section id="diferencias">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><path d="M8 7l-4 5 4 5M16 7l4 5-4 5" stroke="#c9a84c" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
    Comparativa
  </div>
  <h2 class="section-title">Diferencias y <span>Similitudes</span></h2>
  <div class="divider"></div>
  <p class="section-sub">El tratado constitutivo se distingue de otros instrumentos del Derecho Internacional por su función, alcance y jerarquía normativa.</p>
  <div class="table-wrap">
    <table>
      <thead>
        <tr>
          <th>Instrumento</th>
          <th>¿Crea organismo?</th>
          <th>¿Modifica tratado base?</th>
          <th>Finalidad principal</th>
          <th>Jerarquía</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>Tratado constitutivo</td><td><span class="badge badge-yes">Sí</span></td><td><span class="badge badge-no">No</span></td><td>Crear organización internacional</td><td>Norma primaria</td></tr>
        <tr><td>Tratado fundacional</td><td><span class="badge badge-yes">Sí</span></td><td><span class="badge badge-no">No</span></td><td>Fundación político-histórica</td><td>Norma primaria</td></tr>
        <tr><td>Protocolo</td><td><span class="badge badge-cond">No siempre</span></td><td><span class="badge badge-yes">Sí</span></td><td>Complementar/modificar tratado base</td><td>Norma derivada</td></tr>
        <tr><td>Acuerdo de Alcance Parcial</td><td><span class="badge badge-no">No siempre</span></td><td><span class="badge badge-no">No</span></td><td>Cooperación entre algunos miembros</td><td>Norma sectorial</td></tr>
        <tr><td>TLC</td><td><span class="badge badge-cond">No necesariamente</span></td><td><span class="badge badge-no">No</span></td><td>Liberalización comercial</td><td>Norma especial</td></tr>
      </tbody>
    </table>
  </div>
</section>

<!-- FOROS -->
<section id="foros" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z" stroke="#c9a84c" stroke-width="1.6"/></svg>
    Escenarios
  </div>
  <h2 class="section-title">Foros y <span>Cumbres Diplomáticas</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La negociación, adopción y seguimiento de los tratados constitutivos ocurre en cinco grandes escenarios diplomáticos.</p>
  <div class="foros-grid">

    <div class="foro-card">
      <div class="foro-icon-wrap">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><rect x="4" y="30" width="40" height="14" rx="2" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M10 30V18l14-10 14 10v12" stroke="#c9a84c" stroke-width="1.5" fill="none"/><rect x="19" y="20" width="10" height="10" rx="1" fill="#c9a84c" opacity=".3"/><path d="M16 44V34M24 44V34M32 44V34" stroke="#c9a84c" stroke-width="1.2" opacity=".5"/></svg>
      </div>
      <div><h3>Conferencia de Plenipotenciarios</h3><p>Foro más formal y solemne del proceso. Aquí se negocia y adopta oficialmente el texto del tratado.</p></div>
    </div>

    <div class="foro-card">
      <div class="foro-icon-wrap">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><path d="M24 6l3 9h9l-7 5 3 9-8-5-8 5 3-9-7-5h9z" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4" stroke-linejoin="round"/><circle cx="24" cy="24" r="5" fill="#c9a84c" opacity=".25"/><path d="M14 38h20M18 42h12" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round"/></svg>
      </div>
      <div><h3>Cumbres de Jefes de Estado</h3><p>Presidentes y jefes de gobierno firman los tratados, confiriéndoles máxima legitimidad política. Ej: Cumbre de Asunción (1991).</p></div>
    </div>

    <div class="foro-card">
      <div class="foro-icon-wrap">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><rect x="6" y="14" width="36" height="26" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M14 8h20v6H14z" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.3"/><path d="M14 26h20M14 32h14" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round"/><circle cx="36" cy="32" r="5" fill="#1a3a6b" stroke="#f0d080" stroke-width="1.3"/><path d="M34 32l1.5 1.5 3-3" stroke="#f0d080" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </div>
      <div><h3>Reuniones ministeriales</h3><p>Cancilleres y Ministros de RRII resuelven puntos de controversia en sesiones preparatorias antes de la firma formal.</p></div>
    </div>

    <div class="foro-card">
      <div class="foro-icon-wrap">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><circle cx="24" cy="24" r="17" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><ellipse cx="24" cy="24" rx="7" ry="17" stroke="#c9a84c" stroke-width="1.2" fill="none"/><line x1="7" y1="24" x2="41" y2="24" stroke="#c9a84c" stroke-width="1.2"/><line x1="9" y1="17" x2="39" y2="17" stroke="#c9a84c" stroke-width="1" opacity=".4"/><line x1="9" y1="31" x2="39" y2="31" stroke="#c9a84c" stroke-width="1" opacity=".4"/><path d="M24 7v6M24 35v6" stroke="#f0d080" stroke-width="1.3" stroke-linecap="round"/></svg>
      </div>
      <div><h3>Asamblea General ONU</h3><p>Para tratados bajo auspicios de la ONU, la adopción puede ocurrir en el marco de la Asamblea General o conferencias convocadas por ella.</p></div>
    </div>

    <div class="foro-card">
      <div class="foro-icon-wrap">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><rect x="10" y="10" width="28" height="32" rx="3" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><path d="M16 20h16M16 26h16M16 32h10" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round"/><path d="M10 16h28" stroke="#c9a84c" stroke-width="1.2" opacity=".4"/><circle cx="36" cy="38" r="7" fill="#0a1628" stroke="#c9a84c" stroke-width="1.3"/><path d="M33 38h6M36 35v6" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round"/></svg>
      </div>
      <div><h3>Secretaría y depositario</h3><p>Tras la firma, el depositario custodia los originales y administra el proceso de depósito de instrumentos de ratificación.</p></div>
    </div>

  </div>
</div>
</section>

<!-- EJEMPLOS -->
<section id="ejemplos">
  <div class="section-tag">
    <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" stroke="#c9a84c" stroke-width="1.6"/><path d="M12 8v4l3 3" stroke="#c9a84c" stroke-width="1.6" stroke-linecap="round"/></svg>
    Historia
  </div>
  <h2 class="section-title">Ejemplos <span>Paradigmáticos</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La historia del multilateralismo moderno está marcada por estos tratados que transformaron la arquitectura de la gobernanza global.</p>
  <div class="ejemplos-grid">

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><circle cx="24" cy="24" r="18" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><ellipse cx="24" cy="24" rx="7" ry="18" stroke="#c9a84c" stroke-width="1.2" fill="none"/><line x1="6" y1="24" x2="42" y2="24" stroke="#c9a84c" stroke-width="1.2"/><path d="M24 8l2 5-2 1-2-1zM24 40l2-5-2-1-2 1z" fill="#c9a84c" opacity=".6"/><path d="M14 16c3 2 6 3 10 2M14 32c3-2 6-3 10-2" stroke="#f0d080" stroke-width="1" opacity=".7"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1945</span><span class="ej-org">San Francisco, EE.UU.</span></div>
      <h3>Carta de las Naciones Unidas</h3>
      <p>Firmada el 26 de junio de 1945, crea la ONU con 193 Estados miembros. Establece la Asamblea General, el Consejo de Seguridad y la Corte Internacional de Justicia.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><circle cx="8" cy="8" r="6" stroke="#c9a84c" stroke-width="1.4"/><ellipse cx="8" cy="8" rx="3" ry="6" stroke="#c9a84c" stroke-width="1" fill="none"/><line x1="2" y1="8" x2="14" y2="8" stroke="#c9a84c" stroke-width="1"/></svg>
        ONU
      </span>
    </div>

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><path d="M24 8l16 10v12l-16 10L8 30V18z" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><circle cx="24" cy="24" r="6" fill="#c9a84c" opacity=".3" stroke="#c9a84c" stroke-width="1.2"/><path d="M16 18l4 3M28 18l4 3M16 30l4-3M28 30l4-3" stroke="#f0d080" stroke-width="1.2" stroke-linecap="round"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1948</span><span class="ej-org">Bogotá, Colombia</span></div>
      <h3>Carta de la OEA</h3>
      <p>Firmada en la IX Conferencia Internacional Americana. Define los principios del sistema interamericano: no intervención, igualdad soberana y solución pacífica de controversias.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><path d="M8 2l6 4v5L8 14 2 11V6z" stroke="#c9a84c" stroke-width="1.3" fill="none"/></svg>
        OEA
      </span>
    </div>

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><path d="M8 32V20l16-12 16 12v12" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5" stroke-linejoin="round"/><rect x="8" y="32" width="32" height="10" rx="2" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.4"/><rect x="20" y="22" width="8" height="10" rx="1" stroke="#c9a84c" stroke-width="1.3" fill="none"/><path d="M16 32h16" stroke="#c9a84c" stroke-width="1.2" opacity=".4"/><circle cx="34" cy="14" r="4" fill="#c9a84c" opacity=".5"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1957</span><span class="ej-org">Roma, Italia</span></div>
      <h3>Tratado de Roma — CEE</h3>
      <p>Firmado por 6 países europeos. Constituyó la Comunidad Económica Europea, estableciendo un mercado común y las instituciones que evolucionaron hasta la actual Unión Europea.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><circle cx="8" cy="8" r="6" stroke="#c9a84c" stroke-width="1.4"/><path d="M5 8h6M8 5v6" stroke="#c9a84c" stroke-width="1.2" stroke-linecap="round"/></svg>
        UE / CEE
      </span>
    </div>

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><path d="M12 36V24l12-14 12 14v12" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5" stroke-linejoin="round"/><path d="M8 38h32" stroke="#c9a84c" stroke-width="1.8" stroke-linecap="round"/><path d="M20 30c0-2.2 1.8-4 4-4s4 1.8 4 4v8h-8z" stroke="#c9a84c" stroke-width="1.3" fill="none"/><path d="M24 10v4M18 16l-3-4M30 16l3-4" stroke="#f0d080" stroke-width="1.3" stroke-linecap="round"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1969</span><span class="ej-org">Cartagena, Colombia</span></div>
      <h3>Acuerdo de Cartagena — CAN</h3>
      <p>Suscrito el 26 de mayo por Bolivia, Colombia, Chile, Ecuador y Perú. Creó la Comunidad Andina para acelerar el desarrollo equilibrado mediante la integración económica.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><path d="M2 12L6 6l4 4 2-3 4 5H2z" stroke="#c9a84c" stroke-width="1.2" fill="none"/></svg>
        Comunidad Andina
      </span>
    </div>

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><path d="M10 38c0-8 14-28 14-28s14 20 14 28" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><path d="M18 38c0-4 6-14 6-14s6 10 6 14" fill="#c9a84c" opacity=".2" stroke="#c9a84c" stroke-width="1.2"/><path d="M10 38h28" stroke="#c9a84c" stroke-width="1.8" stroke-linecap="round"/><path d="M24 10v4M16 20h16" stroke="#f0d080" stroke-width="1.3" stroke-linecap="round"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1991</span><span class="ej-org">Asunción, Paraguay</span></div>
      <h3>Tratado de Asunción — MERCOSUR</h3>
      <p>Firmado por Argentina, Brasil, Paraguay y Uruguay. Establece la libre circulación de bienes, el arancel externo común y la coordinación de políticas macroeconómicas.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><path d="M3 8h4l2-5 2 10 2-5h2" stroke="#c9a84c" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/></svg>
        MERCOSUR
      </span>
    </div>

    <div class="ejemplo-card">
      <div class="ej-icon">
        <svg width="48" height="48" viewBox="0 0 48 48" fill="none"><circle cx="24" cy="24" r="16" fill="#1a3a6b" stroke="#c9a84c" stroke-width="1.5"/><path d="M14 24h20M24 14v20" stroke="#c9a84c" stroke-width="1.8" stroke-linecap="round"/><circle cx="24" cy="24" r="4" fill="#c9a84c" opacity=".4"/><path d="M16 16l3 3M29 16l3 3M16 32l3-3M29 32l3-3" stroke="#f0d080" stroke-width="1.2" stroke-linecap="round"/></svg>
      </div>
      <div class="ej-header"><span class="ej-year">1991</span><span class="ej-org">Tegucigalpa, Honduras</span></div>
      <h3>Protocolo de Tegucigalpa — SICA</h3>
      <p>Constituye el Sistema de Integración Centroamericana. Panamá se incorporó como miembro pleno en 2013, destacando su vocación internacionalista y su posición geográfica estratégica.</p>
      <span class="ej-tag">
        <svg width="12" height="12" viewBox="0 0 16 16" fill="none"><path d="M8 2l1.5 4.5H14l-3.7 2.7 1.4 4.3L8 11 4.3 13.5l1.4-4.3L2 6.5h4.5z" stroke="#c9a84c" stroke-width="1.2" fill="none"/></svg>
        SICA — Relevante para Panamá
      </span>
    </div>

  </div>
</section>

<!-- FOOTER -->
<footer>
  <div style="display:flex;align-items:center;justify-content:center;gap:10px;margin-bottom:.5rem">
    <svg width="22" height="22" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" stroke="#c9a84c" stroke-width="1.5"/><ellipse cx="12" cy="12" rx="4" ry="9" stroke="#c9a84c" stroke-width="1.2" fill="none"/><line x1="3" y1="12" x2="21" y2="12" stroke="#c9a84c" stroke-width="1.2"/></svg>
    <div class="footer-logo">Tratados Constitutivos &amp; Procesos de Integración</div>
  </div>
  <p class="footer-sub">Universidad de Panamá · Facultad de Administración Pública · Escuela de Relaciones Internacionales</p>
  <p class="footer-sub" style="margin-top:.25rem">Licenciatura en Relaciones Internacionales · Grupo 4 Año Nocturno · Salón 210 · 25 Mayo, 2026</p>
  <p class="footer-sub" style="margin-top:.25rem">Profesora: Mitzi Cárdenas</p>
  <div class="footer-credits">
    <span class="credit"><span>Mizraim Flaco</span> | 8-1037-2263</span>
    <span class="credit"><span>Fabio Hernández</span> | 8-942-29</span>
    <span class="credit"><span>Tenessee Ortega</span> | 8-955-128</span>
    <span class="credit"><span>Juanita Páez</span> | EC-0035-11806</span>
  </div>
</footer>

</body>
</html>
