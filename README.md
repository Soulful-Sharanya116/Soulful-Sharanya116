<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sharanya Sasmal – Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&family=Fira+Code:wght@400;600&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:       #0d1117;
    --bg2:      #161b22;
    --bg3:      #1c2128;
    --border:   #30363d;
    --text:     #e6edf3;
    --muted:    #8b949e;
    --pink:     #f778ba;
    --purple:   #a371f7;
    --green:    #3fb950;
    --cyan:     #39d353;
    --orange:   #f78166;
    --yellow:   #e3b341;
    --blue:     #58a6ff;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    max-width: 900px;
    margin: 0 auto;
    padding: 0 16px 48px;
    font-size: 15px;
    line-height: 1.6;
  }

  /* ── HERO BANNER ── */
  .hero {
    background: linear-gradient(135deg, #1a0a2e 0%, #2d1b6b 40%, #1e1040 70%, #0d1117 100%);
    border-radius: 16px;
    margin: 20px 0;
    padding: 32px 36px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
    overflow: hidden;
    position: relative;
    min-height: 160px;
  }
  .hero-left { flex: 1; }
  .hero-name { font-size: 2rem; font-weight: 900; line-height: 1.1; margin-bottom: 4px; }
  .hero-name span { color: var(--pink); }
  .hero-sub { font-size: 0.75rem; color: var(--muted); margin-bottom: 10px; letter-spacing: 0.03em; }
  .hero-tagline { font-size: 0.9rem; color: #c9d1d9; }
  .hero-right {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 4px;
    font-size: 0.82rem;
    color: #c9d1d9;
    font-style: italic;
  }
  .hero-right span { display: block; text-align: right; }
  .hero-right .pink { color: var(--pink); font-weight: 700; }
  /* Illustration placeholder – a decorative monitor SVG-ish shape */
  .hero-illustration {
    width: 200px;
    height: 120px;
    flex-shrink: 0;
    position: relative;
  }
  .hero-illustration svg { width: 100%; height: 100%; }

  /* ── INTRO SECTION ── */
  .intro { margin: 32px 0; }
  .section-title {
    font-size: 1.5rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 12px;
  }
  .intro-grid {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 24px;
    align-items: start;
  }
  .intro-text { font-size: 0.95rem; color: #c9d1d9; margin-bottom: 16px; }
  .intro-bullets { list-style: none; display: flex; flex-direction: column; gap: 8px; }
  .intro-bullets li {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    font-size: 0.88rem;
    color: var(--text);
  }
  .intro-bullets li .icon { font-size: 1rem; flex-shrink: 0; margin-top: 1px; }

  .quote-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 22px;
    max-width: 220px;
    min-width: 200px;
    position: relative;
  }
  .quote-mark {
    font-size: 2rem;
    color: var(--pink);
    font-family: Georgia, serif;
    line-height: 1;
    margin-bottom: 6px;
  }
  .quote-text {
    font-size: 1rem;
    font-weight: 700;
    line-height: 1.4;
    color: var(--text);
  }
  .quote-mark-close {
    font-size: 2rem;
    color: var(--pink);
    font-family: Georgia, serif;
    line-height: 1;
    text-align: right;
    margin-top: 6px;
  }

  /* ── TECH STACK ── */
  .tech-section { margin: 36px 0; }
  .tech-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  .tech-title {
    font-size: 1.3rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .tech-title .bracket { color: var(--pink); font-family: 'Fira Code', monospace; }
  .always-learning {
    background: transparent;
    border: 1.5px solid var(--pink);
    color: var(--pink);
    border-radius: 20px;
    padding: 5px 14px;
    font-size: 0.78rem;
    font-weight: 600;
    display: flex;
    align-items: center;
    gap: 5px;
  }
  .always-learning::before { content: '♥'; }

  .tech-group { display: flex; align-items: center; gap: 12px; margin-bottom: 14px; }
  .tech-group-label {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 0.82rem;
    color: var(--muted);
    min-width: 160px;
    font-weight: 500;
  }
  .tech-group-label .dot {
    width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0;
  }
  .dot-pink   { background: var(--pink); }
  .dot-purple { background: var(--purple); }
  .dot-green  { background: #3fb950; }

  .badges { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 8px;
    font-size: 0.78rem;
    font-weight: 800;
    letter-spacing: 0.04em;
    color: #fff;
    text-transform: uppercase;
  }
  .badge svg, .badge img { width: 16px; height: 16px; object-fit: contain; }

  /* badge colors matched to image */
  .b-html5      { background: #e34c26; }
  .b-css3       { background: #1572b6; }
  .b-js         { background: #f7df1e; color: #000; }
  .b-figma      { background: #a259ff; }
  .b-cpp        { background: #0d4fa8; }
  .b-java       { background: #e76f00; }
  .b-python     { background: #3776ab; }
  .b-mysql      { background: #2d6d8e; }
  .b-matlab     { background: #e87722; }
  .b-git        { background: #f05032; }
  .b-github     { background: #24292e; border: 1px solid #444; }
  .b-arduino    { background: #00979d; }
  .b-blender    { background: #e87d0d; }

  /* ── GITHUB STATS ── */
  .stats-section { margin: 36px 0; }
  .stats-title {
    font-size: 1.3rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 20px;
  }
  .stats-title .bar-icon { color: var(--pink); font-size: 1.1rem; }

  .stats-cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-bottom: 16px; }
  .stat-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    display: flex;
    align-items: center;
    gap: 14px;
  }
  .stat-icon {
    width: 44px; height: 44px; border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.3rem; flex-shrink: 0;
  }
  .si-blue   { background: linear-gradient(135deg, #1a3a6b, #2d6bc4); }
  .si-red    { background: linear-gradient(135deg, #6b1a1a, #c44040); }
  .si-yellow { background: linear-gradient(135deg, #6b5a1a, #c4a040); }
  .stat-info { flex: 1; }
  .stat-number { font-size: 1.6rem; font-weight: 800; line-height: 1; }
  .stat-label { font-size: 0.82rem; color: var(--text); font-weight: 600; margin-top: 2px; }
  .stat-sub { font-size: 0.72rem; color: var(--muted); margin-top: 2px; }

  /* ── CONTRIBUTION + LANGUAGES ── */
  .bottom-grid { display: grid; grid-template-columns: 1.5fr 1fr; gap: 16px; margin-bottom: 36px; }

  .contrib-card, .lang-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
  }
  .card-title {
    font-size: 0.9rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 16px;
    color: var(--text);
  }

  /* Contribution graph */
  .contrib-months {
    display: flex;
    gap: 0;
    margin-bottom: 4px;
    padding-left: 36px;
  }
  .month-label {
    font-size: 0.65rem;
    color: var(--muted);
    flex: 1;
    text-align: left;
  }
  .contrib-grid { display: flex; gap: 0; }
  .day-labels {
    display: flex;
    flex-direction: column;
    gap: 2px;
    margin-right: 4px;
    padding-top: 0;
  }
  .day-label {
    font-size: 0.6rem;
    color: var(--muted);
    height: 11px;
    display: flex;
    align-items: center;
  }
  .day-label.hidden { color: transparent; }
  .weeks { display: flex; gap: 2px; }
  .week { display: flex; flex-direction: column; gap: 2px; }
  .cell {
    width: 11px; height: 11px; border-radius: 2px;
    background: #161b22;
    border: 1px solid rgba(255,255,255,0.04);
  }
  .c0 { background: #161b22; }
  .c1 { background: #0e4429; }
  .c2 { background: #006d32; }
  .c3 { background: #26a641; }
  .c4 { background: #39d353; }
  /* pink highlight */
  .cp { background: var(--pink); }

  .contrib-legend {
    display: flex;
    align-items: center;
    gap: 4px;
    margin-top: 8px;
    font-size: 0.65rem;
    color: var(--muted);
    justify-content: flex-end;
  }
  .legend-cell { width: 10px; height: 10px; border-radius: 2px; }

  /* Languages */
  .lang-item { margin-bottom: 10px; }
  .lang-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 4px;
    font-size: 0.82rem;
  }
  .lang-name { display: flex; align-items: center; gap: 6px; font-weight: 500; }
  .lang-dot { width: 9px; height: 9px; border-radius: 50%; }
  .lang-pct { color: var(--muted); font-size: 0.78rem; }
  .lang-bar { height: 7px; border-radius: 4px; }
  .lc-cpp    { background: linear-gradient(90deg, var(--pink), #f7a8d6); }
  .lc-py     { background: linear-gradient(90deg, var(--purple), #c8a5f9); }
  .lc-java   { background: linear-gradient(90deg, #7c8cf8, #a5adfc); }
  .lc-html   { background: linear-gradient(90deg, var(--blue), #8fcaff); }
  .lc-css    { background: linear-gradient(90deg, #56d8e4, #9aebf1); }

  /* ── CONNECT SECTION ── */
  .connect-section { margin: 36px 0 20px; }
  .connect-title {
    font-size: 1.3rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 6px;
  }
  .connect-sub { font-size: 0.88rem; color: var(--muted); margin-bottom: 16px; }
  .connect-buttons { display: flex; flex-wrap: wrap; gap: 10px; }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 9px 18px;
    border-radius: 8px;
    font-size: 0.82rem;
    font-weight: 700;
    color: #fff;
    text-decoration: none;
    cursor: pointer;
    border: none;
  }
  .cb-linkedin  { background: #0a66c2; }
  .cb-instagram { background: linear-gradient(135deg, #833ab4, #fd1d1d, #fcb045); }
  .cb-github    { background: #24292e; border: 1px solid #555; }
  .cb-gfg       { background: #2f8d46; }
  .cb-discord   { background: #5865f2; }
  .cb-email     { background: #d93025; }

  /* divider */
  .divider { border: none; border-top: 1px solid var(--border); margin: 28px 0; }

  /* tech bracket icon */
  .bracket-icon { font-family: 'Fira Code', monospace; color: var(--pink); font-weight: 700; }
</style>
</head>
<body>

<!-- ══ HERO BANNER ══ -->
<div class="hero">
  <div class="hero-left">
    <div class="hero-name">SHARANYA <span>SASMAL</span></div>
    <div class="hero-sub">Frontend Development &nbsp;|&nbsp; UI/UX Design &nbsp;|&nbsp; Web Technologies</div>
    <div class="hero-tagline">Turning ideas into meaningful<br>digital experiences</div>
  </div>

  <!-- decorative monitor illustration -->
  <div class="hero-illustration">
    <svg viewBox="0 0 220 130" xmlns="http://www.w3.org/2000/svg">
      <!-- monitor -->
      <rect x="10" y="5" width="170" height="105" rx="8" fill="#1c1a3a" stroke="#4b3f8f" stroke-width="2"/>
      <rect x="18" y="13" width="154" height="90" rx="4" fill="#12102a"/>
      <!-- chart lines -->
      <polyline points="24,90 50,70 75,78 100,55 125,60 150,35 162,42" fill="none" stroke="#f778ba" stroke-width="2.5"/>
      <polyline points="24,95 50,85 75,88 100,75 125,78 150,65 162,68" fill="none" stroke="#a371f7" stroke-width="1.8" stroke-dasharray="4,3"/>
      <!-- bars -->
      <rect x="30" y="72" width="14" height="18" rx="2" fill="#3a2e7a" opacity="0.8"/>
      <rect x="50" y="62" width="14" height="28" rx="2" fill="#4a3a9a" opacity="0.8"/>
      <rect x="70" y="55" width="14" height="35" rx="2" fill="#f778ba" opacity="0.7"/>
      <!-- pie donut -->
      <circle cx="148" cy="35" r="20" fill="none" stroke="#f778ba" stroke-width="8" stroke-dasharray="50 76"/>
      <circle cx="148" cy="35" r="20" fill="none" stroke="#a371f7" stroke-width="8" stroke-dasharray="30 96" stroke-dashoffset="-50"/>
      <!-- stand -->
      <rect x="80" y="110" width="30" height="6" rx="3" fill="#4b3f8f"/>
      <rect x="70" y="116" width="50" height="5" rx="2.5" fill="#4b3f8f"/>
      <!-- girl silhouette (simplified) -->
      <ellipse cx="195" cy="95" rx="14" ry="18" fill="#f7c5e0"/>
      <circle cx="195" cy="68" r="12" fill="#f7c5e0"/>
      <!-- hair -->
      <ellipse cx="194" cy="60" rx="13" ry="8" fill="#2c1a0e"/>
      <path d="M182 62 Q178 80 183 95" stroke="#2c1a0e" stroke-width="8" fill="none"/>
      <!-- shirt -->
      <ellipse cx="195" cy="95" rx="14" ry="18" fill="#f06292"/>
      <!-- arm pointing -->
      <line x1="185" y1="80" x2="165" y2="55" stroke="#f7c5e0" stroke-width="5" stroke-linecap="round"/>
      <!-- plant -->
      <rect x="205" y="105" width="8" height="15" rx="2" fill="#5c3d1e"/>
      <ellipse cx="209" cy="98" rx="10" ry="12" fill="#2e7d32"/>
      <ellipse cx="202" cy="103" rx="7" ry="9" fill="#388e3c"/>
    </svg>
  </div>

  <div class="hero-right">
    <span>Design</span>
    <span>Code</span>
    <span>Create</span>
    <span>Learn</span>
    <span class="pink">Grow</span>
    <span style="color:var(--pink);margin-top:4px;">——</span>
  </div>
</div>

<!-- ══ INTRO ══ -->
<div class="intro">
  <div class="section-title">👋 Hi there! I'm <span style="color:var(--pink);margin-left:6px;">Sharanya</span></div>
  <div class="intro-grid">
    <div>
      <div class="intro-text">A frontend developer who loves turning clean UI/UX designs into seamless digital experiences.</div>
      <ul class="intro-bullets">
        <li><span class="icon">🎓</span> Second-year Electronics and Computer Engineering student at Vellore Institute of Technology, Chennai.</li>
        <li><span class="icon">💡</span> Passionate about UI/UX design, web development, and creating user-centric solutions.</li>
        <li><span class="icon">🎯</span> Exploring the intersection of electronics and web technologies.</li>
        <li><span class="icon">🌱</span> Always learning, building, and looking for opportunities to grow.</li>
      </ul>
    </div>
    <div class="quote-card">
      <div class="quote-mark">"</div>
      <div class="quote-text">Good design turns ideas into opportunities.</div>
      <div class="quote-mark-close">"</div>
    </div>
  </div>
</div>

<hr class="divider"/>

<!-- ══ TECH STACK ══ -->
<div class="tech-section">
  <div class="tech-header">
    <div class="tech-title">
      <span class="bracket-icon">&lt;/&gt;</span> Tech Stack
    </div>
    <div class="always-learning">Always learning more...</div>
  </div>

  <!-- Web & Design -->
  <div class="tech-group">
    <div class="tech-group-label"><span class="dot dot-pink"></span>Web &amp; Design</div>
    <div class="badges">
      <span class="badge b-html5">
        <svg viewBox="0 0 32 32" fill="white"><path d="M5.9 0l2.2 25.1 7.9 2.2 7.9-2.2 2.2-25.1zm16 21.4l-5.9 1.7-5.9-1.7-.4-5.2h2.9l.2 2.7 3.2.9 3.2-.9.4-4.3H9.2L9 10.7h13.9zm-.5-8.7H10.6l-.2-2.9h11.2z"/></svg>
        HTML5
      </span>
      <span class="badge b-css3">
        <svg viewBox="0 0 32 32" fill="white"><path d="M5.9 0l2.2 25.1 7.9 2.2 7.9-2.2 2.2-25.1zm16 21.4l-5.9 1.7-5.9-1.7-.4-5.2h2.9l.2 2.7 3.2.9 3.2-.9.3-3.4H9l-.5-5.5h13.9l-.2 2.9H11.6l.2 1.9h9.6z"/></svg>
        CSS3
      </span>
      <span class="badge b-js">
        <svg viewBox="0 0 32 32"><rect width="32" height="32" fill="#f7df1e"/><path d="M19.6 25.2c.5.8 1.2 1.4 2.4 1.4 1 0 1.7-.5 1.7-1.2 0-.8-.7-1.1-1.8-1.6l-.6-.3c-1.8-.8-3-1.7-3-3.8 0-1.9 1.4-3.3 3.6-3.3 1.6 0 2.7.6 3.5 2l-1.9 1.2c-.4-.8-.9-1.1-1.6-1.1-.7 0-1.2.5-1.2 1.1 0 .8.5 1.1 1.6 1.5l.6.3c2.1.9 3.3 1.8 3.3 3.9 0 2.3-1.8 3.5-4.2 3.5-2.3 0-3.8-1.1-4.6-2.6zm-9.4.3c.4.7.7 1.2 1.5 1.2.7 0 1.2-.3 1.2-1.5v-8.1h2.4v8.1c0 2.5-1.4 3.6-3.6 3.6-1.9 0-3-1-3.6-2.2z"/></svg>
        JAVASCRIPT
      </span>
      <span class="badge b-figma">
        <svg viewBox="0 0 32 32" fill="white"><path d="M16 14.7a4 4 0 1 1 0 8 4 4 0 0 1 0-8zm-8-5.4a4 4 0 0 1 4-4h4v8h-4a4 4 0 0 1-4-4zm0 9.4a4 4 0 0 1 4-4h4v4a4 4 0 1 1-8 0zm8-13.4h4a4 4 0 0 1 0 8h-4V5.3zm4 8a4 4 0 1 1 0 8v-8z"/></svg>
        FIGMA
      </span>
    </div>
  </div>

  <!-- Programming & Databases -->
  <div class="tech-group">
    <div class="tech-group-label"><span class="dot dot-purple"></span>Programming &amp; Databases</div>
    <div class="badges">
      <span class="badge b-cpp">
        <svg viewBox="0 0 32 32" fill="white"><text x="4" y="22" font-size="16" font-weight="bold" font-family="monospace">C++</text></svg>
        C/C++
      </span>
      <span class="badge b-java">
        <svg viewBox="0 0 32 32" fill="white"><path d="M12 4c0 0-3 2.6-3 6.2 0 4 3.2 5.1 3.2 9.1 0 2.3-1.5 4.2-1.5 4.2s3.8-2 3.8-7c0-4.5-3.5-5.3-3.5-9.3C11 5.6 12 4 12 4zm4 4s-2 1.5-2 4.3c0 2.8 2.5 3.7 2.5 6.7 0 1.8-1 3-1 3s2.7-1.4 2.7-5c0-3.5-2.2-4-2.2-6.5 0-1.9.7-3 .7-3l-.7.5z"/></svg>
        JAVA
      </span>
      <span class="badge b-python">
        <svg viewBox="0 0 32 32" fill="white"><path d="M15.9 4C10 4 10.4 6.5 10.4 6.5V9h5.6v1H7.2S4 9.6 4 15.9s2.8 6.2 2.8 6.2H8v-3S7.9 16 11 16h9s2.8.1 2.8-2.8V7.2S23.3 4 15.9 4zm-1.6 2.1c.6 0 1 .4 1 1s-.4 1-1 1-1-.4-1-1 .4-1 1-1zm1.7 21.8C22 27.9 21.6 25.4 21.6 25.4V23H16v-1h8.8S28 22.4 28 16.1s-2.8-6.2-2.8-6.2H24v3S24.1 16 21 16h-9s-2.8-.1-2.8 2.8v5.9S8.7 27.9 16 27.9zm1.6-2c-.6 0-1-.4-1-1s.4-1 1-1 1 .4 1 1-.4 1-1 1z"/></svg>
        PYTHON
      </span>
      <span class="badge b-mysql">
        <svg viewBox="0 0 32 32" fill="white"><path d="M3 22.4s.2-6 6.8-6.6C16 15.2 21 14.6 21 10c0 0 .5 12.4-18 12.4z"/><path d="M21 10c0 2.8-1.6 4.4-5.2 5.3C21.8 13 26.5 9.3 26 4c0 0 0 3-5 6z" opacity=".6"/></svg>
        MYSQL
      </span>
      <span class="badge b-matlab">
        <svg viewBox="0 0 32 32"><rect width="32" height="32" rx="4" fill="#e87722"/><text x="6" y="22" font-size="11" font-weight="bold" fill="white" font-family="sans-serif">MAT</text></svg>
        MATLAB
      </span>
    </div>
  </div>

  <!-- Tools & Platforms -->
  <div class="tech-group">
    <div class="tech-group-label"><span class="dot dot-green"></span>Tools &amp; Platforms</div>
    <div class="badges">
      <span class="badge b-git">
        <svg viewBox="0 0 32 32" fill="white"><path d="M29.5 13.9L18.1 2.5a1.7 1.7 0 0 0-2.4 0l-2.4 2.4 3 3a2 2 0 0 1 2.5 2.6l2.9 2.9a2 2 0 1 1-1.2 1.2l-2.7-2.7v7a2 2 0 1 1-1.6 0V11.6a2 2 0 0 1-1.1-2.6L12.5 6 3.3 15.2a1.7 1.7 0 0 0 0 2.4l11.4 11.4a1.7 1.7 0 0 0 2.4 0l12.4-12.4a1.7 1.7 0 0 0 0-2.7z"/></svg>
        GIT
      </span>
      <span class="badge b-github">
        <svg viewBox="0 0 32 32" fill="white"><path d="M16 2a14 14 0 0 0-4.4 27.3c.7.1 1-.3 1-.7v-2.5c-3.9.8-4.7-1.9-4.7-1.9-.6-1.6-1.5-2-1.5-2-1.2-.8.1-.8.1-.8 1.4.1 2.1 1.4 2.1 1.4 1.2 2.1 3.2 1.5 4 1.1.1-.9.5-1.5.9-1.8-3.1-.4-6.4-1.6-6.4-7 0-1.5.5-2.8 1.4-3.8-.1-.3-.6-1.8.1-3.7 0 0 1.2-.4 3.8 1.4a13 13 0 0 1 7 0c2.6-1.8 3.8-1.4 3.8-1.4.7 1.9.3 3.4.1 3.7.9 1 1.4 2.3 1.4 3.8 0 5.4-3.3 6.6-6.4 7 .5.4 1 1.3 1 2.6v3.8c0 .4.3.8 1 .7A14 14 0 0 0 16 2z"/></svg>
        GITHUB
      </span>
      <span class="badge b-arduino">
        <svg viewBox="0 0 32 32" fill="white"><path d="M16 4C9.4 4 4 9.4 4 16s5.4 12 12 12 12-5.4 12-12S22.6 4 16 4zm-3.5 14.5H9.2v-1.4h3.3v1.4zm0-2.5H9.2v-1.4h3.3V16zm0-2.5H9.2v-1.4h3.3V13.5zm10.3 2.5h-3.3v1.4h3.3v1.4h-3.3v1.4h-1.5v-5.8h1.5V15h3.3v1z"/></svg>
        ARDUINO
      </span>
      <span class="badge b-blender">
        <svg viewBox="0 0 32 32" fill="white"><circle cx="19" cy="14" r="5"/><path d="M8 22c0-3.9 2.5-7 5.8-8H7l9-6H8l10.5-4.5C11.5 4 6 9.4 6 16c0 2.8.9 5.4 2.4 7.5L10 22H8z"/></svg>
        BLENDER
      </span>
    </div>
  </div>
</div>

<hr class="divider"/>

<!-- ══ GITHUB STATS ══ -->
<div class="stats-section">
  <div class="stats-title">
    <span class="bar-icon">📊</span> GitHub Stats
  </div>

  <div class="stats-cards">
    <div class="stat-card">
      <div class="stat-icon si-blue">⬆️</div>
      <div class="stat-info">
        <div class="stat-number">27</div>
        <div class="stat-label">Total Contributions</div>
        <div class="stat-sub">Aug 1, 2024 – Present</div>
      </div>
    </div>
    <div class="stat-card">
      <div class="stat-icon si-red">🔥</div>
      <div class="stat-info">
        <div class="stat-number">1</div>
        <div class="stat-label">Current Streak</div>
        <div class="stat-sub">Sep 5</div>
      </div>
    </div>
    <div class="stat-card">
      <div class="stat-icon si-yellow">⭐</div>
      <div class="stat-info">
        <div class="stat-number">1</div>
        <div class="stat-label">Longest Streak</div>
        <div class="stat-sub">Aug 1, 2024</div>
      </div>
    </div>
  </div>

  <div class="bottom-grid">
    <!-- Contribution Graph -->
    <div class="contrib-card">
      <div class="card-title">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="#c9d1d9"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
        Contribution Graph
      </div>
      <!-- Month labels -->
      <div class="contrib-months">
        <span class="month-label">Jan</span>
        <span class="month-label">Feb</span>
        <span class="month-label">Mar</span>
        <span class="month-label">Apr</span>
        <span class="month-label">May</span>
        <span class="month-label">Jun</span>
        <span class="month-label">Jul</span>
        <span class="month-label">Aug</span>
        <span class="month-label">Sep</span>
        <span class="month-label">Oct</span>
        <span class="month-label">Nov</span>
        <span class="month-label">Dec</span>
      </div>
      <!-- Grid -->
      <div class="contrib-grid">
        <div class="day-labels">
          <div class="day-label hidden">S</div>
          <div class="day-label">Mon</div>
          <div class="day-label hidden">T</div>
          <div class="day-label">Wed</div>
          <div class="day-label hidden">T</div>
          <div class="day-label">Fri</div>
          <div class="day-label hidden">S</div>
        </div>
        <div class="weeks" id="contribWeeks"></div>
      </div>
      <!-- Legend -->
      <div class="contrib-legend">
        <span>Less</span>
        <div class="legend-cell" style="background:#161b22;border:1px solid #444;"></div>
        <div class="legend-cell" style="background:#0e4429;"></div>
        <div class="legend-cell" style="background:#006d32;"></div>
        <div class="legend-cell" style="background:#26a641;"></div>
        <div class="legend-cell" style="background:#39d353;"></div>
        <span>More</span>
      </div>
    </div>

    <!-- Top Languages -->
    <div class="lang-card">
      <div class="card-title">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="#f778ba"><path d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm0 1c.94 0 1.85.16 2.71.45L2.45 10.71A7 7 0 0 1 1 8c0-3.86 3.14-7 7-7zm0 14c-.94 0-1.85-.16-2.71-.45l8.26-8.26A7 7 0 0 1 15 8c0 3.86-3.14 7-7 7z"/></svg>
        Top Languages
      </div>

      <div class="lang-item">
        <div class="lang-row">
          <div class="lang-name"><span class="lang-dot" style="background:var(--pink);"></span>C++</div>
          <span class="lang-pct">34.1%</span>
        </div>
        <div class="lang-bar lc-cpp" style="width:100%;"></div>
      </div>
      <div class="lang-item">
        <div class="lang-row">
          <div class="lang-name"><span class="lang-dot" style="background:var(--purple);"></span>Python</div>
          <span class="lang-pct">24.4%</span>
        </div>
        <div class="lang-bar lc-py" style="width:71.6%;"></div>
      </div>
      <div class="lang-item">
        <div class="lang-row">
          <div class="lang-name"><span class="lang-dot" style="background:#7c8cf8;"></span>Java</div>
          <span class="lang-pct">19.5%</span>
        </div>
        <div class="lang-bar lc-java" style="width:57.2%;"></div>
      </div>
      <div class="lang-item">
        <div class="lang-row">
          <div class="lang-name"><span class="lang-dot" style="background:var(--blue);"></span>HTML</div>
          <span class="lang-pct">12.2%</span>
        </div>
        <div class="lang-bar lc-html" style="width:35.8%;"></div>
      </div>
      <div class="lang-item">
        <div class="lang-row">
          <div class="lang-name"><span class="lang-dot" style="background:#56d8e4;"></span>CSS</div>
          <span class="lang-pct">9.8%</span>
        </div>
        <div class="lang-bar lc-css" style="width:28.7%;"></div>
      </div>
    </div>
  </div>
</div>

<hr class="divider"/>

<!-- ══ CONNECT ══ -->
<div class="connect-section">
  <div class="connect-title">🔗 Let's Connect</div>
  <div class="connect-sub">Feel free to reach out for collaborations, opportunities, or just a chat about tech and design!</div>
  <div class="connect-buttons">
    <a href="#" class="connect-btn cb-linkedin">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a href="#" class="connect-btn cb-instagram">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 0 0 0-12.324zM12 16a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.881 1.44 1.44 0 0 0 0-2.881z"/></svg>
      Instagram
    </a>
    <a href="#" class="connect-btn cb-github">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
      GitHub
    </a>
    <a href="#" class="connect-btn cb-gfg">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M21.45 14.315c-.143.28-.334.532-.565.745a3.691 3.691 0 0 1-1.104.695 4.51 4.51 0 0 1-2.solange.28v-.69a3.8 3.8 0 0 0 1.66-.34 2.94 2.94 0 0 0 1.116-1.102c.277-.476.441-1.032.441-1.643v-.03a3.537 3.537 0 0 0-.071-.716H21v.716c0 .75-.19 1.44-.55 2.074zM12 2C6.477 2 2 6.477 2 12s4.477 10 10 10 10-4.477 10-10S17.523 2 12 2z"/></svg>
      GeeksforGeeks
    </a>
    <a href="#" class="connect-btn cb-discord">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M20.317 4.492c-1.53-.69-3.17-1.2-4.885-1.49a.075.075 0 0 0-.079.036c-.21.369-.444.85-.608 1.23a18.566 18.566 0 0 0-5.487 0 12.36 12.36 0 0 0-.617-1.23A.077.077 0 0 0 8.562 3c-1.714.29-3.354.8-4.885 1.491a.07.07 0 0 0-.032.027C.533 9.093-.32 13.555.099 17.961a.08.08 0 0 0 .031.055 20.03 20.03 0 0 0 5.993 2.98.078.078 0 0 0 .084-.026c.462-.62.874-1.275 1.226-1.963.021-.04.001-.088-.041-.104a13.201 13.201 0 0 1-1.872-.878.075.075 0 0 1-.008-.125c.126-.093.252-.19.372-.287a.075.075 0 0 1 .078-.01c3.927 1.764 8.18 1.764 12.061 0a.075.075 0 0 1 .079.009c.12.098.245.195.372.288a.075.075 0 0 1-.006.125c-.598.344-1.22.635-1.873.877a.075.075 0 0 0-.041.105c.36.687.772 1.341 1.225 1.962a.077.077 0 0 0 .084.028 19.963 19.963 0 0 0 6.002-2.981.076.076 0 0 0 .032-.054c.5-5.094-.838-9.52-3.549-13.442a.06.06 0 0 0-.031-.028z"/></svg>
      Discord
    </a>
    <a href="#" class="connect-btn cb-email">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
      Email
    </a>
  </div>
</div>

<script>
// Generate a realistic contribution graph for ~52 weeks
(function() {
  const weeksEl = document.getElementById('contribWeeks');
  const totalWeeks = 52;
  // Sparse contributions matching the screenshot (mostly empty with a few greens and one pink)
  const specialDays = new Set([
    '3-1','4-1','4-3','18-1','18-3','18-5',
    '32-1','32-3','48-1','48-3','51-0'
  ]);
  const pinkDays = new Set(['51-0','51-1']);

  for (let w = 0; w < totalWeeks; w++) {
    const weekEl = document.createElement('div');
    weekEl.className = 'week';
    for (let d = 0; d < 7; d++) {
      const cell = document.createElement('div');
      const key = `${w}-${d}`;
      if (pinkDays.has(key)) {
        cell.className = 'cell cp';
      } else if (specialDays.has(key)) {
        const lvl = Math.floor(Math.random() * 3) + 2;
        cell.className = `cell c${lvl}`;
      } else {
        // very sparse random contributions
        const r = Math.random();
        cell.className = r < 0.04 ? 'cell c2' : r < 0.06 ? 'cell c3' : 'cell c0';
      }
      weekEl.appendChild(cell);
    }
    weeksEl.appendChild(weekEl);
  }
})();
</script>
</body>
</html>
