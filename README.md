# Pursuit Kit

Most AI GTM tools are built for people who control their full stack — founders, solo operators, SDRs with a CRM connected to enrichment tools and outbound sequencing.

I built Pursuit Kit from a different seat. I'm an enterprise practitioner with some AI access, compliance constraints, and sales cycles that involve in-person rooms, not email threads. It's built on the assumption that you already have two things in abundance: rep knowledge and human judgment. Everything else, it helps you build. *(More on this: [You're Not Behind. You're in the Middle](https://apurvap.substack.com/p/youre-not-behind-youre-in-the-middle?r=4iyvm))*

I'm a GTM Strategist with years of experience supporting enterprise sales teams across APAC. The three things that help reps win complex deals are: understand the client's pain, know how your product solves it, and bring enough creativity and personality to tell a great story in the room. Pursuit Kit helps with the first two.

---

## What It Does

Five commands that cover the enterprise pursuit from first context to post-meeting capture:

**`kickoff`** — Entry point for every new pursuit. Gathers client context, runs a light research pass, populates `deal_context.md`, and routes you to the right next step based on how much time you have before the meeting.

**`qualify`** — MEDDPICC-based pursuit orchestration. Researches each element using your company context as the lens, distinguishes confirmed from assumed from unknown, and produces an action summary with the questions you need to ask in your next client conversation.

**`plays`** — Value story builder. Draws from your story bank or generates plays based on confirmed pain and buyer context. Each play includes when to deploy it, who it works best with, what to show, what to say, what to ask, and how to adapt it for this specific client and market.

**`prep`** — Pre-meeting brief. Run within 48 hours of the meeting. Surfaces fresh research on the client and attendees, sharpens your talking points, prepares you for likely objections, and defines the specific ask for this meeting.

**`recap`** — Post-meeting capture. Takes notes in any format — typed notes, AI companion summaries (Zoom, Granola), call logs (Gong), email recaps, or Salesforce notes. If you have nothing written, it interviews you. Updates `deal_context.md` and recommends the next step based on what emerged.

Every command reads your GTM context (what you sell, your USPs, your proof points) before doing anything. The research lens comes from your product — not a generic template.

---

## Quick Start

### Paid tier — Claude Code or Codex CLI (recommended)

Requires a paid Claude or ChatGPT plan.

```bash
git clone https://github.com/apurva-prasanna/pursuit-kit.git
cd pursuit-kit
```

**For Claude Code:**
```bash
claude
```

**For Codex CLI:**
```bash
codex
```

Then say `kickoff`. On first run, kickoff detects that your context files are empty, copies the templates from `context/` automatically, and walks you through setup — starting with your company website URL. No manual file renaming required.

Once setup is complete, kickoff asks whether you're starting an immediate pursuit or have time to prepare properly, then routes you accordingly.

Your context files and deal data stay local. The `.gitignore` ensures nothing from `context/` or `deal_context.md` gets pushed to GitHub.

### Free tier — Claude Projects, ChatGPT Projects, or Copilot Notebooks

No Claude Code or Codex required. Works with any paid or free plan.

Instructions for each platform are in the `free-tier/` folder:

- `claude-project-instructions.txt` — for Claude.ai Projects (free users get up to 5 Projects)
- `chatgpt-project-instructions.txt` — for ChatGPT Projects
- `copilot-notebook-instructions.txt` — for Microsoft Copilot Notebooks (enterprise)

Create one Project or Notebook per client pursuit. The conversation history maintains deal context between sessions.

---

## Commands

| Command | When to run | What you get |
|---------|------------|--------------|
| `kickoff` | Start of every new pursuit | Client context gathered, deal_context.md populated, routing to next step |
| `qualify` | After kickoff, when you have time to prepare properly | MEDDPICC assessment + action summary + questions to ask |
| `plays` | After qualify, or when a meeting is imminent | Value stories and deployment guidance for this specific room |
| `prep` | Within 48 hours of the meeting | Pre-meeting brief with fresh research, talking points, and the ask |
| `recap` | After every meeting | Deal context updated, next step recommended |

### Pursuit flows

**Immediate opportunity (meeting within 5 days):**
```
kickoff → plays → prep → [meeting] → recap
```

**Full pursuit (more than 5 days):**
```
kickoff → qualify → plays → prep → [meeting] → recap → [repeat]
```

After each recap, the tool reads what emerged and recommends whether to run `qualify` again or go straight to `plays` for the next interaction.

---

## Repo Structure

```
pursuit-kit/
├── CLAUDE.md                   # The brain — read automatically by Claude Code every session
├── AGENTS.md                   # Codex CLI equivalent of CLAUDE.md
├── deal_context.md             # Live state file for the current pursuit — gitignored
├── README.md                   # This file
├── .gitignore                  # Keeps your context and deal data off GitHub
│
├── context/                    # Your GTM knowledge base — populated once, read every session
│   ├── company-template.md     # Auto-copied to company.md by kickoff on first run
│   ├── usps-template.md        # Auto-copied to usps.md by kickoff on first run
│   ├── market-template.md      # Auto-copied to market.md by kickoff on first run
│   └── value-story-bank-template.md  # Auto-copied on first run — grows through use
│
├── commands/                   # One file per command — loaded on demand
│   ├── kickoff.md
│   ├── qualify.md
│   ├── plays.md
│   ├── prep.md
│   └── recap.md
│
└── free-tier/                  # Paste-in instructions for non-Claude Code users
    ├── claude-project-instructions.txt
    ├── chatgpt-project-instructions.txt
    └── copilot-notebook-instructions.txt
```

---

## A Note on Data

Pursuit Kit runs locally. Your company context and client data live in files on your machine — they don't get sent anywhere outside your Claude Code or Codex session, and they don't get pushed to GitHub.

The tool only uses publicly available information for prospect research. It flags every finding with a source and asks you to confirm before treating anything as fact. If you're working in a compliance-sensitive environment, the rule is simple: only put in what you'd be comfortable using in any approved AI tool.

---

## What's Coming

- Deck generation from plays output (V2)
- Localise command — adapt a master narrative for a specific market (V2)
- Practice mode — simulate the client before the meeting (V2)

This is a V1 build, documented as part of [Narratives and Nodes](https://apurvap.substack.com) — a build-in-public series on AI applications in enterprise B2B GTM.

---

## Feedback

I'm building this in public, which means I want to know what actually happens when you use it. What landed, what felt off, what the tool got wrong about how enterprise selling actually works.

Find me on [Substack](https://apurvap.substack.com) or open an issue here.

---

## Credits

Built by [Apurva Prasanna](https://apurvap.substack.com) — GTM Strategist based in Sydney, Australia.

Part of the [Narratives and Nodes](https://apurvap.substack.com) project — a build-in-public series on AI applications in enterprise B2B GTM.

**Inspired by:**
- [Interview Coach](https://github.com/noamseg/interview-coach-skill) by Noam Segal — the repo structure, session state pattern, and command file architecture that pursuit-kit is built on.
- [gtm-starter-kit](https://github.com/KarlRaf/gtm-starter-kit) — the context folder and auto-populate from URL pattern.
