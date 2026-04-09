<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Arun M — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Space+Grotesk:wght@400;500;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #8b949e;
    --purple: #a855f7;
    --purple2: #7c3aed;
    --cyan: #22d3ee;
    --green: #22c55e;
    --orange: #f97316;
    --pink: #ec4899;
    --blue: #3b82f6;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Particle canvas */
  #particles { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: 0; pointer-events: none; }

  .wrapper { position: relative; z-index: 1; max-width: 900px; margin: 0 auto; padding: 2rem 1.5rem 4rem; }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 3rem 1rem 2rem;
    animation: fadeInDown 0.8s ease both;
  }
  .hero-avatar {
    width: 100px; height: 100px; border-radius: 50%;
    background: linear-gradient(135deg, var(--purple), var(--cyan));
    display: flex; align-items: center; justify-content: center;
    font-size: 2.5rem; margin: 0 auto 1.5rem;
    box-shadow: 0 0 40px #a855f740;
    animation: pulse 3s ease-in-out infinite;
  }
  @keyframes pulse { 0%,100%{box-shadow:0 0 40px #a855f740} 50%{box-shadow:0 0 70px #a855f780} }
  .hero h1 {
    font-size: 3rem; font-weight: 700; letter-spacing: -1px;
    background: linear-gradient(90deg, var(--purple), var(--cyan), var(--purple));
    background-size: 200%;
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    animation: shimmer 3s linear infinite;
  }
  @keyframes shimmer { 0%{background-position:0%} 100%{background-position:200%} }
  .hero-sub { color: var(--muted); font-size: 1.05rem; margin-top: 0.5rem; }

  /* Typing */
  .typing-wrap { margin: 1.5rem auto; font-family: 'JetBrains Mono', monospace; font-size: 1.1rem; color: var(--cyan); height: 1.6em; }
  .cursor { display: inline-block; width: 2px; height: 1.1em; background: var(--cyan); animation: blink 0.8s step-end infinite; vertical-align: text-bottom; margin-left: 2px; }
  @keyframes blink { 50%{opacity:0} }

  /* Status badges */
  .badges { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin-top: 1.5rem; }
  .badge {
    display: inline-flex; align-items: center; gap: 6px;
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 999px; padding: 5px 14px; font-size: 0.8rem; color: var(--muted);
    transition: all 0.2s;
  }
  .badge:hover { border-color: var(--purple); color: var(--text); transform: translateY(-2px); }
  .badge .dot { width: 7px; height: 7px; border-radius: 50%; }
  .dot-purple { background: var(--purple); box-shadow: 0 0 6px var(--purple); }
  .dot-cyan   { background: var(--cyan);   box-shadow: 0 0 6px var(--cyan); }
  .dot-green  { background: var(--green);  box-shadow: 0 0 6px var(--green); }

  /* Social links */
  .socials { display: flex; gap: 12px; justify-content: center; margin-top: 1.5rem; flex-wrap: wrap; }
  .social-btn {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 10px; padding: 8px 18px; color: var(--text);
    text-decoration: none; font-size: 0.85rem; font-weight: 500;
    transition: all 0.2s;
  }
  .social-btn:hover { border-color: var(--purple); background: #a855f710; transform: translateY(-2px); }
  .social-icon { width: 18px; height: 18px; }

  /* ── SECTION ── */
  .section { margin-top: 3rem; animation: fadeInUp 0.6s ease both; }
  .section-title {
    font-size: 1.3rem; font-weight: 700; margin-bottom: 1.5rem;
    display: flex; align-items: center; gap: 10px;
  }
  .section-title::after { content: ''; flex: 1; height: 1px; background: var(--border); }
  .section-title span { color: var(--purple); }

  /* ── CODE BLOCK (About Me) ── */
  .code-block {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 12px; overflow: hidden;
  }
  .code-header {
    background: var(--bg3); padding: 10px 16px;
    display: flex; align-items: center; gap: 8px; border-bottom: 1px solid var(--border);
  }
  .dot-r{width:12px;height:12px;border-radius:50%;background:#ff5f57;}
  .dot-y{width:12px;height:12px;border-radius:50%;background:#febc2e;}
  .dot-g{width:12px;height:12px;border-radius:50%;background:#28c840;}
  .code-fname { margin-left: auto; font-size: 0.75rem; color: var(--muted); font-family: 'JetBrains Mono', monospace; }
  .code-body { padding: 1.25rem 1.5rem; font-family: 'JetBrains Mono', monospace; font-size: 0.82rem; line-height: 1.9; overflow-x: auto; }
  .kw  { color: #ff79c6; }
  .cls { color: #8be9fd; }
  .fn  { color: #50fa7b; }
  .str { color: #f1fa8c; }
  .cm  { color: #6272a4; }
  .nu  { color: #bd93f9; }
  .op  { color: var(--muted); }

  /* ── SKILL PILLS ── */
  .skill-group { margin-bottom: 1.5rem; }
  .skill-label { font-size: 0.78rem; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px; }
  .pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 8px; padding: 5px 13px;
    font-size: 0.8rem; font-weight: 500;
    display: flex; align-items: center; gap: 6px;
    transition: all 0.2s; cursor: default;
  }
  .pill:hover { transform: translateY(-2px); border-color: var(--purple); background: #a855f715; }
  .p-purple { border-color: #a855f740; color: #c084fc; }
  .p-cyan   { border-color: #22d3ee40; color: #67e8f9; }
  .p-green  { border-color: #22c55e40; color: #86efac; }
  .p-orange { border-color: #f9731640; color: #fdba74; }
  .p-blue   { border-color: #3b82f640; color: #93c5fd; }
  .p-pink   { border-color: #ec489940; color: #f9a8d4; }

  /* ── PROJECTS ── */
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  @media(max-width:640px){ .projects-grid { grid-template-columns: 1fr; } }
  .project-card {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 14px; padding: 1.3rem; transition: all 0.25s;
    position: relative; overflow: hidden;
  }
  .project-card::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--purple), var(--cyan));
    transform: scaleX(0); transform-origin: left;
    transition: transform 0.3s ease;
  }
  .project-card:hover { border-color: var(--purple); transform: translateY(-4px); box-shadow: 0 8px 30px #a855f720; }
  .project-card:hover::before { transform: scaleX(1); }
  .project-title { font-size: 0.95rem; font-weight: 700; margin-bottom: 6px; display: flex; align-items: center; gap: 8px; }
  .project-emoji { font-size: 1.2rem; }
  .project-desc { font-size: 0.8rem; color: var(--muted); line-height: 1.6; margin-bottom: 12px; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 12px; }
  .tag {
    font-size: 0.7rem; padding: 2px 9px; border-radius: 999px;
    background: #a855f715; color: #c084fc; border: 1px solid #a855f730;
  }
  .tag-c  { background: #22d3ee10; color: #67e8f9; border-color: #22d3ee30; }
  .tag-g  { background: #22c55e10; color: #86efac; border-color: #22c55e30; }
  .tag-o  { background: #f9731610; color: #fdba74; border-color: #f9731630; }
  .project-stat { font-size: 0.75rem; color: var(--green); font-weight: 600; }
  .wip-badge { font-size: 0.65rem; background: #f9731620; color: #fdba74; border: 1px solid #f9731640; border-radius: 999px; padding: 2px 8px; }

  /* ── INTERNSHIP TIMELINE ── */
  .timeline { position: relative; padding-left: 28px; }
  .timeline::before { content: ''; position: absolute; left: 8px; top: 6px; bottom: 6px; width: 2px; background: linear-gradient(to bottom, var(--purple), var(--cyan)); border-radius: 2px; }
  .tl-item { position: relative; margin-bottom: 2rem; }
  .tl-dot {
    position: absolute; left: -24px; top: 4px;
    width: 14px; height: 14px; border-radius: 50%;
    background: var(--bg2); border: 2px solid var(--purple);
    box-shadow: 0 0 8px var(--purple);
  }
  .tl-company { font-size: 1rem; font-weight: 700; display: flex; align-items: center; gap: 10px; }
  .tl-meta { font-size: 0.78rem; color: var(--muted); margin: 3px 0 8px; }
  .tl-points { list-style: none; }
  .tl-points li { font-size: 0.82rem; color: var(--muted); line-height: 1.7; padding-left: 14px; position: relative; }
  .tl-points li::before { content: '▸'; position: absolute; left: 0; color: var(--purple); }

  /* ── CERTS ── */
  .certs-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 12px; }
  .cert-card {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 10px; padding: 1rem 1.1rem;
    display: flex; align-items: flex-start; gap: 12px;
    transition: all 0.2s;
  }
  .cert-card:hover { border-color: var(--cyan); transform: translateY(-2px); }
  .cert-icon { font-size: 1.4rem; flex-shrink: 0; margin-top: 2px; }
  .cert-name { font-size: 0.82rem; font-weight: 600; line-height: 1.4; }
  .cert-by   { font-size: 0.72rem; color: var(--muted); margin-top: 2px; }

  /* ── STATS ── */
  .stats-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
  @media(max-width:500px){ .stats-row { grid-template-columns: 1fr 1fr; } }
  .stat-card {
    background: var(--bg2); border: 1px solid var(--border);
    border-radius: 12px; padding: 1.2rem 1rem; text-align: center;
    transition: all 0.25s;
  }
  .stat-card:hover { border-color: var(--purple); transform: translateY(-3px); }
  .stat-number { font-size: 2rem; font-weight: 700; background: linear-gradient(135deg, var(--purple), var(--cyan)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .stat-label { font-size: 0.75rem; color: var(--muted); margin-top: 4px; }

  /* ── CONTRIBUTION BAR ── */
  .contrib-bar { background: var(--bg2); border: 1px solid var(--border); border-radius: 12px; padding: 1.5rem; }
  .contrib-grid { display: grid; grid-template-columns: repeat(52, 1fr); gap: 3px; margin-top: 1rem; }
  .contrib-cell { aspect-ratio: 1; border-radius: 2px; }
  .c0 { background: var(--bg3); }
  .c1 { background: #0d4429; }
  .c2 { background: #006d32; }
  .c3 { background: #26a641; }
  .c4 { background: #39d353; }

  /* ── LANG BARS ── */
  .lang-item { margin-bottom: 1rem; }
  .lang-row { display: flex; justify-content: space-between; font-size: 0.82rem; margin-bottom: 5px; }
  .lang-pct { color: var(--muted); }
  .lang-bar-bg { background: var(--bg3); border-radius: 999px; height: 7px; overflow: hidden; }
  .lang-bar-fill { height: 100%; border-radius: 999px; transition: width 1.2s cubic-bezier(.4,0,.2,1); }

  /* ── QUOTE ── */
  .quote-block {
    border-left: 3px solid var(--purple);
    padding: 1rem 1.5rem; margin-top: 1rem;
    background: var(--bg2); border-radius: 0 12px 12px 0;
    font-style: italic; color: var(--muted); font-size: 0.9rem; line-height: 1.7;
  }
  .quote-author { margin-top: 8px; font-style: normal; color: var(--purple); font-size: 0.8rem; font-weight: 600; }

  /* ── FOOTER ── */
  .footer { text-align: center; margin-top: 4rem; padding-top: 2rem; border-top: 1px solid var(--border); }
  .footer-wave { font-size: 2rem; animation: wave 2s ease-in-out infinite; display: inline-block; }
  @keyframes wave { 0%,100%{transform:rotate(0)} 25%{transform:rotate(20deg)} 75%{transform:rotate(-10deg)} }
  .footer p { color: var(--muted); font-size: 0.8rem; margin-top: 1rem; }

  @keyframes fadeInDown { from{opacity:0;transform:translateY(-24px)} to{opacity:1;transform:translateY(0)} }
  @keyframes fadeInUp   { from{opacity:0;transform:translateY(24px)}  to{opacity:1;transform:translateY(0)} }

  .delay1 { animation-delay: 0.1s; }
  .delay2 { animation-delay: 0.2s; }
  .delay3 { animation-delay: 0.3s; }
  .delay4 { animation-delay: 0.4s; }
  .delay5 { animation-delay: 0.5s; }
</style>
</head>
<body>

<canvas id="particles"></canvas>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-avatar">🧑‍💻</div>
    <h1>ARUN M</h1>
    <p class="hero-sub">Chennai, India 🇮🇳 &nbsp;·&nbsp; B.Tech AI & Data Science @ SJIT &nbsp;·&nbsp; CGPA 8.08</p>
    <div class="typing-wrap">
      <span id="typing"></span><span class="cursor"></span>
    </div>
    <div class="badges">
      <span class="badge"><span class="dot dot-green"></span>Open to Opportunities</span>
      <span class="badge"><span class="dot dot-purple"></span>Full Stack Developer</span>
      <span class="badge"><span class="dot dot-cyan"></span>AI / ML Engineer</span>
      <span class="badge"><span class="dot dot-green"></span>3 Internships Done</span>
    </div>
    <div class="socials">
      <a class="social-btn" href="mailto:arun.m.dev06@gmail.com">
        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Gmail
      </a>
      <a class="social-btn" href="https://linkedin.com/in/arunvijay-5a2845317" target="_blank">
        <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a class="social-btn" href="https://github.com/Arun597134" target="_blank">
        <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
        GitHub
      </a>
      <a class="social-btn" href="https://arunmportfolioin.netlify.app" target="_blank">
        <svg class="social-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Portfolio
      </a>
    </div>
  </div>

  <!-- ABOUT ME -->
  <div class="section delay1">
    <h2 class="section-title"><span>01.</span> About Me</h2>
    <div class="code-block">
      <div class="code-header">
        <span class="dot-r"></span><span class="dot-y"></span><span class="dot-g"></span>
        <span class="code-fname">arun.py</span>
      </div>
      <div class="code-body">
        <div><span class="kw">class</span> <span class="cls">ArunM</span><span class="op">:</span></div>
        <div>&nbsp;&nbsp;<span class="fn">name</span>       <span class="op">=</span> <span class="str">"Arun M"</span></div>
        <div>&nbsp;&nbsp;<span class="fn">role</span>       <span class="op">=</span> <span class="op">[</span><span class="str">"Full Stack Developer"</span><span class="op">,</span> <span class="str">"AI/ML Engineer"</span><span class="op">]</span></div>
        <div>&nbsp;&nbsp;<span class="fn">education</span>  <span class="op">=</span> <span class="str">"B.Tech – AI & Data Science, SJIT Chennai"</span></div>
        <div>&nbsp;&nbsp;<span class="fn">cgpa</span>       <span class="op">=</span> <span class="nu">8.08</span></div>
        <div>&nbsp;&nbsp;<span class="fn">year</span>       <span class="op">=</span> <span class="str">"2023 – 2027"</span></div>
        <br/>
        <div>&nbsp;&nbsp;<span class="fn">currently</span>  <span class="op">=</span> <span class="str">"Building MERN LMS Platform 🚀"</span></div>
        <div>&nbsp;&nbsp;<span class="fn">open_to</span>    <span class="op">=</span> <span class="str">"Internships, Collabs & Full-time Roles"</span></div>
        <div>&nbsp;&nbsp;<span class="fn">fun_fact</span>   <span class="op">=</span> <span class="str">"I turn ☕ into AI models & full-stack apps"</span></div>
        <br/>
        <div>&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">say_hi</span><span class="op">(</span><span class="cls">self</span><span class="op">):</span></div>
        <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">print</span><span class="op">(</span><span class="str">"Thanks for visiting! Let's build something amazing 🤝"</span><span class="op">)</span></div>
        <br/>
        <div><span class="fn">me</span> <span class="op">=</span> <span class="cls">ArunM</span><span class="op">()</span></div>
        <div><span class="fn">me</span><span class="op">.</span><span class="fn">say_hi</span><span class="op">()</span></div>
        <br/>
        <div><span class="cm"># Output: Thanks for visiting! Let's build something amazing 🤝</span></div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section delay2">
    <h2 class="section-title"><span>02.</span> Tech Stack</h2>

    <div class="skill-group">
      <div class="skill-label">🎨 Frontend</div>
      <div class="pills">
        <span class="pill p-cyan">⚛️ React.js</span>
        <span class="pill p-purple">🔄 Redux Toolkit</span>
        <span class="pill p-cyan">💨 Tailwind CSS</span>
        <span class="pill p-orange">🟧 HTML5</span>
        <span class="pill p-blue">🔵 CSS3</span>
        <span class="pill p-orange">⚡ JavaScript</span>
        <span class="pill p-orange">🧠 TensorFlow.js</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">🔧 Backend</div>
      <div class="pills">
        <span class="pill p-green">🟢 Node.js</span>
        <span class="pill p-green">🚂 Express.js</span>
        <span class="pill p-blue">🔗 RESTful APIs</span>
        <span class="pill p-purple">🧩 Microservices</span>
        <span class="pill p-pink">🔐 JWT + bcrypt</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">🗄️ Databases</div>
      <div class="pills">
        <span class="pill p-green">🍃 MongoDB</span>
        <span class="pill p-green">🔗 Mongoose</span>
        <span class="pill p-blue">🔷 SQL</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">🤖 AI / ML</div>
      <div class="pills">
        <span class="pill p-blue">🐍 Python</span>
        <span class="pill p-orange">🧠 TensorFlow</span>
        <span class="pill p-orange">🤖 scikit-learn</span>
        <span class="pill p-cyan">💬 NLP</span>
        <span class="pill p-blue">🔢 NumPy</span>
        <span class="pill p-purple">🐼 Pandas</span>
        <span class="pill p-green">🔧 Feature Engineering</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">☁️ DevOps & Cloud</div>
      <div class="pills">
        <span class="pill p-orange">📦 Git & CI/CD</span>
        <span class="pill p-pink">☁️ Oracle Cloud</span>
        <span class="pill p-blue">▲ Vercel</span>
        <span class="pill p-cyan">🖼️ Cloudinary</span>
        <span class="pill p-green">🚀 Render</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-label">💻 Languages</div>
      <div class="pills">
        <span class="pill p-blue">🐍 Python</span>
        <span class="pill p-orange">☕ Java</span>
        <span class="pill p-orange">⚡ JavaScript</span>
        <span class="pill p-blue">🔷 SQL</span>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section delay3">
    <h2 class="section-title"><span>03.</span> Featured Projects</h2>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-title"><span class="project-emoji">🤖</span> HireWise AI</div>
        <div class="project-desc">AI interview simulation generating 20+ tailored questions per session using NLP-based resume parsing and keyword extraction.</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">NLP</span>
          <span class="tag">scikit-learn</span>
          <span class="tag">Tkinter</span>
        </div>
        <div class="project-stat">↑ 40% question relevance boost</div>
      </div>

      <div class="project-card">
        <div class="project-title"><span class="project-emoji">📝</span> AI Assessment Platform</div>
        <div class="project-desc">Full-stack exam platform with webcam-based proctoring, real-time integrity scores, anti-cheating mechanisms, and analytics dashboard.</div>
        <div class="project-tags">
          <span class="tag tag-c">React.js</span>
          <span class="tag tag-g">Node.js</span>
          <span class="tag tag-g">MongoDB</span>
          <span class="tag tag-o">TensorFlow.js</span>
        </div>
        <div class="project-stat">Real-time face + tab-switch detection</div>
      </div>

      <div class="project-card">
        <div class="project-title">
          <span class="project-emoji">🎓</span> MERN LMS
          <span class="wip-badge">In Dev</span>
        </div>
        <div class="project-desc">Feature-rich Learning Management System with role-based access, JWT auth, video course management, progress tracking & AI-powered ML services.</div>
        <div class="project-tags">
          <span class="tag tag-c">React</span>
          <span class="tag tag-c">Redux</span>
          <span class="tag tag-g">Node.js</span>
          <span class="tag tag-g">MongoDB</span>
          <span class="tag">Cloudinary</span>
        </div>
        <div class="project-stat">Student / Instructor / Admin roles</div>
      </div>

      <div class="project-card">
        <div class="project-title"><span class="project-emoji">🌐</span> Responsive Web Pages</div>
        <div class="project-desc">3+ responsive web pages built during Codtech internship with RESTful API integration and structured Git branching workflows.</div>
        <div class="project-tags">
          <span class="tag tag-o">HTML5</span>
          <span class="tag tag-o">CSS3</span>
          <span class="tag tag-o">JavaScript</span>
          <span class="tag tag-g">Node.js</span>
        </div>
        <div class="project-stat">REST API frontend-backend integration</div>
      </div>

    </div>
  </div>

  <!-- INTERNSHIPS -->
  <div class="section delay3">
    <h2 class="section-title"><span>04.</span> Internship Experience</h2>
    <div class="timeline">

      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-company">🏢 Codtech IT Solutions</div>
        <div class="tl-meta">Web Development Intern &nbsp;·&nbsp; 2024 – 2025</div>
        <ul class="tl-points">
          <li>Built 3+ responsive web pages using HTML5, CSS3, JavaScript, and Node.js</li>
          <li>Integrated RESTful API endpoints to connect frontend and backend</li>
          <li>Maintained structured Git branching and commit workflows</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-company">🏢 Prodigy Infotech</div>
        <div class="tl-meta">Software Development Intern &nbsp;·&nbsp; July – August 2025</div>
        <ul class="tl-points">
          <li>Architected scalable UI modules using component-based design patterns</li>
          <li>Resolved 10+ issues through systematic debugging and code reviews</li>
          <li>Deployed feature updates via CI/CD pipelines with Git version control</li>
        </ul>
      </div>

      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-company">🏢 Codsoft IT Solutions</div>
        <div class="tl-meta">Java Programming Intern &nbsp;·&nbsp; January – February 2025</div>
        <ul class="tl-points">
          <li>Constructed 5+ Java programs applying OOP and Data Structures</li>
          <li>Refactored code into reusable modules for better maintainability</li>
        </ul>
      </div>

    </div>
  </div>

  <!-- STATS -->
  <div class="section delay4">
    <h2 class="section-title"><span>05.</span> At a Glance</h2>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-number" id="cnt-projects">0</div>
        <div class="stat-label">Real-world Projects</div>
      </div>
      <div class="stat-card">
        <div class="stat-number" id="cnt-internships">0</div>
        <div class="stat-label">Internships Completed</div>
      </div>
      <div class="stat-card">
        <div class="stat-number" id="cnt-certs">0</div>
        <div class="stat-label">Certifications Earned</div>
      </div>
    </div>
  </div>

  <!-- CONTRIBUTION HEATMAP -->
  <div class="section delay4">
    <h2 class="section-title"><span>06.</span> Contribution Activity</h2>
    <div class="contrib-bar">
      <div style="font-size:0.8rem;color:var(--muted)">GitHub-style contribution graph (simulated)</div>
      <div class="contrib-grid" id="contrib-grid"></div>
      <div style="display:flex;align-items:center;gap:6px;margin-top:10px;font-size:0.72rem;color:var(--muted)">
        Less
        <span style="width:11px;height:11px;border-radius:2px;background:var(--bg3);display:inline-block"></span>
        <span style="width:11px;height:11px;border-radius:2px;background:#0d4429;display:inline-block"></span>
        <span style="width:11px;height:11px;border-radius:2px;background:#006d32;display:inline-block"></span>
        <span style="width:11px;height:11px;border-radius:2px;background:#26a641;display:inline-block"></span>
        <span style="width:11px;height:11px;border-radius:2px;background:#39d353;display:inline-block"></span>
        More
      </div>
    </div>
  </div>

  <!-- LANGUAGES -->
  <div class="section delay4">
    <h2 class="section-title"><span>07.</span> Languages Used</h2>
    <div id="lang-bars"></div>
  </div>

  <!-- CERTS -->
  <div class="section delay5">
    <h2 class="section-title"><span>08.</span> Certifications</h2>
    <div class="certs-grid">
      <div class="cert-card">
        <div class="cert-icon">🟠</div>
        <div><div class="cert-name">Front End Web Developer</div><div class="cert-by">Infosys Springboard · 2025</div></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🍃</div>
        <div><div class="cert-name">Basics of MongoDB</div><div class="cert-by">MongoDB University · 2025</div></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🔴</div>
        <div><div class="cert-name">OCI AI Foundations</div><div class="cert-by">Oracle University · 2025</div></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🔵</div>
        <div><div class="cert-name">Intro to Large Language Models</div><div class="cert-by">Google Cloud · 2025</div></div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🔵</div>
        <div><div class="cert-name">Intro to Generative AI</div><div class="cert-by">Google Cloud · 2025</div></div>
      </div>
    </div>
  </div>

  <!-- QUOTE -->
  <div class="section delay5">
    <h2 class="section-title"><span>09.</span> Dev Wisdom</h2>
    <div class="quote-block" id="quote-text">
      "The best code is no code at all. Every new line of code you willingly bring into the world is code that has to be debugged, code that has to be read and understood, code that has to be supported."
      <div class="quote-author">— Jeff Atwood</div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span class="footer-wave">👋</span>
    <p>Thanks for visiting! Feel free to reach out — let's build something awesome together.</p>
    <p style="margin-top:8px">📧 arun.m.dev06@gmail.com &nbsp;·&nbsp; 📱 +91 88255 21904</p>
    <p style="margin-top:16px;font-size:0.7rem;color:#444">Made with ❤️ by Arun M</p>
  </div>

</div>

<script>
/* ── PARTICLES ── */
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');
let W, H, pts = [];
function resize(){ W = canvas.width = window.innerWidth; H = canvas.height = window.innerHeight; }
resize();
window.addEventListener('resize', resize);
for(let i=0;i<80;i++) pts.push({ x:Math.random()*window.innerWidth, y:Math.random()*window.innerHeight, vx:(Math.random()-.5)*.3, vy:(Math.random()-.5)*.3, r:Math.random()*1.5+.5 });
function drawParticles(){
  ctx.clearRect(0,0,W,H);
  pts.forEach(p=>{ p.x+=p.vx; p.y+=p.vy; if(p.x<0||p.x>W) p.vx*=-1; if(p.y<0||p.y>H) p.vy*=-1; ctx.beginPath(); ctx.arc(p.x,p.y,p.r,0,Math.PI*2); ctx.fillStyle='rgba(168,85,247,0.35)'; ctx.fill(); });
  for(let i=0;i<pts.length;i++) for(let j=i+1;j<pts.length;j++){
    const d=Math.hypot(pts[i].x-pts[j].x,pts[i].y-pts[j].y);
    if(d<120){ ctx.beginPath(); ctx.moveTo(pts[i].x,pts[i].y); ctx.lineTo(pts[j].x,pts[j].y); ctx.strokeStyle=`rgba(168,85,247,${(1-d/120)*.15})`; ctx.stroke(); }
  }
  requestAnimationFrame(drawParticles);
}
drawParticles();

/* ── TYPING ── */
const lines = [
  'Building scalable full-stack apps 🚀',
  'Crafting intelligent AI/ML models 🤖',
  'Turning data into decisions 📊',
  'Open to amazing opportunities ✨',
  'React · Node · MongoDB · Python 💻',
];
let li=0, ci=0, del=false, el=document.getElementById('typing');
function type(){
  if(!del){ el.textContent=lines[li].slice(0,++ci); if(ci===lines[li].length){ del=true; setTimeout(type,1800); return; } }
  else { el.textContent=lines[li].slice(0,--ci); if(ci===0){ del=false; li=(li+1)%lines.length; } }
  setTimeout(type, del?40:60);
}
type();

/* ── COUNTER ANIMATION ── */
function animCount(id, target){
  let v=0; const step=Math.ceil(target/40);
  const t=setInterval(()=>{ v=Math.min(v+step,target); document.getElementById(id).textContent=v+'+'; if(v>=target) clearInterval(t); },40);
}
const observer=new IntersectionObserver(entries=>{ entries.forEach(e=>{ if(e.isIntersecting){ animCount('cnt-projects',3); animCount('cnt-internships',3); animCount('cnt-certs',5); observer.disconnect(); } }); },{threshold:.5});
observer.observe(document.getElementById('cnt-projects'));

/* ── CONTRIBUTION HEATMAP ── */
const grid=document.getElementById('contrib-grid');
const weights=[0,0,0,0,1,1,2,2,3,4];
for(let i=0;i<52*7;i++){
  const w=weights[Math.floor(Math.random()*weights.length)];
  const d=document.createElement('div');
  d.className='contrib-cell c'+w; grid.appendChild(d);
}

/* ── LANGUAGE BARS ── */
const langs=[
  {name:'JavaScript',pct:38,color:'#f7df1e'},
  {name:'Python',pct:28,color:'#3776ab'},
  {name:'Java',pct:15,color:'#f89820'},
  {name:'HTML/CSS',pct:12,color:'#e34f26'},
  {name:'SQL',pct:7,color:'#4479a1'},
];
const lb=document.getElementById('lang-bars');
langs.forEach(l=>{
  lb.innerHTML+=`<div class="lang-item">
    <div class="lang-row"><span>${l.name}</span><span class="lang-pct">${l.pct}%</span></div>
    <div class="lang-bar-bg"><div class="lang-bar-fill" style="width:0%;background:${l.color}" data-w="${l.pct}"></div></div>
  </div>`;
});
setTimeout(()=>{ document.querySelectorAll('.lang-bar-fill').forEach(b=>{ b.style.width=b.dataset.w+'%'; }); },300);

/* ── SCROLL FADE IN ── */
const sections=document.querySelectorAll('.section');
const sObs=new IntersectionObserver(entries=>{ entries.forEach(e=>{ if(e.isIntersecting){ e.target.style.opacity='1'; e.target.style.transform='translateY(0)'; } }); },{threshold:.1});
sections.forEach(s=>{ s.style.opacity='0'; s.style.transform='translateY(30px)'; s.style.transition='opacity .6s ease, transform .6s ease'; sObs.observe(s); });
</script>
</body>
</html>
