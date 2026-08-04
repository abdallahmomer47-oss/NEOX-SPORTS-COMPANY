<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NEOX COMBAT SPORTS</title>
    <style>
        :root {
            --primary: #00ffcc;
            --dark: #0a0f1d;
            --light: #ffffff;
            --gray: #1e293b;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: var(--dark);
            color: var(--light);
            overflow-x: hidden;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 5%;
            background: rgba(10, 15, 29, 0.9);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(0, 255, 204, 0.1);
        }
        .logo-container {
            display: flex;
            align-items: center;
        }
        .logo-img {
            height: 50px; /* Ändert die Größe deines Logos in der Menüleiste */
            object-fit: contain;
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin-left: 30px;
        }
        nav ul li a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: var(--primary);
        }
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            background: linear-gradient(135deg, rgba(10,15,29,1) 0%, rgba(30,41,59,1) 100%);
        }
        /* Großes Logo im Startbereich */
        .hero-logo {
            height: 180px;
            margin-bottom: 20px;
            animation: pulse 2s infinite alternate;
        }
        @keyframes pulse {
            from { transform: scale(1); filter: drop-shadow(0 0 5px rgba(0,255,204,0.3)); }
            to { transform: scale(1.05); filter: drop-shadow(0 0 20px var(--primary)); }
        }
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }
        .hero h1 span {
            color: var(--primary);
        }
        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 40px;
            color: #94a3b8;
        }
        .btn {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            padding: 12px 35px;
            font-size: 1rem;
            font-weight: bold;
            text-transform: uppercase;
            cursor: pointer;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        .btn:hover {
            background: var(--primary);
            color: var(--dark);
            box-shadow: 0 0 20px var(--primary);
        }
        .products {
            padding: 100px 5%;
            text-align: center;
        }
        .products h2 {
            font-size: 2.5rem;
            margin-bottom: 50px;
            text-transform: uppercase;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
        }
        .card {
            background: var(--gray);
            border-radius: 10px;
            padding: 30px;
            transition: transform 0.3s;
            border: 1px solid rgba(255,255,255,0.05);
        }
        .card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
        }
        .card .icon {
            font-size: 3rem;
            margin-bottom: 15px;
            display: block;
        }
        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        footer {
            background: #05070f;
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid rgba(255,255,255,0.05);
            color: #64748b;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-container">
            <!-- Logo oben links im Menü -->
            <img src="logo.png" alt="NEOX Logo" class="logo-img">
        </div>
        <nav>
            <ul>
                <li><a href="#">🏠 Home</a></li>
                <li><a href="#">🥊 Equipment</a></li>
                <li><a href="#">🔥 Fight Wear</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <!-- Großes, pulsierendes Logo im Startbereich -->
        <img src="logo.png" alt="NEOX Combat Sports" class="hero-logo">
        <h1>NEOX <span>COMBAT SPORTS</span></h1>
        <p>Die nächste Generation der Kampfsport-Ausrüstung. Schütze dich. Maximiere deine Power. 🥊🔥</p>
        <button class="btn" onclick="alert('Willkommen im NEOX Fight Shop! Die Kollektion droppt bald.')">🛒 Shop betreten</button>
    </section>

    <section class="products">
        <h2>Fight Equipment 🎯</h2>
        <div class="grid">
            <div class="card">
                <span class="icon">🥊</span>
                <h3>Premium Gloves</h3>
                <p>Ergonomischer Handgelenkschutz und maximale Dämpfung für härteste Sparrings.</p>
            </div>
            <div class="card">
                <span class="icon">🩳</span>
                <h3>Fight Shorts</h3>
                <p>Ultra-leichte Materialien mit maximalem Stretch für High-Kicks und Grappling.</p>
            </div>
            <div class="card">
                <span class="icon">🛡️</span>
                <h3>Protection Gear</h3>
                <p>Schienbeinschützer und Bandagen auf Profi-Niveau. Dein Schild im Ring.</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 NEOX COMBAT SPORTS. Alle Rechte vorbehalten. 💪</p>
    </footer>

</body>
</html>
