<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>Almira Nur Kholisoh Ramadani — Profil Premium</title>
  <!-- Font: Manrope & Inter (fallback) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free) untuk ikon -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* ===== RESET & VARIABLES ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #ffffff;
      --bg-soft: #fafbfc;
      --text: #1e1e2a;
      --text-secondary: #4a4a5a;
      --accent: #0f3b3e; /* emerald gelap premium */
      --accent-light: #e1f0ef;
      --gold: #c5a572;
      --border: #e9eef2;
      --shadow-sm: 0 8px 20px rgba(0,0,0,0.02), 0 4px 12px rgba(0,0,0,0.03);
      --shadow-md: 0 25px 40px -12px rgba(0,0,0,0.08);
      --radius: 20px;
      --radius-sm: 14px;
      --transition: 0.35s cubic-bezier(0.25,0.46,0.45,0.94);
      --font-main: 'Manrope', 'Inter', sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-main);
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      font-weight: 400;
      overflow-x: hidden;
    }

    h1, h2, h3, h4, h5 {
      font-weight: 700;
      line-height: 1.3;
      letter-spacing: -0.01em;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 24px;
    }

    section {
      padding: 90px 0;
      position: relative;
    }

    .section-label {
      display: inline-block;
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--accent);
      background: var(--accent-light);
      padding: 6px 18px;
      border-radius: 30px;
      margin-bottom: 15px;
    }

    .section-title {
      font-size: 2.5rem;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 20px;
    }

    .section-sub {
      color: var(--text-secondary);
      max-width: 650px;
      margin-bottom: 50px;
      font-size: 1.1rem;
    }

    /* ===== BUTTONS ===== */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 14px 32px;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.95rem;
      transition: var(--transition);
      border: 1px solid transparent;
      cursor: pointer;
      letter-spacing: 0.3px;
    }
    .btn-primary {
      background: var(--accent);
      color: #fff;
      box-shadow: 0 10px 20px rgba(15,59,62,0.15);
    }
    .btn-primary:hover {
      background: #0a2f31;
      transform: translateY(-3px);
      box-shadow: 0 18px 30px rgba(15,59,62,0.2);
    }
    .btn-outline {
      background: transparent;
      border-color: #cdd6dc;
      color: var(--text);
    }
    .btn-outline:hover {
      border-color: var(--accent);
      background: var(--accent-light);
      color: var(--accent);
      transform: translateY(-3px);
    }
    .btn-gold {
      background: var(--gold);
      color: #1e1e2a;
    }
    .btn-gold:hover {
      background: #b18b4a;
      transform: translateY(-3px);
    }

    /* ===== NAVBAR ===== */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(255,255,255,0.78);
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(0,0,0,0.02);
      transition: var(--transition);
      padding: 14px 0;
    }
    .nav-container {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .logo {
      font-weight: 800;
      font-size: 1.7rem;
      color: var(--accent);
      letter-spacing: -0.5px;
    }
    .nav-links {
      display: flex;
      align-items: center;
      gap: 26px;
    }
    .nav-links a {
      font-weight: 600;
      font-size: 0.95rem;
      color: var(--text-secondary);
      transition: var(--transition);
      position: relative;
      padding: 5px 0;
    }
    .nav-links a:hover,
    .nav-links a.active {
      color: var(--accent);
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0%;
      height: 2px;
      background: var(--accent);
      transition: var(--transition);
    }
    .nav-links a:hover::after,
    .nav-links a.active::after {
      width: 100%;
    }
    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
      background: transparent;
      border: none;
      gap: 5px;
      padding: 5px;
    }
    .hamburger span {
      display: block;
      width: 26px;
      height: 2px;
      background: var(--text);
      transition: var(--transition);
    }
    .hamburger.active span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
    .hamburger.active span:nth-child(2) { opacity: 0; }
    .hamburger.active span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

    /* Mobile menu */
    .mobile-menu {
      display: none;
      flex-direction: column;
      background: white;
      border-bottom: 1px solid var(--border);
      padding: 0 24px 24px;
      gap: 5px;
      box-shadow: 0 20px 30px rgba(0,0,0,0.04);
    }
    .mobile-menu a {
      padding: 14px 0;
      border-bottom: 1px solid #f0f3f5;
      font-weight: 600;
      color: var(--text);
    }
    .mobile-menu a:last-child {
      border-bottom: none;
    }

    /* ===== HERO ===== */
    .hero {
      padding: 70px 0 90px;
      background: radial-gradient(circle at 10% 20%, #f3f9f9, transparent 40%),
                  radial-gradient(circle at 90% 70%, #faf5ee, transparent 50%);
    }
    .hero-grid {
      display: flex;
      align-items: center;
      gap: 50px;
      flex-wrap: wrap;
    }
    .hero-content {
      flex: 1 1 400px;
      animation: fadeUp 0.8s ease;
    }
    .hero-image {
      flex: 0 0 320px;
      display: flex;
      justify-content: center;
      animation: fadeIn 1s ease;
    }
    .hero-image img {
      width: 280px;
      height: 280px;
      object-fit: cover;
      border-radius: 50%;
      box-shadow: 0 30px 40px -15px rgba(0,0,0,0.15);
      border: 6px solid white;
      background: #e6edf0;
    }
    .hero-sub {
      font-weight: 600;
      color: var(--accent);
      letter-spacing: 2px;
      text-transform: uppercase;
      font-size: 0.85rem;
      margin-bottom: 10px;
    }
    .hero h1 {
      font-size: 3.2rem;
      font-weight: 800;
      margin-bottom: 10px;
    }
    .hero h1 span {
      color: var(--accent);
    }
    .hero-desc {
      font-size: 1.2rem;
      color: var(--text-secondary);
      max-width: 500px;
      margin: 20px 0 30px;
    }
    .hero-actions {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    /* ===== ABOUT ===== */
    .about-grid {
      display: flex;
      gap: 50px;
      flex-wrap: wrap;
      align-items: center;
    }
    .about-image {
      flex: 0 0 380px;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow-md);
      background: #eef2f3;
    }
    .about-image img {
      width: 100%;
      height: 420px;
      object-fit: cover;
    }
    .about-info {
      flex: 1 1 400px;
    }
    .about-info h3 {
      font-size: 1.8rem;
      margin-bottom: 15px;
    }
    .about-info p {
      color: var(--text-secondary);
      margin-bottom: 20px;
    }
    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin: 25px 0;
    }
    .skill-tag {
      background: var(--bg-soft);
      border: 1px solid var(--border);
      padding: 8px 18px;
      border-radius: 30px;
      font-size: 0.85rem;
      font-weight: 500;
      transition: var(--transition);
    }
    .skill-tag:hover {
      background: var(--accent-light);
      border-color: var(--accent);
      color: var(--accent);
    }

    /* ===== CV TIMELINE ===== */
    .timeline {
      position: relative;
      max-width: 800px;
      margin: 0 auto;
    }
    .timeline::before {
      content: '';
      position: absolute;
      left: 20px;
      top: 0;
      bottom: 0;
      width: 2px;
      background: var(--border);
    }
    .timeline-item {
      position: relative;
      padding-left: 60px;
      margin-bottom: 40px;
    }
    .timeline-dot {
      position: absolute;
      left: 12px;
      top: 5px;
      width: 18px;
      height: 18px;
      background: var(--accent);
      border-radius: 50%;
      border: 3px solid white;
      box-shadow: 0 0 0 3px var(--accent-light);
    }
    .timeline-date {
      font-weight: 600;
      color: var(--accent);
      font-size: 0.9rem;
    }
    .timeline-title {
      font-weight: 700;
      font-size: 1.2rem;
      margin: 5px 0;
    }
    .timeline-desc {
      color: var(--text-secondary);
    }

    /* ===== PORTFOLIO ===== */
    .filter-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 40px;
    }
    .filter-btn {
      background: transparent;
      border: 1px solid var(--border);
      padding: 8px 20px;
      border-radius: 30px;
      font-weight: 600;
      cursor: pointer;
      transition: var(--transition);
      font-size: 0.9rem;
    }
    .filter-btn.active,
    .filter-btn:hover {
      background: var(--accent);
      color: white;
      border-color: var(--accent);
    }
    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 25px;
    }
    .portfolio-card {
      background: white;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow-sm);
      transition: var(--transition);
      border: 1px solid var(--border);
    }
    .portfolio-card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow-md);
    }
    .portfolio-img {
      height: 200px;
      background: #eef2f3;
      overflow: hidden;
    }
    .portfolio-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s ease;
    }
    .portfolio-card:hover .portfolio-img img {
      transform: scale(1.05);
    }
    .portfolio-body {
      padding: 20px;
    }
    .portfolio-category {
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      color: var(--accent);
      letter-spacing: 1px;
    }
    .portfolio-title {
      font-weight: 700;
      font-size: 1.2rem;
      margin: 8px 0;
    }
    .portfolio-year {
      color: var(--text-secondary);
      font-size: 0.85rem;
      margin-bottom: 10px;
    }

    /* ===== GALERI & ARTIKEL ===== */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 15px;
      margin-bottom: 40px;
    }
    .gallery-item {
      border-radius: var(--radius-sm);
      overflow: hidden;
      cursor: pointer;
      height: 180px;
      background: #eef2f3;
      transition: var(--transition);
    }
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: 0.5s;
    }
    .gallery-item:hover img {
      transform: scale(1.08);
    }
    .article-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 25px;
      transition: var(--transition);
      box-shadow: var(--shadow-sm);
      margin-bottom: 20px;
    }
    .article-card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-5px);
    }
    .article-date {
      color: var(--text-secondary);
      font-size: 0.85rem;
      margin-bottom: 8px;
    }
    .article-title {
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 10px;
    }
    .article-excerpt {
      color: var(--text-secondary);
    }

    /* ===== SOCIAL ===== */
    .social-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .social-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      width: 120px;
      height: 120px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 10px;
      font-weight: 600;
      transition: var(--transition);
      box-shadow: var(--shadow-sm);
    }
    .social-card i {
      font-size: 2rem;
      color: var(--accent);
    }
    .social-card:hover {
      transform: translateY(-8px);
      border-color: var(--accent);
      background: var(--accent-light);
    }

    /* ===== KONTAK ===== */
    .contact-grid {
      display: flex;
      gap: 50px;
      flex-wrap: wrap;
    }
    .contact-info {
      flex: 1 1 300px;
    }
    .contact-info p {
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 12px;
      color: var(--text-secondary);
    }
    .contact-info i {
      width: 25px;
      color: var(--accent);
    }
    .contact-form {
      flex: 2 1 400px;
      display: grid;
      gap: 20px;
    }
    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 14px 18px;
      border: 1px solid var(--border);
      border-radius: var(--radius-sm);
      font-family: var(--font-main);
      font-size: 0.95rem;
      background: var(--bg-soft);
      transition: var(--transition);
    }
    .form-group input:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: var(--accent);
      background: white;
    }

    /* ===== TESTIMONI ===== */
    .testimonial-carousel {
      display: flex;
      gap: 25px;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      padding: 10px 0 20px;
      scrollbar-width: thin;
    }
    .testimonial-item {
      min-width: 300px;
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 30px;
      scroll-snap-align: start;
      box-shadow: var(--shadow-sm);
      transition: var(--transition);
    }
    .testimonial-item:hover {
      box-shadow: var(--shadow-md);
    }
    .testimonial-stars {
      color: #eab308;
      margin-bottom: 15px;
    }
    .testimonial-text {
      color: var(--text-secondary);
      font-style: italic;
    }
    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-top: 20px;
    }
    .testimonial-author img {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background: #dce5e8;
      object-fit: cover;
    }
    .testimonial-name {
      font-weight: 700;
    }
    .testimonial-role {
      font-size: 0.85rem;
      color: var(--text-secondary);
    }

    /* ===== FOOTER ===== */
    footer {
      background: var(--bg-soft);
      padding: 50px 0 20px;
      border-top: 1px solid var(--border);
    }
    .footer-grid {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 30px;
      margin-bottom: 30px;
    }
    .footer-col h5 {
      margin-bottom: 20px;
    }
    .footer-col a {
      display: block;
      color: var(--text-secondary);
      margin-bottom: 10px;
      transition: var(--transition);
    }
    .footer-col a:hover {
      color: var(--accent);
    }
    .footer-bottom {
      border-top: 1px solid var(--border);
      padding-top: 20px;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 10px;
      font-size: 0.85rem;
      color: var(--text-secondary);
    }

    /* ===== ANIMATIONS ===== */
    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }
    .fade-up {
      animation: fadeUp 0.7s ease both;
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px) {
      .nav-links { display: none; }
      .hamburger { display: flex; }
      .hero h1 { font-size: 2.5rem; }
      .hero-grid { gap: 30px; }
      .hero-image { flex-basis: 200px; }
      .hero-image img { width: 200px; height: 200px; }
    }
    @media (max-width: 600px) {
      section { padding: 60px 0; }
      .section-title { font-size: 2rem; }
      .container { padding: 0 18px; }
      .about-grid, .hero-grid { flex-direction: column; }
      .about-image, .hero-image { flex-basis: auto; width: 100%; }
    }
  </style>
</head>
<body>
  <!-- NAVBAR -->
  <nav class="navbar" id="navbar">
    <div class="container nav-container">
      <div class="logo">Almira<span style="color:var(--accent)">.</span></div>
      <div class="nav-links" id="navLinks">
        <a href="#beranda" class="active">Beranda</a>
        <a href="#tentang">Tentang Kami</a>
        <a href="#cv">CV</a>
        <a href="#karya">Hasil Karya</a>
        <a href="#foto-artikel">Foto & Artikel</a>
        <a href="#sosmed">Link Media Sosial</a>
        <a href="#kontak">Kontak</a>
        <a href="#testimoni">Testimoni</a>
      </div>
      <button class="hamburger" id="hamburger" aria-label="Menu">
        <span></span><span></span><span></span>
      </button>
    </div>
    <div class="mobile-menu" id="mobileMenu">
      <a href="#beranda">Beranda</a>
      <a href="#tentang">Tentang Kami</a>
      <a href="#cv">CV</a>
      <a href="#karya">Hasil Karya</a>
      <a href="#foto-artikel">Foto & Artikel</a>
      <a href="#sosmed">Link Media Sosial</a>
      <a href="#kontak">Kontak</a>
      <a href="#testimoni">Testimoni</a>
    </div>
  </nav>

  <!-- HERO / BERANDA -->
  <section class="hero" id="beranda">
    <div class="container hero-grid">
      <div class="hero-content fade-up">
        <div class="hero-sub">Pelajar • Aktif • Tangguh</div>
        <h1>Almira Nur <span>Kholisoh Ramadani</span></h1>
        <p class="hero-desc">Saya adalah seorang pelajar yang aktif, berjiwa juang dan tangguh. Senang berkolaborasi, belajar hal baru, dan memberi dampak positif.</p>
        <div class="hero-actions">
          <a href="#karya" class="btn btn-primary"><i class="fas fa-arrow-down"></i> Lihat Hasil Karya</a>
          <a href="#kontak" class="btn btn-outline"><i class="fas fa-comment"></i> Hubungi Saya</a>
        </div>
      </div>
      <div class="hero-image">
        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='280' height='280' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='45' fill='%23c5d5d8'/%3E%3Ctext x='50' y='55' font-family='Manrope, sans-serif' font-size='40' fill='%230f3b3e' text-anchor='middle'%3EA%3C/text%3E%3C/svg%3E" alt="Foto Almira">
      </div>
    </div>
  </section>

  <!-- TENTANG KAMI -->
  <section id="tentang">
    <div class="container">
      <span class="section-label">Tentang Kami</span>
      <h2 class="section-title">Profil Singkat & Nilai</h2>
      <div class="about-grid">
        <div class="about-image">
          <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='420' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%23dbe7ea'/%3E%3Ctext x='50' y='55' font-family='Manrope' font-size='30' fill='%230f3b3e' text-anchor='middle'%3E[FOTO]%3C/text%3E%3C/svg%3E" alt="Tentang Almira">
        </div>
        <div class="about-info">
          <h3>Visi & Misi</h3>
          <p><strong>Visi:</strong> Menjadi pribadi yang berintegritas, berkontribusi nyata, dan menginspirasi generasi muda untuk berani bermimpi.</p>
          <p><strong>Misi:</strong> Mengembangkan potensi diri melalui pendidikan, organisasi, dan pengalaman lapangan. Berkomitmen pada kejujuran, kerja keras, dan kolaborasi.</p>
          <div class="skill-tags">
            <span class="skill-tag">Kepemimpinan</span>
            <span class="skill-tag">Public Speaking</span>
            <span class="skill-tag">Manajemen Waktu</span>
            <span class="skill-tag">Kreativitas</span>
            <span class="skill-tag">Kerja Tim</span>
          </div>
          <p><strong>Pengalaman:</strong> Aktif di organisasi sekolah, volunteer kegiatan sosial, dan lomba akademik/non-akademik.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CV -->
  <section id="cv" style="background: var(--bg-soft);">
    <div class="container">
      <span class="section-label">CV</span>
      <h2 class="section-title">Perjalanan & Pencapaian</h2>
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2020 - Sekarang</div>
          <div class="timeline-title">Pelajar Aktif — [SEKOLAH]</div>
          <div class="timeline-desc">Menempuh pendidikan menengah, aktif dalam OSIS dan ekstrakurikuler debat.</div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2023</div>
          <div class="timeline-title">Juara 2 Lomba Pidato Bahasa Indonesia</div>
          <div class="timeline-desc">Penghargaan tingkat kota yang memotivasi kemampuan public speaking.</div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2022</div>
          <div class="timeline-title">Sertifikasi Pelatihan Kepemimpinan</div>
          <div class="timeline-desc">Mengikuti program leadership camp selama 3 hari.</div>
        </div>
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2021</div>
          <div class="timeline-title">Volunteer Kegiatan Sosial</div>
          <div class="timeline-desc">Berpartisipasi dalam bakti sosial dan penggalangan dana.</div>
        </div>
      </div>
      <div style="margin-top: 10px;">
        <a href="#" class="btn btn-primary"><i class="fas fa-download"></i> Download CV</a>
      </div>
    </div>
  </section>

  <!-- HASIL KARYA -->
  <section id="karya">
    <div class="container">
      <span class="section-label">Hasil Karya</span>
      <h2 class="section-title">Portofolio Pilihan</h2>
      <div class="filter-buttons">
        <button class="filter-btn active" data-filter="semua">Semua</button>
        <button class="filter-btn" data-filter="akademik">Akademik</button>
        <button class="filter-btn" data-filter="organisasi">Organisasi</button>
        <button class="filter-btn" data-filter="kreatif">Kreatif</button>
      </div>
      <div class="portfolio-grid" id="portfolioGrid">
        <div class="portfolio-card" data-category="akademik">
          <div class="portfolio-img"><img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='200' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23cfe0e4'/%3E%3Ctext x='50' y='35' font-size='18' fill='%230f3b3e' text-anchor='middle'%3EKarya 1%3C/text%3E%3C/svg%3E" alt="Karya 1"></div>
          <div class="portfolio-body">
            <div class="portfolio-category">Akademik</div>
            <div class="portfolio-title">Karya Tulis Ilmiah</div>
            <p class="portfolio-year">2023</p>
            <a href="#" class="btn btn-outline" style="padding:8px 18px; font-size:0.8rem;">Lihat Detail</a>
          </div>
        </div>
        <div class="portfolio-card" data-category="organisasi">
          <div class="portfolio-img"><img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='200' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23dbe7ea'/%3E%3Ctext x='50' y='35' font-size='18' fill='%230f3b3e' text-anchor='middle'%3EKarya 2%3C/text%3E%3C/svg%3E" alt="Karya 2"></div>
          <div class="portfolio-body">
            <div class="portfolio-category">Organisasi</div>
            <div class="portfolio-title">Proyek Sosial Sekolah</div>
            <p class="portfolio-year">2022</p>
            <a href="#" class="btn btn-outline" style="padding:8px 18px; font-size:0.8rem;">Lihat Detail</a>
          </div>
        </div>
        <div class="portfolio-card" data-category="kreatif">
          <div class="portfolio-img"><img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='200' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23e2ecef'/%3E%3Ctext x='50' y='35' font-size='18' fill='%230f3b3e' text-anchor='middle'%3EKarya 3%3C/text%3E%3C/svg%3E" alt="Karya 3"></div>
          <div class="portfolio-body">
            <div class="portfolio-category">Kreatif</div>
            <div class="portfolio-title">Desain Poster</div>
            <p class="portfolio-year">2023</p>
            <a href="#" class="btn btn-outline" style="padding:8px 18px; font-size:0.8rem;">Lihat Detail</a>
          </div>
        </div>
        <div class="portfolio-card" data-category="akademik">
          <div class="portfolio-img"><img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='200' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23cfe0e4'/%3E%3Ctext x='50' y='35' font-size='18' fill='%230f3b3e' text-anchor='middle'%3EKarya 4%3C/text%3E%3C/svg%3E" alt="Karya 4"></div>
          <div class="portfolio-body">
            <div class="portfolio-category">Akademik</div>
            <div class="portfolio-title">Presentasi Riset</div>
            <p class="portfolio-year">2023</p>
            <a href="#" class="btn btn-outline" style="padding:8px 18px; font-size:0.8rem;">Lihat Detail</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FOTO & ARTIKEL -->
  <section id="foto-artikel" style="background: var(--bg-soft);">
    <div class="container">
      <span class="section-label">Foto & Artikel</span>
      <h2 class="section-title">Galeri & Publikasi</h2>
      <div class="gallery-grid">
        <div class="gallery-item"><img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='
