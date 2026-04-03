# Promptlens
AI-powered prompt analyzer, paste any prompt, get a quality score, weakness breakdown, and smarter rewrite. Assisted with Claude API.
# PromptLens — AI Prompt Analyzer

> Paste any AI prompt. Get an instant quality score, weakness breakdown, and a smarter rewrite — powered by Claude.

**[Live Demo →](https://gregoire1029-lgtm.github.io/Promptlens)** &nbsp;|&nbsp; Built by Gregoire

---

## What it does

Most people write bad AI prompts without knowing it. PromptLens fixes that.

You paste a prompt. The app sends it to Claude, which analyzes it across four dimensions (Clarity, Specificity, Context, Structure) and returns:

- An overall score out of 100
- A list of strengths and weaknesses
- Three actionable tips to improve it
- A rewritten version of your prompt, ready to copy

It's a single HTML file. No install, no framework, no backend. Just open it in a browser.

---

## Why I built this

I was learning how to write better prompts for Claude and kept making the same mistakes — being too vague, not giving context, writing prompts that could mean anything.

I wanted a tool that could give me instant, structured feedback. I built one.

It also shows something I think matters: using AI as the *engine* inside a product, not just as a chat interface.

---

## How it works

```
User input (prompt)
      ↓
Sent to Claude API (claude-sonnet-4)
      ↓
Claude returns structured JSON analysis
      ↓
UI parses JSON and renders score, cards, and improved prompt
```

The entire logic lives in one `index.html` file:

- **HTML** — structure and layout
- **CSS** — custom design system with CSS variables, animations, grid
- **JavaScript** — API call, JSON parsing, dynamic DOM rendering

No React. No npm. No build step.

---

## Technical decisions

**Why a single file?**
Simplicity. A recruiter or user can download one file, open it, and it works. No server needed.

**Why Claude?**
The output needs to be structured JSON with specific fields. Claude handles this reliably with a strong system prompt and `json-only` instruction.

**Why no backend?**
The API key is stored in `localStorage` — the user brings their own key. This means zero hosting cost and zero data stored server-side.

**Why this project?**
It's directly relevant to AI tooling work. It shows I can use the Claude API, design a clean UI, and build something useful from scratch.

---

## Run it locally

No installation needed.

1. Clone this repo:
   ```bash
   git clone https://github.com/gregoire/promptlens.git
   cd promptlens
   ```

2. Open `index.html` in your browser:
   ```bash
   open index.html       # macOS
   start index.html      # Windows
   xdg-open index.html   # Linux
   ```

3. Get a free API key at [console.anthropic.com](https://console.anthropic.com)

4. Paste your key into the field at the top, click **Save**, and start analyzing.

That's it. No npm install, no server, no config files.

---

## Deploy it (free, in 2 minutes)

### Option A — GitHub Pages (recommended)
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. GitHub gives you a live URL: `https://yourusername.github.io/promptlens`

### Option B — Netlify
1. Drag the `index.html` file to [netlify.com/drop](https://netlify.com/drop)
2. Get a live URL instantly

---

## Project structure

```
promptlens/
└── index.html       # The entire app — HTML, CSS, and JS in one file
└── README.md        # This file
```

---

## Screenshots

*(Add a screenshot here after you run it — just take one with Cmd+Shift+4 on Mac)*

---

## What I'd build next

- History log of past analyzed prompts (localStorage)
- Side-by-side comparison: original vs improved
- Export analysis as PDF
- Score trends over time as a chart
- Support for GPT-4 and Gemini API keys too

---

## Stack

| Layer | Tech |
|---|---|
| Frontend | HTML, CSS, Vanilla JS |
| AI | Claude API (`claude-sonnet-4`) |
| Hosting | GitHub Pages |
| Dependencies | None |

---

## Author

**Gregoire** — built this as part of learning AI-native development.

Questions? Open an issue or reach out.
