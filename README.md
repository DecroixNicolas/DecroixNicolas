<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Géopolitique</title>
  <style>
    :root {
      --bg-dark: #0f172a;
      --sidebar-bg: #1e293b;
      --accent-blue: #38bdf8;
      --accent-pink: #f472b6;
      --text-main: #f1f5f9;
      --text-dim: #94a3b8;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* BOUTON MENU */
    .menu-btn {
      position: fixed;
      top: 20px;
      left: 20px;
      z-index: 1001;
      background: var(--sidebar-bg);
      border: 1px solid #334155;
      padding: 12px;
      border-radius: 8px;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      gap: 5px;
    }
    .menu-btn span { display: block; width: 22px; height: 2px; background: var(--accent-blue); }

    /* SIDEBAR */
    .sidebar {
      position: fixed;
      top: 0;
      left: -280px;
      width: 280px;
      height: 100%;
      background: var(--sidebar-bg);
      z-index: 1000;
      transition: 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      padding: 100px 20px 20px;
      border-right: 1px solid #334155;
    }
    .sidebar.open { left: 0; }

    .nav-item {
      display: block;
      width: 100%;
      padding: 14px 18px;
      margin-bottom: 8px;
      color: var(--text-dim);
      background: transparent;
      border: none;
      border-radius: 8px;
      text-align: left;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
    }
    .nav-item.active { background: var(--bg-dark); color: var(--accent-blue); }

    /* CONTENU */
    .content-area { padding: 60px 20px; max-width: 1100px; margin: 0 auto; transition: 0.4s; }
    
    .tab-pane { display: none; animation: fadeIn 0.4s; }
    .tab-pane.active { display: block; }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    h2 { font-size: 24px; border-left: 4px solid var(--accent-pink); padding-left: 15px; margin-bottom: 30px; color: var(--accent-blue); }
    
    .card {
      background: var(--sidebar-bg);
      border: 1px solid #334155;
      border-radius: 12px;
      padding: 25px;
      margin-bottom: 25px;
    }

    .exp-title { color: var(--accent-blue); font-size: 18px; margin-bottom: 5px; }
    .exp-meta { color: var(--accent-pink); font-size: 13px; font-weight: bold; margin-bottom: 10px; display: block; }
    
    ul { margin-left: 20px; color: var(--text-dim); font-size: 14px; }
    li { margin-bottom: 5px; }

    .lang-list { list-style: none; margin-left: 0; display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 10px; }
    .lang-item { background: var(--bg-dark); padding: 10px; border-radius: 6px; border: 1px solid #334155; text-align: center; }

    .overlay { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.6); z-index: 999; }
    .overlay.active { display: block; }
  </style>
</head>
<body id="mainBody">

  <button class="menu-btn" onclick="toggleMenu()"><span></span><span></span><span></span></button>
  <div class="overlay" id="overlay" onclick="toggleMenu()"></div>

  <nav class="sidebar" id="sidebar">
    <button class="nav-item active" onclick="switchTab(event, 'exps')">💼 Expériences</button>
    <button class="nav-item" onclick="switchTab(event, 'parcours')">🎓 Cursus</button>
    <button class="nav-item" onclick="switchTab(event, 'skills')">🛠 Compétences</button>
    <button class="nav-item" onclick="switchTab(event, 'recherche')">📚 Recherche</button>
  </nav>

  <main class="content-area">
    
    <div id="exps" class="tab-pane active">
      <h2>Expériences Professionnelles</h2>
      
      <div class="card">
        <span class="exp-meta">Novembre 2024 — Décembre 2025</span>
        <h3 class="exp-title">Student Assistant to the Secretary General</h3>
        <p style="font-size: 14px; margin-bottom: 10px;"><strong>European Reform Universities Alliance (ERUA)</strong> - Université Paris-VIII</p>
        <ul>
          <li>Rapports analytiques de documents européens sur l'éducation pour la secrétaire générale</li>
          <li>Création de présentations et d'ateliers de comité de pilotage</li>
          <li>Analyse d'assurance qualité et d'impact de l'alliance</li>
          <li>Organisation et vérification de conformité sur les bases de données collaboratives</li>
          <li>Réunions et productions réalisées intégralement en anglais à destination des partenaires européens</li>
          <li>Veille sur les évèn
