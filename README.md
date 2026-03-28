<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Asia Athumani Mtonga</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,600;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
–rose: #C2185B;
–blush: #F48FB1;
–mauve: #6A1B4D;
–nude: #FDF6F0;
–charcoal: #1C1C1E;
–glass: rgba(255,255,255,0.06);
–glass-border: rgba(255,255,255,0.1);
}

body {
min-height: 100vh;
background: var(–charcoal);
font-family: ‘Jost’, sans-serif;
display: flex;
justify-content: center;
align-items: flex-start;
padding: 48px 18px 64px;
overflow-x: hidden;
position: relative;
}

/* Subtle background gradient */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background:
radial-gradient(ellipse 60% 50% at 15% 10%, rgba(194,24,91,0.18) 0%, transparent 70%),
radial-gradient(ellipse 50% 60% at 90% 85%, rgba(106,27,77,0.22) 0%, transparent 70%),
radial-gradient(ellipse 40% 40% at 55% 50%, rgba(244,143,177,0.06) 0%, transparent 70%);
z-index: 0;
pointer-events: none;
}

/* Thin decorative line accent */
body::after {
content: ‘’;
position: fixed;
top: 0; left: 50%; transform: translateX(-50%);
width: 1px; height: 100px;
background: linear-gradient(to bottom, transparent, var(–rose), transparent);
z-index: 0;
opacity: 0.4;
}

.container {
position: relative;
z-index: 1;
width: 100%;
max-width: 400px;
display: flex;
flex-direction: column;
align-items: center;
}

/* ── PHOTO ── */
.photo-wrap {
margin-bottom: 22px;
animation: popIn 0.8s cubic-bezier(.34,1.4,.64,1) both;
position: relative;
}

.photo-wrap::after {
content: ‘’;
position: absolute;
inset: -6px;
border-radius: 50%;
border: 1px solid rgba(194,24,91,0.35);
animation: pulseRing 3s ease-in-out infinite;
}

@keyframes pulseRing {
0%, 100% { transform: scale(1); opacity: 0.6; }
50%       { transform: scale(1.05); opacity: 0.2; }
}

@keyframes popIn {
from { opacity:0; transform: scale(0.75) translateY(10px); }
to   { opacity:1; transform: scale(1) translateY(0); }
}

.photo-ring {
width: 108px; height: 108px;
border-radius: 50%;
padding: 2.5px;
background: linear-gradient(135deg, var(–rose), var(–blush), var(–mauve));
}

.photo-inner {
width: 100%; height: 100%;
border-radius: 50%;
background: linear-gradient(145deg, #2a1020, #1C1C1E);
display: flex;
align-items: center;
justify-content: center;

```
overflow: hidden;
border: 2.5px solid var(--charcoal);
```

}

/* ── NAME ── */
.name {
font-family: ‘Cormorant Garamond’, serif;
font-size: 2rem;
font-weight: 600;
color: var(–nude);
text-align: center;
letter-spacing: 0.5px;
line-height: 1.1;
margin-bottom: 4px;
animation: fadeUp 0.6s 0.15s both;
}

.name em {
font-style: italic;
color: var(–blush);
font-weight: 400;
}

.tagline {
font-size: 0.68rem;
color: rgba(244,143,177,0.7);
text-align: center;
letter-spacing: 3px;
text-transform: uppercase;
font-weight: 500;
margin-bottom: 20px;
animation: fadeUp 0.6s 0.25s both;
}

/* ── DIVIDER ── */
.divider {
display: flex;
align-items: center;
gap: 10px;
width: 80%;
margin-bottom: 20px;
animation: fadeUp 0.5s 0.3s both;
}
.divider::before, .divider::after {
content: ‘’;
flex: 1;
height: 1px;
background: linear-gradient(to right, transparent, rgba(194,24,91,0.4));
}
.divider::after {
background: linear-gradient(to left, transparent, rgba(194,24,91,0.4));
}
.divider-dot {
width: 4px; height: 4px;
border-radius: 50%;
background: var(–rose);
opacity: 0.7;
}

/* ── ABOUT ── */
.about {
background: var(–glass);
border: 1px solid var(–glass-border);
border-radius: 14px;
padding: 18px 22px;
text-align: center;
color: rgba(253,246,240,0.65);
font-size: 0.85rem;
line-height: 1.7;
margin-bottom: 28px;
width: 100%;
animation: fadeUp 0.6s 0.4s both;
backdrop-filter: blur(12px);
-webkit-backdrop-filter: blur(12px);
}

.about strong {
color: var(–nude);
font-weight: 600;
}

/* ── PILLS (roles) ── */
.pills {
display: flex;
flex-wrap: wrap;
gap: 7px;
justify-content: center;
margin-bottom: 28px;
animation: fadeUp 0.6s 0.5s both;
}

.pill {
padding: 5px 13px;
border-radius: 100px;
font-size: 0.7rem;
letter-spacing: 0.5px;
font-weight: 500;
border: 1px solid;
}
.pill-rose   { color: var(–blush); border-color: rgba(194,24,91,0.4); background: rgba(194,24,91,0.1); }
.pill-mauve  { color: #CE93D8; border-color: rgba(106,27,77,0.5); background: rgba(106,27,77,0.15); }
.pill-nude   { color: rgba(253,246,240,0.6); border-color: rgba(253,246,240,0.15); background: rgba(253,246,240,0.05); }

/* ── LINKS ── */
.links {
width: 100%;
display: flex;
flex-direction: column;
gap: 10px;
}

.link-btn {
display: flex;
align-items: center;
gap: 14px;
width: 100%;
padding: 15px 18px;
border-radius: 14px;
text-decoration: none;
border: 1px solid var(–glass-border);
backdrop-filter: blur(12px);
-webkit-backdrop-filter: blur(12px);
transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease, background 0.22s ease;
animation: fadeUp 0.5s both;
position: relative;
overflow: hidden;
background: var(–glass);
}

.link-btn:hover {
transform: translateY(-2px);
border-color: rgba(194,24,91,0.4);
box-shadow: 0 8px 30px rgba(194,24,91,0.15);
background: rgba(194,24,91,0.08);
}
.link-btn:active { transform: scale(0.985); }

.btn-linkedin  { animation-delay: 0.55s; }
.btn-hgf       { animation-delay: 0.63s; }
.btn-insta     { animation-delay: 0.71s; }
.btn-tech4dev  { animation-delay: 0.79s; }
.btn-email     { animation-delay: 0.87s; }

.icon {
width: 40px; height: 40px;
border-radius: 10px;
display: flex;
align-items: center;
justify-content: center;
font-size: 18px;
flex-shrink: 0;
background: rgba(194,24,91,0.12);
border: 1px solid rgba(194,24,91,0.2);
}

.btn-linkedin .icon  { background: rgba(10,102,194,0.15); border-color: rgba(10,102,194,0.25); }
.btn-hgf .icon       { background: rgba(194,24,91,0.15); border-color: rgba(194,24,91,0.3); }
.btn-insta .icon     { background: rgba(244,143,177,0.12); border-color: rgba(244,143,177,0.25); }
.btn-tech4dev .icon  { background: rgba(106,27,77,0.2); border-color: rgba(106,27,77,0.35); }
.btn-email .icon     { background: rgba(253,246,240,0.07); border-color: rgba(253,246,240,0.12); }

.btn-text { flex: 1; }

.btn-title {
display: block;
color: var(–nude);
font-weight: 500;
font-size: 0.9rem;
letter-spacing: 0.2px;
}
.btn-sub {
display: block;
color: rgba(253,246,240,0.4);
font-size: 0.72rem;
margin-top: 2px;
font-weight: 300;
}

.arrow {
color: rgba(253,246,240,0.25);
font-size: 16px;
transition: transform 0.2s, color 0.2s;
flex-shrink: 0;
}
.link-btn:hover .arrow {
transform: translateX(3px);
color: var(–blush);
}

/* ── FOOTER ── */
.footer {
margin-top: 40px;
text-align: center;
animation: fadeUp 0.5s 1.1s both;
}
.footer-name {
font-family: ‘Cormorant Garamond’, serif;
font-style: italic;
color: rgba(244,143,177,0.4);
font-size: 0.85rem;
letter-spacing: 1px;
}
.footer-year {
display: block;
color: rgba(253,246,240,0.15);
font-size: 0.65rem;
letter-spacing: 2px;
text-transform: uppercase;
margin-top: 4px;
}

@keyframes fadeUp {
from { opacity:0; transform: translateY(14px); }
to   { opacity:1; transform: translateY(0); }
}
</style>

</head>
<body>

<!-- Floating dots decoration -->

<div class="dot" style="width:6px;height:6px;background:var(--pink);left:10%;animation-duration:12s;animation-delay:-3s;"></div>
<div class="dot" style="width:4px;height:4px;background:var(--gold);left:25%;animation-duration:9s;animation-delay:-6s;"></div>
<div class="dot" style="width:8px;height:8px;background:var(--purple);left:70%;animation-duration:15s;animation-delay:-1s;"></div>
<div class="dot" style="width:5px;height:5px;background:var(--pink);left:85%;animation-duration:11s;animation-delay:-8s;"></div>
<div class="dot" style="width:3px;height:3px;background:var(--gold);left:50%;animation-duration:13s;animation-delay:-4s;"></div>

<div class="container">

  <!-- Photo -->

  <div class="photo-wrap">
    <div class="photo-ring">
      <div class="photo-inner">
        <img src="data:image/jpeg;base64,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" style="width:100%;height:100%;object-fit:cover;object-position:center top;" />
      </div>
    </div>
  </div>

  <!-- Name -->

  <h1 class="name">Asia <em>Athumani</em> Mtonga</h1>
  <p class="tagline">Engineer · Changemaker · Founder</p>

  <div class="divider"><div class="divider-dot"></div></div>

  <!-- Role Pills -->

  <div class="pills">
    <span class="pill pill-rose">UNDP Youth Advisory Panel</span>
    <span class="pill pill-mauve">EE Student @ DIT</span>
    <span class="pill pill-rose">Founder & COO · HGF</span>
    <span class="pill pill-nude">Tech4Dev Volunteer</span>
    <span class="pill pill-mauve">TGEE Bootcamp Mentor 2026</span>
    <span class="pill pill-nude">Millennium Fellow 2025</span>
  </div>

  <!-- About -->

  <div class="about">
    Electrical Engineering student at DIT and <strong>UNDP Youth Advisory Panel</strong> member driving youth-led change across Tanzania. Founder & COO of <strong>Heartful Giving Foundation</strong> — supporting orphans and vulnerable children in Dar es Salaam, Morogoro, Mbeya & Tanga. <strong>Tech4Dev</strong> volunteer and proud mentor at the <strong>TGEE IT Boot Camp 2026</strong>. 🇹🇿
  </div>

  <!-- Links -->

  <div class="links">

```
<a href="https://linkedin.com/in/asia-mtonga" target="_blank" class="link-btn btn-linkedin">
  <div class="icon">💼</div>
  <div class="btn-text">
    <span class="btn-title">LinkedIn</span>
    <span class="btn-sub">Professional journey & milestones</span>
  </div>
  <span class="arrow">›</span>
</a>

<a href="https://instagram.com/heartful_giving_foundation" target="_blank" class="link-btn btn-hgf">
  <div class="icon">💗</div>
  <div class="btn-text">
    <span class="btn-title">Heartful Giving Foundation</span>
    <span class="btn-sub">@heartful_giving_foundation</span>
  </div>
  <span class="arrow">›</span>
</a>

<a href="https://instagram.com/asia_mtonga" target="_blank" class="link-btn btn-insta">
  <div class="icon">✨</div>
  <div class="btn-text">
    <span class="btn-title">Instagram</span>
    <span class="btn-sub">@asia_mtonga</span>
  </div>
  <span class="arrow">›</span>
</a>

<a href="https://tech4dev.com" target="_blank" class="link-btn btn-tech4dev">
  <div class="icon">💻</div>
  <div class="btn-text">
    <span class="btn-title">Tech4Dev</span>
    <span class="btn-sub">Tech Girls Drive Advocacy 2026</span>
  </div>
  <span class="arrow">›</span>
</a>

<a href="/cdn-cgi/l/email-protection#92f3e1fbf3ffe6fdfcf5f3d2f5fff3fbfebcf1fdff" class="link-btn btn-email">
  <div class="icon">📩</div>
  <div class="btn-text">
    <span class="btn-title">Get in Touch</span>
    <span class="btn-sub"><span class="__cf_email__" data-cfemail="93f2e0faf2fee7fcfdf4f2d3f4fef2faffbdf0fcfe">[email&#160;protected]</span></span>
  </div>
  <span class="arrow">›</span>
</a>
```

  </div>

  <div class="footer">
    <span class="footer-na
