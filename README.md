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
      transition: 0.2s;
    }
    .nav-btn:hover, .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

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
    }

    /* CONTENU */
    .main-content { padding: 60px 50px 100px 50px; max-width: 1300px; margin: 0 auto; }
    .tab-pane { display: none; animation: fadeIn 0.4s ease; }
    .tab-pane.active { display: block; }
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 26px; margin-bottom: 35px; border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 18px; margin: 25px 0 15px 0; color: var(--accent); }

    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 10px; padding: 25px; margin-bottom: 25px; }

    /* LAYOUT RECHERCHE OPTIMISÉ */
    .research-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
    }
    .pdf-frame { width: 100%; height: 500px; border-radius: 6px; border: 1px solid var(--border); }
    .image-gallery { display: flex; flex-direction: column; gap: 15px; }
    .image-gallery img { width: 100%; border-radius: 6px; border: 1px solid var(--border); display: block; }

    /* COMPÉTENCES TAGS */
    .skill-tag-container { display: flex; flex-wrap: wrap; gap: 10px; }
    .skill-tag { border: 1px solid var(--accent); padding: 5px 15px; border-radius: 20px; font-size: 13px; }

    /* PREVIEW ARTICLE */
    .article-preview {
      display: flex;
      gap: 20px;
      background: rgba(0,0,0,0.2);
      padding: 15px;
      border-radius: 8px;
      border: 1px solid var(--border);
      text-decoration: none;
      color: inherit;
      transition: 0.3s;
    }
    .article-preview:hover { border-color: var(--accent); }
    .article-img { width: 120px; height: 80px; object-fit: cover; border-radius: 4px; background: #334155; }
    .article-info h4 { color: var(--accent); font-size: 15px; margin-bottom: 5px; }
    .article-info p { font-size: 12px; color: var(--text-dim); font-style: italic; }

    @media (max-width: 1100px) {
      body { padding-left: 0; }
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { padding: 20px; }
      .research-grid { grid-template-columns: 1fr; }
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
      <p style="font-size: 11px; color: var(--text-dim); margin-bottom: 10px;">✉️ decroix.nicolasfrancois@gmail.com</p>
      <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="linkedin-link">LinkedIn ↗</a>
    </div>
  </aside>

  <main class="main-content">
    
    <div id="exps" class="tab-pane active">
      <h2>Parcours Professionnel & Stages</h2>
      <div class="card">
        <div style="display:flex; justify-content:space-between;">
          <span style="font-weight:700; color:var(--accent);">Assistant au Secrétariat Général</span>
          <span style="font-size:11px; color:var(--text-dim);">Nov. 2024 — Déc. 2025</span>
        </div>
        <span style="display:block; font-size:14px; margin-bottom:10px;">ERUA - Université Paris-VIII</span>
        <ul style="font-size:14px; color:var(--text-dim); margin-left:20px;">
          <li>Analyses stratégiques et rapports de conformité européenne.</li>
          <li>Animation de comités de pilotage (Environnement anglophone).</li>
        </ul>
      </div>

      <div class="card">
        <div style="display:flex; justify-content:space-between;">
          <span style="font-weight:700; color:var(--accent);">Stagiaire Recherche</span>
          <span style="font-size:11px; color:var(--text-dim);">ÉTÉ 2023</span>
        </div>
        <span style="display:block; font-size:14px; margin-bottom:10px;">CNRS - Equipex MATRICE</span>
        <ul style="font-size:14px; color:var(--text-dim); margin-left:20px;">
          <li>Transcription de témoignages sensibles (Attentats 2015).</li>
        </ul>
      </div>
    </div>

    <div id="projets" class="tab-pane">
      <h2>Projets & Travaux</h2>
      
      <div class="card">
        <h3>1. Recherche Académique (Mémoire M1)</h3>
        <p style="margin-bottom: 20px; font-size: 14px;"><strong>Sujet :</strong> Militarisation de la frontière Kaliningrad / Pologne (Note: 17/20).</p>
        <div class="research-grid">
          <iframe class="pdf-frame" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          <div class="image-gallery">
            <img src="Carte-nationale.png" alt="Carte Nationale">
            <img src="Carte-Region.png" alt="Carte Régionale">
            <img src="Carte-Varmie.png" alt="Carte Locale">
          </div>
        </div>
      </div>

      <div class="card">
        <h3>2. Activités & Engagements</h3>
        
        <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="article-preview">
          <div style="width:120px; height:80px; background:url('http://wns.uwm.edu.pl/sites/default/files/styles/medium/public/images/inp/img_20230620_111005.jpg') center/cover; border-radius:4px;"></div>
          <div class="article-info">
            <h4>Wizyta naukowa studenta z Francji</h4>
            <p>Traduction : "Visite scientifique d'un étudiant français" — Rencontre officielle avec les autorités académiques à l'Université d'Olsztyn (UWM).</p>
          </div>
        </a>

        <div style="margin-top:20px; padding:15px; border-left:2px solid var(--accent); background:rgba(255,255,255,0.02);">
          <p><strong>Contribution Encyclopédique</strong></p>
          <p style="font-size:13px; color:var(--text-dim);">Rédaction d'une chronique pour l'ouvrage <em>666 Albums Metal</em> (Éditions du Nouveau Monde).</p>
        </div>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Expertises & Langues</h2>
      <div class="card">
        <h3 style="margin-top:0;">Compétences Techniques</h3>
        <div class="skill-tag-container">
          <span class="skill-tag">QGIS / ArcGIS</span>
          <span class="skill-tag">Analyse Géopolitique</span>
          <span class="skill-tag">OSINT / Veille</span>
          <span class="skill-tag">Adobe Illustrator</span>
          <span class="skill-tag">Suite Office</span>
        </div>
      </div>
      <div class="card">
        <h3>Langues</h3>
        <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap:10px;">
          <div style="background:var(--bg-dark); padding:10px; border-radius:6px; text-align:center;"><strong>Anglais</strong><br><small>C2 (Bilingue)</small></div>
          <div style="background:var(--bg-dark); padding:10px; border-radius:6px; text-align:center;"><strong>Polonais</strong><br><small>B1-B2</small></div>
          <div style="background:var(--bg-dark); padding:10px; border-radius:6px; text-align:center;"><strong>Espagnol</strong><br><small>B1</small></div>
        </div>
      </div>
    </div>

    <div id="formation" class="tab-pane">
      <h2>Cursus Académique</h2>
      <div class="card">
        <p><strong>2024-2026 :</strong> Master Géopolitique (IFG). Spé. Nouveaux Acteurs.</p>
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
