<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Elias Jokar | Applied Mathematician focused on applied AI, Founder</title>
  <meta name="description" content="Personal website of Elias Jokar — applied mathematicianfocused on applied AI, and founder, sharing ideas, work, and a link to EntiAI." />
  <style>
    :root {
      --bg: #07111f;
      --bg-soft: #0d1b2a;
      --card: rgba(255,255,255,0.06);
      --line: rgba(255,255,255,0.12);
      --text: #f8fafc;
      --muted: #cbd5e1;
      --accent: #38bdf8;
      --accent-2: #8b5cf6;
      --shadow: 0 20px 50px rgba(0,0,0,0.28);
      --radius: 24px;
      --max: 1120px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at top left, rgba(56,189,248,0.18), transparent 28%),
        radial-gradient(circle at 85% 10%, rgba(139,92,246,0.18), transparent 25%),
        linear-gradient(180deg, #06101d 0%, #081321 40%, #0b1726 100%);
      color: var(--text);
      line-height: 1.6;
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    .container {
      width: min(calc(100% - 32px), var(--max));
      margin: 0 auto;
    }

    .nav {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(14px);
      background: rgba(7,17,31,0.72);
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }

    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 16px 0;
      gap: 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 700;
      letter-spacing: 0.2px;
    }

    .brand-mark {
      width: 40px;
      height: 40px;
      border-radius: 14px;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      box-shadow: var(--shadow);
    }

    .nav-links {
      display: flex;
      gap: 20px;
      color: var(--muted);
      font-size: 0.96rem;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .nav-links a:hover { color: var(--text); }

    .hero {
      padding: 86px 0 56px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 28px;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 10px 14px;
      border: 1px solid rgba(56,189,248,0.18);
      border-radius: 999px;
      background: rgba(56,189,248,0.08);
      color: #bae6fd;
      font-size: 0.92rem;
      margin-bottom: 18px;
    }

    h1 {
      margin: 0;
      font-size: clamp(2.6rem, 6vw, 5rem);
      line-height: 0.98;
      letter-spacing: -0.04em;
    }

    .gradient {
      background: linear-gradient(90deg, #7dd3fc, #60a5fa, #a78bfa);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .lead {
      margin: 22px 0 0;
      max-width: 680px;
      font-size: 1.12rem;
      color: var(--muted);
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-top: 30px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 14px 20px;
      border-radius: 16px;
      font-weight: 600;
      transition: transform 0.2s ease, opacity 0.2s ease, background 0.2s ease;
      border: 1px solid transparent;
    }

    .btn:hover { transform: translateY(-1px); }
    .btn-primary {
      background: #ffffff;
      color: #0b1726;
    }
    .btn-secondary {
      background: rgba(255,255,255,0.06);
      border-color: rgba(255,255,255,0.14);
      color: var(--text);
    }

    .hero-card, .card {
      background: var(--card);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      backdrop-filter: blur(12px);
    }

    .hero-card {
      padding: 24px;
    }

    .profile-top {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-bottom: 18px;
    }

    .avatar {
      width: 74px;
      height: 74px;
      border-radius: 22px;
      background: linear-gradient(135deg, rgba(56,189,248,0.35), rgba(139,92,246,0.35));
      display: grid;
      place-items: center;
      font-size: 1.4rem;
      font-weight: 700;
      color: white;
      border: 1px solid rgba(255,255,255,0.14);
    }

    .role {
      color: var(--muted);
      font-size: 0.96rem;
    }

    .mini-list {
      display: grid;
      gap: 12px;
      margin-top: 18px;
    }

    .mini-item {
      padding: 14px 16px;
      border-radius: 18px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
      color: var(--muted);
    }

    section {
      padding: 26px 0;
    }

    .section-title {
      margin: 0 0 18px;
      font-size: clamp(1.7rem, 3vw, 2.4rem);
      letter-spacing: -0.03em;
    }

    .section-copy {
      color: var(--muted);
      max-width: 760px;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 22px;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .card {
      padding: 24px;
    }

    .card h3 {
      margin: 0 0 10px;
      font-size: 1.15rem;
    }

    .card p {
      margin: 0;
      color: var(--muted);
    }

    .tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 18px;
    }

    .tag {
      padding: 9px 12px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.12);
      background: rgba(255,255,255,0.04);
      color: #e2e8f0;
      font-size: 0.92rem;
    }

    .timeline {
      display: grid;
      gap: 16px;
      margin-top: 20px;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: 110px 1fr;
      gap: 18px;
      padding: 18px;
      border-radius: 20px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
    }

    .timeline-item .year {
      color: #7dd3fc;
      font-weight: 700;
    }

    .quote {
      font-size: 1.08rem;
      color: #e2e8f0;
    }

    .footer {
      padding: 28px 0 46px;
      color: var(--muted);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
      border-top: 1px solid rgba(255,255,255,0.08);
      padding-top: 24px;
    }

    @media (max-width: 920px) {
      .hero-grid,
      .grid-2,
      .grid-3 {
        grid-template-columns: 1fr;
      }

      .timeline-item {
        grid-template-columns: 1fr;
        gap: 8px;
      }
    }

    @media (max-width: 640px) {
      .nav-inner {
        align-items: flex-start;
        flex-direction: column;
      }

      .hero {
        padding-top: 54px;
      }

      .hero-card,
      .card {
        padding: 20px;
      }
    }
  </style>
</head>
<body>
  <nav class="nav">
    <div class="container nav-inner">
      <a href="#top" class="brand">
        <span class="brand-mark"></span>
        <span>Elias Jokar</span>
      </a>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#mathematics">Mathematics</a>
        <a href="#work">Work</a>
        <a href="#journey">Journey</a>
        <a href="#connect">Connect</a>
      </div>
    </div>
  </nav>

  <header class="hero" id="top">
    <div class="container hero-grid">
      <div>
        <div class="eyebrow">Personal website • Mathematics, AI, and building</div>
        <h1>
          Hi, I'm <span class="gradient">Elias Jokar</span>.
          <br />
          I work at the intersection of <span class="gradient">mathematics, AI, and digital innovation</span>.
        </h1>
        <p class="lead">
          This is my personal space on the web — a place to share who I am, what I work on, and how my background in mathematics shapes my approach to AI, problem-solving, and building meaningful digital experiences. For my company and business-facing work, visit <strong>EntiAI</strong>.
        </p>
        <div class="cta-row">
          <a class="btn btn-primary" href="https://entiai.com" target="_blank" rel="noopener noreferrer">Visit EntiAI</a>
          <a class="btn btn-secondary" href="#about">Learn more about me</a>
        </div>
      </div>

      <aside class="hero-card">
        <div class="profile-top">
          <div class="avatar">YN</div>
          <div>
            <h2 style="margin:0; font-size:1.3rem;">Your Name</h2>
            <div class="role">Mathematician / Founder / AI Builder</div>
          </div>
        </div>
        <p style="margin:0; color:var(--muted);">
          I’m interested in how mathematical thinking can shape useful, human-centered AI — combining abstraction, structure, and practical value.
        </p>
        <div class="mini-list">
          <div class="mini-item">Grounded in mathematics, logic, and analytical thinking</div>
          <div class="mini-item">Focused on AI products, workflows, and digital identity</div>
          <div class="mini-item">Building public-facing work through <strong>entiai.com</strong></div>
        </div>
      </aside>
    </div>
  </header>

  <main>
    <section id="about">
      <div class="container grid-2">
        <div class="card">
          <h2 class="section-title">About me</h2>
          <p class="section-copy">
            I’m a mathematician with a strong interest in artificial intelligence, technology, and the transformation of ideas into practical systems. Mathematics has shaped the way I think — with clarity, structure, abstraction, and rigor — and that mindset continues to influence how I approach AI, product development, and digital strategy.
          </p>
          <div class="tag-row">
            <span class="tag">Mathematics</span>
            <span class="tag">AI</span>
            <span class="tag">Analytical thinking</span>
            <span class="tag">Product thinking</span>
            <span class="tag">Digital strategy</span>
          </div>
        </div>

        <div class="card">
          <h2 class="section-title">What this site is for</h2>
          <p class="section-copy">
            This personal site introduces the person behind the work. It gives context to my background, values, intellectual interests, and direction. It complements my professional website rather than replacing it.
          </p>
          <p class="section-copy" style="margin-top:14px;">
            <strong>Personal website:</strong> who I am, how I think, what I’m learning.<br />
            <strong>EntiAI:</strong> my professional work, business direction, and public offering.
          </p>
        </div>
      </div>
    </section>

    <section id="mathematics">
      <div class="container grid-2">
        <div class="card">
          <h2 class="section-title">Mathematics and my mindset</h2>
          <p class="section-copy">
            Mathematics is not only part of my background — it is part of how I think. It influences how I work with abstraction, how I break down difficult problems, and how I look for elegant and reliable solutions.
          </p>
        </div>

        <div class="card">
          <h2 class="section-title">Why it matters in AI</h2>
          <p class="section-copy">
            My interest in AI is closely connected to my interest in mathematics. Both involve patterns, structure, logic, and the challenge of turning complexity into insight. This connection shapes the way I approach innovation and problem-solving.
          </p>
        </div>
      </div>
    </section>

    <section id="work">
      <div class="container">
        <h2 class="section-title">What I work on</h2>
        <p class="section-copy">
          My work is centered on mathematical clarity, thoughtful digital experiences, and exploring how AI can support real people, teams, and businesses.
        </p>
        <div class="grid-3" style="margin-top:22px;">
          <div class="card">
            <h3>Mathematical thinking in practice</h3>
            <p>I use mathematical reasoning to approach complexity, structure ideas, and solve problems with clarity and precision.</p>
          </div>
          <div class="card">
            <h3>AI ideas into real products</h3>
            <p>I explore how concepts from mathematics and AI can become useful tools, workflows, websites, and product directions.</p>
          </div>
          <div class="card">
            <h3>Clear and rigorous communication</h3>
            <p>I care about making advanced ideas understandable, approachable, and connected to real outcomes for people and businesses.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="journey">
      <div class="container grid-2">
        <div class="card">
          <h2 class="section-title">My journey</h2>
          <div class="timeline">
            <div class="timeline-item">
              <div class="year">Beginning</div>
              <div>
                <h3 style="margin:0 0 8px;">A foundation in mathematics</h3>
                <p>My early interest in mathematics shaped the way I approach ideas — through logic, abstraction, structure, and disciplined problem-solving.</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">Development</div>
              <div>
                <h3 style="margin:0 0 8px;">From theory to application</h3>
                <p>Over time, I became increasingly interested in how mathematical and analytical thinking could be applied to technology, AI, and digital products.</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">Today</div>
              <div>
                <h3 style="margin:0 0 8px;">Building with AI and mathematical clarity</h3>
                <p>I’m building a stronger professional presence through EntiAI while keeping this site as a more personal introduction to my academic mindset, values, and direction.</p>
              </div>
            </div>
          </div>
        </div>

        <div class="card">
          <h2 class="section-title">What matters to me</h2>
          <p class="quote">
            “Mathematics teaches clarity; technology gives that clarity a way to create impact.”
          </p>
          <p class="section-copy" style="margin-top:18px;">
            I value clarity, curiosity, thoughtful ambition, and building things that connect ideas with action. I’m especially interested in work where innovation still feels human and intellectually grounded.
          </p>
          <div class="tag-row">
            <span class="tag">Curiosity</span>
            <span class="tag">Clarity</span>
            <span class="tag">Logic</span>
            <span class="tag">Usefulness</span>
          </div>
        </div>
      </div>
    </section>

    <section id="connect">
      <div class="container">
        <div class="card">
          <h2 class="section-title">Let’s connect</h2>
          <p class="section-copy">
            This site is the personal side of my online presence. If you want to learn more about my professional work, collaborations, or projects, visit EntiAI.
          </p>
          <div class="cta-row">
            <a class="btn btn-primary" href="https://entiai.com" target="_blank" rel="noopener noreferrer">Go to EntiAI</a>
            <a class="btn btn-secondary" href="mailto:your@email.com">Email me</a>
            <a class="btn btn-secondary" href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container footer-inner">
      <div>© 2026 Elias Jokar</div>
      <div>Personal website • Connected to <a href="https://entiai.com" target="_blank" rel="noopener noreferrer"><strong>entiai.com</strong></a></div>
    </div>
  </footer>
</body>
</html>
