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

### Provider Setup & Testing

#### OpenAI (GPT-4o / GPT-4o-mini)
- Click **Add API Provider** and select **OpenAI**.
- Enter your model name, e.g., `gpt-4o` or `gpt-4o-mini`.
- Set the input and output cost per million tokens using current OpenAI pricing.
- Paste your OpenAI API key (starts with `sk-`). Keys not starting with `sk-` will trigger an invalid-key alert.
- Optionally add a nickname to identify the key.
- Save the provider, then open the **Playground**, select your OpenAI provider, and send a test prompt. The dashboard will update with token and cost data.

#### Anthropic (Claude models)
- Click **Add API Provider** and select **Anthropic**.
- Enter your model name, such as `claude-3-sonnet-20240229` or `claude-3-haiku-20240307`.
- Set the input and output costs per million tokens according to Anthropic’s pricing.
- Paste your Anthropic API key (prefix `sk-ant-` or `sk-`). The app validates the prefix and will warn if the key format is incorrect.
- Provide a nickname if desired and save the provider.
- Use the **Playground** to send a message with your Anthropic provider. The dashboard should reflect usage and cost.

#### Gemini / Custom Providers
- Choose **Custom** in the **Add API Provider** modal for Gemini or other custom models.
- Fill in provider name (e.g., `Gemini`), endpoint URL, model name, and pricing (input/output cost per million tokens).
- Paste your API key (no prefix validation for custom providers).
- Save and test via the **Playground**. Token estimates and costs will be computed using the heuristic estimator built into the app.

### Notes
- Version 2.1 introduces token estimation, usage event logging, and cost aggregation for today, this week, this month, and all time.
- All data (API keys and usage history) stays in your browser’s local storage and is never sent to any server.
- You can clear all stored data via the **Settings** modal.
