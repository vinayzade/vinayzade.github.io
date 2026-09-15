[index.html](https://github.com/user-attachments/files/32225971/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vinay Zade — Senior React Native Developer</title>
<meta name="description" content="Vinay Zade — Senior React Native developer in Mumbai with 9+ years shipping Android and iOS apps. Founder of Ganadhisha.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@400;600;700;800&family=Manrope:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#15122a;
    --bg-2:#1d1a38;
    --ink:#f4f0e8;
    --ink-soft:#b9b3cc;
    --marigold:#f3b53f;
    --marigold-deep:#e08a1e;
    --teal:#3fd0b6;
    --line:rgba(244,240,232,.12);
    --radius-lg:28px;
    --radius:14px;
    --maxw:1120px;
    --display:'Sora',sans-serif;
    --body:'Manrope',sans-serif;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{
    font-family:var(--body);
    background:var(--bg);
    color:var(--ink);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  body::before{
    content:"";position:fixed;inset:0;z-index:-1;pointer-events:none;
    background:
      radial-gradient(900px 500px at 85% -10%, rgba(243,181,63,.16), transparent 60%),
      radial-gradient(700px 500px at -10% 110%, rgba(63,208,182,.12), transparent 60%);
  }
  a{color:inherit;text-decoration:none}
  a:focus-visible,button:focus-visible{outline:2px solid var(--marigold);outline-offset:3px;border-radius:6px}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 24px}
  h1,h2,h3{font-family:var(--display);line-height:1.1;letter-spacing:-.02em}
  h2{font-size:clamp(1.8rem,3.4vw,2.6rem);font-weight:700;margin-bottom:40px}
  section{padding:96px 0}

  /* NAV */
  nav{
    position:sticky;top:0;z-index:50;
    backdrop-filter:blur(14px);
    background:rgba(21,18,42,.72);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{display:flex;align-items:center;justify-content:space-between;height:64px}
  .logo{font-family:var(--display);font-weight:800;font-size:1.1rem}
  .logo span{color:var(--marigold)}
  nav ul{display:flex;gap:28px;list-style:none;font-size:.92rem;color:var(--ink-soft)}
  nav ul a:hover{color:var(--ink)}
  @media(max-width:700px){nav ul{display:none}}

  /* HERO */
  .hero{padding:80px 0 60px;min-height:calc(100vh - 64px);display:flex;align-items:center}
  .hero .wrap{display:grid;grid-template-columns:1.15fr .85fr;gap:48px;align-items:center}
  .hero-kicker{
    display:inline-flex;align-items:center;gap:10px;
    font-size:.85rem;color:var(--ink-soft);margin-bottom:24px;
    padding:8px 14px;border:1px solid var(--line);border-radius:999px;background:rgba(255,255,255,.03);
  }
  .hero-kicker i{width:8px;height:8px;border-radius:50%;background:var(--teal);box-shadow:0 0 0 0 rgba(63,208,182,.6);animation:pulse 2.2s infinite}
  @keyframes pulse{0%{box-shadow:0 0 0 0 rgba(63,208,182,.6)}70%{box-shadow:0 0 0 10px rgba(63,208,182,0)}100%{box-shadow:0 0 0 0 rgba(63,208,182,0)}}
  h1{font-size:clamp(2.6rem,6vw,4.8rem);font-weight:800;margin-bottom:20px}
  .hero p.lead{font-size:1.15rem;color:var(--ink-soft);max-width:34rem;margin-bottom:34px}
  .cta-row{display:flex;gap:14px;flex-wrap:wrap}
  .btn{
    display:inline-flex;align-items:center;gap:8px;padding:14px 22px;border-radius:999px;
    font-weight:600;font-size:.95rem;transition:transform .2s,background .2s,box-shadow .2s;border:1px solid transparent;
  }
  .btn-primary{background:var(--marigold);color:#1b1408;box-shadow:0 10px 30px rgba(243,181,63,.25)}
  .btn-primary:hover{transform:translateY(-2px);background:#ffc45a}
  .btn-ghost{border-color:var(--line);color:var(--ink)}
  .btn-ghost:hover{background:rgba(255,255,255,.05)}
  .stats{display:flex;gap:36px;margin-top:48px;flex-wrap:wrap}
  .stat b{font-family:var(--display);font-size:1.9rem;display:block;color:var(--ink);line-height:1}
  .stat span{font-size:.85rem;color:var(--ink-soft)}

  /* hero entrance — the one orchestrated moment */
  .rise{opacity:0;transform:translateY(22px);animation:rise .8s cubic-bezier(.2,.7,.2,1) forwards}
  .rise:nth-child(1){animation-delay:.05s}.rise:nth-child(2){animation-delay:.18s}.rise:nth-child(3){animation-delay:.31s}
  .rise:nth-child(4){animation-delay:.44s}.rise:nth-child(5){animation-delay:.57s}
  @keyframes rise{to{opacity:1;transform:none}}

  /* PHONE */
  .phone-stage{position:relative;display:flex;justify-content:center;perspective:1200px}
  .phone{
    width:290px;height:590px;border-radius:44px;background:#0b0a16;
    border:8px solid #2a2746;box-shadow:0 40px 80px rgba(0,0,0,.55),inset 0 0 0 2px #000;
    position:relative;overflow:hidden;
    transform:rotateY(-10deg) rotateX(4deg);
    animation:phoneIn 1.2s cubic-bezier(.2,.7,.2,1) .3s both, float 6s ease-in-out 1.5s infinite;
  }
  @keyframes phoneIn{from{opacity:0;transform:rotateY(-30deg) rotateX(8deg) translateY(40px)}to{opacity:1;transform:rotateY(-10deg) rotateX(4deg)}}
  @keyframes float{0%,100%{transform:rotateY(-10deg) rotateX(4deg) translateY(0)}50%{transform:rotateY(-10deg) rotateX(4deg) translateY(-12px)}}
  .notch{position:absolute;top:10px;left:50%;transform:translateX(-50%);width:100px;height:26px;background:#000;border-radius:999px;z-index:5}
  .screen{position:absolute;inset:0}
  .app{position:absolute;inset:0;opacity:0;transition:opacity .7s;padding:56px 18px 20px;display:flex;flex-direction:column}
  .app.active{opacity:1}
  .app-name{font-family:var(--display);font-weight:700;font-size:1.05rem}
  .app-sub{font-size:.72rem;color:var(--ink-soft);margin-bottom:14px}
  .tag{font-size:.62rem;padding:3px 8px;border-radius:999px;background:rgba(255,255,255,.08);color:var(--ink-soft);margin-right:4px;display:inline-block;margin-bottom:4px}

  /* app 1: map */
  .map{flex:1;border-radius:18px;position:relative;overflow:hidden;
    background:
      linear-gradient(rgba(255,255,255,.05) 1px,transparent 1px),
      linear-gradient(90deg,rgba(255,255,255,.05) 1px,transparent 1px),
      linear-gradient(160deg,#1d2a48,#141c33);
    background-size:28px 28px,28px 28px,100% 100%}
  .road{position:absolute;background:rgba(255,255,255,.08);border-radius:4px}
  .route{position:absolute;inset:0;fill:none;stroke:var(--teal);stroke-width:4;stroke-linecap:round;stroke-dasharray:6 8}
  .pin{position:absolute;width:14px;height:14px;background:var(--marigold);border-radius:50% 50% 50% 0;transform:rotate(-45deg);box-shadow:0 0 12px rgba(243,181,63,.7)}
  .avatar{position:absolute;width:18px;height:18px;border-radius:50%;background:var(--teal);border:3px solid #fff;
    offset-path:path("M30 250 C 60 200, 120 210, 140 150 S 210 60, 230 40");animation:walk 7s linear infinite}
  @keyframes walk{to{offset-distance:100%}}
  .eta{position:absolute;left:12px;right:12px;bottom:12px;background:rgba(11,10,22,.9);border-radius:12px;padding:10px 12px;font-size:.72rem;display:flex;justify-content:space-between}
  .eta b{color:var(--teal)}

  /* app 2: onboarding */
  .card-list{display:flex;flex-direction:column;gap:10px;flex:1}
  .row{background:rgba(255,255,255,.06);border-radius:12px;padding:10px 12px;display:flex;align-items:center;gap:10px;font-size:.75rem}
  .row i{width:26px;height:26px;border-radius:8px;background:rgba(243,181,63,.2);flex:none}
  .row .ok{margin-left:auto;color:var(--teal);font-weight:700}
  .face{flex:1;border-radius:16px;background:radial-gradient(circle at 50% 40%,rgba(63,208,182,.2),transparent 50%),rgba(255,255,255,.04);position:relative;margin-top:8px;overflow:hidden}
  .face .frame{position:absolute;inset:22% 25%;border:2px solid var(--teal);border-radius:50%;animation:scan 2.4s ease-in-out infinite}
  @keyframes scan{0%,100%{box-shadow:0 0 0 0 rgba(63,208,182,.4)}50%{box-shadow:0 0 0 8px rgba(63,208,182,0)}}
  .face .line{position:absolute;left:25%;right:25%;height:2px;background:var(--teal);opacity:.8;animation:scanline 2.4s ease-in-out infinite}
  @keyframes scanline{0%,100%{top:22%}50%{top:78%}}

  /* app 3: fintech */
  .score{flex:1;display:flex;flex-direction:column;align-items:center;justify-content:center}
  .ring{width:150px;height:150px;border-radius:50%;background:conic-gradient(var(--marigold) var(--p,0deg),rgba(255,255,255,.08) 0);display:grid;place-items:center;animation:ring 3s ease-out forwards}
  .ring::after{content:"";width:118px;height:118px;border-radius:50%;background:#0b0a16;position:absolute}
  .ring b{position:relative;z-index:1;font-family:var(--display);font-size:1.8rem}
  @property --p{syntax:'<angle>';inherits:false;initial-value:0deg}
  @keyframes ring{to{--p:274deg}}
  .score small{color:var(--ink-soft);font-size:.72rem;margin-top:10px}

  .dots{position:absolute;bottom:-34px;left:50%;transform:translateX(-50%);display:flex;gap:8px}
  .dots i{width:7px;height:7px;border-radius:50%;background:var(--line);transition:background .3s,width .3s}
  .dots i.on{background:var(--marigold);width:20px;border-radius:99px}

  /* ABOUT */
  .about .wrap{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:start}
  .about p{color:var(--ink-soft);font-size:1.05rem;margin-bottom:18px;max-width:38rem}
  .about p strong{color:var(--ink);font-weight:600}
  .now{background:var(--bg-2);border:1px solid var(--line);border-radius:var(--radius-lg);padding:30px}
  .now h3{font-size:1.05rem;margin-bottom:14px}
  .now ul{list-style:none;display:grid;gap:12px}
  .now li{display:flex;gap:12px;font-size:.95rem;color:var(--ink-soft)}
  .now li::before{content:"";width:6px;height:6px;border-radius:50%;background:var(--marigold);margin-top:10px;flex:none}

  /* PROJECTS */
  .feature{
    display:grid;grid-template-columns:1.1fr .9fr;gap:40px;
    background:linear-gradient(135deg,rgba(243,181,63,.12),rgba(63,208,182,.08));
    border:1px solid rgba(243,181,63,.25);border-radius:var(--radius-lg);padding:44px;margin-bottom:28px;
  }
  .feature h3{font-size:1.8rem;margin-bottom:8px}
  .feature .live{display:inline-flex;align-items:center;gap:8px;color:var(--teal);font-weight:600;font-size:.9rem;margin-bottom:18px}
  .feature .live i{width:8px;height:8px;border-radius:50%;background:var(--teal);animation:pulse 2.2s infinite}
  .feature p{color:var(--ink-soft);margin-bottom:16px}
  .feature ul{list-style:none;display:grid;gap:10px;margin-bottom:22px}
  .feature li{display:flex;gap:12px;font-size:.95rem;color:var(--ink-soft)}
  .feature li::before{content:"";width:6px;height:6px;border-radius:50%;background:var(--marigold);margin-top:11px;flex:none}
  .chips{display:flex;flex-wrap:wrap;gap:8px}
  .chip{font-size:.8rem;padding:6px 12px;border-radius:999px;border:1px solid var(--line);color:var(--ink-soft);background:rgba(255,255,255,.03)}
  .feature-visual{display:grid;grid-template-columns:1fr 1fr;gap:14px;align-content:start}
  .mini{background:rgba(11,10,22,.6);border:1px solid var(--line);border-radius:18px;padding:18px;font-size:.85rem;color:var(--ink-soft)}
  .mini b{display:block;font-family:var(--display);color:var(--ink);font-size:1.4rem;margin-bottom:4px}
  .mini.wide{grid-column:1/-1}

  .grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px}
  .proj{background:var(--bg-2);border:1px solid var(--line);border-radius:var(--radius-lg);padding:30px;display:flex;flex-direction:column;gap:12px;transition:border-color .25s,transform .25s}
  .proj:hover{border-color:rgba(243,181,63,.4);transform:translateY(-3px)}
  .proj h3{font-size:1.2rem}
  .proj .ctx{font-size:.82rem;color:var(--marigold);font-weight:600}
  .proj p{color:var(--ink-soft);font-size:.95rem}
  .proj ul{list-style:none;display:grid;gap:8px;font-size:.92rem;color:var(--ink-soft)}
  .proj li{display:flex;gap:10px}.proj li::before{content:"";width:5px;height:5px;border-radius:50%;background:var(--teal);margin-top:10px;flex:none}
  .more{margin-top:24px;display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
  .more div{border:1px solid var(--line);border-radius:var(--radius);padding:18px;font-size:.9rem;color:var(--ink-soft)}
  .more b{color:var(--ink);display:block;margin-bottom:4px;font-weight:600}

  /* EXPERIENCE timeline */
  .timeline{position:relative;padding-left:32px}
  .timeline::before{content:"";position:absolute;left:8px;top:8px;bottom:8px;width:2px;background:linear-gradient(var(--marigold),var(--line))}
  .job{position:relative;padding-bottom:40px}
  .job::before{content:"";position:absolute;left:-30px;top:8px;width:14px;height:14px;border-radius:50%;background:var(--bg);border:3px solid var(--marigold)}
  .job:first-child::before{background:var(--marigold);box-shadow:0 0 0 6px rgba(243,181,63,.2)}
  .job header{display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap;margin-bottom:8px}
  .job h3{font-size:1.15rem}
  .job .co{color:var(--marigold);font-weight:600;font-size:.95rem}
  .job time{color:var(--ink-soft);font-size:.9rem}
  .job ul{list-style:none;display:grid;gap:8px;color:var(--ink-soft);font-size:.95rem;max-width:44rem}
  .job li{display:flex;gap:10px}.job li::before{content:"";width:5px;height:5px;border-radius:50%;background:var(--teal);margin-top:10px;flex:none}
  .job p{color:var(--ink-soft);font-size:.95rem;max-width:44rem}

  /* SKILLS */
  .skills{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
  .sk{background:var(--bg-2);border:1px solid var(--line);border-radius:var(--radius-lg);padding:26px}
  .sk h3{font-size:1rem;margin-bottom:14px}
  .sk .chips .chip{background:transparent}

  /* CONTACT */
  .contact{padding-bottom:120px}
  .contact-box{background:linear-gradient(135deg,var(--marigold),var(--marigold-deep));color:#1b1408;border-radius:var(--radius-lg);padding:56px;display:grid;grid-template-columns:1.2fr .8fr;gap:40px;align-items:center}
  .contact-box h2{margin-bottom:12px;color:#1b1408}
  .contact-box p{max-width:30rem;font-size:1.05rem;color:rgba(27,20,8,.8)}
  .contact-links{display:grid;gap:12px}
  .contact-links a{background:rgba(27,20,8,.12);border-radius:14px;padding:14px 18px;font-weight:600;display:flex;justify-content:space-between;transition:background .2s}
  .contact-links a:hover{background:rgba(27,20,8,.22)}
  footer{text-align:center;color:var(--ink-soft);font-size:.85rem;padding:30px 0}


  /* reveal on scroll (subtle, once) */
  .reveal{opacity:0;transform:translateY(16px);transition:opacity .7s,transform .7s}
  .reveal.in{opacity:1;transform:none}

  @media(max-width:900px){
    .hero .wrap,.about .wrap,.feature,.contact-box{grid-template-columns:1fr}
    .phone-stage{order:-1;margin-bottom:20px}
    .phone{width:240px;height:490px;transform:none;animation:phoneIn2 1s .3s both}
    @keyframes phoneIn2{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:none}}
    .skills,.grid,.more{grid-template-columns:1fr}
    .feature{padding:28px}
    .contact-box{padding:36px}
    section{padding:72px 0}
  }
  @media(prefers-reduced-motion:reduce){
    *,*::before,*::after{animation:none!important;transition:none!important}
    .rise,.reveal{opacity:1;transform:none}
    .phone{transform:none}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <a class="logo" href="#top">Vinay Zade<span>.</span></a>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<header class="hero" id="top">
  <div class="wrap">
    <div>
      <div class="hero-kicker rise"><i></i> Available to join</div>
      <h1 class="rise">I build mobile apps people use every day.</h1>
      <p class="lead rise">Vinay Zade — Senior React Native developer in Mumbai. 9+ years shipping Android and iOS apps for enterprises, and founder of two live products: Ganadhisha, a festival-navigation PWA, and VinAssist, an AI document assistant on Google Play.</p>
      <div class="cta-row rise">
        <a class="btn btn-primary" href="#work">See my work</a>
        <a class="btn btn-ghost" href="https://www.ganadhisha.com" target="_blank" rel="noopener">Open Ganadhisha live</a>
      </div>
      <div class="stats rise">
        <div class="stat"><b>9+</b><span>years in mobile</span></div>
        <div class="stat"><b>6+</b><span>years React Native</span></div>
        <div class="stat"><b>10+</b><span>apps shipped</span></div>
        <div class="stat"><b>2</b><span>products founded</span></div>
      </div>
    </div>

    <div class="phone-stage">
      <div class="phone" aria-hidden="true">
        <div class="notch"></div>
        <div class="screen">
          <div class="app active" data-app="0">
            <div class="app-name">Ganadhisha</div>
            <div class="app-sub">Live darshan navigation · Lalbaug</div>
            <div class="map">
              <div class="road" style="left:20px;top:60px;width:6px;height:200px"></div>
              <div class="road" style="left:20px;top:150px;width:200px;height:6px"></div>
              <div class="road" style="left:150px;top:30px;width:6px;height:230px"></div>
              <svg class="route" viewBox="0 0 254 300" preserveAspectRatio="none"><path d="M30 250 C 60 200, 120 210, 140 150 S 210 60, 230 40"/></svg>
              <div class="pin" style="left:222px;top:26px"></div>
              <div class="pin" style="left:95px;top:120px;opacity:.6"></div>
              <div class="avatar"></div>
              <div class="eta"><span>Lalbaugcha Raja</span><b>650 m · 8 min</b></div>
            </div>
          </div>

          <div class="app" data-app="1">
            <div class="app-name">MyJob</div>
            <div class="app-sub">Online test · Candidate verification</div>
            <div class="card-list">
              <div class="row"><i></i>Documents uploaded <span class="ok">✓</span></div>
              <div class="row"><i></i>Offer accepted <span class="ok">✓</span></div>
              <div class="row"><i></i>Face verification <span style="margin-left:auto;color:var(--marigold)">…</span></div>
              <div class="face"><div class="frame"></div><div class="line"></div></div>
            </div>
          </div>

          <div class="app" data-app="2">
            <div class="app-name">VinAssist</div>
            <div class="app-sub">AI document assistant · Google Play</div>
            <div class="card-list">
              <div class="face" style="flex:0 0 130px;margin-top:0"><div class="frame" style="border-radius:8px;inset:14% 12%"></div><div class="line"></div></div>
              <div class="row"><i></i>OCR (on-device) <span class="ok">✓</span></div>
              <div class="row"><i></i>Total: ₹4,250 · Due 30 Sep <span class="ok">✓</span></div>
              <div class="row"><i></i>Ask the document… <span style="margin-left:auto;color:var(--marigold)">→</span></div>
            </div>
          </div>
        </div>
      </div>
      <div class="dots"><i class="on"></i><i></i><i></i></div>
    </div>
  </div>
</header>

<section class="about" id="about">
  <div class="wrap">
    <div class="reveal">
      <h2>About me</h2>
      <p>I've spent nine years building mobile apps, the last six leading <strong>React Native</strong> work across Android and iOS. My day-to-day is architecture, state management with Redux Toolkit, native modules in Kotlin and Java, and getting releases out through the App Store and Google Play.</p>
      <p>At Tech Mahindra I lead the mobile side of enterprise projects — I'm the technical contact for clients, I mentor a team of 3–5 developers, and I own the architecture. I've migrated native Kotlin apps to React Native and cut development effort by around 40% without losing platform features.</p>
      <p>Outside work I've shipped two products of my own: <strong>Ganadhisha</strong>, a full-stack PWA with custom maps, AI features and payments for Mumbai's Ganpati festival, and <strong>VinAssist</strong>, an AI document assistant on Google Play with on-device OCR and a RAG-based document chat.</p>
    </div>
    <div class="now reveal">
      <h3>What I bring to a team</h3>
      <ul>
        <li>End-to-end ownership: from technical design and library choices to production monitoring.</li>
        <li>Native depth: React Native bridging, Kotlin/Java modules, TensorFlow Lite and ML Kit on device.</li>
        <li>Product thinking: I've shipped and monetised my own apps, so I care about users, not just code.</li>
        <li>Clear communication with clients, product managers and junior developers.</li>
      </ul>
    </div>
  </div>
</section>

<section id="work">
  <div class="wrap">
    <h2 class="reveal">Selected work</h2>

    <article class="feature reveal">
      <div>
        <h3>Ganadhisha</h3>
        <a class="live" href="https://www.ganadhisha.com" target="_blank" rel="noopener"><i></i> Live at ganadhisha.com</a>
        <p>A mobile-first Progressive Web App that helps devotees navigate Mumbai's Ganpati festival across Lalbaug, Parel and Khetwadi — from finding pandals to walking there to taking home an AI-generated souvenir photo. Founder and sole developer.</p>
        <ul>
          <li>Custom animated Mapbox map with live GPS tracking; a personalised avatar walks the route with distance and time estimates.</li>
          <li>Festival facilities layer: food, washrooms, water, medical help, police, parking, petrol pumps and stations with one-tap navigation.</li>
          <li>"Selfie with Bappa": upload a selfie, pick a Ganpati, and an AI pipeline composes a shareable souvenir.</li>
          <li>Marathi, Hindi and English UI; installable with offline caching; Razorpay payments, sponsored listings and GA4 analytics.</li>
          <li>Traction (GA4, last 7 days of the live festival): 756 active users and 5,563 events.</li>
        </ul>
        <div class="chips">
          <span class="chip">Next.js</span><span class="chip">TypeScript</span><span class="chip">Redux Toolkit</span><span class="chip">RTK Query</span><span class="chip">PWA</span><span class="chip">Mapbox</span><span class="chip">FastAPI</span><span class="chip">PostgreSQL</span><span class="chip">pgvector</span><span class="chip">JWT auth</span><span class="chip">Vercel</span><span class="chip">Railway</span><span class="chip">Cloudflare</span><span class="chip">Razorpay</span>
        </div>
      </div>
      <div class="feature-visual">
        <div class="mini"><b>756</b>active users in 7 days (GA4)</div>
        <div class="mini"><b>5,563</b>events tracked, live festival</div>
        <div class="mini wide"><b>Full stack</b>Next.js frontend on Vercel, FastAPI backend on Railway, PostgreSQL, Cloudflare in front. Designed, built and deployed by one person.</div>
        <div class="mini wide"><b>Real users</b>Serves festival visitors every year during Ganeshotsav — live now.</div>
      </div>
    </article>

    <div class="grid">
      <article class="proj reveal">
        <span class="ctx">Tech Mahindra · Android & iOS</span>
        <h3>MyJob — recruitment & digital onboarding</h3>
        <p>Enterprise platform for online tests, document upload, offer acceptance and candidate engagement.</p>
        <ul>
          <li>Directed the React Native architecture and team delivery; standardised Redux Toolkit, modular structure and reusable components.</li>
          <li>Embedded TensorFlow Lite face detection and candidate verification via React Native-to-Android bridging.</li>
          <li>Built image quality validation, sentiment analysis and a rule-based FAQ chatbot.</li>
        </ul>
        <div class="chips"><span class="chip">React Native</span><span class="chip">TypeScript</span><span class="chip">TensorFlow Lite</span><span class="chip">Firebase</span><span class="chip">Native Android</span></div>
      </article>

      <article class="proj reveal">
        <span class="ctx">Personal product · Android · <a href="https://play.google.com/store/search?q=VinsAiAssist&c=apps" target="_blank" rel="noopener" style="text-decoration:underline">Live on Google Play as "VinsAiAssist"</a></span>
        <h3>VinAssist — AI document assistant</h3>
        <p>Turns photos of documents, receipts and invoices into usable data — text, summaries, structured fields and Q&amp;A. Founder and sole developer.</p>
        <ul>
          <li>Privacy-first capture: Kotlin native modules wrap Google ML Kit for on-device OCR, face detection and sharpness/exposure checks — images never leave the phone for validation.</li>
          <li>RAG document chat: documents are chunked, embedded (MiniLM) and stored in pgvector; only the top matching chunks reach Llama 3.1, which cites its sources.</li>
          <li>FastAPI + async SQLAlchemy on PostgreSQL, JWT with rotating refresh tokens, vendor-neutral AI provider layer, ~320 automated tests.</li>
        </ul>
        <div class="chips"><span class="chip">React Native</span><span class="chip">TypeScript</span><span class="chip">Kotlin</span><span class="chip">Google ML Kit</span><span class="chip">FastAPI</span><span class="chip">PostgreSQL</span><span class="chip">pgvector</span><span class="chip">Hugging Face</span></div>
      </article>
    </div>

    <div class="more reveal">
      <div><b>Perks</b>React Native home-services app: cart, scheduling, checkout.</div>
      <div><b>PORT</b>Native Android live-events and artist-merchandise app.</div>
      <div><b>Crowd Wisdom</b>Native Android quizzes, prediction games and live blog.</div>
      <div><b>Employee Self Services</b>React Native attendance, leave and task workflows.</div>
      <div><b>Dove</b>Angular and mobile enterprise modules with production support.</div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <h2 class="reveal">Experience</h2>
    <div class="timeline">
      <div class="job reveal">
        <header><div><h3>Senior Mobile Application Developer (React Native Lead)</h3><span class="co">Tech Mahindra Ltd.</span></div><time>Dec 2020 – Present</time></header>
        <ul>
          <li>Lead React Native development for Android and iOS — architecture, state management, module structure, library selection and delivery.</li>
          <li>Integrate native Android capabilities, third-party SDKs, Firebase, SSL pinning and camera workflows through native modules and bridging.</li>
          <li>Migrated native Kotlin apps to React Native, reducing development effort by ~40%.</li>
          <li>Primary technical contact for clients; mentor 3–5 developers, run code reviews and own production releases.</li>
        </ul>
      </div>
      <div class="job reveal">
        <header><div><h3>Mobile Application Developer</h3><span class="co">Sunday Mobility</span></div><time>Feb 2020 – Oct 2020</time></header>
        <p>Native Android modules with Kotlin, MVVM, Coroutines, ViewModel, LiveData, Retrofit and dependency injection.</p>
      </div>
      <div class="job reveal">
        <header><div><h3>Mobile App Developer</h3><span class="co">Balaji Data Services</span></div><time>Feb 2019 – Feb 2020</time></header>
        <p>Native Android apps in Java for attendance, leave and task management with REST-driven workflows.</p>
      </div>
      <div class="job reveal">
        <header><div><h3>Mobile App Developer</h3><span class="co">WeApplify Technologies</span></div><time>May 2017 – Dec 2018</time></header>
        <p>Android apps in Java and Kotlin using REST APIs and third-party SDKs in Agile teams.</p>
      </div>
      <div class="job reveal">
        <header><div><h3>Software Developer (Mobile)</h3><span class="co">Technople Solution</span></div><time>Mar 2016 – Oct 2016</time></header>
        <p>Native Android apps with Java, REST API and SDK integrations.</p>
      </div>
    </div>
    <p class="reveal" style="color:var(--ink-soft);margin-top:8px">B.Sc. Information Technology, Mumbai University (2015) · Certifications: AI White Belt, Claude Code Certification</p>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <h2 class="reveal">Skills</h2>
    <div class="skills">
      <div class="sk reveal"><h3>React Native & web</h3><div class="chips"><span class="chip">React Native CLI</span><span class="chip">TypeScript</span><span class="chip">Redux Toolkit</span><span class="chip">React Navigation</span><span class="chip">Hooks & Context</span><span class="chip">Next.js</span><span class="chip">React.js</span><span class="chip">RTK Query</span><span class="chip">PWA</span></div></div>
      <div class="sk reveal"><h3>Native mobile</h3><div class="chips"><span class="chip">Android</span><span class="chip">iOS</span><span class="chip">Kotlin</span><span class="chip">Java</span><span class="chip">Native modules</span><span class="chip">Bridging</span><span class="chip">Camera</span><span class="chip">Geolocation</span><span class="chip">Device APIs</span></div></div>
      <div class="sk reveal"><h3>Architecture & performance</h3><div class="chips"><span class="chip">Clean Architecture</span><span class="chip">MVVM</span><span class="chip">Modular design</span><span class="chip">Caching</span><span class="chip">Performance tuning</span><span class="chip">SSL pinning</span></div></div>
      <div class="sk reveal"><h3>Backend & cloud</h3><div class="chips"><span class="chip">REST APIs</span><span class="chip">Firebase</span><span class="chip">FCM</span><span class="chip">Crashlytics</span><span class="chip">Python</span><span class="chip">FastAPI</span><span class="chip">PostgreSQL</span><span class="chip">pgvector</span><span class="chip">JWT auth</span><span class="chip">Vercel</span><span class="chip">Railway</span><span class="chip">Cloudflare</span><span class="chip">CI/CD</span></div></div>
      <div class="sk reveal"><h3>AI integration</h3><div class="chips"><span class="chip">TensorFlow Lite</span><span class="chip">Face detection</span><span class="chip">Image validation</span><span class="chip">Sentiment analysis</span><span class="chip">Hugging Face</span><span class="chip">Generative image APIs</span><span class="chip">Google ML Kit</span><span class="chip">RAG / pgvector</span><span class="chip">Llama 3.1</span></div></div>
      <div class="sk reveal"><h3>Delivery & leadership</h3><div class="chips"><span class="chip">Agile / Scrum</span><span class="chip">Technical design</span><span class="chip">Client communication</span><span class="chip">Mentoring</span><span class="chip">Code reviews</span><span class="chip">App Store & Play releases</span><span class="chip">Jest</span><span class="chip">Detox</span></div></div>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="wrap">
    <div class="contact-box reveal">
      <div>
        <h2>Let's build something.</h2>
        <p>I'm available to join and open to senior React Native and mobile lead roles. Mumbai or remote.</p>
      </div>
      <div class="contact-links">
        <a href="mailto:zadevinay15@gmail.com"><span>Email</span><span>zadevinay15@gmail.com</span></a>
        <a href="tel:+919870055219"><span>Phone</span><span>+91 98700 55219</span></a>
        <a href="https://www.linkedin.com/in/vinay-zade-8b453810a/" target="_blank" rel="noopener"><span>LinkedIn</span><span>vinay-zade</span></a>
        <a href="https://github.com/vinayzade/" target="_blank" rel="noopener"><span>GitHub</span><span>vinayzade</span></a>
        <a href="https://www.ganadhisha.com" target="_blank" rel="noopener"><span>Ganadhisha</span><span>ganadhisha.com</span></a>
      </div>
    </div>
  </div>
</section>

<footer>© <span id="yr"></span> Vinay Suresh Zade, Mumbai, India &nbsp;·&nbsp; <a href="https://www.linkedin.com/in/vinay-zade-8b453810a/" target="_blank" rel="noopener">LinkedIn</a> &nbsp;·&nbsp; <a href="https://github.com/vinayzade/" target="_blank" rel="noopener">GitHub</a></footer>

<script>
  document.getElementById('yr').textContent = new Date().getFullYear();

  // Phone screen carousel
  const apps = document.querySelectorAll('.app');
  const dots = document.querySelectorAll('.dots i');
  let idx = 0;
  const reduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  if (!reduced) {
    setInterval(() => {
      apps[idx].classList.remove('active'); dots[idx].classList.remove('on');
      idx = (idx + 1) % apps.length;
      apps[idx].classList.add('active'); dots[idx].classList.add('on');
      }, 4500);
  }

  // Scroll reveal (once)
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>
</body>
</html>
