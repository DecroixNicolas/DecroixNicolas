<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio</title>
  <style>
    :root {
      --bg: #0f172a; --card: #1e293b; --accent: #38bdf8;
      --text: #f1f5f9; --dim: #94a3b8; --border: #334155;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Inter', system-ui, sans-serif; background: var(--bg); color: var(--text); line-height: 1.6; padding-top: 70px; }
    
    header { position: fixed; top: 0; width: 100%; height: 70px; background: var(--card); border-bottom: 1px solid var(--border); z-index: 1000; display: flex; justify-content: center; }
    nav { display: flex; gap: 10px; overflow-x: auto; padding: 0 15px; align-items: center; scrollbar-width: none; }
    .nav-btn { padding: 8px 16px; color: var(--dim); background: none; border: 1px solid transparent; border-radius: 20px; font-weight: 600; cursor: pointer; white-space: nowrap; transition: 0.3s; }
    .nav-btn.active { background: var(--accent); color: var(--bg); }

    main { max-width: 900px; margin: 0 auto; padding: 20px; }
    .tab-pane { display: none; animation: fadeIn 0.4s ease; }
    .tab-pane.active { display: block; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 20px; }
    h2 { color: var(--accent); margin-bottom: 20px; font-size: 22px; border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 19px; margin-bottom: 5px; }
    .date { color: var(--accent); font-size: 13px; font-weight: bold; display: block; margin-bottom: 10px; }
    ul { margin-left: 20px; font-size: 15px; color: var(--text); }
    li { margin-bottom: 8px; }

    .pdf-box { width: 100%; height: 600px; border-radius: 8px; border: 1px solid var(--border); margin: 20px 0; }
    .img-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; margin-top: 20px; }
    .img-card { position: relative; border-radius: 10px; overflow: hidden; border: 1px solid var(--border); transition: 0.3s; }
    .img-card:hover { border-color: var(--accent); transform: scale(1.02); }
    .img-card img { width: 100%; height: 200px; object-fit: cover; display: block; }
    .img-label { position: absolute; bottom: 0; width: 100%; background: rgba(0,0,0,0.8); padding: 8px; text-align: center; font-size: 12px; }

    .skill-badge { display: inline-block; padding: 10px 20px; border: 1px solid var(--accent); border-radius: 8px; margin: 5px; font-weight: bold; }
  </style>
</head>
<body>
  <header><nav id="menu"></nav></header>
  <main id="content"></main>

  <script>
    const data = {
      home: `
        <div class="card" style="text-align:center; padding:50px 20px;">
          <h1 style="font-size:36px; color:var(--accent)">Nicolas Decroix</h1>
          <p style="font-size:20px; color:var(--dim); margin-bottom:20px;">Analyste en Géopolitique & Nouveaux Acteurs</p>
          <p style="text-align:justify; max-width:700px; margin:0 auto;">Étudiant à l'Institut Français de Géopolitique (Paris-VIII), je me spécialise dans la sécurité de l'espace OTAN en Europe Centrale et Orientale. Mon travail porte sur la militarisation du Flanc Est et les enjeux de défense face à la Russie.</p>
          <div style="margin-top:30px;">
            <a href="mailto:decroix.nicolasfrancois@gmail.com" style="color:var(--accent); text-decoration:none; margin:0 10px; font-weight:bold;">Email</a>
            <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" style="color:var(--accent); text-decoration:none; margin:0 10px; font-weight:bold;">LinkedIn</a>
          </div>
        </div>`,
      parcours: `
        <h2>Formation Académique</h2>
        <div class="card">
          <h3>Master Géopolitique</h3>
          <span class="date">2024 — 2026 | IFG (Paris-VIII)</span>
        </div>
        <div class="card">
          <h3>Double Licence Histoire-Géographie</h3>
          <span class="date">2021 — 2024 | Lyon-III (Mention Bien)</span>
        </div>
        <h2>Expériences Professionnelles</h2>
        <div class="card">
          <h3>Assistant auprès de la Secrétaire Générale</h3>
          <span class="date">Nov. 2024 — Présent | ERUA</span>
          <ul>
            <li>Rapports analytiques sur les politiques européennes d'éducation.</li>
            <li>Ateliers de comité de pilotage et présentations stratégiques.</li>
            <li>Analyse assurance qualité et conformité bases de données.</li>
            <li>Travail intégralement en anglais.</li>
            <li>Veille évènementielle européenne.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Stagiaire Recherche - Programme 13-Novembre</h3>
          <span class="date">2023 | CNRS - MATRICE</span>
          <ul>
            <li>Transcription de témoignages (Attentats 2015 / Déportés).</li>
            <li>Suivi du vade-mecum de transcription scientifique.</li>
            <li>Haute confidentialité.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Stagiaire Urbanisme</h3>
          <span class="date">2022 | Mairie de Caluire</span>
          <ul>
            <li>Implantation énergie solaire.</li>
            <li>Notes stratégiques pour Monsieur le Maire.</li>
            <li>Utilisation de ArcGIS et QGIS.</li>
          </ul>
        </div>`,
      recherche: `
        <h2>Recherche & Mémoire</h2>
        <div class="card">
          <h3>Mémoire de M1 (Note : 17/20)</h3>
          <p>Militarisation de la frontière russo-polonaise.</p>
          <div style="background:rgba(56,189,248,0.1); padding:15px; border-radius:8px; margin:15px 0; border:1px dashed var(--accent);">
            <p style="font-size:14px; margin-bottom:10px;">📄 <b>Terrain :</b> Visite scientifique à Olsztyn (Pologne).</p>
            <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" style="background:var(--accent); color:var(--bg); padding:8px 15px; border-radius:5px; text-decoration:none; font-weight:bold; font-size:13px;">Article Officiel ↗</a>
          </div>
          <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          <div class="img-grid">
            <div class="img-card"><img src="carte-nationale.png" onerror="this.src='https://via.placeholder.com/400x250'"><div class="img-label">Échelle Nationale</div></div>
            <div class="img-card"><img src="Carte-Région.png" onerror="this.src='https://via.placeholder.com/400x250'"><div class="img-label">Échelle Régionale</div></div>
            <div class="img-card"><img src="Carte-Varmie.png" onerror="this.src='https://via.placeholder.com/400x250'"><div class="img-label">Échelle Locale</div></div>
          </div>
        </div>`,
      travaux: `
        <h2>Projets en cours</h2>
        <div class="card"><h3>Mémoire M2</h3><p>Infrastructures de défense sur le corridor de Suwałki.</p></div>
        <div class="card"><h3>Veille OSINT</h3><p>Fortifications frontalières par imagerie satellite.</p></div>`,
      skills: `
        <h2>Compétences</h2>
        <div class="card" style="text-align:center;">
          <div class="skill-badge">SIG (QGIS/ArcGIS)</div>
          <div class="skill-badge">Analyse Géopolitique</div>
          <div class="skill-badge">OSINT</div>
          <div class="skill-badge">Adobe Illustrator</div>
        </div>
        <h2>Langues</h2>
        <div class="card">
          <p><b>Français :</b> Maternel</p>
          <p><b>Anglais :</b> C2 (Bilingue)</p>
          <p><b>Polonais :</b> B1-B2</p>
          <p><b>Espagnol :</b> B1</p>
        </div>`
    };

    function switchTab(id) {
      document.querySelectorAll('.nav-btn').forEach(b
