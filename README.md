<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NEOX COMBAT SPORTS</title>
    <style>
        :root {
            --primary: #00bfff; /* Strahlendes Hellblau/Türkis wie auf dem Bild */
            --dark-bg: #02060d; /* Tiefschwarzer, leicht bläulicher Hintergrund */
            --card-bg: #070f1e; /* Dunkelblaue Produktboxen */
            --text-light: #ffffff;
            --text-gray: #94a3b8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--text-light);
            overflow-x: hidden;
        }

        /* 1. Promo-Leiste ganz oben */
        .promo-bar {
            background: linear-gradient(90deg, #02060d, #0b192c, #02060d);
            text-align: center;
            padding: 8px 20px;
            font-size: 11px;
            letter-spacing: 1px;
            text-transform: uppercase;
            border-bottom: 1px solid rgba(0, 191, 255, 0.2);
            color: var(--text-light);
        }
        .promo-bar span {
            color: var(--primary);
            font-weight: bold;
        }

        /* 2. Navigationsleiste */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            background: rgba(2, 6, 13, 0.95);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .logo {
            display: flex;
            flex-direction: column;
        }
        .logo .main-title {
            font-size: 26px;
            font-weight: 900;
            letter-spacing: 2px;
            color: var(--text-light);
        }
        .logo .sub-title {
            font-size: 10px;
            letter-spacing: 3px;
            color: var(--primary);
            text-transform: uppercase;
            margin-top: -4px;
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin: 0 20px;
        }
        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-size: 13px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: color 0.3s;
        }
        nav ul li a:hover, nav ul li a.active {
            color: var(--primary);
        }
        .nav-icons {
            display: flex;
            gap: 20px;
            font-size: 18px;
            cursor: pointer;
        }
        .nav-icons span:hover {
            color: var(--primary);
        }

        /* 3. Hero / Startbereich */
        .hero {
            position: relative;
            height: 85vh;
            display: flex;
            align-items: center;
            padding: 0 8%;
            /* Platzhalter für den Athleten im Hintergrund */
            background: linear-gradient(90deg, rgba(2,6,13,1) 35%, rgba(2,6,13,0.6) 60%, rgba(7,15,30,0.3) 100%), 
                        url('https://unsplash.com') no-repeat center right;
            background-size: cover;
        }
        .hero-content {
            max-width: 600px;
            z-index: 2;
        }
        .hero h1 {
            font-size: 4rem;
            font-weight: 900;
            line-height: 1.1;
            text-transform: uppercase;
            margin-bottom: 25px;
            letter-spacing: 1px;
        }
        .hero h1 span {
            color: var(--primary);
            display: block;
        }
        .hero p {
            font-size: 15px;
            color: var(--text-gray);
            margin-bottom: 35px;
            line-height: 1.6;
            max-width: 450px;
        }
        .hero-buttons {
            display: flex;
            gap: 20px;
        }
        .btn-filled {
            background-color: var(--primary);
            color: #000;
            border: none;
            padding: 14px 28px;
            font-size: 12px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .btn-filled:hover {
            box-shadow: 0 0 20px var(--primary);
            transform: translateY(-2px);
        }
        .btn-outline {
            background: transparent;
            border: 2px solid var(--text-light);
            color: var(--text-light);
            padding: 14px 28px;
            font-size: 12px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .btn-outline:hover {
            border-color: var(--primary);
            color: var(--primary);
            transform: translateY(-2px);
        }

        /* 4. Bestseller Sektion */
        .bestseller {
            padding: 80px 5%;
            text-align: center;
        }
        .bestseller h2 {
            font-size: 22px;
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-bottom: 50px;
            position: relative;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }
        .product-card {
            background-color: var(--card-bg);
            border-radius: 6px;
            padding: 25px 15px;
            text-align: center;
            position: relative;
            border: 1px solid rgba(255, 255, 255, 0.03);
            transition: all 0.3s ease;
        }
        .product-card:hover {
            transform: translateY(-5px);
            border-color: rgba(0, 191, 255, 0.4);
            box-shadow: 0 10px 30px rgba(0, 191, 255, 0.1);
        }
        .badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: var(--primary);
            color: #000;
            font-size: 10px;
            font-weight: 800;
            padding: 3px 8px;
            border-radius: 3px;
            text-transform: uppercase;
        }
        .product-img-placeholder {
            height: 180px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px;
            opacity: 0.8;
        }
        .product-card h3 {
            font-size: 12px;
            letter-spacing: 1px;
            text-transform: uppercase;
            margin-bottom: 8px;
            color: var(--text-light);
        }
        .price {
            color: var(--primary);
            font-weight: 700;
            font-size: 14px;
        }
        .btn-shop {
            background: transparent;
            border: 1px solid var(--text-light);
            color: var(--text-light);
            padding: 10px 40px;
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .btn-shop:hover {
            background-color: var(--text-light);
            color: #000;
        }

        /* 5. Info-Leiste ganz unten */
        .info-footer {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            padding: 40px 5%;
            background-color: #010409;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            gap: 20px;
        }
        .info-item {
            display: flex;
            align-items: center;
            gap: 15px;
            max-width: 250px;
            text-align: left;
        }
        .info-icon {
            font-size: 24px;
            color: var(--primary);
        }
        .info-text h4 {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 2px;
        }
        .info-text p {
            font-size: 11px;
            color: var(--text-gray);
        }
    </style>
</head>
<body>

    <!-- 1. Promo-Leiste -->
    <div class="promo-bar">
        Kostenloser Versand ab 60€ | Code: <span>NEOX10</span> für 10% Rabatt
    </div>

    <!-- 2. Header -->
    <header>
        <div class="logo">
            <span class="main-title">NEOX</span>
            <span class="sub-title">Combat Sports</span>
        </div>
        <nav>
            <ul>
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#">Shop</a></li>
                <li><a href="#">Kollektion</a></li>
                <li><a href="#">Über uns</a></li>
                <li><a href="#">Kontakt</a></li>
            </ul>
        </nav>
        <div class="nav-icons">
            <span>🔍</span>
            <span>👤</span>
            <span>🛒</span>
        </div>
    </header>

    <!-- 3. Hero Bereich -->
    <section class="hero">
        <div class="hero-content">
            <h1>Train Hard. <span>Wear Neox.</span></h1>
            <p>Hochwertige Sportbekleidung für Athleten, die keine Kompromisse machen.</p>
            <div class="hero-buttons">
                <button class="btn-filled">Jetzt Shoppen →</button>
                <button class="btn-outline">Unsere Kollektion</button>
            </div>
        </div>
    </section>

    <!-- 4. Bestseller Bereich -->
    <section class="bestseller">
        <h2>Unsere Bestseller</h2>
        <div class="product-grid">
            <!-- Karte 1 -->
            <div class="product-card">
