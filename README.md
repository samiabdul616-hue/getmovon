
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movon Express - Logistics Management Solutions</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Work+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FF6B35;
            --secondary: #004E89;
            --accent: #F7B801;
            --dark: #1A1A2E;
            --light: #F8F9FA;
            --gradient: linear-gradient(135deg, #004E89 0%, #00A8CC 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Work Sans', sans-serif;
            color: var(--dark);
            overflow-x: hidden;
            background: var(--light);
        }
        
        /* Header */
        header {
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            animation: slideDown 0.6s ease;
        }
        
        @keyframes slideDown {
            from { transform: translateY(-100%); }
            to { transform: translateY(0); }
        }
        
        nav {
            max-width: 1400px;
            margin: 0 auto;
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 2rem;
            letter-spacing: 2px;
            color: var(--secondary);
            position: relative;
        }
        
        .logo span {
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            position: relative;
            transition: color 0.3s;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            margin-top: 80px;
            min-height: 90vh;
            background: var(--gradient);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><rect width="1" height="1" x="50" y="50" fill="white" opacity="0.1"/></svg>');
            background-size: 50px 50px;
            animation: moveGrid 20s linear infinite;
        }
        
        @keyframes moveGrid {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }
        
        .hero-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 4rem 2rem;
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 5rem;
            color: white;
            letter-spacing: 3px;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            animation: fadeInUp 0.8s ease 0.2s backwards;
        }
        
        .hero p {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.95);
            max-width: 600px;
            margin-bottom: 2.5rem;
            animation: fadeInUp 0.8s ease 0.4s backwards;
        }
        
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
        
        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: var(--primary);
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            border-radius: 50px;
            transition: all 0.3s;
            animation: fadeInUp 0.8s ease 0.6s backwards;
            box-shadow: 0 10px 30px rgba(255, 107, 53, 0.3);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(255, 107, 53, 0.4);
        }
        
        /* Services Section */
        .services {
            padding: 6rem 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .section-title {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 3.5rem;
            text-align: center;
            margin-bottom: 3rem;
            letter-spacing: 2px;
            color: var(--secondary);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        
        .service-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
            transform: scaleX(0);
            transition: transform 0.4s;
        }
        
        .service-card:hover::before {
            transform: scaleX(1);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.12);
        }
        
        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }
        
        .service-card h3 {
            font-family: 'Bebas Neue', sans-serif;
            font-size: 1.8rem;
            margin-bottom: 1rem;
            letter-spacing: 1px;
            color: var(--secondary);
        }
        
        .service-card p {
            color: #666;
            line-height: 1.7;
        }
        
        /* Contact Section */
        .contact {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .contact-container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 2rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--secondary);
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-family: 'Work Sans', sans-serif;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }
        
        .form-group textarea {
            resize: vertical;
            min-height: 150px;
        }
        
        .submit-btn {
            width: 100%;
            padding: 1.2rem;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            font-family: 'Work Sans', sans-serif;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 78, 137, 0.3);
        }
        
        .success-message {
            display: none;
            padding: 1rem;
            background: #4CAF50;
            color: white;
            border-radius: 10px;
            margin-top: 1rem;
            text-align: center;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }
        
        footer p {
            margin-bottom: 1rem;
        }
        
        .footer-email {
            color: var(--accent);
            text-decoration: none;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">MOVON <span>EXPRESS</span></div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>LOGISTICS<br>SIMPLIFIED</h1>
            <p>Expert logistics management solutions that keep your operations moving efficiently. From planning to execution, we handle it all.</p>
            <a href="#contact" class="cta-button">Get Started</a>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <h2 class="section-title">Our Services</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">📦</div>
                <h3>Supply Chain Management</h3>
                <p>End-to-end supply chain optimization ensuring seamless flow from suppliers to customers.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🚚</div>
                <h3>Fleet Management</h3>
                <p>Comprehensive fleet tracking and management systems for maximum efficiency and cost savings.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">📊</div>
                <h3>Operations Planning</h3>
                <p>Strategic planning and execution of logistics operations tailored to your business needs.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🌐</div>
                <h3>Real-Time Tracking</h3>
                <p>Advanced tracking systems providing real-time visibility of your shipments and operations.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">📈</div>
                <h3>Analytics & Reporting</h3>
                <p>Detailed analytics and insights to optimize your logistics performance and reduce costs.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🤝</div>
                <h3>Consulting Services</h3>
                <p>Expert consultation to transform and streamline your logistics operations.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="contact-container">
            <h2 class="section-title">Get In Touch</h2>
            <form id="contactForm">
                <div class="form-group">
                    <label for="name">Name *</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Phone</label>
                    <input type="tel" id="phone" name="phone">
                </div>
                <div class="form-group">
                    <label for="message">Message *</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit" class="submit-btn">Send Message</button>
                <div class="success-message" id="successMessage">
                    Thank you! Your message has been sent successfully.
                </div>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p><strong>MOVON EXPRESS</strong></p>
        <p>Email: <a href="mailto:samiabdul616@gmail.com" class="footer-email">samiabdul616@gmail.com</a></p>
        <p>Phone: <a href="tel:+919518291392" class="footer-email">+91 9518291392</a></p>
        <p>&copy; 2024 Movon Express. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                message: document.getElementById('message').value
            };
            
            // Create mailto link
            const subject = encodeURIComponent('New Contact Form Submission - Movon Express');
            const body = encodeURIComponent(
                `Name: ${formData.name}\n` +
                `Email: ${formData.email}\n` +
                `Phone: ${formData.phone}\n\n` +
                `Message:\n${formData.message}`
            );
            
            // Open email client
            window.location.href = `mailto:samiabdul616@gmail.com?subject=${subject}&body=${body}`;
            
            // Show success message
            document.getElementById('successMessage').style.display = 'block';
            
            // Reset form
            this.reset();
            
            // Hide success message after 5 seconds
            setTimeout(() => {
                document.getElementById('successMessage').style.display = 'none';
            }, 5000);
        });
    </script>
</body>
</html>
