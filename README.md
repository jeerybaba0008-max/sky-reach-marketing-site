<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>SKY REACH MARKETING</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Font Family Updated to Poppins */
        body { margin: 0; font-family: 'Poppins', sans-serif; background: #f5f5f5; }
        
        header { background: #003366; color: white; padding: 20px; text-align: center; font-size: 28px; font-weight: 700; }
        nav { background: white; padding: 10px 20px; box-shadow: 0 2px 6px rgba(0,0,0,0.1); display: flex; justify-content: center; gap: 25px; }
        nav a { text-decoration: none; color: #003366; font-size: 18px; transition: color 0.3s; }
        nav a:hover { color: #ff6600; /* Hover Effect Added */ }

        /* Hero Image Updated */
        .hero { 
            background: url('https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1400&q=80') center/cover no-repeat; 
            height: 350px; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            color: white; 
            font-size: 36px; /* Slightly larger text */
            font-weight: 700; 
            text-shadow: 1px 1px 6px black; 
            padding: 0 20px;
            text-align: center;
        }

        .section { padding: 50px 20px; text-align: center; }
        .services { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); /* Card size increased */ gap: 20px; margin-top: 30px; }
        
        .card { 
            background: white; 
            padding: 25px; /* Padding increased */
            border-radius: 12px; 
            box-shadow: 0 4px 12px rgba(0,0,0,0.1); /* Shadow improved */
            transition: transform 0.3s; /* Hover Effect Added */
        }
        .card:hover { transform: translateY(-5px); }
        
        /* Service Card Images Updated */
        .card img { width: 100%; height: 150px; object-fit: cover; border-radius: 8px; margin-bottom: 15px; }
        
        .about, .pricing, .testimonials, .portfolio, .contact-form { background: white; margin: 40px auto; max-width: 900px; padding: 40px; border-radius: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.15); }

        .pricing-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .price-card { background: #eef2ff; padding: 25px; border-radius: 12px; border: 2px solid #003366; }

        .testimonial-card { background: #fff3cd; padding: 25px; border-radius: 12px; margin-bottom: 15px; text-align: left; border-left: 5px solid #ffc107; }

        form input, form textarea { width: 100%; padding: 12px; margin-top: 10px; border: 1px solid #ccc; border-radius: 8px; box-sizing: border-box; }
        form button { background: #003366; color: white; padding: 14px 25px; border: none; margin-top: 20px; border-radius: 8px; font-size: 18px; cursor: pointer; transition: background 0.3s; }
        form button:hover { background: #0056b3; }

        footer { margin-top: 60px; background: #003366; color: white; padding: 30px; text-align: center; }

        .whatsapp-floating { 
            position: fixed; 
            bottom: 25px; 
            right: 25px; 
            background: #25d366; 
            color: white; 
            padding: 15px 20px; 
            border-radius: 50%; 
            text-decoration: none; 
            font-size: 24px; 
            box-shadow: 0 4px 12px rgba(0,0,0,0.25);
            z-index: 1000;
        }
    </style>
</head>
<body>
    <header>SKY REACH MARKETING</header>

    <nav>
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#about">About Us</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="hero" id="home">Grow Your Business With SKY REACH MARKETING</div>

    <div class="section" id="services">
        <h2>Our Services</h2>
        <div class="services">
            <div class="card"><img src="https://images.unsplash.com/photo-1543286386-713fea52c3c4?fit=crop&w=300&h=200&q=80" alt="Facebook Ads"/><h3>Facebook Ads</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1611944212959-b1d551e1837d?fit=crop&w=300&h=200&q=80" alt="Instagram Ads"/><h3>Instagram Ads</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1580971556396-857c3d1f04fd?fit=crop&w=300&h=200&q=80" alt="TikTok Ads"/><h3>TikTok Ads</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1557827885-e6533036e76d?fit=crop&w=300&h=200&q=80" alt="Gmail Marketing"/><h3>Gmail Marketing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1606132410317-5e921d22228b?fit=crop&w=300&h=200&q=80" alt="Graphic Designing"/><h3>Graphic Designing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1522030612170-466d3326177b?fit=crop&w=300&h=200&q=80" alt="Video Editing"/><h3>Video Editing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1549692520-222a101f3536?fit=crop&w=300&h=200&q=80" alt="Website Designing"/><h3>Website Designing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1551608779-8b83286b62d3?fit=crop&w=300&h=200&q=80" alt="SEO Services"/><h3>SEO Services</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1588661726007-88544c8c7f8a?fit=crop&w=300&h=200&q=80" alt="Facebook Page Management"/><h3>Facebook Page Management</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1627964408930-bc5db0844781?fit=crop&w=300&h=200&q=80" alt="Instagram Account Management"/><h3>Instagram Account Management</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1616782531998-051f67f0412e?fit=crop&w=300&h=200&q=80" alt="TikTok Account Management"/><h3>TikTok Account Management</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?fit=crop&w=300&h=200&q=80" alt="Daily Posting"/><h3>Daily Posting</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1587560418386-8a964a27f677?fit=crop&w=300&h=200&q=80" alt="Comments & Messages Handling"/><h3>Comments & Messages Handling</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1550534246-8178122d6454?fit=crop&w=300&h=200&q=80" alt="Thumbnail Design"/><h3>Thumbnail Design</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1528641977938-e66699d7a224?fit=crop&w=300&h=200&q=80" alt="Short Videos"/><h3>Short Videos</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1609869584485-f551b9e0787d?fit=crop&w=300&h=200&q=80" alt="YouTube Video Editing"/><h3>YouTube Video Editing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1563729781615-562e8310c855?fit=crop&w=300&h=200&q=80" alt="Logo Designing"/><h3>Logo Designing</h3></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1581093581728-6e696f8c772c?fit=crop&w=300&h=200&q=80" alt="Business Card Designing"/><h3>Business Card Designing</h3></div>
        </div>
    </div>

    <div class="section about" id="about">
        <h2>About Us</h2>
        <p>Sky Reach Marketing ek professional digital marketing agency hai jo businesses ko growth, branding aur online presence improve karne mein help karti hai. Hum Facebook Ads, Instagram Ads, TikTok Promotions, YouTube Management, Video Editing aur Graphic Designing jaisi top-tier services provide karte hain. Hamari team aapke business ko next level tak le jane ke liye passionate hai!</p>
    </div>

    <div class="section portfolio" id="portfolio">
        <h2>Portfolio</h2>
        <p>Our recent work and client results. We believe in transparency and measurable results.</p>
        <img src="https://images.unsplash.com/photo-1507207611509-ec012433ff52?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=900&q=80" style="width:100%; border-radius:12px;" alt="Digital Marketing Portfolio Showcase"/>
    </div>

    <div class="section testimonials">
        <h2>Client Reviews</h2>
        <div class="testimonial-card">"Great Facebook Ads results! Highly recommended. My sales increased by 40% after working with Sky Reach Marketing."</div>
        <div class="testimonial-card">"Professional designs and fast delivery. They truly understand modern digital trends."</div>
    </div>

    <div class="section pricing" id="pricing">
        <h2>Pricing Plans</h2>
        <div class="pricing-grid">
            <div class="price-card">
                <h3>Basic</h3>
                <p>Facebook Ad Setup + 1 Design. Ideal for small businesses starting out.</p>
            </div>
            <div class="price-card">
                <h3>Standard</h3>
                <p>Facebook + Instagram Ads + 3 Designs. Complete Social Media Presence.</p>
            </div>
            <div class="price-card">
                <h3>Premium</h3>
                <p>All Ads + SEO + Full Branding Kit. The ultimate growth package for established companies.</p>
            </div>
        </div>
    </div>

    <div class="section contact-form" id="contact">
        <h2>Contact Us</h2>
        <form>
            <input type="text" placeholder="Your Name" required />
            <input type="email" placeholder="Your Email" required />
            <textarea placeholder="Your Message" rows="5" required></textarea>
            <button>Send Message</button>
        </form>
    </div>

    <footer>
        <p>© 2025 SKY REACH MARKETING — All Rights Reserved</p>
    </footer>

    <a href="https://wa.me/923175181014" class="whatsapp-floating">💬</a>
</body>
</html>
