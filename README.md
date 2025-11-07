# AI Cost Tracker (Privacy‑first, Client‑side)

A single‑file app that tracks your OpenAI and Anthropic usage and costs locally in your browser. No servers, no telemetry, no backend.

## Features
- Add and manage API keys (stored in `localStorage`, never sent to us)
- Real‑time cost tracking per provider/model
- 7‑day cost trend chart (Chart.js)
- Playground to send test messages and auto‑log usage
- Export all data as JSON
- Light/Dark theme

## Quick Start
1. Download `index.html`
2. Double‑click to open it in your browser
3. Click **Add API Provider** and paste your key(s)
4. Use the **Playground** to make a request
5. Watch your dashboard update

> Keys and usage data live only in this browser profile.

## Deploy on GitHub Pages
1. Create a repo named `ai-cost-tracker`
2. Upload `index.html` (and this `README.md` if you like)
3. In **Settings → Pages**, set **Deploy from a branch**, source **main** at `/ (root)`
4. Wait a minute, then visit: `https://YOUR-USERNAME.github.io/ai-cost-tracker/`

## Pricing Notes
Pricing tables are defined per‑token in the script and can be updated as needed.
Edit the `OPENAI_PRICING` and `ANTHROPIC_PRICING` objects.

## Security
- No analytics, no third‑party calls other than LLM APIs
- Keys are masked in UI
- Clear all data from **Settings → Clear all data**

## Extend
- Add more providers by adding a pricing map and API call function
- Add budget alerts by scanning totals on each render
- Add CSV export by converting the JSON to CSV

---

Built following the provided implementation spec.
