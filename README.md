<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SONU CYBER ONLINE SERVICE PORTAL | Sonu Cyber Goreakothi</title>
    <meta name="description" content="Fast, Safe & Smart Digital Services Portal - Sonu Cyber Goreakothi, College Road, Goreakothi, Siwan, Bihar.">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #080c1a;
            --bg-card: rgba(16, 24, 48, 0.75);
            --bg-card-hover: rgba(28, 40, 78, 0.85);
            --neon-blue: #00f0ff;
            --neon-purple: #9d4edd;
            --neon-pink: #ff007f;
            --neon-cyan: #00e5ff;
            --text-main: #f0f4f8;
            --text-sub: #a0aec0;
            --border-glow: rgba(0, 240, 255, 0.3);
            --shadow-glow: 0 8px 32px 0 rgba(0, 240, 255, 0.15);
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
                radial-gradient(circle at 15% 15%, rgba(157, 78, 221, 0.15) 0%, transparent 40%),
                radial-gradient(circle at 85% 85%, rgba(0, 240, 255, 0.15) 0%, transparent 40%),
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
            background: rgba(8, 12, 26, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-glow);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 1rem 2rem;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
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
            filter: drop-shadow(0 0 8px rgba(0, 240, 255, 0.5));
        }

        .brand-text h1 {
            font-size: 1.4rem;
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
            font-weight: 700;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 10px rgba(157, 78, 221, 0.3);
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
            background: rgba(16, 24, 48, 0.9);
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
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.4);
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
            font-size: 0.9rem;
            color: var(--text-sub);
        }

        .breadcrumbs span.active {
            color: var(--neon-blue);
            font-weight: 600;
        }

        .btn-back {
            display: none;
            align-items: center;
            gap: 0.5rem;
            background: linear-gradient(135deg, rgba(157, 78, 221, 0.3), rgba(0, 240, 255, 0.3));
            border: 1px solid var(--neon-blue);
            color: #fff;
            padding: 0.5rem 1.2rem;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .btn-back:hover {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-blue));
            box-shadow: 0 0 12px rgba(0, 240, 255, 0.5);
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
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid rgba(255, 255, 255, 0.08);
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
            font-size: 1.1rem;
            font-weight: 600;
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
            padding: 0.6rem 1rem;
            background: rgba(0, 240, 255, 0.1);
            border: 1px solid var(--neon-blue);
            color: var(--neon-cyan);
            border-radius: 8px;
            text-align: center;
            font-size: 0.85rem;
            font-weight: 600;
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
            box-shadow: 0 0 10px rgba(0, 240, 255, 0.5);
        }

        /* Disclaimer Box */
        .disclaimer-box {
            background: rgba(255, 193, 7, 0.08);
            border: 1px solid rgba(255, 193, 7, 0.3);
            border-radius: 12px;
            padding: 1rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            color: #ffca28;
            font-size: 0.85rem;
        }

        .disclaimer-box i {
            font-size: 1.5rem;
            flex-shrink: 0;
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
            font-size: 0.85rem;
            color: var(--text-sub);
            flex-wrap: wrap;
            justify-content: center;
        }

        .footer-note {
            font-size: 0.75rem;
            color: #6c757d;
            max-width: 700px;
            line-height: 1.4;
        }

        /* Floating WhatsApp Button */
        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: linear-gradient(135deg, #25d366, #128c7e);
            color: white;
            border-radius: 50px;
            padding: 12px 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            font-weight: 700;
            font-size: 0.95rem;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            z-index: 1000;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .whatsapp-float:hover {
            transform: translateY(-4px) scale(1.05);
            box-shadow: 0 6px 25px rgba(37, 211, 102, 0.6);
            color: white;
        }

        .whatsapp-float i {
            font-size: 1.5rem;
        }

        /* Responsive Breakpoints */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                align-items: flex-start;
            }

            .hero h2 {
                font-size: 1.5rem;
            }

            .grid-container {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
                gap: 1rem;
            }

            .whatsapp-float span {
                display: inline;
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
        <h2>Smart Access to All Digital & Government Services</h2>
        <p>Find official government links, education portals, utilities, and online forms instantly.</p>
        <div class="search-box">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" id="searchInput" placeholder="Search service (e.g., Aadhaar, PAN, Scholarship, SSC)..." onkeyup="handleSearch()">
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
        <div id="disclaimerContainer"></div>
        <div class="grid-container" id="portalGrid">
            <!-- Categories or Services render here via JavaScript -->
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <span><strong>Sonu Cyber Goreakothi</strong></span> | 
                <span>Location: College Road, Goreakothi, Siwan, Bihar</span>
            </div>
            <p class="footer-note">
                <strong>Disclaimer:</strong> This website is an independent informational service directory maintained by Sonu Cyber Goreakothi. It is not affiliated with or endorsed by any government agency. All links point directly to official government and university portals.
            </p>
            <p style="font-size: 0.8rem; color: var(--text-sub);">&copy; 2026 SONU CYBER ONLINE SERVICE PORTAL. All rights reserved.</p>
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
        // Categories & Services Structured Data
        const portalData = [
            {
                id: 'aadhaar',
                title: 'Aadhaar Services',
                icon: 'fa-id-card',
                color: '#00f0ff',
                desc: 'UIDAI services, e-Aadhaar download, status check & information.',
                disclaimer: 'Note: Online updates are limited to demography as per UIDAI rules. Biometric & Mobile updates require visiting an Authorized Aadhaar Seva Kendra.',
                services: [
                    { name: 'UIDAI Official Website', url: 'https://uidai.gov.in/', desc: 'Official Unique Identification Authority of India Portal' },
                    { name: 'My Aadhaar Portal', url: 'https://myaadhaar.uidai.gov.in/', desc: 'Direct resident services portal for online Aadhaar tasks' },
                    { name: 'Download e-Aadhaar', url: 'https://myaadhaar.uidai.gov.in/genricDownloadAadhaar', desc: 'Download electronic password-protected Aadhaar PDF' },
                    { name: 'Aadhaar Status Check', url: 'https://myaadhaar.uidai.gov.in/CheckAadharStatus', desc: 'Check status of update requests or new enrollment' },
                    { name: 'Aadhaar Address Update', url: 'https://myaadhaar.uidai.gov.in/', desc: 'Update residential address online with valid proof' },
                    { name: 'Name Update Information', url: 'https://uidai.gov.in/', desc: 'Guidelines & proof documents required for Name change' },
                    { name: 'Date of Birth Update Info', url: 'https://uidai.gov.in/', desc: 'Rules & valid valid documents for DOB correction' },
                    { name: 'Mobile Number Update Info', url: 'https://uidai.gov.in/', desc: 'Information: Requires physical biometric visit at Kendra' },
                    { name: 'Book Aadhaar Appointment', url: 'https://appointments.uidai.gov.in/', desc: 'Book appointment slot at nearest official Aadhaar Kendra' },
                    { name: 'Find Aadhaar Centre', url: 'https://appointments.uidai.gov.in/easeose/locatecenter.aspx', desc: 'Locate authorized Aadhaar Kendra near Goreakothi/Siwan' },
                    { name: 'Verify Aadhaar', url: 'https://myaadhaar.uidai.gov.in/verifyAadhar', desc: 'Verify if an Aadhaar number is valid and active' },
                    { name: 'Virtual ID (VID) Generator', url: 'https://myaadhaar.uidai.gov.in/myaadhaar/generate-vid', desc: 'Generate 16-digit temporary Virtual ID for privacy' },
                    { name: 'Aadhaar Authentication History', url: 'https://myaadhaar.uidai.gov.in/auth-history', desc: 'View past authentication records for your Aadhaar' }
                ]
            },
            {
                id: 'pan',
                title: 'PAN Card & Income Tax',
                icon: 'fa-file-invoice-dollar',
                color: '#9d4edd',
                desc: 'Apply PAN, link Aadhaar-PAN, e-Filing & Income Tax services.',
                services: [
                    { name: 'Apply New PAN Card', url: 'https://www.protean-tinpan.com/', desc: 'Online application via Protean (NSDL) portal' },
                    { name: 'PAN Correction / Update', url: 'https://www.protean-tinpan.com/', desc: 'Request correction in Name, DOB, Photo or Father Name' },
                    { name: 'PAN Application Status', url: 'https://www.trackpan.utiitsl.com/PANONLINE/#forward', desc: 'Track acknowledgement status for PAN card delivery' },
                    { name: 'Instant e-PAN Information', url: 'https://www.incometax.gov.in/', desc: 'Instant free e-PAN issuance using Aadhaar e-KYC' },
                    { name: 'Link PAN with Aadhaar', url: 'https://www.incometax.gov.in/iec/foportal/', desc: 'Mandatory PAN-Aadhaar linkage portal' },
                    { name: 'Income Tax e-Filing Portal', url: 'https://www.incometax.gov.in/', desc: 'Official portal for ITR filing and tax compliance' }
                ]
            },
            {
                id: 'scholarship',
                title: 'Scholarship Services',
                icon: 'fa-graduation-cap',
                color: '#ff007f',
                desc: 'National & Bihar state scholarship portals and application tracking.',
                services: [
                    { name: 'National Scholarship Portal (NSP)', url: 'https://scholarships.gov.in/', desc: 'Central government pre-matric and post-matric schemes' },
                    { name: 'Bihar Post Matric Scholarship', url: 'https://pmsonline.bihar.gov.in/', desc: 'BC, EBC, SC & ST Post Matric scholarship portal Bihar' },
                    { name: 'MedhaSoft Bihar', url: 'https://medhasoft.bihar.gov.in/', desc: 'DBT school scholarship portal for Bihar school students' },
                    { name: 'Bihar e-Kalyan Portal', url: 'https://ekalyan.bihar.gov.in/', desc: 'Mukhyamantri Kanya Utthan and educational incentive schemes' },
                    { name: 'Scholarship Application Info', url: 'https://pmsonline.bihar.gov.in/', desc: 'Required documents list: Caste, Income, Marksheet, Bonafide' },
                    { name: 'Check Scholarship Status', url: 'https://pmsonline.bihar.gov.in/', desc: 'Track application approval status at college & district level' }
                ]
            },
            {
                id: 'jpu',
                title: 'JPU University Services',
                icon: 'fa-university',
                color: '#00e5ff',
                desc: 'Jai Prakash University Chapra admissions, exams & notices.',
                services: [
                    { name: 'JPU Official Website', url: 'https://www.jpv.ac.in/', desc: 'Main portal of Jai Prakash University, Chapra' },
                    { name: 'JPU Admission Portal', url: 'https://jpvadm.samarth.edu.in/', desc: 'UG / PG online admission application and merit list portal' },
                    { name: 'Examination Forms & Notices', url: 'https://www.jpv.ac.in/', desc: 'Online submission of semester and degree exam forms' },
                    { name: 'Semester Examination Info', url: 'https://www.jpv.ac.in/', desc: 'Schedules, exam center lists, and guidelines' },
                    { name: 'Admit Card Downloads', url: 'https://jpvadm.samarth.edu.in/', desc: 'Download exam admit cards for university courses' },
                    { name: 'Results & Notifications', url: 'https://www.jpv.ac.in/', desc: 'Check UG/PG examination results and official gazette' },
                    { name: 'Registration Information', url: 'https://jpvadm.samarth.edu.in/', desc: 'Student registration slips and verification updates' },
                    { name: 'College & University Notices', url: 'https://www.jpv.ac.in/', desc: 'Latest press releases, holiday lists, and circulars' }
                ]
            },
            {
                id: 'bihar_gov',
                title: 'Bihar Government Services',
                icon: 'fa-building-columns',
                color: '#ffc107',
                desc: 'RTPS certificates, Bihar Bhumi land records, Ration card & CRS.',
                services: [
                    { name: 'RTPS Bihar Portal', url: 'https://serviceonline.bihar.gov.in/', desc: 'Right to Public Services portal for government certificates' },
                    { name: 'Caste Certificate (Jati)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for Category/Caste Certificate' },
                    { name: 'Income Certificate (Aaya)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for annual Income Certificate' },
                    { name: 'Residence Certificate (Niwas)', url: 'https://serviceonline.bihar.gov.in/', desc: 'Online application for Domicile/Residence proof' },
                    { name: 'EWS & Non-Creamy Layer (NCL)', url: 'https://serviceonline.bihar.gov.in/', desc: 'EWS and OBC/EBC Non-Creamy Layer issuance' },
                    { name: 'Bihar Bhumi Land Records', url: 'https://biharbhumi.bihar.gov.in/', desc: 'Khatian, Jamabandi, LPC & Online Land Tax (Lagan)' },
                    { name: 'Ration Card Services (epds)', url: 'https://epds.bihar.gov.in/', desc: 'Apply online for new Ration Card or correction' },
                    { name: 'Birth & Death Registration', url: 'https://crsorgi.gov.in/', desc: 'Civil Registration System (CRS) portal for certificates' },
                    { name: 'Bihar Home Department', url: 'https://homeonline.bihar.gov.in/', desc: 'Online Character Certificate (Police Verification) portal' }
                ]
            },
            {
                id: 'jobs',
                title: 'Jobs & Recruitment',
                icon: 'fa-briefcase',
                color: '#00e676',
                desc: 'SSC, UPSC, BPSC, Railway, Bihar Police & GDS online forms.',
                services: [
                    { name: 'SSC Portal', url: 'https://ssc.gov.in/', desc: 'Staff Selection Commission - CGL, CHSL, MTS, GD' },
                    { name: 'UPSC Portal', url: 'https://www.upsc.gov.in/', desc: 'Union Public Service Commission civil services & exams' },
                    { name: 'BPSC Portal', url: 'https://bpsc.bihar.gov.in/', desc: 'Bihar Public Service Commission recruitment & notices' },
                    { name: 'BSSC Portal', url: 'https://bssc.bihar.gov.in/', desc: 'Bihar Staff Selection Commission CGL & Inter Level' },
                    { name: 'BTSC Portal', url: 'https://btsc.bihar.gov.in/', desc: 'Bihar Technical Service Commission specialist recruitment' },
                    { name: 'Bihar Police Recruitment', url: 'https://police.bihar.gov.in/', desc: 'CSBC and BPSSC constable & SI recruitment' },
                    { name: 'India Post GDS Online', url: 'https://indiapostgdsonline.gov.in/', desc: 'Gramin Dak Sevak online recruitment portal' },
                    { name: 'Railway Recruitment (RRB)', url: 'https://www.rrbcdg.gov.in/', desc: 'NTPC, Group D, ALP & Technician vacancy portal' },
                    { name: 'National Career Service (NCS)', url: 'https://www.ncs.gov.in/', desc: 'Government job search and employment exchange registration' }
                ]
            },
            {
                id: 'education',
                title: 'Education & Universities',
                icon: 'fa-book-bookmark',
                color: '#ff9100',
                desc: 'OFSS admission, CBSE, IGNOU, NIOS, NTA & Student Credit Card.',
                services: [
                    { name: 'Bihar OFSS Intermediate', url: 'https://ofssbihar.net/', desc: 'Online Facilitation System for 11th class admissions' },
                    { name: 'CBSE Official Portal', url: 'https://www.cbse.gov.in/', desc: 'Central Board of Secondary Education board results & notifications' },
                    { name: 'IGNOU Portal', url: 'https://www.ignou.ac.in/', desc: 'Distance learning admissions, assignment & re-registration' },
                    { name: 'NIOS Portal', url: 'https://nios.ac.in/', desc: 'National Institute of Open Schooling admissions & exams' },
                    { name: 'National Testing Agency (NTA)', url: 'https://nta.ac.in/', desc: 'JEE Main, NEET UG, CUET & UGC NET exam portal' },
                    { name: 'Academic Bank of Credits (ABC)', url: 'https://www.abc.gov.in/', desc: 'Create DigiLocker ABC ID for university credit transfers' },
                    { name: 'UGC Portal', url: 'https://www.ugc.gov.in/', desc: 'University Grants Commission higher education guidelines' },
                    { name: 'AICTE Portal', url: 'https://www.aicte-india.org/', desc: 'Technical education council scholarships & approvals' },
                    { name: 'Bihar Student Credit Card', url: 'https://www.7nishchay-yuvaupmission.bihar.gov.in/', desc: 'MNSSBY loan scheme up to Rs 4 Lakhs for higher studies' }
                ]
            },
            {
                id: 'identity',
                title: 'Identity & Passport',
                icon: 'fa-passport',
                color: '#e040fb',
                desc: 'Passport Seva, Voter ID portal & DigiLocker document storage.',
                services: [
                    { name: 'Passport Seva Portal', url: 'https://www.passportindia.gov.in/', desc: 'Apply online for Fresh Passport or Renewal' },
                    { name: 'Voter Service Portal', url: 'https://voters.eci.gov.in/', desc: 'Apply new Voter ID (Form 6), correction & download e-EPIC' },
                    { name: 'DigiLocker Portal', url: 'https://www.digilocker.gov.in/', desc: 'Access verified government digital documents safely' },
                    { name: 'Identity Document Info', url: 'https://voters.eci.gov.in/', desc: 'List of valid identity proofs required across portals' }
                ]
            },
            {
                id: 'transport',
                title: 'Railway & Transport',
                icon: 'fa-train-subway',
                color: '#00b0ff',
                desc: 'IRCTC train booking, Parivahan driving license & e-Challan.',
                services: [
                    { name: 'IRCTC Rail Connect', url: 'https://www.irctc.co.in/', desc: 'Official train ticket booking, Tatkal & PNR status' },
                    { name: 'Parivahan Sewa Portal', url: 'https://parivahan.gov.in/', desc: 'Ministry of Road Transport & Highways official services' },
                    { name: 'Driving Licence Services', url: 'https://parivahan.gov.in/', desc: 'Learner License application, Renewal & DL test booking' },
                    { name: 'Vehicle Registration (RC)', url: 'https://parivahan.gov.in/', desc: 'RC status, Transfer of ownership, Fitness & Tax payment' },
                    { name: 'e-Challan Payment', url: 'https://echallan.parivahan.nic.in/', desc: 'Check and pay traffic e-challan online' }
                ]
            },
            {
                id: 'rural',
                title: 'Farmer & Rural Schemes',
                icon: 'fa-wheat-awn',
                color: '#76ff03',
                desc: 'PM-Kisan Samman Nidhi, MGNREGA, PMAY Gramin & Jal Jeevan.',
                services: [
                    { name: 'PM-Kisan Portal', url: 'https://pmkisan.gov.in/', desc: 'Farmer e-KYC, beneficiary status & new registration' },
                    { name: 'MGNREGA Portal', url: 'https://nrega.nic.in/', desc: 'Job card download, worker payment status & muster rolls' },
                    { name: 'PMAY-Gramin Portal', url: 'https://pmayg.nic.in/', desc: 'Pradhan Mantri Awaas Yojana rural beneficiary status' },
                    { name: 'NRLM (Aajeevika)', url: 'https://nrlm.gov.in/', desc: 'National Rural Livelihood Mission & SHG self-help groups' },
                    { name: 'Jal Jeevan Mission', url: 'https://jaljeevanmission.gov.in/', desc: 'Har Ghar Jal progress reports & water supply scheme info' }
                ]
            },
            {
                id: 'health',
                title: 'Health, Labour & Pension',
                icon: 'fa-heart-pulse',
                color: '#ff5252',
                desc: 'Ayushman Card beneficiary, e-Shram, EPFO PF & NSAP Pension.',
                services: [
                    { name: 'Ayushman Beneficiary Portal', url: 'https://beneficiary.nha.gov.in/', desc: 'Create & Download Ayushman Bharat 5 Lakh Health Card' },
                    { name: 'e-Shram Portal', url: 'https://eshram.gov.in/', desc: 'Unorganized worker registration card download & update' },
                    { name: 'EPFO Member Portal', url: 'https://www.epfindia.gov.in/', desc: 'Check PF Balance Passbook, UAN activation & Online Claim' },
                    { name: 'NSAP Pension Services', url: 'https://nsap.nic.in/', desc: 'Old age, widow & disability pension status tracking' },
                    { name: 'Bihar Labour Department', url: 'https://state.bihar.gov.in/labour/', desc: 'BOCW Labour card registration & worker welfare schemes' },
                    { name: 'Shram Suvidha Portal', url: 'https://shramsuvidha.gov.in/', desc: 'Unified compliance labor identification number (LIN)' }
                ]
            },
            {
                id: 'business',
                title: 'Business & Registration',
                icon: 'fa-store',
                color: '#ffd700',
                desc: 'Udyam MSME, GST Portal, MCA, GeM & CSC Digital Seva.',
                services: [
                    { name: 'Udyam Registration', url: 'https://udyamregistration.gov.in/', desc: 'Free online MSME Udyog Aadhaar registration for business' },
                    { name: 'GST Portal', url: 'https://www.gst.gov.in/', desc: 'Goods & Services Tax registration and return filing' },
                    { name: 'MCA Services', url: 'https://www.mca.gov.in/', desc: 'Ministry of Corporate Affairs company & LLP filing' },
                    { name: 'Government e-Marketplace (GeM)', url: 'https://gem.gov.in/', desc: 'Government vendor seller registration & procurement' },
                    { name: 'FSSAI FoSCoS Portal', url: 'https://foscos.fssai.gov.in/', desc: 'Food license and hygiene registration for shops/hotels' },
                    { name: 'Startup India Portal', url: 'https://www.startupindia.gov.in/', desc: 'DPIIT recognition and startup support benefits' },
                    { name: 'CSC Digital Seva', url: 'https://digitalseva.csc.gov.in/', desc: 'Common Services Centre operator VLE login portal' }
                ]
            },
            {
                id: 'tools',
                title: 'PDF, Photo & Utility Tools',
                icon: 'fa-wand-magic-sparkles',
                color: '#69f0ae',
                desc: 'PDF conversion, image resize, background removal & Canva.',
                services: [
                    { name: 'PDF24 Tools', url: 'https://tools.pdf24.org/', desc: 'Free browser-based PDF converter, editor & unlocker' },
                    { name: 'iLovePDF', url: 'https://www.ilovepdf.com/', desc: 'Merge, split, compress & convert Office files to PDF' },
                    { name: 'Smallpdf', url: 'https://smallpdf.com/', desc: 'Compress PDF file size for government online forms' },
                    { name: 'Remove.bg', url: 'https://www.remove.bg/', desc: 'Automatic 100% free photo background remover' },
                    { name: 'Photopea Online Editor', url: 'https://www.photopea.com/', desc: 'Full Photoshop alternative inside web browser' },
                    { name: 'Canva Design', url: 'https://www.canva.com/', desc: 'Create posters, banners, visiting cards & thumbnails' },
                    { name: 'Google Translate', url: 'https://translate.google.com/', desc: 'Translate Hindi <-> English text and documents' },
                    { name: 'Google Drive', url: 'https://drive.google.com/', desc: 'Cloud storage to save scanned photos and certificates' }
                ]
            },
            {
                id: 'legal',
                title: 'Legal, RTI & Utility Services',
                icon: 'fa-scale-balanced',
                color: '#ff80ab',
                desc: 'RTI Online, eCourts, Electricity Bill Payment & Skill India.',
                services: [
                    { name: 'RTI Online Portal', url: 'https://rtionline.gov.in/', desc: 'File Right to Information applications to central ministries' },
                    { name: 'CPGRAMS Public Grievance', url: 'https://pgportal.gov.in/', desc: 'Lodge complaints directly to government departments' },
                    { name: 'National Consumer Helpline', url: 'https://consumerhelpline.gov.in/', desc: 'Lodge consumer fraud & product service complaints' },
                    { name: 'eCourts Services', url: 'https://services.ecourts.gov.in/ecourtindia_v6/', desc: 'Check court case status, cause list & orders online' },
                    { name: 'Bihar e-Procurement (eProc2)', url: 'https://eproc2.bihar.gov.in/EPSV2Web/', desc: 'Bihar government tenders and contractor portal' },
                    { name: 'UMANG Portal', url: 'https://web.umang.gov.in/', desc: 'Unified Mobile Application for New-age Governance' },
                    { name: 'SBPDCL Electricity Bill', url: 'https://www.sbpdcl.co.in/', desc: 'South Bihar Power Distribution bill pay & new connection' },
                    { name: 'NBPDCL Electricity Bill', url: 'https://www.nbpdcl.co.in/', desc: 'North Bihar Power Distribution bill pay (Siwan region)' },
                    { name: 'Apprenticeship India', url: 'https://www.apprenticeshipindia.gov.in/', desc: 'NAPS apprenticeship training portal for ITI & graduates' },
                    { name: 'Skill India Digital', url: 'https://www.skillindiadigital.gov.in/', desc: 'Skill development courses and PMKVY certificates' }
                ]
            }
        ];

        let currentCategoryId = null;

        // Initialize Page
        document.addEventListener('DOMContentLoaded', () => {
            showCategories();
        });

        // Step 1: Render All Category Cards
        function showCategories() {
            currentCategoryId = null;
            const grid = document.getElementById('portalGrid');
            const breadcrumbs = document.getElementById('breadcrumbs');
            const backBtn = document.getElementById('backBtn');
            const disclaimerContainer = document.getElementById('disclaimerContainer');
            const searchInput = document.getElementById('searchInput');

            searchInput.value = '';
            disclaimerContainer.innerHTML = '';
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

        // Step 2: Render Services under Selected Category
        function showServices(categoryId) {
            currentCategoryId = categoryId;
            const category = portalData.find(c => c.id === categoryId);
            if (!category) return;

            const grid = document.getElementById('portalGrid');
            const breadcrumbs = document.getElementById('breadcrumbs');
            const backBtn = document.getElementById('backBtn');
            const disclaimerContainer = document.getElementById('disclaimerContainer');
            const searchInput = document.getElementById('searchInput');

            searchInput.value = '';
            backBtn.style.display = 'inline-flex';
            breadcrumbs.innerHTML = `
                <span style="cursor:pointer;" onclick="showCategories()"><i class="fa-solid fa-house"></i> Home</span>
                <i class="fa-solid fa-chevron-right" style="font-size:0.7rem;"></i>
                <span class="active">${category.title}</span>
            `;

            // Disclaimer Box if present
            if (category.disclaimer) {
                disclaimerContainer.innerHTML = `
                    <div class="disclaimer-box">
                        <i class="fa-solid fa-triangle-exclamation"></i>
                        <div>${category.disclaimer}</div>
                    </div>
                `;
            } else {
                disclaimerContainer.innerHTML = '';
            }

            renderServiceList(category.services, category.color, category.icon);
        }

        function renderServiceList(services, color, defaultIcon) {
            const grid = document.getElementById('portalGrid');
            grid.innerHTML = '';

            if (services.length === 0) {
                grid.innerHTML = `
                    <div class="no-results">
                        <i class="fa-solid fa-circle-xmark"></i>
                        <h3>No matching services found</h3>
                        <p>Try searching with another keyword like "Aadhaar", "PAN", or "SSC".</p>
                    </div>
                `;
                return;
            }

            services.forEach(srv => {
                const card = document.createElement('div');
                card.className = 'card service-card';
                card.innerHTML = `
                    <div class="card-header">
                        <div class="card-icon" style="color: ${color || 'var(--neon-blue)'}">
                            <i class="fa-solid ${defaultIcon || 'fa-globe'}"></i>
                        </div>
                        <div>
                            <div class="card-title" style="font-size:1rem;">${srv.name}</div>
                        </div>
                    </div>
                    <div class="card-desc">${srv.desc}</div>
                    <a href="${srv.url}" target="_blank" rel="noopener noreferrer" class="service-link-btn" onclick="event.stopPropagation();">
                        <span>Open Official Website</span>
                        <i class="fa-solid fa-arrow-up-right-from-square"></i>
                    </a>
                `;
                // Clicking card also triggers external link
                card.onclick = () => window.open(srv.url, '_blank', 'noopener,noreferrer');
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

            // Search across ALL services in all categories if searching globally
            const backBtn = document.getElementById('backBtn');
            const breadcrumbs = document.getElementById('breadcrumbs');
            const disclaimerContainer = document.getElementById('disclaimerContainer');

            disclaimerContainer.innerHTML = '';
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
                            categoryTitle: cat.title,
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
