<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Géopolitique & Défense</title>
  <style>
    /* RESET ET STYLE SYSTÈME */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #0f172a;
      color: #f1f5f9;
      line-height: 1.6;
      overflow-x: hidden;
    }
    .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; }
    
    /* HEADER */
    header { border-bottom: 1px solid #1e293b; padding-bottom: 30px; margin-bottom: 30px; }
    h1 { font-size: 42px; color: #38bdf8; letter-spacing: -1px; }
    .subtitle { font-size: 18px; color: #f472b6; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; }
    .contact-info { margin-top: 15px; font-size: 14px; color: #94a3b8; }
    
    /* BARRE D'ONGLETS (TABS) */
    .tabs-nav {
      display: flex;
      gap: 10px;
      margin-bottom: 40px;
      border-bottom: 1px solid #1e293b;
      padding-bottom: 10px;
      overflow-x: auto;
    }
    .tab-btn {
      background: none;
      border: none;
      color: #94a3b8;
      padding: 10px 20px;
      cursor: pointer;
      font-weight: 700;
      font-size: 14px;
      text-transform: uppercase;
      transition: 0.3s;
      white-space: nowrap;
      border-radius: 6px;
    }
    .tab-btn:hover { color: #38bdf8; background: #1e293b; }
    .tab-btn.active {
      color: #38bdf8;
      background: #1e293b;
      box-shadow: 0 2px 0 #38bdf8;
    }

    /* CONTENU DES ONGLETS */
    .tab-content { display: none; animation: fadeIn 0.4s ease; }
    .tab-content.active { display: block; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* STYLES DES SECTIONS (REPRISE DE TON CODE) */
    h2 { font-size: 24px; color: #38bdf8; margin-bottom: 35px; border-left: 4px solid #f472b6; padding-left: 15px; }

    /* TIMELINE */
    .timeline { position: relative; max-width: 850px; margin: 0 auto; padding-left: 40px; }
    .timeline::after { content: ''; position: absolute; width: 2px; background-color: #1e293b; top: 0; bottom: 0; left: 7px; }
    .timeline-item { position: relative; margin-bottom: 35px; }
    .timeline-item::before {
      content: ''; position: absolute; width: 14px; height: 14px; left: -40px; 
      background-color: #0f172a; border: 3px solid #f472b6; border-radius: 50%; z-index: 1; top: 6px;
    }
    .timeline-date { font-weight: 700; color: #f472b6; font-size: 14px; margin-bottom: 5px; display: block; }
    .timeline-content { background: #1e293b; padding: 20px; border-radius: 8px; border: 1px solid #334155; }

    /* MÉMOIRE */
    .research-card { background: #1e293b; border: 1px solid #334155; border-radius: 12px; padding: 25px; }
    .research-grid { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 20px; }
    .pdf-window { background: #000; border-radius: 6px; height: 480px; overflow: hidden; border: 1px solid #334155; }
    .pdf-window iframe { width: 100%; height: 100%; border: none; }
    .visual-gallery { display: flex; flex-direction: column; gap: 10px; }
    .visual-gallery a img { width: 100%; border-radius: 4px; border: 1px solid #334155; height: 153px; object-fit: cover; transition: 0.3s; }
    .visual-gallery a img:hover { border-color: #38bdf8; }

    /* SKILLS */
    .skills-bar { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; margin-top: 20px; }
    .skill-tag { background: #1a2233; border: 1px solid #334155; padding: 15px; border-radius: 6px; border-bottom: 3px solid #f472b6; }
    .skill-tag strong { color: #38bdf8; display: block; margin-bottom: 5px; }

    footer { text-align: center; color: #475569; font-size: 12px; margin-top: 80px; padding: 40px 0; border-top: 1px solid #1e293b; }

    /* RESPONSIVE MOBILE */
    @media (max-width: 850px) {
      .research-grid { grid-template-columns: 1fr; }
      .visual-gallery { flex-direction: row; overflow-x: auto; gap: 10px; }
      .visual-gallery a { width: 160px; flex-shrink: 0; height: 120px; }
      .visual-gallery a img { height: 100%; }
    }
  </style>
</head>
<body>

<div class="container">
  <header>
    <h1>Nicolas Decroix</h1>
    <p class="subtitle">Analyste Géopolitique & Défense</p>
    <p class="contact-info">📍 Paris, France | 📧 decroix.nicolasfrancois@gmail.com</p>
  </header>

  <nav class="tabs-nav">
    <button class="tab-btn active" onclick="openTab(event, 'recherche')">📚 Recherche</button>
    <button class="tab-btn" onclick="openTab(event, 'parcours')">🎓 Parcours</button>
    <button class="tab-btn" onclick="openTab(event, 'experiences')">💼 Expériences</button>
    <button class="tab-btn" onclick="openTab(event, 'expertises')">🛠 Expertises</button>
  </nav>

  <div id="recherche" class="tab-content active">
    <section>
      <h2>📚 Travaux de Recherche</h2>
      <div class="research-card">
        <h3 style="color: #f1f5f9; margin-bottom: 10px;">La Pologne et l'exclave de Kaliningrad</h3>
        <div class="research-grid">
          <div class="pdf-window">
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          </div>
          <div class="visual-gallery">
            <a href="carte-nationale.jpg" target="_blank"><img src="carte-nationale.jpg" alt="Carte 1"></a>
            <a href="Carte-Région.png" target="_blank"><img src="Carte-Région.png" alt="Carte 2"></a>
            <a href="Carte-Varmie.png" target="_blank"><img src="Carte-Varmie.png" alt="Carte 3"></a>
          </div>
        </div>
      </div>
    </section>
  </div>

  <div id="parcours" class="tab-content">
    <section>
      <h2>🎓 Cursus Académique</h2>
      <div class="timeline">
        <div class="timeline-item">
          <span class="timeline-date">2024 — 2026</span>
          <div class="timeline-content">
            <h3>Master de Géopolitique</h3>
            <p>IFG - Université Paris-VIII</p>
          </div>
        </div>
        <div class="timeline-item">
          <span class="timeline-date">2021 — 2024</span>
          <div class="timeline-content">
            <h3>Double Licence Histoire & Géographie</h3>
            <p>Université Jean Moulin Lyon-III</p>
          </div>
        </div>
      </div>
    </section>
  </div>

  <div id="experiences" class="tab-content">
    <section>
      <h2>💼 Expériences Professionnelles</h2>
      <div class="skills-bar" style="grid-template-columns: 1fr;">
        <div class="skill-tag">
          <strong>Assistant de la Secrétaire Générale — ERUA</strong>
          <span>Analyses stratégiques et rapports institutionnels (2024-2025).</span>
        </div>
        <div class="skill-tag" style="margin-top:15px;">
          <strong>Stagiaire Recherche — CNRS</strong>
          <span>Programme 13-Novembre : Analyse de données et confidentialité.</span>
        </div>
      </div>
    </section>
  </div>

  <div id="expertises" class="tab-content">
    <section>
      <h2>🛠 Compétences Techniques</h2>
      <div class="skills-bar">
        <div class="skill-tag"><strong>Langues</strong><span>Anglais (C2), Polonais (B1-B2)</span></div>
        <div class="skill-tag"><strong>Outils SIG</strong><span>QGIS, ArcGIS, Illustrator</span></div>
        <div class="skill-tag"><strong>Méthodes</strong><span>OSINT, Veille stratégique</span></div>
      </div>
    </section>
  </div>

  <footer>
    <p>Nicolas Decroix — 2026 — Analyste Géopolitique & Défense</p>
  </footer>
</div>

<script>
  function openTab(evt, tabName) {
    // 1. Cacher tous les contenus
    var contents = document.getElementsByClassName("tab-content");
    for (var i = 0; i < contents.length; i++) {
      contents[i].classList.remove("active");
    }

    // 2. Désactiver tous les boutons
    var btns = document.getElementsByClassName("tab-btn");
    for (var i = 0; i < btns.length; i++) {
      btns[i].classList.remove("active");
    }

    // 3. Afficher l'onglet cliqué et activer son bouton
    document.getElementById(tabName).classList.add("active");
    evt.currentTarget.classList.add("active");
  }
</script>

</body>
</html>
