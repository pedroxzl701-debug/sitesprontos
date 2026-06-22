<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Copynet Gráfica Rápida — Natal/RN</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --black:#111111;--white:#FFFFFF;--gray:#F5F5F3;--gray2:#E9E9E6;
  --muted:#888884;--cyan:#00B4D8;--cyan-dk:#0090AD;--cyan-bg:#E6F8FC;
  --green:#25D366;--border:rgba(17,17,17,.1);--r:6px;--rL:14px;
  --pad:clamp(1.25rem,5vw,4.5rem);
}
html{scroll-behavior:smooth}
body{font-family:'Inter',sans-serif;background:var(--white);color:var(--black);line-height:1.6;overflow-x:hidden}

/* ════ NAV ════ */
nav{
  position:fixed;top:0;left:0;right:0;z-index:300;
  height:62px;display:flex;align-items:center;justify-content:space-between;
  padding:0 var(--pad);
  background:rgba(17,17,17,.97);backdrop-filter:blur(18px);
  border-bottom:1px solid rgba(255,255,255,.07);
}
.logo{display:flex;align-items:center;gap:10px;text-decoration:none;flex-shrink:0}
.logo-box{width:34px;height:34px;border-radius:5px;background:var(--cyan);display:flex;align-items:center;justify-content:center}
.logo-box svg{width:18px;height:18px;fill:var(--black)}
.logo-name{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:.95rem;color:var(--white);letter-spacing:-.02em}
.logo-sub{font-size:.6rem;color:rgba(255,255,255,.38);letter-spacing:.06em;text-transform:uppercase}
.nav-links{display:flex;gap:1.75rem;list-style:none}
.nav-links a{
  font-size:.78rem;color:rgba(255,255,255,.5);text-decoration:none;
  letter-spacing:.01em;transition:color .2s;padding:4px 0;
  border-bottom:2px solid transparent;
}
.nav-links a:hover,.nav-links a.active{color:var(--white)}
.nav-links a.active{border-bottom-color:var(--cyan)}
.nav-right{display:flex;align-items:center;gap:.75rem}
.nav-orcamento{
  background:var(--cyan);color:var(--black);
  padding:.48rem 1.1rem;border-radius:var(--r);
  font-size:.78rem;font-weight:600;text-decoration:none;
  white-space:nowrap;transition:background .2s;cursor:pointer;border:none;
  font-family:'Inter',sans-serif;letter-spacing:.01em;
}
.nav-orcamento:hover{background:var(--cyan-dk);color:var(--white)}
.nav-toggle{display:none;background:none;border:none;cursor:pointer;padding:4px}
.nav-toggle span{display:block;width:22px;height:2px;background:var(--white);margin:5px 0;transition:.3s;border-radius:2px}

/* ════ MOBILE MENU ════ */
.mob-nav{
  display:none;position:fixed;inset:0;top:62px;z-index:290;
  background:rgba(17,17,17,.99);backdrop-filter:blur(18px);
  flex-direction:column;align-items:center;justify-content:center;gap:2.25rem;
}
.mob-nav.open{display:flex}
.mob-nav a{font-family:'Space Grotesk',sans-serif;font-size:1.6rem;font-weight:700;color:rgba(255,255,255,.65);text-decoration:none;transition:color .2s}
.mob-nav a:hover{color:var(--white)}
.mob-nav .mob-cta{background:var(--cyan);color:var(--black);padding:.7rem 2.5rem;border-radius:var(--r);font-size:1rem;margin-top:.5rem}

/* ════ HERO ════ */
.hero{
  background:var(--black);min-height:100svh;
  padding:calc(62px + 5rem) var(--pad) 5rem;
  display:flex;flex-direction:column;justify-content:center;
  position:relative;overflow:hidden;
}
.cmyk-bar{position:absolute;top:62px;left:0;right:0;height:4px;display:flex}
.cmyk-bar span{flex:1}
.cmyk-bar span:nth-child(1){background:#00AEEF}
.cmyk-bar span:nth-child(2){background:#EC008C}
.cmyk-bar span:nth-child(3){background:#FFF200}
.cmyk-bar span:nth-child(4){background:#333}
.hero-inner{max-width:1100px;margin:0 auto;width:100%}
.hero-tag{
  display:inline-flex;align-items:center;gap:7px;
  border:1px solid rgba(255,255,255,.14);color:rgba(255,255,255,.55);
  font-size:.7rem;letter-spacing:.09em;text-transform:uppercase;
  padding:.35rem .9rem;border-radius:100px;margin-bottom:2rem;
}
.hero-tag::before{content:'';width:6px;height:6px;border-radius:50%;background:var(--cyan);animation:blink 2s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.2}}
.hero h1{
  font-family:'Space Grotesk',sans-serif;
  font-size:clamp(3rem,7.5vw,6.5rem);
  font-weight:700;line-height:.95;letter-spacing:-.04em;color:var(--white);
  margin-bottom:2.5rem;
}
.hero h1 em{font-style:normal;color:var(--cyan)}
.hero-bottom{
  display:flex;align-items:flex-end;justify-content:space-between;
  gap:2rem;flex-wrap:wrap;
  border-top:1px solid rgba(255,255,255,.08);padding-top:2rem;
}
.hero-desc{font-size:.98rem;color:rgba(255,255,255,.5);max-width:400px;line-height:1.75}
.hero-actions{display:flex;gap:.75rem;flex-shrink:0;flex-wrap:wrap}
.btn-cyan{
  background:var(--cyan);color:var(--black);
  padding:.85rem 1.75rem;border-radius:var(--r);
  font-size:.9rem;font-weight:600;text-decoration:none;cursor:pointer;
  display:inline-flex;align-items:center;gap:8px;
  transition:background .2s,transform .15s;white-space:nowrap;border:none;
  font-family:'Inter',sans-serif;
}
.btn-cyan:hover{background:var(--cyan-dk);color:var(--white);transform:translateY(-1px)}
.btn-outline-w{
  background:transparent;color:var(--white);
  padding:.85rem 1.5rem;border-radius:var(--r);
  border:1px solid rgba(255,255,255,.2);font-size:.9rem;font-weight:500;
  text-decoration:none;cursor:pointer;font-family:'Inter',sans-serif;
  display:inline-flex;align-items:center;gap:8px;
  transition:border-color .2s,background .2s;white-space:nowrap;
}
.btn-outline-w:hover{border-color:rgba(255,255,255,.5);background:rgba(255,255,255,.06)}

/* ════ PILLS ════ */
.pills{
  background:var(--cyan);padding:.9rem var(--pad);
  display:flex;gap:2rem;align-items:center;overflow-x:auto;scrollbar-width:none;
}
.pills::-webkit-scrollbar{display:none}
.pill{display:flex;align-items:center;gap:6px;font-family:'Space Grotesk',sans-serif;font-size:.75rem;font-weight:600;color:var(--black);white-space:nowrap}
.pill::after{content:'·';color:rgba(0,0,0,.3);margin-left:.5rem}
.pill:last-child::after{display:none}

/* ════ SECTIONS ════ */
.sec{padding:5rem var(--pad)}
.sec-inner{max-width:1100px;margin:0 auto}
.eyebrow{font-size:.67rem;font-weight:600;letter-spacing:.13em;text-transform:uppercase;color:var(--cyan);margin-bottom:.6rem;display:block}
.sec h2{font-family:'Space Grotesk',sans-serif;font-size:clamp(1.75rem,3.5vw,2.6rem);font-weight:700;letter-spacing:-.03em;line-height:1.1;margin-bottom:.7rem}
.sec-lead{font-size:.97rem;color:var(--muted);max-width:480px;line-height:1.75}

/* ════ SERVICES ════ */
#servicos{background:var(--gray)}
.srv-header{display:flex;align-items:flex-end;justify-content:space-between;gap:1rem;flex-wrap:wrap;margin-bottom:2.5rem}
.srv-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--border);border:1px solid var(--border);border-radius:var(--rL);overflow:hidden}
.srv{background:var(--gray);padding:1.75rem 1.5rem;transition:background .2s,box-shadow .2s;cursor:default;position:relative}
.srv:hover{background:var(--white);box-shadow:inset 0 0 0 1.5px var(--cyan)}
.srv-ic{width:44px;height:44px;border-radius:var(--r);background:var(--white);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:1.25rem;margin-bottom:1rem}
.srv h3{font-family:'Space Grotesk',sans-serif;font-size:.92rem;font-weight:600;margin-bottom:.35rem}
.srv p{font-size:.78rem;color:var(--muted);line-height:1.65}
.srv-tag{display:inline-block;font-size:.65rem;font-weight:600;letter-spacing:.07em;text-transform:uppercase;background:var(--cyan-bg);color:var(--cyan);padding:.2rem .55rem;border-radius:100px;margin-top:.75rem}

/* ════ PROCESS ════ */
#processo{background:var(--black)}
#processo .eyebrow{color:var(--cyan)}
#processo h2{color:var(--white)}
#processo .sec-lead{color:rgba(255,255,255,.4)}
.proc-grid{display:grid;grid-template-columns:repeat(4,1fr);border:1px solid rgba(255,255,255,.08);border-radius:var(--rL);overflow:hidden;margin-top:2.5rem}
.proc-step{padding:2rem 1.5rem;border-right:1px solid rgba(255,255,255,.08);position:relative}
.proc-step:last-child{border-right:none}
.proc-n{font-family:'Space Grotesk',sans-serif;font-size:3rem;font-weight:700;letter-spacing:-.04em;color:rgba(255,255,255,.05);line-height:1;margin-bottom:1.5rem}
.proc-dot{width:8px;height:8px;border-radius:50%;background:var(--cyan);margin-bottom:1.1rem}
.proc-step h3{font-family:'Space Grotesk',sans-serif;font-size:.92rem;font-weight:600;color:var(--white);margin-bottom:.4rem}
.proc-step p{font-size:.78rem;color:rgba(255,255,255,.38);line-height:1.7}
.proc-step .proc-detail{font-size:.72rem;color:rgba(255,255,255,.22);margin-top:.75rem;line-height:1.6}

/* ════ PORTFOLIO ════ */
#portfolio{background:var(--white)}
.port-header{display:flex;align-items:flex-end;justify-content:space-between;gap:1rem;flex-wrap:wrap;margin-bottom:2.5rem}
.port-grid{display:grid;grid-template-columns:repeat(3,1fr);grid-template-rows:220px 220px;gap:10px}
.port-card{border-radius:var(--rL);overflow:hidden;display:flex;flex-direction:column;justify-content:flex-end;padding:1.25rem;position:relative;transition:transform .22s,box-shadow .22s;cursor:pointer}
.port-card:hover{transform:translateY(-3px);box-shadow:0 12px 32px rgba(0,0,0,.18)}
.port-card.wide{grid-column:1/3}
.port-card.tall{grid-row:1/3;grid-column:3}
.pb1{background:linear-gradient(140deg,#0A1628 0%,#1A3050 100%)}
.pb2{background:linear-gradient(140deg,#111 0%,#1e1e1e 100%)}
.pb3{background:linear-gradient(140deg,#007EA7 0%,#00B4D8 100%)}
.pb4{background:linear-gradient(140deg,#F0EDE6 0%,#DDD 100%)}
.pb5{background:linear-gradient(140deg,#1A1A1A 0%,#282828 100%)}
.port-card::before{content:'';position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.5) 0%,transparent 60%);border-radius:var(--rL)}
.pb4::before{background:linear-gradient(to top,rgba(0,0,0,.25) 0%,transparent 60%)}
.port-icon{position:absolute;top:1.25rem;left:1.25rem;font-size:2rem;z-index:1}
.port-info{position:relative;z-index:1}
.port-sub{font-size:.65rem;letter-spacing:.08em;text-transform:uppercase;color:rgba(255,255,255,.5);margin-bottom:.2rem}
.pb4 .port-sub{color:rgba(0,0,0,.4)}
.port-label{font-family:'Space Grotesk',sans-serif;font-size:1rem;font-weight:600;color:var(--white)}
.pb4 .port-label{color:var(--black)}
.port-badge{position:absolute;top:1.25rem;right:1.25rem;z-index:1;background:var(--cyan);color:var(--black);font-size:.62rem;font-weight:700;letter-spacing:.06em;padding:.2rem .55rem;border-radius:100px}

/* ════ DEPOIMENTOS ════ */
#depoimentos{background:var(--gray)}
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;margin-top:2.5rem}
.test-card{background:var(--white);border:1px solid var(--border);border-radius:var(--rL);padding:1.5rem;display:flex;flex-direction:column;gap:.9rem}
.test-stars{color:#F59E0B;font-size:.85rem;letter-spacing:2px}
.test-text{font-size:.85rem;color:var(--muted);line-height:1.75;flex:1}
.test-author{display:flex;align-items:center;gap:10px;padding-top:.9rem;border-top:1px solid var(--border)}
.test-av{width:36px;height:36px;min-width:36px;border-radius:50%;background:var(--cyan-bg);color:var(--cyan);display:flex;align-items:center;justify-content:center;font-family:'Space Grotesk',sans-serif;font-size:.7rem;font-weight:700}
.test-name{font-size:.82rem;font-weight:500}
.test-role{font-size:.7rem;color:var(--muted)}
.test-verified{display:inline-flex;align-items:center;gap:4px;font-size:.65rem;color:var(--cyan);margin-top:2px}

/* ════ CTA STRIP ════ */
.cta-strip{background:var(--cyan);padding:3.5rem var(--pad)}
.cta-inner{max-width:1100px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:2rem;flex-wrap:wrap}
.cta-inner h2{font-family:'Space Grotesk',sans-serif;font-size:clamp(1.4rem,2.8vw,2.1rem);font-weight:700;letter-spacing:-.025em;color:var(--black)}
.cta-inner p{font-size:.88rem;color:rgba(0,0,0,.55);margin-top:.3rem}
.btn-black{background:var(--black);color:var(--white);padding:.9rem 1.75rem;border-radius:var(--r);font-size:.88rem;font-weight:600;text-decoration:none;cursor:pointer;border:none;font-family:'Inter',sans-serif;display:inline-flex;align-items:center;gap:8px;transition:transform .15s,background .2s;white-space:nowrap}
.btn-black:hover{transform:translateY(-1px);background:#2a2a2a}

/* ════ CONTACT ════ */
#contato{background:var(--white)}
.contact-grid{display:grid;grid-template-columns:1fr 1.25fr;gap:4rem;align-items:start;margin-top:3rem}
.contact-aside h3{font-family:'Space Grotesk',sans-serif;font-size:.95rem;font-weight:600;margin-bottom:1.25rem}
.info-list{display:flex;flex-direction:column;gap:.75rem}
.info-item{display:flex;align-items:flex-start;gap:12px;padding:1rem;border:1px solid var(--border);border-radius:var(--r);background:var(--gray);transition:border-color .2s}
.info-item:hover{border-color:var(--cyan)}
.info-ic{width:40px;height:40px;min-width:40px;border-radius:var(--r);background:var(--white);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:1.1rem}
.info-item strong{display:block;font-size:.82rem;font-weight:500;margin-bottom:2px}
.info-item a,.info-item span{font-size:.78rem;color:var(--muted);text-decoration:none}
.info-item a{color:var(--cyan)}
.info-item a:hover{text-decoration:underline}
.info-desc{font-size:.7rem;color:rgba(0,0,0,.3);margin-top:2px}

.hours-box{margin-top:1.25rem;background:var(--black);border-radius:var(--r);padding:1.25rem}
.hours-box h4{font-family:'Space Grotesk',sans-serif;font-size:.78rem;font-weight:600;color:var(--white);margin-bottom:.9rem;display:flex;align-items:center;gap:6px}
.h-row{display:flex;justify-content:space-between;align-items:center;padding:.38rem 0;border-bottom:1px solid rgba(255,255,255,.06)}
.h-row:last-child{border-bottom:none}
.h-row span:first-child{font-size:.74rem;color:rgba(255,255,255,.38)}
.h-row .hval{font-size:.74rem;color:var(--white);font-weight:500}
.h-row .hval.closed{color:rgba(255,255,255,.22)}
.h-row .open-badge{font-size:.62rem;background:rgba(37,211,102,.15);color:#25D366;padding:.15rem .45rem;border-radius:100px;font-weight:600}

.form-wrap{background:var(--gray);border:1px solid var(--border);border-radius:var(--rL);padding:2rem}
.form-wrap h3{font-family:'Space Grotesk',sans-serif;font-size:.95rem;font-weight:600;margin-bottom:.25rem}
.form-wrap>p{font-size:.8rem;color:var(--muted);margin-bottom:1.5rem}
.form{display:flex;flex-direction:column;gap:.85rem}
.fg{display:flex;flex-direction:column;gap:5px}
.fg label{font-size:.73rem;font-weight:500;color:var(--black);letter-spacing:.02em}
.fg input,.fg select,.fg textarea{padding:.7rem .9rem;border:1px solid var(--gray2);border-radius:var(--r);font-size:.86rem;font-family:'Inter',sans-serif;background:var(--white);color:var(--black);outline:none;transition:border-color .2s}
.fg input:focus,.fg select:focus,.fg textarea:focus{border-color:var(--cyan)}
.fg textarea{resize:vertical;min-height:88px;line-height:1.55}
.fg-row{display:grid;grid-template-columns:1fr 1fr;gap:.85rem}
.btn-wa{background:var(--green);color:var(--white);padding:.9rem;border:none;border-radius:var(--r);font-size:.88rem;font-weight:600;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;transition:background .2s;font-family:'Inter',sans-serif;margin-top:.25rem}
.btn-wa:hover{background:#1ebe5d}
.form-note{font-size:.7rem;color:var(--muted);text-align:center;margin-top:.35rem}

/* ════ FOOTER ════ */
footer{background:var(--black);border-top:1px solid rgba(255,255,255,.07);padding:3.5rem var(--pad) 2rem}
.foot-inner{max-width:1100px;margin:0 auto}
.foot-top{display:grid;grid-template-columns:1.5fr 1fr 1fr 1fr;gap:3rem;padding-bottom:2.5rem;border-bottom:1px solid rgba(255,255,255,.07);margin-bottom:2rem}
.foot-brand{}
.foot-logo{display:flex;align-items:center;gap:9px;text-decoration:none;margin-bottom:1rem}
.foot-logo-box{width:30px;height:30px;background:var(--cyan);border-radius:4px;display:flex;align-items:center;justify-content:center}
.foot-logo-box svg{width:15px;height:15px;fill:var(--black)}
.foot-logo-name{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:.92rem;color:var(--white)}
.foot-brand-desc{font-size:.78rem;color:rgba(255,255,255,.35);line-height:1.7;max-width:220px;margin-bottom:1.25rem}
.foot-social{display:flex;gap:.6rem}
.social-btn{width:34px;height:34px;border-radius:var(--r);background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.1);display:flex;align-items:center;justify-content:center;text-decoration:none;font-size:.85rem;transition:background .2s,border-color .2s}
.social-btn:hover{background:rgba(255,255,255,.14);border-color:rgba(255,255,255,.25)}
.foot-col h5{font-family:'Space Grotesk',sans-serif;font-size:.72rem;font-weight:600;letter-spacing:.08em;text-transform:uppercase;color:rgba(255,255,255,.3);margin-bottom:1rem}
.foot-col ul{list-style:none;display:flex;flex-direction:column;gap:.55rem}
.foot-col a{font-size:.78rem;color:rgba(255,255,255,.45);text-decoration:none;transition:color .2s}
.foot-col a:hover{color:rgba(255,255,255,.85)}
.foot-col .contact-link{display:flex;align-items:center;gap:7px}
.foot-col .contact-link span{font-size:.85rem}
.foot-col .contact-link small{display:block;font-size:.68rem;color:rgba(255,255,255,.25)}
.foot-bottom{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1rem}
.foot-bottom p{font-size:.72rem;color:rgba(255,255,255,.22)}
.foot-cmyk{display:flex;gap:4px;align-items:center}
.cmyk-dot{width:8px;height:8px;border-radius:50%}

/* ════ FLOAT WA ════ */
.wa-float{position:fixed;bottom:1.5rem;right:1.5rem;z-index:400;width:54px;height:54px;border-radius:50%;background:var(--green);color:var(--white);display:flex;align-items:center;justify-content:center;text-decoration:none;box-shadow:0 4px 20px rgba(37,211,102,.45);transition:transform .2s}
.wa-float:hover{transform:scale(1.1)}

/* ════ OVERLAY/MODAL ════ */
.overlay{
  position:fixed;inset:0;z-index:500;
  background:rgba(0,0,0,.7);backdrop-filter:blur(6px);
  display:none;align-items:flex-end;justify-content:center;
  padding:0;
}
.overlay.open{display:flex}
.sheet{
  background:var(--white);width:100%;max-width:700px;
  border-radius:var(--rL) var(--rL) 0 0;
  max-height:92svh;overflow-y:auto;
  animation:slideUp .3s ease;
}
@keyframes slideUp{from{transform:translateY(60px);opacity:0}to{transform:translateY(0);opacity:1}}
.sheet-handle{width:40px;height:4px;background:var(--gray2);border-radius:2px;margin:1rem auto .5rem}
.sheet-head{padding:1rem 1.5rem 0;display:flex;align-items:center;justify-content:space-between}
.sheet-title{font-family:'Space Grotesk',sans-serif;font-size:1.1rem;font-weight:700;letter-spacing:-.02em}
.sheet-close{background:var(--gray);border:none;cursor:pointer;width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.1rem;transition:background .2s}
.sheet-close:hover{background:var(--gray2)}
.sheet-body{padding:1.25rem 1.5rem 2rem}

/* SERVICES SHEET */
.srv-sheet-grid{display:grid;grid-template-columns:1fr 1fr;gap:.75rem;margin-top:.25rem}
.srv-sheet-item{display:flex;align-items:flex-start;gap:12px;padding:1rem;border:1px solid var(--border);border-radius:var(--r);background:var(--gray);transition:border-color .2s,background .2s}
.srv-sheet-item:hover{background:var(--white);border-color:var(--cyan)}
.srv-sheet-ic{width:40px;height:40px;min-width:40px;background:var(--white);border:1px solid var(--border);border-radius:var(--r);display:flex;align-items:center;justify-content:center;font-size:1.15rem}
.srv-sheet-item h4{font-family:'Space Grotesk',sans-serif;font-size:.85rem;font-weight:600;margin-bottom:.2rem}
.srv-sheet-item p{font-size:.75rem;color:var(--muted);line-height:1.55}
.srv-sheet-cta{margin-top:1.25rem;background:var(--cyan);color:var(--black);border:none;border-radius:var(--r);padding:.85rem;font-size:.88rem;font-weight:600;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;font-family:'Inter',sans-serif;width:100%;transition:background .2s}
.srv-sheet-cta:hover{background:var(--cyan-dk);color:var(--white)}

/* ORCAMENTO SHEET - steps */
.step-dots{display:flex;gap:.5rem;margin-bottom:1.5rem}
.sdot{width:8px;height:8px;border-radius:50%;background:var(--gray2);transition:background .3s,width .3s}
.sdot.active{background:var(--cyan);width:24px;border-radius:4px}
.step-content{display:none}
.step-content.active{display:block}
.orc-options{display:grid;grid-template-columns:1fr 1fr;gap:.65rem;margin-top:.5rem}
.orc-opt{border:1.5px solid var(--border);border-radius:var(--r);padding:1rem;cursor:pointer;transition:border-color .2s,background .2s;text-align:left;background:var(--white);font-family:'Inter',sans-serif}
.orc-opt:hover{border-color:var(--cyan);background:var(--cyan-bg)}
.orc-opt.selected{border-color:var(--cyan);background:var(--cyan-bg)}
.orc-opt-ic{font-size:1.4rem;margin-bottom:.4rem;display:block}
.orc-opt-name{font-family:'Space Grotesk',sans-serif;font-size:.85rem;font-weight:600;display:block;margin-bottom:.15rem}
.orc-opt-desc{font-size:.72rem;color:var(--muted)}
.step-lbl{font-size:.78rem;font-weight:500;color:var(--black);margin-bottom:.4rem;display:block}
.step-fg{display:flex;flex-direction:column;gap:.75rem;margin-top:.5rem}
.step-fg input,.step-fg select,.step-fg textarea{padding:.7rem .9rem;border:1px solid var(--gray2);border-radius:var(--r);font-size:.86rem;font-family:'Inter',sans-serif;background:var(--white);color:var(--black);outline:none;transition:border-color .2s;width:100%}
.step-fg input:focus,.step-fg select:focus,.step-fg textarea:focus{border-color:var(--cyan)}
.step-fg textarea{min-height:80px;resize:vertical}
.step-fg .fgrow{display:grid;grid-template-columns:1fr 1fr;gap:.75rem}
.sheet-nav{display:flex;gap:.75rem;margin-top:1.5rem}
.btn-prev{flex:1;background:var(--gray);border:none;border-radius:var(--r);padding:.82rem;font-size:.86rem;font-weight:500;cursor:pointer;font-family:'Inter',sans-serif;transition:background .2s}
.btn-prev:hover{background:var(--gray2)}
.btn-next{flex:2;background:var(--cyan);color:var(--black);border:none;border-radius:var(--r);padding:.82rem;font-size:.86rem;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;transition:background .2s}
.btn-next:hover{background:var(--cyan-dk);color:var(--white)}
.btn-next.send{background:var(--green);color:var(--white)}
.btn-next.send:hover{background:#1ebe5d}
.orc-confirm{text-align:center;padding:1rem 0}
.orc-confirm .big-ic{font-size:3rem;margin-bottom:.75rem}
.orc-confirm h3{font-family:'Space Grotesk',sans-serif;font-size:1.15rem;font-weight:700;margin-bottom:.4rem}
.orc-confirm p{font-size:.83rem;color:var(--muted);margin-bottom:1.25rem}
.orc-confirm .summary{background:var(--gray);border-radius:var(--r);padding:1rem;text-align:left;margin-bottom:1.25rem}
.orc-confirm .summary-row{display:flex;justify-content:space-between;font-size:.78rem;padding:.3rem 0;border-bottom:1px solid var(--border)}
.orc-confirm .summary-row:last-child{border-bottom:none}
.orc-confirm .summary-row span:first-child{color:var(--muted)}
.orc-confirm .summary-row span:last-child{font-weight:500}

/* SECTION SHEETS */
.proc-sheet-steps{display:flex;flex-direction:column;gap:.75rem;margin-top:.5rem}
.proc-sheet-step{display:flex;gap:1rem;padding:1.1rem;border:1px solid var(--border);border-radius:var(--r);background:var(--gray)}
.pss-num{font-family:'Space Grotesk',sans-serif;font-size:1.4rem;font-weight:700;color:var(--gray2);line-height:1;min-width:32px}
.pss-body h4{font-family:'Space Grotesk',sans-serif;font-size:.88rem;font-weight:600;margin-bottom:.25rem}
.pss-body p{font-size:.78rem;color:var(--muted);line-height:1.6}
.pss-body .pss-note{font-size:.72rem;color:var(--cyan);margin-top:.35rem}

.port-sheet-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:.65rem;margin-top:.5rem}
.port-sheet-card{aspect-ratio:1;border-radius:var(--r);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.4rem;font-family:'Space Grotesk',sans-serif;font-size:.8rem;font-weight:600;cursor:pointer;transition:transform .18s}
.port-sheet-card:hover{transform:scale(1.04)}
.port-sheet-card span{font-size:1.75rem}
.port-sheet-card small{font-size:.65rem;opacity:.6;font-weight:400}

.avaliacao-grid{display:flex;flex-direction:column;gap:.75rem;margin-top:.5rem}
.av-card{background:var(--gray);border-radius:var(--r);padding:1.1rem}
.av-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:.6rem}
.av-stars{color:#F59E0B;font-size:.8rem}
.av-date{font-size:.68rem;color:var(--muted)}
.av-text{font-size:.8rem;color:var(--muted);line-height:1.65;margin-bottom:.75rem}
.av-author{display:flex;align-items:center;gap:8px}
.av-av{width:30px;height:30px;border-radius:50%;background:var(--cyan-bg);color:var(--cyan);display:flex;align-items:center;justify-content:center;font-family:'Space Grotesk',sans-serif;font-size:.65rem;font-weight:700}
.av-name{font-size:.78rem;font-weight:500}
.av-role{font-size:.68rem;color:var(--muted)}
.av-summary{background:var(--cyan-bg);border-radius:var(--r);padding:1rem;display:flex;align-items:center;gap:1rem;margin-bottom:1rem}
.av-score{font-family:'Space Grotesk',sans-serif;font-size:2.5rem;font-weight:700;color:var(--cyan);line-height:1}
.av-score-label{font-size:.72rem;color:var(--muted);margin-top:.15rem}
.av-bars{flex:1}
.av-bar-row{display:flex;align-items:center;gap:.5rem;margin-bottom:.3rem}
.av-bar-row span{font-size:.65rem;color:var(--muted);min-width:8px}
.av-bar{flex:1;height:4px;background:var(--gray2);border-radius:2px;overflow:hidden}
.av-bar-fill{height:100%;background:var(--cyan);border-radius:2px}

/* ════ RESPONSIVE ════ */
@media(max-width:900px){
  .nav-links,.nav-orcamento{display:none}
  .nav-toggle{display:block}
  .srv-grid{grid-template-columns:repeat(2,1fr)}
  .proc-grid{grid-template-columns:repeat(2,1fr)}
  .proc-step:nth-child(2){border-right:none}
  .proc-step:nth-child(3),.proc-step:nth-child(4){border-top:1px solid rgba(255,255,255,.08)}
  .test-grid{grid-template-columns:1fr 1fr}
  .contact-grid{grid-template-columns:1fr}
  .foot-top{grid-template-columns:1fr 1fr;gap:2rem}
  .port-grid{grid-template-columns:1fr 1fr;grid-template-rows:auto}
  .port-card.wide{grid-column:1/-1;aspect-ratio:16/7}
  .port-card.tall{grid-row:auto;aspect-ratio:4/3;grid-column:auto}
  .orc-options{grid-template-columns:1fr 1fr}
  .srv-sheet-grid{grid-template-columns:1fr}
}
@media(max-width:600px){
  .hero h1{font-size:clamp(2.4rem,10vw,3.5rem)}
  .hero-bottom{flex-direction:column;align-items:flex-start}
  .srv-grid,.proc-grid{grid-template-columns:1fr}
  .proc-step{border-right:none!important;border-top:1px solid rgba(255,255,255,.08)!important}
  .proc-step:first-child{border-top:none!important}
  .test-grid{grid-template-columns:1fr}
  .port-grid{grid-template-columns:1fr;grid-template-rows:auto}
  .port-card.wide,.port-card.tall{grid-column:auto;grid-row:auto;aspect-ratio:4/3}
  .fg-row,.fgrow,.step-fg .fgrow{grid-template-columns:1fr}
  .foot-top{grid-template-columns:1fr}
  .cta-inner{flex-direction:column}
  .orc-options{grid-template-columns:1fr}
  .port-sheet-grid{grid-template-columns:repeat(2,1fr)}
  nav{padding:0 1.1rem}
  .sheet{border-radius:var(--rL) var(--rL) 0 0;max-height:88svh}
}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>

<!-- ════ NAV ════ -->
<nav id="mainNav">
  <a href="#" class="logo">
    <div class="logo-box">
      <svg viewBox="0 0 24 24"><path d="M5 3h14a2 2 0 012 2v6H3V5a2 2 0 012-2zM3 13h18v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6zm13 3a1 1 0 100 2 1 1 0 000-2zm-4 0a1 1 0 100 2 1 1 0 000-2z"/></svg>
    </div>
    <div>
      <div class="logo-name">Copynet</div>
      <div class="logo-sub">Gráfica Rápida</div>
    </div>
  </a>

  <ul class="nav-links">
    <li><a href="#servicos" data-section="servicos">Serviços</a></li>
    <li><a href="#processo" data-section="processo">Como funciona</a></li>
    <li><a href="#portfolio" data-section="portfolio">Portfólio</a></li>
    <li><a href="#depoimentos" data-section="depoimentos">Avaliações</a></li>
    <li><a href="#contato" data-section="contato">Contato</a></li>
  </ul>

  <div class="nav-right">
    <button class="nav-orcamento" onclick="openSheet('orcamento')">Pedir orçamento</button>
    <button class="nav-toggle" id="toggle" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<ul class="mob-nav" id="mobNav">
  <li><a href="#servicos" onclick="closeMenu()">Serviços</a></li>
  <li><a href="#processo" onclick="closeMenu()">Como funciona</a></li>
  <li><a href="#portfolio" onclick="closeMenu()">Portfólio</a></li>
  <li><a href="#depoimentos" onclick="closeMenu()">Avaliações</a></li>
  <li><a href="#contato" onclick="closeMenu()">Contato</a></li>
  <li><a href="#" class="mob-cta" onclick="closeMenu();openSheet('orcamento')">Pedir orçamento</a></li>
</ul>

<!-- ════ HERO ════ -->
<section class="hero">
  <div class="cmyk-bar"><span></span><span></span><span></span><span></span></div>
  <div class="hero-inner">
    <div class="hero-tag">Natal, RN · Gráfica Rápida</div>
    <h1>Impressão<br>que faz <em>sua<br>marca</em> aparecer.</h1>
    <div class="hero-bottom">
      <p class="hero-desc">Cartões, banners, panfletos, adesivos e muito mais. Orçamento na hora — sem enrolação.</p>
      <div class="hero-actions">
        <button class="btn-cyan" onclick="openSheet('orcamento')">💬 Orçamento grátis</button>
        <button class="btn-outline-w" onclick="openSheet('servicos')">Ver serviços</button>
      </div>
    </div>
  </div>
</section>

<!-- PILLS -->
<div class="pills">
  <div class="pill">🖨️ Impressão rápida</div>
  <div class="pill">🎨 Arte inclusa</div>
  <div class="pill">📦 Retirada ou entrega</div>
  <div class="pill">✅ Aprovação antes de imprimir</div>
  <div class="pill">⭐ Atendimento 5 estrelas</div>
  <div class="pill">💬 Resposta imediata no WhatsApp</div>
</div>

<!-- ════ SERVICES ════ -->
<section class="sec" id="servicos">
  <div class="sec-inner">
    <div class="srv-header">
      <div>
        <span class="eyebrow">O que fazemos</span>
        <h2>Tudo que você precisa<br>para se destacar</h2>
        <p class="sec-lead">Do mais simples ao mais elaborado — qualidade e agilidade em cada pedido.</p>
      </div>
    </div>
    <div class="srv-grid">
      <div class="srv"><div class="srv-ic">💳</div><h3>Cartão de visita</h3><p>Couchê 300g, laminação fosca ou brilho, verniz localizado. Frente e verso.</p><span class="srv-tag">Mais pedido</span></div>
      <div class="srv"><div class="srv-ic">🏷️</div><h3>Panfleto e folder</h3><p>Couchê 115g a 150g. Ideal para promoções, eventos e divulgação local.</p></div>
      <div class="srv"><div class="srv-ic">🖼️</div><h3>Banner e lona</h3><p>Impressão digital em lona 440g com ilhós. Qualquer tamanho.</p></div>
      <div class="srv"><div class="srv-ic">🔖</div><h3>Adesivo e etiqueta</h3><p>Vinil colorido para produtos, embalagens, brindes e decoração.</p></div>
      <div class="srv"><div class="srv-ic">📋</div><h3>Cardápio</h3><p>Plastificado ou PVC rígido para restaurantes, lanchonetes e bares.</p></div>
      <div class="srv"><div class="srv-ic">📦</div><h3>Embalagem personalizada</h3><p>Caixas e kraft com a identidade visual do seu negócio.</p></div>
      <div class="srv"><div class="srv-ic">🎨</div><h3>Criação de arte</h3><p>Não tem o arquivo? Nossa equipe cria o layout profissional para você.</p><span class="srv-tag">Grátis no 1º pedido</span></div>
      <div class="srv"><div class="srv-ic">📄</div><h3>Cópias e impressões</h3><p>Preto e branco ou colorido, encadernação e plastificação.</p></div>
    </div>
  </div>
</section>

<!-- ════ PROCESS ════ -->
<section class="sec" id="processo">
  <div class="sec-inner">
    <span class="eyebrow">Como funciona</span>
    <h2>Pedir é simples assim</h2>
    <p class="sec-lead">Quatro passos do primeiro contato à entrega.</p>
    <div class="proc-grid">
      <div class="proc-step">
        <div class="proc-n">01</div>
        <div class="proc-dot"></div>
        <h3>Mande uma mensagem</h3>
        <p>Fale pelo WhatsApp dizendo o que você precisa. Respondemos em minutos.</p>
        <p class="proc-detail">Seg–Sex das 08h às 17h30 · Sáb até 12h</p>
      </div>
      <div class="proc-step">
        <div class="proc-n">02</div>
        <div class="proc-dot"></div>
        <h3>Receba o orçamento</h3>
        <p>Prazo, valor e especificações — tudo transparente, sem surpresas.</p>
        <p class="proc-detail">Orçamento gratuito e sem compromisso</p>
      </div>
      <div class="proc-step">
        <div class="proc-n">03</div>
        <div class="proc-dot"></div>
        <h3>Aprove a arte</h3>
        <p>Envie seu arquivo ou peça que criemos. Você aprova antes de imprimir.</p>
        <p class="proc-detail">Revisões até você ficar satisfeito</p>
      </div>
      <div class="proc-step">
        <div class="proc-n">04</div>
        <div class="proc-dot"></div>
        <h3>Receba seu pedido</h3>
        <p>Retire na loja ou solicite entrega. Garantia de qualidade em cada peça.</p>
        <p class="proc-detail">Prazo expresso disponível</p>
      </div>
    </div>
  </div>
</section>

<!-- ════ PORTFOLIO ════ -->
<section class="sec" id="portfolio">
  <div class="sec-inner">
    <div class="port-header">
      <div>
        <span class="eyebrow">Portfólio</span>
        <h2>O que já saiu das<br>nossas máquinas</h2>
        <p class="sec-lead">Uma amostra dos trabalhos que produzimos para nossos clientes.</p>
      </div>
    </div>
    <div class="port-grid">
      <div class="port-card wide pb1" onclick="openSheet('portfolio')">
        <div class="port-badge">Mais pedido</div>
        <div class="port-icon">💳</div>
        <div class="port-info"><div class="port-sub">Alta qualidade</div><div class="port-label">Cartões de visita</div></div>
      </div>
      <div class="port-card tall pb3" onclick="openSheet('portfolio')">
        <div class="port-icon">🖼️</div>
        <div class="port-info"><div class="port-sub">Qualquer tamanho</div><div class="port-label">Banners e lonas</div></div>
      </div>
      <div class="port-card pb2" onclick="openSheet('portfolio')">
        <div class="port-icon">🏷️</div>
        <div class="port-info"><div class="port-sub">Divulgação</div><div class="port-label">Panfletos</div></div>
      </div>
      <div class="port-card pb4" onclick="openSheet('portfolio')">
        <div class="port-icon">🔖</div>
        <div class="port-info"><div class="port-sub">Vinil colorido</div><div class="port-label">Adesivos</div></div>
      </div>
      <div class="port-card pb5" onclick="openSheet('portfolio')">
        <div class="port-icon">📋</div>
        <div class="port-info"><div class="port-sub">Restaurantes e bares</div><div class="port-label">Cardápios</div></div>
      </div>
    </div>
  </div>
</section>

<!-- ════ DEPOIMENTOS ════ -->
<section class="sec" id="depoimentos">
  <div class="sec-inner">
    <span class="eyebrow">Avaliações</span>
    <h2>Quem pediu,<br>recomenda</h2>
    <p class="sec-lead">Clientes reais que confiam na Copynet.</p>
    <div class="test-grid">
      <div class="test-card">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">"Pedi 500 cartões e ficaram perfeitos! Entrega rápida, qualidade excelente e o atendimento foi incrível do começo ao fim."</p>
        <div class="test-author">
          <div class="test-av">MA</div>
          <div>
            <div class="test-name">Maria Aparecida</div>
            <div class="test-role">Salão de beleza · Natal</div>
            <div class="test-verified">✓ Compra verificada</div>
          </div>
        </div>
      </div>
      <div class="test-card">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">"Fiz banners para o restaurante e o resultado superou tudo. Criaram a arte sem custo extra e entregaram antes do prazo."</p>
        <div class="test-author">
          <div class="test-av">RO</div>
          <div>
            <div class="test-name">Roberto Oliveira</div>
            <div class="test-role">Restaurante Sabor do Norte</div>
            <div class="test-verified">✓ Compra verificada</div>
          </div>
        </div>
      </div>
      <div class="test-card">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">"Precisei de panfletos com urgência para um evento e entregaram no mesmo dia! Preço justo e atendimento pelo WhatsApp muito prático."</p>
        <div class="test-author">
          <div class="test-av">JS</div>
          <div>
            <div class="test-name">João Silva</div>
            <div class="test-role">Produtor de eventos</div>
            <div class="test-verified">✓ Compra verificada</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA STRIP -->
<div class="cta-strip">
  <div class="cta-inner">
    <div>
      <h2>Pronto para começar?</h2>
      <p>Orçamento gratuito e sem compromisso. Respondemos na hora.</p>
    </div>
    <button class="btn-black" onclick="openSheet('orcamento')">💬 Pedir orçamento grátis</button>
  </div>
</div>

<!-- ════ CONTATO ════ -->
<section class="sec" id="contato">
  <div class="sec-inner">
    <span class="eyebrow">Contato</span>
    <h2>Fale com a gente</h2>
    <p class="sec-lead">Orçamento em minutos pelo WhatsApp ou preencha o formulário abaixo.</p>
    <div class="contact-grid">
      <div class="contact-aside">
        <h3>Nossas informações</h3>
        <div class="info-list">
          <a href="https://wa.me/5584988627223?text=Olá!%20Vim%20pelo%20site%20e%20quero%20um%20orçamento%20🖨️" target="_blank" class="info-item" style="text-decoration:none;color:inherit">
            <div class="info-ic">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="#25D366"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg>
            </div>
            <div>
              <strong>WhatsApp</strong>
              <span style="color:var(--cyan)">(84) 98862-7223</span>
              <div class="info-desc">Toque para abrir conversa · resposta imediata</div>
            </div>
          </a>
          <div class="info-item">
            <div class="info-ic">📍</div>
            <div>
              <strong>Localização</strong>
              <span>Natal, Rio Grande do Norte</span>
              <div class="info-desc">Atendemos Natal e região · retirada ou entrega</div>
            </div>
          </div>
          <a href="https://instagram.com/copynet.grafica" target="_blank" class="info-item" style="text-decoration:none;color:inherit">
            <div class="info-ic">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="url(#ig)"><defs><linearGradient id="ig" x1="0%" y1="100%" x2="100%" y2="0%"><stop offset="0%" style="stop-color:#f09433"/><stop offset="25%" style="stop-color:#e6683c"/><stop offset="50%" style="stop-color:#dc2743"/><stop offset="75%" style="stop-color:#cc2366"/><stop offset="100%" style="stop-color:#bc1888"/></linearGradient></defs><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
            </div>
            <div>
              <strong>Instagram</strong>
              <span style="color:var(--cyan)">@copynet.grafica</span>
              <div class="info-desc">Veja nossos trabalhos e novidades</div>
            </div>
          </a>
        </div>
        <div class="hours-box">
          <h4>⏰ Horário de atendimento</h4>
          <div class="h-row"><span>Segunda — Sexta</span><span class="hval">08h às 17h30 <span class="open-badge">Aberto</span></span></div>
          <div class="h-row"><span>Sábado</span><span class="hval">08h às 12h</span></div>
          <div class="h-row"><span>Domingo</span><span class="hval closed">Fechado</span></div>
        </div>
      </div>

      <div class="form-wrap">
        <h3>Solicitar orçamento</h3>
        <p>Preencha abaixo e receba o orçamento no seu WhatsApp.</p>
        <div class="form">
          <div class="fg-row">
            <div class="fg"><label>Seu nome</label><input type="text" id="c-nome" placeholder="Ana Lima" autocomplete="name"></div>
            <div class="fg"><label>WhatsApp</label><input type="tel" id="c-tel" placeholder="(84) 9xxxx-xxxx" autocomplete="tel"></div>
          </div>
          <div class="fg">
            <label>Tipo de serviço</label>
            <select id="c-srv">
              <option value="">Selecione...</option>
              <option>Cartão de visita</option><option>Panfleto / folder</option>
              <option>Banner / lona</option><option>Adesivo / etiqueta</option>
              <option>Cardápio</option><option>Embalagem personalizada</option>
              <option>Criação de arte</option><option>Cópias e impressões</option><option>Outro</option>
            </select>
          </div>
          <div class="fg"><label>Detalhes do pedido</label><textarea id="c-det" placeholder="Quantidade, tamanho, prazo, referências..."></textarea></div>
          <button class="btn-wa" onclick="enviarWA('c-nome','c-tel','c-srv','c-det')">
            <svg width="17" height="17" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg>
            Enviar pelo WhatsApp
          </button>
          <p class="form-note">Você será redirecionado para o WhatsApp com a mensagem pronta.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ════ FOOTER ════ -->
<footer>
  <div class="foot-inner">
    <div class="foot-top">
      <div class="foot-brand">
        <a href="#" class="foot-logo">
          <div class="foot-logo-box"><svg viewBox="0 0 24 24" fill="#111"><path d="M5 3h14a2 2 0 012 2v6H3V5a2 2 0 012-2zM3 13h18v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6zm13 3a1 1 0 100 2 1 1 0 000-2zm-4 0a1 1 0 100 2 1 1 0 000-2z"/></svg></div>
          <span class="foot-logo-name">Copynet</span>
        </a>
        <p class="foot-brand-desc">Impressões de qualidade para negócios que querem se destacar em Natal e região.</p>
        <div class="foot-social">
          <a href="https://wa.me/5584988627223" target="_blank" class="social-btn" title="WhatsApp">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="#25D366"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg>
          </a>
          <a href="https://instagram.com/copynet.grafica" target="_blank" class="social-btn" title="Instagram">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="url(#ig2)"><defs><linearGradient id="ig2" x1="0%" y1="100%" x2="100%" y2="0%"><stop offset="0%" style="stop-color:#f09433"/><stop offset="50%" style="stop-color:#dc2743"/><stop offset="100%" style="stop-color:#bc1888"/></linearGradient></defs><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          </a>
          <a href="https://maps.google.com/?q=Natal+RN" target="_blank" class="social-btn" title="Localização">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="var(--cyan)"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
          </a>
        </div>
      </div>

      <div class="foot-col">
        <h5>Serviços</h5>
        <ul>
          <li><a href="#servicos">Cartão de visita</a></li>
          <li><a href="#servicos">Panfleto e folder</a></li>
          <li><a href="#servicos">Banner e lona</a></li>
          <li><a href="#servicos">Adesivos</a></li>
          <li><a href="#servicos">Cardápio</a></li>
          <li><a href="#servicos">Criação de arte</a></li>
        </ul>
      </div>

      <div class="foot-col">
        <h5>Empresa</h5>
        <ul>
          <li><a href="#processo">Como funciona</a></li>
          <li><a href="#portfolio">Portfólio</a></li>
          <li><a href="#depoimentos">Avaliações</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </div>

      <div class="foot-col">
        <h5>Contato direto</h5>
        <ul>
          <li>
            <a href="https://wa.me/5584988627223" target="_blank" class="contact-link">
              <span>📱</span>
              <div><div>(84) 98862-7223</div><small>WhatsApp</small></div>
            </a>
          </li>
          <li>
            <a href="https://instagram.com/copynet.grafica" target="_blank" class="contact-link">
              <span>📸</span>
              <div><div>@copynet.grafica</div><small>Instagram</small></div>
            </a>
          </li>
          <li>
            <a href="https://maps.google.com/?q=Natal+RN" target="_blank" class="contact-link">
              <span>📍</span>
              <div><div>Natal, RN</div><small>Ver no mapa</small></div>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="foot-bottom">
      <p>© 2025 Copynet Gráfica Rápida · Todos os direitos reservados</p>
      <div class="foot-cmyk">
        <div class="cmyk-dot" style="background:#00AEEF"></div>
        <div class="cmyk-dot" style="background:#EC008C"></div>
        <div class="cmyk-dot" style="background:#FFF200"></div>
        <div class="cmyk-dot" style="background:#555"></div>
      </div>
    </div>
  </div>
</footer>

<!-- FLOAT WA -->
<a href="https://wa.me/5584988627223?text=Olá!%20Vim%20pelo%20site%20e%20quero%20um%20orçamento%20🖨️" target="_blank" class="wa-float" title="Falar no WhatsApp">
  <svg width="24" height="24" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg>
</a>

<!-- ════ SHEET: SERVIÇOS ════ -->
<div class="overlay" id="sheet-servicos" onclick="closeSheet('servicos')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title">Nossos serviços</span>
      <button class="sheet-close" onclick="closeSheet('servicos')">✕</button>
    </div>
    <div class="sheet-body">
      <p style="font-size:.82rem;color:var(--muted);margin-bottom:1rem">Toque em um serviço para solicitar orçamento direto.</p>
      <div class="srv-sheet-grid">
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Cartão de visita')"><div class="srv-sheet-ic">💳</div><div><h4>Cartão de visita</h4><p>Couchê 300g, laminação, verniz. Frente e verso.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Panfleto / folder')"><div class="srv-sheet-ic">🏷️</div><div><h4>Panfleto e folder</h4><p>Couchê 115–150g. Promoções e eventos.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Banner / lona')"><div class="srv-sheet-ic">🖼️</div><div><h4>Banner e lona</h4><p>Lona 440g com ilhós. Qualquer tamanho.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Adesivo / etiqueta')"><div class="srv-sheet-ic">🔖</div><div><h4>Adesivo e etiqueta</h4><p>Vinil colorido para produtos e brindes.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Cardápio')"><div class="srv-sheet-ic">📋</div><div><h4>Cardápio</h4><p>Plastificado ou PVC rígido.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Embalagem personalizada')"><div class="srv-sheet-ic">📦</div><div><h4>Embalagem</h4><p>Caixas e kraft personalizados.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Criação de arte')"><div class="srv-sheet-ic">🎨</div><div><h4>Criação de arte</h4><p>Layout profissional incluso no 1º pedido.</p></div></div>
        <div class="srv-sheet-item" onclick="closeSheet('servicos');openSheet('orcamento');selectOrc('Cópias e impressões')"><div class="srv-sheet-ic">📄</div><div><h4>Cópias</h4><p>P&B ou colorido, encadernação.</p></div></div>
      </div>
      <button class="srv-sheet-cta" onclick="closeSheet('servicos');openSheet('orcamento')">💬 Pedir orçamento grátis</button>
    </div>
  </div>
</div>

<!-- ════ SHEET: ORÇAMENTO (3 steps) ════ -->
<div class="overlay" id="sheet-orcamento" onclick="closeSheet('orcamento')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title" id="orc-title">O que você precisa?</span>
      <button class="sheet-close" onclick="closeSheet('orcamento')">✕</button>
    </div>
    <div class="sheet-body">
      <div class="step-dots">
        <div class="sdot active" id="dot-0"></div>
        <div class="sdot" id="dot-1"></div>
        <div class="sdot" id="dot-2"></div>
      </div>

      <!-- Step 1: escolher serviço -->
      <div class="step-content active" id="step-0">
        <div class="orc-options">
          <button class="orc-opt" onclick="selectOrcBtn(this,'Cartão de visita')"><span class="orc-opt-ic">💳</span><span class="orc-opt-name">Cartão de visita</span><span class="orc-opt-desc">Couchê 300g, laminação</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Panfleto / folder')"><span class="orc-opt-ic">🏷️</span><span class="orc-opt-name">Panfleto / folder</span><span class="orc-opt-desc">Couchê 115–150g</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Banner / lona')"><span class="orc-opt-ic">🖼️</span><span class="orc-opt-name">Banner / lona</span><span class="orc-opt-desc">Impressão digital</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Adesivo / etiqueta')"><span class="orc-opt-ic">🔖</span><span class="orc-opt-name">Adesivo / etiqueta</span><span class="orc-opt-desc">Vinil colorido</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Cardápio')"><span class="orc-opt-ic">📋</span><span class="orc-opt-name">Cardápio</span><span class="orc-opt-desc">Plastificado ou PVC</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Embalagem personalizada')"><span class="orc-opt-ic">📦</span><span class="orc-opt-name">Embalagem</span><span class="orc-opt-desc">Caixas e kraft</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Criação de arte')"><span class="orc-opt-ic">🎨</span><span class="orc-opt-name">Criação de arte</span><span class="orc-opt-desc">Layout profissional</span></button>
          <button class="orc-opt" onclick="selectOrcBtn(this,'Outro')"><span class="orc-opt-ic">📄</span><span class="orc-opt-name">Outro</span><span class="orc-opt-desc">Me diga o que precisa</span></button>
        </div>
        <div class="sheet-nav"><button class="btn-next" onclick="nextStep()">Próximo →</button></div>
      </div>

      <!-- Step 2: detalhes -->
      <div class="step-content" id="step-1">
        <div class="step-fg">
          <div class="fgrow">
            <div><label class="step-lbl">Seu nome</label><input type="text" id="o-nome" placeholder="Ana Lima" autocomplete="name"></div>
            <div><label class="step-lbl">WhatsApp</label><input type="tel" id="o-tel" placeholder="(84) 9xxxx-xxxx" autocomplete="tel"></div>
          </div>
          <div>
            <label class="step-lbl">Quantidade</label>
            <select id="o-qtd">
              <option value="">Selecione...</option>
              <option>Até 100 unidades</option><option>100 – 500 unidades</option>
              <option>500 – 1000 unidades</option><option>Acima de 1000</option><option>Não sei ainda</option>
            </select>
          </div>
          <div>
            <label class="step-lbl">Prazo desejado</label>
            <select id="o-prazo">
              <option value="">Selecione...</option>
              <option>Urgente (mesmo dia)</option><option>1–2 dias</option>
              <option>3–5 dias</option><option>Sem pressa</option>
            </select>
          </div>
          <div>
            <label class="step-lbl">Observações (opcional)</label>
            <textarea id="o-obs" placeholder="Cores, tamanho, referências, tem arquivo pronto?..."></textarea>
          </div>
        </div>
        <div class="sheet-nav">
          <button class="btn-prev" onclick="prevStep()">← Voltar</button>
          <button class="btn-next" onclick="nextStep()">Revisar →</button>
        </div>
      </div>

      <!-- Step 3: confirmar -->
      <div class="step-content" id="step-2">
        <div class="orc-confirm">
          <div class="big-ic">🖨️</div>
          <h3>Tudo certo!</h3>
          <p>Revise as informações e envie pelo WhatsApp.</p>
          <div class="summary" id="orc-summary"></div>
          <button class="btn-next send" style="width:100%;margin-top:0" onclick="enviarOrcWA()">
            <svg width="17" height="17" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg>
            Enviar pelo WhatsApp
          </button>
          <button class="btn-prev" style="width:100%;margin-top:.6rem" onclick="prevStep()">← Editar informações</button>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ════ SHEET: PORTFÓLIO ════ -->
<div class="overlay" id="sheet-portfolio" onclick="closeSheet('portfolio')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title">Portfólio</span>
      <button class="sheet-close" onclick="closeSheet('portfolio')">✕</button>
    </div>
    <div class="sheet-body">
      <p style="font-size:.82rem;color:var(--muted);margin-bottom:1rem">Exemplos dos trabalhos que produzimos. Toque para pedir igual.</p>
      <div class="port-sheet-grid">
        <div class="port-sheet-card pb1" style="color:white" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Cartão de visita')"><span>💳</span>Cartões<small>300g laminado</small></div>
        <div class="port-sheet-card pb2" style="color:white" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Panfleto / folder')"><span>🏷️</span>Panfletos<small>Couchê 150g</small></div>
        <div class="port-sheet-card pb3" style="color:white" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Banner / lona')"><span>🖼️</span>Banners<small>Lona 440g</small></div>
        <div class="port-sheet-card pb4" style="color:#111" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Adesivo / etiqueta')"><span>🔖</span>Adesivos<small>Vinil colorido</small></div>
        <div class="port-sheet-card pb5" style="color:white" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Cardápio')"><span>📋</span>Cardápios<small>Plastificado</small></div>
        <div class="port-sheet-card" style="background:var(--cyan-bg);color:var(--cyan)" onclick="closeSheet('portfolio');openSheet('orcamento');selectOrc('Criação de arte')"><span>🎨</span>Arte<small>Design incluso</small></div>
      </div>
      <button class="srv-sheet-cta" style="margin-top:1.25rem" onclick="closeSheet('portfolio');openSheet('orcamento')">💬 Quero fazer igual</button>
    </div>
  </div>
</div>

<!-- ════ SHEET: AVALIAÇÕES ════ -->
<div class="overlay" id="sheet-depoimentos" onclick="closeSheet('depoimentos')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title">Avaliações dos clientes</span>
      <button class="sheet-close" onclick="closeSheet('depoimentos')">✕</button>
    </div>
    <div class="sheet-body">
      <div class="av-summary">
        <div><div class="av-score">5.0</div><div class="av-score-label">de 5 estrelas</div></div>
        <div class="av-bars">
          <div class="av-bar-row"><span>5</span><div class="av-bar"><div class="av-bar-fill" style="width:95%"></div></div></div>
          <div class="av-bar-row"><span>4</span><div class="av-bar"><div class="av-bar-fill" style="width:5%"></div></div></div>
          <div class="av-bar-row"><span>3</span><div class="av-bar"><div class="av-bar-fill" style="width:0%"></div></div></div>
          <div class="av-bar-row"><span>2</span><div class="av-bar"><div class="av-bar-fill" style="width:0%"></div></div></div>
          <div class="av-bar-row"><span>1</span><div class="av-bar"><div class="av-bar-fill" style="width:0%"></div></div></div>
        </div>
      </div>
      <div class="avaliacao-grid">
        <div class="av-card"><div class="av-header"><div class="av-stars">★★★★★</div><span class="av-date">Jun 2025</span></div><p class="av-text">"Pedi 500 cartões e ficaram perfeitos! Entrega rápida, qualidade excelente e o atendimento foi incrível do começo ao fim."</p><div class="av-author"><div class="av-av">MA</div><div><div class="av-name">Maria Aparecida</div><div class="av-role">Salão de beleza · Natal</div></div></div></div>
        <div class="av-card"><div class="av-header"><div class="av-stars">★★★★★</div><span class="av-date">Mai 2025</span></div><p class="av-text">"Fiz banners para o restaurante e o resultado superou tudo. Criaram a arte sem custo extra e entregaram antes do prazo."</p><div class="av-author"><div class="av-av">RO</div><div><div class="av-name">Roberto Oliveira</div><div class="av-role">Restaurante · Natal</div></div></div></div>
        <div class="av-card"><div class="av-header"><div class="av-stars">★★★★★</div><span class="av-date">Abr 2025</span></div><p class="av-text">"Precisei de panfletos com urgência e entregaram no mesmo dia! Preço justo e WhatsApp muito prático."</p><div class="av-author"><div class="av-av">JS</div><div><div class="av-name">João Silva</div><div class="av-role">Produtor de eventos</div></div></div></div>
        <div class="av-card"><div class="av-header"><div class="av-stars">★★★★★</div><span class="av-date">Mar 2025</span></div><p class="av-text">"Minha loja nunca teve um material tão profissional. As embalagens ficaram lindas e o atendimento foi excelente."</p><div class="av-author"><div class="av-av">CF</div><div><div class="av-name">Carla Freitas</div><div class="av-role">Loja de roupas · Natal</div></div></div></div>
      </div>
      <button class="srv-sheet-cta" style="margin-top:1.25rem" onclick="closeSheet('depoimentos');openSheet('orcamento')">💬 Quero meu orçamento</button>
    </div>
  </div>
</div>

<!-- ════ SHEET: COMO FUNCIONA ════ -->
<div class="overlay" id="sheet-processo" onclick="closeSheet('processo')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title">Como funciona</span>
      <button class="sheet-close" onclick="closeSheet('processo')">✕</button>
    </div>
    <div class="sheet-body">
      <p style="font-size:.82rem;color:var(--muted);margin-bottom:1rem">Simples, rápido e transparente — do contato à entrega.</p>
      <div class="proc-sheet-steps">
        <div class="proc-sheet-step"><div class="pss-num">01</div><div class="pss-body"><h4>Mande uma mensagem</h4><p>Entre em contato pelo WhatsApp ou pelo formulário do site dizendo o que você precisa.</p><p class="pss-note">⚡ Respondemos em minutos</p></div></div>
        <div class="proc-sheet-step"><div class="pss-num">02</div><div class="pss-body"><h4>Receba o orçamento</h4><p>Enviamos o valor, prazo e especificações completas. Tudo transparente, sem surpresas.</p><p class="pss-note">✅ Orçamento grátis e sem compromisso</p></div></div>
        <div class="proc-sheet-step"><div class="pss-num">03</div><div class="pss-body"><h4>Aprove a arte</h4><p>Envie seu arquivo ou deixe que a gente crie. Você aprova a arte antes de qualquer impressão.</p><p class="pss-note">🎨 Revisões até ficar perfeito</p></div></div>
        <div class="proc-sheet-step"><div class="pss-num">04</div><div class="pss-body"><h4>Receba seu pedido</h4><p>Retire na loja em Natal ou solicite entrega. Garantia de qualidade em cada peça.</p><p class="pss-note">🚀 Prazo expresso disponível</p></div></div>
      </div>
      <button class="srv-sheet-cta" style="margin-top:1.25rem" onclick="closeSheet('processo');openSheet('orcamento')">💬 Começar agora</button>
    </div>
  </div>
</div>

<!-- ════ SHEET: CONTATO ════ -->
<div class="overlay" id="sheet-contato" onclick="closeSheet('contato')">
  <div class="sheet" onclick="event.stopPropagation()">
    <div class="sheet-handle"></div>
    <div class="sheet-head">
      <span class="sheet-title">Fale com a gente</span>
      <button class="sheet-close" onclick="closeSheet('contato')">✕</button>
    </div>
    <div class="sheet-body">
      <div style="display:flex;flex-direction:column;gap:.75rem;margin-bottom:1.25rem">
        <a href="https://wa.me/5584988627223?text=Olá!%20Vim%20pelo%20site%20e%20quero%20um%20orçamento%20🖨️" target="_blank" class="info-item" style="text-decoration:none;color:inherit">
          <div class="info-ic"><svg width="18" height="18" viewBox="0 0 24 24" fill="#25D366"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.561 4.14 1.533 5.877L.057 23.925l6.224-1.451A11.953 11.953 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.002-1.373l-.36-.212-3.693.862.878-3.593-.234-.369A9.818 9.818 0 012.182 12c0-5.421 4.397-9.818 9.818-9.818 5.421 0 9.818 4.397 9.818 9.818 0 5.421-4.397 9.818-9.818 9.818z"/></svg></div>
          <div><strong>WhatsApp</strong><span style="color:var(--cyan)">(84) 98862-7223</span><div class="info-desc">Toque para abrir · resposta imediata</div></div>
        </a>
        <a href="https://instagram.com/copynet.grafica" target="_blank" class="info-item" style="text-decoration:none;color:inherit">
          <div class="info-ic">📸</div>
          <div><strong>Instagram</strong><span style="color:var(--cyan)">@copynet.grafica</span><div class="info-desc">Veja nossos trabalhos</div></div>
        </a>
        <a href="https://maps.google.com/?q=Natal+RN" target="_blank" class="info-item" style="text-decoration:none;color:inherit">
          <div class="info-ic">📍</div>
          <div><strong>Localização</strong><span>Natal, Rio Grande do Norte</span><div class="info-desc">Retirada ou entrega</div></div>
        </a>
      </div>
      <button class="srv-sheet-cta" onclick="closeSheet('contato');openSheet('orcamento')">💬 Pedir orçamento grátis</button>
    </div>
  </div>
</div>

<script>
/* ── NAV TOGGLE ── */
const toggle=document.getElementById('toggle');
const mobNav=document.getElementById('mobNav');
toggle.addEventListener('click',()=>{
  mobNav.classList.toggle('open');
  const s=toggle.querySelectorAll('span');
  const open=mobNav.classList.contains('open');
  s[0].style.transform=open?'rotate(45deg) translate(5px,5px)':'';
  s[1].style.opacity=open?'0':'';
  s[2].style.transform=open?'rotate(-45deg) translate(5px,-5px)':'';
});
function closeMenu(){mobNav.classList.remove('open');toggle.querySelectorAll('span').forEach(s=>{s.style.transform='';s.style.opacity='';})}

/* ── ACTIVE NAV ── */
const sections=['servicos','processo','portfolio','depoimentos','contato'];
const navLinks=document.querySelectorAll('.nav-links a[data-section]');
const obs=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){navLinks.forEach(a=>a.classList.remove('active'));const a=document.querySelector(`.nav-links a[data-section="${e.target.id}"]`);if(a)a.classList.add('active')}})},{threshold:.4});
sections.forEach(id=>{const el=document.getElementById(id);if(el)obs.observe(el)});

/* ── SHEETS ── */
function openSheet(id){document.getElementById('sheet-'+id).classList.add('open');document.body.style.overflow='hidden'}
function closeSheet(id){document.getElementById('sheet-'+id).classList.remove('open');document.body.style.overflow=''}

/* ── ORÇAMENTO STEPS ── */
let currentStep=0;
let selectedService='';
function updateDots(){for(let i=0;i<3;i++){const d=document.getElementById('dot-'+i);d.classList.toggle('active',i<=currentStep)}}
function showStep(n){document.querySelectorAll('.step-content').forEach((s,i)=>s.classList.toggle('active',i===n));const titles=['O que você precisa?','Seus dados','Confirme o pedido'];document.getElementById('orc-title').textContent=titles[n];currentStep=n;updateDots()}
function nextStep(){
  if(currentStep===0){if(!selectedService){alert('Selecione um serviço.');return;}showStep(1);}
  else if(currentStep===1){
    const nome=document.getElementById('o-nome').value.trim();
    if(!nome){alert('Informe seu nome.');return;}
    buildSummary();showStep(2);
  }
}
function prevStep(){if(currentStep>0)showStep(currentStep-1)}
function selectOrcBtn(el,srv){document.querySelectorAll('.orc-opt').forEach(b=>b.classList.remove('selected'));el.classList.add('selected');selectedService=srv}
function selectOrc(srv){selectedService=srv;document.querySelectorAll('.orc-opt').forEach(b=>{b.classList.toggle('selected',b.querySelector('.orc-opt-name')&&b.querySelector('.orc-opt-name').textContent===srv)})}
function buildSummary(){
  const fields=[['Serviço',selectedService],['Nome',document.getElementById('o-nome').value||'—'],['WhatsApp',document.getElementById('o-tel').value||'—'],['Quantidade',document.getElementById('o-qtd').value||'—'],['Prazo',document.getElementById('o-prazo').value||'—'],['Obs.',document.getElementById('o-obs').value||'—']];
  document.getElementById('orc-summary').innerHTML=fields.map(([k,v])=>`<div class="summary-row"><span>${k}</span><span>${v}</span></div>`).join('');
}
function enviarOrcWA(){
  const nome=document.getElementById('o-nome').value.trim();
  const tel=document.getElementById('o-tel').value.trim();
  const qtd=document.getElementById('o-qtd').value;
  const prazo=document.getElementById('o-prazo').value;
  const obs=document.getElementById('o-obs').value.trim();
  let t=`Olá! Vim pelo site da Copynet e gostaria de um orçamento.\n\n`;
  t+=`*Serviço:* ${selectedService}\n`;
  t+=`*Nome:* ${nome}\n`;
  if(tel)t+=`*WhatsApp:* ${tel}\n`;
  if(qtd)t+=`*Quantidade:* ${qtd}\n`;
  if(prazo)t+=`*Prazo:* ${prazo}\n`;
  if(obs)t+=`*Observações:* ${obs}`;
  window.open('https://wa.me/5584988627223?text='+encodeURIComponent(t),'_blank');
  closeSheet('orcamento');
  showStep(0);selectedService='';document.querySelectorAll('.orc-opt').forEach(b=>b.classList.remove('selected'));
}

/* ── CONTATO FORM ── */
function enviarWA(nId,tId,sId,dId){
  const nome=document.getElementById(nId).value.trim();
  const tel=document.getElementById(tId).value.trim();
  const srv=document.getElementById(sId).value;
  const det=document.getElementById(dId).value.trim();
  if(!nome){alert('Informe seu nome.');return;}
  let t=`Olá! Vim pelo site da Copynet e gostaria de um orçamento.\n\n*Nome:* ${nome}\n`;
  if(tel)t+=`*WhatsApp:* ${tel}\n`;
  if(srv)t+=`*Serviço:* ${srv}\n`;
  if(det)t+=`*Detalhes:* ${det}`;
  window.open('https://wa.me/5584988627223?text='+encodeURIComponent(t),'_blank');
}

/* ── CLOSE ON ESC ── */
document.addEventListener('keydown',e=>{if(e.key==='Escape'){['servicos','orcamento','portfolio','depoimentos','processo','contato'].forEach(id=>{const el=document.getElementById('sheet-'+id);if(el&&el.classList.contains('open'))closeSheet(id)})}});
</script>
</body>
</html>
