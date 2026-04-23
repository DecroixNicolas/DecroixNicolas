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
    nav { 
      display: flex; gap: 8px; overflow-x: auto; padding: 0 15px; 
      scrollbar-width: none; width: 100%; max-width: 900px;
    }
    nav::-webkit-scrollbar { display: none; }
    
    .nav-btn {
      padding: 10px 18px; color: var(--text-dim); background: transparent;
      border: 1px solid transparent; border-radius: 25px; font-size: 13px;
      font-weight: 600; cursor: pointer; white-space: nowrap; transition: 0.3s;
    }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU */
    main { max-width: 900px; margin: 0 auto; padding: 30px 20px; }
    
    /* On cache tout par défaut sauf la home */
    .tab-pane { display: none; opacity: 0; transition: opacity 0.4s ease; }
    .tab-pane.active { display: block; opacity: 1; }

    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; }
    h2 { font-size: 24px; margin-bottom: 25px; color: var(--accent); border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 19px; margin-bottom: 8px; color: var(--text-main); }
    .date { font-size: 13px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 15px; }

    /* RECHERCHE */
    .pdf-box { width: 100%; height: 550px; border: 1px solid var(--border); border-radius: 8px; margin: 20px 0; background: #000; }
    .image-gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; }
    .img-link { position: relative; cursor: pointer; border-radius: 10px; border: 1px solid var(--border); display: block; overflow: hidden; }
    .img-link img { width: 100%; display: block; object-fit: cover; min-height: 150px; background: #0f172a; }
    .img-label { position: absolute; bottom: 0; width: 100%; background: rgba(0,0,0,0.8); color: white; font-size: 11px; padding: 5px; text-align: center; }

    /* SKILLS */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; }
    .skill-card { background: var(--bg-dark); border: 1px solid var(--accent); padding: 20px; border-radius: 12px; text-align: center; font-weight: bold; }
    .lang-item { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid var(--border); }

    footer { text-align: center; padding: 40px; border-top: 1px solid var(--border); color: var(--text-dim); }
    .social-link { color: var(--accent); text-decoration: none; margin: 0 10px; font-weight: bold; }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('exps')">Expériences</button>
      <button class="nav-btn" onclick="switchTab('travaux')">Travaux en cours</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 40px;">
        <h1 style="font-size: 32px; color: var(--accent);">Nicolas Decroix</h1>
        <p style="font-size: 18px; color: var(--text-dim); margin: 10px 0 25px 0;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 700px; margin: 0 auto;">
          Étudiant à l'Institut Français de Géopolitique (Paris-VIII), spécialisé dans la sécurité de l'espace OTAN et la militarisation du Flanc Est.
        </p>
        <div style="margin-top: 30px;">
          <a href="mailto:decroix.nicolasfrancois@gmail.com" class="social-link">Email</a>
          <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="social-link">LinkedIn</a>
        </div>
      </div>
    </section>

    <section id="exps" class="tab-pane">
      <h2>Expériences Professionnelles</h2>
      <div class="card">
        <h3>Assistant Étudiant - Secrétariat Général</h3>
        <span class="date">Nov. 2024 — Présent | ERUA</span>
        <p>Analyse de politiques européennes et coordination stratégique en anglais.</p>
      </div>
      <div class="card">
        <h3>Stagiaire Recherche</h3>
        <span class="date">2023 | CNRS</span>
        <p>Transcription de témoignages (Programme 13-Novembre).</p>
      </div>
      <div class="card">
        <h3>Stagiaire Urbanisme</h3>
        <span class="date">2022 | Mairie de Caluire</span>
        <p>Étude SIG sur l'énergie solaire.</p>
      </div>
    </section>

    <section id="travaux" class="tab-pane">
      <h2>Travaux en cours</h2>
      <div class="card">
        <h3>Recherche Master 2 (2025-2026)</h3>
        <p>Analyse des mutations sécuritaires sur le flanc oriental de l'OTAN.</p>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Recherche Académique</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (17/20)</h3>
        <p>Militarisation de la frontière russo-polonaise.</p>
        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
        
        <div class="image-gallery">
          <a href="carte-nationale.png" target="_blank" class="img-link">
            <img src="carte-nationale.png" alt="Carte" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Nationale'">
            <div class="img-label">Échelle Nationale ↗</div>
          </a>
          <a href="Carte-Région.png" target="_blank" class="img-link">
            <img src="Carte-Région.png" alt="Carte" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Région'">
            <div class="img-label">Échelle Régionale ↗</div>
          </a>
          <a href="Carte-Varmie.png" target="_blank" class="img-link">
            <img src="Carte-Varmie.png" alt="Carte" onerror="this.src='https://via.placeholder.com/400x300/1e293b/38bdf8?text=Carte+Varmie'">
            <div class="img-label">Échelle Locale ↗</div>
          </a>
        </div>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Expertises Techniques</h2>
      <div class="skills-grid" style="margin-bottom: 30px;">
        <div class="skill-card">SIG (QGIS / ArcGIS)</div>
        <div class="skill-card">Analyse Géopolitique</div>
        <div class="skill-card">Veille OSINT</div>
        <div class="skill-card">Adobe Illustrator</div>
      </div>
      <h2>Langues</h2>
      <div class="card">
        <div class="lang-item"><span>Français</span><span style="color:var(--accent)">Maternel</span></div>
        <div class="lang-item"><span>Anglais</span><span style="color:var(--accent)">C2 (Bilingue)</span></div>
        <div class="lang-item"><span>Polonais</span><span style="color:var(--accent)">B1-B2</span></div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix</p>
  </footer>

  <script>
    function switchTab(tabId) {
      // 1. Cacher toutes les sections
      const sections = document.querySelectorAll('.tab-pane');
      sections.forEach(s => {
        s.classList.remove('active');
        s.style.display = 'none';
      });

      // 2. Désactiver les boutons
      const btns = document.querySelectorAll('.nav-btn');
      btns.forEach(b => b.classList.remove('active'));

      // 3. Afficher la section demandée
      const target = document.getElementById(tabId);
      if(target) {
        target.style.display = 'block';
        // Petit délai pour l'effet de fondu
        setTimeout(() => target.classList.add('active'), 10);
      }

      // 4. Activer le bouton correspondant
      const activeBtn = Array.from(btns).find(b => b.getAttribute('onclick').includes(tabId));
      if(activeBtn) activeBtn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Sécurité : charger la home au démarrage
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
