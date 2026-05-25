![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=shimu-i/CareerLens)


# CareerLens

**An open, intelligent career preparation platform — free to use, optional to join.**

CareerLens helps fresh graduates and early-career professionals analyze their resumes with real AI feedback, practice mock interviews with an adaptive AI interviewer, track their learning progress over time, and revisit weak areas with personal notes — all without a mandatory account.

---

## Vision & Purpose

Most AI-powered career tools gate their best features behind paywalls, limit the number of resume scans per month, or require account creation just to get started. For students and entry-level job seekers — the people who need this most — those barriers are real.

CareerLens is built on a different premise: **career preparation should be free, private, and unlimited.**

Guests get full access to every tool, every time, with no sign-up required. Those who want to go further — tracking their progress across sessions, reviewing questions they got wrong, building a consistent practice habit — can create a free account. The account unlocks memory and accountability, not features.

This is not a demo or a portfolio piece dressed up as a product. It is a practical tool designed with the same care as commercial alternatives — just without the cost.

---

## Who This Is For

- **Fresh graduates** preparing to enter the job market for the first time
- **Career switchers** updating resumes after a gap or a pivot
- **Students** practicing interview skills before campus recruitment season
- **Self-taught developers or designers** who need their resume to work harder than a formal credential
- **Anyone** who wants honest AI feedback and a structured way to improve over time

---

## How Access Works

CareerLens follows a **guest-first, account-optional** model:

| Capability | Guest | Signed-in User |
|---|---|---|
| Resume analysis | ✅ Unlimited | ✅ Unlimited |
| JD match & gap analysis | ✅ Unlimited | ✅ Unlimited |
| Mock interviews (text + voice) | ✅ Unlimited | ✅ Unlimited |
| Export analysis as PDF | ✅ | ✅ |
| Practice streak heatmap | ❌ | ✅ |
| Interview history & scores | ❌ | ✅ |
| Wrong answer review queue | ❌ | ✅ |
| Personal notes per question | ❌ | ✅ |
| Progress analytics dashboard | ❌ | ✅ |

No feature is locked behind a paid tier. The account exists purely to give you memory — a record of where you've been and what still needs work.

---

## Features

### Resume Analyzer

Upload a PDF or DOCX resume (or paste text directly) and receive a detailed AI-powered evaluation across five dimensions:

- **ATS Compatibility** — how well the resume parses through applicant tracking systems
- **Keyword Density** — whether industry-relevant terms are present and distributed naturally
- **Action Language** — ratio of metric-driven, impact-focused statements versus passive descriptions
- **Structure & Clarity** — section ordering, hierarchy, white space, and readability
- **Overall Impact Score** — a composite score from 0–100 with a plain-English summary

Each dimension produces specific, line-level suggestions. Not "use stronger verbs" — but "replace 'responsible for managing' with 'led' or 'directed' to align with ATS keyword patterns for senior roles."

### JD Match Analyzer

Paste any job description alongside your resume to get a targeted gap analysis:

- Missing hard skills and keywords for that specific role
- Alignment score between your resume and the JD
- Recommended additions and reframings tailored to the posting
- Natural keyword injection suggestions that don't read as stuffed

### AI Mock Interviewer — Text Mode

Select a role, seniority level, and interview type (technical, behavioral, HR, or mixed). CareerLens generates an adaptive interview session:

- Questions are generated fresh each session based on your role selection
- AI evaluates written responses for depth, relevance, and clarity
- Adaptive follow-ups probe vague or surface-level answers
- Post-session report covers every answer with scoring and better alternatives

### AI Mock Interviewer — Voice Mode

The same interview experience, conducted by voice using the browser's built-in Web Speech API:

- No plugins, no extensions, no paid voice services required
- Works in Chrome, Edge, and Safari
- AI listens, transcribes, evaluates, and responds verbally
- Full session transcript with timestamped annotations

### Practice Streak & Activity Heatmap

For signed-in users, the dashboard displays a GitHub-style contribution heatmap showing daily practice activity across the past year:

- Any activity counts: resume analysis, interview sessions, note reviews, confidence ratings
- Streak counter shows current and longest consecutive practice streaks
- Designed to build and sustain a daily learning habit — the single biggest predictor of interview readiness

### Wrong Answer Review Queue

After every interview session, answers marked as weak, incorrect, or uncertain are saved to a personal review queue:

- Each saved question shows the original AI feedback and a model answer
- User assigns a **confidence rating**: *still unsure / getting better / confident*
- The queue automatically surfaces questions marked "still unsure" at the top each session
- Acts as a lightweight spaced-repetition system without the complexity of flashcard apps

### Personal Notes Per Question

Every question in the review queue has a dedicated notes field:

- Plain text, autosaved as you type — no formatting overhead, no folders
- Write your own answer, summarize the model answer in your words, or note what you keep forgetting
- Notes persist across sessions and are searchable from the dashboard
- Designed for the moment before a real interview: open your notes, read through your saved answers, go in prepared

### Progress Analytics Dashboard

A single-screen view of how your skills are developing over time:

- Score history charts per interview type (behavioral, technical, HR)
- Improvement delta — how much each metric has moved since your first session
- Category breakdown of where your wrong answers cluster (e.g., "most weak answers are in behavioral questions about conflict resolution")
- Streak history and total sessions logged

The goal is not to show you how much you've done, but to show you whether you're actually getting better.

### Resume Improvement Generator

Based on analysis output, CareerLens can regenerate individual resume sections:

- Rewrite experience bullets for stronger impact
- Rephrase your summary for a specific target role
- Suggest skill additions based on your job title and industry

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                        User Opens CareerLens                    │
└───────────────┬─────────────────────────────────────────────────┘
                │
        ┌───────▼────────┐
        │  Guest or       │
        │  Signed In?     │
        └───┬────────┬────┘
            │        │
      Guest │        │ Signed In
            ▼        ▼
   Full tool     Full tools +
   access,       history, streak,
   no history    notes, dashboard
            │        │
            └────┬───┘
                 │
         ┌───────▼────────────────────┐
         │     Upload Resume /        │
         │     Start Interview        │
         └───────┬────────────────────┘
                 │
         ┌───────▼────────────────────┐
         │  PDF.js extracts text      │
         │  (client-side, no server)  │
         └───────┬────────────────────┘
                 │
         ┌───────▼────────────────────┐
         │  AI Analysis               │
         │  Gemini API (primary)      │
         │  Puter.js (fallback)       │
         └───────┬────────────────────┘
                 │
         ┌───────▼────────────────────┐
         │  Results rendered:         │
         │  Scores, suggestions,      │
         │  interview feedback        │
         └───────┬────────────────────┘
                 │
         ┌───────▼────────────────────┐
         │  If signed in:             │
         │  Save to Firebase,         │
         │  update streak + queue     │
         └───────┬────────────────────┘
                 │
         ┌───────▼────────────────────┐
         │  Export PDF / copy text    │
         │  Review notes / re-attempt │
         └────────────────────────────┘
```

---

## Tech Stack

| Layer | Technology | Why |
|---|---|---|
| Framework | React 18 + Vite | Fast builds, excellent DX |
| Styling | Tailwind CSS | Utility-first, consistent system |
| Components | shadcn/ui | Accessible, composable primitives |
| PDF Parsing | PDF.js (Mozilla) | Client-side, no backend needed |
| AI — Primary | Google Gemini API (free tier) | 1,500 req/day free, high quality |
| AI — Fallback | Puter.js | No API key required, always free |
| Voice | Web Speech API (browser native) | Zero cost, no third-party service |
| Auth | Firebase Authentication | Free tier, email + Google OAuth |
| Database | Firebase Firestore | Free tier, real-time, schemaless |
| State | Zustand | Minimal, hook-based |
| Routing | React Router v7 | Nested routes, loaders |
| Export | jsPDF + html2canvas | Client-side PDF generation |
| Deployment | Vercel / Cloudflare Pages | Free, global CDN |

**AI inference is free. Auth and database use Firebase free tier (10GB storage, 50K reads/day). Hosting is free. Total operating cost: $0.**

---

## System Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                        Browser (Client)                       │
│                                                              │
│  ┌────────────┐  ┌────────────┐  ┌──────────┐  ┌─────────┐ │
│  │  React UI  │  │  PDF.js    │  │  Voice   │  │ Zustand │ │
│  │  + Router  │  │  Parser    │  │  (WSA)   │  │  Store  │ │
│  └─────┬──────┘  └─────┬──────┘  └────┬─────┘  └────┬────┘ │
│        └───────────────┴──────────────┴──────────────┘      │
│                              │                               │
│                    ┌─────────▼──────────┐                    │
│                    │   Analysis Engine  │                    │
│                    │   + Prompt Layer   │                    │
│                    └────┬──────────┬────┘                    │
│                         │          │                         │
│               ┌─────────▼─┐  ┌─────▼──────────┐            │
│               │ Gemini API│  │   Puter.js AI  │            │
│               │ (primary) │  │   (fallback)   │            │
│               └───────────┘  └────────────────┘            │
│                                                              │
│                    ┌───────────────────┐                     │
│                    │  Auth Layer       │                     │
│                    │  Firebase Auth    │                     │
│                    └────────┬──────────┘                     │
│                             │                                │
│               ┌─────────────▼──────────────┐                │
│               │       Firebase Firestore    │                │
│               │  sessions / wrong answers  │                │
│               │  notes / streaks / scores  │                │
│               └────────────────────────────┘                │
└──────────────────────────────────────────────────────────────┘
```

Guest users bypass the auth and Firestore layers entirely. Their session state lives in browser memory only.

---

## Database Schema (Firestore)

```
users/{uid}
  ├── profile
  │   ├── displayName: string
  │   ├── email: string
  │   └── createdAt: timestamp
  │
  ├── sessions/{sessionId}
  │   ├── type: "resume" | "interview" | "jd-match"
  │   ├── createdAt: timestamp
  │   ├── score: number
  │   ├── role: string (interview sessions)
  │   └── questions/{questionId}
  │       ├── text: string
  │       ├── userAnswer: string
  │       ├── aiScore: number
  │       ├── aiFeeback: string
  │       ├── modelAnswer: string
  │       ├── flagged: boolean          ← saved to review queue
  │       ├── confidence: "unsure" | "improving" | "confident"
  │       └── notes: string             ← personal notes field
  │
  ├── streaks
  │   ├── current: number
  │   ├── longest: number
  │   └── activityLog/{YYYY-MM-DD}: true  ← heatmap data
  │
  └── stats
      ├── totalSessions: number
      ├── totalQuestions: number
      ├── avgScoreByType: { behavioral, technical, hr }
      └── scoreHistory: [{ date, score, type }]
```

---

## Project Structure

```
careerlens/
├── public/
│   └── fonts/
├── src/
│   ├── components/
│   │   ├── ui/               # shadcn/ui base components
│   │   ├── resume/           # Upload, preview, highlights
│   │   ├── analysis/         # Score panels, feedback cards
│   │   ├── interview/        # Question cards, timer, voice
│   │   ├── dashboard/        # Heatmap, stats, review queue
│   │   └── shared/           # Layout, nav, auth modals
│   ├── lib/
│   │   ├── pdf.ts            # PDF.js text extraction
│   │   ├── ai.ts             # Gemini + Puter.js abstraction
│   │   ├── prompts.ts        # All AI prompt templates
│   │   ├── scoring.ts        # Evaluation rubric logic
│   │   ├── voice.ts          # Web Speech API wrapper
│   │   ├── firebase.ts       # Firebase init + helpers
│   │   └── export.ts         # PDF report generation
│   ├── store/
│   │   ├── resume.ts         # Resume state
│   │   ├── session.ts        # Interview session state
│   │   └── auth.ts           # Auth state (Zustand)
│   ├── pages/
│   │   ├── Home.tsx
│   │   ├── Analyze.tsx
│   │   ├── Interview.tsx
│   │   ├── Dashboard.tsx     # Signed-in users only
│   │   ├── Review.tsx        # Wrong answer queue
│   │   └── Report.tsx
│   └── main.tsx
├── .env.example
├── vite.config.ts
├── tailwind.config.ts
└── package.json
```

---

## Getting Started

### Prerequisites

- Node.js 18 or higher
- npm or pnpm
- A free Google Gemini API key (optional)
- A free Firebase project (required only for auth + history features)

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/careerlens.git
cd careerlens
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up Firebase

1. Go to [console.firebase.google.com](https://console.firebase.google.com) and create a new project
2. Enable **Authentication** → Email/Password and Google sign-in
3. Enable **Firestore Database** → start in test mode
4. Copy your project config from Project Settings

### 4. Configure environment variables

```bash
cp .env.example .env.local
```

```env
# Google Gemini — free tier, 1500 requests/day
# https://aistudio.google.com/app/apikey
VITE_GEMINI_API_KEY=your_key_here

# Firebase project config
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=

VITE_BASE_URL=http://localhost:5173
```

> If you skip the Gemini key, the app uses Puter.js automatically.
> If you skip Firebase entirely, the app works in full guest mode only.

### 5. Run the development server

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

### 6. Build for production

```bash
npm run build
```

Deploy the `dist/` folder to Vercel, Netlify, or Cloudflare Pages.

---

## Browser Compatibility

| Feature | Chrome | Edge | Safari | Firefox |
|---|---|---|---|---|
| Resume analysis | ✅ | ✅ | ✅ | ✅ |
| PDF parsing | ✅ | ✅ | ✅ | ✅ |
| Text interview | ✅ | ✅ | ✅ | ✅ |
| Voice interview | ✅ | ✅ | ✅ | ⚠️ Limited |
| Account + history | ✅ | ✅ | ✅ | ✅ |

Voice mode works best in Chromium-based browsers. A text fallback is always available.

---

## Privacy

CareerLens is designed around privacy as a constraint, not an afterthought:

- **Guest users:** nothing leaves your browser. No resume is stored anywhere.
- **Signed-in users:** only session scores, question history, notes, and streak data are stored in Firestore — not the resume text itself
- **No analytics, no tracking, no ads** — the app makes no third-party analytics calls
- **Account deletion** wipes all Firestore data permanently, on request
- AI calls go directly from your browser to Gemini or Puter.js — not through a CareerLens server

---

## Roadmap

### v1.0
- [x] Resume upload and analysis
- [x] JD match and gap analysis
- [x] Text and voice mock interviews
- [x] PDF export
- [x] Optional account with Firebase
- [x] Practice streak heatmap
- [x] Wrong answer review queue
- [x] Personal notes per question
- [x] Progress analytics dashboard

### v1.1
- [ ] LinkedIn and GitHub profile import
- [ ] Dark mode
- [ ] Multi-language resume support
- [ ] Shareable session reports (hash-based, no server)

### v1.2
- [ ] Confidence-based question scheduling (spaced repetition)
- [ ] Role-specific question banks
- [ ] Interview performance comparison across sessions (overlaid charts)

### v2.0
- [ ] Cover letter generator aligned to resume + JD
- [ ] Portfolio brief analyzer (URL input)
- [ ] Offline mode via service worker
- [ ] Role-specific AI interviewer personas

---

## Contributing

Before adding a feature, ask:

1. Does it work without a paid dependency?
2. Does it respect guest users (no forced sign-up)?
3. Does it make the learning loop better, or just add surface area?

```bash
git checkout -b feature/your-feature-name
# make changes
npm run test
npm run lint
# open a pull request
```

Every new AI prompt must live in `src/lib/prompts.ts` with a comment explaining its intent and expected output structure. No `any` types in new TypeScript. UI components should be accessible — use shadcn/ui as a base.

---

## License

MIT. See [LICENSE](./LICENSE). Free to use, modify, and distribute — commercially or otherwise — with attribution.

---

## Acknowledgements

Inspired by [JavaScript Mastery](https://www.youtube.com/@javascriptmastery) (Prepwise, AI Resume Analyzer), the [Puter.js](https://puter.com) team for making serverless AI genuinely free, and every job seeker who has been told their resume "needs work" without being told exactly why.

---

*CareerLens — built for the people who need it most.*
