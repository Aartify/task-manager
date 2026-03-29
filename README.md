# ⬡ TaskAI — Intelligent Task Manager

A sleek, AI-powered task manager built with vanilla HTML/CSS/JS and **Claude (Anthropic)** as the AI backbone. Deploy to any static hosting platform in minutes.

![TaskAI Screenshot](screenshot.png)

## ✦ Features

- **AI Assistant** — Chat with Claude to get task suggestions, breakdowns, and priorities
- **Smart Task Cards** — Priority-colored cards with due dates and completion tracking
- **Claude on Save** — Automatically gets a productivity tip from Claude when you add a task
- **Analytics Dashboard** — Visual donut chart, completion gauge, and priority timeline
- **Gravity Buttons** — Smooth animated buttons with shimmer effects
- **Dark Futuristic UI** — Animated background orbs, glassmorphism sidebar, gradient accents
- **Persistent Storage** — Tasks saved in localStorage — survives page refreshes
- **Fully Responsive** — Works on mobile, tablet, and desktop

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/task-ai.git
cd task-ai
```

### 2. Add your Claude API key

Open `app.js` and find this section:

```js
const response = await fetch('https://api.anthropic.com/v1/messages', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'x-api-key': 'YOUR_API_KEY_HERE',   // ← add your key
    'anthropic-version': '2023-06-01',
    'anthropic-dangerous-direct-browser-access': 'true'
  },
  ...
```

Get a free API key at [console.anthropic.com](https://console.anthropic.com).

> ⚠️ **Note:** For production, use a backend proxy to keep your API key secret.

### 3. Open in browser

Just open `index.html` in your browser — no build step needed!

```bash
open index.html
# or on Linux:
xdg-open index.html
```

## ☁️ Deploy to Netlify (Free)

1. Push your code to GitHub
2. Go to [netlify.com](https://netlify.com) → **New site from Git**
3. Select your repo → Deploy
4. Add your API key as a Netlify environment variable (use a proxy for security)

## ☁️ Deploy to Vercel (Free)

```bash
npm i -g vercel
vercel
```

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| UI | Vanilla HTML + CSS + JS (zero dependencies) |
| AI | Anthropic Claude Sonnet via REST API |
| Fonts | Syne (display) + DM Sans (body) + DM Mono |
| Storage | Browser localStorage |
| Hosting | Any static host (Netlify, Vercel, GitHub Pages) |

## 📁 File Structure

```
task-ai/
├── index.html      # App markup and layout
├── style.css       # Dark theme with Gravity button styles
├── app.js          # Task logic + Claude API calls
└── README.md       # This file
```

## 🤖 AI Features Explained

### Chat Assistant
Navigate to **AI Assistant** to chat directly with Claude. It has full context of your current tasks.

### Smart Suggestions on Save
When adding a task, check **"Let Claude suggest improvements"** to get a one-line Claude tip automatically.

### Suggested Prompts
Click any chip in the AI view to instantly ask Claude about prioritization, task breakdowns, or today's focus.

## 🎨 Customization

Change the accent color in `style.css`:
```css
:root {
  --accent: #a78bfa;   /* purple */
  --accent2: #38bdf8;  /* sky blue */
}
```

## 📄 License

MIT — free to use, modify, and deploy.

---

Made with ⬡ and Claude AI
