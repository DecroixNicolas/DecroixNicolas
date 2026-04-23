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
      /* On décale tout le corps de la page pour laisser la place à la sidebar */
      padding-left: var(--sidebar-width); 
      min-height: 100vh;
    }

    /* SIDEBAR FIXE À GAUCHE */
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
    .linkedin-link:hover { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU PRINCIPAL - DÉFILEMENT GLOBAL */
    .main-content {
      padding: 60px 50px 100px 50px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }

    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 26px; margin-bottom: 35px; border-left: 4px solid var(--accent); padding-left: 15px; color: var(--text-main); }

    /* CARTES */
    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 30px;
      margin-bottom: 30px;
    }

    .exp-header { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 10px; }
    .exp-title { font-weight: 700; color: var(--accent); font-size: 19px; }
    .exp-date { font-size: 11px; color: var(--text-dim); font-weight: bold; text-transform: uppercase; }
    .exp-org { color: var(--text-main); font-size: 16px; font-weight: 600; margin-bottom: 15px; display: block; }

    ul { margin-left: 20px; color: var(--text-dim); font-size: 14.5px; }
    li { margin-bottom: 10px; }

    /* LANGUES */
    .lang-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 12px; margin-top: 15px; }
    .lang-badge { background: var(--bg-dark); border: 1px solid var(--border); padding: 12px; border-radius: 6px; text-align: center; }
    .lang-level { color: var(--accent); font-weight: bold; font-size: 12px; display: block; }

    /* SECTION MÉMOIRE */
    .pdf-frame { width: 100%; height: 800px; border-radius: 8px; border: 1px solid var(--border); background: #000; margin-bottom: 30px;}
    .image-gallery { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
      gap: 20px; 
    }
    .image-gallery img { width: 100%; border-radius: 6px; border: 1px solid var(--border); box-shadow: 0 4px 15px rgba(0,0,0,0.3); }

    /* RESPONSIVE */
    @media (max-width: 1024px) {
      body { padding-left: 0; }
      .sidebar { width: 100%; height: auto; position: relative; border-right: none; border-bottom: 1px solid var(--border); }
      .main-content { padding: 30px 20px; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <div class="status">Analyste Géopolitique & Défense</div>
    
    <nav>
      <button class="nav-btn active" onclick="switchTab('exps')">💼 Parcours & Stages</button>
      <button class="nav-btn" onclick="switchTab('recherche')">📚 Mémoire & Cartes</button>
      <button class="nav-btn" onclick="switchTab('skills')">🛠 Compétences & Pubs</button>
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
        <div class="exp-header">
          <span class="exp-title">Student Assistant to the Secretary General</span>
          <span class="exp-date">Nov. 2024 — Déc. 2025</span>
        </div>
        <span class="exp-org">European Reform Universities Alliance (ERUA) - Paris-VIII</span>
        <ul>
          <li>Rapports analytiques de documents européens sur l'éducation pour la secrétaire générale.</li>
          <li>Création de présentations et d'ateliers de comité de pilotage.</li>
          <li>Analyse d'assurance qualité et d'impact de l'alliance.</li>
          <li>Organisation et vérification de conformité sur les bases de données collaboratives.</li>
          <li>Productions réalisées intégralement en anglais pour les partenaires européens.</li>
          <li>Veille sur les évènements européens du secteur de l'éducation.</li>
        </ul>
      </div>

      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Stagiaire Recherche (Programme 13-Novembre)</span>
          <span class="exp-date">Juillet — Août 2023</span>
        </div>
        <span class="exp-org">CNRS - Equipex MATRICE</span>
        <ul>
          <li>Transcription de témoignages de victimes des attentats de 2015 en France et de déportés français.</li>
          <li>Suivi rigoureux du vade-mecum de transcription.</li>
          <li>Respect strict des protocoles et de la clause de confidentialité.</li>
        </ul>
      </div>

      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Stagiaire au service Urbanisme</span>
          <span class="exp-date">Juillet — Août 2022</span>
        </div>
        <span class="exp-org">Mairie de Caluire-et-Cuire</span>
        <ul>
          <li>Travail de recherche pour l'implantation de mode de production d'énergie solaire sur la ville.</li>
          <li>Rédaction de notes et rapports à destination du maire.</li>
          <li>Utilisation intensive de SIG : <strong>ArcGIS, QGIS</strong>.</li>
        </ul>
      </div>
    </div>

    <div id="recherche" class="tab-pane">
      <h2>Mémoire de Recherche M1</h2>
      <div class="card">
        <p style="margin-bottom: 25px;"><strong>Sujet :</strong> La militarisation de la frontière russo-polonaise avec Kaliningrad (Note : 17/20).</p>
        
        <iframe class="pdf-frame" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
        
        <h3 style="color:var(--accent); margin-bottom:20px; font-size:18px;">Extraits Cartographiques (SIG)</h3>
        <div class="image-gallery">
          <img src="Carte-nationale.png" alt="Carte 1">
          <img src="Carte-Region.png" alt="Carte 2">
          <img src="Carte-Varmie.png" alt="Carte 3">
        </div>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Compétences & Publications</h2>
      
      <div class="card">
        <h3 style="color:var(--accent); margin-bottom:15px;">Maîtrise des Langues</h3>
        <div class="lang-grid">
          <div class="lang-badge">Français<span class="lang-level">Maternel</span></div>
          <div class="lang-badge">Anglais<span class="lang-level">C2 (Bilingue)</span></div>
          <div class="lang-badge">Polonais<span class="lang-level">B1-B2</span></div>
          <div class="lang-badge">Espagnol<span class="lang-level">B1</span></div>
        </div>
      </div>

      <div class="card">
        <h3 style="color:var(--accent); margin-bottom:15px;">Expertises Techniques</h3>
        <ul>
          <li>Analyse géopolitique et Veille OSINT.</li>
          <li>Cartographie : <strong>QGIS</strong> et <strong>Adobe Illustrator</strong>.</li>
          <li>Systèmes d'Information Géographique : <strong>ArcGIS</strong>.</li>
          <li>Maîtrise experte de la Suite Office.</li>
        </ul>
      </div>

      <div class="card">
        <h3 style="color:var(--accent); margin-bottom:15px;">Publications & Engagements</h3>
        <ul>
          <li><strong>Diploweb.com</strong> : Rédaction d'un article de géopolitique (dir. P. Verluise, 2025).</li>
          <li><strong>Université de Varsovie</strong> : Présentation lors du séminaire de l'Office Français (2025).</li>
          <li><strong>666 Albums Metal</strong> : Rédaction d'une chronique pour l'encyclopédie (Nouveau Monde).</li>
        </ul>
      </div>
    </div>

    <div id="formation" class="tab-pane">
      <h2>Cursus Académique</h2>
      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Master de Géopolitique</span>
          <span class="exp-date">2024 — 2026</span>
        </div>
        <span class="exp-org">IFG - Université Paris-VIII</span>
        <p style="font-size:14px; color:var(--text-dim);">Spécialisation : Nouveaux Acteurs de la Compétition Stratégique.</p>
      </div>
      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Double Licence Histoire / Géographie</span>
          <span class="exp-date">2021 — 2024</span>
        </div>
        <span class="exp-org">Université Jean Moulin Lyon-III</span>
        <p style="font-size:14px; color:var(--text-dim);">Mention Bien pour les deux licences.</p>
      </div>
    </div>

  </main>

  <script>
    function switchTab(tabId) {
      // Masquer tous les onglets
      document.querySelectorAll('.tab-pane').forEach(p => p.classList.remove('active'));
      // Désactiver tous les boutons
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));

      // Afficher l'onglet cible
      const target = document.getElementById(tabId);
      if(target) target.classList.add('active');
      
      // Activer le bouton correspondant
      const activeBtn = Array.from(document.querySelectorAll('.nav-btn'))
                             .find(b => b.getAttribute('onclick').includes(tabId));
      if (activeBtn) activeBtn.classList.add('active');

      // Remonter en haut de la page lors du changement
      window.scrollTo(0, 0);
    }
  </script>

</body>
</html>
