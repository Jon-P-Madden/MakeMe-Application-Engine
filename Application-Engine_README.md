# Make Me! Application Engine

**Make Me! Application Engine** is an AI-assisted job application workspace that analyzes postings, tailors application materials, generates cover letters, and tracks application activity.

Part of the **Make Me!** career tools suite - built by a Senior Technical Program Manager to solve real job search problems with practical AI-assisted workflows.

Most job trackers record activity. This one helps create the application package.

No installation. No backend. No friction.

![Make Me! Application Engine](Screenshot.png)

---

## What This Demonstrates

- Guided application workflow that moves from job posting to application-ready materials
- AI-assisted job description analysis and fit review
- Job-specific tailoring built on user profile and resume positioning
- Cover letter generation as part of the application workflow
- Lightweight application tracking and status management
- Browser-first prototype architecture with local persistence and export support

---

## The Problem

Applying to jobs is not just a tracking problem. A user has to understand the posting, identify what matters, adapt their resume, write a credible cover letter, decide what to do next, and remember where each application stands.

Most tools split those tasks apart. A tracker stores the status. A document editor holds the resume. A separate AI chat may draft a cover letter without enough context. The Application Engine brings those steps into one job-specific workflow.

---

## The Solution

The engine turns career positioning into job-specific execution:

1. Captures the job description, company, role, profile, resume version, and application context
2. Analyzes the role requirements and fit signals
3. Identifies tailoring opportunities for the application package
4. Generates job-specific application guidance and cover letter content
5. Supports follow-up message drafting when tied to the application
6. Tracks application notes, status, and next steps
7. Keeps the workflow focused on the specific job opportunity

Cover letters belong inside this engine because they are part of the job-specific application package.

---

## Design Constraints (Intentional)

- Single-file browser prototype for portability and easy review
- No backend required for the current prototype
- Runtime API key input instead of stored secrets
- Browser `localStorage` persistence for application data
- Browser-first workflow for quick local use
- Application-centered UX rather than a generic document generator
- Cover letter generation integrated directly into the application workflow

---

## Features

### Job Intake

- Job description intake
- Company and target role context
- User profile and resume context
- Optional LinkedIn profile/version context
- Application status and notes
- Tone preference

### AI Analysis

- Job description analysis
- Job fit review
- Role requirement extraction
- Keyword and gap review
- Recommended next steps

### Application Materials

- Job-specific resume tailoring support
- Cover letter generation
- Application notes
- Follow-up message drafts
- Tailored guidance for the target role

### Pipeline / Tracking

- Application status tracking
- Pipeline updates
- Saved application records
- Dashboard-style application activity overview in the prototype
- Local persistence through the browser

---

## Architecture

```text
User Browser
  |
  v
Application Engine UI
  |
  +--> Job description and application intake
  |
  +--> localStorage application/profile data
  |
  +--> Job analysis and tailoring workflow
  |       |
  |       v
  |   Runtime-selected AI provider/model
  |
  v
Application guidance, cover letter, follow-up drafts, pipeline updates, and exports
```

The current engine is designed as a local-first browser prototype. The UI captures job and user context, local storage keeps application activity available in the browser, AI-assisted analysis supports tailoring, and the output workflow creates practical application materials.

---

## Setup

1. Clone or download the repository.
2. Open `app/engines/job-application.html` in a browser.
3. Enter an API key for the selected AI provider when prompted by the app.
4. Add a job description and application context.
5. Review the job analysis and tailoring guidance.
6. Generate a cover letter, save application notes, and update the application status.

**No installation. No build step. No server.**

---

## Known Limitations

- Client-side API calls are prototype-oriented and may depend on provider browser policies.
- `localStorage` is browser-local and does not sync across devices.
- The prototype has no backend, database, authentication, or cloud sync.
- Job URL extraction can be limited in a static browser-only workflow.
- Generated application materials still need human review before use.
- Pipeline tracking is local to the current browser environment.

---

## Tech Stack

- Vanilla HTML / CSS / JavaScript
- Browser `localStorage`
- Runtime AI provider/API key input
- No backend
- No database
- No build tooling required for the prototype

---

## Roadmap

- Strengthen job description parsing and structured validation
- Improve application history, filtering, and analytics
- Add richer application-stage workflows
- Integrate more deeply with resume and LinkedIn versions
- Expand export options for application materials
- Separate shared storage, profile, and pipeline systems when the architecture matures

---

## Part of the Make Me! Suite

| Engine | Tool | Purpose |
|--------|------|---------|
| Engine 1 | **Make Me! Resume Positioning Engine** | Build a strategically positioned resume from raw career history |
| Engine 2 | **Make Me! Application Engine** | Analyze job postings, tailor application materials, generate cover letters, and track applications |
| Engine 3 | **Make Me! LinkedIn Optimization Engine** | Optimize LinkedIn profiles for recruiter searchability and credibility |
| Engine 4 | **Make Me! Interview Prep Engine** | Planned engine for interview questions, STAR stories, and role-specific prep |
| Engine 5 | **Make Me! Salary Negotiation Engine** | Planned engine for compensation strategy, counteroffers, and negotiation messaging |
| Engine 6 | **Make Me! Recruiter Outreach Engine** | Planned engine for recruiter, referral, and networking outreach |

---

## Why This Exists

Job seekers do not need another place to simply record that they applied. They need help turning a real job posting into a stronger application package.

This engine exists because the most valuable application work happens between reading the posting and pressing submit: understanding fit, adapting positioning, writing a relevant cover letter, and deciding what to do next. The Application Engine makes that middle work visible, guided, and reusable.

- **Application design** - organizes the messy middle of applying, not just the final status
- **AI as interpreter** - model output used to read the job posting and connect it to user context
- **Workflow thinking** - job analysis, tailoring, cover letter, notes, and status in one flow
- **Constraint-driven architecture** - browser-first, local-first, and portable

---

## License

MIT — use it, fork it, adapt it.

---

*Built by Jonathan Madden*
*[LinkedIn](https://linkedin.com/in/jonathan-p-madden) - [github.com/Jon-P-Madden](https://github.com/Jon-P-Madden)*
