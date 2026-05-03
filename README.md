# ai-tools-hub
My AI Tools Hub Project
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>AI Tools for Students — Complete Student AI Hub 2026</title>
<meta name="description" content="The best AI tools for students — study smarter, build faster, earn money. Free and paid AI tools for engineering students."/>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg:#f7f3ee;--surface:#f0ebe3;--card:#fffef9;--card2:#faf6f0;
  --border:#e8e0d4;--accent:#2d5a27;--accent2:#4a8c3f;--gold:#c17f24;
  --green:#2d5a27;--red:#9b2c2c;--blue:#1e3a6e;--orange:#c05c1a;
  --text:#1a1208;--muted:#7a6d5e;--muted2:#a8997f;
  --radius:16px;--radius-sm:10px;
  --font-display:'Fraunces',Georgia,serif;
  --font-body:'Plus Jakarta Sans',sans-serif;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{font-family:var(--font-body);background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden;}

/* TEXTURE */
body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.03'/%3E%3C/svg%3E");pointer-events:none;z-index:0;}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:100;background:rgba(247,243,238,0.92);backdrop-filter:blur(20px);border-bottom:1px solid var(--border);padding:0 clamp(1rem,5vw,4rem);height:64px;display:flex;align-items:center;justify-content:space-between;}
.nav-brand{display:flex;align-items:center;gap:10px;text-decoration:none;}
.nav-badge{background:var(--accent);color:#fff;width:32px;height:32px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:.9rem;font-weight:700;}
.nav-name{font-family:var(--font-display);font-size:1.05rem;font-weight:700;color:var(--text);}
.nav-name span{color:var(--accent);}
.nav-links{display:flex;gap:2rem;list-style:none;}
.nav-links a{color:var(--muted);text-decoration:none;font-size:.85rem;font-weight:500;transition:color .2s;}
.nav-links a:hover{color:var(--text);}
.nav-right{display:flex;align-items:center;gap:.75rem;}
.nav-cta{background:var(--accent);color:#fff;padding:.45rem 1.1rem;border-radius:100px;font-size:.82rem;font-weight:600;text-decoration:none;transition:opacity .2s;}
.nav-cta:hover{opacity:.85;}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;background:none;border:none;padding:4px;}
.hamburger span{display:block;width:22px;height:2px;background:var(--muted);border-radius:2px;}

/* HERO */
.hero{position:relative;z-index:1;padding:120px clamp(1.5rem,5vw,4rem) 5rem;text-align:center;overflow:hidden;}
.hero-tag{display:inline-flex;align-items:center;gap:.5rem;background:rgba(45,90,39,.08);border:1px solid rgba(45,90,39,.2);color:var(--accent);padding:.4rem 1.1rem;border-radius:100px;font-size:.75rem;font-weight:600;letter-spacing:.08em;text-transform:uppercase;margin-bottom:1.75rem;animation:fadeUp .8s ease both;}
.hero-dot{width:6px;height:6px;background:var(--accent2);border-radius:50%;animation:pulse 2s ease infinite;}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:.3;}}
.hero h1{font-family:var(--font-display);font-size:clamp(2.8rem,7vw,5.5rem);font-weight:900;line-height:1.05;letter-spacing:-.03em;margin-bottom:1rem;animation:fadeUp .8s .1s ease both;}
.hero h1 em{font-style:italic;color:var(--accent);}
.hero-sub{color:var(--muted);font-size:clamp(.95rem,2vw,1.15rem);max-width:520px;margin:0 auto 2.5rem;line-height:1.75;font-weight:300;animation:fadeUp .8s .2s ease both;}
.hero-actions{display:flex;gap:.85rem;justify-content:center;flex-wrap:wrap;margin-bottom:3.5rem;animation:fadeUp .8s .3s ease both;}
.btn-p{background:var(--accent);color:#fff;padding:.85rem 2rem;border-radius:100px;font-size:.92rem;font-weight:600;text-decoration:none;display:inline-flex;align-items:center;gap:.5rem;transition:opacity .2s,transform .2s;}
.btn-p:hover{opacity:.88;transform:translateY(-2px);}
.btn-s{background:transparent;color:var(--text);border:1.5px solid var(--border);padding:.85rem 2rem;border-radius:100px;font-size:.92rem;font-weight:500;text-decoration:none;display:inline-flex;align-items:center;gap:.5rem;transition:border-color .2s,background .2s;}
.btn-s:hover{border-color:var(--accent);background:rgba(45,90,39,.04);}

/* STATS */
.stats{display:flex;gap:clamp(2rem,5vw,5rem);justify-content:center;flex-wrap:wrap;animation:fadeUp .8s .4s ease both;}
.stat-num{font-family:var(--font-display);font-size:2.6rem;font-weight:900;color:var(--accent);line-height:1;}
.stat-label{font-size:.75rem;color:var(--muted);text-transform:uppercase;letter-spacing:.07em;margin-top:.25rem;}

@keyframes fadeUp{from{opacity:0;transform:translateY(22px);}to{opacity:1;transform:none;}}

/* SEARCH */
.search-sec{position:relative;z-index:1;padding:2rem clamp(1.5rem,5vw,4rem) 1.5rem;background:var(--surface);border-top:1px solid var(--border);border-bottom:1px solid var(--border);}
.search-inner{max-width:640px;margin:0 auto;}
.search-box{position:relative;margin-bottom:1.25rem;}
.search-box svg{position:absolute;left:1.1rem;top:50%;transform:translateY(-50%);color:var(--muted);pointer-events:none;}
#search{width:100%;padding:.95rem 1.25rem .95rem 3.25rem;background:var(--card);border:1.5px solid var(--border);border-radius:100px;color:var(--text);font-family:var(--font-body);font-size:.95rem;outline:none;transition:border-color .2s,box-shadow .2s;}
#search:focus{border-color:var(--accent);box-shadow:0 0 0 3px rgba(45,90,39,.1);}
#search::placeholder{color:var(--muted2);}
.filters{display:flex;gap:.5rem;flex-wrap:wrap;justify-content:center;}
.filter-btn{background:var(--card);border:1.5px solid var(--border);color:var(--muted);padding:.4rem 1rem;border-radius:100px;font-size:.8rem;font-weight:500;cursor:pointer;font-family:var(--font-body);transition:all .2s;white-space:nowrap;}
.filter-btn:hover{border-color:var(--accent);color:var(--accent);}
.filter-btn.active{background:var(--accent);border-color:var(--accent);color:#fff;font-weight:600;}

/* SECTIONS */
.tools-sec{position:relative;z-index:1;padding:3rem clamp(1.5rem,5vw,4rem) 5rem;}
.sec-header{display:flex;align-items:baseline;justify-content:space-between;margin-bottom:2.5rem;flex-wrap:wrap;gap:1rem;}
.sec-title{font-family:var(--font-display);font-size:clamp(1.8rem,3.5vw,2.6rem);font-weight:900;letter-spacing:-.02em;}
.sec-title em{font-style:italic;color:var(--accent);}
.count-pill{background:rgba(45,90,39,.08);border:1px solid rgba(45,90,39,.15);color:var(--accent);padding:.25rem .85rem;border-radius:100px;font-size:.78rem;font-weight:600;}

/* CAT GROUP */
.cat-group{margin-bottom:3.5rem;}
.cat-header{display:flex;align-items:center;gap:.85rem;margin-bottom:1.25rem;padding-bottom:.85rem;border-bottom:2px solid var(--border);}
.cat-icon{width:38px;height:38px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1.1rem;flex-shrink:0;}
.cat-title{font-family:var(--font-display);font-size:1.15rem;font-weight:700;}
.cat-count{background:var(--surface);border:1px solid var(--border);color:var(--muted);padding:.15rem .6rem;border-radius:100px;font-size:.72rem;font-weight:500;margin-left:auto;}
.cat-tag{background:rgba(193,127,36,.1);border:1px solid rgba(193,127,36,.2);color:var(--gold);padding:.15rem .6rem;border-radius:100px;font-size:.68rem;font-weight:700;text-transform:uppercase;letter-spacing:.04em;}

/* TOOL CARDS */
.tools-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));gap:1rem;}
.tool-card{background:var(--card);border:1.5px solid var(--border);border-radius:var(--radius);padding:1.4rem;display:flex;flex-direction:column;gap:.9rem;transition:transform .25s,border-color .25s,box-shadow .25s;position:relative;}
.tool-card:hover{transform:translateY(-4px);border-color:var(--accent);box-shadow:0 12px 40px rgba(45,90,39,.1);}
.tool-card.hidden{display:none;}
.card-top{display:flex;align-items:flex-start;gap:.9rem;}
.card-icon{width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.25rem;flex-shrink:0;border:1px solid var(--border);}
.card-name{font-weight:700;font-size:.98rem;letter-spacing:-.01em;margin-bottom:.2rem;display:flex;align-items:center;gap:.45rem;flex-wrap:wrap;}
.card-tag{font-size:.7rem;color:var(--muted);font-weight:400;}
.badge-new{background:rgba(193,127,36,.12);color:var(--gold);border:1px solid rgba(193,127,36,.25);font-size:.6rem;font-weight:700;padding:.1rem .45rem;border-radius:100px;text-transform:uppercase;letter-spacing:.04em;}
.badge-hot{background:rgba(155,44,44,.1);color:var(--red);border:1px solid rgba(155,44,44,.2);font-size:.6rem;font-weight:700;padding:.1rem .45rem;border-radius:100px;text-transform:uppercase;}
.card-desc{color:var(--muted);font-size:.84rem;line-height:1.65;flex:1;}
.card-footer{display:flex;align-items:center;gap:.5rem;flex-wrap:wrap;margin-top:auto;}
.btn-visit{display:inline-flex;align-items:center;gap:.35rem;background:var(--accent);color:#fff;text-decoration:none;padding:.45rem 1rem;border-radius:100px;font-size:.78rem;font-weight:600;transition:opacity .2s,transform .2s;}
.btn-visit:hover{opacity:.85;transform:scale(1.04);}
.badge-free{background:rgba(45,90,39,.08);color:var(--green);border:1px solid rgba(45,90,39,.2);border-radius:100px;padding:.15rem .55rem;font-size:.67rem;font-weight:600;}
.badge-paid{background:rgba(193,127,36,.08);color:var(--gold);border:1px solid rgba(193,127,36,.2);border-radius:100px;padding:.15rem .55rem;font-size:.67rem;font-weight:600;}
.badge-freemium{background:rgba(30,58,110,.08);color:var(--blue);border:1px solid rgba(30,58,110,.2);border-radius:100px;padding:.15rem .55rem;font-size:.67rem;font-weight:600;}
.btn-fav{background:none;border:1.5px solid var(--border);border-radius:50%;width:33px;height:33px;cursor:pointer;font-size:.85rem;display:flex;align-items:center;justify-content:center;transition:all .2s;margin-left:auto;flex-shrink:0;}
.btn-fav:hover{border-color:var(--red);}
.btn-fav.faved{border-color:var(--red);background:rgba(155,44,44,.08);}

/* FAVS */
.favs-sec{position:relative;z-index:1;padding:3rem clamp(1.5rem,5vw,4rem);background:var(--surface);border-top:1px solid var(--border);}
.fav-empty{text-align:center;color:var(--muted);padding:2.5rem;font-size:.9rem;}

/* PROMPTS */
.prompts-sec{position:relative;z-index:1;padding:3rem clamp(1.5rem,5vw,4rem);}
.prompts-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1rem;}
.prompt-card{background:var(--card);border:1.5px solid var(--border);border-radius:var(--radius);padding:1.4rem;display:flex;flex-direction:column;gap:.75rem;transition:border-color .2s,transform .2s;}
.prompt-card:hover{border-color:var(--accent);transform:translateY(-3px);}
.prompt-label{font-size:.7rem;color:var(--accent);font-weight:700;text-transform:uppercase;letter-spacing:.07em;}
.prompt-text{color:var(--text);font-size:.88rem;line-height:1.65;flex:1;}
.btn-copy{background:rgba(45,90,39,.08);border:1px solid rgba(45,90,39,.15);color:var(--accent);padding:.38rem .85rem;border-radius:8px;font-size:.76rem;font-weight:600;cursor:pointer;font-family:var(--font-body);transition:all .2s;align-self:flex-start;}
.btn-copy:hover{background:var(--accent);color:#fff;}
.btn-copy.copied{background:var(--accent2);border-color:var(--accent2);color:#fff;}

/* TIPS */
.tips-sec{position:relative;z-index:1;padding:3rem clamp(1.5rem,5vw,4rem);background:var(--surface);border-top:1px solid var(--border);}
.tips-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:1rem;}
.tip-card{background:var(--card);border:1.5px solid var(--border);border-radius:var(--radius);padding:1.5rem;transition:transform .2s,border-color .2s;}
.tip-card:hover{transform:translateY(-4px);border-color:var(--accent);}
.tip-num{font-family:var(--font-display);font-size:2.5rem;font-weight:900;font-style:italic;color:rgba(45,90,39,.15);line-height:1;margin-bottom:.6rem;}
.tip-title{font-weight:700;font-size:.96rem;margin-bottom:.45rem;letter-spacing:-.01em;}
.tip-body{color:var(--muted);font-size:.84rem;line-height:1.65;}

/* QUOTE */
.quote-sec{position:relative;z-index:1;padding:4.5rem clamp(1.5rem,5vw,4rem);text-align:center;border-top:1px solid var(--border);}
.quote-inner{max-width:700px;margin:0 auto;}
.quote-mark{font-family:var(--font-display);font-size:5rem;font-weight:900;font-style:italic;color:var(--accent);opacity:.15;line-height:.8;margin-bottom:1rem;}
.quote-text{font-family:var(--font-display);font-size:clamp(1.5rem,3.5vw,2.3rem);font-weight:700;font-style:italic;line-height:1.4;letter-spacing:-.02em;color:var(--text);margin-bottom:1.25rem;}
.quote-text em{color:var(--accent);font-style:normal;}
.quote-sub{color:var(--muted);font-size:.88rem;}

/* FOOTER */
footer{position:relative;z-index:1;padding:2rem clamp(1.5rem,5vw,4rem);border-top:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1rem;}
.footer-brand{font-family:var(--font-display);font-weight:700;font-size:.95rem;color:var(--accent);}
footer p{font-size:.82rem;color:var(--muted);}
.footer-links{display:flex;gap:1.5rem;}
.footer-links a{color:var(--muted);text-decoration:none;font-size:.82rem;transition:color .2s;}
.footer-links a:hover{color:var(--accent);}

/* UTILS */
#backTop{position:fixed;bottom:2rem;right:2rem;z-index:500;width:44px;height:44px;background:var(--accent);color:#fff;border:none;border-radius:50%;cursor:pointer;font-size:1.1rem;display:flex;align-items:center;justify-content:center;opacity:0;pointer-events:none;transition:opacity .3s,transform .3s;box-shadow:0 4px 16px rgba(45,90,39,.3);}
#backTop.show{opacity:1;pointer-events:all;}
#backTop:hover{transform:translateY(-3px);}
#toast{position:fixed;bottom:5.5rem;left:50%;transform:translateX(-50%) translateY(10px);background:var(--text);color:var(--bg);padding:.65rem 1.4rem;border-radius:100px;font-size:.84rem;font-weight:500;opacity:0;pointer-events:none;transition:all .3s;z-index:600;white-space:nowrap;box-shadow:0 6px 24px rgba(0,0,0,.15);}
#toast.show{opacity:1;transform:translateX(-50%) translateY(0);}
#noResults{display:none;text-align:center;color:var(--muted);padding:3rem;grid-column:1/-1;}
#noResults.show{display:block;}
.reveal{opacity:0;transform:translateY(24px);transition:opacity .6s ease,transform .6s ease;}
.reveal.visible{opacity:1;transform:none;}

@media(max-width:768px){
  .nav-links{display:none;flex-direction:column;position:fixed;top:64px;left:0;right:0;background:rgba(247,243,238,.97);backdrop-filter:blur(20px);padding:2rem;gap:1.5rem;border-bottom:1px solid var(--border);z-index:99;}
  .nav-links.open{display:flex;}
  .nav-links a{font-size:1.1rem;color:var(--text);}
  .hamburger{display:flex;}
  .nav-cta{display:none;}
  footer{flex-direction:column;text-align:center;}
  .footer-links{justify-content:center;}
}
</style>
</head>
<body>

<button id="backTop">↑</button>
<div id="toast"></div>

<!-- NAV -->
<nav>
  <a href="#" class="nav-brand">
    <div class="nav-badge">⚡</div>
    <span class="nav-name">AI Tools <span>for Students</span></span>
  </a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#tools">Tools</a></li>
    <li><a href="#favs">Favourites</a></li>
    <li><a href="#prompts">Prompts</a></li>
    <li><a href="#tips">Tips</a></li>
  </ul>
  <div class="nav-right">
    <a href="#tools" class="nav-cta">Explore Tools →</a>
    <button class="hamburger" id="hamburger"><span></span><span></span><span></span></button>
  </div>
</nav>

<!-- HERO -->
<header class="hero">
  <div class="hero-tag"><div class="hero-dot"></div>Made for Students · Free to Use · 2026</div>
  <h1>The Best AI Tools<br/>for <em>Students</em></h1>
  <p class="hero-sub">Study smarter. Build faster. Earn money. All the AI tools you need as a student — organised in one place.</p>
  <div class="hero-actions">
    <a href="#tools" class="btn-p">Explore All Tools →</a>
    <a href="#prompts" class="btn-s">📋 Copy Prompts</a>
  </div>
  <div class="stats">
    <div class="stat"><div class="stat-num">40+</div><div class="stat-label">Student Tools</div></div>
    <div class="stat"><div class="stat-num">7</div><div class="stat-label">Categories</div></div>
    <div class="stat"><div class="stat-num" id="statFavs">0</div><div class="stat-label">Your Favs</div></div>
    <div class="stat"><div class="stat-num">Free</div><div class="stat-label">To Browse</div></div>
  </div>
</header>

<!-- SEARCH -->
<div class="search-sec" id="tools">
  <div class="search-inner">
    <div class="search-box">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
      <input type="text" id="search" placeholder="Search any AI tool for students…" autocomplete="off"/>
    </div>
    <div class="filters">
      <button class="filter-btn active" data-cat="all">🌟 All</button>
      <button class="filter-btn" data-cat="study">📚 Study</button>
      <button class="filter-btn" data-cat="coding">💻 Coding</button>
      <button class="filter-btn" data-cat="writing">✍️ Writing</button>
      <button class="filter-btn" data-cat="research">🔍 Research</button>
      <button class="filter-btn" data-cat="design">🎨 Design</button>
      <button class="filter-btn" data-cat="productivity">📋 Productivity</button>
      <button class="filter-btn" data-cat="earn">💰 Earn Money</button>
    </div>
  </div>
</div>

<!-- ALL TOOLS -->
<section class="tools-sec">
  <div class="sec-header reveal">
    <h2 class="sec-title">All <em>Tools</em></h2>
    <span class="count-pill" id="toolCount">40+ Student Tools</span>
  </div>

  <div id="toolsContainer">

    <!-- STUDY TOOLS -->
    <div class="cat-group reveal" data-section="study">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(45,90,39,.1)">📚</div>
        <span class="cat-title">Study & Learning Tools</span>
        <span class="cat-count">8 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="study" data-name="chatgpt openai study qa explain"><div class="card-top"><div class="card-icon" style="background:rgba(16,163,127,.1)">🤖</div><div><div class="card-name">ChatGPT</div><div class="card-tag">Study · Q&A · Explanations</div></div></div><p class="card-desc">Ask any question, get instant explanations, create study guides and practice for exams. The most popular AI study partner for students worldwide.</p><div class="card-footer"><a href="https://chat.openai.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="chatgpt">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="claude anthropic deep study research"><div class="card-top"><div class="card-icon" style="background:rgba(239,166,84,.1)">🧠</div><div><div class="card-name">Claude</div><div class="card-tag">Deep Study · Analysis · Writing</div></div></div><p class="card-desc">Best AI for understanding tough concepts, long reading material and research. Explains things clearly and patiently — perfect for engineering students.</p><div class="card-footer"><a href="https://claude.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="claude">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="notebooklm google study notes pdf lecture"><div class="card-top"><div class="card-icon" style="background:rgba(59,130,246,.1)">📓</div><div><div class="card-name">NotebookLM <span class="badge-new">Must Try</span></div><div class="card-tag">Study Notes · PDF Chat · Audio</div></div></div><p class="card-desc">Upload your lecture notes and PDFs then CHAT with them. Ask questions about your own notes! Also creates audio podcast summaries of your study material.</p><div class="card-footer"><a href="https://notebooklm.google" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="notebooklm">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="quizlet ai flashcards quiz exam"><div class="card-top"><div class="card-icon" style="background:rgba(74,140,63,.1)">🃏</div><div><div class="card-name">Quizlet AI</div><div class="card-tag">Flashcards · Practice Tests</div></div></div><p class="card-desc">Auto-generate flashcards and practice tests from your notes. AI creates everything for you — just paste your content and start memorizing for exams.</p><div class="card-footer"><a href="https://quizlet.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="quizlet">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="otter ai lecture transcription notes recording"><div class="card-top"><div class="card-icon" style="background:rgba(59,130,246,.1)">🎙️</div><div><div class="card-name">Otter.ai</div><div class="card-tag">Lecture Recording · Auto Notes</div></div></div><p class="card-desc">Record your lectures and Otter automatically transcribes everything the professor says in real time. Never miss a word in class ever again!</p><div class="card-footer"><a href="https://otter.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="otter">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="explainpaper research paper simplify understand"><div class="card-top"><div class="card-icon" style="background:rgba(168,85,247,.1)">📄</div><div><div class="card-name">Explainpaper</div><div class="card-tag">Research Papers · Simplify</div></div></div><p class="card-desc">Upload any research paper and AI explains complex sections in simple language. Perfect for literature reviews and understanding academic papers quickly.</p><div class="card-footer"><a href="https://explainpaper.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="explainpaper">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="wolfram alpha maths science solver engineering"><div class="card-top"><div class="card-icon" style="background:rgba(239,68,68,.1)">🔢</div><div><div class="card-name">Wolfram Alpha</div><div class="card-tag">Maths · Physics · Chemistry</div></div></div><p class="card-desc">Solve complex maths, physics and chemistry problems with detailed step-by-step solutions. Every engineering student's most important tool for tough problems.</p><div class="card-footer"><a href="https://wolframalpha.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="wolfram">🤍</button></div></div>

        <div class="tool-card" data-cat="study" data-name="scholarcy summarize research paper literature review"><div class="card-top"><div class="card-icon" style="background:rgba(16,185,129,.1)">📊</div><div><div class="card-name">Scholarcy</div><div class="card-tag">Paper Summaries · Literature Review</div></div></div><p class="card-desc">Summarize 30-page research papers in seconds. Extracts key findings, main points and important references automatically — perfect for project reports.</p><div class="card-footer"><a href="https://scholarcy.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="scholarcy">🤍</button></div></div>
      </div>
    </div>

    <!-- CODING TOOLS -->
    <div class="cat-group reveal" data-section="coding">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(30,58,110,.1)">💻</div>
        <span class="cat-title">Coding & Project Tools</span>
        <span class="cat-count">7 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="coding" data-name="cursor ai code editor student project"><div class="card-top"><div class="card-icon" style="background:rgba(59,130,246,.1)">🖱️</div><div><div class="card-name">Cursor <span class="badge-new">Top Pick</span></div><div class="card-tag">AI Code Editor</div></div></div><p class="card-desc">Write code by describing what you want in English. The smartest AI code editor for students building projects. Complete assignments 10x faster than normal.</p><div class="card-footer"><a href="https://cursor.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="cursor">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="github copilot free student code ai"><div class="card-top"><div class="card-icon" style="background:rgba(0,0,0,.06)">👨‍💻</div><div><div class="card-name">GitHub Copilot <span class="badge-new">Free for Students</span></div><div class="card-tag">AI Pair Programmer</div></div></div><p class="card-desc">AI that suggests code as you type. Free for all students with GitHub Student Pack. Like having a senior developer helping you with every line of code.</p><div class="card-footer"><a href="https://github.com/features/copilot" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free for Students</span><button class="btn-fav" data-tool="copilot">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="replit browser coding online ide student"><div class="card-top"><div class="card-icon" style="background:rgba(249,115,22,.1)">🔄</div><div><div class="card-name">Replit</div><div class="card-tag">Browser IDE · No Install</div></div></div><p class="card-desc">Code in your browser with zero installation. AI helps you write and debug code. Perfect for students without powerful laptops or who code on shared computers.</p><div class="card-footer"><a href="https://replit.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="replit">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="bolt new build app student project fast"><div class="card-top"><div class="card-icon" style="background:rgba(245,158,11,.1)">⚡</div><div><div class="card-name">Bolt.new</div><div class="card-tag">Build Full Apps Instantly</div></div></div><p class="card-desc">Build complete applications just by describing them in plain English. No setup needed. Perfect for hackathons, college projects and building your portfolio fast.</p><div class="card-footer"><a href="https://bolt.new" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="bolt">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="kaggle python machine learning free course certificate"><div class="card-top"><div class="card-icon" style="background:rgba(32,178,170,.1)">📈</div><div><div class="card-name">Kaggle</div><div class="card-tag">Free Courses · ML · Certificates</div></div></div><p class="card-desc">Free Python, ML and Data Science courses with free certificates. Real datasets and competitions where you can win cash prizes. Owned by Google — completely free.</p><div class="card-footer"><a href="https://kaggle.com/learn" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="kaggle">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="v0 vercel ui react frontend student"><div class="card-top"><div class="card-icon" style="background:rgba(0,0,0,.06)">🎯</div><div><div class="card-name">v0 by Vercel</div><div class="card-tag">UI Generator · React</div></div></div><p class="card-desc">Generate beautiful React UI components from text descriptions instantly. Perfect for students building web projects who want professional looking interfaces fast.</p><div class="card-footer"><a href="https://v0.dev" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="v0">🤍</button></div></div>

        <div class="tool-card" data-cat="coding" data-name="google antigravity agent ide new 2026"><div class="card-top"><div class="card-icon" style="background:rgba(66,133,244,.1)">🌌</div><div><div class="card-name">Google Antigravity <span class="badge-new">NEW 2026</span></div><div class="card-tag">Agent-First IDE · Google</div></div></div><p class="card-desc">Google's brand new agent-first development platform. AI agents plan, write and test your code autonomously. Completely free during public preview — try it now!</p><div class="card-footer"><a href="https://antigravity.google" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free Preview</span><button class="btn-fav" data-tool="antigravity">🤍</button></div></div>
      </div>
    </div>

    <!-- WRITING TOOLS -->
    <div class="cat-group reveal" data-section="writing">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(193,127,36,.1)">✍️</div>
        <span class="cat-title">Writing & Assignment Tools</span>
        <span class="cat-count">5 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="writing" data-name="grammarly grammar english writing assignment"><div class="card-top"><div class="card-icon" style="background:rgba(22,160,133,.1)">✅</div><div><div class="card-name">Grammarly <span class="badge-new">Must Have</span></div><div class="card-tag">Grammar · Writing Quality</div></div></div><p class="card-desc">Fix grammar mistakes, improve your writing style and check plagiarism automatically. Works everywhere — Gmail, Google Docs, any website. Essential for every student.</p><div class="card-footer"><a href="https://grammarly.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="grammarly">🤍</button></div></div>

        <div class="tool-card" data-cat="writing" data-name="hemingway app writing clarity simple english"><div class="card-top"><div class="card-icon" style="background:rgba(245,158,11,.1)">📝</div><div><div class="card-name">Hemingway App</div><div class="card-tag">Writing Clarity · Simplify</div></div></div><p class="card-desc">Makes your writing clear and bold. Highlights complex sentences, passive voice and hard words. Helps you write assignments that are easy to read and understand.</p><div class="card-footer"><a href="https://hemingwayapp.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="hemingway">🤍</button></div></div>

        <div class="tool-card" data-cat="writing" data-name="wordtune rewrite improve writing paraphrase"><div class="card-top"><div class="card-icon" style="background:rgba(99,102,241,.1)">🔄</div><div><div class="card-name">Wordtune</div><div class="card-tag">Rewrite · Paraphrase · Improve</div></div></div><p class="card-desc">AI that rewrites and improves your sentences instantly. Multiple suggestions for every sentence. Perfect for improving your assignment writing quality fast.</p><div class="card-footer"><a href="https://wordtune.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="wordtune">🤍</button></div></div>

        <div class="tool-card" data-cat="writing" data-name="jenni ai academic writing essay report"><div class="card-top"><div class="card-icon" style="background:rgba(239,68,68,.1)">🎓</div><div><div class="card-name">Jenni AI</div><div class="card-tag">Academic Writing · Essays</div></div></div><p class="card-desc">AI writing assistant built specifically for students and academics. Helps write essays, research reports and academic papers with proper citations.</p><div class="card-footer"><a href="https://jenni.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="jenni">🤍</button></div></div>

        <div class="tool-card" data-cat="writing" data-name="quillbot paraphrase summarize writing tool student"><div class="card-top"><div class="card-icon" style="background:rgba(16,185,129,.1)">🪶</div><div><div class="card-name">QuillBot</div><div class="card-tag">Paraphrase · Summarize</div></div></div><p class="card-desc">Paraphrase and summarize any text instantly. Improve your writing with AI suggestions. Most popular writing tool among students worldwide in 2026.</p><div class="card-footer"><a href="https://quillbot.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="quillbot">🤍</button></div></div>
      </div>
    </div>

    <!-- RESEARCH TOOLS -->
    <div class="cat-group reveal" data-section="research">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(99,102,241,.1)">🔍</div>
        <span class="cat-title">Research & Information Tools</span>
        <span class="cat-count">5 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="research" data-name="perplexity ai search research sources student"><div class="card-top"><div class="card-icon" style="background:rgba(99,102,241,.1)">🔍</div><div><div class="card-name">Perplexity AI <span class="badge-new">Top Pick</span></div><div class="card-tag">AI Search · Cited Answers</div></div></div><p class="card-desc">Get direct answers with real sources for any research question. No fake information. Perfect for research assignments and finding accurate information fast.</p><div class="card-footer"><a href="https://perplexity.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="perplexity">🤍</button></div></div>

        <div class="tool-card" data-cat="research" data-name="consensus research paper academic science student"><div class="card-top"><div class="card-icon" style="background:rgba(16,185,129,.1)">📊</div><div><div class="card-name">Consensus</div><div class="card-tag">Academic Research · Papers</div></div></div><p class="card-desc">Search thousands of research papers and get evidence-based answers from real scientific studies. Perfect for college projects and literature reviews.</p><div class="card-footer"><a href="https://consensus.app" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="consensus">🤍</button></div></div>

        <div class="tool-card" data-cat="research" data-name="elicit research assistant paper finder student"><div class="card-top"><div class="card-icon" style="background:rgba(168,85,247,.1)">🔬</div><div><div class="card-name">Elicit</div><div class="card-tag">Research Assistant · Paper Finder</div></div></div><p class="card-desc">AI research assistant that finds and summarizes relevant papers for any topic automatically. Saves hours of manual searching for student projects.</p><div class="card-footer"><a href="https://elicit.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="elicit">🤍</button></div></div>

        <div class="tool-card" data-cat="research" data-name="semantic scholar free academic paper search"><div class="card-top"><div class="card-icon" style="background:rgba(59,130,246,.1)">🎓</div><div><div class="card-name">Semantic Scholar</div><div class="card-tag">Free Academic Papers</div></div></div><p class="card-desc">Find and read millions of free academic papers. AI helps you understand papers and find related work. Essential for any college research project.</p><div class="card-footer"><a href="https://semanticscholar.org" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="semantic">🤍</button></div></div>

        <div class="tool-card" data-cat="research" data-name="google scholar research paper free citation"><div class="card-top"><div class="card-icon" style="background:rgba(66,133,244,.1)">📚</div><div><div class="card-name">Google Scholar</div><div class="card-tag">Academic Papers · Citations</div></div></div><p class="card-desc">Search millions of academic papers, theses and books for free. Find proper citations for your assignments. The most trusted academic search engine for students.</p><div class="card-footer"><a href="https://scholar.google.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="gscholar">🤍</button></div></div>
      </div>
    </div>

    <!-- DESIGN TOOLS -->
    <div class="cat-group reveal" data-section="design">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(192,92,26,.1)">🎨</div>
        <span class="cat-title">Design & Presentation Tools</span>
        <span class="cat-count">5 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="design" data-name="canva ai design presentation poster student"><div class="card-top"><div class="card-icon" style="background:rgba(0,197,168,.1)">🎨</div><div><div class="card-name">Canva AI <span class="badge-new">Must Have</span></div><div class="card-tag">Design · Presentations · Posters</div></div></div><p class="card-desc">Create professional presentations, posters and thumbnails in minutes with AI. No design skills needed. Free for students and perfect for all college submissions.</p><div class="card-footer"><a href="https://canva.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="canva">🤍</button></div></div>

        <div class="tool-card" data-cat="design" data-name="gamma ai presentation slides deck student"><div class="card-top"><div class="card-icon" style="background:rgba(168,85,247,.1)">🚀</div><div><div class="card-name">Gamma AI</div><div class="card-tag">AI Presentations · Slides</div></div></div><p class="card-desc">Generate beautiful slide decks from a single text prompt in under a minute. The fastest way for students to create professional project presentations.</p><div class="card-footer"><a href="https://gamma.app" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="gamma">🤍</button></div></div>

        <div class="tool-card" data-cat="design" data-name="ideogram text image poster thumbnail"><div class="card-top"><div class="card-icon" style="background:rgba(6,182,212,.1)">📝</div><div><div class="card-name">Ideogram</div><div class="card-tag">AI Images with Text</div></div></div><p class="card-desc">Best AI tool for generating images with accurate readable text. Perfect for creating posters, blog thumbnails and project banners as a student.</p><div class="card-footer"><a href="https://ideogram.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="ideogram">🤍</button></div></div>

        <div class="tool-card" data-cat="design" data-name="adobe firefly image design student free"><div class="card-top"><div class="card-icon" style="background:rgba(239,68,68,.1)">🔥</div><div><div class="card-name">Adobe Firefly</div><div class="card-tag">AI Image Generation</div></div></div><p class="card-desc">Generate professional quality images for your projects and assignments. Commercially safe — you can use these images in college submissions without copyright issues.</p><div class="card-footer"><a href="https://firefly.adobe.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="firefly">🤍</button></div></div>

        <div class="tool-card" data-cat="design" data-name="beautiful ai presentation smart slides"><div class="card-top"><div class="card-icon" style="background:rgba(99,102,241,.1)">✨</div><div><div class="card-name">Beautiful.ai</div><div class="card-tag">Smart Presentations</div></div></div><p class="card-desc">AI that automatically designs your slides as you add content. Keeps everything looking professional without any design effort from you.</p><div class="card-footer"><a href="https://beautiful.ai" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="beautifulai">🤍</button></div></div>
      </div>
    </div>

    <!-- PRODUCTIVITY TOOLS -->
    <div class="cat-group reveal" data-section="productivity">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(16,185,129,.1)">📋</div>
        <span class="cat-title">Productivity & Organisation</span>
        <span class="cat-count">5 tools</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="productivity" data-name="notion ai notes workspace student study plan"><div class="card-top"><div class="card-icon" style="background:rgba(0,0,0,.06)">📓</div><div><div class="card-name">Notion AI</div><div class="card-tag">Notes · Study Plans · Organisation</div></div></div><p class="card-desc">AI-powered workspace to organise all your notes, assignments and deadlines. Summarise lecture notes, create study plans and manage your entire semester in one place.</p><div class="card-footer"><a href="https://notion.so" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-freemium">Freemium</span><button class="btn-fav" data-tool="notion">🤍</button></div></div>

        <div class="tool-card" data-cat="productivity" data-name="todoist task management student schedule deadline"><div class="card-top"><div class="card-icon" style="background:rgba(239,68,68,.1)">✅</div><div><div class="card-name">Todoist AI</div><div class="card-tag">Task Management · Deadlines</div></div></div><p class="card-desc">AI-powered task manager that helps you organise assignments, project deadlines and exam schedules. Never miss a submission deadline again as a student.</p><div class="card-footer"><a href="https://todoist.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="todoist">🤍</button></div></div>

        <div class="tool-card" data-cat="productivity" data-name="focusmate accountability study partner pomodoro"><div class="card-top"><div class="card-icon" style="background:rgba(245,158,11,.1)">⏱️</div><div><div class="card-name">Focusmate</div><div class="card-tag">Study Accountability · Focus</div></div></div><p class="card-desc">Study with a real accountability partner online. Book a session, show up and work together silently. Proven to dramatically increase student focus and productivity.</p><div class="card-footer"><a href="https://focusmate.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="focusmate">🤍</button></div></div>

        <div class="tool-card" data-cat="productivity" data-name="google calendar schedule study timetable student"><div class="card-top"><div class="card-icon" style="background:rgba(66,133,244,.1)">📅</div><div><div class="card-name">Google Calendar</div><div class="card-tag">Schedule · Study Timetable</div></div></div><p class="card-desc">Plan your entire study schedule with AI suggestions. Set exam reminders, block study time and manage all your college deadlines in one organised calendar.</p><div class="card-footer"><a href="https://calendar.google.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="gcal">🤍</button></div></div>

        <div class="tool-card" data-cat="productivity" data-name="motion ai calendar planner schedule student"><div class="card-top"><div class="card-icon" style="background:rgba(168,85,247,.1)">🗓️</div><div><div class="card-name">Motion AI</div><div class="card-tag">AI Planner · Auto Schedule</div></div></div><p class="card-desc">AI automatically schedules your tasks and study sessions based on your deadlines and priorities. Builds your perfect daily timetable without any effort from you.</p><div class="card-footer"><a href="https://usemotion.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-paid">Paid</span><button class="btn-fav" data-tool="motion">🤍</button></div></div>
      </div>
    </div>

    <!-- EARN MONEY TOOLS -->
    <div class="cat-group reveal" data-section="earn">
      <div class="cat-header">
        <div class="cat-icon" style="background:rgba(193,127,36,.1)">💰</div>
        <span class="cat-title">Earn Money as a Student</span>
        <span class="cat-count">5 tools</span>
        <span class="cat-tag">Student Income</span>
      </div>
      <div class="tools-grid">
        <div class="tool-card" data-cat="earn" data-name="fiverr freelance earn money student gig"><div class="card-top"><div class="card-icon" style="background:rgba(16,185,129,.1)">💼</div><div><div class="card-name">Fiverr</div><div class="card-tag">Freelance · Sell Services</div></div></div><p class="card-desc">Sell your skills as a student — website building, content writing, design, AI tools setup. Create a gig and earn ₹3,000-₹50,000 per project from home.</p><div class="card-footer"><a href="https://fiverr.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free to Join</span><button class="btn-fav" data-tool="fiverr">🤍</button></div></div>

        <div class="tool-card" data-cat="earn" data-name="internshala internship freelance student india"><div class="card-top"><div class="card-icon" style="background:rgba(239,68,68,.1)">🎓</div><div><div class="card-name">Internshala <span class="badge-new">India</span></div><div class="card-tag">Internships · Freelance · India</div></div></div><p class="card-desc">India's best platform for student internships and freelance work. Find paid internships, part-time jobs and freelance projects specifically for Indian students.</p><div class="card-footer"><a href="https://internshala.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="internshala">🤍</button></div></div>

        <div class="tool-card" data-cat="earn" data-name="hashnode blog earn money student writing"><div class="card-top"><div class="card-icon" style="background:rgba(30,58,110,.1)">✍️</div><div><div class="card-name">Hashnode</div><div class="card-tag">Tech Blog · Earn from Writing</div></div></div><p class="card-desc">Start a free tech blog and earn money through affiliate links, sponsorships and AdSense. Best platform for student bloggers writing about AI and technology topics.</p><div class="card-footer"><a href="https://hashnode.com" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free</span><button class="btn-fav" data-tool="hashnode">🤍</button></div></div>

        <div class="tool-card" data-cat="earn" data-name="canva affiliate earn commission design student"><div class="card-top"><div class="card-icon" style="background:rgba(0,197,168,.1)">💳</div><div><div class="card-name">Canva Affiliates</div><div class="card-tag">Earn Commission · Affiliate</div></div></div><p class="card-desc">Recommend Canva to others and earn 80% of their first payment as commission. Students can earn ₹5,000+ per month just by sharing their Canva affiliate link.</p><div class="card-footer"><a href="https://canva.com/affiliates" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free to Join</span><button class="btn-fav" data-tool="canvaaffiliate">🤍</button></div></div>

        <div class="tool-card" data-cat="earn" data-name="grammarly affiliate earn commission writing student"><div class="card-top"><div class="card-icon" style="background:rgba(22,160,133,.1)">💰</div><div><div class="card-name">Grammarly Affiliates</div><div class="card-tag">Earn $20 Per Sale</div></div></div><p class="card-desc">Earn $20 for every student who buys Grammarly Premium through your link. Perfect passive income for students who blog or post on LinkedIn about AI tools.</p><div class="card-footer"><a href="https://grammarly.com/affiliates" target="_blank" class="btn-visit">Visit ↗</a><span class="badge-free">Free to Join</span><button class="btn-fav" data-tool="grammarlyaffiliate">🤍</button></div></div>
      </div>
    </div>

    <div id="noResults">😕 No tools found. Try a different search!</div>
  </div>
</section>

<!-- FAVOURITES -->
<section class="favs-sec" id="favs">
  <div class="sec-header reveal">
    <h2 class="sec-title">Your <em>Favourites</em></h2>
    <span class="count-pill" id="favPill">0 saved</span>
  </div>
  <div class="tools-grid" id="favsGrid">
    <p class="fav-empty">Click 🤍 on any tool to save it here!</p>
  </div>
</section>

<!-- PROMPTS -->
<section class="prompts-sec" id="prompts">
  <div class="sec-header reveal">
    <h2 class="sec-title">Study <em>Prompts</em></h2>
    <span class="count-pill">Copy & Use Now</span>
  </div>
  <div class="prompts-grid">
    <div class="prompt-card reveal"><div class="prompt-label">Explain Concept</div><p class="prompt-text">Explain [topic] like I am a complete beginner. Use one simple real world example I can relate to as a student.</p><button class="btn-copy" onclick="copyP(this,'Explain [topic] like I am a complete beginner. Use one simple real world example I can relate to as a student.')">Copy</button></div>
    <div class="prompt-card reveal"><div class="prompt-label">Exam Preparation</div><p class="prompt-text">Create 15 practice questions with answers for my [subject] exam. Include easy, medium and hard difficulty questions.</p><button class="btn-copy" onclick="copyP(this,'Create 15 practice questions with answers for my [subject] exam. Include easy, medium and hard difficulty questions.')">Copy</button></div>
    <div class="prompt-card reveal"><div class="prompt-label">Debug My Code</div><p class="prompt-text">Find the bug in this code, explain what went wrong in simple words and show me the corrected version: [paste code]</p><button class="btn-copy" onclick="copyP(this,'Find the bug in this code, explain what went wrong in simple words and show me the corrected version: [paste code]')">Copy</button></div>
    <div class="prompt-card reveal"><div class="prompt-label">Study Plan</div><p class="prompt-text">Create a 7-day study plan for my [subject] exam covering [topics]. Include daily goals and 15-minute revision sessions.</p><button class="btn-copy" onclick="copyP(this,'Create a 7-day study plan for my [subject] exam covering [topics]. Include daily goals and 15-minute revision sessions.')">Copy</button></div>
    <div class="prompt-card reveal"><div class="prompt-label">Summarize Notes</div><p class="prompt-text">Summarize these lecture notes into the 5 most important points I must remember for my exam: [paste notes]</p><button class="btn-copy" onclick="copyP(this,'Summarize these lecture notes into the 5 most important points I must remember for my exam: [paste notes]')">Copy</button></div>
    <div class="prompt-card reveal"><div class="prompt-label">Assignment Help</div><p class="prompt-text">I need to write a [word count] report on [topic]. Give me a complete outline with 5 sections and key points for each section.</p><button class="btn-copy" onclick="copyP(this,'I need to write a [word count] report on [topic]. Give me a complete outline with 5 sections and key points for each section.')">Copy</button></div>
  </div>
</section>

<!-- TIPS -->
<section class="tips-sec" id="tips">
  <div class="sec-header reveal">
    <h2 class="sec-title">Smart Student <em>Tips</em></h2>
    <span class="count-pill">Pro Tips</span>
  </div>
  <div class="tips-grid">
    <div class="tip-card reveal"><div class="tip-num">01</div><div class="tip-title">Use AI to Learn — Not Just to Get Answers</div><p class="tip-body">When AI explains something, read it carefully and ask follow-up questions. Understanding beats copy-pasting every single time.</p></div>
    <div class="tip-card reveal"><div class="tip-num">02</div><div class="tip-title">30 Minutes Daily Beats 5 Hours on Sunday</div><p class="tip-body">Practice coding or learning AI tools for just 30 minutes every day. Consistency creates skills — cramming does not.</p></div>
    <div class="tip-card reveal"><div class="tip-num">03</div><div class="tip-title">Upload Lecture Notes to NotebookLM</div><p class="tip-body">Before every exam, upload all your notes to NotebookLM and chat with them. Ask it to quiz you. This alone can improve your grades significantly.</p></div>
    <div class="tip-card reveal"><div class="tip-num">04</div><div class="tip-title">Build Projects — Not Just Tutorials</div><p class="tip-body">After every tutorial you watch, build something with what you learned. Real projects teach you 10x more than watching alone.</p></div>
    <div class="tip-card reveal"><div class="tip-num">05</div><div class="tip-title">Start Your Blog as a 2nd Year Student</div><p class="tip-body">Write about what you learn each week. Even one post per week builds a portfolio, personal brand and passive income over time.</p></div>
    <div class="tip-card reveal"><div class="tip-num">06</div><div class="tip-title">Know Tools Early — Stay 2 Years Ahead</div><p class="tip-body">The students who know today's AI tools are 2-3 years ahead of everyone else. Explore one new tool every single week without fail.</p></div>
  </div>
</section>

<!-- QUOTE -->
<section class="quote-sec">
  <div class="quote-inner reveal">
    <div class="quote-mark">"</div>
    <p class="quote-text">The skill is not just knowing how to code — it is knowing <em>what to build</em> and using AI to build it.</p>
    <p class="quote-sub">Start today. The future belongs to students who act early.</p>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div>
    <div class="footer-brand">⚡ AI Tools for Students</div>
    <p>© 2026 · Made with ❤️ for students everywhere · Karnataka, India</p>
  </div>
  <div class="footer-links">
    <a href="#tools">Tools</a>
    <a href="#prompts">Prompts</a>
    <a href="#tips">Tips</a>
    <a href="https://usingaitoolsasstudent.blogspot.com" target="_blank">Blog</a>
  </div>
</footer>

<script>
// NAV
const hamburger = document.getElementById('hamburger');
const navLinks = document.getElementById('navLinks');
hamburger.addEventListener('click', () => navLinks.classList.toggle('open'));
document.querySelectorAll('.nav-links a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

// TOAST
function toast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2400);
}

// SEARCH + FILTER
const searchInput = document.getElementById('search');
const catGroups = document.querySelectorAll('.cat-group');
let activeFilter = 'all';

function filterTools() {
  const q = searchInput.value.toLowerCase().trim();
  let total = 0;
  catGroups.forEach(group => {
    const sec = group.dataset.section;
    const cards = group.querySelectorAll('.tool-card');
    let visible = 0;
    cards.forEach(card => {
      const name = (card.dataset.name || '').toLowerCase();
      const text = card.textContent.toLowerCase();
      const cat = card.dataset.cat || '';
      const matchQ = !q || name.includes(q) || text.includes(q);
      const matchF = activeFilter === 'all' || cat === activeFilter || sec === activeFilter;
      const show = matchQ && matchF;
      card.classList.toggle('hidden', !show);
      if (show) { visible++; total++; }
    });
    group.style.display = visible === 0 ? 'none' : '';
  });
  document.getElementById('noResults').classList.toggle('show', total === 0);
}

searchInput.addEventListener('input', filterTools);
document.querySelectorAll('.filter-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    activeFilter = btn.dataset.cat;
    filterTools();
  });
});

// FAVOURITES
const favs = new Set();
function updateFavs() {
  const count = favs.size;
  document.getElementById('favPill').textContent = count + ' saved';
  document.getElementById('statFavs').textContent = count;
  const grid = document.getElementById('favsGrid');
  grid.innerHTML = '';
  if (count === 0) { grid.innerHTML = '<p class="fav-empty">Click 🤍 on any tool to save it here!</p>'; return; }
  favs.forEach(tool => {
    const orig = document.querySelector(`.tool-card [data-tool="${tool}"]`)?.closest('.tool-card');
    if (orig) {
      const clone = orig.cloneNode(true);
      clone.classList.remove('hidden');
      const fb = clone.querySelector('.btn-fav');
      if (fb) fb.remove();
      grid.appendChild(clone);
    }
  });
}

document.addEventListener('click', e => {
  const btn = e.target.closest('.btn-fav');
  if (!btn) return;
  const tool = btn.dataset.tool;
  if (favs.has(tool)) {
    favs.delete(tool);
    btn.textContent = '🤍';
    btn.classList.remove('faved');
    toast('Removed from favourites');
  } else {
    favs.add(tool);
    btn.textContent = '❤️';
    btn.classList.add('faved');
    toast('Saved to favourites ❤️');
  }
  updateFavs();
});

// COPY PROMPT
function copyP(btn, text) {
  navigator.clipboard.writeText(text).then(() => {
    const orig = btn.textContent;
    btn.textContent = '✓ Copied!';
    btn.classList.add('copied');
    toast('Prompt copied! 📋');
    setTimeout(() => { btn.textContent = orig; btn.classList.remove('copied'); }, 2000);
  });
}

// BACK TO TOP
const backTop = document.getElementById('backTop');
window.addEventListener('scroll', () => backTop.classList.toggle('show', window.scrollY > 400));
backTop.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));

// SCROLL REVEAL
const observer = new IntersectionObserver(entries => {
  entries.forEach((entry, i) => {
    if (entry.isIntersecting) {
      setTimeout(() => entry.target.classList.add('visible'), i * 70);
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.08 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
