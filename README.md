
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ILHA Carbon × Cauvery Calling — A Proposal for Anand Ethirajalu</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --soil:    #3D2B1F;
    --earth:   #6B4C35;
    --clay:    #A0714F;
    --sand:    #D4B896;
    --cream:   #F5EEE4;
    --moss:    #4A6741;
    --leaf:    #7A9E6E;
    --mist:    #C8D8C4;
    --river:   #4A7B9D;
    --sky:     #D6E8F2;
    --gold:    #C4933F;
    --warm:    #E8D5B7;
  }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--soil);
    overflow-x: hidden;
  }
  /* ── COVER ── */
  .cover {
    min-height: 100vh;
    background: var(--soil);
    display: grid;
    grid-template-rows: 1fr auto;
    position: relative;
    overflow: hidden;
  }
  .cover-texture {
    position: absolute; inset: 0;
    background-image:
      radial-gradient(ellipse 80% 60% at 20% 80%, rgba(74,103,65,0.25) 0%, transparent 60%),
      radial-gradient(ellipse 60% 80% at 80% 20%, rgba(74,123,157,0.15) 0%, transparent 50%),
      radial-gradient(ellipse 40% 40% at 50% 50%, rgba(196,147,63,0.08) 0%, transparent 60%);
  }
  /* Subtle soil-layer lines */
  .cover-texture::after {
    content: '';
    position: absolute; inset: 0;
    background-image:
      repeating-linear-gradient(
        0deg,
        transparent,
        transparent 120px,
        rgba(212, 184, 150, 0.04) 120px,
        rgba(212, 184, 150, 0.04) 121px
      );
  }
  .cover-inner {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 8vw 10vw;
    position: relative;
    z-index: 1;
  }
  .cover-eyebrow {
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: .18em;
    text-transform: uppercase;
    color: var(--sand);
    opacity: .7;
    margin-bottom: 2rem;
    display: flex;
    align-items: center;
    gap: 14px;
  }
  .cover-eyebrow::before {
    content: '';
    display: block;
    width: 32px;
    height: 1px;
    background: var(--sand);
    opacity: .5;
  }
  .cover-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 6vw, 5.2rem);
    font-weight: 400;
    line-height: 1.1;
    color: var(--cream);
    max-width: 760px;
    margin-bottom: 1.8rem;
  }
  .cover-title em {
    font-style: italic;
    color: var(--sand);
  }
  .cover-sub {
    font-size: 16px;
    font-weight: 300;
    color: var(--sand);
    opacity: .75;
    max-width: 480px;
    line-height: 1.7;
    margin-bottom: 3.5rem;
  }
  .cover-divider {
    width: 48px;
    height: 2px;
    background: var(--gold);
    margin-bottom: 2rem;
  }
  .cover-meta {
    display: flex;
    gap: 3rem;
  }
  .cover-meta-item { }
  .cover-meta-label {
    font-size: 10px;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--sand);
    opacity: .5;
    margin-bottom: 4px;
  }
  .cover-meta-val {
    font-size: 13px;
    color: var(--sand);
    opacity: .85;
  }
  .cover-footer {
    padding: 2rem 10vw;
    border-top: 1px solid rgba(212,184,150,.12);
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    z-index: 1;
  }
  .cover-footer-brand {
    font-family: 'Playfair Display', serif;
    font-size: 15px;
    color: var(--sand);
    opacity: .6;
    letter-spacing: .04em;
  }
  .cover-scroll {
    font-size: 11px;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--sand);
    opacity: .4;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .cover-scroll::after {
    content: '↓';
    animation: bob 2s ease-in-out infinite;
  }
  @keyframes bob {
    0%,100% { transform: translateY(0); }
    50%      { transform: translateY(4px); }
  }
  /* ── SECTIONS ── */
  section {
    padding: 7vw 10vw;
    position: relative;
  }
  section.alt { background: var(--soil); color: var(--cream); }
  section.warm { background: var(--warm); }
  section.moss-bg { background: #2D3D29; color: var(--cream); }
  section.river-bg { background: #1E3345; color: var(--cream); }
  .section-label {
    font-size: 10px;
    letter-spacing: .18em;
    text-transform: uppercase;
    color: var(--clay);
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::before {
    content: '';
    display: block;
    width: 24px;
    height: 1px;
    background: var(--clay);
  }
  section.alt .section-label,
  section.moss-bg .section-label,
  section.river-bg .section-label {
    color: var(--sand);
    opacity: .6;
  }
  section.alt .section-label::before,
  section.moss-bg .section-label::before,
  section.river-bg .section-label::before {
    background: var(--sand);
    opacity: .4;
  }
  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 400;
    line-height: 1.2;
    margin-bottom: 1.5rem;
    max-width: 720px;
  }
  h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.35rem;
    font-weight: 400;
    margin-bottom: .75rem;
  }
  p {
    font-size: 15px;
    line-height: 1.8;
    max-width: 660px;
    font-weight: 300;
    margin-bottom: 1.2rem;
    opacity: .9;
  }
  p strong { font-weight: 500; opacity: 1; }
  /* ── PULL QUOTE ── */
  .pull-quote {
    border-left: 3px solid var(--gold);
    padding: 1.5rem 2rem;
    margin: 2.5rem 0;
    background: rgba(196,147,63,.08);
    border-radius: 0 8px 8px 0;
    max-width: 680px;
  }
  .pull-quote p {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.1rem, 2vw, 1.4rem);
    font-style: italic;
    font-weight: 400;
    line-height: 1.6;
    margin: 0;
    color: var(--soil);
    opacity: 1;
  }
  .pull-quote .attr {
    font-family: 'DM Sans', sans-serif;
    font-size: 12px;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--clay);
    margin-top: .75rem;
    font-weight: 500;
    font-style: normal;
  }
  section.alt .pull-quote { background: rgba(196,147,63,.12); }
  section.alt .pull-quote p { color: var(--cream); }
  section.alt .pull-quote .attr { color: var(--sand); }
  section.moss-bg .pull-quote { background: rgba(196,147,63,.12); }
  section.moss-bg .pull-quote p { color: var(--cream); }
  section.moss-bg .pull-quote .attr { color: var(--mist); }
  /* ── STAT STRIP ── */
  .stat-strip {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1px;
    background: rgba(0,0,0,.1);
    border-radius: 12px;
    overflow: hidden;
    margin: 2.5rem 0;
  }
  .stat-cell {
    background: var(--cream);
    padding: 1.75rem 1.5rem;
  }
  section.alt .stat-cell,
  section.moss-bg .stat-cell {
    background: rgba(255,255,255,.06);
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.8rem);
    font-weight: 600;
    color: var(--moss);
    line-height: 1;
    margin-bottom: .4rem;
  }
  section.alt .stat-num,
  section.moss-bg .stat-num { color: var(--leaf); }
  section.river-bg .stat-num { color: var(--sky); }
  .stat-label {
    font-size: 12px;
    font-weight: 400;
    opacity: .6;
    line-height: 1.4;
  }
  /* ── TWO COLUMN ── */
  .two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }
  @media (max-width: 700px) { .two-col { grid-template-columns: 1fr; gap: 2.5rem; } }
  /* ── BRIDGE VISUAL ── */
  .bridge {
    display: flex;
    align-items: stretch;
    gap: 0;
    margin: 2.5rem 0;
    border-radius: 12px;
    overflow: hidden;
    min-height: 160px;
  }
  .bridge-side {
    flex: 1;
    padding: 2rem 1.75rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .bridge-left { background: #2D3D29; }
  .bridge-right { background: #1E3345; }
  .bridge-mid {
    width: 60px;
    background: linear-gradient(to right, #2D3D29, #1E3345);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .bridge-mid-icon {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background: var(--gold);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
  }
  .bridge-tag {
    font-size: 10px;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: rgba(255,255,255,.4);
    margin-bottom: .5rem;
  }
  .bridge-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    color: #fff;
    line-height: 1.3;
    margin-bottom: .5rem;
  }
  .bridge-desc {
    font-size: 13px;
    color: rgba(255,255,255,.55);
    line-height: 1.6;
  }
  /* ── OFFER CARDS ── */
  .offer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
    margin: 2.5rem 0;
  }
  .offer-card {
    border: 1px solid rgba(61,43,31,.12);
    border-radius: 12px;
    padding: 1.75rem;
    background: #fff;
    position: relative;
    overflow: hidden;
  }
  .offer-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
  }
  .offer-card.green::before  { background: var(--moss); }
  .offer-card.gold::before   { background: var(--gold); }
  .offer-card.river::before  { background: var(--river); }
  .offer-card-icon {
    font-size: 22px;
    margin-bottom: 1rem;
  }
  .offer-card h3 {
    font-size: 1rem;
    font-family: 'DM Sans', sans-serif;
    font-weight: 500;
    margin-bottom: .5rem;
  }
  .offer-card p {
    font-size: 13px;
    line-height: 1.7;
    margin: 0;
    opacity: .7;
  }
  /* ── WATERSHED MAP VISUAL ── */
  .watershed {
    background: #1a2e1a;
    border-radius: 16px;
    padding: 2.5rem;
    margin: 2.5rem 0;
    position: relative;
    overflow: hidden;
  }
  .watershed::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 120% 80% at 30% 70%, rgba(74,123,157,.2) 0%, transparent 60%);
  }
  .watershed-title {
    font-size: 11px;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: rgba(200,216,196,.5);
    margin-bottom: 1.5rem;
    position: relative;
    z-index: 1;
  }
  .flow-chain {
    display: flex;
    align-items: center;
    gap: 0;
    flex-wrap: wrap;
    position: relative;
    z-index: 1;
  }
  .flow-node {
    padding: .6rem 1.1rem;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
    white-space: nowrap;
  }
  .flow-node.site   { background: rgba(74,103,65,.6);  color: var(--mist); }
  .flow-node.river  { background: rgba(74,123,157,.5); color: var(--sky); }
  .flow-node.ocean  { background: rgba(30,51,69,.8);   color: var(--sky); border: 1px solid rgba(74,123,157,.4); }
  .flow-node.isha   { background: rgba(196,147,63,.25); color: var(--sand); border: 1px solid rgba(196,147,63,.35); }
  .flow-arrow {
    color: rgba(200,216,196,.3);
    font-size: 16px;
    padding: 0 .4rem;
  }
  .flow-note {
    font-size: 11px;
    color: rgba(200,216,196,.4);
    margin-top: 1rem;
    line-height: 1.5;
  }
  /* ── TIMELINE ── */
  .timeline { margin: 2rem 0; }
  .tl-row {
    display: flex;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
    align-items: flex-start;
  }
  .tl-dot {
    flex-shrink: 0;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--gold);
    margin-top: 5px;
  }
  .tl-body { flex: 1; }
  .tl-time {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: .08em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 2px;
  }
  .tl-title {
    font-size: 15px;
    font-weight: 500;
    margin-bottom: 3px;
    color: var(--cream);
  }
  .tl-desc { font-size: 13px; opacity: .55; line-height: 1.55; max-width: none; margin: 0; }
  /* ── ASK SECTION ── */
  .ask-box {
    border: 1px solid rgba(196,147,63,.35);
    border-radius: 16px;
    padding: 2.5rem 3rem;
    max-width: 720px;
    background: rgba(196,147,63,.06);
    margin: 2rem 0;
  }
  .ask-box h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 400;
    margin-bottom: 1rem;
    color: var(--cream);
  }
  .ask-box p { color: rgba(245,238,228,.75); max-width: none; }
  .ask-list { list-style: none; margin: 1rem 0; }
  .ask-list li {
    font-size: 14px;
    line-height: 1.7;
    padding: .4rem 0;
    border-bottom: 1px solid rgba(196,147,63,.15);
    color: rgba(245,238,228,.75);
    display: flex;
    gap: 12px;
    align-items: flex-start;
  }
  .ask-list li::before {
    content: '—';
    color: var(--gold);
    flex-shrink: 0;
    font-weight: 300;
    margin-top: 1px;
  }
  .ask-list li:last-child { border-bottom: none; }
  /* ── CLOSING ── */
  .closing {
    min-height: 60vh;
    background: var(--soil);
    display: flex;
    align-items: center;
    padding: 8vw 10vw;
    position: relative;
    overflow: hidden;
  }
  .closing::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 70% 70% at 15% 85%, rgba(74,103,65,.3) 0%, transparent 55%),
                radial-gradient(ellipse 50% 50% at 85% 15%, rgba(74,123,157,.15) 0%, transparent 50%);
  }
  .closing-inner { position: relative; z-index: 1; max-width: 680px; }
  .closing h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.4rem);
    font-weight: 400;
    color: var(--cream);
    line-height: 1.2;
    margin-bottom: 1.5rem;
    max-width: 600px;
  }
  .closing h2 em { font-style: italic; color: var(--sand); }
  .closing p {
    color: var(--sand);
    opacity: .7;
    font-size: 15px;
    margin-bottom: 2.5rem;
    max-width: 520px;
  }
  .cta-line {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    flex-wrap: wrap;
  }
  .cta-name {
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    color: var(--cream);
    opacity: .5;
  }
  .cta-divider { width: 1px; height: 24px; background: rgba(212,184,150,.2); }
  .cta-role {
    font-size: 12px;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--sand);
    opacity: .4;
  }
  /* ── ANIMATIONS ── */
  .reveal {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity .7s ease, transform .7s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  /* ── PROGRESS ── */
  .progress-bar {
    position: fixed;
    top: 0; left: 0;
    height: 2px;
    background: var(--gold);
    z-index: 100;
    transition: width .1s linear;
  }
  /* ── NAV DOTS ── */
  .nav-dots {
    position: fixed;
    right: 2rem;
    top: 50%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    gap: 10px;
    z-index: 50;
  }
  .nav-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--clay);
    opacity: .3;
    cursor: pointer;
    transition: all .2s;
  }
  .nav-dot.active { opacity: 1; background: var(--gold); transform: scale(1.4); }
  @media (max-width: 600px) {
    .nav-dots { display: none; }
    section { padding: 12vw 6vw; }
    .cover-inner { padding: 12vw 6vw; }
    .cover-meta { flex-direction: column; gap: 1.2rem; }
  }
</style>
</head>
<body>
<div class="progress-bar" id="progress"></div>
<div class="nav-dots" id="navDots">
  <div class="nav-dot active" onclick="scrollTo(0)"></div>
  <div class="nav-dot" onclick="document.getElementById('s1').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s2').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s3').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s4').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s5').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s6').scrollIntoView({behavior:'smooth'})"></div>
  <div class="nav-dot" onclick="document.getElementById('s7').scrollIntoView({behavior:'smooth'})"></div>
</div>
<!-- ══════════ COVER ══════════ -->
<div class="cover" id="s0">
  <div class="cover-texture"></div>
  <div class="cover-inner">
    <div class="cover-eyebrow">A collaboration proposal</div>
    <h1 class="cover-title">
      The mineral foundation<br>
      <em>beneath the movement</em>
    </h1>
    <p class="cover-sub">
      How crushed Deccan Trap basalt applied to Cauvery basin soils
      can amplify Save Soil's mission — and generate India's first
      internationally verified carbon removal numbers.
    </p>
    <div class="cover-divider"></div>
    <div class="cover-meta">
      <div class="cover-meta-item">
        <div class="cover-meta-label">Presented to</div>
        <div class="cover-meta-val">Anand Ethirajalu, Project Director<br>Conscious Planet – Cauvery Calling</div>
      </div>
      <div class="cover-meta-item">
        <div class="cover-meta-label">From</div>
        <div class="cover-meta-val">ILHA Carbon<br>Tamil Nadu Agricultural University</div>
      </div>
      <div class="cover-meta-item">
        <div class="cover-meta-label">Date</div>
        <div class="cover-meta-val">March 2026</div>
      </div>
    </div>
  </div>
  <div class="cover-footer">
    <div class="cover-footer-brand">ILHA Carbon × TNAU Coimbatore</div>
    <div class="cover-scroll">Scroll to explore</div>
  </div>
</div>
<!-- ══════════ 1 — THE SHARED MISSION ══════════ -->
<section id="s1" class="warm">
  <div class="section-label reveal">Common ground</div>
  <h2 class="reveal">You said it best.</h2>
  <div class="pull-quote reveal">
    <p>"Climate change cannot be fixed in the atmosphere.<br>It can be fixed only in the soil."</p>
    <div class="attr">Anand Ethirajalu — COP29, 2024</div>
  </div>
  <p class="reveal">
    That statement is the scientific foundation of everything ILHA Carbon is building.
    Not a metaphor. Not inspiration. <strong>Literally true</strong> — and now provable
    with numbers, in Tamil Nadu, in the same river basin where Cauvery Calling
    is already working.
  </p>
  <p class="reveal">
    We are not asking Cauvery Calling to change direction.
    We are offering to measure and amplify what you are already doing.
  </p>
  <div class="stat-strip reveal">
    <div class="stat-cell">
      <div class="stat-num">3.8%</div>
      <div class="stat-label">Increase in soil organic carbon from basalt amendment in tropical latitudes<br><em style="opacity:.5;font-size:11px">Global Change Biology, Sept 2025</em></div>
    </div>
    <div class="stat-cell">
      <div class="stat-num">40°N–30°S</div>
      <div class="stat-label">The latitude band where ERW most powerfully builds organic soil health — Tamil Nadu is at 11°N, squarely inside</div>
    </div>
    <div class="stat-cell">
      <div class="stat-num">0</div>
      <div class="stat-label">Peer-reviewed ERW carbon removal studies published from Tamil Nadu soils — this is the gap we fill</div>
    </div>
  </div>
</section>
<!-- ══════════ 2 — THE SCIENCE ══════════ -->
<section id="s2">
  <div class="section-label reveal">The mechanism</div>
  <h2 class="reveal">What basalt does to soil that trees cannot do alone.</h2>
  <div class="two-col">
    <div>
      <p class="reveal">
        When finely crushed Deccan Trap basalt is applied to agricultural soil,
        it dissolves slowly — releasing calcium, magnesium, silicon, and phosphorus.
        These are the exact minerals that depleted tropical soils have lost over
        centuries of cultivation.
      </p>
      <p class="reveal">
        The dissolution reaction consumes atmospheric CO₂, converting it to
        bicarbonate ions that travel through the soil, into rivers, and ultimately
        to the ocean — where they are stored for <strong>over 10,000 years</strong>.
        No forest fire, no land use change, no drought can reverse this.
      </p>
      <p class="reveal">
        But here is what matters most for Save Soil: the same mineral release
        that sequesters carbon <strong>also physically protects organic matter</strong>
        from decomposition. The reactive minerals from basalt bind to soil organic
        carbon and shield it. Trees grow faster. Soil life thrives.
        The organic carbon your farmers are building through agroforestry
        stays in the soil longer.
      </p>
    </div>
    <div>
      <div class="offer-grid" style="grid-template-columns:1fr;">
        <div class="offer-card green reveal">
          <div class="offer-card-icon">🌱</div>
          <h3>Soil organic carbon</h3>
          <p>Basalt application increases SOC by up to 3.8% in tropical latitudes. The minerals released bind and protect organic matter, making every tree Cauvery Calling plants more effective at building soil carbon.</p>
        </div>
        <div class="offer-card gold reveal">
          <div class="offer-card-icon">🌾</div>
          <h3>Crop yields</h3>
          <p>Tamil Nadu Alfisol groundnut: +8–15% yield. Maize: +5–10%. Sugarcane: +3–8%. Silicon strengthens plant walls. pH correction unlocks phosphorus. Calcium and magnesium fill critical deficiencies.</p>
        </div>
        <div class="offer-card river reveal">
          <div class="offer-card-icon">💧</div>
          <h3>Permanent carbon removal</h3>
          <p>Bicarbonate ions travel the Noyyal → Cauvery → Bay of Bengal pathway and are stored in the ocean for &gt;10,000 years. This is the most durable form of carbon removal on Earth.</p>
        </div>
      </div>
    </div>
  </div>
</section>
<!-- ══════════ 3 — THE CAUVERY CONNECTION ══════════ -->
<section id="s3" class="moss-bg">
  <div class="section-label reveal">The geography</div>
  <h2 class="reveal" style="color:var(--cream)">Our projects share the same watershed.</h2>
  <p class="reveal" style="color:rgba(245,238,228,.7)">
    This is not a coincidence of alignment. It is literal geography.
    The ILHA Carbon pilot site at TNAU Coimbatore sits within the
    <strong style="color:var(--mist)">Noyyal River sub-catchment</strong>
    — a tributary of the Cauvery.
    The bicarbonate ions produced by basalt weathering at our field site
    travel the same river system that 12.2 crore Cauvery Calling saplings
    are planted alongside.
  </p>
  <div class="watershed reveal">
    <div class="watershed-title">Carbon removal pathway — ILHA Carbon site to ocean</div>
    <div class="flow-chain">
      <div class="flow-node isha">Cauvery Calling farms</div>
      <div class="flow-arrow">+</div>
      <div class="flow-node site">TNAU Coimbatore<br><span style="font-size:11px;opacity:.6">ILHA Carbon pilot</span></div>
      <div class="flow-arrow">→</div>
      <div class="flow-node river">Noyyal River</div>
      <div class="flow-arrow">→</div>
      <div class="flow-node river">Cauvery River</div>
      <div class="flow-arrow">→</div>
      <div class="flow-node ocean">Bay of Bengal<br><span style="font-size:11px;opacity:.6">>10,000 yr storage</span></div>
    </div>
    <div class="flow-note">
      Isometric Protocol v1.1 and Verra VM0046 require documented riverine connectivity for permanence claims.<br>
      CWC hydrological maps confirm Noyyal–Cauvery–Bay of Bengal as a verified, monitorable transport pathway.
    </div>
  </div>
  <p class="reveal" style="color:rgba(245,238,228,.7)">
    Cauvery Calling's tree-planting programme builds organic carbon above ground.
    ILHA Carbon's basalt programme builds mineral carbon below ground and in the river system.
    <strong style="color:var(--mist)">These are not competing approaches. They are complementary layers
    of the same carbon cycle.</strong>
  </p>
  <div class="pull-quote reveal" style="border-left-color:var(--leaf)">
    <p style="font-size:1.1rem">"ERW and organic farming are synergistic — combining ground rock with organic amendments
    produced the highest rates of both enhanced weathering and organic carbon accumulation together."</p>
    <div class="attr" style="color:var(--mist)">Anthony et al., AGU Advances, 2025</div>
  </div>
</section>
<!-- ══════════ 4 — WHAT WE'VE BUILT ══════════ -->
<section id="s4" class="warm">
  <div class="section-label reveal">The project</div>
  <h2 class="reveal">India's first registry-grade ERW project.<br>Already in development.</h2>
  <p class="reveal">
    ILHA Carbon has developed a complete Project Design Document (PDD) for an
    Enhanced Rock Weathering pilot at TNAU Coimbatore — benchmarked against
    <strong>Verra VCS VM0046</strong>, <strong>Isometric Enhanced Weathering Protocol v1.1</strong>,
    and <strong>Puro.earth CORC (2025)</strong>. This is not a concept. It is a submission-grade
    technical document.
  </p>
  <div class="stat-strip reveal">
    <div class="stat-cell">
      <div class="stat-num">2 ha</div>
      <div class="stat-label">Phase 1 pilot at TNAU Experimental Farm, Coimbatore campus</div>
    </div>
    <div class="stat-cell">
      <div class="stat-num">Salem</div>
      <div class="stat-label">Deccan Trap basalt sourced 120 km from Coimbatore — CaO+MgO >20 wt%</div>
    </div>
    <div class="stat-cell">
      <div class="stat-num">Oct 2026</div>
      <div class="stat-label">Project start date — first basalt application, pre-Northeast Monsoon</div>
    </div>
    <div class="stat-cell">
      <div class="stat-num">500 ha</div>
      <div class="stat-label">Phase 3 target — 30 FPOs across multiple Tamil Nadu districts</div>
    </div>
  </div>
  <p class="reveal">
    TNAU provides ISO 17025-accredited laboratories, 40 years of continuous
    agrometeorological data, and a 38-district farmer extension network.
    The institutional infrastructure for scaling this across Tamil Nadu
    already exists. <strong>We are not starting from zero.</strong>
  </p>
</section>
<!-- ══════════ 5 — THE OFFER ══════════ -->
<section id="s5" class="alt">
  <div class="section-label reveal">The partnership</div>
  <h2 class="reveal" style="color:var(--sand)">What we are offering Cauvery Calling.</h2>
  <p class="reveal" style="color:rgba(245,238,228,.7)">
    This is not a funding request. It is a data partnership — and an opportunity
    for Cauvery Calling to have something it currently cannot generate on its own:
    internationally peer-reviewed, registry-certified carbon removal numbers
    from Tamil Nadu soils.
  </p>
  <div class="bridge reveal">
    <div class="bridge-side bridge-left">
      <div class="bridge-tag">What ILHA Carbon brings</div>
      <div class="bridge-title">Registry-grade science,<br>field-ready now</div>
      <div class="bridge-desc">Complete PDD · TNAU laboratory infrastructure · TiCAT MRV methodology · Deccan Trap basalt feedstock · Salem quarry sourcing · LCA framework · VCS + Isometric compliance</div>
    </div>
    <div class="bridge-mid">
      <div class="bridge-mid-icon">⇄</div>
    </div>
    <div class="bridge-side bridge-right">
      <div class="bridge-tag">What Cauvery Calling brings</div>
      <div class="bridge-title">Scale, trust,<br>and field access</div>
      <div class="bridge-desc">160 field executives · 32,000+ enrolled farmlands · Farmer trust built over years · Cauvery basin geography · FPO networks · TNAU partnership history · Movement credibility</div>
    </div>
  </div>
 offer-card {
  background: #2D3D29; /* deep moss dark */
  border: 1px solid rgba(122,158,110,.25);
  border-radius: 12px;
  padding: 1.75rem;
  position: relative;
  overflow: hidden;
}
  <div class="offer-grid reveal">
    <div class="offer-card green">
      <div class="offer-card-icon"></div>
      <h3>Carbon impact quantification</h3>
      <p>Your programme will receive the first internationally peer-reviewed carbon sequestration numbers from Tamil Nadu soils under agroforestry conditions. Data belongs to the movement.</p>
    </div>
    <div class="offer-card gold">
      <div class="offer-card-icon"></div>
      <h3>Scientific credibility</h3>
      <p>Published results in Global Change Biology or Geoderma, co-authored with TNAU and Cauvery Calling — giving Save Soil its first rigorous, independently verified CDR dataset from India.</p>
    </div>
    <div class="offer-card river">
      <div class="offer-card-icon"></div>
      <h3>Farmer benefit — at no cost</h3>
      <p>Enrolled Cauvery Calling farmers in the pilot area receive free basalt application, documented yield improvement, soil pH correction, and reduced fertiliser dependency.</p>
    </div>
  </div>
  
  <p class="reveal" style="color:rgba(245,238,228,.7)">
    ILHA Carbon's carbon credit revenue — earned from international buyers like Microsoft,
    Google, and Frontier Climate — flows directly back to Tamil Nadu farmers and
    to TNAU research. This is the climate finance reaching agriculture that
    you called for at COP29. <strong style="color:var(--cream)">We are building the mechanism
    to make it happen.</strong>
  </p>
</section>
<!-- ══════════ 6 — PATH FORWARD ══════════ -->
<section id="s6" class="river-bg">
  <div class="section-label reveal">The path forward</div>
  <h2 class="reveal" style="color:var(--cream)">How we work together.</h2>
  <div class="timeline reveal">
    <div class="tl-row">
      <div class="tl-dot"></div>
      <div class="tl-body">
        <div class="tl-time">April 2026</div>
        <div class="tl-title">Exploratory meeting</div>
        <div class="tl-desc">30 minutes at a time and place convenient to you. We walk through the science, the PDD, and the specific Cauvery basin geography. No commitments required.</div>
      </div>
    </div>
    <div class="tl-row">
      <div class="tl-dot"></div>
      <div class="tl-body">
        <div class="tl-time">May–June 2026</div>
        <div class="tl-title">Pilot site selection together</div>
        <div class="tl-desc">Identify 2–3 Cauvery Calling enrolled farms in Coimbatore or Erode district suitable for co-deployment. Farmers opt in voluntarily. Baseline soil sampling begins.</div>
      </div>
    </div>
    <div class="tl-row">
      <div class="tl-dot"></div>
      <div class="tl-body">
        <div class="tl-time">October 2026</div>
        <div class="tl-title">First basalt application</div>
        <div class="tl-desc">Pre-Northeast Monsoon. Basalt applied to TNAU pilot + selected Cauvery Calling farms. MRV monitoring begins. The science starts generating data.</div>
      </div>
    </div>
    <div class="tl-row">
      <div class="tl-dot"></div>
      <div class="tl-body">
        <div class="tl-time">2027–2028</div>
        <div class="tl-title">First peer-reviewed publication</div>
        <div class="tl-desc">Tamil Nadu's first internationally published ERW carbon removal data. Co-authored by TNAU and ILHA Carbon. Cauvery Calling acknowledged as field partner. This is Save Soil's scientific evidence base.</div>
      </div>
    </div>
    <div class="tl-row">
      <div class="tl-dot"></div>
      <div class="tl-body">
        <div class="tl-time">2028–2030</div>
        <div class="tl-title">Scale across FPO network</div>
        <div class="tl-desc">500 hectares across 30 FPOs. Carbon credits issued and sold to Frontier Climate / Microsoft / Google. Revenue shared with enrolled farmers. Cauvery Calling farmers earn from the carbon their soil sequesters.</div>
      </div>
    </div>
  </div>
</section>
<!-- ══════════ 7 — THE ASK ══════════ -->
<section id="s7" class="alt">
  <div class="section-label reveal">The ask</div>
  <h2 class="reveal" style="color:var(--cream)">One conversation.<br>No commitment required.</h2>
  <div class="ask-box reveal">
    <h3>What we are asking for</h3>
    <ul class="ask-list">
      <li>30 minutes of your time to explore whether this collaboration makes sense</li>
      <li>If it does — introductions to 2–3 field coordinators in Coimbatore or Erode district for site assessment</li>
      <li>If pilots are promising — access to Cauvery Calling's enrolled farmer data for Coimbatore district to identify willing co-deployment candidates</li>
    </ul>
    <p style="margin-top:1.2rem;">
      We are not asking for funding. We are not asking Cauvery Calling to change its programme.
      We are asking for the chance to show you that the soil science and the movement
      are pointing at the same answer.
    </p>
  </div>
  <p class="reveal" style="color:rgba(245,238,228,.7); margin-top:2rem;">
    The full Project Design Document — 33 sections, fully benchmarked against
    Verra VCS VM0046 and Isometric Protocol v1.1 — is available for your review
    ahead of or after our conversation.
  </p>
</section>
<!-- ══════════ CLOSING ══════════ -->
<div class="closing">
  <div class="closing-inner">
    <h2>The soil knows.<br><em>We are learning to measure it.</em></h2>
    <p>
      Enhanced Rock Weathering is not a technology that competes with
      what Cauvery Calling has built. It is the mineral layer that makes
      your work more permanent, more measurable, and more fundable
      by international climate finance.
    </p>
    <p>
      Tamil Nadu's soils, the Cauvery river, and the Bay of Bengal
      are already part of one of Earth's great carbon pathways.
      ILHA Carbon is here to document it, verify it, and ensure
      the farmers who steward it are rewarded for it.
    </p>
    <div class="cta-line">
      <div class="cta-name">Aswin Sivaprakash · ILHA Carbon</div>
      <div class="cta-divider"></div>
      <div class="cta-role">In partnership with TNAU Coimbatore</div>
    </div>
  </div>
</div>
<script>
  // Progress bar
  window.addEventListener('scroll', () => {
    const pct = window.scrollY / (document.body.scrollHeight - window.innerHeight) * 100;
    document.getElementById('progress').style.width = pct + '%';
    // Nav dots
    const sections = ['s0','s1','s2','s3','s4','s5','s6','s7'];
    const dots = document.querySelectorAll('.nav-dot');
    sections.forEach((id, i) => {
      const el = document.getElementById(id);
      if (!el) return;
      const rect = el.getBoundingClientRect();
      if (rect.top <= window.innerHeight/2 && rect.bottom >= window.innerHeight/2) {
        dots.forEach(d => d.classList.remove('active'));
        if (dots[i]) dots[i].classList.add('active');
      }
    });
  });
  // Reveal on scroll
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
      }
    });
  }, { threshold: 0.12 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
