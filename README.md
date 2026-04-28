<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Eduardo Cayky - Criador de Conteúdo com IA | Fotos, Vídeos e Design</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0f0f1e 0%, #1a1a2e 50%, #16213e 100%);
      color: #e0e0e0;
      line-height: 1.6;
      min-height: 100vh;
    }

    /* Navbar */
    nav {
      background: rgba(15, 15, 30, 0.95);
      padding: 1.5rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid rgba(100, 200, 255, 0.2);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      backdrop-filter: blur(10px);
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      background: linear-gradient(45deg, #64c8ff, #ff006e);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      cursor: pointer;
    }

    nav a {
      color: #e0e0e0;
      text-decoration: none;
      margin: 0 1.5rem;
      transition: color 0.3s ease;
      font-size: 0.95rem;
    }

    nav a:hover {
      color: #64c8ff;
    }

    /* Hero Section */
    .hero {
      margin-top: 80px;
      padding: 5rem 2rem;
      text-align: center;
      background: linear-gradient(180deg, rgba(100, 200, 255, 0.1) 0%, transparent 100%);
      min-height: 90vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(100, 200, 255, 0.1) 0%, transparent 70%);
      border-radius: 50%;
      top: 10%;
      left: 10%;
      animation: float 6s ease-in-out infinite;
    }

    .hero::after {
      content: '';
      position: absolute;
      width: 300px;
      height: 300px;
      background: radial-gradient(circle, rgba(255, 0, 110, 0.1) 0%, transparent 70%);
      border-radius: 50%;
      bottom: 10%;
      right: 10%;
      animation: float 8s ease-in-out infinite;
    }

    .hero-content {
      position: relative;
      z-index: 10;
      max-width: 800px;
      margin: 0 auto;
    }

    .hero h1 {
      font-size: 3.5rem;
      margin-bottom: 1.5rem;
      background: linear-gradient(45deg, #64c8ff, #ff006e, #64c8ff);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: gradient 8s ease infinite;
      font-weight: 800;
      line-height: 1.2;
    }

    .hero p {
      font-size: 1.3rem;
      margin-bottom: 2rem;
      color: #b0b0b0;
      line-height: 1.8;
    }

    .cta-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 2rem;
    }

    .btn {
      padding: 1rem 2.5rem;
      border: none;
      border-radius: 50px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
      display: inline-block;
    }

    .btn-primary {
      background: linear-gradient(45deg, #64c8ff, #00d4ff);
      color: #0f0f1e;
      box-shadow: 0 0 30px rgba(100, 200, 255, 0.4);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 0 50px rgba(100, 200, 255, 0.6);
    }

    .btn-secondary {
      background: rgba(100, 200, 255, 0.2);
      color: #64c8ff;
      border: 2px solid #64c8ff;
    }

    .btn-secondary:hover {
      background: rgba(100, 200, 255, 0.3);
      transform: translateY(-3px);
    }

    /* Services Section */
    .services {
      padding: 5rem 2rem;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section-title {
      text-align: center;
      font-size: 2.5rem;
      margin-bottom: 3rem;
      background: linear-gradient(45deg, #64c8ff, #ff006e);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin-bottom: 3rem;
    }

    .service-card {
      background: linear-gradient(135deg, rgba(100, 200, 255, 0.1) 0%, rgba(255, 0, 110, 0.05) 100%);
      border: 1px solid rgba(100, 200, 255, 0.3);
      border-radius: 15px;
      padding: 2rem;
      transition: all 0.3s ease;
      cursor: pointer;
      position: relative;
      overflow: hidden;
    }

    .service-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(100, 200, 255, 0.2), transparent);
      transition: left 0.5s ease;
    }

    .service-card:hover::before {
      left: 100%;
    }

    .service-card:hover {
      border-color: #64c8ff;
      background: linear-gradient(135deg, rgba(100, 200, 255, 0.2) 0%, rgba(255, 0, 110, 0.1) 100%);
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(100, 200, 255, 0.2);
    }

    .service-icon {
      font-size: 3rem;
      margin-bottom: 1rem;
    }

    .service-card h3 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #64c8ff;
    }

    .service-card p {
      color: #a0a0a0;
      line-height: 1.8;
    }

    /* Pricing Section */
    .pricing {
      padding: 5rem 2rem;
      background: linear-gradient(180deg, rgba(100, 200, 255, 0.05) 0%, transparent 100%);
      max-width: 1200px;
      margin: 0 auto;
    }

    .pricing-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
    }

    .price-card {
      background: rgba(26, 26, 46, 0.8);
      border: 1px solid rgba(100, 200, 255, 0.2);
      border-radius: 15px;
      padding: 2.5rem;
      text-align: center;
      position: relative;
      transition: all 0.3s ease;
    }

    .price-card.featured {
      border: 2px solid #64c8ff;
      box-shadow: 0 0 30px rgba(100, 200, 255, 0.3);
      transform: scale(1.05);
    }

    .price-card:hover {
      border-color: #ff006e;
      background: rgba(26, 26, 46, 0.95);
    }

    .price-card h3 {
      color: #64c8ff;
      margin-bottom: 1rem;
      font-size: 1.3rem;
    }

    .price-value {
      font-size: 2.5rem;
      color: #ff006e;
      font-weight: bold;
      margin-bottom: 1.5rem;
    }

    .price-features {
      list-style: none;
      margin-bottom: 2rem;
      text-align: left;
    }

    .price-features li {
      padding: 0.5rem 0;
      color: #b0b0b0;
      border-bottom: 1px solid rgba(100, 200, 255, 0.1);
    }

    .price-features li:last-child {
      border-bottom: none;
    }

    .price-features li::before {
      content: '✓ ';
      color: #00ff88;
      font-weight: bold;
      margin-right: 0.5rem;
    }

    /* Contact Section */
    .contact {
      padding: 5rem 2rem;
      max-width: 1200px;
      margin: 0 auto;
      text-align: center;
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-bottom: 3rem;
    }

    .contact-item {
      background: rgba(100, 200, 255, 0.1);
      border: 1px solid rgba(100, 200, 255, 0.2);
      border-radius: 15px;
      padding: 2rem;
      transition: all 0.3s ease;
    }

    .contact-item:hover {
      background: rgba(100, 200, 255, 0.15);
      border-color: #64c8ff;
      transform: translateY(-5px);
    }

    .contact-item h4 {
      color: #64c8ff;
      margin-bottom: 1rem;
      font-size: 1.1rem;
    }

    .contact-item a {
      color: #ff006e;
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s ease;
    }

    .contact-item a:hover {
      color: #64c8ff;
    }

    /* Footer */
    footer {
      background: rgba(15, 15, 30, 0.95);
      border-top: 1px solid rgba(100, 200, 255, 0.2);
      padding: 2rem;
      text-align: center;
      color: #808080;
    }

    /* Animations */
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(30px); }
    }

    @keyframes gradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes glow {
      0%, 100% { box-shadow: 0 0 20px rgba(100, 200, 255, 0.4); }
      50% { box-shadow: 0 0 40px rgba(100, 200, 255, 0.8); }
    }

    /* Responsive */
    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        gap: 1rem;
      }

      nav a {
        margin: 0.5rem 0;
      }

      .hero h1 {
        font-size: 2rem;
      }

      .hero p {
        font-size: 1rem;
      }

      .section-title {
        font-size: 1.8rem;
      }

      .cta-buttons {
        flex-direction: column;
      }

      .price-card.featured {
        transform: scale(1);
      }
    }
  </style>
</head>
<body>
  <!-- Navigation -->
  <nav>
    <div class="logo">ec</div>
    <div>
      <a href="#services">Serviços</a>
      <a href="#pricing">Preços</a>
      <a href="#contact">Contato</a>
      <a href="https://www.instagram.com/eduardocayky/" target="_blank">Instagram</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1>Crie Conteúdo Profissional com IA</h1>
      <p>Imagens, vídeos e designs incríveis usando inteligência artificial. Transforme ideias em resultados que vendem.</p>
      <div class="cta-buttons">
        <a href="https://wa.me/5594999081542?text=Olá! Gostaria de conhecer mais sobre seus serviços de criação de conteúdo com IA" target="_blank" class="btn btn-primary">Fazer Pedido</a>
        <a href="https://www.instagram.com/eduardocayky/" target="_blank" class="btn btn-secondary">Ver Portfólio</a>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section class="services" id="services">
    <h2 class="section-title">O que eu Ofereço</h2>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">🎨</div>
        <h3>Design com IA</h3>
        <p>Criamos designs personalizados e profissionais usando as melhores ferramentas de inteligência artificial do mercado.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">📸</div>
        <h3>Fotos Profissionais</h3>
        <p>Geração de fotos de alta qualidade para seus ensaios, produtos e conteúdo de redes sociais com IA avançada.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">🎬</div>
        <h3>Vídeos Criativos</h3>
        <p>Vídeos profissionais e dinâmicos criados com IA, perfeitos para YouTube, TikTok e outras plataformas.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">💡</div>
        <h3>Prompts & Estratégia</h3>
        <p>Ajudamos você com prompts eficientes e estratégias de conteúdo que vendem e engajam sua audiência.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">🚀</div>
        <h3>Pacotes Customizados</h3>
        <p>Soluções personalizadas de acordo com suas necessidades. Desde freelancers até grandes projetos.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">⭐</div>
        <h3>Suporte Premium</h3>
        <p>Acompanhamento completo do seu projeto com revisões ilimitadas até ficar perfeito.</p>
      </div>
    </div>
  </section>

  <!-- Pricing Section -->
  <section class="pricing" id="pricing">
    <h2 class="section-title">Tabela de Preços</h2>
    <div class="pricing-cards">
      <div class="price-card">
        <h3>Básico</h3>
        <div class="price-value">R$ 49,90</div>
        <ul class="price-features">
          <li>3 Fotos com IA</li>
          <li>Ensaio completo</li>
          <li>1 Ajuste gratuito</li>
          <li>Entrega em 24h</li>
        </ul>
        <a href="https://wa.me/5594999081542?text=Olá! Gostaria de contratar o plano Básico (R$ 49,90) - 3 Fotos com IA" target="_blank" class="btn btn-secondary">Solicitar</a>
      </div>

      <div class="price-card featured">
        <h3>Ouro</h3>
        <div class="price-value">R$ 89,90</div>
        <ul class="price-features">
          <li>8 Fotos profissionais</li>
          <li>Design personalizado</li>
          <li>2 Vídeos (15s cada)</li>
          <li>Revisões ilimitadas</li>
          <li>Entrega em 48h</li>
        </ul>
        <a href="https://wa.me/5594999081542?text=Olá! Gostaria de contratar o plano Ouro (R$ 89,90) - 8 Fotos + Design + 2 Vídeos" target="_blank" class="btn btn-primary">Começar Agora</a>
      </div>

      <div class="price-card">
        <h3>Diamante</h3>
        <div class="price-value">R$ 149,90</div>
        <ul class="price-features">
          <li>12 Fotos profissionais</li>
          <li>Design avançado</li>
          <li>4 Vídeos (30s cada)</li>
          <li>Estratégia de conteúdo</li>
          <li>Revisões ilimitadas</li>
          <li>Entrega em 48h</li>
        </ul>
        <a href="https://wa.me/5594999081542?text=Olá! Gostaria de contratar o plano Diamante (R$ 149,90) - 12 Fotos + Design + 4 Vídeos" target="_blank" class="btn btn-secondary">Contratar</a>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact" id="contact">
    <h2 class="section-title">Entre em Contato</h2>
    <p style="font-size: 1.2rem; margin-bottom: 2rem; color: #b0b0b0;">
      Escolha o melhor meio para conversar comigo:
    </p>
    <div class="contact-info">
      <div class="contact-item">
        <h4>💬 WhatsApp</h4>
        <p>Respondo rápido e posso tirar suas dúvidas sobre os serviços</p>
        <a href="https://wa.me/5594999081542" target="_blank">(94) 99908-1542</a>
      </div>
      <div class="contact-item">
        <h4>📧 Email</h4>
        <p>Para propostas e projetos maiores</p>
        <a href="mailto:cayyky@gmail.com">cayyky@gmail.com</a>
      </div>
      <div class="contact-item">
        <h4>📱 Instagram</h4>
        <p>Veja meu portfólio e acompanhe meus trabalhos</p>
        <a href="https://www.instagram.com/eduardocayky/" target="_blank">@eduardocayky</a>
      </div>
    </div>

    <div style="background: linear-gradient(45deg, rgba(100, 200, 255, 0.2), rgba(255, 0, 110, 0.2)); border: 1px solid rgba(100, 200, 255, 0.3); border-radius: 15px; padding: 2rem; margin-top: 3rem;">
      <h3 style="color: #64c8ff; margin-bottom: 1rem;">Pronto para começar?</h3>
      <p style="color: #b0b0b0; margin-bottom: 1.5rem;">
        Envie uma mensagem no WhatsApp e vamos discutir como posso ajudar seus projetos com criatividade e tecnologia!
      </p>
      <a href="https://wa.me/5594999081542" target="_blank" class="btn btn-primary">Conversar no WhatsApp</a>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2024 Eduardo Cayky - Criador de Conteúdo Digital com IA. Todos os direitos reservados.</p>
    <p style="margin-top: 1rem; font-size: 0.9rem;">Transformando ideias em resultados | Estratégia, criatividade e tecnologia</p>
  </footer>

  <script>
    function scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  </script>
</body>
</html>
