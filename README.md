<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sonu Digital Service</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:linear-gradient(135deg,#eef2ff,#fdf2f8,#ecfeff);
    color:#172033;
}

/* HEADER */
header{
    background:linear-gradient(135deg,#4f46e5,#7c3aed,#db2777);
    color:white;
    padding:25px 15px;
    text-align:center;
    box-shadow:0 5px 20px #0003;
}

header h1{
    font-size:30px;
    font-weight:800;
}

header p{
    margin-top:7px;
    font-size:14px;
}

/* NAVIGATION */
nav{
    background:white;
    padding:12px;
    display:flex;
    justify-content:center;
    gap:10px;
    flex-wrap:wrap;
    position:sticky;
    top:0;
    z-index:100;
    box-shadow:0 3px 12px #0002;
}

nav a{
    text-decoration:none;
    color:#4f46e5;
    font-weight:bold;
    padding:9px 15px;
    border-radius:20px;
}

nav a:hover{
    background:#4f46e5;
    color:white;
}

/* HERO */
.hero{
    margin:20px auto;
    max-width:1100px;
    padding:35px 20px;
    border-radius:25px;
    text-align:center;
    background:linear-gradient(135deg,#06b6d4,#2563eb,#7c3aed);
    color:white;
    box-shadow:0 10px 30px #0003;
}

.hero h2{
    font-size:28px;
    margin-bottom:10px;
}

.hero p{
    font-size:15px;
}

/* SECTION */
.container{
    max-width:1100px;
    margin:auto;
    padding:10px 15px 40px;
}

.section-title{
    margin:30px 0 15px;
    font-size:23px;
    font-weight:800;
}

/* SERVICE GRID */
.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:18px;
}

/* CARD */
.card{
    background:white;
    border-radius:20px;
    padding:20px;
    box-shadow:0 7px 20px #0002;
    border:1px solid #ffffff;
    transition:.3s;
    position:relative;
    overflow:hidden;
}

.card:hover{
    transform:translateY(-7px);
    box-shadow:0 15px 30px #0003;
}

.card::before{
    content:"";
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:5px;
    background:linear-gradient(90deg,#06b6d4,#6366f1,#ec4899);
}

.icon{
    font-size:38px;
    margin-bottom:10px;
}

.card h3{
    font-size:18px;
    margin-bottom:8px;
}

.card p{
    color:#64748b;
    font-size:13px;
    min-height:38px;
}

.btn{
    display:block;
    text-align:center;
    text-decoration:none;
    color:white;
    margin-top:15px;
    padding:11px;
    border-radius:12px;
    font-weight:bold;
    background:linear-gradient(135deg,#4f46e5,#7c3aed);
}

.btn:hover{
    background:linear-gradient(135deg,#db2777,#ef4444);
}

/* CONTACT */
.contact{
    margin-top:30px;
    padding:25px;
    border-radius:20px;
    background:white;
    text-align:center;
    box-shadow:0 7px 20px #0002;
}

.contact a{
    display:inline-block;
    margin:8px;
    padding:11px 18px;
    border-radius:12px;
    color:white;
    background:#16a34a;
    text-decoration:none;
    font-weight:bold;
}

/* FOOTER */
footer{
    background:#111827;
    color:white;
    text-align:center;
    padding:25px 10px;
    margin-top:30px;
}

footer p{
    margin:5px;
    font-size:13px;
}

/* MOBILE */
@media(max-width:600px){
    header h1{
        font-size:23px;
    }

    .hero h2{
        font-size:22px;
    }

    .grid{
        grid-template-columns:1fr 1fr;
        gap:12px;
    }

    .card{
        padding:15px;
    }

    .icon{
        font-size:30px;
    }

    .card h3{
        font-size:15px;
    }
}
</style>
</head>

<body>

<header>
    <h1>🌐 SONU DIGITAL SERVICE</h1>
    <p>Fast • Secure • Digital Online Services</p>
</header>

<nav>
    <a href="#home">🏠 Home</a>
    <a href="#aadhaar">🪪 Aadhaar</a>
    <a href="#pan">💳 PAN</a>
    <a href="#gov">📄 Government</a>
    <a href="#education">🎓 Education</a>
    <a href="#printing">🖨️ Printing</a>
    <a href="#contact">📞 Contact</a>
</nav>

<section class="hero" id="home">
    <h2>Digital Services At One Place</h2>
    <p>Select any service below and open its dedicated official website.</p>
</section>

<div class="container">

<!-- AADHAAR -->
<h2 class="section-title" id="aadhaar">🪪 Aadhaar Services</h2>

<div class="grid">

<div class="card">
<div class="icon">🆕</div>
<h3>New Aadhaar</h3>
<p>Aadhaar enrolment information</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📥</div>
<h3>Aadhaar Download</h3>
<p>Download your e-Aadhaar</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">🔎</div>
<h3>Aadhaar Status</h3>
<p>Check Aadhaar enrolment/update status</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">✏️</div>
<h3>Aadhaar Update</h3>
<p>Update Aadhaar details</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">💳</div>
<h3>PVC Card</h3>
<p>Order Aadhaar PVC card</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">✅</div>
<h3>Verify Aadhaar</h3>
<p>Verify Aadhaar number</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📅</div>
<h3>Appointment</h3>
<p>Book Aadhaar appointment</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

</div>


<!-- PAN -->
<h2 class="section-title" id="pan">💳 PAN Card Services</h2>

<div class="grid">

<div class="card">
<div class="icon">🪪</div>
<h3>New PAN</h3>
<p>Apply for a new PAN card</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">✏️</div>
<h3>PAN Correction</h3>
<p>Update PAN details</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📲</div>
<h3>e-PAN</h3>
<p>Access e-PAN related service</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">🔍</div>
<h3>PAN Status</h3>
<p>Check PAN application status</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

</div>


<!-- GOVERNMENT -->
<h2 class="section-title" id="gov">📄 Government Services</h2>

<div class="grid">

<div class="card">
<div class="icon">🏛️</div>
<h3>RTPS</h3>
<p>Bihar online public services</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📜</div>
<h3>Caste Certificate</h3>
<p>Apply/check caste certificate service</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">💰</div>
<h3>Income Certificate</h3>
<p>Income certificate service</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">🏠</div>
<h3>Residence Certificate</h3>
<p>Residence certificate service</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

</div>


<!-- EDUCATION -->
<h2 class="section-title" id="education">🎓 Education Services</h2>

<div class="grid">

<div class="card">
<div class="icon">🎓</div>
<h3>Scholarship</h3>
<p>Scholarship application services</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📝</div>
<h3>Admission Form</h3>
<p>Online admission services</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">📋</div>
<h3>Exam Form</h3>
<p>Online examination forms</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

<div class="card">
<div class="icon">🏆</div>
<h3>Result</h3>
<p>Check examination results</p>
<a class="btn" href="OFFICIAL_LINK_HERE" target="_blank">Open Service ↗</a>
</div>

</div>


<!-- PRINTING -->
<h2 class="section-title" id="printing">🖨️ Printing Services</h2>

<div class="grid">

<div class="card">
<div class="icon">📸</div>
<h3>Photo</h3>
<p>Passport size photo service</p>
<a class="btn" href="#contact">Contact Us</a>
</div>

<div class="card">
<div class="icon">🖨️</div>
<h3>Print</h3>
<p>Colour and black & white printing</p>
<a class="btn" href="#contact">Contact Us</a>
</div>

<div class="card">
<div class="icon">📄</div>
<h3>Scan</h3>
<p>Document scanning service</p>
<a class="btn" href="#contact">Contact Us</a>
</div>

<div class="card">
<div class="icon">📚</div>
<h3>Lamination</h3>
<p>Document lamination service</p>
<a class="btn" href="#contact">Contact Us</a>
</div>

</div>


<!-- CONTACT -->
<div class="contact" id="contact">
<h2>📞 Contact sonu Digital Service</h2>
<p>For online & offline digital services</p>

<a href="tel:+918227002020">📞 Call Now</a>
<a href="https://wa.me/918227002020" target="_blank">💬 WhatsApp</a>
</div>

</div>

<footer>
<p>© 2026 sonu Digital Service</p>
<p>Fast • Secure • Reliable Digital Services</p>
</footer>

</body>
</html>
