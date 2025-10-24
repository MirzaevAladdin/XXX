<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TOBA RACING TIME</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Roboto+Condensed:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        body {
            box-sizing: border-box;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-black: #0a0a0a;
            --primary-white: #ffffff;
            --primary-blue: #1e40af;
            --neon-green: #00ff88;
            --dark-gray: #1a1a1a;
            --light-gray: #f5f5f5;
            --text-light: #e5e5e5;
            --text-dark: #333333;
        }

        [data-theme="light"] {
            --bg-primary: var(--primary-white);
            --bg-secondary: var(--light-gray);
            --text-primary: var(--text-dark);
            --text-secondary: #666666;
            --card-bg: #ffffff;
            --border-color: #e0e0e0;
        }

        [data-theme="dark"] {
            --bg-primary: var(--primary-black);
            --bg-secondary: var(--dark-gray);
            --text-primary: var(--text-light);
            --text-secondary: #b0b0b0;
            --card-bg: #1a1a1a;
            --border-color: #333333;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: var(--bg-primary);
            color: var(--text-primary);
            transition: all 0.3s ease;
            overflow-x: hidden;
        }

        /* Header */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 2rem;
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-family: 'Roboto Condensed', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--neon-green);
            text-shadow: 0 0 10px var(--neon-green);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-item {
            cursor: pointer;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            transition: all 0.3s ease;
            color: var(--primary-white);
            font-weight: 500;
            position: relative;
            overflow: hidden;
        }

        .nav-item:hover {
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 255, 136, 0.3);
        }

        .nav-item.active {
            background: var(--neon-green);
            color: var(--primary-black);
        }

        .controls {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .theme-toggle {
            background: none;
            border: 2px solid var(--neon-green);
            color: var(--neon-green);
            padding: 0.5rem;
            border-radius: 50%;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .theme-toggle:hover {
            background: var(--neon-green);
            color: var(--primary-black);
            transform: rotate(180deg);
        }

        .language-selector {
            display: flex;
            gap: 0.5rem;
        }

        .lang-btn {
            background: none;
            border: 1px solid var(--border-color);
            color: var(--text-primary);
            padding: 0.3rem 0.6rem;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.8rem;
        }

        .lang-btn:hover, .lang-btn.active {
            background: var(--neon-green);
            color: var(--primary-black);
            border-color: var(--neon-green);
        }

        /* Main Content */
        .main-content {
            margin-top: 80px;
            min-height: calc(100vh - 80px);
        }

        .page {
            display: none;
            opacity: 0;
            transform: translateX(100px);
            transition: all 0.5s ease;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .page.active {
            display: block;
            opacity: 1;
            transform: translateX(0);
        }

        /* Home Page */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, rgba(10, 10, 10, 0.8), rgba(30, 64, 175, 0.6)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><defs><linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" style="stop-color:%23001122"/><stop offset="100%" style="stop-color:%23003366"/></linearGradient></defs><rect width="1200" height="800" fill="url(%23bg)"/><path d="M0,400 Q300,200 600,400 T1200,400 L1200,800 L0,800 Z" fill="%23004488" opacity="0.3"/></svg>');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero-bg-animation {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }

        .cyclist-silhouette {
            position: absolute;
            font-size: 3rem;
            opacity: 0.1;
            animation: cyclistMove 15s linear infinite;
        }

        .cyclist-1 {
            top: 20%;
            animation-delay: 0s;
        }

        .cyclist-2 {
            top: 50%;
            animation-delay: -5s;
        }

        .cyclist-3 {
            top: 70%;
            animation-delay: -10s;
        }

        @keyframes cyclistMove {
            0% {
                left: -10%;
                transform: translateY(0);
            }
            25% {
                transform: translateY(-20px);
            }
            50% {
                transform: translateY(0);
            }
            75% {
                transform: translateY(20px);
            }
            100% {
                left: 110%;
                transform: translateY(0);
            }
        }

        .road-lines {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: repeating-linear-gradient(
                90deg,
                transparent,
                transparent 20px,
                rgba(0, 255, 136, 0.3) 20px,
                rgba(0, 255, 136, 0.3) 40px
            );
            animation: roadMove 3s linear infinite;
        }

        @keyframes roadMove {
            0% { transform: translateX(0); }
            100% { transform: translateX(-40px); }
        }

        .hero-content {
            z-index: 2;
            max-width: 900px;
            padding: 2rem;
        }

        .hero h1 {
            font-family: 'Roboto Condensed', sans-serif;
            font-size: 4.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--primary-white), var(--neon-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 2s ease-in-out infinite alternate;
        }

        .hero-subtitle {
            font-size: 1.2rem;
            color: var(--neon-green);
            font-weight: 600;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .hero-description {
            font-size: 1.3rem;
            margin-bottom: 3rem;
            color: var(--text-light);
            opacity: 0.9;
            line-height: 1.6;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            display: block;
            font-size: 3rem;
            font-weight: 700;
            color: var(--neon-green);
            font-family: 'Roboto Condensed', sans-serif;
        }

        .stat-label {
            display: block;
            font-size: 0.9rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 0.5rem;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        @keyframes glow {
            from { text-shadow: 0 0 20px rgba(0, 255, 136, 0.5); }
            to { text-shadow: 0 0 30px rgba(0, 255, 136, 0.8); }
        }

        .cta-button {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            overflow: hidden;
        }

        .cta-button.primary {
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            color: var(--primary-white);
        }

        .cta-button.secondary {
            background: transparent;
            color: var(--primary-white);
            border: 2px solid var(--neon-green);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 255, 136, 0.4);
        }

        .cta-button.secondary:hover {
            background: var(--neon-green);
            color: var(--primary-black);
        }

        .cta-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }

        .cta-button:hover::before {
            left: 100%;
        }

        /* About Page */
        .team-intro {
            background: var(--card-bg);
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            margin-bottom: 3rem;
            border: 1px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        .team-intro::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-blue), var(--neon-green));
        }

        .intro-content h3 {
            font-size: 2rem;
            color: var(--neon-green);
            margin-bottom: 1rem;
            font-family: 'Roboto Condensed', sans-serif;
        }

        .intro-content p {
            font-size: 1.2rem;
            line-height: 1.6;
            color: var(--text-secondary);
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .about-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .about-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 255, 136, 0.1);
        }

        .about-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-blue), var(--neon-green));
        }

        .card-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        .achievements-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin-top: 1rem;
        }

        .achievement-item {
            text-align: center;
            padding: 1rem;
            background: var(--bg-secondary);
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .achievement-item:hover {
            transform: scale(1.05);
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            color: var(--primary-white);
        }

        .achievement-number {
            display: block;
            font-size: 2rem;
            font-weight: 700;
            color: var(--neon-green);
            font-family: 'Roboto Condensed', sans-serif;
        }

        .achievement-item:hover .achievement-number {
            color: var(--primary-white);
        }

        .achievement-text {
            display: block;
            font-size: 0.9rem;
            margin-top: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .values-list {
            list-style: none;
            padding: 0;
            margin-top: 1rem;
        }

        .values-list li {
            padding: 0.8rem 0;
            border-bottom: 1px solid var(--border-color);
            transition: all 0.3s ease;
            font-size: 1.1rem;
        }

        .values-list li:hover {
            color: var(--neon-green);
            transform: translateX(10px);
        }

        .values-list li:last-child {
            border-bottom: none;
        }

        .team-members {
            margin-top: 1rem;
        }

        .member-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background: var(--bg-secondary);
            border-radius: 10px;
            margin-bottom: 1rem;
            transition: all 0.3s ease;
        }

        .member-item:hover {
            transform: translateX(10px);
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            color: var(--primary-white);
        }

        .member-avatar {
            font-size: 2.5rem;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--card-bg);
            border-radius: 50%;
            border: 2px solid var(--neon-green);
        }

        .member-info h4 {
            margin: 0;
            font-size: 1.1rem;
            font-weight: 600;
        }

        .member-info p {
            margin: 0.2rem 0 0 0;
            font-size: 0.9rem;
            opacity: 0.8;
        }

        /* Calendar */
        .calendar-container {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 2rem;
            margin-top: 2rem;
            border: 1px solid var(--border-color);
        }

        .calendar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }

        .calendar-nav {
            background: var(--neon-green);
            color: var(--primary-black);
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .calendar-nav:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0, 255, 136, 0.3);
        }

        .events-list {
            display: grid;
            gap: 1rem;
        }

        .event-item {
            background: var(--bg-secondary);
            padding: 1.5rem;
            border-radius: 15px;
            border-left: 4px solid var(--neon-green);
            transition: all 0.3s ease;
        }

        .event-item:hover {
            transform: translateX(10px);
            box-shadow: 0 5px 15px rgba(0, 255, 136, 0.2);
        }

        /* Gallery */
        .gallery-upload {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid var(--border-color);
        }

        .upload-area {
            border: 2px dashed var(--neon-green);
            border-radius: 15px;
            padding: 3rem;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .upload-area:hover {
            background: rgba(0, 255, 136, 0.05);
            border-color: var(--primary-blue);
        }

        .upload-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .upload-area h3 {
            color: var(--neon-green);
            margin-bottom: 0.5rem;
            font-family: 'Roboto Condensed', sans-serif;
        }

        .upload-area p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
        }

        .upload-btn {
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            color: var(--primary-white);
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .upload-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 255, 136, 0.3);
        }

        .gallery-categories {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .category-btn {
            background: var(--card-bg);
            color: var(--text-primary);
            border: 2px solid var(--border-color);
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .category-btn:hover, .category-btn.active {
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            color: var(--primary-white);
            border-color: transparent;
            transform: translateY(-2px);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .gallery-item {
            aspect-ratio: 1;
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-white);
        }

        .gallery-content {
            font-size: 4rem;
            z-index: 2;
            transition: all 0.3s ease;
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0, 0, 0, 0.8));
            color: var(--primary-white);
            padding: 2rem 1rem 1rem;
            transform: translateY(100%);
            transition: all 0.3s ease;
        }

        .gallery-overlay h4 {
            margin: 0;
            font-size: 1.1rem;
            font-weight: 600;
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(0, 255, 136, 0.3);
        }

        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }

        .gallery-item:hover .gallery-content {
            transform: translateY(-20px);
        }

        .gallery-item.hidden {
            display: none;
        }

        /* Payment */
        .payment-form {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            max-width: 600px;
            margin: 2rem auto;
            border: 1px solid var(--border-color);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--text-primary);
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 1rem;
            border: 2px solid var(--border-color);
            border-radius: 10px;
            background: var(--bg-secondary);
            color: var(--text-primary);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus, .form-group select:focus {
            outline: none;
            border-color: var(--neon-green);
            box-shadow: 0 0 10px rgba(0, 255, 136, 0.2);
        }

        .payment-demo {
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            color: white;
            padding: 1rem;
            border-radius: 10px;
            text-align: center;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        /* Contact */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 2rem;
        }

        .contact-form {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--border-color);
        }

        .contact-info {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--border-color);
        }

        .map-container {
            width: 100%;
            height: 300px;
            background: linear-gradient(45deg, var(--primary-blue), var(--neon-green));
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-white);
            font-size: 1.2rem;
            margin-top: 1rem;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            max-width: 90%;
            max-height: 90%;
            border-radius: 15px;
            overflow: hidden;
            position: relative;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: var(--neon-green);
            color: var(--primary-black);
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 1.2rem;
            font-weight: bold;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .header {
                padding: 1rem;
            }
            
            .nav-container {
                flex-wrap: wrap;
                gap: 1rem;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.6s ease forwards;
        }

        /* Loading Animation */
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(0, 255, 136, 0.3);
            border-radius: 50%;
            border-top-color: var(--neon-green);
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body data-theme="dark">
    <header class="header">
        <nav class="nav-container">
            <div class="logo">TOBA RACING TIME</div>
            <ul class="nav-menu">
                <li class="nav-item active" data-page="home" data-en="🏠 Home" data-ru="🏠 Главная" data-az="🏠 Ana səhifə">🏠 Home</li>
                <li class="nav-item" data-page="about" data-en="🚴‍♂️ About" data-ru="🚴‍♂️ О нас" data-az="🚴‍♂️ Haqqımızda">🚴‍♂️ About</li>
                <li class="nav-item" data-page="calendar" data-en="📅 Calendar" data-ru="📅 Календарь" data-az="📅 Təqvim">📅 Calendar</li>
                <li class="nav-item" data-page="gallery" data-en="📸 Gallery" data-ru="📸 Фотографии" data-az="📸 Qalereya">📸 Gallery</li>
                <li class="nav-item" data-page="payment" data-en="💳 Payment" data-ru="💳 Оплата" data-az="💳 Ödəniş">💳 Payment</li>
                <li class="nav-item" data-page="contact" data-en="📍 Contact" data-ru="📍 Контакты" data-az="📍 Əlaqə">📍 Contact</li>
            </ul>
            <div class="controls">
                <div class="language-selector">
                    <button class="lang-btn active" data-lang="en">🇬🇧</button>
                    <button class="lang-btn" data-lang="ru">🇷🇺</button>
                    <button class="lang-btn" data-lang="az">🇦🇿</button>
                </div>
                <button class="theme-toggle" title="Toggle Theme">🌓</button>
            </div>
        </nav>
    </header>

    <main class="main-content">
        <!-- Home Page -->
        <section id="home" class="page active">
            <div class="hero">
                <!-- Animated Background -->
                <div class="hero-bg-animation">
                    <div class="cyclist-silhouette cyclist-1">🚴‍♂️</div>
                    <div class="cyclist-silhouette cyclist-2">🚴‍♀️</div>
                    <div class="cyclist-silhouette cyclist-3">🚵‍♂️</div>
                    <div class="road-lines"></div>
                </div>
                
                <div class="hero-content fade-in">
                    <h1 data-en="TOBA RACING TIME" data-ru="Команда VeloMotion" data-az="VeloMotion Komandası">TOBA RACING TIME</h1>
                    <p class="hero-subtitle" data-en="Professional Cycling Excellence Since 2018" data-ru="Профессиональное велосипедное мастерство с 2018 года" data-az="2018-ci ildən peşəkar velosiped mükəmməlliyi">Professional Cycling Excellence Since 2018</p>
                    <p class="hero-description" data-en="Speed. Freedom. Victory. Join the ultimate cycling experience where champions are made and legends are born." data-ru="Скорость. Свобода. Победа. Присоединяйтесь к лучшей велосипедной команде, где рождаются чемпионы и создаются легенды." data-az="Sürət. Azadlıq. Qələbə. Çempionların yarandığı və əfsanələrin doğulduğu ən yaxşı velosiped təcrübəsinə qoşulun.">Speed. Freedom. Victory. Join the ultimate cycling experience where champions are made and legends are born.</p>
                    
                    <div class="hero-stats">
                        <div class="stat-item">
                            <span class="stat-number">25+</span>
                            <span class="stat-label" data-en="Athletes" data-ru="Спортсменов" data-az="İdmançı">Athletes</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">15</span>
                            <span class="stat-label" data-en="Victories" data-ru="Побед" data-az="Qələbə">Victories</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">12</span>
                            <span class="stat-label" data-en="Countries" data-ru="Стран" data-az="Ölkə">Countries</span>
                        </div>
                    </div>
                    
                    <div class="hero-buttons">
                        <button class="cta-button primary" data-en="Join Our Team" data-ru="Присоединиться" data-az="Komandaya qoşul">Join Our Team</button>
                        <button class="cta-button secondary" data-en="Watch Our Story" data-ru="Наша история" data-az="Hekayəmizi izləyin">Watch Our Story</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Page -->
        <section id="about" class="page">
            <h2 data-en="About TOBA RACING TIME" data-ru="О команде VeloMotion" data-az="VeloMotion Komandası haqqında" style="font-size: 2.5rem; margin-bottom: 2rem; text-align: center;">About TOBA RACING TIME</h2>
            
            <!-- Team Introduction -->
            <div class="team-intro">
                <div class="intro-content">
                    <h3 data-en="Excellence in Motion" data-ru="Совершенство в движении" data-az="Hərəkətdə mükəmməllik">Excellence in Motion</h3>
                    <p data-en="We are more than just a cycling team - we are a family of passionate athletes dedicated to pushing the limits of human performance while inspiring the next generation of cyclists." data-ru="Мы больше чем просто велосипедная команда - мы семья страстных спортсменов, стремящихся раздвинуть границы человеческих возможностей и вдохновить новое поколение велосипедистов." data-az="Biz sadəcə velosiped komandası deyilik - biz insan performansının sərhədlərini genişləndirməyə və yeni nəsil velosipedçiləri ruhlandırmağa həsr olunmuş ehtiraslı idmançılar ailəsiyik.">We are more than just a cycling team - we are a family of passionate athletes dedicated to pushing the limits of human performance while inspiring the next generation of cyclists.</p>
                </div>
            </div>

            <div class="about-grid">
                <div class="about-card fade-in">
                    <div class="card-icon">📚</div>
                    <h3 data-en="Our History" data-ru="Наша история" data-az="Bizim tariximiz">Our History</h3>
                    <p data-en="Founded in 2018 by former Olympic cyclist Maria Rodriguez, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide. Our journey began with just 5 riders and a dream to revolutionize competitive cycling." data-ru="Основанная в 2018 году бывшей олимпийской велосипедисткой Марией Родригес, команда VeloMotion стала одной из ведущих профессиональных велосипедных команд, участвующих в международных чемпионатах. Наш путь начался с 5 гонщиков и мечты революционизировать велоспорт." data-az="2018-ci ildə keçmiş olimpiya velosipedçisi Maria Rodriguez tərəfindən yaradılan VeloMotion Komandası beynəlxalq çempionatlarda iştirak edən aparıcı peşəkar velosiped komandalarından birinə çevrilmişdir. Səyahətimiz cəmi 5 çapışçı və rəqabətli velosipedi inqilab etmək arzusu ilə başladı.">Founded in 2018 by former Olympic cyclist Maria Rodriguez, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide. Our journey began with just 5 riders and a dream to revolutionize competitive cycling.</p>
                </div>
                
                <div class="about-card fade-in">
                    <div class="card-icon">🏆</div>
                    <h3 data-en="Achievements" data-ru="Достижения" data-az="Nailiyyətlər">Achievements</h3>
                    <div class="achievements-list">
                        <div class="achievement-item">
                            <span class="achievement-number">15</span>
                            <span class="achievement-text" data-en="International victories" data-ru="Международных побед" data-az="Beynəlxalq qələbə">International victories</span>
                        </div>
                        <div class="achievement-item">
                            <span class="achievement-number">3</span>
                            <span class="achievement-text" data-en="National championships" data-ru="Национальных чемпионата" data-az="Milli çempionat">National championships</span>
                        </div>
                        <div class="achievement-item">
                            <span class="achievement-number">25</span>
                            <span class="achievement-text" data-en="Professional riders" data-ru="Профессиональных гонщиков" data-az="Peşəkar çapışçı">Professional riders</span>
                        </div>
                        <div class="achievement-item">
                            <span class="achievement-number">12</span>
                            <span class="achievement-text" data-en="Countries competed" data-ru="Стран участия" data-az="Ölkədə yarışlar">Countries competed</span>
                        </div>
                    </div>
                </div>
                
                <div class="about-card fade-in">
                    <div class="card-icon">🎯</div>
                    <h3 data-en="Our Mission" data-ru="Наша миссия" data-az="Bizim missiyamız">Our Mission</h3>
                    <p data-en="To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide. We believe in the power of cycling to transform lives, build communities, and protect our environment." data-ru="Расширять границы велосипедного спорта, продвигая экологичный транспорт и здоровый образ жизни в сообществах по всему миру. Мы верим в силу велоспорта изменять жизни, строить сообщества и защищать окружающую среду." data-az="Velosiped performansının sərhədlərini genişləndirərək, dünya üzrə icmalarda davamlı nəqliyyat və sağlam həyat tərzini təşviq etmək. Biz velosipedin həyatları dəyişdirmək, icmalar qurmaq və ətraf mühiti qorumaq gücünə inanırıq.">To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide. We believe in the power of cycling to transform lives, build communities, and protect our environment.</p>
                </div>
                
                <div class="about-card fade-in">
                    <div class="card-icon">🌟</div>
                    <h3 data-en="Our Values" data-ru="Наши ценности" data-az="Bizim dəyərlərimiz">Our Values</h3>
                    <ul class="values-list">
                        <li data-en="🔥 Passion for excellence" data-ru="🔥 Страсть к совершенству" data-az="🔥 Mükəmməlliyə ehtiras">🔥 Passion for excellence</li>
                        <li data-en="🤝 Team unity and support" data-ru="🤝 Командное единство и поддержка" data-az="🤝 Komanda birliyi və dəstək">🤝 Team unity and support</li>
                        <li data-en="🌱 Environmental responsibility" data-ru="🌱 Экологическая ответственность" data-az="🌱 Ekoloji məsuliyyət">🌱 Environmental responsibility</li>
                        <li data-en="💪 Continuous improvement" data-ru="💪 Постоянное совершенствование" data-az="💪 Davamlı təkmilləşmə">💪 Continuous improvement</li>
                    </ul>
                </div>
                
                <div class="about-card fade-in">
                    <div class="card-icon">👥</div>
                    <h3 data-en="Team Members" data-ru="Участники команды" data-az="Komanda üzvləri">Team Members</h3>
                    <div class="team-members">
                        <div class="member-item">
                            <div class="member-avatar">🚴‍♀️</div>
                            <div class="member-info">
                                <h4 data-en="Maria Rodriguez" data-ru="Мария Родригес" data-az="Maria Rodriguez">Maria Rodriguez</h4>
                                <p data-en="Team Captain & Founder" data-ru="Капитан команды и основатель" data-az="Komanda kapitanı və təsisçi">Team Captain & Founder</p>
                            </div>
                        </div>
                        <div class="member-item">
                            <div class="member-avatar">🚴‍♂️</div>
                            <div class="member-info">
                                <h4 data-en="Alex Thompson" data-ru="Алекс Томпсон" data-az="Alex Thompson">Alex Thompson</h4>
                                <p data-en="Lead Sprinter" data-ru="Ведущий спринтер" data-az="Aparıcı sprinter">Lead Sprinter</p>
                            </div>
                        </div>
                        <div class="member-item">
                            <div class="member-avatar">🚵‍♀️</div>
                            <div class="member-info">
                                <h4 data-en="Sarah Chen" data-ru="Сара Чен" data-az="Sarah Chen">Sarah Chen</h4>
                                <p data-en="Mountain Specialist" data-ru="Специалист по горам" data-az="Dağ mütəxəssisi">Mountain Specialist</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="about-card fade-in">
                    <div class="card-icon">🎯</div>
                    <h3 data-en="Future Goals" data-ru="Будущие цели" data-az="Gələcək məqsədlər">Future Goals</h3>
                    <p data-en="Our vision extends beyond racing victories. By 2025, we aim to establish youth development programs in 20 countries, launch our sustainable cycling gear line, and become carbon-neutral as an organization. We're not just racing towards the finish line - we're racing towards a better future." data-ru="Наше видение выходит за рамки побед в гонках. К 2025 году мы планируем создать программы развития молодежи в 20 странах, запустить линию экологичного велосипедного снаряжения и стать углеродно-нейтральной организацией." data-az="Bizim baxışımız yarış qələbələrindən kənara çıxır. 2025-ci ilə qədər 20 ölkədə gənclər üçün inkişaf proqramları yaratmaq, davamlı velosiped avadanlıqları xəttini işə salmaq və karbon-neytral təşkilat olmaq məqsədindəyik.">Our vision extends beyond racing victories. By 2025, we aim to establish youth development programs in 20 countries, launch our sustainable cycling gear line, and become carbon-neutral as an organization. We're not just racing towards the finish line - we're racing towards a better future.</p>
                </div>
            </div>
        </section>

        <!-- Calendar Page -->
        <section id="calendar" class="page">
            <h2 data-en="Events Calendar" data-ru="Календарь событий" data-az="Tədbirlər təqvimi" style="font-size: 2.5rem; margin-bottom: 2rem; text-align: center;">Events Calendar</h2>
            <div class="calendar-container">
                <div class="calendar-header">
                    <button class="calendar-nav" id="prevMonth">‹</button>
                    <h3 id="currentMonth">December 2024</h3>
                    <button class="calendar-nav" id="nextMonth">›</button>
                </div>
                <div class="events-list" id="eventsList">
                    <div class="event-item">
                        <h4 data-en="Winter Training Camp" data-ru="Зимний тренировочный лагерь" data-az="Qış məşq düşərgəsi">Winter Training Camp</h4>
                        <p data-en="📅 Dec 15-20, 2024 | 📍 Alps, Switzerland" data-ru="📅 15-20 декабря 2024 | 📍 Альпы, Швейцария" data-az="📅 15-20 dekabr 2024 | 📍 Alp dağları, İsveçrə">📅 Dec 15-20, 2024 | 📍 Alps, Switzerland</p>
                    </div>
                    <div class="event-item">
                        <h4 data-en="New Year Championship" data-ru="Новогодний чемпионат" data-az="Yeni il çempionatı">New Year Championship</h4>
                        <p data-en="📅 Jan 5, 2025 | 📍 Barcelona, Spain" data-ru="📅 5 января 2025 | 📍 Барселона, Испания" data-az="📅 5 yanvar 2025 | 📍 Barselona, İspaniya">📅 Jan 5, 2025 | 📍 Barcelona, Spain</p>
                    </div>
                    <div class="event-item">
                        <h4 data-en="Team Building Event" data-ru="Командообразующее мероприятие" data-az="Komanda quruculuğu tədbiri">Team Building Event</h4>
                        <p data-en="📅 Jan 15, 2025 | 📍 Local Training Center" data-ru="📅 15 января 2025 | 📍 Местный тренировочный центр" data-az="📅 15 yanvar 2025 | 📍 Yerli məşq mərkəzi">📅 Jan 15, 2025 | 📍 Local Training Center</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Gallery Page -->
        <section id="gallery" class="page">
            <h2 data-en="Team Gallery" data-ru="Галерея команды" data-az="Komanda qalereyası" style="font-size: 2.5rem; margin-bottom: 2rem; text-align: center;">Team Gallery</h2>
            
            <!-- Upload Section -->
            <div class="gallery-upload">
                <div class="upload-area" id="uploadArea">
                    <div class="upload-icon">📸</div>
                    <h3 data-en="Upload Team Photos" data-ru="Загрузить фото команды" data-az="Komanda şəkillərini yüklə">Upload Team Photos</h3>
                    <p data-en="Drag & drop photos here or click to browse" data-ru="Перетащите фото сюда или нажмите для выбора" data-az="Şəkilləri bura sürükləyin və ya seçmək üçün klikləyin">Drag & drop photos here or click to browse</p>
                    <input type="file" id="photoInput" accept="image/*" multiple style="display: none;">
                    <button class="upload-btn" onclick="document.getElementById('photoInput').click()" data-en="Browse Files" data-ru="Выбрать файлы" data-az="Faylları seç">Browse Files</button>
                </div>
            </div>

            <!-- Gallery Categories -->
            <div class="gallery-categories">
                <button class="category-btn active" data-category="all" data-en="All Photos" data-ru="Все фото" data-az="Bütün şəkillər">All Photos</button>
                <button class="category-btn" data-category="members" data-en="👥 Team Members" data-ru="👥 Участники" data-az="👥 Komanda üzvləri">👥 Team Members</button>
                <button class="category-btn" data-category="races" data-en="Races" data-ru="Гонки" data-az="Yarışlar">Races</button>
                <button class="category-btn" data-category="training" data-en="Training" data-ru="Тренировки" data-az="Məşqlər">Training</button>
                <button class="category-btn" data-category="team" data-en="Team Events" data-ru="Командные события" data-az="Komanda tədbirləri">Team Events</button>
            </div>

            <!-- Gallery Grid -->
            <div class="gallery-grid" id="galleryGrid">
                <!-- Team Members Photos -->
                <div class="gallery-item" data-category="members" onclick="openModal('👩‍🦰', 'Maria Rodriguez - Team Captain')">
                    <div class="gallery-content">👩‍🦰</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Maria Rodriguez - Team Captain" data-ru="Мария Родригес - Капитан команды" data-az="Maria Rodriguez - Komanda kapitanı">Maria Rodriguez - Team Captain</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="members" onclick="openModal('👨‍🦱', 'Alex Thompson - Lead Sprinter')">
                    <div class="gallery-content">👨‍🦱</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Alex Thompson - Lead Sprinter" data-ru="Алекс Томпсон - Ведущий спринтер" data-az="Alex Thompson - Aparıcı sprinter">Alex Thompson - Lead Sprinter</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="members" onclick="openModal('👩‍🦳', 'Sarah Chen - Mountain Specialist')">
                    <div class="gallery-content">👩‍🦳</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Sarah Chen - Mountain Specialist" data-ru="Сара Чен - Специалист по горам" data-az="Sarah Chen - Dağ mütəxəssisi">Sarah Chen - Mountain Specialist</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="members" onclick="openModal('👨‍🦲', 'David Martinez - Endurance Expert')">
                    <div class="gallery-content">👨‍🦲</div>
                    <div class="gallery-overlay">
                        <h4 data-en="David Martinez - Endurance Expert" data-ru="Дэвид Мартинес - Эксперт по выносливости" data-az="David Martinez - Dözümlülük mütəxəssisi">David Martinez - Endurance Expert</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="members" onclick="openModal('👩‍🦱', 'Emma Johnson - Time Trial Specialist')">
                    <div class="gallery-content">👩‍🦱</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Emma Johnson - Time Trial Specialist" data-ru="Эмма Джонсон - Специалист по гонкам на время" data-az="Emma Johnson - Vaxt yarışı mütəxəssisi">Emma Johnson - Time Trial Specialist</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="members" onclick="openModal('👨‍🦰', 'Michael Brown - Team Coach')">
                    <div class="gallery-content">👨‍🦰</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Michael Brown - Team Coach" data-ru="Майкл Браун - Тренер команды" data-az="Michael Brown - Komanda məşqçisi">Michael Brown - Team Coach</h4>
                    </div>
                </div>
                
                <!-- Race Photos -->
                <div class="gallery-item" data-category="races" onclick="openModal('🚴‍♂️', 'Championship Race 2024')">
                    <div class="gallery-content">🚴‍♂️</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Championship Race 2024" data-ru="Чемпионат 2024" data-az="Çempionat yarışı 2024">Championship Race 2024</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="team" onclick="openModal('🏆', 'Victory Celebration')">
                    <div class="gallery-content">🏆</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Victory Celebration" data-ru="Празднование победы" data-az="Qələbə bayramı">Victory Celebration</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="training" onclick="openModal('🌄', 'Mountain Training')">
                    <div class="gallery-content">🌄</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Mountain Training" data-ru="Горные тренировки" data-az="Dağ məşqləri">Mountain Training</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="races" onclick="openModal('🚵‍♀️', 'Women\'s Competition')">
                    <div class="gallery-content">🚵‍♀️</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Women's Competition" data-ru="Женские соревнования" data-az="Qadın yarışları">Women's Competition</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="races" onclick="openModal('🏁', 'Finish Line Moments')">
                    <div class="gallery-content">🏁</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Finish Line Moments" data-ru="Моменты финиша" data-az="Finiş xətti anları">Finish Line Moments</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="team" onclick="openModal('🌟', 'Team Awards')">
                    <div class="gallery-content">🌟</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Team Awards" data-ru="Командные награды" data-az="Komanda mükafatları">Team Awards</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="training" onclick="openModal('🚴‍♀️', 'Daily Training')">
                    <div class="gallery-content">🚴‍♀️</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Daily Training" data-ru="Ежедневные тренировки" data-az="Gündəlik məşqlər">Daily Training</h4>
                    </div>
                </div>
                <div class="gallery-item" data-category="training" onclick="openModal('⛰️', 'Alpine Challenge')">
                    <div class="gallery-content">⛰️</div>
                    <div class="gallery-overlay">
                        <h4 data-en="Alpine Challenge" data-ru="Альпийский вызов" data-az="Alp çağırışı">Alpine Challenge</h4>
                    </div>
                </div>
            </div>
        </section>

        <!-- Payment Page -->
        <section id="payment" class="page">
            <h2 data-en="Membership Payment" data-ru="Оплата участия" data-az="Üzvlük ödənişi" style="font-size: 2.5rem; margin-bottom: 2rem; text-align: center;">Membership Payment</h2>
            <div class="payment-form">
                <div class="payment-demo">
                    <span data-en="⚠️ DEMO MODE - This is a sample payment form for demonstration purposes only" data-ru="⚠️ ДЕМО РЕЖИМ - Это образец формы оплаты только для демонстрации" data-az="⚠️ DEMO REJİMİ - Bu yalnız nümayiş məqsədləri üçün nümunə ödəniş formasıdır">⚠️ DEMO MODE - This is a sample payment form for demonstration purposes only</span>
                </div>
                <form id="paymentForm">
                    <div class="form-group">
                        <label for="membershipType" data-en="Membership Type" data-ru="Тип участия" data-az="Üzvlük növü">Membership Type</label>
                        <select id="membershipType" required>
                            <option value="basic" data-en="Basic - $50/month" data-ru="Базовый - $50/месяц" data-az="Əsas - $50/ay">Basic - $50/month</option>
                            <option value="premium" data-en="Premium - $100/month" data-ru="Премиум - $100/месяц" data-az="Premium - $100/ay">Premium - $100/month</option>
                            <option value="pro" data-en="Professional - $200/month" data-ru="Профессиональный - $200/месяц" data-az="Peşəkar - $200/ay">Professional - $200/month</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="currency" data-en="Currency" data-ru="Валюта" data-az="Valyuta">Currency</label>
                        <select id="currency" required>
                            <option value="usd">USD ($)</option>
                            <option value="eur">EUR (€)</option>
                            <option value="azn">AZN (₼)</option>
                            <option value="rub">RUB (₽)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="fullName" data-en="Full Name" data-ru="Полное имя" data-az="Tam ad">Full Name</label>
                        <input type="text" id="fullName" required>
                    </div>
                    <div class="form-group">
                        <label for="email" data-en="Email Address" data-ru="Email адрес" data-az="Email ünvanı">Email Address</label>
                        <input type="email" id="email" required>
                    </div>
                    <button type="submit" class="cta-button" style="width: 100%;" data-en="Process Payment (Demo)" data-ru="Обработать платеж (Демо)" data-az="Ödənişi emal et (Demo)">Process Payment (Demo)</button>
                </form>
            </div>
        </section>

        <!-- Contact Page -->
        <section id="contact" class="page">
            <h2 data-en="Contact Us" data-ru="Свяжитесь с нами" data-az="Bizimlə əlaqə" style="font-size: 2.5rem; margin-bottom: 2rem; text-align: center;">Contact Us</h2>
            <div class="contact-grid">
                <div class="contact-form">
                    <h3 data-en="Send us a message" data-ru="Отправьте нам сообщение" data-az="Bizə mesaj göndərin">Send us a message</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="contactName" data-en="Your Name" data-ru="Ваше имя" data-az="Adınız">Your Name</label>
                            <input type="text" id="contactName" required>
                        </div>
                        <div class="form-group">
                            <label for="contactEmail" data-en="Your Email" data-ru="Ваш Email" data-az="Email ünvanınız">Your Email</label>
                            <input type="email" id="contactEmail" required>
                        </div>
                        <div class="form-group">
                            <label for="message" data-en="Message" data-ru="Сообщение" data-az="Mesaj">Message</label>
                            <textarea id="message" rows="5" style="width: 100%; padding: 1rem; border: 2px solid var(--border-color); border-radius: 10px; background: var(--bg-secondary); color: var(--text-primary); font-family: inherit; resize: vertical;" required></textarea>
                        </div>
                        <button type="submit" class="cta-button" style="width: 100%;" data-en="Send Message" data-ru="Отправить сообщение" data-az="Mesaj göndər">Send Message</button>
                    </form>
                </div>
                <div class="contact-info">
                    <h3 data-en="Get in touch" data-ru="Свяжитесь с нами" data-az="Əlaqə saxlayın">Get in touch</h3>
                    <div style="margin: 2rem 0;">
                        <p><strong data-en="📍 Address:" data-ru="📍 Адрес:" data-az="📍 Ünvan:">📍 Address:</strong></p>
                        <p data-en="123 Cycling Street, Sports District, City 12345" data-ru="ул. Велосипедная 123, Спортивный район, Город 12345" data-az="Velosiped küçəsi 123, İdman rayonu, Şəhər 12345">123 Cycling Street, Sports District, City 12345</p>
                        
                        <p style="margin-top: 1rem;"><strong data-en="📞 Phone:" data-ru="📞 Телефон:" data-az="📞 Telefon:">📞 Phone:</strong></p>
                        <p>+1 (555) 123-4567</p>
                        
                        <p style="margin-top: 1rem;"><strong data-en="✉️ Email:" data-ru="✉️ Email:" data-az="✉️ Email:">✉️ Email:</strong></p>
                        <p>info@velomotionteam.com</p>
                    </div>
                    <div class="map-container">
                        <span data-en="🗺️ Interactive Map Location" data-ru="🗺️ Интерактивная карта" data-az="🗺️ İnteraktiv xəritə">🗺️ Interactive Map Location</span>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Modal -->
    <div id="imageModal" class="modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">×</button>
            <div id="modalImage" style="font-size: 10rem; padding: 2rem; background: linear-gradient(45deg, var(--primary-blue), var(--neon-green)); border-radius: 15px; color: white; text-align: center;">🚴‍♂️</div>
        </div>
    </div>

    <script>
        // Language data
        const translations = {
            en: {
                'TOBA RACING TIME': 'TOBA RACING TIME',
                'Speed. Freedom. Victory. Join the ultimate cycling experience.': 'Speed. Freedom. Victory. Join the ultimate cycling experience.',
                'Join Our Team': 'Join Our Team',
                'About TOBA RACING TIME': 'About TOBA RACING TIME',
                'Our History': 'Our History',
                'Founded in 2018, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide.': 'Founded in 2018, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide.',
                'Achievements': 'Achievements',
                '🏆 15 International victories<br>🥇 3 National championships<br>🚴‍♂️ 25 professional riders<br>🌍 Competing in 12 countries': '🏆 15 International victories<br>🥇 3 National championships<br>🚴‍♂️ 25 professional riders<br>🌍 Competing in 12 countries',
                'Our Mission': 'Our Mission',
                'To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide.': 'To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide.'
            },
            ru: {
                'TOBA RACING TIME': 'Команда VeloMotion',
                'Speed. Freedom. Victory. Join the ultimate cycling experience.': 'Скорость. Свобода. Победа. Присоединяйтесь к лучшей велосипедной команде.',
                'Join Our Team': 'Присоединиться',
                'About TOBA RACING TIME': 'О команде VeloMotion',
                'Our History': 'Наша история',
                'Founded in 2018, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide.': 'Основанная в 2018 году, команда VeloMotion стала одной из ведущих профессиональных велосипедных команд, участвующих в международных чемпионатах.',
                'Achievements': 'Достижения',
                '🏆 15 International victories<br>🥇 3 National championships<br>🚴‍♂️ 25 professional riders<br>🌍 Competing in 12 countries': '🏆 15 международных побед<br>🥇 3 национальных чемпионата<br>🚴‍♂️ 25 профессиональных гонщиков<br>🌍 Соревнования в 12 странах',
                'Our Mission': 'Наша миссия',
                'To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide.': 'Расширять границы велосипедного спорта, продвигая экологичный транспорт и здоровый образ жизни в сообществах по всему миру.'
            },
            az: {
                'TOBA RACING TIME': 'VeloMotion Komandası',
                'Speed. Freedom. Victory. Join the ultimate cycling experience.': 'Sürət. Azadlıq. Qələbə. Ən yaxşı velosiped təcrübəsinə qoşulun.',
                'Join Our Team': 'Komandaya qoşul',
                'About TOBA RACING TIME': 'VeloMotion Komandası haqqında',
                'Our History': 'Bizim tariximiz',
                'Founded in 2018, TOBA RACING TIME has become one of the leading professional cycling teams, competing in international championships and inspiring cyclists worldwide.': '2018-ci ildə yaradılan VeloMotion Komandası beynəlxalq çempionatlarda iştirak edən aparıcı peşəkar velosiped komandalarından birinə çevrilmişdir.',
                'Achievements': 'Nailiyyətlər',
                '🏆 15 International victories<br>🥇 3 National championships<br>🚴‍♂️ 25 professional riders<br>🌍 Competing in 12 countries': '🏆 15 beynəlxalq qələbə<br>🥇 3 milli çempionat<br>🚴‍♂️ 25 peşəkar çapışçı<br>🌍 12 ölkədə yarışlar',
                'Our Mission': 'Bizim missiyamız',
                'To push the boundaries of cycling performance while promoting sustainable transportation and healthy lifestyle choices for communities worldwide.': 'Velosiped performansının sərhədlərini genişləndirərək, dünya üzrə icmalarda davamlı nəqliyyat və sağlam həyat tərzini təşviq etmək.'
            }
        };

        let currentLang = 'en';
        let currentTheme = 'dark';

        // Navigation
        function showPage(pageId) {
            // Hide all pages
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Show selected page
            document.getElementById(pageId).classList.add('active');
            
            // Update nav items
            document.querySelectorAll('.nav-item').forEach(item => {
                item.classList.remove('active');
            });
            document.querySelector(`[data-page="${pageId}"]`).classList.add('active');
        }

        // Language switching
        function switchLanguage(lang) {
            currentLang = lang;
            
            // Update language buttons
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            document.querySelector(`[data-lang="${lang}"]`).classList.add('active');
            
            // Update all translatable elements
            document.querySelectorAll('[data-en]').forEach(element => {
                const key = element.getAttribute(`data-${lang}`);
                if (key) {
                    if (element.innerHTML.includes('<br>')) {
                        element.innerHTML = key;
                    } else {
                        element.textContent = key;
                    }
                }
            });
        }

        // Theme switching
        function toggleTheme() {
            currentTheme = currentTheme === 'dark' ? 'light' : 'dark';
            document.body.setAttribute('data-theme', currentTheme);
        }

        // Modal functions
        function openModal(content, title = '') {
            document.getElementById('modalImage').textContent = content;
            document.getElementById('imageModal').classList.add('active');
        }

        function closeModal() {
            document.getElementById('imageModal').classList.remove('active');
        }

        // Gallery functions
        function filterGallery(category) {
            const items = document.querySelectorAll('.gallery-item');
            const buttons = document.querySelectorAll('.category-btn');
            
            // Update active button
            buttons.forEach(btn => btn.classList.remove('active'));
            document.querySelector(`[data-category="${category}"]`).classList.add('active');
            
            // Filter items
            items.forEach(item => {
                if (category === 'all' || item.getAttribute('data-category') === category) {
                    item.classList.remove('hidden');
                } else {
                    item.classList.add('hidden');
                }
            });
        }

        function handleFileUpload(files) {
            const galleryGrid = document.getElementById('galleryGrid');
            
            Array.from(files).forEach((file, index) => {
                if (file.type.startsWith('image/')) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        const galleryItem = document.createElement('div');
                        galleryItem.className = 'gallery-item';
                        galleryItem.setAttribute('data-category', 'team');
                        galleryItem.onclick = () => openModal('📷', file.name);
                        
                        galleryItem.innerHTML = `
                            <div class="gallery-content">📷</div>
                            <div class="gallery-overlay">
                                <h4>${file.name}</h4>
                            </div>
                        `;
                        
                        galleryGrid.appendChild(galleryItem);
                    };
                    reader.readAsDataURL(file);
                }
            });
            
            // Show success message
            const uploadArea = document.getElementById('uploadArea');
            const originalContent = uploadArea.innerHTML;
            uploadArea.innerHTML = `
                <div class="upload-icon">✅</div>
                <h3>${currentLang === 'en' ? 'Photos Uploaded Successfully!' : 
                      currentLang === 'ru' ? 'Фото успешно загружены!' : 
                      'Şəkillər uğurla yükləndi!'}</h3>
                <p>${files.length} ${currentLang === 'en' ? 'photos added to gallery' : 
                                   currentLang === 'ru' ? 'фото добавлено в галерею' : 
                                   'şəkil qalereyaya əlavə edildi'}</p>
            `;
            
            setTimeout(() => {
                uploadArea.innerHTML = originalContent;
            }, 3000);
        }

        // Calendar functionality
        let currentMonth = 11; // December (0-indexed)
        let currentYear = 2024;

        function updateCalendar() {
            const months = {
                en: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
                ru: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
                az: ['Yanvar', 'Fevral', 'Mart', 'Aprel', 'May', 'İyun', 'İyul', 'Avqust', 'Sentyabr', 'Oktyabr', 'Noyabr', 'Dekabr']
            };
            
            document.getElementById('currentMonth').textContent = `${months[currentLang][currentMonth]} ${currentYear}`;
        }

        // Form submissions
        function handlePaymentSubmit(e) {
            e.preventDefault();
            const button = e.target.querySelector('button[type="submit"]');
            const originalText = button.textContent;
            
            button.innerHTML = '<span class="loading"></span> Processing...';
            button.disabled = true;
            
            setTimeout(() => {
                alert(currentLang === 'en' ? 'Demo payment processed successfully!' : 
                      currentLang === 'ru' ? 'Демо-платеж успешно обработан!' : 
                      'Demo ödəniş uğurla emal edildi!');
                button.textContent = originalText;
                button.disabled = false;
                e.target.reset();
            }, 2000);
        }

        function handleContactSubmit(e) {
            e.preventDefault();
            const button = e.target.querySelector('button[type="submit"]');
            const originalText = button.textContent;
            
            button.innerHTML = '<span class="loading"></span> Sending...';
            button.disabled = true;
            
            setTimeout(() => {
                alert(currentLang === 'en' ? 'Message sent successfully!' : 
                      currentLang === 'ru' ? 'Сообщение успешно отправлено!' : 
                      'Mesaj uğurla göndərildi!');
                button.textContent = originalText;
                button.disabled = false;
                e.target.reset();
            }, 2000);
        }

        // Event listeners
        document.addEventListener('DOMContentLoaded', function() {
            // Navigation
            document.querySelectorAll('.nav-item').forEach(item => {
                item.addEventListener('click', () => {
                    showPage(item.getAttribute('data-page'));
                });
            });

            // Language switching
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    switchLanguage(btn.getAttribute('data-lang'));
                });
            });

            // Theme toggle
            document.querySelector('.theme-toggle').addEventListener('click', toggleTheme);

            // Calendar navigation
            document.getElementById('prevMonth').addEventListener('click', () => {
                currentMonth--;
                if (currentMonth < 0) {
                    currentMonth = 11;
                    currentYear--;
                }
                updateCalendar();
            });

            document.getElementById('nextMonth').addEventListener('click', () => {
                currentMonth++;
                if (currentMonth > 11) {
                    currentMonth = 0;
                    currentYear++;
                }
                updateCalendar();
            });

            // Form submissions
            document.getElementById('paymentForm').addEventListener('submit', handlePaymentSubmit);
            document.getElementById('contactForm').addEventListener('submit', handleContactSubmit);

            // Modal close on outside click
            document.getElementById('imageModal').addEventListener('click', (e) => {
                if (e.target === e.currentTarget) {
                    closeModal();
                }
            });

            // CTA button action
            document.querySelector('.cta-button.primary').addEventListener('click', () => {
                showPage('contact');
            });

            document.querySelector('.cta-button.secondary').addEventListener('click', () => {
                showPage('about');
            });

            // Gallery category filters
            document.querySelectorAll('.category-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    filterGallery(btn.getAttribute('data-category'));
                });
            });

            // File upload handling
            const photoInput = document.getElementById('photoInput');
            const uploadArea = document.getElementById('uploadArea');

            photoInput.addEventListener('change', (e) => {
                if (e.target.files.length > 0) {
                    handleFileUpload(e.target.files);
                }
            });

            // Drag and drop functionality
            uploadArea.addEventListener('dragover', (e) => {
                e.preventDefault();
                uploadArea.style.background = 'rgba(0, 255, 136, 0.1)';
            });

            uploadArea.addEventListener('dragleave', (e) => {
                e.preventDefault();
                uploadArea.style.background = '';
            });

            uploadArea.addEventListener('drop', (e) => {
                e.preventDefault();
                uploadArea.style.background = '';
                const files = e.dataTransfer.files;
                if (files.length > 0) {
                    handleFileUpload(files);
                }
            });

            uploadArea.addEventListener('click', () => {
                photoInput.click();
            });

            // Initialize calendar
            updateCalendar();

            // Add fade-in animation to elements when they come into view
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('fade-in');
                    }
                });
            });

            document.querySelectorAll('.about-card, .event-item').forEach(el => {
                observer.observe(el);
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99383dd5f764686a',t:'MTc2MTI5NTk4My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
