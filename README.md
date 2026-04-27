<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Présentation | Portfolio</title>
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

    main { max-width: 1100px; margin: 0 auto; padding: 30px 20px; }
    .tab-pane { display: none; animation: fadeIn 0.4s ease; }
    .tab-pane.active { display: block; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 25px; margin-bottom: 25px; }
    h2 { font-size: 24px; margin-bottom: 20px; color: var(--accent); border-left: 4px solid var(--accent); padding-left: 15px; text-transform: uppercase; }
    h3 { font-size: 19px; color: var(--text); margin-bottom: 5px; }
    .date { font-size: 13px; color: var(--accent); font-weight: bold; display: block; margin-bottom: 12px; }
    
    ul { margin-left: 20px; margin-bottom: 15px; }
    li { margin-bottom: 8px; font-size: 15px; color: var(--text); }

    /* LAYOUT MÉMOIRE */
    .memo-flex { display: flex; gap: 30px; flex-wrap: wrap; }
    .memo-left { flex: 1.2; min-width: 320px; }
    .memo-right { flex: 0.8; min-width: 300px; display: flex; flex-direction: column; gap: 15px; }

    .pdf-box { width: 100%; height: 550px; border: 1px solid var(--border); border-radius: 8px; margin-top: 15px; background: #000; }
    
    .img-item { position: relative; border-radius: 10px; overflow: hidden; border: 2px solid var(--border); transition: 0.3s; display: block; }
    .img-item:hover { border-color: var(--accent); transform: scale(1.02); }
    .img-item img { width: 100%; height: 200px; object-fit: cover; display: block; background: #0f172a; }
    .img-tag { position: absolute; bottom: 0; width: 100%; background: rgba(15, 23, 42, 0.9); color: white; font-size: 11px; padding: 6px; text-align: center; font-weight: bold; }

    .action-btn {
      display: inline-block; padding: 10px 20px; background: var(--accent); color: var(--bg);
      text-decoration: none; border-radius: 8px; font-weight: bold; font-size: 14px; margin: 10px 0; transition: 0.3s;
    }
    .action-btn:hover { filter: brightness(1.1); }

    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-bottom: 30px; }
    .skill-box { background: var(--bg); border: 1px solid var(--border); padding: 15px; border-radius: 12px; text-align: center; }
    .skill-box strong { display: block; margin-bottom: 5px; color: var(--accent); }
    
    .lang-row { display: flex; justify-content: space-between; padding: 12px 0; border-bottom: 1px solid var(--border); }
    .interest-tag { display: inline-block; padding: 5px 15px; background: var(--border); border-radius: 20px; margin: 5px; font-size: 14px; color: var(--dim); }

    footer { text-align: center; padding: 60px 40px; color: var(--dim); font-size: 14px; border-top: 1px solid var(--border); }

    @media (max-width: 850px) {
      .memo-flex { flex-direction: column; }
      .memo-right { flex-direction: row; flex-wrap: wrap; }
      .memo-right .img-item { flex: 1; min-width: 250px; }
    }
  </style>
</head>
<body>

  <header>
    <nav>
      <button class="nav-btn active" onclick="switchTab('home')">Présentation</button>
      <button class="nav-btn" onclick="switchTab('parcours')">Parcours & Expériences</button>
      <button class="nav-btn" onclick="switchTab('recherche')">Recherche & Publications</button>
      <button class="nav-btn" onclick="switchTab('skills')">Compétences</button>
    </nav>
  </header>

  <main>
    <section id="home" class="tab-pane active">
      <div class="card" style="text-align: center; padding: 60px 30px;">
        <h1 style="font-size: 42px; color: var(--accent); margin-bottom: 10px;">Nicolas Decroix</h1>
        <p style="font-size: 22px; color: var(--dim); margin-bottom: 35px; font-weight: 300;">Analyste en Géopolitique & Nouveaux Acteurs</p>
        <p style="text-align: justify; max-width: 750px; margin: 0 auto; font-size: 18px; color: var(--text);">
          Étudiant en Master à l'Institut Français de Géopolitique, je me spécialise dans la compétition stratégique et la sécurité de l'espace OTAN. Mon expertise porte sur la militarisation du Flanc Est et l'analyse de défense face aux nouveaux enjeux de puissance.
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
        <p>Institut Français de Géopolitique (IFG) - Université Paris-VIII</p>
      </div>
      <div class="card">
        <span class="date">2021 — 2024</span>
        <h3>Double Licence Histoire & Géographie</h3>
        <p>Université Jean Moulin Lyon-III | <strong>Mention Bien</strong></p>
      </div>
      <div class="card">
        <span class="date">2020 — 2021</span>
        <h3>Baccalauréat Général</h3>
        <p>Institution des Chartreux | <strong>Mention Très Bien</strong> (Maths & HGGSP)</p>
      </div>

      <h2 style="margin-top: 40px;">Expériences Professionnelles</h2>
      <div class="card">
        <span class="date">Nov. 2024 — Présent</span>
        <h3>Student Assistant to the Secretary General</h3>
        <p>European Reform Universities Alliance (ERUA) - Paris-VIII</p>
        <ul>
          <li>Production de rapports analytiques sur les politiques européennes d'éducation.</li>
          <li>Animation d’ateliers de comité de pilotage et présentations stratégiques.</li>
          <li>Analyse d'assurance qualité et vérification de conformité de données.</li>
        </ul>
      </div>

      <div class="card">
        <span class="date">Juin — Août 2023</span>
        <h3>Stagiaire Recherche</h3>
        <p>CNRS - Programme 13-Novembre & Équipex MATRICE</p>
        <ul>
          <li>Transcription de témoignages de victimes d'attentats et de déportés.</li>
          <li>Respect du vade-mecum de transcription scientifique et des clauses de confidentialité.</li>
        </ul>
      </div>
    </section>

    <section id="recherche" class="tab-pane">
      <h2>Travaux de Recherche</h2>
      <div class="card">
        <div class="memo-flex">
          <div class="memo-left">
            <h3>Mémoire de Master 1 (17/20)</h3>
            <p style="margin-bottom: 12px;"><em>"La militarisation de la frontière russo-polonaise avec Kaliningrad"</em></p>
            <p style="font-size: 14px; text-align: justify; color: var(--dim); margin-bottom: 15px;">
              Ce travail documente une visite scientifique à l'Université d'Olsztyn (Pologne), détaillant des échanges directs avec les chercheurs locaux et les autorités sur la sécurité frontalière.
            </p>
            <a href="http://wns.uwm.edu.pl/inp/wizyta-naukowa-studenta-z-francji" target="_blank" class="action-btn" style="padding: 8px 15px; font-size: 12px;">Article de terrain ↗</a>
            <iframe class="pdf-box" src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
          </div>

          <div class="memo-right">
            <div class="img-item">
              <img src="carte-nationale.jpg" alt="Carte Nationale" onerror="this.src='https://via.placeholder.com/500x320/1e293b/38bdf8?text=carte-nationale.jpg'">
              <div class="img-tag">Échelle Nationale</div>
            </div>
            <div class="img-item">
              <img src="Carte-Région.png" alt="Carte Région" onerror="this.src='https://via.placeholder.com/500x320/1e293b/38bdf8?text=Carte-Région.png'">
              <div class="img-tag">Échelle Régionale</div>
            </div>
            <div class="img-item">
              <img src="Carte-Varmie.png" alt="Carte Locale" onerror="this.src='https://via.placeholder.com/500x320/1e293b/38bdf8?text=Carte-Varmie.png'">
              <div class="img-tag">Échelle Locale (Varmie)</div>
            </div>
          </div>
        </div>
      </div>

      <h2 style="margin-top: 40px;">Engagements</h2>
      <div class="card">
        <ul style="list-style-type: '⚡ '; margin-left: 25px;">
          <li><strong>Office Français (Varsovie) :</strong> Présentation d'ouvrage en séminaire de lecture (2025).</li>
          <li><strong>Encyclopédie Musicale :</strong> Chronique d'album dans <em>"666 Albums Metal Essentiels"</em> (Éd. du Nouveau Monde, 2025).</li>
          <li><strong>Association Géodote :</strong> Chargé des partenariats au sein de l'IFG (2025-2026).</li>
        </ul>
      </div>
    </section>

    <section id="skills" class="tab-pane">
      <h2>Expertises</h2>
      <div class="skills-grid">
        <div class="skill-box"><strong>Analyse</strong>Géopolitique & OSINT</div>
        <div class="skill-box"><strong>Cartographie</strong>QGIS & Illustrator</div>
        <div class="skill-box"><strong>Outils SIG</strong>ArcGIS / QGIS</div>
        <div class="skill-box"><strong>Bureautique</strong>Suite Office</div>
      </div>

      <h2 style="margin-top: 40px;">Maîtrise des Langues</h2>
      <div class="card">
        <div class="lang-row"><span>Français</span><span style="color:var(--accent); font-weight:bold;">C2+</span></div>
        <div class="lang-row"><span>Anglais</span><span style="color:var(--accent); font-weight:bold;">C2</span></div>
        <div class="lang-row"><span>Polonais</span><span style="color:var(--accent); font-weight:bold;">B1-B2</span></div>
        <div class="lang-row" style="border:none;"><span>Espagnol</span><span style="color:var(--accent); font-weight:bold;">B1</span></div>
      </div>

      <h2 style="margin-top: 40px;">Centres d'intérêt</h2>
      <div class="card" style="text-align: center;">
        <span class="interest-tag">Actualité Géopolitique</span>
        <span class="interest-tag">Histoire Européenne</span>
        <span class="interest-tag">Musique</span>
        <span class="interest-tag">Basket-ball</span>
        <span class="interest-tag">Fitness</span>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2026 Nicolas Decroix | Analyste Géopolitique</p>
  </footer>

  <script>
    function switchTab(id) {
      // 1. Gestion des panneaux
      document.querySelectorAll('.tab-pane').forEach(p => {
        p.classList.remove('active');
        p.style.display = 'none';
      });
      
      // 2. Gestion des boutons
      document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
      
      // 3. Activation
      const target = document.getElementById(id);
      if(target) {
        target.style.display = 'block';
        setTimeout(() => target.classList.add('active'), 10);
        
        // --- MISE À JOUR DE L'ONGLET NAVIGATEUR ---
        const titles = {
          'home': 'Présentation',
          'parcours': 'Parcours',
          'recherche': 'Recherche',
          'skills': 'Compétences'
        };
        document.title = titles[id] + " | Portfolio";
      }
      
      const btn = Array.from(document.querySelectorAll('.nav-btn')).find(b => b.getAttribute('onclick').includes(id));
      if(btn) btn.classList.add('active');

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
    window.onload = () => switchTab('home');
  </script>
</body>
</html>
