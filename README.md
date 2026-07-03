# GenAI Ninja — Builder Program LMS

A personal learning management system for the GenAI Ninja Builder Program.

## Live site

Hosted on GitHub Pages:  
`https://<your-github-username>.github.io/genai-ninja-lms/`

## Setup (5 minutes)

### 1. Create the repository

```bash
# Option A — GitHub CLI (recommended)
gh repo create genai-ninja-lms --public --description "GenAI Ninja Builder Program LMS"

# Option B — Create manually at github.com/new
# Name: genai-ninja-lms | Visibility: Public
```

### 2. Push the files

```bash
git clone https://github.com/<your-username>/genai-ninja-lms.git
cd genai-ninja-lms
cp /path/to/genai-ninja-lms.html index.html
cp /path/to/README.md README.md
git add .
git commit -m "Initial LMS deploy"
git push origin main
```

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main` | Folder: `/ (root)`
5. Click **Save**

Your site will be live at `https://<username>.github.io/genai-ninja-lms/` within 1–2 minutes.

## Features

- **Dashboard** — live progress stats, today's goals, module cards
- **Lessons** — content, code lab (runnable Python), and quiz per module  
- **Roadmap** — prerequisite-gated module graph
- **Spaced review** — SM-2 flashcard queue with Again/Hard/Good/Easy ratings
- **AI Mentor** — Claude-powered chat grounded in your current module
- **Portfolio** — projects unlock as you complete lessons, with resume bullets
- **Journal** — freeform notes attached to your learning session
- **Analytics** — live progress bars derived from actual lesson completions
- **⌘K** — command palette for keyboard navigation

## Progress persistence

Progress is stored in **browser localStorage** — it survives page refreshes automatically. Use the **reset progress** button in the sidebar footer to start fresh.

## Notes

- The AI Mentor requires an Anthropic API key passed through the `claude.ai` hosted environment. If running standalone, the mentor falls back to curated offline responses.
- No backend, no database, no build step — pure HTML + React (CDN).

## Tech stack

| Layer | Tech |
|---|---|
| UI framework | React 18 (CDN, Babel standalone) |
| Icons | Tabler Icons (webfont) |
| Fonts | IBM Plex Mono + Inter (Google Fonts) |
| Storage | Browser localStorage |
| AI | Anthropic Claude API (claude-sonnet-4-6) |
| Hosting | GitHub Pages (static) |
