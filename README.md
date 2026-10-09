
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sonu Cyber Online Service Portal</title>
<style>
:root {
  --blue:#155eef;
  --dark:#102448;
  --bg:#f3f6fc;
}
* { box-sizing:border-box; }
body {
  margin:0;
  font-family:Arial,"Noto Sans Devanagari",sans-serif;
  background:var(--bg);
  color:#172033;
}
header {
  padding:30px 16px;
  text-align:center;
  color:white;
  background:linear-gradient(135deg,#102448,#155eef,#7c3aed);
}
.logo {
  display:inline-grid;
  place-items:center;
  width:65px;height:65px;
  background:#ffffff22;
  border:1px solid #ffffff55;
  border-radius:20px;
  font-size:30px;
}
header h1 { margin:12px 0 5px; font-size:27px; }
header p { margin:5px 0; }
.search-wrap { max-width:650px; margin:22px auto 0; }
input {
  width:100%; padding:15px;
  border:0; border-radius:12px;
  font-size:16px; outline:none;
}
.container { max-width:1200px; margin:auto; padding:20px 14px; }
.welcome {
  background:white; padding:18px;
  border-radius:16px; margin-bottom:22px;
  box-shadow:0 3px 14px #14254b0c;
}
h2 { font-size:21px; margin:8px 0 16px; }
.category-grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(145px,1fr));
  gap:12px; margin-bottom:30px;
}
.category {
  padding:18px 10px; border-radius:15px;
  border:1px solid #e3e8f3;
  background:white; cursor:pointer;
  text-align:center; font-weight:bold;
  transition:.2s; color:#172033;
}
.category:hover,.category.active {
  transform:translateY(-3px);
  border-color:#155eef;
  box-shadow:0 6px 20px #155eef20;
}
.category .emoji { display:block; font-size:28px; margin-bottom:9px; }
.section { margin:26px 0; scroll-margin-top:15px; }
.section-title {
  display:flex; align-items:center; gap:10px;
  padding-bottom:10px; border-bottom:2px solid #e2e8f0;
}
.services {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:13px; margin-top:14px;
}
.service {
  background:white; border:1px solid #e3e8f3;
  border-radius:14px; padding:16px;
  box-shadow:0 3px 12px #17203308;
  display:flex; flex-direction:column; gap:10px;
}
.service h3 { font-size:16px; margin:0; }
.service p { font-size:13px; color:#667085; margin:0; flex:1; }
.open {
  display:block; text-decoration:none; text-align:center;
  padding:11px; border-radius:9px;
  color:white; background:var(--blue); font-weight:bold;
}
.open:hover { background:#1048bd; }
.empty { display:none; padding:25px; text-align:center; }
footer {
  background:var(--dark); color:white;
  text-align:center; padding:25px 12px; margin-top:30px;
  font-size:13px; line-height:1.8;
}
.notice { color:#475467; font-size:13px; line-height:1.7; }
@media(max-width:480px) {
  header h1 { font-size:23px; }
  .services { grid-template-columns:1fr 1fr; gap:9px; }
  .service { padding:12px; }
  .service h3 { font-size:14px; }
  .open { font-size:12px; }
}
</style>
</head>
<body>

<header>
  <div class="logo">💻</div>
  <h1>SONU CYBER</h1>
  <p><b>ONLINE SERVICE PORTAL</b></p>
  <p>All Digital Services at One Place</p>
  <div class="search-wrap">
    <input id="search" type="search"
      placeholder="🔎 Search service, scholarship, JPU, Aadhaar..."
      aria-label="Search services">
  </div>
</header>

<main class="container">
  <div class="welcome">
    <h2>🙏 Welcome to Sonu Cyber</h2>
    <p>अपनी जरूरत की सेवा चुनें और संबंधित वेबसाइट खोलें।</p>
    <p class="notice">यह एक link directory है। आवेदन और भुगतान संबंधित आधिकारिक वेबसाइट पर होंगे।</p>
  </div>

  <h2>📂 All Service Categories</h2>
  <div class="category-grid" id="categories"></div>
  <div id="allSections"></div>
  <div class="empty" id="empty">कोई सेवा नहीं मिली। दूसरा शब्द खोजें।</div>
</main>

<footer>
  <b>SONU CYBER ONLINE SERVICE PORTAL</b><br>
  Digital Services • Education • Government Portals<br>
  सरकारी वेबसाइटों के लोगो और सेवाएँ उनके संबंधित विभागों के हैं।
  <br>किसी निजी वेबसाइट पर दस्तावेज या भुगतान देने से पहले URL जाँचें।
</footer>

<script>
const groups = [
{
 title:"Aadhaar Services", icon:"🪪", color:"#e0f2fe",
 items:[
  ["UIDAI Official Website","https://uidai.gov.in/"],
  ["My Aadhaar Portal","https://myaadhaar.uidai.gov.in/"],
  ["Aadhaar Download / Services","https://myaadhaar.uidai.gov.in/"],
  ["Aadhaar Centre Information","https://uidai.gov.in/"],
  ["Aadhaar Appointment / Update Info","https://uidai.gov.in/"]
 ]
},
{
 title:"PAN Card & Income Tax", icon:"💳", color:"#fce7f3",
 items:[
  ["Protean PAN Services","https://www.protean-tinpan.com/"],
  ["Income Tax e-Filing","https://www.incometax.gov.in/"],
  ["UTIITSL PAN Services","https://www.pan.utiitsl.com/"],
  ["GST Portal","https://www.gst.gov.in/"]
 ]
},
{
 title:"Scholarship Services", icon:"🎓", color:"#dcfce7",
 items:[
  ["National Scholarship Portal (NSP)","https://scholarships.gov.in/"],
  ["Bihar Post Matric Scholarship","https://pmsonline.bihar.gov.in/"],
  ["Bihar MedhaSoft","https://medhasoft.bihar.gov.in/"],
  ["Bihar e-Kalyan","https://ekalyan.bihar.gov.in/"],
  ["PFMS Payment Status","https://pfms.nic.in/"],
  ["Academic Bank of Credits (ABC)","https://www.abc.gov.in/"],
  ["DigiLocker Documents","https://www.digilocker.gov.in/"]
 ]
},
{
 title:"Education & JPU University", icon:"📚", color:"#fef3c7",
 items:[
  ["JPU Official Website","https://www.jpv.ac.in/"],
  ["JPU Admission Portal","https://jpvadm.samarth.edu.in/"],
  ["JPU Notices & Exam Form Updates","https://www.jpv.ac.in/notification"],
  ["JPU Results","https://www.jpv.ac.in/"],
  ["JPU Syllabus","https://www.jpv.ac.in/"],
  ["Bihar Board (BSEB)","https://biharboardonline.bihar.gov.in/"],
  ["CBSE","https://www.cbse.gov.in/"],
  ["IGNOU","https://www.ignou.ac.in/"],
  ["OFSS Bihar Admission","https://ofssbihar.net/"],
  ["NTA","https://nta.ac.in/"],
  ["NIOS","https://nios.ac.in/"],
  ["UGC","https://www.ugc.gov.in/"],
  ["AICTE","https://www.aicte-india.org/"]
 ]
},
{
 title:"Bihar Government Services", icon:"🏛️", color:"#ede9fe",
 items:[
  ["Bihar RTPS / ServicePlus","https://serviceonline.bihar.gov.in/"],
  ["Bihar Bhumi Land Records","https://biharbhumi.bihar.gov.in/"],
  ["Bihar Ration Card (EPDS)","https://epds.bihar.gov.in/"],
  ["Bihar Government Portal","https://state.bihar.gov.in/"],
  ["Bihar Student Credit Card","https://www.7nishchay-yuvaupmission.bihar.gov.in/"],
  ["South Bihar Electricity (SBPDCL)","https://www.sbpdcl.co.in/"],
  ["North Bihar Electricity (NBPDCL)","https://www.nbpdcl.co.in/"],
  ["Bihar Police","https://police.bihar.gov.in/"],
  ["Bihar Labour Department","https://state.bihar.gov.in/labour/"],
  ["Bihar e-Procurement","https://eproc2.bihar.gov.in/EPSV2Web/"]
 ]
},
{
 title:"Government Jobs & Recruitment", icon:"💼", color:"#ffedd5",
 items:[
  ["SSC","https://ssc.gov.in/"],
  ["UPSC","https://www.upsc.gov.in/"],
  ["BPSC","https://bpsc.bihar.gov.in/"],
  ["BSSC","https://bssc.bihar.gov.in/"],
  ["BTSC","https://btsc.bihar.gov.in/"],
  ["Railway Recruitment Board","https://www.rrbcdg.gov.in/"],
  ["India Post GDS Recruitment","https://indiapostgdsonline.gov.in/"],
  ["National Career Service","https://www.ncs.gov.in/"],
  ["Apprenticeship India","https://www.apprenticeshipindia.gov.in/"],
  ["Skill India Digital","https://www.skillindiadigital.gov.in/"],
  ["Indian Army Recruitment","https://joinindianarmy.nic.in/"],
  ["Indian Navy Recruitment","https://www.joinindiannavy.gov.in/"],
  ["Indian Air Force","https://indianairforce.nic.in/"]
 ]
},
{
 title:"Voter, Passport & Identity", icon:"🗳️", color:"#cffafe",
 items:[
  ["Voter Services","https://voters.eci.gov.in/"],
  ["Election Commission of India","https://www.eci.gov.in/"],
  ["Passport Seva","https://www.passportindia.gov.in/"],
  ["DigiLocker","https://www.digilocker.gov.in/"],
  ["UMANG","https://web.umang.gov.in/"],
  ["CSC Digital Seva","https://digitalseva.csc.gov.in/"]
 ]
},
{
 title:"Railway, Travel & Transport", icon:"🚆", color:"#dbeafe",
 items:[
  ["IRCTC Train Booking","https://www.irctc.co.in/"],
  ["Indian Railways","https://indianrailways.gov.in/"],
  ["Parivahan Services","https://parivahan.gov.in/"],
  ["Traffic e-Challan","https://echallan.parivahan.nic.in/"],
  ["India Post","https://www.indiapost.gov.in/"]
 ]
},
{
 title:"Farmer & Rural Schemes", icon:"🌾", color:"#ecfccb",
 items:[
  ["PM Kisan","https://pmkisan.gov.in/"],
  ["MGNREGA","https://nrega.nic.in/"],
  ["PMAY-Gramin","https://pmayg.nic.in/"],
  ["National Rural Livelihood Mission","https://nrlm.gov.in/"],
  ["Jal Jeevan Mission","https://jaljeevanmission.gov.in/"],
  ["National Food Security Portal","https://nfsa.gov.in/"]
 ]
},
{
 title:"Health, Labour & Pension", icon:"🏥", color:"#ffe4e6",
 items:[
  ["Ayushman Bharat Beneficiary","https://beneficiary.nha.gov.in/"],
  ["e-Shram","https://eshram.gov.in/"],
  ["EPFO","https://www.epfindia.gov.in/"],
  ["National Social Assistance / Pension","https://nsap.nic.in/"],
  ["Shram Suvidha","https://shramsuvidha.gov.in/"],
  ["Birth & Death Registration","https://crsorgi.gov.in/"]
 ]
},
{
 title:"Business, GST & Registration", icon:"🏢", color:"#f3e8ff",
 items:[
  ["GST","https://www.gst.gov.in/"],
  ["Udyam Registration","https://udyamregistration.gov.in/"],
  ["MCA Company Services","https://www.mca.gov.in/"],
  ["GeM Government Marketplace","https://gem.gov.in/"],
  ["Startup India","https://www.startupindia.gov.in/"],
  ["FSSAI FoSCoS","https://foscos.fssai.gov.in/"],
  ["ICEGATE","https://www.icegate.gov.in/"],
  ["RBI","https://www.rbi.org.in/"]
 ]
},
{
 title:"PDF, Photo & Design Tools", icon:"📄", color:"#f1f5f9",
 items:[
  ["PDF24 Tools","https://tools.pdf24.org/"],
  ["iLovePDF","https://www.ilovepdf.com/"],
  ["Smallpdf","https://smallpdf.com/"],
  ["Canva Design","https://www.canva.com/"],
  ["Remove Background","https://www.remove.bg/"],
  ["Photopea Editor","https://www.photopea.com/"],
  ["Google Drive","https://drive.google.com/"],
  ["Google Translate","https://translate.google.com/"]
 ]
},
{
 title:"Legal, RTI & Complaints", icon:"⚖️", color:"#fef9c3",
 items:[
  ["eCourts","https://services.ecourts.gov.in/ecourtindia_v6/"],
  ["RTI Online","https://rtionline.gov.in/"],
  ["CPGRAMS Public Grievance","https://pgportal.gov.in/"],
  ["National Consumer Helpline","https://consumerhelpline.gov.in/"],
  ["India Government Services","https://services.india.gov.in/"],
  ["National Portal of India","https://www.india.gov.in/"]
 ]
}
];

const categories = document.getElementById("categories");
const allSections = document.getElementById("allSections");
const search = document.getElementById("search");
const empty = document.getElementById("empty");

groups.forEach((group, index) => {
  const cat = document.createElement("button");
  cat.className = "category";
  cat.style.background = group.color;
  cat.innerHTML = `<span class="emoji">${group.icon}</span>${group.title}`;
  cat.onclick = () => {
    document.getElementById("section-" + index)
      .scrollIntoView({behavior:"smooth",block:"start"});
  };
  categories.appendChild(cat);

  const section = document.createElement("section");
  section.className = "section";
  section.id = "section-" + index;
  section.innerHTML =
    `<h2 class="section-title"><span>${group.icon}</span>${group.title}</h2>`;

  const grid = document.createElement("div");
  grid.className = "services";

  group.items.forEach(([name, url]) => {
    const card = document.createElement("article");
    card.className = "service";
    card.dataset.search = (name + " " + group.title).toLowerCase();

    const heading = document.createElement("h3");
    heading.textContent = name;

    const desc = document.createElement("p");
    desc.textContent = group.title;

    const link = document.createElement("a");
    link.className = "open";
    link.href = url;
    link.target = "_blank";
    link.rel = "noopener noreferrer";
    link.textContent = "Open Website ↗";

    card.append(heading, desc, link);
    grid.appendChild(card);
  });

  section.appendChild(grid);
  allSections.appendChild(section);
});

search.addEventListener("input", () => {
  const query = search.value.trim().toLowerCase();
  let total = 0;

  document.querySelectorAll(".section").forEach(section => {
    let count = 0;
    section.querySelectorAll(".service").forEach(card => {
      const show = card.dataset.search.includes(query);
      card.style.display = show ? "flex" : "none";
      if (show) count++;
    });
    section.style.display = count ? "block" : "none";
    total += count;
  });

  categories.style.display = query ? "none" : "grid";
  empty.style.display = total ? "none" : "block";
});
</script>
</body>
</html>
