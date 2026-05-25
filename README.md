<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Tratados Constitutivos</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --navy:#0a1628;--gold:#c9a84c;--gold-light:#f0d080;--blue:#1a3a6b;--blue-mid:#2255a4;
  --text:#e8eaf0;--text-muted:#9ba3b5;--card:#0f1f3d;--card2:#122347;--border:#1e3560;
}
body{font-family:'Segoe UI',system-ui,sans-serif;background:var(--navy);color:var(--text);overflow-x:hidden}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(10,22,40,0.92);backdrop-filter:blur(10px);border-bottom:1px solid var(--border);padding:0 2rem;display:flex;align-items:center;justify-content:space-between;height:60px}
.nav-logo{font-size:14px;font-weight:600;color:var(--gold);letter-spacing:1px}
.nav-links{display:flex;gap:1.5rem;list-style:none}
.nav-links a{color:var(--text-muted);text-decoration:none;font-size:13px;transition:color .2s}
.nav-links a:hover{color:var(--gold)}

/* HERO */
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
.btn-primary{background:var(--gold);color:var(--navy);padding:12px 28px;border-radius:8px;font-weight:700;font-size:14px;text-decoration:none;border:none;cursor:pointer;transition:background .2s}
.btn-primary:hover{background:var(--gold-light)}
.btn-outline{background:transparent;color:var(--text);padding:12px 28px;border-radius:8px;font-weight:600;font-size:14px;text-decoration:none;border:1px solid var(--border);cursor:pointer;transition:border-color .2s}
.btn-outline:hover{border-color:var(--gold)}
.hero-stats{display:flex;gap:3rem;margin-top:4rem;flex-wrap:wrap;justify-content:center}
.stat{text-align:center}
.stat-num{font-size:2.2rem;font-weight:700;color:var(--gold)}
.stat-label{font-size:13px;color:var(--text-muted);margin-top:4px}

/* SECTIONS */
section{padding:5rem 2rem;max-width:1100px;margin:0 auto}
.section-tag{display:inline-block;background:#1a3a6b;color:var(--gold);font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;padding:4px 14px;border-radius:20px;margin-bottom:1rem}
.section-title{font-size:clamp(1.6rem,3vw,2.4rem);font-weight:700;color:#fff;margin-bottom:.75rem}
.section-title span{color:var(--gold)}
.section-sub{color:var(--text-muted);font-size:1rem;line-height:1.7;max-width:680px;margin-bottom:3rem}
.divider{width:60px;height:3px;background:var(--gold);border-radius:2px;margin:1rem 0 2.5rem}

/* QUÉ ES */
.def-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem}
.def-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.5rem;position:relative;overflow:hidden}
.def-card::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--gold)}
.def-icon{font-size:28px;color:var(--gold);margin-bottom:.75rem}
.def-card h3{font-size:1rem;font-weight:600;color:#fff;margin-bottom:.5rem}
.def-card p{font-size:.875rem;color:var(--text-muted);line-height:1.6}

/* ACTORES */
.actors-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1.2rem}
.actor-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.25rem;text-align:center;transition:border-color .2s,transform .2s}
.actor-card:hover{border-color:var(--gold);transform:translateY(-4px)}
.actor-icon{width:56px;height:56px;border-radius:50%;background:#1a3a6b;display:flex;align-items:center;justify-content:center;margin:0 auto 1rem;font-size:24px;color:var(--gold)}
.actor-card h3{font-size:.95rem;font-weight:600;color:#fff;margin-bottom:.4rem}
.actor-card p{font-size:.8rem;color:var(--text-muted);line-height:1.5}

/* TIMELINE */
.timeline{position:relative;padding-left:2.5rem}
.timeline::before{content:'';position:absolute;left:16px;top:0;bottom:0;width:2px;background:linear-gradient(to bottom,var(--gold),var(--blue-mid))}
.t-step{position:relative;margin-bottom:2rem}
.t-dot{position:absolute;left:-2.5rem;top:4px;width:32px;height:32px;border-radius:50%;background:var(--gold);display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;color:var(--navy)}
.t-body{background:var(--card);border:1px solid var(--border);border-radius:12px;padding:1.25rem 1.5rem}
.t-body h3{font-size:1rem;font-weight:600;color:#fff;margin-bottom:.4rem}
.t-body p{font-size:.875rem;color:var(--text-muted);line-height:1.6}

/* FIRMA */
.firma-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.2rem}
.firma-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.4rem;transition:border-color .2s}
.firma-card:hover{border-color:var(--gold)}
.firma-num{font-size:2rem;font-weight:700;color:var(--gold);margin-bottom:.5rem}
.firma-card h3{font-size:.95rem;font-weight:600;color:#fff;margin-bottom:.5rem}
.firma-card p{font-size:.825rem;color:var(--text-muted);line-height:1.6}

/* TABLA COMP */
.table-wrap{overflow-x:auto;border-radius:14px;border:1px solid var(--border)}
table{width:100%;border-collapse:collapse;font-size:.875rem}
thead{background:#1a3a6b}
thead th{padding:12px 16px;text-align:left;color:var(--gold);font-weight:600;letter-spacing:.5px}
tbody tr{border-top:1px solid var(--border)}
tbody tr:hover{background:#0f1f3d88}
tbody td{padding:12px 16px;color:var(--text-muted);vertical-align:middle}
tbody td:first-child{color:#fff;font-weight:500}
.badge{display:inline-block;padding:2px 10px;border-radius:20px;font-size:11px;font-weight:600}
.badge-yes{background:#0d3320;color:#4ade80}
.badge-no{background:#3a1515;color:#f87171}
.badge-cond{background:#2a2010;color:#fbbf24}

/* FOROS */
.foros-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.2rem}
.foro-card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:1.4rem;display:flex;gap:1rem;align-items:flex-start;transition:border-color .2s}
.foro-card:hover{border-color:var(--gold)}
.foro-icon-wrap{width:44px;height:44px;min-width:44px;border-radius:10px;background:#1a3a6b;display:flex;align-items:center;justify-content:center;font-size:20px;color:var(--gold)}
.foro-card h3{font-size:.95rem;font-weight:600;color:#fff;margin-bottom:.35rem}
.foro-card p{font-size:.8rem;color:var(--text-muted);line-height:1.5}

/* EJEMPLOS */
.ejemplos-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:1.5rem}
.ejemplo-card{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:1.75rem;transition:border-color .2s,transform .2s;cursor:pointer}
.ejemplo-card:hover{border-color:var(--gold);transform:translateY(-4px)}
.ej-header{display:flex;align-items:center;gap:1rem;margin-bottom:1rem}
.ej-year{background:#1a3a6b;color:var(--gold);font-size:12px;font-weight:700;padding:4px 12px;border-radius:20px}
.ej-org{font-size:.85rem;color:var(--text-muted)}
.ej-card h3{font-size:1.05rem;font-weight:600;color:#fff;margin-bottom:.6rem}
.ejemplo-card h3{font-size:1.05rem;font-weight:600;color:#fff;margin-bottom:.6rem}
.ejemplo-card p{font-size:.845rem;color:var(--text-muted);line-height:1.65}
.ej-tag{display:inline-block;margin-top:1rem;background:#1a3a6b44;border:1px solid var(--border);color:var(--gold);font-size:11px;padding:3px 10px;border-radius:20px}

/* FOOTER */
footer{background:#060e1c;border-top:1px solid var(--border);padding:3rem 2rem;text-align:center}
.footer-logo{font-size:1.1rem;font-weight:700;color:var(--gold);margin-bottom:.5rem}
.footer-sub{font-size:.85rem;color:var(--text-muted);margin-bottom:.25rem}
.footer-credits{display:flex;flex-wrap:wrap;justify-content:center;gap:.75rem 2rem;margin-top:1.5rem}
.credit{font-size:.8rem;color:var(--text-muted)}
.credit span{color:var(--text)}

/* SCROLL behavior */
html{scroll-behavior:smooth}
@media(max-width:640px){
  .def-grid{grid-template-columns:1fr}
  .hero-stats{gap:2rem}
  nav{padding:0 1rem}
  .nav-links{display:none}
}
</style>
</head>
<body>

<nav>
  <div class="nav-logo"><i class="ti ti-world" aria-hidden="true"></i> Tratados Constitutivos</div>
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
  <div class="globe-ring"></div>
  <div class="globe-ring"></div>
  <div class="globe-ring"></div>
  <div style="position:relative;z-index:2">
    <div class="hero-badge"><i class="ti ti-certificate" aria-hidden="true"></i> Derecho Internacional Público</div>
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
  <div class="section-tag"><i class="ti ti-book" aria-hidden="true"></i> Fundamentos</div>
  <h2 class="section-title">¿Qué es un <span>Tratado Constitutivo</span>?</h2>
  <div class="divider"></div>
  <p class="section-sub">Acuerdo internacional multilateral celebrado entre Estados soberanos mediante el cual se crea una organización internacional, dotándola de personalidad jurídica propia, estructura institucional y un ordenamiento jurídico interno.</p>
  <div class="def-grid">
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-gavel" aria-hidden="true"></i></div>
      <h3>Naturaleza jurídica</h3>
      <p>Funciona como la "ley fundamental" o "carta magna" de la organización que crea. Es la norma primaria y jerárquicamente superior: todos los demás actos jurídicos deben subordinarse a él.</p>
    </div>
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-building-bank" aria-hidden="true"></i></div>
      <h3>Nuevo sujeto de derecho</h3>
      <p>Crea un nuevo sujeto de derecho internacional: la organización misma, que adquiere personalidad jurídica diferenciada de la de sus Estados miembros.</p>
    </div>
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-calendar-time" aria-hidden="true"></i></div>
      <h3>Cuándo se utiliza</h3>
      <p>Cuando los Estados deciden institucionalizar su cooperación creando un organismo internacional permanente, ya sea para integración económica, política o seguridad colectiva.</p>
    </div>
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-shield-check" aria-hidden="true"></i></div>
      <h3>Marco normativo</h3>
      <p>Regulado por la Convención de Viena sobre el Derecho de los Tratados (1969), que en su artículo 2.1.a) define los elementos constitutivos de todo tratado internacional.</p>
    </div>
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-infinity" aria-hidden="true"></i></div>
      <h3>Permanencia</h3>
      <p>A diferencia de tratados de ejecución única, los tratados constitutivos están diseñados para vigencia indefinida o de largo plazo, con mecanismos propios de enmienda.</p>
    </div>
    <div class="def-card">
      <div class="def-icon"><i class="ti ti-door-enter" aria-hidden="true"></i></div>
      <h3>Adhesión abierta</h3>
      <p>Suelen incluir cláusulas de adhesión que permiten a otros Estados incorporarse posteriormente, ampliando la membresía de la organización.</p>
    </div>
  </div>
</section>

<!-- ACTORES -->
<section id="actores" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag"><i class="ti ti-users" aria-hidden="true"></i> Participantes</div>
  <h2 class="section-title">¿Para quiénes y <span>por quiénes</span>?</h2>
  <div class="divider"></div>
  <p class="section-sub">Los tratados constitutivos involucran actores con roles específicos en su elaboración, firma y aplicación.</p>
  <div class="actors-grid">
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-flag" aria-hidden="true"></i></div>
      <h3>Estados soberanos</h3>
      <p>Sujetos primarios del derecho internacional. Son los creadores y miembros de la organización. Deben ratificar el tratado internamente.</p>
    </div>
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-user-star" aria-hidden="true"></i></div>
      <h3>Plenipotenciarios</h3>
      <p>Representantes con plenos poderes emitidos por el Jefe de Estado o Canciller para negociar, adoptar y autenticar el texto.</p>
    </div>
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-building" aria-hidden="true"></i></div>
      <h3>Parlamentos nacionales</h3>
      <p>Órganos legislativos que aprueban la ratificación del tratado en cada Estado, confiriéndole validez jurídica interna.</p>
    </div>
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-world" aria-hidden="true"></i></div>
      <h3>Org. internacionales</h3>
      <p>Pueden actuar como depositarios, brindar asistencia técnica o auspiciar las negociaciones (ej. la ONU convoca conferencias diplomáticas).</p>
    </div>
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-writing" aria-hidden="true"></i></div>
      <h3>Cancillerías</h3>
      <p>Ministerios de Relaciones Exteriores que coordinan la posición nacional, preparan el texto y gestionan el proceso de ratificación.</p>
    </div>
    <div class="actor-card">
      <div class="actor-icon"><i class="ti ti-school" aria-hidden="true"></i></div>
      <h3>Estudiantes y académicos</h3>
      <p>Futuros diplomáticos y especialistas en RRII cuya comprensión de estos instrumentos es esencial para la práctica profesional.</p>
    </div>
  </div>
</div>
</section>

<!-- PROCESO -->
<section id="proceso">
  <div class="section-tag"><i class="ti ti-route" aria-hidden="true"></i> Etapas</div>
  <h2 class="section-title">Pasos y <span>Proceso</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La celebración de un tratado constitutivo es un proceso jurídico-diplomático complejo. El régimen aplicable está consagrado en la Convención de Viena (1969).</p>
  <div class="timeline">
    <div class="t-step"><div class="t-dot">1</div><div class="t-body"><h3>Iniciativa y propuesta</h3><p>Uno o varios Estados proponen la creación de una organización. Surge en cumbres presidenciales, reuniones ministeriales o foros preexistentes, precedida de "diplomacia de corredor".</p></div></div>
    <div class="t-step"><div class="t-dot">2</div><div class="t-body"><h3>Conferencia de plenipotenciarios</h3><p>Se convoca una Conferencia Diplomática formal. Los Estados participan mediante delegaciones con plenos poderes: documentos que acreditan su autoridad para negociar y adoptar el texto.</p></div></div>
    <div class="t-step"><div class="t-dot">3</div><div class="t-body"><h3>Negociación del texto</h3><p>Los delegados negocian artículo por artículo: objetivos, estructura institucional, competencias, procedimientos de decisión, cláusulas de adhesión y disposiciones de enmienda.</p></div></div>
    <div class="t-step"><div class="t-dot">4</div><div class="t-body"><h3>Adopción y autenticación</h3><p>Los Estados adoptan el texto final por consenso o mayoría de dos tercios. La autenticación certifica que el texto es auténtico y definitivo (firma, rúbrica u otro procedimiento acordado).</p></div></div>
    <div class="t-step"><div class="t-dot">5</div><div class="t-body"><h3>Firma del tratado</h3><p>Acto solemne mediante el cual los Estados expresan su intención de quedar vinculados. Puede ser firma definitiva, ad referéndum o rúbrica, según las circunstancias.</p></div></div>
    <div class="t-step"><div class="t-dot">6</div><div class="t-body"><h3>Ratificación interna</h3><p>El Ejecutivo somete el tratado al Parlamento. El órgano legislativo debate y vota su aprobación. Si es aprobado, el Ejecutivo queda autorizado para depositar el instrumento de ratificación.</p></div></div>
    <div class="t-step"><div class="t-dot">7</div><div class="t-body"><h3>Depósito y entrada en vigor</h3><p>El Estado deposita su instrumento ante el depositario. El tratado entra en vigor cuando se alcanza el número mínimo de ratificaciones estipulado en el propio instrumento.</p></div></div>
    <div class="t-step" style="margin-bottom:0"><div class="t-dot">8</div><div class="t-body"><h3>Registro ante la ONU</h3><p>Conforme al Artículo 102 de la Carta de la ONU, el tratado debe registrarse ante la Secretaría. Los tratados no registrados no pueden invocarse ante órganos de la ONU.</p></div></div>
  </div>
</section>

<!-- FIRMA -->
<section id="firma" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag"><i class="ti ti-signature" aria-hidden="true"></i> Firma</div>
  <h2 class="section-title">Métodos de <span>Firma</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La firma es uno de los momentos más solemnes de la diplomacia multilateral. Existen cuatro modalidades reconocidas por el derecho internacional.</p>
  <div class="firma-grid">
    <div class="firma-card">
      <div class="firma-num">01</div>
      <h3>Firma definitiva</h3>
      <p>Expresa el consentimiento del Estado en obligarse por el tratado. Cuando el tratado no requiere ratificación posterior, la firma sola es suficiente para vincular al Estado.</p>
    </div>
    <div class="firma-card">
      <div class="firma-num">02</div>
      <h3>Firma ad referéndum</h3>
      <p>Firma provisional sujeta a confirmación posterior. No produce por sí misma efectos jurídicos plenos, pero expresa la intención del Estado de someterse al proceso de ratificación.</p>
    </div>
    <div class="firma-card">
      <div class="firma-num">03</div>
      <h3>Rúbrica (initialing)</h3>
      <p>Consiste en la firma de las iniciales del representante. Autentica el texto pero no expresa el consentimiento del Estado en obligarse. Común en la etapa de autenticación.</p>
    </div>
    <div class="firma-card">
      <div class="firma-num">04</div>
      <h3>Protocolo multilateral</h3>
      <p>Proceso formal: verificación de plenos poderes → orden alfabético de firma → declaraciones → acta final. Los Estados pueden formular reservas en el momento de la firma.</p>
    </div>
  </div>
</div>
</section>

<!-- DIFERENCIAS -->
<section id="diferencias">
  <div class="section-tag"><i class="ti ti-arrows-diff" aria-hidden="true"></i> Comparativa</div>
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
        <tr>
          <td>Tratado constitutivo</td>
          <td><span class="badge badge-yes">Sí</span></td>
          <td><span class="badge badge-no">No</span></td>
          <td>Crear organización internacional</td>
          <td>Norma primaria</td>
        </tr>
        <tr>
          <td>Tratado fundacional</td>
          <td><span class="badge badge-yes">Sí</span></td>
          <td><span class="badge badge-no">No</span></td>
          <td>Fundación político-histórica</td>
          <td>Norma primaria</td>
        </tr>
        <tr>
          <td>Protocolo</td>
          <td><span class="badge badge-cond">No siempre</span></td>
          <td><span class="badge badge-yes">Sí</span></td>
          <td>Complementar/modificar tratado base</td>
          <td>Norma derivada</td>
        </tr>
        <tr>
          <td>Acuerdo de Alcance Parcial</td>
          <td><span class="badge badge-no">No siempre</span></td>
          <td><span class="badge badge-no">No</span></td>
          <td>Cooperación entre algunos miembros</td>
          <td>Norma sectorial</td>
        </tr>
        <tr>
          <td>TLC</td>
          <td><span class="badge badge-cond">No necesariamente</span></td>
          <td><span class="badge badge-no">No</span></td>
          <td>Liberalización comercial</td>
          <td>Norma especial</td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- FOROS -->
<section id="foros" style="background:#060e1c;max-width:100%;padding:5rem 2rem">
<div style="max-width:1100px;margin:0 auto">
  <div class="section-tag"><i class="ti ti-building-community" aria-hidden="true"></i> Escenarios</div>
  <h2 class="section-title">Foros y <span>Cumbres Diplomáticas</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La negociación, adopción y seguimiento de los tratados constitutivos ocurre en cinco grandes escenarios diplomáticos.</p>
  <div class="foros-grid">
    <div class="foro-card">
      <div class="foro-icon-wrap"><i class="ti ti-podium" aria-hidden="true"></i></div>
      <div><h3>Conferencia de Plenipotenciarios</h3><p>Foro formal donde se negocia y adopta el texto. El escenario más solemne del proceso constitutivo.</p></div>
    </div>
    <div class="foro-card">
      <div class="foro-icon-wrap"><i class="ti ti-crown" aria-hidden="true"></i></div>
      <div><h3>Cumbres de Jefes de Estado</h3><p>Los tratados se firman ante presidentes y jefes de gobierno, confiriéndoles máxima legitimidad política. Ej: Cumbre de Asunción (1991).</p></div>
    </div>
    <div class="foro-card">
      <div class="foro-icon-wrap"><i class="ti ti-briefcase" aria-hidden="true"></i></div>
      <div><h3>Reuniones ministeriales</h3><p>Cancilleres y Ministros de RRII resuelven puntos de controversia en sesiones preparatorias antes de la firma formal.</p></div>
    </div>
    <div class="foro-card">
      <div class="foro-icon-wrap"><i class="ti ti-world-globe" aria-hidden="true"></i></div>
      <div><h3>Asamblea General ONU</h3><p>Para tratados bajo auspicios de la ONU, la adopción puede ocurrir en el marco de la Asamblea General o conferencias convocadas por ella.</p></div>
    </div>
    <div class="foro-card">
      <div class="foro-icon-wrap"><i class="ti ti-archive" aria-hidden="true"></i></div>
      <div><h3>Secretaría y depositario</h3><p>Tras la firma, el depositario custodia los originales y administra el proceso de depósito de instrumentos de ratificación.</p></div>
    </div>
  </div>
</div>
</section>

<!-- EJEMPLOS -->
<section id="ejemplos">
  <div class="section-tag"><i class="ti ti-history" aria-hidden="true"></i> Historia</div>
  <h2 class="section-title">Ejemplos <span>Paradigmáticos</span></h2>
  <div class="divider"></div>
  <p class="section-sub">La historia del multilateralismo moderno está marcada por estos tratados constitutivos que transformaron la arquitectura de la gobernanza global.</p>
  <div class="ejemplos-grid">
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1945</span><span class="ej-org">San Francisco, EE.UU.</span></div>
      <h3>Carta de las Naciones Unidas</h3>
      <p>Firmada el 26 de junio de 1945, crea la ONU con 193 Estados miembros actuales. Establece la Asamblea General, el Consejo de Seguridad, la Secretaría y la Corte Internacional de Justicia.</p>
      <span class="ej-tag"><i class="ti ti-world" aria-hidden="true"></i> ONU</span>
    </div>
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1948</span><span class="ej-org">Bogotá, Colombia</span></div>
      <h3>Carta de la OEA</h3>
      <p>Firmada el 30 de abril en la IX Conferencia Internacional Americana. Define los principios del sistema interamericano: no intervención, igualdad soberana y solución pacífica.</p>
      <span class="ej-tag"><i class="ti ti-flag" aria-hidden="true"></i> OEA</span>
    </div>
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1957</span><span class="ej-org">Roma, Italia</span></div>
      <h3>Tratado de Roma — CEE</h3>
      <p>Firmado por Alemania, Francia, Italia, Bélgica, Países Bajos y Luxemburgo. Constituyó la Comunidad Económica Europea, predecesora de la actual Unión Europea.</p>
      <span class="ej-tag"><i class="ti ti-building-bank" aria-hidden="true"></i> UE / CEE</span>
    </div>
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1969</span><span class="ej-org">Cartagena, Colombia</span></div>
      <h3>Acuerdo de Cartagena — CAN</h3>
      <p>Suscrito el 26 de mayo por Bolivia, Colombia, Chile, Ecuador y Perú. Creó el Pacto Andino con el objetivo de acelerar el desarrollo equilibrado mediante la integración económica.</p>
      <span class="ej-tag"><i class="ti ti-mountain" aria-hidden="true"></i> Comunidad Andina</span>
    </div>
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1991</span><span class="ej-org">Asunción, Paraguay</span></div>
      <h3>Tratado de Asunción — MERCOSUR</h3>
      <p>Firmado el 26 de marzo por Argentina, Brasil, Paraguay y Uruguay. Establece la libre circulación de bienes, el arancel externo común y la coordinación macroeconómica.</p>
      <span class="ej-tag"><i class="ti ti-arrows-exchange" aria-hidden="true"></i> MERCOSUR</span>
    </div>
    <div class="ejemplo-card">
      <div class="ej-header"><span class="ej-year">1991</span><span class="ej-org">Tegucigalpa, Honduras</span></div>
      <h3>Protocolo de Tegucigalpa — SICA</h3>
      <p>Firmado el 13 de diciembre. Constituye el Sistema de Integración Centroamericana. Panamá se incorporó como miembro pleno en 2013, destacando su vocación internacionalista.</p>
      <span class="ej-tag"><i class="ti ti-map-pin" aria-hidden="true"></i> SICA — Relevante para Panamá</span>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo"><i class="ti ti-world" aria-hidden="true"></i> Tratados Constitutivos &amp; Procesos de Integración</div>
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
