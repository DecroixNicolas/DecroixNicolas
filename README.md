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
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      overflow: hidden; /* Important pour garder le menu fixe */
    }

    /* BARRE LATÉRALE FIXE */
    .sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: 280px;
      height: 100vh;
      background: var(--sidebar-bg);
      padding: 40px 20px;
      border-right: 1px solid var(--border);
      z-index: 100;
    }

    .sidebar h1 { font-size: 20px; color: var(--accent); margin-bottom: 5px; }
    .sidebar .status { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--text-dim); margin-bottom: 40px; }

    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px 15px;
      margin-bottom: 10px;
      color: var(--text-dim);
      background: rgba(255,255,255,0.05);
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

    /* ZONE DE CONTENU PRINCIPAL */
    .main-content {
      margin-left: 280px; /* Aligné sur la largeur de la sidebar */
      height: 100vh;
      overflow-y: auto;
      padding: 40px 40px 100px 40px; /* 100px en bas pour l'espace de lecture */
    }

    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    h2 { font-size: 24px; margin-bottom: 30px; border-left: 4px solid var(--accent); padding-left: 15px; color: var(--text-main); }

    /* CARTES D'EXPÉRIENCE (TEXTE INTÉGRAL CV) */
    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 25px;
      margin-bottom: 25px;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }

    .exp-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 10px; }
    .exp-title { font-weight: 700; color: var(--accent); font-size: 18px; }
    .exp-date { font-size: 12px; color: var(--text-dim); font-weight: bold; background: rgba(0,0,0,0.2); padding: 4px 8px; border-radius: 4px; }
    .exp-org { color: var(--text-main); font-size: 15px; font-weight: 600; margin-bottom: 15px; display: block; }

    ul { margin-left: 20px; color: var(--text-dim); font-size: 14px; }
    li { margin-bottom: 8px; }

    /* SECTION MÉMOIRE & IMAGES */
    .memory-layout { display: flex; flex-direction: column; gap: 20px; }
    .pdf-frame { width: 100%; height: 600px; border-radius: 8px; border: 1px solid var(--border); }
    .image-gallery { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); 
      gap: 15px; 
      margin-top: 10px;
    }
    .image-gallery div { border: 1px solid var(--border); border-radius: 8px; background: #000; overflow: hidden; }
    .image-gallery img { width: 100%; height: auto; display: block; opacity: 0.8; transition: 0.3s; }
    .image-gallery img:hover { opacity: 1; }

    /* BAS DE PAGE / ESPACE SUPPLÉMENTAIRE */
    .spacer { height: 100px; width: 100%; }

    @media (max-width: 1024px) {
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { margin-left: 0; padding: 20px; height: auto; overflow: visible; }
      body { overflow-y: auto; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <div class="status">Analyste Géopolitique & Défense</div>
    
    <nav id="mainNav">
      <button class="nav-btn active" onclick="switchTab('exps')">💼 Parcours & Stages</button>
      <button class="nav-btn" onclick="switchTab('recherche')">📚 Mémoire & Cartes</button>
      <button class="nav-btn" onclick="switchTab('skills')">🛠 Compétences</button>
      <button class="nav-btn" onclick="switchTab('formation')">🎓 Formation</button>
    </nav>

    <div style="position: absolute; bottom: 30px; font-size: 12px; color: var(--text-dim);">
      📍 Paris, France<br>
      ✉️ decroix.nicolasfrancois@gmail.com
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
          <li>Rapports analytiques de documents européens sur l’éducation pour la secrétaire générale.</li>
          <li>Création de présentations et d’ateliers de comité de pilotage.</li>
          <li>Analyse d’assurance qualité et d’impact de l’alliance.</li>
          <li>Organisation et vérification de conformité sur les bases de données collaboratives.</li>
          <li>Réunions et productions réalisées intégralement en anglais pour les partenaires européens.</li>
          <li>Veille sur les évènements européens du secteur de l’éducation.</li>
        </ul>
      </div>

      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Stagiaire Recherche - Programme 13-Novembre</span>
          <span class="exp-date">Juillet — Août 2023</span>
        </div>
        <span class="exp-org">CNRS - Equipex MATRICE</span>
        <ul>
          <li>Transcription de témoignages de victimes des attentats de 2015 et de déportés français.</li>
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
          <li>Recherche pour l'implantation de mode de production d'énergie solaire sur la ville.</li>
          <li>Rédaction de notes et rapports à destination du maire.</li>
          <li>Utilisation de SIG : ArcGIS, QGIS.</li>
        </ul>
      </div>
      <div class="spacer"></div>
    </div>

    <div id="recherche" class="tab-pane">
      <h2>Travaux de Recherche</h2>
      <div class="card">
        <p style="margin-bottom: 20px;"><strong>Mémoire de M1 :</strong> La militarisation de la frontière russo-polonaise avec Kaliningrad (Note : 17/20).</p>
        
        <div class="memory-layout">
          <iframe class="pdf-frame" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          
          <h3 style="font-size:16px; color:var(--accent); margin-top:20px;">Cartographie & SIG</h3>
          <div class="image-gallery">
            <div><img src="carte1.jpg" alt="Carte Kaliningrad 1"></div>
            <div><img src="carte2.jpg" alt="Carte Kaliningrad 2"></div>
            <div><img src="carte3.jpg" alt="Carte Kaliningrad 3"></div>
          </div>
        </div>
      </div>
      <div class="spacer"></div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Compétences & Langues</h2>
      <div class="card">
        <h3 style="color:var(--accent); margin-bottom:15px;">Langues</h3>
        <ul>
          <li><strong>Français :</strong> Maternel</li>
          <li><strong>Anglais :</strong> C2 (Bilingue)</li>
          <li><strong>Polonais :</strong> B1-B2</li>
          <li><strong>Espagnol :</strong> B1</li>
        </ul>
      </div>
      <div class="card">
        <h3 style="color:var(--accent); margin-bottom:15px;">Expertises Techniques</h3>
        <ul>
          <li>Analyse géopolitique et Veille OSINT</li>
          <li>Cartographie : QGIS et Adobe Illustrator</li>
          <li>Systèmes d'Information Géographique : ArcGIS</li>
          <li>Maîtrise experte de la Suite Office</li>
        </ul>
      </div>
      <div class="spacer"></div>
    </div>

    <div id="formation" class="tab-pane">
      <h2>Cursus Académique</h2>
      <div class="card">
        <p><strong>2024-2026 :</strong> Master de Géopolitique (IFG - Paris-VIII). Spécialisation Nouveaux Acteurs.</p>
      </div>
      <div class="card">
        <p><strong>2021-2024 :</strong> Double licence Histoire / Géographie (Lyon-III). Mention Bien.</p>
      </div>
      <div class="card">
        <p><strong>2020-2021 :</strong> Baccalauréat Mention Très Bien (Les Chartreux, Lyon).</p>
      </div>
      <div class="spacer"></div>
    </div>

  </main>

  <script>
    function switchTab(tabId) {
      // 1. Cacher tous les onglets
      const panes = document.querySelectorAll('.tab-pane');
      panes.forEach(p => p.classList.remove('active'));

      // 2. Retirer l'état actif de tous les boutons
      const btns = document.querySelectorAll('.nav-btn');
      btns.forEach(b => b.classList.remove('active'));

      // 3. Afficher le bon onglet
      const targetPane = document.getElementById(tabId);
      if(targetPane) {
        targetPane.classList.add('active');
      }

      // 4. Mettre le bouton cliqué en surbrillance
      // On cherche le bouton qui a l'attribut onclick contenant le nom du tab
      btns.forEach(b => {
        if(b.getAttribute('onclick').includes(tabId)) {
          b.classList.add('active');
        }
      });

      // 5. Remonter tout en haut du contenu lors du changement
      document.querySelector('.main-content').scrollTop = 0;
    }
  </script>

</body>
</html>
