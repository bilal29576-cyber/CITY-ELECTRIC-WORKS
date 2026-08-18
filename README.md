<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>City Electric Works - Islamabad</title>
    <meta name="description" content="City Electric Works - Best quality products, wires, fans, switches & industrial equipment in Islamabad.">
    <meta name="robots" content="index, follow">
    <link rel="icon" type="image/png" href="assets/T.png">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        :root {
            --primary: #0d7a5f;
            --primary-dark: #074e3d;
            --primary-light: #129e6f;
            --accent: #f59e0b;
            --bg-dark: #0f172a;
            --bg-card: #1e293b;
            --text-light: #f8fafc;
            --text-muted: #94a3b8;
            --glass: rgba(30, 41, 59, 0.85);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* STICKY NAVBAR */
        .navbar {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--glass);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--glass-border);
            padding: 0.8rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .brand img {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            object-fit: cover;
            border: 2px solid var(--primary-light);
        }

        .brand-text {
            font-size: 1.25rem;
            font-weight: 800;
            color: #fff;
            letter-spacing: -0.5px;
        }

        .brand-text span {
            color: var(--primary-light);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--text-light);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
            border-radius: 2px;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background: var(--text-light);
            border-radius: 2px;
        }

        /* HERO SECTION */
        .hero {
            position: relative;
            min-height: 85vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 4rem 1.5rem;
            background: radial-gradient(circle at center, rgba(18, 158, 111, 0.25) 0%, rgba(15, 23, 42, 1) 75%);
            overflow: hidden;
        }

        .hero-content {
            max-width: 850px;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }

        /* ENHANCED & ENLARGED HERO BRANDING LOGO */
        .hero-top-brand {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 18px;
            margin-bottom: 1.8rem;
            animation: pulseGlow 3s infinite ease-in-out;
        }

        .hero-top-logo {
            width: 100px;
            height: 100px;
            border-radius: 20px;
            object-fit: cover;
            border: 3px solid var(--primary-light);
            box-shadow: 0 0 30px rgba(18, 158, 111, 0.7);
            animation: floatLogo 3s ease-in-out infinite;
        }

        .hero-top-title {
            font-size: 2.5rem;
            font-weight: 800;
            color: #fff;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .hero-top-title span {
            color: var(--primary-light);
        }

        .hero-badge {
            display: inline-block;
            padding: 8px 20px;
            background: rgba(18, 158, 111, 0.25);
            border: 1px solid var(--primary-light);
            color: var(--primary-light);
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            letter-spacing: 0.5px;
        }

        .hero-title {
            font-size: 3.2rem;
            font-weight: 800;
            line-height: 1.15;
            margin-bottom: 1.2rem;
            background: linear-gradient(135deg, #ffffff 0%, #cbd5e1 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-title span {
            background: linear-gradient(135deg, #34d399 0%, var(--primary-light) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle {
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-bottom: 2.5rem;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 14px 32px;
            background: linear-gradient(135deg, var(--primary-light), var(--primary));
            color: white;
            font-weight: 600;
            border-radius: 12px;
            text-decoration: none;
            box-shadow: 0 10px 25px -5px rgba(18, 158, 111, 0.4);
            transition: all 0.3s ease;
        }

        .hero-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px -5px rgba(18, 158, 111, 0.6);
        }

        /* SECTIONS COMMON */
        .section {
            padding: 5rem 5%;
        }

        .section-header {
            text-align: center;
            max-width: 650px;
            margin: 0 auto 3.5rem auto;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 800;
            color: #fff;
            margin-bottom: 0.8rem;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--primary-light);
            margin: 8px auto 0 auto;
            border-radius: 2px;
        }

        .section-desc {
            color: var(--text-muted);
            font-size: 1rem;
        }

        /* PRODUCT & SERVICE GRID */
        .gallery-grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.8rem;
        }

        .media-card {
            background: var(--bg-card);
            border: 1px solid var(--glass-border);
            border-radius: 18px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            height: 280px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .media-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-light);
            box-shadow: 0 20px 40px rgba(18, 158, 111, 0.25);
        }

        .media-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        .media-card:hover img {
            transform: scale(1.1);
        }

        .media-card::before {
            content: '🔍 Click to View';
            position: absolute;
            inset: 0;
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(2px);
            color: #fff;
            font-weight: 600;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            z-index: 2;
            transition: opacity 0.3s ease;
            pointer-events: none; /* Allows direct click to the underlying element */
        }

        .media-card:hover::before {
            opacity: 1;
        }

        /* VIDEO CONTAINER */
        .video-wrapper {
            margin-top: 3rem;
            width: 100%;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
            background: var(--bg-card);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 1rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            text-align: center;
        }

        .video-wrapper h3 {
            color: var(--primary-light);
            font-size: 1.2rem;
            margin-bottom: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .video-container {
            width: 100%;
            max-height: 480px;
            border-radius: 14px;
            overflow: hidden;
            background: #000;
        }

        .video-container video {
            width: 100%;
            height: 100%;
            max-height: 480px;
            object-fit: cover;
            display: block;
        }

        /* ABOUT SECTION */
        .about-card {
            background: var(--bg-card);
            border: 1px solid var(--glass-border);
            border-radius: 24px;
            padding: 3rem;
            max-width: 900px;
            margin: 0 auto;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .about-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .feature-item {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--glass-border);
            padding: 1.25rem;
            border-radius: 16px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .feature-icon {
            background: rgba(18, 158, 111, 0.2);
            color: var(--primary-light);
            width: 40px;
            height: 40px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        /* CONTACT & LOCATION */
        .contact-wrapper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            max-width: 1100px;
            margin: 0 auto;
        }

        .contact-box {
            background: linear-gradient(135deg, rgba(18, 158, 111, 0.15), rgba(30, 41, 59, 0.8));
            border: 1px solid rgba(18, 158, 111, 0.3);
            border-radius: 20px;
            padding: 2.5rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .contact-item {
            margin-bottom: 1.5rem;
        }

        .contact-item h4 {
            color: var(--primary-light);
            margin-bottom: 0.3rem;
            font-size: 1.1rem;
        }

        .map-frame {
            width: 100%;
            height: 100%;
            min-height: 350px;
            border-radius: 20px;
            border: 1px solid var(--glass-border);
        }

        /* LIGHTBOX */
        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            justify-content: center;
            align-items: center;
            z-index: 2000;
            cursor: zoom-out;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 85vh;
            border-radius: 16px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
            border: 1px solid var(--glass-border);
        }

        /* FOOTER */
        footer {
            background: #090d16;
            border-top: 1px solid var(--glass-border);
            padding: 2rem 5%;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* ANIMATIONS */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes floatLogo {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-8px); }
        }

        @keyframes pulseGlow {
            0%, 100% { filter: drop-shadow(0 0 12px rgba(18, 158, 111, 0.3)); }
            50% { filter: drop-shadow(0 0 25px rgba(18, 158, 111, 0.7)); }
        }

        /* RESPONSIVE MEDIA QUERIES */
        @media (max-width: 992px) {
            .gallery-grid-3 {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .menu-toggle { display: flex; }

            .nav-links {
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--bg-card);
                flex-direction: column;
                padding: 1.5rem;
                gap: 1.2rem;
                border-bottom: 1px solid var(--glass-border);
                display: none;
            }

            .nav-links.active { display: flex; }

            .hero-top-brand {
                flex-direction: column;
                gap: 10px;
            }
            .hero-top-logo { width: 75px; height: 75px; }
            .hero-top-title { font-size: 1.8rem; }
            .hero-title { font-size: 2.2rem; }

            .gallery-grid-3 {
                grid-template-columns: 1fr;
            }

            .contact-wrapper { grid-template-columns: 1fr; }
            .section { padding: 3.5rem 4%; }
        }
    </style>
</head>
<body>

    <!-- STICKY NAVBAR -->
    <nav class="navbar">
        <a href="#" class="brand">
            <img src="assets/T.png" alt="City Electric Works Logo">
            <div class="brand-text">CITY <span>ELECTRIC WORKS</span></div>
        </a>
        
        <div class="menu-toggle" id="menuToggle">
            <span></span>
            <span></span>
            <span></span>
        </div>

        <ul class="nav-links" id="navLinks">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#products">Products</a></li>
            <li><a href="#about">About Us</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- HERO SECTION -->
    <section id="home" class="hero">
        <div class="hero-content">
            <div class="hero-top-brand">
                <img src="assets/T.png" alt="City Electric Works Logo" class="hero-top-logo">
                <div class="hero-top-title">CITY <span>ELECTRIC WORKS</span></div>
            </div>

            <div class="hero-badge">⚡ Serving Islamabad for 20+ Years</div>
            <h1 class="hero-title">Powering Your Life With <span>Premium Electrical</span> Solutions</h1>
            <p class="hero-subtitle">Islamabad's trusted partner for top-quality wiring, switches, fans, LED lighting, and heavy-duty industrial equipment.</p>
            <a href="#products" class="hero-btn">🛒 Explore Our Products</a>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section id="services" class="section">
        <div class="section-header">
            <h2 class="section-title">OUR SERVICES</h2>
            <p class="section-desc">Reliable and certified electrical components for home & business supply</p>
        </div>
        <div class="gallery-grid-3">
            <div class="media-card"><img src="assets/images (001).jfif" alt="Electrical Service 1" class="zoom-img"></div>
            <div class="media-card"><img src="assets/images (02).jfif" alt="Electrical Service 2" class="zoom-img"></div>
            <div class="media-card"><img src="assets/images (1).jfif" alt="Electrical Service 3" class="zoom-img"></div>
            <div class="media-card"><img src="assets/images (4).jfif" alt="Electrical Service 4" class="zoom-img"></div>
            <div class="media-card"><img src="assets/images000.webp" alt="Electrical Service 5" class="zoom-img"></div>
            <div class="media-card"><img src="assets/images.jfif" alt="Electrical Service 6" class="zoom-img"></div>
        </div>
    </section>

    <!-- PRODUCTS SECTION -->
    <section id="products" class="section" style="background: rgba(255, 255, 255, 0.01);">
        <div class="section-header">
            <h2 class="section-title">FEATURED PRODUCTS</h2>
            <p class="section-desc">Browse our extensive inventory of top-tier brands and equipment</p>
        </div>

        <div class="gallery-grid-3">
            <div class="media-card"><img src="assets/cables.pak.jfif" alt="Pakistan Cables Wiring" class="zoom-img"></div>
            <div class="media-card"><img src="assets/bracket=prod.jpg" alt="Bracket Fan Product" class="zoom-img"></div>
            <div class="media-card"><img src="assets/breker=prod.webp" alt="Safety Breakers" class="zoom-img"></div>
            <div class="media-card"><img src="assets/bulb=prod.png" alt="Energy Saving Light Bulb" class="zoom-img"></div>
            <div class="media-card"><img src="assets/cable=products.jfif" alt="Industrial Cables" class="zoom-img"></div>
            <div class="media-card"><img src="assets/fan=products.jpg" alt="Ceiling Fan Collection" class="zoom-img"></div>
            <div class="media-card"><img src="assets/heat=prod.jpg" alt="Electrical Heater Element" class="zoom-img"></div>
            <div class="media-card"><img src="assets/heater=prod.jfif" alt="Electric Room Heater" class="zoom-img"></div>
            <div class="media-card"><img src="assets/osaka-smd=prod.webp" alt="Osaka SMD Lights" class="zoom-img"></div>
            <div class="media-card"><img src="assets/prime=products.jfif" alt="Prime Switches" class="zoom-img"></div>
            <div class="media-card"><img src="assets/tj-allure-black-4-gang-switch=products.jpg" alt="Black 4-Gang Luxury Switch" class="zoom-img"></div>
            <div class="media-card"><img src="assets/tj=products.jfif" alt="TJ Electrical Products" class="zoom-img"></div>
            <div class="media-card"><img src="assets/WhatsApp Image 2026-07-25 at 10.00.05 PM.jpeg" alt="Electrical Store Stock" class="zoom-img"></div>
            <div class="media-card"><img src="assets/WhatsApp Image 2026-07-25 at 10.04.39 PM (1).jpeg" alt="Lighting Stock" class="zoom-img"></div>
            <div class="media-card"><img src="assets/WhatsApp Image 2026-07-25 at 10.05.06 PM.jpeg" alt="Wiring Display" class="zoom-img"></div>
            <div class="media-card"><img src="assets/WhatsApp Image 2026-07-25 at 10.05.33 PM.jpeg" alt="Store Front Items" class="zoom-img"></div>
            <div class="media-card"><img src="assets/6164jVL3U5L.jpg" alt="Electrical Accessories" class="zoom-img"></div>
        </div>

        <!-- PRODUCT VIDEO SHOWCASE -->
        <div class="video-wrapper">
            <h3>📹 Featured Product Showcase</h3>
            <div class="video-container">
                <video controls muted autoplay loop>
                    <source src="assets/WhatsApp Video 2026-08-18 at 10.08.41 PM.mp4" type="video/mp4">
                </video>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="section">
        <div class="about-card">
            <div class="section-header" style="margin-bottom: 2rem;">
                <h2 class="section-title">ABOUT CITY ELECTRIC WORKS</h2>
            </div>
            <p style="color: var(--text-muted); text-align: center; font-size: 1.05rem; line-height: 1.8;">
                At <b>CITY ELECTRIC WORKS</b>, we believe electricity powers life — and we make sure you get the highest quality products to keep your home and business running smoothly. Serving Islamabad for over <b>20+ years</b> with trusted electrical supplies.
            </p>
            <div class="about-features">
                <div class="feature-item">
                    <div class="feature-icon">✔</div>
                    <div><b>Top Quality Products</b><br><small style="color:var(--text-muted);">100% Genuine Brands</small></div>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">💰</div>
                    <div><b>Affordable Prices</b><br><small style="color:var(--text-muted);">Guaranteed Satisfaction</small></div>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">💡</div>
                    <div><b>Expert Guidance</b><br><small style="color:var(--text-muted);">Technical Support</small></div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT & LOCATION SECTION -->
    <section id="contact" class="section">
        <div class="section-header">
            <h2 class="section-title">VISIT OR CONTACT US</h2>
            <p class="section-desc">Get in touch for bulk orders, inquiries, or store visits</p>
        </div>
        <div class="contact-wrapper">
            <div class="contact-box">
                <div class="contact-item">
                    <h4>📞 Phone / WhatsApp</h4>
                    <p style="color: #cbd5e1;">+92 3005163531</p>
                </div>
                <div class="contact-item">
                    <h4>📍 Store Location</h4>
                    <p style="color: #cbd5e1;">H583+23V, Soan Ave, Soan Gardens Block D, Islamabad, Pakistan</p>
                </div>
                <div class="contact-item" style="margin-bottom: 0;">
                    <h4>🕒 Store Hours</h4>
                    <p style="color: #cbd5e1;">Monday – Sunday (9:00 AM – 9:00 PM)</p>
                </div>
            </div>

            <div>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3324.548205865444!2d73.15008237440736!3d33.565112943297365!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38dfed2cd4a20c91%3A0xe677ba8899959956!2sCity%20Electric%20Store!5e0!3m2!1sen!2s!4v1755531690576!5m2!1sen!2s" class="map-frame" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>© City Electric Works Islamabad. All Rights Reserved.</p>
    </footer>

    <!-- LIGHTBOX MODAL -->
    <div id="lightbox">
        <img id="lightbox-img" src="" alt="Zoomed View">
    </div>

    <!-- JAVASCRIPT -->
    <script>
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        const cards = document.querySelectorAll('.media-card');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightbox-img');

        cards.forEach(card => {
            card.addEventListener('click', () => {
                const img = card.querySelector('img');
                if (img) {
                    lightbox.style.display = 'flex';
                    lightboxImg.src = img.src;
                }
            });
        });

        lightbox.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });
    </script>
</body>
</html>
