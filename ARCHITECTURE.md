# 🧠 ForgeLab Architecture

## Overview

ForgeLab is a **multi-agent AI development environment** that runs entirely in the browser. It combines 5 specialized AI agents with a proprietary self-healing audit loop to automatically generate, test, and fix full-stack projects.

---

## Core Components

### 1. Brain Mode — Multi-Agent Orchestrator

The Brain is the central orchestrator that manages the entire project generation lifecycle.

**5 Specialized Agents:**

| Agent | Role | Model Recommendation |
|-------|------|---------------------|
| 🚦 **Conductor** | Orchestrates workflow, decides next actions | Fast/cheap model |
| 📐 **Architect** | Plans project structure, file breakdown, task assignment | Fast/cheap model |
| 💻 **Senior Dev** | Writes production code (4–5 in parallel) | Best available model |
| 🐛 **Bug Hunter Fast** | Quick pre-scan for obvious errors | Fast/cheap model |
| 🐛 **Bug Hunter Deep** | Complex debugging and integration fixes | Strong reasoning model |

**Execution Phases:**

```
PHASE 1: DISCOVERY
├── Knowledge base search
├── Intent extraction (style, must-have features, constraints)
├── Goal extraction (measurable deliverables)
└── Stack detection

PHASE 2: PLANNING
├── Architect creates file list
├── Task breakdown (1 file = 1 task)
├── Dependency chain resolution
└── Interface contract definition

PHASE 3: EXECUTION
├── Phase 0: Config files (package.json, vite.config, etc.)
├── Phase 1: Entry points (index.html, main.jsx, App.jsx)
├── Phase 2: Core infrastructure (layout, routing, context)
├── Phase 3: Components (all UI components in parallel)
└── Phase 4: Content & assets

PHASE 4: VALIDATION & RETRY
├── Missing file recovery
├── Auto-dependency installation
├── Final integrity check
└── Retry failed tasks
```

---

### 2. Audit Loop — Self-Healing System

The Audit Loop is what makes ForgeLab unique. After code generation, it enters an automated fix cycle:

```
┌─────────────────────────────────────┐
│           AUDIT LOOP                │
│  (max 5 iterations)                 │
│                                     │
│  Phase 1: Build Check               │
│  └── npm run build → find errors    │
│                                     │
│  Phase 2: Cross Validator           │
│  └── Prop mismatches, missing       │
│      imports, broken routes,        │
│      enum inconsistencies           │
│                                     │
│  Phase 3: ESLint                    │
│  └── Code quality issues            │
│                                     │
│  Phase 4: TypeScript Check          │
│  └── Type errors (if tsconfig)      │
│                                     │
│  Phase 5: Holistic Review           │
│  └── Full project overview by       │
│      a large-context AI model       │
│                                     │
│  Phase 6: Runtime Verification      │
│  └── Browser console capture,       │
│      terminal error parsing         │
│                                     │
│  All clean? → EXIT ✅               │
│  Issues found? → Fix → REPEAT 🔄    │
└─────────────────────────────────────┘
```

**Stagnation Detection:** If 2 consecutive iterations don't reduce error count, the loop stops to prevent regression.

**Rollback Protection:** Full VFS snapshots are saved before every fix. If a fix makes things worse, it's automatically reverted.

---

### 3. Diff Patcher — 7-Level PATCH Engine

When the AI suggests a fix, ForgeLab doesn't just overwrite the file. It uses a proprietary 7-level matching strategy:

| Level | Strategy | Description |
|-------|----------|-------------|
| 0 | Pre-substitution | Extracts real original lines from the file using unique anchors |
| 1 | Exact match | Direct string match |
| 2 | Trimmed match | Handles trailing whitespace differences |
| 2.5 | Full-trim match | Handles leading indent differences (2-space vs 4-space) |
| 3 | Fuzzy match | 85%+ similarity threshold per line |
| 4 | Context anchor | Multi-anchor sequence matching |
| 5 | First+last line | Matches significant first and last lines |
| 6 | Unique anchor | Single unique line matching |
| 7 | Tab/space normalize | Normalizes indentation and retries |

Only if ALL levels fail does the system fall back to a full file rewrite.

---

### 4. Brain Memory — Global Learning System

Every project contributes to a shared knowledge base:

- **Successful patterns** — what works well (stored with stack, intent type)
- **Common issues** — what breaks often (stored with category, error type)
- **Reinforced warnings** — issues that recur 3+ times get promoted to mandatory rules
- **Stack preferences** — which tech stacks have the highest success rates

This data is anonymized (URLs, emails stripped) and shared across all users to continuously improve generation quality.

---

### 5. VFS History — Undo System

Every AI modification is snapshotted before changes are applied:

- Up to 20 snapshots stored
- Full project state saved (not just changed files)
- One-click undo from error cards or file tree
- Survives audit loop iterations

---

## Technical Stack

### Browser-Side
- **WebContainer API** — In-browser Node.js runtime (npm, Vite, Next.js)
- **Judge0 API** — Server-side Python/Java/C++/etc. execution
- **Monaco Editor** — VS Code-like code editor
- **xterm.js** — Multi-tab terminal emulator

### AI Integration
- **OpenRouter** — Unified API for 50+ AI models
- **Streaming (SSE)** — Real-time code generation display
- **Sync API** — Server-validated non-streaming mode for Brain tasks

### Backend
- **PHP** — Authentication, database, session management
- **Node.js** — SSE streaming endpoint
- **Supabase** — Conversation storage, Brain Memory, user data
- **Cloudflare Pages** — One-click project deployment

---

## Security

- **BYOK (Bring Your Own Key)** — Users can use their own OpenRouter API key
- **Session-based authentication** — PHP sessions with Supabase integration
- **API key encryption** — Keys stored encrypted at rest
- **No code storage** — Generated projects are ephemeral (unless deployed)
