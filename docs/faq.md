# ❓ Frequently Asked Questions

## General

**Q: What makes ForgeLab different from Bolt.new or v0?**  
A: ForgeLab has a unique **self-healing Audit Loop** that automatically finds and fixes errors. Other tools generate code and leave you to debug it manually. We also use a multi-agent system (5 specialized AI agents) instead of a single AI response.

**Q: Is it free?**  
A: There are three tiers:
- **Free** — ForgeLab's API with free models only. Brain Mode, Audit Loop, and other advanced features are not available.
- **Pro** — no monthly fee, purchase ForgeLab tokens and use them as you go. Full access to all features and models, with higher queue priority.
- **BYOK** — $6.99/month platform fee (7-day free trial), bring your own OpenRouter API key. Full access to all features.

**Q: What tech stacks are supported?**  
A: React, Next.js, Vue, Svelte, Node.js/Express, Python/FastAPI, static HTML/CSS/JS, and more.

## Brain Mode

**Q: How does Brain Mode work?**  
A: 5 AI agents work together — a Conductor manages the workflow, an Architect plans the structure, multiple Senior Developers write code in parallel, and Bug Hunters find and fix errors automatically.

**Q: How long does it take?**  
A: Small projects (3-5 files): ~2 minutes. Medium projects (8-12 files): ~4 minutes. Larger projects: up to 8 minutes.

**Q: Can I stop it mid-way?**  
A: Yes, click the Stop button anytime. You'll keep all files generated so far.

## Audit Loop

**Q: What is the Audit Loop?**  
A: After generating code, ForgeLab automatically runs build checks, code validators, and linters. If it finds errors, it fixes them and re-checks — up to 5 times — until the project is clean.

**Q: Does it always fix everything?**  
A: Currently ~85-90% of issues are fixed automatically. For the remaining edge cases, you can manually prompt the AI to fix specific problems.

## Privacy & Security

**Q: Is my code stored?**  
A: Yes — your projects are saved to a database and accessible from your account. Deployed projects are hosted on Cloudflare Pages.

**Q: Can I use my own API key?**  
A: Yes! Add your OpenRouter API key in Settings. You'll only pay OpenRouter's usage pricing.

## Technical

**Q: How does it run in the browser?**  
A: We use WebContainer API, which runs a real Node.js environment directly in your browser. No server required for builds.

**Q: What about Python projects?**  
A: Python and other non-JavaScript languages run via Judge0, a cloud-based code execution service.
