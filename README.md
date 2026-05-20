<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CV - Karim Richard Clain</title>
  <style>
    :root {
      --dark: #152238;
      --blue: #3a86ff;
      --purple: #8338ec;
      --yellow: #ffb703;
      --cream: #f7f3ea;
      --white: #ffffff;
      --text-soft: rgba(21, 34, 56, 0.75);
      --radius: 28px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--cream);
      color: var(--dark);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .page {
      position: relative;
      min-height: 100vh;
      padding: 40px 24px;
      overflow: hidden;
    }

    .blob {
      position: absolute;
      border-radius: 50%;
      filter: blur(70px);
      opacity: 0.45;
      z-index: 0;
    }

    .blob-yellow {
      width: 320px;
      height: 320px;
      background: var(--yellow);
      left: -120px;
      top: -120px;
    }

    .blob-blue {
      width: 320px;
      height: 320px;
      background: var(--blue);
      right: -120px;
      top: 90px;
    }

    .blob-purple {
      width: 400px;
      height: 400px;
      background: var(--purple);
      left: 35%;
      bottom: -180px;
      opacity: 0.2;
    }

    .container {
      position: relative;
      z-index: 1;
      max-width: 1150px;
      margin: auto;
    }

    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      padding: 16px;
      margin-bottom: 38px;
      border-radius: var(--radius);
      background: rgba(255, 255, 255, 0.68);
      border: 1px solid rgba(255, 255, 255, 0.8);
      box-shadow: 0 10px 35px rgba(21, 34, 56, 0.08);
      backdrop-filter: blur(12px);
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .brand-icon {
      width: 48px;
      height: 48px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 18px;
      background: var(--dark);
      color: white;
      font-size: 22px;
    }

    .brand-label {
      font-size: 12px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      color: var(--blue);
    }

    .brand-name {
      font-weight: 800;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .nav-links a {
      padding: 10px 16px;
      background: white;
      border-radius: 999px;
      font-size: 14px;
      box-shadow: 0 6px 20px rgba(21, 34, 56, 0.08);
      transition: 0.2s ease;
    }

    .nav-links a:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(21, 34, 56, 0.14);
    }

    .hero {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 28px;
      align-items: stretch;
    }

    .hero-main {
      background: var(--dark);
      color: white;
      padding: 48px;
      border-radius: 36px;
      box-shadow: 0 20px 45px rgba(21, 34, 56, 0.2);
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 15px;
      margin-bottom: 24px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.1);
      color: #ffdc7d;
      font-size: 14px;
      font-weight: 700;
    }

    h1 {
      font-size: clamp(42px, 7vw, 78px);
      line-height: 1;
      font-weight: 900;
      max-width: 850px;
    }

    .hero-name-row {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 28px;
    }

    .profile-photo {
      width: 175px;
      height: 175px;
      object-fit: cover;
      border-radius: 26px;
      border: 4px solid rgba(255, 255, 255, 0.18);
      box-shadow: 0 14px 30px rgba(0, 0, 0, 0.22);
      flex-shrink: 0;
    }

    .hero-text {
      margin-top: 26px;
      max-width: 720px;
      font-size: 20px;
      color: rgba(255, 255, 255, 0.82);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      margin-top: 34px;
    }

    .contact-item {
      padding: 14px;
      border-radius: 18px;
      background: rgba(255, 255, 255, 0.1);
      font-size: 14px;
      color: rgba(255, 255, 255, 0.88);
      word-break: break-word;
    }

    .profile-card,
    .card,
    .section-card,
    .quality-card,
    .final-card {
      border-radius: 36px;
      box-shadow: 0 14px 35px rgba(21, 34, 56, 0.1);
    }

    .profile-card {
      padding: 34px;
      background: white;
      border: 1px solid rgba(21, 34, 56, 0.08);
    }

    .small-title {
      margin-bottom: 14px;
      color: var(--purple);
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 13px;
      font-weight: 900;
    }

    .profile-card p {
      font-size: 18px;
      color: var(--text-soft);
    }

    .info-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
      margin-top: 30px;
    }

    .card {
      background: white;
      padding: 28px;
    }

    .icon-box {
      width: 54px;
      height: 54px;
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 18px;
      background: #e7f0ff;
      color: var(--blue);
      font-size: 26px;
    }

    .card h3 {
      margin-top: 8px;
      font-size: 22px;
      font-weight: 900;
    }

    .card p {
      margin-top: 8px;
      color: var(--text-soft);
    }

    .content-grid {
      display: grid;
      grid-template-columns: 0.8fr 1.2fr;
      gap: 28px;
      margin-top: 38px;
    }

    .left-stack,
    .right-stack {
      display: flex;
      flex-direction: column;
      gap: 28px;
    }

    .section-card {
      padding: 34px;
      background: white;
    }

    .section-card h2,
    .quality-card h2 {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 22px;
      font-size: 28px;
      font-weight: 900;
    }

    .skills-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .skill {
      display: flex;
      align-items: flex-start;
      gap: 12px;
      padding: 13px;
      border-radius: 18px;
      background: var(--cream);
    }

    .check {
      color: var(--blue);
      font-weight: 900;
    }

    .quality-card {
      padding: 34px;
      background: var(--yellow);
    }

    .quality-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .quality-tags span {
      padding: 10px 16px;
      background: rgba(255, 255, 255, 0.75);
      border-radius: 999px;
      font-weight: 800;
      font-size: 14px;
    }

    .engagement-box {
      padding: 26px;
      border-radius: 26px;
      background: #f0ebff;
    }

    .engagement-box h3,
    .timeline-item h3 {
      font-size: 20px;
      font-weight: 900;
    }

    .engagement-box p,
    .timeline-item p {
      margin-top: 8px;
      color: var(--text-soft);
    }

    .timeline {
      position: relative;
      display: flex;
      flex-direction: column;
      gap: 28px;
      padding-left: 28px;
      border-left: 2px solid rgba(58, 134, 255, 0.25);
    }

    .timeline-item {
      position: relative;
    }

    .timeline-item::before {
      content: "";
      position: absolute;
      left: -37px;
      top: 8px;
      width: 14px;
      height: 14px;
      border-radius: 50%;
      background: var(--blue);
      box-shadow: 0 0 0 6px #e7f0ff;
    }

    .final-card {
      margin-top: 38px;
      padding: 42px;
      background: var(--dark);
      color: white;
    }

    .final-grid {
      display: grid;
      grid-template-columns: 0.8fr 1.2fr;
      gap: 30px;
      align-items: center;
    }

    .final-card .small-title {
      color: var(--yellow);
    }

    .final-card h2 {
      margin-top: 10px;
      font-size: 38px;
      line-height: 1.1;
      font-weight: 900;
    }

    .final-points {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
    }

    .final-point {
      padding: 22px;
      border-radius: 24px;
      background: rgba(255, 255, 255, 0.1);
      color: rgba(255, 255, 255, 0.85);
    }

    .final-point strong {
      display: block;
      margin-bottom: 10px;
      color: var(--yellow);
      font-size: 22px;
    }

    @media (max-width: 900px) {
      .navbar,
      .hero,
      .info-grid,
      .content-grid,
      .final-grid,
      .final-points {
        grid-template-columns: 1fr;
      }

      .navbar {
        align-items: flex-start;
        flex-direction: column;
      }

      .hero-main {
        padding: 34px;
      }

      .profile-photo {
        width: 140px;
        height: 140px;
        border-radius: 22px;
      }

      .hero-name-row {
        align-items: flex-start;
        justify-content: space-between;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    @media print {
      .page {
        padding: 0;
      }

      .navbar,
      .blob {
        display: none;
      }

      .container {
        max-width: none;
      }

      .hero-main,
      .card,
      .section-card,
      .quality-card,
      .final-card,
      .profile-card {
        box-shadow: none;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <div class="blob blob-yellow"></div>
    <div class="blob blob-blue"></div>
    <div class="blob blob-purple"></div>

    <div class="container">
      <nav class="navbar">
        <div class="brand">
          <div class="brand-icon">✦</div>
          <div>
            <p class="brand-label">CV numérique</p>
            <p class="brand-name">Karim Richard Clain</p>
          </div>
        </div>

        <div class="nav-links">
          <a href="mailto:karim.richardclain@gmail.com">Email</a>
          <a href="tel:+262692716841">Téléphone</a>
          <a href="#experiences">Expériences</a>
        </div>
      </nav>

      <header class="hero">
        <section class="hero-main">
          <p class="tag">🤝 Candidat – Service civique</p>
          <div class="hero-name-row">
            <h1>Karim Richard Clain</h1>
            <img class="profile-photo" src="tete karim.png" alt="Photo de Karim Richard Clain">
          </div>
          <p class="hero-text">
            Accompagnement, inclusion et orientation des étudiants en situation de handicap dans la vie universitaire.
          </p>

          <div class="contact-grid">
            <div class="contact-item">📍 Saint-André, La Réunion</div>
            <div class="contact-item">✉️ karim.richardclain@gmail.com</div>
            <div class="contact-item">📞 06 92 71 68 41</div>
          </div>
        </section>

        <aside class="profile-card">
          <p class="small-title">Profil</p>
          <p>
            Diplômé d’une licence d’anglais, je souhaite m’engager dans une mission utile et humaine centrée sur l’accompagnement des étudiants en situation de handicap. À l’écoute, sérieux et bienveillant, je souhaite contribuer à faciliter leur intégration et leur accès aux services universitaires.
          </p>
        </aside>
      </header>

      <section class="info-grid">
        <article class="card">
          <div class="icon-box">🎓</div>
          <p class="small-title">Formation</p>
          <h3>Licence d’anglais</h3>
          <p>Obtenue en 2026 – Université de La Réunion</p>
          <hr class="mini-separator">
          <h3>BTS SIO</h3>
          <p>Formation suivie de 2021 à 2023 – Lycée Nelson Mandela, Bras-Fusil</p>
          <hr class="mini-separator">
          <h3>Baccalauréat général</h3>
          <p>Obtenu – Options Mathématiques et NSI, Lycée Amiral Bouvet, Saint-Benoît, 2018 à 2021</p>
        </article>

        <article class="card">
          <div class="icon-box">🌍</div>
          <p class="small-title">Langues</p>
          <h3>Français & Anglais</h3>
          <p>Français courant, anglais très bon niveau</p>
        </article>

        <article class="card">
          <div class="icon-box">🧩</div>
          <p class="small-title">Mission visée</p>
          <h3>Inclusion étudiante</h3>
          <p>Faciliter l’insertion des étudiants en situation de handicap</p>
        </article>
      </section>

      <section class="content-grid">
        <div class="left-stack">
          <section class="section-card">
            <h2>📘 Compétences</h2>
            <div class="skills-list">
              <div class="skill"><span class="check">✓</span><span>Accueil et orientation du public</span></div>
              <div class="skill"><span class="check">✓</span><span>Écoute et accompagnement</span></div>
              <div class="skill"><span class="check">✓</span><span>Communication écrite et orale</span></div>
              <div class="skill"><span class="check">✓</span><span>Sens de l’inclusion et de la confidentialité</span></div>
              <div class="skill"><span class="check">✓</span><span>Organisation et rigueur</span></div>
              <div class="skill"><span class="check">✓</span><span>Travail en équipe</span></div>
              <div class="skill"><span class="check">✓</span><span>Aisance en anglais</span></div>
            </div>
          </section>

          <section class="quality-card">
            <h2>✨ Qualités</h2>
            <div class="quality-tags">
              <span>Bienveillant</span>
              <span>Patient</span>
              <span>Organisé</span>
              <span>Adaptable</span>
              <span>Sérieux</span>
              <span>À l’écoute</span>
              <span>Autonome</span>
            </div>
          </section>
        </div>

        <div class="right-stack">
          <section class="section-card">
            <h2>🤝 Projet d’engagement</h2>
            <div class="engagement-box">
              <h3>Service civique – Mission handicap</h3>
              <p>
                Souhait de participer à la facilitation de l’insertion des étudiants en situation de handicap, à leur orientation et à leur accompagnement dans la vie universitaire.
              </p>
            </div>
          </section>

          <section class="section-card" id="experiences">
            <h2>💼 Expériences</h2>
            <div class="timeline">
              <div class="timeline-item">
                <h3>Stage au collège Hubert Delisle – Saint-Benoît</h3>
                <p>2021 – Stage réalisé avec l’informaticien du collège : découverte du support informatique, de la maintenance et de l’accompagnement des utilisateurs.</p>
              </div>

              <div class="timeline-item">
                <h3>Stage au lycée Amiral Bouvet – Saint-Benoît</h3>
                <p>2022 – Stage réalisé avec l’informaticien du lycée : observation du fonctionnement du service informatique et aide aux tâches techniques du quotidien.</p>
              </div>

              <div class="timeline-item">
                <h3>Stage en école primaire – École élémentaire Jean Petit, Saint-Joseph</h3>
                <p>2025 – Stage réalisé avec un professeur des écoles : observation de la classe, accompagnement des élèves et participation à la vie scolaire.</p>
              </div>
            </div>
          </section>
        </div>
      </section>

      <section class="final-card">
        <div class="final-grid">
          <div>
            <p class="small-title">Atouts pour la mission</p>
            <h2>Contribuer à une université plus accessible</h2>
          </div>

          <div class="final-points">
            <div class="final-point"><strong>✓</strong>Créer un accueil rassurant et accessible</div>
            <div class="final-point"><strong>✓</strong>Aider à transmettre les bonnes informations</div>
            <div class="final-point"><strong>✓</strong>Favoriser une inclusion concrète</div>
          </div>
        </div>
      </section>
    </div>
  </main>
</body>
</html>
