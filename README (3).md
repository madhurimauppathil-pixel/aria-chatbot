# ARIA — AI Chatbot Assistant

> A professional, generative AI chatbot with intent recognition, context memory, smart fallback, analytics, and an embeddable website widget. Built with HTML, CSS, and JavaScript — powered by the Claude API.

![ARIA Chatbot](https://img.shields.io/badge/AI-Claude%20API-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/status-live-brightgreen?style=flat-square)
![Deploy](https://img.shields.io/badge/deployed-GitHub%20Pages-black?style=flat-square)

---

## Live Demo

🔗 **[View Live → https://YOUR-USERNAME.github.io/aria-chatbot](https://YOUR-USERNAME.github.io/aria-chatbot)**

---

## Screenshots

| Chat Interface | Website Widget |
|---|---|
| Clean chat UI with intent detection | Embeddable floating widget for any website |

---

## Features

| Feature | Description |
|---|---|
| **Context Awareness** | Full conversation history sent with every request — ARIA remembers everything |
| **Intent Recognition** | Automatically classifies messages as Help, Pricing, Support, or General |
| **Smart Fallback** | Detects uncertainty and offers escalation to a human agent |
| **Generative AI** | Powered by Claude API with real-time streaming responses |
| **Website Widget** | Embeddable floating chat widget — drop into any website |
| **Export Chat** | Download full conversation as a `.txt` file |

---

## Tech Stack

- **Frontend** — Pure HTML, CSS, JavaScript (no framework needed)
- **AI Engine** — [Anthropic Claude API](https://docs.anthropic.com) (claude-sonnet-4)
- **Fonts** — DM Sans + DM Serif Display (Google Fonts)
- **Hosting** — GitHub Pages (free)
- **No backend required** — runs entirely in the browser

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/aria-chatbot.git
cd aria-chatbot
```

### 2. Open Locally

Just open `index.html` in your browser — no build step, no server needed.

```bash
# On Mac
open index.html

# On Windows
start index.html

# Or just drag the file into Chrome/Firefox
```

### 3. Add Your API Key

The chatbot runs in **demo mode** by default (pre-written responses, no API needed).

To enable live AI responses:
1. Get a free API key at [console.anthropic.com](https://console.anthropic.com)
2. Open the app, click **"Connect API key"** in the input bar footer
3. Paste your key — it's stored only in your browser's session memory

> ⚠️ **Never commit your API key to GitHub.** The key is stored in `sessionStorage` and never leaves your browser.

---

## Project Structure

```
aria-chatbot/
│
├── index.html          ← Main chatbot interface (everything in one file)
├── README.md           ← This file
└── .gitignore          ← Ignores sensitive files
```

> This project is intentionally a single HTML file for simplicity and portability. You can drop it into any project or host it anywhere.

---

## Deploying to GitHub Pages (Free Live Hosting)

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon → **New repository**
3. Name it: `aria-chatbot`
4. Set it to **Public**
5. Click **Create repository**

### Step 2 — Upload Your Files

**Option A — Using the GitHub website (easiest):**
1. Click **"uploading an existing file"** on the new repo page
2. Drag and drop `aria-chatbot.html` and `README.md`
3. Rename `aria-chatbot.html` → `index.html` (important!)
4. Click **Commit changes**

**Option B — Using Git terminal:**
```bash
# Inside your project folder
git init
git add .
git commit -m "Initial commit — ARIA AI Chatbot"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/aria-chatbot.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Choose branch: **main**, folder: **/ (root)**
6. Click **Save**

### Step 4 — Your site is live! 🎉

After 1–2 minutes, your chatbot will be live at:
```
https://YOUR-USERNAME.github.io/aria-chatbot
```

> GitHub Pages rebuilds automatically every time you push a new commit.

---

## Embedding the Widget on Any Website

Copy this single line into any HTML page to show the chat widget:

```html
<!-- Add before </body> -->
<script>
  const iframe = document.createElement('iframe');
  iframe.src = 'https://YOUR-USERNAME.github.io/aria-chatbot';
  iframe.style.cssText = 'position:fixed;bottom:20px;right:20px;width:370px;height:520px;border:none;border-radius:16px;box-shadow:0 8px 32px rgba(0,0,0,0.15);z-index:9999';
  document.body.appendChild(iframe);
</script>
```

Or use the built-in widget by clicking the **grid icon** in the chatbot header.

---

## Customisation

### Change the AI Personality

Edit the system prompt in the code (search for `system:` in `index.html`):

```javascript
system: 'You are ARIA, a professional AI assistant for [YOUR COMPANY]. 
         Help users with questions about [YOUR PRODUCT]. 
         Be friendly, concise, and always suggest escalation if unsure.'
```

### Change the Model

Switch between models in the dropdown or edit the default:

```javascript
// Fast and cheap
model: 'claude-haiku-4-5-20251001'

// Balanced (default)
model: 'claude-sonnet-4-20250514'
```

### Add Pre-written Responses

In the `demo()` function, add custom responses for your use case:

```javascript
function demo(text, k) {
  var d = {
    pricing: 'Your custom pricing response here...',
    support: 'Your custom support response here...',
    // add more...
  };
  return d[k] || d.general;
}
```

---

## Making Updates After Deployment

Whenever you edit `index.html`, push to GitHub and it auto-deploys:

```bash
git add index.html
git commit -m "Update: improved hero section"
git push
```

Changes go live in ~60 seconds.

---

## Common Issues

| Problem | Fix |
|---|---|
| Site shows 404 | Make sure the file is named `index.html` not `aria-chatbot.html` |
| API responses not working | Check your API key is valid and has credits |
| Changes not showing | Wait 1–2 minutes, then hard refresh (`Ctrl+Shift+R`) |
| Widget not appearing | Make sure GitHub Pages is enabled in repository Settings |

---

## License

MIT License — free to use, modify, and distribute.

---

## Built With

- [Anthropic Claude API](https://docs.anthropic.com)
- [DM Sans & DM Serif Display](https://fonts.google.com) — Google Fonts
- [GitHub Pages](https://pages.github.com) — free hosting

---

*Made with ❤️ — ARIA AI Chatbot v3.0*
