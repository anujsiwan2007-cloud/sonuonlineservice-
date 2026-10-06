<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SONU CYBER - Online Service Centre</title>
    <!-- Google Fonts & Font Awesome Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-color: #0d47a1;
            --secondary-color: #1565c0;
            --accent-color: #ff9800;
            --bg-color: #f4f6f9;
            --card-bg: #ffffff;
            --text-color: #333333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* Header & Banner Section */
        header {
            background: linear-gradient(135deg, #0d47a1, #1e88e5);
            color: white;
            padding: 20px 15px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        header h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        header p {
            font-size: 1rem;
            opacity: 0.9;
        }

        /* Main Container */
        .container {
            max-width: 1000px;
            margin: 20px auto;
            padding: 0 15px;
        }

        /* Notice Board */
        .notice-board {
            background: #fff3cd;
            border-left: 5px solid #ffc107;
            padding: 12px 15px;
            border-radius: 6px;
            margin-bottom: 25px;
            font-weight: 600;
            color: #856404;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Step Wizard Container */
        .wizard-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            margin-bottom: 30px;
        }

        .step-title {
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--primary-color);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 2px solid #e0e0e0;
            padding-bottom: 10px;
        }

        /* Category Grid */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }

        .category-btn {
            background: #f8f9fa;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            color: #495057;
        }

        .category-btn i {
            font-size: 2rem;
            color: var(--secondary-color);
        }

        .category-btn:hover, .category-btn.active {
            background: var(--secondary-color);
            color: white;
            border-color: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: 0 4px 12px rgba(21, 101, 192, 0.3);
        }

        .category-btn:hover i, .category-btn.active i {
            color: white;
        }

        /* Sub-Services List */
        .service-list {
            display: none;
            flex-direction: column;
            gap: 10px;
            margin-top: 15px;
        }

        .service-list.active {
            display: flex;
        }

        .service-item {
            background: #ffffff;
            border: 1px solid #dee2e6;
            padding: 12px 20px;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background 0.2s;
        }

        .service-item:hover {
            background: #e3f2fd;
        }

        .service-link {
            background: var(--accent-color);
            color: white;
            padding: 8px 16px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: background 0.2s;
        }

        .service-link:hover {
            background: #e68a00;
        }

        /* Back Button */
        .back-btn {
            display: inline-block;
            margin-bottom: 15px;
            color: var(--secondary-color);
            cursor: pointer;
            font-weight: 600;
        }

        /* Contact Section */
        .contact-card {
            background: linear-gradient(135deg, #1e88e5, #0d47a1);
            color: white;
            border-radius: 12px;
            padding: 25px;
            text-align: center;
        }

        .contact-card h2 {
            margin-bottom: 15px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.1rem;
        }

        .contact-item a {
            color: #ffeb3b;
            text-decoration: none;
            font-weight: 700;
        }

        footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            color: #6c757d;
            font-size: 0.9rem;
        }

        /* Hidden Class */
        .hidden {
            display: none !important;
        }
    </style>
</head>
<body>

    <!-- Header Banner -->
    <header>
        <h1>SONU CYBER</h1>
        <p>Online Service Centre & Digital Portal</p>
    </header>

    <div class="container">
        <!-- Notice Board -->
        <div class="notice-board">
            <i class="fa-solid fa-bullhorn"></i>
            <span>Welcome to SONU CYBER! Select any government service below to access official direct links.</span>
        </div>

        <!-- Wizard Navigation Container -->
        <div class="wizard-card">
            
            <!-- STEP 1: Select Main Category -->
            <div id="step-1">
                <div class="step-title">
                    <i class="fa-solid fa-list-check"></i>
                    <span>Step 1: Choose Service Category</span>
                </div>
                <div class="grid-container">
                    <div class="category-btn" onclick="showSubCategory('identity')">
                        <i class="fa-solid fa-id-card"></i>
                        <span>Identity Services</span>
                    </div>
                    <div class="category-btn" onclick="showSubCategory('rtps')">
                        <i class="fa-solid fa-file-invoice"></i>
                        <span>RTPS Services</span>
                    </div>
                    <div class="category-btn" onclick="showSubCategory('education')">
                        <i class="fa-solid fa-graduation-cap"></i>
                        <span>Education & Jobs</span>
                    </div>
                    <div class="category-btn" onclick="showSubCategory('travel')">
                        <i class="fa-solid fa-plane"></i>
                        <span>Travel & Booking</span>
                    </div>
                </div>
            </div>

            <!-- STEP 2: Select Sub-Service -->
            <div id="step-2" class="hidden">
                <span class="back-btn" onclick="goBackToStep1()"><i class="fa-solid fa-arrow-left"></i> Change Category</span>
                <div class="step-title">
                    <i class="fa-solid fa-circle-check"></i>
                    <span>Step 2: Select Official Link</span>
                </div>

                <!-- Identity Sub-Services -->
                <div id="identity-list" class="service-list">
                    <div class="service-item">
                        <span>Aadhaar Download / Status</span>
                        <a href="https://myaadhaar.uidai.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                    <div class="service-item">
                        <span>New PAN Card / Correction</span>
                        <a href="https://www.onlineservices.nsdl.com/paam/endUserRegisterContact.html" target="_blank" class="service-link">Open Link</a>
                    </div>
                    <div class="service-item">
                        <span>Voter ID Card Portal</span>
                        <a href="https://voters.eci.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                </div>

                <!-- RTPS Sub-Services -->
                <div id="rtps-list" class="service-list">
                    <div class="service-item">
                        <span>RTPS Bihar (Income, Caste, Residence)</span>
                        <a href="https://serviceonline.bihar.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                    <div class="service-item">
                        <span>Ration Card Portal Bihar</span>
                        <a href="http://epds.bihar.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                </div>

                <!-- Education Sub-Services -->
                <div id="education-list" class="service-list">
                    <div class="service-item">
                        <span>Sarkari Result Direct Portal</span>
                        <a href="https://www.sarkariresult.com/" target="_blank" class="service-link">Open Link</a>
                    </div>
                    <div class="service-item">
                        <span>PM Scholarship Portal</span>
                        <a href="https://scholarships.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                </div>

                <!-- Travel Sub-Services -->
                <div id="travel-list" class="service-list">
                    <div class="service-item">
                        <span>IRCTC Train Ticket Booking</span>
                        <a href="https://www.irctc.co.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                    <div class="service-item">
                        <span>Passport Seva Portal</span>
                        <a href="https://www.passportindia.gov.in/" target="_blank" class="service-link">Open Link</a>
                    </div>
                </div>

            </div>

        </div>

        <!-- Contact Section -->
        <div class="contact-card">
            <h2>Contact SONU CYBER</h2>
            <p>Visit our offline store or call for instant support</p>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fa-solid fa-phone"></i>
                    <span>Phone: <a href="tel:8227002020">8227002020</a></span>
                </div>
                <div class="contact-item">
                    <i class="fa-solid fa-location-dot"></i>
                    <span>College Road, Goreakothi, Siwan, Bihar - 841434</span>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 SONU CYBER. All Rights Reserved.</p>
    </footer>

    <!-- Interactive JavaScript -->
    <script>
        function showSubCategory(categoryId) {
            document.getElementById('step-1').classList.add('hidden');
            document.getElementById('step-2').classList.remove('hidden');

            // Hide all sub-lists
            const lists = document.querySelectorAll('.service-list');
            lists.forEach(list => list.classList.remove('active'));

            // Show selected sub-list
            const selectedList = document.getElementById(categoryId + '-list');
            if (selectedList) {
                selectedList.classList.add('active');
            }
        }

        function goBackToStep1() {
            document.getElementById('step-2').classList.add('hidden');
            document.getElementById('step-1').classList.remove('hidden');
        }
    </script>
</body>
</html>
