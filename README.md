<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Géopolitique & Défense</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
      color: #e0e0e0;
      line-height: 1.8;
      overflow-x: hidden;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 60px 40px;
    }

    /* HEADER */
    header {
      margin-bottom: 60px;
      text-align: left;
    }

    h1 {
      font-size: 48px;
      color: #00d4ff;
      margin-bottom: 10px;
      letter-spacing: -1px;
    }

    .role {
      font-size: 16px;
      color: #ff6b9d;
      font-weight: 600;
      margin-bottom: 20px;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .intro-text {
      font-size: 15px;
      color: #b0b0b0;
      max-width: 600px;
      margin-bottom: 25px;
    }

    /* LINKS */
    .links {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .links a {
      padding: 10px 20px;
      background: #00d4ff;
      color: #1a1a2e;
      text-decoration: none;
      border-radius: 6px;
      font-weight: 600;
      font-size: 14px;
      transition: all 0.3s ease;
    }

    .links a:hover {
      background: #ff6b9d;
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(255, 107, 157, 0.4);
    }

    /* SECTIONS */
    .section {
      margin-bottom: 80px;
    }

    h2 {
      font-size: 28px;
      color: #00d4ff;
      margin-bottom: 30px;
      border-bottom: 2px solid #ff6b9d;
      padding-bottom: 10px;
      display: inline-block;
    }

    /* PROJECT CARD */
    .project {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(0, 212, 255, 0.1);
      padding: 30px;
      margin-bottom: 30px;
      border-radius: 12px;
      transition: all 0.3s ease;
    }

    .project:hover {
      background: rgba(255, 255, 255, 0.06);
      border-color: #00d4ff;
    }

    .project-title {
      font-size: 22px;
      color: #00d4ff;
      margin-bottom: 12px;
      font-weight: 600;
    }

    .project p {
      color: #b0b0b0;
      margin-bottom: 15px;
      font-size: 14px;
    }

    ul {
      padding-left: 20px;
      margin-bottom: 20px;
    }

    li {
      color: #d0d0d0;
      margin-bottom: 10px;
      font-size: 14px;
    }

    strong {
      color: #00d4ff;
      font-weight: 600;
    }

    /* MEMOIRE LAYOUT */
    .memoire-container {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 20px;
      margin-top: 25px;
    }

    .pdf-section {
      background: #000;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid rgba(0, 212, 255, 0.2);
      height: 450px;
    }

    .pdf-section iframe {
      width: 100%;
      height: 100%;
      border: none;
      border-radius: 4px;
    }

    .images-section {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .images-section img {
      width: 100%;
      height: 135px; /* Hauteur fixe pour l'alignement */
      object-fit: cover; /* Recadre proprement l'image */
      border-radius: 6px;
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
    }

    .images-section img:hover {
      border-color: #ff6b9d;
      transform: scale(1.05);
      z-index: 5;
    }

    /* SKILLS GRID */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .skill-card {
      background: rgba(255, 255, 255, 0.05);
      border-left: 3px solid #ff6b9d;
      padding: 20px;
      border-radius: 0 8px 8px 0;
      transition: all 0.3s ease;
    }

    .skill-card:hover {
      background: rgba(255, 107, 157, 0.08);
      transform: translateX(5px);
    }

    .skill-card strong {
      color: #00d4ff;
      display: block;
      margin-bottom: 5px;
    }

    /* FOOTER */
    footer {
      margin-top: 100px;
      padding: 60px 0;
      border-top: 1px solid rgba(0, 212, 255, 0.1);
      text-align: center;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      .container { padding: 30px 20px; }
      h1 { font-size: 36px; }
      .memoire-container { grid-template-columns: 1fr; }
      .pdf-section { height: 350px; }
      .images-section { flex-direction: row; overflow-x: auto; padding-bottom: 10px; }
      .images-section img { width: 150px; flex-shrink: 0; }
    }
  </style>
</head>

<body>
  <div class="container">

    <header>
      <h1>Nicolas Decroix</h1>
      <div class="role">🌍 Master II Géopolitique | Défense & OTAN</div>
      <p class="intro-text">
        Spécialiste en géopolitique de la défense avec une expertise sur la stratégie de l'OTAN, la sécurité du flanc est européen et les enjeux géostratégiques en zone Arctique.
      </p>

      <div class="links">
        <a href="mailto:decroix.nicolasfrancois@gmail.com">📧 Email</a>
        <a href="CV DECROIX Nicolas.pdf" target="_blank">📄 Mon CV</a>
        <a href="https://github.com/DecroixNicolas" target="_blank">💻 GitHub</a>
      </div>
    </header>

    <div class="section" id="research">
      <h2>📚 Travaux de Recherche</h2>

      <div class="project">
        <div class="project-title">Mémoire de Master 1</div>
        <p><strong>La Pologne et l'exclave de Kaliningrad : projet Bouclier Oriental et nouvelles réalités frontalières</strong></p>
        
        <ul>
          <li>Analyse géostratégique basée sur une collecte rigoureuse de <strong>sources ouvertes (OSINT)</strong>.</li>
          <li><strong>Enquête de terrain :</strong> Un mois en Pologne, interviews d'élus, administrateurs et experts universitaires.</li>
          <li>Conception de <strong>cartographies originales</strong> illustrant les dynamiques de défense frontalière.</li>
          <li><strong>Distinction :</strong> Mémoire de 120 pages validé avec une note de <strong>17/20</strong>.</li>
        </ul>

        <div class="memoire-container">
          <div class="pdf-section">
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          </div>
          <div class="images-section">
            <img src="Carte-Nationale.jpg" alt="Cartographie Nationale">
            <img src="Carte-Région.png" alt="Analyse Régionale">
            <img src="Carte-Varmie.png" alt="Détail Varmie-Mazurie">
          </div>
        </div>
      </div>
    </div>

    <div class="section">
      <h2>🎯 Domaines d'Expertise</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <strong>Analyse Géopolitique</strong>
          Stratégie militaire, analyse de conflits, relations internationales.
        </div>
        <div class="skill-card">
          <strong>Défense Européenne</strong>
          Architecture de sécurité de l'OTAN, Flanc Est, Arctique.
        </div>
        <div class="skill-card">
          <strong>Langues</strong>
          Français (maternel), Anglais (C1), Polonais (B2).
        </div>
        <div class="skill-card">
          <strong>Méthodologie</strong>
          Recherche académique, interviews de terrain, OSINT, Cartographie (SIG).
        </div>
      </div>
    </div>

    <div class="section">
      <h2>👤 À Propos</h2>
      <p>
        Diplômé de Master II, je me consacre à l'étude des rapports de force contemporains. Mon approche combine une analyse théorique approfondie et une réalité de terrain, me permettant d'apporter une perspective précise sur les enjeux de sécurité qui redéfinissent l'Europe actuelle.
      </p>
    </div>

    <footer>
      <h2 style="border: none; color: #00d4ff; margin-bottom: 10px;">Contact</h2>
      <p>📧 <strong>decroix.nicolasfrancois@gmail.com</strong></p>
      <p style="margin-top: 25px; opacity: 0.6;">© 2026 Nicolas Decroix | Développé avec des notions de HTML/CSS</p>
    </footer>

  </div>
</body>
</html>
