<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bosa Digital | Home</title>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }

        body {
            color: #1e293b;
            background: #ffffff;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Top Header */
        .top-bar {
            background: #105bbf;
            color: white;
            padding: 10px 0;
            font-size: 0.9rem;
        }
        .top-bar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }
        .top-contact {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }
        .top-contact a, .top-contact span {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .top-contact i {
            font-size: 0.9rem;
        }
        .top-social {
            display: flex;
            gap: 15px;
        }
        .top-social a {
            color: white;
            text-decoration: none;
        }

        /* Navbar */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            flex-wrap: wrap;
            gap: 20px;
        }
        .logo {
            font-size: 2rem;
            font-weight: 700;
            color: #0b1e33;
        }
        .logo span {
            color: #105bbf;
        }
        .nav-links {
            display: flex;
            gap: 35px;
            font-weight: 500;
        }
        .nav-links a {
            text-decoration: none;
            color: #334155;
            transition: color 0.2s;
        }
        .nav-links a:hover, .nav-links a.active {
            color: #105bbf;
        }
        .btn-outline {
            border: 2px solid #105bbf;
            color: #105bbf;
            padding: 10px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.2s;
            background: transparent;
        }
        .btn-outline:hover {
            background: #105bbf;
            color: white;
        }
        .btn-primary {
            background: #105bbf;
            color: white;
            padding: 14px 38px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            display: inline-block;
            border: none;
            font-size: 1rem;
            transition: 0.2s;
            cursor: pointer;
        }
        .btn-primary:hover {
            background: #0d4a9e;
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(16,91,191,0.2);
        }

        /* ===== FLOATING BUTTONS ===== */
        /* Left Side - Chat Box */
        .chat-button {
            position: fixed;
            bottom: 30px;
            left: 30px;
            z-index: 1000;
        }
        .chat-toggle {
            width: 60px;
            height: 60px;
            background: #105bbf;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(16,91,191,0.3);
            transition: 0.3s;
            border: 2px solid white;
        }
        .chat-toggle i {
            color: white;
            font-size: 1.8rem;
        }
        .chat-toggle:hover {
            transform: scale(1.1);
            background: #0d4a9e;
        }
        .chat-box {
            position: absolute;
            bottom: 80px;
            left: 0;
            width: 300px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            display: none;
            overflow: hidden;
            border: 1px solid #e2e8f0;
        }
        .chat-box.active {
            display: block;
        }
        .chat-header {
            background: #105bbf;
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .chat-header i {
            font-size: 1.5rem;
        }
        .chat-header h4 {
            font-size: 1.1rem;
        }
        .chat-body {
            padding: 20px;
        }
        .chat-message {
            background: #f8fafc;
            padding: 12px;
            border-radius: 12px;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        .chat-input {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }
        .chat-input input {
            flex: 1;
            padding: 10px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            outline: none;
        }
        .chat-input input:focus {
            border-color: #105bbf;
        }
        .chat-input button {
            background: #105bbf;
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.2s;
        }
        .chat-input button:hover {
            background: #0d4a9e;
        }

        /* Right Side - WhatsApp Button */
        .whatsapp-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
        }
        .whatsapp-link {
            width: 60px;
            height: 60px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 20px rgba(37,211,102,0.3);
            transition: 0.3s;
            border: 2px solid white;
            text-decoration: none;
        }
        .whatsapp-link i {
            color: white;
            font-size: 2.2rem;
        }
        .whatsapp-link:hover {
            transform: scale(1.1);
            background: #20b859;
        }
        .whatsapp-tooltip {
            position: absolute;
            bottom: 70px;
            right: 0;
            background: white;
            padding: 8px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
            white-space: nowrap;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border: 1px solid #e2e8f0;
            display: none;
        }
        .whatsapp-link:hover + .whatsapp-tooltip {
            display: block;
        }

        /* Hero Section */
        .hero {
            padding: 60px 0;
            background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
        }
        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        .hero h1 {
            font-size: 3.5rem;
            color: #0b1e33;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        .hero h1 span {
            color: #105bbf;
        }
        .hero p {
            color: #475569;
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        /* Contact Form */
        .form-card {
            background: white;
            border-radius: 30px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
        }
        .form-card h3 {
            font-size: 1.8rem;
            margin-bottom: 10px;
        }
        .form-card p {
            color: #64748b;
            margin-bottom: 25px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            font-size: 1rem;
            background: #f8fafc;
        }
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #105bbf;
            background: white;
        }

        /* Services Section */
        .services-section {
            padding: 80px 0;
        }
        .section-header {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 50px;
        }
        .section-header h2 {
            font-size: 2.8rem;
            margin-bottom: 15px;
        }
        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        .service-card {
            background: #f8fafc;
            padding: 35px;
            border-radius: 20px;
            transition: 0.3s;
            border: 1px solid #e2e8f0;
        }
        .service-card:hover {
            transform: translateY(-5px);
            border-color: #105bbf;
            box-shadow: 0 15px 30px rgba(16,91,191,0.08);
        }
        .service-icon {
            width: 60px;
            height: 60px;
            background: white;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }
        .service-icon i {
            font-size: 2rem;
            color: #105bbf;
        }
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 12px;
        }

        /* Stats Section */
        .stats-section {
            background: #105bbf;
            color: white;
            padding: 60px 0;
        }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            text-align: center;
        }
        .stat-number {
            font-size: 3rem;
            font-weight: 700;
        }
        .stat-label {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        /* Process Section */
        .process-section {
            padding: 80px 0;
        }
        .process-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
            margin-top: 50px;
        }
        .process-step {
            text-align: center;
            padding: 30px;
            background: #f8fafc;
            border-radius: 20px;
        }
        .step-number {
            width: 50px;
            height: 50px;
            background: #105bbf;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 auto 20px;
        }

        /* Pricing Section */
        .pricing-section {
            background: #f8fafc;
            padding: 80px 0;
        }
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        .pricing-card {
            background: white;
            padding: 40px 30px;
            border-radius: 24px;
            border: 1px solid #e2e8f0;
            transition: 0.3s;
        }
        .pricing-card:hover {
            transform: translateY(-5px);
            border-color: #105bbf;
        }
        .pricing-card.featured {
            border: 2px solid #105bbf;
            transform: scale(1.05);
        }
        .price {
            font-size: 2.8rem;
            font-weight: 700;
            color: #105bbf;
            margin: 20px 0;
        }

        /* Footer */
        .footer {
            background: #0b1e33;
            color: white;
            padding: 60px 0 30px;
        }
        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
        }
        .footer a {
            color: #cbd5e1;
            text-decoration: none;
        }

        /* Responsive */
        @media (max-width: 900px) {
            .hero-grid,
            .services-grid,
            .stats-grid,
            .process-grid,
            .pricing-grid,
            .footer-grid {
                grid-template-columns: 1fr;
            }
            .pricing-card.featured {
                transform: scale(1);
            }
        }
    </style>
</head>
<body>

<!-- ===== FLOATING CHAT BOX (LEFT SIDE) ===== -->
<div class="chat-button">
    <div class="chat-toggle" onclick="toggleChat()">
        <i class="fas fa-comment-dots"></i>
    </div>
    <div class="chat-box" id="chatBox">
        <div class="chat-header">
            <i class="fas fa-robot"></i>
            <div>
                <h4>Bosa Assistant</h4>
                <p style="font-size: 0.8rem; opacity: 0.9;">Online • Reply in 5 min</p>
            </div>
        </div>
        <div class="chat-body">
            <div class="chat-message">
                👋 Hi! Welcome to Bosa Digital. How can we help you today?
            </div>
            <div class="chat-input">
                <input type="text" placeholder="Type your message..." id="chatInput">
                <button onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
    </div>
</div>

<!-- ===== FLOATING WHATSAPP BUTTON (RIGHT SIDE) ===== -->
<div class="whatsapp-button">
    <a href="https://wa.me/1936527856?text=Hi%20Bosa%20Digital%2C%20I%20need%20help%20with%20your%20services" class="whatsapp-link" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>
    <div class="whatsapp-tooltip">Chat on WhatsApp</div>
</div>

<!-- Top Bar -->
<div class="top-bar">
    <div class="container">
        <div class="top-contact">
            <a href="tel:+1936527856"><i class="fas fa-phone-alt"></i> +193-652-7856</a>
            <a href="mailto:info@bosa.com"><i class="fas fa-envelope"></i> info@bosa.com</a>
            <span><i class="fas fa-map-marker-alt"></i> New York, USA</span>
        </div>
        <div class="top-social">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-linkedin-in"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
        </div>
    </div>
</div>

<!-- Navbar -->
<div class="container">
    <div class="navbar">
        <a href="index.html" class="logo">Bosa<span>.</span></a>
        <div class="nav-links">
            <a href="index.html" class="active">Home</a>
            <a href="services.html">Services</a>
            <a href="seo.html">SEO</a>
            <a href="#">Blog</a>
            <a href="#">FAQ</a>
        </div>
        <a href="#" class="btn-outline">Get started</a>
    </div>
</div>

<!-- Hero Section with Form -->
<section class="hero">
    <div class="container hero-grid">
        <div>
            <h1>Have Any Projects? <span>Let's Get Started.</span></h1>
            <p>Professional digital marketing solutions tailored to grow your business. Join 600+ satisfied clients.</p>
            <a href="#" class="btn-primary">Our services <i class="fas fa-arrow-right"></i></a>
        </div>
        <div class="form-card">
            <h3>Get In Touch</h3>
            <p>We'll respond within 24 hours</p>
            <form>
                <div class="form-group">
                    <input type="text" placeholder="Your name" required>
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Email address" required>
                </div>
                <div class="form-group">
                    <input type="tel" placeholder="Phone number">
                </div>
                <div class="form-group">
                    <textarea placeholder="Your message" rows="3"></textarea>
                </div>
                <button class="btn-primary" style="width: 100%;">Send Message</button>
            </form>
        </div>
    </div>
</section>

<!-- Services Section -->
<section class="services-section">
    <div class="container">
        <div class="section-header">
            <h2>Our Services</h2>
            <p>Comprehensive digital marketing solutions for your business</p>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-search"></i></div>
                <h3>SEO Optimization</h3>
                <p>Boost your rankings and drive organic traffic with our SEO strategies.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-bullhorn"></i></div>
                <h3>PPC Advertising</h3>
                <p>Targeted campaigns that deliver immediate results and ROI.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-chart-line"></i></div>
                <h3>Market Analysis</h3>
                <p>Data-driven insights to understand your market and competitors.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-envelope"></i></div>
                <h3>Email Marketing</h3>
                <p>Nurture leads and build customer loyalty with email campaigns.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-hashtag"></i></div>
                <h3>Social Media</h3>
                <p>Engage your audience across all major social platforms.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fas fa-pen-fancy"></i></div>
                <h3>Content Marketing</h3>
                <p>Create valuable content that attracts and converts.</p>
            </div>
        </div>
    </div>
</section>

<!-- Stats Section -->
<section class="stats-section">
    <div class="container">
        <div class="stats-grid">
            <div class="stat-item">
                <div class="stat-number">250+</div>
                <div class="stat-label">Projects Completed</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">95%</div>
                <div class="stat-label">Client Satisfaction</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">3x</div>
                <div class="stat-label">Average ROI</div>
            </div>
        </div>
    </div>
</section>

<!-- Process Section -->
<section class="process-section">
    <div class="container">
        <div class="section-header">
            <h2>Our Working Process</h2>
            <p>A systematic approach to delivering results</p>
        </div>
        <div class="process-grid">
            <div class="process-step">
                <div class="step-number">1</div>
                <h3>Discovery</h3>
                <p>We analyze your business goals and current performance</p>
            </div>
            <div class="process-step">
                <div class="step-number">2</div>
                <h3>Strategy</h3>
                <p>Custom plan created with clear KPIs</p>
            </div>
            <div class="process-step">
                <div class="step-number">3</div>
                <h3>Implementation</h3>
                <p>Our experts execute the strategy</p>
            </div>
            <div class="process-step">
                <div class="step-number">4</div>
                <h3>Optimization</h3>
                <p>Continuous testing and improvement</p>
            </div>
        </div>
    </div>
</section>

<!-- Pricing Section -->
<section class="pricing-section">
    <div class="container">
        <div class="section-header">
            <h2>Our Pricing Plans</h2>
            <p>Choose the perfect plan for your business</p>
        </div>
        <div class="pricing-grid">
            <div class="pricing-card">
                <h3>Starter</h3>
                <div class="price">$499</div>
                <p>Perfect for small businesses</p>
                <ul style="list-style: none; margin: 20px 0;">
                    <li style="padding: 8px 0;">✓ 15 Keywords</li>
                    <li style="padding: 8px 0;">✓ Monthly Audit</li>
                    <li style="padding: 8px 0;">✓ Basic Reports</li>
                </ul>
                <a href="#" class="btn-outline">Get Started</a>
            </div>
            <div class="pricing-card featured">
                <h3>Professional</h3>
                <div class="price">$999</div>
                <p>Most popular choice</p>
                <ul style="list-style: none; margin: 20px 0;">
                    <li style="padding: 8px 0;">✓ 30 Keywords</li>
                    <li style="padding: 8px 0;">✓ Weekly Audit</li>
                    <li style="padding: 8px 0;">✓ Advanced Reports</li>
                </ul>
                <a href="#" class="btn-primary">Get Started</a>
            </div>
            <div class="pricing-card">
                <h3>Enterprise</h3>
                <div class="price">$1,999</div>
                <p>For large businesses</p>
                <ul style="list-style: none; margin: 20px 0;">
                    <li style="padding: 8px 0;">✓ 50+ Keywords</li>
                    <li style="padding: 8px 0;">✓ Daily Tracking</li>
                    <li style="padding: 8px 0;">✓ Custom Reports</li>
                </ul>
                <a href="#" class="btn-outline">Get Started</a>
            </div>
        </div>
    </div>
</section>

<!-- CTA Banner -->
<section class="container" style="margin: 60px auto;">
    <div style="background: linear-gradient(135deg, #105bbf 0%, #0d4a9e 100%); color: white; padding: 60px; border-radius: 40px; text-align: center;">
        <h2 style="color: white; font-size: 2.8rem; margin-bottom: 20px;">Ready to Grow Your Business?</h2>
        <p style="font-size: 1.3rem; margin-bottom: 30px;">Get a free consultation today</p>
        <a href="#" class="btn-outline" style="background: white; border-color: white; color: #105bbf;">Contact Us Now</a>
    </div>
</section>

<!-- Footer -->
<footer class="footer">
    <div class="container footer-grid">
        <div>
            <h3 style="font-size:2rem;">Bosa<span style="color:#105bbf;">.</span></h3>
            <p style="color:#94a3b8;">Professional digital marketing services for modern businesses.</p>
        </div>
        <div>
            <h4>Company</h4>
            <p><a href="index.html">Home</a></p>
            <p><a href="services.html">Services</a></p>
            <p><a href="#">About</a></p>
        </div>
        <div>
            <h4>Services</h4>
            <p><a href="#">SEO</a></p>
            <p><a href="#">PPC</a></p>
            <p><a href="#">Marketing</a></p>
        </div>
        <div>
            <h4>Contact</h4>
            <p><i class="fas fa-phone"></i> +193-652-7856</p>
            <p><i class="fas fa-envelope"></i> info@bosa.com</p>
        </div>
    </div>
</footer>

<script>
    // Chat Box Toggle Function
    function toggleChat() {
        const chatBox = document.getElementById('chatBox');
        chatBox.classList.toggle('active');
    }

    // Send Message Function
    function sendMessage() {
        const input = document.getElementById('chatInput');
        const message = input.value.trim();
        if (message) {
            alert('Message sent: ' + message + '\n(This is a demo - integrate with your backend)');
            input.value = '';
        }
    }
</script>

</body>
</html>
