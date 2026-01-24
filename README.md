<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>@aliberkyucel | Hizmetler ve Portfolyo</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Bodoni+Moda:wght@700&display=swap" rel="stylesheet">

    <style>
        /* GENEL AYARLAR */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; line-height: 1.6; color: #333; background-color: #f4f7f6; scroll-behavior: smooth; }
        a { text-decoration: none; transition: 0.3s; }

        /* HEADER */
        .header { background: #fff; padding: 20px 0; position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.05); }
        .header-inner { max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; padding: 0 20px; }
        .header-name { font-weight: 700; font-size: 1.2rem; }
        .header-name span { color: #ff4757; }
        .header-nav a { margin-left: 20px; color: #333; font-weight: 600; }
        .header-nav a:hover { color: #ff4757; }

        /* HERO */
        .hero { padding: 80px 20px; text-align: center; background: #fff; border-bottom: 1px solid #eee; }
        .hero h1 { font-size: 2.2rem; margin: 20px 0; color: #222; }
        .hero-links a { display: inline-block; margin: 5px; padding: 10px 18px; border: 1px solid #ddd; color: #555; border-radius: 5px; }
        .hero-links a:hover { background: #ff4757; color: #fff; border-color: #ff4757; }

        /* HİZMETLER SECTION */
        .projects { padding: 80px 20px; max-width: 1200px; margin: 0 auto; }
        .projects h2 { text-align: center; margin-bottom: 50px; font-size: 2rem; position: relative; padding-bottom: 15px; }
        .projects h2::after { content: ''; width: 60px; height: 3px; background: #ff4757; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); }
        
        .project-cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 25px; }
        
        .card { 
            background: #fff; 
            padding: 40px 30px; 
            border-radius: 12px; 
            text-align: center; 
            transition: transform 0.3s, box-shadow 0.3s; 
            border: 1px solid #eee;
        }
        .card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); }
        .card i { font-size: 2.5rem; color: #ff4757; margin-bottom: 20px; }
        .card h3 { margin-bottom: 15px; font-size: 1.3rem; color: #222; }
        .card p { font-size: 0.95rem; color: #666; margin-bottom: 20px; }
        .card-btn { color: #ff4757; font-weight: 700; font-size: 0.9rem; text-transform: uppercase; letter-spacing: 1px; }

        /* GITHUB SHOWCASE FIXES */
        .github-showcase { margin-top: 50px; background: #0d1117; border-radius: 15px; padding: 20px; overflow: hidden; }
        .lp-HeroCarousel-visual video { width: 100%; border-radius: 10px; display: block; }
        .visually-hidden { position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px; overflow: hidden; clip: rect(0,0,0,0); border: 0; }
        .PlayButton { background: none; border: none; color: #fff; cursor: pointer; }

        /* FOOTER */
        .main-footer { background: #1a1a1a; color: #fff; padding: 60px 20px 20px; margin-top: 50px; }
        .footer-container { max-width: 1200px; margin: 0 auto; display: flex; flex-wrap: wrap; justify-content: space-between; gap: 40px; }
        .footer-column { flex: 1; min-width: 280px; }
        .footer-logo { font-family: 'Bodoni Moda', serif; font-size: 1.5rem; letter-spacing: 1px; margin-bottom: 20px; display: block; color: #fff; }
        .footer-column h4 { margin-bottom: 25px; border-left: 3px solid #ff4757; padding-left: 12px; font-size: 1.1rem; text-transform: uppercase; }
        
        .footer-links { list-style: none; margin-bottom: 20px; }
        .footer-links li { margin-bottom: 12px; }
        .footer-links a { color: #bbb; font-size: 0.95rem; }
        .footer-links a:hover { color: #fff; padding-left: 5px; }

        /* ABONE OL KISMI */
        .subscribe-box { margin-top: 15px; }
        .subscribe-btn { 
            background: #ff4757; color: #fff; border: none; padding: 12px 25px; 
            border-radius: 50px; cursor: pointer; font-weight: 700; transition: 0.3s;
            font-size: 0.9rem;
        }
        .subscribe-btn:hover { background: #e04050; transform: scale(1.05); }

        .footer-socials { margin-top: 25px; display: flex; gap: 15px; }
        .footer-socials a { color: #fff; font-size: 1.3rem; transition: 0.3s; }
        .footer-socials a:hover { color: #ff4757; transform: translateY(-3px); }

        /* TAM ORTALANMIŞ FOOTER BOTTOM */
        .footer-bottom { 
            text-align: center; 
            margin-top: 50px; 
            padding-top: 20px; 
            border-top: 1px solid #333; 
            color: #777; 
            font-size: 0.9rem; 
            width: 100%;
        }

        @media (max-width: 768px) {
            .header-nav { display: none; }
            .footer-container { flex-direction: column; text-align: center; }
            .footer-column h4 { border-left: none; padding-left: 0; }
            .footer-socials { justify-content: center; }
        }
    </style>
</head>
<body>

<header class="header">
    <div class="header-inner">
        <div class="header-name"><a href="#" style="color:#333;">ALİ BERK <span>|</span> BİLİŞİM</a></div>
        <nav class="header-nav">
            <a href="https://aliberkbilisim.wordpress.com/">Anasayfa</a>
            <a href="https://aliberkbilisim.wordpress.com/hizmetlerimiz/">Hizmetlerimiz</a>
            <a href="https://aliberkbilisim.wordpress.com/hakkimizda/">Hakkımızda</a>
            <a href="https://aliberkbilisim.wordpress.com/iletisim/">İletişim</a>
            <a href="https://aliberkbilisim.wordpress.com/blog/">Blog</a>
        </nav>
    </div>
</header>

<section class="hero" id="home">
    <h1>Alanında Lider Markalara Projeler</h1>
    <p>Web tasarımından yapay zeka entegrasyonuna kadar geniş bir yelpazede teknolojik çözümler sunuyoruz.</p>
    <p>Alanında lider markalar için yenilikçi, ölçeklenebilir ve sürdürülebilir projeler geliştiriyoruz.</p>
    <div class="hero-links">
        <a href="https://github.com/aliberkyucel" target="_blank"><i class="fab fa-github"></i> GitHub</a>
        <a href="https://linkedin.com/in/aliberkyucel" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="mailto:info@aliberkyucel.com"><i class="fas fa-envelope"></i> Bize Ulaşın</a>
    </div>
</section>

<section class="projects" id="services">
    <h2>Hizmetlerimiz</h2>
    <div class="project-cards">
        
        <div class="card">
            <i class="fas fa-code"></i>
            <h3>Web Tasarım & Yazılım</h3>
            <p>Modern, hızlı ve tüm cihazlarla uyumlu (responsive) web siteleri.</p>
            <a href="https://aliberkbilisim.wordpress.com/web-tasarim-yazilim/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-share-alt"></i>
            <h3>Sosyal Medya Yönetimi</h3>
            <p>Markanızın dijital dünyadaki sesini ve etkileşimini artırıyoruz.</p>
            <a href="https://aliberkbilisim.wordpress.com/sosyal-medya-yonetimi/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-ad"></i>
            <h3>Dijital Reklam Çözümleri</h3>
            <p>Google ve Sosyal Medya reklamları ile doğru kitleye ulaşın.</p>
            <a href="https://aliberkbilisim.wordpress.com/dijital-reklam-cozumleri/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-shopping-cart"></i>
            <h3>E-Ticaret Sistemleri</h3>
            <p>Güvenli ödeme altyapısı ve gelişmiş yönetim panelli mağazalar.</p>
            <a href="https://aliberkbilisim.wordpress.com/e-ticaret-sistemleri/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-mobile-alt"></i>
            <h3>Uygulama Geliştirme</h3>
            <p>iOS ve Android platformları için özel mobil uygulama çözümleri.</p>
            <a href="https://aliberkbilisim.wordpress.com/uygulama-gelistirme-ve-tasarim/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-search"></i>
            <h3>SEO Hizmetleri</h3>
            <p>Arama motorlarında üst sıralara çıkmanız için stratejik optimizasyon.</p>
            <a href="https://aliberkbilisim.wordpress.com/seo-hizmetleri/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-plug"></i>
            <h3>API Geliştirme Hizmetleri</h3>
            <p>Sistemler arası veri entegrasyonu ve ölçeklenebilir API çözümleri.</p>
            <a href="https://aliberkbilisim.wordpress.com/api-gelistirme-hizmetleri/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-cloud"></i>
            <h3>Bulut Tabanlı Sistemler</h3>
            <p>Verilerinizi güvenle saklayın ve her yerden erişilebilir kılın.</p>
            <a href="https://aliberkbilisim.wordpress.com/bulut-tabanli-sistemler/" class="card-btn">İncele →</a>
        </div>

        <div class="card">
            <i class="fas fa-robot"></i>
            <h3>Yapay Zeka Entegrasyonları</h3>
            <p>İş süreçlerinizi otonom hale getiren akıllı AI çözümleri.</p>
            <a href="https://aliberkbilisim.wordpress.com/yapay-zeka-entegrasyonlari/" class="card-btn">İncele →</a>
        </div>

    </div>
    <h2 style="margin-top:20px;">Alanında Lider Markalarla İşbirliği..</h2>
    <div class="github-showcase">
        <div class="lp-HeroCarousel">
            <h2 class="visually-hidden">GitHub features</h2>
            <div class="lp-HeroCarousel-background"><div></div><div></div></div>
            <div class="lp-HeroCarousel-playButton">
                <button class="PlayButton" aria-label="Play">
                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" role="presentation">
                        <path d="M6.24905 3.69194C5.82218 3.45967 5.30225 3.76868 5.30225 4.25466V15.7452C5.30225 16.2312 5.82218 16.5402 6.24906 16.3079L16.8079 10.5626C17.2538 10.32 17.2538 9.67983 16.8079 9.4372L6.24905 3.69194ZM4.021 4.25466C4.021 2.79672 5.58078 1.86969 6.86142 2.56651L17.4203 8.31176C18.758 9.03966 18.758 10.9602 17.4203 11.6881L6.86143 17.4333C5.58079 18.1301 4.021 17.2031 4.021 15.7452V4.25466Z" fill="currentColor"></path>
                    </svg>
                </button>
            </div>
            <div class="lp-HeroCarousel-container">
                <div class="lp-HeroCarousel-content">
                    <div class="lp-HeroCarousel-visual">
                        <div>
                            <video muted autoplay loop playsinline src="https://github.githubassets.com/assets/code-1_desktop-7ab52aea3358.mp4"></video>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<footer class="main-footer">
    <div class="footer-container">
        <div class="footer-column">
            <a href="#" class="footer-logo">ALİ BERK | BİLİŞİM</a>
            <p style="color: #bbb; font-size: 0.9rem; margin-bottom: 20px;">Geleceğin teknolojilerini bugünden inşa ediyoruz. Profesyonel ekibimizle her zaman yanınızdayız.</p>
            <div class="footer-socials">
                <a href="mailto:info@aliberkbilisim.com" title="E-posta"><i class="fas fa-envelope"></i></a>
                <a href="https://aliberkbilisim.wordpress.com/rss" target="_blank" title="RSS"><i class="fas fa-rss"></i></a>
                <a href="https://github.com/aliberkyucel" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
                <a href="https://www.instagram.com/aliberkyucel/" target="_blank" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="https://linkedin.com/in/aliberkyucel" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="https://x.com/aliberkyucel" target="_blank" title="X (Twitter)"><i class="fab fa-x-twitter"></i></a>
            </div>
        </div>

        <div class="footer-column">
            <h4>Hızlı Linkler</h4>
            <ul class="footer-links">
                <li><a href="https://aliberkbilisim.wordpress.com/hakkimizda/">Hakkımızda</a></li>
                <li><a href="https://aliberkbilisim.wordpress.com/hizmetlerimiz/">Hizmetlerimiz</a></li>
                <li><a href="https://aliberkbilisim.wordpress.com/iletisim">İletişim</a></li>
                <li><a href="https://aliberkbilisim.wordpress.com/blog/">Blog</a></li>
            </ul>
        </div>

        <div class="footer-column">
            <h4>Sözleşmeler</h4>
            <ul class="footer-links">
                <li><a href="https://aliberkbilisim.wordpress.com/kullanim-sartlari/">Kullanım Şartları</a></li>
                <li><a href="https://aliberkbilisim.wordpress.com/gizlilik-politikasi/">Gizlilik Politikası</a></li>
                <li><a href="https://aliberkbilisim.wordpress.com/cerez-politikasi/">Çerez Politikası</a></li>
            </ul>
            <div class="subscribe-box">
                <form action="https://wordpress.com/email-subscriptions" method="post">
                    <button type="submit" class="subscribe-btn">Abone Ol</button>
                </form>
            </div>
        </div>
    </div>

    <div class="footer-bottom">
        <p>Ali Berk Bilişim &copy; 2026 Tüm Hakları Saklıdır.</p>
    </div>
</footer>

</body>
</html>
