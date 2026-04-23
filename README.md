<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Analyste</title>
  <style>
    :root {
      --bg-dark: #0f172a;
      --sidebar-bg: #1e293b;
      --card-bg: #1e293b;
      --accent: #38bdf8;
      --text-main: #f1f5f9;
      --text-dim: #94a3b8;
      --border: #334155;
      --sidebar-width: 280px;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      padding-left: var(--sidebar-width); 
      min-height: 100vh;
    }

    /* SIDEBAR */
    .sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: var(--sidebar-width);
      height: 100vh;
      background: var(--sidebar-bg);
      padding: 40px 20px;
      border-right: 1px solid var(--border);
      z-index: 100;
      display: flex;
      flex-direction: column;
    }

    .sidebar h1 { font-size: 20px; color: var(--accent); margin-bottom: 5px; }
    .sidebar .status { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--text-dim); margin-bottom: 40px; }

    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px 15px;
      margin-bottom: 10px;
      color: var(--text-dim);
      background: rgba(255,255,255,0.03);
      border: 1px solid transparent;
      border-radius: 6px;
      text-align: left;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    .nav-btn:hover { border-color: var(--accent); color: var(--accent); }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    .sidebar-footer { margin-top: auto; padding-top: 20px; border-top: 1px solid var(--border); }
    .linkedin-link {
      display: inline-block;
      text-decoration: none;
      color: var(--accent);
      font-size: 13px;
      font-weight: bold;
      border: 1px solid var(--accent);
      padding: 6px 12px;
      border-radius: 4px;
      transition: 0.3s;
    }

    /* CONTENU */
    .main-content {
      padding: 60px 50px 100px 50px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }

    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 26px; margin-bottom: 35px; border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 18px; margin: 25px 0 15px 0; color: var(--accent); }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 30px;
      margin-bottom: 30px;
    }

    /* SKILLS VISUELS (SANS POURCENTAGES) */
    .skill-tag-container { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 10px; }
    .skill-tag { 
        background: var(--bg-dark); 
        border: 1px solid var(--accent); 
        color: var(--text-main); 
        padding: 8px 15px; 
        border-radius: 20px; 
        font-size: 13px;
        font-weight: 600;
    }

    /* PROJETS RECHERCHE : LAYOUT PDF + IMAGES */
    .research-container {
        display: grid;
        grid-template-columns: 1fr 1fr; /* 50/50 pour le mémoire et les cartes */
        gap: 20px;
        align-items: start;
    }
    .pdf-frame { width: 100%; height: 500px; border-radius: 8px; border: 1px solid var(--border); background: #000; }
    
    .image-gallery { 
        display: flex; 
        flex-direction: column; 
        gap: 15px; 
    }
    .image-gallery img { 
        width: 100%; 
        border-radius: 6px; 
        border: 1px solid var(--border);
        transition: 0.3s;
    }
    .image-gallery img:hover { transform: scale(1.02); border-color: var(--accent); }

    .engagement-item {
      padding: 15px;
      border-left: 2px solid var(--border);
      background: rgba(255,255,255,0.02);
      margin-bottom: 15px;
    }

    @media (max-width: 1024px) {
      body { padding-left: 0; }
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { padding: 30px 20px; }
      .research-container { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <div class="status">Analyste Géopolitique & Défense</div>
    
    <nav>
      <button class="nav-btn active" onclick="switchTab('exps')">💼 Parcours & Stages</button>
      <button class="nav-btn" onclick="switchTab('projets')">🚀 Projets & Recherche</button>
      <button class="nav-btn" onclick="switchTab('skills')">🛠 Compétences</button>
      <button class="nav-btn" onclick="switchTab('formation')">🎓 Formation</button>
    </nav>

    <div class="sidebar-footer">
      <p style="font-size: 11px; color: var(--text-dim); margin-bottom: 15px;">
        ✉️ decroix.nicolasfrancois@gmail.com
      </p>
      <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="linkedin-link">LinkedIn ↗</a>
    </div>
  </aside>

  <main class="main-content">
    
    <div id="exps" class="tab-pane active">
      <h2>Parcours Professionnel & Stages</h2>
      <div class="card">
        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
          <span style="font-weight:700; color:var(--accent); font-size:18px;">Student Assistant to the Secretary General</span>
          <span style="font-size:11px; color:var(--text-dim); font-weight:bold;">Nov. 2024 — Déc. 2025</span>
        </div>
        <span style="color:var(--text-main); font-weight:600; margin-bottom:15px; display:block;">ERUA - Université Paris-VIII</span>
        <ul>
          <li>Rapports analytiques de documents européens sur l'éducation.</li>
          <li>Création de présentations et d'ateliers de comité de pilotage.</li>
          <li>Analyse d'assurance qualité et d'impact de l'alliance.</li>
          <li>Productions réalisées intégralement en anglais.</li>
        </ul>
      </div>

      <div class="card">
        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
          <span style="font-weight:700; color:var(--accent); font-size:18px;">Stagiaire Recherche (Programme 13-Novembre)</span>
          <span style="font-size:11px; color:var(--text-dim); font-weight:bold;">ÉTÉ 2023</span>
        </div>
        <span style="color:var(--text-main); font-weight:600; margin-bottom:15px; display:block;">CNRS - Equipex MATRICE</span>
        <ul>
          <li>Transcription de témoignages (attentats de 2015 / déportés).</li>
          <li>Respect rigoureux des clauses de confidentialité.</li>
        </ul>
      </div>

      <div class="card">
        <div style="display:flex; justify-content:space-between; margin-bottom:10px;">
          <span style="font-weight:700; color:var(--accent); font-size:18px;">Stagiaire au service Urbanisme</span>
          <span style="font-size:11px; color:var(--text-dim); font-weight:bold;">ÉTÉ 2022</span>
        </div>
        <span style="color:var(--text-main); font-weight:600; margin-bottom:15px; display:block;">Mairie de Caluire-et-Cuire</span>
        <ul>
          <li>Recherche pour l'implantation de mode de production d'énergie solaire.</li>
          <li>Utilisation intensive de SIG : ArcGIS, QGIS.</li>
        </ul>
      </div>
    </div>

    <div id="projets" class="tab-pane">
      <h2>Projets & Travaux</h2>
      
      <div class="project-section">
        <h3>1. Recherche Académique</h3>
        <div class="card">
          <p style="margin-bottom: 20px;"><strong>Mémoire M1 :</strong> La militarisation de la frontière russo-polonaise avec Kaliningrad (Note : 17/20).</p>
          
          <div class="research-container">
            <div>
              <iframe class="pdf-frame" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
            </div>
            <div class="image-gallery">
              <img src="Carte-nationale.png" alt="Carte 1">
              <img src="Carte-Region.png" alt="Carte 2">
              <img src="Carte-Varmie.png" alt="Carte 3">
              <p style="font-size:11px; color:var(--text-dim); text-align:center;">Extraits cartographiques réalisés sur QGIS</p>
            </div>
          </div>
        </div>
      </div>

      <div class="project-section">
        <h3>2. Activités & Engagements</h3>
        <div class="card">
          <div class="engagement-item">
            <p><strong>Séminaire de l'Office Français (Varsovie)</strong></p>
            <p style="font-size:13px; color:var(--text-dim);">Présentation d'ouvrage lors d'un séminaire de lecture à l'Université de Varsovie (Août 2025).</p>
          </div>
          <div class="engagement-item">
            <p><strong>Contribution Encyclopédique - 666 Albums Metal</strong></p>
            <p style="font-size:13px; color:var(--text-dim);">Rédaction d'une chronique d'album pour l'ouvrage publié aux Éditions du Nouveau Monde.</p>
          </div>
        </div>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Expertises & Langues</h2>
      
      <div class="card">
        <h3>Compétences Techniques</h3>
        <div class="skill-tag-container">
            <div class="skill-tag">Cartographie (QGIS / ArcGIS)</div>
            <div class="skill-tag">Analyse Géopolitique</div>
            <div class="skill-tag">Veille OSINT</div>
            <div class="skill-tag">Adobe Illustrator</div>
            <div class="skill-tag">Suite Office</div>
        </div>
      </div>

      <div class="card">
        <h3>Langues</h3>
        <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap:10px;">
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong>Français</strong><br><span style="color:var(--accent); font-size:12px;">Maternel</span>
          </div>
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong>Anglais</strong><br><span style="color:var(--accent); font-size:12px;">C2 (Bilingue)</span>
          </div>
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong>Polonais</strong><br><span style="color:var(--accent); font-size:12px;">B1-B2</span>
          </div>
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong>Espagnol</strong><br><span style="color:var(--accent); font-size:12px;">B1</span>
          </div>
        </div>
      </div>
    </div>

    <div id="formation" class="tab-pane">
      <h2>Cursus Académique</h2>
      <div class="card">
        <p><strong>2024-2026 :</strong> Master Géopolitique (IFG - Paris-VIII). Nouveaux Acteurs.</p>
      </div>
      <div class="card">
        <p><strong>2021-2024 :</strong> Double licence Histoire / Géographie (Lyon-III). Mention Bien.</p>
      </div>
    </div>

  </main>

  <script>
    function switchTab(tabId) {
      document.querySelectorAll('.tab-pane').forEach(p => p.classList.remove('active'));
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      document.getElementById(tabId).classList.add('active');
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(tabId));
      if(btn) btn.classList.add('active');
      window.scrollTo(0, 0);
    }
  </script>

</body>
</html>
