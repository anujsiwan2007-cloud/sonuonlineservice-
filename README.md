<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SONU CYBER ONLINE SERVICE PORTAL | Sonu Cyber Goreakothi</title>
    <meta name="description" content="Fast, Safe & Smart Digital Services Portal - Sonu Cyber Goreakothi, College Road, Goreakothi, Siwan, Bihar.">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #080c1a;
            --bg-card: rgba(16, 24, 48, 0.85);
            --bg-card-hover: rgba(28, 40, 78, 0.95);
            --neon-blue: #00f0ff;
            --neon-purple: #9d4edd;
            --neon-pink: #ff007f;
            --neon-cyan: #00e5ff;
            --whatsapp-green: #25d366;
            --text-main: #f0f4f8;
            --text-sub: #a0aec0;
            --border-glow: rgba(0, 240, 255, 0.3);
            --shadow-glow: 0 8px 32px 0 rgba(0, 240, 255, 0.2);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Outfit', sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            background-image: 
                radial-gradient(circle at 15% 15%, rgba(157, 78, 221, 0.18) 0%, transparent 40%),
                radial-gradient(circle at 85% 85%, rgba(0, 240, 255, 0.18) 0%, transparent 40%),
                linear-gradient(180deg, #050811 0%, #080c1a 100%);
            background-attachment: fixed;
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden;
        }

        /* Header Styling */
        header {
            background: rgba(8, 12, 26, 0.9);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-glow);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 1rem 1.5rem;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-icon {
            font-size: 2.2rem;
            background: linear-gradient(135deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 0 8px rgba(0, 240, 255, 0.6));
        }

        .brand-text h1 {
            font-size: 1.35rem;
            font-weight: 800;
            letter-spacing: 0.5px;
            background: linear-gradient(90deg, #ffffff, var(--neon-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .brand-text p {
            font-size: 0.8rem;
            color: var(--neon-blue);
            font-weight: 500;
        }

        .location-badge {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(0, 240, 255, 0.1);
            border: 1px solid rgba(0, 240, 255, 0.3);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            color: var(--neon-cyan);
        }

        /* Hero & Search Section */
        .hero {
            text-align: center;
            padding: 2.5rem 1rem 1.5rem 1rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h2 {
            font-size: 2rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 12px rgba(157, 78, 221, 0.4);
        }

        .hero p {
            color: var(--text-sub);
            font-size: 1rem;
            margin-bottom: 1.5rem;
        }

        .search-box {
            position: relative;
            max-width: 600px;
            margin: 0 auto;
        }

        .search-box input {
            width: 100%;
            padding: 1rem 1.5rem 1rem 3.2rem;
            background: rgba(16, 24, 48, 0.95);
            border: 1px solid var(--border-glow);
            border-radius: 50px;
            color: var(--text-main);
            font-size: 1rem;
            outline: none;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.5), var(--shadow-glow);
            transition: all 0.3s ease;
        }

        .search-box input:focus {
            border-color: var(--neon-blue);
            box-shadow: 0 0 20px rgba(0, 240, 255, 0.5);
        }

        .search-box i {
            position: absolute;
            left: 1.2rem;
            top: 50%;
            transform: translateY(-50%);
            color: var(--neon-blue);
            font-size: 1.2rem;
        }

        /* Navigation Controls (Breadcrumb & Back) */
        .nav-controls {
            max-width: 1200px;
            margin: 1rem auto;
            padding: 0 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .breadcrumbs {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 0.95rem;
            color: var(--text-sub);
        }

        .breadcrumbs span.active {
            color: var(--neon-blue);
            font-weight: 700;
        }

        .btn-back {
            display: none;
            align-items: center;
            gap: 0.5rem;
            background: linear-gradient(135deg, rgba(157, 78, 221, 0.4), rgba(0, 240, 255, 0.4));
            border: 1px solid var(--neon-blue);
            color: #fff;
            padding: 0.55rem 1.3rem;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 700;
            transition: all 0.3s ease;
        }

        .btn-back:hover {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-blue));
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.6);
            transform: translateY(-2px);
        }

        /* Container & Cards Grid */
        main {
            max-width: 1200px;
            margin: 0 auto 3rem auto;
            padding: 0 1.5rem;
            flex-grow: 1;
            width: 100%;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 1.5rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card:hover {
            transform: translateY(-6px);
            background: var(--bg-card-hover);
            border-color: var(--border-glow);
            box-shadow: var(--shadow-glow);
        }

        .card:hover::before {
            opacity: 1;
        }

        .card-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin-bottom: 1rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--neon-blue);
            transition: all 0.3s ease;
        }

        .card:hover .card-icon {
            transform: scale(1.1) rotate(3deg);
            color: #fff;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-blue));
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.4);
        }

        .card-title {
            font-size: 1.15rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--text-main);
        }

        .card-desc {
            font-size: 0.85rem;
            color: var(--text-sub);
            line-height: 1.4;
        }

        /* Service Item Card Specifics */
        .service-card {
            align-items: flex-start;
            text-align: left;
        }

        .service-card .card-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 0.8rem;
            width: 100%;
        }

        .service-card .card-icon {
            width: 45px;
            height: 45px;
            font-size: 1.3rem;
            margin-bottom: 0;
            flex-shrink: 0;
        }

        .btn-apply-whatsapp {
            margin-top: 1.2rem;
            width: 100%;
            padding: 0.7rem 1rem;
            background: linear-gradient(135deg, #25d366, #128c7e);
            border: none;
            color: #ffffff;
            border-radius: 8px;
            text-align: center;
            font-size: 0.9rem;
            font-weight: 700;
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.6rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(37, 211, 102, 0.25);
        }

        .service-card:hover .btn-apply-whatsapp {
            transform: scale(1.02);
            box-shadow: 0 6px 18px rgba(37, 211, 102, 0.5);
        }

        /* Empty State */
        .no-results {
            text-align: center;
            padding: 3rem 1rem;
            color: var(--text-sub);
            grid-column: 1 / -1;
        }

        .no-results i {
            font-size: 3rem;
            color: var(--neon-pink);
            margin-bottom: 1rem;
        }

        /* Footer */
        footer {
            background: rgba(4, 6, 14, 0.95);
            border-top: 1px solid var(--border-glow);
            padding: 2rem 1.5rem;
            text-align: center;
            margin-top: auto;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            align-items: center;
        }

        .footer-links {
            display: flex;
            gap: 1.5rem;
            font-size: 0.9rem;
            color: var(--text-sub);
            flex-wrap: wrap;
            justify-content: center;
        }

        /* Floating WhatsApp Button */
        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: linear-gradient(135deg, #25d366, #128c7e);
            color: white;
            border-radius: 50px;
            padding: 12px 22px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            font-weight: 800;
            font-size: 0.95rem;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            z-index: 1000;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .whatsapp-float:hover {
            transform: translateY(-4px) scale(1.05);
            box-shadow: 0 6px 25px rgba(37, 211, 102, 0.6);
            color: white;
        }

        .whatsapp-float i {
            font-size: 1.5rem;
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                align-items: flex-start;
            }

            .hero h2 {
                font-size: 1.5rem;
            }

            .grid-container {
                grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
                gap: 1rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo-section">
                <i class="fa-solid fa-desktop logo-icon"></i>
                <div class="brand-text">
                    <h1>SONU CYBER ONLINE SERVICE PORTAL</h1>
                    <p>Sonu Cyber Goreakothi - Fast, Safe & Smart Digital Services</p>
                </div>
            </div>
            <div class="location-badge">
                <i class="fa-solid fa-location-dot"></i>
                <span>College Road, Goreakothi, Siwan</span>
            </div>
        </div>
    </header>

    <!-- Hero & Search Section -->
    <section class="hero">
        <h2>सभी ऑनलाइन एवं डिजिटल सेवाओं की सुविधा</h2>
        <p>सर्विस चुनें और सीधे सोनू साइबर गोरेयाकोठी से संपर्क करें।</p>
        <div class="search-box">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" id="searchInput" placeholder="Search service (e.g. Aadhaar, PAN, Scholarship, Caste Certificate)..." onkeyup="handleSearch()">
        </div>
    </section>

    <!-- Navigation Breadcrumbs & Back Control -->
    <div class="nav-controls">
        <div class="breadcrumbs" id="breadcrumbs">
            <span><i class="fa-solid fa-house"></i> Home</span>
        </div>
        <button class="btn-back" id="backBtn" onclick="showCategories()">
            <i class="fa-solid fa-arrow-left"></i> Back to Categories
        </button>
    </div>

    <!-- Main Dynamic Content Grid -->
    <main>
        <div class="grid-container" id="portalGrid">
            <!-- Categories and Services render dynamically -->
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <span><strong>Sonu Cyber Goreakothi</strong></span> | 
                <span>Address: College Road, Goreakothi, Siwan, Bihar</span>
            </div>
            <p style="font-size: 0.85rem; color: var(--text-sub);">&copy; 2026 SONU CYBER ONLINE SERVICE PORTAL. All rights reserved.</p>
        </div>
    </footer>

    <!-- Floating General WhatsApp Button -->
    <a href="https://wa.me/918227002020?text=Hello%20Sonu%20Cyber,%20I%20need%20help%20with%20an%20online%20service.%20Please%20guide%20me." 
       class="whatsapp-float" 
       target="_blank" 
       rel="noopener noreferrer">
        <i class="fa-brands fa-whatsapp"></i>
        <span>Get Help</span>
    </a>

    <!-- JavaScript Data & Logic -->
    <script>
        const phoneNo = "918227002020";

        // Category and Services Data
        const portalData = [
            {
                id: 'aadhaar',
                title: 'Aadhaar Services',
                icon: 'fa-id-card',
                color: '#00f0ff',
                desc: 'Download e-Aadhaar, address update, status check & info.',
                services: [
                    { name: 'Download e-Aadhaar', desc: 'Get electronic password-protected Aadhaar PDF.' },
                    { name: 'Aadhaar Status Check', desc: 'Check status of update or enrollment.' },
                    { name: 'Aadhaar Address Update', desc: 'Update residential address with valid proof.' },
                    { name: 'Name & DOB Update Info', desc: 'Correction rules and valid documents guidance.' },
                    { name: 'Mobile / Biometric Update Slot', desc: 'Help with Aadhaar Seva Kendra appointment booking.' },
                    { name: 'Find Aadhaar Centre', desc: 'Locate authorized Aadhaar centers near Goreakothi.' },
                    { name: 'Virtual ID (VID) Generation', desc: 'Generate 16-digit Virtual ID for privacy.' }
                ]
            },
            {
                id: 'pan',
                title: 'PAN Card Services',
                icon: 'fa-file-invoice-dollar',
                color: '#9d4edd',
                desc: 'Apply new PAN, correction, PAN-Aadhaar link & e-PAN.',
                services: [
                    { name: 'Apply New PAN Card', desc: 'New PAN card application service.' },
                    { name: 'PAN Correction & Update', desc: 'Name, DOB, Father Name or Photo correction.' },
                    { name: 'PAN Application Status', desc: 'Track application status.' },
                    { name: 'Link PAN with Aadhaar', desc: 'Mandatory PAN-Aadhaar linking assistance.' },
                    { name: 'e-PAN Card Print', desc: 'Instant PDF download and printing.' }
                ]
            },
            {
                id: 'scholarship',
                title: 'Scholarship Services',
                icon: 'fa-graduation-cap',
                color: '#ff007f',
                desc: 'National & Bihar state scholarship applications.',
                services: [
                    { name: 'Bihar Post Matric Scholarship', desc: 'BC, EBC, SC & ST scholarship application.' },
                    { name: 'National Scholarship Portal (NSP)', desc: 'Pre-matric and post-matric central schemes.' },
                    { name: 'MedhaSoft Bihar', desc: 'School DBT scholarship status & entry.' },
                    { name: 'Bihar e-Kalyan Scheme', desc: 'Kanya Utthan & Matric/Inter incentive schemes.' },
                    { name: 'Scholarship Application Status', desc: 'Track college & district level status.' }
                ]
            },
            {
                id: 'jpu',
                title: 'JPU University Services',
                icon: 'fa-university',
                color: '#00e5ff',
                desc: 'JP University Chapra admissions, exam forms & results.',
                services: [
                    { name: 'JPU Admission Application', desc: 'UG / PG online admission application assistance.' },
                    { name: 'Examination Form Filling', desc: 'UG & PG semester examination forms.' },
                    { name: 'Admit Card Download & Print', desc: 'University examination admit card printing.' },
                    { name: 'JPU Results & Marks Info', desc: 'Check UG/PG examination results.' },
                    { name: 'Registration Slip Download', desc: 'Student registration slips retrieval.' }
                ]
            },
            {
                id: 'bihar_gov',
                title: 'Bihar RTPS & Land Services',
                icon: 'fa-building-columns',
                color: '#ffc107',
                desc: 'Caste, Income, Residence certificates & Bihar Bhumi.',
                services: [
                    { name: 'Caste Certificate (Jati)', desc: 'Online application for Caste Certificate.' },
                    { name: 'Income Certificate (Aaya)', desc: 'Online application for Income Certificate.' },
                    { name: 'Residence Certificate (Niwas)', desc: 'Online application for Domicile/Niwas.' },
                    { name: 'EWS & Non-Creamy Layer (NCL)', desc: 'EWS and OBC/EBC NCL Certificate.' },
                    { name: 'Bihar Bhumi Land Tax & Lagan', desc: 'Khatian, Jamabandi & Online Lagan payment.' },
                    { name: 'Ration Card Online Apply', desc: 'New Ration Card application & modification.' },
                    { name: 'Character Certificate (Police)', desc: 'Online character certificate application.' }
                ]
            },
            {
                id: 'jobs',
                title: 'Govt Jobs & Online Forms',
                icon: 'fa-briefcase',
                color: '#00e676',
                desc: 'SSC, UPSC, BPSC, Railway, Bihar Police & GDS forms.',
                services: [
                    { name: 'SSC Form Apply', desc: 'CGL, CHSL, MTS, GD Constable forms.' },
                    { name: 'BPSC & BSSC Form Apply', desc: 'Bihar Teacher, CGL & Inter level online forms.' },
                    { name: 'Bihar Police & Sub Inspector', desc: 'Constable & SI online application.' },
                    { name: 'Railway Recruitment (RRB)', desc: 'NTPC, Group D, ALP & Technician forms.' },
                    { name: 'India Post GDS Online', desc: 'Gramin Dak Sevak application.' }
                ]
            },
            {
                id: 'education',
                title: 'Education & Admissions',
                icon: 'fa-book-bookmark',
                color: '#ff9100',
                desc: 'OFSS Bihar, IGNOU, NIOS & Student Credit Card.',
                services: [
                    { name: 'Bihar OFSS 11th Admission', desc: 'Online Facilitation System admission form.' },
                    { name: 'IGNOU Admission & Assignments', desc: 'Distance courses application & assignment submission.' },
                    { name: 'NIOS Open School Admission', desc: '10th & 12th open board admission.' },
                    { name: 'Bihar Student Credit Card', desc: 'Education loan scheme application guidance.' },
                    { name: 'DigiLocker ABC ID Creation', desc: 'Academic Bank of Credits ID creation.' }
                ]
            },
            {
                id: 'identity',
                title: 'Passport & Voter ID',
                icon: 'fa-passport',
                color: '#e040fb',
                desc: 'Passport Seva, Voter ID card & DigiLocker.',
                services: [
                    { name: 'Fresh Passport Application', desc: 'Online application & appointment booking.' },
                    { name: 'New Voter ID Card (Form 6)', desc: 'Apply new Voter ID online.' },
                    { name: 'Voter ID Card Correction', desc: 'Name, Address & Photo correction.' },
                    { name: 'Download e-EPIC Voter Card', desc: 'Digital Voter Card PDF download.' }
                ]
            },
            {
                id: 'transport',
                title: 'Railway & Driving License',
                icon: 'fa-train-subway',
                color: '#00b0ff',
                desc: 'Train ticket booking, Learner license & e-Challan.',
                services: [
                    { name: 'Train Ticket Booking (IRCTC)', desc: 'Normal & Tatkal train ticket booking.' },
                    { name: 'Learner Driving License', desc: 'Online application & LL test slot.' },
                    { name: 'Driving License Renewal', desc: 'DL Renewal & address change.' },
                    { name: 'Traffic e-Challan Payment', desc: 'Check and pay vehicle e-challan.' }
                ]
            },
            {
                id: 'rural',
                title: 'Farmer & Rural Schemes',
                icon: 'fa-wheat-awn',
                color: '#76ff03',
                desc: 'PM-Kisan, MGNREGA & PMAY Gramin.',
                services: [
                    { name: 'PM-Kisan Registration & e-KYC', desc: 'PM Kisan Samman Nidhi e-KYC and status.' },
                    { name: 'PMAY Gramin Awaas Status', desc: 'Awaas Yojana beneficiary list & status.' },
                    { name: 'MGNREGA Job Card', desc: 'Job card status and payment tracking.' }
                ]
            },
            {
                id: 'health',
                title: 'Health & Ayushman Card',
                icon: 'fa-heart-pulse',
                color: '#ff5252',
                desc: 'Ayushman Card (5 Lakh), e-Shram & PF.',
                services: [
                    { name: 'Ayushman Bharat Card Download', desc: 'Rs 5 Lakh free health card application.' },
                    { name: 'e-Shram Card Registration', desc: 'Unorganized worker card registration.' },
                    { name: 'EPFO PF Balance & Withdrawal', desc: 'PF passbook check & online claim.' }
                ]
            },
            {
                id: 'business',
                title: 'Business Registrations',
                icon: 'fa-store',
                color: '#ffd700',
                desc: 'Udyam MSME, GST & Food License.',
                services: [
                    { name: 'Udyam Registration (MSME)', desc: 'Free business registration card.' },
                    { name: 'GST Registration', desc: 'New GST number application.' },
                    { name: 'FSSAI Food License', desc: 'Shop & hotel food hygiene registration.' }
                ]
            },
            {
                id: 'tools',
                title: 'Photo & PDF Printing Services',
                icon: 'fa-print',
                color: '#69f0ae',
                desc: 'Photo editing, PDF compress & high quality printouts.',
                services: [
                    { name: 'High Quality Photo & Passport Photo', desc: 'Instant passport size photo printing.' },
                    { name: 'PDF Compress & Format Change', desc: 'Resize & format documents for online forms.' },
                    { name: 'Lamination & Scanning', desc: 'Document scanning and PVC card printout.' }
                ]
            },
            {
                id: 'legal',
                title: 'Electricity Bill & Utility',
                icon: 'fa-bolt',
                color: '#ff80ab',
                desc: 'NBPDCL Electricity bill pay & grievances.',
                services: [
                    { name: 'NBPDCL Electricity Bill Payment', desc: 'Quick online bill payment & receipt.' },
                    { name: 'New Electricity Connection', desc: 'Apply online for new meter.' },
                    { name: 'CPGRAMS Public Grievance', desc: 'Lodge government department complaints.' }
                ]
            }
        ];

        let currentCategoryId = null;

        // Page Init
        document.addEventListener('DOMContentLoaded', () => {
            showCategories();
        });

        // Step 1: Render All Categories
        function showCategories() {
            currentCategoryId = null;
            const grid = document.getElementById('portalGrid');
            const breadcrumbs = document.getElementById('breadcrumbs');
            const backBtn = document.getElementById('backBtn');
            const searchInput = document.getElementById('searchInput');

            searchInput.value = '';
            backBtn.style.display = 'none';
            breadcrumbs.innerHTML = `<span><i class="fa-solid fa-house"></i> Home</span>`;

            grid.innerHTML = '';
            portalData.forEach(cat => {
                const card = document.createElement('div');
                card.className = 'card';
                card.onclick = () => showServices(cat.id);
                card.innerHTML = `
                    <div class="card-icon" style="color: ${cat.color}; border-color: ${cat.color}40">
                        <i class="fa-solid ${cat.icon}"></i>
                    </div>
                    <div class="card-title">${cat.title}</div>
                    <div class="card-desc">${cat.desc}</div>
                `;
                grid.appendChild(card);
            });
        }

        // Step 2: Render Services of Category
        function showServices(categoryId) {
            currentCategoryId = categoryId;
            const category = portalData.find(c => c.id === categoryId);
            if (!category) return;

            const grid = document.getElementById('portalGrid');
            const breadcrumbs = document.getElementById('breadcrumbs');
            const backBtn = document.getElementById('backBtn');
            const searchInput = document.getElementById('searchInput');

            searchInput.value = '';
            backBtn.style.display = 'inline-flex';
            breadcrumbs.innerHTML = `
                <span style="cursor:pointer;" onclick="showCategories()"><i class="fa-solid fa-house"></i> Home</span>
                <i class="fa-solid fa-chevron-right" style="font-size:0.7rem;"></i>
                <span class="active">${category.title}</span>
            `;

            renderServiceList(category.services, category.color, category.icon);
        }

        // Render Services with WhatsApp Help Action
        function renderServiceList(services, color, defaultIcon) {
            const grid = document.getElementById('portalGrid');
            grid.innerHTML = '';

            if (services.length === 0) {
                grid.innerHTML = `
                    <div class="no-results">
                        <i class="fa-solid fa-circle-xmark"></i>
                        <h3>कोई सेवा नहीं मिली</h3>
                        <p>कृपया दूसरे शब्द जैसे "Aadhaar", "PAN", या "Caste" से खोजें।</p>
                    </div>
                `;
                return;
            }

            services.forEach(srv => {
                const waMessage = encodeURIComponent(`Hello Sonu Cyber, I need help with "${srv.name}". Please guide me.`);
                const waUrl = `https://wa.me/${phoneNo}?text=${waMessage}`;

                const card = document.createElement('div');
                card.className = 'card service-card';
                card.onclick = () => window.open(waUrl, '_blank');
                card.innerHTML = `
                    <div class="card-header">
                        <div class="card-icon" style="color: ${color || 'var(--neon-blue)'}">
                            <i class="fa-solid ${defaultIcon || 'fa-hand-holding-hand'}"></i>
                        </div>
                        <div>
                            <div class="card-title" style="font-size:1.05rem;">${srv.name}</div>
                        </div>
                    </div>
                    <div class="card-desc">${srv.desc}</div>
                    <a href="${waUrl}" target="_blank" class="btn-apply-whatsapp" onclick="event.stopPropagation();">
                        <i class="fa-brands fa-whatsapp"></i>
                        <span>Apply / Help via WhatsApp</span>
                    </a>
                `;
                grid.appendChild(card);
            });
        }

        // Search Filter Logic
        function handleSearch() {
            const query = document.getElementById('searchInput').value.toLowerCase().trim();

            if (query === '') {
                if (currentCategoryId) {
                    showServices(currentCategoryId);
                } else {
                    showCategories();
                }
                return;
            }

            const backBtn = document.getElementById('backBtn');
            const breadcrumbs = document.getElementById('breadcrumbs');

            backBtn.style.display = 'inline-flex';
            breadcrumbs.innerHTML = `
                <span style="cursor:pointer;" onclick="showCategories()"><i class="fa-solid fa-house"></i> Home</span>
                <i class="fa-solid fa-chevron-right" style="font-size:0.7rem;"></i>
                <span class="active">Search: "${query}"</span>
            `;

            let matchingServices = [];
            portalData.forEach(cat => {
                cat.services.forEach(srv => {
                    if (srv.name.toLowerCase().includes(query) || srv.desc.toLowerCase().includes(query) || cat.title.toLowerCase().includes(query)) {
                        matchingServices.push({
                            ...srv,
                            color: cat.color,
                            icon: cat.icon
                        });
                    }
                });
            });

            renderServiceList(matchingServices, 'var(--neon-blue)', 'fa-magnifying-glass');
        }
    </script>
</body>
</html>
