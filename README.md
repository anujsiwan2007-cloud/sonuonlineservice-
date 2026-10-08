<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sonu Cyber Goreakothi - Online Digital Services</title>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-color: #0b5ed7;
            --secondary-color: #0a58ca;
            --whatsapp-color: #25D366;
            --dark-color: #212529;
            --light-bg: #f8f9fa;
            --white: #ffffff;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: var(--light-bg);
            color: var(--dark-color);
            line-height: 1.6;
        }

        /* Header / Navbar */
        header {
            background: linear-gradient(135deg, var(--primary-color), #003296);
            color: var(--white);
            padding: 15px 5%;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.15);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            font-size: 28px;
            color: #ffc107;
        }

        .logo h1 {
            font-size: 22px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .logo span {
            font-size: 12px;
            display: block;
            color: #d1e7dd;
            font-weight: 400;
        }

        .btn-header-wa {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background-color: var(--whatsapp-color);
            color: var(--white);
            text-decoration: none;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .btn-header-wa:hover {
            background-color: #1eb956;
        }

        /* Hero Banner */
        .hero {
            background: linear-gradient(rgba(11, 94, 215, 0.85), rgba(10, 88, 202, 0.9)), url('https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=1200&q=80') center/cover;
            color: var(--white);
            text-align: center;
            padding: 60px 20px;
        }

        .hero h2 {
            font-size: 32px;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 16px;
            max-width: 600px;
            margin: 0 auto 25px;
            opacity: 0.95;
        }

        /* Search Box */
        .search-container {
            max-width: 500px;
            margin: 0 auto;
            position: relative;
        }

        .search-container input {
            width: 100%;
            padding: 14px 20px;
            border-radius: 30px;
            border: none;
            outline: none;
            font-size: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 30px;
        }

        .section-title h3 {
            font-size: 26px;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 8px;
        }

        .section-title h3::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background: var(--primary-color);
            bottom: 0;
            left: 25%;
            border-radius: 2px;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }

        .service-card {
            background: var(--white);
            border-radius: 12px;
            padding: 25px 20px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid #e9ecef;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .service-icon {
            width: 65px;
            height: 65px;
            background: #e7f1ff;
            color: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            margin: 0 auto 15px;
        }

        .service-card h4 {
            font-size: 18px;
            margin-bottom: 10px;
            color: var(--dark-color);
        }

        .service-card p {
            font-size: 13px;
            color: #6c757d;
            margin-bottom: 20px;
        }

        .btn-apply {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            background-color: var(--whatsapp-color);
            color: var(--white);
            text-decoration: none;
            padding: 10px 18px;
            border-radius: 25px;
            font-size: 14px;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .btn-apply:hover {
            background-color: #1eb956;
        }

        /* Address Banner */
        .location-info {
            background: #e7f1ff;
            border-left: 5px solid var(--primary-color);
            padding: 20px;
            border-radius: 8px;
            margin: 40px 0;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .location-info i {
            font-size: 32px;
            color: var(--primary-color);
        }

        /* Floating WhatsApp Button (No Number Visible) */
        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            width: 60px;
            height: 60px;
            background-color: var(--whatsapp-color);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 32px;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
            z-index: 1000;
            text-decoration: none;
            transition: transform 0.3s ease;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
        }

        /* Footer */
        footer {
            background-color: #111827;
            color: #9ca3af;
            text-align: center;
            padding: 25px 20px;
            margin-top: 50px;
            font-size: 14px;
        }

        footer strong {
            color: var(--white);
        }

        @media (max-width: 600px) {
            .hero h2 {
                font-size: 24px;
            }
            .hero p {
                font-size: 14px;
            }
            .logo h1 {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header>
        <div class="logo">
            <i class="fa-solid fa-laptop-code"></i>
            <div>
                <h1>Sonu Cyber</h1>
                <span>Goreakothi Digital Point</span>
            </div>
        </div>
        <a href="https://wa.me/918227002020?text=Namaste%20Sonu%20Cyber,%20mujhe%20online%20service%20chahiye." target="_blank" class="btn-header-wa">
            <i class="fa-brands fa-whatsapp" style="font-size: 18px;"></i>
            <span>Contact</span>
        </a>
    </header>

    <!-- Hero Banner -->
    <section class="hero">
        <h2>Sonu Cyber Goreakothi</h2>
        <p>Aapke sabhi digital aur online sarkari kaam ek hi jagah par aasan aur tezi se kiye jaate hain.</p>
        
        <div class="search-container">
            <input type="text" id="searchInput" onkeyup="filterServices()" placeholder="Koyi bhi service search karein (e.g. Aadhar, Pan, Form)...">
        </div>
    </section>

    <!-- Main Content -->
    <main class="container">
        <div class="section-title">
            <h3>Hamari Digital Services</h3>
        </div>

        <div class="services-grid" id="servicesGrid">
            
            <!-- Service Item 1 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-id-card"></i></div>
                    <h4>Aadhar Card Services</h4>
                    <p>Aadhar download, print, address update, aur PVC card order.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Aadhar%20Card%20Service%20chahiye" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 2 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-address-card"></i></div>
                    <h4>PAN Card Apply</h4>
                    <p>Naya Pan Card apply karein, correction aur instant e-PAN banwayein.</p>
                </div>
                <a href="https://wa.me/918227002020?text=PAN%20Card%20Apply%20karna%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 3 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-check-to-slot"></i></div>
                    <h4>Voter ID Card</h4>
                    <p>Naya Voter ID card apply karein, correction aur PVC card download.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Voter%20ID%20Card%20kaam%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 4 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-graduation-cap"></i></div>
                    <h4>Online Job Form</h4>
                    <p>Sarkari naukri, SSC, Railway, Banking aur police form bharein.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Online%20Form%20bharna%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 5 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-user-graduate"></i></div>
                    <h4>Scholarship Form</h4>
                    <p>Post Matric, PMS Bihar aur sabhi prakar ke scholarship forms.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Scholarship%20Form%20bharna%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 6 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-wheat-awn"></i></div>
                    <h4>Ration Card & Caste/Income</h4>
                    <p>Ration card apply, Jati, Aaya, aur Niwas praman patra banwayein.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Jati/Aaya/Niwas/Ration%20Card%20kaam%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 7 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-hand-holding-dollar"></i></div>
                    <h4>Pension & PF Service</h4>
                    <p>Vridha pension application aur EPF withdrawal & KYC.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Pension%20/%20PF%20kaam%20hai" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

            <!-- Service Item 8 -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-print"></i></div>
                    <h4>Print & Photo Service</h4>
                    <p>Color print, Xerox, Lamination aur Passport size photo Service.</p>
                </div>
                <a href="https://wa.me/918227002020?text=Printout%20/%20Photo%20Service" target="_blank" class="btn-apply">
                    <i class="fa-brands fa-whatsapp"></i> Apply via WhatsApp
                </a>
            </div>

        </div>

        <!-- Shop Address Section -->
        <div class="location-info">
            <i class="fa-solid fa-location-dot"></i>
            <div>
                <h4 style="font-size: 18px; color: #0b5ed7;">Dukan ka Pata / Location</h4>
                <p style="font-size: 15px; color: #333; font-weight: 500;">
                    Sonu Cyber, Main Market, Goreakothi, Siwan, Bihar - 841434
                </p>
            </div>
        </div>
    </main>

    <!-- Floating WhatsApp Action Button -->
    <a href="https://wa.me/918227002020?text=Namaste%20Sonu%20Cyber,%20mujhe%20service%20chahiye." class="whatsapp-float" target="_blank" title="Chat on WhatsApp">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 <strong>Sonu Cyber Goreakothi</strong>. All Rights Reserved.</p>
    </footer>

    <!-- Search JavaScript -->
    <script>
        function filterServices() {
            let input = document.getElementById('searchInput').value.toLowerCase();
            let cards = document.getElementsByClassName('service-card');

            for (let i = 0; i < cards.length; i++) {
                let cardText = cards[i].innerText.toLowerCase();
                if (cardText.includes(input)) {
                    cards[i].style.display = "";
                } else {
                    cards[i].style.display = "none";
                }
            }
        }
    </script>
</body>
</html>
