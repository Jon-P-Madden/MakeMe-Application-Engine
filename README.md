# ⚡ Application Engine

**AI-powered job application tool — single-file, no backend, no installs.**

Paste a job URL. Get a match score. If the role clears the bar, generate a tailored resume and cover letter grounded in your actual experience. Everything runs in your browser against the Anthropic Claude API.

---

## Screenshots

> **Analyze Tab — Keyword Analysis & Match Score**
> 
> ![Analyze Tab](screenshots/analyze.png)
> *Paste or fetch a job posting, run analysis, and see your match score, present/missing keywords, gap narrative, and tailoring strategy.*

> **Below Threshold — Gate in Action**
> 
> ![Threshold Banner](screenshots/threshold.png)
> *Roles scoring below 85% are blocked. One click logs them as Not Pursuing and moves you on.*

> **Applications Tab — Pipeline Tracker**
> 
> ![Applications Tab](screenshots/tracker.png)
> *Every application logged with company, role, stage, match score, and source URL.*

> **Dashboard Tab — Funnel & Stage Chart**
> 
> ![Dashboard](screenshots/dashboard.png)
> *Response rate, active pipeline funnel, and stage distribution — all calculated from your live tracker data.*

---

## What It Does

### 1 — Keyword Analysis
Compares a job posting against your base resume using Claude. Returns:
- **Match score (0–100%)** — ATS alignment estimate
- **Keywords present** — what you already cover
- **Keywords missing** — what needs to be addressed
- **Gap narrative** — specific deficiencies explained in plain language
- **Tailoring strategy** — actionable guidance for this exact role

### 2 — The 85% Threshold Gate
The engine will not generate documents for a weak match. If a role scores below **85%**, the action buttons are replaced with a clear "Below Match Threshold" banner and a one-click **Mark as Not Pursuing** button. The role is logged automatically with its score and you move on.

This is intentional. The value of tailored documents is precision — not volume.

### 3 — Tailored Resume Generation
For roles that clear the threshold, generates a revised version of your base resume that:
- Weaves in missing keywords naturally where they fit your actual experience
- Reorders bullets to front-load the most relevant achievements
- Rewrites the professional summary to mirror the job's language and priorities
- **Never fabricates experience or adds unsupported claims**

Downloads as a `.doc` file ready for submission.

### 4 — Custom Cover Letter
Generates a role-specific cover letter grounded in your resume's real achievements:
- Opens with a specific hook — not a generic "I am writing to apply" opener
- References 2–3 quantified achievements mapped to the role's stated needs
- Demonstrates understanding of the company's specific context
- Targets 320–360 words across 4 focused paragraphs

Downloads as a `.doc` file.

### 5 — Application Tracker
Log every application with company, role, stage, match score, and URL. Update stage inline as your pipeline moves. Manually add applications from other sources.

Pipeline stages: **Applied → No Response → Response → Interview → Offer** (plus **Not Pursuing** for screened-out roles).

### 6 — Dashboard
Live stats calculated from your tracker:
- Total applied (excludes Not Pursuing from count)
- Response rate against pursued applications only
- Interview / Offer count
- Application funnel visualization
- Pipeline bar chart by stage

---

## Setup

### 1 — Get an Anthropic API Key
Create an account at [console.anthropic.com](https://console.anthropic.com), generate an API key, and have it ready. You'll paste it into the tool at runtime — it is never stored anywhere.

### 2 — Add Your Resume
Open `Application_Engine.html` in a text editor. Find the `RESUME` constant near the top of the `<script>` block:

```javascript
const RESUME = `YOUR NAME
Your Title | Your Location | your@email.com
...`;
```

Replace the placeholder text with your full resume in plain text. Paste directly from a `.txt` or copy from your `.docx`. Plain text works best — no formatting required.

### 3 — Open the File
Open `Application_Engine.html` directly in any modern browser. No server, no build step, no dependencies to install.

### 4 — Paste Your API Key
The header has an API key field. Paste your `sk-ant-api03-...` key. The indicator dot turns green when the key format is recognized.

---

## Usage

```
1. Paste a job URL → click Fetch  (or paste the job text directly)
2. Click Analyze Keywords
3. Review match score, gaps, and tailoring strategy
4. If score ≥ 85%:
     → Click Resume .doc to download a tailored resume
     → Click Cover Letter .doc to download a custom cover letter
     → Click + Log Application to track it
   If score < 85%:
     → Click ✕ Mark as Not Pursuing to log and move on
```

---

## Configuration

| Constant | Location | Default | Purpose |
|---|---|---|---|
| `THRESHOLD` | `<script>` block | `85` | Minimum match score to unlock document generation |
| `RESUME` | `<script>` block | Placeholder | Your base resume — paste full text here |

To change the threshold, find `const THRESHOLD = 85;` and update the value.

---

## Architecture

| Layer | Detail |
|---|---|
| Runtime | Pure browser — HTML + CSS + vanilla JS, single file |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) via direct fetch |
| Web search | Anthropic's built-in `web_search_20250305` tool — used for URL job fetches |
| Charts | Chart.js 4.4.1 via CDN |
| Storage | `localStorage` — tracker data persists in-browser, never leaves the device |
| Output | `.doc` files via Blob/URL — no server upload |

No frameworks. No build pipeline. No data leaves your machine except the API calls to Anthropic (job text + your resume + API key in the request header).

---

## Privacy

- Your resume is stored only in the HTML file itself (the `RESUME` constant)
- Your API key is held in memory for the session only — never written to localStorage or sent anywhere except Anthropic's API endpoint
- Application tracker data is stored in your browser's localStorage — it does not sync or upload
- Job posting text and your resume are sent to Anthropic's API for analysis and generation — review [Anthropic's privacy policy](https://www.anthropic.com/privacy) for API data handling

---

## Project Context

Built as part of a job search infrastructure project to solve a specific problem: submitting a base resume to every posting produced poor ATS results. The engine enforces discipline — only roles with strong alignment get tailored documents, and the tailoring is done by the same model evaluating the fit.

The threshold gate is the core design decision. A 72% match with a polished cover letter is still a 72% match. The goal is not more applications — it's better ones.

---

## License

MIT — use it, modify it, build on it.
