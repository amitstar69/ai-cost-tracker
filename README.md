# 📉 AI Cost Tracker

**The unified dashboard for your LLM spending. Zero backend. Zero tracking. 100% Local.**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Privacy](https://img.shields.io/badge/privacy-100%25%20local-green.svg)
![Stack](https://img.shields.io/badge/stack-HTML%2FJS-orange.svg)

## 🚀 Why use this?
Developers often have API keys for OpenAI, Anthropic, and OpenRouter, plus local Ollama models running. Tracking how much you spend across all of them in real-time is a pain. 

**AI Cost Tracker** solves this with a single, private dashboard running entirely in your browser.

## ✨ Key Features
* **Unified Dashboard:** Track OpenAI, Anthropic, Gemini, OpenRouter, and Ollama in one view.
* **Real-Time Streaming:** Watch responses token-by-token with instant cost calculation.
* **Cost Segregation:** Filter dashboard stats by specific provider to see exactly who is spending what.
* **Privacy First:** Your API keys and usage history are stored in your browser's `Local Storage`. Nothing is ever sent to a backend server.
* **Data Portability:** Export your full usage history to JSON at any time.

## 🛠️ Quick Start
1.  **[Click here to use the live app](https://YOUR-USERNAME.github.io/YOUR-REPO)**.
2.  Click **+ Connect API**.
3.  Choose a provider (e.g., **OpenRouter** or **Ollama**).
4.  Start prompting.

## 🔒 Security & Privacy
* **Client-Side Only:** This is a static HTML file. Inspect the code—there is no database and no tracking analytics.
* **Direct Connections:** The app connects directly from your browser to the API provider (e.g., `api.openai.com`).
* **CORS Note:** For the best experience with Anthropic/Claude, use an **OpenRouter** key, as Anthropic directly blocks browser-based requests.

---
*Built for developers who want control over their AI budget.*
