<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Analyste Géopolitique</title>
  <style>
    /* THÈME SOBRE ET PROFESSIONNEL */
    :root {
      --bg-body: #f8fafc;        /* Gris très clair */
      --sidebar-bg: #0f172a;    /* Bleu nuit profond */
      --sidebar-text: #94a3b8;
      --accent-main: #334155;    /* Gris ardoise (au lieu du bleu/rose) */
      --text-dark: #1e293b;
      --text-muted: #475569;
      --border: #e2e8f0;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: "Inter", -apple-system, sans-serif;
      background-color: var(--bg-body);
      color: var(--text-dark);
      line-height: 1.5;
      overflow: hidden; /* Fixe la page pour l'effet dashboard */
    }

    /* MENU LATÉRAL */
    .sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: 280px;
      height: 100%;
      background: var(--sidebar-bg);
      color: white;
      padding: 40px 20px;
      z-index: 100;
    }

    .sidebar h1 { font-size: 22px; margin-bottom: 5px; color: white; }
    .sidebar p { font-size: 12px; color: #38bdf8; text-transform: uppercase; margin-bottom: 40px; letter-spacing: 1px; }

    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px 15px;
      margin-bottom: 8px;
      color: var(--sidebar-text);
      background: transparent;
      border: none;
      border-radius: 6px;
      text-align: left;
      font-size: 14px;
      font-weight: 500;
      cursor: pointer;
      transition: 0.2s;
    }
    .nav-btn.active { background: #1e293b; color: white; }
    .nav-btn:hover { color: white; }

    /* ZONE PRINCIPALE */
    .main-content {
      margin-left: 280px;
      height: 100vh;
      padding: 40px;
      overflow-y: auto;
    }

    .tab-content { display: none; animation: fadeIn 0.3s ease; }
    .tab-content.active { display: block; }

    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 20px; color: var(--text-dark); margin-bottom: 25px; border-bottom: 2px solid var(--border); padding-bottom: 10px; }

    /* CARTES D'EXPÉRIENCE */
    .card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 20px;
      margin-bottom: 20px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    }

    .card-header { display: flex; justify-content: space-between; margin-bottom: 10px; }
    .job-title { font-weight: 700; color: var(--text-dark); font-size: 16px; }
    .job-date { font-size: 12px; color: var(--text-muted); font-weight: 600; }
    .job-org { color: var(--text-muted); font-size: 14px; font-style: italic; margin-bottom: 10px; display: block; }

    ul { margin-left: 20px; color: var(--text-muted); font-size: 13.5px; }
    li { margin-bottom: 5px; }

    /* LISTE LANGUES */
    .lang-list { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 10px; }
    .lang-box { border: 1px solid var(--border); padding: 10px; border-radius: 4px; text-align: center; background: white; font-size: 13px; }

    /* IFRAME MÉMOIRE */
    .pdf-viewer { width: 100%; height: 75vh; border: 1px solid var(--border); border-radius: 4px; }

    @media (max-width: 1024px) {
      .sidebar { width: 100%; height: auto; position: relative; padding: 20px; }
      .main-content { margin-left: 0; padding: 20px; height: auto; overflow: visible; }
      body { overflow-y: auto; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <p>Analyste Géopolitique</p>
    
    <nav>
      <button class="nav-btn active" onclick="showTab(event, 'experience')">💼 Expériences & Stages</button>
      <button class="nav-btn" onclick="showTab(event, 'education')">🎓 Formation</button>
      <button class="nav-btn" onclick="showTab(event, 'skills')">🛠 Compétences</button>
      <button class="nav-btn" onclick="showTab(event, 'research')">📚 Recherche (M1)</button>
    </nav>

    <div style="position: absolute; bottom: 20px; font-size: 11px; color: var(--sidebar-text);">
      📍 Paris, France<br>
      📧 decroix.nicolasfrancois@gmail.com
    </div>
  </aside>

  <main class="main-content">
    
    <div id="experience" class="tab-content active">
      <h2>Parcours Professionnel</h2>
      
      <div class="card">
        <div class="card-header">
          <span class="job-title">Student Assistant to the Secretary General</span>
          <span class="job-date">2024 — 2025</span>
        </div>
        <span class="job-org">European Reform Universities Alliance (ERUA) - Paris-VIII</span>
        <ul>
          <li>Analyses stratégiques de documents européens sur l'éducation.</li>
          <li>Conception de supports pour comités de pilotage et ateliers.</li>
          <li>Analyses d'impact et d'assurance qualité de l'alliance.</li>
          <li>Travail intégral en anglais (C2) pour un environnement international.</li>
        </ul>
      </div>

      <div class="card">
        <div class="card-header">
          <span class="job-title">Stagiaire Recherche (Programme 13-Novembre)</span>
          <span class="job-date">ÉTÉ 2023</span>
        </div>
        <span class="job-org">CNRS - Equipex MATRICE</span>
        <ul>
          <li>Transcription de témoignages (attentats de 2015 / déportés).</li>
          <li>Traitement rigoureux de données sensibles sous clause de confidentialité.</li>
        </ul>
      </div>

      <div class="card">
        <div class="card-header">
          <span class="job-title">Stagiaire Urbanisme & Énergie</span>
          <span class="job-date">ÉTÉ 2022</span>
        </div>
        <span class="job-org">Mairie de Caluire-et-Cuire</span>
        <ul>
          <li>Étude d'implantation de production d'énergie solaire.</li>
          <li>Maîtrise opérationnelle des SIG : <strong>ArcGIS, QGIS</strong>.</li>
          <li>Rédaction de notes de synthèse pour l'exécutif local.</li>
        </ul>
      </div>
    </div>

    <div id="education" class="tab-content">
      <h2>Formation Académique</h2>
      <div class="card">
        <span class="job-date">2024 — 2026</span>
        <p><strong>Master de Géopolitique</strong> - Institut Français de Géopolitique (IFG)</p>
        <p style="font-size: 13px; color: var(--text-muted)">Spécialisation Nouveaux Acteurs de la Compétition Stratégique.</p>
      </div>
      <div class="card">
        <span class="job-date">2021 — 2024</span>
        <p><strong>Double Licence Histoire / Géographie</strong> - Université Lyon-III</p>
        <p style="font-size: 13px; color: var(--text-muted)">Mention Bien pour les deux cursus.</p>
      </div>
    </div>

    <div id="skills" class="tab-content">
      <h2>Compétences Techniques & Linguistiques</h2>
      <div class="card">
        <h3 style="font-size: 14px; margin-bottom: 15px;">Langues Étrangères</h3>
        <div class="lang-list">
          <div class="lang-box"><strong>Français</strong> (Maternel)</div>
          <div class="lang-box"><strong>Anglais</strong> (C2)</div>
          <div class="lang-box"><strong>Polonais</strong> (B1-B2)</div>
          <div class="lang-box"><strong>Espagnol</strong> (B1)</div>
        </div>
      </div>
      <div class="card">
        <h3 style="font-size: 14px; margin-bottom: 10px;">Expertises</h3>
        <ul>
          <li>Cartographie & SIG : QGIS, ArcGIS, Adobe Illustrator.</li>
          <li>Veille informationnelle & OSINT.</li>
          <li>Analyse de risques géopolitiques.</li>
        </ul>
      </div>
    </div>

    <div id="research" class="tab-content">
      <h2>Travaux de Recherche</h2>
      <div class="card">
        <p style="margin-bottom: 15px;"><strong>Mémoire M1 :</strong> La militarisation de la frontière russo-polonaise avec Kaliningrad (Note : 17/20).</p>
        <iframe class="pdf-viewer" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
      </div>
    </div>

  </main>

  <script>
    function showTab(evt, tabId) {
      document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      document.getElementById(tabId).classList.add('active');
      evt.currentTarget.classList.add('active');
    }
  </script>

</body>
</html>
