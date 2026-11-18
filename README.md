<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#10152f">
  <title>Aprendiz de Elfo</title>
  <link rel="icon" type="image/png" href="https://raw.githubusercontent.com/calidocamino/medias/main/logo-elfo.png"> <!-- Reemplaza con la ruta de tu logo si es necesario -->
  <meta name="description" content="Muñecos navideños personalizados y artesanales. La magia de la Navidad en los pequeños detalles.">

  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: Arial, Helvetica, sans-serif;
      color: #18213b;
      background: #f7f8ff;
      line-height: 1.6;
    }
    a { text-decoration: none; color: inherit; }
    .container { width: min(1120px, 90%); margin: auto; }

    header {
      background: white;
      border-bottom: 1px solid #e8eaf3;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    nav {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }
    .logo { font-size: 23px; font-weight: 800; color: #b22222; }
    .logo span { color: #18213b; }
    .links { display: flex; align-items: center; gap: 24px; font-size: 14px; }
    .btn {
      display: inline-block;
      padding: 12px 20px;
      border-radius: 10px;
      font-weight: 700;
      border: 0;
      cursor: pointer;
      font-size: 14px;
    }
    .primary { background: #b22222; color: white; }
    .secondary { background: white; color: #b22222; border: 1px solid #f5c6cb; }
    .hero {
      padding: 90px 0;
      background: linear-gradient(120deg, #fff0f0, #ffffff 65%, #eefcff);
    }
    .hero-grid {
      display: grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 50px;
      align-items: center;
    }
    .tag {
      display: inline-block;
      background: #fdf2f2;
      color: #b22222;
      border-radius: 30px;
      padding: 7px 14px;
      font-size: 13px;
      font-weight: 700;
      margin-bottom: 20px;
    }
    h1 { font-size: clamp(38px, 5vw, 60px); line-height: 1.1; letter-spacing: -2px; }
    h1 span { color: #b22222; }
    .hero p { margin: 24px 0; color: #5b647b; font-size: 17px; max-width: 560px; }
    .actions { display: flex; flex-wrap: wrap; gap: 12px; }
    .visual {
      background: white;
      padding: 28px;
      border-radius: 24px;
      box-shadow: 0 20px 60px #303c7a18;
      border: 1px solid #e8eaff;
    }
    .visual h3 { margin-bottom: 18px; }
    .profile {
      background: #f6f6ff;
      padding: 17px;
      margin: 12px 0;
      border-radius: 12px;
      display: flex;
      gap: 14px;
      align-items: center;
    }
    .emoji { font-size: 28px; }
    .profile small { color: #69728a; display: block; }
    section { padding: 75px 0; }
    .section-title { text-align: center; margin-bottom: 38px; }
    .section-title h2 { font-size: 34px; letter-spacing: -1px; }
    .section-title p { color: #69728a; margin-top: 8px; }
    .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 22px; }
    .card {
      padding: 28px;
      background: white;
      border: 1px solid #e9eaf4;
      border-radius: 18px;
      box-shadow: 0 8px 25px #1d285008;
    }
    .card .emoji { display: block; margin-bottom: 14px; }
    .card h3 { margin-bottom: 10px; }
    .card p { color: #687188; font-size: 15px; }
    .steps { background: #fdf2f2; }
    .audiences { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
    .audience { background: white; border-radius: 20px; padding: 32px; }
    .audience ul { padding-left: 20px; margin: 18px 0 24px; color: #59637a; }
    .audience li { margin: 7px 0; }
    .cta {
      background: #171d40;
      color: white;
      text-align: center;
      border-radius: 24px;
      padding: 55px 25px;
    }
    .cta p { color: #d0d5ef; margin: 12px 0 24px; }
    footer { padding: 30px 0; color: #737b90; font-size: 13px; text-align: center; }
    .note { color: #69728a; font-size: 12px; margin-top: 14px; }

    /* Estilo flotante para botones de carrito y contacto */
    .floating-actions {
      position: fixed;
      bottom: 25px;
      right: 25px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      z-index: 99;
    }
    .floating-btn {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 12px 18px;
      border-radius: 30px;
      font-weight: 700;
      color: white;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      transition: transform 0.2s;
      font-size: 14px;
    }
    .floating-btn:hover { transform: scale(1.05); }
    .btn-cart { background: #b22222; }
    .btn-contact { background: #25d366; }

    @media (max-width: 760px) {
      .links { gap: 12px; flex-wrap: wrap; justify-content: flex-end; }
      .links a:not(.btn) { display: none; }
      nav { min-height: 68px; }
      .hero { padding: 55px 0; }
      .hero-grid, .cards, .audiences { grid-template-columns: 1fr; }
      .hero-grid { gap: 32px; }
      section { padding: 52px 0; }
      .section-title h2 { font-size: 28px; }
    }
  </style>
</head>

<body>

  <header>
    <div class="container">
      <nav>
        <a href="#" class="logo">Aprendiz de <span>Elfo</span></a>
        <div class="links">
          <a href="#servicios">Colección</a>
          <a href="#funciona">Personalización</a>
          <a href="#registro">Contacto</a>
          <!-- Botón de Carrito con enlace de Wix -->
          <a href="https://elaprendizdeelfo-my-site-9.editor.wix.com/edit/od/00e69270-0ee4-4397-8a51-ffb2186b4c69?metaSiteId=9d96619a-6cfd-4a8c-8f48-c812024fe809&editorSessionId=02687732-ebe5-4cfa-833c-417875d7fb09&fromOrigin=prompt_page" class="btn primary" target="_blank">🛒 Ver Carrito</a>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <span class="tag">NAVIDAD ARTESANAL Y EXCLUSIVA</span>
          <h1>Dale calidez a tu hogar con <span>muñecos personalizados.</span></h1>
          <p>
            Huye de lo común. Diseñamos muñecos navideños 100% artesanales y hechos a mano 
            para llenar tu sala de magia, tradición y recuerdos inolvidables.
          </p>
          <div class="actions">
            <a href="https://elaprendizdeelfo-my-site-9.editor.wix.com/edit/od/00e69270-0ee4-4397-8a51-ffb2186b4c69?metaSiteId=9d96619a-6cfd-4a8c-8f48-c812024fe809&editorSessionId=02687732-ebe5-4cfa-833c-417875d7fb09&fromOrigin=prompt_page" class="btn primary" target="_blank">🛒 Ir al Carrito →</a>
            <a href="#servicios" class="btn secondary">Conocer colección</a>
          </div>
        </div>

        <div class="visual">
          <h3>✨ Magia y detalle en cada puntada</h3>
          <div class="profile">
            <span class="emoji">🎅</span>
            <div><strong>100% Artesanales</strong><small>Cosidos a mano con amor y tradición</small></div>
          </div>
          <div class="profile">
            <span class="emoji">🎁</span>
            <div><strong>Personalizados</strong><small>Con el nombre de quienes más amas</small></div>
          </div>
          <div class="profile">
            <span class="emoji">🌟</span>
            <div><strong>Exclusividad</strong><small>Transforma tu hogar en un espacio acogedor</small></div>
          </div>
          <p class="note">Piezas únicas creadas para perdurar en el tiempo.</p>
        </div>
      </div>
    </section>

    <section id="servicios">
      <div class="container">
        <div class="section-title">Nuestra Colección Navideña</h2>
          <p>Seis personajes entrañables listos para habitar tu hogar.</p>
        </div>
        <div class="cards">
          <article class="card">
            <span class="emoji">🎅</span>
            <h3>Papá Noel</h3>
            <p>El clásico guardián de la ilusión navideña con sus acabados suaves y tradicionales.</p>
          </article>
          <article class="card">
            <span class="emoji">🦌</span>
            <h3>Reno Navideño</h3>
            <p>Tierno y entrañable, ideal para aportar un toque cálido y rústico a tu sala.</p>
          </article>
          <article class="card">
            <span class="emoji">🧝</span>
            <h3>Duende Elfo</h3>
            <p>El espíritu travieso y mágico que da nombre y alma a nuestra colección.</p>
          </article>
        </div>
      </div>
    </section>
  </main>

  <!-- Botones Flotantes (Carrito y Contacto con Walink) -->
  <div class="floating-actions">
    <a href="https://elaprendizdeelfo-my-site-9.editor.wix.com/edit/od/00e69270-0ee4-4397-8a51-ffb2186b4c69?metaSiteId=9d96619a-6cfd-4a8c-8f48-c812024fe809&editorSessionId=02687732-ebe5-4cfa-833c-417875d7fb09&fromOrigin=prompt_page" class="floating-btn btn-cart" target="_blank" title="Carrito de compras">
      🛒 Carrito
    </a>
    <a href="https://wa.link/tutu" class="floating-btn btn-contact" target="_blank" title="Contactar por WhatsApp">
      💬 Contacto
    </a>
  </div>

  <footer>
    <div class="container">
      © 2026 Aprendiz de Elfo · Todos los derechos reservados.
      <br>Magia, calidez y exclusividad hecha a mano.
    </div>
  </footer>

</body>
</html>
