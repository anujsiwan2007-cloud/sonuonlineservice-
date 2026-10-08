<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>सोनू साइबर</title>
    <style>
        :root {
            --primary: #ff9800;
            --secondary: #253342;
            --accent: #00e676;
            --light: #f4f4f4;
            --dark: #333;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light);
            color: var(--dark);
        }

        header {
            background-color: var(--secondary);
            color: white;
            padding: 20px 0;
            text-align: center;
        }

        .contact-info {
            font-size: 0.9em;
            margin-top: 5px;
        }

        nav {
            background-color: var(--primary);
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        .dropdown {
            position: relative;
            display: inline-block;
            margin: 0 15px;
        }

        .dropbtn {
            background-color: inherit;
            color: white;
            padding: 10px;
            font-size: 16px;
            border: none;
            cursor: pointer;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: white;
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            right: 0;
        }

        .dropdown-content a {
            color: var(--dark);
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            text-align: right;
        }

        .dropdown-content a:hover {
            background-color: #ddd;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        main {
            padding: 20px;
            text-align: center;
        }

        .whatsapp-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: var(--accent);
            color: var(--secondary);
            padding: 15px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
            font-size: 1.1em;
        }

        .whatsapp-icon {
            margin-right: 10px;
            width: 24px;
            height: 24px;
        }

        footer {
            background-color: var(--secondary);
            color: white;
            text-align: center;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

    <header>
        <h1>सोनू साइबर</h1>
        <div class="contact-info">
            कॉलेज रोड, गोरिया कोठी, सिवान, बिहार 841434
        </div>
    </header>

    <nav>
        <div class="dropdown">
            <button class="dropbtn">व्यक्तिगत पहचान</button>
            <div class="dropdown-content">
                <a href="#aadhar">आधार</a>
                <a href="#pan">पैन कार्ड</a>
                <a href="#voter">वोटर आईडी</a>
                <a href="#passport">पासपोर्ट</a>
            </div>
        </div>

        <div class="dropdown">
            <button class="dropbtn">सरकारी प्रमाण पत्र</button>
            <div class="dropdown-content">
                <a href="#jati">जाति प्रमाण पत्र</a>
                <a href="#aay">आय प्रमाण पत्र</a>
                <a href="#niwas">निवास प्रमाण पत्र</a>
                <a href="#ncl">NCL</a>
                <a href="#ews">EWS</a>
                <a href="#charitra">आचरण प्रमाण पत्र</a>
            </div>
        </div>

        <div class="dropdown">
            <button class="dropbtn">शिक्षा और छात्रवृत्ति</button>
            <div class="dropdown-content">
                <a href="#school">स्कूल फॉर्म</a>
                <a href="#scholarship">छात्रवृत्ति</a>
            </div>
        </div>

        <div class="dropdown">
            <button class="dropbtn">सरकारी नौकरियाँ</button>
            <div class="dropdown-content">
                <a href="#jobs">नौकरी के फॉर्म</a>
                <a href="#results">सरकारी रिजल्ट</a>
            </div>
        </div>
    </nav>

    <main>
        <h2>ऑनलाइन सेवाओं के लिए हमसे संपर्क करें</h2>
        <p>ऊपर दी गई किसी भी सेवा के लिए नीचे दिए गए बटन पर क्लिक करके मदद लें।</p>
    </main>

    <a href="https://wa.me/918227002020?text=नमस्ते, मुझे मदद चाहिए।" class="whatsapp-btn" target="_blank">
        Get Help
    </a>

    <footer>
        <p>&copy; 2026 सोनू साइबर। सभी अधिकार सुरक्षित।</p>
    </footer>

</body>
</html>
