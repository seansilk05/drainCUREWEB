# drainCUREWEB
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>drainCURE - Fresh. Clean. Flowing. by bioCURE</title>
    <style>
        /* General Styles */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            color: #333;
            line-height: 1.6;
            background-color: #f4f8f7; /* Light background */
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        h1, h2, h3 {
            color: #1a5273; /* Darker blue for headings */
            text-align: center;
            margin-bottom: 20px;
        }

        p {
            text-align: center;
            margin-bottom: 15px;
        }

        .btn {
            display: inline-block;
            background-color: #4CAF50; /* Green button */
            color: white;
            padding: 12px 25px;
            text-align: center;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
            margin-top: 20px;
        }

        .btn:hover {
            background-color: #45a049;
        }

        /* Header */
        header {
            background-color: #e0f2f7; /* Light blue/green */
            padding: 15px 0;
            border-bottom: 2px solid #a7d9ee;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 30px; /* Adjusted logo size - even smaller */
            margin-right: 10px;
        }

        .logo span {
            font-size: 1.8em;
            font-weight: bold;
            color: #1a5273;
        }

        .nav-links {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .nav-links li {
            margin-left: 25px;
        }

        .nav-links a {
            text-decoration: none;
            color: #1a5273;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #4CAF50;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('CitySkylineSouthAfrica.jpeg') no-repeat center center/cover;
            color: white;
            padding: 100px 20px;
            text-align: center;
        }

        .hero h1 {
            font-size: 3em; /* Adjusted to help fit on one line */
            margin-bottom: 15px;
            color: white;
        }

        .hero p {
            font-size: 1.3em;
            margin-bottom: 30px;
            color: rgba(255, 255, 255, 0.9);
        }

        /* Section Styling */
        section {
            padding: 60px 0;
            text-align: center;
        }

        section:nth-of-type(even) {
            background-color: #f4f8f7;
        }

        .product-features, .how-it-works, .our-story, .usp-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
        }

        /* Styles for the feature items */
        .feature-item, .step-item, .usp-item {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            flex: 1;
            min-width: 280px;
            max-width: 350px;
            text-align: left;
        }

        /* --- UPDATES FOR FEATURE ITEMS BACKGROUND AND TEXT COLOR --- */
        .feature-item {
            background-color: #4CAF50; /* Green background */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Darker shadow for contrast */
        }

        .feature-item i {
            color: white; /* White icon */
        }

        .feature-item h3 {
            color: white; /* White heading text */
        }

        .feature-item p {
            color: rgba(255, 255, 255, 0.9); /* Slightly off-white paragraph text */
        }
        /* -------------------------------------------------------- */


        .feature-item i, .step-item i, .usp-item i {
            font-size: 2.5em;
            color: #4CAF50;
            margin-bottom: 15px;
        }

        .feature-item h3, .step-item h3, .usp-item h3 {
            font-size: 1.5em;
            color: #1a5273;
            margin-top: 0;
            text-align: left;
        }

        .feature-item p, .step-item p, .usp-item p {
            font-size: 1em;
            color: #555;
            text-align: left;
        }

        .our-story-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 30px;
            margin-top: 40px;
        }

        .founder-profile {
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            max-width: 800px;
            text-align: center;
        }

        .founder-profile img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 20px;
            /* UPDATED BORDER COLOR HERE */
            border: 4px solid #4CAF50; /* Green border */
        }

        .founder-profile h4 {
            color: #1a5273;
            margin-bottom: 5px;
        }

        .founder-profile p {
            text-align: center;
        }

        /* Testimonials/Campaigns */
        .testimonials {
            background-color: #e0f2f7;
            padding: 60px 0;
        }

        .testimonial-carousel {
            display: flex;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            gap: 20px;
            padding-bottom: 20px;
            -webkit-overflow-scrolling: touch; /* For smoother scrolling on iOS */
        }

        .testimonial-item {
            flex: 0 0 auto;
            width: 300px; /* Adjust width of each testimonial */
            background-color: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
            scroll-snap-align: start;
            text-align: left;
        }

        .testimonial-item p {
            font-style: italic;
            margin-bottom: 15px;
            text-align: left;
        }

        .testimonial-item span {
            font-weight: bold;
            color: #1a5273;
        }

        /* --- NEW SHOP SECTION STYLES --- */
        .product-listing {
            display: flex;
            justify-content: center;
            margin-top: 40px;
        }

        .product-card {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            max-width: 400px;
            text-align: center;
        }

        .product-img {
            max-width: 80%;
            height: auto;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .product-card h3 {
            color: #1a5273;
            margin-bottom: 10px;
        }

        .product-description {
            color: #555;
            margin-bottom: 20px;
        }

        .price-placeholder {
            font-size: 1.2em;
            font-weight: bold;
            color: #4CAF50;
            margin-bottom: 20px;
        }

        .buy-now-btn {
            background-color: #1a5273; /* Use a darker blue for this button for contrast */
            margin-top: 0; /* Override default button margin-top */
        }

        .buy-now-btn:hover {
            background-color: #28608f;
        }

        .map-container {
            margin-top: 40px;
            border-radius: 8px;
            overflow: hidden; /* Ensures the iframe corners are rounded */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        .map-container iframe {
            display: block; /* Removes extra space below iframe */
        }
        /* ---------------------------------- */


        /* Call to Action - WhatsApp/QR */
        .cta-section {
            background-color: #4CAF50;
            color: white;
            padding: 50px 20px;
        }

        .cta-section h2 {
            color: white;
            margin-bottom: 25px;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        .cta-buttons .btn {
            background-color: white;
            color: #4CAF50;
            border: 2px solid white;
            padding: 15px 30px;
            font-size: 1.1em;
        }

        .cta-buttons .btn:hover {
            background-color: #e0f2f7;
            color: #3e8e41;
        }
        .whatsapp-link {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        .whatsapp-link i {
            font-size: 1.5em;
        }


        /* Footer */
        footer {
            background-color: #1a5273; /* Dark blue */
            color: white;
            padding: 40px 0;
            text-align: center;
            font-size: 0.9em;
        }

        footer .social-links a {
            color: white;
            font-size: 1.5em;
            margin: 0 10px;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer .social-links a:hover {
            color: #4CAF50;
        }

        footer p {
            margin: 10px 0 0;
            color: rgba(255, 255, 255, 0.8);
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                align-items: flex-start;
            }
            .nav-links {
                margin-top: 15px;
                flex-direction: column;
                width: 100%;
            }
            .nav-links li {
                margin: 5px 0;
            }
            .hero h1 {
                font-size: 2.2em; /* Further adjustment for smaller screens */
            }
            .hero p {
                font-size: 1em;
            }
            .feature-item, .step-item, .usp-item, .product-card {
                max-width: 100%;
            }
            .founder-profile {
                width: 100%;
            }
            .testimonial-item {
                width: 250px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8em; /* Even smaller for very small screens */
            }
            .logo img {
                height: 40px;
            }
            .logo span {
                font-size: 1.5em;
            }
            .btn {
                padding: 10px 20px;
                font-size: 0.9em;
            }
            .cta-buttons {
                flex-direction: column;
            }
            .cta-buttons .btn {
                width: 80%;
            }
        }

        /* Font Awesome Icons */
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');
    </style>
</head>
<body>

    <header>
        <div class="container navbar">
            <div class="logo">
                <img src="newbiocurelogo.png" alt="bioCURE Logo">
                <span>drainCURE</span>
            </div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#product">Product</a></li>
                    <li><a href="#how-it-works">How It Works</a></li>
                    <li><a href="#shop">Shop</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <h1>drainCURE: Tough on Clogs. Gentle on Nature.</h1>
            <p>The natural, bacteria-powered solution for a healthier home and planet.</p>
            <a href="#product" class="btn">Discover drainCURE</a>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2>About drainCURE - Fresh. Clean. Flowing.</h2>
            <p>drainCURE, by bioCURE, is positioned as the premium, environmentally conscious solution for home and commercial drain maintenance.</p>
            <div class="product-features">
                <div class="feature-item">
                    <i class="fas fa-seedling"></i>
                    <h3>Natural Bio-Active Power</h3>
                    <p>Powered by natural bacteria for safe, effective breakdown of organic waste.</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-tint"></i>
                    <h3>Eco-Friendly & Biodegradable</h3>
                    <p>Our concentrated formula is eco-friendly and fully biodegradable, protecting our planet.</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-faucet"></i>
                    <h3>Prevents Odours & Blockages</h3>
                    <p>Prevents blockages and odours by clearing build-up at the source, ensuring optimal drain flow.</p>
                </div>
                <div class="feature-item">
                    <i class="fas fa-home"></i>
                    <h3>Safe for Septic Systems</h3>
                    <p>Unlike harsh chemicals, drainCURE is completely safe for all septic systems.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="how-it-works" style="background-color: #e0f2f7;">
        <div class="container">
            <h2>How drainCURE Works for You</h2>
            <p>Easy-to-apply, reliable maintenance for all your drainage needs.</p>
            <div class="how-it-works">
                <div class="step-item">
                    <i class="fas fa-flask"></i>
                    <h3>Targeted Action</h3>
                    <p>Our natural bacteria actively consume grease, food particles, and organic build-up.</p>
                </div>
                <div class="step-item">
                    <i class="fas fa-water"></i>
                    <h3>Restores Flow</h3>
                    <p>Clears existing build-up and maintains optimal drain flow, preventing slow drainage.</p>
                </div>
                <div class="step-item">
                    <i class="fas fa-spray-can"></i>
                    <h3>Eliminates Odours</h3>
                    <p>Eliminates unpleasant odours at their source, leaving your home fresh and clean.</p>
                </div>
            </div>
            <div class="dosage-info" style="margin-top: 40px; background-color: white; padding: 30px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.05);">
                <h3>Directions for Use</h3>
                <p style="text-align: left; font-style: italic;">drainCURE offers multi-purpose dosage instructions for various applications:</p>
                <ul style="text-align: left; list-style-type: disc; margin-left: 20px;">
                    <li>Initial treatment: Pour 500ml near blockage.</li>
                    <li>Maintenance (daily): 120ml for regular drains.</li>
                    <li>Kitchen sinks: 60ml daily.</li>
                    <li>Showers/basins/bathtubs: 120ml weekly.</li>
                    <li>Septic tanks: 500ml bi-weekly for 2 months, then monthly.</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="product">
        <div class="container">
            <h2>drainCURE - Your Concentrated Solution</h2>
            <div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 40px;">
                <div style="flex: 1; min-width: 300px; max-width: 450px;">
                    <img src="drainCURE Picture.png" alt="drainCURE Product Bottle" style="max-width: 100%; height: auto; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
                </div>
                <div style="flex: 1; min-width: 300px; max-width: 600px; text-align: left;">
                    <h3>Premium Drain Maintenance Solution</h3>
                    <p>bioCURE's drainCURE is a natural, bacteria-powered solution designed to eliminate odours, dissolve grease and organic buildup, and maintain free-flowing drains. Ideal for regular use in residential and commercial environments.</p>
                    <ul style="list-style: none; padding: 0;">
                        <li style="margin-bottom: 10px;"><i class="fas fa-check-circle" style="color: #4CAF50; margin-right: 10px;"></i>Clear, bold visual elements: blue/green tones convey cleanliness and natural ingredients.</li>
                        <li style="margin-bottom: 10px;"><i class="fas fa-check-circle" style="color: #4CAF50; margin-right: 10px;"></i>Prominent dosage instructions for both residential and commercial users.</li>
                        <li style="margin-bottom: 10px;"><i class="fas fa-check-circle" style="color: #4CAF50; margin-right: 10px;"></i>"Concentrated Formula" badge emphasizes value and effectiveness.</li>
                    </ul>
                    <p style="font-weight: bold; font-size: 1.1em; color: #1a5273; text-align: center;">Non-Acidic. Family-Safe. Eco Strong.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="shop" style="background-color: #f4f8f7;">
        <div class="container">
            <h2>Shop drainCURE</h2>
            <p>Get your drainCURE bottle today and experience the natural difference!</p>

            <div class="product-listing">
                <div class="product-card">
                    <img src="drainCURE Picture.png" alt="drainCURE Product" class="product-img">
                    <h3>drainCURE 1.5L Concentrated Liquid</h3>
                    <p class="product-description">The natural, bacteria-powered solution designed to eliminate odours, dissolve grease and organic buildup, and maintain free-flowing drains.</p>
                    <div class="price-placeholder">Price available upon inquiry.</div>
                    <a href="#" class="btn buy-now-btn">Buy Now (Coming Soon)</a>
                </div>
            </div>

            <h2 style="margin-top: 60px;">Find Us Locally</h2>
            <p>Explore our current and upcoming retail locations where you can purchase drainCURE.</p>

            <div class="map-container">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3434606.570776999!2d20.73030231575037!3d-30.55948248386419!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1c34a68297f62e07%3A0x6b772421319c8f0e!2sSouth%20Africa!5e0!3m2!1sen!2sza!4v1678901234567!5m2!1sen!2sza?hl=en&q=Stellenbosch+South+Africa&z=12&output=embed"
                    width="100%"
                    height="450"
                    style="border:0;"
                    allowfullscreen=""
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"
                    title="Map of Stellenbosch, South Africa"
                ></iframe>
                <p style="margin-top: 15px; font-style: italic;">Specific retail locations to be updated soon!</p>
            </div>
        </div>
    </section>

    <section id="our-story">
        <div class="container">
            <h2>Our Purpose: From Public to Purpose-Driven</h2>
            <p>At the heart of bioCURE's transformation lies the vision, resilience, and innovation of two formidable women.</p>
            <div class="our-story-content">
                <div class="founder-profile">
                    <img src="bioCURE Noleene.png" alt="Noleen Samuels">
                    <h4>Noleen Samuels, Founder and Director of bioCURE</h4>
                    <p>A pioneering force in South Africa's environmental services sector for over 15 years. Noleen built a business rooted in public-sector excellence and is now pivoting bioCURE towards a sustainable, commercial future.</p>
                </div>
                <div class="founder-profile">
                    <img src="bioCURE Nicky.png" alt="Nicky Lamohr">
                    <h4>Nicky Lamohr, Chief Operating Officer of B.E.C.S</h4>
                    <p>Brings a unique blend of operational discipline and leadership, having played a pivotal role in building out the systems, structures, and team alignment necessary to scale a commercial division from the ground up. As a woman in leadership, her presence not only drives performance but also sets a precedent for what inclusive, dynamic growth leadership looks like.</p>
                </div>
                <p style="max-width: 800px; text-align: center; font-style: italic; margin-top: 20px;">
                    Together, Noleen and Nicky are building a values-driven organisation rooted in service, innovation, and transformation—one that doesn't just clean the environment but clears the path for future women leaders to lead it.
                </p>
            </div>
        </div>
    </section>

    <section id="usp">
        <div class="container">
            <h2>Why Choose drainCURE?</h2>
            <p>Our unique selling propositions set us apart as the superior choice for drain maintenance.</p>
            <div class="usp-grid">
                <div class="usp-item">
                    <i class="fas fa-bacteria"></i>
                    <h3>Natural Bacteria Power</h3>
                    <p>Leverages natural bacteria for safe and effective breakdown of organic waste.</p>
                </div>
                <div class="usp-item">
                    <i class="fas fa-leaf"></i>
                    <h3>Truly Eco-Friendly</h3>
                    <p>Completely biodegradable and environmentally conscious, without harsh chemicals.</p>
                </div>
                <div class="usp-item">
                    <i class="fas fa-wrench"></i>
                    <h3>Preventative Maintenance</h3>
                    <p>Designed for daily/weekly use to prevent issues, not just for emergencies.</p>
                </div>
                <div class="usp-item">
                    <i class="fas fa-handshake"></i>
                    <h3>Trusted Brand</h3>
                    <p>Backed by bioCURE's broader mission in environmental health and sustainability.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="campaigns" class="testimonials">
        <div class="container">
            <h2>Join the #CleanGreenDrain Movement!</h2>
            <p>See what our customers are saying and share your own drainCURE success stories.</p>
            <div class="testimonial-carousel">
                <div class="testimonial-item">
                    <p>"drainCURE has transformed our restaurant's kitchen drains. No more greasy build-up or bad smells!"</p>
                    <span>— Chef Emily, Local Cafe</span>
                </div>
                <div class="testimonial-item">
                    <p>"Finally, an eco-friendly solution that actually works! My shower drain flows freely and no lingering odours."</p>
                    <span>— Sarah M., Homeowner</span>
                </div>
                <div class="testimonial-item">
                    <p>"As a facilities manager, I need reliable products. drainCURE is now a staple for all our properties."</p>
                    <span>— John D., Facilities Management</span>
                </div>
                 <div class="testimonial-item">
                    <p>"Love that it's safe for my septic tank. It's truly a maintenance solution, not just a quick fix."</p>
                    <span>— David R., Eco-conscious Homeowner</span>
                </div>
            </div>
            <p style="margin-top: 30px;">Share your experience using #CleanGreenDrain on social media!</p>
        </div>
    </section>

    <section class="cta-section">
        <div class="container">
            <h2>Ready for Fresh, Clean, Flowing Drains?</h2>
            <p>Scan the QR code on your bottle for demo videos & compliance sheets, or connect with us directly!</p>
            <div class="cta-buttons">
                <a href="#" class="btn whatsapp-link"><i class="fab fa-whatsapp"></i> Chat on WhatsApp</a>
                <a href="https://www.google.com/search?q=buy+draincure" target="_blank" class="btn">Find a Retailer</a>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <div class="social-links">
                <a href="https://www.facebook.com/bioCURESA" target="_blank"><i class="fab fa-facebook-f"></i></a>
                <a href="https://www.instagram.com/biocure_sa" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://www.linkedin.com/company/biocure-environmental-cleaning-services-pty-ltd" target="_blank"><i class="fab fa-linkedin-in"></i></a>
            </div>
            <p>© 2025 bioCURE. All rights reserved. Manufactured in Cape Town, South Africa.</p>
            <p>Complies with SANS 10234 for labelling and disposal.</p>
        </div>
    </footer>

</body>
</html>
