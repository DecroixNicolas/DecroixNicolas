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
      --nav-height: 65px;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      padding-top: var(--nav-height);
    }

    /* NAVIGATION */
    header {
      position: fixed; top: 0; width: 100%; height: var(--nav-height);
      background: var(--card-bg); border-bottom: 1px solid var(--border);
      z-index: 1000; display: flex; align-items: center; justify-content: center;
    }
    nav { display: flex; gap: 8px; overflow-x: auto; padding: 0 10px; scrollbar-width: none; }
    nav::-webkit-scrollbar { display: none; }
    .nav-btn {
      padding: 8px 15px; color: var(--text-dim); background: transparent;
      border: 1px solid transparent; border-radius: 20px; font-size: 13px;
      font-weight: 600; cursor: pointer; white-space: nowrap; transition: 0.3s;
    }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU */
    main { max-width: 900px; margin: 0 auto; padding: 25px 20px; }
    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; }
    h2 { font-size: 22px; margin-bottom: 20px; color: var(--accent); border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 18px; margin-bottom: 10px; color: var(--text-main); }
    .date { font-size: 13px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 10px; }

    /* IMAGES CLIQUABLES */
    .image-gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-top: 20px; }
    .img-container { position: relative; cursor: pointer; overflow: hidden; border-radius: 8px; border: 1px solid var(--border); transition: 0.3s; }
    .img-container:hover { border-color: var(--accent); transform: scale(1.02); }
    .img-container img { width: 100%; display: block; background: #0f172a; }
    .img-label { position: absolute; bottom: 0; width: 100%; background: rgba(0,0,0,0.7); color: white; font-size: 11px; padding: 5px; text-align: center; }

    /* SKILLS GRANDS */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; }
    .skill-card { background: var(--bg-dark); border: 1px solid var(--accent); padding: 20px; border-radius: 10px; text-align: center; font-weight: bold; font-size: 16px; }

    /* LANGUES */
    .lang-item { display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid var(--border); }
    .lang-name { font-weight: 600; }
    .lang-level { color: var(--accent); font-size: 13px; }

    /* PDF */
    .pdf-box { width: 100%; height: 500px; border: 1px solid var(--border); border-radius: 8px; margin: 15px 0; }

    footer { text-align: center; padding: 30px; border-top: 1px solid var(--border); margin-top: 50px; font-size: 14px; }
    .social-link { color: var(--accent); text-decoration: none; margin: 0 10px; font-weight: bold; }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('exps')">Parcours</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Engagements</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
    </nav>
  </header>

  <main>
    <div id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 40px 20px;">
        <h1 style="font-size: 32px; color: var(--accent);">Nicolas Decroix</h1>
        <p style="font-size: 18px; color: var(--text-dim); margin: 10px 0 25px 0;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 700px; margin: 0 auto; color: var(--text-main);">
          Étudiant à l'Institut Français de Géopolitique (Paris-VIII), je me spécialise dans l'analyse des zones de tensions en Europe centrale et orientale. Mon travail se concentre sur les enjeux de militarisation frontalière, la veille OSINT et la cartographie décisionnelle.
        </p>
        <div style="margin-top: 30px;">
            <a href="mailto:decroix.nicolasfrancois@gmail.com" class="social-link">Email</a>
            <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="social-link">LinkedIn</a>
        </div>
      </div>
    </div>

    <div id="exps" class="tab-pane">
      <h2>Expériences Professionnelles</h2>
      <div class="card">
        <h3>Assistant Étudiant auprès de la Secrétaire Générale</h3>
        <span class="date">Nov. 2024 — Présent | ERUA (Université Paris-VIII)</span>
        <ul style="margin-left: 20px; font-size: 14px;">
          <li>Rapports analytiques sur les politiques européennes d'éducation.</li>
          <li>Appui logistique et stratégique aux comités de pilotage.</li>
          <li>Réalisation de présentations et ateliers en anglais.</li>
        </ul>
      </div>
      <div class="card">
        <h3>Stagiaire Recherche - Programme 13-Novembre</h3>
        <span class="date">Juin 2023 — Juillet 2023 | CNRS - MATRICE</span>
        <p style="font-size: 14px;">Transcription et analyse de témoignages dans un cadre de recherche scientifique à haute confidentialité.</p>
      </div>
      <div class="card">
        <h3>Stagiaire Service Urbanisme</h3>
        <span class="date">Juin 2022 — Juillet 2022 | Mairie de Caluire-et-Cuire</span>
        <p style="font-size: 14px;">Étude de faisabilité pour l'implantation d'énergie solaire via les outils SIG (ArcGIS/QGIS).</p>
      </div>
    </div>

    <div id="recherche" class="tab-pane">
      <h2>Recherche Académique & Engagements</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (Note : 17/20)</h3>
        <p style="font-size: 14px; margin-bottom: 10px;"><strong>Sujet :</strong> La militarisation de la frontière russo-polonaise et l'enclave de Kaliningrad.</p>
        
        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>

        <div class="image-gallery">
          <a href="carte-nationale.png" target="_blank" class="img-container">
            <img src="carte-nationale.png" alt="Carte Nationale" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Nationale'">
            <div class="img-label">Échelle Nationale ↗</div>
          </a>
          <a href="Carte-Région.png" target="_blank" class="img-container">
            <img src="Carte-Région.png" alt="Carte Régionale" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Région'">
            <div class="img-label">Échelle Régionale ↗</div>
          </a>
          <a href="Carte-Varmie.png" target="_blank" class="img-container">
            <img src="Carte-Varmie.png" alt="Carte Varmie" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Varmie'">
            <div class="img-label">Échelle Locale (Varmie) ↗</div>
          </a>
        </div>
      </div>

      <div class="card">
        <h3>Terrain & Publications</h3>
        <p style="margin-bottom: 15px; font-size: 14px;">• <strong>Visite scientifique à Olsztyn (Pologne)</strong> : Échanges avec les officiels de l'UWM sur la sécurité frontalière.</p>
        <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" style="color: var(--accent); font-size: 13px; text-decoration: none; border: 1px solid var(--accent); padding: 5px 10px; border-radius: 5px;">Voir l'article officiel ↗</a>
        
        <div style="margin-top: 25px;">
            <p style="font-size: 14px;">• <strong>Séminaire de l'Office Français (Varsovie, 2025)</strong> : Présentation de travaux géopolitiques.</p>
            <p style="font-size: 14px; margin-top: 10px;">• <strong>666 Albums Metal (Éditions du Nouveau Monde)</strong> : Co-auteur de notices encyclopédiques.</p>
        </div>
      </div>
    </div>

    <div id="skills" class="tab-pane">
      <h2>Expertises Techniques</h2>
      <div class="skills-grid" style="margin-bottom: 40px;">
        <div class="skill-card">SIG (QGIS / ArcGIS)</div>
        <div class="skill-card">Analyse Géopolitique</div>
        <div class="skill-tag skill-card">Veille OSINT</div>
        <div class="skill-card">Adobe Illustrator</div>
        <div class="skill-card">Suite Office</div>
      </div>

      <h2>Maîtrise des Langues</h2>
      <div class="card">
        <div class="lang-item"><span class="lang-name">Français</span><span class="lang-level">Maternel</span></div>
        <div class="lang-item"><span class="lang-name">Anglais</span><span class="lang-level">C2 (Bilingue)</span></div>
        <div class="lang-item"><span class="lang-name">Polonais</span><span class="lang-level">B1-B2 (Intermédiaire avancé)</span></div>
        <div class="lang-item" style="border:none;"><span class="lang-name">Espagnol</span><span class="lang-level">B1</span></div>
      </div>

      <h2>Formation</h2>
      <div class="card">
        <p><strong>Master Géopolitique</strong> | Institut Français de Géopolitique | 2024-2026</p>
        <p style="margin-top: 10px;"><strong>Double Licence Hist-Géo</strong> | Lyon-III | 2021-2024 (Mention Bien)</p>
      </div>
    </div>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix - Portfolio Analyste</p>
  </footer>

  <script>
    function switchTab(tabId) {
      document.querySelectorAll('.tab-pane').forEach(p => p.classList.remove('active'));
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      document.getElementById(tabId).classList.add('active');
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(tabId));
      if(btn) btn.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>
</body>
</html>
