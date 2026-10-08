<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>सोनू साइबर - ऑनलाइन सेवाएँ</title>
    <style>
        :root {
            --bg-color: #f0f2f5;
            --primary-gradient: linear-gradient(135deg, #FF9800 0%, #F57C00 100%);
            --secondary-gradient: linear-gradient(135deg, #26A69A 0%, #00897B 100%);
            --accent-gradient: linear-gradient(135deg, #29B6F6 0%, #039BE5 100%);
            --fourth-gradient: linear-gradient(135deg, #AB47BC 0%, #8E24AA 100%);
            --card-bg: #FFFFFF;
            --text-color: #333333;
            --white: #FFFFFF;
            --shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--bg-color);
            color: var(--text-color);
        }

        header {
            background: #1e293b;
            color: var(--white);
            padding: 30px 20px;
            text-align: center;
            box-shadow: var(--shadow);
            border-bottom: 5px solid #FF9800;
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        header .address {
            font-size: 0.9rem;
            margin-top: 10px;
            color: #94a3b8;
        }

        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            height: 250px;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .card-header {
            padding: 40px 20px;
            color: var(--white);
            text-align: center;
            font-size: 1.5rem;
            font-weight: 600;
            flex-grow: 1;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .card-1 { background: var(--primary-gradient); }
        .card-2 { background: var(--secondary-gradient); }
        .card-3 { background: var(--accent-gradient); }
        .card-4 { background: var(--fourth-gradient); }

        .sub-menu {
            display: none;
            background: var(--white);
            padding: 20px;
            border-top: 1px solid #e0e0e0;
            flex-direction: column;
            gap: 10px;
            max-height: 200px;
            overflow-y: auto;
        }

        .sub-menu.active {
            display: flex;
        }

        .sub-menu a {
            background: #f8f9fa;
            padding: 12px 15px;
            border-radius: 10px;
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: background 0.2s ease, color 0.2s ease;
            text-align: center;
            border: 1px solid #e9ecef;
        }

        .sub-menu a:hover {
            background: #FF9800;
            color: var(--white);
            border-color: #FF9800;
        }

        .whatsapp-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25D366;
            color: var(--white);
            padding: 20px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4);
            transition: transform 0.3s ease;
            z-index: 1000;
        }

        .whatsapp-btn:hover {
            transform: scale(1.05);
        }

        .whatsapp-btn img {
            width: 25px;
            height: 25px;
        }

        footer {
            text-align: center;
            padding: 40px;
            color: #64748b;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            header h1 { font-size: 1.8rem; }
            .card { height: auto; }
        }
    </style>
</head>
<body>

    <header>
        <h1>सोनू साइबर</h1>
        <div class="address">कॉलेज रोड, गोरिया कोठी, सिवान, बिहार 841434</div>
    </header>

    <div class="container">
        <!-- Box 1 -->
        <div class="card" onclick="toggleMenu(1)">
            <div class="card-header card-1">व्यक्तिगत पहचान</div>
            <div class="sub-menu" id="menu-1">
                <a href="https://myaadhaar.uidai.gov.in/" target="_blank">आधार कार्ड डाउनलोड</a>
                <a href="https://www.onlineservices.nsdl.com/paam/endUserRegisterContactDetails.html" target="_blank">पैन कार्ड अप्लाई/सुधार</a>
                <a href="https://voters.eci.gov.in/" target="_blank">वोटर आईडी</a>
                <a href="https://www.passportindia.gov.in/" target="_blank">पासपोर्ट</a>
            </div>
        </div>

        <!-- Box 2 -->
        <div class="card" onclick="toggleMenu(2)">
            <div class="card-header card-2">सरकारी प्रमाण पत्र</div>
            <div class="sub-menu" id="menu-2">
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">जाति प्रमाण पत्र</a>
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">आय प्रमाण पत्र</a>
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">निवास प्रमाण पत्र</a>
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">NCL प्रमाण पत्र</a>
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">EWS प्रमाण पत्र</a>
                <a href="https://serviceonline.gov.in/bihar/" target="_blank">आचरण प्रमाण पत्र</a>
            </div>
        </div>

        <!-- Box 3 -->
        <div class="card" onclick="toggleMenu(3)">
            <div class="card-header card-3">शिक्षा और छात्रवृत्ति</div>
            <div class="sub-menu" id="menu-3">
                <a href="https://medhasoft.bih.nic.in/" target="_blank">मेधासॉफ्ट (स्कूल)</a>
                <a href="https://scholarships.gov.in/" target="_blank">नेशनल स्कॉलरशिप</a>
                <a href="https://pmsonline.bih.nic.in/" target="_blank">पोस्ट मैट्रिक स्कॉलरशिप</a>
            </div>
        </div>

        <!-- Box 4 -->
        <div class="card" onclick="toggleMenu(4)">
            <div class="card-header card-4">सरकारी नौकरियाँ</div>
            <div class="sub-menu" id="menu-4">
                <a href="https://www.sarkariresult.com/" target="_blank">सरकारी रिजल्ट</a>
                <a href="https://www.fastjobsearches.com/" target="_blank">फास्ट जॉब</a>
            </div>
        </div>
    </div>

    <a href="https://wa.me/918227002020?text=नमस्ते, मुझे मदद चाहिए।" class="whatsapp-btn" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
        Get Help
    </a>

    <footer>
        <p>&copy; 2026 सोनू साइबर। सभी अधिकार सुरक्षित।</p>
    </footer>

    <script>
        function toggleMenu(cardNumber) {
            const menu = document.getElementById(`menu-${cardNumber}`);
            const allMenus = document.querySelectorAll('.sub-menu');
            
            // Close all other menus
            allMenus.forEach(m => {
                if (m !== menu) m.classList.remove('active');
            });
            
            // Toggle the clicked menu
            menu.classList.toggle('active');
        }
    </script>

</body>
</html>
