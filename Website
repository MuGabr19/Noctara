<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>NOCTARA - Coffee Excellence</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300&family=Tenor+Sans&family=EB+Garamond:ital@0;1&display=swap" rel="stylesheet">
  <style>
    :root{
      --black:#0a0908;
      --white:#f8f7f3;
      --cream:#e8e6e1;
      --cream-dim:#c9c5bd;
      --charcoal:#2a2926;
      --charcoal2:#3a3935;
      --deep:#1a1916;
      --gold:#d4af37;
      --gold-light:#e5c158;
      --gold-dim:#9d8b4a;
      --border:rgba(212,175,55,.1);
      --border-strong:rgba(212,175,55,.25);
    }

    *{margin:0;padding:0;box-sizing:border-box;}
    html{scroll-behavior:smooth;}
    body{background:var(--black);color:var(--white);font-family:'EB Garamond',serif;font-size:16px;line-height:1.6;overflow-x:hidden;}
    
    body.ar{direction:rtl;text-align:right;}
    body.en{direction:ltr;text-align:left;}

    /* NAV */
    nav{
      position:fixed;
      top:0;
      left:0;
      right:0;
      height:88px;
      background:rgba(10,9,8,.6);
      backdrop-filter:blur(16px);
      z-index:500;
      padding:24px 48px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      border-bottom:1px solid var(--border);
      transition:all .3s;
    }
    nav.scrolled{
      height:72px;
      padding:12px 48px;
      background:rgba(10,9,8,.8);
    }

    .nav-logo-wrap{display:flex;align-items:center;gap:12px;text-decoration:none;z-index:2;}
    .nav-logo{width:40px;height:40px;object-fit:contain;filter:drop-shadow(0 0 8px rgba(212,175,55,0.1));}
    .nav-brand{font-family:'Cormorant Garamond',serif;font-size:22px;letter-spacing:.15em;color:var(--white);}

    .nav-links{display:flex;gap:40px;}
    .nav-links a{font-family:'Tenor Sans',sans-serif;font-size:10px;letter-spacing:.35em;text-transform:uppercase;color:var(--cream-dim);text-decoration:none;transition:color .3s;}
    .nav-links a:hover{color:var(--gold);}

    .nav-right{display:flex;align-items:center;gap:20px;}
    .lang-btn{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--gold-dim);background:none;border:1px solid var(--border);padding:6px 14px;cursor:pointer;transition:all .3s;}
    .lang-btn:hover{border-color:var(--gold);color:var(--gold);}
    .lang-btn.active{color:var(--gold);border-color:var(--gold);}

    .cart-icon{position:relative;cursor:pointer;font-size:18px;color:var(--cream-dim);transition:color .3s;}
    .cart-icon:hover{color:var(--gold);}
    .cart-count{position:absolute;top:-8px;right:-8px;background:var(--gold);color:var(--black);width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:bold;font-family:'Tenor Sans',sans-serif;}

    .nav-cta{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--black);background:var(--gold);border:none;padding:9px 22px;cursor:pointer;transition:background .3s;}
    .nav-cta:hover{background:var(--gold-light);}

    .hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;}
    .hamburger span{width:22px;height:1px;background:var(--cream-dim);transition:.3s;}

    /* HERO */
    .hero{min-height:100vh;position:relative;display:flex;flex-direction:column;align-items:center;justify-content:center;overflow:hidden;padding:120px 48px 80px;margin-top:88px;}
    .hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse 55% 60% at 50% 55%,rgba(212,175,55,.06) 0%,transparent 65%),var(--black);}
    .hero-ring{position:absolute;border-radius:50%;border:1px solid var(--border);pointer-events:none;}
    .hero-ring-1{width:500px;height:500px;top:50%;left:50%;transform:translate(-50%,-50%);animation:ringPulse 8s ease-in-out infinite;}
    .hero-ring-2{width:760px;height:760px;top:50%;left:50%;transform:translate(-50%,-50%);animation:ringPulse 8s ease-in-out infinite .8s;opacity:.5;}
    .hero-ring-3{width:1020px;height:1020px;top:50%;left:50%;transform:translate(-50%,-50%);animation:ringPulse 8s ease-in-out infinite 1.6s;opacity:.2;}
    @keyframes ringPulse{0%,100%{opacity:.12;transform:translate(-50%,-50%) scale(1);}50%{opacity:.3;transform:translate(-50%,-50%) scale(1.02);}}
    .hero-line{position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--gold-dim),transparent);animation:lineGlow 4s ease-in-out infinite alternate;}
    @keyframes lineGlow{from{opacity:.2}to{opacity:.7}}

    .hero-content{position:relative;z-index:2;text-align:center;}
    .hero-logo-wrap{margin-bottom:8px;opacity:0;animation:fadeUp 1s ease .2s forwards;}
    .hero-logo-main{width:200px;height:200px;object-fit:contain;filter:drop-shadow(0 0 30px rgba(212,175,55,0.2));mix-blend-mode:screen;background:radial-gradient(circle, rgba(212,175,55,0.1), transparent);}
    .hero-eyebrow{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.6em;color:var(--gold);text-transform:uppercase;margin-bottom:16px;opacity:0;animation:fadeUp .8s ease .4s forwards;}
    .hero-name{font-family:'Cormorant Garamond',serif;font-weight:300;font-size:clamp(64px,11vw,130px);letter-spacing:.15em;line-height:.9;color:var(--white);opacity:0;animation:fadeUp 1s ease .55s forwards;}
    .hero-name-gold{color:var(--gold);}
    .hero-subtitle{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.5em;color:var(--gold-dim);text-transform:uppercase;margin-top:8px;opacity:0;animation:fadeUp .8s ease .7s forwards;}
    .hero-divider{display:flex;align-items:center;justify-content:center;gap:20px;margin:28px auto;opacity:0;animation:fadeUp .8s ease .85s forwards;}
    .hero-divider-line{height:1px;width:64px;background:linear-gradient(90deg,transparent,var(--gold-dim));}
    .hero-divider-line:last-child{background:linear-gradient(90deg,var(--gold-dim),transparent);}
    .hero-divider-gem{width:5px;height:5px;background:var(--gold);transform:rotate(45deg);}
    .hero-tagline{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:clamp(17px,2.5vw,23px);color:var(--cream-dim);letter-spacing:.04em;margin-bottom:52px;opacity:0;animation:fadeUp .8s ease 1s forwards;}
    .hero-actions{display:flex;gap:16px;justify-content:center;flex-wrap:wrap;opacity:0;animation:fadeUp .8s ease 1.15s forwards;}
    .btn-primary{font-family:'Tenor Sans',sans-serif;font-size:10px;letter-spacing:.35em;text-transform:uppercase;color:var(--black);background:var(--gold);border:none;padding:16px 40px;cursor:pointer;transition:background .3s,transform .2s;}
    .btn-primary:hover{background:var(--gold-light);transform:translateY(-1px);}
    .btn-secondary{font-family:'Tenor Sans',sans-serif;font-size:10px;letter-spacing:.35em;text-transform:uppercase;color:var(--cream-dim);background:transparent;border:1px solid var(--border-strong);padding:16px 40px;cursor:pointer;transition:all .3s;}
    .btn-secondary:hover{border-color:var(--gold);color:var(--gold);}

    /* MARQUEE */
    .marquee-wrap{overflow:hidden;border-top:1px solid var(--border);border-bottom:1px solid var(--border);background:var(--charcoal);padding:18px 0;}
    .marquee-track{display:flex;gap:0;white-space:nowrap;animation:marquee 24s linear infinite;}
    .marquee-item{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:15px;color:var(--gold-dim);padding:0 48px;flex-shrink:0;}
    .marquee-dot{color:var(--gold);margin:0 8px;font-style:normal;}
    @keyframes marquee{from{transform:translateX(0)}to{transform:translateX(-50%)}}

    /* SECTIONS */
    .section{padding:100px 48px;max-width:1200px;margin:0 auto;}
    .section-label{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.55em;color:var(--gold);text-transform:uppercase;margin-bottom:48px;display:flex;align-items:center;gap:16px;}
    .section-label::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,var(--gold-dim),transparent);max-width:160px;}
    .section-title{font-family:'Cormorant Garamond',serif;font-weight:300;font-size:clamp(38px,5.5vw,64px);line-height:1.05;color:var(--white);}
    .section-title em{font-style:italic;color:var(--gold);}

    /* STORY */
    .story-inner{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;margin-top:64px;}
    .story-text{font-size:17px;line-height:1.95;color:var(--cream-dim);}
    .story-text strong{color:var(--cream);font-weight:500;}
    .story-visual{position:relative;aspect-ratio:3/4;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;overflow:hidden;}
    .story-visual-bg{position:absolute;inset:0;background:radial-gradient(ellipse at center,rgba(212,175,55,.08) 0%,var(--charcoal) 70%);}
    .story-visual-logo{width:70%;height:70%;object-fit:contain;position:relative;z-index:1;filter:drop-shadow(0 0 20px rgba(212,175,55,0.2));opacity:0.7;}
    .story-visual-corner{position:absolute;width:20px;height:20px;}
    .story-visual-corner.tl{top:16px;left:16px;border-top:1px solid var(--gold-dim);border-left:1px solid var(--gold-dim);}
    .story-visual-corner.tr{top:16px;right:16px;border-top:1px solid var(--gold-dim);border-right:1px solid var(--gold-dim);}
    .story-visual-corner.bl{bottom:16px;left:16px;border-bottom:1px solid var(--gold-dim);border-left:1px solid var(--gold-dim);}
    .story-visual-corner.br{bottom:16px;right:16px;border-bottom:1px solid var(--gold-dim);border-right:1px solid var(--gold-dim);}
    .story-quote{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:clamp(18px,2.5vw,26px);color:var(--gold-light);border-left:2px solid var(--gold);padding:20px 32px;margin:40px 0;line-height:1.5;font-weight:300;}

    /* PRODUCTS */
    .products-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;margin-top:64px;background:var(--border);}
    .product-card{background:var(--deep);position:relative;overflow:hidden;cursor:pointer;transition:background .4s;display:flex;flex-direction:column;}
    .product-card:hover{background:var(--charcoal);}
    .product-card::before{content:'';position:absolute;top:0;left:0;width:100%;height:2px;background:linear-gradient(90deg,var(--gold),transparent);transform:scaleX(0);transform-origin:left;transition:transform .5s;}
    .product-card:hover::before{transform:scaleX(1);}
    .product-visual{aspect-ratio:1;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;border-bottom:1px solid var(--border);}
    .product-visual img{width:100%;height:100%;object-fit:cover;transition:transform .6s ease;filter:brightness(0.85);}
    .product-card:hover .product-visual img{transform:scale(1.04);filter:brightness(1);}
    .product-quote{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(transparent,rgba(10,9,8,0.9));padding:20px 16px 14px;opacity:0;transition:opacity .4s;}
    .product-card:hover .product-quote{opacity:1;}
    .product-quote-text{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:12px;color:var(--cream-dim);line-height:1.4;}
    .product-info{padding:28px 24px 24px;flex:1;display:flex;flex-direction:column;}
    .product-origin{font-family:'Tenor Sans',sans-serif;font-size:8px;letter-spacing:.4em;color:var(--gold-dim);text-transform:uppercase;margin-bottom:10px;}
    .product-name{font-family:'Cormorant Garamond',serif;font-size:clamp(20px,2.2vw,28px);font-weight:300;color:var(--white);line-height:1.1;margin-bottom:10px;}
    .product-desc{font-size:13px;line-height:1.7;color:var(--cream-dim);flex:1;margin-bottom:20px;}
    .product-footer{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:10px;}
    .product-price{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:300;color:var(--gold);}
    .product-price span{font-size:11px;color:var(--gold-dim);margin-right:3px;font-family:'Tenor Sans',sans-serif;}
    .product-btn{font-family:'Tenor Sans',sans-serif;font-size:8px;letter-spacing:.3em;text-transform:uppercase;color:var(--black);background:var(--gold);border:none;padding:9px 18px;cursor:pointer;transition:background .3s;}
    .product-btn:hover{background:var(--gold-light);}

    /* QUOTES */
    .quotes-strip{background:var(--charcoal);border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:64px 48px;}
    .quotes-strip-inner{max-width:1200px;margin:0 auto;}
    .novel-banner{display:flex;align-items:center;gap:24px;margin-bottom:48px;}
    .novel-banner-line{flex:1;height:1px;background:linear-gradient(90deg,var(--gold-dim),transparent);}
    .novel-banner-text{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.5em;color:var(--gold);text-transform:uppercase;white-space:nowrap;}
    .novel-banner-line:last-child{background:linear-gradient(90deg,transparent,var(--gold-dim));}
    .quotes-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;background:var(--border);}
    .quote-card{background:var(--deep);padding:40px 32px;position:relative;overflow:hidden;transition:background .3s;}
    .quote-card:hover{background:var(--charcoal2);}
    .quote-card::before{content:'\"';font-family:'Cormorant Garamond',serif;font-size:100px;color:rgba(212,175,55,.05);position:absolute;top:-10px;left:16px;line-height:1;}
    .quote-text{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:clamp(15px,1.6vw,18px);line-height:1.7;color:var(--cream-dim);margin-bottom:20px;position:relative;z-index:1;}
    .quote-source{font-family:'Tenor Sans',sans-serif;font-size:8px;letter-spacing:.35em;color:var(--gold-dim);text-transform:uppercase;}

    /* RITUAL */
    .ritual-wrap{background:var(--charcoal);border-top:1px solid var(--border);border-bottom:1px solid var(--border);}
    .ritual-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:0;}
    .ritual-item{padding:56px 36px;border-right:1px solid var(--border);transition:background .3s;}
    .ritual-item:last-child{border-right:none;}
    .ritual-item:hover{background:rgba(212,175,55,.03);}
    .ritual-num{font-family:'Cormorant Garamond',serif;font-size:52px;font-weight:300;font-style:italic;color:rgba(212,175,55,.08);line-height:1;margin-bottom:20px;}
    .ritual-title{font-family:'Tenor Sans',sans-serif;font-size:10px;letter-spacing:.35em;color:var(--gold);text-transform:uppercase;margin-bottom:14px;}
    .ritual-text{font-size:14px;line-height:1.75;color:var(--cream-dim);}

    /* ABOUT */
    .about-inner{display:grid;grid-template-columns:1.2fr 1fr;gap:80px;align-items:start;margin-top:64px;}
    .about-stat-grid{display:grid;grid-template-columns:1fr 1fr;gap:2px;background:var(--border);margin-top:40px;}
    .about-stat{background:var(--deep);padding:28px 24px;}
    .about-stat-num{font-family:'Cormorant Garamond',serif;font-size:clamp(32px,3.5vw,48px);font-weight:300;color:var(--gold);line-height:1;margin-bottom:8px;}
    .about-stat-label{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;color:var(--cream-dim);text-transform:uppercase;}

    /* TESTIMONIALS */
    .testi-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;margin-top:64px;background:var(--border);}
    .testi-card{background:var(--deep);padding:44px 36px;position:relative;overflow:hidden;}
    .testi-card::before{content:'\\201C';font-family:'Cormorant Garamond',serif;font-size:120px;color:rgba(212,175,55,.05);position:absolute;top:-10px;left:20px;line-height:1;}
    .testi-text{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:clamp(15px,1.7vw,18px);line-height:1.7;color:var(--cream-dim);margin-bottom:24px;position:relative;z-index:1;}
    .testi-stars{color:var(--gold);font-size:11px;letter-spacing:3px;margin-bottom:14px;}
    .testi-author{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;color:var(--gold-dim);text-transform:uppercase;}

    /* CART DRAWER */
    .cart-drawer{position:fixed;right:0;top:0;width:100%;max-width:420px;height:100vh;background:var(--deep);border-left:1px solid var(--border);transform:translateX(100%);transition:transform .4s ease;z-index:600;overflow-y:auto;display:flex;flex-direction:column;}
    .cart-drawer.open{transform:translateX(0);}
    body.ar .cart-drawer{right:auto;left:0;border-left:none;border-right:1px solid var(--border);transform:translateX(-100%);}
    body.ar .cart-drawer.open{transform:translateX(0);}

    .cart-header{padding:24px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center;position:sticky;top:0;background:var(--deep);}
    .cart-header-title{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:300;color:var(--white);}
    .cart-close{background:none;border:none;color:var(--cream-dim);font-size:24px;cursor:pointer;transition:color .3s;}
    .cart-close:hover{color:var(--gold);}

    .cart-items{flex:1;overflow-y:auto;padding:24px;}
    .cart-item{display:grid;grid-template-columns:60px 1fr 50px;gap:16px;margin-bottom:24px;padding-bottom:24px;border-bottom:1px solid var(--border);}
    .cart-item:last-child{border-bottom:none;}
    .cart-item-img{width:60px;height:60px;background:var(--charcoal);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--gold-dim);font-size:11px;text-align:center;}
    .cart-item-info{display:flex;flex-direction:column;justify-content:space-between;}
    .cart-item-name{font-family:'Cormorant Garamond',serif;font-size:14px;color:var(--white);margin-bottom:4px;}
    .cart-item-price{font-family:'Tenor Sans',sans-serif;font-size:11px;color:var(--gold);margin-bottom:8px;}
    .cart-item-qty{display:flex;align-items:center;gap:8px;font-size:12px;}
    .qty-btn{background:var(--charcoal);border:1px solid var(--border);color:var(--gold-dim);width:24px;height:24px;cursor:pointer;transition:all .2s;}
    .qty-btn:hover{background:var(--gold);color:var(--black);}
    .cart-item-remove{display:flex;align-items:center;justify-content:center;color:var(--gold-dim);cursor:pointer;font-size:18px;transition:color .3s;}
    .cart-item-remove:hover{color:var(--gold);}

    .cart-empty{padding:40px 24px;text-align:center;color:var(--cream-dim);}

    .cart-footer{padding:24px;border-top:1px solid var(--border);position:sticky;bottom:0;background:var(--deep);}
    .cart-total{display:flex;justify-content:space-between;margin-bottom:20px;font-family:'Cormorant Garamond',serif;font-size:18px;}
    .cart-total-label{color:var(--cream-dim);}
    .cart-total-price{color:var(--gold);}
    .cart-checkout-btn{width:100%;padding:14px;background:var(--gold);color:var(--black);border:none;font-family:'Tenor Sans',sans-serif;font-size:11px;letter-spacing:.3em;text-transform:uppercase;cursor:pointer;transition:background .3s;margin-bottom:10px;}
    .cart-checkout-btn:hover{background:var(--gold-light);}
    .cart-checkout-btn:disabled{opacity:.5;cursor:not-allowed;}
    .cart-continue-btn{width:100%;padding:14px;background:transparent;color:var(--cream-dim);border:1px solid var(--border);font-family:'Tenor Sans',sans-serif;font-size:11px;letter-spacing:.3em;text-transform:uppercase;cursor:pointer;transition:all .3s;}
    .cart-continue-btn:hover{border-color:var(--gold);color:var(--gold);}

    .cart-overlay{position:fixed;inset:0;background:rgba(0,0,0,.5);opacity:0;pointer-events:none;transition:opacity .4s;z-index:550;}
    .cart-overlay.open{opacity:1;pointer-events:all;}

    /* CHECKOUT */
    .checkout-modal{position:fixed;inset:0;background:rgba(0,0,0,.8);z-index:700;display:none;align-items:center;justify-content:center;padding:20px;overflow-y:auto;}
    .checkout-modal.open{display:flex;}
    .checkout-content{background:var(--deep);width:100%;max-width:600px;border:1px solid var(--border);border-radius:4px;position:relative;}

    .checkout-header{padding:28px 32px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center;}
    .checkout-title{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:300;color:var(--white);}
    .checkout-close{background:none;border:none;color:var(--cream-dim);font-size:28px;cursor:pointer;transition:color .3s;}
    .checkout-close:hover{color:var(--gold);}

    .checkout-body{padding:32px;}
    .form-section{margin-bottom:32px;}
    .form-section-title{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.4em;color:var(--gold);text-transform:uppercase;margin-bottom:16px;}
    .form-group{margin-bottom:16px;}
    .form-label{display:block;font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;color:var(--cream-dim);text-transform:uppercase;margin-bottom:8px;}
    .form-input,.form-select,.form-textarea{width:100%;padding:12px;background:var(--charcoal);border:1px solid var(--border);color:var(--cream-dim);font-family:inherit;font-size:14px;transition:all .3s;}
    .form-input:focus,.form-select:focus,.form-textarea:focus{outline:none;border-color:var(--gold);background:var(--charcoal2);}
    .form-input::placeholder{color:var(--gold-dim);}

    .form-row{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
    .form-textarea{resize:vertical;min-height:80px;}

    .payment-methods{display:grid;grid-template-columns:1fr;gap:12px;margin-bottom:20px;}
    .payment-method{padding:16px;border:1px solid var(--border);background:var(--charcoal);cursor:pointer;transition:all .3s;display:flex;align-items:center;gap:12px;}
    .payment-method:hover{border-color:var(--gold);background:var(--charcoal2);}
    .payment-method input[type="radio"]{cursor:pointer;}
    .payment-method.selected{border-color:var(--gold);background:rgba(212,175,55,.1);}
    .payment-label{font-family:'Tenor Sans',sans-serif;font-size:12px;letter-spacing:.2em;color:var(--white);cursor:pointer;flex:1;}

    .upload-area{border:2px dashed var(--border);padding:24px;text-align:center;cursor:pointer;transition:all .3s;border-radius:4px;position:relative;}
    .upload-area:hover{border-color:var(--gold);background:rgba(212,175,55,.05);}
    .upload-area.active{border-color:var(--gold);background:rgba(212,175,55,.1);}
    .upload-icon{font-size:32px;margin-bottom:8px;}
    .upload-text{font-family:'Tenor Sans',sans-serif;font-size:11px;color:var(--cream-dim);margin-bottom:4px;}
    .upload-hint{font-family:'Tenor Sans',sans-serif;font-size:9px;color:var(--gold-dim);}
    .upload-file-input{position:absolute;width:100%;height:100%;opacity:0;cursor:pointer;}
    .upload-preview{margin-top:16px;padding:12px;background:var(--charcoal);border:1px solid var(--border);border-radius:4px;display:flex;align-items:center;gap:12px;}
    .upload-preview-img{width:60px;height:60px;object-fit:cover;border-radius:2px;}
    .upload-preview-info{flex:1;text-align:left;}
    .upload-preview-name{font-family:'Tenor Sans',sans-serif;font-size:11px;color:var(--white);margin-bottom:4px;}
    .upload-preview-size{font-family:'Tenor Sans',sans-serif;font-size:9px;color:var(--gold-dim);}
    .upload-remove{background:none;border:none;color:var(--gold-dim);cursor:pointer;font-size:18px;transition:color .3s;}
    .upload-remove:hover{color:var(--gold);}

    .order-summary{background:var(--charcoal);padding:20px;border:1px solid var(--border);border-radius:4px;margin-top:24px;}
    .order-summary-title{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;color:var(--gold);text-transform:uppercase;margin-bottom:16px;}
    .summary-row{display:flex;justify-content:space-between;margin-bottom:8px;font-size:13px;}
    .summary-row-label{color:var(--cream-dim);}
    .summary-row-value{color:var(--white);}
    .summary-total{border-top:1px solid var(--border);padding-top:12px;margin-top:12px;display:flex;justify-content:space-between;font-family:'Cormorant Garamond',serif;font-size:20px;}
    .summary-total-label{color:var(--cream-dim);}
    .summary-total-price{color:var(--gold);}

    .checkout-actions{display:flex;gap:12px;margin-top:32px;}
    .checkout-cancel{flex:1;padding:14px;background:transparent;color:var(--cream-dim);border:1px solid var(--border);font-family:'Tenor Sans',sans-serif;font-size:11px;letter-spacing:.3em;text-transform:uppercase;cursor:pointer;transition:all .3s;}
    .checkout-cancel:hover{border-color:var(--gold);color:var(--gold);}
    .checkout-confirm{flex:1;padding:14px;background:var(--gold);color:var(--black);border:none;font-family:'Tenor Sans',sans-serif;font-size:11px;letter-spacing:.3em;text-transform:uppercase;cursor:pointer;transition:background .3s;}
    .checkout-confirm:hover{background:var(--gold-light);}
    .checkout-confirm:disabled{opacity:.5;cursor:not-allowed;}

    /* FOOTER */
    footer{background:var(--black);border-top:1px solid var(--border);padding:80px 48px 40px;}
    .footer-top{display:grid;grid-template-columns:1.5fr 1fr 1fr 1fr;gap:60px;margin-bottom:64px;}
    .footer-logo-wrap{display:flex;align-items:center;gap:12px;margin-bottom:16px;}
    .footer-logo-img{height:40px;width:auto;object-fit:contain;}
    .footer-brand-name{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:300;letter-spacing:.4em;color:var(--white);}
    .footer-brand-tag{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:14px;color:var(--gold-dim);margin-bottom:24px;}
    .footer-brand-text{font-size:14px;line-height:1.8;color:var(--cream-dim);}
    .footer-col-title{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.4em;color:var(--gold);text-transform:uppercase;margin-bottom:24px;}
    .footer-links{list-style:none;display:flex;flex-direction:column;gap:12px;}
    .footer-links a{font-size:14px;color:var(--cream-dim);text-decoration:none;transition:color .3s;}
    .footer-links a:hover{color:var(--gold);}
    .footer-social{display:flex;gap:12px;margin-top:20px;}
    .footer-social-link{width:36px;height:36px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--cream-dim);text-decoration:none;font-size:13px;font-family:'Tenor Sans',sans-serif;letter-spacing:.1em;transition:all .3s;}
    .footer-social-link:hover{border-color:var(--gold);color:var(--gold);}
    .footer-bottom{border-top:1px solid var(--border);padding-top:28px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;}
    .footer-copy{font-family:'Tenor Sans',sans-serif;font-size:9px;letter-spacing:.3em;color:var(--gold-dim);text-transform:uppercase;}

    /* TOAST */
    .toast{position:fixed;bottom:32px;right:32px;z-index:900;background:var(--charcoal);border:1px solid var(--border-strong);padding:16px 24px;font-family:'Tenor Sans',sans-serif;font-size:10px;letter-spacing:.3em;color:var(--gold);text-transform:uppercase;opacity:0;transform:translateY(16px);transition:all .4s;pointer-events:none;border-radius:4px;}
    .toast.show{opacity:1;transform:none;pointer-events:all;}
    body.ar .toast{right:auto;left:32px;}

    @media(max-width:900px){
      .nav-links{display:none;}
      .hamburger{display:flex;}
      .products-grid{grid-template-columns:1fr 1fr;}
      .quotes-grid{grid-template-columns:1fr;}
      .ritual-grid{grid-template-columns:1fr 1fr;}
      .story-inner,.about-inner{grid-template-columns:1fr;gap:40px;}
      .testi-grid{grid-template-columns:1fr;}
      .footer-top{grid-template-columns:1fr 1fr;gap:40px;}
      .section{padding:70px 24px;}
      .cart-drawer{max-width:100%;}
      .checkout-content{max-width:100%;}
    }
    @media(max-width:500px){
      .products-grid{grid-template-columns:1fr;}
      .ritual-grid{grid-template-columns:1fr;}
      .ritual-item{border-right:none;border-bottom:1px solid var(--border);}
      .footer-top{grid-template-columns:1fr;}
      .about-stat-grid{grid-template-columns:1fr;}
      .hero-actions{flex-direction:column;align-items:center;}
      .form-row{grid-template-columns:1fr;}
      .checkout-actions{flex-direction:column;}
    }
  </style>
</head>
<body class="ar">

<!-- CART OVERLAY -->
<div class="cart-overlay" id="cartOverlay"></div>

<!-- CART DRAWER -->
<div class="cart-drawer" id="cartDrawer">
  <div class="cart-header">
    <div class="cart-header-title" data-ar="السلة" data-en="Cart">السلة</div>
    <button class="cart-close" onclick="closeCart()">✕</button>
  </div>
  <div class="cart-items" id="cartItems">
    <div class="cart-empty" data-ar="السلة فارغة" data-en="Cart is empty">السلة فارغة</div>
  </div>
  <div class="cart-footer" id="cartFooter" style="display:none;">
    <div class="cart-total">
      <span class="cart-total-label" data-ar="الإجمالي:" data-en="Total:">الإجمالي:</span>
      <span class="cart-total-price" id="cartTotalPrice">0 ر.س</span>
    </div>
    <button class="cart-checkout-btn" onclick="openCheckout()" data-ar="المتابعة للدفع" data-en="Proceed to Checkout">المتابعة للدفع</button>
    <button class="cart-continue-btn" onclick="closeCart()" data-ar="المتابعة بالتسوق" data-en="Continue Shopping">المتابعة بالتسوق</button>
  </div>
</div>

<!-- CHECKOUT MODAL -->
<div class="checkout-modal" id="checkoutModal">
  <div class="checkout-content">
    <div class="checkout-header">
      <div class="checkout-title" data-ar="إكمال الطلب" data-en="Complete Order">إكمال الطلب</div>
      <button class="checkout-close" onclick="closeCheckout()">✕</button>
    </div>
    <div class="checkout-body">
      <!-- Customer Info -->
      <div class="form-section">
        <div class="form-section-title" data-ar="بيانات العميل" data-en="Customer Information">بيانات العميل</div>
        <div class="form-group">
          <label class="form-label" data-ar="الاسم بالكامل" data-en="Full Name">الاسم بالكامل</label>
          <input type="text" class="form-input" id="customerName" placeholder="أدخل اسمك الكامل" required>
        </div>
        <div class="form-row">
          <div class="form-group">
            <label class="form-label" data-ar="رقم الهاتف" data-en="Phone Number">رقم الهاتف</label>
            <input type="tel" class="form-input" id="customerPhone" placeholder="966501234567" required>
          </div>
          <div class="form-group">
            <label class="form-label" data-ar="البريد الإلكتروني" data-en="Email">البريد الإلكتروني</label>
            <input type="email" class="form-input" id="customerEmail" placeholder="example@email.com">
          </div>
        </div>
        <div class="form-group">
          <label class="form-label" data-ar="العنوان" data-en="Address">العنوان</label>
          <textarea class="form-textarea" id="customerAddress" placeholder="أدخل عنوان التوصيل بالتفصيل" required></textarea>
        </div>
        <div class="form-row">
          <div class="form-group">
            <label class="form-label" data-ar="المدينة" data-en="City">المدينة</label>
            <input type="text" class="form-input" id="customerCity" placeholder="مثل: الرياض" required>
          </div>
          <div class="form-group">
            <label class="form-label" data-ar="المنطقة (اختياري)" data-en="Region (Optional)">المنطقة (اختياري)</label>
            <input type="text" class="form-input" id="customerRegion" placeholder="مثل: الشرقية">
          </div>
        </div>
      </div>

      <!-- Payment Method -->
      <div class="form-section">
        <div class="form-section-title" data-ar="طريقة الدفع" data-en="Payment Method">طريقة الدفع</div>
        <div class="payment-methods">
          <label class="payment-method selected" onclick="selectPayment('instapay')">
            <input type="radio" name="payment" value="instapay" checked>
            <span class="payment-label" data-ar="انستا باي / محفظة رقمية" data-en="Instapay / Digital Wallet">انستا باي / محفظة رقمية</span>
          </label>
          <label class="payment-method" onclick="selectPayment('bank')">
            <input type="radio" name="payment" value="bank">
            <span class="payment-label" data-ar="تحويل بنكي" data-en="Bank Transfer">تحويل بنكي</span>
          </label>
        </div>
        <div class="form-group">
          <label class="form-label" data-ar="رقم المحفظة / الحساب" data-en="Wallet / Account Number">رقم المحفظة / الحساب</label>
          <input type="text" class="form-input" id="paymentAccount" value="01551290097" readonly style="color:var(--gold);">
        </div>
        <div class="form-group">
          <label class="form-label" data-ar="رفع صورة التحويل" data-en="Upload Transfer Receipt">رفع صورة التحويل <span style="color:var(--gold);">*</span></label>
          <div class="upload-area" id="uploadArea" ondrop="handleDrop(event)" ondragover="handleDragOver(event)" ondragleave="handleDragLeave(event)" onclick="document.getElementById('fileInput').click()">
            <input type="file" id="fileInput" class="upload-file-input" accept="image/*" onchange="handleFileSelect(event)">
            <div class="upload-icon">📸</div>
            <div class="upload-text" data-ar="اسحب الصورة هنا أو انقر للاختيار" data-en="Drag image here or click to select">اسحب الصورة هنا أو انقر للاختيار</div>
            <div class="upload-hint" data-ar="(JPG, PNG - أقل من 5MB)" data-en="(JPG, PNG - Max 5MB)">(JPG, PNG - أقل من 5MB)</div>
          </div>
          <div id="uploadPreview" style="display:none;"></div>
        </div>
      </div>

      <!-- Order Summary -->
      <div class="order-summary">
        <div class="order-summary-title" data-ar="ملخص الطلب" data-en="Order Summary">ملخص الطلب</div>
        <div id="checkoutSummary"></div>
      </div>

      <!-- Actions -->
      <div class="checkout-actions">
        <button class="checkout-cancel" onclick="closeCheckout()" data-ar="إلغاء" data-en="Cancel">إلغاء</button>
        <button class="checkout-confirm" id="confirmBtn" onclick="confirmOrder()" data-ar="تأكيد الطلب" data-en="Confirm Order">تأكيد الطلب</button>
      </div>
    </div>
  </div>
</div>

<!-- NAV -->
<nav id="nav">
  <a href="#" class="nav-logo-wrap">
    <svg class="nav-logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
      <circle cx="100" cy="100" r="95" fill="none" stroke="#d4af37" stroke-width="1" opacity="0.3"/>
      <circle cx="100" cy="100" r="85" fill="none" stroke="#d4af37" stroke-width="0.5" opacity="0.2"/>
      <text x="100" y="115" font-family="Cormorant Garamond" font-size="48" font-weight="300" text-anchor="middle" fill="#d4af37" letter-spacing="2">NOCTARA</text>
      <circle cx="100" cy="100" r="70" fill="none" stroke="#d4af37" stroke-width="0.5" opacity="0.15"/>
    </svg>
    <span class="nav-brand">NOCTARA</span>
  </a>
  <div class="nav-links">
    <a href="#story" data-ar="القصة" data-en="Story">القصة</a>
    <a href="#products" data-ar="المنتجات" data-en="Products">المنتجات</a>
    <a href="#about" data-ar="عننا" data-en="About">عننا</a>
    <a href="#testimonials" data-ar="التقييمات" data-en="Reviews">التقييمات</a>
  </div>
  <div class="nav-right">
    <button class="lang-btn active" onclick="setLang('ar')" data-ar="العربية" data-en="العربية">العربية</button>
    <button class="lang-btn" onclick="setLang('en')" data-ar="English" data-en="English">English</button>
    <div class="cart-icon" onclick="openCart()">
      🛍️
      <span class="cart-count" id="cartCount" style="display:none;">0</span>
    </div>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-ring hero-ring-1"></div>
  <div class="hero-ring hero-ring-2"></div>
  <div class="hero-ring hero-ring-3"></div>
  <div class="hero-line"></div>
  <div class="hero-content">
    <div class="hero-logo-wrap">
      <svg class="hero-logo-main" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <radialGradient id="logoGrad" cx="50%" cy="50%" r="50%">
            <stop offset="0%" style="stop-color:#d4af37;stop-opacity:0.3" />
            <stop offset="100%" style="stop-color:#d4af37;stop-opacity:0" />
          </radialGradient>
        </defs>
        <circle cx="100" cy="100" r="95" fill="none" stroke="#d4af37" stroke-width="2" opacity="0.4"/>
        <circle cx="100" cy="100" r="80" fill="url(#logoGrad)" opacity="0.6"/>
        <text x="100" y="120" font-family="Cormorant Garamond" font-size="72" font-weight="300" text-anchor="middle" fill="#d4af37" letter-spacing="3">NOCTARA</text>
        <text x="100" y="145" font-family="Tenor Sans" font-size="12" text-anchor="middle" fill="#d4af37" letter-spacing="1.5" opacity="0.7">COFFEE</text>
      </svg>
    </div>
    <div class="hero-eyebrow" data-ar="قهوة حرفية" data-en="Artisan Coffee">قهوة حرفية</div>
    <h1 class="hero-name">
      <span data-ar="نوكتارا" data-en="NOCTARA">نوكتارا</span> <span class="hero-name-gold" data-ar="الليل الأسود" data-en="The Black Night">الليل الأسود</span>
    </h1>
    <div class="hero-subtitle" data-ar="تجربة القهوة الفاخرة" data-en="Premium Coffee Experience">تجربة القهوة الفاخرة</div>
    <div class="hero-divider">
      <div class="hero-divider-line"></div>
      <div class="hero-divider-gem"></div>
      <div class="hero-divider-line"></div>
    </div>
    <p class="hero-tagline" data-ar="قهوة من أفضل مزارع العالم، محمصة بعناية، تقدمها بحب" data-en="Premium beans from the world's finest farms, carefully roasted, served with love">قهوة من أفضل مزارع العالم، محمصة بعناية، تقدمها بحب</p>
    <div class="hero-actions">
      <button class="btn-primary" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})" data-ar="استكشف المنتجات" data-en="Explore Products">استكشف المنتجات</button>
      <button class="btn-secondary" onclick="openCart()" data-ar="عرض السلة" data-en="View Cart">عرض السلة</button>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <div class="marquee-item" data-ar="أفضل القهوة" data-en="The Finest Coffee">أفضل القهوة</div>
    <span class="marquee-dot">•</span>
    <div class="marquee-item" data-ar="محمصة حرفية" data-en="Artisan Roasting">محمصة حرفية</div>
    <span class="marquee-dot">•</span>
    <div class="marquee-item" data-ar="من مختلف أنحاء العالم" data-en="From Around the World">من مختلف أنحاء العالم</div>
    <span class="marquee-dot">•</span>
    <div class="marquee-item" data-ar="أفضل القهوة" data-en="The Finest Coffee">أفضل القهوة</div>
    <span class="marquee-dot">•</span>
    <div class="marquee-item" data-ar="محمصة حرفية" data-en="Artisan Roasting">محمصة حرفية</div>
    <span class="marquee-dot">•</span>
    <div class="marquee-item" data-ar="من مختلف أنحاء العالم" data-en="From Around the World">من مختلف أنحاء العالم</div>
  </div>
</div>

<!-- STORY -->
<section class="section" id="story">
  <div class="section-label" data-ar="قصتنا" data-en="Our Story">قصتنا</div>
  <h2 class="section-title" data-ar="رحلة <em>نوكتارا</em>" data-en="The <em>NOCTARA</em> Journey">رحلة <em>نوكتارا</em></h2>
  <div class="story-inner">
    <div class="story-text">
      <p data-ar="نوكتارا ولدت من شغف عميق بفن إعداد القهوة. كل حبة قهوة في مجموعتنا تختار بعناية من أفضل مزارع العالم، من أثيوبيا إلى كولومبيا، من كينيا إلى البرازيل. نحن نؤمن بأن الجودة ليست مجرد كلمة - إنها التزام يومي." data-en="NOCTARA was born from a deep passion for the art of coffee making. Every coffee bean in our collection is carefully selected from the world's finest farms, from Ethiopia to Colombia, from Kenya to Brazil. We believe that quality is not just a word - it is a daily commitment.">نوكتارا ولدت من شغف عميق بفن إعداد القهوة. كل حبة قهوة في مجموعتنا تختار بعناية من أفضل مزارع العالم، من أثيوبيا إلى كولومبيا، من كينيا إلى البرازيل. نحن نؤمن بأن الجودة ليست مجرد كلمة - إنها التزام يومي.</p>
      <br>
      <p data-ar="بدأنا برؤية بسيطة: جعل أفضل القهوة متاحة للجميع. اليوم، نفخر بكل فنجان نقدمه، لأننا نعرف أنه يحمل قصة من الرحلة والشغف والتفاني." data-en="We started with a simple vision: to make the finest coffee accessible to everyone. Today, we are proud of every cup we serve, because we know it carries a story of journey, passion, and dedication.">بدأنا برؤية بسيطة: جعل أفضل القهوة متاحة للجميع. اليوم، نفخر بكل فنجان نقدمه، لأننا نعرف أنه يحمل قصة من الرحلة والشغف والتفاني.</p>
    </div>
    <div class="story-visual">
      <div class="story-visual-bg"></div>
      <svg class="story-visual-logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
        <circle cx="100" cy="100" r="90" fill="none" stroke="#d4af37" stroke-width="1" opacity="0.3"/>
        <text x="100" y="120" font-family="Cormorant Garamond" font-size="60" font-weight="300" text-anchor="middle" fill="#d4af37" letter-spacing="2">NOCTARA</text>
      </svg>
      <div class="story-visual-corner tl"></div>
      <div class="story-visual-corner tr"></div>
      <div class="story-visual-corner bl"></div>
      <div class="story-visual-corner br"></div>
    </div>
  </div>
  <div class="story-quote" data-ar="&quot;في كل فنجان قهوة، هناك قصة - قصة المزرعة، المحمصة، والدقائق التي تتحول فيها الحبات الخضراء إلى ذهب.&quot;" data-en="&quot;In every cup of coffee, there is a story - a story of the farm, the roaster, and the minutes when green beans turn to gold.&quot;">"في كل فنجان قهوة، هناك قصة - قصة المزرعة، المحمصة، والدقائق التي تتحول فيها الحبات الخضراء إلى ذهب."</div>
</section>

<!-- PRODUCTS -->
<section class="section" id="products">
  <div class="section-label" data-ar="المنتجات" data-en="Products">المنتجات</div>
  <h2 class="section-title" data-ar="مجموعتنا <em>الحصرية</em>" data-en="Our <em>Exclusive</em> Collection">مجموعتنا <em>الحصرية</em></h2>
  <div class="products-grid">
    <!-- Product 1: Nomad -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#2a2926,#1a1916);font-size:64px;">☕</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="نكهة خفيفة مع حموضة لطيفة" data-en="Light flavor with gentle acidity">نكهة خفيفة مع حموضة لطيفة</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="إثيوبيا" data-en="Ethiopia">إثيوبيا</div>
        <h3 class="product-name" data-ar="الرحالة" data-en="Nomad">الرحالة</h3>
        <p class="product-desc" data-ar="بنكهات زهرية وفواكه استوائية، الخيار المثالي للصباح." data-en="Floral and tropical fruit notes, perfect for mornings.">بنكهات زهرية وفواكه استوائية، الخيار المثالي للصباح.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 89</span>
          <button class="product-btn" onclick="addToCart('الرحالة - Nomad', 89, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>

    <!-- Product 2: Obsidian -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#1a1916,#0a0908);font-size:64px;">🌑</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="نكهة عميقة وجريئة" data-en="Deep and bold flavor">نكهة عميقة وجريئة</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="البرازيل" data-en="Brazil">البرازيل</div>
        <h3 class="product-name" data-ar="أوبسيديان" data-en="Obsidian">أوبسيديان</h3>
        <p class="product-desc" data-ar="محمصة داكنة مع نكهات الشوكولاتة والجوز، قوة الليل." data-en="Dark roast with chocolate and nutty notes, strength of night.">محمصة داكنة مع نكهات الشوكولاتة والجوز، قوة الليل.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 95</span>
          <button class="product-btn" onclick="addToCart('أوبسيديان - Obsidian', 95, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>

    <!-- Product 3: Aurora -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#d4af37,#e5c158);font-size:64px;color:#0a0908;">🌅</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="توازن مثالي بين الحموضة والجسم" data-en="Perfect balance of acidity and body">توازن مثالي بين الحموضة والجسم</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="كولومبيا" data-en="Colombia">كولومبيا</div>
        <h3 class="product-name" data-ar="الشفق" data-en="Aurora">الشفق</h3>
        <p class="product-desc" data-ar="متوسط الحموضة مع نكهات الفواكه الحمراء، محمصة متوسطة." data-en="Medium acidity with red fruit notes, medium roast.">متوسط الحموضة مع نكهات الفواكه الحمراء، محمصة متوسطة.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 92</span>
          <button class="product-btn" onclick="addToCart('الشفق - Aurora', 92, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>

    <!-- Product 4: Pearl -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#c9c5bd,#e8e6e1);font-size:64px;color:#0a0908;">💎</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="نكهة نقية وخالصة" data-en="Pure and clean flavor">نكهة نقية وخالصة</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="كينيا" data-en="Kenya">كينيا</div>
        <h3 class="product-name" data-ar="اللؤلؤ" data-en="Pearl">اللؤلؤ</h3>
        <p class="product-desc" data-ar="محمصة فاتحة مع حموضة نظيفة وحلاوة طبيعية." data-en="Light roast with clean acidity and natural sweetness.">محمصة فاتحة مع حموضة نظيفة وحلاوة طبيعية.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 88</span>
          <button class="product-btn" onclick="addToCart('اللؤلؤ - Pearl', 88, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>

    <!-- Product 5: Andes -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#8b7355,#a0826d);font-size:64px;">🏔️</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="حموضة عالية وقوام متوسط" data-en="High acidity with medium body">حموضة عالية وقوام متوسط</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="البيرو" data-en="Peru">البيرو</div>
        <h3 class="product-name" data-ar="الأنديز" data-en="Andes">الأنديز</h3>
        <p class="product-desc" data-ar="نكهات حمضية منعشة مع تلميحات من الكاكاو." data-en="Bright acidic flavors with cocoa hints.">نكهات حمضية منعشة مع تلميحات من الكاكاو.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 91</span>
          <button class="product-btn" onclick="addToCart('الأنديز - Andes', 91, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>

    <!-- Product 6: Amazon -->
    <div class="product-card">
      <div class="product-visual">
        <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#2d5016,#3a6b1f);font-size:64px;">🌿</div>
        <div class="product-quote"><div class="product-quote-text" data-ar="نكهات غابية وأرضية" data-en="Earthy and forest notes">نكهات غابية وأرضية</div></div>
      </div>
      <div class="product-info">
        <div class="product-origin" data-ar="بيرو / بوليفيا" data-en="Peru / Bolivia">بيرو / بوليفيا</div>
        <h3 class="product-name" data-ar="الأمازون" data-en="Amazon">الأمازون</h3>
        <p class="product-desc" data-ar="محمصة متوسطة مع نكهات الشوكولاتة الداكنة والتراب." data-en="Medium roast with dark chocolate and earthy notes.">محمصة متوسطة مع نكهات الشوكولاتة الداكنة والتراب.</p>
        <div class="product-footer">
          <span class="product-price"><span data-ar="ر.س" data-en="SAR">ر.س</span> 90</span>
          <button class="product-btn" onclick="addToCart('الأمازون - Amazon', 90, 250)" data-ar="أضف للسلة" data-en="Add to Cart">أضف للسلة</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- QUOTES STRIP -->
<div class="quotes-strip">
  <div class="quotes-strip-inner">
    <div class="novel-banner">
      <div class="novel-banner-line"></div>
      <div class="novel-banner-text" data-ar="أقوال مشهورة" data-en="Famous Quotes">أقوال مشهورة</div>
      <div class="novel-banner-line"></div>
    </div>
    <div class="quotes-grid">
      <div class="quote-card">
        <div class="quote-text" data-ar="&quot;القهوة هي تعويذة سحرية في كوب.&quot;" data-en="&quot;Coffee is a magical spell in a cup.&quot;">"القهوة هي تعويذة سحرية في كوب."</div>
        <div class="quote-source" data-ar="كاتب مشهور" data-en="Famous Author">كاتب مشهور</div>
      </div>
      <div class="quote-card">
        <div class="quote-text" data-ar="&quot;الحياة طويلة جداً لتضيع على قهوة سيئة.&quot;" data-en="&quot;Life is too long to waste on bad coffee.&quot;">"الحياة طويلة جداً لتضيع على قهوة سيئة."</div>
        <div class="quote-source" data-ar="عشاق القهوة" data-en="Coffee Lovers">عشاق القهوة</div>
      </div>
      <div class="quote-card">
        <div class="quote-text" data-ar="&quot;في كل فنجان قهوة، تجد السلام والهدوء والإلهام.&quot;" data-en="&quot;In every cup of coffee, you find peace, calmness and inspiration.&quot;">"في كل فنجان قهوة، تجد السلام والهدوء والإلهام."</div>
        <div class="quote-source" data-ar="فلاسفة القهوة" data-en="Coffee Philosophers">فلاسفة القهوة</div>
      </div>
    </div>
  </div>
</div>

<!-- RITUAL -->
<div class="ritual-wrap">
  <div class="ritual-grid">
    <div class="ritual-item">
      <div class="ritual-num">1</div>
      <div class="ritual-title" data-ar="الاختيار" data-en="Selection">الاختيار</div>
      <div class="ritual-text" data-ar="نختار أفضل الحبات من أفضل المزارع" data-en="Select the finest beans from premier farms">نختار أفضل الحبات من أفضل المزارع</div>
    </div>
    <div class="ritual-item">
      <div class="ritual-num">2</div>
      <div class="ritual-title" data-ar="الحماية" data-en="Preservation">الحماية</div>
      <div class="ritual-text" data-ar="نحافظ على النكهات بعناية طوال الرحلة" data-en="Carefully preserve flavors throughout the journey">نحافظ على النكهات بعناية طوال الرحلة</div>
    </div>
    <div class="ritual-item">
      <div class="ritual-num">3</div>
      <div class="ritual-title" data-ar="الحماسة" data-en="Roasting">الحماسة</div>
      <div class="ritual-text" data-ar="نحمص بشغف وفن لإظهار أفضل نكهاتها" data-en="Roast with passion and art to reveal best flavors">نحمص بشغف وفن لإظهار أفضل نكهاتها</div>
    </div>
    <div class="ritual-item">
      <div class="ritual-num">4</div>
      <div class="ritual-title" data-ar="التسليم" data-en="Delivery">التسليم</div>
      <div class="ritual-text" data-ar="نسلمها لك طازجة ومليئة بالحب" data-en="Deliver them fresh and full of love to you">نسلمها لك طازجة ومليئة بالحب</div>
    </div>
  </div>
</div>

<!-- ABOUT -->
<section class="section" id="about">
  <div class="section-label" data-ar="عن نوكتارا" data-en="About NOCTARA">عن نوكتارا</div>
  <h2 class="section-title" data-ar="مهمتنا و رؤيتنا" data-en="Our Mission & Vision">مهمتنا و رؤيتنا</h2>
  <div class="about-inner">
    <div>
      <p style="margin-bottom:20px;color:var(--cream-dim);" data-ar="نوكتارا ليست مجرد علامة قهوة، بل هي فلسفة حياة. نحن نؤمن بأن أفضل اللحظات تتشكل حول فنجان قهوة جيدة." data-en="NOCTARA is not just a coffee brand, it's a life philosophy. We believe the best moments are formed around a good cup of coffee.">نوكتارا ليست مجرد علامة قهوة، بل هي فلسفة حياة. نحن نؤمن بأن أفضل اللحظات تتشكل حول فنجان قهوة جيدة.</p>
      <p style="color:var(--cream-dim);" data-ar="التزامنا تجاه الاستدامة والأخلاقيات يعكس قيمنا الأساسية. نتعاون مع المزارعين الذين يشاركوننا رؤيتنا لمستقبل أفضل." data-en="Our commitment to sustainability and ethics reflects our core values. We partner with farmers who share our vision for a better future.">التزامنا تجاه الاستدامة والأخلاقيات يعكس قيمنا الأساسية. نتعاون مع المزارعين الذين يشاركوننا رؤيتنا لمستقبل أفضل.</p>
      <div class="about-stat-grid">
        <div class="about-stat">
          <div class="about-stat-num">18+</div>
          <div class="about-stat-label" data-ar="دولة" data-en="Countries">دولة</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">2K+</div>
          <div class="about-stat-label" data-ar="عميل سعيد" data-en="Happy Customers">عميل سعيد</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">100%</div>
          <div class="about-stat-label" data-ar="أخلاقي" data-en="Ethical">أخلاقي</div>
        </div>
        <div class="about-stat">
          <div class="about-stat-num">50+</div>
          <div class="about-stat-label" data-ar="مزرعة" data-en="Farms">مزرعة</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="section" id="testimonials">
  <div class="section-label" data-ar="آراء العملاء" data-en="Customer Reviews">آراء العملاء</div>
  <h2 class="section-title" data-ar="ماذا يقول <em>عملاؤنا</em>" data-en="What Our <em>Customers</em> Say">ماذا يقول <em>عملاؤنا</em></h2>
  <div class="testi-grid">
    <div class="testi-card">
      <div class="testi-text" data-ar="&quot;أفضل قهوة جربتها في حياتي. الجودة والطعم لا يُصدّقان. سأطلب مرة أخرى بالتأكيد.&quot;" data-en="&quot;The best coffee I've ever tasted. Quality and flavor are unbelievable. I'll definitely order again.&quot;">"أفضل قهوة جربتها في حياتي. الجودة والطعم لا يُصدّقان. سأطلب مرة أخرى بالتأكيد."</div>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author" data-ar="سارة الدعيجان" data-en="Sarah Al-Dowaigan">سارة الدعيجان</div>
    </div>
    <div class="testi-card">
      <div class="testi-text" data-ar="&quot;تجربة استثنائية من البداية إلى النهاية. الخدمة رائعة والقهوة تستحق كل ريال.&quot;" data-en="&quot;Exceptional experience from start to finish. Great service and coffee worth every riyal.&quot;">"تجربة استثنائية من البداية إلى النهاية. الخدمة رائعة والقهوة تستحق كل ريال."</div>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author" data-ar="محمد العبدالله" data-en="Mohammed Al-Abdullah">محمد العبدالله</div>
    </div>
    <div class="testi-card">
      <div class="testi-text" data-ar="&quot;لم أتوقع هذا المستوى من الاحترافية والجودة. نوكتارا أصبحت خيارنا الأول.&quot;" data-en="&quot;I didn't expect this level of professionalism and quality. NOCTARA is now our first choice.&quot;">"لم أتوقع هذا المستوى من الاحترافية والجودة. نوكتارا أصبحت خيارنا الأول."</div>
      <div class="testi-stars">★★★★★</div>
      <div class="testi-author" data-ar="فاطمة المطيري" data-en="Fatima Al-Mutairi">فاطمة المطيري</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div>
      <div class="footer-logo-wrap">
        <svg class="footer-logo-img" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
          <circle cx="100" cy="100" r="95" fill="none" stroke="#d4af37" stroke-width="1" opacity="0.3"/>
          <text x="100" y="115" font-family="Cormorant Garamond" font-size="38" font-weight="300" text-anchor="middle" fill="#d4af37" letter-spacing="2">NOCTARA</text>
        </svg>
        <span class="footer-brand-name">NOCTARA</span>
      </div>
      <p class="footer-brand-tag" data-ar="قهوة الليل الأسود" data-en="The Black Night Coffee">قهوة الليل الأسود</p>
      <p class="footer-brand-text" data-ar="قهوة حرفية من أفضل مزارع العالم، مختارة بعناية ومحمصة بشغف." data-en="Artisan coffee from the world's finest farms, carefully selected and passionately roasted.">قهوة حرفية من أفضل مزارع العالم، مختارة بعناية ومحمصة بشغف.</p>
    </div>
    <div>
      <div class="footer-col-title" data-ar="الروابط" data-en="Links">الروابط</div>
      <ul class="footer-links">
        <li><a href="#story" data-ar="القصة" data-en="Story">القصة</a></li>
        <li><a href="#products" data-ar="المنتجات" data-en="Products">المنتجات</a></li>
        <li><a href="#about" data-ar="عننا" data-en="About">عننا</a></li>
        <li><a href="#testimonials" data-ar="التقييمات" data-en="Reviews">التقييمات</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title" data-ar="التواصل" data-en="Contact">التواصل</div>
      <ul class="footer-links">
        <li><a href="https://wa.me/201551290097" target="_blank" data-ar="واتساب" data-en="WhatsApp">واتساب</a></li>
        <li><a href="mailto:info@noctara.com" data-ar="البريد" data-en="Email">البريد</a></li>
        <li><a href="#" data-ar="الموقع" data-en="Website">الموقع</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title" data-ar="المتابعة" data-en="Follow">المتابعة</div>
      <div class="footer-social">
        <a href="#" class="footer-social-link" title="Instagram">📷</a>
        <a href="#" class="footer-social-link" title="Facebook">f</a>
        <a href="#" class="footer-social-link" title="Twitter">𝕏</a>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <p class="footer-copy" data-ar="© 2024 NOCTARA. جميع الحقوق محفوظة." data-en="© 2024 NOCTARA. All rights reserved.">© 2024 NOCTARA. جميع الحقوق محفوظة.</p>
    <p class="footer-copy" data-ar="مصنوع بـ ❤️ من المملكة العربية السعودية" data-en="Made with ❤️ from Saudi Arabia">مصنوع بـ ❤️ من المملكة العربية السعودية</p>
  </div>
</footer>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
// ========== STATE ==========
let cart = [];
let currentLang = 'ar';

// ========== LANGUAGE ==========
function setLang(lang) {
  currentLang = lang;
  const root = document.documentElement;
  root.lang = lang;
  document.body.className = lang === 'ar' ? 'ar' : 'en';
  
  document.querySelectorAll('[data-ar][data-en]').forEach(el => {
    el.textContent = lang === 'ar' ? el.getAttribute('data-ar') : el.getAttribute('data-en');
  });
  
  document.querySelectorAll('button.lang-btn').forEach(btn => {
    btn.classList.remove('active');
  });
  event.target.classList.add('active');
}

// ========== CART ==========
function addToCart(name, price, size = 250) {
  const item = {
    id: Date.now(),
    name,
    price,
    size,
    qty: 1
  };
  
  const existing = cart.find(p => p.name === name);
  if (existing) {
    existing.qty++;
  } else {
    cart.push(item);
  }
  
  updateCart();
  showToast(currentLang === 'ar' ? 'تمت إضافة المنتج للسلة' : 'Product added to cart');
}

function updateCart() {
  const count = cart.reduce((sum, item) => sum + item.qty, 0);
  const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
  
  const cartCount = document.getElementById('cartCount');
  const cartItems = document.getElementById('cartItems');
  const cartFooter = document.getElementById('cartFooter');
  const cartTotal = document.getElementById('cartTotalPrice');
  
  if (count === 0) {
    cartCount.style.display = 'none';
    cartItems.innerHTML = '<div class="cart-empty" data-ar="السلة فارغة" data-en="Cart is empty">السلة فارغة</div>';
    cartFooter.style.display = 'none';
  } else {
    cartCount.textContent = count;
    cartCount.style.display = 'flex';
    cartFooter.style.display = 'block';
    
    cartItems.innerHTML = cart.map(item => `
      <div class="cart-item">
        <div class="cart-item-img">☕ ${item.size}g</div>
        <div class="cart-item-info">
          <div class="cart-item-name">${item.name}</div>
          <div class="cart-item-price">${item.price} ر.س</div>
          <div class="cart-item-qty">
            <button class="qty-btn" onclick="updateQty(${item.id}, -1)">−</button>
            <span>${item.qty}</span>
            <button class="qty-btn" onclick="updateQty(${item.id}, 1)">+</button>
          </div>
        </div>
        <div class="cart-item-remove" onclick="removeFromCart(${item.id})">🗑️</div>
      </div>
    `).join('');
    
    cartTotal.textContent = `${total} ر.س`;
  }
}

function updateQty(id, delta) {
  const item = cart.find(p => p.id === id);
  if (item) {
    item.qty += delta;
    if (item.qty <= 0) {
      removeFromCart(id);
    } else {
      updateCart();
    }
  }
}

function removeFromCart(id) {
  cart = cart.filter(item => item.id !== id);
  updateCart();
}

function openCart() {
  document.getElementById('cartDrawer').classList.add('open');
  document.getElementById('cartOverlay').classList.add('open');
}

function closeCart() {
  document.getElementById('cartDrawer').classList.remove('open');
  document.getElementById('cartOverlay').classList.remove('open');
}

// ========== CHECKOUT ==========
let uploadedFile = null;

function openCheckout() {
  closeCart();
  document.getElementById('checkoutModal').classList.add('open');
  updateCheckoutSummary();
}

function closeCheckout() {
  document.getElementById('checkoutModal').classList.remove('open');
}

function updateCheckoutSummary() {
  const summary = document.getElementById('checkoutSummary');
  const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
  
  summary.innerHTML = `
    ${cart.map(item => `
      <div class="summary-row">
        <span class="summary-row-label">${item.name} × ${item.qty}</span>
        <span class="summary-row-value">${item.price * item.qty} ر.س</span>
      </div>
    `).join('')}
    <div class="summary-total">
      <span class="summary-total-label" data-ar="الإجمالي" data-en="Total">الإجمالي</span>
      <span class="summary-total-price">${total} ر.س</span>
    </div>
  `;
}

function selectPayment(method) {
  document.querySelectorAll('.payment-method').forEach(m => m.classList.remove('selected'));
  event.target.closest('.payment-method').classList.add('selected');
}

function handleDragOver(e) {
  e.preventDefault();
  document.getElementById('uploadArea').classList.add('active');
}

function handleDragLeave(e) {
  e.preventDefault();
  document.getElementById('uploadArea').classList.remove('active');
}

function handleDrop(e) {
  e.preventDefault();
  document.getElementById('uploadArea').classList.remove('active');
  const files = e.dataTransfer.files;
  if (files.length > 0) {
    handleFileSelect({target: {files}});
  }
}

function handleFileSelect(e) {
  const file = e.target.files[0];
  if (!file) return;
  
  if (file.size > 5 * 1024 * 1024) {
    showToast(currentLang === 'ar' ? 'حجم الملف كبير جداً (5MB max)' : 'File too large (5MB max)');
    return;
  }
  
  uploadedFile = file;
  const reader = new FileReader();
  reader.onload = (ev) => {
    const preview = document.getElementById('uploadPreview');
    preview.innerHTML = `
      <div class="upload-preview">
        <img src="${ev.target.result}" class="upload-preview-img">
        <div class="upload-preview-info">
          <div class="upload-preview-name">${file.name}</div>
          <div class="upload-preview-size">${(file.size / 1024).toFixed(2)} KB</div>
        </div>
        <button class="upload-remove" onclick="clearUpload()">✕</button>
      </div>
    `;
    preview.style.display = 'block';
    document.getElementById('uploadArea').style.display = 'none';
  };
  reader.readAsDataURL(file);
}

function clearUpload() {
  uploadedFile = null;
  document.getElementById('uploadPreview').style.display = 'none';
  document.getElementById('uploadArea').style.display = 'block';
  document.getElementById('fileInput').value = '';
}

function confirmOrder() {
  const name = document.getElementById('customerName').value.trim();
  const phone = document.getElementById('customerPhone').value.trim();
  const email = document.getElementById('customerEmail').value.trim();
  const address = document.getElementById('customerAddress').value.trim();
  const city = document.getElementById('customerCity').value.trim();
  const region = document.getElementById('customerRegion').value.trim();
  const payment = document.querySelector('input[name="payment"]:checked').value;
  
  if (!name || !phone || !address || !city) {
    showToast(currentLang === 'ar' ? 'يرجى ملء جميع الحقول المطلوبة' : 'Please fill all required fields');
    return;
  }
  
  if (!uploadedFile && payment === 'instapay') {
    showToast(currentLang === 'ar' ? 'يرجى رفع صورة التحويل' : 'Please upload transfer receipt');
    return;
  }
  
  const orderText = formatOrderMessage(name, phone, email, address, city, region, payment);
  const whatsappUrl = `https://wa.me/201551290097?text=${encodeURIComponent(orderText)}`;
  
  window.open(whatsappUrl, '_blank');
  
  // Reset
  cart = [];
  updateCart();
  closeCheckout();
  clearUpload();
  document.getElementById('checkoutModal').querySelector('form')?.reset();
  
  showToast(currentLang === 'ar' ? 'تم إرسال طلبك بنجاح! شكراً لك 💚' : 'Order sent successfully! Thank you 💚');
}

function formatOrderMessage(name, phone, email, address, city, region, payment) {
  const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
  const items = cart.map(item => `• ${item.name} × ${item.qty} = ${item.price * item.qty} ر.س`).join('\n');
  
  return currentLang === 'ar' 
    ? `🎁 *طلب جديد من نوكتارا*\n\n👤 الاسم: ${name}\n📱 الهاتف: ${phone}\n📧 البريد: ${email || 'لم يتم تقديمه'}\n\n📍 العنوان: ${address}\n🏙️ المدينة: ${city}${region ? '\n📌 المنطقة: ' + region : ''}\n\n🛍️ *الطلب:*\n${items}\n\n💰 *الإجمالي: ${total} ريال*\n\n💳 طريقة الدفع: ${payment === 'instapay' ? 'انستا باي / محفظة' : 'تحويل بنكي'}\n\nشكراً لاختيارك نوكتارا! ❤️`
    : `🎁 *New Order from NOCTARA*\n\n👤 Name: ${name}\n📱 Phone: ${phone}\n📧 Email: ${email || 'Not provided'}\n\n📍 Address: ${address}\n🏙️ City: ${city}${region ? '\n📌 Region: ' + region : ''}\n\n🛍️ *Order:*\n${items}\n\n💰 *Total: ${total} SAR*\n\n💳 Payment Method: ${payment === 'instapay' ? 'Instapay / Digital Wallet' : 'Bank Transfer'}\n\nThank you for choosing NOCTARA! ❤️`;
}

function showToast(message) {
  const toast = document.getElementById('toast');
  toast.textContent = message;
  toast.classList.add('show');
  setTimeout(() => toast.classList.remove('show'), 3000);
}

// ========== SCROLL EFFECTS ==========
window.addEventListener('scroll', () => {
  const nav = document.getElementById('nav');
  nav.classList.toggle('scrolled', window.scrollY > 50);
});

// ========== INIT ==========
setLang('ar');
updateCart();
document.getElementById('cartOverlay').addEventListener('click', closeCart);
</script>

</body>
</html>
