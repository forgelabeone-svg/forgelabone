# 🚀 Getting Started with ForgeLab

## What is ForgeLab?

ForgeLab is an AI-powered development environment that runs in your browser. Describe what you want to build, and a team of AI agents will create it for you — complete with automatic error fixing.

## Two Ways to Build

### 💬 Single Chat Mode
Talk directly to one AI agent. Best for:
- Quick questions
- Small code changes
- Learning and explanations
- Simple single-file projects

### 🧠 Brain Mode (Recommended)
A full team of 5 AI agents works together:
1. **Conductor** manages the workflow
2. **Architect** plans the project structure
3. **Senior Developers** write the code in parallel
4. **Bug Hunters** find and fix every error automatically

Best for any real project with multiple files.

## Quick Start

1. Go to **[forgelab.one](https://forgelab.one)**
2. Choose a template or type your project idea
3. Toggle **Brain Mode** ON
4. Click **Send**

That's it! Watch as your project is built, tested, and fixed automatically.

## Templates

Templates give the AI a head start with the right tech stack. Pick one that matches what you want:

| Template | Best For |
|----------|----------|
| Modern React App | Dashboards, SPAs, web apps |
| Next.js SaaS Core | Full-stack apps with auth |
| Vue 3 App | Vue projects |
| Landing Page | Marketing sites, portfolios |
| Node.js Express API | Backend APIs |
| Python FastAPI | Python backends |
| Full-Stack App | React + Express projects |

## Tips for Best Results

- **Be specific** — "A dark-themed admin dashboard with user management, revenue charts, and a settings page" works better than "admin panel"
- **Use templates** — They save time and reduce errors
- **Let the Audit Loop work** — If the preview shows an error, wait. The system fixes itself automatically.
- **Choose a strong model** — In Brain Mode, the Senior Dev agent benefits most from a capable model (Claude Sonnet or equivalent). Cheaper models may produce incomplete code.
- **Bring your own key** — BYOK mode ($7.99/mo, 7-day free trial) lets you use your own OpenRouter API key at cost price. Or go Pro and purchase ForgeLab tokens with no monthly commitment.

## 🗄️ Connecting a Real Backend

By default, generated projects use mock data, no setup needed. If your app needs real auth, a real database, or both:

1. Connect your own Supabase project in the workspace
2. ForgeLab detects the data model your app needs and provisions the tables with one click, with row-level security enabled automatically
3. React, Vue, Svelte, and Next.js projects switch from mock data to real Supabase Auth and real database calls

For Next.js specifically, you'll be asked to choose between a **static export** (client-side auth, stays deployable with the one-click Publish button) or a **full backend** (server-side sessions via middleware, works in Preview, but you deploy it yourself to a Node-capable host since Publish only serves static output).

## 🛡️ Audit Loop — Standalone Feature

The Audit Loop is not just part of Brain Mode — it's an independent feature you can run on any project, including existing ones.

**To run the Audit Loop on an existing project:**

1. Upload your project files into the VFS (Virtual File System)
2. Enable the **Audit Loop** toggle
3. A progress card appears and walks you through each step automatically:
   - Build check
   - Cross validation
   - ESLint
   - TypeScript check
   - Runtime verification
4. Any issues found are fixed automatically, then re-checked

This is useful for auditing and fixing projects that weren't built in ForgeLab, or for re-running a fix pass on an older project.

---

## Need Help?

- Watch the [demo video](https://youtu.be/Ce-2hYqLku4)
- Visit [forgelab.one](https://forgelab.one) to try it live
- Browse the [FAQ](faq.md) for common questions
