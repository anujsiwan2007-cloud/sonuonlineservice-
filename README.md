<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sonu Cyber Goreakothi - Digital Service Portal</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary: #1e3c72;
            --secondary: #2a5298;
            --accent: #ff9800;
            --light-bg: #f4f7f6;
            --dark: #333333;
            --card-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        body {
            background-color: var(--light-bg);
            color: var(--dark);
        }

        /* Top Bar */
        .top-bar {
            background: var(--dark);
            color: #ffffff;
            padding: 8px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 13px;
        }

        .top-bar i {
            margin-right: 5px;
            color: var(--accent);
        }

        /* Navigation Header */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-container i {
            font-size: 32px;
            color: var(--accent);
        }

        .logo-text h1 {
            font-size: 20px;
            font-weight: 700;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .logo-text p {
            font-size: 12px;
            color: #d0e1fd;
        }

        /* Banner Hero Section */
        .hero {
            background: linear-gradient(rgba(30, 60, 114, 0.8), rgba(42, 82, 152, 0.85)), url('https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?auto=format&fit=crop&w=1200&q=80') center/cover;
            color: white;
            padding: 50px 20px;
            text-align: center;
        }

        .hero h2 {
            font-size: 28px;
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 15px;
            margin-bottom: 25px;
            color: #e0e6ed;
        }

        /* Search Input Box */
        .search-box {
            max-width: 550px;
            margin: 0 auto;
            position: relative;
        }

        .search-box input {
            width: 100%;
            padding: 14px 20px 14px 45px;
            border-radius: 30px;
            border: none;
            outline: none;
            font-size: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
        }

        .search-box i {
            position: absolute;
            left: 18px;
            top: 50%;
            transform: translateY(-50%);
            color: #777;
            font-size: 16px;
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 35px auto;
            padding: 0 20px;
        }

        .section-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .section-header h3 {
            font-size: 24px;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 8px;
        }

        .section-header h3::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 3px;
            background: var(--accent);
            bottom: 0;
            left: 20%;
            border-radius: 2px;
        }

        /* Services Grid Layout */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }

        .service-card {
            background: white;
            border-radius: 10px;
            padding: 22px 18px;
            text-align: center;
            box-shadow: var(--card-shadow);
            transition: all 0.3s ease;
            border: 1px solid #e1e8ed;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.12);
        }

        .icon-box {
            width: 60px;
            height: 60px;
            background: #eef4ff;
            color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 26px;
            margin: 0 auto 15px;
        }

        .service-card h4 {
            font-size: 17px;
            margin-bottom: 8px;
            color: var(--dark);
        }

        .service-card p {
            font-size: 13px;
            color: #666;
            margin-bottom: 18px;
        }

        .btn-link {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            padding: 9px 18px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 500;
            transition: background 0.3s ease;
        }

        .btn-link:hover {
            background-color: var(--secondary);
        }

        /* Address Box Section */
        .address-card {
            background: #ffffff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: var(--card-shadow);
            margin: 40px 0;
            display: flex;
            align-items: center;
            gap: 15px;
            border-left: 5px solid var(--accent);
        }

        .address-card i {
            font-size: 32px;
            color: var(--accent);
        }

        .address-card h4 {
            font-size: 18px;
            color: var(--primary);
        }

        .address-card p {
            font-size: 14px;
            color: #555;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: #aaaaaa;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            font-size: 13px;
        }

        footer strong {
            color: #ffffff;
        }

        @media (max-width: 600px) {
            .hero h2 {
                font-size: 22px;
            }
            .logo-text h1 {
                font-size: 16px;
            }
            .top-bar {
                flex-direction: column;
                gap: 5px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Top Announcement Bar -->
    <div class="top-bar">
        <div><i class="fa-solid fa-store"></i> Digital & Online Services Center</div>
        <div><i class="fa-solid fa-location-dot"></i> Goreakothi, Siwan (Bihar)</div>
    </div>

    <!-- Header Section -->
    <header>
        <div class="logo-container">
            <i class="fa-solid fa-laptop-code"></i>
            <div class="logo-text">
                <h1>Sonu Cyber</h1>
                <p>Goreakothi Online Services</p>
            </div>
        </div>
    </header>

    <!-- Hero Banner -->
    <section class="hero">
        <h2>Sonu Cyber Goreakothi</h2>
        <p>Sabhi prakar ke online va digital karya yahan kiye jaate hain.</p>
        
        <div class="search-box">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" id="searchInput" onkeyup="filterServices()" placeholder="Service search karein (e.g. Aadhar, PAN, Form, Voter)...">
        </div>
    </section>

    <!-- Main Content Container -->
    <main class="container">
        <div class="section-header">
            <h3>Hamari Digital Services</h3>
        </div>

        <div class="services-grid" id="servicesGrid">
            
            <!-- Service 1 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-id-card"></i></div>
                    <h4>Aadhar Card Services</h4>
                    <p>Aadhar download, PVC Card order aur Aadhar updates.</p>
                </div>
                <a href="https://myaadhaar.uidai.gov.in" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 2 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-address-card"></i></div>
                    <h4>PAN Card Services</h4>
                    <p>Naya PAN Card apply karein, correction aur e-PAN download.</p>
                </div>
                <a href="https://www.onlineservices.nsdl.com/paam/endUserRegisterContact.html" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 3 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-check-to-slot"></i></div>
                    <h4>Voter ID Services</h4>
                    <p>Naya Voter Card apply karein, status check aur download.</p>
                </div>
                <a href="https://voters.eci.gov.in" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 4 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-graduation-cap"></i></div>
                    <h4>Sarkari Online Form</h4>
                    <p>Sabhi sarkari naukri, admit card aur result form online bharein.</p>
                </div>
                <a href="https://www.sarkariresult.com" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 5 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-user-graduate"></i></div>
                    <h4>Scholarship Form</h4>
                    <p>PMS Bihar, Medhasoft aur post matric scholarship form.</p>
                </div>
                <a href="https://pmsonline.bih.nic.in" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 6 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-file-invoice"></i></div>
                    <h4>RTPS Bihar Services</h4>
                    <p>Jati, Aaya, Niwas praman patra aur Ration Card services.</p>
                </div>
                <a href="https://serviceonline.bihar.gov.in" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 7 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-wallet"></i></div>
                    <h4>EPFO & Pension Portal</h4>
                    <p>PF withdrawal, EPFO passbook check, KYC aur pension form.</p>
                </div>
                <a href="https://unifiedportal-mem.epfindia.gov.in/memberinterface/" target="_blank" class="btn-link">Open Official Link</a>
            </div>

            <!-- Service 8 -->
            <div class="service-card">
                <div>
                    <div class="icon-box"><i class="fa-solid fa-car-side"></i></div>
                    <h4>Parivahan Services</h4>
                    <p>Driving License, Learner License aur Vehicle Registration.</p>
                </div>
                <a href="
