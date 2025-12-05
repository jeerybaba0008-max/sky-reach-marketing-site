<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>SKY REACH MARKETING</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* BASE STYLES & PREMIUM COLOR PALETTE */
        :root {
            --primary-color: #003366; /* Deep Navy Blue */
            --secondary-color: #ff6600; /* Bright Orange for accents */
            --background-light: #f5f8fb;
            --background-dark: #e0e6ed;
            --card-shadow: 0 8px 25px rgba(0, 51, 102, 0.1); /* Subtle Blue Shadow */
        }

        body { 
            margin: 0; 
            font-family: 'Poppins', sans-serif; 
            background: var(--background-light); 
            opacity: 0; /* Initial opacity for fade-in effect */
            transition: opacity 1.5s ease;
        }

        /* HEADER & NAVIGATION */
        header { 
            background: var(--primary-color); 
            color: white; 
            padding: 25px; 
            text-align: center; 
            font-size: 32px; 
            font-weight: 700; 
        }

        nav { 
            background: white; 
            padding: 15px 20px; 
            box-shadow: 0 4px 10px rgba(0,0,0,0.05); 
            display: flex; 
            justify-content: center; 
            gap: 30px; 
            position: sticky; 
            top: 0; 
            z-index: 100;
        }
        nav a { 
            text-decoration: none; 
            color: var(--primary-color); 
            font-size: 17px; 
            font-weight: 600;
            padding: 5px 0;
            transition: color 0.3s; 
        }
        nav a:hover { color: var(--secondary-color); border-bottom: 2px solid var(--secondary-color); }

        /* HERO SECTION */
        .hero { 
            background: url('https://picsum.photos/seed/digitalmarketing/1400/350') center/cover no-repeat; 
            height: 400px; /* Taller Hero */
            display: flex; 
            align-items: center; 
            justify-content: center; 
            color: white; 
            font-size: 44px; 
            font-weight: 700; 
            text-shadow: 1px 1px 8px rgba(0,0,0,0.8); 
            padding: 0 20px;
            text-align: center;
        }

        /* GENERAL SECTION STYLING */
        .section { 
            padding: 60px 20px; 
            text-align: center; 
            transition: opacity 0.8s, transform 0.8s; /* Animation properties */
            opacity: 0; 
            transform: translateY(30px);
        }
        .section.fade-in {
            opacity: 1;
            transform: translateY(0);
        }
        
        h2 {
            color: var(--primary-color);
            font-weight: 700;
            margin-bottom: 40px;
            position: relative;
        }
        h2::after { /* Underline for heading */
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 70px;
            height: 3px;
            background: var(--secondary-color);
            border-radius: 2px;
        }

        /* SERVICES GRID */
        .services { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; margin-top: 30px; }
        
        .card { 
            background: white; 
            padding: 25px; 
            border-radius: 15px; 
            box-shadow: var(--card-shadow); 
            transition: transform 0.3s, box-shadow 0.3s; 
            border-top: 5px solid transparent; 
        }
        .card:hover { 
            transform: translateY(-8px); 
            box-shadow: 0 12px 30px rgba(0, 51, 102, 0.2); 
            border-top-color: var(--secondary-color); /* Premium accent on hover */
        }
        
        .card img { width: 100%; height: 160px; object-fit: cover; border-radius: 10px; margin-bottom: 15px; }
        .card h3 { color: var(--primary-color); font-weight: 600; }

        /* OTHER SECTIONS */
        .about, .pricing, .testimonials, .portfolio, .contact-form { 
            background: white; 
            margin: 40px auto; 
            max-width: 1000px; 
            padding: 50px; 
            border-radius: 20px; 
            box-shadow: var(--card-shadow); 
            text-align: left;
        }
        
        .portfolio img { 
            width: 100%; 
            border-radius: 15px; 
            box-shadow: 0 4px 15px rgba(0,0,0,0.1); 
            margin-top: 20px; 
        }

        /* PRICING */
        .pricing-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .price-card { 
            background: var(--background-dark); 
            padding: 30px; 
            border-radius: 15px; 
            border: 3px solid var(--primary-color); 
            text-align: center;
        }
        .price-card h3 { color: var(--primary-color); font-size: 24px; margin-top: 0; }

        /* TESTIMONIALS */
        .testimonial-card { 
            background: #e6f7ff; /* Light Blue Background */
            color: #333;
            padding: 25px; 
            border-radius: 12px; 
            margin-bottom: 20px; 
            text-align: left; 
            border-left: 6px solid var(--secondary-color); 
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            font-style: italic;
        }

        /* CONTACT FORM */
        form input, form textarea { 
            width: 100%; 
            padding: 15px; 
            margin-top: 15px; 
            border: 1px solid #ccc; 
            border-radius: 10px; 
            box-sizing: border-box; 
            font-family: 'Poppins', sans-serif;
        }
        form textarea { resize: vertical; }

        form button { 
            background: var(--secondary-color); 
            color: white; 
            padding: 15px 30px; 
            border: none; 
            margin-top: 25px; 
            border-radius: 10px; 
            font-size: 18px; 
            cursor: pointer; 
            font-weight: 600;
            transition: background 0.3s; 
        }
        form button:hover { background: #e05c00; }

        /* FOOTER */
        footer { margin-top: 60px; background: var(--primary-color); color: white; padding: 35px; text-align: center; }

        /* WHATSAPP FLOAT */
        .whatsapp-floating { 
            position: fixed; 
            bottom: 30px; 
            right: 30px; 
            background: #25d366; 
            color: white; 
            padding: 18px 23px; /* Slightly larger button */
            border-radius: 50%; 
            text-decoration: none; 
            font-size: 26px; 
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
            z-index: 1000;
        }

        /* KEYFRAMES FOR ANIMATION */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
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
            <div class="card"><img src="https://picsum.photos/seed/facebookads/300/200" alt="Facebook Ads"/><h3>Facebook Ads</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/instagramads/300/200" alt="Instagram Ads"/><h3>Instagram Ads</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/tiktokads/300/200" alt="TikTok Ads"/><h3>TikTok Ads</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/gmailmarketing/300/200" alt="Gmail Marketing"/><h3>Gmail Marketing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/graphicdesign/300/200" alt="Graphic Designing"/><h3>Graphic Designing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/videoediting/300/200" alt="Video Editing"/><h3>Video Editing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/websitedesign/300/200" alt="Website Designing"/><h3>Website Designing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/seoservices/300/200" alt="SEO Services"/><h3>SEO Services</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/pagemanagement/300/200" alt="Facebook Page Management"/><h3>Facebook Page Management</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/accountmanagement/300/200" alt="Instagram Account Management"/><h3>Instagram Account Management</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/tiktokmanagement/300/200" alt="TikTok Account Management"/><h3>TikTok Account Management</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/dailyposting/300/200" alt="Daily Posting"/><h3>Daily Posting</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/comments/300/200" alt="Comments & Messages Handling"/><h3>Comments & Messages Handling</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/thumbnaildesign/300/200" alt="Thumbnail Design"/><h3>Thumbnail Design</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/shortvideos/300/200" alt="Short Videos"/><h3>Short Videos</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/youtubeedit/300/200" alt="YouTube Video Editing"/><h3>YouTube Video Editing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/logodesign/300/200" alt="Logo Designing"/><h3>Logo Designing</h3></div>
            <div class="card"><img src="https://picsum.photos/seed/businesscard/300/200" alt="Business Card Designing"/><h3>Business Card Designing</h3></div>
        </div>
    </div>

    <div class="section about" id="about">
        <h2>About Us</h2>
        <p>Sky Reach Marketing ek professional digital marketing agency hai jo businesses ko growth, branding aur online presence improve karne mein help karti hai. Hum Facebook Ads, Instagram Ads, TikTok Promotions, YouTube Management, Video Editing aur Graphic Designing jaisi top-tier services provide karte hain. Hamari team aapke business ko next level tak le jane ke liye passionate hai!</p>
    </div>

    <div class="section portfolio" id="portfolio">
        <h2>Portfolio</h2>
        <p>Our recent work and client results. We believe in transparency and measurable results.</p>
        <img src="https://picsum.photos/seed/portfolio/900/300" style="width:100%; border-radius:15px;" alt="Digital Marketing Portfolio Showcase"/>
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

    <script>
        // 1. Initial Fade-In Animation for the whole body
        document.addEventListener('DOMContentLoaded', (event) => {
            document.body.style.opacity = '1';
        });

        // 2. Scroll Reveal Animation for sections
        const sections = document.querySelectorAll('.section');

        const observerOptions = {
            root: null,
            threshold: 0.1, // Element is visible 10%
            rootMargin: '0px'
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                    observer.unobserve(entry.target); // Stop observing once animated
                }
            });
        }, observerOptions);

        sections.forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
