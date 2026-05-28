<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lori Hurwitz — Chief of Staff · Iterative Health</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,400&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--p:#5B3CC4;--p2:#7B5CE4;--light:#F4F2FD;--border:#E2DDF5;--muted:#6B6780;--dark:#1C1B2E;--white:#fff}
body{font-family:'DM Sans',system-ui,sans-serif;background:#fff;color:var(--dark);min-height:100vh}

/* HEADER */
.topbar{background:var(--p);padding:11px 40px;display:flex;align-items:center;justify-content:space-between}
.topbar-title{color:#fff;font-size:11px;letter-spacing:0.1em;text-transform:uppercase;font-weight:600}
.topbar-date{color:rgba(255,255,255,0.5);font-size:11px}

/* HERO */
.hero{padding:52px 40px 40px;max-width:800px;margin:0 auto}
.hero-tag{display:inline-block;background:var(--light);color:var(--p);font-size:11px;font-weight:600;letter-spacing:0.08em;text-transform:uppercase;padding:5px 12px;border-radius:20px;margin-bottom:20px}
.hero h1{font-size:36px;font-weight:600;color:var(--dark);line-height:1.2;margin-bottom:16px}
.hero h1 span{color:var(--p)}
.hero-sub{font-size:16px;color:var(--muted);line-height:1.7;max-width:580px;margin-bottom:32px}
.memo-block{display:flex;flex-direction:column;gap:6px;background:var(--light);border-radius:10px;padding:18px 22px;border-left:3px solid var(--p);max-width:480px}
.memo-row{display:flex;gap:16px}
.memo-label{font-size:12px;color:var(--muted);font-weight:500;min-width:40px}
.memo-value{font-size:12px;color:var(--dark)}

/* TABS */
.tabs-wrap{border-bottom:1px solid var(--border);position:sticky;top:0;background:#fff;z-index:10}
.tabs{display:flex;gap:0;max-width:800px;margin:0 auto;padding:0 40px}
.tab{padding:14px 20px;font-size:13px;font-weight:500;color:var(--muted);cursor:pointer;border-bottom:2px solid transparent;transition:all 0.2s;white-space:nowrap;background:none;border-top:none;border-left:none;border-right:none;font-family:inherit}
.tab:hover{color:var(--dark)}
.tab.active{color:var(--p);border-bottom-color:var(--p)}

/* CONTENT */
.content{max-width:800px;margin:0 auto;padding:40px 40px 80px}
.panel{display:none}
.panel.active{display:block}

/* SECTION LABEL */
.slabel{font-size:10px;letter-spacing:0.12em;text-transform:uppercase;color:var(--p);font-weight:600;margin-bottom:12px}

/* SKILLS GRID */
.skills-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin-bottom:40px}
.skill-card{border:1px solid var(--border);border-radius:12px;padding:22px;cursor:pointer;transition:all 0.2s;position:relative;overflow:hidden}
.skill-card:hover,.skill-card.active{border-color:var(--p);background:var(--light)}
.skill-card.active .skill-expand{display:block}
.skill-num{font-size:28px;font-weight:600;color:var(--p);line-height:1;margin-bottom:4px}
.skill-unit{font-size:12px;color:var(--muted);margin-bottom:12px}
.skill-title{font-size:14px;font-weight:500;color:var(--dark);margin-bottom:6px}
.skill-preview{font-size:12px;color:var(--muted);line-height:1.5}
.skill-expand{display:none;font-size:12px;color:var(--muted);line-height:1.6;margin-top:12px;padding-top:12px;border-top:1px solid var(--border)}
.skill-tag{display:inline-block;background:#fff;border:1px solid var(--border);color:var(--muted);font-size:10px;padding:3px 8px;border-radius:4px;margin:3px 3px 0 0;font-weight:500}

/* WHAT I BUILD */
.build-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px;margin-bottom:40px}
.build-item{background:var(--light);border-radius:10px;padding:18px 20px}
.build-icon{font-size:20px;margin-bottom:10px}
.build-title{font-size:13px;font-weight:600;color:var(--dark);margin-bottom:6px}
.build-desc{font-size:12px;color:var(--muted);line-height:1.55}

/* TIMELINE */
.timeline{position:relative;padding-left:24px;border-left:2px solid var(--border)}
.titem{position:relative;margin-bottom:32px;cursor:pointer}
.titem:last-child{margin-bottom:0}
.tdot{width:10px;height:10px;border-radius:50%;background:var(--border);border:2px solid #fff;position:absolute;left:-29px;top:4px;transition:background 0.2s}
.titem.active .tdot,.titem:hover .tdot{background:var(--p)}
.trange{font-size:10px;color:var(--p);font-weight:600;letter-spacing:0.06em;margin-bottom:3px}
.taction{font-size:14px;font-weight:500;color:var(--dark);margin-bottom:4px}
.tdetail{font-size:13px;color:var(--muted);line-height:1.6;max-height:0;overflow:hidden;transition:max-height 0.3s ease}
.titem.active .tdetail{max-height:200px}
.texpand{font-size:11px;color:var(--p);margin-top:4px;font-weight:500}

/* EXPERIENCE */
.exp-list{display:flex;flex-direction:column;gap:16px}
.exp-item{border:1px solid var(--border);border-radius:10px;padding:20px 22px}
.exp-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:8px}
.exp-role{font-size:14px;font-weight:600;color:var(--dark)}
.exp-co{font-size:13px;color:var(--p);font-weight:500}
.exp-date{font-size:11px;color:var(--muted)}
.exp-desc{font-size:13px;color:var(--muted);line-height:1.6}
.exp-tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:10px}
.etag{background:var(--light);color:var(--p);font-size:11px;padding:3px 10px;border-radius:4px;font-weight:500}

/* GAP BOX */
.gap-box{background:var(--light);border-radius:12px;padding:24px 28px;border-left:3px solid var(--p);margin-bottom:32px}
.gap-box p{font-size:14px;color:var(--dark);line-height:1.75}

/* CTA */
.cta-bar{background:var(--p);border-radius:12px;padding:28px 32px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;margin-top:40px}
.cta-name{font-size:16px;font-weight:600;color:#fff;margin-bottom:3px}
.cta-sub{font-size:13px;color:rgba(255,255,255,0.65)}
.cta-links{display:flex;gap:10px}
.btn-white{background:#fff;color:var(--p);padding:10px 18px;border-radius:8px;font-size:13px;font-weight:600;text-decoration:none;font-family:inherit}
.btn-outline{border:1px solid rgba(255,255,255,0.35);color:#fff;padding:10px 18px;border-radius:8px;font-size:13px;font-weight:500;text-decoration:none;font-family:inherit}

/* STAT ROW */
.stat-row{display:flex;gap:24px;flex-wrap:wrap;margin-bottom:36px}
.stat{text-align:left}
.stat-num{font-size:26px;font-weight:600;color:var(--p)}
.stat-label{font-size:11px;color:var(--muted);margin-top:2px}

@media(max-width:600px){
  .hero{padding:32px 20px 28px}
  .tabs{padding:0 20px;overflow-x:auto}
  .content{padding:28px 20px 60px}
  .topbar{padding:11px 20px}
  .cta-bar{flex-direction:column;align-items:flex-start}
}
</style>
</head>
<body>

<div class="topbar">
  <span class="topbar-title">Chief of Staff Application</span>
  <span class="topbar-date">Iterative Health · May 2026</span>
</div>

<div class="hero">
  <div class="hero-tag">For: Jonathan Ng, CEO</div>
  <h1>I want to be your<br><span>Chief of Staff.</span></h1>
  <p class="hero-sub">You just closed a $77M Series C, acquired three cardiology sites, and added GV and Intrepid to your board. The next 18 months are the hardest ones to run. Here's why I'm the right operator for them.</p>
  <div class="memo-block">
    <div class="memo-row"><span class="memo-label">To</span><span class="memo-value">Jonathan Ng, Founder & CEO</span></div>
    <div class="memo-row"><span class="memo-label">From</span><span class="memo-value">Lori Hurwitz, Columbia MBA '26</span></div>
    <div class="memo-row"><span class="memo-label">Re</span><span class="memo-value">Chief of Staff — Why Now, Why Me</span></div>
  </div>
</div>

<div class="tabs-wrap">
  <div class="tabs">
    <button class="tab active" onclick="showTab('skills')">The Match</button>
    <button class="tab" onclick="showTab('build')">What I Build</button>
    <button class="tab" onclick="showTab('days')">First 90 Days</button>
    <button class="tab" onclick="showTab('experience')">Experience</button>
    <button class="tab" onclick="showTab('gap')">On the Gap</button>
  </div>
</div>

<div class="content">

  <!-- TAB: THE MATCH -->
  <div class="panel active" id="panel-skills">
    <div class="slabel">Why I fit the role</div>
    <div class="stat-row">
      <div class="stat"><div class="stat-num">$1.2B+</div><div class="stat-label">M&A deal value</div></div>
      <div class="stat"><div class="stat-num">0→1</div><div class="stat-label">platforms built</div></div>
      <div class="stat"><div class="stat-num">2 sides</div><div class="stat-label">operator + investor</div></div>
      <div class="stat"><div class="stat-num">Day 1</div><div class="stat-label">AI-native</div></div>
    </div>
    <p style="font-size:13px;color:var(--muted);margin-bottom:20px">Click any card to expand.</p>
    <div class="skills-grid">
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">$1.2B+</div>
        <div class="skill-unit">in transactions closed</div>
        <div class="skill-title">Deal execution at scale</div>
        <div class="skill-preview">RBI + LiveRamp M&A across three landmark deals</div>
        <div class="skill-expand">
          Led or supported the $1B Firehouse Subs acquisition at RBI and the $200M Habu deal at LiveRamp — cross-functional coordination, board communications, and integration planning under real deadline pressure. The NextStage cardiology acquisition just closed. This is muscle memory.
          <div style="margin-top:10px">
            <span class="skill-tag">M&A diligence</span>
            <span class="skill-tag">Integration planning</span>
            <span class="skill-tag">Board comms</span>
            <span class="skill-tag">Cross-functional PM</span>
          </div>
        </div>
      </div>
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">0→1</div>
        <div class="skill-unit">new function built</div>
        <div class="skill-title">Stood up new platforms</div>
        <div class="skill-preview">Built LiveRamp's inaugural venture arm from scratch</div>
        <div class="skill-expand">
          No roadmap. Defined the thesis, built the operating model, and managed cross-functional stakeholders from day one. Chief of Staff is fundamentally a 0→1 operating role — designing systems that don't exist yet, under pressure. I've done that.
          <div style="margin-top:10px">
            <span class="skill-tag">Thesis development</span>
            <span class="skill-tag">Operating model design</span>
            <span class="skill-tag">Stakeholder alignment</span>
          </div>
        </div>
      </div>
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">Day 1</div>
        <div class="skill-unit">AI-native operator</div>
        <div class="skill-title">Builds with AI, not just about it</div>
        <div class="skill-preview">Daily stack: Claude, Granola, Wispr Flow, Loveable, Zo</div>
        <div class="skill-expand">
          I've built an AI deal-sourcing agent, a consumer app (Pawdy), and automated my own research workflows. IH's moat is proprietary AI — I can translate between engineering, clinical ops, and the C-suite in a way most CoS candidates can't.
          <div style="margin-top:10px">
            <span class="skill-tag">AI agent building</span>
            <span class="skill-tag">Product development</span>
            <span class="skill-tag">Workflow automation</span>
            <span class="skill-tag">Claude · Loveable · Zo</span>
          </div>
        </div>
      </div>
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">2</div>
        <div class="skill-unit">funds — operator + investor</div>
        <div class="skill-title">Board-ready by default</div>
        <div class="skill-preview">Amex Ventures + The 98 — board narratives, memos, comms</div>
        <div class="skill-expand">
          Worked both sides of the table — operator (RBI, LiveRamp) and investor (Amex Ventures, The 98). Built board narratives, investment memos, and sponsor-facing materials. Series C board engagement and investor comms are core CoS deliverables — this is familiar ground.
          <div style="margin-top:10px">
            <span class="skill-tag">Board materials</span>
            <span class="skill-tag">Investment memos</span>
            <span class="skill-tag">Investor relations</span>
            <span class="skill-tag">Executive comms</span>
          </div>
        </div>
      </div>
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">5+</div>
        <div class="skill-unit">years high-velocity ops</div>
        <div class="skill-title">Strategy & operations backbone</div>
        <div class="skill-preview">Corp dev, venture investing, and operator roles back to back</div>
        <div class="skill-expand">
          Corporate development at Restaurant Brands International and LiveRamp, CVC investing at Amex Ventures, early-stage at The 98 — each role required rapid context-switching, stakeholder management at every level, and delivering work that reached the C-suite and board.
          <div style="margin-top:10px">
            <span class="skill-tag">Corp dev</span>
            <span class="skill-tag">Venture investing</span>
            <span class="skill-tag">Financial modeling</span>
            <span class="skill-tag">Strategic analysis</span>
          </div>
        </div>
      </div>
      <div class="skill-card" onclick="toggleSkill(this)">
        <div class="skill-num">MBA</div>
        <div class="skill-unit">Columbia Business School '26</div>
        <div class="skill-title">Trained to operate at the top</div>
        <div class="skill-preview">Co-organized Columbia's inaugural Restaurant & CPG Innovation Summit</div>
        <div class="skill-expand">
          Columbia Business School Class of 2026 — with coursework and projects spanning strategy, operations, and venture. Built and ran Columbia's first Restaurant & CPG Innovation Summit in April 2026 as an example of the kind of cross-functional event production a CoS owns routinely.
          <div style="margin-top:10px">
            <span class="skill-tag">Event production</span>
            <span class="skill-tag">Community building</span>
            <span class="skill-tag">Strategy coursework</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- TAB: WHAT I BUILD -->
  <div class="panel" id="panel-build">
    <div class="slabel">Proof of work</div>
    <p style="font-size:15px;line-height:1.75;color:var(--dark);margin-bottom:28px">Most CoS candidates can make decks. I also build things. Here's a sample of what I've shipped.</p>
    <div class="build-grid">
      <div class="build-item">
        <div class="build-icon">🐾</div>
        <div class="build-title">Pawdy</div>
        <div class="build-desc">Consumer puppy prep app — wireframes, payment flow, UX research, full persona development. Built end-to-end as a product project.</div>
      </div>
      <div class="build-item">
        <div class="build-icon">🤖</div>
        <div class="build-title">AI Deal-Sourcing Agent</div>
        <div class="build-desc">Built an AI agent via Zo Computer for autonomous deal sourcing — surfaces companies matching a thesis, outputs structured research.</div>
      </div>
      <div class="build-item">
        <div class="build-icon">🌐</div>
        <div class="build-title">lorihurwitz.xyz</div>
        <div class="build-desc">Personal site built in Next.js 15 + Tailwind CSS — six pages covering bio, resume, and investment theses. Deployed and maintained independently.</div>
      </div>
      <div class="build-item">
        <div class="build-icon">📊</div>
        <div class="build-title">Investment Thesis Work</div>
        <div class="build-desc">Developed three original frameworks: Personal Health OS, User-Embedded Social, and Fashion Decision Layer — each with full market maps and deal sourcing.</div>
      </div>
      <div class="build-item">
        <div class="build-icon">🎤</div>
        <div class="build-title">Restaurant & CPG Summit</div>
        <div class="build-desc">Co-organized Columbia Business School's inaugural Restaurant & CPG Innovation Summit, April 2026 — end-to-end event production and speaker coordination.</div>
      </div>
      <div class="build-item">
        <div class="build-icon">⚡</div>
        <div class="build-title">This Page</div>
        <div class="build-desc">Built with Claude as a CoS application artifact — because sending a PDF felt like a missed opportunity to show rather than tell.</div>
      </div>
    </div>
    <div style="background:var(--light);border-radius:10px;padding:20px 24px;border-left:3px solid var(--p)">
      <div class="slabel" style="margin-bottom:8px">Daily AI stack</div>
      <div style="display:flex;flex-wrap:wrap;gap:8px">
        <span class="etag">Claude</span>
        <span class="etag">Granola</span>
        <span class="etag">Wispr Flow</span>
        <span class="etag">Zo Computer</span>
        <span class="etag">Loveable</span>
        <span class="etag">Cursor</span>
      </div>
    </div>
  </div>

  <!-- TAB: FIRST 90 DAYS -->
  <div class="panel" id="panel-days">
    <div class="slabel">What I'd actually do</div>
    <p style="font-size:15px;line-height:1.75;color:var(--dark);margin-bottom:32px">Click each phase to expand the plan.</p>
    <div class="timeline">
      <div class="titem active" onclick="toggleDay(this)">
        <div class="tdot"></div>
        <div class="trange">Days 1–30</div>
        <div class="taction">Listen and map</div>
        <div class="tdetail">Shadow every exec team member. Audit the operating cadence — what meetings exist, what decisions get made where, what is falling through the cracks at Series C scale. No agenda except to understand. Deliver a gaps memo to the CEO at day 30.</div>
        <div class="texpand">↑ collapse</div>
      </div>
      <div class="titem" onclick="toggleDay(this)">
        <div class="tdot"></div>
        <div class="trange">Days 31–60</div>
        <div class="taction">Own the cardiology integration</div>
        <div class="tdetail">The NextStage acquisition just closed. Three Texas sites — Beaumont, Port Arthur, Waco — need an onboarding playbook: centralized ops integration, SKOUT AI tools adoption, sponsor pipeline alignment. I own the PM layer so clinical leadership stays focused on site quality and trial execution.</div>
        <div class="texpand">↓ expand</div>
      </div>
      <div class="titem" onclick="toggleDay(this)">
        <div class="tdot"></div>
        <div class="trange">Days 61–90</div>
        <div class="taction">Build the operating rhythm</div>
        <div class="tdetail">Stand up the quarterly planning cadence, KPI framework, and board reporting infrastructure for the new scale post-Series C. Build the template layer so the CEO is not rebuilding it from scratch for every board cycle or investor update.</div>
        <div class="texpand">↓ expand</div>
      </div>
      <div class="titem" onclick="toggleDay(this)">
        <div class="tdot"></div>
        <div class="trange">90 Days+</div>
        <div class="taction">Become the connective tissue</div>
        <div class="tdetail">The best CoS becomes invisible infrastructure — decisions move faster, the CEO's time goes to the right places, and the organization trusts that things won't fall through the cracks. That's the job. I want to earn that role.</div>
        <div class="texpand">↓ expand</div>
      </div>
    </div>
  </div>

  <!-- TAB: EXPERIENCE -->
  <div class="panel" id="panel-experience">
    <div class="slabel">Where I've been</div>
    <div class="exp-list">
      <div class="exp-item">
        <div class="exp-header">
          <div>
            <div class="exp-role">Corporate Development</div>
            <div class="exp-co">Restaurant Brands International</div>
          </div>
          <div class="exp-date">Pre-MBA</div>
        </div>
        <div class="exp-desc">Supported the $1B acquisition of Firehouse Subs — one of the largest QSR deals of the year. End-to-end involvement in diligence, deal structuring, and cross-functional coordination across legal, finance, and operations teams.</div>
        <div class="exp-tags">
          <span class="etag">M&A</span><span class="etag">Diligence</span><span class="etag">Deal structuring</span><span class="etag">Integration</span>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-header">
          <div>
            <div class="exp-role">Corporate Development + Venture</div>
            <div class="exp-co">LiveRamp</div>
          </div>
          <div class="exp-date">Pre-MBA</div>
        </div>
        <div class="exp-desc">Supported the $200M acquisition of Habu. Helped stand up LiveRamp's inaugural venture arm from scratch — defining the investment thesis, building the operating model, and sourcing early-stage companies.</div>
        <div class="exp-tags">
          <span class="etag">M&A</span><span class="etag">0→1 platform</span><span class="etag">Venture</span><span class="etag">Thesis development</span>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-header">
          <div>
            <div class="exp-role">CVC Investor</div>
            <div class="exp-co">Amex Ventures</div>
          </div>
          <div class="exp-date">Pre-MBA</div>
        </div>
        <div class="exp-desc">Early-stage and growth investing at American Express's corporate venture arm. Investment memos, board materials, portfolio monitoring, and strategic analysis across fintech and consumer technology.</div>
        <div class="exp-tags">
          <span class="etag">CVC</span><span class="etag">Investment memos</span><span class="etag">Board materials</span><span class="etag">Fintech</span>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-header">
          <div>
            <div class="exp-role">Investor</div>
            <div class="exp-co">The 98</div>
          </div>
          <div class="exp-date">Pre-MBA</div>
        </div>
        <div class="exp-desc">Early-stage consumer venture investing. Deal sourcing, founder relationships, and thesis development across consumer, fashion tech, and AI-native applications.</div>
        <div class="exp-tags">
          <span class="etag">Early-stage VC</span><span class="etag">Consumer</span><span class="etag">Deal sourcing</span><span class="etag">Thesis</span>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-header">
          <div>
            <div class="exp-role">MBA</div>
            <div class="exp-co">Columbia Business School</div>
          </div>
          <div class="exp-date">Class of 2026</div>
        </div>
        <div class="exp-desc">Co-organized Columbia's inaugural Restaurant & CPG Innovation Summit (April 2026). Investment thesis development across healthcare AI, consumer, and fashion tech. Adobe equity research (BUY recommendation). LVS capstone case presentation.</div>
        <div class="exp-tags">
          <span class="etag">Strategy</span><span class="etag">Operations</span><span class="etag">Event production</span><span class="etag">Research</span>
        </div>
      </div>
    </div>
  </div>

  <!-- TAB: ON THE GAP -->
  <div class="panel" id="panel-gap">
    <div class="slabel">The honest case</div>
    <div class="gap-box">
      <p>I don't have clinical research experience. I'm naming it directly because I think a CoS should be direct about what they don't know.</p>
    </div>
    <p style="font-size:15px;line-height:1.75;color:var(--dark);margin-bottom:20px">What I do have is a demonstrated track record of learning new domains quickly and operating inside them with rigor. At RBI I learned QSR operations. At LiveRamp I learned data infrastructure and adtech. At Amex Ventures I learned fintech. Each time, the pattern was the same: show up, learn fast, earn trust, deliver.</p>
    <p style="font-size:15px;line-height:1.75;color:var(--dark);margin-bottom:20px">The skills that make a Chief of Staff effective — problem structuring, stakeholder alignment, executive communication, running complex multi-threaded initiatives — are domain-agnostic. They transfer.</p>
    <p style="font-size:15px;line-height:1.75;color:var(--dark);margin-bottom:32px">The IH-specific context — clinical trial execution, site network operations, sponsor relationships, therapeutic area strategy — I will learn. Fast. I'm asking for the chance to prove that.</p>
    <div style="background:var(--light);border-radius:10px;padding:20px 24px">
      <div class="slabel" style="margin-bottom:12px">What I bring on Day 1</div>
      <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:10px">
        <div style="font-size:13px;color:var(--dark);display:flex;gap:8px;align-items:flex-start"><span style="color:var(--p);font-weight:600">→</span>M&A execution instincts (just closed = active)</div>
        <div style="font-size:13px;color:var(--dark);display:flex;gap:8px;align-items:flex-start"><span style="color:var(--p);font-weight:600">→</span>Board + investor communication fluency</div>
        <div style="font-size:13px;color:var(--dark);display:flex;gap:8px;align-items:flex-start"><span style="color:var(--p);font-weight:600">→</span>AI tooling that immediately improves ops efficiency</div>
        <div style="font-size:13px;color:var(--dark);display:flex;gap:8px;align-items:flex-start"><span style="color:var(--p);font-weight:600">→</span>Operating in ambiguity without needing a playbook</div>
      </div>
    </div>
  </div>

  <div class="cta-bar">
    <div>
      <div class="cta-name">Lori Hurwitz</div>
      <div class="cta-sub">Columbia Business School MBA '26 · New York, NY · lori@lorihurwitz.xyz</div>
    </div>
    <div class="cta-links">
      <a href="https://lorihurwitz.xyz" target="_blank" class="btn-white">lorihurwitz.xyz →</a>
      <a href="https://linkedin.com/in/lorihurwitz" target="_blank" class="btn-outline">LinkedIn</a>
    </div>
  </div>

</div>

<script>
function showTab(id) {
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
  event.currentTarget.classList.add('active');
  document.getElementById('panel-' + id).classList.add('active');
}
function toggleSkill(card) {
  const wasActive = card.classList.contains('active');
  document.querySelectorAll('.skill-card').forEach(c => c.classList.remove('active'));
  if (!wasActive) card.classList.add('active');
}
function toggleDay(item) {
  const wasActive = item.classList.contains('active');
  document.querySelectorAll('.titem').forEach(i => {
    i.classList.remove('active');
    i.querySelector('.texpand').textContent = '↓ expand';
  });
  if (!wasActive) {
    item.classList.add('active');
    item.querySelector('.texpand').textContent = '↑ collapse';
  }
}
</script>
</body>
</html># iterative-health
