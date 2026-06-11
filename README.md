<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NOCTARA — Where Darkness Meets Perfection</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&family=Tenor+Sans&family=EB+Garamond:ital,wght@0,400;0,500;1,400&family=Noto+Serif+Arabic:wght@300;400&display=swap" rel="stylesheet">
<style>
:root {
  --black: #070707;
  --deep: #0d0b0a;
  --charcoal: #181411;
  --charcoal2: #221e1a;
  --gold: #c8a24a;
  --gold-light: #dfc070;
  --gold-dim: #7a6130;
  --gold-glow: rgba(200,162,74,0.12);
  --cream: #ede4d3;
  --cream-dim: #a8967a;
  --white: #f8f3ea;
  --border: rgba(200,162,74,0.12);
  --border-strong: rgba(200,162,74,0.28);
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior: smooth; font-size: 16px; }

body {
  background: var(--black);
  color: var(--cream);
  font-family: 'EB Garamond', serif;
  overflow-x: hidden;
  cursor: none;
}

body.ar { direction: rtl; }
body.ar .nav-links { flex-direction: row-reverse; }
body.ar .hero-text { text-align: right; }
body.ar .section-label::after { margin-left: 0; margin-right: auto; }

/* ── CURSOR ── */
#cur { position:fixed; width:7px; height:7px; background:var(--gold); border-radius:50%; pointer-events:none; z-index:9999; transform:translate(-50%,-50%); transition:width .2s,height .2s; mix-blend-mode:screen; }
#cur-r { position:fixed; width:28px; height:28px; border:1px solid var(--gold-dim); border-radius:50%; pointer-events:none; z-index:9998; transform:translate(-50%,-50%); transition:transform .06s linear; }
body:has(a:hover) #cur, body:has(button:hover) #cur { width:14px; height:14px; }

/* ── NOISE ── */
body::after {
  content:''; position:fixed; inset:0; pointer-events:none; z-index:1000; opacity:.35;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23n)' opacity='.08'/%3E%3C/svg%3E");
}

/* ── SCROLLBAR ── */
::-webkit-scrollbar { width:3px; }
::-webkit-scrollbar-track { background:var(--black); }
::-webkit-scrollbar-thumb { background:var(--gold-dim); }

/* ══════════════════════════════════════
   NAV
══════════════════════════════════════ */
nav {
  position: fixed; top:0; left:0; right:0; z-index:500;
  padding: 24px 48px;
  display: flex; align-items:center; justify-content:space-between;
  transition: background .5s, padding .4s, backdrop-filter .5s;
}
nav.scrolled {
  background: rgba(7,7,7,0.92);
  backdrop-filter: blur(12px);
  padding: 16px 48px;
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family:'Cormorant Garamond',serif;
  font-size:22px; font-weight:300; letter-spacing:.4em;
  color:var(--white); text-decoration:none;
}
.nav-logo span { color:var(--gold); }
.nav-links { display:flex; align-items:center; gap:40px; list-style:none; }
.nav-links a {
  font-family:'Tenor Sans',sans-serif; font-size:10px;
  letter-spacing:.35em; text-transform:uppercase;
  color:var(--cream-dim); text-decoration:none;
  transition:color .3s;
}
.nav-links a:hover { color:var(--gold); }
.nav-right { display:flex; align-items:center; gap:20px; }
.lang-btn {
  font-family:'Tenor Sans',sans-serif; font-size:9px;
  letter-spacing:.3em; text-transform:uppercase;
  color:var(--gold-dim); background:none; border:1px solid var(--border);
  padding:6px 14px; cursor:pointer; transition:all .3s;
}
.lang-btn:hover { border-color:var(--gold); color:var(--gold); }
.nav-cta {
  font-family:'Tenor Sans',sans-serif; font-size:9px;
  letter-spacing:.3em; text-transform:uppercase;
  color:var(--black); background:var(--gold);
  border:none; padding:9px 22px; cursor:pointer;
  transition: background .3s;
}
.nav-cta:hover { background:var(--gold-light); }
.hamburger { display:none; flex-direction:column; gap:5px; cursor:pointer; }
.hamburger span { width:22px; height:1px; background:var(--cream-dim); transition:.3s; }

/* ══════════════════════════════════════
   HERO
══════════════════════════════════════ */
.hero {
  min-height: 100vh; position:relative;
  display:flex; flex-direction:column;
  align-items:center; justify-content:center;
  overflow:hidden; padding:120px 48px 80px;
}
.hero-bg {
  position:absolute; inset:0;
  background:
    radial-gradient(ellipse 55% 60% at 50% 55%, rgba(200,162,74,.07) 0%, transparent 65%),
    radial-gradient(ellipse 30% 40% at 15% 80%, rgba(200,162,74,.04) 0%, transparent 60%),
    var(--black);
}
.hero-ring {
  position:absolute; border-radius:50%;
  border:1px solid var(--border); pointer-events:none;
}
.hero-ring-1 { width:500px; height:500px; top:50%; left:50%; transform:translate(-50%,-50%); animation:ringPulse 8s ease-in-out infinite; }
.hero-ring-2 { width:750px; height:750px; top:50%; left:50%; transform:translate(-50%,-50%); animation:ringPulse 8s ease-in-out infinite .8s; opacity:.5; }
.hero-ring-3 { width:1000px; height:1000px; top:50%; left:50%; transform:translate(-50%,-50%); animation:ringPulse 8s ease-in-out infinite 1.6s; opacity:.25; }
@keyframes ringPulse {
  0%,100% { opacity:.15; transform:translate(-50%,-50%) scale(1); }
  50% { opacity:.35; transform:translate(-50%,-50%) scale(1.02); }
}
.hero-line { position:absolute; top:0; left:0; right:0; height:1px; background:linear-gradient(90deg,transparent,var(--gold-dim),transparent); animation:lineGlow 4s ease-in-out infinite alternate; }
@keyframes lineGlow { from{opacity:.2} to{opacity:.7} }

.hero-content { position:relative; z-index:2; text-align:center; }
.hero-eyebrow {
  font-family:'Tenor Sans',sans-serif; font-size:9px;
  letter-spacing:.6em; color:var(--gold); text-transform:uppercase;
  margin-bottom:40px; opacity:0;
  animation: fadeUp .8s ease .3s forwards;
}
.hero-name {
  font-family:'Cormorant Garamond',serif; font-weight:300;
  font-size:clamp(72px,13vw,148px); letter-spacing:.12em;
  line-height:.9; color:var(--white);
  opacity:0; animation:fadeUp 1s ease .5s forwards;
}
.hero-name-gold { color:var(--gold); }
.hero-divider {
  display:flex; align-items:center; justify-content:center; gap:20px;
  margin:32px auto;
  opacity:0; animation:fadeUp .8s ease .7s forwards;
}
.hero-divider-line { height:1px; width:64px; background:linear-gradient(90deg,transparent,var(--gold-dim)); }
.hero-divider-line:last-child { background:linear-gradient(90deg,var(--gold-dim),transparent); }
.hero-divider-gem { width:5px; height:5px; background:var(--gold); transform:rotate(45deg); }
.hero-tagline {
  font-family:'Cormorant Garamond',serif; font-style:italic;
  font-size:clamp(17px,2.5vw,24px); color:var(--cream-dim);
  letter-spacing:.04em; margin-bottom:56px;
  opacity:0; animation:fadeUp .8s ease .9s forwards;
}
.hero-actions {
  display:flex; gap:16px; justify-content:center; flex-wrap:wrap;
  opacity:0; animation:fadeUp .8s ease 1.1s forwards;
}
.btn-primary {
  font-family:'Tenor Sans',sans-serif; font-size:10px;
  letter-spacing:.35em; text-transform:uppercase;
  color:var(--black); background:var(--gold);
  border:none; padding:16px 40px; cursor:pointer;
  transition:background .3s,transform .2s;
}
.btn-primary:hover { background:var(--gold-light); transform:translateY(-1px); }
.btn-secondary {
  font-family:'Tenor Sans',sans-serif; font-size:10px;
  letter-spacing:.35em; text-transform:uppercase;
  color:var(--cream-dim); background:transparent;
  border:1px solid var(--border-strong); padding:16px 40px;
  cursor:pointer; transition:all .3s;
}
.btn-secondary:hover { border-color:var(--gold); color:var(--gold); }
.hero-scroll {
  position:absolute; bottom:36px; left:50%; transform:translateX(-50%);
  display:flex; flex-direction:column; align-items:center; gap:8px;
  font-family:'Tenor Sans',sans-serif; font-size:8px;
  letter-spacing:.4em; color:var(--gold-dim); text-transform:uppercase;
  animation:fadeUp .8s ease 1.5s forwards; opacity:0;
}
.hero-scroll-line { width:1px; height:40px; background:linear-gradient(var(--gold-dim),transparent); animation:scrollLine 2s ease-in-out infinite; }
@keyframes scrollLine { 0%,100%{opacity:.3;transform:scaleY(.6)} 50%{opacity:1;transform:scaleY(1)} }

@keyframes fadeUp { from{opacity:0;transform:translateY(28px)} to{opacity:1;transform:translateY(0)} }

/* ══════════════════════════════════════
   MARQUEE
══════════════════════════════════════ */
.marquee-wrap { overflow:hidden; border-top:1px solid var(--border); border-bottom:1px solid var(--border); background:var(--charcoal); padding:18px 0; }
.marquee-track { display:flex; gap:0; white-space:nowrap; animation:marquee 22s linear infinite; }
.marquee-item {
  font-family:'Cormorant Garamond',serif; font-style:italic;
  font-size:15px; color:var(--gold-dim); padding:0 48px;
  flex-shrink:0;
}
.marquee-dot { color:var(--gold); margin:0 8px; font-style:normal; }
@keyframes marquee { from{transform:translateX(0)} to{transform:translateX(-50%)} }

/* ══════════════════════════════════════
   SECTIONS SHARED
══════════════════════════════════════ */
.section { padding:100px 48px; max-width:1200px; margin:0 auto; }
.section-label {
  font-family:'Tenor Sans',sans-serif; font-size:9px;
  letter-spacing:.55em; color:var(--gold); text-transform:uppercase;
  margin-bottom:48px; display:flex; align-items:center; gap:16px;
}
.section-label::after { content:''; flex:1; height:1px; background:linear-gradient(90deg,var(--gold-dim),transparent); max-width:160px; }
.section-title {
  font-family:'Cormorant Garamond',serif; font-weight:300;
  font-size:clamp(38px,5.5vw,64px); line-height:1.05; color:var(--white);
}
.section-title em { font-style:italic; color:var(--gold); }
.reveal { opacity:0; transform:translateY(30px); transition:opacity .9s ease,transform .9s ease; }
.reveal.on { opacity:1; transform:none; }

/* ══════════════════════════════════════
   STORY SECTION
══════════════════════════════════════ */
.story-inner { display:grid; grid-template-columns:1fr 1fr; gap:80px; align-items:center; margin-top:64px; }
.story-text { font-size:17px; line-height:1.95; color:var(--cream-dim); }
.story-text strong { color:var(--cream); font-weight:500; }
.story-visual {
  position:relative; aspect-ratio:3/4;
  border:1px solid var(--border);
  display:flex; align-items:center; justify-content:center;
  overflow:hidden;
}
.story-visual-bg {
  position:absolute; inset:0;
  background:radial-gradient(ellipse at center, rgba(200,162,74,.08) 0%, var(--charcoal) 70%);
}
.story-visual-name {
  font-family:'Cormorant Garamond',serif; font-size:clamp(40px,6vw,80px);
  font-weight:300; letter-spacing:.3em; color:rgba(200,162,74,.15);
  position:relative; z-index:1; writing-mode:vertical-rl; text-orientation:mixed;
}
.story-visual-corner { position:absolute; width:20px; height:20px; }
.story-visual-corner.tl { top:16px; left:16px; border-top:1px solid var(--gold-dim); border-left:1px solid var(--gold-dim); }
.story-visual-corner.tr { top:16px; right:16px; border-top:1px solid var(--gold-dim); border-right:1px solid var(--gold-dim); }
.story-visual-corner.bl { bottom:16px; left:16px; border-bottom:1px solid var(--gold-dim); border-left:1px solid var(--gold-dim); }
.story-visual-corner.br { bottom:16px; right:16px; border-bottom:1px solid var(--gold-dim); border-right:1px solid var(--gold-dim); }
.story-quote {
  font-family:'Cormorant Garamond',serif; font-style:italic;
  font-size:clamp(20px,2.8vw,28px); color:var(--gold-light);
  border-left:2px solid var(--gold); padding:20px 32px;
  margin:40px 0; line-height:1.5; font-weight:300;
}
body.ar .story-quote { border-left:none; border-right:2px solid var(--gold); padding:20px 32px 20px 0; }

/* ══════════════════════════════════════
   PRODUCTS
══════════════════════════════════════ */
.products-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:2px; margin-top:64px; background:var(--border); }
.product-card {
  background:var(--deep); position:relative; overflow:hidden;
  cursor:pointer; transition:background .4s;
  display:flex; flex-direction:column;
}
.product-card:hover { background:var(--charcoal); }
.product-card::before {
  content:''; position:absolute; top:0; left:0; width:100%; height:2px;
  background:linear-gradient(90deg,var(--gold),transparent);
  transform:scaleX(0); transform-origin:left; transition:transform .5s;
}
.product-card:hover::before { transform:scaleX(1); }
.product-visual {
  aspect-ratio:1; display:flex; align-items:center; justify-content:center;
  position:relative; overflow:hidden;
  background:radial-gradient(ellipse at center, rgba(200,162,74,.06) 0%, var(--black) 70%);
  border-bottom:1px solid var(--border);
}
.product-icon { font-size:60px; opacity:.7; transition:transform .4s, opacity .4s; }
.product-card:hover .product-icon { transform:scale(1.08); opacity:.9; }
.product-badge {
  position:absolute; top:16px; right:16px;
  font-family:'Tenor Sans',sans-serif; font-size:8px;
  letter-spacing:.3em; text-transform:uppercase;
  color:var(--black); background:var(--gold); padding:5px 12px;
}
body.ar .product-badge { right:auto; left:16px; }
.product-info { padding:32px 28px 28px; flex:1; display:flex; flex-direction:column; }
.product-origin {
  font-family:'Tenor Sans',sans-serif; font-size:8px;
  letter-spacing:.4em; color:var(--gold-dim); text-transform:uppercase; margin-bottom:12px;
}
.product-name {
  font-family:'Cormorant Garamond',serif; font-size:clamp(22px,2.5vw,30px);
  font-weight:300; color:var(--white); line-height:1.1; margin-bottom:12px;
}
.product-desc { font-size:14px; line-height:1.7; color:var(--cream-dim); flex:1; margin-bottom:24px; }
.product-footer { display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:12px; }
.product-price {
  font-family:'Cormorant Garamond',serif; font-size:26px;
  font-weight:300; color:var(--gold);
}
.product-price span { font-size:13px; color:var(--gold-dim); margin-right:4px; font-family:'Tenor Sans',sans-serif; }
.product-btn {
  font-family:'Tenor Sans',sans-serif; font-size:9px;
  letter-spacing:.3em; text-transform:uppercase;
  color:var(--black); background:var(--gold);
  border:none; padding:10px 20px; cursor:pointer;
  transition:background .3s;
}
.product-btn:hover { background:var(--gold-light); }

/* ══════════════════════════════════════
   RITUAL / FEATURES
══════════════════════════════════════ */
.ritual-wrap { background:var(--charcoal); border-top:1px solid var(--border); border-bottom:1px solid var(--border); }
.ritual-grid { display:grid; grid-template-columns:repeat(4,1fr); gap:0; }
.ritual-item {
  padding:60px 40px; position:relative;
  border-right:1px solid var(--border);
  transition:background .3s;
}
.ritual-item:last-child { border-right:none; }
.ritual-item:hover { background:rgba(200,162,74,.03); }
.ritual-num {
  font-family:'Cormorant Garamond',serif; font-size:52px;
  font-weight:300; font-style:italic; color:rgba(200,162,74,.1);
  line-height:1; margin-bottom:20px;
}
.ritual-title {
  font-family:'Tenor Sans',sans-serif; font-size:10px;
  letter-spacing:.35em; color:var(--gold); text-transform:uppercase;
  margin-bottom:14px;
}
.ritual-text { font-size:15px; line-height:1.75; color:var(--cream-dim); }

/* ══════════════════════════════════════
   ABOUT
══════════════════════════════════════ */
.about-inner { display:grid; grid-template-columns:1.2fr 1fr; gap:80px; align-items:start; margin-top:64px; }
.about-stat-grid { display:grid; grid-template-columns:1fr 1fr; gap:2px; background:var(--border); margin-top:40px; }
.about-stat { background:var(--deep); padding:32px 28px; }
.about-stat-num {
  font-family:'Cormorant Garamond',serif; font-size:clamp(36px,4vw,52px);
  font-weight:300; color:var(--gold); line-height:1; margin-bottom:8px;
}
.about-stat-label { font-family:'Tenor Sans',sans-serif; font-size:9px; letter-spacing:.35em; color:var(--cream-dim); text-transform:uppercase; }
.about-manifesto {
  font-family:'Cormorant Garamond',serif; font-size:clamp(18px,2.5vw,26px);
  font-weight:300; font-style:italic; line-height:1.5; color:var(--cream-dim);
}
.about-manifesto strong { color:var(--white); font-style:normal; font-weight:300; }

/* ══════════════════════════════════════
   TESTIMONIALS
══════════════════════════════════════ */
.testi-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:2px; margin-top:64px; background:var(--border); }
.testi-card { background:var(--deep); padding:44px 36px; position:relative; overflow:hidden; }
.testi-card::before { content:'\201C'; font-family:'Cormorant Garamond',serif; font-size:120px; color:rgba(200,162,74,.06); position:absolute; top:-10px; left:20px; line-height:1; }
.testi-text { font-family:'Cormorant Garamond',serif; font-style:italic; font-size:clamp(16px,1.8vw,19px); line-height:1.7; color:var(--cream-dim); margin-bottom:28px; position:relative; z-index:1; }
.testi-stars { color:var(--gold); font-size:12px; letter-spacing:3px; margin-bottom:16px; }
.testi-author { font-family:'Tenor Sans',sans-serif; font-size:9px; letter-spacing:.3em; color:var(--gold-dim); text-transform:uppercase; }

/* ══════════════════════════════════════
   ORDER / WHATSAPP CTA
══════════════════════════════════════ */
.order-section {
  background:var(--charcoal); border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);
  text-align:center; padding:100px 48px;
  position:relative; overflow:hidden;
}
.order-bg {
  position:absolute; inset:0;
  background:radial-gradient(ellipse 60% 80% at 50% 50%, rgba(200,162,74,.06) 0%, transparent 70%);
}
.order-inner { position:relative; z-index:1; max-width:700px; margin:0 auto; }
.order-section .section-label { justify-content:center; }
.order-section .section-label::after { display:none; }
.order-title {
  font-family:'Cormorant Garamond',serif; font-weight:300;
  font-size:clamp(36px,5vw,60px); line-height:1.1; color:var(--white); margin-bottom:20px;
}
.order-title em { color:var(--gold); font-style:italic; }
.order-sub { font-size:17px; line-height:1.8; color:var(--cream-dim); margin-bottom:48px; }
.wa-btn {
  display:inline-flex; align-items:center; gap:14px;
  background:var(--gold); color:var(--black);
  font-family:'Tenor Sans',sans-serif; font-size:11px;
  letter-spacing:.35em; text-transform:uppercase;
  border:none; padding:18px 48px; cursor:pointer;
  transition:all .3s; text-decoration:none;
  font-weight:normal;
}
.wa-btn:hover { background:var(--gold-light); transform:translateY(-2px); box-shadow:0 8px 32px rgba(200,162,74,.2); }
.wa-icon { font-size:18px; }
.order-note { font-family:'Tenor Sans',sans-serif; font-size:9px; letter-spacing:.3em; color:var(--gold-dim); text-transform:uppercase; margin-top:28px; }

/* ══════════════════════════════════════
   FOOTER
══════════════════════════════════════ */
footer {
  background:var(--black); border-top:1px solid var(--border);
  padding:80px 48px 40px;
}
.footer-top { display:grid; grid-template-columns:1.5fr 1fr 1fr 1fr; gap:60px; margin-bottom:64px; }
.footer-brand-name {
  font-family:'Cormorant Garamond',serif; font-size:32px;
  font-weight:300; letter-spacing:.4em; color:var(--white); margin-bottom:16px;
}
.footer-brand-tag { font-family:'Cormorant Garamond',serif; font-style:italic; font-size:15px; color:var(--gold-dim); margin-bottom:28px; }
.footer-brand-text { font-size:14px; line-height:1.8; color:var(--cream-dim); }
.footer-col-title { font-family:'Tenor Sans',sans-serif; font-size:9px; letter-spacing:.4em; color:var(--gold); text-transform:uppercase; margin-bottom:24px; }
.footer-links { list-style:none; display:flex; flex-direction:column; gap:12px; }
.footer-links a { font-size:15px; color:var(--cream-dim); text-decoration:none; transition:color .3s; }
.footer-links a:hover { color:var(--gold); }
.footer-social { display:flex; gap:16px; margin-top:8px; }
.footer-social-link {
  width:36px; height:36px; border:1px solid var(--border);
  display:flex; align-items:center; justify-content:center;
  color:var(--cream-dim); text-decoration:none; font-size:14px;
  transition:all .3s;
}
.footer-social-link:hover { border-color:var(--gold); color:var(--gold); }
.footer-bottom { border-top:1px solid var(--border); padding-top:32px; display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:16px; }
.footer-copy { font-family:'Tenor Sans',sans-serif; font-size:9px; letter-spacing:.3em; color:var(--gold-dim); text-transform:uppercase; }

/* ══════════════════════════════════════
   MOBILE NAV MENU
══════════════════════════════════════ */
.mobile-menu {
  position:fixed; inset:0; background:rgba(7,7,7,.97);
  backdrop-filter:blur(16px); z-index:490;
  display:flex; flex-direction:column; align-items:center; justify-content:center; gap:40px;
  opacity:0; pointer-events:none; transition:opacity .4s;
}
.mobile-menu.open { opacity:1; pointer-events:all; }
.mobile-menu a {
  font-family:'Cormorant Garamond',serif; font-size:36px; font-weight:300;
  color:var(--cream-dim); text-decoration:none; letter-spacing:.1em;
  transition:color .3s;
}
.mobile-menu a:hover { color:var(--gold); }

/* ══════════════════════════════════════
   TOAST
══════════════════════════════════════ */
.toast {
  position:fixed; bottom:32px; right:32px; z-index:800;
  background:var(--charcoal); border:1px solid var(--border-strong);
  padding:16px 24px; font-family:'Tenor Sans',sans-serif;
  font-size:10px; letter-spacing:.3em; color:var(--gold); text-transform:uppercase;
  opacity:0; transform:translateY(16px); transition:all .4s;
  pointer-events:none;
}
.toast.show { opacity:1; transform:none; }
body.ar .toast { right:auto; left:32px; }

/* ══════════════════════════════════════
   RESPONSIVE
══════════════════════════════════════ */
@media(max-width:900px) {
  nav { padding:20px 24px; }
  nav.scrolled { padding:14px 24px; }
  .nav-links { display:none; }
  .hamburger { display:flex; }
  .products-grid { grid-template-columns:1fr; }
  .ritual-grid { grid-template-columns:1fr 1fr; }
  .story-inner, .about-inner { grid-template-columns:1fr; gap:40px; }
  .testi-grid { grid-template-columns:1fr; }
  .footer-top { grid-template-columns:1fr 1fr; gap:40px; }
  .section { padding:70px 24px; }
  .order-section { padding:70px 24px; }
}
@media(max-width:500px) {
  .ritual-grid { grid-template-columns:1fr; }
  .ritual-item { border-right:none; border-bottom:1px solid var(--border); }
  .footer-top { grid-template-columns:1fr; }
  .about-stat-grid { grid-template-columns:1fr; }
  .hero-actions { flex-direction:column; align-items:center; }
}

/* separator */
.sep { height:1px; background:linear-gradient(90deg,transparent,var(--border-strong),transparent); margin:0; }
</style>
</head>
<body>

<!-- CURSOR -->
<div id="cur"></div>
<div id="cur-r"></div>

<!-- MOBILE MENU -->
<div class="mobile-menu" id="mobileMenu">
  <a href="#story" onclick="closeMobile()" data-en="Our Story" data-ar="قصتنا">Our Story</a>
  <a href="#products" onclick="closeMobile()" data-en="Shop" data-ar="المنتجات">Shop</a>
  <a href="#about" onclick="closeMobile()" data-en="About" data-ar="من نحن">About</a>
  <a href="#order" onclick="closeMobile()" data-en="Order Now" data-ar="اطلب الآن">Order Now</a>
</div>

<!-- NAV -->
<nav id="navbar">
  <a class="nav-logo" href="#"><span>N</span>OCTARA</a>
  <ul class="nav-links">
    <li><a href="#story" data-en="Story" data-ar="القصة">Story</a></li>
    <li><a href="#products" data-en="Shop" data-ar="المنتجات">Shop</a></li>
    <li><a href="#ritual" data-en="Ritual" data-ar="الطقوس">Ritual</a></li>
    <li><a href="#about" data-en="About" data-ar="عنا">About</a></li>
    <li><a href="#order" data-en="Order" data-ar="اطلب">Order</a></li>
  </ul>
  <div class="nav-right">
    <button class="lang-btn" id="langBtn" onclick="toggleLang()">عربي</button>
    <button class="nav-cta" onclick="scrollToOrder()" data-en="Order Now" data-ar="اطلب الآن">Order Now</button>
    <div class="hamburger" id="hamburger" onclick="toggleMobile()">
      <span></span><span></span><span></span>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-line"></div>
  <div class="hero-ring hero-ring-1"></div>
  <div class="hero-ring hero-ring-2"></div>
  <div class="hero-ring hero-ring-3"></div>
  <div class="hero-content">
    <p class="hero-eyebrow" data-en="Premium Coffee · Cairo, Egypt" data-ar="قهوة فاخرة · القاهرة، مصر">Premium Coffee · Cairo, Egypt</p>
    <h1 class="hero-name">NOC<span class="hero-name-gold">T</span>ARA</h1>
    <div class="hero-divider">
      <div class="hero-divider-line"></div>
      <div class="hero-divider-gem"></div>
      <div class="hero-divider-line"></div>
    </div>
    <p class="hero-tagline" data-en="Where darkness meets perfection" data-ar="حيث يلتقي الظلام بالكمال">Where darkness meets perfection</p>
    <div class="hero-actions">
      <button class="btn-primary" onclick="scrollToOrder()" data-en="Order Now" data-ar="اطلب الآن">Order Now</button>
      <button class="btn-secondary" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})" data-en="Explore Collection" data-ar="استكشف المجموعة">Explore Collection</button>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="hero-scroll-line"></div>
    <span data-en="Scroll" data-ar="اسحب">Scroll</span>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track" id="marqueeTrack">
    <span class="marquee-item">Dark Roast <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Single Origin <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Where Darkness Meets Perfection <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Crafted With Obsession <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Premium Coffee <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">قهوة فاخرة <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Cairo, Egypt <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Dark Roast <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Single Origin <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Where Darkness Meets Perfection <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Crafted With Obsession <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Premium Coffee <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">قهوة فاخرة <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Cairo, Egypt <span class="marquee-dot">✦</span></span>
  </div>
</div>

<!-- STORY -->
<div id="story">
<div class="section reveal">
  <p class="section-label" data-en="Our Story" data-ar="قصتنا">Our Story</p>
  <h2 class="section-title" data-en="Born in <em>darkness</em>,<br>perfected in silence" data-ar="وُلد في <em>الظلام</em>،<br>وصُقل في الصمت">Born in <em>darkness</em>,<br>perfected in silence</h2>
  <div class="story-inner">
    <div>
      <p class="story-text" data-en="<strong>NOCTARA</strong> was born from a single conviction — that the finest coffee lives in the dark. In the depth of the roast, in the quiet moments before the world wakes, in the space between one sip and the next.<br><br>The name carries the Latin root <em>Nocte</em> — night — fused with the ancient idea of a guiding star that appears only when darkness is deep enough to see it. NOCTARA is that star.<br><br>We source, select, and roast every batch with an obsession that borders on the sacred. No shortcuts. No compromise. Only the pursuit of depth — in every cup we deliver to your door." data-ar="وُلدت <strong>NOCTARA</strong> من قناعة واحدة — أن أجود القهوة تعيش في الظلام. في أعماق التحميص، في اللحظات الهادئة قبل أن يصحو العالم، في المسافة بين رشفة وأخرى.<br><br>يحمل الاسم الجذر اللاتيني <em>Nocte</em> — الليل — مدموجاً بفكرة النجم المرشد القديم الذي يظهر فقط حين يعمق الظلام بما يكفي لرؤيته. NOCTARA هو ذلك النجم.<br><br>نختار ونحمص كل دفعة بهوس يكاد يكون مقدساً. لا اختصارات. لا تنازلات. فقط السعي نحو العمق — في كل كوب نوصله إلى بابك."><strong>NOCTARA</strong> was born from a single conviction — that the finest coffee lives in the dark. In the depth of the roast, in the quiet moments before the world wakes, in the space between one sip and the next.<br><br>The name carries the Latin root <em>Nocte</em> — night — fused with the ancient idea of a guiding star that appears only when darkness is deep enough to see it. NOCTARA is that star.<br><br>We source, select, and roast every batch with an obsession that borders on the sacred. No shortcuts. No compromise. Only the pursuit of depth — in every cup we deliver to your door.</p>
      <div class="story-quote" data-en='"Not everyone can handle the dark.<br>But those who can — taste everything."' data-ar='"ليس الجميع يتحمل الظلام.<br>لكن من يتحمله — يتذوق كل شيء."'>"Not everyone can handle the dark.<br>But those who can — taste everything."</div>
    </div>
    <div class="story-visual">
      <div class="story-visual-bg"></div>
      <div class="story-visual-name">NOCTARA</div>
      <div class="story-visual-corner tl"></div>
      <div class="story-visual-corner tr"></div>
      <div class="story-visual-corner bl"></div>
      <div class="story-visual-corner br"></div>
    </div>
  </div>
</div>
</div>

<div class="sep"></div>

<!-- PRODUCTS -->
<div id="products">
<div class="section reveal">
  <p class="section-label" data-en="The Collection" data-ar="المجموعة">The Collection</p>
  <h2 class="section-title" data-en="Crafted for <em>those<br>who seek depth</em>" data-ar="صُنعت <em>لمن يبحث<br>عن العمق</em>">Crafted for <em>those<br>who seek depth</em></h2>
  <div class="products-grid">

    <!-- Product 1 -->
    <div class="product-card">
      <div class="product-visual">
        <div style="font-size:72px;opacity:.65;">☕</div>
        <div class="product-badge" data-en="Bestseller" data-ar="الأكثر مبيعاً">Bestseller</div>
      </div>
      <div class="product-info">
        <p class="product-origin" data-en="Ethiopia · Single Origin" data-ar="إثيوبيا · أصل واحد">Ethiopia · Single Origin</p>
        <h3 class="product-name" data-en="Noctara Dark" data-ar="نوكتارا داكن">Noctara Dark</h3>
        <p class="product-desc" data-en="Our signature dark roast. Bold, complex, with deep chocolate and smoky undertones. The cup that started it all." data-ar="تحميصنا الداكن المميز. جريء، معقد، مع نكهات الشوكولاتة العميقة والدخانية. الكوب الذي بدأ كل شيء.">Our signature dark roast. Bold, complex, with deep chocolate and smoky undertones. The cup that started it all.</p>
        <div class="product-footer">
          <div class="product-price"><span data-en="EGP" data-ar="ج.م">EGP</span> 280</div>
          <button class="product-btn" onclick="orderProduct('Noctara Dark — 250g')" data-en="Order via WhatsApp" data-ar="اطلب واتساب">Order via WhatsApp</button>
        </div>
      </div>
    </div>

    <!-- Product 2 -->
    <div class="product-card">
      <div class="product-visual">
        <div style="font-size:72px;opacity:.65;">🌙</div>
      </div>
      <div class="product-info">
        <p class="product-origin" data-en="Colombia · Medium Roast" data-ar="كولومبيا · تحميص متوسط">Colombia · Medium Roast</p>
        <h3 class="product-name" data-en="Noctara Velvet" data-ar="نوكتارا مخمل">Noctara Velvet</h3>
        <p class="product-desc" data-en="Silky smooth with caramel and hazelnut notes. The perfect balance between darkness and elegance. For those who want depth without bitterness." data-ar="ناعم كالحرير مع نكهات الكراميل والبندق. التوازن المثالي بين الظلام والأناقة. لمن يريد العمق بلا مرارة.">Silky smooth with caramel and hazelnut notes. The perfect balance between darkness and elegance. For those who want depth without bitterness.</p>
        <div class="product-footer">
          <div class="product-price"><span data-en="EGP" data-ar="ج.م">EGP</span> 310</div>
          <button class="product-btn" onclick="orderProduct('Noctara Velvet — 250g')" data-en="Order via WhatsApp" data-ar="اطلب واتساب">Order via WhatsApp</button>
        </div>
      </div>
    </div>

    <!-- Product 3 -->
    <div class="product-card">
      <div class="product-visual">
        <div style="font-size:72px;opacity:.65;">⭐</div>
        <div class="product-badge" data-en="Limited" data-ar="محدود">Limited</div>
      </div>
      <div class="product-info">
        <p class="product-origin" data-en="Yemen · Rare Reserve" data-ar="اليمن · احتياطي نادر">Yemen · Rare Reserve</p>
        <h3 class="product-name" data-en="Noctara Noir" data-ar="نوكتارا نوار">Noctara Noir</h3>
        <p class="product-desc" data-en="Our rarest offering. Yemeni beans with centuries of heritage, delivering wine-like complexity and floral darkness unlike anything else." data-ar="عرضنا الأندر. حبوب يمنية بتراث يمتد لقرون، تمنح تعقيداً يشبه النبيذ وظلاماً زهرياً لا مثيل له.">Our rarest offering. Yemeni beans with centuries of heritage, delivering wine-like complexity and floral darkness unlike anything else.</p>
        <div class="product-footer">
          <div class="product-price"><span data-en="EGP" data-ar="ج.م">EGP</span> 450</div>
          <button class="product-btn" onclick="orderProduct('Noctara Noir — 250g')" data-en="Order via WhatsApp" data-ar="اطلب واتساب">Order via WhatsApp</button>
        </div>
      </div>
    </div>

  </div>
</div>
</div>

<div class="sep"></div>

<!-- RITUAL -->
<div id="ritual">
<div class="ritual-wrap reveal">
  <div class="section" style="padding-top:0;padding-bottom:0;max-width:100%;">
    <div style="padding:80px 48px 0; max-width:1200px; margin:0 auto;">
      <p class="section-label" data-en="The Ritual" data-ar="الطقوس">The Ritual</p>
      <h2 class="section-title" style="margin-bottom:56px;" data-en="Why <em>NOCTARA</em>" data-ar="لماذا <em>NOCTARA</em>">Why <em>NOCTARA</em></h2>
    </div>
    <div class="ritual-grid">
      <div class="ritual-item">
        <div class="ritual-num">01</div>
        <p class="ritual-title" data-en="Selected Beans" data-ar="حبوب مختارة">Selected Beans</p>
        <p class="ritual-text" data-en="Every bean is hand-selected from the world's finest origins. We reject what doesn't meet our standard — and our standard is uncompromising." data-ar="كل حبة مختارة يدوياً من أجود مصادر العالم. نرفض ما لا يرقى إلى معيارنا — ومعيارنا لا تنازل فيه.">Every bean is hand-selected from the world's finest origins. We reject what doesn't meet our standard — and our standard is uncompromising.</p>
      </div>
      <div class="ritual-item">
        <div class="ritual-num">02</div>
        <p class="ritual-title" data-en="Precision Roast" data-ar="تحميص دقيق">Precision Roast</p>
        <p class="ritual-text" data-en="Each roast profile is calibrated to the degree. We don't guess. We don't rush. We roast until the darkness is exactly right." data-ar="كل ملف تحميص مُعاير بدقة. لا نخمن. لا نتسرع. نحمص حتى يكون الظلام صحيحاً تماماً.">Each roast profile is calibrated to the degree. We don't guess. We don't rush. We roast until the darkness is exactly right.</p>
      </div>
      <div class="ritual-item">
        <div class="ritual-num">03</div>
        <p class="ritual-title" data-en="Fast Delivery" data-ar="توصيل سريع">Fast Delivery</p>
        <p class="ritual-text" data-en="Order via WhatsApp, receive at your door. Nationwide delivery across Egypt within 48 hours. Fresh, sealed, and ready to brew." data-ar="اطلب عبر واتساب، استلم على بابك. توصيل على مستوى مصر خلال 48 ساعة. طازج، مغلق، وجاهز للتحضير.">Order via WhatsApp, receive at your door. Nationwide delivery across Egypt within 48 hours. Fresh, sealed, and ready to brew.</p>
      </div>
      <div class="ritual-item" style="border-right:none;">
        <div class="ritual-num">04</div>
        <p class="ritual-title" data-en="Luxury Packaging" data-ar="تغليف فاخر">Luxury Packaging</p>
        <p class="ritual-text" data-en="Matte black with gold detailing. Every NOCTARA package is an object worth keeping. Because how coffee arrives matters as much as how it tastes." data-ar="أسود مطفي مع تفاصيل ذهبية. كل عبوة NOCTARA شيء يستحق الاحتفاظ به. لأن كيفية وصول القهوة تهم بقدر ما تهم طعمها.">Matte black with gold detailing. Every NOCTARA package is an object worth keeping. Because how coffee arrives matters as much as how it tastes.</p>
      </div>
    </div>
  </div>
</div>
</div>

<div class="sep"></div>

<!-- ABOUT -->
<div id="about">
<div class="section reveal">
  <p class="section-label" data-en="About NOCTARA" data-ar="عن NOCTARA">About NOCTARA</p>
  <h2 class="section-title" data-en="A brand built on<br><em>obsession</em>" data-ar="براند بُني على<br><em>الهوس</em>">A brand built on<br><em>obsession</em></h2>
  <div class="about-inner">
    <div>
      <p class="about-manifesto" data-en='NOCTARA is not just coffee.<br><br>It is a <strong>commitment to depth</strong> in a world that has grown comfortable with the surface. We exist for those who taste the difference. For the professional whose morning ritual is sacred. For the night owl who measures time in cups. For <strong>everyone who refuses to settle</strong> for ordinary.' data-ar='NOCTARA ليست مجرد قهوة.<br><br>إنها <strong>التزام بالعمق</strong> في عالم اعتاد السطحية. نوجد لمن يتذوق الفرق. للمحترف الذي طقوس صباحه مقدسة. لصاحي الليل الذي يقيس الوقت بالأكواب. <strong>لكل من يرفض الاستسلام</strong> للعادي.'>NOCTARA is not just coffee.<br><br>It is a <strong>commitment to depth</strong> in a world that has grown comfortable with the surface. We exist for those who taste the difference. For the professional whose morning ritual is sacred. For the night owl who measures time in cups. For <strong>everyone who refuses to settle</strong> for ordinary.</p>
      <div class="about-stat-grid">
        <div class="about-stat">
          <div class="about-stat-num">3</div>
          <div class="about-stat-label" data-en="Unique Blends" data-ar="مزيجات فريدة">Unique Blends</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">48h</div>
          <div class="about-stat-label" data-en="Max Delivery" data-ar="أقصى توصيل">Max Delivery</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">100%</div>
          <div class="about-stat-label" data-en="Arabica Beans" data-ar="حبوب عربيكا">Arabica Beans</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">EG</div>
          <div class="about-stat-label" data-en="Nationwide Shipping" data-ar="شحن على مستوى مصر">Nationwide Shipping</div>
        </div>
      </div>
    </div>
    <div>
      <p class="story-text" data-en="We are an Egyptian brand with a global soul. Based in Cairo, we believe the world deserves access to extraordinary coffee — not as a luxury for the few, but as a right for anyone willing to taste.<br><br>NOCTARA ships across all of Egypt. Every order arrives fresh, roasted to order, sealed in our signature black packaging.<br><br>We are small. We are intentional. And we are just getting started." data-ar="نحن براند مصري بروح عالمية. مقرنا القاهرة، ونؤمن أن العالم يستحق الوصول إلى قهوة استثنائية — ليس كرفاهية للقلة، بل كحق لكل من يريد أن يتذوق.<br><br>NOCTARA تشحن عبر مصر كلها. كل طلب يصل طازجاً، محمصاً عند الطلب، مغلقاً في عبواتنا السوداء المميزة.<br><br>نحن صغار. نحن متعمدون. ونحن نبدأ للتو.">We are an Egyptian brand with a global soul. Based in Cairo, we believe the world deserves access to extraordinary coffee — not as a luxury for the few, but as a right for anyone willing to taste.<br><br>NOCTARA ships across all of Egypt. Every order arrives fresh, roasted to order, sealed in our signature black packaging.<br><br>We are small. We are intentional. And we are just getting started.</p>
    </div>
  </div>
</div>
</div>

<div class="sep"></div>

<!-- TESTIMONIALS -->
<div class="section reveal">
  <p class="section-label" data-en="What They Say" data-ar="ما يقولونه">What They Say</p>
  <h2 class="section-title" data-en="Voices of <em>the dark</em>" data-ar="أصوات <em>الظلام</em>">Voices of <em>the dark</em></h2>
  <div class="testi-grid">
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text" data-en='"I have tried every specialty coffee brand in Cairo. NOCTARA is the first that genuinely made me pause and just... taste."' data-ar='"جربت كل براندات القهوة المتخصصة في القاهرة. NOCTARA هي الأولى التي جعلتني فعلاً أتوقف وأتذوق."'>
        "I have tried every specialty coffee brand in Cairo. NOCTARA is the first that genuinely made me pause and just... taste."
      </p>
      <p class="testi-author" data-en="Karim A. · Cairo" data-ar="كريم أ. · القاهرة">Karim A. · Cairo</p>
    </div>
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text" data-en='"The packaging alone is worth it. But then you open it and the aroma hits you — that is when you understand what NOCTARA means."' data-ar='"التغليف وحده يستحق. لكن حين تفتحه وتضربك الرائحة — هنا تفهم ما تعنيه NOCTARA."'>
        "The packaging alone is worth it. But then you open it and the aroma hits you — that is when you understand what NOCTARA means."
      </p>
      <p class="testi-author" data-en="Nour M. · Alexandria" data-ar="نور م. · الإسكندرية">Nour M. · Alexandria</p>
    </div>
    <div class="testi-card">
      <div class="testi-stars">★★★★★</div>
      <p class="testi-text" data-en='"Ordered at night, arrived next day. Fresh, perfectly roasted, and the Noctara Noir? I did not know Egyptian coffee could feel this global."' data-ar='"طلبت ليلاً، وصل في اليوم التالي. طازج، محمص بشكل مثالي، ونوكتارا نوار؟ لم أعلم أن القهوة المصرية يمكن أن تشعر بهذا العالمية."'>
        "Ordered at night, arrived next day. Fresh, perfectly roasted, and the Noctara Noir? I did not know Egyptian coffee could feel this global."
      </p>
      <p class="testi-author" data-en="Omar S. · New Cairo" data-ar="عمر س. · القاهرة الجديدة">Omar S. · New Cairo</p>
    </div>
  </div>
</div>

<div class="sep"></div>

<!-- ORDER CTA -->
<div id="order">
<div class="order-section reveal">
  <div class="order-bg"></div>
  <div class="order-inner">
    <p class="section-label" style="justify-content:center;" data-en="Order Now" data-ar="اطلب الآن">Order Now</p>
    <h2 class="order-title" data-en="Ready to taste <em>the darkness?</em>" data-ar="مستعد لتذوق <em>الظلام؟</em>">Ready to taste <em>the darkness?</em></h2>
    <p class="order-sub" data-en="Order directly via WhatsApp. Tell us your choice, your address, and we handle the rest. Delivered fresh to your door anywhere in Egypt." data-ar="اطلب مباشرة عبر واتساب. أخبرنا باختيارك وعنوانك، ونحن نتولى الباقي. يُسلم طازجاً لبابك في أي مكان في مصر.">Order directly via WhatsApp. Tell us your choice, your address, and we handle the rest. Delivered fresh to your door anywhere in Egypt.</p>
    <a class="wa-btn" id="mainWaBtn" href="https://wa.me/201000000000?text=Hello%20NOCTARA%2C%20I%20would%20like%20to%20place%20an%20order." target="_blank">
      <span class="wa-icon">💬</span>
      <span data-en="Order on WhatsApp" data-ar="اطلب على واتساب">Order on WhatsApp</span>
    </a>
    <p class="order-note" data-en="Fast Response · Nationwide Delivery · Fresh Roasted" data-ar="رد سريع · توصيل لكل مصر · محمص طازج">Fast Response · Nationwide Delivery · Fresh Roasted</p>
  </div>
</div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div>
      <div class="footer-brand-name">NOCTARA</div>
      <div class="footer-brand-tag" data-en="Where darkness meets perfection" data-ar="حيث يلتقي الظلام بالكمال">Where darkness meets perfection</div>
      <p class="footer-brand-text" data-en="A premium Egyptian coffee brand. Sourced globally, roasted locally, delivered to your door." data-ar="براند قهوة مصري فاخر. مصادر عالمية، تحميص محلي، توصيل لبابك.">A premium Egyptian coffee brand. Sourced globally, roasted locally, delivered to your door.</p>
      <div class="footer-social" style="margin-top:24px;">
        <a class="footer-social-link" href="#" title="Instagram">ig</a>
        <a class="footer-social-link" href="#" title="TikTok">tt</a>
        <a class="footer-social-link" href="https://wa.me/201000000000" target="_blank" title="WhatsApp">wa</a>
      </div>
    </div>
    <div>
      <p class="footer-col-title" data-en="Collection" data-ar="المجموعة">Collection</p>
      <ul class="footer-links">
        <li><a href="#products" data-en="Noctara Dark" data-ar="نوكتارا داكن">Noctara Dark</a></li>
        <li><a href="#products" data-en="Noctara Velvet" data-ar="نوكتارا مخمل">Noctara Velvet</a></li>
        <li><a href="#products" data-en="Noctara Noir" data-ar="نوكتارا نوار">Noctara Noir</a></li>
      </ul>
    </div>
    <div>
      <p class="footer-col-title" data-en="Company" data-ar="الشركة">Company</p>
      <ul class="footer-links">
        <li><a href="#story" data-en="Our Story" data-ar="قصتنا">Our Story</a></li>
        <li><a href="#about" data-en="About Us" data-ar="من نحن">About Us</a></li>
        <li><a href="#ritual" data-en="Our Ritual" data-ar="طقوسنا">Our Ritual</a></li>
      </ul>
    </div>
    <div>
      <p class="footer-col-title" data-en="Order" data-ar="الطلب">Order</p>
      <ul class="footer-links">
        <li><a href="https://wa.me/201000000000" target="_blank" data-en="WhatsApp" data-ar="واتساب">WhatsApp</a></li>
        <li><a href="#" data-en="Instagram DM" data-ar="إنستغرام">Instagram DM</a></li>
        <li><a href="#" data-en="Delivery Info" data-ar="معلومات التوصيل">Delivery Info</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p class="footer-copy" data-en="© 2025 NOCTARA · Cairo, Egypt · All Rights Reserved" data-ar="© 2025 NOCTARA · القاهرة، مصر · جميع الحقوق محفوظة">© 2025 NOCTARA · Cairo, Egypt · All Rights Reserved</p>
    <p class="footer-copy" data-en="Where Darkness Meets Perfection" data-ar="حيث يلتقي الظلام بالكمال">Where Darkness Meets Perfection</p>
  </div>
</footer>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
// ── CURSOR
const cur = document.getElementById('cur');
const curR = document.getElementById('cur-r');
let mx=0,my=0,rx=window.innerWidth/2,ry=window.innerHeight/2;
document.addEventListener('mousemove',e=>{
  mx=e.clientX; my=e.clientY;
  cur.style.left=mx+'px'; cur.style.top=my+'px';
});
(function loop(){
  rx+=(mx-rx)*.1; ry+=(my-ry)*.1;
  curR.style.left=rx+'px'; curR.style.top=ry+'px';
  requestAnimationFrame(loop);
})();

// ── NAV SCROLL
window.addEventListener('scroll',()=>{
  document.getElementById('navbar').classList.toggle('scrolled',window.scrollY>60);
});

// ── MOBILE MENU
let menuOpen=false;
function toggleMobile(){
  menuOpen=!menuOpen;
  document.getElementById('mobileMenu').classList.toggle('open',menuOpen);
}
function closeMobile(){ menuOpen=false; document.getElementById('mobileMenu').classList.remove('open'); }

// ── LANGUAGE
let lang='en';
const translations={};
document.querySelectorAll('[data-en]').forEach(el=>{
  translations[el]={en:el.getAttribute('data-en'),ar:el.getAttribute('data-ar')};
});

function toggleLang(){
  lang=lang==='en'?'ar':'en';
  document.getElementById('langBtn').textContent=lang==='en'?'عربي':'EN';
  document.documentElement.setAttribute('lang',lang);
  document.body.classList.toggle('ar',lang==='ar');
  document.querySelectorAll('[data-en]').forEach(el=>{
    const ar=el.getAttribute('data-ar');
    const en=el.getAttribute('data-en');
    const txt=lang==='ar'?ar:en;
    if(!txt) return;
    if(el.tagName==='INPUT'||el.tagName==='BUTTON'||el.tagName==='A'){
      el.textContent=txt;
    } else {
      el.innerHTML=txt;
    }
  });
  // update wa btn
  const waText=lang==='ar'?'اطلب على واتساب':'Order on WhatsApp';
  const waSpan=document.querySelector('#mainWaBtn span:last-child');
  if(waSpan) waSpan.textContent=waText;
}

// ── SCROLL TO ORDER
function scrollToOrder(){
  document.getElementById('order').scrollIntoView({behavior:'smooth'});
}

// ── PRODUCT ORDER
function orderProduct(name){
  const msg=encodeURIComponent(`Hello NOCTARA! I would like to order: ${name}\n\nPlease share details for delivery.`);
  window.open(`https://wa.me/201000000000?text=${msg}`,'_blank');
  showToast(lang==='ar'?'جاري فتح واتساب...':'Opening WhatsApp...');
}

// ── TOAST
function showToast(msg){
  const t=document.getElementById('toast');
  t.textContent=msg; t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'),3000);
}

// ── REVEAL ON SCROLL
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('on'); obs.unobserve(e.target); } });
},{threshold:.08});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

// ── MARQUEE CLONE
const track=document.getElementById('marqueeTrack');
track.innerHTML+=track.innerHTML;
</script>
</body>
</html>
