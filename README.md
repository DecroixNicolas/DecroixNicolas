<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nicolas Decroix | Portfolio Analyste</title>
  <style>
    :root {
      --bg-dark: #0f172a;
      --sidebar-bg: #1e293b;
      --card-bg: #1e293b;
      --accent: #38bdf8;
      --text-main: #f1f5f9;
      --text-dim: #94a3b8;
      --border: #334155;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      overflow: hidden; /* Fixe la structure globale */
    }

    /* SIDEBAR CORRIGÉE */
    .sidebar {
      position: fixed;
      top: 0;
      left: 0;
      width: 280px;
      height: 100vh;
      background: var(--sidebar-bg);
      padding: 40px 20px;
      border-right: 1px solid var(--border);
      z-index: 100;
      display: flex;
      flex-direction: column;
    }

    .sidebar h1 { font-size: 20px; color: var(--accent); margin-bottom: 5px; }
    .sidebar .status { font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--text-dim); margin-bottom: 40px; }

    .nav-btn {
      display: block;
      width: 100%;
      padding: 12px 15px;
      margin-bottom: 10px;
      color: var(--text-dim);
      background: rgba(255,255,255,0.03);
      border: 1px solid transparent;
      border-radius: 6px;
      text-align: left;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    .nav-btn:hover { border-color: var(--accent); color: var(--accent); }
    .nav-btn.active { background: var(--accent); color: var(--bg-dark); }

    .sidebar-footer { margin-top: auto; padding-top: 20px; border-top: 1px solid var(--border); }
    .linkedin-link {
      display: inline-block;
      text-decoration: none;
      color: var(--accent);
      font-size: 13px;
      font-weight: bold;
      border: 1px solid var(--accent);
      padding: 6px 12px;
      border-radius: 4px;
      transition: 0.3s;
    }
    .linkedin-link:hover { background: var(--accent); color: var(--bg-dark); }

    /* CONTENU PRINCIPAL AVEC MARGE DE SÉCURITÉ */
    .main-content {
      margin-left: 280px;
      height: 100vh;
      overflow-y: auto;
      padding: 40px 40px 120px 40px; /* 120px en bas pour éviter que le texte soit caché */
    }

    .tab-pane { display: none; }
    .tab-pane.active { display: block; animation: fadeIn 0.4s ease; }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; } }

    h2 { font-size: 24px; margin-bottom: 30px; border-left: 4px solid var(--accent); padding-left: 15px; color: var(--text-main); }

    /* CARTES */
    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 25px;
      margin-bottom: 25px;
    }

    .exp-header { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 10px; }
    .exp-title { font-weight: 700; color: var(--accent); font-size: 18px; }
    .exp-date { font-size: 11px; color: var(--text-dim); font-weight: bold; text-transform: uppercase; }
    .exp-org { color: var(--text-main); font-size: 15px; font-weight: 600; margin-bottom: 15px; display: block; }

    ul { margin-left: 20px; color: var(--text-dim); font-size: 14px; }
    li { margin-bottom: 8px; }

    /* LANGUES BADGES */
    .lang-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 10px; margin-top: 15px; }
    .lang-badge { background: var(--bg-dark); border: 1px solid var(--border); padding: 10px; border-radius: 6px; text-align: center; }
    .lang-level { color: var(--accent); font-weight: bold; font-size: 12px; display: block; }

    /* SECTION MÉMOIRE */
    .pdf-frame { width: 100%; height: 600px; border-radius: 8px; border: 1px solid var(--border); background: #000; }
    .image-gallery { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
      gap: 15px; 
      margin-top: 20px;
    }
    .image-gallery img { width: 100%; border-radius: 6px; border: 1px solid var(--border); cursor: zoom-in; }

    @media (max-width: 1024px) {
      .sidebar { width: 100%; height: auto; position: relative; }
      .main-content { margin-left: 0; padding: 20px; height: auto; overflow: visible; }
      body { overflow-y: auto; }
    }
  </style>
</head>
<body>

  <aside class="sidebar">
    <h1>Nicolas Decroix</h1>
    <div class="status">Analyste Géopolitique & Défense</div>
    
    <nav>
      <button class="nav-btn active" onclick="switchTab('exps')">💼 Parcours & Stages</button>
      <button class="nav-btn" onclick="switchTab('recherche')">📚
