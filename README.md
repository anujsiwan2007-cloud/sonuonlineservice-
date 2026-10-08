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

        .btn-portal-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background-color: #ffc107;
            color: #000;
            text-decoration: none;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .btn-portal-link:hover {
            background-color: #e0a800;
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

        .btn-official {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            background-color: var(--primary-color);
            color: var(--white);
            text-decoration: none;
            padding: 10px 18px;
            border-radius: 25px;
            font-size: 14px;
            font-weight: 600;
            transition: background 0.3s ease;
        }

        .btn-official:hover {
            background-color: var(--secondary-color);
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
        <a href="https://sarkariresult.com" target="_blank" class="btn-portal-link">
            <i class="fa-solid fa-globe"></i>
            <span>Govt Portal</span>
        </a>
    </header>

    <!-- Hero Banner -->
    <section class="hero">
        <h2>Sonu Cyber Goreakothi</h2>
        <p>Aapke sabhi digital aur online sarkari kaam ke official portals ki jankari aur link.</p>
        
        <div class="search-container">
            <input type="text" id="searchInput" onkeyup="filterServices()" placeholder="Koyi bhi service search karein (e.g. Aadhar, Pan, Form)...">
        </div>
    </section>

    <!-- Main Content -->
    <main class="container">
        <div class="section-title">
            <h3>Official Digital Portals</h3>
        </div>

        <div class="services-grid" id="servicesGrid">
            
            <!-- Service Item 1: UIDAI Aadhar Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-id-card"></i></div>
                    <h4>Aadhar Card Portal</h4>
                    <p>UIDAI Official Portal: Download Aadhar, Status Check, PVC Card Order.</p>
                </div>
                <a href="https://myaadhaar.uidai.gov.in" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> UIDAI Portal Open
                </a>
            </div>

            <!-- Service Item 2: PAN Card Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-address-card"></i></div>
                    <h4>PAN Card Portal</h4>
                    <p>NSDL / UTIITSL Portal: Naya PAN apply karein aur correction karein.</p>
                </div>
                <a href="https://www.onlineservices.nsdl.com/paam/endUserRegisterContact.html" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> NSDL PAN Portal
                </a>
            </div>

            <!-- Service Item 3: Voter ID Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-check-to-slot"></i></div>
                    <h4>Voter Service Portal</h4>
                    <p>Voters Service Portal: Naya Voter ID card aur Correction Portal.</p>
                </div>
                <a href="https://voters.eci.gov.in" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> Voter Portal Open
                </a>
            </div>

            <!-- Service Item 4: Sarkari Jobs Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-graduation-cap"></i></div>
                    <h4>Sarkari Result Portal</h4>
                    <p>Sabhi Sarkari Naukri, Admit Card aur Result portal link.</p>
                </div>
                <a href="https://www.sarkariresult.com" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> Sarkari Result Open
                </a>
            </div>

            <!-- Service Item 5: Bihar Scholarship Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-user-graduate"></i></div>
                    <h4>Medhasoft Scholarship</h4>
                    <p>Bihar PMS & Medhasoft Scholarship Portal for Students.</p>
                </div>
                <a href="https://pmsonline.bih.nic.in" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> Scholarship Portal
                </a>
            </div>

            <!-- Service Item 6: RTPS Bihar (Jati, Aaya, Niwas) -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-file-contract"></i></div>
                    <h4>RTPS Bihar (Jati/Aaya/Niwas)</h4>
                    <p>ServicePlus Bihar: Jati, Aaya, Niwas, LPC & Ration Card Services.</p>
                </div>
                <a href="https://serviceonline.bihar.gov.in" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> RTPS Bihar Open
                </a>
            </div>

            <!-- Service Item 7: EPFO Pension & PF Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-hand-holding-dollar"></i></div>
                    <h4>EPFO Unified Portal</h4>
                    <p>Member Passbook, Pension, EPF Balance & Claim Portal.</p>
                </div>
                <a href="https://unifiedportal-mem.epfindia.gov.in/memberinterface/" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> EPFO Portal Open
                </a>
            </div>

            <!-- Service Item 8: Driving License Portal -->
            <div class="service-card">
                <div>
                    <div class="service-icon"><i class="fa-solid fa-id-badge"></i></div>
                    <h4>Parivahan Sewa</h4>
                    <p>Driving License, Learner License & Vehicle Registration Portal.</p>
                </div>
                <a href="https://parivahan.gov.in" target="_blank" class="btn-official">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> Parivahan Portal
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
