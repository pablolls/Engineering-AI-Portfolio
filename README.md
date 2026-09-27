<!DOCTYPE html><html lang="es"><head>
  <meta charset="UTF-8">
  <title>Pablo Llorente Senín | Carta de Presentación &amp; Portfolio</title>
  <style>
    @page { margin: 0; }
    *, *::before, *::after { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; }
    html { background-color: #ffffff; }
    @media (prefers-color-scheme: dark) {
        html { background-color: #1f1f1f; }
    }
    body { 
        padding: 24px 0;
        margin: 0 auto;
        max-width: 900px !important;
        border: none !important;
        background: transparent !important; 
        font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, Helvetica, Arial, sans-serif;
        color: #1e293b;
    }
    .page {
        height: 297mm;
        margin: 0 auto 12px auto;
        padding: 18mm 18mm 12mm 18mm;
        background-color: #ffffff;
        border: 1px solid rgba(0, 0, 0, 0.12);
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        position: relative;
        overflow: hidden;
    }
    @media screen and (max-width: 600px) {
        body { padding: 16px 0; }
        .page { margin: 0 auto 8px auto; border: none; padding: 12px 20px; }
    }
    .page-content {
        flex: 1 1 0;
        min-height: 0;
        overflow: hidden;
    }
    .page-footer {
        flex-shrink: 0;
        margin-top: auto;
        padding-top: 4mm;
        border-top: 1px solid #e2e8f0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: 8.5pt;
        color: #64748b;
    }
    @media print {
        *, *::before, *::after {
            box-shadow: none !important;
            text-shadow: none !important;
            -webkit-print-color-adjust: exact;
            print-color-adjust: exact;
        }
        body { padding: 0; background: none; }
        .page {
            margin: 0;
            border: none;
            height: 297mm;
            break-after: page;
            page-break-after: always;
        }
        .page:last-child { break-after: auto; page-break-after: auto; }
    }
    [contenteditable]:focus { outline: none; }

    /* Custom Design Elements */
    .header-banner {
        display: flex;
        align-items: center;
        justify-content: space-between;
        border-bottom: 2px solid #0f172a;
        padding-bottom: 14px;
        margin-bottom: 18px;
    }
    .header-text h1 {
        font-size: 20pt;
        font-weight: 700;
        color: #0f172a;
        margin: 0 0 4px 0;
        letter-spacing: -0.02em;
    }
    .header-text h2 {
        font-size: 11pt;
        font-weight: 600;
        color: #2563eb;
        margin: 0;
        text-transform: uppercase;
        letter-spacing: 0.05em;
    }
    .contact-pills {
        display: flex;
        gap: 12px;
        font-size: 8.5pt;
        color: #475569;
        margin-top: 6px;
    }
    .pill {
        background: #f1f5f9;
        padding: 3px 8px;
        border-radius: 4px;
        border: 1px solid #e2e8f0;
    }
    
    .intro-card {
        background: #f8fafc;
        border-left: 4px solid #2563eb;
        padding: 12px 16px;
        border-radius: 0 6px 6px 0;
        margin-bottom: 16px;
    }
    .intro-card p {
        margin: 0;
        font-size: 9.5pt;
        line-height: 1.5;
        color: #334155;
    }

    .letter-body {
        font-size: 9.5pt;
        line-height: 1.55;
        color: #334155;
        margin-bottom: 16px;
    }
    .letter-body p {
        margin: 0 0 10px 0;
    }

    .section-title {
        font-size: 11pt;
        font-weight: 700;
        color: #0f172a;
        border-bottom: 1px solid #cbd5e1;
        padding-bottom: 4px;
        margin: 16px 0 10px 0;
        text-transform: uppercase;
        letter-spacing: 0.03em;
        display: flex;
        align-items: center;
        gap: 8px;
    }

    .grid-2 {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
        margin-bottom: 14px;
    }

    .card {
        border: 1px solid #e2e8f0;
        background: #ffffff;
        border-radius: 6px;
        padding: 10px 12px;
    }
    .card-title {
        font-weight: 700;
        font-size: 9.5pt;
        color: #1e293b;
        margin-bottom: 2px;
    }
    .card-subtitle {
        font-size: 8.5pt;
        color: #2563eb;
        font-weight: 600;
        margin-bottom: 6px;
    }
    .card-text {
        font-size: 8.5pt;
        color: #475569;
        line-height: 1.4;
    }

    .tech-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 6px;
        margin-top: 6px;
    }
    .tag {
        font-size: 8pt;
        background: #eff6ff;
        color: #1d4ed8;
        padding: 2px 8px;
        border-radius: 12px;
        border: 1px solid #bfdbfe;
        font-weight: 500;
    }

    .skills-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
        margin-top: 8px;
    }
    .skill-box {
        background: #f8fafc;
        border: 1px solid #e2e8f0;
        border-radius: 6px;
        padding: 8px 10px;
    }
    .skill-box h4 {
        margin: 0 0 4px 0;
        font-size: 8.5pt;
        color: #0f172a;
        font-weight: 700;
    }
    .skill-box ul {
        margin: 0;
        padding-left: 14px;
        font-size: 8pt;
        color: #475569;
    }
    .skill-box li {
        margin-bottom: 2px;
    }

    .signature-block {
        margin-top: 16px;
        font-size: 9.5pt;
        color: #334155;
    }
    .signature-name {
        font-weight: 700;
        color: #0f172a;
        margin-top: 4px;
    }
  </style>
<style data-bard-injected="true">
@media screen {
    html {
        background-color: #ffffff;
    }
    body {
        padding: 8px 0 24px 0;
    }
}
@media screen and (prefers-color-scheme: dark) {
    html {
        background-color: #1f1f1f;
    }
}
@media screen and (max-width: 600px) {
    body {
        padding: 4px 0 16px 0;
        margin: 0 auto;
    }
}
</style></head>
<body>
  <div contenteditable="true">
    <section class="page">
      <div class="page-content">
        
        <!-- Header Masthead -->
        <header class="header-banner">
          <div class="header-text">
            <h1>Pablo Llorente Senín</h1>
            <h2>Ingeniero Informático &amp; Consultor IT</h2>
            <div class="contact-pills">
              <span class="pill">📍 Madrid, España</span>
              <span class="pill">📞 (+34) 678 88 15 63</span>
              <span class="pill">✉️ pablollorente02@gmail.com</span>
              <span class="pill">🌐 github.com/pablolls</span>
            </div>
          </div>
        </header>

        <!-- Intro Highlight Card -->
        <div class="intro-card">
          <p><strong>¡Hola! Te doy la bienvenida a mi portfolio profesional.</strong> Soy un Ingeniero Informático apasionado por el desarrollo de software robusto, la arquitectura de datos y la integración práctica de la Inteligencia Artificial para la resolución de retos complejos en sectores altamente exigentes.</p>
        </div>

        <!-- Carta de Presentación -->
        <div class="letter-body">
          <p>A lo largo de mi trayectoria profesional y académica, he tenido la oportunidad de trabajar en la conceptualización, desarrollo y optimización de soluciones tecnológicas de alto valor añadido. Mi perfil combina una sólida base técnica en ingeniería de software con una visión analítica orientada a resultados y eficiencia operativa.</p>
          <p>Actualmente me desempeño como <strong>IT Consultant en NFQ Advisory</strong>, donde participo activamente en proyectos de gestión de datos de mercado e instrumentos financieros para clientes de primer nivel como <strong>BBVA</strong>. En este rol, combino la ingeniería de datos con el diseño e implementación de herramientas basadas en Inteligencia Artificial para la automatización de procesos y optimización del trabajo operativo.</p>
        </div>

        <!-- Experiencia Destacada (Cards Grid) -->
        <div class="section-title">💼 Experiencia Clave</div>
        <div class="grid-2">
          <div class="card">
            <div class="card-title">IT Consultant</div>
            <div class="card-subtitle">NFQ Advisory, Solutions &amp; Outsourcing | 10/2025 – Actualidad</div>
            <div class="card-text">
              Análisis y gestión de datos financieros (CIB, Asset Control, Algorithmics). Diseño e implementación de soluciones basadas en IA para automatización y optimización de procesos en el ámbito bancario.
            </div>
          </div>
          <div class="card">
            <div class="card-title">Ingeniero Informático / Software Developer</div>
            <div class="card-subtitle">Delonia SW | 03/2024 – 09/2025</div>
            <div class="card-text">
              Desarrollo full-stack de aplicaciones web, diseño y optimización de bases de datos, seguridad de la información y colaboración activa bajo metodologías ágiles (Git, Java, ReactJS, Python).
            </div>
          </div>
        </div>

        <!-- Stack Tecnológico y Competencias -->
        <div class="section-title">🛠️ Competencias Técnicas &amp; Stack</div>
        <div class="skills-container">
          <div class="skill-box">
            <h4>Desarrollo &amp; Lenguajes</h4>
            <ul>
              <li>Java, Python, C, PHP</li>
              <li>JavaScript, ReactJS</li>
              <li>HTML5, CSS3, Tailwind</li>
            </ul>
          </div>
          <div class="skill-box">
            <h4>Datos &amp; Arquitectura</h4>
            <ul>
              <li>SQL &amp; Bases de Datos</li>
              <li>Modelado &amp; Gestión de datos</li>
              <li>Seguridad de la información</li>
            </ul>
          </div>
          <div class="skill-box">
            <h4>IA &amp; Metodologías</h4>
            <ul>
              <li>Automatización de procesos</li>
              <li>Gestión de Proyectos / Agile</li>
              <li>Git &amp; Control de versiones</li>
            </ul>
          </div>
        </div>

        <!-- Proyectos y Enfoque -->
        <div class="section-title">🎯 Mi Enfoque &amp; Valor Añadido</div>
        <div class="letter-body" style="margin-bottom: 0;">
          <p>Mi objetivo constante es tender un puente entre la innovación técnica y las necesidades reales del negocio. Destaco por mi capacidad de adaptación tecnológica, el rigor en el tratamiento de la información y mi entusiasmo por seguir investigando las fronteras de la Inteligencia Artificial aplicada.</p>
        </div>

        <!-- Firma -->
        <div class="signature-block">
          <p>Quedo a tu entera disposición para conversar sobre posibles colaboraciones o proyectos tecnológicos.</p>
          <div class="signature-name">Pablo Llorente Senín</div>
          <div style="font-size: 8.5pt; color: #64748b;">Ingeniero Informático de Servicios y Aplicaciones (Universidad de Valladolid)</div>
        </div>

      </div>

      <footer class="page-footer">
        <span>Pablo Llorente Senín — Carta de Bienvenida &amp; Portfolio</span>
        <span>Página 1 de 1</span>
      </footer>
    </section>
  </div>

<script data-bard-injected="true">
(function() {
  async function fetchFifeImageBlobUsingAlr(urlString) {
    if (urlString.startsWith('blob:') || urlString.startsWith('data:')) {
      throw new Error('Input URL is already a blob or data URL.');
    }
    var url = new URL(urlString, window.location.href);
    url.searchParams.set('alr', 'yes');
    for (var i = 0; i < 5; i++) {
      var response = await fetch(url.toString(), {credentials: 'include'});
      if (!response.ok) {
        throw new Error('Fetch received not OK response: ' + response.status);
      }
      var contentType = response.headers.get('content-type');
      if (!contentType || !contentType.startsWith('text/plain')) {
        var blob = await response.blob();
        if (blob.size > 0 && blob.type.startsWith('image/')) {
          return blob;
        }
        throw new Error('Fetched blob is not a valid image.');
      }
      url = new URL(await response.text());
    }
    throw new Error('Exceeded maximum number of redirects.');
  }

  async function updateImageSourcesUsingAlr() {
    var imgs = Array.from(document.querySelectorAll('img'));
    await Promise.all(imgs.map(async function(img) {
      if (img.src && img.src.includes('googleusercontent')) {
        try {
          var blob = await fetchFifeImageBlobUsingAlr(img.src);
          img.src = URL.createObjectURL(blob);
        } catch (e) {}
      }
    }));

    var elements = document.querySelectorAll('[style*="googleusercontent"]');
    var urlRegex = /url\((['"]?)(https?:\/\/.*?googleusercontent.*?)\1\)/;
    await Promise.all(Array.from(elements).map(async function(el) {
      var bg = el.style.backgroundImage;
      var match = bg ? bg.match(urlRegex) : null;
      if (match && match[2]) {
        try {
          var blob = await fetchFifeImageBlobUsingAlr(match[2]);
          var blobUrl = URL.createObjectURL(blob);
          el.style.backgroundImage = bg.replace(match[2], blobUrl);
        } catch (e) {}
      }
    }));
  }

  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', updateImageSourcesUsingAlr);
  } else {
    updateImageSourcesUsingAlr();
  }
})();
</script></body></html>
