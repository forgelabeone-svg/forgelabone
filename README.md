# 🧠 ForgeLab — The Self-Healing AI Development Environment

> **Write what you want. It builds, tests, and fixes itself automatically.**

ForgeLab is a browser-based, multi-agent AI development environment powered by **OpenRouter**. Describe your idea in plain English — 5 specialized AI agents work in parallel to plan, build, test, fix, and deploy a fully working project. No setup, no installs.

---

## ✨ Why ForgeLab?

| Feature | ForgeLab | Other AI Coding Tools |
|---------|----------|----------------------|
| **Self-healing** | ✅ Automatic build-test-fix cycle | ❌ Manual fixes only |
| **Multi-agent** | ✅ 5 agents working in parallel | ❌ Single AI response |
| **Audit Loop** | ✅ Build → Validator → ESLint → Fix → Repeat | ❌ Generate & pray |
| **Brain Memory** | ✅ Learns from every project | ❌ No learning |
| **Undo System** | ✅ Full VFS history, rollback anytime | ❌ No undo |
| **BYOK** | ✅ Bring your own OpenRouter API key | Varies |

---

## 🎥 Demo

[Watch on YouTube](https://youtu.be/Ce-2hYqLku4)

---

## 🏗️ Architecture

ForgeLab uses a proprietary **Brain Mode** system with 5 specialized AI agents:

```
User Prompt
│
▼
┌─────────────────┐
│   🧠 Conductor   │ ← Orchestrates the entire workflow
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│   📐 Architect   │ ← Plans project structure & file breakdown
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  💻 Senior Dev   │ ← Writes code (4–5 agents in parallel)
└────────┬────────┘
         │
         ▼
┌─────────────────────────────┐
│  🛡️ AUDIT LOOP              │
│  ┌───────────────────────┐  │
│  │ 🔨 Build Check        │  │
│  │ 🔍 Cross Validator    │  │ ← Automatic detection
│  │ 🧹 ESLint             │  │
│  │ 📐 TypeScript Check   │  │
│  │ 🔬 Runtime Verify     │  │
│  └───────────┬───────────┘  │
│              ▼              │
│  ┌───────────────────────┐  │
│  │ 🐛 Bug Hunter Deep    │  │ ← Automatic fixing
│  │ 🐛 Bug Hunter Fast    │  │
│  └───────────┬───────────┘  │
│              ▼              │
│        All clean? ──▶ YES ──▶ Done! │
│              │              │
│              NO ──▶ Repeat  │
└─────────────────────────────┘
         │
         ▼
┌─────────────────┐
│   🌐 Deploy      │ ← One-click Cloudflare Pages
└─────────────────┘
```

---

## 📊 By the Numbers

Real usage data, live on [forgelab.one](https://forgelab.one):

- **129M+** Tokens via OpenRouter
- **15K+** AI requests processed
- **19+** AI models available
- **101** Registered users
- **67** Brain projects built
- **13** Project templates

---

## 💰 Pricing

| Plan | Price | What you get |
|------|-------|---------------|
| **Free** | $0 | 400,000 tokens/month, automatically. Full access to every AI model in Single Chat, plus deployment and Brain Knowledge. Brain Mode & Fix My Project require Pro or BYOK. |
| **Pro** | Pay-as-you-go | Purchase ForgeLab tokens, no monthly fee. Full access to everything, including Brain Mode and Fix My Project. |
| **BYOK** | $7.99/mo (7-day free trial) | Bring your own OpenRouter API key. Full access to everything, at OpenRouter's own usage pricing. |

No credit card required for the Free plan. Upgrading only happens when you choose to purchase tokens or subscribe to BYOK.

---

## 🚀 Quick Start

1. Visit **[forgelab.one](https://forgelab.one)**
2. Choose a template or describe your project
3. Enable **Brain Mode** for multi-agent generation (Pro/BYOK), or just chat directly with any model on Free
4. Your project is built, tested, and previewed live
5. Deploy with one click

---

## 🔧 Tech Stack

- **Frontend:** Vanilla JS, WebContainer API, Monaco Editor, xterm.js
- **AI:** OpenRouter (Claude, GPT, Gemini, Grok, DeepSeek, and 19+ models)
- **Backend:** PHP (auth/DB), Node.js (streaming)
- **Build:** WebContainer (in-browser Node.js), Judge0 (Python/Java/etc.)
- **Deploy:** Cloudflare Pages

---

## 📦 Project Templates

| Stack | Template |
|-------|----------|
| ⚛️ React + Vite + Tailwind | Modern React App |
| ▲ Next.js 14 App Router | Next.js SaaS Core |
| 💚 Vue 3 + Composition API | Vue 3 App |
| 🧡 SvelteKit | Svelte App |
| ✨ HTML/CSS/JS | Landing Page |
| 🚀 Node.js + Express | REST API |
| ⚡ Python FastAPI | Python API |
| 🏗️ React + Express | Full-Stack App |
| 🤖 React + Streaming | AI Chatbot UI |
| 🐍 Python + Pandas | Data Analyzer |
| 📱 React Native + Expo | Mobile App |
| 🧩 Manifest V3 | Chrome Extension |

---

## 📄 License

This repository contains documentation and public assets. The ForgeLab engine is proprietary software — see [LICENSE](LICENSE).

---

## 🔗 Links

- **Website:** [forgelab.one](https://forgelab.one)
- **YouTube:** [Demo Video](https://youtu.be/Ce-2hYqLku4)
