# CIC Onboarding Platform
**Accenture Connected Innovation Centre — Americas**

A personalized, interactive onboarding web app for new CIC analysts. Built as a static single-page application — no backend required.

---

## Deploying to GitHub Pages

### Step 1 — Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `cic-onboarding` (or anything you like)
4. Set visibility to **Private** (recommended for internal tools)
5. Click **Create repository**

### Step 2 — Upload the file
**Option A — Drag and drop (easiest):**
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag `index.html` into the upload area
4. Click **Commit changes**

**Option B — Git CLI:**
```bash
git init
git add index.html
git commit -m "Initial CIC onboarding prototype"
git remote add origin https://github.com/YOUR_USERNAME/cic-onboarding.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repository → **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: `main`, folder: `/ (root)`
4. Click **Save**
5. Wait ~60 seconds, then visit: `https://YOUR_USERNAME.github.io/cic-onboarding`

---

## Activating the AI Chatbot

The CIC Buddy chatbot works in two modes:

**Fallback mode (default, no setup needed)**
Answers common onboarding questions using built-in keyword matching. Works immediately with no API key.

**AI mode (full Claude-powered answers)**
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up for a free account
3. Navigate to **API Keys → Create Key**
4. Copy the key (starts with `sk-ant-...`)
5. Open the prototype → click the purple chat button (bottom right)
6. Paste your key into the **API key** field → click **Save**

The chatbot will switch to AI mode immediately, with the full CIC knowledge base embedded.

> **Note:** The API key is stored in browser memory only and is never saved or transmitted anywhere other than the Anthropic API. Each session requires re-entering the key.

---

## Customising the knowledge base

To update the chatbot's knowledge (e.g. when org structure changes):

1. Open `index.html` in any text editor
2. Find the line: `const SYSTEM =`
3. The long string after it is the knowledge base — edit the section between `ACCENTURE CIC ONBOARDING KNOWLEDGE BASE` and the end of the string
4. Save and re-upload to GitHub

---

## Features
- 4-step personalised onboarding flow
- 6 stages with 24 tasks drawn from the Quick Start Guide and board game
- Grid view and interactive Map view (task islands)
- Per-task illustrations and video placeholders
- Peer notes / comments section per stage
- Real-time progress tracking
- AI-powered chatbot (Claude) with full CIC knowledge base
- Fallback keyword responses when no API key is set
- Accenture brand colours and logo embedded

