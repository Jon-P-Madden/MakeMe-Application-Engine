<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TPM Application Engine</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#070b14;--surface:#0d1424;--card:#111d30;--card2:#162236;
  --border:#1e3050;--border2:#253d61;
  --amber:#f59e0b;--amber-h:#fbbf24;--amber-d:rgba(245,158,11,.12);--amber-d2:rgba(245,158,11,.06);
  --blue:#3b82f6;--blue-d:rgba(59,130,246,.12);
  --green:#10b981;--green-d:rgba(16,185,129,.12);
  --red:#ef4444;--red-d:rgba(239,68,68,.12);
  --purple:#a78bfa;--purple-d:rgba(167,139,250,.12);
  --text:#e2e8f0;--text-m:#94a3b8;--text-d:#4b6280;
  --mono:'JetBrains Mono',monospace;--sans:'Outfit',sans-serif;
  --r:8px;--rl:12px;
}
html,body{min-height:100vh;background:var(--bg);color:var(--text);font-family:var(--sans);font-size:14px;line-height:1.6}
::-webkit-scrollbar{width:5px;height:5px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:3px}

/* HEADER */
.hdr{display:flex;align-items:center;justify-content:space-between;padding:0 24px;height:58px;background:var(--surface);border-bottom:1px solid var(--border);position:sticky;top:0;z-index:100}
.logo{display:flex;align-items:center;gap:10px;font-size:15px;font-weight:600}
.logo-icon{width:30px;height:30px;background:var(--amber);border-radius:7px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0}
.logo-sub{color:var(--text-d);font-weight:400;font-size:12px;margin-left:2px}
.api-row{display:flex;align-items:center;gap:8px}
.api-dot{width:8px;height:8px;border-radius:50%;background:var(--text-d);flex-shrink:0;transition:background .3s}
.api-dot.ok{background:var(--green)}
.api-dot.bad{background:var(--red)}
.api-in{background:var(--card);border:1px solid var(--border);color:var(--text);padding:7px 12px;border-radius:var(--r);font-family:var(--mono);font-size:12px;width:290px;outline:none;transition:border-color .2s}
.api-in:focus{border-color:var(--amber)}
.api-in::placeholder{color:var(--text-d)}

/* TABS */
.tabs{display:flex;gap:2px;padding:0 24px;background:var(--surface);border-bottom:1px solid var(--border)}
.tb{padding:11px 18px;background:none;border:none;border-bottom:2px solid transparent;color:var(--text-m);font-family:var(--sans);font-size:13px;font-weight:500;cursor:pointer;transition:all .15s;display:flex;align-items:center;gap:7px}
.tb:hover{color:var(--text)}
.tb.on{color:var(--amber);border-bottom-color:var(--amber)}
.tbadge{background:var(--amber-d);color:var(--amber);font-size:10px;font-weight:600;padding:1px 7px;border-radius:10px;font-family:var(--mono)}

/* LAYOUT */
.main{padding:22px 24px;max-width:1360px;margin:0 auto}
.panel{display:none}
.panel.on{display:block}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px}
@media(max-width:900px){.g2,.g3{grid-template-columns:1fr}}

/* CARDS */
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--rl);padding:20px}
.ch{display:flex;align-items:center;justify-content:space-between;margin-bottom:16px;padding-bottom:12px;border-bottom:1px solid var(--border)}
.ct{font-size:11px;font-weight:600;color:var(--text-d);text-transform:uppercase;letter-spacing:.09em}

/* FORM ELEMENTS */
.lbl{display:block;font-size:11px;font-weight:500;color:var(--text-m);margin-bottom:5px;letter-spacing:.04em}
input[type=text],input[type=url],input[type=password],textarea,select{width:100%;background:var(--surface);border:1px solid var(--border);color:var(--text);padding:8px 11px;border-radius:var(--r);font-family:var(--sans);font-size:13px;outline:none;transition:border-color .15s;resize:vertical}
input[type=text]:focus,input[type=url]:focus,input[type=password]:focus,textarea:focus,select:focus{border-color:var(--amber)}
input::placeholder,textarea::placeholder{color:var(--text-d)}
select{appearance:none;cursor:pointer;background-image:url("data:image/svg+xml,%3Csvg width='10' height='6' viewBox='0 0 10 6' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1 1L5 5L9 1' stroke='%234b6280' stroke-width='1.5' stroke-linecap='round'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 10px center;padding-right:28px}
select option{background:var(--card)}

/* BUTTONS */
.btn{display:inline-flex;align-items:center;gap:6px;padding:8px 15px;border-radius:var(--r);font-family:var(--sans);font-size:13px;font-weight:500;cursor:pointer;border:none;transition:all .15s;white-space:nowrap}
.btn:disabled{opacity:.4;cursor:not-allowed}
.btn-p{background:var(--amber);color:#000}
.btn-p:hover:not(:disabled){background:var(--amber-h)}
.btn-o{background:transparent;color:var(--text);border:1px solid var(--border2)}
.btn-o:hover:not(:disabled){background:var(--card2);border-color:var(--amber);color:var(--amber)}
.btn-g{background:transparent;color:var(--text-m);border:none;padding:6px 10px}
.btn-g:hover:not(:disabled){color:var(--text);background:var(--card)}
.btn-s{padding:6px 12px;font-size:12px}
.btn-grn{background:var(--green-d);color:#6ee7b7;border:1px solid rgba(16,185,129,.2)}
.btn-grn:hover:not(:disabled){background:rgba(16,185,129,.2)}
.btn-blu{background:var(--blue-d);color:#93c5fd;border:1px solid rgba(59,130,246,.2)}
.btn-blu:hover:not(:disabled){background:rgba(59,130,246,.2)}
.btn-row{display:flex;gap:8px;flex-wrap:wrap;align-items:center}

/* ALERTS */
.alert{padding:9px 13px;border-radius:var(--r);font-size:12px;margin-bottom:14px;display:flex;align-items:center;gap:8px;animation:fi .3s ease}
.ai{background:var(--blue-d);border:1px solid rgba(59,130,246,.2);color:#93c5fd}
.as{background:var(--green-d);border:1px solid rgba(16,185,129,.2);color:#6ee7b7}
.ae{background:var(--red-d);border:1px solid rgba(239,68,68,.2);color:#fca5a5}
.aw{background:var(--amber-d);border:1px solid rgba(245,158,11,.2);color:#fcd34d}
@keyframes fi{from{opacity:0;transform:translateY(-3px)}to{opacity:1;transform:translateY(0)}}

/* SPINNER */
.spin{display:inline-block;width:13px;height:13px;border:2px solid var(--border2);border-top-color:var(--amber);border-radius:50%;animation:sp .7s linear infinite}
@keyframes sp{to{transform:rotate(360deg)}}

/* SCORE RING */
.ring-wrap{display:flex;align-items:center;gap:18px;padding:12px 0 16px}
.ring{position:relative;width:82px;height:82px;flex-shrink:0}
.ring svg{transform:rotate(-90deg)}
.ring-txt{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);text-align:center}
.ring-n{font-size:17px;font-weight:600;font-family:var(--mono);color:var(--amber);display:block}
.ring-l{font-size:9px;color:var(--text-d);text-transform:uppercase;letter-spacing:.06em}

/* CHIPS */
.chips{display:flex;flex-wrap:wrap;gap:5px;margin-top:7px}
.chip{padding:2px 9px;border-radius:20px;font-size:11px;font-weight:500;font-family:var(--mono)}
.c-grn{background:var(--green-d);color:#6ee7b7;border:1px solid rgba(16,185,129,.2)}
.c-red{background:var(--red-d);color:#fca5a5;border:1px solid rgba(239,68,68,.2)}
.c-blu{background:var(--blue-d);color:#93c5fd;border:1px solid rgba(59,130,246,.2)}

/* SECTION HEADING */
.sh{font-size:10px;font-weight:600;color:var(--text-d);text-transform:uppercase;letter-spacing:.1em;margin-bottom:7px}

/* APPS TABLE */
.at{width:100%;border-collapse:collapse}
.at th{text-align:left;padding:9px 13px;font-size:10px;font-weight:600;color:var(--text-d);text-transform:uppercase;letter-spacing:.09em;border-bottom:1px solid var(--border);background:var(--surface);white-space:nowrap}
.at td{padding:11px 13px;border-bottom:1px solid var(--border);font-size:13px;vertical-align:middle}
.at tr:last-child td{border-bottom:none}
.at tbody tr:hover td{background:var(--card2)}
.sb{padding:3px 9px;border-radius:20px;font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.06em}
.s-ap{background:var(--blue-d);color:#93c5fd;border:1px solid rgba(59,130,246,.2)}
.s-nr{background:rgba(75,98,128,.15);color:var(--text-d);border:1px solid var(--border)}
.s-rs{background:var(--amber-d);color:var(--amber);border:1px solid rgba(245,158,11,.2)}
.s-iv{background:var(--purple-d);color:var(--purple);border:1px solid rgba(167,139,250,.2)}
.s-of{background:var(--green-d);color:#6ee7b7;border:1px solid rgba(16,185,129,.2)}

/* STAT CARDS */
.sc{background:var(--card);border:1px solid var(--border);border-radius:var(--rl);padding:18px 20px}
.sc-lbl{font-size:10px;color:var(--text-m);text-transform:uppercase;letter-spacing:.09em;margin-bottom:6px}
.sc-val{font-size:28px;font-weight:600;font-family:var(--mono)}
.sc-sub{font-size:11px;color:var(--text-d);margin-top:4px}

/* LOG FORM */
.lf{background:var(--surface);border:1px solid var(--border);border-radius:var(--rl);padding:16px;margin-top:14px;display:none}
.lf.on{display:block;animation:fi .2s ease}
.lfg{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px;margin-bottom:10px}
@media(max-width:700px){.lfg{grid-template-columns:1fr}}

/* EMPTY STATE */
.empty{text-align:center;padding:56px 20px;color:var(--text-d)}
.empty-ico{font-size:38px;margin-bottom:10px;opacity:.3}

/* FUNNEL */
.funnel-legend{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:14px}
.fl-item{display:flex;align-items:center;gap:6px;font-size:11px;color:var(--text-m)}
.fl-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}
</style>
</head>
<body>

<div class="hdr">
  <div class="logo">
    <div class="logo-icon">⚡</div>
    TPM Application Engine
    <span class="logo-sub">/ AI-Powered Job Search Tool</span>
  </div>
  <div class="api-row">
    <div class="api-dot" id="apiDot"></div>
    <input type="password" class="api-in" id="apiIn" placeholder="Paste Anthropic API key — sk-ant-api03-..." autocomplete="off">
  </div>
</div>

<div class="tabs">
  <button class="tb on" onclick="gotoTab('analyze')" id="tb-analyze">
    <svg width="13" height="13" viewBox="0 0 13 13" fill="none"><path d="M1 10L4.5 6.5L7.5 9.5L12 2.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
    Analyze Job
  </button>
  <button class="tb" onclick="gotoTab('apps')" id="tb-apps">
    <svg width="13" height="13" viewBox="0 0 13 13" fill="none"><rect x="1.5" y="2" width="10" height="9" rx="1.5" stroke="currentColor" stroke-width="1.4"/><line x1="4" y1="5.5" x2="9" y2="5.5" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/><line x1="4" y1="8" x2="7.5" y2="8" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
    Applications
    <span class="tbadge" id="appBadge">0</span>
  </button>
  <button class="tb" onclick="gotoTab('dash')" id="tb-dash">
    <svg width="13" height="13" viewBox="0 0 13 13" fill="none"><rect x="1" y="7" width="2.5" height="5" rx="1" stroke="currentColor" stroke-width="1.3"/><rect x="5.25" y="4" width="2.5" height="8" rx="1" stroke="currentColor" stroke-width="1.3"/><rect x="9.5" y="1.5" width="2.5" height="10.5" rx="1" stroke="currentColor" stroke-width="1.3"/></svg>
    Dashboard
  </button>
</div>

<div class="main">

  <!-- ═══ ANALYZE TAB ═══ -->
  <div class="panel on" id="panel-analyze">
    <div id="ga"></div>
    <div class="g2">

      <!-- LEFT: Input -->
      <div>
        <div class="card">
          <div class="ch">
            <span class="ct">Job Posting Input</span>
            <span id="fetchSpin" style="display:none;"><span class="spin"></span></span>
          </div>
          <div style="margin-bottom:12px;">
            <label class="lbl">Job URL (fetched via AI)</label>
            <div style="display:flex;gap:8px;">
              <input type="url" id="jobUrl" placeholder="https://jobs.lever.co/stripe/..." style="flex:1;">
              <button class="btn btn-o" onclick="fetchJob()" id="fetchBtn" style="white-space:nowrap;">Fetch ↓</button>
            </div>
          </div>
          <div style="margin-bottom:14px;">
            <label class="lbl">Job Posting Text — paste or fetch above</label>
            <textarea id="jobTxt" rows="14" placeholder="Paste the full job description here, or use Fetch to pull it from a URL...&#10;&#10;Include: title, company, responsibilities, requirements, preferred qualifications."></textarea>
          </div>
          <div class="btn-row">
            <button class="btn btn-p" onclick="runAnalysis()" id="analyzeBtn">
              <svg width="13" height="13" viewBox="0 0 13 13" fill="none"><circle cx="6.5" cy="6.5" r="5" stroke="currentColor" stroke-width="1.4"/><path d="M6.5 4v3l1.5 1.5" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
              Analyze Keywords
            </button>
            <div id="analyzeSpin" style="display:none;align-items:center;gap:7px;color:var(--text-m);font-size:12px;">
              <span class="spin"></span> Running analysis…
            </div>
          </div>
        </div>
      </div>

      <!-- RIGHT: Results -->
      <div>
        <div class="card" id="rcard">
          <div class="ch">
            <span class="ct">Analysis Results</span>
            <span id="rLabel" style="font-size:11px;color:var(--text-m);"></span>
          </div>

          <div id="rEmpty" style="text-align:center;padding:50px 20px;color:var(--text-d);">
            <div style="font-size:42px;margin-bottom:12px;opacity:.25;">◎</div>
            <div style="font-size:13px;line-height:1.7;">Paste a job posting and click<br><strong style="color:var(--amber);">Analyze Keywords</strong> to see your match score,<br>keyword gaps, and tailoring strategy.</div>
          </div>

          <div id="rContent" style="display:none;">
            <!-- Score -->
            <div class="ring-wrap">
              <div class="ring">
                <svg width="82" height="82" viewBox="0 0 82 82">
                  <circle cx="41" cy="41" r="35" fill="none" stroke="var(--border)" stroke-width="7"/>
                  <circle id="ringArc" cx="41" cy="41" r="35" fill="none" stroke="var(--amber)" stroke-width="7"
                    stroke-dasharray="219.9" stroke-dashoffset="219.9" stroke-linecap="round"
                    style="transition:stroke-dashoffset .9s ease,stroke .5s ease;"/>
                </svg>
                <div class="ring-txt">
                  <span class="ring-n" id="ringNum">0%</span>
                  <span class="ring-l">match</span>
                </div>
              </div>
              <div>
                <div style="font-size:13px;color:var(--text);margin-bottom:6px;" id="rSummary"></div>
              </div>
            </div>

            <div style="margin-bottom:13px;">
              <div class="sh">Keywords Present ✓</div>
              <div class="chips" id="kPresent"></div>
            </div>

            <div style="margin-bottom:13px;">
              <div class="sh">Keywords to Add ✗</div>
              <div class="chips" id="kMissing"></div>
            </div>

            <div style="margin-bottom:13px;">
              <div class="sh">Gaps to Address</div>
              <div id="gapsList" style="font-size:12px;color:var(--text-m);line-height:1.9;"></div>
            </div>

            <div style="margin-bottom:16px;padding:12px;background:var(--amber-d2);border:1px solid rgba(245,158,11,.1);border-radius:var(--r);">
              <div class="sh" style="color:var(--amber);margin-bottom:5px;">Tailoring Strategy</div>
              <div id="rStrategy" style="font-size:12px;color:var(--text-m);line-height:1.75;"></div>
            </div>

            <div class="btn-row" style="margin-bottom:10px;">
              <button class="btn btn-grn btn-s" onclick="genResume()" id="genRBtn">
                <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><rect x="1.5" y="1.5" width="9" height="9" rx="1.5" stroke="currentColor" stroke-width="1.3"/><line x1="3.5" y1="4.5" x2="8.5" y2="4.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/><line x1="3.5" y1="6.5" x2="6.5" y2="6.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/></svg>
                Resume .doc
                <span id="rSpin" style="display:none;"><span class="spin" style="width:10px;height:10px;border-width:1.5px;"></span></span>
              </button>
              <button class="btn btn-blu btn-s" onclick="genCL()" id="genCLBtn">
                <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M1.5 3C1.5 2.45 1.95 2 2.5 2h7c.55 0 1 .45 1 1v6.5c0 .55-.45 1-1 1h-7c-.55 0-1-.45-1-1V3z" stroke="currentColor" stroke-width="1.3"/><path d="M1.5 3.5L6 6.5l4.5-3" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/></svg>
                Cover Letter .doc
                <span id="clSpin" style="display:none;"><span class="spin" style="width:10px;height:10px;border-width:1.5px;"></span></span>
              </button>
              <button class="btn btn-o btn-s" onclick="toggleLF()">+ Log Application</button>
            </div>

            <!-- Inline log form -->
            <div class="lf" id="logForm">
              <div class="sh" style="margin-bottom:10px;">Log This Application</div>
              <div class="lfg">
                <div><label class="lbl">Company</label><input type="text" id="lComp" placeholder="e.g. Stripe"></div>
                <div><label class="lbl">Role</label><input type="text" id="lRole" placeholder="e.g. Sr. TPM"></div>
                <div><label class="lbl">Stage</label>
                  <select id="lStage">
                    <option>Applied</option><option>No Response</option>
                    <option>Response</option><option>Interview</option><option>Offer</option>
                  </select>
                </div>
              </div>
              <div class="btn-row">
                <button class="btn btn-p btn-s" onclick="doLog()">Save Application</button>
                <button class="btn btn-g btn-s" onclick="toggleLF()">Cancel</button>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ═══ APPLICATIONS TAB ═══ -->
  <div class="panel" id="panel-apps">
    <div class="card">
      <div class="ch">
        <span class="ct">Application Tracker</span>
        <button class="btn btn-o btn-s" onclick="toggleMF()">+ New Entry</button>
      </div>
      <div id="mfWrap" style="display:none;background:var(--surface);border:1px solid var(--border);border-radius:var(--r);padding:16px;margin-bottom:16px;">
        <div class="lfg" style="margin-bottom:10px;">
          <div><label class="lbl">Company</label><input type="text" id="mComp" placeholder="Company name"></div>
          <div><label class="lbl">Role</label><input type="text" id="mRole" placeholder="Job title"></div>
          <div><label class="lbl">Job URL (optional)</label><input type="url" id="mUrl" placeholder="https://..."></div>
        </div>
        <div style="margin-bottom:10px;"><label class="lbl">Stage</label>
          <select id="mStage" style="width:180px;"><option>Applied</option><option>No Response</option><option>Response</option><option>Interview</option><option>Offer</option></select>
        </div>
        <div class="btn-row">
          <button class="btn btn-p btn-s" onclick="saveMF()">Save</button>
          <button class="btn btn-g btn-s" onclick="closeMF()">Cancel</button>
        </div>
      </div>
      <div id="tblWrap"></div>
    </div>
  </div>

  <!-- ═══ DASHBOARD TAB ═══ -->
  <div class="panel" id="panel-dash">
    <div class="g3" style="margin-bottom:18px;" id="statRow"></div>
    <div class="g2">
      <div class="card">
        <div class="ch"><span class="ct">Application Funnel</span></div>
        <div id="funnelWrap"></div>
      </div>
      <div class="card">
        <div class="ch"><span class="ct">Pipeline by Stage</span></div>
        <div style="position:relative;height:280px;"><canvas id="stageChart"></canvas></div>
      </div>
    </div>
  </div>

</div><!-- /main -->

<script>
// ══════════════════════════════════════════════
//  BASE RESUME
// ══════════════════════════════════════════════
// ─────────────────────────────────────────────────────────────────
//  PASTE YOUR BASE RESUME HERE
//  Replace everything between the backticks with your resume text.
//  Plain text works best — paste directly from your .txt or .docx.
//  The AI will use this as the baseline for all analysis and tailoring.
// ─────────────────────────────────────────────────────────────────
const RESUME = `YOUR NAME
Your Title | Your Location | your@email.com

PROFESSIONAL SUMMARY
[Paste your professional summary here]

CORE COMPETENCIES
[Paste your core competencies here]

PROFESSIONAL EXPERIENCE

Job Title | Company Name | Start Date – End Date
• Accomplishment or responsibility
• Accomplishment or responsibility

Job Title | Company Name | Start Date – End Date
• Accomplishment or responsibility
• Accomplishment or responsibility

EDUCATION
Degree – Field of Study | University Name | Year`;

// ══════════════════════════════════════════════
//  STATE
// ══════════════════════════════════════════════
let KEY = '';
let analysis = null;
let apps = [];
let chartInst = null;
const STAGES = ['Applied','No Response','Response','Interview','Offer'];
const SCOLOR = {Applied:'#3b82f6','No Response':'#4b6280',Response:'#f59e0b',Interview:'#a78bfa',Offer:'#10b981'};
const SCLS   = {Applied:'s-ap','No Response':'s-nr',Response:'s-rs',Interview:'s-iv',Offer:'s-of'};

function loadApps(){try{apps=JSON.parse(localStorage.getItem('tpm_apps')||'[]')}catch{apps=[]}}
function saveApps(){try{localStorage.setItem('tpm_apps',JSON.stringify(apps))}catch{}}

// ══════════════════════════════════════════════
//  API KEY
// ══════════════════════════════════════════════
document.getElementById('apiIn').addEventListener('input',function(){
  KEY=this.value.trim();
  const d=document.getElementById('apiDot');
  d.className='api-dot'+(KEY.startsWith('sk-ant')?'  ok':KEY.length>5?' bad':'');
});

// ══════════════════════════════════════════════
//  TAB NAVIGATION
// ══════════════════════════════════════════════
function gotoTab(t){
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('on'));
  document.querySelectorAll('.tb').forEach(b=>b.classList.remove('on'));
  document.getElementById('panel-'+t).classList.add('on');
  document.getElementById('tb-'+t).classList.add('on');
  if(t==='dash') renderDash();
  if(t==='apps') renderTable();
}

// ══════════════════════════════════════════════
//  ALERTS
// ══════════════════════════════════════════════
function flash(msg,type='ai',cid='ga'){
  const c=document.getElementById(cid);
  if(!c)return;
  const cls={ai:'ai',as:'as',ae:'ae',aw:'aw'}[type]||'ai';
  c.innerHTML=`<div class="alert ${cls}"><span>${{ai:'ℹ',as:'✓',ae:'✕',aw:'⚠'}[type]||'ℹ'}</span>${msg}</div>`;
  setTimeout(()=>{if(c.innerHTML)c.innerHTML='';},5000);
}
function requireKey(){if(!KEY){flash('Paste your Anthropic API key in the header first.','ae');return false;}return true;}

// ══════════════════════════════════════════════
//  ANTHROPIC API WRAPPER
// ══════════════════════════════════════════════
async function claude(prompt, system='', opts={}){
  const{useSearch=false,maxTokens=4096}=opts;
  const body={
    model:'claude-sonnet-4-20250514',
    max_tokens:maxTokens,
    messages:[{role:'user',content:prompt}]
  };
  if(system) body.system=system;
  if(useSearch) body.tools=[{type:'web_search_20250305',name:'web_search'}];

  const r=await fetch('https://api.anthropic.com/v1/messages',{
    method:'POST',
    headers:{
      'Content-Type':'application/json',
      'x-api-key':KEY,
      'anthropic-version':'2023-06-01',
      'anthropic-dangerous-direct-browser-access':'true'
    },
    body:JSON.stringify(body)
  });

  if(!r.ok){
    let m=`API error ${r.status}`;
    try{const e=await r.json();m=e.error?.message||m;}catch{}
    throw new Error(m);
  }

  const d=await r.json();

  // If web_search triggered a tool_use loop, handle it
  if(d.stop_reason==='tool_use'){
    const msgs=[
      {role:'user',content:prompt},
      {role:'assistant',content:d.content},
      {role:'user',content:d.content.filter(b=>b.type==='tool_use').map(b=>({type:'tool_result',tool_use_id:b.id,content:'(search executed by Anthropic infrastructure)'}))}
    ];
    const body2={...body,messages:msgs};
    const r2=await fetch('https://api.anthropic.com/v1/messages',{
      method:'POST',
      headers:{
        'Content-Type':'application/json',
        'x-api-key':KEY,
        'anthropic-version':'2023-06-01',
        'anthropic-dangerous-direct-browser-access':'true'
      },
      body:JSON.stringify(body2)
    });
    const d2=await r2.json();
    return d2.content.filter(b=>b.type==='text').map(b=>b.text).join('\n');
  }

  return d.content.filter(b=>b.type==='text').map(b=>b.text).join('\n');
}

// ══════════════════════════════════════════════
//  1. FETCH JOB
// ══════════════════════════════════════════════
async function fetchJob(){
  if(!requireKey()) return;
  const url=document.getElementById('jobUrl').value.trim();
  if(!url){flash('Enter a job posting URL first.','aw');return;}
  const btn=document.getElementById('fetchBtn');
  const sp=document.getElementById('fetchSpin');
  btn.disabled=true; sp.style.display='inline-block';
  try{
    const txt=await claude(
      `Fetch and extract the complete job posting from: ${url}\n\nReturn ONLY the job posting content: company name, job title, location, salary if shown, job description, responsibilities, required qualifications, and preferred qualifications. No preamble, no commentary — just the raw job text.`,
      '',{useSearch:true,maxTokens:3000}
    );
    document.getElementById('jobTxt').value=txt;
    flash('Job posting fetched successfully.','as');
  }catch(e){
    flash('Fetch failed: '+e.message,'ae');
  }finally{
    btn.disabled=false; sp.style.display='none';
  }
}

// ══════════════════════════════════════════════
//  2. KEYWORD ANALYSIS
// ══════════════════════════════════════════════
async function runAnalysis(){
  if(!requireKey()) return;
  const jt=document.getElementById('jobTxt').value.trim();
  if(!jt){flash('Paste or fetch a job posting first.','aw');return;}

  const btn=document.getElementById('analyzeBtn');
  const sp=document.getElementById('analyzeSpin');
  btn.style.display='none'; sp.style.display='flex';

  try{
    const raw=await claude(
      `Compare this job posting against the candidate resume and return ONLY a valid JSON object. No markdown, no code blocks, no commentary — raw JSON only.\n\nRESUME:\n${RESUME}\n\nJOB POSTING:\n${jt}\n\nReturn exactly this structure:\n{"company":"","role":"","location":"","match_score":0,"keywords_present":[],"keywords_missing":[],"key_requirements":[],"strengths":[],"gaps":[],"tailoring_suggestions":"","summary":""}`,
      'You are an expert ATS optimization specialist. Respond with raw JSON only — no preamble, no markdown, no backticks.',
      {maxTokens:2200}
    );
    const s=raw.indexOf('{'), e=raw.lastIndexOf('}')+1;
    analysis=JSON.parse(raw.slice(s,e));
    analysis._jt=jt;

    // Pre-fill log form fields
    document.getElementById('lComp').value=analysis.company||'';
    document.getElementById('lRole').value=analysis.role||'';

    renderResults(analysis);
    flash(`Analysis complete — <strong>${analysis.match_score}%</strong> keyword match for ${analysis.role||'this role'} at ${analysis.company||'this company'}.`,'as');
  }catch(e){
    flash('Analysis error: '+e.message,'ae');
  }finally{
    btn.style.display='inline-flex'; sp.style.display='none';
  }
}

function renderResults(a){
  document.getElementById('rEmpty').style.display='none';
  document.getElementById('rContent').style.display='block';
  document.getElementById('rLabel').textContent=(a.company&&a.role)?`${a.role} @ ${a.company}`:'';

  const score=Math.min(100,Math.max(0,a.match_score||0));
  const C=2*Math.PI*35;
  document.getElementById('ringArc').style.strokeDashoffset=C-(score/100)*C;
  document.getElementById('ringNum').textContent=score+'%';
  const col=score>=75?'var(--green)':score>=50?'var(--amber)':'var(--red)';
  document.getElementById('ringArc').style.stroke=col;
  document.getElementById('ringNum').style.color=col;
  document.getElementById('rSummary').textContent=a.summary||'';

  document.getElementById('kPresent').innerHTML=(a.keywords_present||[]).slice(0,16).map(k=>`<span class="chip c-grn">${k}</span>`).join('');
  document.getElementById('kMissing').innerHTML=(a.keywords_missing||[]).slice(0,14).map(k=>`<span class="chip c-red">${k}</span>`).join('');
  document.getElementById('gapsList').innerHTML=(a.gaps||[]).map(g=>`<div style="display:flex;gap:7px;margin-bottom:3px;"><span style="color:var(--amber);flex-shrink:0;">›</span><span>${g}</span></div>`).join('');
  document.getElementById('rStrategy').textContent=a.tailoring_suggestions||'';
}

// ══════════════════════════════════════════════
//  3. GENERATE TAILORED RESUME
// ══════════════════════════════════════════════
async function genResume(){
  if(!requireKey()) return;
  if(!analysis){flash('Run keyword analysis first.','aw');return;}
  const btn=document.getElementById('genRBtn');
  const sp=document.getElementById('rSpin');
  btn.disabled=true; sp.style.display='inline-block';
  try{
    const html=await claude(
      `Create a tailored version of this resume optimized for the job posting below.\n\nRULES — follow these exactly:\n- TARGET LENGTH: 1-2 pages maximum. Be concise throughout.\n- Naturally incorporate these missing keywords where they genuinely fit: ${(analysis.keywords_missing||[]).join(', ')}\n- Reorder bullets to front-load achievements most relevant to this role\n- Revise the professional summary to mirror the job's language and priorities — 2 paragraphs max, 3 sentences each\n- CRITICAL: Preserve all facts — never fabricate experience, metrics, certifications, or credentials not in the base resume\n- CRITICAL: Do NOT add any certifications to the title line or anywhere else unless they appear in the base resume\n- CRITICAL: Keep EXACTLY 4 Core Competency categories — no more, no fewer\n- Core Competencies format MUST be: <p class="comp"><strong>Category Label:</strong> Item 1 • Item 2 • Item 3</p> — NOT bullet lists\n- Keep EXACTLY 4 bullets per role — no more\n- Each bullet must be under 20 words — tight and outcome-focused\n- Do not add bullets, roles, or sections not in the base resume\n\nJOB POSTING:\n${analysis._jt}\n\nBASE RESUME:\n${RESUME}\n\nReturn clean HTML only. Use these elements:\n<h1> for name\n<p class="subtitle"> for title line only — no certifications unless in base resume\n<p class="contact"> for contact info\n<h2> for section headers (PROFESSIONAL SUMMARY, CORE COMPETENCIES, PROFESSIONAL EXPERIENCE, EDUCATION)\n<p class="comp"> for each competency line — format: <strong>Label:</strong> item • item • item\n<h3> for job titles\n<p class="co-meta"> for company | date lines (italic)\n<ul><li> for bullet points — max 4 per role, max 20 words each\n<hr> between major sections\nNO inline styles. NO markdown. NO commentary.`,
      'You are an expert TPM resume writer. Return only clean semantic HTML — no markdown, no backticks, no commentary.',
      {maxTokens:3500}
    );
    const ro=(analysis.role||'TPM').replace(/[^\w]/g,'_');
    const co=(analysis.company||'Co').replace(/[^\w]/g,'_');
    dlDoc(html,`Resume_${ro}_${co}.doc`,false);
    flash('Tailored resume downloaded!','as');
  }catch(e){
    flash('Resume generation failed: '+e.message,'ae');
  }finally{
    btn.disabled=false; sp.style.display='none';
  }
}

// ══════════════════════════════════════════════
//  4. GENERATE COVER LETTER
// ══════════════════════════════════════════════
async function genCL(){
  if(!requireKey()) return;
  if(!analysis){flash('Run keyword analysis first.','aw');return;}
  const btn=document.getElementById('genCLBtn');
  const sp=document.getElementById('clSpin');
  btn.disabled=true; sp.style.display='inline-block';
  try{
    const today=new Date().toLocaleDateString('en-US',{month:'long',day:'numeric',year:'numeric'});
    const html=await claude(
      `Write a compelling, personalized cover letter for this application.\n\nCANDIDATE RESUME:\n${RESUME}\n\nTARGET: ${analysis.role||'Senior TPM'} at ${analysis.company||'the company'}\nDATE: ${today}\n\nJOB POSTING:\n${analysis._jt}\n\nKEY STRENGTHS IDENTIFIED:\n${(analysis.strengths||[]).join('\n')}\n\nWriting guidelines:\n- Open with a strong, specific hook — NOT "I am writing to apply for..."\n- Reference 2-3 specific, quantified achievements that map directly to their stated needs\n- Show you understand their specific business context or challenge\n- Use confident, direct language — avoid filler phrases\n- Close with a clear call to action\n- Target 320-360 words, 4 paragraphs\n\nReturn clean HTML only:\n<p class="cl-date"> for the date\n<p class="cl-addr"> for the company address block (company name and location)\n<p class="cl-sal"> for the salutation\n<p> for each body paragraph\n<p class="cl-close"> for "Sincerely," or similar\n<p class="cl-sig"> for the candidate name\nNO inline styles. NO markdown.`,
      'You are an expert cover letter writer for senior technical program management roles. Return only clean HTML — no markdown, no backticks, no commentary.',
      {maxTokens:1800}
    );
    const co=(analysis.company||'Company').replace(/[^\w]/g,'_');
    const ro=(analysis.role||'TPM').replace(/[^\w]/g,'_');
    dlDoc(html,`CoverLetter_${co}_${ro}.doc`,true);
    flash('Cover letter downloaded!','as');
  }catch(e){
    flash('Cover letter generation failed: '+e.message,'ae');
  }finally{
    btn.disabled=false; sp.style.display='none';
  }
}

// ══════════════════════════════════════════════
//  DOWNLOAD AS WORD .DOC
// ══════════════════════════════════════════════
function dlDoc(bodyHtml,fname,isCL){
  const rs=`
    @page{margin:.9in .85in}
    body{font-family:Calibri,'Segoe UI',Arial,sans-serif;font-size:10.5pt;line-height:1.45;color:#111}
    h1{font-size:20pt;font-weight:700;color:#0b1628;margin-bottom:2pt;letter-spacing:.01em}
    .subtitle{font-size:11pt;color:#2d4a7a;font-weight:500;margin-bottom:3pt}
    .contact{font-size:9.5pt;color:#555;margin-bottom:16pt}
    h2{font-size:10.5pt;font-weight:700;color:#0b1628;text-transform:uppercase;letter-spacing:.08em;border-bottom:1.5pt solid #c8940e;padding-bottom:2pt;margin-top:14pt;margin-bottom:6pt}
    h3{font-size:10.5pt;font-weight:700;color:#111;margin-top:8pt;margin-bottom:1pt}
    .co-meta{font-size:9.5pt;color:#555;margin-bottom:4pt;font-style:italic}
    ul{margin-left:13pt;margin-top:2pt}li{margin-bottom:2.5pt;font-size:10pt}
    hr{border:none;border-top:.5pt solid #ddd;margin:8pt 0}
    .comp{font-size:10pt;margin-bottom:3pt;line-height:1.5}`;
  const cs=`
    @page{margin:1in}
    body{font-family:Calibri,'Segoe UI',Arial,sans-serif;font-size:11pt;line-height:1.65;color:#111}
    .cl-date{color:#555;margin-bottom:18pt}
    .cl-addr{margin-bottom:16pt;color:#222}
    .cl-sal{font-weight:600;margin-bottom:13pt}
    p{margin-bottom:12pt;text-align:justify}
    .cl-close{margin-top:26pt}
    .cl-sig{font-weight:700;font-size:12pt;margin-top:5pt;color:#0b1628}`;
  const doc=`<!DOCTYPE html>
<html xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:w="urn:schemas-microsoft-com:office:word" xmlns="http://www.w3.org/TR/REC-html40">
<head><meta charset="utf-8"><title>${fname}</title>
<style>${isCL?cs:rs}</style></head>
<body>${bodyHtml}</body></html>`;
  const blob=new Blob([doc],{type:'application/msword'});
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');
  a.href=url; a.download=fname;
  document.body.appendChild(a); a.click(); document.body.removeChild(a);
  setTimeout(()=>URL.revokeObjectURL(url),1000);
}

// ══════════════════════════════════════════════
//  5. APPLICATION TRACKER
// ══════════════════════════════════════════════
function toggleLF(){
  const f=document.getElementById('logForm');
  f.classList.toggle('on');
}

function doLog(){
  const co=document.getElementById('lComp').value.trim();
  const ro=document.getElementById('lRole').value.trim();
  if(!co||!ro){flash('Company and role are required.','aw');return;}
  apps.unshift({
    id:Date.now(),
    date:new Date().toLocaleDateString('en-US',{month:'short',day:'numeric',year:'numeric'}),
    company:co, role:ro,
    stage:document.getElementById('lStage').value,
    url:document.getElementById('jobUrl').value.trim(),
    score:analysis?.match_score||null
  });
  saveApps(); updateBadge();
  document.getElementById('logForm').classList.remove('on');
  flash(`Logged: <strong>${ro}</strong> at <strong>${co}</strong>`, 'as');
}

function toggleMF(){
  const w=document.getElementById('mfWrap');
  w.style.display=w.style.display==='none'?'block':'none';
}
function closeMF(){document.getElementById('mfWrap').style.display='none';}

function saveMF(){
  const co=document.getElementById('mComp').value.trim();
  const ro=document.getElementById('mRole').value.trim();
  if(!co||!ro){alert('Company and role required.');return;}
  apps.unshift({
    id:Date.now(),
    date:new Date().toLocaleDateString('en-US',{month:'short',day:'numeric',year:'numeric'}),
    company:co, role:ro,
    stage:document.getElementById('mStage').value,
    url:document.getElementById('mUrl').value.trim(),
    score:null
  });
  saveApps(); updateBadge(); renderTable(); closeMF();
  ['mComp','mRole','mUrl'].forEach(id=>document.getElementById(id).value='');
}

function setStage(id,s){const a=apps.find(x=>x.id===id);if(a){a.stage=s;saveApps();}}

function delApp(id){
  if(!confirm('Remove this application?')) return;
  apps=apps.filter(a=>a.id!==id);
  saveApps(); updateBadge(); renderTable();
}

function updateBadge(){
  document.getElementById('appBadge').textContent=apps.length;
}

function renderTable(){
  const w=document.getElementById('tblWrap');
  if(!apps.length){
    w.innerHTML=`<div class="empty"><div class="empty-ico">📋</div><div>No applications yet.<br>Analyze a job posting, then click <strong>+ Log Application</strong>.</div></div>`;
    return;
  }
  const rows=apps.map(a=>{
    const opts=STAGES.map(s=>`<option value="${s}"${a.stage===s?' selected':''}>${s}</option>`).join('');
    const scoreHtml=a.score!=null
      ?`<span style="font-family:var(--mono);font-size:11px;color:${a.score>=75?'var(--green)':a.score>=50?'var(--amber)':'var(--red)'}">${a.score}%</span>`
      :`<span style="color:var(--text-d);">—</span>`;
    const urlHtml=a.url
      ?`<a href="${a.url}" target="_blank" style="color:var(--blue);font-size:11px;text-decoration:none;">↗</a>`
      :`<span style="color:var(--text-d);">—</span>`;
    return `<tr>
      <td style="color:var(--text-d);font-family:var(--mono);font-size:11px;white-space:nowrap;">${a.date}</td>
      <td style="font-weight:500;">${a.company}</td>
      <td style="color:var(--text-m);">${a.role}</td>
      <td>
        <select onchange="setStage(${a.id},this.value)" style="background:var(--surface);border:1px solid var(--border);color:var(--text);padding:4px 8px;border-radius:6px;font-size:11px;width:132px;cursor:pointer;appearance:none;">
          ${opts}
        </select>
      </td>
      <td>${scoreHtml}</td>
      <td>${urlHtml}</td>
      <td><button onclick="delApp(${a.id})" style="background:none;border:none;color:var(--text-d);cursor:pointer;font-size:14px;padding:2px 6px;" title="Remove">✕</button></td>
    </tr>`;
  }).join('');
  w.innerHTML=`<table class="at">
    <thead><tr>
      <th>Date</th><th>Company</th><th>Role</th><th>Stage</th><th>Match</th><th>URL</th><th></th>
    </tr></thead>
    <tbody>${rows}</tbody>
  </table>`;
}

// ══════════════════════════════════════════════
//  6. DASHBOARD — FUNNEL + CHART
// ══════════════════════════════════════════════
function renderDash(){
  const total=apps.length;
  const counts={};
  STAGES.forEach(s=>counts[s]=0);
  apps.forEach(a=>{if(counts[a.stage]!==undefined)counts[a.stage]++;});

  const responded=counts['Response']+counts['Interview']+counts['Offer'];
  const rr=total>0?Math.round((responded/total)*100):0;

  // Stat cards
  document.getElementById('statRow').innerHTML=`
    <div class="sc">
      <div class="sc-lbl">Total Applied</div>
      <div class="sc-val" style="color:var(--blue);">${total}</div>
      <div class="sc-sub">All time</div>
    </div>
    <div class="sc">
      <div class="sc-lbl">Response Rate</div>
      <div class="sc-val" style="color:var(--amber);">${rr}%</div>
      <div class="sc-sub">${responded} of ${total} responses</div>
    </div>
    <div class="sc">
      <div class="sc-lbl">In Interview / Offer</div>
      <div class="sc-val" style="color:var(--green);">${counts['Interview']+counts['Offer']}</div>
      <div class="sc-sub">${counts['Offer']} offer${counts['Offer']!==1?'s':''} received</div>
    </div>`;

  renderFunnel(counts, total);
  renderBarChart(counts);
}

function renderFunnel(counts, total){
  const W=360, H=50, gap=5;
  const maxW=W, minW=80;
  // Fixed trapezoid widths that narrow per stage
  const widths=[360,310,250,185,120];
  const totalH=STAGES.length*(H+gap)-gap;

  const shapes=STAGES.map((s,i)=>{
    const w1=widths[i];
    const w2=i<STAGES.length-1?widths[i+1]:widths[i]*0.75;
    const x1=(W-w1)/2, x2=x1+w1;
    const x3=(W-w2)/2, x4=x3+w2;
    const y=i*(H+gap);
    const col=SCOLOR[s];
    const pct=total>0?Math.round((counts[s]/total)*100):0;
    return `<g>
      <path d="M${x1.toFixed(1)},${y} L${x2.toFixed(1)},${y} L${x4.toFixed(1)},${y+H} L${x3.toFixed(1)},${y+H} Z"
        fill="${col}" opacity="${counts[s]>0?'.82':'.25'}"/>
      <text x="${W/2}" y="${y+H/2+4}" text-anchor="middle"
        font-family="Outfit,sans-serif" font-size="13" font-weight="600" fill="white" opacity="${counts[s]>0?'1':'.5'}">
        ${s}${counts[s]>0?` — ${counts[s]} (${pct}%)`:''}
      </text>
    </g>`;
  }).join('');

  const legend=STAGES.map(s=>`
    <div class="fl-item">
      <span class="fl-dot" style="background:${SCOLOR[s]}"></span>
      ${s}: ${counts[s]}
    </div>`).join('');

  document.getElementById('funnelWrap').innerHTML=`
    <svg viewBox="0 0 ${W} ${totalH}" width="100%" style="max-width:400px;display:block;margin:0 auto;">
      ${shapes}
    </svg>
    <div class="funnel-legend">${legend}</div>`;
}

function renderBarChart(counts){
  if(chartInst){chartInst.destroy();chartInst=null;}
  const ctx=document.getElementById('stageChart');
  if(!ctx) return;
  chartInst=new Chart(ctx,{
    type:'bar',
    data:{
      labels:STAGES,
      datasets:[{
        data:STAGES.map(s=>counts[s]),
        backgroundColor:STAGES.map(s=>SCOLOR[s]+'bb'),
        borderColor:STAGES.map(s=>SCOLOR[s]),
        borderWidth:1,
        borderRadius:5,
        borderSkipped:false
      }]
    },
    options:{
      responsive:true,
      maintainAspectRatio:false,
      plugins:{legend:{display:false}},
      scales:{
        x:{ticks:{color:'#64748b',font:{family:'Outfit',size:11}},grid:{color:'#1e3050'}},
        y:{beginAtZero:true,ticks:{color:'#64748b',font:{family:'Outfit',size:11},stepSize:1,precision:0},grid:{color:'#1e3050'}}
      }
    }
  });
}

// ══════════════════════════════════════════════
//  INIT
// ══════════════════════════════════════════════
loadApps();
updateBadge();
</script>
</body>
</html>
