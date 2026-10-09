
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sonu Cyber | Digital Service Portal</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f1f5ff;color:#182348}
header{padding:28px 16px;color:white;text-align:center;background:linear-gradient(130deg,#10154e,#245bea,#05b7ca)}
header h1{margin:0;font-size:29px}
header p{margin:10px 0}
.phone{display:inline-block;background:#ffffff22;padding:9px 16px;border-radius:20px}
main{max-width:1100px;margin:auto;padding:18px}
input{width:100%;padding:15px;border:1px solid #d7def2;border-radius:12px;font-size:16px;margin-bottom:20px}
h2{font-size:21px}
.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
.cat{background:white;border:1px solid #e0e6f5;border-radius:15px;padding:16px 8px;text-align:center;cursor:pointer;box-shadow:0 5px 15px #172b6410}
.cat:hover{transform:translateY(-3px);border-color:#3866f2}
.cat span{font-size:29px;display:block;margin-bottom:9px}
.cat strong{font-size:13px}
#services{margin-top:26px}
.list{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.item{background:white;padding:14px;border-radius:12px;border:1px solid #e1e6f2}
.item a{display:block;color:#2458df;font-weight:bold;text-decoration:none;margin-top:9px;font-size:13px}
.item a:hover{text-decoration:underline}
.back{padding:10px 14px;background:#172a72;color:white;border:0;border-radius:9px;cursor:pointer}
footer{margin-top:35px;padding:24px;background:#101746;color:white;text-align:center;font-size:13px;line-height:1.8}
@media(max-width:750px){.grid{grid-template-columns:repeat(2,1fr)}.list{grid-template-columns:repeat(2,1fr)}}
@media(max-width:420px){.list{grid-template-columns:1fr}header h1{font-size:24px}}
</style>
</head>
<body>
<header>
<h1>🖥️ SONU CYBER</h1>
<p>GOREAKOTHI • DIGITAL SERVICE PORTAL</p>
<p>सभी जरूरी ऑनलाइन सेवाएँ एक ही जगह</p>
<div class="phone">📞 8227002020</div>
</header>

<main>
<input id="search" placeholder="🔎 सेवा खोजें: Aadhaar, PAN, Scholarship..." oninput="searchServices()">

<h2>📂 सभी Categories</h2>
<div class="grid" id="categories"></div>

<section id="services" hidden>
<button class="back" onclick="showCategories()">← सभी Categories</button>
<h2 id="heading"></h2>
<div class="list" id="list"></div>
</section>
</main>

<footer>
<strong>SONU CYBER GOREAKOTHI</strong><br>
Collage Road, Goreakothi<br>
Contact: 8227002020<br>
यह एक स्वतंत्र लिंक डायरेक्टरी है, सरकारी वेबसाइट नहीं।
</footer>

<script>
const data=[
{n:"बिहार सरकारी सेवाएँ",e:"🏛️",s:[
["Bihar RTPS","https://serviceonline.bihar.gov.in/"],
["Bihar Government","https://state.bihar.gov.in/"],
["Bihar Public Grievance","https://lokshikayat.bihar.gov.in/"],
["Bihar Police","https://police.bihar.gov.in/"],
["Bihar Tourism","https://tourism.bihar.gov.in/"],
["UMANG","https://web.umang.gov.in/"],
["MyScheme","https://www.myscheme.gov.in/"],
["Government Services","https://services.india.gov.in/"]
]},
{n:"Aadhaar & Identity",e:"🪪",s:[
["UIDAI Official","https://uidai.gov.in/"],
["My Aadhaar","https://myaadhaar.uidai.gov.in/"],
["DigiLocker","https://www.digilocker.gov.in/"],
["Voter Services","https://voters.eci.gov.in/"],
["Election Commission","https://www.eci.gov.in/"],
["Passport Seva","https://www.passportindia.gov.in/"]
]},
{n:"PAN & Tax Services",e:"💳",s:[
["Income Tax e-Filing","https://www.incometax.gov.in/"],
["Protean PAN","https://www.protean-tinpan.com/"],
["UTIITSL PAN","https://www.pan.utiitsl.com/"],
["GST Portal","https://www.gst.gov.in/"],
["MCA Services","https://www.mca.gov.in/"],
["Udyam Registration","https://udyamregistration.gov.in/"]
]},
{n:"जमीन व राजस्व",e:"🌾",s:[
["Bihar Bhumi","https://biharbhumi.bihar.gov.in/"],
["Bhumijankari","https://bhumijankari.bihar.gov.in/"],
["Land Records Department","https://land.bihar.gov.in/"],
["Registration Department","https://nibandhan.bihar.gov.in/"],
["Department of Land Resources","https://dolr.gov.in/"]
]},
{n:"Scholarship",e:"🎓",s:[
["National Scholarship Portal","https://scholarships.gov.in/"],
["Bihar Post Matric Scholarship","https://pmsonline.bih.nic.in/"],
["Education Ministry","https://www.education.gov.in/"],
["AICTE","https://www.aicte-india.org/"],
["UGC","https://www.ugc.gov.in/"]
]},
{n:"पढ़ाई व परीक्षा",e:"📚",s:[
["Bihar Board","https://biharboardonline.bihar.gov.in/"],
["BSEB Secondary","https://secondary.biharboardonline.com/"],
["CBSE","https://www.cbse.gov.in/"],
["NTA","https://nta.ac.in/"],
["CUET","https://exams.nta.nic.in/cuet-ug/"],
["JEE Main","https://jeemain.nta.nic.in/"],
["NEET","https://neet.nta.nic.in/"],
["IGNOU","https://www.ignou.ac.in/"],
["SWAYAM","https://swayam.gov.in/"]
]},
{n:"सरकारी नौकरी",e:"🧑‍💼",s:[
["SSC","https://ssc.gov.in/"],
["UPSC","https://upsc.gov.in/"],
["BPSC","https://bpsc.bihar.gov.in/"],
["BSSC","https://bssc.bihar.gov.in/"],
["BTSC","https://btsc.bihar.gov.in/"],
["CSBC Bihar Police","https://csbc.bihar.gov.in/"],
["National Career Service","https://www.ncs.gov.in/"],
["Railway Recruitment","https://www.rrbcdg.gov.in/"],
["India Post GDS","https://indiapostgdsonline.gov.in/"],
["Employment News","https://employmentnews.gov.in/"]
]},
{n:"किसान योजनाएँ",e:"🚜",s:[
["PM-KISAN","https://pmkisan.gov.in/"],
["PM Fasal Bima","https://pmfby.gov.in/"],
["Soil Health Card","https://soilhealth.dac.gov.in/"],
["e-NAM","https://www.enam.gov.in/"],
["Agriculture Ministry","https://agriwelfare.gov.in/"]
]},
{n:"बैंकिंग व पेंशन",e:"🏦",s:[
["RBI","https://www.rbi.org.in/"],
["NPCI","https://www.npci.org.in/"],
["SBI","https://sbi.co.in/"],
["Bank of Baroda","https://www.bankofbaroda.in/"],
["Punjab National Bank","https://www.pnbindia.in/"],
["India Post Payments Bank","https://www.ippbonline.com/"],
["EPFO","https://www.epfindia.gov.in/"],
["ESIC","https://www.esic.gov.in/"],
["e-Shram","https://eshram.gov.in/"],
["Pension Portal","https://pensionersportal.gov.in/"]
]},
{n:"Railway & Transport",e:"🚆",s:[
["IRCTC","https://www.irctc.co.in/"],
["Indian Railways","https://indianrailways.gov.in/"],
["Train Enquiry","https://enquiry.indianrail.gov.in/"],
["Parivahan","https://parivahan.gov.in/"],
["Driving Licence","https://sarathi.parivahan.gov.in/"],
["Vehicle Services","https://vahan.parivahan.gov.in/"],
["eChallan","https://echallan.parivahan.gov.in/"],
["India Post","https://www.indiapost.gov.in/"]
]},
{n:"शिकायत व नागरिक मदद",e:"⚖️",s:[
["CPGRAMS","https://pgportal.gov.in/"],
["Consumer Helpline","https://consumerhelpline.gov.in/"],
["Cyber Crime Portal","https://cybercrime.gov.in/"],
["RTI Online","https://rtionline.gov.in/"],
["eCourts","https://ecourts.gov.in/"],
["India Code","https://www.indiacode.nic.in/"],
["MyGov","https://www.mygov.in/"]
]},
{n:"Design & PDF Tools",e:"🎨",s:[
["Canva","https://www.canva.com/"],
["Adobe Express","https://www.adobe.com/express/"],
["Photopea","https://www.photopea.com/"],
["Remove Background","https://www.remove.bg/"],
["Google Docs","https://docs.google.com/"],
["Google Forms","https://forms.google.com/"],
["Google Drive","https://drive.google.com/"],
["PDF24","https://tools.pdf24.org/"],
["iLovePDF","https://www.ilovepdf.com/"],
["Smallpdf","https://smallpdf.com/"]
]},
{n:"स्वास्थ्य सेवाएँ",e:"🏥",s:[
["Health Ministry","https://mohfw.gov.in/"],
["Ayushman Bharat","https://pmjay.gov.in/"],
["ABHA Health ID","https://abha.abdm.gov.in/"],
["eSanjeevani","https://esanjeevani.mohfw.gov.in/"],
["Bihar Health Department","https://state.bihar.gov.in/health/"]
]},
{n:"ऑनलाइन सीखना",e:"💡",s:[
["SWAYAM","https://swayam.gov.in/"],
["NPTEL","https://nptel.ac.in/"],
["DIKSHA","https://diksha.gov.in/"],
["ePathshala","https://epathshala.nic.in/"],
["Khan Academy","https://www.khanacademy.org/"],
["Coursera","https://www.coursera.org/"]
]},
{n:"Business & Digital Work",e:"🧾",s:[
["GeM Portal","https://gem.gov.in/"],
["Startup India","https://www.startupindia.gov.in/"],
["CSC Official","https://csc.gov.in/"],
["Digital India","https://www.digitalindia.gov.in/"],
["Government e-Tenders","https://eprocure.gov.in/"]
]},
{n:"Email & Online Tools",e:"☁️",s:[
["Gmail","https://mail.google.com/"],
["Google Search","https://www.google.com/"],
["Google Translate","https://translate.google.com/"],
["Google Maps","https://maps.google.com/"],
["Google Photos","https://photos.google.com/"],
["Microsoft Office","https://www.office.com/"],
["OneDrive","https://onedrive.live.com/"]
]}
];

const cats=document.getElementById("categories");
const section=document.getElementById("services");
const list=document.getElementById("list");
const heading=document.getElementById("heading");
const search=document.getElementById("search");

function showCategories(){
 section.hidden=true;
 cats.parentElement.hidden=false;
 cats.style.display="grid";
}
function openCategory(index){
 const category=data[index];
 heading.textContent=category.e+" "+category.n;
 list.innerHTML="";
 category.s.forEach(item=>addItem(item[0],item[1],category.n));
 cats.style.display="none";
 section.hidden=false;
 section.scrollIntoView({behavior:"smooth"});
}
function addItem(name,url,category){
 const div=document.createElement("div");
 div.className="item";
 const title=document.createElement("strong");
 title.textContent=name;
 const desc=document.createElement("div");
 desc.style.cssText="font-size:12px;color:#68738b;margin-top:5px";
 desc.textContent=category;
 const a=document.createElement("a");
 a.href=url;a.target="_blank";a.rel="noopener noreferrer";
 a.textContent="Open Website ↗";
 div.append(title,desc,a);list.appendChild(div);
}
function renderCategories(){
 cats.innerHTML="";
 data.forEach((c,i)=>{
  const b=document.createElement("button");
  b.className="cat";
  b.innerHTML="<span>"+c.e+"</span><strong>"+c.n+"</strong>";
  b.onclick=()=>openCategory(i);
  cats.appendChild(b);
 });
 cats.style.display="grid";
}
function searchServices(){
 const q=search.value.trim().toLowerCase();
 if(!q){showCategories();return}
 const matches=[];
 data.forEach(c=>c.s.forEach(s=>{
  if((s[0]+" "+c.n+" "+s[1]).toLowerCase().includes(q))
   matches.push({name:s[0],url:s[1],category:c.n});
 }));
 heading.textContent="🔎 Search Results";
 list.innerHTML="";
 matches.forEach(x=>addItem(x.name,x.url,x.category));
 cats.style.display="none";
 section.hidden=false;
 if(!matches.length){
  const msg=document.createElement("p");
  msg.textContent="कोई लिंक नहीं मिला। दूसरा नाम खोजें।";
  list.appendChild(msg);
 }
}
renderCategories();
</script>
</body>
</html>
