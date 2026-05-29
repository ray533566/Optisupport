# ⬡ OptiSupport — Optical Transceiver AI Assistant

> AI-powered customer support portal for optical transceiver technology.  
> Built with HTML · CSS · JavaScript · Claude Sonnet 4 API

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Ready-brightgreen)
![Claude API](https://img.shields.io/badge/Powered%20by-Claude%20Sonnet%204-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📡 Overview

**OptiSupport** is a single-page AI assistant website for optical transceiver support engineers and customers. It provides expert-level answers on:

- **Product specifications** — QSFP-DD, QSFP28, SFP28, CFP2, OSFP
- **Link budget calculations** — power, loss, dispersion analysis
- **CMIS 5.2** — register maps, module state machine, CDB commands
- **FEC / BER** — RS-FEC, KP4-FEC, pre/post-FEC thresholds
- **DOM / DDM diagnostics** — alarms, thresholds, real-time monitoring
- **Troubleshooting** — BER issues, thermal problems, module detection
- **Standards** — IEEE 802.3, SFF-8472, SFF-8636, SFF-8024, OIF

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Step 1 — Fork or create repository

```bash
# Option A: Clone this repo
git clone https://github.com/YOUR_USERNAME/optisupport.git

# Option B: Create new repo and add files
git init optisupport
cd optisupport
```

### Step 2 — Add the files

Copy `index.html` and `README.md` into the repository root:

```
optisupport/
├── index.html      ← main website file
└── README.md       ← this file
```

### Step 3 — Push to GitHub

```bash
git add .
git commit -m "Initial commit — OptiSupport AI assistant"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/optisupport.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select: `Deploy from a branch`
4. Branch: `main` · Folder: `/ (root)`
5. Click **Save**

Your site will be live at:
```
https://YOUR_USERNAME.github.io/optisupport/
```
> ⏱ GitHub Pages typically takes 1–3 minutes to publish.

---

## 🔑 API Key Setup

OptiSupport uses the **Anthropic Claude API** to power the AI assistant.

1. Sign up at [console.anthropic.com](https://console.anthropic.com)
2. Go to **API Keys** → **Create Key**
3. Copy your key (starts with `sk-ant-api03-...`)
4. When you open the website, paste the key in the startup dialog

> **Security note:** The API key is stored in browser memory only (not localStorage). It is sent directly to `api.anthropic.com` and never passed through any intermediate server. Each browser session will prompt for the key again.

---

## 🏗 Project Structure

```
optisupport/
├── index.html          Single-file application (HTML + CSS + JS)
└── README.md           Documentation
```

Everything is contained in `index.html` — no build tools, no npm, no dependencies to install.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 AI Chat | Multi-turn conversation with Claude Sonnet 4 |
| 📋 Topic Sidebar | Quick-access buttons for product lines and topics |
| ⚡ Quick Replies | Context-aware follow-up suggestion buttons |
| 📊 Reference Panel | Live spec cards (wavelengths, DOM thresholds, reach guide) |
| 🔍 Expert System Prompt | Pre-tuned for optical transceiver domain knowledge |
| 🌙 Dark Theme | CMIS-5.2 inspired dark navy design system |
| 📱 Responsive | Works on desktop, tablet, and mobile browsers |

---

## 🔧 Customization

### Change the company name / branding

In `index.html`, find and replace:
```html
<span class="logo-text">OptiSupport</span>
```
Update to your company name.

### Tune the AI expertise

Find the `SYSTEM_PROMPT` constant in the `<script>` section and edit the knowledge domains, tone, or response guidelines to match your product line.

### Add product-specific knowledge

Extend the system prompt with your exact product specs:
```javascript
const SYSTEM_PROMPT = `...existing prompt...

Our product line includes:
- Model XYZ-400G-LR4: TX power -3 to +3 dBm, reach 10km, case temp 0–70°C
- Model XYZ-100G-SR4: TX power -8.4 to +2.4 dBm, reach 100m OM4
`;
```

### Sidebar topics

Add new topic buttons by copying the pattern in `index.html`:
```html
<button class="topic-btn" onclick="sendTopic('Your topic description here')">
  <div class="topic-icon" style="background:rgba(79,142,247,0.15)">🔹</div> Button Label
</button>
```

---

## 🌐 Custom Domain (Optional)

To use your own domain (e.g. `support.yourcompany.com`):

1. In your repo, create a file named `CNAME` with your domain:
   ```
   support.yourcompany.com
   ```
2. In your DNS provider, add a `CNAME` record:
   - Host: `support`
   - Points to: `YOUR_USERNAME.github.io`
3. In GitHub Pages settings, enter your custom domain and enable **Enforce HTTPS**

---

## 📋 Technical Stack

| Component | Technology |
|---|---|
| Frontend | Vanilla HTML5 + CSS3 + JavaScript (ES2020) |
| AI Backend | Anthropic Claude Sonnet 4 (`claude-sonnet-4-20250514`) |
| API | Anthropic Messages API v1 |
| Fonts | IBM Plex Sans + IBM Plex Mono (Google Fonts) |
| Hosting | GitHub Pages (static, free) |
| Build tools | None — zero dependencies |

---

## 🔒 Security & Privacy

- API key is **never stored** in localStorage or cookies
- API key is **never sent** to any server except `api.anthropic.com`
- Conversation history stays in browser memory only — cleared on page refresh
- No analytics, no tracking, no third-party scripts (except Google Fonts)

---

## 📄 License

MIT License — free to use, modify, and deploy for commercial purposes.

---

## 🤝 Contributing

Pull requests welcome. For major changes, please open an issue first.

---

*Built for optical transceiver support teams · Powered by Claude AI*
