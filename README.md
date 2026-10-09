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

        .service-link-btn {
            margin-top: 1rem;
            width: 100%;
            padding: 0.65rem 1rem;
            background: rgba(0, 240, 255, 0.1);
            border: 1px solid var(--neon-blue);
            color: var(--neon-cyan);
            border-radius: 8px;
            text-align: center;
            font-size: 0.85rem;
            font-weight: 700;
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            transition: all 0.3s ease;
        }

        .service-card:hover .service-link-btn {
            background: var(--neon-blue);
            color: #080c1a;
            box-shadow: 0 0 12px rgba(0, 240, 255, 0.6);
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

        .footer-note {
            font-size: 0.78rem;
            color: #6c757d;
            max-width: 750px;
            line-height: 1.4;
        }

        /* Floating WhatsApp Help Button */
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
        <h2>सभी ऑनलाइन एवं सरकारी सेवाओं की सीधी पहुँच</h2>
        <p>अपनी आवश्यक सेवा खोजें और आधिकारिक पोर्टल पर जाएँ या मदद प्राप्त करें।</p>
        <div class="search-box">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" id="searchInput" placeholder="Search service (e.g. Aadhaar, PAN, Scholarship, SSC)..." onkeyup="handleSearch()">
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
            <p class="footer-note">
                <strong>Disclaimer:</strong> This website is an independent informational service portal maintained by Sonu Cyber Goreakothi. All links redirect directly to official government and university websites.
            </p>
            <p style="font-size: 0.85rem; color: var(--text-sub);">&copy; 2026 SONU CYBER ONLINE SERVICE PORTAL. All rights reserved.</p>
        </div>
    </footer>

    <!-- Floating WhatsApp Help Button -->
    <a href="https://wa.me/918227002020?text=Hello%20Sonu%20Cyber,%20I%20need%20help%20with%20an%20online%20service.%20Please%20guide%20me." 
       class="whatsapp-float" 
       target="_blank" 
       rel="noopener noreferrer">
        <i class="fa-brands fa-whatsapp"></i>
        <span>Get Help</span>
    </a>

    <!-- JavaScript Data & Logic -->
    <script>
        // Category and Official Services Data
        const portalData = [
            {
                id: 'aadhaar',
                title: 'Aadhaar Services',
                icon: 'fa-id-card',
                color: '#00f0ff',
                desc: 'UIDAI official services, e-Aadhaar download & status check.',
                services: [
                    { name: 'UIDAI Official Website', url: 'https://uidai.gov.in/', desc: 'Official Unique Identification Authority of India portal.' },
                    { name: 'My Aadhaar Portal', url: 'https://myaadhaar.uidai.gov.in/', desc: 'Direct resident portal for online Aadhaar services.' },
                    { name: 'Download e-Aadhaar', url: 'https://myaadhaar.uidai.gov.in/genricDownloadAadhaar', desc: 'Download password-protected electronic Aadhaar PDF.' },
                    { name: 'Aadhaar Status Check', url: 'https://myaadhaar.uidai.gov.in/CheckAadharStatus', desc: 'Check status of Aadhaar update or new enrollment.' },
                    { name: 'Aadhaar Address Update', url: 'https://myaadhaar.uidai.gov.in/', desc: 'Online address update with valid proof of residence.' },
                    { name: 'Name & DOB Update Info', url: 'https://uidai.gov.in/', desc: 'Official guidelines & proof documents list.' },
                    { name: 'Mobile / Biometric Slot Booking', url: 'https://appointments.uidai.gov.in/', desc: 'Book appointment at nearest Aadhaar Seva Kendra.' },
                    { name: 'Find Aadhaar Centre', url: 'https://appointments.uidai.gov.in/easeose/locatecenter.aspx', desc: 'Locate authorized Aadhaar centers near Goreakothi.' },
                    { name: 'Virtual ID (VID) Generator', url: 'https://myaadhaar.uidai.gov.in/myaadhaar/generate-vid', desc: 'Generate 16-digit Virtual ID for safe authentication.' }
                ]
            },
            {
                id: 'pan',
                title: 'PAN Card & Income Tax',
                icon: 'fa-file-invoice-dollar',
                color: '#9d4edd',
                desc: 'Apply PAN card, PAN-Aadhaar linking & Income Tax e-Filing.',
                services: [
                    { name: 'Apply New PAN Card (Protean)', url: 'https://www.protean-tinpan.com/', desc: 'Online NSDL/Protean PAN card application portal.' },
                    { name: 'PAN Card Correction / Update', url: 'https://www.protean-tinpan.com/', desc: 'Update Name, DOB, Photo or Father Name in PAN.' },
                    { name: 'PAN Application Status', url: 'https://www.trackpan.utiitsl.com/PANONLINE/#forward', desc: 'Track acknowledgement status for PAN card.' },
                    { name: 'Link PAN with Aadhaar', url: 'https://www.incometax.gov.in/iec/foportal/', desc: 'Mandatory PAN-Aadhaar linking official portal.' },
                    { name: 'Income Tax e-Filing Portal', url: 'https://www.incometax.gov.in/', desc: 'Official portal for ITR filing & tax services.' }
                ]
            },
            {
                id: 'scholarship',
                title: 'Scholarship Services',
                icon: 'fa-graduation-cap',
                color: '#ff007f',
                desc: 'National & Bihar state scholarship portals.',
                services: [
                    { name: 'National Scholarship Portal (NSP)', url: 'https://scholarships.gov.in/', desc: 'Central government pre-matric & post-matric schemes.' },
                    { name: 'Bihar Post Matric Scholarship', url: 'https://pmsonline.bihar.gov.in/', desc: 'BC, EBC, SC & ST Post Matric scholarship Bihar.' },
                    { name: 'MedhaSoft Bihar', url: 'https://medhasoft.bihar.gov.in/', desc: 'DBT school scholarship entry & status portal.' },
                    { name: 'Bihar e-Kalyan Portal', url: 'https://ekalyan.bihar.gov.in/', desc: 'Kanya Utthan & educational incentive schemes.' }
                ]
            },
            {
                id: 'jpu',
                title: 'JPU University Services',
                icon: 'fa-university',
                color: '#00e5ff',
                desc: 'Jai Prakash University Chapra admissions, exams & notices.',
                services: [
                    { name: 'JPU Official Website', url: 'https://www.jpv.ac.in/', desc: 'Main portal of Jai Prakash University, Chapra.' },
                    { name: 'JPU Admission Portal', url: 'https://jpvadm.samarth.edu.in/', desc: 'UG / PG online admission application and merit list.' },
                    { name: 'Examination Forms & Notices', url: 'https://www.jpv.ac.in/', desc: 'Online submission of semester exam forms.' },
                    { name: 'Admit Card Downloads', url: 'https://jpvadm.samarth.edu.in/', desc: 'Download exam admit cards for university courses.' },
                    { name: 'JPU Results & Notifications', url: 'https://www.jpv.ac.in/', desc: 'Check UG/PG examination results & circulars.' }
                ]
            },
            {
                id: 'bihar_gov',
                title: 'Bihar Government & RTPS',
                icon: 'fa-building-columns',
                color: '#ffc107',
                desc: 'Caste, Income, Residence certificates, Bihar Bhumi & Ration Card.',
                services: [
                    { name: 'RTPS Bihar Portal', url: 'https://serviceonline.bihar.gov.in/', desc: 'Right to Public Services portal for certificates.' },
                    { name: 'Caste Certificate (Jati)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for Category/Caste Certificate.' },
                    { name: 'Income Certificate (Aaya)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for annual Income Certificate.' },
                    { name: 'Residence Certificate (Niwas)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for Domicile/Residence proof.' },
                    { name: 'EWS & Non-Creamy Layer (NCL)', url: 'https://serviceonline.bihar.gov.in/', desc: 'EWS and OBC/EBC Non-Creamy Layer issuance.' },
                    { name: 'Bihar Bhumi Land Records', url: 'https://biharbhumi.bihar.gov.in/', desc: 'Khatian, Jamabandi, LPC & Online Lagan payment.' },
                    { name: 'Ration Card Services (epds)', url: 'https://epds.bihar.gov.in/', desc: 'Apply online for new Ration Card or modification.' },
                    { name: 'Birth & Death Registration (CRS)', url: 'https://crsorgi.gov.in/', desc: 'Civil Registration System portal for certificates.' },
                    { name: 'Bihar Character Certificate', url: 'https://homeonline.bihar.gov.in/', desc: 'Online Police Verification / Character certificate portal.' }
                ]
            },
            {
                id: 'jobs',
                title: 'Govt Jobs & Recruitment',
                icon: 'fa-briefcase',
                color: '#00e676',
                desc: 'SSC, UPSC, BPSC, BSSC, Railway & Bihar Police forms.',
                services: [
                    { name: 'SSC Portal', url: 'https://ssc.gov.in/', desc: 'Staff Selection Commission - CGL, CHSL, MTS, GD.' },
                    { name: 'UPSC Portal', url: 'https://www.upsc.gov.in/', desc: 'Union Public Service Commission recruitment portal.' },
                    { name: 'BPSC Portal', url: 'https://bpsc.bihar.gov.in/', desc: 'Bihar Public Service Commission exam portal.' },
                    { name: 'BSSC Portal', url: 'https://bssc.bihar.gov.in/', desc: 'Bihar Staff Selection Commission CGL & Inter Level.' },
                    { name: 'BTSC Portal', url: 'https://btsc.bihar.gov.in/', desc: 'Bihar Technical Service Commission recruitment.' },
                    { name: 'Bihar Police Recruitment', url: 'https://police.bihar.gov.in/', desc: 'Constable & Sub Inspector recruitment portal.' },
                    { name: 'India Post GDS Online', url: 'https://indiapostgdsonline.gov.in/', desc: 'Gramin Dak Sevak recruitment portal.' },
                    { name: 'Railway Recruitment (RRB)', url: 'https://www.rrbcdg.gov.in/', desc: 'NTPC, Group D, ALP & Technician portal.' },
                    { name: 'National Career Service (NCS)', url: 'https://www.ncs.gov.in/', desc: 'Government employment exchange registration.' }
                ]
            },
            {
                id: 'education',
                title: 'Education & Admissions',
                icon: 'fa-book-bookmark',
                color: '#ff9100',
                desc: 'Bihar OFSS, CBSE, IGNOU, NIOS & Student Credit Card.',
                services: [
                    { name: 'Bihar OFSS Intermediate', url: 'https://ofssbihar.net/', desc: 'Online Facilitation System for 11th admissions.' },
                    { name: 'CBSE Official Portal', url: 'https://www.cbse.gov.in/', desc: 'Central Board board results & notifications.' },
                    { name: 'IGNOU Portal', url: 'https://www.ignou.ac.in/', desc: 'Distance learning admissions & assignments.' },
                    { name: 'NIOS Open School Portal', url: 'https://nios.ac.in/', desc: 'National Institute of Open Schooling admissions.' },
                    { name: 'National Testing Agency (NTA)', url: 'https://nta.ac.in/', desc: 'JEE Main, NEET UG & CUET exam portal.' },
                    { name: 'Academic Bank of Credits (ABC)', url: 'https://www.abc.gov.in/', desc: 'Create DigiLocker ABC ID for students.' },
                    { name: 'Bihar Student Credit Card', url: 'https://www.7nishchay-yuvaupmission.bihar.gov.in/', desc: 'MNSSBY loan scheme up to Rs 4 Lakhs.' }
                ]
            },
            {
                id: 'identity',
                title: 'Passport & Voter Services',
                icon: 'fa-passport',
                color: '#e040fb',
                desc: 'Passport Seva, Voter ID portal & DigiLocker.',
                services: [
                    { name: 'Passport Seva Portal', url: 'https://www.passportindia.gov.in/', desc: 'Apply online for Fresh Passport or Renewal.' },
                    { name: 'Voter Service Portal', url: 'https://voters.eci.gov.in/', desc: 'Apply new Voter ID (Form 6) & correction.' },
                    { name: 'DigiLocker Portal', url: 'https://www.digilocker.gov.in/', desc: 'Access verified government digital documents.' }
                ]
            },
            {
                id: 'transport',
                title: 'Railway & Transport',
                icon: 'fa-train-subway',
                color: '#00b0ff',
                desc: 'IRCTC train booking, Parivahan DL & e-Challan.',
                services: [
                    { name: 'IRCTC Rail Connect', url: 'https://www.irctc.co.in/', desc: 'Official train ticket booking & PNR status.' },
                    { name: 'Parivahan Sewa Portal', url: 'https://parivahan.gov.in/', desc: 'Ministry of Road Transport official portal.' },
                    { name: 'Driving Licence Services', url: 'https://parivahan.gov.in/', desc: 'Learner License application & renewal.' },
                    { name: 'Vehicle RC Status', url: 'https://parivahan.gov.in/', desc: 'RC status, Transfer of ownership & tax.' },
                    { name: 'e-Challan Payment', url: 'https://echallan.parivahan.nic.in/', desc: 'Check and pay traffic e-challan online.' }
                ]
            },
            {
                id: 'rural',
                title: 'Farmer & Rural Schemes',
                icon: 'fa-wheat-awn',
                color: '#76ff03',
                desc: 'PM-Kisan, MGNREGA & PMAY Gramin.',
                services: [
                    { name: 'PM-Kisan Portal', url: 'https://pmkisan.gov.in/', desc: 'Farmer e-KYC, status & new registration.' },
                    { name: 'MGNREGA Portal', url: 'https://nrega.nic.in/', desc: 'Job card download & payment status.' },
                    { name: 'PMAY-Gramin Portal', url: 'https://pmayg.nic.in/', desc: 'Awaas Yojana rural beneficiary status.' },
                    { name: 'Jal Jeevan Mission', url: 'https://jaljeevanmission.gov.in/', desc: 'Har Ghar Jal progress reports & info.' }
                ]
            },
            {
                id: 'health',
                title: 'Health, Labour & Pension',
                icon: 'fa-heart-pulse',
                color: '#ff5252',
                desc: 'Ayushman Card (5 Lakh), e-Shram & EPFO.',
                services: [
                    { name: 'Ayushman Beneficiary Portal', url: 'https://beneficiary.nha.gov.in/', desc: 'Create & download 5 Lakh Health Card.' },
                    { name: 'e-Shram Portal', url: 'https://eshram.gov.in/', desc: 'Unorganized worker registration card.' },
                    { name: 'EPFO Member Portal', url: 'https://www.epfindia.gov.in/', desc: 'Check PF balance passbook & online claim.' },
                    { name: 'NSAP Pension Portal', url: 'https://nsap.nic.in/', desc: 'Old age, widow & disability pension status.' },
                    { name: 'Bihar Labour Department', url: 'https://state.bihar.gov.in/labour/', desc: 'BOCW Labour card registration portal.' }
                ]
            },
            {
                id: 'business',
                title: 'Business Registrations',
                icon: 'fa-store',
                color: '#ffd700',
                desc: 'Udyam MSME, GST & FSSAI Food License.',
                services: [
                    { name: 'Udyam Registration', url: 'https://udyamregistration.gov.in/', desc: 'Free online MSME Udyog Aadhaar portal.' },
                    { name: 'GST Portal', url: 'https://www.gst.gov.in/', desc: 'GST registration and return filing portal.' },
                    { name: 'FSSAI FoSCoS Portal', url: 'https://foscos.fssai.gov.in/', desc: 'Food license & hygiene registration for shops.' },
                    { name: 'CSC Digital Seva', url: 'https://digitalseva.csc.gov.in/', desc: 'Common Services Centre operator VLE login.' }
                ]
            },
            {
                id: 'tools',
                title: 'PDF, Photo & Utilities',
                icon: 'fa-wand-magic-sparkles',
                color: '#69f0ae',
                desc: 'PDF tools, photo background removal & Canva.',
                services: [
                    { name: 'PDF24 Tools', url: 'https://tools.pdf24.org/', desc: 'Free browser-based PDF converter & editor.' },
                    { name: 'iLovePDF', url: 'https://www.ilovepdf.com/', desc: 'Merge, split, compress & convert PDFs.' },
                    { name: 'Smallpdf', url: 'https://smallpdf.com/', desc: 'Compress PDF file size for online forms.' },
                    { name: 'Remove.bg', url: 'https://www.remove.bg/', desc: 'Automatic photo background remover.' },
                    { name: 'Canva Design', url: 'https://www.canva.com/', desc: 'Create posters, banners & visiting cards.' },
                    { name: 'Google Translate', url: 'https://translate.google.com/', desc: 'Translate Hindi <-> English text and documents.' }
                ]
            },
            {
                id: 'legal',
                title: 'Electricity Bill & Utility',
                icon: 'fa-scale-balanced',
                color: '#ff80ab',
                desc: 'NBPDCL Electricity bill pay & grievances.',
                services: [
                    { name: 'NBPDCL Electricity Bill', url: 'https://www.nbpdcl.co.in/', desc: 'North Bihar Power Distribution bill pay (Siwan).' },
                    { name: 'SBPDCL Electricity Bill', url: 'https://www.sbpdcl.co.in/', desc: 'South Bihar Power Distribution bill pay.' },
                    { name: 'RTI Online Portal', url: 'https://rtionline.gov.in/', desc: 'File Right to Information applications.' },
                    { name: 'CPGRAMS Public Grievance', url: 'https://pgportal.gov.in/', desc: 'Lodge complaints to government departments.' },
                    { name: 'Skill India Digital', url: 'https://www.skillindiadigital.gov.in/', desc: 'Skill development courses & PMKVY certificates.' }
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

        // Render Services with Official Link Button
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
                const card = document.createElement('div');
                card.className = 'card service-card';
                card.onclick = () => window.open(srv.url, '_blank', 'noopener,noreferrer');
                card.innerHTML = `
                    <div class="card-header">
                        <div class="card-icon" style="color: ${color || 'var(--neon-blue)'}">
                            <i class="fa-solid ${defaultIcon || 'fa-globe'}"></i>
                        </div>
                        <div>
                            <div class="card-title" style="font-size:1.05rem;">${srv.name}</div>
                        </div>
                    </div>
                    <div class="card-desc">${srv.desc}</div>
                    <a href="${srv.url}" target="_blank" rel="noopener noreferrer" class="service-link-btn" onclick="event.stopPropagation();">
                        <span>Open Official Website</span>
                        <i class="fa-solid fa-arrow-up-right-from-square"></i>
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
