I'll create a beautiful website for "Glow Gems" - a jelly and gemstone seller. Here's a complete, responsive website:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glow Gems - Premium Jelly & Gemstones</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            text-decoration: none;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255,215,0,0.5);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ffd700;
        }

        .cart-icon {
            position: relative;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%231e3c72" width="1200" height="600"/><circle fill="%23ffd700" opacity="0.3" cx="200" cy="150" r="80"/><circle fill="%23ff6b6b" opacity="0.3" cx="800" cy="200" r="60"/><circle fill="%234ecdc4" opacity="0.3" cx="1000" cy="400" r="70"/><circle fill="%23ffe66d" opacity="0.4" cx="400" cy="450" r="90"/></svg>');
            background-size: cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 80px;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #ffd700, #ffed4a);
            color: #1e3c72;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 5px 15px rgba(255,215,0,0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255,215,0,0.6);
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
            margin-bottom: 3rem;
            color: #1e3c72;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .product-image {
            height: 250px;
            background: linear-gradient(45deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: white;
            position: relative;
        }

        .product-image i {
            text-shadow: 0 0 20px rgba(255,255,255,0.8);
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-title {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #1e3c72;
        }

        .product-price {
            font-size: 2rem;
            font-weight: bold;
            color: #ffd700;
            margin-bottom: 1rem;
        }

        .product-description {
            color: #666;
            margin-bottom: 1.5rem;
        }

        .add-to-cart {
            width: 100%;
            background: linear-gradient(45deg, #1e3c72, #2a5298);
            color: white;
            border: none;
            padding: 1rem;
            border-radius: 10px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background 0.3s;
        }

        .add-to-cart:hover {
            background: linear-gradient(45deg, #2a5298, #1e3c72);
        }

        /* Features Section */
        .features {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 5rem 2rem;
        }

        .features-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature-item {
            padding: 2rem;
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-info h3 {
            color: #1e3c72;
            margin-bottom: 1rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }

        .contact-item i {
            color: #ffd700;
            margin-right: 1rem;
            font-size: 1.2rem;
        }

        .contact-form {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #1e3c72;
        }

        /* Footer */
        footer {
            background: #1e3c72;
            color: white;
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

            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Animations */
        @keyframes glow {
            0%, 100% { text-shadow: 0 0 5px #ffd700; }
            50% { text-shadow: 0 0 20px #ffd700, 0 0 30px #ffd700; }
        }

        .logo {
            animation: glow 2s infinite;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <a href="#" class="logo">✨ Glow Gems ✨</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#features">Why Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="cart-icon">
                <i class="fas fa-shopping-cart"></i>
                <span style="position: absolute; top: -8px; right: -8px; background: #ff6b6b; color: white; border-radius: 50%; width: 20px; height: 20px; font-size: 0.8rem; display: flex; align-items: center; justify-content: center;">0</span>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Glow Gems</h1>
            <p>Premium Jelly & Authentic Gemstones<br>Shining Quality, Sparkling Prices</p>
            <a href="#products" class="cta-button">Shop Now</a>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <h2 class="section-title">Our Sparkling Collection</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-gem"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Amethyst Jelly</h3>
                    <div class="product-price">$29.99</div>
                    <p class="product-description">Purple perfection in every bite. Natural amethyst-infused jelly with crystal-like texture.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-diamond"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Rose Quartz Gems</h3>
                    <div class="product-price">$49.99</div>
                    <p class="product-description">Authentic rose quartz gemstones. Perfect for jewelry making or crystal healing.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-candy-cane"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Emerald Jelly Pack</h3>
                    <div class="product-price">$24.99</div>
                    <p class="product-description">6-pack of emerald green jelly. Rich flavor with stunning crystal clear appearance.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-gem"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Citrine Crystal</h3>
                    <div class="product-price">$89.99</div>
                    <p class="product-description">Premium citrine gemstone. Golden energy stone for abundance and prosperity.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-star"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Sapphire Jelly</h3>
                    <div class="product-price">$34.99</div>
                    <p class="product-description">Royal blue sapphire jelly. Luxury treat with deep, rich flavor profile.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <i class="fas fa-crown"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Diamond Dust Gems</h3>
                    <div class="product-price">$199.99</div>
                    <p class="product-description">Premium assortment of faceted gemstones. Collector quality assortment.</p>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="features-content">
            <h2 class="section-title" style="color: white;">Why Choose Glow Gems?</h2>
            <div class="features-grid">
                <div class="feature-item">
                    <i class="fas fa-shipping-fast feature-icon"></i>
                    <h3>Fast Shipping</h3>
                    <p>Delivered within 2-3 business days worldwide</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-shield-alt feature-icon"></i>
                    <h3>Quality Guaranteed</h3>
                    <p>100% authentic gemstones & premium ingredients</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-undo feature-icon"></i>
                    <h3>Easy Returns</h3>
                    <p>30-day money back guarantee</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-lock feature-icon"></i>
                    <h3>Secure Checkout</h3>
                    <p>SSL encrypted & trusted payment methods</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <h3>Visit Glow Gems</h3>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>123 Crystal Street, Gem City, GC 12345</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+1 (555) 123-GEMS</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>hello@glowgems.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-clock"></i>
                    <span>Mon-Fri: 9AM-6PM | Sat-Sun: 10AM-4PM</span>
                </div>
            </div>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <input type="text" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <input type="text" placeholder="Subject" required>
                    </div>
                    <div class="form-group">
                        <textarea rows="5" placeholder="Your Message..." required></textarea>
                    </div>
                    <button type="submit" class="cta-button" style="width: 100%; margin-top: 1rem;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Glow Gems. All rights reserved. | <a href="#" style="color: #ffd700;">Privacy Policy</a> | <a href="#" style="color: #ffd700;">Terms of Service</a></p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add to cart functionality
        let cartCount = 0;
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', function() {
                cartCount++;
                document.querySelector('.aq
