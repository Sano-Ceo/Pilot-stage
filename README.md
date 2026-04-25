# Pilot-stage
<br>
Development team
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lunar Scents - Celestial Fragrances from the Moon</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a3a 50%, #2d1b69 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: rgba(0, 0, 0, 0.8);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }
        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #e0e0ff;
            text-shadow: 0 0 10px #4a90e2;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        .nav-links a {
            color: #e0e0ff;
            text-decoration: none;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #4a90e2;
            text-shadow: 0 0 5px #4a90e2;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="g" cx="50%" cy="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="50%" stop-color="%23ffffff" stop-opacity="0.05"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="200" cy="200" r="50" fill="url(%23g)"><animate attributeName="cy" values="200;150;200" dur="3s" repeatCount="indefinite"/></circle><circle cx="800" cy="300" r="30" fill="url(%23g)"><animate attributeName="cy" values="300;250;300" dur="4s" repeatCount="indefinite"/></circle><circle cx="500" cy="800" r="40" fill="url(%23g)"><animate attributeName="cy" values="800;750;800" dur="5s" repeatCount="indefinite"/></circle></svg>') center/cover;
            position: relative;
        }
        .hero-content h1 {
            font-size: 4rem;
            color: #e0e0ff;
            text-shadow: 0 0 20px #4a90e2;
            margin-bottom: 1rem;
            animation: glow 2s ease-in-out infinite alternate;
        }
        @keyframes glow {
            from { text-shadow: 0 0 20px #4a90e2; }
            to { text-shadow: 0 0 30px #4a90e2, 0 0 40px #4a90e2; }
        }
        .hero-content p {
            font-size: 1.5rem;
            color: #ccc;
            margin-bottom: 2rem;
        }
        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #4a90e2, #357abd);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.2rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(74, 144, 226, 0.4);
        }

        /* Products Section */
        .products {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        .section-title {
            text-align: center;
            font-size: 3rem;
            color: #e0e0ff;
            margin-bottom: 3rem;
            text-shadow: 0 0 10px #4a90e2;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        .product-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }
        .product-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 15px;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #4a90e2, #357abd);
        }
        .product-card h3 {
            color: #e0e0ff;
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        .product-card p {
            color: #ccc;
            margin-bottom: 1.5rem;
        }
        .price {
            font-size: 1.8rem;
            color: #4a90e2;
            font-weight: bold;
        }

        /* About Section */
        .about {
            padding: 5rem 2rem;
            background: rgba(0, 0, 0, 0.4);
            text-align: center;
        }
        .about-content {
            max-width: 800px;
            margin: 0 auto;
        }
        .about-content h2 {
            font-size: 2.5rem;
            color: #e0e0ff;
            margin-bottom: 2rem;
        }
        .about-content p {
            font-size: 1.2rem;
            color: #ccc;
            margin-bottom: 1.5rem;
        }

        /* Footer */
        footer {
            background: rgba(0, 0, 0, 0.9);
            color: #ccc;
            text-align: center;
            padding: 2rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .section-title {
                font-size: 2rem;
            }
        }

        /* Floating Particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        .particle {
            position: absolute;
            background: rgba(74, 144, 226, 0.5);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.5; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 1; }
        }
    </style>
</head>
<body>
    <!-- Floating Particles -->
    <div class="particles" id="particles"></div>

    <!-- Header -->
    <header>
        <nav>
            <div class="logo">🌙 Lunar Scents</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Lunar Scents</h1>
            <p>Experience the ethereal aromas captured from the moon's surface. Fragrances that transport you to cosmic tranquility.</p>
            <a href="#products" class="cta-button">Discover Our Collection</a>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <h2 class="section-title">Our Celestial Collection</h2>
        <div class="product-grid">
            <div class="product-card">
                <div style="background: linear-gradient(45deg, #ff6b6b, #ee5a24); height: 200px; display: flex; align-items: center; justify-content: center; color: white; font-size: 3rem; border-radius: 15px; margin-bottom: 1rem;">🌑</div>
                <h3>Moon Dust Elixir</h3>
                <p>A mystical blend of lunar regolith and stardust notes, evoking the silence of the Sea of Tranquility.</p>
                <div class="price">$49.99</div>
            </div>
            <div class="product-card">
                <div style="background: linear-gradient(45deg, #4ecdc4, #44a08d); height: 200px; display: flex; align-items: center; justify-content: center; color: white; font-size: 3rem; border-radius: 15px; margin-bottom: 1rem;">🌒</div>
                <h3>Crescent Whisper</h3>
                <p>Soft vanilla and cosmic lavender, inspired by the gentle curve of the waxing moon.</p>
                <div class="price">$59.99</div>
            </div>
            <div class="product-card">
                <div style="background: linear-gradient(45deg, #feca57, #ff9ff3); height: 200px; display: flex; align-items: center; justify-content: center; color: white; font-size: 3rem; border-radius: 15px; margin-bottom: 1rem;">🌓</div>
                <h3>Full Moon Radiance</h3>
                <p>Bright citrus and silver orchid, capturing the luminous glow of a full lunar night.</p>
                <div class="price">$69.99</div>
            </div>
            <div class="product-card">
                <div style="background: linear-gradient(45deg, #a8edea, #fed6e3); height: 200px; display: flex; align-items: center; justify-content: center; color: white; font-size: 3rem; border-radius: 15px; margin-bottom: 1rem;">🌔</div>
                <h3>Waning Nebula</h3>
                <p>Deep sandalwood and nebula mist, fading into the infinite cosmos.</p>
                <div class="price">$54.99</div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="about-content">
            <h2>About Lunar Scents</h2>
            <p>Founded by lunar enthusiasts and master perfumers, Lunar Scents brings the otherworldly aromas of the moon to your everyday life. Using advanced olfactory synthesis, we've recreated the scents of moon rocks, solar winds, and cosmic voids.</p>
            <p>Each fragrance is crafted with rare earth elements and celestial-inspired notes, bottled under the full moon for maximum potency.</p>
            <p>Join thousands of stargazers who have elevated their senses with Lunar Scents.</p>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <p>&copy; 2024 Lunar Scents. All rights reserved. | <a href="#" style="color: #4a90e2;">contact@lunarscents.com</a></p>
    </footer>

    <script>
        // Generate floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.width = particle.style.height = (Math.random() * 4 + 2) + 'px';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 4) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        createParticles();

        // Smooth scrolling for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(0, 0, 0, 0.95)';
            } else {
                header.style.background = 'rgba(0, 0, 0, 0.8)';
            }
        });
    </script>
</body>
</html>
