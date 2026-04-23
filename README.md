<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio</title>
  <style>
    :root {
      --bg-dark: #0f172a;
      --card-bg: #1e293b;
      --accent: #38bdf8;
      --text-main: #f1f5f9;
      --text-dim: #94a3b8;
      --border: #334155;
      --nav-height: 70px;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      padding-top: var(--nav-height); /* Espace pour le menu fixe */
    }

    /* NAVIGATION HORIZONTALE FIXE */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      height: var(--nav-height);
      background: var(--card-bg);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0 10px;
    }

    nav {
      display: flex;
      gap: 10px;
      max-width: 1200px;
      width: 100%;
      overflow-x: auto; /* Scroll horizontal sur petit mobile */
      white-space: nowrap;
      padding-bottom: 5px;
    }

    .nav-btn {
      padding: 8px 16px;
      color: var(--text-dim);
      background: transparent;
      border: 1px solid transparent;
      border-radius: 20px;
      font-size: 13px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
    }

    .nav-btn:hover { color: var(--accent); }
    .nav-btn.active {
      background: var(--accent);
      color: var(--bg-dark);
    }

    /* CONTENU */
    main {
      max-width: 900px;
      margin: 0 auto;
      padding: 30px 20px;
    }

    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    h1 { font-size: 22px; color: var(--accent); margin-bottom: 5px; text-align: center; }
    .intro { text-align: center; font-size: 12px; text-transform: uppercase; color: var(--text-dim); margin-bottom: 30px; letter-spacing: 1px; }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 25px;
      margin-bottom: 25px;
    }

    h2 { font-size: 20px; margin-bottom: 20px; border-left: 4px solid var(--accent); padding-left: 15px; }

    /* LAYOUT RECHERCHE */
    .research-layout {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    
    .pdf-container { width: 100%; height: 500px; border-radius: 8px; overflow: hidden; border: 1px solid var(--border); }
    iframe { width: 100%; height: 100%; border: none; }

    .image-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }
    .image-grid img {
      width: 100%;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: #0f172a;
    }

    /* ARTICLE LINK */
    .article-card {
      display: block;
      text-decoration: none;
      color: inherit;
      background: rgba(56, 189, 248, 0.05);
      border: 1px solid var(--accent);
      padding: 20px;
      border-radius: 10px;
      transition: 0.3s;
    }
    .article-card:hover { background: rgba(56, 189, 248, 0.1); }
    .article-card h4 { color: var(--accent); margin-bottom: 10px; }

    /* SKILLS */
    .skills-flex { display: flex; flex-wrap: wrap; gap: 10px; }
    .tag { background: var(--bg-dark); border: 1px solid var(--accent); padding: 5px 12px; border-radius: 15px; font-size: 13px; }

    footer { text-align: center; padding: 40px 0; color: var(--text-dim); font-size: 13px; }
    .contact-link { color: var(--accent); text-decoration: none; font-weight: bold; }

    /* MOBILE ADJUSTMENTS */
    @media (max-width: 600px) {
      .nav-btn { padding: 6px 12px; font-size: 12px; }
      h2 { font-size: 18px; }
      .pdf-container { height: 400px; }
    }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('exps')">Parcours</button>
      <button class="nav-btn" onclick="switchTab('projets')">Recherche</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
      <button class="nav-btn" onclick="switchTab('formation')">Formation</button>
    </nav>
  </header>

  <main>
    <h1>Nicolas Decroix</h1>
    <p class="intro">Analyste Géopolitique & Défense</p>

    <div id="exps" class="tab-pane active">
      <div class="card">
        <h2>Expériences</h2>
        <div style="margin-bottom: 20px;">
          <h3 style="color:var(--accent); font-size: 17px;">Student Assistant to the Secretary General</h3>
          <p style="font-size: 13px; color: var(--text-dim);">ERUA - Paris-VIII | Nov. 2024 — Présent</p>
          <ul style="margin: 10px 0 0 18px; font-size: 14px;">
            <li>Analyse de documents stratégiques européens.</li>
            <li>Appui à la gouvernance internationale.</li>
          </ul>
        </div>
        <div style="margin-bottom: 20px;">
          <h3 style="color:var(--accent); font-size: 17px;">Stagiaire Recherche</h3>
          <p style="font-size: 13px; color: var(--text-dim);">CNRS - Equipex MATRICE | 2023</p>
        </div>
        <div>
          <h3 style="color:var(--accent); font-size: 17px;">Stagiaire Urbanisme</h3>
          <p style="font-size: 13px; color: var(--text-dim);">Mairie de Caluire-et-Cuire | 2022</p>
        </div>
      </div>
    </div>

    <div id="projets" class="tab-pane">
      <div class="card">
        <h2>Mémoire & Terrain</h2>
        <p style="margin-bottom: 15px;"><strong>M1 :</strong> Militarisation de la frontière russo-polonaise (Kaliningrad). <span style="color:var(--accent)">Note : 17/20</span></p>
        
        <div class="research-layout">
          <div class="pdf-container">
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          </div>
          
          <div class="image-grid">
            <img src="Carte-nationale.png" alt="Carte">
            <img src="Carte-Region.png" alt="Carte">
             <img src="Carte-Varmie.png" alt="Carte">
          </div>
        </div>

        <h3 style="margin: 30px 0 15px 0; color:var(--accent);">Coopération Internationale</h3>
        <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="article-card">
          <h4>Wizyta naukowa studenta z Francji (UWM Olsztyn) ↗</h4>
          <p style="font-size: 13px; color: var(--text-dim);">"Visite scientifique d'un étudiant français" — Article de l'Université polonaise relatant mon terrain de recherche.</p>
        </a>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <div class="card">
        <h2>Compétences</h2>
        <div class="skills-flex" style="margin-bottom: 30px;">
          <span class="tag">Cartographie (QGIS / ArcGIS)</span>
          <span class="tag">Analyse Géopolitique</span>
          <span class="tag">Veille OSINT</span>
          <span class="tag">Adobe Illustrator</span>
          <span class="tag">Anglais (C2)</span>
          <span class="tag">Polonais (B1-B2)</span>
        </div>
        
        <h2>Autres Engagements</h2>
        <p style="font-size: 14px; margin-bottom: 10px;">• <strong>Séminaire Varsovie (2025)</strong> : Présentation à l'Office Français.</p>
        <p style="font-size: 14px;">• <strong>666 Albums Metal</strong> : Chroniqueur pour les Éditions du Nouveau Monde.</p>
      </div>
    </div>

    <div id="formation" class="tab-pane">
      <div class="card">
        <h2>Formation</h2>
        <p><strong>Master Géopolitique</strong><br>Institut Français de Géopolitique | 2024-2026</p>
        <hr style="margin: 15px 0; border: 0; border-top: 1px solid var(--border);">
        <p><strong>Double Licence Histoire-Géographie</strong><br>Université Lyon-III | 2021-2024</p>
      </div>
    </div>

    <footer>
      <p>✉️ <a href="mailto:decroix.nicolasfrancois@gmail.com" class="contact-link">decroix.nicolasfrancois@gmail.com</a></p>
      <p style="margin-top:10px;"><a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="contact-link">LinkedIn ↗</a></p>
    </footer>
  </main>

  <script>
    function switchTab(tabId) {
      // Désactiver tout
      document.querySelectorAll('.tab-pane').forEach(p => p.classList.remove('active'));
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      // Activer l'onglet choisi
      document.getElementById(tabId).classList.add('active');
      
      // Activer le bouton correspondant
      const btn = Array.from(document.querySelectorAll('.nav-btn'))
                       .find(b => b.getAttribute('onclick').includes(tabId));
      if(btn) btn.classList.add('active');

      // Retour en haut de page
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>

</body>
</html>
