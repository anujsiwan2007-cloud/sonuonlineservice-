<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JPU Chhapra | Question Bank</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f2f5ff;color:#172554}
header{background:linear-gradient(135deg,#101d55,#2563eb,#7c3aed);color:white;text-align:center;padding:30px 15px}
header h1{margin:0;font-size:32px}
header p{margin-bottom:0}
main{max-width:1000px;margin:20px auto;padding:0 12px}
.box{background:white;padding:18px;margin-bottom:16px;border-radius:16px;box-shadow:0 5px 18px #0000000d}
h2{font-size:20px;margin-top:0}
select,input{width:100%;padding:13px;margin:6px 0 12px;border:1px solid #d4dcf5;border-radius:10px;font-size:15px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
button{padding:13px;border:1px solid #dbe4ff;background:#edf2ff;color:#1d3b91;border-radius:12px;font-weight:bold;cursor:pointer}
button:hover,button.active{background:#2563eb;color:white}
.subjects{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.qa{border:1px solid #dbe4f5;border-radius:12px;margin:12px 0;overflow:hidden}
.question{background:#eaf0ff;padding:14px;font-weight:bold}
.answer{padding:14px;line-height:1.7}
a{color:#2563eb}
footer{text-align:center;padding:20px;color:#64748b;font-size:13px}
@media(max-width:600px){.grid{grid-template-columns:1fr}.subjects{grid-template-columns:repeat(2,1fr)}header h1{font-size:27px}}
</style>
</head>
<body>

<header>
<h1>🎓 JPU CHHAPRA</h1>
<p>All Subjects | All Semesters | Question & Answer</p>
</header>

<main>
<section class="box">
<h2>📚 Select Your Course</h2>

<label>Course</label>
<select id="course">
<option>B.Sc.</option>
<option>B.A.</option>
<option>B.Com.</option>
</select>

<div class="grid">
<div>
<label>Year</label>
<select id="year">
<option value="1">1st Year</option>
<option value="2" selected>2nd Year</option>
<option value="3">3rd Year</option>
<option value="4">4th Year</option>
</select>
</div>

<div>
<label>Semester</label>
<select id="semester">
<option value="1">Semester 1</option>
<option value="2">Semester 2</option>
<option value="3" selected>Semester 3</option>
<option value="4">Semester 4</option>
<option value="5">Semester 5</option>
<option value="6">Semester 6</option>
<option value="7">Semester 7</option>
<option value="8">Semester 8</option>
</select>
</div>

<div>
<label>Search</label>
<input id="search" placeholder="Search question...">
</div>
</div>
<p id="selection"></p>
</section>

<section class="box">
<h2>📖 Select Subject</h2>
<div id="subjects" class="subjects"></div>
</section>

<section class="box">
<h2 id="heading">Question & Answer</h2>
<div id="questions"></div>
<p><a href="https://www.jpv.ac.in/syllabi" target="_blank" rel="noopener">Open Official JPU Syllabus ↗</a></p>
</section>
</main>

<footer>
JPU CHHAPRA | Student Study Portal<br>
Independent educational website; not an official university website.
</footer>

<script>
const subjects={
"B.Sc.":["Zoology","Botany","Physics","Chemistry","Mathematics","Statistics","Geology","Computer Science"],
"B.A.":["Hindi","English","History","Political Science","Geography","Economics","Psychology","Sociology","Philosophy","Sanskrit"],
"B.Com.":["Accountancy","Business Studies","Economics","Business Law","Finance","Management"]
};

const data={
"Zoology":[
{q:"What is Zoology?",a:"Zoology is the branch of biology that deals with the study of animals. / प्राणी विज्ञान जीव विज्ञान की वह शाखा है जिसमें जानवरों का अध्ययन किया जाता है।"},
{q:"What is a cell?",a:"A cell is the basic structural and functional unit of life. / कोशिका जीवन की मूल संरचनात्मक और क्रियात्मक इकाई है।"},
{q:"What is a vertebrate?",a:"A vertebrate is an animal that has a backbone. / कशेरुकी वह जीव है जिसमें रीढ़ की हड्डी होती है।"},
{q:"What is an ecosystem?",a:"An ecosystem includes living organisms and their physical environment. / पारितंत्र में जीव और उनका भौतिक पर्यावरण शामिल होते हैं।"}
],
"Botany":[
{q:"What is Botany?",a:"Botany is the branch of biology that studies plants. / वनस्पति विज्ञान में पौधों का अध्ययन किया जाता है।"},
{q:"What is photosynthesis?",a:"Photosynthesis is the process by which green plants make food using light energy. / प्रकाश संश्लेषण में हरे पौधे प्रकाश की ऊर्जा से भोजन बनाते हैं।"}
],
"Physics":[
{q:"What is force?",a:"Force is a push or pull that can change the motion of an object. / बल धक्का या खिंचाव है जो किसी वस्तु की गति बदल सकता है।"},
{q:"What is the SI unit of force?",a:"The SI unit of force is Newton (N). / बल की SI इकाई न्यूटन है।"}
],
"Chemistry":[
{q:"What is an atom?",a:"An atom is the smallest unit of an element that retains its chemical identity. / परमाणु किसी तत्व की सबसे छोटी इकाई है जो उसकी रासायनिक पहचान बनाए रखती है।"},
{q:"What is a molecule?",a:"A molecule consists of two or more atoms chemically bonded together. / अणु दो या अधिक रासायनिक रूप से जुड़े परमाणुओं से बनता है।"}
],
"Mathematics":[
{q:"What is a set?",a:"A set is a well-defined collection of distinct objects. / समुच्चय अलग-अलग वस्तुओं का स्पष्ट रूप से परिभाषित संग्रह है।"},
{q:"What is a matrix?",a:"A matrix is a rectangular arrangement of elements in rows and columns. / आव्यूह पंक्तियों और स्तंभों में तत्वों की आयताकार व्यवस्था है।"}
]
};

let selected="Zoology";

function renderSubjects(){
const course=document.getElementById("course").value;
const list=subjects[course];

if(!list.includes(selected)) selected=list[0];

document.getElementById("subjects").innerHTML=list.map(s=>
`<button class="${s===selected?'active':''}" onclick="chooseSubject('${s}')">${s}</button>`
).join("");

renderQuestions();
}

function chooseSubject(s){
selected=s;
renderSubjects();
}

function renderQuestions(){
const course=document.getElementById("course").value;
const year=document.getElementById("year").value;
const semester=document.getElementById("semester").value;
const term=document.getElementById("search").value.toLowerCase();

document.getElementById("selection").textContent=
`${course} | Year ${year} | Semester ${semester}`;

document.getElementById("heading").textContent=
selected+" — Question & Answer";

const list=(data[selected]||[]).filter(item=>
(item.q+" "+item.a).toLowerCase().includes(term)
);

if(list.length===0){
document.getElementById("questions").innerHTML=
"<p>इस विषय के प्रश्न-उत्तर अभी नहीं जोड़े गए हैं। इस विषय का सही सिलेबस देखकर प्रश्न-उत्तर जोड़ें।</p>";
return;
}

document.getElementById("questions").innerHTML=list.map((item,i)=>
`<div class="qa">
<div class="question">Q${i+1}. ${item.q}</div>
<div class="answer"><b>Answer:</b> ${item.a}</div>
</div>`
).join("");
}

["course","year","semester"].forEach(id=>
document.getElementById(id).addEventListener("change",renderSubjects)
);

document.getElementById("search").addEventListener("input",renderQuestions);

renderSubjects();
</script>
</body>
</html>
