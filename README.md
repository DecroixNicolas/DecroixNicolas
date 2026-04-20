<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Géopolitique & Défense</title>
  <style>
    /* STYLE SANS TRACKING - FONTS SYSTÈME */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #0f172a;
      color: #f1f5f9;
      line-height: 1.6;
    }
    .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; }
    
    /* EN-TÊTE PROFESSIONNEL */
    header { border-bottom: 1px solid #1e293b; padding-bottom: 30px; margin-bottom: 40px; }
    h1 { font-size: 42px; color: #38bdf8; letter-spacing: -1px; }
    .subtitle { font-size: 18px; color: #f472b6; font-weight: 600; margin-top: 5px; text-transform: uppercase; letter-spacing: 1px; }
    .contact-info { margin-top: 15px; font-size: 14px; color: #94a3b8; }
    
    .nav-btns { display: flex; gap: 12px; margin-top: 25px; flex-wrap: wrap; }
    .btn { text-decoration: none; padding: 10px 22px; border-radius: 6px; font-size: 14px; font-weight: 600; transition: 0.3s; }
    .btn-blue { background: #38bdf8; color: #0f172a; }
    .btn-outline { border: 1px solid #334155; color: #f1f5f9; }
    .btn:hover { transform: translateY(-3px); box-shadow: 0 4px 12px rgba(56, 189, 248, 0.2); }

    /* SECTIONS */
    section { margin-bottom: 60px; }
    h2 { font-size: 24px; color: #38bdf8; margin-bottom: 25px; border-left: 4px solid #f472b6; padding-left: 15px; }

    /* BLOC MÉMOIRE - LE "POSTE DE COMMANDE" */
    .research-card { background: #1e293b; border: 1px solid #334155; border-radius: 12px; padding: 30px; }
    .research-header { margin-bottom: 20px; }
    .research-grid { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 25px; align-items: start; }
    
    /* Fenêtre PDF */
    .pdf-window { 
      background: #000; border-radius: 8px; border: 1px solid #334155; height: 480px; overflow: hidden; 
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }
    .pdf-window iframe { width: 100%; height: 100%; border: none; }

    /* Galerie de cartes */
    .visual-gallery { display: flex; flex-direction: column; gap: 12px; }
    .visual-gallery a { 
      display: block; border-radius: 6px; overflow: hidden; border: 1px solid #334155; height: 152px; 
      transition: 0.3s; cursor: zoom-in;
    }
    .visual-gallery img { width: 100%; height: 100%; object-fit: cover; }
    .visual-gallery a:hover { border-color: #38bdf8; transform: scale(1.02); }

    /* EXPÉRIENCES & FORMATION */
    .info-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
    .card { background: #1e293b; border: 1px solid #334155; border-radius: 8px; padding: 20px; transition: 0.3s; }
    .card:hover { border-color: #f472b6; }
    .card-top { display: flex; justify-content: space-between; font-size: 13px; margin-bottom: 5px; }
    .date { color: #f472b6; font-weight: 600; }
    .org { color: #38bdf8; font-weight: 600; display: block; margin-bottom: 10px; }
    .content { font-size: 14px; color: #94a3b8; }
    .content ul { padding-left: 15px; margin-top: 10px; }

    /* SKILLS */
    .skills-bar { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; margin-top: 20px; }
    .skill-tag { background: #0f172a; border: 1px solid #334155; padding: 15px; border-radius: 6px; text-align: center; }
    .skill-tag strong { color: #38bdf8; display: block; font-size: 14px; margin-bottom: 5px; }
    .skill-tag span { font-size: 12px; color: #94a3b8; }

    footer { text-align: center; color: #475569; font-size: 12px; margin-top: 80px; padding: 40px 0; border-top: 1px solid #1e293b; }

    @media (max-width: 850px) {
      .research-grid { grid-template-columns: 1fr; }
      .pdf-window { height: 400px; }
      .visual-gallery { flex-direction: row; overflow-x: auto; padding-bottom: 10px; }
      .visual-gallery a { width: 180px; flex-shrink: 0; }
    }
  </style>
</head>
<body>

<div class="container">
  <header>
    <h1>Nicolas Decroix</h1>
    <p class="subtitle">Analyste Géopolitique & Défense | Flanc Est & OTAN</p>
    <p class="contact-info">📍 Paris / Nord | 📧 decroix.nicolasfrancois@gmail.com | 📞 +33 7 69 28 30 80</p>
    <div class="nav-btns">
      <a href="CV DECROIX Nicolas.pdf" target="_blank" class="btn btn-blue">📄 Télécharger CV (PDF)</a>
      <a href="https://linkedin.com/in/nicolas-decroix" target="_blank" class="btn btn-outline">🔗 LinkedIn</a>
      <a href="https://github.com/DecroixNicolas" target="_blank" class="btn btn-outline">💻 GitHub / SIG</a>
    </div>
  </header>

  <section>
    <h2>📚 Travaux de Recherche (IFG)</h2>
    <div class="research-card">
      <div class="research-header">
        <h3 style="font-size: 20px; color: #f1f5f9;">La Pologne et l'exclave de Kaliningrad : le projet Bouclier Oriental</h3>
        <p style="color: #94a3b8; font-size: 14px; margin-top: 5px;">Mémoire de Master 1 validé avec la note de <strong>17/20</strong></p>
      </div>
      
      <div class="research-grid">
        <div class="pdf-window">
          <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview"></iframe>
        </div>
        
        <div class="visual-gallery">
          <a href="carte-nationale.jpg" target="_blank" title="Voir la carte nationale">
            <img src="carte-nationale.jpg" alt="Carte Nationale">
          </a>
          <a href="Carte-Région.png" target="_blank" title="Voir l'analyse régionale">
            <img src="Carte-Région.png" alt="Carte Régionale">
          </a>
          <a href="Carte-Varmie.png" target="_blank" title="Voir le détail Varmie-Mazurie">
            <img src="Carte-Varmie.png" alt="Carte Varmie">
          </a>
          <div style="text-align: center; padding-top: 5px;">
            <p style="font-size: 11px; color: #f472b6; font-weight: 600;">↖ Cliquez sur les cartes pour zoomer</p>
          </div>
        </div>
      </div>
      <div style="margin-top: 20px; font-size: 14px; color: #94a3b8;">
        <p><strong>Méthodologie :</strong> Un mois d'enquête de terrain en Pologne, interviews d'acteurs politiques et militaires, analyse de sources ouvertes (OSINT).</p>
      </div>
    </div>
  </section>

  <section>
    <h2>💼 Parcours Professionnel & Académique</h2>
    <div class="info-grid">
      
      <div class="card">
        <div class="card-top"><span class="date">2024 — Présent</span></div>
        <span class="org">European Reform Universities Alliance (ERUA)</span>
        <div class="content">
          <strong>Assistant de la Secrétaire Générale</strong>
          <ul>
            <li>Analyses stratégiques des politiques éducatives de l'UE.</li>
            <li>Rédaction de rapports en anglais (C2).</li>
          </ul>
        </div>
      </div>

      <div class="card">
        <div class="card-top"><span class="date">Été 2023</span></div>
        <span class="org">CNRS - Programme 13-Novembre</span>
        <div class="content">
          <strong>Stagiaire Recherche</strong>
          <p>Transcription et analyse de témoignages (victimes attentats/déportés). Respect strict de la confidentialité.</p>
        </div>
      </div>

      <div class="card">
        <div class="card-top"><span class="date">2024 — 2026</span></div>
        <span class="org">Institut Français de Géopolitique</span>
        <div class="content">
          <strong>Master Géopolitique (NACS)</strong>
          <p>Spécialisation : Nouveaux Acteurs de la Compétition Stratégique. Focus : Flanc Est et défense européenne.</p>
        </div>
      </div>

      <div class="card">
        <div class="card-top"><span class="date">2021 — 2024</span></div>
        <span class="org">Université Jean Moulin Lyon-III</span>
        <div class="content">
          <strong>Double Licence Histoire & Géographie</strong>
          <p>Mention Bien pour les deux cursus. Solides bases en analyse spatiale et temps long.</p>
        </div>
      </div>

    </div>
  </section>

  <section>
    <h2>🛠 Expertises Techniques</h2>
    <div class="skills-bar">
      <div class="skill-tag">
        <strong>Cartographie & SIG</strong>
        <span>QGIS, ArcGIS, Adobe Illustrator</span>
      </div>
      <div class="skill-tag">
        <strong>Analyse Stratégique</strong>
        <span>OSINT, Veille défense, Enquêtes terrain</span>
      </div>
      <div class="skill-tag">
        <strong>Langues</strong>
        <span>Anglais (C2), Polonais (B1-B2), Espagnol (B1)</span>
      </div>
      <div class="skill-tag">
        <strong>Publications</strong>
        <span>Diploweb, Éditions du Nouveau Monde</span>
      </div>
    </div>
  </section>

  <footer>
    <p>Nicolas Decroix — Portfolio Analyste Géopolitique — 2026</p>
    <p style="margin-top: 5px; opacity: 0.5;">Hébergé via GitHub Pages - Design optimisé pour le recrutement</p>
  </footer>
</div>

</body>
</html>
