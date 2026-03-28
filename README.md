<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Udoka Nwankwo | Physicist &amp; Data Scientist</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,600&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..500;9..600&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet"/>
<style>
:root{
  --bg:#04080f;
  --surface:#0a1220;
  --card:#0f1b2d;
  --border:rgba(100,255,218,.12);
  --teal:#64ffda;
  --teal-dim:rgba(100,255,218,.15);
  --amber:#f0a500;
  --amber-dim:rgba(240,165,0,.15);
  --txt:#ccd6f6;
  --txt-muted:#8892b0;
  --nav-h:70px;
}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth;font-size:16px}
body{background:var(--bg);color:var(--txt);font-family:'DM Sans',sans-serif;overflow-x:hidden;line-height:1.7}

/* ── SCROLLBAR ─────────────────────────────────────── */
::-webkit-scrollbar{width:6px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--teal);border-radius:3px}

/* ── NAV ───────────────────────────────────────────── */
nav{position:fixed;top:0;left:0;width:100%;height:var(--nav-h);display:flex;align-items:center;justify-content:space-between;padding:0 5%;z-index:1000;backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);background:rgba(4,8,15,.7);border-bottom:1px solid var(--border);transition:all .3s}
.logo{font-family:'Cormorant Garamond',serif;font-size:1.8rem;font-weight:700;color:var(--teal);letter-spacing:2px;text-decoration:none;position:relative}
.logo::after{content:'';position:absolute;bottom:-2px;left:0;width:0;height:2px;background:var(--amber);transition:.4s}
.logo:hover::after{width:100%}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{color:var(--txt-muted);text-decoration:none;font-size:.85rem;letter-spacing:1.5px;text-transform:uppercase;font-family:'Space Mono',monospace;transition:.3s;position:relative;padding-bottom:4px}
.nav-links a::after{content:'';position:absolute;bottom:0;left:0;width:0;height:1px;background:var(--teal);transition:.3s}
.nav-links a:hover{color:var(--teal)}
.nav-links a:hover::after{width:100%}
.nav-links a.active{color:var(--teal)}
.nav-links a.active::after{width:100%}

/* ── SECTION BASE ─────────────────────────────────── */
section{min-height:100vh;padding:calc(var(--nav-h) + 4rem) 10% 5rem;position:relative}
.section-label{font-family:'Space Mono',monospace;color:var(--teal);font-size:.8rem;letter-spacing:3px;text-transform:uppercase;margin-bottom:.6rem}
.section-title{font-family:'Cormorant Garamond',serif;font-size:clamp(2rem,5vw,3.5rem);font-weight:600;line-height:1.1;color:#e8f0fe;margin-bottom:1rem}
.section-divider{width:60px;height:2px;background:linear-gradient(90deg,var(--teal),transparent);margin:1.5rem 0 3rem}
.reveal{opacity:0;transform:translateY(30px);transition:opacity .7s ease,transform .7s ease}
.reveal.visible{opacity:1;transform:translateY(0)}

/* ── HERO ─────────────────────────────────────────── */
#home{min-height:100vh;display:flex;align-items:center;padding:0 10%;position:relative;overflow:hidden}
canvas#particles{position:absolute;top:0;left:0;width:100%;height:100%;z-index:0;opacity:.6}
.hero-content{position:relative;z-index:1;max-width:850px}
.hero-eyebrow{font-family:'Space Mono',monospace;color:var(--teal);font-size:.85rem;letter-spacing:3px;text-transform:uppercase;margin-bottom:1.2rem;display:flex;align-items:center;gap:.8rem}
.hero-eyebrow::before{content:'';width:40px;height:1px;background:var(--teal)}
.hero-title{font-family:'Cormorant Garamond',serif;font-size:clamp(3rem,7vw,5.5rem);font-weight:700;line-height:1.05;color:#e8f0fe;margin-bottom:1rem}
.hero-title span{color:var(--teal);font-style:italic}
.hero-subtitle{font-size:1rem;color:var(--txt-muted);max-width:680px;line-height:1.8;margin-bottom:2.5rem;font-weight:300}
.tags-row{display:flex;flex-wrap:wrap;gap:.6rem;margin-bottom:2.5rem}
.tag{font-family:'Space Mono',monospace;font-size:.72rem;padding:.35rem .85rem;border:1px solid var(--border);border-radius:100px;color:var(--txt-muted);background:var(--teal-dim);transition:.3s;letter-spacing:.5px}
.tag:hover{border-color:var(--teal);color:var(--teal);background:rgba(100,255,218,.08)}
.hero-cta{display:flex;gap:1rem;flex-wrap:wrap}
.btn-primary{display:inline-block;padding:.8rem 2rem;background:transparent;border:1.5px solid var(--teal);color:var(--teal);font-family:'Space Mono',monospace;font-size:.8rem;letter-spacing:2px;text-decoration:none;transition:.3s;text-transform:uppercase}
.btn-primary:hover{background:var(--teal-dim);box-shadow:0 0 20px rgba(100,255,218,.2)}
.btn-secondary{display:inline-block;padding:.8rem 2rem;background:var(--amber);border:1.5px solid var(--amber);color:#000;font-family:'Space Mono',monospace;font-size:.8rem;letter-spacing:2px;text-decoration:none;transition:.3s;text-transform:uppercase;font-weight:700}
.btn-secondary:hover{background:transparent;color:var(--amber)}
.scroll-hint{position:absolute;bottom:2.5rem;left:50%;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;gap:.4rem;color:var(--txt-muted);font-size:.7rem;letter-spacing:2px;text-transform:uppercase;font-family:'Space Mono',monospace;animation:float 2.5s ease-in-out infinite}
.scroll-hint .arrow{width:20px;height:20px;border-right:2px solid var(--teal);border-bottom:2px solid var(--teal);transform:rotate(45deg);animation:pulse-arrow 2s infinite}
@keyframes float{0%,100%{transform:translateX(-50%) translateY(0)}50%{transform:translateX(-50%) translateY(8px)}}
@keyframes pulse-arrow{0%,100%{opacity:1}50%{opacity:.3}}

/* ── ABOUT ────────────────────────────────────────── */
#about{background:var(--surface)}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:start}
.about-bio{font-size:.95rem;color:var(--txt-muted);line-height:1.9;margin-bottom:2rem}
.about-bio p+p{margin-top:1rem}
.strengths{margin-top:2rem}
.strengths h4{font-family:'Space Mono',monospace;font-size:.8rem;color:var(--teal);letter-spacing:2px;text-transform:uppercase;margin-bottom:1rem}
.strength-item{display:flex;align-items:flex-start;gap:.8rem;padding:.7rem 0;border-bottom:1px solid var(--border)}
.strength-item::before{content:'▸';color:var(--amber);font-size:.8rem;margin-top:.2rem;flex-shrink:0}
.strength-item span{font-size:.9rem;color:var(--txt)}
.edu-timeline{border-left:2px solid var(--border);padding-left:2rem;margin-top:1rem}
.edu-item{position:relative;margin-bottom:2.2rem}
.edu-item::before{content:'';position:absolute;left:-2.6rem;top:.4rem;width:10px;height:10px;background:var(--teal);border-radius:50%;box-shadow:0 0 10px var(--teal)}
.edu-degree{font-family:'Cormorant Garamond',serif;font-size:1.25rem;font-weight:600;color:#e8f0fe;margin-bottom:.2rem}
.edu-major{font-size:.85rem;color:var(--amber);font-weight:500;margin-bottom:.2rem;font-family:'Space Mono',monospace;font-size:.75rem}
.edu-school{font-size:.85rem;color:var(--txt-muted)}
.edu-year{font-size:.75rem;color:var(--teal);font-family:'Space Mono',monospace;margin-top:.2rem}

/* ── SKILLS ─────────────────────────────────────────*/
#skills{}
.skills-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2rem}
.skill-card{background:var(--card);border:1px solid var(--border);padding:2rem;border-radius:4px;transition:.3s;position:relative;overflow:hidden}
.skill-card::before{content:'';position:absolute;top:0;left:0;width:3px;height:0;background:var(--teal);transition:.4s}
.skill-card:hover::before{height:100%}
.skill-card:hover{border-color:var(--teal);transform:translateY(-4px);box-shadow:0 10px 30px rgba(0,0,0,.4)}
.skill-card h3{font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:600;color:#e8f0fe;margin-bottom:.3rem}
.skill-card .sk-sub{font-family:'Space Mono',monospace;font-size:.7rem;color:var(--teal);letter-spacing:2px;text-transform:uppercase;margin-bottom:1.2rem}
.skill-tags{display:flex;flex-wrap:wrap;gap:.5rem}
.sk-tag{font-size:.75rem;padding:.3rem .7rem;background:var(--teal-dim);border:1px solid var(--border);color:var(--txt);border-radius:3px;font-family:'Space Mono',monospace;transition:.3s}
.sk-tag:hover{border-color:var(--teal);color:var(--teal)}
.sk-tag.amber{background:var(--amber-dim);border-color:rgba(240,165,0,.25);color:var(--amber)}
.sk-tag.amber:hover{border-color:var(--amber)}

/* ── PROJECTS ─────────────────────────────────────── */
#projects{background:var(--surface)}
.projects-grid{display:grid;grid-template-columns:1fr;gap:2rem}
.project-card{background:var(--card);border:1px solid var(--border);border-radius:4px;padding:2.5rem;transition:.3s;position:relative;overflow:hidden}
.project-card::after{content:'';position:absolute;inset:0;background:linear-gradient(135deg,var(--teal-dim),transparent 60%);opacity:0;transition:.4s;pointer-events:none}
.project-card:hover{border-color:var(--teal);transform:translateY(-3px);box-shadow:0 15px 40px rgba(0,0,0,.5)}
.project-card:hover::after{opacity:1}
.project-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:1rem;flex-wrap:wrap;gap:.5rem}
.project-title{font-family:'Cormorant Garamond',serif;font-size:1.5rem;font-weight:600;color:#e8f0fe;line-height:1.2}
.project-time{font-family:'Space Mono',monospace;font-size:.72rem;color:var(--amber);padding:.25rem .7rem;border:1px solid rgba(240,165,0,.3);border-radius:100px;white-space:nowrap}
.project-meta{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-top:1.2rem}
.pm-block{padding:.8rem 1rem;background:rgba(100,255,218,.04);border-left:2px solid var(--border);transition:.3s}
.pm-block:hover{border-left-color:var(--teal)}
.pm-label{font-family:'Space Mono',monospace;font-size:.65rem;color:var(--teal);letter-spacing:2px;text-transform:uppercase;margin-bottom:.3rem}
.pm-text{font-size:.85rem;color:var(--txt-muted);line-height:1.7}
.pm-block.full{grid-column:1/-1}
.project-contribution{margin-top:1.2rem;padding:.8rem 1rem;background:var(--amber-dim);border-left:2px solid var(--amber);font-size:.85rem;color:var(--txt-muted)}
.project-contribution strong{color:var(--amber);font-family:'Space Mono',monospace;font-size:.7rem;letter-spacing:1px;text-transform:uppercase;display:block;margin-bottom:.2rem}

/* ── RESUME ──────────────────────────────────────── */
#resume{text-align:center}
.resume-inner{max-width:700px;margin:0 auto;display:flex;flex-direction:column;align-items:center}
.cv-icon{font-size:5rem;margin-bottom:1.5rem;filter:drop-shadow(0 0 20px rgba(100,255,218,.3))}
.resume-desc{color:var(--txt-muted);font-size:.95rem;line-height:1.8;margin-bottom:2rem;max-width:500px;text-align:center}
.resume-note{margin-top:1.5rem;font-family:'Space Mono',monospace;font-size:.72rem;color:var(--txt-muted);letter-spacing:1px;border:1px solid var(--border);padding:.6rem 1.2rem;border-radius:3px}
.resume-quick{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:3rem;width:100%;text-align:left}
.rq-card{background:var(--card);border:1px solid var(--border);padding:1.2rem;border-radius:4px}
.rq-card h4{font-family:'Space Mono',monospace;font-size:.7rem;color:var(--teal);letter-spacing:2px;text-transform:uppercase;margin-bottom:.8rem}
.rq-item{font-size:.8rem;color:var(--txt-muted);padding:.3rem 0;border-bottom:1px solid var(--border)}
.rq-item:last-child{border-bottom:none}

/* ── CONTACT ─────────────────────────────────────── */
#contact{background:var(--surface);display:flex;align-items:center}
.contact-inner{max-width:700px}
.contact-intro{font-size:1rem;color:var(--txt-muted);line-height:1.8;margin-bottom:3rem}
.contact-links{display:flex;flex-direction:column;gap:1.2rem}
.contact-link{display:flex;align-items:center;gap:1.2rem;padding:1.2rem 1.5rem;border:1px solid var(--border);background:var(--card);text-decoration:none;color:var(--txt);transition:.3s;border-radius:4px;position:relative;overflow:hidden}
.contact-link::before{content:'';position:absolute;inset:0;background:var(--teal-dim);transform:translateX(-100%);transition:.4s}
.contact-link:hover::before{transform:translateX(0)}
.contact-link:hover{border-color:var(--teal);color:var(--teal)}
.contact-link:hover .cl-label{color:var(--teal)}
.cl-icon{font-size:1.3rem;z-index:1;width:30px;text-align:center}
.cl-body{z-index:1}
.cl-label{font-family:'Space Mono',monospace;font-size:.7rem;letter-spacing:2px;text-transform:uppercase;color:var(--teal);display:block;margin-bottom:.1rem;transition:.3s}
.cl-value{font-size:.9rem}

/* ── FOOTER ──────────────────────────────────────── */
footer{text-align:center;padding:2rem;border-top:1px solid var(--border);font-family:'Space Mono',monospace;font-size:.72rem;color:var(--txt-muted);letter-spacing:1px}
footer span{color:var(--teal)}

/* ── RESPONSIVE ──────────────────────────────────── */
@media(max-width:900px){
  .about-grid{grid-template-columns:1fr}
  .skills-grid{grid-template-columns:1fr}
  .project-meta{grid-template-columns:1fr}
  .pm-block.full{grid-column:1}
  .resume-quick{grid-template-columns:1fr}
  .nav-links{gap:1rem}
}
@media(max-width:600px){
  section{padding:calc(var(--nav-h) + 3rem) 6% 4rem}
  #home{padding:0 6%}
  .nav-links{display:none}
}
</style>
</head>
<body>

<!-- ─── NAV ─────────────────────────────────────────── -->
<nav id="navbar">
  <a href="#home" class="logo">UN</a>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#resume">Resume</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- ─── HOME ─────────────────────────────────────────── -->
<section id="home">
  <canvas id="particles"></canvas>
  <div class="hero-content">
    <div class="hero-eyebrow">Physicist &amp; Data Scientist</div>
    <h1 class="hero-title">Udoka<br/><span>Nwankwo</span></h1>
    <p class="hero-subtitle">
      As a highly motivated Theoretical and Computational Material Physicist specialising in atomistic modelling and molecular dynamics simulation of emerging materials, with a strong foundation in Data Science, I am seeking a challenging role that leverages my analytical skills, programming expertise, and passion for data-driven insights to drive innovation and solve complex problems.
    </p>
    <div class="tags-row">
      <span class="tag">Data Science</span>
      <span class="tag">Physics</span>
      <span class="tag">Machine Learning</span>
      <span class="tag">Python</span>
      <span class="tag">Data Analysis</span>
      <span class="tag">Statistical Modeling</span>
      <span class="tag">Computational Physics</span>
      <span class="tag">Data Visualization</span>
      <span class="tag">Scientific Computing</span>
      <span class="tag">Molecular Dynamics</span>
    </div>
    <div class="hero-cta">
      <a href="#projects" class="btn-primary">View Projects</a>
      <a href="#resume" class="btn-secondary">Download CV</a>
    </div>
  </div>
  <div class="scroll-hint"><span>Scroll</span><div class="arrow"></div></div>
</section>

<!-- ─── ABOUT ─────────────────────────────────────────── -->
<section id="about">
  <div class="section-label">01 / About Me</div>
  <h2 class="section-title">The Person<br/>Behind the Physics</h2>
  <div class="section-divider"></div>
  <div class="about-grid reveal">
    <div>
      <div class="about-bio">
        <p>Hi, I'm Udoka Nwankwo, a highly motivated and accomplished physicist with a strong background in computational materials science and molecular dynamics simulations, currently expanding my expertise into Data Science.</p>
        <p>I hold a Ph.D. in Applied Physics from The Hong Kong Polytechnic University, where I developed a long-range Coulomb interaction method for reactive atomistic simulations. My research spans theoretical physics, computational materials science, and machine learning, with publications in reputable journals and presentations at international conferences.</p>
        <p>I have also worked as an assistant lecturer and teaching assistant, sharing my knowledge with students and mentoring final-year projects. My goal is to leverage my skills to contribute to innovative research and development in materials science and related fields.</p>
      </div>
      <div class="strengths">
        <h4>Focus Areas</h4>
        <div class="strength-item"><span>Data-driven analytics &amp; scientific insight extraction</span></div>
        <div class="strength-item"><span>Machine Learning for Materials Property Prediction</span></div>
        <div class="strength-item"><span>ML / Transfer Learning for Adaptive Diagnostics</span></div>
        <div class="strength-item"><span>Molecular Dynamics Simulation &amp; Atomistic Modelling</span></div>
      </div>
    </div>
    <div>
      <div class="section-label" style="margin-bottom:1.5rem">Education</div>
      <div class="edu-timeline">
        <div class="edu-item">
          <div class="edu-degree">Ph.D. Applied Physics</div>
          <div class="edu-major">Theoretical &amp; Computational Materials Science</div>
          <div class="edu-school">The Hong Kong Polytechnic University (PolyU)<br/>Hong Kong SAR, China</div>
          <div class="edu-year">2023</div>
        </div>
        <div class="edu-item">
          <div class="edu-degree">M.Sc. Theoretical Physics</div>
          <div class="edu-major">Theoretical Physics</div>
          <div class="edu-school">African University of Science and Technology (AUST)<br/>Abuja, Nigeria</div>
          <div class="edu-year">2014</div>
        </div>
        <div class="edu-item">
          <div class="edu-degree">B.Sc. Physics &amp; Astronomy</div>
          <div class="edu-major">Physics &amp; Astronomy</div>
          <div class="edu-school">University of Nigeria Nsukka (UNN)<br/>Enugu State, Nigeria</div>
          <div class="edu-year">2011</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── SKILLS ─────────────────────────────────────────── -->
<section id="skills">
  <div class="section-label">02 / Skills</div>
  <h2 class="section-title">Tools &amp;<br/>Capabilities</h2>
  <div class="section-divider"></div>
  <div class="skills-grid reveal">
    <div class="skill-card">
      <h3>Technical &amp; Programming</h3>
      <div class="sk-sub">Languages &amp; Computation</div>
      <div class="skill-tags">
        <span class="sk-tag">Python</span>
        <span class="sk-tag">R</span>
        <span class="sk-tag">C++</span>
        <span class="sk-tag">SQL / MySQL</span>
        <span class="sk-tag">LaTeX</span>
        <span class="sk-tag">LAMMPS</span>
        <span class="sk-tag">Quantum ESPRESSO</span>
        <span class="sk-tag">VASP</span>
        <span class="sk-tag">Gnuplot</span>
        <span class="sk-tag">OVITO</span>
        <span class="sk-tag">VMD</span>
        <span class="sk-tag">AVOGADRO</span>
        <span class="sk-tag">VESTA</span>
        <span class="sk-tag">KNIME</span>
        <span class="sk-tag">WEKA</span>
      </div>
    </div>
    <div class="skill-card">
      <h3>Data Science &amp; ML</h3>
      <div class="sk-sub">Libraries &amp; Frameworks</div>
      <div class="skill-tags">
        <span class="sk-tag">Pandas</span>
        <span class="sk-tag">NumPy</span>
        <span class="sk-tag">Scikit-learn</span>
        <span class="sk-tag">TensorFlow</span>
        <span class="sk-tag">PyTorch</span>
        <span class="sk-tag">Matplotlib</span>
        <span class="sk-tag">Seaborn</span>
        <span class="sk-tag">Jupyter</span>
        <span class="sk-tag">Statistical Modeling</span>
        <span class="sk-tag">Data Visualization</span>
        <span class="sk-tag">NLP</span>
        <span class="sk-tag">Deep Learning</span>
        <span class="sk-tag">CNN / PINN</span>
        <span class="sk-tag">Reinforcement Learning</span>
      </div>
    </div>
    <div class="skill-card">
      <h3>Business &amp; Research</h3>
      <div class="sk-sub">Analytical &amp; Leadership</div>
      <div class="skill-tags">
        <span class="sk-tag amber">Data-Driven Decision Making</span>
        <span class="sk-tag amber">Metrics Definition &amp; Tracking</span>
        <span class="sk-tag amber">Problem Framing</span>
        <span class="sk-tag amber">Project Management</span>
        <span class="sk-tag amber">Technical Writing</span>
        <span class="sk-tag amber">Research &amp; Publication</span>
        <span class="sk-tag amber">Teaching &amp; Mentoring</span>
        <span class="sk-tag amber">Reporting &amp; Storytelling</span>
      </div>
    </div>
  </div>
</section>

<!-- ─── PROJECTS ─────────────────────────────────────────── -->
<section id="projects">
  <div class="section-label">03 / Projects</div>
  <h2 class="section-title">Selected<br/>Work</h2>
  <div class="section-divider"></div>
  <div class="projects-grid">

    <!-- PROJECT 1 -->
    <div class="project-card reveal">
      <div class="project-header">
        <div class="project-title">Farm Defence: Game Against Invading Animals Based on Reinforcement Learning</div>
        <div class="project-time">Feb 2026</div>
      </div>
      <div class="project-meta">
        <div class="pm-block">
          <div class="pm-label">Problem</div>
          <div class="pm-text">Designed and implemented an RL-based game where an autonomous AI agent learns to protect crops from intruding boars, training the agent to make optimal decisions to maximise crop protection in a dynamic environment.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Data</div>
          <div class="pm-text">No external data source; the game environment itself generates experiential data through agent-environment interaction during training episodes.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Approach</div>
          <div class="pm-text">Deep Q-Network (DQN) reinforcement learning algorithm; Pygame for UI and game environment simulation.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Outcome / Impact</div>
          <div class="pm-text">Demonstrated effective use of DQN to train an autonomous agent. Achieved optimal policy convergence, consistent performance, and adaptation to dynamic environment changes. Provided key insights into critical factors for RL success.</div>
        </div>
      </div>
      <div class="project-contribution"><strong>Contribution</strong>Solely carried out and completed this project end-to-end.</div>
    </div>

    <!-- PROJECT 2 -->
    <div class="project-card reveal">
      <div class="project-header">
        <div class="project-title">ML-Driven Prediction of Sintering Properties in Cu Nanoparticles via CNN and PINN</div>
        <div class="project-time">Mar 2026</div>
      </div>
      <div class="project-meta">
        <div class="pm-block">
          <div class="pm-label">Problem</div>
          <div class="pm-text">Employed CNN and PINN as ML surrogates to predict sintering properties of Cu-Cu nanoparticles, bypassing the high computational cost of full MD simulations.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Data</div>
          <div class="pm-text">Generated via Molecular Dynamics (MD) simulation of Cu-Cu nanoparticles sintering at varying conditions in LAMMPS; post-processed atomic trajectories into ML-applicable datasets.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Approach</div>
          <div class="pm-text">MD-generated data-driven ML pipeline using Convolutional Neural Networks (CNN) and Physics-Informed Neural Networks (PINN).</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Outcome / Impact</div>
          <div class="pm-text">Both CNN and PINN substantially outperformed the classical Kuczynski analytical model. CNN excelled at neck radius/ratio predictions; PINN surpassed for shrinkage and density. MSD prediction remained a shared challenge.</div>
        </div>
      </div>
      <div class="project-contribution"><strong>Contribution</strong>Led the project from MD simulation design through data post-processing, ML model training, evaluation, and final reporting.</div>
    </div>

    <!-- PROJECT 3 -->
    <div class="project-card reveal">
      <div class="project-header">
        <div class="project-title">Efficient Domain Adaptation of GPT-2 for Legal Text Generation with LoRA</div>
        <div class="project-time">Mar 2026</div>
      </div>
      <div class="project-meta">
        <div class="pm-block">
          <div class="pm-label">Problem</div>
          <div class="pm-text">Can an adapted parameter set optimise a pre-trained language model such that its application on a subset of legal text closely represents the true full distribution, while minimising computational overhead?</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Data</div>
          <div class="pm-text">NLP-AUEB/eurlex dataset from HuggingFace — a corpus of European Union legal texts in multiple languages.</div>
        </div>
        <div class="pm-block">
          <div class="pm-label">Approach</div>
          <div class="pm-text">GPT-2 with Byte Pair Encoding (BPE) tokenization and Low-Rank Adapter (LoRA) Parameter-Efficient Fine-Tuning (PEFT) for domain adaptation.</div>
        </div>
        <div class="pm-block full">
          <div class="pm-label">Outcome / Impact</div>
          <div class="pm-text">LoRA (r=8) achieved strong domain adaptation with only 294,912 trainable parameters (0.236% of GPT-2). Improved over zero-shot GPT-2: PPL 41.99 → 6.89 | BLEU-4 0.46 → 17.07 | ROUGE-L 0.084 → 0.303. Full fine-tuning achieved best perplexity (PPL 4.49), but LoRA showed superior overlap-based generation scores, highlighting different optimisation strengths.</div>
        </div>
      </div>
      <div class="project-contribution"><strong>Contribution</strong>Contributed from topic ideation and description through the full coding pipeline, project report writing, and presentation preparation.</div>
    </div>

  </div>
</section>

<!-- ─── RESUME ─────────────────────────────────────────── -->
<section id="resume">
  <div class="section-label">04 / Resume</div>
  <h2 class="section-title">Curriculum<br/>Vitae</h2>
  <div class="section-divider" style="margin:1.5rem auto 3rem"></div>
  <div class="resume-inner reveal">
    <div class="cv-icon">📄</div>
    <p class="resume-desc">Download my full CV for a complete overview of my academic background, research experience, publications, and technical skills.</p>
    <a href="CV.pdf" download class="btn-primary" style="font-size:.85rem;padding:1rem 2.5rem;">⬇ &nbsp;Download CV (PDF)</a>
    <p class="resume-note">&#128204; Upload your CV.pdf file to the same GitHub repository to enable this button.</p>
    <div class="resume-quick">
      <div class="rq-card">
        <h4>Education</h4>
        <div class="rq-item">Ph.D. Applied Physics — PolyU HK (2023)</div>
        <div class="rq-item">M.Sc. Theoretical Physics — AUST (2014)</div>
        <div class="rq-item">B.Sc. Physics &amp; Astronomy — UNN (2011)</div>
      </div>
      <div class="rq-card">
        <h4>Research</h4>
        <div class="rq-item">Coulomb interaction method for reactive MD</div>
        <div class="rq-item">ML surrogates for nanomaterials</div>
        <div class="rq-item">RL-based autonomous agents</div>
        <div class="rq-item">LLM fine-tuning with PEFT/LoRA</div>
      </div>
      <div class="rq-card">
        <h4>Academic Roles</h4>
        <div class="rq-item">Assistant Lecturer</div>
        <div class="rq-item">Teaching Assistant</div>
        <div class="rq-item">Final-Year Project Mentor</div>
        <div class="rq-item">International Conference Presenter</div>
      </div>
    </div>
  </div>
</section>

<!-- ─── CONTACT ─────────────────────────────────────────── -->
<section id="contact">
  <div class="section-label">05 / Contact</div>
  <h2 class="section-title">Get In<br/>Touch</h2>
  <div class="section-divider"></div>
  <div class="contact-inner reveal">
    <p class="contact-intro">I am actively seeking research positions, data science roles, and collaborative opportunities. Whether you have a project, an opening, or just want to connect — my inbox is open.</p>
    <div class="contact-links">
      <a href="mailto:engelsudoka@gmail.com" class="contact-link">
        <div class="cl-icon">✉</div>
        <div class="cl-body"><span class="cl-label">Email</span><span class="cl-value">engelsudoka@gmail.com</span></div>
      </a>
      <a href="https://github.com/engelsudoka" target="_blank" class="contact-link">
        <div class="cl-icon">⌥</div>
        <div class="cl-body"><span class="cl-label">GitHub</span><span class="cl-value">github.com/engelsudoka</span></div>
      </a>
      <a href="https://orcid.org/0000-0003-1049-6831" target="_blank" class="contact-link">
        <div class="cl-icon">◎</div>
        <div class="cl-body"><span class="cl-label">ORCID</span><span class="cl-value">0000-0003-1049-6831 — Udoka Nwankwo</span></div>
      </a>
    </div>
  </div>
</section>

<!-- ─── FOOTER ─────────────────────────────────────────── -->
<footer>
  <p>Designed &amp; built by <span>Udoka Nwankwo</span> &nbsp;·&nbsp; Hosted on <span>GitHub Pages</span></p>
</footer>

<script>
// ── PARTICLES ──────────────────────────────────────────
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');
let particles = [];
function resize(){canvas.width=window.innerWidth;canvas.height=window.innerHeight}
resize();
window.addEventListener('resize',resize);
class Particle{
  constructor(){this.reset()}
  reset(){
    this.x=Math.random()*canvas.width;
    this.y=Math.random()*canvas.height;
    this.r=Math.random()*1.5+.3;
    this.vx=(Math.random()-.5)*.2;
    this.vy=(Math.random()-.5)*.2;
    this.alpha=Math.random()*.7+.1;
    this.color=Math.random()>.7?'100,255,218':'100,120,200';
  }
  draw(){
    ctx.beginPath();
    ctx.arc(this.x,this.y,this.r,0,Math.PI*2);
    ctx.fillStyle=`rgba(${this.color},${this.alpha})`;
    ctx.fill();
  }
  update(){
    this.x+=this.vx;this.y+=this.vy;
    if(this.x<0||this.x>canvas.width||this.y<0||this.y>canvas.height)this.reset();
  }
}
for(let i=0;i<120;i++)particles.push(new Particle());
// Draw connections
function drawConnections(){
  for(let i=0;i<particles.length;i++){
    for(let j=i+1;j<particles.length;j++){
      const dx=particles[i].x-particles[j].x;
      const dy=particles[i].y-particles[j].y;
      const d=Math.sqrt(dx*dx+dy*dy);
      if(d<120){
        ctx.beginPath();
        ctx.strokeStyle=`rgba(100,255,218,${.08*(1-d/120)})`;
        ctx.lineWidth=.5;
        ctx.moveTo(particles[i].x,particles[i].y);
        ctx.lineTo(particles[j].x,particles[j].y);
        ctx.stroke();
      }
    }
  }
}
function animate(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  drawConnections();
  particles.forEach(p=>{p.update();p.draw()});
  requestAnimationFrame(animate);
}
animate();

// ── SCROLL REVEAL ──────────────────────────────────────
const reveals=document.querySelectorAll('.reveal');
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target)}});
},{threshold:.12});
reveals.forEach(r=>obs.observe(r));

// ── ACTIVE NAV ──────────────────────────────────────────
const sections=document.querySelectorAll('section[id]');
const navLinks=document.querySelectorAll('.nav-links a');
window.addEventListener('scroll',()=>{
  let current='';
  sections.forEach(s=>{if(window.scrollY>=s.offsetTop-100)current=s.id});
  navLinks.forEach(a=>{
    a.classList.remove('active');
    if(a.getAttribute('href')==='#'+current)a.classList.add('active');
  });
});
</script>
</body>
</html>
