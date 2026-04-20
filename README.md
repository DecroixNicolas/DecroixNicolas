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
    }

    .role {
      font-size: 16px;
      color: #ff6b9d;
      font-weight: 600;
      margin-bottom: 20px;
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
      transition: all 0.2s ease;
      border: none;
      cursor: pointer;
    }

    .links a:hover {
      background: #ff6b9d;
      transform: translateY(-2px);
    }

    /* SECTIONS */
    .section {
      margin-bottom: 60px;
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
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(0, 212, 255, 0.2);
      padding: 30px;
      margin-bottom: 30px;
      border-radius: 10px;
      transition: all 0.2s ease;
    }

    .project:hover {
      background: rgba(255, 255, 255, 0.08);
      border-color: #00d4ff;
      transform: translateY(-2px);
    }

    .project-title {
      font-size: 20px;
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

    /* MEMOIRE */
    .memoire-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      margin-top: 20px;
    }

    .pdf-section {
      background: rgba(0, 0, 0, 0.3);
      padding: 15px;
      border-radius: 8px;
      border: 1px solid rgba(0, 212, 255, 0.15);
    }

    .pdf-section iframe {
      width: 100% !important;
      border-radius: 6px;
    }

    .images-section {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .images-section img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      border: 1px solid rgba(0, 212, 255, 0.2);
      transition: all 0.2s ease;
      cursor: pointer;
    }

    .images-section img:hover {
      border-color: #00d4ff;
      transform: scale(1.02);
    }

    /* BUTTONS */
    .project-links {
      display: flex;
      gap: 12px;
      margin-top: 20px;
      flex-wrap: wrap;
    }

    .project-links a {
      padding: 8px 16px;
      background: rgba(0, 212, 255, 0.1);
      border: 1px solid #00d4ff;
      color: #00d4ff;
      text-decoration: none;
      border-radius: 5px;
      font-size: 13px;
      transition: all 0.2s ease;
    }

    .project-links a:hover {
      background: #00d4ff;
      color: #1a1a2e;
    }

    /* SKILLS GRID */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 15px;
      margin-top: 20px;
    }

    .skill-card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 107, 157, 0.3);
      padding: 20px;
      border-radius: 8px;
      transition: all 0.2s ease;
    }

    .skill-card:hover {
      background: rgba(255, 107, 157, 0.1);
      border-color: #ff6b9d;
      transform: translateY(-2px);
    }

    .skill-card strong {
      color: #ff6b9d;
      display: block;
      margin-bottom: 8px;
      font-size: 14px;
    }

    .skill-card {
      font-size: 13px;
      color: #b0b0b0;
    }

    /* FOOTER */
    footer {
      margin-top: 60px;
      padding-top: 30px;
      border-top: 1px solid rgba(0, 212, 255, 0.2);
      text-align: center;
      color: #808080;
      font-size: 13px;
    }

    footer a {
      color: #00d4ff;
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      .container {
        padding: 40px 20px;
      }

      h1 {
        font-size: 32px;
      }

      h2 {
        font-size: 22px;
      }

      .memoire-container {
        grid-template-columns: 1fr;
      }

      .links {
        flex-direction: column;
        width: 100%;
      }

      .links a {
        width: 100%;
        text-align: center;
      }
    }
  </style>
</head>

<body>
  <div class="container">

    <!-- HERO -->
    <header>
      <h1>Nicolas Decroix</h1>
      <div class="role">🌍 Master II Géopolitique | Défense & OTAN</div>
      <p class="intro-text">
        Spécialiste en géopolitique de la défense avec expertise en stratégie OTAN, sécurité du flanc est et enjeux arctiques.
      </p>

      <div class="links">
        <a href="mailto:decroix.nicolasfrancois@gmail.com">📧 Email</a>
        <a href="CV DECROIX Nicolas.pdf" target="_blank">📄 CV</a>
        <a href="https://github.com/DecroixNicolas" target="_blank">💻 GitHub</a>
      </div>
    </header>

    <!-- PROJECTS -->
    <div class="section">
      <h2>📚 Recherches</h2>

      <div class="project">
        <div class="project-title">Mémoire de Master 1</div>
        <p><strong>La Pologne et l'exclave de Kaliningrad : projet Bouclier Oriental et nouvelles réalités frontalières</strong></p>
        <ul>
          <li>Travail de recherche combinant <strong>études théoriques et collecte de sources ouvertes</strong></li>
          <li><strong>Terrain d'un mois en Pologne</strong> : interviews avec maires, administrateurs régionaux et universitaires</li>
          <li>Création de <strong>cartes originales</strong> pour illustrer les analyses géostratégiques</li>
          <li><strong>Résultat : 120 pages, note 17/20</strong></li>
        </ul>

        <div class="memoire-container">
          <div class="pdf-section">
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview" height="350px"></iframe>
          </div>
          <div class="images-section">
            <img src="Carte-Nationale.jpg" alt="Carte nationale">
            <img src="Carte-Région.png" alt="Carte Région">
            <img src="Carte-Varmie.png" alt="Carte Varmie">
          </div>
        </div>

        <div class="project-links">
          <a href="#">Lire le mémoire</a>
          <a href="#">Ressources</a>
        </div>
      </div>

    </div>

    <!-- SKILLS -->
    <div class="section">
      <h2>🎯 Compétences</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <strong>Géopolitique</strong>
          Stratégie, analyse de conflits, relations internationales
        </div>
        <div class="skill-card">
          <strong>Défense</strong>
          OTAN, stratégies de défense, sécurité européenne
        </div>
        <div class="skill-card">
          <strong>Régions</strong>
          Flanc Est, Arctique, Bassin méditerranéen
        </div>
        <div class="skill-card">
          <strong>Langues</strong>
          Français, Anglais, Polonais
        </div>
        <div class="skill-card">
          <strong>Outils</strong>
          Cartographie, SIG, analyses qualitatives
        </div>
        <div class="skill-card">
          <strong>Recherche</strong>
          Rédaction académique, sources ouvertes
        </div>
      </div>
    </div>

    <!-- ABOUT -->
    <div class="section">
      <h2>👤 À Propos</h2>
      <p>
        Diplômé du Master II Géopolitique, je suis spécialisé dans l'analyse des enjeux de défense et de sécurité, particulièrement concernant l'OTAN et le flanc est européen. Ma recherche combine approche théorique rigoureuse et travail de terrain avec expérience d'interviews multilingues.
      </p>
    </div>

    <!-- CONTACT -->
    <footer>
      <h2 style="border: none; display: block; margin-bottom: 20px; color: #00d4ff;">Contactez-moi</h2>
      <p>📧 <strong>decroix.nicolasfrancois@gmail.com</strong></p>
      <p>🔗 <a href="https://github.com/DecroixNicolas">GitHub</a></p>
      <p style="margin-top: 20px;">© 2026 Nicolas Decroix</p>
    </footer>

  </div>
</body>
</html>