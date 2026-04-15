# TPM Application Engine

A browser-based, AI-powered job application workflow tool built on the Anthropic Claude API. Single HTML file. No installation. No backend. No subscription.

Built by a Senior TPM to solve a real problem: ATS keyword mismatch was killing application conversion rates. Manual tailoring didn't scale. This tool does it in seconds.

![TPM Application Engine screenshot](Screenshot.png)

---

## The Problem

After diagnosing low interview conversion across an active job search, the root cause was clear: resumes weren't being tailored to individual postings, and ATS systems were filtering them before a human ever saw them. Manual tailoring is time-intensive, inconsistent, and doesn't scale.

Secondary problems:
- No visibility into application pipeline status across concurrent applications
- Cover letters were generic or took too long to personalize
- No feedback loop between keyword strategy and application outcomes

---

## The Solution

A self-contained tool that uses Claude to analyze any job posting against your base resume, surface keyword gaps, generate tailored documents, and track your pipeline — all in one browser tab.

**Design constraints applied:**
- Single HTML file — zero dependencies, zero deployment surface, runs in any browser
- API key entered at runtime — never stored, never leaves your browser except in API calls
- No backend, no database, no build step — open the file and go
- State persisted in localStorage — simple, durable, private

---

## Features

### Analyze Job
- Paste or fetch any job posting URL
- Claude extracts keywords, required skills, and role signals
- Compares against your base resume and returns a **match score**
- Surfaces keywords present, keywords missing, and a tailoring strategy
- One click to generate a tailored resume or cover letter

### Resume Tailoring
- Generates a keyword-optimized resume variant based on the gap analysis
- Naturally incorporates missing terms without fabricating experience
- Downloads as a `.doc` file ready to submit

### Cover Letter Generation
- Writes a role-specific cover letter using job context and candidate strengths
- Follows a structured narrative: hook → achievement alignment → company context → CTA
- Downloads as a `.doc` file

### Application Pipeline Tracker
- Log applications directly from the analysis view
- Track status across: Applied → No Response → Response → Interview → Offer
- Full table view with editable stage dropdowns

### Dashboard
- Visual application funnel showing conversion at each stage
- Bar chart of pipeline distribution
- Response rate and offer metrics

---

## Architecture

```
┌──────────────────────────────────────────────────┐
│              Browser (Single HTML File)           │
│                                                  │
│  ┌──────────────┐    ┌──────────────────────┐   │
│  │  Job Posting  │    │    Base Resume        │   │
│  │  (paste/fetch)│    │    (RESUME constant)  │   │
│  └──────┬───────┘    └──────────┬────────────┘   │
│         │                       │                 │
│         └──────────┬────────────┘                 │
│                    ▼                              │
│          ┌─────────────────┐                     │
│          │  Prompt Engine   │                     │
│          │  (task routing)  │                     │
│          └────────┬────────┘                     │
│                   │                               │
│  ┌────────────────┼──────────────────────────┐   │
│  │  localStorage  │  Application State        │   │
│  └────────────────┘                           │   │
└──────────────────────┼───────────────────────────┘
                       │ HTTPS
                       ▼
              ┌─────────────────┐
              │  Anthropic API   │
              │  claude-sonnet   │
              └─────────────────┘
```

**Prompt engineering approach:**
Each task uses a dedicated prompt with explicit output format instructions — raw JSON for analysis, semantic HTML for document generation. Prompts are structured to produce consistent, parseable output, not conversational responses. The web search tool is used for URL fetching.

---

## Setup

1. Clone or download this repo
2. Open `TPM_Application_Engine.html` in any modern browser — Chrome recommended
3. Get an [Anthropic API key](https://console.anthropic.com/) (requires an Anthropic account)
4. Paste your API key in the header field — the dot turns green when valid
5. Paste your base resume into the `RESUME` constant in the script (line ~360)
6. Paste a job posting and run the analysis

**No installation. No build step. No server.**

---

## How to Add Your Resume

Open the HTML file in a text editor and find the `RESUME` constant near line 360:

```javascript
const RESUME = `YOUR NAME
Your Title | Your Location | your@email.com
...`;
```

Replace the placeholder text with your resume content in plain text format. Save the file. Done.

---

## Tech Stack

- **Vanilla HTML / CSS / JS** — single file, no framework
- **Anthropic Claude API** — `claude-sonnet-4-20250514` via `/v1/messages`
- **Chart.js** — pipeline visualization (loaded via CDN)
- **No backend. No database. No build tooling.**

---

## Roadmap

**Phase 2 — Email Integration**
Connect to Gmail/Outlook API to monitor for application status signals and auto-update pipeline stage based on recruiter or ATS response emails.

**Phase 3 — Outcome Feedback Loop**
Tag applications with final outcomes and analyze which keyword strategies correlated with higher screen rates. Feed outcome data back into tailoring prompts.

**Phase 4 — Persistence Layer**
Replace localStorage with IndexedDB or a lightweight backend for cross-session history and CSV export.

---

## Why This Is in a Portfolio

This project demonstrates three things relevant to a senior TPM profile:

**AI API integration** — direct use of the Anthropic Messages API, prompt engineering for structured JSON and HTML output, web search tool integration, multi-turn conversation handling for tool use responses.

**Product thinking applied to a real problem** — the tool came from a specific, diagnosed problem (ATS keyword mismatch), not from a tutorial. Constraints were defined deliberately, scope was controlled for v1, and the roadmap is sequenced by value.

**TPM perspective on build decisions** — every architectural choice has an explicit rationale. The single-file constraint wasn't laziness; it was a deliberate decision to minimize deployment surface and maximize portability. Tradeoffs are documented, not hidden.

This is not a showcase of frontend engineering. The UI is functional, not polished. The point is the workflow logic, the AI integration layer, and the thinking behind both.

---

## License

MIT — use it, fork it, adapt it.

---

*Built by Jonathan Madden — Senior Technical Program Manager*
*[LinkedIn](https://linkedin.com/in/jonathan-p-madden)*
