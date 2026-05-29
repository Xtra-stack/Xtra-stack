<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Ajay Dhar Dubey — GitHub README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
:root{
  --bg:#0d1117;--bg2:#161b22;--bg3:#21262d;
  --border:#30363d;--border2:#21262d;
  --txt:#e6edf3;--txt2:#c9d1d9;--txt3:#8b949e;
  --purple:#7F77DD;--teal:#5DCAA5;--amber:#ffa657;--blue:#58a6ff;--red:#ff7b72;
  --purpleDim:#3C348920;--tealDim:#5DCAA520;
  --mono:'JetBrains Mono',monospace;
  --sans:'Space Grotesk',sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{background:#010409}
body{font-family:var(--sans);background:#010409;color:var(--txt);min-height:100vh;padding:2rem 1rem}

.page{max-width:900px;margin:0 auto;background:var(--bg);border-radius:16px;overflow:hidden;border:0.5px solid var(--border)}

/* ── HEADER ── */
.hero{position:relative;overflow:hidden;padding:3rem 2.5rem 2rem;text-align:center;background:var(--bg)}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(var(--border2) 1px,transparent 1px),linear-gradient(90deg,var(--border2) 1px,transparent 1px);background-size:40px 40px;opacity:.3}
.hero-glow{position:absolute;top:-60px;left:50%;transform:translateX(-50%);width:500px;height:300px;background:radial-gradient(ellipse,rgba(127,119,221,.15) 0%,transparent 70%);pointer-events:none}
.hero-content{position:relative;z-index:1}

.logo-wrap{margin:0 auto 1.5rem;display:inline-block}
.logo-ring{animation:ringDraw 2s ease forwards}
@keyframes ringDraw{from{stroke-dashoffset:220}to{stroke-dashoffset:0}}
.logo-inner{animation:fadeUp .8s .3s ease both}

.hero-label{font-family:var(--mono);font-size:11px;color:var(--purple);letter-spacing:3px;text-transform:uppercase;margin-bottom:.5rem;animation:fadeUp .6s .4s ease both;opacity:0;animation-fill-mode:forwards}
.hero-name{font-size:42px;font-weight:700;color:var(--txt);letter-spacing:-1.5px;line-height:1;margin-bottom:.75rem;animation:fadeUp .6s .5s ease both;opacity:0;animation-fill-mode:forwards}
.hero-name span{color:var(--purple)}
.hero-typing{font-family:var(--mono);font-size:14px;color:var(--blue);min-height:22px;margin-bottom:1.25rem;animation:fadeUp .6s .6s ease both;opacity:0;animation-fill-mode:forwards}
.cur{display:inline-block;width:2px;height:14px;background:var(--blue);vertical-align:middle;animation:blink 1s step-end infinite;margin-left:1px}

.hero-badges{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin-bottom:1.25rem;animation:fadeUp .6s .7s ease both;opacity:0;animation-fill-mode:forwards}
.hbadge{font-family:var(--mono);font-size:10px;font-weight:500;padding:4px 12px;border-radius:20px;letter-spacing:.5px}
.hb-p{background:#26215C;color:#CECBF6;border:0.5px solid #534AB7}
.hb-t{background:#04342C;color:#9FE1CB;border:0.5px solid #0F6E56}
.hb-b{background:#042C53;color:#B5D4F4;border:0.5px solid #185FA5}
.hb-c{background:#4A1B0C;color:#F5C4B3;border:0.5px solid #993C1D}
.hb-g{background:#173404;color:#C0DD97;border:0.5px solid #3B6D11}

.social-row{display:flex;gap:8px;justify-content:center;flex-wrap:wrap;animation:fadeUp .6s .8s ease both;opacity:0;animation-fill-mode:forwards}
.sbtn{display:inline-flex;align-items:center;gap:6px;font-family:var(--mono);font-size:11px;font-weight:500;padding:6px 14px;border-radius:6px;text-decoration:none;transition:opacity .2s}
.sbtn:hover{opacity:.8}
.sb-li{background:#0A66C2;color:#fff}.sb-gh{background:#161b22;color:var(--txt);border:0.5px solid var(--border)}.sb-mail{background:#EA4335;color:#fff}.sb-port{background:var(--purple);color:#fff}

/* ── LAYOUT ── */
.body{padding:0 2rem 2rem}
.section{margin-top:2rem}
.sec-head{display:flex;align-items:center;gap:10px;margin-bottom:1rem}
.sec-icon{width:28px;height:28px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0}
.si-p{background:#26215C}.si-t{background:#04342C}.si-b{background:#042C53}.si-a{background:#412402}
.sec-title{font-size:14px;font-weight:600;color:var(--txt);font-family:var(--mono)}
.sec-line{flex:1;height:.5px;background:var(--border)}

/* ── CODE BLOCK ── */
.code-wrap{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;overflow:hidden;font-family:var(--mono);font-size:12px;line-height:1.9}
.code-bar{background:var(--bg3);padding:8px 14px;display:flex;align-items:center;gap:6px;border-bottom:0.5px solid var(--border)}
.dot-r{width:10px;height:10px;border-radius:50%;background:#ff5f57}
.dot-y{width:10px;height:10px;border-radius:50%;background:#febc2e}
.dot-g{width:10px;height:10px;border-radius:50%;background:#28c840}
.code-fname{font-family:var(--mono);font-size:11px;color:var(--txt3);margin-left:4px}
.code-body{padding:1rem 1.25rem;position:relative;overflow:hidden}
.scanline{position:absolute;left:0;right:0;height:80px;background:linear-gradient(transparent,rgba(127,119,221,.04),transparent);animation:scan 5s linear infinite;pointer-events:none}
@keyframes scan{0%{top:-80px}100%{top:100%}}
.kw{color:#ff7b72}.str{color:#a5d6ff}.key{color:#79c0ff}.val{color:#ffa657}.cmt{color:#8b949e}.fn{color:#d2a8ff}.op{color:#e6edf3}
.indent{padding-left:1.5rem}
.indent2{padding-left:3rem}

/* ── SKILL PILLS ── */
.skill-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(120px,1fr));gap:7px}
.skill-pill{background:var(--bg2);border:0.5px solid var(--border);border-radius:7px;padding:8px 11px;font-family:var(--mono);font-size:11px;color:var(--txt2);display:flex;align-items:center;gap:7px;transition:border-color .2s,transform .2s;cursor:default}
.skill-pill:hover{border-color:var(--purple);transform:translateY(-2px)}
.sdot{width:7px;height:7px;border-radius:50%;flex-shrink:0}

/* ── CHARTS ── */
.charts-row{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-top:1rem}
.chart-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:1rem}
.chart-label{font-family:var(--mono);font-size:10px;color:var(--txt3);text-transform:uppercase;letter-spacing:1px;margin-bottom:.75rem}
.chart-wrap{position:relative;height:200px}
.radar-wrap{position:relative;height:220px}

/* ── PROFICIENCY BARS ── */
.prof-list{display:flex;flex-direction:column;gap:10px}
.prof-item{}
.prof-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:5px}
.prof-name{font-family:var(--mono);font-size:11px;color:var(--txt2)}
.prof-pct{font-family:var(--mono);font-size:11px;color:var(--purple)}
.prof-track{height:5px;background:var(--bg3);border-radius:3px;overflow:hidden}
.prof-fill{height:100%;border-radius:3px;background:linear-gradient(90deg,var(--purple),var(--teal));transform-origin:left;animation:barGrow .8s ease both}
@keyframes barGrow{from{transform:scaleX(0)}to{transform:scaleX(1)}}

/* ── PROJECT CARDS ── */
.proj-grid{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
.proj-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:1.1rem;transition:border-color .2s,transform .25s;animation:floatCard 5s ease-in-out infinite}
.proj-card:hover{border-color:var(--purple);transform:translateY(-4px) !important}
.proj-card:nth-child(2){animation-delay:1.4s}
.proj-card:nth-child(3){animation-delay:2.8s}
.proj-card:nth-child(4){animation-delay:0.7s}
@keyframes floatCard{0%,100%{transform:translateY(0)}50%{transform:translateY(-5px)}}
.proj-top{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:.5rem}
.proj-icon{width:36px;height:36px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.pi-p{background:#26215C}.pi-t{background:#04342C}.pi-b{background:#042C53}.pi-a{background:#412402}
.proj-live{display:inline-flex;align-items:center;gap:4px;font-family:var(--mono);font-size:9px;padding:3px 8px;border-radius:20px;background:var(--tealDim);color:var(--teal);border:0.5px solid var(--teal)}
.live-dot{width:5px;height:5px;border-radius:50%;background:var(--teal);animation:pulse 1.5s ease-in-out infinite}
@keyframes pulse{0%,100%{opacity:.5;transform:scale(1)}50%{opacity:1;transform:scale(1.3)}}
.proj-title{font-size:14px;font-weight:600;color:var(--txt);margin-bottom:.35rem;margin-top:.5rem}
.proj-sub{font-size:12px;color:var(--txt3);line-height:1.6;margin-bottom:.75rem}
.proj-tags{display:flex;flex-wrap:wrap;gap:4px}
.ptag{font-family:var(--mono);font-size:9px;padding:2px 7px;border-radius:20px;background:var(--bg3);color:var(--txt3);border:0.5px solid var(--border)}

/* ── STATS ROW ── */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:.75rem}
.stat-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:8px;padding:.9rem;text-align:center}
.stat-num{font-family:var(--mono);font-size:22px;font-weight:700;color:var(--purple)}
.stat-lbl{font-size:10px;color:var(--txt3);text-transform:uppercase;letter-spacing:.5px;margin-top:2px}

/* ── CONTRIB GRAPH ── */
.contrib-grid{display:flex;flex-wrap:wrap;gap:3px}
.cc{width:11px;height:11px;border-radius:2px}
.c0{background:var(--bg3);border:0.5px solid var(--border2)}
.c1{background:#0e4429}.c2{background:#006d32}.c3{background:#26a641}.c4{background:#39d353}

/* ── OSS CARDS ── */
.oss-grid{display:grid;grid-template-columns:1fr 1fr;gap:.75rem}
.oss-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:8px;padding:.9rem}
.oss-name{font-size:13px;font-weight:600;color:var(--txt);margin-bottom:.3rem;display:flex;align-items:center;gap:6px}
.oss-desc{font-size:11px;color:var(--txt3);line-height:1.6}
.oss-tag{display:inline-block;margin-top:6px;font-family:var(--mono);font-size:9px;padding:2px 8px;border-radius:20px;background:var(--tealDim);color:var(--teal);border:0.5px solid var(--teal)}

/* ── CERT ── */
.cert-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:8px;padding:.9rem 1rem;display:flex;align-items:center;gap:12px}
.cert-badge{width:40px;height:40px;border-radius:8px;background:#26215C;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
.cert-name{font-size:13px;font-weight:500;color:var(--txt)}
.cert-meta{font-family:var(--mono);font-size:10px;color:var(--txt3);margin-top:2px}

/* ── SOLAR ── */
.solar-box{display:flex;flex-direction:column;align-items:center;padding:1rem}
.solar{width:110px;height:110px;position:relative;display:flex;align-items:center;justify-content:center}
.sun{width:20px;height:20px;border-radius:50%;background:var(--amber);animation:pulse 2s ease-in-out infinite}
.oring{position:absolute;border-radius:50%;border:.5px solid var(--border)}
.or1{width:52px;height:52px}.or2{width:76px;height:76px}.or3{width:104px;height:104px}
.planet{position:absolute;border-radius:50%;top:50%;left:50%;transform-origin:0 0}
.p1{width:7px;height:7px;background:#61dafb;margin:-3.5px;animation:orbit1 3s linear infinite}
.p2{width:7px;height:7px;background:var(--teal);margin:-3.5px;animation:orbit2 5s linear infinite}
.p3{width:6px;height:6px;background:var(--red);margin:-3px;animation:orbit3 9s linear infinite}
@keyframes orbit1{from{transform:rotate(0deg) translateX(26px) rotate(0deg)}to{transform:rotate(360deg) translateX(26px) rotate(-360deg)}}
@keyframes orbit2{from{transform:rotate(60deg) translateX(38px) rotate(-60deg)}to{transform:rotate(420deg) translateX(38px) rotate(-420deg)}}
@keyframes orbit3{from{transform:rotate(180deg) translateX(52px) rotate(-180deg)}to{transform:rotate(540deg) translateX(52px) rotate(-540deg)}}

/* ── FOOTER ── */
.footer{background:var(--bg2);border-top:.5px solid var(--border);padding:1.5rem 2rem;text-align:center}
.footer-wave{width:100%;display:block;margin-bottom:.75rem}
.footer-links{display:flex;gap:8px;justify-content:center;flex-wrap:wrap;margin-bottom:.75rem}
.footer-text{font-family:var(--mono);font-size:11px;color:var(--txt3)}
.footer-text a{color:var(--blue);text-decoration:none}

/* ── ANIMATIONS ── */
@keyframes fadeUp{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
.fa1{animation:fadeUp .6s .2s ease both}
.fa2{animation:fadeUp .6s .4s ease both}
.fa3{animation:fadeUp .6s .6s ease both}
.fa4{animation:fadeUp .6s .8s ease both}
.fa5{animation:fadeUp .6s 1s ease both}
</style>
</head>
<body>

<div class="page">

<!-- HERO -->
<div class="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-content">

    <div class="logo-wrap">
      <svg width="80" height="80" viewBox="0 0 80 80">
        <defs>
          <linearGradient id="lg" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#7F77DD"/>
            <stop offset="100%" stop-color="#5DCAA5"/>
          </linearGradient>
        </defs>
        <circle cx="40" cy="40" r="37" fill="none" stroke="url(#lg)" stroke-width="1.5" stroke-dasharray="232" class="logo-ring"/>
        <circle cx="40" cy="40" r="30" fill="#161b22"/>
        <text x="40" y="33" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="9" fill="#8b949e">const</text>
        <text x="40" y="47" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="15" fill="#7F77DD" font-weight="700">AJD</text>
        <text x="40" y="60" text-anchor="middle" font-family="JetBrains Mono,monospace" font-size="8" fill="#5DCAA5">= dev()</text>
      </svg>
    </div>

    <div class="hero-label">Full-Stack Developer</div>
    <div class="hero-name">Ajay <span>Dhar</span> Dubey</div>
    <div class="hero-typing"><span id="typing"></span><span class="cur"></span></div>

    <div class="hero-badges">
      <span class="hbadge hb-p">React 18</span>
      <span class="hbadge hb-t">Node.js</span>
      <span class="hbadge hb-b">Docker</span>
      <span class="hbadge hb-c">B.Tech CSE '26</span>
      <span class="hbadge hb-g">Open Source</span>
    </div>

    <div class="social-row">
      <a class="sbtn sb-li" href="https://linkedin.com/in/ajay-dubey-7a8939260">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a class="sbtn sb-gh" href="https://github.com/Xtra-stack">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        GitHub
      </a>
      <a class="sbtn sb-mail" href="mailto:ajy2bey@gmail.com">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
      <a class="sbtn sb-port" href="https://my-portfolio-eta-flame-78.vercel.app">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Portfolio
      </a>
    </div>
  </div>
</div>

<div class="body">

<!-- ABOUT -->
<div class="section fa1">
  <div class="sec-head">
    <div class="sec-icon si-p">🧑‍💻</div>
    <div class="sec-title">about.js</div>
    <div class="sec-line"></div>
  </div>
  <div class="code-wrap">
    <div class="code-bar">
      <div class="dot-r"></div><div class="dot-y"></div><div class="dot-g"></div>
      <span class="code-fname">about.js</span>
    </div>
    <div class="code-body">
      <div class="scanline"></div>
      <div><span class="kw">const</span> <span class="key">ajay</span> <span class="op">=</span> {</div>
      <div class="indent"><span class="key">name</span><span class="op">:</span>     <span class="str">"Ajay Dhar Dubey"</span><span class="op">,</span></div>
      <div class="indent"><span class="key">role</span><span class="op">:</span>     <span class="str">"Full-Stack Developer"</span><span class="op">,</span></div>
      <div class="indent"><span class="key">degree</span><span class="op">:</span>   <span class="str">"B.Tech CSE @ Bundelkhand University (2026)"</span><span class="op">,</span></div>
      <div class="indent"><span class="key">stack</span><span class="op">:</span>    <span class="op">[</span><span class="str">"React"</span><span class="op">,</span> <span class="str">"Node.js"</span><span class="op">,</span> <span class="str">"MongoDB"</span><span class="op">,</span> <span class="str">"Docker"</span><span class="op">],</span></div>
      <div class="indent"><span class="key">open_to</span><span class="op">:</span>  <span class="op">[</span><span class="str">"SWE"</span><span class="op">,</span> <span class="str">"Full-Stack"</span><span class="op">,</span> <span class="str">"Backend Engineering"</span><span class="op">],</span></div>
      <div class="indent"><span class="key">offline</span><span class="op">:</span>  <span class="op">[</span><span class="str">"Chess ♟"</span><span class="op">,</span> <span class="str">"CompProg"</span><span class="op">,</span> <span class="str">"Writing"</span><span class="op">,</span> <span class="str">"Dancing"</span><span class="op">],</span></div>
      <div class="indent"><span class="key">mantra</span><span class="op">:</span>   <span class="fn">() =></span> <span class="str">"Ship it. Break it. Fix it better. 🚀"</span></div>
      <div><span class="op">};</span></div>
    </div>
  </div>
</div>

<!-- SKILLS -->
<div class="section fa2">
  <div class="sec-head">
    <div class="sec-icon si-t">⚡</div>
    <div class="sec-title">tech-stack.json</div>
    <div class="sec-line"></div>
  </div>
  <div class="skill-grid">
    <div class="skill-pill"><div class="sdot" style="background:#F7DF1E"></div>JavaScript</div>
    <div class="skill-pill"><div class="sdot" style="background:#61DAFB"></div>React 18</div>
    <div class="skill-pill"><div class="sdot" style="background:#339933"></div>Node.js</div>
    <div class="skill-pill"><div class="sdot" style="background:#47A248"></div>MongoDB</div>
    <div class="skill-pill"><div class="sdot" style="background:#2496ED"></div>Docker</div>
    <div class="skill-pill"><div class="sdot" style="background:#00599C"></div>C++</div>
    <div class="skill-pill"><div class="sdot" style="background:#010101;border:.5px solid #555"></div>Socket.io</div>
    <div class="skill-pill"><div class="sdot" style="background:#009639"></div>Nginx</div>
    <div class="skill-pill"><div class="sdot" style="background:#000000;border:.5px solid #555"></div>JWT/RBAC</div>
    <div class="skill-pill"><div class="sdot" style="background:#2088FF"></div>GitHub Actions</div>
    <div class="skill-pill"><div class="sdot" style="background:#646CFF"></div>Vite</div>
    <div class="skill-pill"><div class="sdot" style="background:#06B6D4"></div>Tailwind</div>
  </div>
</div>

<!-- CHARTS -->
<div class="section fa3">
  <div class="sec-head">
    <div class="sec-icon si-b">📊</div>
    <div class="sec-title">analytics.chart</div>
    <div class="sec-line"></div>
  </div>
  <div class="charts-row">
    <div class="chart-card">
      <div class="chart-label">Skill proficiency</div>
      <div class="prof-list" id="profList"></div>
    </div>
    <div class="chart-card">
      <div class="chart-label">Tech radar</div>
      <div class="radar-wrap"><canvas id="radarChart" role="img" aria-label="Radar chart of skill levels"></canvas></div>
    </div>
  </div>
  <div style="margin-top:1rem">
    <div class="chart-card">
      <div class="chart-label">Tech usage frequency</div>
      <div class="chart-wrap"><canvas id="barChart" role="img" aria-label="Bar chart of technology usage"></canvas></div>
    </div>
  </div>
</div>

<!-- PROJECTS -->
<div class="section fa3">
  <div class="sec-head">
    <div class="sec-icon si-a">🔥</div>
    <div class="sec-title">projects/</div>
    <div class="sec-line"></div>
  </div>
  <div class="proj-grid">

    <div class="proj-card">
      <div class="proj-top">
        <div class="proj-icon pi-p">🧠</div>
        <div class="proj-live"><div class="live-dot"></div>Live</div>
      </div>
      <div class="proj-title">VIE Platform</div>
      <div class="proj-sub">Role-based SDLC sim. Junior → Senior → Manager. Real task lifecycle with approval gates, Monaco Editor, JWT + RBAC, Nodemailer. Dockerised + GitHub Actions CI/CD.</div>
      <div class="proj-tags">
        <span class="ptag">React 18</span><span class="ptag">Node.js</span><span class="ptag">MongoDB</span><span class="ptag">Docker</span><span class="ptag">JWT</span><span class="ptag">Nginx</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-top">
        <div class="proj-icon pi-t">🌐</div>
        <div class="proj-live"><div class="live-dot"></div>GitHub</div>
      </div>
      <div class="proj-title">Network Inspector</div>
      <div class="proj-sub">C++ libpcap/Npcap sniffer → Node.js backend → Socket.io → React dashboard. Protocol analysis (HTTP, DNS, TCP, UDP) + suspicious traffic detection + Recharts.</div>
      <div class="proj-tags">
        <span class="ptag">C++</span><span class="ptag">Socket.io</span><span class="ptag">MongoDB</span><span class="ptag">React</span><span class="ptag">Recharts</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-top">
        <div class="proj-icon pi-b">📁</div>
        <div class="proj-live"><div class="live-dot"></div>Live</div>
      </div>
      <div class="proj-title">P2P File Share</div>
      <div class="proj-sub">Browser-to-browser via WebRTC data channels. Zero server-side storage — your files never touch a server. Tested up to 500MB transfers.</div>
      <div class="proj-tags">
        <span class="ptag">WebRTC</span><span class="ptag">Node.js</span><span class="ptag">Express</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-top">
        <div class="proj-icon pi-a">🪐</div>
        <div class="proj-live"><div class="live-dot"></div>Live</div>
      </div>
      <div class="proj-title">3D Solar Portfolio</div>
      <div class="proj-sub">Interactive Three.js solar system. Orbital animations, planet clicks, real-time camera controls. Optimized render loop holds 60fps on all devices.</div>
      <div class="proj-tags">
        <span class="ptag">Three.js</span><span class="ptag">JavaScript</span>
      </div>
      <div class="solar-box">
        <div class="solar">
          <div class="oring or1"></div><div class="oring or2"></div><div class="oring or3"></div>
          <div class="sun"></div>
          <div class="planet p1"></div><div class="planet p2"></div><div class="planet p3"></div>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- STATS -->
<div class="section fa4">
  <div class="sec-head">
    <div class="sec-icon si-p">📈</div>
    <div class="sec-title">github-stats</div>
    <div class="sec-line"></div>
  </div>
  <div class="stats-row">
    <div class="stat-card"><div class="stat-num" data-target="4">0</div><div class="stat-lbl">Projects</div></div>
    <div class="stat-card"><div class="stat-num" data-target="5">0</div><div class="stat-lbl">OSS Commits</div></div>
    <div class="stat-card"><div class="stat-num" data-target="8">0</div><div class="stat-lbl">Repos</div></div>
    <div class="stat-card"><div class="stat-num" data-target="12">0</div><div class="stat-lbl">Tech Stack</div></div>
  </div>

  <div style="margin-top:1rem;background:var(--bg2);border:.5px solid var(--border);border-radius:10px;padding:1rem">
    <div style="font-family:var(--mono);font-size:10px;color:var(--txt3);text-transform:uppercase;letter-spacing:1px;margin-bottom:.75rem">Contribution activity</div>
    <div class="contrib-grid" id="contrib"></div>
    <div style="display:flex;gap:6px;margin-top:8px;align-items:center">
      <span style="font-family:var(--mono);font-size:10px;color:var(--txt3)">Less</span>
      <div class="cc c0"></div><div class="cc c1"></div><div class="cc c2"></div><div class="cc c3"></div><div class="cc c4"></div>
      <span style="font-family:var(--mono);font-size:10px;color:var(--txt3)">More</span>
    </div>
  </div>
</div>

<!-- OSS -->
<div class="section fa4">
  <div class="sec-head">
    <div class="sec-icon si-t">🤝</div>
    <div class="sec-title">open-source/</div>
    <div class="sec-line"></div>
  </div>
  <div class="oss-grid">
    <div class="oss-card">
      <div class="oss-name">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#8b949e" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        Dating_Source_code
      </div>
      <div class="oss-desc">Contributed <code style="font-size:10px;color:var(--purple);background:var(--bg3);padding:1px 5px;border-radius:3px">updatePreferences</code> API with input validation and full test coverage.</div>
      <span class="oss-tag">✓ merged</span>
    </div>
    <div class="oss-card">
      <div class="oss-name">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#8b949e" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        CleanerX
      </div>
      <div class="oss-desc">Auth setup, middleware, cart &amp; wishlist, login fixes. 5 commits merged to the production branch.</div>
      <span class="oss-tag">✓ 5 commits to prod</span>
    </div>
  </div>
</div>

<!-- CERT -->
<div class="section fa5">
  <div class="sec-head">
    <div class="sec-icon si-a">🏅</div>
    <div class="sec-title">certifications</div>
    <div class="sec-line"></div>
  </div>
  <div class="cert-card">
    <div class="cert-badge">🏅</div>
    <div>
      <div class="cert-name">Internship Completion Certificate — Cognifyz Technologies</div>
      <div class="cert-meta">Aug 2025 &nbsp;·&nbsp; ID: CTI/A1/C182540 &nbsp;·&nbsp; Web Development Intern</div>
    </div>
  </div>
</div>

</div><!-- /body -->

<!-- FOOTER -->
<div class="footer">
  <svg class="footer-wave" viewBox="0 0 900 40" preserveAspectRatio="none" height="40">
    <path d="M0,20 C150,40 300,0 450,20 C600,40 750,0 900,20 L900,40 L0,40 Z" fill="#161b22"/>
  </svg>
  <div class="footer-links">
    <a class="sbtn sb-li" href="https://linkedin.com/in/ajay-dubey-7a8939260">LinkedIn</a>
    <a class="sbtn sb-gh" href="https://github.com/Xtra-stack">GitHub</a>
    <a class="sbtn sb-mail" href="mailto:ajy2bey@gmail.com">ajy2bey@gmail.com</a>
    <a class="sbtn sb-port" href="https://my-portfolio-eta-flame-78.vercel.app">Portfolio</a>
  </div>
  <div class="footer-text">Made with obsession, not templates &nbsp;·&nbsp; Last updated May 2026</div>
</div>

</div><!-- /page -->

<script>
const phrases=["Full-Stack Developer 🚀","React 18 + Node.js + Docker 🐳","Building real things that ship 🛠️","Open Source Contributor 🌟","B.Tech CSE '26 @ Bundelkhand Uni"];
let pi=0,ci=0,del=false;
const tel=document.getElementById("typing");
function type(){
  const p=phrases[pi];
  if(!del){tel.textContent=p.slice(0,++ci);if(ci===p.length){del=true;setTimeout(type,1800);return}}
  else{tel.textContent=p.slice(0,--ci);if(ci===0){del=false;pi=(pi+1)%phrases.length}}
  setTimeout(type,del?35:75);
}
type();

const profData=[
  {name:"React 18",pct:90,color:"#61DAFB"},
  {name:"Node.js",pct:88,color:"#339933"},
  {name:"MongoDB",pct:82,color:"#47A248"},
  {name:"Docker",pct:78,color:"#2496ED"},
  {name:"C++ / libpcap",pct:72,color:"#00599C"},
  {name:"WebRTC",pct:70,color:"#333"},
];
const pl=document.getElementById("profList");
profData.forEach((d,i)=>{
  pl.innerHTML+=`<div class="prof-item"><div class="prof-header"><span class="prof-name">${d.name}</span><span class="prof-pct">${d.pct}%</span></div><div class="prof-track"><div class="prof-fill" style="width:${d.pct}%;background:linear-gradient(90deg,${d.color},var(--teal));animation-delay:${i*0.1}s"></div></div></div>`;
});

new Chart(document.getElementById("radarChart"),{
  type:"radar",
  data:{
    labels:["React","Node.js","MongoDB","Docker","C++","WebRTC"],
    datasets:[{
      data:[90,88,82,78,72,70],
      backgroundColor:"rgba(127,119,221,0.18)",
      borderColor:"#7F77DD",
      borderWidth:1.5,
      pointBackgroundColor:"#7F77DD",
      pointBorderColor:"#0d1117",
      pointRadius:4,
      pointHoverRadius:6
    }]
  },
  options:{
    responsive:true,maintainAspectRatio:false,
    plugins:{legend:{display:false}},
    scales:{r:{
      angleLines:{color:"#21262d"},
      grid:{color:"#21262d"},
      pointLabels:{color:"#c9d1d9",font:{size:11,family:"JetBrains Mono"}},
      ticks:{display:false,stepSize:20},
      min:0,max:100
    }}
  }
});

new Chart(document.getElementById("barChart"),{
  type:"bar",
  data:{
    labels:["JS","React","Node","MongoDB","Docker","C++","Socket.io","Nginx"],
    datasets:[{
      data:[95,90,88,82,78,72,68,65],
      backgroundColor:["#F7DF1E30","#61DAFB30","#33993330","#47A24830","#2496ED30","#00599C30","#55555530","#00963930"],
      borderColor:["#F7DF1E","#61DAFB","#339933","#47A248","#2496ED","#00599C","#aaaaaa","#009639"],
      borderWidth:1.5,
      borderRadius:5,
      borderSkipped:false
    }]
  },
  options:{
    responsive:true,maintainAspectRatio:false,
    plugins:{legend:{display:false}},
    scales:{
      x:{grid:{color:"#21262d"},ticks:{color:"#8b949e",font:{size:11,family:"JetBrains Mono"}}},
      y:{grid:{color:"#21262d"},ticks:{color:"#8b949e",font:{size:10},callback:v=>v+"%"},min:0,max:100}
    }
  }
});

const cg=document.getElementById("contrib");
const lvls=[0,0,1,0,2,1,3,0,2,3,4,2,1,3,4,3,2,1,0,2,3,4,3,2,4,3,2,1,0,1,2,3,2,1,4,3,2,1,0,1,2,3,4,3,2,1,0,2,3,4,3,2,1,4,3,2,1,0,2,3,4,4,3,2,1,0,1,2,3,2,1,0,2,3,4,3,2,1,0,1,2,3,2,4,3,1,0,1,2,3,4,3,2,1,0,1,3,2,4,3,2,1,0,1,2,3,4,3,2,1];
lvls.forEach(l=>{const c=document.createElement("div");c.className=`cc c${l}`;cg.appendChild(c);});

const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.querySelectorAll("[data-target]").forEach(el=>{
        const target=+el.dataset.target;
        let n=0;
        const step=()=>{n=Math.min(n+1,target);el.textContent=n+(target>=10?"+":"");if(n<target)setTimeout(step,80);};
        step();
      });
      obs.unobserve(e.target);
    }
  });
},{threshold:.3});
document.querySelectorAll(".stats-row").forEach(el=>obs.observe(el));
</script>
</body>
</html>
