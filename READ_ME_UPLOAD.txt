<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="crossorigin"><link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&family=Raleway:wght@700;800&display=swap" rel="stylesheet"><style>
html{scroll-behavior:smooth}
body{margin:0;background:#0D0B1A;font-family:'DM Sans',system-ui,sans-serif;color:#F4F0FF;color-scheme:dark}
a{color:#F577A1;text-decoration:none}a:hover{color:#F8A0BE}
input::placeholder{color:#77719A}select:invalid{color:#77719A}
@keyframes ots-marquee{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.ots-hero-cinematic{position:relative;min-height:calc(100vh - 70px);display:flex;align-items:center;overflow:hidden;border-bottom:1px solid rgba(244,240,255,.12);background:#0D0B1A}
.ots-hero-cinematic:before{content:"";position:absolute;inset:-7%;background-image:linear-gradient(90deg,rgba(13,11,26,.88) 0%,rgba(13,11,26,.63) 46%,rgba(13,11,26,.2) 100%),linear-gradient(180deg,rgba(13,11,26,.46),rgba(13,11,26,.78)),url("./assets/ots-group-stage.jpg");background-size:cover;background-position:center 44%;background-attachment:fixed;transform:scale(1.04);filter:saturate(1.12) contrast(1.08) brightness(1.08)}
.ots-hero-cinematic:after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(13,11,26,.04) 42%,#0D0B1A 100%);pointer-events:none}
.ots-hero-content{position:relative;z-index:1;width:min(1140px,100% - 48px);margin:0 auto;display:block;padding:clamp(104px,13vw,178px) 0 clamp(86px,10vw,128px)}
.ots-eyebrow{font-size:clamp(11px,1.2vw,12.5px);font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1}
.ots-title{margin:16px 0 0;max-width:14ch;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(48px,7.8vw,104px);line-height:.94;color:#F4F0FF;text-wrap:balance}
.ots-title em{font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent}
.ots-lede{margin:24px 0 0;max-width:55ch;font-size:clamp(16px,1.55vw,20px);line-height:1.65;color:#C9C3DE;text-wrap:pretty}
.ots-actions{display:flex;align-items:center;gap:18px;flex-wrap:wrap;margin-top:28px}
.ots-primary{display:flex;align-items:center;justify-content:center;gap:8px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);color:#fff;font-size:15px;font-weight:700;padding:16px 28px;border-radius:3px;box-shadow:0 16px 60px rgba(245,119,161,.24)}
.ots-secondary{font-size:13.5px;font-weight:500;color:#B9B3D0;text-decoration:underline;text-underline-offset:3px}
.ots-meta{margin-top:20px;font-size:13px;color:#B9B3D0}
.ots-hero-proof{border:1px solid rgba(244,240,255,.2);background:rgba(13,11,26,.58);backdrop-filter:blur(16px);border-radius:3px;padding:18px;box-shadow:0 24px 80px rgba(0,0,0,.28)}
.ots-proof-label{font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1}
.ots-proof-image{margin-top:12px;aspect-ratio:16/10;border-radius:3px;overflow:hidden;border:1px solid rgba(244,240,255,.16)}
.ots-proof-image img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .85s cubic-bezier(.2,.7,.2,1),filter .85s ease}
.ots-hero-proof:hover .ots-proof-image img{transform:scale(1.08);filter:saturate(1.1) contrast(1.08)}
.ots-proof-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:12px}
.ots-proof-grid div{border:1px solid rgba(244,240,255,.13);background:rgba(244,240,255,.05);padding:13px 12px;border-radius:3px}
.ots-proof-grid strong{display:block;font-family:'Playfair Display',serif;font-size:28px;line-height:1;color:#F4F0FF}
.ots-proof-grid span{display:block;margin-top:5px;font-size:10px;text-transform:uppercase;letter-spacing:.08em;color:#7E78A0}
.zoom-media{position:relative;overflow:hidden;border-radius:3px;isolation:isolate;background:rgba(244,240,255,.05)}
.zoom-media img{transition:transform .85s cubic-bezier(.2,.7,.2,1),filter .85s ease;will-change:transform;backface-visibility:hidden}
.zoom-media:after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,transparent 45%,rgba(13,11,26,.36));opacity:0;transition:opacity .55s ease;pointer-events:none}
.zoom-media:hover img{transform:scale(1.08);filter:saturate(1.08) contrast(1.06)}
.zoom-media:hover:after{opacity:1}
.ots-parallax-band{position:relative;min-height:clamp(270px,34vw,430px);display:flex;align-items:center;overflow:hidden;margin-top:clamp(34px,5vw,72px);border-top:1px solid rgba(244,240,255,.2);border-bottom:1px solid rgba(244,240,255,.2);background:#0D0B1A}
.ots-parallax-band:before{content:"";position:absolute;inset:-6%;background-image:linear-gradient(90deg,rgba(13,11,26,.9),rgba(13,11,26,.48),rgba(13,11,26,.86)),var(--band-image);background-size:var(--band-size,cover);background-repeat:no-repeat;background-position:var(--band-position,center);background-attachment:fixed;transform:scale(1.04);filter:saturate(1.06) contrast(1.04)}
.ots-portrait-band{min-height:clamp(360px,27vw,510px)}
.ots-portrait-band:before{inset:-16%;background-image:var(--band-image);background-size:cover;background-position:var(--band-back-position,center 52%);background-attachment:scroll;transform:scale(1.08);filter:blur(15px) saturate(1.06) contrast(1.03) brightness(1.02);opacity:1}
.ots-portrait-band:after{background:linear-gradient(180deg,rgba(244,240,255,.02) 0 15%,rgba(244,240,255,.2) 15%,rgba(13,11,26,.36) 15.2%,rgba(13,11,26,.36) 86%,rgba(13,11,26,.12) 86.2% 100%),linear-gradient(90deg,rgba(13,11,26,.45) 0%,rgba(13,11,26,.22) 48%,rgba(13,11,26,.42) 100%)}
.ots-portrait-band .ots-band-inner{width:min(1420px,75vw);min-height:clamp(360px,27vw,510px);padding:0;display:grid;grid-template-columns:minmax(0,1fr) minmax(200px,260px);gap:44px;align-items:center;position:relative;isolation:isolate}
.ots-portrait-band .ots-band-inner:before{content:"";position:absolute;top:0;bottom:0;left:58%;width:min(20vw,392px);z-index:-1;background-image:var(--band-image);background-size:cover;background-position:var(--band-position,center 50%);background-repeat:no-repeat;opacity:.94;filter:saturate(1.06) contrast(1.03);-webkit-mask-image:linear-gradient(90deg,transparent 0%,rgba(0,0,0,.7) 8%,#000 17%,#000 82%,rgba(0,0,0,.72) 91%,transparent 100%);mask-image:linear-gradient(90deg,transparent 0%,rgba(0,0,0,.7) 8%,#000 17%,#000 82%,rgba(0,0,0,.72) 91%,transparent 100%)}
.ots-portrait-band .ots-band-inner>div:first-child{transform:translateY(12px)}
.ots-portrait-band .ots-band-kicker{font-size:clamp(12px,.85vw,16px);letter-spacing:.06em;color:#ff5d9b;margin-bottom:clamp(16px,1.25vw,24px)}
.ots-portrait-band .ots-band-title{font-size:clamp(54px,4.75vw,90px);line-height:.72;max-width:680px;color:#f7f1ff}
.ots-portrait-band .ots-band-copy{font-size:clamp(18px,1.35vw,25px);line-height:1.28;max-width:800px;margin-top:clamp(20px,1.5vw,28px);color:#f2eefb}
.ots-portrait-band .ots-band-card{justify-self:end;align-self:end;margin-bottom:clamp(70px,5.6vw,106px);width:clamp(170px,11.8vw,224px);height:clamp(55px,3.8vw,72px);padding:0;display:flex;align-items:center;justify-content:center;border-color:#ff5d9b;background:rgba(13,11,26,.82);box-shadow:none;font-size:clamp(12px,.85vw,16px);letter-spacing:.06em;color:#ff5d9b}
.ots-parallax-band:after{content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(13,11,26,.18),rgba(13,11,26,.46));pointer-events:none}
.ots-band-inner{position:relative;z-index:1;width:min(1140px,100% - 48px);margin:0 auto;padding:clamp(60px,7vw,96px) 0;display:flex;flex-direction:column;gap:16px;align-items:flex-start}
.ots-band-inner.center{align-items:center;text-align:center}
.ots-band-kicker{font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1}
.ots-band-title{margin:0;max-width:16ch;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(34px,5vw,70px);line-height:1;color:#F4F0FF;text-wrap:balance}
.ots-band-copy{margin:0;max-width:54ch;font-size:clamp(15px,1.5vw,18px);line-height:1.65;color:#C9C3DE;text-wrap:pretty}
.ots-final-cta{margin-top:clamp(56px,8vw,104px)}
.ots-final-cta .ots-band-title{max-width:22ch}
.ots-concept-divider{width:min(1140px,100% - 48px);margin:0 auto;padding:clamp(44px,7vw,72px) 0 clamp(28px,4vw,48px)}
.ots-concept-divider h2{margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(30px,4.8vw,56px);line-height:1.05;color:#F4F0FF;text-wrap:balance}
.ots-concept-divider p{margin:8px 0 0;font-size:13px;letter-spacing:.12em;text-transform:uppercase;color:#7E78A0}
.ots-gradient-rule{height:4px;margin-top:22px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)}
.ots-band-card{align-self:flex-end;border:1px solid rgba(245,119,161,.78);background:rgba(13,11,26,.78);padding:20px 26px;border-radius:3px;font-size:12px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1;box-shadow:0 20px 70px rgba(0,0,0,.28)}
.ots-why-section{position:relative;overflow:hidden;background:#0D0B1A;padding:clamp(40px,6vw,72px) 0 clamp(36px,6vw,70px)}
.ots-why-section:after{content:"";position:absolute;inset:0;z-index:1;background:linear-gradient(90deg,rgba(13,11,26,.88) 0%,rgba(13,11,26,.64) 44%,rgba(13,11,26,.82) 100%),linear-gradient(180deg,#0D0B1A 0%,rgba(13,11,26,.18) 24%,rgba(13,11,26,.34) 68%,#0D0B1A 100%);pointer-events:none}
.ots-why-photo{position:absolute;inset:-7%;z-index:0;background-image:url("./assets/ots-why-wide.jpg");background-repeat:no-repeat;background-size:cover;background-position:center top;background-attachment:scroll;transform:scale(1.04);filter:saturate(1.1) contrast(1.06) brightness(.92);opacity:.96;pointer-events:none}
.ots-why-inner{position:relative;z-index:2;width:min(1140px,100% - 48px);min-height:clamp(420px,38vw,520px);margin:0 auto;display:grid;grid-template-columns:minmax(120px,170px) minmax(180px,1fr) minmax(300px,420px);gap:clamp(24px,4vw,58px);align-items:center}
.ots-why-kicker{align-self:start;margin-top:clamp(24px,4vw,48px);font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1}
.ots-why-copy{grid-column:3;display:flex;flex-direction:column;gap:22px}
.ots-why-copy p{margin:0;max-width:32ch;font-size:clamp(18px,1.8vw,24px);line-height:1.5;color:#E4DFF6;text-wrap:pretty}
.ots-why-copy .ots-why-line{max-width:12ch;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(38px,4.2vw,64px);line-height:1.04;color:#F4F0FF;text-wrap:balance}
.ots-why-copy .ots-why-line em{font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent}
@media (min-width:801px){.ots-band-inner.split{display:grid;grid-template-columns:minmax(0,1fr) minmax(220px,320px);align-items:center}.ots-band-inner.split .ots-band-card{justify-self:end}}
@media (max-width:800px){.ots-hero-content{padding-top:82px}.ots-hero-cinematic:before,.ots-parallax-band:before,.ots-why-photo{background-attachment:scroll}.ots-proof-grid{grid-template-columns:repeat(3,1fr)}.ots-title{font-size:clamp(44px,14vw,76px)}.ots-band-card{align-self:flex-start}.ots-why-inner{grid-template-columns:1fr;min-height:560px;align-items:start}.ots-why-photo{inset:-7%;background-position:center top;opacity:.96;filter:saturate(1.1) contrast(1.06) brightness(.92)}.ots-why-section:after{background:linear-gradient(90deg,rgba(13,11,26,.88) 0%,rgba(13,11,26,.64) 44%,rgba(13,11,26,.82) 100%),linear-gradient(180deg,#0D0B1A 0%,rgba(13,11,26,.18) 24%,rgba(13,11,26,.34) 68%,#0D0B1A 100%)}.ots-why-copy{grid-column:1;margin-top:220px}.ots-why-copy p{font-size:17px}.ots-portrait-band{min-height:560px}.ots-portrait-band .ots-band-inner{width:min(720px,calc(100% - 48px));grid-template-columns:1fr;min-height:560px;padding:56px 0;gap:20px;align-items:start}.ots-portrait-band .ots-band-inner:before{top:180px;bottom:42px;left:8%;width:84%;opacity:.78}.ots-portrait-band .ots-band-inner>div:first-child{transform:none}.ots-portrait-band .ots-band-title{font-size:clamp(46px,13vw,68px);line-height:.82}.ots-portrait-band .ots-band-copy{font-size:16px;line-height:1.5}.ots-portrait-band .ots-band-card{justify-self:start;align-self:end;margin-bottom:0;width:190px;height:60px}}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}html{scroll-behavior:auto}.ots-hero-cinematic:before,.ots-parallax-band:before{background-attachment:scroll}}
</style>
</head>
<body>

<div style="display:flex;flex-direction:column;min-height:100vh;background:#0D0B1A">
<div style="display:flex;align-items:center;justify-content:center;gap:12px;flex-wrap:wrap;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);color:#fff;padding:9px 20px;font-size:12.5px;font-weight:700;text-align:center">
<span>Cohort 1 forming now â€” 7 of 15 seats left</span>
<a href="#apply" style="color:#fff;font-weight:700;white-space:nowrap;text-decoration:underline;text-underline-offset:3px">Claim yours â†’</a>
</div>
<div data-screen-label="Nav" style="position:sticky;top:0;z-index:50;background:rgba(13,11,26,.97);border-bottom:1px solid rgba(244,240,255,.12)">
<div style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:16px;flex-wrap:wrap;padding:16px 0">
<div style="font-family:Raleway,sans-serif;font-weight:800;font-size:17px;color:#F4F0FF;white-space:nowrap">On The Streets</div>
<div style="display:flex;align-items:center;gap:clamp(14px,2.5vw,28px);font-size:11px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;flex-wrap:wrap">
<a href="#method" style="color:#B9B3D0">Method</a><a href="#pace" style="color:#B9B3D0">Pace</a><a href="#stories" style="color:#B9B3D0">Stories</a><a href="#faq" style="color:#B9B3D0">FAQ</a>
</div>
<a href="https://wa.me/919841610111?text=Hi%2C%20I%27m%20interested%20in%20joining%20the%20performer%20program." style="border:1px solid rgba(244,240,255,.35);color:#F4F0FF;font-size:11px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;padding:9px 14px;border-radius:3px;white-space:nowrap">WhatsApp us</a>
</div>
</div>
<section data-screen-label="Hero" class="ots-hero-cinematic">
<div class="ots-hero-content">
<div>
<div class="ots-eyebrow">The Couch-to-Stage Program Â· Chennai</div>
<h1 class="ots-title">From your couch to a stage <em>perform in 45 days.</em></h1>
<p class="ots-lede">Solo â€” your own 3â€“5 song set, played to a real crowd. Even if you've never held a guitar. Not lessons. A stage.</p>
<div class="ots-actions">
<a href="https://wa.me/919841610111?text=Hi%2C%20I%27m%20interested%20in%20joining%20the%20performer%20program." class="ots-primary">Message us on WhatsApp â†’</a>
<a href="#apply" class="ots-secondary">or apply with the form</a>
</div>
<div class="ots-meta">45 days Â· 3 online sessions a week, from home Â· one real stage at the end.</div>
</div>
</div>
</section>
<div style="border-top:1px solid rgba(244,240,255,.12);border-bottom:1px solid rgba(244,240,255,.12);padding:20px 0;display:flex;flex-direction:column;gap:14px">
<div style="text-align:center;font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#7E78A0">Where On The Streets has played</div>
<div style="overflow:hidden">
<div style="display:flex;width:max-content;animation:ots-marquee 36s linear infinite">
<div style="display:flex;align-items:center;gap:28px;padding-right:28px">
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Marina Beach</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Chennai Metro</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">City parks</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Awe50me Weekend</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">VTK audio launch â€” opened for A.R. Rahman</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Little Boy â€” the music van</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">1,500+ street shows</span><span style="color:#F577A1;font-size:8px">â—†</span>
</div>
<div style="display:flex;align-items:center;gap:28px;padding-right:28px">
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Marina Beach</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Chennai Metro</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">City parks</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Awe50me Weekend</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">VTK audio launch â€” opened for A.R. Rahman</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">Little Boy â€” the music van</span><span style="color:#F577A1;font-size:8px">â—†</span>
<span style="font-family:'Playfair Display',serif;font-style:italic;font-size:17px;color:#C9C3DE;white-space:nowrap">1,500+ street shows</span><span style="color:#F577A1;font-size:8px">â—†</span>
</div>
</div>
</div>
</div>
<section data-screen-label="Why OTS" class="ots-why-section">
<div class="ots-why-photo" aria-hidden="true"></div>
<div class="ots-why-inner">
<div class="ots-why-kicker">Why OTS</div>
<div class="ots-why-copy">
<p>OTS is a stage with a method attached. A real venue. A 74,000-strong audience. A 1,000+ musician network.</p>
<div class="ots-why-line">People <em>end the someday.</em></div>
<a href="#method" style="font-size:14px;font-weight:700;color:#F577A1">Explore the method â†’</a>
</div>
</div>
</section>
<div class="ots-concept-divider">
<h2>From Chennai streets to <em style="font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent">your first stage.</em></h2>
<p>real shows + real crowd + real deadline</p>
<div class="ots-gradient-rule"></div>
</div>
<section data-screen-label="Word on the street" class="ots-parallax-band" style="--band-image:url('./assets/ots-stage-lights.jpg');--band-position:center 48%">
<div class="ots-band-inner split">
<div>
<div class="ots-band-kicker">Word on the street</div>
<h2 class="ots-band-title" style="font-style:italic">"You guys made our day."</h2>
<p class="ots-band-copy">A stranger said it at the cafe jam where On The Streets began. That sentence is why OTS exists.</p>
</div>
<div class="ots-band-card">Spreading smiles</div>
</div>
</section>
<section id="stories" data-screen-label="Stories" class="ots-parallax-band ots-portrait-band" style="--band-image:url('./assets/ots-real-chennai-guitarist.png');--band-back-position:center 52%;--band-position:center 50%">
<div class="ots-band-inner split">
<div>
<div class="ots-band-kicker">Stories</div>
<h2 class="ots-band-title">Real Chennai locations.</h2>
<p class="ots-band-copy">The program is built around actual public performance energy, not a classroom-only promise. You train for a real moment.</p>
</div>
<div class="ots-band-card">Week 1 to stage</div>
</div>
</section>
<section data-screen-label="Crowd proof" class="ots-parallax-band" style="--band-image:url('./assets/ots-beach-crowd.jpg');--band-position:center 58%">
<div class="ots-band-inner split">
<div>
<div class="ots-band-kicker">Crowd proof</div>
<h2 class="ots-band-title">A deadline you can feel.</h2>
<p class="ots-band-copy">A real crowd at the end changes how people practise. The show date is the method.</p>
</div>
<div class="ots-band-card">45 days - 1 stage</div>
</div>
</section>
<div id="method" data-screen-label="The method" style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<div style="font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1">The method</div>
<div style="display:flex;align-items:flex-end;justify-content:space-between;gap:20px;flex-wrap:wrap">
<h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(30px,3.6vw,44px);line-height:1.12;color:#F4F0FF">Couch to <em style="font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent">Stage</em></h2>
<p style="margin:0;font-size:14px;line-height:1.65;color:#B9B3D0;max-width:46ch;text-wrap:pretty">Like Couch-to-5K, but the finish line is a stage. Four checkpoints, day by day â€” 1:1 coaching at the core, plus a weekly group class with your cohort of 15.</p>
</div>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(230px,100%),1fr));gap:clamp(16px,2.5vw,28px);margin-top:8px">
<div style="border-top:1px solid rgba(245,119,161,.4);padding-top:18px;display:flex;flex-direction:column;gap:10px">
<div style="width:34px;height:34px;border-radius:3px;background:rgba(244,240,255,.05);border:1px solid rgba(245,119,161,.5);color:#F577A1;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center">01</div>
<div style="font-family:'Playfair Display',serif;font-weight:600;font-size:21px;color:#F4F0FF">Busker <span style="color:#F577A1">Â· ~day 12</span></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">Your hands hurt, then your first riff lands. "I can't" becomes "I played that."</p>
</div>
<div style="border-top:1px solid rgba(245,119,161,.4);padding-top:18px;display:flex;flex-direction:column;gap:10px">
<div style="width:34px;height:34px;border-radius:3px;background:rgba(244,240,255,.05);border:1px solid rgba(245,119,161,.5);color:#F577A1;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center">02</div>
<div style="font-family:'Playfair Display',serif;font-weight:600;font-size:21px;color:#F4F0FF">Soloist <span style="color:#F577A1">Â· ~day 30</span></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">You can play your whole 3â€“5 song set, solo, start to finish.</p>
</div>
<div style="border-top:1px solid rgba(245,119,161,.4);padding-top:18px;display:flex;flex-direction:column;gap:10px">
<div style="width:34px;height:34px;border-radius:3px;background:rgba(244,240,255,.05);border:1px solid rgba(245,119,161,.5);color:#F577A1;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center">03</div>
<div style="font-family:'Playfair Display',serif;font-weight:600;font-size:21px;color:#F4F0FF">Dress <span style="color:#F577A1">Â· ~day 40</span></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">A full run in front of a small room. Nerves, handled.</p>
</div>
<div style="border-top:2px solid #F577A1;padding-top:18px;display:flex;flex-direction:column;gap:10px">
<div style="width:34px;height:34px;border-radius:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);color:#fff;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center">04</div>
<div style="font-family:'Playfair Display',serif;font-weight:600;font-size:21px;color:#F4F0FF">Headliner <span style="color:#F577A1">Â· day 45</span></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">You walk on a real OTS stage and perform. Solo.</p>
</div>
</div>
</div>
<div id="pace" data-screen-label="Pick your pace" style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<div style="font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1">Pick your pace</div>
<div style="display:flex;align-items:flex-end;justify-content:space-between;gap:20px;flex-wrap:wrap">
<h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(30px,3.6vw,44px);line-height:1.12;color:#F4F0FF">Your stage. <em style="font-style:italic">Your pace.</em></h2>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0;max-width:40ch">Same finish line â€” a real stage. Pick the pace your week allows.</p>
</div>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(260px,100%),1fr));gap:16px;margin-top:8px;align-items:stretch">
<div style="border-radius:3px;padding:1px;background:linear-gradient(135deg,#F0771E,#F577A1,#9E76CC)">
<div style="background:#17142B;border-radius:2px;padding:clamp(20px,2.5vw,28px);display:flex;flex-direction:column;gap:10px;height:100%;box-sizing:border-box">
<div style="display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap"><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(26px,2.6vw,32px);color:#F4F0FF">45 days</div><div style="font-size:10px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#fff;background:linear-gradient(90deg,#F0771E,#F577A1);padding:4px 10px;border-radius:999px">Intensive</div></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">Most reps, fastest ramp. For when you've got the time and want it now.</p>
</div>
</div>
<div style="border:1px solid rgba(244,240,255,.14);background:rgba(244,240,255,.03);border-radius:3px;padding:clamp(20px,2.5vw,28px);display:flex;flex-direction:column;gap:10px;box-sizing:border-box">
<div style="display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap"><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(26px,2.6vw,32px);color:#F4F0FF">60 days</div><div style="font-size:10px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1;border:1px solid rgba(245,119,161,.5);padding:4px 10px;border-radius:999px">Standard</div></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">A steadier climb with more room to consolidate.</p>
</div>
<div style="border:1px solid rgba(244,240,255,.14);background:rgba(244,240,255,.03);border-radius:3px;padding:clamp(20px,2.5vw,28px);display:flex;flex-direction:column;gap:10px;box-sizing:border-box">
<div style="display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap"><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(26px,2.6vw,32px);color:#F4F0FF">90 days</div><div style="font-size:10px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1;border:1px solid rgba(245,119,161,.5);padding:4px 10px;border-radius:999px">Relaxed</div></div>
<p style="margin:0;font-size:14px;line-height:1.6;color:#B9B3D0">For busy weeks â€” the same journey, more breathing space.</p>
</div>
</div>
<p style="margin:0;font-size:13px;line-height:1.6;color:#7E78A0">Never played, coming back, or already strum a little? We place you right on the call.</p>
</div>
<div data-screen-label="The numbers" style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<div style="font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1">The numbers</div>
<h2 style="margin:0;max-width:26ch;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(28px,3.2vw,40px);line-height:1.16;color:#F4F0FF;text-wrap:pretty">A community that's been on the streets <em style="font-style:italic">since day one</em></h2>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(170px,100%),1fr));gap:clamp(16px,2.5vw,28px);margin-top:8px">
<div style="border-top:1px solid rgba(244,240,255,.16);padding-top:16px;display:flex;flex-direction:column;gap:6px"><div style="font-family:'Playfair Display',serif;font-weight:700;font-size:clamp(30px,3.2vw,40px);color:#F4F0FF">1,500+</div><div style="font-size:13px;color:#9C96BC">Street shows performed</div></div>
<div style="border-top:1px solid rgba(244,240,255,.16);padding-top:16px;display:flex;flex-direction:column;gap:6px"><div style="font-family:'Playfair Display',serif;font-weight:700;font-size:clamp(30px,3.2vw,40px);color:#F4F0FF">74,000</div><div style="font-size:13px;color:#9C96BC">Audience behind the stage</div></div>
<div style="border-top:1px solid rgba(244,240,255,.16);padding-top:16px;display:flex;flex-direction:column;gap:6px"><div style="font-family:'Playfair Display',serif;font-weight:700;font-size:clamp(30px,3.2vw,40px);color:#F4F0FF">1,000+</div><div style="font-size:13px;color:#9C96BC">Musicians in the network</div></div>
<div style="border-top:1px solid rgba(244,240,255,.16);padding-top:16px;display:flex;flex-direction:column;gap:6px"><div style="font-family:'Playfair Display',serif;font-weight:700;font-size:clamp(30px,3.2vw,40px);color:#F4F0FF">15</div><div style="font-size:13px;color:#9C96BC">Seats per cohort</div></div>
<div style="border-top:1px solid rgba(244,240,255,.16);padding-top:16px;display:flex;flex-direction:column;gap:6px"><div style="font-family:'Playfair Display',serif;font-weight:700;font-size:clamp(30px,3.2vw,40px);background:linear-gradient(90deg,#F0771E,#F577A1);-webkit-background-clip:text;background-clip:text;color:transparent">45</div><div style="font-size:13px;color:#9C96BC">Days, couch to stage</div></div>
</div>
</div>
<div data-screen-label="Our promises" style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<div style="font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1">Our promises</div>
<h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(30px,3.6vw,44px);line-height:1.12;color:#F4F0FF">Built on <em style="font-style:italic">straight talk</em></h2>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(240px,100%),1fr));gap:16px;margin-top:8px">
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;padding:22px;display:flex;flex-direction:column;gap:8px"><div style="font-size:15px;font-weight:700;color:#F4F0FF;line-height:1.35">No invented testimonials</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">Cohort 1 is the first. Its real footage and words come after the show.</p></div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;padding:22px;display:flex;flex-direction:column;gap:8px"><div style="font-size:15px;font-weight:700;color:#F4F0FF;line-height:1.35">No fake counters</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">The seat count is real and CRM-driven. It never fake-decrements.</p></div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;padding:22px;display:flex;flex-direction:column;gap:8px"><div style="font-size:15px;font-weight:700;color:#F4F0FF;line-height:1.35">A real date, a real stage</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">Your show is on the calendar from day one. That deadline is the method.</p></div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;padding:22px;display:flex;flex-direction:column;gap:8px"><div style="font-size:15px;font-weight:700;color:#F4F0FF;line-height:1.35">Numbers talked 1:1</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">Founding-cohort pricing, discussed on the call once we both know it's a fit.</p></div>
</div>
</div>
<div id="apply" data-screen-label="Apply" style="width:min(1140px,100% - 48px);margin:0 auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(min(320px,100%),1fr));gap:clamp(28px,4vw,64px);padding:clamp(56px,8vw,104px) 0 0;align-items:start">
<div style="display:flex;flex-direction:column;gap:18px">
<h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(32px,3.8vw,48px);line-height:1.1;color:#F4F0FF">Apply for <em style="font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent">your seat.</em></h2>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<p style="margin:0;max-width:44ch;font-size:15.5px;line-height:1.65;color:#C9C3DE;text-wrap:pretty">Two minutes. We call you back within the hour to see if it's a fit â€” a real commitment, not a sign-up.</p>
<a href="https://wa.me/919841610111?text=Hi%2C%20I%27m%20interested%20in%20joining%20the%20performer%20program." style="display:flex;align-items:center;justify-content:center;gap:8px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);color:#fff;font-size:14.5px;font-weight:700;padding:15px 22px;border-radius:3px;align-self:flex-start">Fastest â€” message us on WhatsApp â†’</a>
<p style="margin:0;max-width:44ch;font-size:13px;line-height:1.65;color:#7E78A0;text-wrap:pretty">We'll ring you shortly. Bring your questions â€” "am I too old", "I've failed before", all of it. That's what the call is for.</p>
<div style="display:flex;align-items:center;gap:10px"><span style="font-size:12px;font-weight:700;color:#F4F0FF;border:1px solid rgba(244,240,255,.35);padding:6px 12px;border-radius:999px">7 of 15 seats left</span><span style="font-size:12px;color:#7E78A0">Cohort 1 forming now</span></div>
</div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;padding:clamp(22px,3vw,32px);display:flex;flex-direction:column;gap:16px">
<div style="display:flex;align-items:center;gap:12px"><div style="height:1px;flex:1;background:rgba(244,240,255,.14)"></div><span style="font-size:11.5px;font-weight:500;color:#7E78A0">or fill the form</span><div style="height:1px;flex:1;background:rgba(244,240,255,.14)"></div></div>
<form id="application-form" onsubmit="event.preventDefault();this.style.display='none';document.getElementById('application-success').style.display='flex';" style="display:flex;flex-direction:column;gap:14px">
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-name" style="font-size:12.5px;font-weight:700;color:#C9C3DE">Name *</label><input id="r-name" name="name" type="text" required="required" placeholder="Your name" style="width:100%;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"></input></div>
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-phone" style="font-size:12.5px;font-weight:700;color:#C9C3DE">Phone / WhatsApp *</label><div style="display:flex;gap:8px"><span style="display:flex;align-items:center;padding:0 12px;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;font-size:14px;color:#B9B3D0">+91</span><input id="r-phone" name="phone" type="tel" required="required" placeholder="98400 00000" style="flex:1;min-width:0;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"></input></div></div>
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-email" style="font-size:12.5px;font-weight:700;color:#C9C3DE">Email (optional)</label><input id="r-email" name="email" type="email" placeholder="you@example.com" style="width:100%;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"></input></div>
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-played" style="font-size:12.5px;font-weight:700;color:#C9C3DE">Have you played guitar before? *</label><select id="r-played" name="played_before" required="required" value="" style="width:100%;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"><option value="" disabled="disabled">Choose oneâ€¦</option><option value="never">Never</option><option value="a-little">A little</option><option value="own-dust">I own one, gathers dust</option><option value="rusty">Yes, a bit rusty</option></select></div>
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-time" style="font-size:12.5px;font-weight:700;color:#C9C3DE">How much time can you give each week? *</label><select id="r-time" name="weekly_time" required="required" value="" style="width:100%;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"><option value="" disabled="disabled">Choose oneâ€¦</option><option value="45">Lots â€” intensive (45 days)</option><option value="60">Steady â€” standard (60 days)</option><option value="90">A little â€” relaxed (90 days)</option><option value="unsure">Not sure yet</option></select></div>
<div style="display:flex;flex-direction:column;gap:6px"><label for="r-pull" style="font-size:12.5px;font-weight:700;color:#C9C3DE">Which pulls you most? (optional)</label><select id="r-pull" name="pull" value="" style="width:100%;box-sizing:border-box;background:rgba(13,11,26,.7);border:1px solid rgba(244,240,255,.16);border-radius:3px;padding:13px 14px;font-size:15px;font-family:'DM Sans',sans-serif;color:#F4F0FF"><option value="" disabled="disabled">Choose oneâ€¦</option><option value="stage">Playing on a real stage</option><option value="learning">Finally learning properly</option><option value="community">Meeting other musicians</option></select></div>
<button type="submit" style="border:0;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);color:#fff;font-size:15px;font-weight:700;font-family:'DM Sans',sans-serif;padding:16px 22px;border-radius:3px">Send my application â†’</button>
</form>
<div id="application-success" style="border:1px solid rgba(245,119,161,.55);background:rgba(245,119,161,.08);border-radius:3px;padding:26px;display:none;flex-direction:column;gap:8px;text-align:center">
<div style="font-family:'Playfair Display',serif;font-style:italic;font-weight:600;font-size:26px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);-webkit-background-clip:text;background-clip:text;color:transparent">You're in.</div>
<p style="margin:0;font-size:14.5px;line-height:1.6;color:#C9C3DE">Keep your phone close â€” we call within the hour.</p>
</div>
</div>
</div>
<div id="faq" data-screen-label="FAQ" style="width:min(760px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(28px,3.2vw,38px);line-height:1.16;color:#F4F0FF;text-align:center">The questions <em style="font-style:italic">everyone</em> asks</h2>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC);margin:0 auto"></div>
<div style="display:flex;flex-direction:column;border-top:1px solid rgba(244,240,255,.12);margin-top:8px">
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>Am I too old / not talented?</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">No. Day one is built for people who&#x27;ve never held a guitar. The variable is showing up three times a week, not your age.</p></details>
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>I&#x27;ve tried and quit before.</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">You didn&#x27;t fail. You practised alone, with no stage and no deadline. That&#x27;s exactly what we fixed ? a day-by-day plan and a real show date.</p></details>
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>I have no time.</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">Three online sessions a week, from home. Pick 45, 60, or 90 days by the time you&#x27;ve got. No commute. If you can give that, we get you on stage.</p></details>
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>Do I perform with a band?</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">No ? this is you, solo. Your own 3?5 song set, your moment on the stage.</p></details>
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>Is it a class or 1:1?</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">Both ? 1:1 sessions with a coach built around your songs and pace, plus a weekly group class and an orientation. A small cohort (~15), never a crowded lecture hall.</p></details>
<details style="border-bottom:1px solid rgba(244,240,255,.12)"><summary style="cursor:pointer;display:flex;align-items:center;justify-content:space-between;gap:12px;padding:18px 2px;font-family:'DM Sans',sans-serif;font-size:15.5px;font-weight:700;color:#F4F0FF;list-style:none"><span>What does it cost?</span><span style="color:#F577A1;font-size:19px;line-height:1;flex:none">+</span></summary><p style="margin:0;padding:0 2px 18px;font-size:14.5px;line-height:1.65;color:#B9B3D0;text-wrap:pretty">Founding-cohort pricing. We talk numbers on the call, once we know it&#x27;s a fit.</p></details>
</div>
</div>
<div id="blog" data-screen-label="From the streets" style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:16px;padding:clamp(56px,8vw,104px) 0 0">
<div style="display:flex;align-items:flex-end;justify-content:space-between;gap:20px;flex-wrap:wrap">
<div style="display:flex;flex-direction:column;gap:12px"><div style="font-size:11px;font-weight:700;letter-spacing:.16em;text-transform:uppercase;color:#F577A1">From the streets</div><h2 style="margin:0;font-family:'Playfair Display',serif;font-weight:600;font-size:clamp(30px,3.6vw,44px);line-height:1.12;color:#F4F0FF">Read before <em style="font-style:italic">you leap.</em></h2></div>
<a href="#blog" style="font-size:13.5px;font-weight:700;color:#F577A1;white-space:nowrap">All stories â†’</a>
</div>
<div style="width:44px;height:3px;background:linear-gradient(90deg,#F0771E,#F577A1,#9E76CC)"></div>
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(280px,100%),1fr));gap:16px;margin-top:8px">
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;overflow:hidden;display:flex;flex-direction:column">
<div class="zoom-media" style="aspect-ratio:16/9;position:relative"><img src="./assets/ots-metro-performer.jpg" alt="OTS performer singing with guitar at Chennai Metro" loading="lazy" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;display:block;"></div>
<div style="padding:20px;display:flex;flex-direction:column;gap:7px"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1">The method</div><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:19px;line-height:1.3;color:#F4F0FF">Why an app can't get you on a stage</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">Practising alone with no deadline is the thing that fails â€” not you. Here's what changes with a show date.</p></div>
</div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;overflow:hidden;display:flex;flex-direction:column">
<div class="zoom-media" style="aspect-ratio:16/9;position:relative"><img src="./assets/ots-stage-lights.jpg" alt="OTS audience holding lights during a street show" loading="lazy" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;display:block;"></div>
<div style="padding:20px;display:flex;flex-direction:column;gap:7px"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1">Show night</div><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:19px;line-height:1.3;color:#F4F0FF">What actually happens at an OTS show</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">House lights, a real crowd, your name on the line-up. A walkthrough of the night you're training for.</p></div>
</div>
<div style="background:rgba(244,240,255,.05);border:1px solid rgba(244,240,255,.12);border-radius:3px;overflow:hidden;display:flex;flex-direction:column">
<div class="zoom-media" style="aspect-ratio:16/9;position:relative"><img src="./assets/ots-beach-crowd.jpg" alt="Beach crowd cheering at an OTS show" loading="lazy" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;display:block;"></div>
<div style="padding:20px;display:flex;flex-direction:column;gap:7px"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#F577A1">Couch-to-Stage</div><div style="font-family:'Playfair Display',serif;font-weight:600;font-size:19px;line-height:1.3;color:#F4F0FF">Days 1â€“12: hands hurt, then the riff lands</div><p style="margin:0;font-size:13.5px;line-height:1.6;color:#B9B3D0">The honest first fortnight â€” sore fingertips, the chord engine, and the first "I played that."</p></div>
</div>
</div>
</div>
<section data-screen-label="Final CTA" class="ots-parallax-band ots-final-cta" style="--band-image:url('./assets/ots-beach-crowd.jpg');--band-position:center 58%">
<div class="ots-band-inner center">
<h2 class="ots-band-title">The next show is happening. The only question is whether you're <em style="font-style:italic">in the crowd</em> or <em style="font-style:italic;background:linear-gradient(90deg,#F0771E,#F577A1);-webkit-background-clip:text;background-clip:text;color:transparent">on the stage.</em></h2>
<a href="https://wa.me/919841610111?text=Hi%2C%20I%27m%20interested%20in%20joining%20the%20performer%20program." class="ots-primary">WhatsApp us â€” get on stage â†’</a>
<div style="display:flex;align-items:center;gap:14px;flex-wrap:wrap;justify-content:center">
<span style="font-size:12px;font-weight:700;color:#F4F0FF;border:1px solid rgba(244,240,255,.35);padding:6px 12px;border-radius:999px;background:rgba(13,11,26,.45)">7 of 15 seats left</span>
<a href="#apply" class="ots-secondary">or use the application form</a>
</div>
</div>
</section>
<div data-screen-label="Footer" style="border-top:1px solid rgba(244,240,255,.12)">
<div style="width:min(1140px,100% - 48px);margin:0 auto;display:flex;flex-direction:column;gap:32px;padding:clamp(40px,5vw,64px) 0 28px">
<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(220px,100%),1fr));gap:clamp(24px,3vw,40px)">
<div style="display:flex;flex-direction:column;gap:10px;grid-column:span 1">
<div style="font-family:Raleway,sans-serif;font-weight:800;font-size:18px;color:#F4F0FF">On The Streets</div>
<p style="margin:0;max-width:30ch;font-size:13.5px;line-height:1.6;color:#B9B3D0">A Chennai music community putting first-timers on real stages. <em style="font-family:'Playfair Display',serif;font-style:italic;color:#F577A1">Spreading Smiles!</em></p>
</div>
<div style="display:flex;flex-direction:column;gap:10px;align-items:flex-start"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#7E78A0">Program</div><a href="#method" style="font-size:13px;color:#B9B3D0">The method</a><a href="#pace" style="font-size:13px;color:#B9B3D0">Pick your pace</a><a href="#apply" style="font-size:13px;color:#B9B3D0">Apply</a><a href="#faq" style="font-size:13px;color:#B9B3D0">FAQ</a></div>
<div style="display:flex;flex-direction:column;gap:10px;align-items:flex-start"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#7E78A0">Stories</div><a href="#stories" style="font-size:13px;color:#B9B3D0">Real people, real stage</a><a href="#blog" style="font-size:13px;color:#B9B3D0">From the streets</a></div>
<div style="display:flex;flex-direction:column;gap:10px;align-items:flex-start"><div style="font-size:10.5px;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:#7E78A0">Talk to us</div><a href="https://wa.me/919841610111?text=Hi%2C%20I%27m%20interested%20in%20joining%20the%20performer%20program." style="font-size:13px;color:#F577A1;font-weight:700">WhatsApp us â†’</a><a href="https://www.instagram.com/" style="font-size:13px;color:#B9B3D0">Instagram</a><a href="https://www.youtube.com/" style="font-size:13px;color:#B9B3D0">YouTube</a></div>
</div>
<div style="display:flex;align-items:center;justify-content:space-between;gap:10px;border-top:1px solid rgba(244,240,255,.12);padding-top:18px;flex-wrap:wrap">
<span style="font-size:12px;color:#7E78A0">Â© 2026 On The Streets Foundation, Chennai</span>
<span style="font-size:10.5px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:#7E78A0">Cohort 1 Â· Couch-to-Stage</span>
</div>
</div>
</div>
</div>
</body>
</html>

