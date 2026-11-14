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

### 1. Google Antigravity & Gemini CLI
Clone or symlink into your user skills directory:
```bash
git clone https://github.com/theajmalrazaq/resurface.git ~/.gemini/config/skills/resurface
```
Antigravity automatically registers the skill upon start.

### 2. Claude Code
Symlink into your global or project Claude skills directory:
```bash
# Global installation for all Claude Code sessions:
mkdir -p ~/.claude/skills
ln -s /path/to/resurface ~/.claude/skills/resurface

# Or project-level:
mkdir -p .claude/skills
cp /path/to/resurface/SKILL.md .claude/skills/SKILL.md
```

### 3. Cursor & Windsurf
Add as a project rule or cursor rule:
```bash
# Cursor
mkdir -p .cursor/rules
cp /path/to/resurface/SKILL.md .cursor/rules/resurface.md

# Windsurf
cat /path/to/resurface/SKILL.md >> .windsurfrules
```

### 4. OpenAI Codex / Custom Agent Harness
Place `SKILL.md` in your agent's system prompt or workspace context file (`skills/resurface/SKILL.md`).

---

## How to Trigger the Skill

Once installed, invoke your agent with any of these prompts:

> *"Resurface this legacy website: `https://portal.mycompany.com`."*

> *"I have an ugly intranet site at `https://hr.internal`. Crawl it with Obscura, map the routes recursively, handle the login, and build me a modern Chrome extension overlay."*

> *"Redesign this legacy ASP.NET website using the Resurface WXT/React overlay architecture with zero FOUC."*

---

## License

MIT © [Ajmal Razaq](https://github.com/theajmalrazaq)
