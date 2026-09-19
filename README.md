<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Fernando G. T. | Portfolio</title>
    <style>
      :root {
        --bg: #07111f;
        --bg-soft: #0f1b2d;
        --panel: rgba(15, 23, 42, 0.82);
        --panel-strong: #111827;
        --line: rgba(148, 163, 184, 0.18);
        --text: #e5eefb;
        --muted: #9fb0c7;
        --primary: #38bdf8;
        --primary-2: #8b5cf6;
        --accent: #22c55e;
        --warning: #f59e0b;
        --shadow: 0 25px 55px rgba(15, 23, 42, 0.45);
      }

      * { box-sizing: border-box; }

      html {
        scroll-behavior: smooth;
      }

      body {
        margin: 0;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        background:
          radial-gradient(circle at top left, rgba(56, 189, 248, 0.18), transparent 30%),
          radial-gradient(circle at bottom right, rgba(139, 92, 246, 0.16), transparent 30%),
          var(--bg);
        color: var(--text);
        line-height: 1.7;
      }

      a {
        color: inherit;
        text-decoration: none;
      }

      .container {
        max-width: 1120px;
        margin: 0 auto;
        padding: 32px 20px 80px;
      }

      .hero {
        padding: 32px 0 18px;
      }

      .hero-shell {
        position: relative;
        background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(10, 16, 28, 0.92));
        border: 1px solid var(--line);
        border-radius: 28px;
        box-shadow: var(--shadow);
        overflow: hidden;
      }

      .hero-shell::before {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(120deg, transparent, rgba(56, 189, 248, 0.08), transparent);
        pointer-events: none;
      }

      .hero-content {
        position: relative;
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        gap: 24px;
        align-items: center;
        padding: 36px;
      }

      .eyebrow {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        background: rgba(56, 189, 248, 0.08);
        border: 1px solid rgba(56, 189, 248, 0.2);
        color: var(--primary);
        border-radius: 999px;
        padding: 8px 14px;
        font-size: 12px;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        font-weight: 700;
      }

      h1 {
        font-size: clamp(2.2rem, 4vw, 4.2rem);
        line-height: 1.05;
        margin: 16px 0 12px;
        letter-spacing: -0.04em;
      }

      .highlight {
        background: linear-gradient(135deg, var(--primary), var(--primary-2));
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
      }

      .subtitle {
        color: var(--muted);
        font-size: 1.05rem;
        max-width: 640px;
        margin: 0 0 22px;
      }

      .cta-row {
        display: flex;
        flex-wrap: wrap;
        gap: 14px;
        margin-bottom: 20px;
      }

      .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        border-radius: 12px;
        padding: 12px 18px;
        font-weight: 700;
        transition: transform 0.2s ease, opacity 0.2s ease;
      }

      .btn:hover {
        transform: translateY(-1px);
      }

      .btn-primary {
        background: linear-gradient(135deg, var(--primary), var(--primary-2));
        color: white;
        box-shadow: 0 10px 22px rgba(59, 130, 246, 0.3);
      }

      .btn-secondary {
        border: 1px solid var(--line);
        background: rgba(148, 163, 184, 0.04);
        color: var(--text);
      }

      .socials {
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
      }

      .socials a {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 42px;
        height: 42px;
        border-radius: 12px;
        background: rgba(148, 163, 184, 0.06);
        border: 1px solid var(--line);
        transition: all 0.2s ease;
      }

      .socials a:hover {
        border-color: rgba(56, 189, 248, 0.38);
        transform: translateY(-2px);
      }

      .profile-card {
        display: flex;
        flex-direction: column;
        gap: 18px;
        align-items: center;
        justify-self: center;
        width: min(100%, 340px);
        padding: 20px;
        border-radius: 22px;
        background: rgba(148, 163, 184, 0.04);
        border: 1px solid var(--line);
      }

      .avatar {
        width: 170px;
        height: 170px;
        border-radius: 50%;
        object-fit: cover;
        border: 3px solid rgba(56, 189, 248, 0.4);
        box-shadow: 0 18px 38px rgba(56, 189, 248, 0.2);
      }

      .mini-stats {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        width: 100%;
        gap: 12px;
      }

      .mini-stat {
        background: rgba(15, 23, 42, 0.8);
        border: 1px solid var(--line);
        border-radius: 14px;
        padding: 12px 8px;
        text-align: center;
      }

      .mini-stat strong {
        display: block;
        font-size: 1.15rem;
        margin-bottom: 2px;
      }

      .mini-stat span {
        color: var(--muted);
        font-size: 0.75rem;
      }

      section {
        margin-top: 28px;
      }

      .section-header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 16px;
        margin-bottom: 18px;
      }

      .section-header h2 {
        margin: 0;
        font-size: clamp(1.5rem, 2vw, 2rem);
      }

      .section-header .line {
        flex: 1;
        height: 1px;
        background: linear-gradient(90deg, rgba(56, 189, 248, 0.45), rgba(148, 163, 184, 0.1));
      }

      .about-grid,
      .projects-grid,
      .contact-grid {
        display: grid;
        gap: 20px;
      }

      .about-grid {
        grid-template-columns: 1.4fr 0.9fr;
      }

      .panel {
        background: var(--panel);
        border: 1px solid var(--line);
        border-radius: 22px;
        box-shadow: var(--shadow);
      }

      .about-card,
      .stack-card,
      .projects-card,
      .contact-card {
        padding: 24px;
      }

      .about-card p {
        margin: 0;
        color: var(--muted);
        font-size: 1rem;
      }

      .tag-list {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-top: 18px;
      }

      .tag {
        background: rgba(56, 189, 248, 0.08);
        border: 1px solid rgba(56, 189, 248, 0.2);
        color: #caf0ff;
        border-radius: 999px;
        padding: 8px 12px;
        font-size: 0.76rem;
        letter-spacing: 0.04em;
        font-weight: 700;
      }

      .stack-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 18px;
      }

      .stack-card h3 {
        margin-top: 0;
        margin-bottom: 16px;
      }

      .chip-list {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
      }

      .chip {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 8px 12px;
        border-radius: 10px;
        background: rgba(148, 163, 184, 0.06);
        border: 1px solid var(--line);
        color: var(--text);
        font-size: 0.74rem;
        font-weight: 700;
      }

      .projects-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .projects-card {
        position: relative;
        overflow: hidden;
      }

      .projects-card::before {
        content: "";
        position: absolute;
        inset: 0 auto auto 0;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, var(--primary), var(--primary-2));
      }

      .projects-card h3 {
        margin-top: 0;
        margin-bottom: 10px;
      }

      .projects-card p {
        color: var(--muted);
        margin: 0 0 18px;
      }

      .techs {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
        margin-bottom: 18px;
      }

      .tech {
        padding: 6px 10px;
        border-radius: 999px;
        font-size: 0.7rem;
        color: #dfeefe;
        background: rgba(56, 189, 248, 0.08);
        border: 1px solid rgba(56, 189, 248, 0.18);
      }

      .project-list {
        list-style: none;
        padding: 0;
        margin: 0;
        display: grid;
        gap: 8px;
        color: var(--muted);
      }

      .project-list li::before {
        content: "✓";
        color: var(--accent);
        margin-right: 8px;
        font-weight: 700;
      }

      .stats-banner {
        margin-top: 26px;
        padding: 18px 22px;
        border-radius: 22px;
        border: 1px solid var(--line);
        background: linear-gradient(135deg, rgba(20, 184, 166, 0.1), rgba(59, 130, 246, 0.08));
      }

      .stats-banner .gh-grid {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 16px;
        align-items: center;
      }

      .stats-banner img {
        max-width: 100%;
        border-radius: 12px;
      }

      .certs {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 18px;
      }

      .cert-item {
        padding: 18px 18px 16px;
        border-radius: 18px;
        background: rgba(148, 163, 184, 0.03);
        border: 1px solid var(--line);
      }

      .cert-item strong {
        display: block;
        margin-bottom: 8px;
      }

      .cert-item span {
        display: inline-block;
        color: var(--muted);
        font-size: 0.86rem;
      }

      .contact-grid {
        grid-template-columns: 1.2fr 0.8fr;
      }

      .contact-card p {
        color: var(--muted);
        margin-top: 0;
      }

      .contact-links {
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
        margin-top: 18px;
      }

      .contact-links a {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        min-width: 150px;
        padding: 12px 16px;
        border-radius: 12px;
        font-weight: 700;
        border: 1px solid var(--line);
        background: rgba(148, 163, 184, 0.04);
      }

      .contact-links a.primary {
        background: linear-gradient(135deg, rgba(59, 130, 246, 0.18), rgba(139, 92, 246, 0.18));
        border-color: rgba(99, 102, 241, 0.32);
      }

      .contact-box {
        padding: 20px;
        border-radius: 18px;
        border: 1px solid var(--line);
        background: rgba(148, 163, 184, 0.03);
      }

      .contact-box strong {
        display: block;
        margin-bottom: 8px;
      }

      .footer {
        text-align: center;
        color: var(--muted);
        padding-top: 20px;
        font-size: 0.9rem;
      }

      @media (max-width: 900px) {
        .hero-content,
        .about-grid,
        .contact-grid,
        .projects-grid,
        .stack-grid,
        .certs {
          grid-template-columns: 1fr;
        }

        .hero-content {
          padding: 24px 18px;
        }

        .profile-card {
          width: 100%;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <header class="hero">
        <div class="hero-shell">
          <div class="hero-content">
            <div>
              <span class="eyebrow">👋 Disponível para oportunidades</span>
              <h1>Olá, eu sou <span class="highlight">Fernando</span></h1>
              <p class="subtitle">
                Desenvolvedor Full Stack especializado em criar experiências digitais modernas,
                escaláveis e orientadas ao usuário. Transformo ideias em produtos funcionais,
                performáticos e visualmente impactantes.
              </p>

              <div class="cta-row">
                <a class="btn btn-primary" href="mailto:seu-email@exemplo.com">✉️ Contato</a>
                <a class="btn btn-secondary" href="https://github.com/fernando-gt" target="_blank" rel="noreferrer">💻 GitHub</a>
              </div>

              <div class="socials">
                <a href="https://linkedin.com/in/seu-perfil" target="_blank" rel="noreferrer" aria-label="LinkedIn">💼</a>
                <a href="mailto:seu-email@exemplo.com" aria-label="Email">📧</a>
                <a href="https://wa.me/5511999999999" target="_blank" rel="noreferrer" aria-label="WhatsApp">📱</a>
                <a href="https://fernando-gt.github.io" target="_blank" rel="noreferrer" aria-label="Portfólio">🌐</a>
              </div>
            </div>

            <div class="profile-card">
              <img class="avatar" src="https://github.com/fernando-gt.png" alt="Perfil" />
              <div class="mini-stats">
                <div class="mini-stat">
                  <strong>5+</strong>
                  <span>Anos</span>
                </div>
                <div class="mini-stat">
                  <strong>20+</strong>
                  <span>Projetos</span>
                </div>
                <div class="mini-stat">
                  <strong>100%</strong>
                  <span>Dedicação</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </header>

      <section>
        <div class="section-header">
          <h2>Sobre mim</h2>
          <div class="line"></div>
        </div>

        <div class="about-grid">
          <div class="panel about-card">
            <p>
              Com experiência em desenvolvimento web, sou especialista em criar soluções completas que
              unem funcionalidade, performance e design. Minha abordagem foca em experiências intuitivas,
              interfaces limpas e arquitetura escalável para entregar valor real ao usuário final.
            </p>
            <div class="tag-list">
              <span class="tag">Full Stack</span>
              <span class="tag">React</span>
              <span class="tag">Node.js</span>
              <span class="tag">UX/UI</span>
              <span class="tag">APIs</span>
              <span class="tag">Performance</span>
            </div>
          </div>

          <div class="panel about-card">
            <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=22D3EE&center=true&vCenter=true&width=420&lines=Desenvolvedor+Full+Stack;Especialista+em+React+e+Node.js;Apaixonado+por+UX%2FUI;Soluções+escaláveis+e+eficientes" alt="Typing SVG" style="width: 100%; border-radius: 12px;" />
          </div>
        </div>
      </section>

      <section>
        <div class="section-header">
          <h2>Stack tecnológica</h2>
          <div class="line"></div>
        </div>

        <div class="stack-grid">
          <div class="panel stack-card">
            <h3>Frontend</h3>
            <div class="chip-list">
              <span class="chip">HTML</span>
              <span class="chip">CSS</span>
              <span class="chip">JavaScript</span>
              <span class="chip">TypeScript</span>
              <span class="chip">React</span>
              <span class="chip">Next.js</span>
              <span class="chip">Tailwind</span>
              <span class="chip">Figma</span>
            </div>
          </div>

          <div class="panel stack-card">
            <h3>Backend</h3>
            <div class="chip-list">
              <span class="chip">Node.js</span>
              <span class="chip">Express</span>
              <span class="chip">Python</span>
              <span class="chip">Django</span>
              <span class="chip">PHP</span>
              <span class="chip">REST API</span>
            </div>
          </div>

          <div class="panel stack-card">
            <h3>Dados & DevOps</h3>
            <div class="chip-list">
              <span class="chip">MySQL</span>
              <span class="chip">PostgreSQL</span>
              <span class="chip">MongoDB</span>
              <span class="chip">Docker</span>
              <span class="chip">AWS</span>
              <span class="chip">GitHub</span>
            </div>
          </div>
        </div>
      </section>

      <section>
        <div class="section-header">
          <h2>Projetos em destaque</h2>
          <div class="line"></div>
        </div>

        <div class="projects-grid">
          <article class="panel projects-card">
            <h3>Sistema de Gestão Empresarial</h3>
            <p>Dashboard completo para gestão de clientes, vendas e indicadores em tempo real.</p>
            <div class="techs">
              <span class="tech">React</span>
              <span class="tech">Node.js</span>
              <span class="tech">MongoDB</span>
            </div>
            <ul class="project-list">
              <li>Dashboard analítico</li>
              <li>API REST segura</li>
              <li>Autenticação JWT</li>
            </ul>
          </article>

          <article class="panel projects-card">
            <h3>Plataforma de Cursos Online</h3>
            <p>Plataforma moderna, responsiva e otimizada para a experiência de aprendizagem.</p>
            <div class="techs">
              <span class="tech">Next.js</span>
              <span class="tech">Tailwind</span>
              <span class="tech">Firebase</span>
            </div>
            <ul class="project-list">
              <li>UI responsiva</li>
              <li>Pagamento integrado</li>
              <li>Player de vídeo</li>
            </ul>
          </article>

          <article class="panel projects-card">
            <h3>Aplicativo de Finanças Pessoais</h3>
            <p>Ferramenta para organização financeira com relatórios intuitivos e sincronização.</p>
            <div class="techs">
              <span class="tech">React Native</span>
              <span class="tech">Python</span>
              <span class="tech">SQLite</span>
            </div>
            <ul class="project-list">
              <li>Gráficos interativos</li>
              <li>Notificações</li>
              <li>Sincronização em nuvem</li>
            </ul>
          </article>
        </div>
      </section>

      <section>
        <div class="section-header">
          <h2>Certificações</h2>
          <div class="line"></div>
        </div>

        <div class="certs">
          <div class="cert-item">
            <strong>Desenvolvimento Web Avançado</strong>
            <span>Udemy • 2024 • React, Node.js, MongoDB</span>
          </div>
          <div class="cert-item">
            <strong>Arquitetura de Software</strong>
            <span>Alura • 2023 • Microserviços, Docker, AWS</span>
          </div>
          <div class="cert-item">
            <strong>UX/UI Design</strong>
            <span>Coursera • 2023 • Figma, Prototipagem</span>
          </div>
          <div class="cert-item">
            <strong>Segurança da Informação</strong>
            <span>DIO • 2022 • OWASP, Criptografia</span>
          </div>
        </div>
      </section>

      <section>
        <div class="stats-banner panel">
          <div class="section-header" style="margin-bottom: 10px;">
            <h2>Estatísticas do GitHub</h2>
            <div class="line"></div>
          </div>
          <div class="gh-grid">
            <img src="https://github-readme-stats.vercel.app/api?username=fernando-gt&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&locale=pt-br" alt="GitHub Stats" />
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=fernando-gt&layout=compact&langs_count=7&theme=tokyonight&locale=pt-br" alt="Top Languages" />
            <img src="https://streak-stats.demolab.com?user=fernando-gt&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D&locale=pt-br&mode=weekly" alt="GitHub Streak" />
          </div>
        </div>
      </section>

      <section>
        <div class="section-header">
          <h2>Vamos conversar?</h2>
          <div class="line"></div>
        </div>

        <div class="contact-grid">
          <div class="panel contact-card">
            <p>
              Estou sempre aberto a novas oportunidades, projetos desafiadores e colaborações que
              gerem impacto real para pessoas e negócios.
            </p>
            <div class="contact-links">
              <a class="primary" href="mailto:seu-email@exemplo.com">📩 Enviar e-mail</a>
              <a href="https://linkedin.com/in/seu-perfil" target="_blank" rel="noreferrer">💼 LinkedIn</a>
              <a href="https://wa.me/5511999999999" target="_blank" rel="noreferrer">📱 WhatsApp</a>
            </div>
          </div>

          <div class="panel contact-box">
            <strong>Resumo profissional</strong>
            <span style="color: var(--muted);">
              Desenvolvimento de produtos digitais, arquitetura web, interfaces modernas e soluções orientadas
              por dados, eficiência e experiência do usuário.
            </span>
          </div>
        </div>
      </section>

      <div class="footer">
        © 2026 Fernando G. T. — Desenvolvedor Full Stack
      </div>
    </div>
  </body>
</html>
