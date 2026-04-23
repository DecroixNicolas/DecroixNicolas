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
      position: fixed; top: 0; left: 0; width: var(--sidebar-width); height: 100vh;
      background: var(--sidebar-bg); padding: 40px 20px; border-right: 1px solid var(--border);
      z-index: 100; display: flex; flex-direction: column;
    }
    .sidebar h1 { font-size: 20px; color: var(--accent); margin-bottom: 5px; }
    .sidebar .status { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--text-dim); margin-bottom: 40px; }

    .nav-btn {
      display: block; width: 100%; padding: 12px 15px; margin-bottom: 10px;
      color: var(--text-dim); background: rgba(255,255,255,0.03); border: 1px solid transparent;
      border-radius: 6px; text-align: left; font-size: 14px; font-weight: 600; cursor: pointer; transition: 0.2s;
    }
    .nav-btn:hover { border-color: var(--accent); color: var(--accent); }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU */
    .main-content { padding: 60px 50px 100px 50px; max-width: 1200px; margin: 0 auto; }
    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 26px; margin-bottom: 35px; border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 18px; margin: 25px 0 15px 0; color: var(--accent); border-bottom: 1px solid var(--border); padding-bottom: 5px; }

    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 10px; padding: 30px; margin-bottom: 30px; }

    /* LAYOUT RECHERCHE */
    .research-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 25px; align-items: start; margin-bottom: 30px; }
    .pdf-mini { width: 100%; height: 500px; border-radius: 8px; border: 1px solid var(--border); background: #000; }
    .image-gallery { display: flex; flex-direction: column; gap: 15px; }
    .image-gallery img { 
      width: 100%; border-radius: 6px; border: 1px solid var(--border); 
      background: #0f172a; min-height: 100px; /* Zone visible même si image absente */
    }

    /* ARTICLE LINK BLOCK */
    .article-box {
      display: flex; gap: 20px; background: rgba(15, 23, 42, 0.5); padding: 20px; 
      border-radius: 8px; border: 1px solid var(--accent); text-decoration: none; 
      color: inherit; transition: 0.3s; align-items: center;
    }
    .article-box:hover { background: rgba(56, 189, 248, 0.1); transform: translateY(-2px); }
    .article-thumb { width: 150px; height: 100px; object-fit: cover; border-radius: 4px; background: #334155; flex-shrink: 0; }
    .article-text h4 { color: var(--accent); margin-bottom: 8px; font-size: 16px; }
    .article-text p { font-size: 13px; color: var(--text-dim); line-height: 1.4; }

    /* SKILLS TAGS */
    .skill-tag-container { display: flex; flex-wrap: wrap; gap: 10px; }
    .skill-tag { background: var(--bg-dark); border: 1px solid var(--accent); padding: 6px 14px; border-radius: 20px; font-size: 13px; }

    @media (max-width: 1024px) {
      body { padding-left: 0; }
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { padding: 30px 20px; }
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
    <div class="sidebar-footer" style="margin-top:auto;">
      <p style="font-size: 11px; color: var(--text-dim); margin-bottom: 15px;">✉️ decroix.nicolasfrancois@gmail.com</p>
      <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="linkedin-link" style="display: inline-block; text-decoration: none; color: var(--accent); font-size: 13px; font-weight: bold; border: 1px solid var(--accent); padding: 6px 12px; border-radius: 4px;">LinkedIn ↗</a>
    </div>
  </aside>

  <main class="main-content">
    
    <div id="exps" class="tab-pane active">
      <h2>Parcours Professionnel & Stages</h2>
      <div class="card">
        <div style="display:flex; justify-content:space-between; align-items:baseline;">
          <span style="font-weight:700; color:var(--accent); font-size:18px;">Student Assistant to the Secretary General</span>
          <span style="font-size:11px; color:var(--text-dim); font-weight:bold;">Nov. 2024 — Présent</span>
        </div>
        <span style="color:var(--text-main); font-weight:600; margin-bottom:15px; display:block;">ERUA - Université Paris-VIII</span>
        <ul>
          <li>Analyse de documents stratégiques européens.</li>
          <li>Appui à la gouvernance de l'alliance universitaire.</li>
          <li>Environnement de travail bilingue Anglais/Français.</li>
        </ul>
      </div>

      <div class="card">
        <div style="display:flex; justify-content:space-between; align-items:baseline;">
          <span style="font-weight:700; color:var(--accent); font-size:18px;">Stagiaire Recherche</span>
          <span style="font-size:11px; color:var(--text-dim); font-weight:bold;">2023</span>
        </div>
        <span style="color:var(--text-main); font-weight:600; margin-bottom:15px; display:block;">CNRS - Equipex MATRICE</span>
        <p style="font-size:14px; color:var(--text-dim);">Traitement de données sensibles liées aux programmes de mémoire traumatique (13-Novembre).</p>
      </div>
    </div>

    <div id="projets" class="tab-pane">
      <h2>Recherche Académique & Projets</h2>
      
      <div class="card">
        <h3>Mémoire de Recherche (Master 1)</h3>
        <p style="margin-bottom: 20px; font-size: 15px;">
            <strong>Thématique :</strong> Militarisation de la frontière russo-polonaise et enjeux de l'exclave de Kaliningrad. 
            <span style="color:var(--accent); font-weight:bold;">Note : 17/20</span>
        </p>
        
        <div class="research-grid">
          <iframe class="pdf-mini" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          
          <div class="image-gallery">
            <img src="Carte-nationale.png" alt="[Image de la carte nationale de Kaliningrad]" onerror="this.src='https://via.placeholder.com/400x250/1e293b/38bdf8?text=Image+non+trouvée:+Carte-nationale.png'">
            <img src="Carte-Region.png" alt="[Image de la carte régionale de Kaliningrad]" onerror="this.src='https://via.placeholder.com/400x250/1e293b/38bdf8?text=Image+non+trouvée:+Carte-Region.png'">
            <p style="font-size:11px; color:var(--text-dim); text-align:center; font-style:italic;">Cartographies réalisées via QGIS et Adobe Illustrator</p>
          </div>
        </div>

        <h3>Terrain & Coopération Internationale</h3>
        <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="article-box">
            <img src="preview-uwm.jpg" class="article-thumb" alt="Visite Olsztyn" onerror="this.src='https://via.placeholder.com/150x100/1e293b/38bdf8?text=Article+Logo'">
            <div class="article-text">
                <h4>Wizyta naukowa studenta z Francji (UWM Olsztyn)</h4>
                <p><strong>Traduction :</strong> "Visite scientifique d'un étudiant français".</p>
                <p>Article de l'Université de Warmie et Mazurie relatant ma visite de recherche et mes échanges avec les instances académiques polonaises sur la sécurité frontalière.</p>
            </div>
        </a>
      </div>

      <div class="card">
        <h3>Autres Engagements</h3>
        <ul style="list-style: none;">
            <li style="margin-bottom: 15px; padding-left: 15px; border-left: 2px solid var(--accent);">
                <strong>Séminaire Université de Varsovie (2025)</strong><br>
                <span style="font-size: 13px; color:var(--text-dim);">Présentation d'ouvrage géopolitique à l'Office Français.</span>
            </li>
            <li style="padding-left: 15px; border-left: 2px solid var(--accent);">
                <strong>666 Albums Metal (Éd. Nouveau Monde)</strong><br>
                <span style="font-size: 13px; color:var(--text-dim);">Rédaction d'une chronique d'album pour l'encyclopédie musicale.</span>
            </li>
        </ul>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Expertises</h2>
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
        <div style="display:grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap:15px;">
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong style="display:block;">Français</strong><span style="color:var(--accent); font-size:11px;">Maternel</span>
          </div>
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong style="display:block;">Anglais</strong><span style="color:var(--accent); font-size:11px;">C2 (Bilingue)</span>
          </div>
          <div style="background:var(--bg-dark); padding:15px; border-radius:8px; text-align:center; border:1px solid var(--border);">
            <strong style="display:block;">Polonais</strong><span style="color:var(--accent); font-size:11px;">B1-B2</span>
          </div>
        </div>
      </div>
    </div>

    <div id="formation" class="tab-pane">
      <h2>Parcours Académique</h2>
      <div class="card">
        <p><strong>Master Géopolitique</strong> | Institut Français de Géopolitique (Paris-VIII)</p>
        <p style="font-size:13px; color:var(--text-dim);">Spécialisation : Nouveaux Acteurs de la Compétition Stratégique.</p>
      </div>
      <div class="card">
        <p><strong>Double Licence Histoire & Géographie</strong> | Université Lyon-III</p>
        <p style="font-size:13px; color:var(--text-dim);">Mention Bien pour les deux cursus.</p>
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
