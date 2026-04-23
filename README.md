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
      padding-top: var(--nav-height);
    }

    /* NAVIGATION */
    header {
      position: fixed; top: 0; width: 100%; height: var(--nav-height);
      background: var(--card-bg); border-bottom: 1px solid var(--border);
      z-index: 1000; display: flex; align-items: center; justify-content: center;
    }
    nav { display: flex; gap: 10px; overflow-x: auto; padding: 0 15px; scrollbar-width: none; max-width: 900px; width: 100%; }
    nav::-webkit-scrollbar { display: none; }
    
    .nav-btn {
      padding: 10px 20px; color: var(--text-dim); background: transparent;
      border: 1px solid transparent; border-radius: 25px; font-size: 14px;
      font-weight: 600; cursor: pointer; white-space: nowrap; transition: 0.3s;
    }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU */
    main { max-width: 900px; margin: 0 auto; padding: 30px 20px; }
    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease-out; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; }
    h2 { font-size: 26px; margin-bottom: 25px; color: var(--accent); border-left: 5px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 20px; margin-bottom: 10px; color: var(--text-main); }
    .date { font-size: 14px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 15px; }

    /* IMAGES ET CARTES */
    .image-gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin: 25px 0; }
    .img-container { 
      position: relative; cursor: pointer; overflow: hidden; border-radius: 10px; 
      border: 2px solid var(--border); transition: 0.3s; display: block; 
    }
    .img-container:hover { border-color: var(--accent); transform: translateY(-5px); }
    .img-container img { width: 100%; display: block; height: 220px; object-fit: cover; background: #0f172a; }
    .img-label { position: absolute; bottom: 0; width: 100%; background: rgba(15, 23, 42, 0.9); color: white; font-size: 12px; padding: 10px; text-align: center; font-weight: bold; }

    /* COMPÉTENCES */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 30px; }
    .skill-card { 
      background: var(--bg-dark); border: 1px solid var(--accent); padding: 20px; border-radius: 12px; 
      text-align: center; font-weight: bold; font-size: 16px; color: var(--accent);
    }

    .lang-item { display: flex; justify-content: space-between; align-items: center; padding: 12px 0; border-bottom: 1px solid var(--border); }
    .lang-level { color: var(--accent); font-weight: bold; font-size: 13px; border: 1px solid var(--accent); padding: 2px 10px; border-radius: 15px; }

    /* PDF & BOUTONS */
    .pdf-box { width: 100%; height: 600px; border: 1px solid var(--border); border-radius: 8px; margin: 20px 0; }
    .btn-link { 
      display: inline-block; padding: 10px 20px; background: var(--accent); color: var(--bg-dark); 
      text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; transition: 0.3s;
      margin-top: 10px;
    }
    .btn-link:hover { opacity: 0.9; transform: scale(1.02); }

    footer { text-align: center; padding: 50px 20px; color: var(--text-dim); }
    .social-link { color: var(--accent); text-decoration: none; margin: 0 15px; font-weight: bold; }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('parcours')">Parcours & Expériences</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Mémoire</button>
      <button class="nav-btn" onclick="switchTab('travaux')">Travaux en cours</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 60px 30px;">
        <h1 style="font-size: 40px; color: var(--accent); margin-bottom: 15px;">Nicolas Decroix</h1>
        <p style="font-size: 22px; color: var(--text-dim); margin-bottom: 35px;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 750px; margin: 0 auto; font-size: 18px;">
          Étudiant à l'Institut Français de Géopolitique (Paris-VIII), je me spécialise dans l'analyse de la sécurité dans l'espace de l'OTAN en Europe Centrale, Orientale et du Nord.
        </p>
        <div style="margin-top: 45px;">
          <a href="mailto:decroix.nicolasfrancois@gmail.com" class="social-link">📧 Email</a>
          <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="social-link">🔗 LinkedIn</a>
        </div>
      </div>
    </section>

    <section id="parcours" class="tab-pane">
      <h2>Formation Académique</h2>
      <div class="card">
        <h3>Master Géopolitique</h3>
        <span class="date">2024 — 2026 | Institut Français de Géopolitique (Paris-VIII)</span>
        <p>Spécialisation sur le Flanc Est de l'OTAN et les enjeux de défense européens.</p>
      </div>
      <div class="card">
        <h3>Double Licence Histoire-Géographie</h3>
        <span class="date">2021 — 2024 | Université Lyon-III</span>
        <p>Mention Bien. Analyse spatiale et historique des dynamiques de puissance.</p>
      </div>

      <h2 style="margin-top: 40px;">Expériences Professionnelles</h2>
      <div class="card">
        <h3>Assistant Étudiant auprès de la Secrétaire Générale</h3>
        <span class="date">Nov. 2024 — Présent | ERUA (Université Paris-VIII)</span>
        <ul style="margin-left: 20px; font-size: 15px;">
          <li>Rapports analytiques sur les politiques européennes d'éducation.</li>
          <li>Création de supports stratégiques pour les comités de pilotage.</li>
          <li>Productions et réunions réalisées intégralement en anglais.</li>
        </ul>
      </div>
      <div class="card">
        <h3>Stagiaire Recherche - Programme 13-Novembre</h3>
        <span class="date">Juin 2023 — Juil. 2023 | CNRS - MATRICE</span>
        <p style="font-size: 15px;">Transcription de témoignages (Attentats de 2015 / MATRICE) sous protocole de haute confidentialité.</p>
      </div>
      <div class="card">
        <h3>Stagiaire Service Urbanisme</h3>
        <span class="date">Juin 2022 — Juil. 2022 | Mairie de Caluire-et-Cuire</span>
        <p style="font-size: 15px;">Utilisation de SIG (ArcGIS/QGIS) pour l'implantation d'énergie solaire urbaine.</p>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Recherche & Production Scientifique</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (Note : 17/20)</h3>
        <p style="margin-bottom: 10px;"><strong>Sujet :</strong> La militarisation de la frontière russo-polonaise et l'enclave de Kaliningrad.</p>
        
        <div style="background: rgba(56, 189, 248, 0.1); padding: 15px; border-radius: 8px; border: 1px dashed var(--accent); margin-bottom: 20px;">
          <p style="font-size: 14px; margin-bottom: 10px;">📄 <strong>Publication liée :</strong> Retrouvez l'article officiel suite à ma visite scientifique à Olsztyn (Pologne).</p>
          <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="btn-link">Voir l'article officiel ↗</a>
        </div>

        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>

        <div class="image-gallery">
          <a href="carte-nationale.png" target="_blank" class="img-container">
            <img src="carte-nationale.png" alt="Carte" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Nationale'">
            <div class="img-label">Échelle Nationale ↗</div>
          </a>
          <a href="Carte-Région.png" target="_blank" class="img-container">
            <img src="Carte-Région.png" alt="Carte" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Région'">
            <div class="img-label">Échelle Régionale ↗</div>
          </a>
          <a href="Carte-Varmie.png" target="_blank" class="img-container">
            <img src="Carte-Varmie.png" alt="Carte" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Varmie'">
            <div class="img-label">Échelle Locale ↗</div>
          </a>
        </div>

        <p style="margin-top: 20px; font-size: 14px; color: var(--text-dim);">• Co-auteur de notices encyclopédiques pour "666 Albums Metal" (Éditions du Nouveau Monde).</p>
      </div>
    </section>

    <section id="travaux" class="tab-pane">
      <h2>Projets Actuels</h2>
      <div class="card">
        <h3>Mémoire de Master 2</h3>
        <p>Analyse prospective des infrastructures de défense et de la résilience civile sur le corridor de Suwałki.</p>
      </div>
      <div class="card">
        <h3>Veille OSINT</h3>
        <p>Cartographie des fortifications frontalières en Europe de l'Est via imagerie satellite.</p>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Expertises Techniques</h2>
      <div class="skills-grid">
        <div class="skill-card">SIG (QGIS / ArcGIS)</div>
        <div class="skill-card">Analyse Géopolitique</div>
        <div class="skill-card">OSINT</div>
        <div class="skill-card">Adobe Illustrator</div>
      </div>

      <h2 style="margin-top: 30px;">Maîtrise des Langues</h2>
      <div class="card">
        <div class="lang-item"><span>Français</span><span class="lang-level">Maternel</span></div>
        <div class="lang-item"><span>Anglais</span><span class="lang-level">C2 (Bilingue)</span></div>
        <div class="lang-item"><span>Polonais</span><span class="lang-level">B1-B2</span></div>
        <div class="lang-item" style="border:none;"><span>Espagnol</span><span class="lang-level">B1</span></div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix - Portfolio</p>
  </footer>

  <script>
    function switchTab(tabId) {
      document.querySelectorAll('.tab-pane').forEach(p => {
        p.classList.remove('active');
        p.style.display = 'none';
      });
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      const target = document.getElementById(tabId);
      if(target) {
        target.style.display = 'block';
        setTimeout(() => target.classList.add('active'), 10);
      }
      
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(tabId));
      if(btn) btn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
