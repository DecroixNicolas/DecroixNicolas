<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Analyste Géopolitique</title>
  <style>
    :root {
      --bg: #0f172a;
      --card: #1e293b;
      --accent: #38bdf8;
      --text: #f1f5f9;
      --dim: #94a3b8;
      --border: #334155;
      --nav-h: 70px;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', system-ui, sans-serif;
      background-color: var(--bg);
      color: var(--text);
      line-height: 1.6;
      padding-top: var(--nav-h);
    }

    /* NAVIGATION */
    header {
      position: fixed; top: 0; width: 100%; height: var(--nav-h);
      background: var(--card); border-bottom: 1px solid var(--border);
      z-index: 1000; display: flex; justify-content: center;
    }
    nav { display: flex; gap: 10px; overflow-x: auto; padding: 0 15px; align-items: center; scrollbar-width: none; width: 100%; max-width: 1000px; }
    nav::-webkit-scrollbar { display: none; }
    
    .nav-btn {
      padding: 10px 18px; color: var(--dim); background: transparent;
      border: 1px solid transparent; border-radius: 25px; font-size: 13px;
      font-weight: 600; cursor: pointer; white-space: nowrap; transition: 0.3s;
    }
    .nav-btn.active { background: var(--accent); color: var(--bg); }

    /* CONTENU */
    main { max-width: 900px; margin: 0 auto; padding: 30px 20px; }
    .tab-pane { display: none; animation: fadeIn 0.4s ease; }
    .tab-pane.active { display: block; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; }
    h2 { font-size: 24px; margin-bottom: 20px; color: var(--accent); border-left: 4px solid var(--accent); padding-left: 15px; }
    h3 { font-size: 19px; color: var(--text); margin-bottom: 5px; }
    .date { font-size: 13px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 12px; }
    
    ul { margin-left: 20px; margin-bottom: 15px; }
    li { margin-bottom: 8px; font-size: 15px; }

    /* RECHERCHE & CARTES */
    .pdf-box { width: 100%; height: 600px; border: 1px solid var(--border); border-radius: 8px; margin: 20px 0; background: #000; }
    .img-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 15px; margin-top: 20px; }
    .img-item { position: relative; border-radius: 10px; overflow: hidden; border: 2px solid var(--border); transition: 0.3s; display: block; text-decoration: none; }
    .img-item:hover { border-color: var(--accent); transform: translateY(-5px); }
    .img-item img { width: 100%; height: 200px; object-fit: cover; display: block; background: #0f172a; }
    .img-tag { position: absolute; bottom: 0; width: 100%; background: rgba(15, 23, 42, 0.9); color: white; font-size: 12px; padding: 8px; text-align: center; font-weight: bold; }

    /* BOUTONS ACTIONS */
    .action-btn {
      display: inline-block; padding: 10px 20px; background: var(--accent); color: var(--bg);
      text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; margin: 10px 0; transition: 0.3s;
    }
    .action-btn:hover { transform: scale(1.03); filter: brightness(1.1); }

    /* SKILLS */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; margin-bottom: 30px; }
    .skill-box { background: var(--bg); border: 1px solid var(--accent); padding: 20px; border-radius: 12px; text-align: center; font-weight: bold; }
    
    .lang-row { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid var(--border); }

    footer { text-align: center; padding: 40px; color: var(--dim); font-size: 14px; }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('parcours')">Parcours & Expériences</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Terrain</button>
      <button class="nav-btn" onclick="switchTab('travaux')">Projets en cours</button>
      <button class="nav-btn" onclick="switchTab('skills')">Expertises</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 50px 20px;">
        <h1 style="font-size: 38px; color: var(--accent); margin-bottom: 10px;">Nicolas Decroix</h1>
        <p style="font-size: 20px; color: var(--dim); margin-bottom: 30px;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 750px; margin: 0 auto; font-size: 17px; color: var(--text);">
          Étudiant à l'Institut Français de Géopolitique (Paris-VIII), je me spécialise dans la sécurité de l'espace OTAN en Europe Centrale et Orientale. Mon expertise se concentre sur la militarisation du Flanc Est face à la Russie et l'analyse des nouvelles dynamiques de défense frontalière.
        </p>
        <div style="margin-top: 40px;">
          <a href="mailto:decroix.nicolasfrancois@gmail.com" style="color:var(--accent); text-decoration:none; font-weight:bold; margin: 0 15px;">📧 Email</a>
          <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" style="color:var(--accent); text-decoration:none; font-weight:bold; margin: 0 15px;">🔗 LinkedIn</a>
        </div>
      </div>
    </section>

    <section id="parcours" class="tab-pane">
      <h2>Formation Académique</h2>
      <div class="card">
        <h3>Master de Géopolitique</h3>
        <span class="date">2024 — 2026 | Institut Français de Géopolitique (IFG) - Paris-VIII</span>
        <p>Spécialisation sur les enjeux sécuritaires européens et le Flanc Est de l'Alliance Atlantique.</p>
      </div>
      <div class="card">
        <h3>Double Licence Histoire-Géographie</h3>
        <span class="date">2021 — 2024 | Université Lyon-III Jean Moulin</span>
        <p>Obtenue avec <strong>Mention Bien</strong>. Focus sur les relations internationales et la cartographie historique.</p>
      </div>

      <h2 style="margin-top: 40px;">Expériences Professionnelles</h2>
      <div class="card">
        <h3>Assistant Étudiant auprès de la Secrétaire Générale</h3>
        <span class="date">Nov. 2024 — Présent | ERUA (Université Paris-VIII)</span>
        <ul>
          <li>Production de rapports analytiques sur les politiques européennes d'éducation.</li>
          <li>Animation d’ateliers et création de supports pour comités de pilotage.</li>
          <li>Analyse de l'assurance qualité et évaluation d'impact de l'alliance.</li>
          <li>Vérification de conformité et gestion de bases de données collaboratives.</li>
          <li><strong>Travail intégralement en anglais</strong> au sein d'équipes internationales.</li>
          <li>Veille stratégique sur les évènements européens du secteur éducatif.</li>
        </ul>
      </div>

      <div class="card">
        <h3>Stagiaire Recherche - Programme 13-Novembre</h3>
        <span class="date">Juin 2023 — Juillet 2023 | CNRS - MATRICE</span>
        <ul>
          <li>Transcription de témoignages (Victimes des attentats de 2015 / Déportés français).</li>
          <li>Respect rigoureux du vade-mecum de transcription scientifique.</li>
          <li>Gestion de données sensibles sous protocole de <strong>haute confidentialité</strong>.</li>
        </ul>
      </div>

      <div class="card">
        <h3>Stagiaire Service Urbanisme</h3>
        <span class="date">Juin 2022 — Juillet 2022 | Mairie de Caluire-et-Cuire</span>
        <ul>
          <li>Recherche stratégique pour l’implantation photovoltaïque urbaine.</li>
          <li>Rédaction de notes de synthèse et rapports pour les élus.</li>
          <li>Maîtrise opérationnelle des outils SIG (ArcGIS, QGIS).</li>
        </ul>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Recherche & Production Scientifique</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (Note : 17/20)</h3>
        <p style="margin-bottom: 15px;"><strong>Thématique :</strong> Militarisation de la frontière russo-polonaise (Kaliningrad) et impacts locaux.</p>
        
        <div style="background: rgba(56, 189, 248, 0.1); padding: 20px; border-radius: 10px; border: 1px dashed var(--accent); margin-bottom: 25px;">
          <p style="font-size: 15px; margin-bottom: 10px;">🌍 <strong>Rapport de Terrain :</strong> Suite à ma visite scientifique à l'Université d'Olsztyn (Pologne), retrouvez l'article officiel traitant de la sécurité frontalière.</p>
          <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="action-btn">Lire l'article officiel ↗</a>
        </div>

        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>

        <div class="img-grid">
          <a href="carte-nationale.png" target="_blank" class="img-item">
            <img src="carte-nationale.png" alt="Carte" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Carte+Nationale'">
            <div class="img-tag">Échelle Nationale ↗</div>
          </a>
          <a href="Carte-Région.png" target="_blank" class="img-item">
            <img src="Carte-Région.png" alt="Carte" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Carte+Région'">
            <div class="img-tag">Échelle Régionale ↗</div>
          </a>
          <a href="Carte-Varmie.png" target="_blank" class="img-item">
            <img src="Carte-Varmie.png" alt="Carte" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Carte+Varmie'">
            <div class="img-tag">Échelle Locale (Varmie) ↗</div>
          </a>
        </div>

        <p style="margin-top: 25px; font-size: 14px; color: var(--dim);">• Co-auteur de notices encyclopédiques pour l'ouvrage "666 Albums Metal" (Éditions du Nouveau Monde).</p>
      </div>
    </section>

    <section id="travaux" class="tab-pane">
      <h2>Projets de Recherche Actuels</h2>
      <div class="card">
        <h3>Mémoire de Master 2 (2025-2026)</h3>
        <p>Analyse prospective des infrastructures de défense (Ligne de défense balte) et de la résilience civile sur le flanc oriental.</p>
      </div>
      <div class="card">
        <h3>Veille OSINT & GEOINT</h3>
        <p>Monitorage par imagerie satellite des fortifications frontalières et des mouvements d'infrastructure dans l'oblast de Kaliningrad et en Biélorussie.</p>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Expertises Techniques</h2>
      <div class="skills-grid">
        <div class="skill-box">SIG (QGIS / ArcGIS)</div>
        <div class="skill-box">Analyse Géopolitique</div>
        <div class="skill-box">Méthodologie OSINT</div>
        <div class="skill-box">Adobe Illustrator</div>
        <div class="skill-box">Analyse de Données</div>
      </div>

      <h2 style="margin-top: 40px;">Maîtrise des Langues</h2>
      <div class="card">
        <div class="lang-row"><span>Français</span><span style="color:var(--accent); font-weight:bold;">Maternel</span></div>
        <div class="lang-row"><span>Anglais</span><span style="color:var(--accent); font-weight:bold;">C2 (Bilingue / Professionnel)</span></div>
        <div class="lang-row"><span>Polonais</span><span style="color:var(--accent); font-weight:bold;">B1-B2 (Intermédiaire)</span></div>
        <div class="lang-row" style="border:none;"><span>Espagnol</span><span style="color:var(--accent); font-weight:bold;">B1</span></div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix - Tous droits réservés</p>
  </footer>

  <script>
    function switchTab(id) {
      // 1. Masquer tout
      document.querySelectorAll('.tab-pane').forEach(p => {
        p.classList.remove('active');
        p.style.display = 'none';
      });
      // 2. Désactiver boutons
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      // 3. Activer cible
      const target = document.getElementById(id);
      if(target) {
        target.style.display = 'block';
        setTimeout(() => target.classList.add('active'), 10);
      }
      
      // 4. Activer bouton correspondant
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(id));
      if(btn) btn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
    // Lancer sur l'accueil
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
