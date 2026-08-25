# ❓ Frequently Asked Questions

## General

**Q: What makes ForgeLab different from Bolt.new or v0?**  
A: ForgeLab has a unique **self-healing Audit Loop** that automatically finds and fixes errors. Other tools generate code and leave you to debug it manually. We also use a multi-agent system (5 specialized AI agents) instead of a single AI response.

**Q: Is it free?**  
A: There are three tiers:
- **Free:** 400,000 tokens every month, automatically, no credit card required. Full access to every AI model in single chat, plus one-click deployment and Brain Knowledge. If you use up your monthly tokens before the next refresh, you can still send up to 10 messages a day using free-category models. Brain Mode and Fix My Project (the Audit Loop) require Pro or BYOK.
- **Pro:** no monthly fee, purchase ForgeLab tokens and use them as you go. Full access to all features, including Brain Mode and Fix My Project, with higher queue priority.
- **BYOK:** $7.99/month platform fee (7-day free trial), bring your own OpenRouter API key. Full access to all features.

**Q: What tech stacks are supported?**  
A: React, Next.js, Vue, Svelte, Node.js/Express, Python/FastAPI, PHP, static HTML/CSS/JS, and more.

**Q: Can I connect a real backend and database?**  
A: Yes. Connect your own Supabase project, and ForgeLab detects the data model your app needs and provisions the tables for you, with row-level security enabled automatically. Once connected, React, Vue, Svelte, and Next.js projects write real database calls and use real Supabase Auth instead of mock data. Nothing changes if you don't connect a database, projects still work fine with mock data.

**Q: For Next.js, what's the difference between static export and full backend mode?**  
A: Static export keeps auth on the client side and stays deployable with ForgeLab's one-click Publish button. Full backend mode adds real server-side session handling via middleware, works completely in Preview, but needs to be deployed yourself to a Node-capable host (e.g. Vercel), since Publish only supports static output.

## Brain Mode

**Q: Which plans include Brain Mode?**  
A: Pro and BYOK. It's the most token-hungry feature on the platform (several agents run in parallel), so it's not included on the Free plan. Fix My Project (the Audit Loop) runs on the same engine as Brain Mode, so it's Pro/BYOK only too. Single chat, on the other hand, has full access to every AI model on every plan, including Free.

**Q: How does Brain Mode work?**  
A: 5 AI agents work together — a Conductor manages the workflow, an Architect plans the structure, multiple Senior Developers write code in parallel, and Bug Hunters find and fix errors automatically.

**Q: How long does it take?**  
A: Small projects (3-5 files): ~2 minutes. Medium projects (8-12 files): ~4 minutes. Larger projects: up to 8 minutes.

**Q: Can I stop it mid-way?**  
A: Yes, click the Stop button anytime. You'll keep all files generated so far.

**Q: Does model choice affect quality?**  
A: Yes, significantly. Cheaper or smaller models may not follow complex formatting rules as reliably, which can result in incomplete or incorrectly structured files. For Brain Mode, a stronger model (like Claude Sonnet or GPT-4 class) is recommended for the Senior Dev agent. You can configure per-agent models in Settings → Brain Mode Config.

## Audit Loop

**Q: What is the Audit Loop?**  
A: After generating code, ForgeLab automatically runs build checks, code validators, and linters. If it finds errors, it fixes them and re-checks — up to 5 times — until the project is clean.

**Q: Does it always fix everything?**  
A: Currently ~85-90% of issues are fixed automatically. For the remaining edge cases, you can manually prompt the AI to fix specific problems.

## Privacy & Security

**Q: Is my code stored?**  
A: Yes — your generated projects are saved to your account and accessible from your conversation history. Only you can see your projects. Conversation history and project files are encrypted at rest (AES-256). Deployed projects are hosted on Cloudflare Pages under a public URL you control.

**Q: Can I use my own API key?**  
A: Yes! Add your OpenRouter API key in Settings. You'll only pay OpenRouter's usage pricing, plus the $7.99/month BYOK platform fee (7-day free trial included).

**Q: How is my API key stored?**  
A: Your API key is encrypted with AES-256-CBC before being stored. It is never logged or transmitted in plain text.

**Q: Can I add extra account security?**  
A: Yes — two-factor authentication (TOTP via an authenticator app, or an emailed code) is available in Settings → Account, off by default, with one-time backup codes in case you lose access.

## Technical

**Q: How does it run in the browser?**  
A: We use WebContainer API, which runs a real Node.js environment directly in your browser. No server required for builds.

**Q: What about Python projects?**  
A: Python and other non-JavaScript languages run via Judge0, a cloud-based code execution service.

**Q: Can I use a local AI model?**  
A: Yes — BYOK users can connect their own Ollama instance in Settings → Local Model. Note that smaller local models may produce lower quality results than cloud models, especially in Brain Mode.
