# my-portfolio


<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Aditya Singh | Freelance Web Developer</title>

<meta name="description" content="Aditya Singh - Freelance Web Developer, Portfolio Designer & Digital Creator. Premium websites for businesses and creators.">

<meta name="keywords" content="Web Developer, Portfolio Website, Freelance Developer, QR Menu Website, Business Website">

<meta name="author" content="Aditya Singh">

<meta property="og:title" content="Aditya Singh | Freelance Web Developer">

<meta property="og:description" content="Premium websites for businesses & creators">

<meta property="og:type" content="website">

<meta property="og:image" content="https://images.unsplash.com/photo-1498050108023-c5249f4df085"> 

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

html{
scroll-behavior:smooth;
}

body{
background:#020617;
color:white;
overflow-x:hidden;
}

::selection{
background:#38bdf8;
color:white;
}

/* LOADER */

#loader{
position:fixed;
width:100%;
height:100%;
background:#020617;
display:flex;
justify-content:center;
align-items:center;
z-index:99999;
}

.spinner{
width:60px;
height:60px;
border:5px solid rgba(255,255,255,.1);
border-top:5px solid #38bdf8;
border-radius:50%;
animation:spin 1s linear infinite;
}

@keyframes spin{
100%{
transform:rotate(360deg);
}
}

/* BACKGROUND */

.bg{
position:fixed;
width:100%;
height:100%;
z-index:-1;
overflow:hidden;
}

.circle{
position:absolute;
border-radius:50%;
filter:blur(100px);
opacity:.4;
animation:float 8s infinite alternate;
}

.circle:nth-child(1){
width:300px;
height:300px;
background:#38bdf8;
top:-100px;
left:-100px;
}

.circle:nth-child(2){
width:250px;
height:250px;
background:#818cf8;
bottom:-100px;
right:-50px;
}

@keyframes float{
from{
transform:translateY(0px);
}
to{
transform:translateY(40px);
}
}

/* SCROLL BAR */

.progress{
position:fixed;
top:0;
left:0;
width:0%;
height:4px;
background:#38bdf8;
z-index:999;
}

/* NAVBAR */

nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 10%;
position:sticky;
top:0;
backdrop-filter:blur(12px);
background:rgba(255,255,255,0.05);
border-bottom:1px solid rgba(255,255,255,0.08);
z-index:100;
}

.logo{
font-size:24px;
font-weight:700;
}

nav a{
text-decoration:none;
color:white;
margin-left:20px;
transition:.3s;
position:relative;
}

nav a::after{
content:'';
position:absolute;
left:0;
bottom:-5px;
width:0%;
height:2px;
background:#38bdf8;
transition:.3s;
}

nav a:hover::after,
nav a.active::after{
width:100%;
}

nav a:hover,
nav a.active{
color:#38bdf8;
}

/* HERO */

.hero{
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
padding:20px;
}

.badge{
display:inline-block;
padding:8px 18px;
border-radius:30px;
background:rgba(56,189,248,.15);
border:1px solid rgba(56,189,248,.3);
color:#38bdf8;
margin-bottom:20px;
font-size:14px;
}

.hero h1{
font-size:70px;
line-height:1.1;
margin-bottom:20px;
}

.hero span{
background:linear-gradient(90deg,#38bdf8,#818cf8);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.hero p{
max-width:750px;
color:#cbd5e1;
font-size:18px;
}

.hero-buttons{
margin-top:30px;
}

.btn{
padding:14px 30px;
border:none;
border-radius:50px;
cursor:pointer;
font-size:16px;
margin:10px;
transition:.3s;
font-weight:600;
}

.primary{
background:linear-gradient(90deg,#38bdf8,#818cf8);
color:white;
}

.secondary{
background:transparent;
border:1px solid rgba(255,255,255,0.2);
color:white;
}

.btn:hover{
transform:translateY(-5px) scale(1.03);
box-shadow:0 15px 40px rgba(56,189,248,.35);
}

/* TRUST */

.trust{
display:flex;
gap:15px;
flex-wrap:wrap;
justify-content:center;
margin-top:30px;
}

.trust div{
background:rgba(255,255,255,0.05);
padding:10px 18px;
border-radius:30px;
font-size:14px;
color:#cbd5e1;
border:1px solid rgba(255,255,255,0.08);
}

/* STATS */

.stats{
display:flex;
justify-content:center;
gap:25px;
margin-top:50px;
flex-wrap:wrap;
}

.stat{
background:rgba(255,255,255,0.05);
padding:20px 30px;
border-radius:20px;
backdrop-filter:blur(10px);
}

.stat h2{
color:#38bdf8;
}

/* SECTION */

section{
padding:100px 10%;
}

.title{
text-align:center;
font-size:42px;
margin-bottom:50px;
background:linear-gradient(90deg,#38bdf8,#818cf8);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

/* GRID */

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
}

/* CARDS */

.card{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.08);
padding:30px;
border-radius:25px;
backdrop-filter:blur(10px);
transition:.4s;
position:relative;
overflow:hidden;
}

.card::before{
content:'';
position:absolute;
top:0;
left:-100%;
width:100%;
height:100%;
background:linear-gradient(
90deg,
transparent,
rgba(255,255,255,.08),
transparent
);
transition:.7s;
}

.card:hover::before{
left:100%;
}

.card:hover{
transform:translateY(-12px) scale(1.02);
box-shadow:0 20px 40px rgba(56,189,248,.25);
border-color:#38bdf8;
}

.card h3{
margin-bottom:15px;
}

.card p{
color:#cbd5e1;
}

/* PROJECTS */

.project-img{
width:100%;
border-radius:18px;
margin-bottom:15px;
transition:.5s;
}

.card:hover .project-img{
transform:scale(1.06);
}

/* CTA */

.cta{
text-align:center;
padding:60px;
border-radius:30px;
background:linear-gradient(90deg,#38bdf8,#818cf8);
color:black;
}

.cta h2{
font-size:42px;
}

.cta p{
margin-top:15px;
font-size:18px;
}

/* CONTACT */

.contact-form{
max-width:600px;
margin:auto;
background:rgba(255,255,255,0.05);
padding:40px;
border-radius:25px;
border:1px solid rgba(255,255,255,0.08);
}

.form-group{
margin-bottom:20px;
}

.form-group input,
.form-group textarea{
width:100%;
padding:14px;
background:rgba(255,255,255,.08);
border:1px solid rgba(255,255,255,.1);
border-radius:12px;
color:white;
font-size:14px;
}

.form-group textarea{
resize:none;
height:140px;
}

.form-group input:focus,
.form-group textarea:focus{
outline:none;
border-color:#38bdf8;
}

/* SOCIAL */

#socials a{
text-decoration:none;
color:white;
}

/* WHATSAPP */

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
padding:16px;
border-radius:50%;
text-decoration:none;
color:white;
font-size:22px;
box-shadow:0 10px 30px rgba(0,0,0,.3);
animation:pulse 2s infinite;
transition:.3s;
}

.whatsapp:hover{
transform:scale(1.12) rotate(8deg);
}

@keyframes pulse{
0%{
box-shadow:0 0 0 0 rgba(37,211,102,.5);
}
70%{
box-shadow:0 0 0 18px rgba(37,211,102,0);
}
100%{
box-shadow:0 0 0 0 rgba(37,211,102,0);
}
}

/* FOOTER */

footer{
text-align:center;
padding:30px;
color:#94a3b8;
}

/* RESPONSIVE */

@media(max-width:768px){

.hero h1{
font-size:42px;
}

.title{
font-size:30px;
}

nav{
padding:15px 5%;
flex-direction:column;
gap:10px;
}

nav div:last-child{
display:flex;
flex-wrap:wrap;
justify-content:center;
}

}

</style>
</head>

<body>

<!-- LOADER -->

<div id="loader">
<div class="spinner"></div>
</div>

<!-- BACKGROUND -->

<div class="bg">
<div class="circle"></div>
<div class="circle"></div>
</div>

<div class="progress" id="progress"></div>

<!-- NAVBAR -->

<nav>

<div class="logo">
Aditya
</div>

<div>
<a href="#services">Services</a>
<a href="#projects">Projects</a>
<a href="#pricing">Pricing</a>
<a href="#contact">Contact</a>
</div>

</nav>

<!-- HERO -->

<section class="hero">

<div class="badge">
🚀 Freelance Developer & Digital Creator
</div>

<h1 data-aos="fade-up">
I Build <span id="typing"></span><br>
For Businesses & Creators
</h1>

<p data-aos="fade-up" data-aos-delay="200">
Helping businesses and creators build premium digital experiences that attract customers and grow online.
</p>

<div class="hero-buttons">

<a href="https://wa.me/917827362981" target="_blank" rel="noopener noreferrer">

<button class="btn primary">
🚀 Hire Me
</button>

</a>

<a href="#services">

<button class="btn secondary">
View Services
</button>

</a>

</div>

<div class="trust">

<div>✔ SEO Friendly</div>
<div>✔ Fast Loading</div>
<div>✔ Premium UI/UX</div>
<div>✔ Mobile Responsive</div>

</div>

<div class="stats">

<div class="stat">
<h2>10+</h2>
<p>Projects</p>
</div>

<div class="stat">
<h2>100%</h2>
<p>Responsive</p>
</div>

<div class="stat">
<h2>24/7</h2>
<p>Support</p>
</div>

</div>

</section>

<!-- SERVICES -->

<section id="services">

<h2 class="title">
Services
</h2>

<div class="grid">

<div class="card">
<h3>🌐 Business Website</h3>
<p>Premium responsive websites for businesses.</p>
</div>

<div class="card">
<h3>🎨 Logo Design</h3>
<p>Professional modern logos and branding.</p>
</div>

<div class="card">
<h3>📱 Social Media Design</h3>
<p>Instagram posts, ads and branding content.</p>
</div>

<div class="card">
<h3>▶ YouTube Thumbnails</h3>
<p>High CTR modern thumbnails.</p>
</div>

<div class="card">
<h3>💼 Portfolio Websites</h3>
<p>Modern portfolio websites for creators.</p>
</div>

<div class="card">
<h3>🍽 QR Menu Websites</h3>
<p>Digital restaurant menu systems.</p>
</div>

</div>

</section>

<!-- PROJECTS -->

<section id="projects">

<h2 class="title">
Recent Projects
</h2>

<div class="grid">

<div class="card">

<img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1200&auto=format&fit=crop" class="project-img">

<h3>🏋 Gym Website</h3>

<p>Modern fitness website with WhatsApp support.</p>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?q=80&w=1200&auto=format&fit=crop" class="project-img">

<h3>🍽 QR Menu Website</h3>

<p>Restaurant digital menu website.</p>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1499750310107-5fef28a66643?q=80&w=1200&auto=format&fit=crop" class="project-img">

<h3>💼 Creator Portfolio</h3>

<p>Animated portfolio for creators.</p>

</div>

</div>

</section>

<!-- PRICING -->

<section id="pricing">

<h2 class="title">
Pricing
</h2>

<div class="grid">

<div class="card">
<h3>Basic</h3>
<h1 style="color:#38bdf8;">₹2,999</h1>
<p>Single Page Website</p>
</div>

<div class="card">
<h3>Standard</h3>
<h1 style="color:#38bdf8;">₹6,999</h1>
<p>Business Website + Animations</p>
</div>

<div class="card">
<h3>Premium</h3>
<h1 style="color:#38bdf8;">₹12,999</h1>
<p>Full Premium Website + Branding</p>
</div>

</div>

</section>

<!-- SOCIAL -->

<section id="socials">

<h2 class="title">
Connect With Me
</h2>

<div class="grid">

<a href="https://www.instagram.com/aadirk.growth?igsh=NDF5NDRkcmVzYnFh"
target="_blank"
rel="noopener noreferrer">

<div class="card">

<h3>📸 Instagram</h3>

<p>
DM for projects and collaborations.
</p>

</div>

</a>

<a href="https://github.com/"
target="_blank"
rel="noopener noreferrer">

<div class="card">

<h3>💻 GitHub</h3>

<p>
View coding projects and portfolio work.
</p>

</div>

</a>

<a href="https://linkedin.com/"
target="_blank"
rel="noopener noreferrer">

<div class="card">

<h3>💼 LinkedIn</h3>

<p>
Professional networking and business profile.
</p>

</div>

</a>

</div>

</section>

<!-- CTA -->

<section>

<div class="cta">

<h2>
🎁 Free Homepage Demo Available
</h2>

<p>
Get a free homepage demo before placing your order.
</p>

<br>

<a href="https://wa.me/917827362981" target="_blank" rel="noopener noreferrer">

<button class="btn primary">
🚀 Start Your Project
</button>

</a>

</div>

</section>

<!-- CONTACT -->

<section id="contact">

<h2 class="title">
Contact Me
</h2>

<form class="contact-form"
action="https://formsubmit.co/adityassgj952@gmail.com"
method="POST">

<input type="hidden" name="_captcha" value="false">

<div class="form-group">
<input type="text" name="name" placeholder="Your Name" required>
</div>

<div class="form-group">
<input type="email" name="email" placeholder="Your Email" required>
</div>

<div class="form-group">
<input type="text" name="subject" placeholder="Subject" required>
</div>

<div class="form-group">
<textarea name="message" placeholder="Your Message" required></textarea>
</div>

<button type="submit" class="btn primary">
✉ Send Message
</button>

</form>

</section>

<!-- WHATSAPP -->

<a href="https://wa.me/917827362981"
class="whatsapp"
target="_blank"
rel="noopener noreferrer">

💬

</a>

<!-- FOOTER -->

<footer>

© 2026 Aditya Singh • All Rights Reserved

</footer>

<!-- AOS -->

<script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>

<script>

/* LOADER */

window.addEventListener("load", ()=>{

document.getElementById("loader").style.display = "none";

});

/* AOS */

AOS.init({
duration:1000,
once:true
});

/* SCROLL PROGRESS */

window.onscroll = ()=>{

let winScroll =
document.body.scrollTop ||
document.documentElement.scrollTop;

let height =
document.documentElement.scrollHeight -
document.documentElement.clientHeight;

let scrolled = (winScroll / height) * 100;

document.getElementById("progress").style.width =
scrolled + "%";

};

/* ACTIVE NAV */

const sections = document.querySelectorAll("section");
const navLinks = document.querySelectorAll("nav a");

window.addEventListener("scroll", ()=>{

let current = "";

sections.forEach(section=>{

const sectionTop = section.offsetTop;

if(pageYOffset >= sectionTop - 200){
current = section.getAttribute("id");
}

});

navLinks.forEach(a=>{

a.classList.remove("active");

if(a.getAttribute("href").includes(current)){
a.classList.add("active");
}

});

});

/* TYPING EFFECT */

const texts = [
"Premium Websites",
"Modern Brands",
"Digital Experiences"
];

let count = 0;
let index = 0;
let currentText = '';
let letter = '';

(function type(){

if(count === texts.length){
count = 0;
}

currentText = texts[count];
letter = currentText.slice(0, ++index);

document.getElementById('typing').textContent = letter;

if(letter.length === currentText.length){

count++;

index = 0;

setTimeout(type, 1500);

}else{

setTimeout(type, 100);

}

})();

</script>

</body>
</html>