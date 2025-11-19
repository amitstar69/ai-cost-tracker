# 📉 AI Cost Tracker (Privacy-First & Local-Only)

**The unified dashboard for your LLM spending. Zero backend. Zero tracking. 100% Open Source.**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Privacy](https://img.shields.io/badge/privacy-100%25%20local-green.svg)
![Stack](https://img.shields.io/badge/stack-HTML%2FJS-orange.svg)

## 😫 The Problem
To check your AI spending today, you have to:
1. Log into OpenAI.
2. Log into Anthropic.
3. Log into OpenRouter/Google/DeepSeek.
4. Add it all up manually.

## 🚀 The Solution
**AI Cost Tracker** is a single-file HTML application that runs entirely in your browser. It connects directly to API endpoints to track usage and estimate costs in real-time as you test prompts.

### ✨ Key Features
*   **Unified Dashboard:** Track OpenAI, Gemini, and Custom (Ollama/LocalAI) costs in one view.
*   **Privacy First:** API keys are stored in your browser's `localStorage`. Nothing is ever sent to our servers (because we don't have one).
*   **Playground:** Test prompts with Markdown rendering support.
*   **Real-Time Estimates:** See how much a prompt will cost *before* you send it.
*   **Ollama Ready:** Treat your local models like paid APIs to calculate "theoretical" savings.

## 🛠️ Quick Start
There are two ways to use this:

### Option A: The 30-Second Setup (Recommended)
1.  [Click here to view the live app](https://YOUR-USERNAME.github.io/REPO-NAME).
2.  Click **+ Add Provider**.
3.  Enter your API Key (e.g., OpenAI) or Local URL (Ollama).
4.  Start typing in the Playground.

### Option B: Run Locally (For maximum paranoia)
1.  Download the `index.html` file from this repository.
2.  Disconnect your internet (optional, to verify safety).
3.  Double-click `index.html` to open it in your browser.

## 🔒 Security & Privacy
We take security seriously. Here is how this app works:
*   **Client-Side Only:** This app is a static HTML file. There is no database and no backend server.
*   **Network Activity:** Open your browser's "Network" tab. You will see requests *only* to the APIs you configure (e.g., `api.openai.com`) and `cdn.tailwindcss.com` for styling.
*   **Key Storage:** Keys are saved in `localStorage`. Clearing your browser cache wipes them instantly.

## ⚠️ Important Note on CORS
Some providers (like **Anthropic**) block browser-based API calls for security.
*   **OpenAI / Gemini / OpenRouter:** Work out of the box.
*   **Ollama / LM Studio:** Work out of the box (ensure CORS is enabled locally).
*   **Anthropic:** Requires a local proxy. We recommend using OpenRouter or a proxy server if you need Claude in the browser.

## 🤝 Contributing
Missing a feature? Found a bug?
1.  Fork this repo.
2.  Edit `index.html` directly.
3.  Submit a PR.

---
*Built for developers who hate fragmented billing.*
