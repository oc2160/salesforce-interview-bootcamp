# 🚀 Salesforce Interview Bootcamp — AI-Powered Training App

> An interactive, AI-powered Salesforce Developer interview preparation tool built as a single-page HTML application. Covers all 8 phases of interview readiness — from Salesforce fundamentals to mock interviews — with a live AI interviewer that scores answers, gives feedback, and simulates real MNC interview conditions.

---

## 📸 Preview

> The app features a dark-themed, professional UI with:
> - A phase-based curriculum sidebar (8 phases)
> - Structured theory cards (Concept → Analogy → Interview Answer → Tricky Questions → Code Examples)
> - A live AI Interviewer chat panel with scoring
> - Full Mock Interview, Rapid Fire, and Coding Challenge modes

---

## 🎯 What This App Covers

| Phase | Topics |
|-------|--------|
| **1 — SF Fundamentals** | Architecture, Multitenancy, Objects, Security Model, Flows, Validation Rules, Deployment |
| **2 — Apex Development** | Triggers, Governor Limits, Bulkification, SOQL/SOSL, Async Apex, Test Classes |
| **3 — LWC** | Architecture, Decorators (@api/@wire/@track), Events, Apex Integration, Lifecycle Hooks |
| **4 — Scenario Mastery** | Trigger Recursion, Bulk Issues, Security Gaps, Integration Failures, Flow vs Trigger |
| **5 — Interview Simulation** | HR rounds, Fresher challenges, Tell Me About Yourself, Project discussions |
| **6 — Advanced Topics** | Agentforce, Prompt Builder, DevOps/SFDX, Sandbox Strategy, AI in Salesforce |
| **7 — Mock Interviews** | Rapid Fire rounds, Coding challenges, Full mock simulations |
| **8 — Job Readiness** | Resume tips, LinkedIn, Application strategy, Company-specific preparation |

---

## ⚡ Features

- **AI Interviewer** — Powered by Anthropic Claude API. Evaluates answers, scores out of 10, gives specific feedback like a real MNC hiring manager
- **Full Mock Interview Mode** — Simulates a complete Technical + HR round
- **Rapid Fire Mode** — 10 quick questions with instant scoring
- **Coding Challenge Mode** — Write Apex code and receive code-review-style feedback
- **Structured Theory Cards** — Every topic broken into: Concept, Real-World Analogy, Interview Answer, Tricky Follow-Ups, Beginner Mistakes, Scenario Questions, and Code Examples
- **Quick Reply Buttons** — Context-aware suggested responses to keep interview flow going

---

## 🛠️ Tech Stack

| Technology | Usage |
|-----------|-------|
| HTML5 / CSS3 | UI structure and styling |
| Vanilla JavaScript (ES6+) | App logic, state management, API calls |
| Anthropic Claude API (`claude-sonnet-4-20250514`) | AI Interviewer responses and evaluation |
| Google Fonts (Syne, IBM Plex Mono, Inter) | Typography |
| CSS Custom Properties | Theming and design tokens |

---

## 🔧 How to Run

### Option 1 — View as Static UI (No AI, works offline)
1. Clone this repository
   ```bash
   git clone https://github.com/YOUR_USERNAME/salesforce-interview-bootcamp.git
   ```
2. Open `sf_bootcamp.html` in any browser
3. The theory content, cards, and UI will fully work
4. The AI Interviewer chat requires an API key (see Option 2)

### Option 2 — Enable AI Interviewer (Requires Anthropic API Key)
The AI chat panel calls the [Anthropic Messages API](https://docs.anthropic.com/en/api/messages). To enable it locally:

1. Open `sf_bootcamp.html` in a code editor
2. Find the `fetch('https://api.anthropic.com/v1/messages', ...)` call
3. Add your API key to the headers:
   ```javascript
   headers: {
     'Content-Type': 'application/json',
     'x-api-key': 'YOUR_API_KEY_HERE',          // Add this
     'anthropic-version': '2023-06-01'            // Add this
   }
   ```
4. Get an API key at [console.anthropic.com](https://console.anthropic.com)

> ⚠️ **Note:** Never commit your API key to a public repository. For production use, proxy the API call through a backend server.

---

## 💡 Why I Built This

As a fresher Salesforce Developer preparing for interviews at Indian MNCs (TCS, Infosys, Accenture, Deloitte, Cognizant, Capgemini) and Salesforce partner companies, I wanted a structured, interactive preparation tool that:

- Covers theory **and** teaches you how to *explain* it in interviews
- Simulates actual MNC interviewer behavior (not just Q&A lists)
- Gives scored feedback on answers to track improvement
- Includes scenario-based questions from real interview experiences

The app is built as a **single HTML file** — no build tools, no npm, no frameworks — just clean HTML/CSS/JS with an API integration.

---

## 📚 Topics Deep-Dived

### Salesforce Architecture
- Multitenant cloud, Hyperforce, MVC pattern, Governor limits rationale

### Apex Best Practices
- One trigger per object pattern, Handler classes, Bulkification, Collections over loops
- All 4 Async patterns: @future, Queueable, Batch, Scheduled — when to use each

### LWC
- Shadow DOM, @wire vs Imperative Apex, Parent-child event communication
- LWC lifecycle hooks: connectedCallback, disconnectedCallback, renderedCallback

### Security Model
- 4 layers: Org → Object (CRUD) → Field (FLS) → Record (OWD/Sharing)
- Profile vs Permission Set vs Role — the interview trap question

### Agentforce & AI
- Atlas Reasoning Engine, Topics, Actions, Einstein Trust Layer
- Prompt Builder, grounding, debugging AI agents

---

## 🏗️ Project Structure

```
salesforce-interview-bootcamp/
│
├── sf_bootcamp.html        # Main application (single file)
├── README.md               # This file
└── screenshots/            # (Optional) Add screenshots of the UI
```

---

## 👨‍💻 About the Developer

**Omkar** — Fresher Salesforce Developer from Pune, India

- 🏆 Salesforce Certified Platform Developer I (PD1)
- 🎓 MCA in Data Science — MIT ADT University (2023–2025)
- 💼 IBM Intern — Watson Assistant, IBM Cloud, AI/ML
- ✅ Superbadges: Apex Web Service, Record Triggered Flow, Flow Fundamentals, Agentforce Service, Flow Optimization
- 📍 Open to: Salesforce Developer roles in Pune / Mumbai / Bangalore / Remote

[![Salesforce](https://img.shields.io/badge/Salesforce-PD1_Certified-00A1E0?style=flat&logo=salesforce)](https://trailhead.salesforce.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/YOUR_LINKEDIN)

---

## 🤝 Contributing

Feel free to open issues or PRs if you:
- Want to add more Salesforce topics
- Find an incorrect answer or outdated information
- Want to add a new interview mode

---

## 📄 License

MIT License — free to use, modify, and share.

---

> 💬 *"Built this to crack my own Salesforce interviews. If it helps you too, give it a ⭐"*
