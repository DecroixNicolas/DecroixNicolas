<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Analyste</title>
  <style>
    :root {
      --bg-dark: #0f172a;        /* Fond principal */
      --sidebar-bg: #1e293b;    /* Fond menu */
      --card-bg: #1e293b;       /* Fond cartes */
      --accent: #38bdf8;        /* Bleu info */
      --text-main: #f1f5f9;     /* Texte blanc cassé */
      --text-dim: #94a3b8;      /* Texte gris */
      --border: #334155;        /* Bordures discrètes */
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      overflow: hidden; /* Dashboard fixe */
    }

    /* NAVIGATION LATÉRALE RÉGLÉE */
    .sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: 280px;
      height: 100%;
      background: var(--sidebar-bg);
      padding: 40px 20px;
      border-right: 1px solid var(--border);
      z-index: 100;
    }

    .sidebar h1 { font-size: 20px; color: var(--accent); margin-bottom: 5px; }
    .sidebar .status { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--text-dim); margin-bottom: 40px; }

    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px 15px;
      margin-bottom: 10px;
      color: var(--text-dim);
      background: transparent;
      border: none;
      border-radius: 6px;
      text-align: left;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
    }
    .nav-btn.active, .nav-btn:hover { background: var(--bg-dark); color: var(--accent); }

    /* ZONE DE CONTENU DÉCALÉE POUR NE PAS MASQUER LE TITRE */
    .main-content {
      margin-left: 280px; /* Largeur de la sidebar */
      height: 100vh;
      padding: 40px;
      overflow-y: auto;
    }

    .tab-pane { display: none; animation: fadeIn 0.3s ease; }
    .tab-pane.active { display: block; }

    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    h2 { font-size: 22px; margin-bottom: 25px; border-left: 4px solid var(--accent); padding-left: 15px; }

    /* CARTES EXPÉRIENCES */
    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 25px;
      margin-bottom: 20px;
    }

    .exp-header { display: flex; justify-content: space-between; margin-bottom: 10px; }
    .exp-title { font-weight: bold; color: var(--accent); font-size: 17px; }
    .exp-date { font-size: 12px; color: var(--text-dim); }
    .exp-org { color: var(--text-main); font-size: 14px; font-weight: 600; display: block; margin-bottom: 10px; }

    ul { margin-left: 20px; color: var(--text-dim); font-size: 14px; }
    li { margin-bottom: 6px; }

    /* GRILLE IMAGES MÉMOIRE */
    .memory-grid {
      display: grid;
      grid-template-columns: 1.5fr 1fr;
      gap: 20px;
      margin-top: 20px;
    }
    .pdf-box { height: 600px; border-radius: 4px; overflow: hidden; background: #000; }
    .img-gallery { display: flex; flex-direction: column; gap: 15px; }
    .img-gallery img { width: 100%; border-radius: 4px; border: 1px solid var(--border); filter: grayscale(20%); transition: 0.3s; }
    .img-gallery img:hover { filter: grayscale(0%); border-color: var(--accent); }

    /* RESPONSIVE */
    @media (max-width: 1024px) {
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { margin-left: 0; padding: 20px; height: auto; }
      body { overflow-y: auto; }
      .memory-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <div class="status">Analyste Géopolitique & Défense</div>
    
    <nav>
      <button class="nav-btn active" onclick="showTab(event, 'exps')">💼 Parcours & Stages</button>
      <button class="nav-btn" onclick="showTab(event, 'recherche')">📚 Mémoire & Cartes</button>
      <button class="nav-btn" onclick="showTab(event, 'skills')">🛠 Compétences</button>
      <button class="nav-btn" onclick="showTab(event, 'formation')">🎓 Formation</button>
    </nav>

    <div style="position: absolute; bottom: 30px; font-size: 12px; color: var(--text-dim);">
      📍 Paris, France<br>
      📞 +33 (0)7 69 28 30 80
    </div>
  </aside>

  <main class="main-content">
    
    <div id="exps" class="tab-pane active">
      <h2>Parcours Professionnel & Stages</h2>
      
      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Student Assistant to the Secretary General</span>
          <span class="exp-date">Nov. 2024 — Déc. 2025</span>
        </div>
        <span class="exp-org">European Reform Universities Alliance (ERUA) - Paris-VIII</span>
        <ul>
          <li>Rapports analytiques de documents européens sur l’éducation pour la secrétaire générale.</li>
          <li>Création de présentations et d’ateliers de comité de pilotage.</li>
          <li>Analyse d’assurance qualité et d’impact de l’alliance.</li>
          <li>Organisation et vérification de conformité sur les bases de données collaboratives.</li>
          <li>Réunions et productions réalisées intégralement en anglais pour les partenaires européens.</li>
          <li>Veille sur les évènements européens du secteur de l’éducation.</li>
        </ul>
      </div>

      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Stagiaire Recherche - Programme 13-Novembre</span>
          <span class="exp-date">Juillet — Août 2023</span>
        </div>
        <span class="exp-org">CNRS - Equipex MATRICE</span>
        <ul>
          <li>Transcription de témoignages de victimes des attentats de 2015 et de déportés français.</li>
          <li>Suivi rigoureux du vade-mecum de transcription.</li>
          <li>Respect strict des protocoles et de la clause de confidentialité.</li>
        </ul>
      </div>

      <div class="card">
        <div class="exp-header">
          <span class="exp-title">Stagiaire au service Urbanisme</span>
          <span class="exp-date">Juillet — Août 2022</span>
        </div>
        <span class="exp-org">Mairie de Caluire-et-Cuire</span>
        <ul>
          <li>Travail de recherche pour l'implantation de mode de production d'énergie solaire sur la ville.</li>
          <li>Rédaction de notes et rapports à destination du maire.</li>
          <li>Utilisation intensive de SIG : ArcGIS, QGIS.</li>
        </ul>
      </div>
    </div>

    <div id="recherche" class="tab-pane">
      <h2>Mémoire : Kaliningrad & Frontière Russo-Polonaise</h2>
      <div class="card">
        <p style="margin-bottom: 20px;"><strong>Sujet :</strong> La militarisation de la frontière et les nouvelles réalités géopolitiques de l'exclave. Travail récompensé par la note de <strong>17/20</strong>.</p>
        
        <div class="memory-grid">
          <div class="pdf-box">
            <iframe src="https://drive.google.com/file/d/1biwjkTJpX5jVcjh5E2IlDCJIIUYt-F4T/preview" width="100%" height="100%" style="border:none;"></iframe>
          </div>
          <div class="img-gallery">
            <img src="carte-nationale.jpg" alt="Carte SIG 1">
            <img src="Carte-Rég
