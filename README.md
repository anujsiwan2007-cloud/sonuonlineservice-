<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Nova PAN Desk</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;font-family:Arial,sans-serif;background:#f5f3fb;color:#201b38
}
button,input,select,textarea{font:inherit}
.hidden{display:none!important}

/* LOGIN */
.login{
 min-height:100vh;display:flex;
 background:linear-gradient(135deg,#241550,#6845e8)
}
.login-left{
 width:55%;padding:70px;color:white;position:relative;overflow:hidden
}
.login-left h1{
 font-size:55px;line-height:1.1;margin-top:100px
}
.login-left h1 span{color:#ffc477}
.login-left p{max-width:500px;color:#ddd5ff;line-height:1.8}
.logo{
 display:flex;align-items:center;gap:10px;font-weight:bold
}
.logo-box{
 width:45px;height:45px;border-radius:14px;
 background:linear-gradient(135deg,#ffd08b,#ff956b);
 display:grid;place-items:center;color:#37206d;font-weight:900
}
.login-right{
 width:45%;background:white;display:flex;
 align-items:center;justify-content:center;padding:30px
}
.login-card{width:380px}
.login-card h2{font-size:30px;margin-bottom:8px}
.muted{color:#89849d;font-size:13px;line-height:1.6}
label{display:block;font-size:12px;font-weight:bold;margin:17px 0 7px}
input,select,textarea{
 width:100%;padding:13px;border:1px solid #e3dfef;
 border-radius:9px;outline:none;background:white
}
input:focus,select:focus,textarea:focus{
 border-color:#7653e8;box-shadow:0 0 0 3px #7653e815
}
.btn{
 border:0;border-radius:9px;padding:12px 17px;
 cursor:pointer;font-weight:bold
}
.primary{
 background:linear-gradient(100deg,#6240df,#8b5cf6);
 color:white
}
.full{width:100%;margin-top:20px}
.demo{
 margin-top:20px;background:#f5f1ff;padding:13px;
 border-radius:9px;font-size:12px
}

/* APP */
.topbar{
 height:70px;background:white;border-bottom:1px solid #e9e5f2;
 display:flex;align-items:center;padding:0 25px;gap:25px
}
.topbar .search{width:330px;margin-left:30px}
.topbar .search input{background:#f8f7fb;border:0}
.user{margin-left:auto;font-size:12px;font-weight:bold}
.app{display:flex;min-height:calc(100vh - 70px)}
.sidebar{
 width:245px;background:white;border-right:1px solid #e9e5f2;
 padding:25px 13px
}
.side-title{
 font-size:9px;color:#aaa4b9;font-weight:bold;
 letter-spacing:1.5px;margin:15px 10px 8px
}
.nav{
 width:100%;border:0;background:transparent;
 padding:12px;border-radius:9px;text-align:left;
 color:#77718e;cursor:pointer;margin:2px 0
}
.nav:hover,.nav.active{
 background:#f0ebff;color:#6744e8;font-weight:bold
}
.main{flex:1;padding:30px;min-width:0}
.head{
 display:flex;justify-content:space-between;
 align-items:center;margin-bottom:25px
}
.head h2{margin:0;font-size:27px}
.cards{
 display:grid;grid-template-columns:repeat(4,1fr);gap:15px
}
.card{
 background:white;border:1px solid #ebe7f3;
 border-radius:15px;padding:20px
}
.stat b{font-size:30px;display:block;margin-top:12px}
.stat span{font-size:12px;color:#89849d}
.grid{
 display:grid;grid-template-columns:1.5fr 1fr;
 gap:18px;margin-top:18px
}
.panel h3{margin-top:0;font-size:15px}
.quick{
 display:grid;grid-template-columns:1fr 1fr;gap:10px
}
.quick button{
 padding:18px;text-align:left;border:1px solid #eee9f6;
 background:white;border-radius:12px;cursor:pointer
}
.quick button:hover{border-color:#b7a4f6}
.table-wrap{
 overflow:auto;background:white;border-radius:14px;
 border:1px solid #ebe7f3
}
table{width:100%;border-collapse:collapse;min-width:700px}
th,td{
 padding:13px;border-bottom:1px solid #eee;
 text-align:left;font-size:12px
}
th{font-size:9px;color:#9993aa;background:#faf9fd}
.status{
 padding:6px 9px;border-radius:20px;font-size:9px;font-weight:bold
}
.pending{background:#fff1cf;color:#a96d12}
.processing{background:#e8e5ff;color:#6547d6}
.completed{background:#dcf7e8;color:#218457}
.rejected{background:#ffe5e8;color:#bd3948}
.form-grid{
 display:grid;grid-template-columns:1fr 1fr;gap:0 18px
}
.fullrow{grid-column:1/-1}
.upload{
 border:2px dashed #d2c7f4;
 background:#faf8ff;border-radius:12px;
 padding:25px;text-align:center;margin-top:10px
}
.notice{
 background:#fff8e8;border:1px solid #ffe9bd;
 padding:14px;border-radius:10px;
 font-size:11px;margin-bottom:18px
}
.actions{
 display:flex;justify-content:flex-end;gap:10px;margin-top:20px
}
#toast{
 display:none;position:fixed;right:20px;bottom:20px;
 background:#211846;color:white;padding:13px 18px;
 border-radius:9px;z-index:100;font-size:12px
}

/* MOBILE */
.menu{display:none;border:0;background:none;font-size:23px}
@media(max-width:900px){
 .login-left{display:none}
 .login-right{width:100%}
 .menu{display:block}
 .sidebar{
  position:fixed;left:-260px;top:70px;bottom:0;
  z-index:10;transition:.2s;box-shadow:10px 0 30px #0001
 }
 .sidebar.open{left:0}
 .topbar{padding:0 15px}
 .topbar .search{display:none}
 .cards{grid-template-columns:1fr 1fr}
 .grid{grid-template-columns:1fr}
 .main{padding:18px}
}
@media(max-width:550px){
 .cards{grid-template-columns:1fr}
 .form-grid{grid-template-columns:1fr}
 .fullrow{grid-column:auto}
 .head{flex-direction:column;align-items:flex-start;gap:12px}
}
</style>
</head>

<body>

<div id="toast"></div>

<!-- LOGIN -->
<section id="login" class="login">

<div class="login-left">
 <div class="logo">
  <div class="logo-box">N+</div>
  <div>NOVA PAN DESK<br>
   <small>APPLICATION WORKSPACE</small>
  </div>
 </div>

 <h1>One workspace.<br>
 <span>Every application.</span></h1>

 <p>
 Manage PAN service requests, documents and application
 progress from one clean professional dashboard.
 </p>
</div>

<div class="login-right">
 <div class="login-card">
  <div class="logo">
   <div class="logo-box">N+</div>
   NOVA PAN DESK
  </div>

  <h2>Sign in</h2>
  <p class="muted">
   Enter your workspace credentials to continue.
  </p>

  <form id="loginForm">

   <label>User ID / Email</label>
   <input id="username" required placeholder="Enter user ID">

   <label>Password</label>
   <input id="password" type="password" required
          placeholder="Enter password">

   <button class="btn primary full">
    Sign in →
   </button>

  </form>

  <div class="demo">
   <b>Demo Login</b><br><br>
   User ID: <b>admin</b><br>
   Password: <b>admin123</b>
  </div>
 </div>
</div>

</section>


<!-- APPLICATION -->
<section id="application" class="hidden">

<header class="topbar">

 <button class="menu" onclick="toggleMenu()">☰</button>

 <div class="logo">
  <div class="logo-box">N+</div>
  <b>NOVA PAN DESK</b>
 </div>

 <div class="search">
  <input placeholder="Search application...">
 </div>

 <div class="user">
  ADMINISTRATOR
 </div>

 <button class="btn" onclick="logout()">Logout</button>

</header>


<div class="app">

<aside id="sidebar" class="sidebar">

 <div class="side-title">WORKSPACE</div>

 <button class="nav active" onclick="page('dashboard',this)">
  ▦ Overview
 </button>

 <div class="side-title">PAN SERVICES</div>

 <button class="nav" onclick="page('newpan',this)">
  ＋ New PAN Application
 </button>

 <button class="nav" onclick="page('correction',this)">
  ✎ PAN Correction
 </button>

 <button class="nav" onclick="page('reprint',this)">
  ▤ PAN Reprint
 </button>

 <div class="side-title">MANAGEMENT</div>

 <button class="nav" onclick="page('applications',this)">
  ☷ All Applications
 </button>

 <button class="nav" onclick="page('documents',this)">
  ▧ Documents
 </button>

 <button class="nav" onclick="page('settings',this)">
  ⚙ Settings
 </button>

</aside>


<main id="main" class="main"></main>

</div>
</section>


<script>

let applications =
 JSON.parse(localStorage.getItem("novaApplications") || "[]");

const $ = id => document.getElementById(id);

function save(){
 localStorage.setItem(
  "novaApplications",
  JSON.stringify(applications)
 );
}

function toast(text){
 const t=$("toast");
 t.innerText=text;
 t.style.display="block";
 setTimeout(()=>t.style.display="none",2500);
}


/* LOGIN */

$("loginForm").onsubmit=function(e){
 e.preventDefault();

 if(
   $("username").value==="admin" &&
   $("password").value==="admin123"
 ){
   $("login").classList.add("hidden");
   $("application").classList.remove("hidden");
   dashboard();
 }else{
   toast("Invalid login details");
 }
};


function logout(){
 location.reload();
}

function toggleMenu(){
 $("sidebar").classList.toggle("open");
}


/* PAGE */

function page(name,button){

 document.querySelectorAll(".nav")
 .forEach(x=>x.classList.remove("active"));

 if(button)button.classList.add("active");

 $("sidebar").classList.remove("open");

 if(name==="dashboard")dashboard();
 if(name==="newpan")form("NEW");
 if(name==="correction")form("CORRECTION");
 if(name==="reprint")form("REPRINT");
 if(name==="applications")applicationList();
 if(name==="documents")documents();
 if(name==="settings")settings();
}


/* DASHBOARD */

function dashboard(){

 let pending=applications.filter(x=>x.status==="Pending").length;
 let processing=applications.filter(x=>x.status==="Processing").length;
 let completed=applications.filter(x=>x.status==="Completed").length;

 $("main").innerHTML=`

 <div class="head">
  <div>
   <h2>Dashboard</h2>
   <p class="muted">
    Welcome to your PAN application workspace.
   </p>
  </div>

  <button class="btn primary"
   onclick="page('newpan')">
   + New Application
  </button>
 </div>


 <div class="cards">

  <div class="card stat">
   <span>Total Applications</span>
   <b>${applications.length}</b>
  </div>

  <div class="card stat">
   <span>Pending</span>
   <b>${pending}</b>
  </div>

  <div class="card stat">
   <span>Processing</span>
   <b>${processing}</b>
  </div>

  <div class="card stat">
   <span>Completed</span>
   <b>${completed}</b>
  </div>

 </div>


 <div class="grid">

  <div class="card panel">

   <h3>Recent Applications</h3>

   ${
    applications.length
    ? table(applications.slice(0,5))
    : `
    <div style="text-align:center;padding:40px">
     <h3>No Applications</h3>
     <p class="muted">
      Create your first application.
     </p>
     <button class="btn primary"
      onclick="page('newpan')">
      Create Application
     </button>
    </div>`
   }

  </div>


  <div class="card panel">

   <h3>Quick Services</h3>

   <div class="quick">

    <button onclick="page('newpan')">
     🪪<br><br>
     <b>New PAN</b><br>
     <small>New application</small>
    </button>

    <button onclick="page('correction')">
     ✎<br><br>
     <b>Correction</b><br>
     <small>Update details</small>
    </button>

    <button onclick="page('reprint')">
     ▤<br><br>
     <b>Reprint</b><br>
     <small>PAN reprint</small>
    </button>

    <button onclick="page('applications')">
     ☷<br><br>
     <b>Track</b><br>
     <small>Application status</small>
    </button>

   </div>

  </div>

 </div>

 `;
}


/* FORM */

function form(type){

 let title =
 type==="NEW" ? "New PAN Application" :
 type==="CORRECTION" ? "PAN Correction" :
 "PAN Reprint";

 $("main").innerHTML=`

 <div class="head">
  <div>
   <h2>${title}</h2>
   <p class="muted">
    Fill the application details carefully.
   </p>
  </div>
 </div>

 <div class="notice">
  <b>Demo mode:</b>
  Use sample data only. This frontend does not submit
  a real PAN application.
 </div>

 <form id="panForm" class="card">

  <h3>Applicant Details</h3>

  <div class="form-grid">

   <div>
    <label>Full Name *</label>
    <input id="name" required
     placeholder="Applicant full name">
   </div>

   <div>
    <label>Father / Parent Name *</label>
    <input id="parent" required
     placeholder="Parent name">
   </div>

   <div>
    <label>Date of Birth *</label>
    <input id="dob" type="date" required>
   </div>

   <div>
    <label>Mobile Number *</label>
    <input id="mobile" required
     maxlength="10"
     placeholder="10 digit mobile">
   </div>

   <div>
    <label>Email</label>
    <input id="email"
     type="email"
     placeholder="Email address">
   </div>

   <div>
    <label>Existing PAN / Reference</label>
    <input id="reference"
     placeholder="Demo reference only">
   </div>

   <div class="fullrow">
    <label>Full Address *</label>
    <textarea id="address" required
     placeholder="Complete address"></textarea>
   </div>

   ${
    type==="CORRECTION"
    ? `
    <div>
     <label>Correction Type</label>
     <select id="correction">
      <option>Name</option>
      <option>Date of Birth</option>
      <option>Father Name</option>
      <option>Address</option>
      <option>Other</option>
     </select>
    </div>`
    : ""
   }

  </div>


  <h3 style="margin-top:30px">
   Documents
  </h3>

  <div class="upload">

   <b>Upload Supporting Documents</b>

   <p class="muted">
    PDF / JPG / PNG
   </p>

   <input id="files"
    type="file"
    multiple
    accept=".pdf,.jpg,.jpeg,.png">

  </div>


  <div class="actions">

   <button type="button"
    class="btn"
    onclick="dashboard()">
    Cancel
   </button>

   <button class="btn primary">
    Save Application →
   </button>

  </div>

 </form>
 `;


 $("panForm").onsubmit=function(e){

  e.preventDefault();

  const id=
   "NOVA-"+Date.now().toString().slice(-7);

  applications.unshift({

   id:id,
   type:type,
   name:$("name").value,
   parent:$("parent").value,
   dob:$("dob").value,
   mobile:$("mobile").value,
   email:$("email").value,
   reference:$("reference").value,
   address:$("address").value,

   files:[
    ...$("files").files
   ].map(x=>x.name),

   status:"Pending",
   date:new Date().toLocaleString()

  });

  save();

  toast("Application created: "+id);

  setTimeout(applicationList,500);
 };
}


/* APPLICATION TABLE */

function table(list){

 return `
 <div class="table-wrap">

 <table>

 <tr>
  <th>APPLICATION ID</th>
  <th>APPLICANT</th>
  <th>SERVICE</th>
  <th>STATUS</th>
 </tr>

 ${
 list.map(x=>`

 <tr>

  <td><b style="color:#6744e8">
   ${x.id}
  </b></td>

  <td>
   <b>${escapeHTML(x.name)}</b><br>
   ${x.mobile}
  </td>

  <td>
   ${serviceName(x.type)}
  </td>

  <td>
   ${status(x.status)}
  </td>

 </tr>

 `).join("")
 }

 </table>

 </div>
 `;
}


function applicationList(){

 $("main").innerHTML=`

 <div class="head">

  <div>
   <h2>All Applications</h2>
   <p class="muted">
    Manage application records.
   </p>
  </div>

  <button class="btn primary"
   onclick="page('newpan')">
   + New Application
  </button>

 </div>

 <div class="table-wrap">

 ${table(applications)}

 </div>

 `;
}


function serviceName(type){

 if(type==="NEW")return "New PAN";
 if(type==="CORRECTION")return "PAN Correction";
 return "PAN Reprint";
}


function status(s){

 return `
 <span class="status ${s.toLowerCase()}">
 ${s}
 </span>
 `;
}


/* DOCUMENTS */

function documents(){

 let rows=[];

 applications.forEach(a=>{
  (a.files||[]).forEach(f=>{
   rows.push(`
   <tr>
    <td>${a.id}</td>
    <td>${escapeHTML(a.name)}</td>
    <td>${escapeHTML(f)}</td>
    <td>Filename only</td>
   </tr>
   `);
  });
 });

 $("main").innerHTML=`

 <div class="head">
  <div>
   <h2>Document Register</h2>
   <p class="muted">
    Selected document filenames.
   </p>
  </div>
 </div>

 <div class="notice">
  Files are not securely uploaded in this frontend demo.
 </div>

 <div class="table-wrap">

 <table>

 <tr>
  <th>APPLICATION</th>
  <th>APPLICANT</th>
  <th>FILE</th>
  <th>TYPE</th>
 </tr>

 ${rows.join("")}

 </table>

 </div>
 `;
}


/* SETTINGS */

function settings(){

 $("main").innerHTML=`

 <div class="head">

  <div>
   <h2>Workspace Settings</h2>
   <p class="muted">
    Account and production information.
   </p>
  </div>

 </div>

 <div class="grid">

  <div class="card">

   <h3>Administrator</h3>

   <label>Login ID</label>
   <input value="admin" readonly>

   <label>Account Type</label>
   <input value="Administrator" readonly>

   <label>Portal</label>
   <input value="Nova PAN Desk" readonly>

  </div>


  <div class="card">

   <h3>Production Requirements</h3>

   <p class="muted">
    Secure backend<br><br>
    Database<br><br>
    Authorized PAN API<br><br>
    Secure document storage<br><br>
    Payment gateway<br><br>
    HTTPS and authentication
   </p>

  </div>

 </div>

 `;
}


function escapeHTML(str){

 return String(str||"")
 .replace(/[&<>"']/g,m=>({
  "&":"&amp;",
  "<":"&lt;",
  ">":"&gt;",
  '"':"&quot;",
  "'":"&#039;"
 }[m]));

}

</script>

</body>
</html>
