<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pedro Francisco | Desenvolvedor Backend</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
  <style>
    html {
      scroll-behavior: smooth;
    }
    body {
      margin: 0;
      font-family: 'Poppins', Arial, sans-serif;
      background: #000;
      color: #f5f6fa;
      min-height: 100vh;
    }
    a { color: inherit; text-decoration: none; }
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 24px;
    }
    header {
      background: #000;
      border-bottom: 1.5px solid #111827;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 16px #0d6efd11;
    }
    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 0;
    }
    .navbar .logo {
      color: #0d6efd;
      font-size: 1.7rem;
      font-weight: 700;
      letter-spacing: 1px;
    }
    .navbar nav {
      display: flex;
      gap: 32px;
    }
    .navbar nav a {
      color: #f5f6fa;
      font-weight: 500;
      font-size: 1.05rem;
      padding: 6px 12px;
      border-radius: 6px;
      transition: background 0.2s, color 0.2s;
    }
    .navbar nav a:hover, .navbar nav a.active {
      background: #0d6efd;
      color: #fff;
    }
    .hero {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 60vh;
      text-align: center;
      padding: 64px 0 32px 0;
      background: linear-gradient(120deg, #000 60%, #0d6efd22 100%);
      animation: fadeIn 1.2s;
    }
    .hero h1 {
      font-size: 2.6rem;
      color: #0d6efd;
      font-weight: 700;
      margin-bottom: 10px;
      letter-spacing: 1px;
    }
    .hero h2 {
      font-size: 1.3rem;
      font-weight: 600;
      color: #f5f6fa;
      margin-bottom: 18px;
    }
    .hero p {
      color: #b0b8c1;
      font-size: 1.1rem;
      max-width: 500px;
      margin: 0 auto 18px auto;
    }
    .hero .contact-info {
      margin-top: 18px;
      color: #b0b8c1;
      font-size: 1rem;
    }
    .section {
      padding: 64px 0 32px 0;
      animation: fadeInUp 1.2s;
    }
    .section-title {
      color: #0d6efd;
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 24px;
      text-align: center;
      letter-spacing: 1px;
    }
    .about {
      max-width: 700px;
      margin: 0 auto;
      color: #e0e6ed;
      font-size: 1.15rem;
      text-align: center;
      background: #0a0a1a;
      border-radius: 18px;
      padding: 32px 24px;
      box-shadow: 0 2px 16px #0d6efd22;
    }
    .tech-list {
      display: flex;
      flex-wrap: wrap;
      gap: 32px;
      justify-content: center;
      margin-top: 24px;
    }
    .tech {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
      background: #0a0a1a;
      border-radius: 12px;
      padding: 18px 18px 12px 18px;
      min-width: 90px;
      box-shadow: 0 2px 12px #0d6efd22;
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .tech i {
      font-size: 2.1rem;
      color: #0d6efd;
      margin-bottom: 4px;
    }
    .tech span {
      font-size: 1rem;
      color: #f5f6fa;
      font-weight: 500;
    }
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
      gap: 32px;
      margin-top: 24px;
    }
    .project-card {
      background: #0a0a1a;
      border-radius: 16px;
      box-shadow: 0 2px 16px #0d6efd22;
      padding: 0 0 18px 0;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      transition: transform 0.2s, box-shadow 0.2s;
      border: 1.5px solid #0d6efd22;
      position: relative;
      overflow: hidden;
      min-height: 180px;
      animation: fadeInUp 1.2s;
    }
    .project-card:hover {
      transform: scale(1.04) translateY(-6px);
      box-shadow: 0 8px 32px #0d6efd44, 0 0 0 2px #0d6efd;
      z-index: 3;
    }
    .project-card img {
      width: 100%;
      height: 160px;
      object-fit: cover;
      border-radius: 16px 16px 0 0;
      margin-bottom: 8px;
      background: #222;
      display: block;
    }
    .project-card h3 {
      margin: 16px 0 8px 18px;
      color: #0d6efd;
      font-size: 1.2rem;
    }
    .project-card p {
      margin: 0 0 12px 18px;
      color: #b0b8c1;
      text-align: left;
      font-size: 1rem;
    }
    .project-tech {
      margin-left: 18px;
      margin-bottom: 10px;
      color: #0d6efd;
      font-size: 0.98rem;
      font-weight: 500;
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }
    .project-btn {
      margin-left: 18px;
      background: #0d6efd;
      color: #fff;
      border: none;
      border-radius: 8px;
      padding: 8px 22px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.2s, box-shadow 0.2s;
      box-shadow: 0 2px 8px #0d6efd33;
      display: inline-block;
    }
    .project-btn:hover {
      background: #0a58ca;
      box-shadow: 0 4px 16px #0d6efd55;
    }
    .contact-section {
      max-width: 500px;
      margin: 0 auto;
      background: #0a0a1a;
      border-radius: 16px;
      box-shadow: 0 2px 16px #0d6efd22;
      padding: 32px 24px 24px 24px;
      text-align: center;
    }
    .contact-section h2 {
      margin-bottom: 18px;
    }
    .contact-form {
      display: flex;
      flex-direction: column;
      gap: 14px;
      margin-top: 12px;
    }
    .contact-form input,
    .contact-form textarea {
      padding: 12px;
      border: 1px solid #0d6efd;
      border-radius: 8px;
      font-size: 1rem;
      font-family: inherit;
      background: #181828;
      color: #fff;
      resize: none;
      transition: border 0.2s, background 0.2s;
    }
    .contact-form input:focus,
    .contact-form textarea:focus {
      border: 1.5px solid #0a58ca;
      background: #22223a;
      outline: none;
    }
    .contact-form button {
      align-self: flex-end;
      background: #0d6efd;
      color: #fff;
      border: none;
      border-radius: 8px;
      padding: 10px 28px;
      font-size: 1.1rem;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 2px 8px #0d6efd44;
      transition: background 0.2s, transform 0.2s;
    }
    .contact-form button:hover {
      background: #0a58ca;
      transform: scale(1.05);
    }
    .contact-info {
      margin-top: 18px;
      color: #b0b8c1;
      font-size: 1rem;
      text-align: center;
    }
    .footer {
      background: #0a0a1a;
      color: #b0b8c1;
      text-align: center;
      padding: 24px 0 12px 0;
      font-size: 1rem;
      border-top: 1.5px solid #111827;
      margin-top: 48px;
    }
    .footer .footer-social {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      gap: 18px;
    }
    .footer .footer-social a {
      color: #0d6efd;
      font-size: 1.5rem;
      transition: color 0.2s;
    }
    .footer .footer-social a:hover {
      color: #fff;
    }
    #backToTop {
      position: fixed;
      bottom: 32px;
      right: 32px;
      background: #0d6efd;
      color: #fff;
      border: none;
      border-radius: 50%;
      width: 48px;
      height: 48px;
      font-size: 1.5rem;
      box-shadow: 0 2px 12px #0d6efd44;
      cursor: pointer;
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 100;
      transition: background 0.2s, transform 0.2s;
    }
    #backToTop.show {
      display: flex;
      animation: fadeIn 0.5s;
    }
    #backToTop:hover {
      background: #0a58ca;
      transform: scale(1.1);
    }
    @media (max-width: 900px) {
      .projects-grid { grid-template-columns: 1fr; }
      .navbar nav { gap: 18px; }
    }
    @media (max-width: 600px) {
      .container { padding: 0 4px; }
      .hero h1 { font-size: 1.5rem; }
      .section-title { font-size: 1.2rem; }
      .about { padding: 18px 6px; }
      .tech-list { gap: 16px; }
      .project-card img { height: 120px; }
      .contact-section { padding: 18px 6px; }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: none; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container navbar">
      <div class="logo">Pedro.dev</div>
      <nav>
        <a href="#home" class="active">Home</a>
        <a href="#about">Sobre</a>
        <a href="#tech">Tecnologias</a>
        <a href="#projects">Projetos</a>
        <a href="#contact">Contato</a>
      </nav>
    </div>
  </header>
  <main>
    <section class="hero" id="home">
      <h1>Olá, eu sou Pedro Francisco</h1>
      <h2>Desenvolvedor Backend Júnior</h2>
      <p>Desenvolvedor apaixonado por transformar lógica em soluções eficientes. Foco em Java, mas com interesse constante em aprender novas linguagens e frameworks. Buscando crescimento profissional em projetos desafiadores e colaborativos.</p>
      <div class="contact-info">
        <span><i class="fas fa-envelope"></i> pedroradical06@gmail.com</span> &nbsp;|&nbsp;
        <span><i class="fas fa-phone"></i> (21) 96902-1332</span>
      </div>
    </section>
    <section class="section" id="about">
      <h2 class="section-title">Sobre</h2>
      <div class="about">
        Sou um desenvolvedor backend júnior com paixão por transformar lógica em soluções eficientes. Tenho experiência com Java, Spring Boot, bancos de dados e APIs REST, mas estou sempre buscando aprender novas linguagens e frameworks. Gosto de trabalhar em equipe, enfrentar desafios e contribuir para projetos inovadores.
      </div>
    </section>
    <section class="section" id="tech">
      <h2 class="section-title">Tecnologias</h2>
      <div class="tech-list">
        <div class="tech"><i class="fab fa-java"></i><span>Java</span></div>
        <div class="tech"><i class="fas fa-leaf"></i><span>Spring Boot</span></div>
        <div class="tech"><i class="fab fa-js-square"></i><span>JavaScript</span></div>
        <div class="tech"><i class="fab fa-node-js"></i><span>Node.js</span></div>
        <div class="tech"><i class="fab fa-html5"></i><span>HTML5</span></div>
        <div class="tech"><i class="fab fa-css3-alt"></i><span>CSS3</span></div>
        <div class="tech"><i class="fab fa-git-alt"></i><span>Git & GitHub</span></div>
        <div class="tech"><i class="fas fa-database"></i><span>MySQL</span></div>
      </div>
    </section>
    <section class="section" id="projects">
      <h2 class="section-title">Projetos</h2>
      <div class="projects-grid">
        <div class="project-card">
          <img src="https://placehold.co/400x200/0d6efd/fff?text=API+de+Tarefas" alt="API de Gerenciamento de Tarefas">
          <h3>API de Gerenciamento de Tarefas</h3>
          <p>API RESTful em Java para organizar tarefas, com autenticação JWT e integração com banco de dados.</p>
          <div class="project-tech"><span>Java</span><span>Spring Boot</span><span>MySQL</span></div>
          <a href="#" class="project-btn" target="_blank">Ver no GitHub</a>
        </div>
        <div class="project-card">
          <img src="https://placehold.co/400x200/0d6efd/fff?text=Sistema+Reservas" alt="Sistema de Reservas">
          <h3>Sistema de Reservas</h3>
          <p>Backend em Java para reservas de restaurantes, com notificações automáticas e painel administrativo.</p>
          <div class="project-tech"><span>Java</span><span>Spring Boot</span><span>MySQL</span></div>
          <a href="#" class="project-btn" target="_blank">Ver no GitHub</a>
        </div>
        <div class="project-card">
          <img src="https://placehold.co/400x200/0d6efd/fff?text=Blog+Tech" alt="Blog de Tecnologia">
          <h3>Blog de Tecnologia</h3>
          <p>Blog pessoal com backend em Node.js e painel para publicação dinâmica de artigos sobre tecnologia.</p>
          <div class="project-tech"><span>Node.js</span><span>JavaScript</span><span>MySQL</span></div>
          <a href="#" class="project-btn" target="_blank">Ver no GitHub</a>
        </div>
      </div>
    </section>
    <section class="section contact-section" id="contact">
      <h2 class="section-title">Contato</h2>
      <form class="contact-form">
        <input type="text" name="nome" placeholder="Seu nome" required>
        <input type="email" name="email" placeholder="Seu e-mail" required>
        <textarea name="mensagem" placeholder="Sua mensagem" required></textarea>
        <button type="submit">Enviar</button>
      </form>
      <div class="contact-info">
        <span><i class="fas fa-envelope"></i> pedroradical06@gmail.com</span><br>
        <span><i class="fas fa-phone"></i> (21) 96902-1332</span>
      </div>
    </section>
  </main>
  <footer class="footer">
    <div>Pedro Francisco &mdash; pedroradical06@gmail.com &mdash; (21) 96902-1332</div>
    <div class="footer-social">
      <a href="#" title="GitHub" target="_blank"><i class="fab fa-github"></i></a>
      <a href="#" title="LinkedIn" target="_blank"><i class="fab fa-linkedin"></i></a>
    </div>
  </footer>
  <button id="backToTop" title="Voltar ao topo"><i class="fas fa-arrow-up"></i></button>
  <script>
    // Scroll suave e botão voltar ao topo
    const navLinks = document.querySelectorAll('.navbar nav a');
    navLinks.forEach(link => {
      link.addEventListener('click', function(e) {
        navLinks.forEach(l => l.classList.remove('active'));
        this.classList.add('active');
      });
    });
    const backToTop = document.getElementById('backToTop');
    window.addEventListener('scroll', () => {
      if(window.scrollY > 300) backToTop.classList.add('show');
      else backToTop.classList.remove('show');
    });
    backToTop.onclick = () => window.scrollTo({top:0,behavior:'smooth'});
  </script>
</body>
</html>
