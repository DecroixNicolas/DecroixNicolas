<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Géopolitique & Défense</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    /* RESET PROPRE */
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
      overflow-x: hidden; /* Empêche le scroll horizontal parasite */
    }

    .container {
      max-width: 940px; /* Légèrement élargi pour le confort visuel */
      margin: 0 auto;
      padding: 60px 40px;
    }

    /* HEADER */
    header {
      margin-bottom: 70px;
      text-align: left;
    }

    h1 {
      font-size: 52px;
      color: #00d4ff;
      margin-bottom: 10px;
      letter-spacing: -1.5px;
      font-weight: 700;
    }

    .role {
      font-size: 17px;
      color: #ff6b9d;
      font-weight: 600;
      margin-bottom: 25px;
      text-transform: uppercase;
      letter-spacing: 1.5px;
    }

    .intro-text {
      font-size: 16px;
      color: #b0b0b0;
      max-width: 650px;
      margin-bottom: 30px;
    }

    /* BOUTONS DE LIENS PRINCIPAUX */
    .links {
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
    }

    .links a {
      padding: 12px 24px;
      background: #00d4ff;
      color: #1a1a2e;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 700;
      font-size: 15px;
      transition: all 0.3s ease;
      box-shadow: 0 4px 6px rgba(0, 212, 255, 0.2);
    }

    .links a:hover {
      background: #ff6b9d;
      transform: translateY(-4px);
      box-shadow: 0 6px 15px rgba(255, 107, 157, 0.5);
    }

    /* SECTIONS */
    .section {
      margin-bottom: 90px;
    }

    h2 {
      font-size: 30px;
      color: #00d4ff;
      margin-bottom: 35px;
      border-bottom: 3px solid #ff6b9d;
      padding-bottom: 12px;
      display: inline-block;
      font-weight: 700;
    }

    /* CARTE DE PROJET (RECHERCHES) */
    .project {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(0, 212, 255, 0.12);
      padding: 35px;
      margin-bottom: 30px;
      border-radius: 14px;
      transition: all 0.3s ease;
    }

    .project:hover {
      background: rgba(255, 255, 255, 0.07);
      border-color: rgba(0, 212, 255, 0.4);
    }

    .project-title {
      font-size: 24px;
      color: #00d4ff;
      margin-bottom: 15px;
      font-weight: 700;
    }

    .project p {
      color: #b0b0b0;
      margin-bottom: 20px;
      font-size: 15px;
    }

    ul {
      padding-left: 22px;
      margin-bottom: 25px;
    }

    li {
      color: #d0d0d0;
      margin-bottom: 12px;
      font-size: 15px;
    }

    strong {
      color: #00d4ff;
      font-weight: 600;
    }

    /* GRILLE DE LAYOUT DU MÉMOIRE */
    .memoire-container {
      display: grid;
      grid-template-columns: 1.3fr 0.7fr; /* Plus d'espace pour le PDF */
      gap: 25px;
      margin-top: 30px;
    }

    /* SECTION PDF (IFRAME) */
    .pdf-section {
      background: #000; /* Fond noir pour le contraste du PDF */
      padding: 8px;
      border-radius: 10px;
      border: 1px solid rgba(0, 212, 255, 0.2);
      height: 500px; /* Hauteur généreuse pour la lecture */
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
    }

    .pdf-section iframe {
      width: 100%;
      height: 100%;
      border: none;
      border-radius: 6px;
    }

    /* SECTION IMAGES (CARTES) */
    .images-section {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    /* Conteneur de lien pour chaque image cliquable */
    .images-section a {
      display: block;
      width: 100%;
      height: 155px; /* Aligné sur la grille PDF */
      overflow: hidden; /* Empêche le débordement lors du zoom */
      border-radius: 8px;
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
      cursor: zoom-in; /* Indique que l'image est cliquable */
    }

    .images-section img {
      width: 100%;
      height: 100%;
      object-fit: cover; /* Recadre proprement sans déformer */
      transition: transform 0.4s ease; /* Animation fluide du zoom */
    }

    /* EFFETS AU SURVOL DES IMAGES */
    .images-section a:hover {
      border-color: #ff6b9d;
      box-shadow: 0 5px 15px rgba(255, 107, 157, 0.3);
      z-index: 2; /* Passe au-dessus des autres */
    }

    .images-section a:hover img {
      transform: scale(1.08); /* Léger effet de zoom dans le cadre */
    }

    /* SKILLS GRID (COMPÉTENCES) */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 25px;
    }

    .skill-card {
      background: rgba(255, 255, 255, 0.04);
      border-left: 4px solid #ff6b9d;
      padding: 25px;
      border-radius: 0 10px 10px 0;
      transition: all 0.3s ease;
    }

    .skill-card:hover {
      background: rgba(255, 107, 157, 0.08);
      transform: translateX(8px);
    }

    .skill-card strong {
      color: #00d4ff;
      display: block;
      margin-bottom: 8px;
      font-size: 16px;
      font-weight: 700;
    }

    .skill-card span {
      font-size: 14px;
      color: #b0b0b0;
    }

    /* FOOTER */
    footer {
      margin-top: 120px;
      padding: 70px 0;
      border-top: 1px solid rgba(0, 212, 255, 0.1);
      text-align: center;
      background: rgba(0,0,0,0.1);
    }

    footer h2 {
      border: none;
      color: #00d4ff;
      margin-bottom: 15px;
      padding-bottom: 0;
    }

    /* RESPONSIVE (MOBILE) */
    @media (max-width: 768px) {
      .container { padding: 40px 20px; }
      h1 { font-size: 38px; }
      .role { font-size: 14px; }
      
      .memoire-container {
        grid-template-columns: 1fr; /* Pile tout en colonne */
      }
      
      .pdf-section { height: 400px; }
      
      .images-section {
        flex-direction: row; /* Aligne les cartes horizontalement */
        overflow-x: auto; /* Permet le défilement horizontal */
        padding-bottom: 15px;
        gap: 10px;
      }
      
      .images-section a {
        width: 200px; /* Largeur fixe pour le scroll */
        flex-shrink: 0;
        height: 150px;
      }
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
        <a href="mailto:decroix.nicolasfrancois@gmail.com">📧 Me Contacter</a>
        <a href="CV DECROIX Nicolas.pdf" target="CV DECROIX Nicolas.pdf">📄 Mon CV (PDF)</a>
        <a href="https://github.com/DecroixNicolas" target="_blank">💻 Profil GitHub</a>
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
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview" allow="autoplay"></iframe>
          </div>
          
          <div class="images-section">
            <a href="carte-nationale.jpg" target="_blank" title="Cliquez pour agrandir">
              <img src="carte-nationale.jpg" alt="Cartographie Nationale de Défense">
            </a>
            
            <a href="Carte-Région.png" target="_blank" title="Cliquez pour agrandir">
              <img src="Carte-Région.png" alt="Analyse Géopolitique Régionale">
            </a>
            
            <a href="Carte-Varmie.png" target="_blank" title="Cliquez pour agrandir">
              <img src="Carte-Varmie.png" alt="Détail Varmie-Mazurie">
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="section">
      <h2>🎯 Domaines d'Expertise</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <strong>Analyse Géopolitique</strong>
          <span>Stratégie militaire, analyse de conflits, relations internationales contemporaines.</span>
        </div>
        <div class="skill-card">
          <strong>Défense Européenne</strong>
          <span>Architecture de sécurité de l'OTAN, sécurité du Flanc Est, enjeux Arctique.</span>
        </div>
        <div class="skill-card">
          <strong>Langues</strong>
          <span>Français (maternel), Anglais (C1 - Professionnel), Polonais (B2).</span>
        </div>
        <div class="skill-card">
          <strong>Méthodologie</strong>
          <span>Recherche académique, interviews de terrain, OSINT, Cartographie (SIG).</span>
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
      <h2>Me Contacter</h2>
      <p>📧 <strong>decroix.nicolasfrancois@gmail.com</strong></p>
      <p style="margin-top: 25px; opacity: 0.5; font-size: 13px;">© 2026 Nicolas Decroix | Profil Géopolitique & Défense</p>
    </footer>

  </div>
</body>
</html>
