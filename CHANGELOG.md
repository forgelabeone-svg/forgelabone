# 📝 Changelog

## v8.3 (Current) — June 2026

### New Features
- 🖥️ **Local Model Support** — Connect your own Ollama instance as the AI backend (BYOK users)
- 🔒 **BYOK Subscription System** — Stripe integration, 7-day free trial, active subscription enforcement across all endpoints
- 🧠 **Memory Priority for Local Models** — Memory context is prepended to the system prompt for better adherence by smaller models
- 🌟 **New Models** — Added Claude Opus 4.8, Minimax M3, Qwen 3.7 Max
- 📢 **Announcement Bar** — HTML-rendered system announcements
- ⚙️ **Closed Beta Mode** — Feature flag to disable token purchases during closed beta

### Improvements
- ⚡ Brain agent model tuning: Senior Dev → Claude Sonnet 4.6 for better instruction adherence
- 💰 Bug Hunter → DeepSeek V4 Pro (equivalent quality, lower cost)
- 🌍 Chat history dates now always display in English regardless of browser locale
- 📋 Onboarding wizard: added "Model Quality Matters" slide to set expectations

### Bug Fixes
- Fixed trial duration inconsistency (was showing 30 days in some places, 7 days in others)
- Fixed Brain Mode disable state when local model is active

---

## v8.2 — May 2026

### New Features
- 🚀 **Closed Beta Launch** — Invited user access
- 💳 **Stripe Live Mode** — BYOK subscription payments in production
- 🧩 **Component Contract System** — Architect defines prop interfaces shared across all parallel Senior Dev agents
- 📋 **10-slide Onboarding Wizard** — Full product walkthrough for new users

### Improvements
- Brain Mode disabled (grayed out) when local model is active
- Per-file generation mode as default (more reliable than batch)
- BYOK trial enforcement added to all API endpoints

---

## v8.1 — April 2026

### New Features
- 🧠 Brain Memory in every task execution
- 📊 Live usage counter on landing page
- 🔧 Smart import/export registry (cross-file validation)

### Improvements
- ⚡ Adaptive parallelism (auto-adjusts after 429 errors)
- 🔒 Template lock system (prevents config file overwrites)
- 📦 Auto-dependency installer improvements

### Bug Fixes
- Fixed race condition in parallel task file creation
- Fixed duplicate BrowserRouter injection
- Fixed circular @apply detection in CSS

---

## v8.0 — March 2026

### New Features
- 🔧 Smart live linter (auto-fixes missing imports/exports)
- 🔒 Comprehensive integrity checker
- 📦 Auto-dependency installer
- 📋 Project template system (13 templates)
- ⚡ Real-time file validation

### Bug Fixes
- Fixed premature npm run dev start
- Fixed loading screen timing
- Fixed file corruption protection

---

## v7.1 — February 2026

### New Features
- 📊 Project completion tracking
- ⏱️ Controlled dev server start
- 🔒 File corruption protection
- ⏱️ Timeout synchronization

---

## v7.0 — January 2026

### New Features
- 🧠 Initial Brain Mode (multi-agent)
- 🔄 Conductor-based workflow
- 📋 Task queue with parallel execution
- 🐛 Bug Hunter agents

---

## v1.0 — December 2025

- 🚀 Initial release
- 💬 Single chat mode
- 👤 Multiple AI personas
- 📁 File system + code editor
- 🖥️ Terminal integration
- 🌐 WebContainer preview
