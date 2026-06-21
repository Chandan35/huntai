# 🎯 HuntAI — Personal Job Hunt Agent

An AI-powered job hunt agent built with Claude AI. Runs entirely in your browser — no backend, no server, just a single HTML file.

**Live demo:** [your-username.github.io/huntai](https://chandan35.github.io/huntai)

---

## ✨ Features

| Feature | What it does |
|---|---|
| **Resume Parser** | Paste your resume → AI extracts skills, domain, seniority, experience |
| **Job Scanner** | Finds matching jobs from LinkedIn & Indeed based on your profile |
| **Career Links** | Add any company careers page → AI pulls JDs from there |
| **JD Aligner** | Paste any JD → see match %, keywords you have, gaps, and rephrase suggestions |
| **Application Tracker** | Track status (applied → reviewing → interview → offer / rejected) |
| **AI Agent** | Chat with Claude for cover letters, interview prep, follow-up emails |
| **PWA** | Install on phone home screen — works like a native app |
| **Export/Import** | Back up all your data as JSON |

---

## 🚀 Setup Guide (10 minutes)

### Step 1 — Fork & clone this repo

```bash
# Option A: Fork on GitHub (click Fork button top-right), then clone your fork
git clone https://github.com/YOUR_USERNAME/huntai.git
cd huntai

# Option B: Create new repo and push this code (see Step 3)
```

### Step 2 — Get an Anthropic API key (free)

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up / log in
3. Click **API Keys** in the left sidebar
4. Click **Create Key** → copy it (starts with `sk-ant-`)

> **Cost:** Very cheap for personal use. Parsing a resume ≈ $0.001. A full month of job hunting ≈ ₹50–200 total.

### Step 3 — Push to GitHub

If you created a new repo:

```bash
git init
git add .
git commit -m "🎯 Initial HuntAI setup"
git branch -M main
git remote add origin https://github.com/chandan35/huntai.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **GitHub Actions**
4. Click **Save**

GitHub will now auto-deploy every time you push to `main`.

Your app will be live at:
```
https://chandan35.github.io/huntai
```

(Takes ~2 minutes for first deploy)

### Step 5 — Open the app & add your API key

1. Visit your GitHub Pages URL
2. The app will prompt you for your Anthropic API key
3. Enter your `sk-ant-...` key → click **Save**
4. Your key is stored only in your browser's `localStorage`

### Step 6 — Install on your phone (PWA)

**Android (Chrome):**
1. Open the app URL in Chrome
2. Tap the **⋮ menu** → **Add to Home screen**
3. Tap **Add** — it appears as a real app icon

**iPhone (Safari):**
1. Open the app URL in Safari
2. Tap the **Share button** (box with arrow)
3. Scroll down → tap **Add to Home Screen**
4. Tap **Add** — done!

---

## 📁 Project structure

```
huntai/
├── index.html              # Complete app (single file)
├── manifest.json           # PWA manifest
├── sw.js                   # Service worker (offline support)
├── icons/
│   ├── icon-192.png        # App icon (mobile)
│   └── icon-512.png        # App icon (splash)
├── .github/
│   └── workflows/
│       └── deploy.yml      # Auto-deploy to GitHub Pages
└── README.md               # This file
```

---

## 🔐 Privacy & Security

- **Your API key** is stored only in your browser's `localStorage`. It's never sent anywhere except directly to `api.anthropic.com`.
- **Your resume and application data** is stored only in your browser's `localStorage`. Nothing is sent to any server.
- **No analytics, no tracking, no ads.**

---

## 💡 How to use

### Workflow

```
1. Profile → paste resume → AI analyses
       ↓
2. Find Jobs → Scan Jobs → see matches
       ↓
3. JD Aligner → paste JD → see alignment %
       ↓
4. Apply → click Apply on job card
       ↓
5. Tracker → update status as you hear back
       ↓
6. AI Agent → cover letters, follow-ups, interview prep
```

### Tips

- **Load the sample resume** first to see how everything works before pasting your own
- **JD Aligner** is the most powerful feature — paste JDs from any job portal
- **Career links**: paste `https://company.com/careers` for company-specific jobs
- **Export your data** regularly as a backup (Settings → Export JSON)
- **AI Agent quick prompts** cover 80% of use cases — cover letter, follow-up, interview prep

---

## 🔧 Local development

No build step needed. Just open `index.html` in your browser:

```bash
# Option 1: Python server (recommended)
python3 -m http.server 3000
# Open http://localhost:3000

# Option 2: Node serve
npx serve .
# Open http://localhost:3000

# Option 3: VS Code Live Server extension
# Right-click index.html → Open with Live Server
```

---

## 🛣️ Roadmap

- [ ] Supabase integration for cross-device sync
- [ ] Email notifications for application follow-ups
- [ ] Weekly digest email with job matches
- [ ] Resume PDF generation
- [ ] Interview timer + notes
- [ ] Salary benchmarking

---

## 🤝 Built by

**Chandan Kumar G** · [@chandan35](https://github.com/Chandan35)  
Backend Engineer, Bengaluru · Java · Spring Boot · Microservices

Built with [Claude AI](https://anthropic.com) by Anthropic.

---

## 📄 License

MIT — use it, fork it, make it yours.
