<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>Elias Jokar | Applied Mathematician & AI</title>
  <meta
    name="description"
    content="Personal website of Elias Jokar — applied mathematician focused on applied AI, problem-solving, and digital innovation."
  />

  <style>
    :root {
      --bg: #07111f;
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

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system,
        BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at top left, rgba(56,189,248,0.18), transparent 28%),
        radial-gradient(circle at 85% 10%, rgba(139,92,246,0.18), transparent 25%),
        linear-gradient(180deg, #06101d 0%, #081321 45%, #0b1726 100%);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(calc(100% - 32px), var(--max));
      margin: 0 auto;
    }

    /* Navigation */
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
      gap: 20px;
      padding: 14px 0;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 700;
    }

    .brand-mark {
      width: 38px;
      height: 38px;
      border-radius: 13px;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      box-shadow: var(--shadow);
    }

    .nav-links {
      display: flex;
      gap: 22px;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .nav-links a:hover {
      color: var(--text);
    }

    /* Hero */
    .hero {
      padding: 72px 0 44px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.25fr 0.75fr;
      gap: 28px;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      padding: 9px 13px;
      margin-bottom: 17px;
      border-radius: 999px;
      border: 1px solid rgba(56,189,248,0.18);
      background: rgba(56,189,248,0.08);
      color: #bae6fd;
      font-size: 0.9rem;
    }

    h1 {
      margin: 0;
      font-size: clamp(2.5rem, 5.7vw, 4.8rem);
      line-height: 1;
      letter-spacing: -0.04em;
    }

    .gradient {
      background: linear-gradient(90deg, #7dd3fc, #60a5fa, #a78bfa);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .lead {
      max-width: 700px;
      margin: 22px 0 0;
      color: var(--muted);
      font-size: 1.08rem;
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 26px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 13px 18px;
      border-radius: 15px;
      border: 1px solid transparent;
      font-weight: 600;
      transition: transform 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-1px);
    }

    .btn-primary {
      background: #fff;
      color: #0b1726;
    }

    .btn-secondary {
      background: rgba(255,255,255,0.06);
      border-color: rgba(255,255,255,0.14);
    }

    /* Cards */
    .card {
      padding: 24px;
      border-radius: var(--radius);
      background: var(--card);
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
      backdrop-filter: blur(12px);
    }

    .profile-title {
      margin: 0;
      font-size: 1.45rem;
    }

    .role {
      margin-top: 4px;
      color: var(--muted);
      font-size: 0.96rem;
    }

    .profile-copy {
      margin: 18px 0 0;
      color: var(--muted);
    }

    .mini-list {
      display: grid;
      gap: 10px;
      margin-top: 18px;
    }

    .mini-item {
      padding: 12px 14px;
      border-radius: 15px;
      border: 1px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.04);
      color: var(--muted);
      font-size: 0.95rem;
    }

    /* Main */
    section {
      padding: 22px 0;
    }

    .section-title {
      margin: 0 0 14px;
      font-size: clamp(1.6rem, 3vw, 2.25rem);
      letter-spacing: -0.03em;
    }

    .section-copy {
      margin: 0;
      color: var(--muted);
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 22px;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
      margin-top: 18px;
    }

    .focus-card h3 {
      margin: 0 0 8px;
      font-size: 1.08rem;
    }

    .focus-card p {
      margin: 0;
      color: var(--muted);
      font-size: 0.96rem;
    }

    .tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 18px;
    }

    .tag {
      padding: 8px 11px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.12);
      background: rgba(255,255,255,0.04);
      color: #e2e8f0;
      font-size: 0.88rem;
    }

    .quote {
      margin: 0;
      font-size: 1.1rem;
      color: #e2e8f0;
    }

    /* Footer */
    .footer {
      padding: 24px 0 34px;
      color: var(--muted);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
      padding-top: 20px;
      border-top: 1px solid rgba(255,255,255,0.08);
      font-size: 0.93rem;
    }

    @media (max-width: 900px) {
      .hero-grid,
      .grid-2,
      .grid-3 {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 640px) {
      .nav-inner {
        align-items: flex-start;
        flex-direction: column;
      }

      .nav-links {
        gap: 15px;
        flex-wrap: wrap;
      }

      .hero {
        padding-top: 48px;
      }

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
        <a href="#focus">Focus</a>
        <a href="#connect">Connect</a>
      </div>
    </div>
  </nav>

  <header class="hero" id="top">
    <div class="container hero-grid">

      <div>
        <div class="eyebrow">Applied Mathematics • AI • Innovation</div>

        <h1>
          Hi, I'm <span class="gradient">Elias Jokar</span>.
          <br />
          I connect <span class="gradient">mathematics with applied AI</span>.
        </h1>

        <p class="lead">
          I’m an applied mathematician focused on turning analytical thinking,
          AI, and complex ideas into practical solutions. My work combines
          mathematical clarity, technology, and real-world problem-solving.
        </p>

        <div class="cta-row">
          <a
            class="btn btn-primary"
            href="https://entiai.com"
            target="_blank"
            rel="noopener noreferrer"
          >
            Visit EntiAI
          </a>

          <a class="btn btn-secondary" href="#about">
            About me
          </a>
        </div>
      </div>

      <aside class="card">
        <h2 class="profile-title">Elias Jokar</h2>
        <div class="role">Applied Mathematician • AI • Founder</div>

        <p class="profile-copy">
          Mathematics shapes how I think: structure, abstraction, logic,
          and precision. AI gives me a way to turn that thinking into
          useful systems and products.
        </p>

        <div class="mini-list">
          <div class="mini-item">Applied mathematics & analytical problem-solving</div>
          <div class="mini-item">Artificial intelligence & intelligent systems</div>
          <div class="mini-item">Professional work through <strong>entiai.com</strong></div>
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
            My background in mathematics has shaped the way I approach
            difficult problems: understand the structure, reduce complexity,
            and search for clear and reliable solutions.
          </p>

          <p class="section-copy" style="margin-top:14px;">
            Today, I apply this mindset to artificial intelligence,
            technology, digital products, and innovation.
          </p>

          <div class="tag-row">
            <span class="tag">Applied Mathematics</span>
            <span class="tag">Artificial Intelligence</span>
            <span class="tag">Problem Solving</span>
            <span class="tag">Innovation</span>
          </div>
        </div>

        <div class="card">
          <h2 class="section-title">How I think</h2>

          <p class="quote">
            “Mathematics brings clarity to complexity.
            AI turns that clarity into practical impact.”
          </p>

          <p class="section-copy" style="margin-top:18px;">
            I’m especially interested in the point where mathematical
            reasoning, data, technology, and human needs come together.
            That intersection is where I believe AI becomes genuinely useful.
          </p>
        </div>

      </div>
    </section>

    <section id="focus">
      <div class="container">

        <h2 class="section-title">What I focus on</h2>

        <div class="grid-3">

          <div class="card focus-card">
            <h3>Mathematics</h3>
            <p>
              Using abstraction, structure, modelling, and analytical reasoning
              to understand difficult problems.
            </p>
          </div>

          <div class="card focus-card">
            <h3>Applied AI</h3>
            <p>
              Turning AI and machine-learning ideas into practical systems,
              workflows, and intelligent applications.
            </p>
          </div>

          <div class="card focus-card">
            <h3>From ideas to impact</h3>
            <p>
              Connecting technical thinking with useful outcomes for people,
              products, and organizations.
            </p>
          </div>

        </div>
      </div>
    </section>

    <section id="connect">
      <div class="container">

        <div class="card">
          <h2 class="section-title">Let’s connect</h2>

          <p class="section-copy">
            This is the personal side of my online presence.
            For professional projects, collaborations, and my work in AI,
            visit EntiAI.
          </p>

          <div class="cta-row">
            <a
              class="btn btn-primary"
              href="https://entiai.com"
              target="_blank"
              rel="noopener noreferrer"
            >
              Go to EntiAI
            </a>

            <a class="btn btn-secondary" href="mailto:your@email.com">
              Email me
            </a>

            <a
              class="btn btn-secondary"
              href="https://www.linkedin.com/"
              target="_blank"
              rel="noopener noreferrer"
            >
              LinkedIn
            </a>
          </div>
        </div>

      </div>
    </section>

  </main>

  <footer class="footer">
    <div class="container footer-inner">
      <div>© 2026 Elias Jokar</div>

      <div>
        Applied Mathematics • AI •
        <a
          href="https://entiai.com"
          target="_blank"
          rel="noopener noreferrer"
        >
          <strong>EntiAI</strong>
        </a>
      </div>
    </div>
  </footer>

</body>
</html>
