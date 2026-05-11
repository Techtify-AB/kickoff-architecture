# Kickoff Architecture

A project template for AI-assisted development. Pre-configured with agent skills,
IDE settings, and conventions so you can go from idea to working code in one session.

## What's included

```
.claude/skills/   — 70+ agent skills (auth, testing, payments, CI, etc.)
.cursor/rules/    — IDE-specific conventions for Cursor
.github/          — PR templates and CI workflows
CLAUDE.md         — Agent instructions (read by Claude Code + Cursor)
AGENTS.md         — Points to CLAUDE.md
```

## Getting started

1. **Create a repo from this template** (or clone it).

2. **Describe what you're building** — paste your vision into the chat
   (Cursor IDE or Claude Code CLI). The agent will ask clarifying questions,
   then create `plan.md` and start building.

3. **That's it.** The agent handles scaffolding, installs deps, writes code,
   commits, and creates PRs. You review and merge.

## How it works

The agent reads `CLAUDE.md` for all project conventions: git protocol,
scaffolding rules, testing approach, communication style, and stack defaults.

Skills in `.claude/skills/` are discovered automatically. The agent picks
relevant ones based on what you're building (e.g. `adding-auth` if you mention
login, `adding-stripe` if you need payments).

## For Codepilot / Shipyard users

If this project was created via the Shipyard dashboard, the agent already has
your vision and design preferences — it received them via the system prompt.
You don't need to do anything; just chat.

## Manual use (Cursor / Claude Code CLI)

Open the project in Cursor or run `claude` in the terminal. Tell the agent
what you want to build. Example:

```
Build a SaaS dashboard for tracking team OKRs. Next.js, dark theme,
Stripe for billing, GitHub OAuth for login.
```

The agent will:
1. Ask 1-3 clarifying questions (if needed)
2. Create `plan.md` with a phased build plan
3. Create `memory.md` with stack decisions
4. Start building Phase 1
