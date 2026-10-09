
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sonu Cyber Online Service Portal</title>
<style>
:root {
  --navy:#061735;
  --blue:#087cff;
  --cyan:#13d8ff;
  --green:#079b57;
  --light:#f1f7ff;
  --border:#d9e7f8;
}
*{box-sizing:border-box}
body{
  margin:0;
  font-family:Arial,Helvetica,sans-serif;
  color:#142b4c;
  background:var(--light);
}
button,input{font:inherit}
button{cursor:pointer}
.hero{
  color:white;
  min-height:360px;
  background:
    linear-gradient(90deg,rgba(3,13,37,.96),rgba(3,20,53,.75),rgba(3,20,53,.30)),
    url("https://images.unsplash.com/photo-1516321310764-8d8e2b1f7f20?auto=format&fit=crop&w=2000&q=85")
    center/cover no-repeat;
}
header{padding:20px 5%;display:flex;align-items:center;justify-content:space-between;gap:20px}
.brand{display:flex;align-items:center;gap:12px}
.logo{
  width:58px;height:58px;border-radius:17px;
  display:grid;place-items:center;font-size:32px;
  background:linear-gradient(135deg,#12e1ff,#075cff);
  box-shadow:0 0 24px #078cff88
}
.brand h1{font-size:clamp(20px,3vw,32px);margin:0}
.brand h1 span{color:#20ddff}
.brand small{display:block;letter-spacing:1px;margin-top:5px}
nav{display:flex;gap:8px;flex-wrap:wrap}
nav a{
  color:white;text-decoration:none;padding:11px 15px;
  background:#061735bb;border-radius:25px
}
nav a:hover{background:#087cff}
.hero-content{padding:20px 5% 65px;max-width:900px}
.hero-content h2{font-size:clamp(35px,5vw,60px);margin:0 0 12px}
.hero-content h2 span{color:#ffdc32}
.hero-content p{font-size:17px;line-height:1.6}
.search{display:flex;max-width:650px;background:white;padding:5px;border-radius:40px}
.search input{flex:1;min-width:0;border:0;outline:0;padding:12px 16px;border-radius:30px}
.search button{border:0;color:white;background:linear-gradient(90deg,#087cff,#04c6ef);padding:12px 22px;border-radius:30px;font-weight:bold}
.quick{
  margin:-22px auto 0;max-width:1450px;padding:0 20px;
  position:relative
}
.quick-inner{
  display:flex;gap:8px;overflow:auto;padding:12px;
  border-radius:17px;background:#061735;border:1px solid #18d8ff
}
.quick button{white-space:nowrap;border:0;border-radius:10px;background:#102b55;color:white;padding:11px 14px}
.quick button:hover{background:#087cff}
main{max-width:1450px;margin:28px auto;padding:0 20px}
.heading{margin-bottom:18px}
.heading h2{margin:0 0 6px;font-size:28px}
.heading p{color:#60738d;margin:0}
.layout{display:grid;grid-template-columns:270px minmax(0,1fr);gap:17px}
.panel{background:white;border:1px solid var(--border);border-radius:17px;overflow:hidden;box-shadow:0 7px 22px #123a7010}
.panel-title{padding:17px;border-bottom:1px solid var(--border);background:#f7fbff}
.panel-title h3{margin:0}
.panel-title p{margin:6px 0 0;font-size:13px;color:#667890}
.category-list{padding:10px;display:grid;gap:7px}
.category{
  display:flex;align-items:center;gap:9px;width:100%;
  text-align:left;border:1px solid transparent;border-radius:11px;
  padding:11px;background:#f3f8ff;color:#16385f;font-weight:bold
}
.category:hover,.category.active{background:#e0f3ff;border-color:#80cfff;color:#0068d5}
.category .arrow{margin-left:auto}
.workspace{display:grid;grid-template-columns:minmax(0,1.1fr) minmax(260px,.9fr);gap:15px}
.inner{padding:17px}
.breadcrumb{font-size:12px;color:#087cff;margin-bottom:15px}
.cat-heading{display:flex;align-items:center;gap:12px;margin-bottom:15px}
.cat-emoji{font-size:30px;background:#e3f4ff;padding:12px;border-radius:15px}
.cat-heading h3{margin:0 0 5px}
.cat-heading p{margin:0;font-size:13px;color:#687c95}
.services{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:9px}
.service{
  display:flex;align-items:center;gap:8px;text-align:left;
  border:1px solid var(--border);border-radius:11px;
  padding:12px;background:#fff;color:#18385f;font-size:13px;font-weight:bold;
  min-height:56px
}
.service:hover,.service.active{border-color:#078cff;background:#eaf6ff}
.service .arrow{margin-left:auto;color:#087cff}
.direct-title{background:linear-gradient(90deg,#078c4c,#11bd70);color:white;padding:13px;border-radius:11px;font-weight:bold}
.selected{padding:15px;border:1px solid var(--border);border-radius:13px;margin-top:13px}
.selected h3{margin:0 0 8px}
.selected p{font-size:13px;color:#62758e;line-height:1.5}
.url{font-size:12px;color:#0877d9;word-break:break-all}
.open-link{
  display:block;text-align:center;text-decoration:none;color:white;
  background:linear-gradient(90deg,#078c4c,#10b96a);
  border-radius:10px;padding:14px;margin-top:14px;font-weight:bold
}
.note{background:#eaf6ff;border-radius:10px;padding:12px;font-size:12px;line-height:1.6;margin-top:12px}
.help{
  margin-top:24px;padding:23px;border-radius:18px;
  display:flex;align-items:center;justify-content:space-between;gap:20px;
  color:white;background:linear-gradient(120deg,#061735,#104079)
}
.help h3{margin:0 0 8px}
.help p{margin:0;color:#d7e8ff;line-height:1.5}
.whatsapp{
  display:flex;align-items:center;gap:10px;border:0;border-radius:40px;
  padding:14px 22px;background:#08c86b;color:white;font-weight:bold;
  text-decoration:none;white-space:nowrap
}
.whatsapp svg{width:28px;height:28px;fill:currentColor}
.steps{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:22px}
.step{display:flex;align-items:center;gap:12px;background:white;border:1px solid var(--border);padding:16px;border-radius:14px}
.num{background:#dcf5ff;color:#087cff;width:40px;height:40px;display:grid;place-items:center;border-radius:50%;font-weight:bold}
.step small{display:block;color:#657994;margin-top:5px}
footer{text-align:center;background:#04122b;color:#d8e8ff;padding:26px 12px;margin-top:30px}
footer strong{color:white}
@media(max-width:1000px){
  header{flex-wrap:wrap}
  nav{width:100%}
  .layout{grid-template-columns:1fr}
}
@media(max-width:700px){
  header{padding:15px}
  nav a{padding:9px 11px;font-size:13px}
  .hero-content{padding:20px 16px 55px}
  main{padding:0 12px}
  .quick{padding:0 12px}
  .workspace{grid-template-columns:1fr}
  .category-list{grid-template-columns:1fr}
  .services{grid-template-columns:1fr 1fr}
  .help{align-items:flex-start;flex-direction:column}
  .steps{grid-template-columns:1fr}
}
@media(max-width:390px){.services{grid-template-columns:1fr}.brand small{font-size:10px}}
</style>
</head>
<body>

<section class="hero" id="home">
  <header>
    <div class="brand">
      <div class="logo">🖥️</div>
      <div>
        <h1>SONU <span>CYBER</span></h1>
        <small>ONLINE SERVICE PORTAL</small>
      </div>
    </div>
    <nav>
      <a href="#home">⌂ Home</a>
      <a href="#categories">▦ Categories</a>
      <a href="#how">How It Works</a>
      <a href="#help">Get Help</a>
    </nav>
  </header>
  <div class="hero-content">
    <h2>All Digital Services<br><span>One Place</span></h2>
    <p>Aadhaar · PAN · Scholarship · JPU · Bihar Services · Jobs</p>
    <div class="search">
      <input id="search" placeholder="Search Aadhaar, PAN, JPU, scholarship..." aria-label="Search services">
      <button onclick="searchServices()">Search</button>
    </div>
  </div>
</section>

<div class="quick">
  <div class="quick-inner">
    <button onclick="goCategory('Aadhaar Services')">🪪 Aadhaar</button>
    <button onclick="goCategory('PAN Card & Income Tax')">💳 PAN</button>
    <button onclick="goCategory('Scholarship Services')">🎓 Scholarship</button>
    <button onclick="goCategory('JPU University')">🏛️ JPU</button>
    <button onclick="goCategory('Bihar Government Services')">🏢 Bihar Services</button>
    <button onclick="goCategory('Jobs & Recruitment')">💼 Jobs</button>
    <button onclick="goCategory('Education & Universities')">📚 Education</button>
  </div>
</div>

<main id="categories">
  <div class="heading">
    <h2>Explore All Services</h2>
    <p>Category → Services → Direct Official Link</p>
  </div>
  <div class="layout">
    <aside class="panel">
      <div class="panel-title">
        <h3>▦ All Categories</h3>
        <p>Select a category to see its services</p>
      </div>
      <div class="category-list" id="categoryList"></div>
    </aside>

    <div class="workspace">
      <section class="panel inner">
        <div class="breadcrumb" id="breadcrumb">Home › Categories</div>
        <div class="cat-heading">
          <div class="cat-emoji" id="catEmoji">🌐</div>
          <div><h3 id="catTitle">Choose a category</h3><p id="catSubtitle">Services will appear here</p></div>
        </div>
        <div class="services" id="services"></div>
      </section>

      <section class="panel inner">
        <div class="direct-title">✓ Direct Service Link</div>
        <div class="selected">
          <h3 id="serviceTitle">Select a service</h3>
          <p id="serviceDescription">Choose a service card to see its official link.</p>
          <a class="url" id="serviceUrl" href="#" target="_blank" rel="noopener noreferrer" hidden></a>
          <a class="open-link" id="openLink" href="#" target="_blank" rel="noopener noreferrer" hidden>Open Official Website ↗</a>
        </div>
        <div class="note"><b>Important:</b> Some services require login or OTP on the official website. Never share your OTP or password with anyone.</div>
      </section>
    </div>
  </div>

  <div class="steps" id="how">
    <div class="step"><div class="num">1</div><div><b>Choose Category</b><small>Select your service category</small></div></div>
    <div class="step"><div class="num">2</div><div><b>Select Service</b><small>Find the exact task</small></div></div>
    <div class="step"><div class="num">3</div><div><b>Open Direct Link</b><small>Continue on the official portal</small></div></div>
  </div>

  <section class="help" id="help">
    <div>
      <h3>Need Help? Chat with Us</h3>
      <p>WhatsApp logo par click karein. Aapka message WhatsApp mein ready ho jayega.</p>
    </div>
    <a class="whatsapp"
       href="https://wa.me/918227002020?text=Namaste%2C%20mujhe%20Sonu%20Cyber%20Online%20Service%20Portal%20par%20help%20chahiye."
       target="_blank" rel="noopener noreferrer"
       aria-label="Get help on WhatsApp" title="Get Help on WhatsApp">
      <svg viewBox="0 0 32 32" aria-hidden="true">
        <path d="M16 .8A15 15 0 0 0 3.1 23.5L1 31l7.7-2A15.1 15.1 0 1 0 16 .8zm0 27.4a12.3 12.3 0 0 1-6.3-1.7l-.5-.3-4.6 1.2 1.2-4.5-.3-.5A12.3 12.3 0 1 1 16 28.2zm6.8-9.2c-.4-.2-2.2-1.1-2.5-1.2-.3-.1-.6-.2-.8.2-.2.4-1 1.2-1.2 1.5-.2.2-.4.3-.8.1-.4-.2-1.6-.6-3.1-2-1.1-1-1.8-2.2-2-2.6-.2-.4 0-.6.2-.8l.6-.7c.2-.2.2-.4.4-.6.1-.2 0-.5 0-.7-.1-.2-.8-2-1.1-2.7-.3-.7-.6-.6-.8-.6h-.7c-.2 0-.6.1-.9.4-.3.4-1.2 1.2-1.2 3s1.3 3.4 1.5 3.6c.2.2 2.5 3.8 6.1 5.3.9.4 1.6.6 2.1.7.9.3 1.7.2 2.3.1.7-.1 2.2-.9 2.5-1.8.3-.9.3-1.6.2-1.8-.1-.1-.3-.2-.7-.4z"/>
      </svg>
      Get Help
    </a>
  </section>
</main>

<footer>
  <strong>SONU CYBER ONLINE SERVICE PORTAL</strong>
  <div>Goreakothi · Digital Services · Fast & Safe Work</div>
  <small>Independent service directory. Linked portals are operated by their respective organisations.</small>
</footer>

<script>
const categories = [
{
 name:"Aadhaar Services", emoji:"🪪", subtitle:"Identity and Aadhaar services",
 services:[
  ["Download Aadhaar","https://myaadhaar.uidai.gov.in/","Open the official MyAadhaar portal."],
  ["Retrieve Aadhaar / EID","https://myaadhaar.uidai.gov.in/","Find available Aadhaar or enrolment ID services."],
  ["Verify Email / Mobile","https://myaadhaar.uidai.gov.in/","Open official MyAadhaar services."],
  ["Document Update","https://myaadhaar.uidai.gov.in/","Check the available document update options."],
  ["VID Generator","https://myaadhaar.uidai.gov.in/","Open Virtual ID services."],
  ["Lock / Unlock Aadhaar","https://myaadhaar.uidai.gov.in/","Open official Aadhaar lock services."],
  ["Bank Seeding Status","https://myaadhaar.uidai.gov.in/","Check official service options."],
  ["PVC Card Status","https://myaadhaar.uidai.gov.in/","Open Aadhaar PVC card services."],
  ["Enrolment / Update Status","https://myaadhaar.uidai.gov.in/","Check available status services."],
  ["Locate Enrolment Centre","https://uidai.gov.in/","Find Aadhaar centre information."],
  ["Book Appointment","https://myaadhaar.uidai.gov.in/","Open appointment options."],
  ["Check Aadhaar Validity","https://uidai.gov.in/","Open UIDAI services."],
  ["Grievance / Feedback","https://uidai.gov.in/","Find official help and grievance options."]
]},
{
 name:"PAN Card & Income Tax",emoji:"💳",subtitle:"PAN and tax services",
 services:[
  ["Apply for PAN","https://www.protean-tinpan.com/","Open PAN service provider portal."],
  ["PAN Correction","https://www.protean-tinpan.com/","Find PAN correction options."],
  ["Download e-PAN / Income Tax","https://www.incometax.gov.in/","Open the Income Tax portal."],
  ["Check PAN Status","https://www.protean-tinpan.com/","Find PAN status options."],
  ["Link PAN with Aadhaar","https://www.incometax.gov.in/","Open the official Income Tax portal."],
  ["Income Tax e-Filing","https://www.incometax.gov.in/","Open Income Tax e-Filing."]
]},
{
 name:"Scholarship Services",emoji:"🎓",subtitle:"Student scholarships",
 services:[
  ["National Scholarship Portal","https://scholarships.gov.in/","Central scholarship portal."],
  ["Bihar PMS","https://pmsonline.bihar.gov.in/","Bihar post-matric scholarship portal."],
  ["MedhaSoft","https://medhasoft.bihar.gov.in/","Bihar student scheme portal."],
  ["Bihar e-Kalyan","https://ekalyan.bihar.gov.in/","Bihar e-Kalyan portal."],
  ["Application Status","https://pmsonline.bihar.gov.in/","Open the relevant scholarship portal."],
  ["OTR / Student Registration","https://scholarships.gov.in/","Open NSP registration."]
]},
{
 name:"JPU University",emoji:"🏛️",subtitle:"Jai Prakash University services",
 services:[
  ["JPU Official Website","https://www.jpv.ac.in/","University notices and information."],
  ["Admission / Registration","https://jpvadm.samarth.edu.in/","JPU Samarth admission portal."],
  ["Semester Examination","https://www.jpv.ac.in/","Check official examination notices."],
  ["Examination Form","https://www.jpv.ac.in/","Check current examination form notices."],
  ["Admit Card","https://www.jpv.ac.in/","Find official admit-card announcements."],
  ["Results","https://www.jpv.ac.in/","Find official result announcements."],
  ["Syllabus / Notices","https://www.jpv.ac.in/","University academic information."],
  ["Academic Calendar","https://www.jpv.ac.in/","Check official university notices."]
]},
{
 name:"Bihar Government Services",emoji:"🏢",subtitle:"Certificates and Bihar services",
 services:[
  ["RTPS Services","https://serviceonline.bihar.gov.in/","Bihar ServicePlus portal."],
  ["Caste Certificate","https://serviceonline.bihar.gov.in/","Select the relevant service on Bihar RTPS."],
  ["Income Certificate","https://serviceonline.bihar.gov.in/","Select the relevant service on Bihar RTPS."],
  ["Residence Certificate","https://serviceonline.bihar.gov.in/","Select the relevant service on Bihar RTPS."],
  ["Bihar Bhumi","https://biharbhumi.bihar.gov.in/","Bihar land records portal."],
  ["Ration Card / EPDS","https://epds.bihar.gov.in/","Bihar EPDS portal."],
  ["Electricity Services","https://www.sbpdcl.co.in/","South Bihar electricity services."]
]},
{
 name:"Jobs & Recruitment",emoji:"💼",subtitle:"Government recruitment portals",
 services:[
  ["SSC","https://ssc.gov.in/","Staff Selection Commission."],
  ["BPSC","https://bpsc.bihar.gov.in/","Bihar Public Service Commission."],
  ["BSSC","https://bssc.bihar.gov.in/","Bihar Staff Selection Commission."],
  ["BTSC","https://btsc.bihar.gov.in/","Bihar Technical Service Commission."],
  ["Bihar Police","https://police.bihar.gov.in/","Bihar Police official website."],
  ["UPSC","https://www.upsc.gov.in/","Union Public Service Commission."],
  ["National Career Service","https://www.ncs.gov.in/","National Career Service."],
  ["India Post GDS","https://indiapostgdsonline.gov.in/","India Post GDS recruitment."]
]},
{
 name:"Education & Universities",emoji:"📚",subtitle:"Boards and education portals",
 services:[
  ["Bihar Board","https://biharboardonline.bihar.gov.in/","Bihar School Examination Board."],
  ["CBSE","https://www.cbse.gov.in/","CBSE official website."],
  ["IGNOU","https://www.ignou.ac.in/","IGNOU official website."],
  ["NTA","https://nta.ac.in/","National Testing Agency."],
  ["NIOS","https://nios.ac.in/","National Institute of Open Schooling."],
  ["ABC ID","https://www.abc.gov.in/","Academic Bank of Credits."],
  ["UGC","https://www.ugc.gov.in/","University Grants Commission."]
]},
{
 name:"Voter, Passport & Identity",emoji:"🗳️",subtitle:"Identity document portals",
 services:[
  ["Voter Services","https://voters.eci.gov.in/","Election Commission voter services."],
  ["Passport Seva","https://www.passportindia.gov.in/","Official Passport Seva website."],
  ["DigiLocker","https://www.digilocker.gov.in/","Digital document wallet."],
  ["UMANG","https://web.umang.gov.in/","Government services portal."],
  ["Birth / Death Registration","https://crsorgi.gov.in/","Civil Registration System."]
]},
{
 name:"Railway & Transport",emoji:"🚆",subtitle:"Travel and transport services",
 services:[
  ["IRCTC Ticket Booking","https://www.irctc.co.in/","Official IRCTC portal."],
  ["Parivahan","https://parivahan.gov.in/","Transport services portal."],
  ["Driving Licence","https://parivahan.gov.in/","Open Parivahan services."],
  ["Vehicle Registration","https://parivahan.gov.in/","Vehicle services on Parivahan."],
  ["e-Challan","https://echallan.parivahan.nic.in/","Official e-Challan portal."]
]},
{
 name:"Farmer & Rural Schemes",emoji:"🌾",subtitle:"Farmer and rural schemes",
 services:[
  ["PM-KISAN","https://pmkisan.gov.in/","PM-KISAN official portal."],
  ["MGNREGA","https://nrega.nic.in/","Rural employment information."],
  ["PMAY-Gramin","https://pmayg.nic.in/","Rural housing scheme portal."],
  ["Jal Jeevan Mission","https://jaljeevanmission.gov.in/","Jal Jeevan Mission portal."],
  ["NRLM","https://nrlm.gov.in/","National Rural Livelihoods Mission."]
]},
{
 name:"Health, Labour & Pension",emoji:"🏥",subtitle:"Health, labour and pension portals",
 services:[
  ["Ayushman Bharat Beneficiary","https://beneficiary.nha.gov.in/","Official beneficiary portal."],
  ["e-Shram","https://eshram.gov.in/","e-Shram portal."],
  ["EPFO","https://www.epfindia.gov.in/","Employees Provident Fund Organisation."],
  ["Pension / NSAP","https://nsap.nic.in/","National Social Assistance Programme."],
  ["Bihar Labour","https://state.bihar.gov.in/labour/","Bihar Labour Department."]
]},
{
 name:"Business & Registration",emoji:"🏪",subtitle:"Business registration portals",
 services:[
  ["GST Portal","https://www.gst.gov.in/","Goods and Services Tax portal."],
  ["Udyam Registration","https://udyamregistration.gov.in/","Official MSME Udyam registration."],
  ["MCA Services","https://www.mca.gov.in/","Ministry of Corporate Affairs."],
  ["FSSAI / FoSCoS","https://foscos.fssai.gov.in/","Food safety registration portal."],
  ["GeM Portal","https://gem.gov.in/","Government e-Marketplace."],
  ["Startup India","https://www.startupindia.gov.in/","Startup India portal."]
]},
{
 name:"PDF, Photo & Design Tools",emoji:"🖨️",subtitle:"Online document and design tools",
 services:[
  ["PDF24 Tools","https://tools.pdf24.org/","Online PDF tools."],
  ["iLovePDF","https://www.ilovepdf.com/","PDF tools."],
  ["Smallpdf","https://smallpdf.com/","PDF tools."],
  ["Remove Photo Background","https://www.remove.bg/","Background removal tool."],
  ["Photopea Editor","https://www.photopea.com/","Online image editor."],
  ["Canva Design","https://www.canva.com/","Design tools."]
]},
{
 name:"Legal, RTI & Other Services",emoji:"⚖️",subtitle:"Legal and complaint portals",
 services:[
  ["RTI Online","https://rtionline.gov.in/","Central RTI online portal."],
  ["Public Grievance","https://pgportal.gov.in/","CPGRAMS grievance portal."],
  ["Consumer Helpline","https://consumerhelpline.gov.in/","National Consumer Helpline."],
  ["eCourts","https://services.ecourts.gov.in/ecourtindia_v6/","eCourts services portal."],
  ["India Post","https://www.indiapost.gov.in/","India Post official website."],
  ["CSC Digital Seva","https://digitalseva.csc.gov.in/","CSC Digital Seva portal."]
]}
];

let activeCategory=0,activeService=0;
const el=id=>document.getElementById(id);

function renderCategories(filter=""){
 const list=el("categoryList");list.innerHTML="";
 categories.forEach((c,i)=>{
  const all=(c.name+" "+c.subtitle+" "+c.services.map(s=>s[0]).join(" ")).toLowerCase();
  if(filter&&!all.includes(filter.toLowerCase()))return;
  const b=document.createElement("button");
  b.className="category"+(i===activeCategory?" active":"");
  b.innerHTML=`<span>${c.emoji}</span><span>${i+1}. ${c.name}</span><span class="arrow">›</span>`;
  b.onclick=()=>selectCategory(i);
  list.appendChild(b);
 });
}
function renderServices(filter=""){
 const c=categories[activeCategory];
 el("catEmoji").textContent=c.emoji;
 el("catTitle").textContent=c.name;
 el("catSubtitle").textContent=c.subtitle+" · "+c.services.length+" services";
 el("breadcrumb").textContent="Home › "+c.name;
 const box=el("services");box.innerHTML="";
 c.services.forEach((s,i)=>{
  if(filter&&!s[0].toLowerCase().includes(filter.toLowerCase())&&!c.name.toLowerCase().includes(filter.toLowerCase()))return;
  const b=document.createElement("button");
  b.className="service"+(i===activeService?" active":"");
  b.innerHTML=`<span>🔹</span><span>${s[0]}</span><span class="arrow">›</span>`;
  b.onclick=()=>selectService(i);
  box.appendChild(b);
 });
 if(!box.children.length)box.innerHTML="<p>No matching services. Try a different search.</p>";
}
function showDetail(){
 const s=categories[activeCategory].services[activeService];
 el("serviceTitle").textContent=s[0];
 el("serviceDescription").textContent=s[2];
 el("serviceUrl").textContent=s[1];
 el("serviceUrl").href=s[1];
 el("serviceUrl").hidden=false;
 el("openLink").href=s[1];
 el("openLink").hidden=false;
}
function selectCategory(i){
 activeCategory=i;activeService=0;
 renderCategories(el("search").value.trim());
 renderServices(el("search").value.trim());
 showDetail();
}
function selectService(i){
 activeService=i;renderServices(el("search").value.trim());showDetail();
}
function goCategory(name){
 const i=categories.findIndex(c=>c.name===name);
 if(i>=0){selectCategory(i);el("categories").scrollIntoView({behavior:"smooth"});}
}
function searchServices(){
 const q=el("search").value.trim().toLowerCase();
 if(!q){renderCategories();renderServices();return;}
 let found=-1,service=0;
 categories.some((c,i)=>{
  const si=c.services.findIndex(s=>s[0].toLowerCase().includes(q));
  if(c.name.toLowerCase().includes(q)||si>=0){found=i;service=si>=0?si:0;return true;}
  return false;
 });
 renderCategories(q);
 if(found>=0){activeCategory=found;activeService=service;renderCategories(q);renderServices(q);showDetail();}
 else renderServices(q);
}
el("search").addEventListener("keydown",e=>{if(e.key==="Enter")searchServices();});
renderCategories();renderServices();showDetail();
</script>
</body>
</html>
