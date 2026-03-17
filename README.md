# PM AI Agents

After a decade building AI/ML platforms at Amazon, I built these agents to apply the same thinking to my own workflows: structured intelligence, automated research, and deliberate practice — powered by Claude API.

---

## Projects

### 1. PM Intelligence Brief
> A daily AI-powered intelligence digest that surfaces what's actually shifting in the industry — not just what happened, but what it means.

- **Stack**: Python · Flask · Claude API · SQLite · Railway · APScheduler
- **What it does**: Runs every morning at 7am IST, pulls from 39 curated sources across 8 themes, and runs a 3-pass Claude pipeline — signal extraction per item, cross-source synthesis with inline citations, then LLM-as-judge evaluation across 5 quality dimensions. Every digest is automatically scored on a 100pt weighted scale.
- **Live**: [pm-intelligence-digest-production.up.railway.app](https://pm-intelligence-digest-production.up.railway.app) · [Evals Dashboard](https://pm-intelligence-digest-production.up.railway.app/evals) · [Archive](https://pm-intelligence-digest-production.up.railway.app/history)
- **Repo**: [pm-intelligence-digest](https://github.com/mounicasirineni/pm-intelligence-digest)

---

### 2. PM Research Toolkit
> A personal system for building deep, structured knowledge on products, companies, and markets — powered by Google Deep Research and Claude API.

- **Stack**: Google Deep Research · Bolt (React + Vite) · Supabase (PostgreSQL + Edge Functions) · Claude API
- **What it does**: Four prompt templates (Product Teardown, Domain Primer, Company Deep Dive, Competitive Landscape) that run as sequential 6-7 prompt threads in Google Deep Research. Output pastes into a library app where a Claude API Supabase Edge Function auto-formats plain text into structured markdown. Each piece ends with a synthesis and prepared opinion grounded in the research.
- **Live**: [pm-research-library-xma0.bolt.host](https://pm-research-library-xma0.bolt.host/)
- **Repo**: [pm-research-toolkit](https://github.com/mounicasirineni/pm-research-toolkit)

---

### 3. PM Interview Simulator
> A conversational AI-powered interview simulator — live back-and-forth with an interviewer who pushes back, probes weaknesses, and doesn't let you off the hook with vague answers.

- **Stack**: Vanilla JS · Bolt edge functions · Bolt managed database · Claude Sonnet · Sarvam AI (voice)
- **What it does**: Three-agent system — Generator picks from 70 seeded real PM questions or generates a new one via few-shot prompting; Interviewer conducts category-aware back-and-forth with real pacing; Evaluator scores the full transcript across Structure, Specificity, Opinion Clarity, and Depth Under Pressure with a calibrated rubric and specific debrief. Session history and score trends tracked over time.
- **Repo**: [pm-interview-simulator](https://github.com/mounicasirineni/pm-interview-simulator)

---

## How Claude Is Used Across All Three

Each project uses Claude differently:

| Project | How Claude is used |
|---|---|
| PM Intelligence Brief | Pass 1: signal extraction per source · Pass 2: cross-source synthesis with citations · Pass 3: LLM-as-judge quality evaluation |
| PM Research Toolkit | Supabase Edge Function: plain text → structured markdown auto-formatter |
| PM Interview Simulator | Three-agent system: question generation · live conversational interviewing · transcript evaluation |

## Built With

Python · Flask · SQLite · Railway · React · Vite · Bolt · Supabase · Claude API · Google Deep Research · Sarvam AI · Cursor
