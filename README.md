<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>United Boys F.C. - Jeugdvoetbal met passie</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Open+Sans&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2C5E1A;
            --secondary: #F9C80E;
            --dark: #1A1A1A;
            --light: #F8F9FA;
            --accent: #E63946;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .logo {
            height: 60px;
            width: auto;
        }
        
        .logo-text {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--primary);
        }
        
        .logo-text span {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-family: 'Montserrat', sans-serif;
            transition: color 0.3s;
            position: relative;
        }
        
        nav a:hover {
            color: var(--primary);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1574629810360-7efbbe195018?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 2rem;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-family: 'Montserrat', sans-serif;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--dark);
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 2rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-family: 'Montserrat', sans-serif;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background-color: var(--secondary);
            margin: 0.5rem auto 0;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }
        
        @media (min-width: 768px) {
            .about-content {
                grid-template-columns: 1fr 1fr;
            }
        }
        
        .about-text {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .about-text h2 {
            font-family: 'Montserrat', sans-serif;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .matches {
            background-color: #f1f1f1;
            padding: 3rem 0;
        }
        
        .match-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .match-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .match-card:hover {
            transform: translateY(-5px);
        }
        
        .match-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem;
            text-align: center;
            font-weight: 600;
        }
        
        .match-content {
            padding: 1.5rem;
            text-align: center;
        }
        
        .teams {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .team {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 40%;
        }
        
        .team-logo {
            width: 50px;
            height: 50px;
            margin-bottom: 0.5rem;
        }
        
        .vs {
            font-weight: bold;
            font-size: 1.2rem;
            color: var(--accent);
        }
        
        .match-info {
            margin-top: 1rem;
            font-size: 0.9rem;
            color: var(--dark);
        }
        
        .admin-panel {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            margin-top: 2rem;
        }
        
        .admin-title {
            font-family: 'Montserrat', sans-serif;
            color: var(--primary);
            margin-bottom: 1.5rem;
            text-align: center;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .form-group input, 
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Open Sans', sans-serif;
        }
        
        .form-actions {
            text-align: center;
        }
        
        .btn-admin {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn-admin:hover {
            background-color: #1e4a15;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-column h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column li {
            margin-bottom: 0.5rem;
        }
        
        .footer-column a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .social-links a {
            color: white;
            background-color: rgba(255,255,255,0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Mobile menu */
        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                padding: 2rem 0;
                transition: left 0.3s;
            }
            
            nav ul.active {
                left: 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="navbar">
            <div class="logo-container">
                <img src="https://primary.jwwb.nl/public/w/h/c/temp-qdzjsvkxvxfwoekqwpjg/chatgpt-image-11-apr-2025-22_25_50-high.png" alt="United Boys F.C. logo" class="logo">
                <div class="logo-text">United <span>Boys</span></div>
            </div>
            
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">Over ons</a></li>
                    <li><a href="#team">Team</a></li>
                    <li><a href="#matches">Wedstrijden</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#admin" class="btn-admin">Admin</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero" id="home">
        <div class="container">
            <h1>Welkom bij United Boys F.C.</h1>
            <p>Waar jongeren hun voetbaltalenten ontwikkelen in een positieve en ondersteunende omgeving</p>
            <a href="#matches" class="btn">Bekijk aankomende wedstrijden</a>
        </div>
    </section>
    
    <section class="container" id="about">
        <h2 class="section-title">Over Ons</h2>
        <div class="about-content">
            <div class="about-text">
                <h2>Onze Missie</h2>
                <p>United Boys F.C. is opgericht met als doel het rondhangen van jongeren te verminderen en hen een plezierige en leerzame ervaring te bieden door middel van voetbal. We streven ernaar een positieve en ondersteunende omgeving te creëren waarin jonge spelers zich kunnen ontwikkelen, hun talenten kunnen ontdekken en met enthousiasme kunnen genieten van de sport.</p>
                <p>Ons clubverband biedt structuur, motivatie en kameraadschap, zodat elke speler zich gewaardeerd en geïnspireerd voelt.</p>
            </div>
            <div class="about-image">
                <img src="https://images.unsplash.com/photo-1540747913346-19e32dc3e97e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1605&q=80" alt="United Boys team">
            </div>
        </div>
    </section>
    
    <section class="matches" id="matches">
        <div class="container">
            <h2 class="section-title">Aankomende Wedstrijden</h2>
            <div class="match-container">
                <div class="match-card">
                    <div class="match-header">Competitie Wedstrijd</div>
                    <div class="match-content">
                        <div class="teams">
                            <div class="team">
                                <img src="https://primary.jwwb.nl/public/w/h/c/temp-qdzjsvkxvxfwoekqwpjg/chatgpt-image-11-apr-2025-22_25_50-high.png" alt="United Boys" class="team-logo">
                                <div>United Boys</div>
                            </div>
                            <div class="vs">VS</div>
                            <div class="team">
                                <img src="https://via.placeholder.com/50x50" alt="Tegenstander" class="team-logo">
                                <div>FC Rivalen</div>
                            </div>
                        </div>
                        <div class="match-info">
                            <p><i class="far fa-calendar-alt"></i> 15 Juni 2025</p>
                            <p><i class="far fa-clock"></i> 14:30 uur</p>
                            <p><i class="fas fa-map-marker-alt"></i> Sportpark De Burcht</p>
                        </div>
                    </div>
                </div>
                
                <div class="match-card">
                    <div class="match-header">Vriendschappelijke Wedstrijd</div>
                    <div class="match-content">
                        <div class="teams">
                            <div class="team">
                                <img src="https://primary.jwwb.nl/public/w/h/c/temp-qdzjsvkxvxfwoekqwpjg/chatgpt-image-11-apr-2025-22_25_50-high.png" alt="United Boys" class="team-logo">
                                <div>United Boys</div>
                            </div>
                            <div class="vs">VS</div>
                            <div class="team">
                                <img src="https://via.placeholder.com/50x50" alt="Tegenstander" class="team-logo">
                                <div>SV Vriendschap</div>
                            </div>
                        </div>
                        <div class="match-info">
                            <p><i class="far fa-calendar-alt"></i> 22 Juni 2025</p>
                            <p><i class="far fa-clock"></i> 11:00 uur</p>
                            <p><i class="fas fa-map-marker-alt"></i> Sportpark De Meent</p>
                        </div>
                    </div>
                </div>
                
                <div class="match-card">
                    <div class="match-header">Beker Wedstrijd</div>
                    <div class="match-content">
                        <div class="teams">
                            <div class="team">
                                <img src="https://primary.jwwb.nl/public/w/h/c/temp-qdzjsvkxvxfwoekqwpjg/chatgpt-image-11-apr-2025-22_25_50-high.png" alt="United Boys" class="team-logo">
                                <div>United Boys</div>
                            </div>
                            <div class="vs">VS</div>
                            <div class="team">
                                <img src="https://via.placeholder.com/50x50" alt="Tegenstander" class="team-logo">
                                <div>Beker FC</div>
                            </div>
                        </div>
                        <div class="match-info">
                            <p><i class="far fa-calendar-alt"></i> 29 Juni 2025</p>
                            <p><i class="far fa-clock"></i> 13:00 uur</p>
                            <p><i class="fas fa-map-marker-alt"></i> Sportpark De Burcht</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="container" id="admin">
        <h2 class="section-title">Wedstrijd Beheer</h2>
        <div class="admin-panel">
            <h3 class="admin-title">Voeg nieuwe wedstrijd toe</h3>
            <form id="match-form">
                <div class="form-group">
                    <label for="match-type">Wedstrijd Type</label>
                    <select id="match-type" required>
                        <option value="">Selecteer type</option>
                        <option value="competitie">Competitie</option>
                        <option value="beker">Beker</option>
                        <option value="vriendschappelijk">Vriendschappelijk</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="opponent">Tegenstander</label>
                    <input type="text" id="opponent" required>
                </div>
                
                <div class="form-group">
                    <label for="date">Datum</label>
                    <input type="date" id="date" required>
                </div>
                
                <div class="form-group">
                    <label for="time">Tijd</label>
                    <input type="time" id="time" required>
                </div>
                
                <div class="form-group">
                    <label for="location">Locatie</label>
                    <input type="text" id="location" required>
                </div>
                
                <div class="form-actions">
                    <button type="submit" class="btn-admin">Wedstrijd Toevoegen</button>
                </div>
            </form>
        </div>
    </section>
    
    <footer id="contact">
        <div class="footer-content">
            <div class="footer-column">
                <h3>United Boys F.C.</h3>
                <p>Jeugdvoetbal met passie en plezier. Wij bieden jongeren een positieve omgeving om hun talenten te ontwikkelen.</p>
            </div>
            
            <div class="footer-column">
                <h3>Snelle Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">Over Ons</a></li>
                    <li><a href="#team">Team</a></li>
                    <li><a href="#matches">Wedstrijden</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Contact</h3>
                <ul>
                    <li><i class="fas fa-map-marker-alt"></i> Sportpark De Burcht, Amsterdam</li>
                    <li><i class="fas fa-phone"></i> 020-1234567</li>
                    <li><i class="fas fa-envelope"></i> info@unitedboysfc.nl</li>
                </ul>
            </div>
        </div>
        
        <div class="social-links">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
        
        <div class="copyright">
            <p>&copy; 2025 United Boys F.C. Alle rechten voorbehouden.</p>
        </div>
    </footer>
    
    <script>
        // Mobile menu toggle
        document.querySelector('.menu-toggle').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('active');
        });
        
        // Simple form handling for demo purposes
        document.getElementById('match-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Wedstrijd succesvol toegevoegd! (Dit is een demo)');
            this.reset();
        });
    </script>
</body>
</html>
