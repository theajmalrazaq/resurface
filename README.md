# Resurface (Agent Skill)

> **Universal AI Agent Skill:** Transform ANY clunky, outdated, or frustrating legacy website, portal, or ERP into a 2026-grade modern application using a client-side Chrome Extension overlay.

Compatible with **Antigravity**, **Claude Code**, **OpenAI Codex**, **Cursor**, **Windsurf**, and **GitHub Copilot Workspace**.

---

## Why Overlay Architecture?

Most legacy systems (university portals, internal corporate tools, government sites, banking interfaces, ERPs) suffer from outdated UI, terrible UX, and lack of mobile support. However:
- Rebuilding their backend is impossible without direct database access and organizational approval.
- Scraping them via remote servers risks session invalidation, IP blocks, and security liabilities.

**The Solution:** Build a client-side Web Extension overlay (the proven **SuperFlex** architecture). The legacy backend continues handling authentication, sessions, database transactions, and business logic, while your modern overlay intercepts the DOM before paint and renders a high-performance React 19 + Tailwind interface directly over the host domain.

---

## Key Capabilities

- 🕶️ **Exclusive Stealth Crawling via Obscura:** Uses [Obscura](https://github.com/h4ckf0r0day/obscura) to bypass anti-bot detections, capture authenticated DOM trees, and catalog routes.
- 🗺️ **Recursive Whole-Site Graph Mapping:** Recursively crawls navbar dropdowns, sidebar accordions, secondary/tertiary tabs, and sub-pages to build a complete `audit/site-graph.json` before writing a single line of UI code.
- 🛑 **Interactive Human-in-the-Loop Auth Gate:** Safely pauses for human CAPTCHA solving (Turnstile, reCAPTCHA, hCaptcha) or 2FA without attempting illegal bypasses.
- ⚡ **Zero-FOUC (Flash of Unstyled Content) Guarantee:** Enforces 7-stage anti-FOUC pre-paint suppression, loading skeletons, legacy stylesheet removal, high-res favicon replacement, and zero-flash dark/light mode.
- 🖼️ **Dynamic High-Res Favicon Injection:** Replaces legacy 16x16 blurred `.ico` files with crisp vector / PNG branding before first paint.
- 🌗 **Zero-Flash Adaptive Theme Engine:** Pre-paint synchronous `dark` class mounting, Tailwind v4 CSS variables, and persistent Zustand state (`light`, `dark`, `system`).
- 🧩 **Resilient Semantic Parsers:** Extracts tables, forms, and alerts using header-anchored semantic lookups validated with Zod schemas.
- 🔄 **Form Action Proxying:** Synchronizes modern inputs to hidden legacy forms so CSRF tokens (`__RequestVerificationToken`, `__VIEWSTATE`) and native cookies pass naturally.
- 🎨 **Modern Design System:** Elevated typography, responsive layout, dark/light theme engine, and accessible components.

---

## Installation Across AI Agents

### One-command install (skills CLI / registries)

```bash
# skills.sh — Vercel skills CLI (Claude Code, Codex, Cursor, and 40+ agents)
npx skills add theajmalrazaq/resurface

# Install globally instead of per-project
npx skills add theajmalrazaq/resurface -g -y

# GitHub CLI (validates against the Agent Skills spec)
gh skill install theajmalrazaq/resurface

# Pin the exact v1.0.0 release
gh skill install theajmalrazaq/resurface resurface --pin v1.0.0

# Preview the skill before installing
gh skill preview theajmalrazaq/resurface resurface

# Claude Code plugin marketplace
/plugin marketplace add theajmalrazaq/resurface
/plugin install resurface@resurface

# ClawHub (OpenClaw registry)
npx clawhub install resurface
# or, inside OpenClaw:
openclaw skills install resurface

# Update later
gh skill update --all
npx skills add theajmalrazaq/resurface
```

**Published on:**
- [skills.sh](https://skills.sh/theajmalrazaq/resurface/resurface) — install with `npx skills add theajmalrazaq/resurface`
- [GitHub Releases](https://github.com/theajmalrazaq/resurface/releases/tag/v1.0.0) — `v1.0.0`, install with `gh skill install theajmalrazaq/resurface`
- [ClawHub](https://clawhub.ai/theajmalrazaq/skills/resurface) — install with `openclaw skills install @theajmalrazaq/resurface`
- Agensi — free listing (in review)
- SkillsMP and ClaudeSkills — auto-indexed from this public repo

### 1. Google Antigravity & Gemini CLI
The skill lives in `skills/resurface/` inside this repo. Clone and copy it into your user skills directory:
```bash
git clone https://github.com/theajmalrazaq/resurface.git
cp -r resurface/skills/resurface ~/.gemini/config/skills/resurface
```
Antigravity automatically registers the skill upon start.

### 2. Claude Code
Symlink into your global or project Claude skills directory:
```bash
# Global installation for all Claude Code sessions:
mkdir -p ~/.claude/skills
ln -s /path/to/resurface/skills/resurface ~/.claude/skills/resurface

# Or project-level:
mkdir -p .claude/skills
cp -r /path/to/resurface/skills/resurface .claude/skills/resurface
```

### 3. Cursor & Windsurf
Add as a project rule or cursor rule:
```bash
# Cursor
mkdir -p .cursor/rules
cp /path/to/resurface/skills/resurface/SKILL.md .cursor/rules/resurface.md

# Windsurf
cat /path/to/resurface/skills/resurface/SKILL.md >> .windsurfrules
```

### 4. OpenAI Codex / Custom Agent Harness
Place `skills/resurface/SKILL.md` from this repo in your agent's system prompt or workspace context file.

---

## How to Trigger the Skill

Once installed, invoke your agent with any of these prompts:

> *"Resurface this legacy website: `https://portal.mycompany.com`."*

> *"I have an ugly intranet site at `https://hr.internal`. Crawl it with Obscura, map the routes recursively, handle the login, and build me a modern Chrome extension overlay."*

> *"Redesign this legacy ASP.NET website using the Resurface WXT/React overlay architecture with zero FOUC."*

---

## License

MIT © [Ajmal Razaq](https://github.com/theajmalrazaq)
