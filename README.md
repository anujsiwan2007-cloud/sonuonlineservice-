<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SONU DIGITAL SERVICE | Goreakothi</title>

<style>
:root{
  --primary:#6c5ce7;
  --blue:#0984e3;
  --green:#00b894;
  --pink:#e84393;
  --orange:#fd9644;
  --dark:#17152f;
  --bg:#f5f6ff;
  --white:#fff;
  --text:#19192b;
  --muted:#6d6d80;
  --shadow:0 10px 30px rgba(35,30,90,.12);
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:Arial,Helvetica,sans-serif;
  background:linear-gradient(135deg,#f7f7ff,#eefaff);
  color:var(--text);
}

a{
  text-decoration:none;
  color:inherit;
}

/* HEADER */

header{
  position:sticky;
  top:0;
  z-index:999;
  background:rgba(255,255,255,.92);
  backdrop-filter:blur(15px);
  border-bottom:1px solid #eee;
}

.nav{
  max-width:1200px;
  margin:auto;
  padding:12px 18px;
  display:flex;
  align-items:center;
  gap:20px;
}

.logo{
  display:flex;
  align-items:center;
  gap:10px;
  font-size:20px;
  font-weight:900;
  color:var(--primary);
  white-space:nowrap;
}

.logo-icon{
  width:44px;
  height:44px;
  border-radius:14px;
  display:grid;
  place-items:center;
  color:white;
  font-weight:bold;
  background:linear-gradient(135deg,#6c5ce7,#0984e3);
  box-shadow:0 7px 20px #6c5ce755;
}

.nav-menu{
  margin-left:auto;
  display:flex;
  gap:6px;
  flex-wrap:wrap;
}

.nav-menu a{
  padding:10px 12px;
  border-radius:12px;
  font-size:14px;
  font-weight:bold;
}

.nav-menu a:hover{
  background:#eeeaff;
  color:var(--primary);
}

.menu-btn{
  display:none;
  margin-left:auto;
  border:0;
  padding:10px 13px;
  border-radius:12px;
  background:#eeeaff;
  font-size:20px;
}

/* HERO */

.hero{
  max-width:1200px;
  margin:28px auto;
  padding:0 18px;
}

.hero-box{
  padding:45px 32px;
  border-radius:30px;
  color:white;
  background:
  radial-gradient(circle at 85% 15%,#00b89466,transparent 30%),
  radial-gradient(circle at 10% 90%,#e8439366,transparent 30%),
  linear-gradient(135deg,#29215e,#6c5ce7,#0984e3);
  box-shadow:var(--shadow);
}

.badges{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
}

.badge{
  padding:8px 13px;
  border-radius:30px;
  background:#ffffff20;
  border:1px solid #ffffff40;
  font-size:13px;
  font-weight:bold;
}

.hero h1{
  font-size:clamp(36px,6vw,65px);
  line-height:1;
  margin-top:18px;
}

.hero p{
  max-width:720px;
  margin:18px 0;
  font-size:17px;
  line-height:1.6;
}

.buttons{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:13px 18px;
  border-radius:14px;
  font-weight:bold;
}

.btn-white{
  background:white;
  color:#4939bd;
}

.btn-transparent{
  color:white;
  border:1px solid #ffffff55;
  background:#ffffff18;
}

/* MAIN */

.container{
  max-width:1200px;
  margin:auto;
  padding:0 18px 60px;
}

/* SEARCH */

.search-area{
  margin:20px 0 30px;
}

.search{
  width:100%;
  border:1px solid #e2e2f0;
  background:white;
  border-radius:16px;
  padding:16px;
  outline:none;
  font-size:16px;
  box-shadow:0 5px 20px #312e8110;
}

.search:focus{
  border-color:var(--primary);
}

/* SECTION */

.section{
  margin-top:35px;
  scroll-margin-top:90px;
}

.section-title{
  margin-bottom:17px;
}

.section-title h2{
  font-size:27px;
}

.section-title p{
  color:var(--muted);
  margin-top:5px;
  font-size:14px;
}

/* CARDS */

.grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
}

.card{
  position:relative;
  overflow:hidden;
  background:white;
  border:1px solid #e9e9f2;
  border-radius:22px;
  padding:19px;
  box-shadow:0 7px 22px rgba(39,32,96,.07);
  transition:.25s;
}

.card:hover{
  transform:translateY(-5px);
  box-shadow:var(--shadow);
}

.card::before{
  content:"";
  position:absolute;
  left:0;
  top:0;
  width:5px;
  height:100%;
  background:var(--accent);
}

.icon{
  width:50px;
  height:50px;
  border-radius:15px;
  display:grid;
  place-items:center;
  font-size:25px;
  margin-bottom:13px;
  background:#f0efff;
}

.card h3{
  font-size:17px;
  margin-bottom:7px;
}

.card p{
  color:var(--muted);
  font-size:13px;
  line-height:1.5;
  min-height:40px;
}

.open-btn{
  display:inline-block;
  margin-top:14px;
  padding:10px 13px;
  border-radius:12px;
  background:#f0efff;
  color:#4c3fc0;
  font-size:13px;
  font-weight:bold;
}

.open-btn:hover{
  background:var(--primary);
  color:white;
}

/* COLORS */

.aadhaar{--accent:#6c5ce7}
.pan{--accent:#0984e3}
.gov{--accent:#00b894}
.edu{--accent:#e84393}
.print{--accent:#fd9644}

.aadhaar .icon{background:#eeeaff}
.pan .icon{background:#eaf6ff}
.gov .icon{background:#eafff8}
.edu .icon{background:#fff0f8}
.print .icon{background:#fff5e8}

/* NOTICE */

.notice{
  margin-top:30px;
  padding:20px;
  border-radius:20px;
  background:white;
  border:1px solid #e6e6f0;
  box-shadow:var(--shadow);
}

.notice strong{
  display:block;
  margin-bottom:7px;
}

.notice p{
  color:var(--muted);
  font-size:13px;
  line-height:1.6;
}

/* CONTACT */

.contact-box{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:18px;
}

.contact-card{
  background:white;
  border-radius:24px;
  padding:25px;
  border:1px solid #e7e7f0;
  box-shadow:var(--shadow);
}

.contact-card h3{
  font-size:23px;
  margin-bottom:8px;
}

.contact-card p{
  color:var(--muted);
  line-height:1.6;
}

.contact-buttons{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  margin-top:18px;
}

.whatsapp{
  background:#16a34a;
  color:white;
}

.call{
  background:#0984e3;
  color:white;
}

.map{
  background:#e84393;
  color:white;
}

.admin{
  background:#17152f;
  color:white;
}

/* FOOTER */

footer{
  background:#17152f;
  color:white;
  padding:30px 18px;
}

.footer{
  max-width:1200px;
  margin:auto;
  display:flex;
  justify-content:space-between;
  flex-wrap:wrap;
  gap:15px;
}

.footer p{
  color:#c7c5d9;
  font-size:13px;
  margin-top:5px;
}

/* TOP BUTTON */

.top{
  position:fixed;
  right:18px;
  bottom:18px;
  width:45px;
  height:45px;
  border:0;
  border-radius:14px;
  background:var(--primary);
  color:white;
  font-size:20px;
  cursor:pointer;
  display:none;
}

/* MOBILE */

@media(max-width:950px){

  .grid{
    grid-template-columns:repeat(2,1fr);
  }

  .contact-box{
    grid-template-columns:1fr;
  }

}

@media(max-width:650px){

  .nav-menu{
    display:none;
    position:absolute;
    left:12px;
    right:12px;
    top:68px;
    padding:10px;
    background:white;
    border-radius:18px;
    box-shadow:var(--shadow);
  }

  .nav-menu.open{
    display:grid;
    grid-template-columns:1fr 1fr;
  }

  .menu-btn{
    display:block;
  }

  .hero-box{
    padding:32px 21px;
  }

  .hero p{
    font-size:15px;
  }

  .grid{
    grid-template-columns:1fr 1fr;
    gap:10px;
  }

  .card{
    padding:15px;
    border-radius:18px;
  }

  .card h3{
    font-size:15px;
  }

  .card p{
    font-size:12px;
  }

  .open-btn{
    font-size:12px;
    padding:9px 10px;
  }

}

@media(max-width:390px){

  .grid{
    grid-template-columns:1fr;
  }

  .nav-menu.open{
    grid-template-columns:1fr;
  }

}
</style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header>

<nav class="nav">

<a href="#home" class="logo">
<span class="logo-icon">SD</span>
SONU DIGITAL SERVICE
</a>

<button class="menu-btn" onclick="toggleMenu()">☰</button>

<div class="nav-menu" id="navMenu">

<a href="#home">🏠 Home</a>
<a href="#aadhaar">🪪 Aadhaar</a>
<a href="#pan">💳 PAN</a>
<a href="#government">📄 Govt.</a>
<a href="#education">🎓 Education</a>
<a href="#printing">🖨️ Printing</a>
<a href="#contact">📞 Contact</a>

</div>

</nav>

</header>


<!-- ================= HERO ================= -->

<section class="hero" id="home">

<div class="hero-box">

<div class="badges">

<span class="badge">⚡ Fast Service</span>
<span class="badge">🔗 Official Portals</span>
<span class="badge">📱 Mobile Friendly</span>

</div>

<h1>
SONU DIGITAL<br>
SERVICE
</h1>

<p>
Aadhaar, PAN, Bihar Government, Education,
Printing and Digital Services — all in one place.
Select your required service and continue to the
official portal.
</p>

<div class="buttons">

<a class="btn btn-white" href="#aadhaar">
Explore Services →
</a>

<a class="btn btn-transparent"
href="https://sonu-digital-service.github.io/Chandan-digital-service/"
target="_blank">
Main Portal ↗
</a>

</div>

</div>

</section>


<main class="container">


<!-- SEARCH -->

<div class="search-area">

<input
type="text"
id="search"
class="search"
placeholder="🔎 Search service... Aadhaar, PAN, Caste, Scholarship..."
>

</div>


<!-- ================= AADHAAR ================= -->

<section class="section" id="aadhaar">

<div class="section-title">
<h2>🪪 Aadhaar Services</h2>
<p>Official UIDAI services</p>
</div>

<div class="grid">

<div class="card aadhaar service">
<div class="icon">🆕</div>
<h3>New Aadhaar</h3>
<p>Find an official Aadhaar enrolment centre.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/enrolment-update"
target="_blank">
Open Official ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">📥</div>
<h3>Aadhaar Download</h3>
<p>Download your e-Aadhaar from UIDAI.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/genricDownloadAadhaar/en"
target="_blank">
Download ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">🔎</div>
<h3>Aadhaar Status</h3>
<p>Check Aadhaar enrolment or update status.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/CheckAadhaarStatus/en"
target="_blank">
Check Status ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">✏️</div>
<h3>Aadhaar Update</h3>
<p>Access official Aadhaar update services.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/"
target="_blank">
Update ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">💳</div>
<h3>PVC Card</h3>
<p>Order Aadhaar PVC card online.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/genricPVC/en"
target="_blank">
Order PVC ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">✅</div>
<h3>Verify Aadhaar</h3>
<p>Verify Aadhaar number through UIDAI.</p>
<a class="open-btn"
href="https://myaadhaar.uidai.gov.in/verifyAadhaar"
target="_blank">
Verify ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">📅</div>
<h3>Appointment</h3>
<p>Book an Aadhaar Seva Kendra appointment.</p>
<a class="open-btn"
href="https://bookappointment.uidai.gov.in/"
target="_blank">
Book Now ↗
</a>
</div>


<div class="card aadhaar service">
<div class="icon">📍</div>
<h3>Find Aadhaar Centre</h3>
<p>Locate Aadhaar enrolment/update centres.</p>
<a class="open-btn"
href="https://bhuvan-app3.nrsc.gov.in/aadhaar/"
target="_blank">
Find Centre ↗
</a>
</div>

</div>

</section>


<!-- ================= PAN ================= -->

<section class="section" id="pan">

<div class="section-title">
<h2>💳 PAN Card Services</h2>
<p>Official Income Tax services</p>
</div>

<div class="grid">

<div class="card pan service">

<div class="icon">🆕</div>

<h3>New PAN / e-PAN</h3>

<p>
Access official PAN services.
</p>

<a class="open-btn"
href="https://www.incometax.gov.in/iec/foportal/"
target="_blank">

Open Official ↗

</a>

</div>


<div class="card pan service">

<div class="icon">✏️</div>

<h3>PAN Correction</h3>

<p>
PAN related correction services.
</p>

<a class="open-btn"
href="https://www.incometax.gov.in/iec/foportal/pre-login-services"
target="_blank">

Open Service ↗

</a>

</div>


<div class="card pan service">

<div class="icon">📥</div>

<h3>e-PAN</h3>

<p>
Access e-PAN related services.
</p>

<a class="open-btn"
href="https://www.incometax.gov.in/iec/foportal/"
target="_blank">

Open e-PAN ↗

</a>

</div>


<div class="card pan service">

<div class="icon">🔎</div>

<h3>PAN Verify</h3>

<p>
Verify PAN through official services.
</p>

<a class="open-btn"
href="https://www.incometax.gov.in/iec/foportal/help/all-topics/e-filing-services/verify-your-pan"
target="_blank">

Verify ↗

</a>

</div>

</div>

</section>


<!-- ================= GOVERNMENT ================= -->

<section class="section" id="government">

<div class="section-title">

<h2>📄 Government Services</h2>

<p>
Bihar ServicePlus / RTPS
</p>

</div>

<div class="grid">


<div class="card gov service">

<div class="icon">🏛️</div>

<h3>RTPS</h3>

<p>
Bihar official ServicePlus portal.
</p>

<a class="open-btn"
href="https://serviceonline.bihar.gov.in/"
target="_blank">

Open RTPS ↗

</a>

</div>


<div class="card gov service">

<div class="icon">📜</div>

<h3>Caste Certificate</h3>

<p>
Apply for caste certificate.
</p>

<a class="open-btn"
href="https://serviceonline.bihar.gov.in/"
target="_blank">

Apply ↗

</a>

</div>


<div class="card gov service">

<div class="icon">💰</div>

<h3>Income Certificate</h3>

<p>
Apply for income certificate.
</p>

<a class="open-btn"
href="https://serviceonline.bihar.gov.in/"
target="_blank">

Apply ↗

</a>

</div>


<div class="card gov service">

<div class="icon">🏠</div>

<h3>Residence Certificate</h3>

<p>
Apply for residence certificate.
</p>

<a class="open-btn"
href="https://serviceonline.bihar.gov.in/"
target="_blank">

Apply ↗

</a>

</div>


<div class="card gov service">

<div class="icon">📑</div>

<h3>NCL / EWS / Other</h3>

<p>
Other Bihar government services.
</p>

<a class="open-btn"
href="https://serviceonline.bihar.gov.in/"
target="_blank">

View Services ↗

</a>

</div>

</div>

</section>


<!-- ================= EDUCATION ================= -->

<section class="section" id="education">

<div class="section-title">

<h2>🎓 Education Services</h2>

<p>
Student portals and education services
</p>

</div>

<div class="grid">


<div class="card edu service">

<div class="icon">🎓</div>

<h3>Scholarship</h3>

<p>
Bihar Post Matric Scholarship.
</p>

<a class="open-btn"
href="https://pmsonline.bihar.gov.in/"
target="_blank">

Open PMS ↗

</a>

</div>


<div class="card edu service">

<div class="icon">📝</div>

<h3>Admission Form</h3>

<p>
Access education resources.
</p>

<a class="open-btn"
href="https://www.education.gov.in/"
target="_blank">

Open ↗

</a>

</div>


<div class="card edu service">

<div class="icon">📚</div>

<h3>Exam Form</h3>

<p>
Access official education resources.
</p>

<a class="open-btn"
href="https://www.education.gov.in/"
target="_blank">

Open ↗

</a>

</div>


<div class="card edu service">

<div class="icon">🏆</div>

<h3>Result</h3>

<p>
Find official education resources.
</p>

<a class="open-btn"
href="https://www.education.gov.in/"
target="_blank">

Open ↗

</a>

</div>

</div>

</section>


<!-- ================= PRINTING ================= -->

<section class="section" id="printing">

<div class="section-title">

<h2>🖨️ Printing Services</h2>

<p>
SONU DIGITAL SERVICE local services
</p>

</div>

<div class="grid">


<div class="card print service">

<div class="icon">📸</div>

<h3>Photo</h3>

<p>
Passport photo and photo printing.
</p>

<a class="open-btn"
href="#contact">

Contact ↗

</a>

</div>


<div class="card print service">

<div class="icon">🖨️</div>

<h3>Print</h3>

<p>
Document and colour/B&W printing.
</p>

<a class="open-btn"
href="#contact">

Contact ↗

</a>

</div>


<div class="card print service">

<div class="icon">📄</div>

<h3>Scan</h3>

<p>
Document scanning service.
</p>

<a class="open-btn"
href="#contact">

Contact ↗

</a>

</div>


<div class="card print service">

<div class="icon">🪪</div>

<h3>Lamination</h3>

<p>
Document and card lamination.
</p>

<a class="open-btn"
href="#contact">

Contact ↗

</a>

</div>

</div>

</section>


<!-- ================= NOTICE ================= -->

<div class="notice">

<strong>
🔐 Important Information
</strong>

<p>
SONU DIGITAL SERVICE is a service-navigation website.
Government applications, OTP authentication and approvals
are handled on the respective official portals.
Never share your OTP, password or confidential credentials
with anyone unnecessarily.
</p>

</div>


<!-- ================= CONTACT ================= -->

<section class="section" id="contact">

<div class="section-title">

<h2>📞 Contact</h2>

<p>
SONU DIGITAL SERVICE · Goreakothi, Siwan, Bihar
</p>

</div>


<div class="contact-box">


<div class="contact-card">

<h3>
Need help with an online service?
</h3>

<p>
Contact SONU DIGITAL SERVICE for online forms,
printing, scanning, photographs and assistance
with official portals.
</p>


<div class="contact-buttons">

<a class="btn whatsapp"
href="https://wa.me/918227002020"
target="_blank">

💬 WhatsApp

</a>


<a class="btn call"
href="tel:+918227002020">

📞 Call

</a>


<a class="btn map"
href="https://www.google.com/maps/search/?api=1&query=Goreakothi%2C%20Siwan%2C%20Bihar"
target="_blank">

📍 Google Maps

</a>

</div>

</div>


<div class="contact-card">

<h3>
🔐 Admin Panel
</h3>

<p>
Private admin panel URL can be connected here
after creating a secure backend.
</p>

<div class="contact-buttons">

<a class="btn admin"
href="#"
onclick="adminMessage();return false;">

Open Admin ↗

</a>

</div>

</div>

</div>

</section>

</main>


<!-- ================= FOOTER ================= -->

<footer>

<div class="footer">

<div>

<strong>
SONU DIGITAL SERVICE
</strong>

<p>
Fast • Simple • Official Portal Access
</p>

</div>


<div>

<p>
© 2026 Sonu Digital Service
</p>

</div>

</div>

</footer>


<button class="top"
id="topButton"
onclick="window.scrollTo({top:0,behavior:'smooth'})">

↑

</button>


<script>

/* MOBILE MENU */

function toggleMenu(){

const menu=document.getElementById("navMenu");

menu.classList.toggle("open");

}


/* SEARCH */

const search=document.getElementById("search");

search.addEventListener("input",function(){

const value=this.value.toLowerCase();

const cards=document.querySelectorAll(".service");

cards.forEach(function(card){

const text=card.innerText.toLowerCase();

if(text.includes(value)){

card.style.display="block";

}else{

card.style.display="none";

}

});

});


/* ADMIN */

function adminMessage(){

alert(
"Admin Panel is not configured yet. Replace this button link with your private admin URL."
);

}


/* TOP BUTTON */

window.addEventListener("scroll",function(){

const button=document.getElementById("topButton");

if(window.scrollY>400){

button.style.display="block";

}else{

button.style.display="none";

}

});

</script>

</body>
</html>
