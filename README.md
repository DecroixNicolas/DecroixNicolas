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

    .card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; position: relative; }
    h2 { font-size: 24px; margin-bottom: 20px; color: var(--accent); border-left: 4px solid var(--accent); padding-left: 15px; text-transform: uppercase; letter-spacing: 1px; }
    h3 { font-size: 19px; color: var(--text); margin-bottom: 5px; }
    .date { font-size: 13px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 12px; opacity: 0.9; }
    
    ul { margin-left: 20px; margin-bottom: 15px; }
    li { margin-bottom: 8px; font-size: 15px; color: var(--text); opacity: 0.9; }

    /* RECHERCHE & CARTES */
    .pdf-box { width: 100%; height: 600px; border: 1px solid var(--border); border-radius: 8px; margin: 20px 0; background: #000; }
    .img-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 15px; margin-top: 20px; }
    .img-item { position: relative; border-radius: 10px; overflow: hidden; border: 2px solid var(--border); transition: 0.3s; display: block; }
    .img-item:hover { border-color: var(--accent); transform: translateY(-5px); box-shadow: 0 10px 20px rgba(0,0,0,0.3); }
    .img-item img { width: 100%; height: 200px; object-fit: cover; display: block; background: #0f172a; }
    .img-tag { position: absolute; bottom: 0; width: 100%; background: rgba(15, 23, 42, 0.9); color: white; font-size: 12px; padding: 8px; text-align: center; font-weight: bold; }

    /* BOUTONS ACTIONS */
    .action-btn {
      display: inline-block; padding: 10px 20px; background: var(--accent); color: var(--bg);
      text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; margin: 10px 0; transition: 0.3s;
    }
    .action-btn:hover { transform: scale(1.03); filter: brightness(1.1); }

    /* SKILLS */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 30px; }
    .skill-box { background: var(--bg); border: 1px solid var(--border); padding: 15px; border-radius: 12px; text-align: center; transition: 0.3s; }
    .skill-box:hover { border-color: var(--accent); color: var(--accent); }
    .skill-box strong { display: block; margin-bottom: 5px; color: var(--accent); }
    
    .lang-row { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid var(--border); }

    .interest-tag { display: inline-block; padding: 5px 15px; background: var(--border); border-radius: 20px; margin: 5px; font-size: 14px; color: var(--dim); }

    footer { text-align: center; padding: 60px 40px; color: var(--dim); font-size: 14px; border-top: 1px solid var(--border); }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('parcours')">Parcours & Expériences</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Publications</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences & Loisirs</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 60px 30px;">
        <h1 style="font-size: 42px; color: var(--accent); margin-bottom: 10px;">Nicolas Decroix</h1>
        <p style="font-size: 22px; color: var(--dim); margin-bottom: 35px; font-weight: 300;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 750px; margin: 0 auto; font-size: 18px; color: var(--text);">
          Étudiant en Master à l'Institut Français de Géopolitique [cite: 5], je me spécialise dans la compétition stratégique et la sécurité de l'espace OTAN[cite: 5, 6]. Mon expertise porte sur la militarisation du Flanc Est et l'analyse de défense face aux nouveaux enjeux de puissance[cite: 6, 17].
        </p>
        <div style="margin-top: 45px;">
          <a href="mailto:decroix.nicolasfrancois@gmail.com" class="action-btn">📩 Contactez-moi</a>
          <a href="https://www.linkedin.com/in/nicolas-decroix-805218222/" target="_blank" class="action-btn" style="background: transparent; border: 1px solid var(--accent); color: var(--accent); margin-left: 10px;">🔗 LinkedIn</a>
        </div>
      </div>
    </section>

    <section id="parcours" class="tab-pane">
      <h2>Cursus Académique</h2>
      <div class="card">
        <span class="date">2024 — 2026</span>
        <h3>Master de Géopolitique - Spécialisation Nouveaux Acteurs</h3>
        <p>Institut Français de Géopolitique (IFG) - Université Paris-VIII [cite: 5]</p>
      </div>
      <div class="card">
        <span class="date">2021 — 2024</span>
        <h3>Double Licence Histoire & Géographie</h3>
        <p>Université Jean Moulin Lyon-III | <strong>Mention Bien</strong> pour les deux licences [cite: 7, 8]</p>
      </div>
      <div class="card">
        <span class="date">2020 — 2021</span>
        <h3>Baccalauréat Général</h3>
        <p>Institution des Chartreux | <strong>Mention Très Bien</strong> (Spécialités Maths & HGGSP) [cite: 9, 10]</p>
      </div>

      <h2 style="margin-top: 40px;">Expériences Professionnelles</h2>
      <div class="card">
        <span class="date">Nov. 2024 — Présent</span>
        <h3>Student Assistant to the Secretary General</h3>
        <p>European Reform Universities Alliance (ERUA) - Paris-VIII [cite: 13]</p>
        <ul>
          <li>Production de rapports analytiques sur les politiques européennes d'éducation[cite: 13].</li>
          <li>Animation d’ateliers de comité de pilotage et présentations stratégiques[cite: 13].</li>
          <li>Analyse d'assurance qualité et vérification de conformité de données[cite: 13].</li>
          <li><strong>Production 100% anglophone</strong> à destination des partenaires européens[cite: 13].</li>
        </ul>
      </div>

      <div class="card">
        <span class="date">Juin — Août 2023</span>
        <h3>Stagiaire Recherche</h3>
        <p>CNRS - Programme 13-Novembre & Équipex MATRICE [cite: 13]</p>
        <ul>
          <li>Transcription de témoignages de victimes d'attentats et de déportés[cite: 13].</li>
          <li>Application rigoureuse du vade-mecum de transcription scientifique[cite: 13].</li>
          <li>Respect strict des <strong>clauses de confidentialité</strong> et protocoles éthiques[cite: 13].</li>
        </ul>
      </div>

      <div class="card">
        <span class="date">Juillet — Août 2022</span>
        <h3>Stagiaire Urbanisme</h3>
        <p>Mairie de Caluire-et-Cuire [cite: 13]</p>
        <ul>
          <li>Recherche pour l’implantation de production d'énergie solaire urbaine[cite: 13].</li>
          <li>Rédaction de rapports décisionnels à destination du Maire[cite: 13].</li>
          <li>Utilisation opérationnelle de <strong>SIG (ArcGIS, QGIS)</strong>[cite: 13].</li>
        </ul>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Travaux de Recherche</h2>
      <div class="card">
        <h3>Mémoire de Master 1 (Note : 17/20)</h3>
        <p><em>"La militarisation de la frontière russo-polonaise avec Kaliningrad"</em> [cite: 6]</p>
        
        <div style="background: rgba(56, 189, 248, 0.1); padding: 20px; border-radius: 10px; border: 1px dashed var(--accent); margin-bottom: 25px;">
          <p style="font-size: 15px; margin-bottom: 10px;">🌍 <strong>Rapport de Terrain :</strong> Suite à ma visite scientifique à l'Université d'Olsztyn (Pologne), retrouvez l'article officiel traitant de la sécurité frontalière.</p>
          <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="action-btn">Voir l'article ↗</a>
        </div>

        <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>

        <div class="img-grid">
          <div class="img-item">
            <img src="carte-nationale.png" alt="Échelle Nationale" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Cartographie+Nationale'">
            <div class="img-tag">Analyse Nationale</div>
          </div>
          <div class="img-item">
            <img src="Carte-Région.png" alt="Échelle Régionale" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Cartographie+Régionale'">
            <div class="img-tag">Analyse Régionale</div>
          </div>
          <div class="img-item">
            <img src="Carte-Varmie.png" alt="Échelle Locale" onerror="this.src='https://via.placeholder.com/500x300/1e293b/38bdf8?text=Cartographie+Locale'">
            <div class="img-tag">Analyse Locale (Varmie)</div>
          </div>
        </div>
      </div>

      <h2 style="margin-top: 40px;">Publications & Engagements</h2>
      <div class="card">
        <ul style="list-style-type: '⚡ '; margin-left: 25px;">
          <li><strong>Diploweb.com :</strong> Rédaction d'un article de géopolitique sous la direction de Pierre Verluise (2025)[cite: 14].</li>
          <li><strong>Office Français (Varsovie) :</strong> Présentation d'ouvrage en séminaire de lecture (2025)[cite: 14].</li>
          <li><strong>Encyclopédie Musicale :</strong> Chronique d'album dans <em>"666 Albums Metal Essentiels"</em> (Éd. du Nouveau Monde, 2025)[cite: 14].</li>
          <li><strong>Association Géodote :</strong> Chargé des partenariats (2025-2026) au sein de l'IFG[cite: 15].</li>
        </ul>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Matrice de Compétences</h2>
      <div class="skills-grid">
        <div class="skill-box"><strong>Analyse</strong>Géopolitique & OSINT [cite: 13]</div>
        <div class="skill-box"><strong>Cartographie</strong>QGIS & Illustrator [cite: 13]</div>
        <div class="skill-box"><strong>SIG</strong>ArcGIS / QGIS [cite: 13]</div>
        <div class="skill-box"><strong>Bureautique</strong>Suite Office Expert [cite: 13]</div>
      </div>

      <h2 style="margin-top: 40px;">Langues</h2>
      <div class="card">
        <div class="lang-row"><span>Français</span><span style="color:var(--accent); font-weight:bold;">Langue maternelle [cite: 13]</span></div>
        <div class="lang-row"><span>Anglais</span><span style="color:var(--accent); font-weight:bold;">C2 (Expert) [cite: 13]</span></div>
        <div class="lang-row"><span>Polonais</span><span style="color:var(--accent); font-weight:bold;">B1-B2 (Intermédiaire) [cite: 13]</span></div>
        <div class="lang-row" style="border:none;"><span>Espagnol</span><span style="color:var(--accent); font-weight:bold;">B1 [cite: 13]</span></div>
      </div>

      <h2 style="margin-top: 40px;">Centres d'intérêt</h2>
      <div class="card" style="text-align: center;">
        <span class="interest-tag">Actualité Géopolitique</span>
        <span class="interest-tag">Histoire Européenne</span>
        <span class="interest-tag">Musique (Guitare & Clarinette)</span>
        <span class="interest-tag">Basket-ball</span>
        <span class="interest-tag">Fitness</span>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix | Analyste Géopolitique</p>
    <p style="margin-top: 5px; opacity: 0.5;">Portfolio conçu pour la sécurité et la stratégie.</p>
  </footer>

  <script>
    function switchTab(id) {
      document.querySelectorAll('.tab-pane').forEach(p => {
        p.classList.remove('active');
        p.style.display = 'none';
      });
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      const target = document.getElementById(id);
      if(target) {
        target.style.display = 'block';
        setTimeout(() => target.classList.add('active'), 10);
      }
      
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(id));
      if(btn) btn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
