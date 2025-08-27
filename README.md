Oke! Aku akan buatkan versi final landing page kamu yang jauh lebih profesional, interaktif, dan “kelas 10 miliar”—artinya:

Fitur bisa diklik langsung scroll ke bagian materi lengkap.

Materi fitur (Metode Mikro, EPS-TOPIK, Tracking Progres) sudah ada.

Animasi modern dan smooth, UI/UX premium.

Responsif di semua layar.

CTA jelas, hover effect halus, dan visual “high-end”.


Aku akan menambahkan section tambahan untuk tiap fitur, supaya pengguna bisa langsung melihat modul, latihan mikro, dan dashboard progres.

Berikut versi final HTML-nya:

<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Kholdrush — Belajar Bahasa Korea</title>
<meta name="description" content="Landing page profesional Kholdrush: video interaktif, kurikulum lengkap EPS-TOPIK, testimoni, dan dashboard progres." />
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&family=Noto+Sans+KR:wght@400;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0b1020; --card:#121835; --muted:#96a0c6; --text:#f7f9ff;
  --accent:#6aa6ff; --accent-2:#ff6a95; --ring:0 10px 30px rgba(106,166,255,.25);
  --radius:18px; --maxw:1200px;
}
*{box-sizing:border-box}
html,body{margin:0;padding:0;font-family:Poppins, system-ui, -apple-system, Segoe UI, Roboto, "Noto Sans KR", Arial, sans-serif;background:radial-gradient(1000px 600px at 10% -10%, rgba(255,106,149,.18), transparent 60%),radial-gradient(900px 600px at 110% 10%, rgba(106,166,255,.16), transparent 60%),var(--bg);color:var(--text);line-height:1.6;-webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility;}
.container{max-width:var(--maxw);margin:auto;padding:0 20px}
.btn{display:inline-block;border:none;cursor:pointer;text-decoration:none;background:linear-gradient(135deg,var(--accent),#8ec5ff);color:#001026;font-weight:700;padding:14px 22px;border-radius:999px;box-shadow:var(--ring);transition:transform .15s ease, filter .2s ease}
.btn:hover{transform:translateY(-2px);filter:saturate(1.15)}
.btn.ghost{background:rgba(255,255,255,.08);color:var(--text);box-shadow:none;border:1px solid rgba(255,255,255,.12)}
.nav{position:sticky;top:0;z-index:40;backdrop-filter:saturate(180%) blur(14px);background:linear-gradient(180deg, rgba(11,16,32,.9), rgba(11,16,32,.6));border-bottom:1px solid rgba(255,255,255,.06)}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;height:64px}
.brand{display:flex;gap:10px;align-items:center;font-weight:800;letter-spacing:.2px}
.logo{width:28px;height:28px;border-radius:8px;background:conic-gradient(from 210deg at 50% 50%, var(--accent), var(--accent-2));box-shadow:0 6px 18px rgba(0,0,0,.35)}
.menu{display:flex;gap:18px;align-items:center}
.menu a{color:var(--muted);text-decoration:none;font-weight:600;font-size:.95rem}
.menu a:hover{color:#fff}
.nav .actions{display:flex;gap:10px;align-items:center}
.nav-toggle{display:none}
.hero{position:relative;padding:86px 0 54px}
.hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:36px;align-items:center}
.kicker{color:var(--accent-2);font-weight:800;letter-spacing:.8px;text-transform:uppercase;font-size:.8rem}
.title{font-size:clamp(2rem,5vw,3.4rem);line-height:1.1;margin:.35em 0 .3em;font-weight:800}
.lead{font-size:1.05rem;color:var(--muted);max-width:56ch}
.cta{margin-top:26px;display:flex;gap:12px;flex-wrap:wrap}
.hero-card{background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));border:1px solid rgba(255,255,255,.12);border-radius:var(--radius);padding:22px;box-shadow:0 10px 30px rgba(0,0,0,.25)}
.hero-card h3{margin:0 0 10px}
.pill{display:inline-flex;align-items:center;gap:8px;font-size:.9rem;color:#dfe8ff;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.12);border-radius:999px;padding:8px 12px}
section{padding:64px 0}
.sec-head{display:flex;align-items:end;justify-content:space-between;margin-bottom:24px}
.sec-head h2{font-size:clamp(1.4rem, 3.2vw, 2rem);margin:0}
.muted{color:var(--muted)}
.grid{display:grid;gap:18px}
.grid.cols-3{grid-template-columns:repeat(3,minmax(0,1fr))}
.grid.cols-2{grid-template-columns:repeat(2,minmax(0,1fr))}
.card{background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));border:1px solid rgba(255,255,255,.1);border-radius:var(--radius);padding:22px;transition:transform .18s ease,border-color .2s ease;position:relative;overflow:hidden;cursor:pointer}
.card:hover{transform:translateY(-6px);border-color:rgba(255,255,255,.22)}
.card .icon{width:38px;height:38px;border-radius:12px;display:grid;place-items:center;margin-bottom:10px;background:linear-gradient(135deg,var(--accent),var(--accent-2));box-shadow:var(--ring)}
.video-embed{display:grid;place-items:center}
.video-embed .frame{width:100%;max-width:360px;border-radius:16px;overflow:hidden;box-shadow:0 14px 40px rgba(0,0,0,.35)}
.steps .step{display:flex;gap:14px;align-items:flex-start}
.badge{min-width:34px;height:34px;border-radius:9px;display:grid;place-items:center;font-weight:800;color:#001026;background:linear-gradient(135deg,#fff 40%,#e6f0ff);box-shadow:var(--ring)}
.testi{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.quote{font-style:italic}
.price-wrap{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.price .tag{font-size:.85rem;letter-spacing:.6px;color:#ffeef6;background:rgba(255,255,255,.08);padding:6px 10px;border-radius:999px;display:inline-block}
.price h3{margin:10px 0}
.price .amount{font-size:1.8rem;font-weight:800}
.faq .item{border:1px solid rgba(255,255,255,.1);border-radius:14px;padding:16px}
.faq summary{cursor:pointer;list-style:none;font-weight:700}
.faq summary::-webkit-details-marker{display:none}
footer{padding:36px 0;border-top:1px solid rgba(255,255,255,.08);color:var(--muted)}
@media(max-width:980px){.hero-grid{grid-template-columns:1fr}.grid.cols-3{grid-template-columns:1fr 1fr}.testi,.price-wrap{grid-template-columns:1fr 1fr}}
@media(max-width:640px){.menu{display:none}.nav-toggle{display:inline-flex;gap:8px;align-items:center;color:#fff;background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.1);padding:8px 12px;border-radius:999px}.menu.open{display:flex;position:absolute;inset:64px 10px auto 10px;flex-direction:column;background:#0b1020;border:1px solid rgba(255,255,255,.12);border-radius:14px;padding:12px}.grid.cols-3,.grid.cols-2,.testi,.price-wrap{grid-template-columns:1fr}}
/* Fitur Detail */
.feature-detail{background:var(--card);padding:24px;border-radius:var(--radius);margin-top:24px;box-shadow:0 12px 40px rgba(0,0,0,.35)}
.feature-detail h4{margin-top:0;color:var(--accent-2)}
.feature-detail ul{padding-left:20px}
.feature-detail li{margin-bottom:8px}
</style>
</head>
<body>

<!-- NAV -->
<nav class="nav">
  <div class="container wrap">
    <div class="brand">
      <img src="20250827_222822.png" alt="Kholdrush Logo" class="logo">
      Kholdrush
    </div>
    <div class="menu" id="menu">
      <a href="#home">Beranda</a>
      <a href="#fitur">Fitur</a>
      <a href="#kurikulum">Kurikulum</a>
      <a href="#video">Video</a>
      <a href="#harga">Program</a>
      <a href="#faq">FAQ</a>
    </div>
    <div class="actions">
      <a class="btn ghost" href="#harga">Coba Gratis</a>
      <button class="nav-toggle" id="navToggle">Menu ▾</button>
    </div>
  </div>
</nav>

<!-- HERO -->
<header class="hero container" id="home">
  <div class="hero-grid">
    <div>
      <span class="kicker">Kelas Korea Interaktif</span>
      <h1 class="title">Belajar Bahasa Korea <span style="background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent">lebih cepat</span> dengan video & praktik</h1>
      <p class="lead">Metode Kholdrush menggabungkan <strong>video pendek</strong>, <strong>latihan mikro</strong>, dan <strong>kurikulum EPS‑TOPIK</strong> yang ringkas. Cocok buat pemula sampai pejuang ujian.</p>
      <div class="cta">
        <a class="btn" href="#harga">Mulai Sekarang</a>
        <a class="btn ghost" href="#video">Lihat Contoh Video</a>
      </div>
      <div style="margin-top:18px" class="pill">⚡ 20.000+ menit belajar ditonton</div>
    </div>
    <div class="hero-card">
      <h3>Highlight Minggu Ini</h3>
      <p class="muted">Konsonan rangkap, partikel 은/는, tips cepat huruf 받침.</p>
      <div class="pill" style="margin-top:10px">🎯 Target: 15 menit/hari</div>
    </div>
  </div>
</header>

<!-- FEATURES -->
<section class="container" id="fitur">
  <div class="sec-head">
    <h2>Kenapa Kholdrush?</h2>
    <span class="muted">Fokus hasil, bukan teori bertele‑tele</span>
  </div>
  <div class="grid cols-3">
    <div class="card" onclick="document.getElementById('micro').scrollIntoView({behavior:'smooth'});">
      <div class="icon">🧠</div>
      <h3>Metode Mikro</h3>
      <p class="muted">Materi dipecah jadi bite-size supaya mudah konsisten tiap hari.</p>
      <p class="muted">Klik untuk modul & latihan lengkap.</p>
    </div>
    <div class="card" onclick="document.getElementById('eps').scrollIntoView({behavior:'smooth'});">
      <div class="icon">🇰🇷</div>
      <h3>Fokus EPS‑TOPIK</h3>
      <p class="muted">Kosa kata, grammar, budaya, peralatan kerja sesuai kisi terbaru.</p>
      <p class="muted">Klik untuk materi lengkap EPS‑TOPIK.</p>
    </div>
    <div class="card" onclick="document.getElementById('tracking').scrollIntoView({behavior:'smooth'});">
      <div class="icon">📈</div>
      <h3>Tracking Progres</h3>
      <p class="muted">Checklist harian & milestone supaya kamu lihat kemajuan nyata.</p>
      <p class="muted">Klik untuk dashboard progres & target pribadi.</p>
    </div>
  </div>
</section>

<!-- FEATURE DETAILS -->
<section class="container" id="micro">
  <div class="sec-head"><h2>Latihan Mikro</h2><span class="muted">Belajar cepat tiap hari</span></div>
  <div class="feature-detail">
    <h4>Contoh Modul:</h4>
    <ul>
      <li>5 menit membaca huruf Hangeul tiap hari</li>
      <li>Latihan partikel & grammar singkat</li>
      <li>Mini quiz interaktif harian</li>
      <li>Catatan & tips cepat dari mentor</li>
    </ul>
  </div>
</section>

<section class="container" id="eps">
  <div class="sec-head"><h2>Materi EPS‑TOPIK</h2><span class="muted">Kuasai semua topik penting</span></div>
  <div class="feature-detail">
    <h4>Kisi-kisi Modul:</h4>
    <ul>
      <li>Kosa kata & frasa kerja</li>
      <li>Grammar & pola kalimat inti</li>
      <li>Budaya Korea & etika kerja</li>
      <li>Peralatan kerja & safety</li>
      <li>Mock test & review soal</li>
    </ul>
  </div>
</section>

<section class="container" id="tracking">
  <div class="sec-head"><h2>Tracking Progres</h2><span class="muted">Dashboard pribadi & milestone</span></div>
  <div class="feature-detail">
    <h4>Fitur Utama:</h4>
    <ul>
      <li>Checklist harian & mingguan</li>
      <li>Milestone & target belajar</li>
      <li>Statistik progres visual</li>
      <li>Notifikasi & reminder belajar</li>
      <li>Rekomendasi modul sesuai level</li>
    </ul>
  </div>
</section>

<!-- Kurikulum / roadmap -->
<section class="container" id="kurikulum">
  <div class="sec-head">
    <h2>Roadmap 4 Minggu</h2>
    <span class="muted">Dari Hangeul ke kalimat kerja</span>
  </div>
  <div class="grid cols-2">
    <div class="card step"><div class="badge">1</div><div>
      <h3>Hangeul & 받침</h3>
      <p class="muted">Huruf dasar, rangkap, pola bunyi akhir.</p>
    </div></div>
    <div class="card step"><div class="badge">2</div><div>
      <h3>Frasa Harian</h3>
      <p class="muted">Sapa, tanya, angka, tanggal, waktu.</p>
    </div></div>
    <div class="card step"><div class="badge">3</div><div>
      <h3>Grammar Inti</h3>
      <p class="muted">-아요/어요, -(으)려고, -(으)ㄹ 거예요, -거든요.</p>
    </div></div>
    <div class="card step"><div class="badge">4</div><div>
      <h3>EPS‑TOPIK Drill</h3>
      <p class="muted">Peralatan kerja, safety, budaya—mock test & review.</p>
    </div></div>
  </div>
</section>

<!-- VIDEO EMBED -->
<section class="container" id="video">
  <div class="sec-head">
    <h2>Contoh Video TikTok</h2>
    <span class="muted">Ganti ID video dengan konten kamu</span>
  </div>
  <div class="video-embed">
    <div class="frame">
      <blockquote class="tiktok-embed" cite="https://www.tiktok.com/@kholdrush/video/7398236289425810731" data-video-id="7398236289425810731" style="max-width:360px; min-width:320px;">
        <section>
          <a target="_blank" title="@kholdrush" href="https://www.tiktok.com/@kholdrush">@kholdrush</a>
        </section>
      </blockquote>
      <script async src="https://www.tiktok.com/embed.js"></script>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="container" id="testimoni">
  <div class="sec-head">
    <h2>Yang Mereka Rasakan</h

