# freshbin-website-3
freshcan express
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FreshBin | Trash Bin Cleaning</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Inter',sans-serif;
scroll-behavior:smooth;
}

body{
background:#f6f9fc;
color:#1d2939;
overflow-x:hidden;
}

section{
padding:90px 8%;
}

h1,h2,h3{
font-weight:700;
}

p{
line-height:1.7;
color:#667085;
}

a{
text-decoration:none;
color:inherit;
}

/* Navigation */

header{
position:fixed;
top:0;
left:0;
width:100%;
height:80px;
background:rgba(255,255,255,.85);
backdrop-filter:blur(16px);
display:flex;
align-items:center;
justify-content:space-between;
padding:0 8%;
z-index:1000;
box-shadow:0 10px 30px rgba(0,0,0,.05);
}

.logo{
font-size:1.7rem;
font-weight:800;
color:#2F80ED;
}

nav{
display:flex;
gap:35px;
align-items:center;
}

nav a{
font-weight:600;
transition:.3s;
position:relative;
}

nav a:hover{
color:#2F80ED;
}

nav a::after{
content:"";
position:absolute;
left:0;
bottom:-6px;
width:0%;
height:2px;
background:#2F80ED;
transition:.3s;
}

nav a:hover::after{
width:100%;
}

.button{
background:#2F80ED;
color:white;
padding:14px 26px;
border-radius:50px;
font-weight:600;
transition:.35s;
box-shadow:0 15px 30px rgba(47,128,237,.25);
}

.button:hover{
transform:translateY(-4px);
background:#1f6de0;
}

/* Home */

#home{
padding-top:150px;
display:grid;
grid-template-columns:1fr 1fr;
gap:60px;
align-items:center;
min-height:100vh;
}

.home-text h1{
font-size:3.8rem;
margin-bottom:25px;
line-height:1.1;
}

.home-text span{
color:#2F80ED;
}

.home-text p{
font-size:1.1rem;
margin-bottom:35px;
max-width:520px;
}

.home-buttons{
display:flex;
gap:20px;
flex-wrap:wrap;
}

.secondary{
padding:14px 26px;
border-radius:50px;
background:white;
border:2px solid #d0d5dd;
font-weight:600;
transition:.3s;
}

.secondary:hover{
border-color:#2F80ED;
color:#2F80ED;
}

.home-image{
display:flex;
justify-content:center;
align-items:center;
}

.circle{
width:430px;
height:430px;
border-radius:50%;
background:linear-gradient(145deg,#2F80ED,#80C7FF);
display:flex;
align-items:center;
justify-content:center;
box-shadow:0 35px 80px rgba(47,128,237,.35);
animation:float 5s ease-in-out infinite;
}

.circle::before{
content:"🗑️";
font-size:150px;
background:white;
width:260px;
height:260px;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
}

@keyframes float{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-18px);}
}

/* Cards */

.title{
text-align:center;
margin-bottom:60px;
}

.title h2{
font-size:2.5rem;
margin-bottom:15px;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
}

.card{
background:rgba(255,255,255,.8);
backdrop-filter:blur(20px);
padding:35px;
border-radius:24px;
box-shadow:0 20px 40px rgba(0,0,0,.06);
transition:.35s;
}

.card:hover{
transform:translateY(-12px);
}

.icon{
font-size:3rem;
margin-bottom:20px;
}

.card h3{
margin-bottom:15px;
}

/* About */

.about{
display:grid;
grid-template-columns:1fr 1fr;
gap:60px;
align-items:center;
}

.about-box{
background:white;
padding:45px;
border-radius:25px;
box-shadow:0 25px 40px rgba(0,0,0,.05);
}

.about-box ul{
margin-top:20px;
padding-left:20px;
}

.about-box li{
margin:14px 0;
color:#667085;
}

/* Pricing */

.pricing{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
}

.price{
background:white;
padding:40px;
border-radius:25px;
text-align:center;
box-shadow:0 20px 40px rgba(0,0,0,.06);
transition:.3s;
}

.price:hover{
transform:translateY(-10px);
}

.price h3{
margin-bottom:15px;
}

.cost{
font-size:3rem;
color:#2F80ED;
font-weight:800;
margin:20px 0;
}

.price ul{
list-style:none;
margin-bottom:30px;
}

.price li{
padding:10px;
border-bottom:1px solid #eee;
}
/* FAQ */

.faq{
max-width:900px;
margin:auto;
}

.faq-item{
background:white;
border-radius:20px;
padding:22px;
margin-bottom:18px;
box-shadow:0 15px 35px rgba(0,0,0,.05);
cursor:pointer;
transition:.3s;
}

.faq-item h3{
display:flex;
justify-content:space-between;
align-items:center;
font-size:1.1rem;
}

.faq-answer{
max-height:0;
overflow:hidden;
transition:.4s;
padding-top:0;
color:#667085;
}

.faq-item.active .faq-answer{
max-height:200px;
padding-top:18px;
}

/* Contact */

.contact-grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:40px;
}

.contact-card{
background:white;
padding:40px;
border-radius:25px;
box-shadow:0 20px 40px rgba(0,0,0,.05);
}

form{
display:flex;
flex-direction:column;
gap:18px;
}

input,
textarea{
padding:16px;
border-radius:14px;
border:1px solid #d0d5dd;
font-size:1rem;
outline:none;
transition:.3s;
}

input:focus,
textarea:focus{
border-color:#2F80ED;
box-shadow:0 0 0 4px rgba(47,128,237,.15);
}

textarea{
resize:vertical;
min-height:150px;
}

button{
border:none;
cursor:pointer;
}

/* Footer */

footer{
padding:40px;
text-align:center;
background:white;
margin-top:80px;
color:#667085;
}

/* Scroll Animation */

.fade{
opacity:0;
transform:translateY(40px);
transition:1s;
}

.fade.show{
opacity:1;
transform:translateY(0);
}

/* Responsive */

@media(max-width:900px){

#home,
.about,
.contact-grid{
grid-template-columns:1fr;
}

.home-text{
text-align:center;
}

.home-text p{
margin:auto;
margin-bottom:30px;
}

.home-buttons{
justify-content:center;
}

.circle{
width:300px;
height:300px;
}

.circle::before{
width:180px;
height:180px;
font-size:90px;
}

nav{
display:none;
}

}

</style>

</head>

<body>

<header>

<div class="logo">
FreshBin
</div>

<nav>

<a href="#home">Home</a>
<a href="#services">Services</a>
<a href="#about">About</a>
<a href="#pricing">Pricing</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<a href="#contact" class="button">
Book Now
</a>

</nav>

</header>

<section id="home">

<div class="home-text fade">

<h1>
Keeping Your <span>Trash Bins</span> Cleaner Than Ever
</h1>

<p>
FreshBin provides professional trash bin cleaning, sanitizing,
and deodorizing services for homes and businesses. We eliminate
odor, bacteria, and grime so your bins stay fresh all year.
</p>

<div class="home-buttons">

<a href="#contact" class="button">
Schedule Service
</a>

<a href="#services" class="secondary">
Our Services
</a>

</div>

</div>

<div class="home-image fade">

<div class="circle"></div>

</div>

</section>

<section id="services">

<div class="title fade">

<h2>Our Services</h2>

<p>
Professional cleaning solutions for every type of trash container.
</p>

</div>

<div class="cards">

<div class="card fade">

<div class="icon">🧼</div>

<h3>Deep Cleaning</h3>

<p>
High-pressure washing removes built-up dirt, grime, and residue.
</p>

</div>

<div class="card fade">

<div class="icon">🦠</div>

<h3>Sanitizing</h3>

<p>
Commercial disinfectants eliminate harmful bacteria and germs.
</p>

</div>

<div class="card fade">

<div class="icon">🌿</div>

<h3>Odor Removal</h3>

<p>
Eco-friendly deodorizing leaves every bin smelling fresh.
</p>

</div>

</div>

</section>

<section id="about">

<div class="about">

<div class="about-box fade">

<h2>About FreshBin</h2>

<p>

We believe every neighborhood deserves cleaner, healthier trash
bins. Using modern equipment and environmentally friendly
cleaners, our team delivers dependable service with every visit.

</p>

<ul>

<li>✔ Eco-Friendly Products</li>

<li>✔ Affordable Monthly Plans</li>

<li>✔ Reliable Scheduling</li>

<li>✔ Residential & Commercial Service</li>

</ul>

</div>

<div class="about-box fade">

<h2>Why Choose Us?</h2>

<p>

Our futuristic cleaning process combines high-pressure washing,
professional sanitizing, and odor treatment for a complete
restoration of your bins.

</p>

</div>

</div>

</section>

<section id="pricing">

<div class="title fade">

<h2>Pricing</h2>

<p>
Simple pricing with no hidden fees.
</p>

</div>

<div class="pricing">

<div class="price fade">

<h3>Single Clean</h3>

<div class="cost">$20</div>

<ul>

<li>1 Bin</li>
<li>Sanitized</li>
<li>Odor Removal</li>

</ul>

<a href="#contact" class="button">
Book
</a>

</div>

<div class="price fade">

<h3>Monthly</h3>

<div class="cost">$35</div>

<ul>

<li>2 Bins</li>
<li>Monthly Cleaning</li>
<li>Priority Service</li>

</ul>

<a href="#contact" class="button">
Book
</a>

</div>

<div class="price fade">

<h3>Business</h3>

<div class="cost">Call</div>

<ul>

<li>Custom Plans</li>
<li>Commercial Service</li>
<li>Bulk Pricing</li>

</ul>

<a href="#contact" class="button">
Contact
</a>

</div>

</div>

</section><section id="faq">

    <div class="title fade">
        <h2>Frequently Asked Questions</h2>
        <p>Answers to the questions we hear the most.</p>
    </div>

    <div class="faq">

        <div class="faq-item">
            <h3>How often should my trash bins be cleaned?<span>+</span></h3>
            <div class="faq-answer">
                <p>Most customers choose monthly cleanings to keep odors, bacteria, and pests under control.</p>
            </div>
        </div>

        <div class="faq-item">
            <h3>Do you use eco-friendly products?<span>+</span></h3>
            <div class="faq-answer">
                <p>Yes. We use environmentally friendly cleaners that are safe for families, pets, and landscaping.</p>
            </div>
        </div>

        <div class="faq-item">
            <h3>Do I need to be home?<span>+</span></h3>
            <div class="faq-answer">
                <p>No. Simply leave your bins outside after pickup and we'll take care of the rest.</p>
            </div>
        </div>

    </div>

</section>

<section id="contact">

    <div class="title fade">
        <h2>Contact Us</h2>
        <p>Request a free quote or schedule your next cleaning.</p>
    </div>

    <div class="contact-grid">

        <div class="contact-card fade">

            <h2>Get In Touch</h2>

            <br>

            <p><strong>📞 Phone:</strong> (555) 123-4567</p>

            <br>

            <p><strong>📧 Email:</strong> hello@freshbin.com</p>

            <br>

            <p><strong>📍 Service Area:</strong> Your Local Community</p>

            <br>

            <p>
                We proudly provide professional trash bin cleaning,
                sanitizing, and deodorizing services for residential
                and commercial customers.
            </p>

        </div>

        <div class="contact-card fade">

            <form id="contactForm">

                <input
                    type="text"
                    placeholder="Full Name"
                    required>

                <input
                    type="email"
                    placeholder="Email Address"
                    required>

                <input
                    type="tel"
                    placeholder="Phone Number">

                <textarea
                    placeholder="Tell us how we can help..."
                    required></textarea>

                <button
                    class="button"
                    type="submit">
                    Send Request
                </button>

            </form>

        </div>

    </div>

</section>

<footer>

    <h3>FreshBin</h3>

    <br>

    <p>
        Professional Trash Bin Cleaning • Sanitizing • Deodorizing
    </p>

    <br>

    <p>
        © 2026 FreshBin. All Rights Reserved.
    </p>

</footer>

<script>

// Scroll Animations

const fades = document.querySelectorAll(".fade");

const observer = new IntersectionObserver(entries => {

    entries.forEach(entry => {

        if(entry.isIntersecting){

            entry.target.classList.add("show");

        }

    });

},{
    threshold:.15
});

fades.forEach(el => observer.observe(el));


// FAQ

document.querySelectorAll(".faq-item").forEach(item=>{

    item.addEventListener("click",()=>{

        item.classList.toggle("active");

    });

});


// Contact Form

const form = document.getElementById("contactForm");

form.addEventListener("submit",function(e){

    e.preventDefault();

    alert("Thank you! Your request has been received. We'll contact you soon.");

    form.reset();

});

</script>

</body>
</html>
