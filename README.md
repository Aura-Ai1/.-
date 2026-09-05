<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">

<title>MYK — Mehmet Yalçınkaya</title>

<meta name="description"
content="MYK Restoran by Mehmet Yalçınkaya — İstanbul'da gastronomi, tasarım ve deneyimin buluştuğu özel restoran.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">

<style>

/* =========================================================
   RESET
========================================================= */

:root{
    --black:#050505;
    --black2:#0b0b0b;
    --black3:#111;
    --gold:#c8a66a;
    --gold2:#efd39e;
    --cream:#eee8df;
    --white:#f7f3eb;
    --muted:#888;
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
    background:var(--black);
    color:white;
    font-family:"DM Sans",sans-serif;
    overflow-x:hidden;
}

body::selection{
    background:var(--gold);
    color:#000;
}

a{
    text-decoration:none;
    color:inherit;
}

button,
input,
select{
    font-family:inherit;
}


/* =========================================================
   LOADER
========================================================= */

.loader{
    position:fixed;
    inset:0;
    z-index:99999;
    background:#030303;
    display:flex;
    justify-content:center;
    align-items:center;
    transition:1.1s cubic-bezier(.7,0,.2,1);
}

.loader.hide{
    opacity:0;
    visibility:hidden;
    pointer-events:none;
}

.loader-inner{
    text-align:center;
}

.loader-myk{
    font-family:"Playfair Display",serif;
    font-size:72px;
    letter-spacing:18px;
    padding-left:18px;
}

.loader-sub{
    color:var(--gold);
    font-size:8px;
    letter-spacing:6px;
    margin-top:15px;
}

.loader-line{
    width:0;
    height:1px;
    background:var(--gold);
    margin:28px auto 0;
    animation:loaderLine 1.7s ease forwards;
}

@keyframes loaderLine{
    to{
        width:220px;
    }
}


/* =========================================================
   NAVIGATION
========================================================= */

nav{
    position:fixed;
    left:0;
    top:0;
    width:100%;
    height:92px;
    padding:0 5vw;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:5000;
    transition:.5s ease;
}

nav.scrolled{
    height:70px;
    background:rgba(4,4,4,.78);
    backdrop-filter:blur(22px);
    -webkit-backdrop-filter:blur(22px);
    border-bottom:1px solid rgba(255,255,255,.07);
}

.logo{
    font-family:"Playfair Display",serif;
    font-size:25px;
    letter-spacing:8px;
}

.logo span{
    color:var(--gold);
}

.nav-links{
    display:flex;
    gap:31px;
    list-style:none;
}

.nav-links a{
    font-size:9px;
    letter-spacing:2.5px;
    color:#ccc;
    transition:.3s;
}

.nav-links a:hover{
    color:var(--gold);
}

.nav-reserve{
    padding:13px 20px;
    border:1px solid rgba(200,166,106,.7);
    font-size:9px;
    letter-spacing:2px;
    transition:.35s;
}

.nav-reserve:hover{
    background:var(--gold);
    color:#000;
}


/* =========================================================
   SECTION GENERAL
========================================================= */

.section{
    padding:155px 8vw;
}

.grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:90px;
    align-items:center;
}

.label{
    color:var(--gold);
    font-size:9px;
    letter-spacing:5px;
    margin-bottom:25px;
}

.title{
    font-family:"Playfair Display",serif;
    font-size:clamp(46px,6vw,85px);
    line-height:.94;
    font-weight:400;
}

.title em{
    color:var(--gold);
}

.text{
    color:#999;
    font-size:14px;
    line-height:2;
    max-width:590px;
    margin-top:32px;
}


/* =========================================================
   NEW OPENING DISH
   SAYFANIN EN BAŞI
========================================================= */

.opening-dish{
    position:relative;
    height:170vh;
    min-height:1100px;
    background:
        radial-gradient(
            circle at 50% 48%,
            rgba(200,166,106,.14),
            transparent 28%
        ),
        #040404;
}

.opening-sticky{
    position:sticky;
    top:0;
    height:100vh;
    min-height:700px;
    overflow:hidden;
    display:flex;
    align-items:center;
    justify-content:center;
}

.opening-glow{
    position:absolute;
    width:650px;
    height:650px;
    border-radius:50%;
    background:radial-gradient(
        circle,
        rgba(200,166,106,.15),
        transparent 68%
    );
    filter:blur(20px);
}

.opening-copy{
    position:absolute;
    top:10%;
    left:50%;
    transform:translateX(-50%);
    text-align:center;
    z-index:30;
    width:90%;
}

.opening-copy .label{
    margin-bottom:18px;
}

.opening-copy h2{
    font-family:"Playfair Display",serif;
    font-size:clamp(45px,6vw,82px);
    line-height:.92;
    font-weight:400;
}

.opening-copy h2 em{
    color:var(--gold);
}

.opening-copy p{
    margin-top:17px;
    color:#777;
    font-size:9px;
    letter-spacing:4px;
}


/* PLATE */

.opening-plate{
    width:min(520px,75vw);
    aspect-ratio:1;
    border-radius:50%;
    position:relative;
    z-index:10;

    background:
        radial-gradient(
            circle at center,
            #141414 0 47%,
            #a99e8e 48% 48.5%,
            #e8e1d7 49% 53%,
            #cfc6b9 54% 55%,
            #eeeae4 56% 100%
        );

    box-shadow:
        0 80px 120px rgba(0,0,0,.85),
        0 0 80px rgba(200,166,106,.08),
        inset 0 0 40px rgba(0,0,0,.12);

    transform:scale(.62);
    opacity:.2;
}


/* plate inner */
.opening-plate::before{
    content:"";
    position:absolute;
    inset:15%;
    border-radius:50%;
    border:1px solid rgba(0,0,0,.17);
}

.opening-plate::after{
    content:"";
    position:absolute;
    inset:23%;
    border-radius:50%;
    box-shadow:inset 0 0 45px rgba(0,0,0,.45);
}


/* =========================================================
   FALLING INGREDIENTS
========================================================= */

.falling{
    position:absolute;
    width:86px;
    height:86px;
    border-radius:50%;
    background-position:center;
    background-size:cover;
    z-index:25;

    box-shadow:
        0 20px 40px rgba(0,0,0,.7),
        0 0 0 1px rgba(255,255,255,.08);

    opacity:0;
    will-change:transform;
}

.falling::after{
    content:"";
    position:absolute;
    inset:-10px;
    border-radius:50%;
    border:1px solid rgba(200,166,106,.1);
}


/* different ingredients */

.fall-1{
    background-image:
    url("https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=400&q=90");
}

.fall-2{
    background-image:
    url("https://images.unsplash.com/photo-1512621776951-a57141f2eefd?auto=format&fit=crop&w=400&q=90");
}

.fall-3{
    background-image:
    url("https://images.unsplash.com/photo-1498837167922-ddd27525d352?auto=format&fit=crop&w=400&q=90");
}

.fall-4{
    background-image:
    url("https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=400&q=90");
}

.fall-5{
    background-image:
    url("https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=400&q=90");
}


/* final food */

.final-dish{
    position:absolute;
    inset:17%;
    border-radius:50%;
    overflow:hidden;
    z-index:20;
    opacity:0;
    transform:scale(.35);
}

.final-dish img{
    width:100%;
    height:100%;
    object-fit:cover;
}


/* small particles */

.particle{
    position:absolute;
    width:5px;
    height:5px;
    border-radius:50%;
    background:var(--gold);
    opacity:0;
    z-index:15;
}


/* opening bottom */

.opening-bottom{
    position:absolute;
    bottom:35px;
    left:50%;
    transform:translateX(-50%);
    color:#666;
    font-size:8px;
    letter-spacing:4px;
    z-index:40;
    white-space:nowrap;
}

.opening-bottom::before{
    content:"";
    display:block;
    height:55px;
    width:1px;
    margin:0 auto 13px;
    background:linear-gradient(var(--gold),transparent);
}


/* =========================================================
   HERO
========================================================= */

.hero{
    height:120vh;
    min-height:780px;
    position:relative;
    overflow:hidden;
}

.hero-layer{
    position:absolute;
    inset:0;
    background-position:center;
    background-size:cover;
}

.hero-exterior{
    background-image:
        linear-gradient(
            rgba(0,0,0,.15),
            rgba(0,0,0,.78)
        ),
        url("https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=2400&q=90");

    transform:scale(1.05);
}

.hero-interior{
    background-image:
        linear-gradient(
            rgba(0,0,0,.15),
            rgba(0,0,0,.82)
        ),
        url("https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=2400&q=90");

    opacity:0;
    transform:scale(1.3);
}

.hero-video{
    position:absolute;
    inset:0;
    width:100%;
    height:100%;
    object-fit:cover;
    opacity:.38;
    z-index:1;
}

.hero::after{
    content:"";
    position:absolute;
    inset:0;
    z-index:2;
    background:
        linear-gradient(
            to bottom,
            rgba(0,0,0,.05) 25%,
            transparent 48%,
            rgba(0,0,0,.95)
        );
}

.hero-content{
    position:absolute;
    left:8vw;
    bottom:16vh;
    z-index:5;
    max-width:950px;
}

.hero-kicker{
    color:var(--gold);
    font-size:10px;
    letter-spacing:5px;
    margin-bottom:25px;
}

.hero h1{
    font-family:"Playfair Display",serif;
    font-weight:400;
    font-size:clamp(62px,9vw,140px);
    line-height:.85;
}

.hero h1 em{
    color:var(--gold);
}

.hero-description{
    color:#d0d0d0;
    max-width:560px;
    margin-top:35px;
    line-height:1.9;
    font-size:14px;
}

.hero-buttons{
    display:flex;
    gap:13px;
    margin-top:35px;
}

.btn{
    display:inline-block;
    padding:17px 28px;
    border:1px solid rgba(255,255,255,.35);
    font-size:9px;
    letter-spacing:2px;
    transition:.35s;
}

.btn.gold{
    background:var(--gold);
    border-color:var(--gold);
    color:#050505;
}

.btn:hover{
    transform:translateY(-3px);
    background:#fff;
    color:#000;
}

.hero-scroll{
    position:absolute;
    right:5vw;
    bottom:45px;
    z-index:5;
    writing-mode:vertical-rl;
    color:#888;
    font-size:8px;
    letter-spacing:4px;
}

.hero-scroll::before{
    content:"";
    display:block;
    width:1px;
    height:65px;
    background:linear-gradient(var(--gold),transparent);
    margin:auto auto 13px;
}


/* =========================================================
   STORY
========================================================= */

.story{
    background:
        radial-gradient(
            circle at 80% 20%,
            rgba(200,166,106,.09),
            transparent 30%
        ),
        #080808;
}

.story-image{
    height:650px;
    position:relative;
    background:
        linear-gradient(to bottom,transparent,rgba(0,0,0,.5)),
        url("https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&w=1600&q=90")
        center/cover;
}

.story-number{
    position:absolute;
    right:25px;
    bottom:20px;
    font:400 65px "Playfair Display",serif;
    color:rgba(255,255,255,.14);
}


/* =========================================================
   EXPERIENCE
========================================================= */

.experience{
    background:#0d0d0d;
}

.cards{
    margin-top:80px;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.card{
    height:540px;
    position:relative;
    overflow:hidden;
}

.card img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:1.2s;
}

.card:hover img{
    transform:scale(1.08);
}

.card::after{
    content:"";
    position:absolute;
    inset:0;
    background:
        linear-gradient(
            transparent 25%,
            rgba(0,0,0,.92)
        );
}

.card-content{
    position:absolute;
    z-index:2;
    left:28px;
    right:28px;
    bottom:30px;
}

.card-content h3{
    font:400 32px "Playfair Display",serif;
}

.card-content p{
    color:#bbb;
    font-size:12px;
    line-height:1.7;
    margin-top:8px;
}


/* =========================================================
   DISHES
========================================================= */

.dishes{
    background:var(--cream);
    color:#111;
}

.dishes .label{
    color:#95723b;
}

.dishes .title em{
    color:#95723b;
}

.dish-grid{
    margin-top:80px;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.dish{
    background:#fff;
    overflow:hidden;
}

.dish:nth-child(2){
    transform:translateY(70px);
}

.dish:nth-child(3){
    transform:translateY(140px);
}

.dish img{
    width:100%;
    height:470px;
    object-fit:cover;
    transition:1s;
}

.dish:hover img{
    transform:scale(1.06);
}

.dish-info{
    padding:24px;
}

.dish-info h3{
    font:400 28px "Playfair Display",serif;
}

.dish-info p{
    color:#777;
    font-size:12px;
    margin-top:8px;
}


/* =========================================================
   CHEF
========================================================= */

.chef{
    background:#080808;
}

.chef-image{
    height:700px;
    background:
        linear-gradient(to right,rgba(0,0,0,.8),transparent),
        url("https://images.unsplash.com/photo-1577219491135-ce391730fb2c?auto=format&fit=crop&w=1600&q=90")
        center/cover;
}


/* =========================================================
   CINEMA
========================================================= */

.cinema{
    height:100vh;
    min-height:700px;
    display:grid;
    place-items:center;
    text-align:center;

    background:
        linear-gradient(rgba(0,0,0,.2),rgba(0,0,0,.88)),
        url("https://images.unsplash.com/photo-1559339352-11d035aa65de?auto=format&fit=crop&w=2400&q=90")
        center/cover fixed;
}

.cinema h2{
    font:400 clamp(58px,9vw,130px)/.84 "Playfair Display",serif;
}

.cinema h2 em{
    color:var(--gold);
}

.cinema p{
    margin-top:25px;
    color:#bbb;
    font-size:9px;
    letter-spacing:5px;
}


/* =========================================================
   MENU
========================================================= */

.menu{
    background:#101010;
}

.menu-list{
    max-width:900px;
    margin:75px auto 0;
}

.menu-item{
    display:flex;
    justify-content:space-between;
    gap:30px;
    padding:28px 0;
    border-bottom:1px solid #272727;
}

.menu-item h3{
    font:400 25px "Playfair Display",serif;
}

.menu-item p{
    color:#777;
    font-size:11px;
    margin-top:7px;
}

.menu-tag{
    color:var(--gold);
    font-size:9px;
    letter-spacing:2px;
    white-space:nowrap;
}


/* =========================================================
   RESERVATION
========================================================= */

.reservation{
    background:
        radial-gradient(
            circle at 50% 0,
            rgba(200,166,106,.12),
            transparent 40%
        ),
        #060606;
}

.reservation-box{
    max-width:900px;
    margin:auto;
    text-align:center;
}

.reservation-note{
    color:#777;
    font-size:10px;
    margin-top:12px;
    letter-spacing:1px;
}

.form{
    margin-top:55px;
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:13px;
}

.form input,
.form select{
    width:100%;
    padding:18px;
    background:#111;
    border:1px solid #292929;
    color:white;
    outline:none;
}

.form input:focus,
.form select:focus{
    border-color:var(--gold);
}

.form .wide{
    grid-column:1/-1;
}

.form button{
    grid-column:1/-1;
    padding:20px;
    border:0;
    background:var(--gold);
    color:#000;
    cursor:pointer;
    font-size:10px;
    letter-spacing:3px;
    transition:.3s;
}

.form button:hover{
    background:#ead19e;
}


/* OCCUPIED TIME */

.time-option-full{
    color:#777 !important;
    text-decoration:line-through;
}

.reservation-status{
    margin-top:18px;
    min-height:20px;
    color:var(--gold);
    font-size:10px;
    letter-spacing:1px;
}


/* =========================================================
   CONTACT
========================================================= */

.contact{
    background:var(--cream);
    color:#111;
}

.contact .label{
    color:#95723b;
}

.contact-info{
    margin-top:35px;
}

.contact-line{
    padding:19px 0;
    border-bottom:1px solid rgba(0,0,0,.15);
    line-height:1.7;
}

.contact-line span{
    display:block;
    color:#888;
    font-size:9px;
    letter-spacing:2px;
    margin-bottom:5px;
}

.contact-line a{
    color:#111;
}

.map{
    min-height:500px;
    background:
        linear-gradient(rgba(0,0,0,.25),rgba(0,0,0,.68)),
        url("https://images.unsplash.com/photo-1552566626-52f8b828add9?auto=format&fit=crop&w=1600&q=90")
        center/cover;

    display:grid;
    place-items:center;
}

.map a{
    background:#fff;
    color:#111;
    padding:17px 24px;
    font-size:9px;
    letter-spacing:2px;
}


/* =========================================================
   FOOTER
========================================================= */

footer{
    background:#030303;
    padding:80px 8vw 25px;
}

.footer-top{
    display:flex;
    justify-content:space-between;
    gap:40px;
}

.footer-logo{
    font:400 52px "Playfair Display",serif;
    letter-spacing:6px;
}

.footer-logo span{
    color:var(--gold);
}

.footer-sub{
    color:#555;
    margin-top:8px;
    font-size:10px;
}

.footer-links{
    display:flex;
    gap:25px;
    color:#777;
    font-size:10px;
}

.footer-links a:hover{
    color:var(--gold);
}

.footer-bottom{
    margin-top:80px;
    padding-top:23px;
    border-top:1px solid #202020;
    display:flex;
    justify-content:space-between;
    gap:20px;
    color:#555;
    font-size:9px;
}

.burox-credit{
    color:var(--gold);
    letter-spacing:1px;
}


/* =========================================================
   FLOAT BUTTON
========================================================= */

.float-reserve{
    position:fixed;
    right:22px;
    bottom:22px;
    z-index:4000;
    width:64px;
    height:64px;
    border-radius:50%;
    background:var(--gold);
    color:#050505;
    display:grid;
    place-items:center;
    text-align:center;
    font-size:8px;
    line-height:1.4;
    box-shadow:0 15px 40px rgba(0,0,0,.55);
    transition:.35s;
}

.float-reserve:hover{
    transform:scale(1.1);
}


/* =========================================================
   REVEAL
========================================================= */

.reveal{
    opacity:0;
    transform:translateY(50px);
    transition:
        opacity 1s cubic-bezier(.2,.7,.2,1),
        transform 1s cubic-bezier(.2,.7,.2,1);
}

.reveal.active{
    opacity:1;
    transform:none;
}


/* =========================================================
   MOBILE
========================================================= */

@media(max-width:800px){

    nav{
        height:70px;
        padding:0 20px;
    }

    nav.scrolled{
        height:62px;
    }

    .nav-links{
        display:none;
    }

    .logo{
        font-size:19px;
    }

    .nav-reserve{
        padding:10px 13px;
    }

    .opening-dish{
        min-height:900px;
        height:145vh;
    }

    .opening-copy{
        top:12%;
    }

    .opening-copy h2{
        font-size:47px;
    }

    .opening-plate{
        width:330px;
    }

    .falling{
        width:55px;
        height:55px;
    }

    .hero{
        height:100vh;
        min-height:720px;
    }

    .hero-content{
        left:25px;
        right:25px;
        bottom:90px;
    }

    .hero h1{
        font-size:60px;
    }

    .hero-description{
        font-size:12px;
    }

    .hero-buttons{
        flex-direction:column;
        align-items:flex-start;
    }

    .section{
        padding:105px 25px;
    }

    .grid{
        grid-template-columns:1fr;
        gap:50px;
    }

    .story-image{
        height:450px;
    }

    .cards,
    .dish-grid{
        grid-template-columns:1fr;
    }

    .card{
        height:450px;
    }

    .dish:nth-child(2),
    .dish:nth-child(3){
        transform:none;
    }

    .dish img{
        height:390px;
    }

    .chef-image{
        height:500px;
    }

    .cinema{
        background-attachment:scroll;
    }

    .form{
        grid-template-columns:1fr;
    }

    .form .wide,
    .form button{
        grid-column:auto;
    }

    .footer-top{
        flex-direction:column;
    }

    .footer-links{
        flex-wrap:wrap;
    }

    .footer-bottom{
        flex-direction:column;
    }

    .float-reserve{
        width:57px;
        height:57px;
    }
}

</style>
</head>

<body>


<!-- =====================================================
     LOADER
===================================================== -->

<div class="loader" id="loader">

    <div class="loader-inner">

        <div class="loader-myk">
            MYK
        </div>

        <div class="loader-sub">
            MEHMET YALÇINKAYA
        </div>

        <div class="loader-line"></div>

    </div>

</div>


<!-- =====================================================
     NAV
===================================================== -->

<nav id="nav">

    <a href="#home" class="logo">
        MYK<span>.</span>
    </a>

    <ul class="nav-links">

        <li><a href="#story">HİKÂYE</a></li>

        <li><a href="#experience">DENEYİM</a></li>

        <li><a href="#dishes">LEZZETLER</a></li>

        <li><a href="#chef">ŞEF</a></li>

        <li><a href="#menu">MENÜ</a></li>

        <li><a href="#contact">İLETİŞİM</a></li>

    </ul>

    <a href="#reservation" class="nav-reserve">
        REZERVASYON
    </a>

</nav>


<!-- =====================================================
     01 — FALLING FOOD OPENING
===================================================== -->

<section class="opening-dish">

    <div class="opening-sticky">

        <div class="opening-glow"></div>


        <div class="opening-copy">

            <div class="label">
                01 / MUTFAK
            </div>

            <h2>
                Bir fikirden<br>
                <em>bir tabağa.</em>
            </h2>

            <p>
                AŞAĞI KAYDIR · MALZEMELERİ İZLE
            </p>

        </div>


        <!-- FALLING INGREDIENTS -->

        <div class="falling fall-1" id="fall1"></div>

        <div class="falling fall-2" id="fall2"></div>

        <div class="falling fall-3" id="fall3"></div>

        <div class="falling fall-4" id="fall4"></div>

        <div class="falling fall-5" id="fall5"></div>


        <!-- PLATE -->

        <div class="opening-plate" id="openingPlate">

            <div class="final-dish" id="finalDish">

                <img
                    src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=1200&q=90"
                    alt="MYK gastronomi"
                >

            </div>

        </div>


        <!-- PARTICLES -->

        <span class="particle" style="left:42%;top:35%"></span>
        <span class="particle" style="left:58%;top:32%"></span>
        <span class="particle" style="left:34%;top:58%"></span>
        <span class="particle" style="left:67%;top:61%"></span>
        <span class="particle" style="left:50%;top:70%"></span>


        <div class="opening-bottom">
            DEVAM ET
        </div>

    </div>

</section>


<!-- =====================================================
     02 — HERO
===================================================== -->

<section class="hero" id="home">

    <div
        class="hero-layer hero-exterior"
        id="outside">
    </div>

    <div
        class="hero-layer hero-interior"
        id="inside">
    </div>


    <!-- Aynı klasöre restaurant-entry.mp4 koyarsan kullanılır -->

    <video
        class="hero-video"
        autoplay
        muted
        loop
        playsinline
        poster="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=2200&q=90">

        <source
            src="restaurant-entry.mp4"
            type="video/mp4">

    </video>


    <div class="hero-content">

        <div class="hero-kicker">
            İSTANBUL · GASTRONOMİ · DENEYİM
        </div>

        <h1>
            Lezzetin
            <br>
            <em>ötesinde.</em>
        </h1>

        <p class="hero-description">
            Şef Mehmet Yalçınkaya'nın gastronomi vizyonunu;
            modern mutfak, seçkin servis ve etkileyici atmosferle
            bir araya getiren özel bir deneyim.
        </p>

        <div class="hero-buttons">

            <a
                href="#reservation"
                class="btn gold">
                MASANIZI AYIRTIN
            </a>

            <a
                href="#dishes"
                class="btn">
                LEZZETLERİ KEŞFET
            </a>

        </div>

    </div>


    <div class="hero-scroll">
        AŞAĞI KAYDIR
    </div>

</section>


<!-- =====================================================
     03 — STORY
===================================================== -->

<section class="section story" id="story">

    <div class="grid">

        <div class="reveal">

            <div class="label">
                03 / HİKÂYE
            </div>

            <h2 class="title">
                Bir tabaktan<br>
                <em>daha fazlası.</em>
            </h2>

            <p class="text">
                MYK Restoran; mutfak, tasarım, servis ve
                atmosferin aynı hikâyede buluştuğu bir
                gastronomi deneyimi.
            </p>

        </div>


        <div class="story-image reveal">

            <div class="story-number">
                03
            </div>

        </div>

    </div>

</section>


<!-- =====================================================
     04 — EXPERIENCE
===================================================== -->

<section
    class="section experience"
    id="experience">

    <div class="reveal">

        <div class="label">
            04 / DENEYİM
        </div>

        <h2 class="title">
            Akşamınızın<br>
            <em>her anı.</em>
        </h2>

    </div>


    <div class="cards">


        <article class="card reveal">

            <img
                src="https://images.unsplash.com/photo-1559339352-11d035aa65de?auto=format&fit=crop&w=1200&q=90"
                alt="MYK atmosfer">

            <div class="card-content">

                <h3>
                    Atmosfer
                </h3>

                <p>
                    Işık, müzik ve tasarımın dengelendiği
                    sofistike bir ortam.
                </p>

            </div>

        </article>


        <article class="card reveal">

            <img
                src="https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&w=1200&q=90"
                alt="Gastronomi">

            <div class="card-content">

                <h3>
                    Gastronomi
                </h3>

                <p>
                    Malzemenin karakterini öne çıkaran
                    modern yorumlar.
                </p>

            </div>

        </article>


        <article class="card reveal">

            <img
                src="https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=1200&q=90"
                alt="Masa deneyimi">

            <div class="card-content">

                <h3>
                    Masa
                </h3>

                <p>
                    Paylaşılan anların merkezinde
                    özenli bir servis deneyimi.
                </p>

            </div>

        </article>


    </div>

</section>


<!-- =====================================================
     05 — DISHES
===================================================== -->

<section class="section dishes" id="dishes">

    <div class="reveal">

        <div class="label">
            05 / SEÇKİ
        </div>

        <h2 class="title">
            Şefin<br>
            <em>dokunuşu.</em>
        </h2>

    </div>


    <div class="dish-grid">


        <article class="dish reveal">

            <img
                src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=1200&q=90"
                alt="Şefin seçkisi">

            <div class="dish-info">

                <h3>
                    Şefin Seçkisi
                </h3>

                <p>
                    Mevsimin karakterini taşıyan özel yorum.
                </p>

            </div>

        </article>


        <article class="dish reveal">

            <img
                src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=1200&q=90"
                alt="Modern Anadolu">

            <div class="dish-info">

                <h3>
                    Modern Anadolu
                </h3>

                <p>
                    Geleneksel malzemelere çağdaş yaklaşım.
                </p>

            </div>

        </article>


        <article class="dish reveal">

            <img
                src="https://images.unsplash.com/photo-1512621776951-a57141f2eefd?auto=format&fit=crop&w=1200&q=90"
                alt="Final dokunuş">

            <div class="dish-info">

                <h3>
                    Final Dokunuş
                </h3>

                <p>
                    Gecenin sonuna özel hazırlanmış seçki.
                </p>

            </div>

        </article>


    </div>


    <div style="text-align:center;margin-top:100px">

        <a
            href="https://mykcaferestoran.com.tr/"
            target="_blank"
            class="btn gold">

            TAM MENÜYÜ GÖR

        </a>

    </div>

</section>


<!-- =====================================================
     06 — CHEF
===================================================== -->

<section
    class="section chef"
    id="chef">

    <div class="grid">

        <div class="reveal">

            <div class="label">
                06 / ŞEF
            </div>

            <h2 class="title">
                Mehmet<br>
                <em>Yalçınkaya.</em>
            </h2>

            <p class="text">
                Güçlü malzemeler, modern teknikler ve
                sofrayı bir deneyime dönüştüren bir
                mutfak yaklaşımı.
            </p>

        </div>


        <div class="chef-image reveal"></div>

    </div>

</section>


<!-- =====================================================
     07 — CINEMA
===================================================== -->

<section class="cinema">

    <div class="reveal">

        <div class="label">
            MYK RESTORAN
        </div>

        <h2>
            Masada<br>
            <em>başlar.</em>
        </h2>

        <p>
            LEZZET · ATMOSFER · HİKÂYE
        </p>

    </div>

</section>


<!-- =====================================================
     08 — MENU
===================================================== -->

<section
    class="section menu"
    id="menu">

    <div class="reveal">

        <div class="label">
            08 / MENÜ
        </div>

        <h2 class="title">
            Seçkin<br>
            <em>lezzetler.</em>
        </h2>

    </div>


    <div class="menu-list">


        <div class="menu-item reveal">

            <div>

                <h3>
                    Şefin Başlangıcı
                </h3>

                <p>
                    Mevsimsel dokunuşlarla hazırlanan başlangıç.
                </p>

            </div>

            <span class="menu-tag">
                SEÇKİ
            </span>

        </div>


        <div class="menu-item reveal">

            <div>

                <h3>
                    MYK Ana Tabak
                </h3>

                <p>
                    Şefin modern mutfak yorumu.
                </p>

            </div>

            <span class="menu-tag">
                İMZA
            </span>

        </div>


        <div class="menu-item reveal">

            <div>

                <h3>
                    İmza Lezzet
                </h3>

                <p>
                    Restoranın karakterini yansıtan özel tabak.
                </p>

            </div>

            <span class="menu-tag">
                İMZA
            </span>

        </div>


        <div class="menu-item reveal">

            <div>

                <h3>
                    Final
                </h3>

                <p>
                    Gecenin sonuna özel tatlı deneyimi.
                </p>

            </div>

            <span class="menu-tag">
                SEÇKİ
            </span>

        </div>


    </div>

</section>


<!-- =====================================================
     09 — RESERVATION
===================================================== -->

<section
    class="section reservation"
    id="reservation">

    <div class="reservation-box reveal">

        <div class="label">
            09 / REZERVASYON
        </div>

        <h2 class="title">
            Masanız<br>
            <em>hazır.</em>
        </h2>

        <p
            class="text"
            style="margin-left:auto;margin-right:auto">

            Rezervasyon talebinizi oluşturun.
            Dolu olan tarih ve saatler otomatik olarak
            işaretlenir.

        </p>

        <div class="reservation-note">
            * Aynı tarayıcıda oluşturulan rezervasyonlar
            dolu olarak gösterilir.
        </div>


        <form
            class="form"
            id="reservationForm">


            <input
                id="guestName"
                type="text"
                placeholder="Ad Soyad"
                required>


            <input
                id="guestPhone"
                type="tel"
                placeholder="Telefon"
                required>


            <input
                id="guestDate"
                type="date"
                required>


            <select
                id="guestTime"
                required>

                <option value="">
                    Saat seçin
                </option>

                <option value="18:00">
                    18:00
                </option>

                <option value="18:30">
                    18:30
                </option>

                <option value="19:00">
                    19:00
                </option>

                <option value="19:30">
                    19:30
                </option>

                <option value="20:00">
                    20:00
                </option>

                <option value="20:30">
                    20:30
                </option>

                <option value="21:00">
                    21:00
                </option>

                <option value="21:30">
                    21:30
                </option>

                <option value="22:00">
                    22:00
                </option>

            </select>


            <input
                class="wide"
                id="guestCount"
                type="number"
                min="1"
                max="20"
                value="1"
                placeholder="Kişi sayısı"
                required>


            <button type="submit">
                REZERVASYON TALEBİ GÖNDER
            </button>

        </form>


        <div
            class="reservation-status"
            id="reservationStatus">
        </div>

    </div>

</section>


<!-- =====================================================
     10 — CONTACT
===================================================== -->

<section
    class="section contact"
    id="contact">

    <div class="grid">


        <div class="reveal">

            <div class="label">
                10 / İLETİŞİM
            </div>

            <h2 class="title">
                Bizi<br>
                <em>bulun.</em>
            </h2>


            <div class="contact-info">


                <div class="contact-line">

                    <span>
                        ADRES
                    </span>

                    Convention Center,
                    Yeşilköy Mah. Atatürk Cad,
                    İstanbul WOW Hotel No:23C No:15,
                    34149 Bakırköy / İstanbul

                </div>


                <div class="contact-line">

                    <span>
                        TELEFON
                    </span>

                    <a href="tel:+905301093414">
                        0530 109 34 14
                    </a>

                </div>


                <div class="contact-line">

                    <span>
                        ÇALIŞMA SAATLERİ
                    </span>

                    Her gün · 01:00'e kadar
                    <br>
                    Mutfak · 23:00'e kadar

                </div>


            </div>

        </div>


        <div class="map reveal">

            <a
                target="_blank"
                href="https://www.google.com/maps/search/?api=1&query=MYK+Restoran+by+Mehmet+Yalçınkaya+İstanbul">

                HARİTADA GÖRÜNTÜLE

            </a>

        </div>


    </div>

</section>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div class="footer-top">


        <div>

            <div class="footer-logo">
                MYK<span>.</span>
            </div>

            <div class="footer-sub">
                by Mehmet Yalçınkaya
            </div>

        </div>


        <div class="footer-links">

            <a href="#story">
                Hikâye
            </a>

            <a href="#dishes">
                Lezzetler
            </a>

            <a href="#menu">
                Menü
            </a>

            <a href="#reservation">
                Rezervasyon
            </a>

        </div>


    </div>


    <div class="footer-bottom">

        <span>
            © 2026 MYK Restoran
        </span>

        <span>
            İstanbul · Türkiye
        </span>

        <span class="burox-credit">
            BUROX tarafından tasarlanmış ve geliştirilmiştir.
        </span>

    </div>

</footer>


<!-- FLOATING RESERVATION -->

<a
    href="#reservation"
    class="float-reserve">

    MASA
    <br>
    AYIRT

</a>


<script>

/* =========================================================
   LOADER
========================================================= */

window.addEventListener("load",()=>{

    setTimeout(()=>{

        document
            .getElementById("loader")
            .classList.add("hide");

    },1200);

});


/* =========================================================
   NAV
========================================================= */

const nav=document.getElementById("nav");

window.addEventListener("scroll",()=>{

    if(window.scrollY>50){

        nav.classList.add("scrolled");

    }else{

        nav.classList.remove("scrolled");

    }

});


/* =========================================================
   REVEAL
========================================================= */

const revealObserver=
new IntersectionObserver(

    entries=>{

        entries.forEach(entry=>{

            if(entry.isIntersecting){

                entry.target.classList.add("active");

            }

        });

    },

    {
        threshold:.13
    }

);

document
    .querySelectorAll(".reveal")
    .forEach(el=>{

        revealObserver.observe(el);

    });


/* =========================================================
   FALLING FOOD — SCROLL ENGINE
========================================================= */

const opening=
document.querySelector(".opening-dish");

const plate=
document.getElementById("openingPlate");

const finalDish=
document.getElementById("finalDish");

const fallers=[

    {
        el:document.getElementById("fall1"),
        startX:-260,
        startY:-520,
        targetX:-90,
        targetY:-65,
        delay:.00,
        rotate:540
    },

    {
        el:document.getElementById("fall2"),
        startX:240,
        startY:-650,
        targetX:90,
        targetY:-50,
        delay:.10,
        rotate:-460
    },

    {
        el:document.getElementById("fall3"),
        startX:-120,
        startY:-720,
        targetX:-75,
        targetY:70,
        delay:.20,
        rotate:650
    },

    {
        el:document.getElementById("fall4"),
        startX:170,
        startY:-580,
        targetX:80,
        targetY:72,
        delay:.30,
        rotate:-600
    },

    {
        el:document.getElementById("fall5"),
        startX:20,
        startY:-800,
        targetX:0,
        targetY:0,
        delay:.40,
        rotate:760
    }

];


const particles=
document.querySelectorAll(".particle");


function clamp(value,min,max){

    return Math.max(min,Math.min(max,value));

}


function fallingFoodAnimation(){

    const rect=
        opening.getBoundingClientRect();

    const scrollDistance=
        opening.offsetHeight-window.innerHeight;

    let progress=
        -rect.top/scrollDistance;

    progress=
        clamp(progress,0,1);


    /* PLATE */

    const plateProgress=
        clamp(progress/.32,0,1);

    const plateScale=
        .62+(plateProgress*.38);

    plate.style.transform=
        `scale(${plateScale})`;

    plate.style.opacity=
        .2+(plateProgress*.8);


    /* INGREDIENTS */

    fallers.forEach((item,index)=>{

        let p=
            (progress-item.delay)/.58;

        p=
            clamp(p,0,1);


        /*
           cubic easing:
           önce hızlanıyor,
           sonra yavaşlayıp tabağa oturuyor
        */

        const ease=
            1-Math.pow(1-p,3);


        const x=
            item.startX+
            (item.targetX-item.startX)*ease;


        const y=
            item.startY+
            (item.targetY-item.startY)*ease;


        /*
           küçük yaylanma
        */

        const bounce=
            p>0.72
            ?
            Math.sin((p-.72)*Math.PI*3)*12*(1-p)
            :
            0;


        const rotation=
            item.rotate*(1-p);


        const scale=
            p<.12
            ? .65+p*3
            : 1;


        item.el.style.opacity=
            clamp(p*4,0,1)*
            (p<.95 ? 1 : (1-p)*20);


        item.el.style.transform=
            `translate(
                calc(-50% + ${x}px),
                calc(-50% + ${y+bounce}px)
            )
            rotate(${rotation}deg)
            scale(${scale})`;

    });


    /* FINAL DISH */

    const dishProgress=
        clamp((progress-.67)/.33,0,1);

    finalDish.style.opacity=
        dishProgress;

    finalDish.style.transform=
        `scale(${.35+(dishProgress*.65)})
         rotate(${(1-dishProgress)*12}deg)`;


    /* PARTICLES */

    particles.forEach((particle,index)=>{

        let p=
            clamp((progress-.38)/.45,0,1);

        const angle=
            index*(Math.PI*2/particles.length);

        const distance=
            p*150;

        particle.style.opacity=
            p*(1-p);

        particle.style.transform=
            `translate(
                ${Math.cos(angle)*distance}px,
                ${Math.sin(angle)*distance}px
            )
            scale(${1+p*2})`;

    });

}


window.addEventListener(
    "scroll",
    fallingFoodAnimation,
    {passive:true}
);

fallingFoodAnimation();


/* =========================================================
   HERO CAMERA
========================================================= */

const hero=
document.querySelector(".hero");

const outside=
document.getElementById("outside");

const inside=
document.getElementById("inside");


function heroCamera(){

    const rect=
        hero.getBoundingClientRect();

    const max=
        hero.offsetHeight-window.innerHeight;

    let p=
        -rect.top/max;

    p=
        clamp(p,0,1);


    outside.style.transform=
        `scale(${1.05+p*.35})`;


    inside.style.opacity=
        Math.min(1,p*1.8);


    inside.style.transform=
        `scale(${1.30-p*.38})`;

}


window.addEventListener(
    "scroll",
    heroCamera,
    {passive:true}
);

heroCamera();


/* =========================================================
   HERO MOUSE PARALLAX
========================================================= */

if(window.innerWidth>900){

    document.addEventListener("mousemove",event=>{

        const x=
            (event.clientX/window.innerWidth-.5)*8;

        const y=
            (event.clientY/window.innerHeight-.5)*8;


        document
            .querySelector(".hero-content")
            .style.transform=
            `translate(${x}px,${y}px)`;

    });

}


/* =========================================================
   RESERVATION STORAGE
========================================================= */

const reservationForm=
    document.getElementById("reservationForm");

const dateInput=
    document.getElementById("guestDate");

const timeSelect=
    document.getElementById("guestTime");

const peopleInput=
    document.getElementById("guestCount");

const status=
    document.getElementById("reservationStatus");


/*
   Rezervasyonlar tarayıcıda saklanır.
*/

function getReservations(){

    try{

        return JSON.parse(
            localStorage.getItem("mykReservations")
        ) || [];

    }catch(error){

        return [];

    }

}


function saveReservations(data){

    localStorage.setItem(
        "mykReservations",
        JSON.stringify(data)
    );

}


/* =========================================================
   DOLU SAATLERİ GÖSTER
========================================================= */

function updateOccupiedTimes(){

    const date=
        dateInput.value;

    const reservations=
        getReservations();


    Array.from(timeSelect.options)
    .forEach(option=>{

        if(!option.value){

            return;

        }


        const occupied=
            reservations.some(reservation=>

                reservation.date===date &&
                reservation.time===option.value

            );


        option.disabled=
            occupied;


        option.classList.toggle(
            "time-option-full",
            occupied
        );


        if(occupied){

            option.textContent=
                option.value+
                " — DOLU";

        }else{

            option.textContent=
                option.value;

        }

    });


    /*
       seçili saat dolduysa temizle
    */

    const selected=
        timeSelect.options[
            timeSelect.selectedIndex
        ];


    if(selected && selected.disabled){

        timeSelect.value="";

    }


    if(date){

        const occupiedCount=
            reservations.filter(
                r=>r.date===date
            ).length;


        if(occupiedCount>0){

            status.textContent=
                occupiedCount+
                " rezervasyon bu tarihte kayıtlı.";

        }else{

            status.textContent=
                "Bu tarih için henüz kayıtlı rezervasyon yok.";

        }

    }else{

        status.textContent="";

    }

}


dateInput.addEventListener(
    "change",
    updateOccupiedTimes
);


/* =========================================================
   BUGÜNDEN ÖNCEKİ TARİHLERİ KAPAT
========================================================= */

const today=
    new Date().toISOString().split("T")[0];

dateInput.min=today;


/* =========================================================
   RESERVATION SUBMIT
========================================================= */

reservationForm.addEventListener(
    "submit",
    event=>{

        event.preventDefault();


        const name=
            document.getElementById("guestName").value.trim();

        const phone=
            document.getElementById("guestPhone").value.trim();

        const date=
            dateInput.value;

        const time=
            timeSelect.value;

        const people=
            peopleInput.value;


        if(!date || !time){

            alert(
                "Lütfen tarih ve saat seçin."
            );

            return;

        }


        const reservations=
            getReservations();


        /*
           Aynı tarih + saat tekrar kullanılamaz.
        */

        const alreadyTaken=
            reservations.some(
                reservation=>
                    reservation.date===date &&
                    reservation.time===time
            );


        if(alreadyTaken){

            alert(
                "Bu tarih ve saat artık dolu."
            );

            updateOccupiedTimes();

            return;

        }


        const reservation={

            id:
                Date.now(),

            name:
                name,

            phone:
                phone,

            date:
                date,

            time:
                time,

            people:
                people

        };


        reservations.push(
            reservation
        );


        saveReservations(
            reservations
        );


        /*
           Saat hemen DOLU olur.
        */

        updateOccupiedTimes();


        /*
           WhatsApp mesajı
        */

        const message=
`Merhaba MYK Restoran,

Rezervasyon talebi:

Ad Soyad: ${name}
Telefon: ${phone}
Tarih: ${date}
Saat: ${time}
Kişi Sayısı: ${people}

Rezervasyon talebimi iletmek istiyorum.`;


        const whatsapp=
            "https://wa.me/905301093414?text="+
            encodeURIComponent(message);


        status.textContent=
            "Rezervasyon saati ayrıldı. WhatsApp açılıyor...";


        setTimeout(()=>{

            window.open(
                whatsapp,
                "_blank"
            );

        },500);

    }
);


/* =========================================================
   LAZY IMAGE
========================================================= */

document
    .querySelectorAll("img")
    .forEach(img=>{

        img.loading="lazy";

    });


/* =========================================================
   IMAGE ERROR FALLBACK
========================================================= */

document
    .querySelectorAll("img")
    .forEach(img=>{

        img.addEventListener(
            "error",
            ()=>{

                img.style.background="#151515";

            }
        );

    });


/* =========================================================
   INITIAL
========================================================= */

updateOccupiedTimes();

</script>

</body>
</html>
