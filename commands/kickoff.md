# kickoff.md — Pursuit Kit
*Activated when the rep says `kickoff` or starts a new pursuit.*

---

## What This Command Does

Kickoff is the entry point for every pursuit. It opens with one
question that determines everything that follows:

**"Is this for an immediate meeting or a new pursuit with time to
prepare properly?"**

- **Immediate meeting** (within 5 days) → Path A
- **New pursuit with time** (more than 5 days) → Path B

Before asking this question, kickoff checks whether context/ files
are populated. If they are empty, it runs the setup flow first
regardless of which path the rep chooses. You cannot run a pursuit
without a GTM knowledge base.

---

## First Run — Setup Flow

**Trigger**: company.md, usps.md, or market.md are empty or missing.

Before running the setup flow, check whether template files exist:
- If company-template.md exists but company.md does not → copy
  company-template.md to company.md silently before proceeding.
- Apply the same logic for usps-template.md, market-template.md,
  and value-story-bank-template.md.

The rep does not need to rename files manually. Kickoff handles
this automatically on first run.

Run this before either path. Tell the rep: "Before we start, I need
to understand what you're selling. This only needs to happen once —
the more detail you give me here, the better every command will
perform."

### Step 1 — Company research

Ask for the rep's company website URL. Research the company from
that URL and other public sources. Populate a first draft of:
- company.md — company overview, product, positioning
- usps.md — value propositions and differentiators from public sources
- market.md — target markets, industries, ICP signals

**Research rules:**
- Only use real, verifiable sources. Link every finding.
- Do not fabricate URLs or quote sources that cannot be verified.
- Flag anything that could not be confirmed publicly.

### Step 2 — Rep review

Share a short summary of what was found and what was assumed. Ask
the rep to confirm, correct, or add to each file. Do this one file
at a time, not all at once.

### Step 3 — Gap fill

After review, surface what public sources couldn't tell you.
Ask conversationally, one question at a time:

- Which specific products or solutions from the suite does the rep
  actually sell day to day?
- Which proof points or case studies do they actually use in rooms —
  not the marketing version, the ones that land?
- What does their ICP look like in practice — who do they actually
  win with?
- Are there markets, verticals, or buyer types they do not cover?

Once context/ is confirmed: "Your GTM context is set. Now let's
start your pursuit. Is this for an immediate meeting or a new
pursuit with time to prepare?"

---

## Path A — Immediate Opportunity

**Trigger**: Meeting is within 5 days.

Flag urgency immediately: "You have [X] days. We don't have time
for full qualification. Here's what we're going to do: build you
enough context to show up prepared and credible, with a few sharp
talking points specific to this client. Full qualification happens
after the meeting."

### Step 1 — Client basics

Ask for:
- Client name
- Client website URL
- Market or country
- Meeting date (confirm days until meeting)
- Who initiated the meeting and why

### Step 2 — What the rep knows

Work through these conversationally, one at a time. Skip ahead
when context is already rich:

- Who is in the room? Capture role, seniority, relationship context,
  and agency involvement if relevant. How familiar are they with your
  company and product category?
- What does the rep know about the client's goals or challenges?
- What is the client currently using, and why are they exploring
  alternatives now?
- Are there specific products or features from your suite the rep
  wants to prioritise?

### Step 3 — Light research pass

Research the client using the context-directed lens from company.md
and usps.md. Use the client website URL provided.

**Research rules:**
- Read company.md and usps.md first. Use what you are selling to
  determine what signals to look for.
- Only surface real findings with linked sources. No fabricated URLs.
- Keep it focused — 4 to 6 bullets maximum.
- Flag anything that could not be verified.

Share findings and ask the rep to confirm what aligns and correct
what doesn't before writing anything to deal_context.md.

### Step 4 — Set expectations for plays

Before handing off, be explicit: "With this level of context, I
can't build you a fully customised value story yet — we haven't
done proper qualification. What I'll give you instead is your
standard company and product introduction, sharpened with 2 to 3
research-backed talking points specific to this client. That's
the right approach for this meeting. Use the meeting itself for
discovery, then run `recap` afterwards so we can capture what you
learned."

### Step 5 — Populate deal_context.md and hand off

Write all confirmed context to deal_context.md. Then route:

"Context is set. Run `plays` to get your talking points for this
meeting, then `prep` the day before for your final brief. After
the meeting, come back and run `recap` before your next session —
that's how we keep the context current."

---

## Path B — New Pursuit

**Trigger**: More than 5 days until the meeting, or no meeting
date set yet.

### Step 1 — Client basics

Ask for:
- Client name
- Client website URL
- Market or country
- Meeting date if known

### Step 2 — What the rep knows

Work through these conversationally, one at a time:

- What triggered this pursuit? Who initiated it?
- Who is in the room or buying committee? Capture role, seniority,
  relationship context, and agency involvement if relevant. How
  familiar are they with your company and product category?
- What does the rep know about the client's goals and challenges?
- What is the client currently using, and why are they looking
  beyond it now?
- Are there specific products or features from your suite the rep
  wants to prioritise for this client?

### Step 3 — Light research pass

Research the client using the context-directed lens from company.md
and usps.md. Use the client website URL provided.

**Research rules:**
- Read company.md and usps.md first. The research lens comes from
  what you are selling — not a generic template.
- Only surface real findings with linked sources. No fabricated URLs.
- Keep it to 4 to 6 bullets maximum.
- Flag anything that could not be verified.

Share findings and ask the rep to confirm before writing anything
to deal_context.md.

### Step 4 — Populate deal_context.md and hand off

Write all confirmed context to deal_context.md. Then route:

"Context is set. Run `qualify` to work through the full pursuit —
we'll use MEDDPICC to surface what you still need to find out and
where the gaps are. Once qualification is solid, `plays` will build
your value stories and narrative for the room."

---

## deal_context.md Template

Write to this structure after every kickoff. Update it after every
subsequent command. Never overwrite confirmed information — only
add or refine.

```
# deal_context.md — [Client Name]
Last updated: [date]
Last command run: kickoff
Next recommended action: [qualify / plays depending on path]

## Basics
- Client:
- Client website:
- Market:
- Meeting date:
- Days until meeting:
- Path: [A — Immediate / B — Full pursuit]

## Trigger
- What initiated this pursuit:
- Who initiated it:

## The Room
- Attendees (role, seniority, familiarity, relationship context):
- Agency involvement:
- Familiarity with our company:
- Familiarity with our product category:

## Client Context
- Goals and challenges (known):
- Current tools or solutions:
- Why exploring alternatives now:

## Product Focus
- Solutions or features to prioritise for this pursuit:

## Research Signals
- [Finding] — [Source] — [URL]
- [Finding] — [Source] — [URL]

## Gaps
- What's still unknown and needs to be found in the room or
  through further research:

## Recap Log
- [Date] — [Key learnings from this meeting]
```

---

## Guardrails

- Never skip the setup flow if context/ files are empty.
- Never populate deal_context.md before the rep has confirmed
  research findings.
- Never promise fully customised plays on Path A — be explicit
  that full qualification hasn't happened yet.
- Always end with a specific next command. Never leave the rep
  without a clear next step.
- If the meeting is within 5 days, flag urgency immediately after
  the meeting date is confirmed.
