<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Géopolitique & Défense</title>
  <style>
    /* RESET ET STYLE SYSTÈME */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #0f172a;
      color: #f1f5f9;
      line-height: 1.6;
      overflow-x: hidden; /* Empêche le scroll horizontal parasite */
    }
    .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; }
    
    /* HEADER */
    header { border-bottom: 1px solid #1e293b; padding-bottom: 30px; margin-bottom: 40px; }
    h1 { font-size: 42px; color: #38bdf8; letter-spacing: -1px; }
    .subtitle { font-size: 18px; color: #f472b6; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; }
    .contact-info { margin-top: 15px; font-size: 14px; color: #94a3b8; }
    
    .nav-btns { display: flex; gap: 12px; margin-top: 25px; flex-wrap: wrap; }
    .btn { text-decoration: none; padding: 10px 22px; border-radius: 6px; font-size: 13px; font-weight: 700; transition: 0.3s; text-transform: uppercase; }
    .btn-blue { background: #38bdf8; color: #0f172a; }
    .btn-outline { border: 1px solid #334155; color: #f1f5f9; }
    .btn:hover { transform: translateY(-3px); box-shadow: 0 4px 12px rgba(56, 189, 248, 0.2); }

    /* SECTIONS */
    section { margin-bottom: 60px; }
    h2 { font-size: 24px; color: #38bdf8; margin-bottom: 35px; border-left: 4px solid #f472b6; padding-left: 15px; }

    /* TIMELINE ÉDUCATION */
    .timeline { position: relative; max-width: 850px; margin: 0 auto; padding-left: 40px; }
    .timeline::after { content: ''; position: absolute; width: 2px; background-color: #1e293b; top: 0; bottom: 0; left: 7px; }
    .timeline-item { position: relative; margin-bottom: 35px; }
    .timeline-item::before {
      content: ''; position: absolute; width: 14px; height: 14px; left: -40px; 
      background-color: #0f172a; border: 3px solid #f472b6; border-radius: 50%; z-index: 1; top: 6px;
    }
    .timeline-date { font-weight: 700; color: #f472b6; font-size: 14px; margin-bottom: 5px; display: block; }
    .timeline-content { background: #1e293b; padding: 20px; border-radius: 8px; border: 1px solid #334155; transition: 0.3s; }
    .timeline-content:hover { border-color: #38bdf8; }
    .timeline-content h3 { color: #38bdf8; font-size: 18px; margin-bottom: 5px; }
    .timeline-content p { font-size: 14px; color: #94a3b8; }

    /* SECTION MÉMOIRE - TABLEAU DE BORD */
    .research-card { background: #1e293b; border: 1px solid #334155; border-radius: 12px; padding: 25px; }
    .research-grid { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 20px; margin-top: 20px; }
    
    /* Fenêtre PDF (PC) */
    .pdf-window { background: #000; border-radius: 6px; height: 480px; overflow: hidden; border: 1px solid #334155; }
    .pdf-window iframe { width: 100%; height: 100%; border: none; }
    
    /* Galerie de cartes (PC : Vertical à droite) */
    .visual-gallery { display: flex; flex-direction: column; gap: 10px; }
    .visual-gallery a img { width: 100%; border-radius: 4px; border: 1px solid #334155; transition: 0.3s; height: 153px; object-fit: cover; }
    .visual-gallery a img:hover { border-color: #38bdf8; transform: scale(1.02); }

    /* SKILLS ET EXPS */
    .skills-bar { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; margin-top: 30px; }
    .skill-tag { background: #1a2233; border: 1px solid #334155; padding: 15px; border-radius: 6px; text-align: center; border-bottom: 3px solid #f472b6; }
    .skill-tag strong { color: #38bdf8; display: block; font-size: 14px; margin-bottom: 5px; }
    .skill-tag span { font-size: 12px; color: #94a3b8; }

    footer { text-align: center; color: #475569; font-size: 12px; margin-top: 80px; padding: 40px 0; border-top: 1px solid #1e293b; }

    /* =========================================
       CORRECTION RESPONSIVE (TÉLÉPHONE)
       ========================================= */
    @media (max-width: 850px) {
      .container { padding: 30px 15px; }
      h1 { font-size: 30px; }
      .timeline { padding-left: 30px; }
      
      /* 1. Stack vertical pour le Mémoire */
      .research-grid { grid-template-columns: 1fr; gap: 15px; }
      
      /* 2. Réduction hauteur PDF sur mobile */
      .pdf-window { height: 350px; }
      
      /* 3. TRANSFORMATION DE LA GALERIE D'IMAGES SUR MOBILE */
      .visual-gallery {
        flex-direction: row; /* Aligne les cartes horizontalement */
        overflow-x: auto; /* Active le défilement horizontal */
        padding-bottom: 10px; /* Espace pour la barre de défilement */
        gap: 8px; /* Réduit l'espace entre les cartes */
        -webkit-overflow-scrolling: touch; /* Défilement fluide sur iOS */
      }
      
      /* 4. Fixe la taille des cartes dans le bandeau horizontal */
      .visual-gallery a {
        width: 160px; /* Largeur fixe pour chaque carte */
        flex-shrink: 0; /* Empêche les cartes de rétrécir */
        height: 120px; /* Hauteur ajustée */
      }
      
      .visual-gallery a img {
        height: 100%; /* L'image remplit son conteneur fixe */
      }
      
      /* Masque le texte d'aide sur mobile (inutile avec le scroll) */
      .visual-gallery p { display: none; }
    }
  </style>
</head>
<body>

<div class="container">
  <header>
    <h1>Nicolas Decroix</h1>
    <p class="subtitle">Analyste Géopolitique & Défense | Flanc Est & OTAN</p>
    <p class="contact-info">📍 Paris, France | 📧 decroix.nicolasfrancois@gmail.com | 📞 +33 (0)7 69 28 30 80</p>
    <div class="nav-btns">
      <a href="CV DECROIX Nicolas.pdf" target="_blank" class="btn btn-blue">📄 Mon CV PDF</a>
      <a href="mailto:decroix.nicolasfrancois@gmail.com" class="btn btn-outline">📧 Contact</a>
      <a href="https://linkedin.com/in/nicolas-decroix" target="_blank" class="btn btn-outline">🔗 LinkedIn</a>
    </div>
  </header>

  <section>
    <h2>🎓 Cursus Académique</h2>
    <div class="timeline">
      
      <div class="timeline-item">
        <span class="timeline-date">2024 — 2026</span>
        <div class="timeline-content">
          <h3>Master de Géopolitique</h3>
          <p><strong>Institut Français de Géopolitique (IFG) - Université Paris-VIII</strong></p>
          <p>Spécialisation : Nouveaux Acteurs de la Compétition Stratégique. Recherche approfondie sur le Flanc Est européen.</p>
        </div>
      </div>

      <div class="timeline-item">
        <span class="timeline-date">2021 — 2024</span>
        <div class="timeline-content">
          <h3>Double Licence Histoire & Géographie</h3>
          <p><strong>Université Jean Moulin Lyon-III</strong></p>
          <p>Mention Bien pour les deux cursus. Maîtrise de l'analyse spatiale et du temps long historique.</p>
        </div>
      </div>

      <div class="timeline-item">
        <span class="timeline-date">2020 — 2021</span>
        <div class="timeline-content">
          <h3>Baccalauréat Mention Très Bien</h3>
          <p><strong>Institution des Chartreux (Lyon)</strong></p>
          <p>Spécialités Mathématiques et HGGSP.</p>
        </div>
      </div>

      <div class="timeline-item">
        <span class="timeline-date">2016 — 2020</span>
        <div class="timeline-content">
          <h3>Lycée Français de Varsovie (Pologne)</h3>
          <p>Immersion culturelle et linguistique internationale.</p>
        </div>
      </div>

    </div>
  </section>

  <section>
    <h2>📚 Recherche : Kaliningrad & Bouclier Oriental</h2>
    <div class="research-card">
      <div style="margin-bottom: 15px;">
        <h3 style="color: #f1f5f9; font-size: 18px;">La Pologne et l'exclave de Kaliningrad : nouvelles réalités frontalières</h3>
        <p style="font-size: 14px; color: #94a3b8; margin-top: 5px;">
          Validé avec <strong>17/20</strong>. Terrain en Pologne, interviews et analyse OSINT.
        </p>
      </div>
      
      <div class="research-grid">
        <div class="pdf-window">
          <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
        </div>
        
        <div class="visual-gallery">
          <a href="carte-nationale.jpg" target="_blank" title="Agrandir"><img src="carte-nationale.jpg" alt="Carte 1"></a>
          <a href="Carte-Région.png" target="_blank" title="Agrandir"><img src="Carte-Région.png" alt="Carte 2"></a>
          <a href="Carte-Varmie.png" target="_blank" title="Agrandir"><img src="Carte-Varmie.png" alt="Carte 3"></a>
          <p style="font-size: 11px; color: #f472b6; text-align: center; font-weight: bold; margin-top: 5px;">↖ CARTOGRAPHIE SIG</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <h2>💼 Expériences</h2>
    <div class="skills-bar" style="grid-template-columns: 1fr 1fr; border-bottom: none;">
      <div class="skill-tag" style="text-align: left;">
        <span style="color: #f472b6; font-size: 12px; font-weight: bold;">Novembre 2024 — Décembre 2025</span>
        <strong>Assistant de la Secrétaire Générale</strong>
        <p style="font-size: 13px;">ERUA (Paris-VIII) : Analyses et rapports en anglais (C2).</p>
      </div>
      <div class="skill-tag" style="text-align: left;">
        <span style="color: #f472b6; font-size: 12px; font-weight: bold;">ÉTÉ 2023</span>
        <strong>Stagiaire Recherche (CNRS)</strong>
        <p style="font-size: 13px;">Programme 13-Novembre : Analyse de témoignages et confidentialité.</p>
      </div>
    </div>
  </section>

  <section>
    <h2>🛠 Expertises</h2>
    <div class="skills-bar">
      <div class="skill-tag">
        <strong>Langues</strong>
        <span>Anglais (C2), Polonais (B1-B2), Espagnol (B1)</span>
      </div>
      <div class="skill-tag">
        <strong>Outils SIG</strong>
        <span>QGIS, ArcGIS, Adobe Illustrator</span>
      </div>
      <div class="skill-tag">
        <strong>Méthodologie</strong>
        <span>OSINT, Veille stratégique, Terrain</span>
      </div>
    </div>
  </section>

  <footer>
    <p>Nicolas Decroix — 2026 — Analyste Géopolitique & Défense</p>
  </footer>

</div>

</body>
</html>
