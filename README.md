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
    .image-gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin-top: 25px; }
    .img-container { 
      position: relative; cursor: pointer; overflow: hidden; border-radius: 10px; 
      border: 2px solid var(--border); transition: 0.3s; display: block; 
    }
    .img-container:hover { border-color: var(--accent); transform: translateY(-5px); }
    .img-container img { width: 100%; display: block; height: 220px; object-fit: cover; background: #0f172a; }
    .img-label { position: absolute; bottom: 0; width: 100%; background: rgba(15, 23, 42, 0.9); color: white; font-size: 13px; padding: 10px; text-align: center; font-weight: bold; }

    /* COMPÉTENCES (AGRANDIES) */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; margin-bottom: 40px; }
    .skill-card { 
      background: linear-gradient(145deg, #1e293b, #0f172a); 
      border: 1px solid var(--accent); padding: 30px 20px; border-radius: 15px; 
      text-align: center; font-weight: bold; font-size: 18px; color: var(--accent);
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }

    /* LANGUES (SÉPARÉES) */
    .lang-item { display: flex; justify-content: space-between; align-items: center; padding: 15px 0; border-bottom: 1px solid var(--border); }
    .lang-name { font-size: 18px; font-weight: 600; }
    .lang-level { color: var(--accent); font-weight: bold; font-size: 14px; border: 1px solid var(--accent); padding: 4px 12px; border-radius: 20px; }

    /* PDF */
    .pdf-box { width: 100%; height: 600px; border: 1px solid var(--border); border-radius: 8px; margin: 20px 0; }

    footer { text-align: center; padding: 50px 20px; border-top: 1px solid var(--border); margin-top: 50px; }
    .social-link { color: var(--accent); text-decoration: none; margin: 0 15px; font-weight: bold; font-size: 16px; }
  </style>
</head>
<body>

  <header>
    <nav id="main-nav">
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('exps')">Parcours Pro</button>
      <button class="nav-btn" onclick="switchTab('travaux')">Travaux en cours</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Engagements</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 60px 30px;">
        <h1 style="font-size: 40px; color: var(--accent); margin-bottom: 15px;">Nicolas Decroix</h1>
        <p style="font-size: 22px; color: var(--text-dim); margin-bottom: 35px;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 750px; margin: 0 auto; font-size: 18px; line-height: 1.8;">
          Étudiant à l'Institut Français de Géopolitique (Paris-VIII), je me spécialise dans l'analyse de la sécurité dans l'espace de l'OTAN en Europe Centrale, Orientale et du Nord. Mon travail se concentre sur les enjeux de militarisation des pays du Flanc Est de l'OTAN face à la Russie, les dynamiques frontalières ainsi que leurs conséquences sur la société civile.
        </p>
        <div style="margin-top: 45px;">
          <a href="mailto:decroix.nicolasfrancois@gmail.com" class="social-link">📧 Email</a>
          <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="social-link">🔗 LinkedIn</a>
        </div>
      </div>
    </section>

    <section id="exps" class="tab-pane">
      <h2>Expériences Professionnelles</h2>
      <div class="card">
        <h3>Assistant Étudiant auprès de la Secrétaire Générale</h3>
        <span class="date">Nov. 2024 — Présent | ERUA (Université Paris-VIII)</span>
        <ul style="margin-left: 20px; font-size: 15px;">
          <li>Rapports analytiques sur les politiques européennes d'éducation.</li>
          <li>Création de présentations et d’ateliers de comité de pilotage.</li>
          <li>Analyse assurance qualité et impact de l’alliance.</li>
          <li>Organisation et vérification de conformité sur les bases de données collaboratives.</li>
          <li>Réunions et productions réalisées intégralement en anglais.</li>
          <li>Veille sur les évènements européens du secteur de l’éducation.</li>
        </ul>
      </div>

      <div class="card">
        <h3>Stagiaire Recherche - Programme 13-Novembre</h3>
        <span class="date">Juin 2023 — Juillet 2023 | CNRS - MATRICE</span>
        <ul style="margin-left: 20px; font-size: 15px;">
          <li>Transcription de témoignages de victimes des attentats de 2015 en France et de déportés français.</li>
          <li>Suivi rigoureux du vade-mecum de transcription scientifique.</li>
          <li>Respect strict des protocoles de confidentialité.</li>
        </ul>
      </div>

      <div class="card">
        <h3>Stagiaire Service Urbanisme</h3>
        <span class="date">Juin 2022 — Juillet 2022 | Mairie de Caluire-et-Cuire</span>
        <ul style="margin-left: 20px; font-size: 15px;">
          <li>Recherche pour l’implantation de production d’énergie solaire urbaine.</li>
          <li>Rédaction de notes et rapports décisionnels à destination du maire.</li>
          <li>Utilisation de SIG : ArcGIS, QGIS.</li>
        </ul>
      </div>
    </section>

    <section id="travaux" class="tab-pane">
      <h2>Travaux en cours</h2>
      <div class="card">
        <h3>Mémoire de Recherche - Master 2</h3>
        <span class="date">2025 — 2026</span>
        <p>Analyse des mutations sécuritaires et des infrastructures de défense sur le flanc oriental de l'Alliance Atlantique.</p>
      </div>
      <div class="card">
        <h3>Veille Stratégique OSINT</h3>
        <p>Monitorage en temps réel des dynamiques de militarisation en zone frontalière et cartographie des nouveaux points de tension en Europe de l'Est.</p>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Recherche Académique & Engagements</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (Note : 17/20)</h3>
        <p style="margin-bottom: 15px;"><strong>Sujet :</strong> La militarisation de la frontière russo-polonaise et l'enclave de Kaliningrad.</p>
        
        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>

        <div class="image-gallery">
          <a href="carte-nationale.png" target="_blank" class="img-container">
            <img src="carte-nationale.png" alt="Carte Nationale" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Nationale+Manquante'">
            <div class="img-label">Échelle Nationale ↗</div>
          </a>
          <a href="Carte-Région.png" target="_blank" class="img-container">
            <img src="Carte-Région.png" alt="Carte Régionale" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Région+Manquante'">
            <div class="img-label">Échelle Régionale ↗</div>
          </a>
          <a href="Carte-Varmie.png" target="_blank" class="img-container">
            <img src="Carte-Varmie.png" alt="Carte Varmie" onerror="this.src='https://via.placeholder.com/600x400/1e293b/38bdf8?text=Carte+Varmie+Manquante'">
            <div class="img-label">Échelle Locale (Varmie) ↗</div>
          </a>
        </div>
      </div>

      <div class="card">
        <h3>Terrain & Publications</h3>
        <p style="margin-bottom: 15px;">• <strong>Visite scientifique à Olsztyn (Pologne)</strong> : Échanges avec les officiels de l'UWM sur la sécurité frontalière.</p>
        <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" style="color: var(--accent); text-decoration: none; border: 1px solid var(--accent); padding: 8px 15px; border-radius: 8px; font-size: 14px; display: inline-block; margin-bottom: 20px;">Lire l'article officiel ↗</a>
        
        <p>• <strong>Séminaire de l'Office Français (Varsovie, 2025)</strong> : Présentation de travaux géopolitiques.</p>
        <p style="margin-top: 10px;">• <strong>666 Albums Metal (Éditions du Nouveau Monde)</strong> : Co-auteur de notices encyclopédiques.</p>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Expertises Techniques</h2>
      <div class="skills-grid">
        <div class="skill-card">SIG (QGIS / ArcGIS)</div>
        <div class="skill-card">Analyse Géopolitique</div>
        <div class="skill-card">Veille OSINT</div>
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
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix - Portfolio Analyste Géopolitique</p>
  </footer>

  <script>
    function switchTab(tabId) {
      // 1. Cacher tous les onglets
      document.querySelectorAll('.tab-pane').forEach(p => {
        p.classList.remove('active');
        p.style.display = 'none';
      });
      // 2. Désactiver tous les boutons
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      // 3. Afficher le bon onglet
      const target = document.getElementById(tabId);
      if(target) {
        target.style.display = 'block';
        setTimeout(() => target.classList.add('active'), 10);
      }
      
      // 4. Activer le bouton
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(tabId));
      if(btn) btn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Lancement automatique sur la présentation
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
