<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Basta InfosTech · Télécoms & IA</title>
  <!-- Police élégante et moderne -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (gratuit) pour les icônes techniques -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: #f4f7fb;
      color: #1e293b;
      line-height: 1.6;
      padding: 2rem 1rem;
    }

    .article-container {
      max-width: 1200px;
      margin: 0 auto;
      background: white;
      border-radius: 2rem;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
      overflow: hidden;
    }

    /* En-tête avec titre bilingue et métadonnées */
    .article-header {
      background: linear-gradient(145deg, #0a1a2f 0%, #123456 100%);
      color: white;
      padding: 2.5rem 3rem;
      border-bottom: 4px solid #f5b01e;
    }

    .header-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem 2.5rem;
      margin-bottom: 1.8rem;
      font-size: 0.95rem;
      color: #bdd3f0;
    }

    .meta-item {
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .meta-item i {
      color: #f5b01e;
      width: 1.2rem;
      font-size: 1.1rem;
    }

    .arabic-title {
      font-size: 2.2rem;
      font-weight: 700;
      line-height: 1.4;
      margin-bottom: 1rem;
      font-family: 'Amiri', 'Traditional Arabic', 'Inter', serif;
      letter-spacing: 0.3px;
      border-right: 4px solid #f5b01e;
      padding-right: 1.5rem;
    }

    .french-subhead {
      font-size: 1.4rem;
      font-weight: 500;
      color: #e0edff;
      border-left: 4px solid #f5b01e;
      padding-left: 1.5rem;
      margin-top: 0.5rem;
    }

    /* grille du contenu principal */
    .main-grid {
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 0;
    }

    .left-column {
      padding: 2.5rem 2rem 2.5rem 2.5rem;
      background: #ffffff;
    }

    .right-column {
      padding: 2.5rem 2.5rem 2.5rem 2rem;
      background: #f9fcff;
      border-left: 1px solid #dde7f0;
    }

    /* cartes d'actualité */
    .news-card {
      margin-bottom: 2.8rem;
      border-bottom: 1px dashed #cbd5e1;
      padding-bottom: 2rem;
    }

    .news-card:last-child {
      border-bottom: none;
      padding-bottom: 0;
      margin-bottom: 0;
    }

    .card-tag {
      display: inline-block;
      background: #e6f0ff;
      color: #0a3e6d;
      font-weight: 600;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      padding: 0.3rem 0.9rem;
      border-radius: 30px;
      margin-bottom: 1rem;
      border: 1px solid #b9d5ff;
    }

    .card-title {
      font-size: 1.7rem;
      font-weight: 700;
      margin-bottom: 1rem;
      line-height: 1.3;
      color: #0b2b44;
    }

    .card-title i {
      color: #f5b01e;
      margin-right: 0.5rem;
      font-size: 1.5rem;
    }

    .card-meta {
      display: flex;
      gap: 1.5rem;
      font-size: 0.85rem;
      color: #5f6c80;
      margin-bottom: 1.25rem;
      border-left: 3px solid #f5b01e;
      padding-left: 1rem;
      background: #f2f7ff;
      padding: 0.6rem 1.2rem;
      border-radius: 0 30px 30px 0;
    }

    .card-content p {
      margin-bottom: 1rem;
      font-size: 1.05rem;
      color: #1f344a;
    }

    .card-content strong {
      color: #003f7f;
      font-weight: 600;
    }

    .card-content .arabic-excerpt {
      background: #f0f5fa;
      padding: 1.2rem 1.5rem;
      border-radius: 20px;
      margin: 1.5rem 0 0.8rem;
      font-size: 1.2rem;
      line-height: 1.8;
      text-align: right;
      font-family: 'Amiri', 'Traditional Arabic', serif;
      border-right: 5px solid #f5b01e;
      color: #112b3f;
    }

    .badge {
      background: #002856;
      color: white;
      padding: 0.3rem 1rem;
      border-radius: 50px;
      font-weight: 500;
      font-size: 0.8rem;
      display: inline-block;
      margin-top: 1rem;
    }

    /* colonne droite (IA et congrès) */
    .ia-card {
      background: white;
      border-radius: 1.5rem;
      padding: 1.8rem;
      box-shadow: 0 8px 20px rgba(0,40,80,0.05);
      margin-bottom: 2rem;
      border: 1px solid #e2edf5;
    }

    .ia-card:last-child {
      margin-bottom: 0;
    }

    .ia-icon {
      font-size: 2rem;
      color: #f5b01e;
      margin-bottom: 1rem;
    }

    .ia-card h3 {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 0.75rem;
      color: #0b2b44;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .ia-card h3 i {
      font-size: 1.2rem;
      color: #3b7eb0;
    }

    .ia-card .date-lieu {
      color: #2d577c;
      font-weight: 500;
      font-size: 0.9rem;
      margin-bottom: 1rem;
      background: #eaf3fe;
      padding: 0.3rem 1rem;
      border-radius: 30px;
      display: inline-block;
    }

    .ia-card p {
      color: #1f3a57;
      margin-bottom: 1rem;
    }

    .ia-card ul {
      margin: 1rem 0 1rem 1.5rem;
      color: #1e3a5f;
    }

    .ia-card li {
      margin-bottom: 0.4rem;
    }

    hr {
      border: none;
      border-top: 2px dotted #adc6e0;
      margin: 2rem 0 1rem;
    }

    /* footer */
    .article-footer {
      background: #e8f0fa;
      padding: 1.5rem 3rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      color: #264d7c;
      border-top: 1px solid #c7daf0;
      font-size: 0.9rem;
    }

    .footer-tags {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .footer-tags span {
      background: white;
      padding: 0.3rem 1.2rem;
      border-radius: 30px;
      border: 1px solid #9bb8e0;
      font-weight: 500;
      color: #103a62;
    }

    .footer-credit {
      font-weight: 600;
    }

    .footer-credit i {
      color: #e03a3a;
    }

    /* responsive */
    @media (max-width: 850px) {
      .main-grid {
        grid-template-columns: 1fr;
      }
      .right-column {
        border-left: none;
        border-top: 2px solid #d4e2f0;
      }
      .article-header {
        padding: 1.8rem;
      }
      .arabic-title {
        font-size: 1.8rem;
      }
    }

    @media (max-width: 500px) {
      .card-title {
        font-size: 1.5rem;
      }
      .card-meta {
        flex-wrap: wrap;
        gap: 0.7rem;
      }
    }
  </style>
</head>
<body>
  <div class="article-container">
    <!-- En-tête bilingue avec localisation et contexte -->
    <header class="article-header">
      <div class="header-meta">
        <span class="meta-item"><i class="fas fa-calendar-alt"></i> 5-6 mars 2026</span>
        <span class="meta-item"><i class="fas fa-map-pin"></i> Valence · Barcelone · Espagne</span>
        <span class="meta-item"><i class="fas fa-newspaper"></i> Basta InfosTech / APS</span>
        <span class="meta-item"><i class="fas fa-language"></i> AR · FR</span>
      </div>
      <h1 class="arabic-title">الوزير سيد علي زروقي يتفقد مقر اتصالات الجزائر أوروبا في فالنسيا… مرحلة جديدة في الأفق</h1>
      <div class="french-subhead">📡 Sid Ali Zerrouki à Valence et Barcelone : câble Medusa, IA et hubs numériques</div>
    </header>

    <!-- Contenu principal : grille deux colonnes -->
    <div class="main-grid">
      <!-- COLONNE GAUCHE : Article principal Valence + extrait Medusa -->
      <div class="left-column">
        <!-- Première carte : visite Valencia (arabe/français) -->
        <div class="news-card">
          <span class="card-tag"><i class="fas fa-submarine"></i>  FIBRE OPTIQUE · VALENCE</span>
          <h2 class="card-title"><i class="fas fa-map-marked-alt"></i> اتصالات الجزائر أوروبا – Une nouvelle étape</h2>
          <div class="card-meta">
            <span><i class="fas fa-user"></i> Sid Ali Zerrouki</span>
            <span><i class="fas fa-calendar"></i> 5 mars 2026</span>
            <span><i class="fas fa-globe"></i> Valencia · Espagne</span>
          </div>
          <div class="card-content">
            <!-- Rappel du texte arabe (extrait significatif) -->
            <div class="arabic-excerpt">
              قام وزير البريد والمواصلات السلكية واللاسلكية، السيد سيدعلي زروقي، بزيارة إلى مقر مؤسسة اتصالات الجزائر أوروبا المتواجد مقرها بمدينة فالنسيا، بمعية سفير الجزائر السيد عبد الفتاح دغموم. اطلع السيد الوزير على نجاعة نظام الوصلة البحرية للألياف البصرية الرابط بين الجزائر وهران والشبكة الأوروبية. وأسدى توجيهات تقنية لتعزيز أداء هذه البنية التحتية الاستراتيجية. كما كشف أن اتصالات الجزائر أوروبا ستلعب أدواراً أكثر فاعلية في السوق الأوروبية قريباً.
            </div>
            <p><strong>🔹 Traduction & synthèse :</strong> En marge de sa visite de travail en Espagne, le ministre Sid Ali Zerrouki accompagné de l’ambassadeur Abdelatif Daghmoum s’est rendu au siège d’Algérie Télécom Europe à Valence. Il a inspecté la performance du câble sous-marin à fibre optique reliant Oran/Alger au réseau européen. Des instructions techniques ont été données pour renforcer cette infrastructure stratégique. <strong>Le ministre a annoncé qu’Algérie Télécom Europe jouera un rôle plus actif sur le marché européen</strong> dans le cadre de la stratégie de renforcement de la présence algérienne dans la connectivité internationale.</p>
            <span class="badge"><i class="fas fa-satellite-dish"></i> Hub algérien en Europe</span>
          </div>
        </div>

        <!-- Deuxième carte : câble Medusa (atterrissement Barcelone) + communiqué APS -->
        <div class="news-card">
          <span class="card-tag"><i class="fas fa-network-wired"></i> MEDUSA CABLE · BARCELONE</span>
          <h2 class="card-title"><i class="fas fa-water"></i> Le câble sous‑marin "Medusa" à Barcelone</h2>
          <div class="card-meta">
            <span><i class="fas fa-file-alt"></i> APS · 5 mars 2026</span>
            <span><i class="fas fa-tags"></i> Communications, technologie, congrès</span>
          </div>
          <div class="card-content">
            <p>Le ministre a visité le <strong>centre d’atterrissement du câble sous-marin Medusa à Barcelone</strong>, en marge du Mobile World Congress. Il s’est enquis des préparatifs pour la mise en service prévue <strong>début 2027</strong>. Ce centre constitue une passerelle stratégique entre l’Algérie et l’Europe : augmentation de la capacité internet, amélioration de la qualité des communications internationales, diversification des itinéraires et soutien au développement de la <strong>5G</strong> et de la souveraineté numérique.</p>
            <p>🔹 Rappel : M. Zerrouki avait lancé le projet Medusa depuis Alger en octobre 2025. Ce câble reliera l’Algérie via deux points d’atterrissement (Alger et Collo).</p>
            <p><i class="fas fa-chart-line" style="color:#f5b01e;"></i> <em>“Rôle stratégique dans le système des télécommunications, contribution à la souveraineté numérique.”</em></p>
          </div>
        </div>

        <!-- Petit bloc complémentaire : déclaration spectre / congrès (intégré ici) -->
        <div style="background: #ecf5fb; border-radius: 1.5rem; padding: 1.3rem 1.8rem; margin-top: 1.5rem;">
          <span style="font-weight: 700; display: flex; gap: 0.8rem; align-items: center;"><i class="fas fa-tower-broadcast" style="color:#f5b01e;"></i>  MWC Barcelone – Fréquences 5G/6G</span>
          <p style="margin-top: 0.8rem; font-size: 1rem;">Lors de la réunion ministérielle sur les défis des spectres, le ministre a déclaré : <strong>“la politique du spectre est une décision souveraine, économique et stratégique. Les taxes élevées peuvent retarder les investissements 5G/6G. Il faut des approches équilibrées pour encourager les investissements à long terme.”</strong></p>
        </div>
      </div>

      <!-- COLONNE DROITE : Intelligence artificielle et gouvernance + détails Congrès -->
      <div class="right-column">
        <!-- Carte IA haut niveau -->
        <div class="ia-card">
          <div class="ia-icon"><i class="fas fa-brain"></i></div>
          <h3><i class="fas fa-robot"></i> Gouvernance de l’IA dans les télécoms</h3>
          <div class="date-lieu"><i class="fas fa-calendar-alt"></i> 4 mars 2026 · Barcelone (GSMA/PNUD)</div>
          <p>Le ministre a participé à une rencontre de haut niveau organisée par le PNUD et la GSMA sur la gouvernance de l’intelligence artificielle dans le secteur des télécoms. Il a mis en avant les efforts de l’Algérie pour devenir un <strong>hub technologique régional (Europe, Afrique, monde arabe)</strong> grâce à :</p>
          <ul>
            <li>L’investissement dans les infrastructures télécoms</li>
            <li>Le déploiement accéléré des réseaux 5G</li>
            <li>L’écosystème national de l’IA</li>
            <li>La stratégie nationale de cybersécurité (5 ans)</li>
          </ul>
          <p><strong>« Le véritable enjeu de l’IA est institutionnel : une gouvernance claire est la clé pour faire de l’IA un levier de progrès économique et d’inclusion numérique »</strong> – a souligné M. Zerrouki.</p>
        </div>

        <!-- Carte congrès mondial téléphonie mobile -->
        <div class="ia-card">
          <div class="ia-icon"><i class="fas fa-mobile-alt"></i></div>
          <h3><i class="fas fa-globe-europe"></i> Congrès mondial de la téléphonie mobile</h3>
          <div class="date-lieu"><i class="fas fa-calendar-alt"></i> 3 mars 2026 · Barcelone</div>
          <p>Le ministre a conduit une délégation algérienne composée d’entreprises nationales et de start-up spécialisées dans les applications de messagerie. Cette participation s’inscrit dans <strong>l’engagement de l’État à renforcer sa présence technologique internationale</strong> et à développer des partenariats stratégiques.</p>
          <p>🔹 <strong>Intervention clé :</strong> lors de la réunion ministérielle sur <em>“Défis des spectres de fréquences et renouvellement des licences”</em>, il a plaidé pour une tarification équilibrée afin de stimuler les investissements durables.</p>
          <hr>
          <p><i class="fas fa-check-circle" style="color:#1e7e34;"></i> Objectif : faire de l’Algérie un trait d’union numérique entre l’Europe, l’Afrique et les pays arabes.</p>
        </div>

        <!-- Mini carte rappel : déclaration IA confiance -->
        <div style="background: white; border: 1px solid #f0c78a; border-radius: 1.5rem; padding: 1.2rem 1.5rem; margin-top: 1rem;">
          <i class="fas fa-shield-alt" style="color:#f5b01e; margin-right: 0.5rem;"></i>
          <span style="font-weight: 600;">Confiance & gouvernance :</span> “Instaurer un climat de confiance et des cadres clairs en matière d’IA est une condition <em>sine qua non</em> pour l’innovation et le développement économique et social.”
        </div>
      </div>
    </div>

    <!-- Pied de page (métadonnées et sources) -->
    <footer class="article-footer">
      <div class="footer-tags">
        <span><i class="far fa-file-pdf"></i> APS 108 · 119 · 33</span>
        <span>#Medusa</span>
        <span>#IA_Telecom</span>
        <span>#5G</span>
        <span>#Zerrouki</span>
      </div>
      <div class="footer-credit">
        <i class="fas fa-code"></i> Basta InfosTech – édition spéciale Espagne 2026
      </div>
    </footer>
  </div>

  <!-- petit style complémentaire pour les icônes -->
  <style>
    /* Amélioration police arabe si disponible */
    @import url('https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&display=swap');
    .arabic-excerpt, .arabic-title {
      font-family: 'Amiri', 'Traditional Arabic', 'Inter', serif;
    }
    .fa-chevron-right, .fa-chevron-left {
      pointer-events: none;
    }
  </style>
</body>
</html>
