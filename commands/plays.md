# plays.md — Pursuit Kit
*Activated when the rep says `plays` or when kickoff/qualify routes here.*

---

## What This Command Does

Plays builds the value stories, talking points, and deployment guidance
the rep needs for a specific client interaction. It draws from two
sources — the value-story-bank.md (proven stories and assets built
through real use) and fresh generation based on deal context when no
existing story is a strong enough match.

Plays detects which mode applies automatically from deal_context.md.
The rep does not need to specify.

---

## Before Starting

1. Read deal_context.md in full — client context, pain confirmed,
   buyer profiles, product focus, and which command was last run.
2. Read value-story-bank.md — note what proven stories and assets
   exist and which are most relevant to this pursuit.
3. Read usps.md and company.md — to ground any generated plays in
   real differentiators, not generic claims.
4. Determine which mode applies:

**Mode A — Immediate opportunity**: qualify has not been run, meeting
is within 5 days, deal_context.md has limited qualification depth.
→ Deliver a sharpened company intro with 1-2 research-backed talking
points. Flag clearly that this is not a full value story.

**Mode B — Full pursuit**: qualify has been run, deal_context.md has
solid pain, buyer, and context confirmed.
→ Build 1-3 properly deployed plays matched to the specific buyer
and confirmed pain.

---

## Mode A — Immediate Opportunity

**Trigger**: qualify not run, meeting within 5 days, thin context.

Flag this upfront: "Qualification hasn't been completed for this
pursuit. With the time available I can't build you a fully customised
value story — we don't yet have enough confirmed detail about their
specific pain and buying context. What I'll give you instead is your
standard company and product introduction, sharpened with 1-2
research-backed talking points specific to this client. Use the
meeting itself for discovery."

### Output for Mode A

**Your opening position**
A 3-5 sentence introduction to your company and solution, written
for this specific client based on what's known about their industry,
size, and any research signals from kickoff. Not generic — adapted
to what the rep knows about this prospect.

**Talking points for this client**
1-2 specific signals from the kickoff research pass, framed as
relevant observations rather than a pitch. Something the rep can
reference early in the meeting to show they've done their homework.

Format each talking point as:
- **The signal**: what was found in research
- **Why it's relevant**: how it connects to what you sell
- **How to reference it**: a natural way to bring it into conversation

**What to focus on in the meeting**
The 2-3 discovery questions from qualify (or kickoff if qualify
hasn't run) that are most important to ask in this specific meeting.
These are the rep's priority — understanding pain before pitching.

**After the meeting**
"Run `recap` to capture what you learned. Once recap is complete,
the next step depends on what emerged in the meeting — if significant
new gaps surfaced (new stakeholders, unclear pain, buying process
still unknown), run `qualify` before building the next set of plays.
If the meeting confirmed what you already knew and context is solid,
you can run `plays` directly for the next interaction."

---

## Mode B — Full Pursuit

**Trigger**: qualify has been run, deal_context.md has confirmed pain,
buyer profiles, and product focus.

### Step 1 — Match existing stories first

Check value-story-bank.md for stories or assets that match:
- The confirmed pain from qualify
- The buyer type in the room
- The product or solution focus for this pursuit

If a strong match exists: select it and move to Step 3 to adapt it
for this specific client.

If no strong match exists: flag this and move to Step 2 to generate
a fresh play.

### Step 2 — Generate fresh plays when needed

When generating a play that isn't in the value-story-bank.md, flag
it clearly: "This play has been generated from your client context
and company USPs. It hasn't been tested in a room yet — treat it as
a strong hypothesis and validate before relying on it. If it lands
well, run `recap` afterwards and it will be added to your story bank."

Use confirmed pain, buyer context, and usps.md to generate plays
that are grounded in real differentiators — never generic claims.

### Step 3 — Build and present each play

Present each play in this structure:

---

**[Descriptive title — e.g. "Premium reach story — FMCG buyer, SEA"]**

*Asset type*: Customer story / ROI model / Peer benchmark /
Best practice / TCO / Cost of inaction
*(Flag if generated and untested)*

**When to deploy**
The specific signal or moment in the conversation that triggers
this play. What does the buyer say or ask that tells the rep
this is the right moment?

**Buyer**
Who in the room this play works best with. If there are multiple
buyers present, note how the emphasis shifts for each.

**What to show**
The specific asset, data point, or reference to surface in this
moment. If it's a customer story, give the headline version the
rep can reference verbally — not a full case study to read aloud.
If it's an ROI model or peer benchmark, give the specific number
or framework the rep can use.

**What to say**
The narrative around the asset, adapted for this specific client's
context. Structure it using this four-part framework:
- **Promise** — the business outcome this story points to for
  this specific client
- **Proof** — the asset or evidence that makes it credible
- **Path** — how the client could act on it from where they are now
- **Risks** — the likely objection this play will surface and
  how to handle it

Written in natural language the rep can use loosely —
not a script to read verbatim.

**What to ask**
The follow-up question that opens the next part of the conversation.
One question only — the one most likely to deepen the client's
engagement with the point just made.

**The impact**
The specific metric or proof point that makes this play credible.
A real number where possible. If no number is available, a
directional signal — "companies in this category typically see..."

**How to adapt for this client**
The customisation layer — what makes this play specific to this
pursuit rather than generic. Explicitly address:

- **Client context**: What to emphasise or adjust based on the
  confirmed pain, buyer profile, and product focus in deal_context.md.
- **Market context**: How does this play land in the specific market
  this client operates in? Consider:
  - Local proof points or references that will resonate more than
    global ones — a regional case study lands better than a
    US-headquartered example in most APAC rooms.
  - Market maturity — is this category well understood here or
    does the rep need to establish category value before making
    the play?
  - Local business culture and relationship dynamics — how direct
    or indirect should the delivery be? Is this a market where
    numbers lead or where relationship narrative leads?
  - Agency or partner dynamics specific to this market — if an
    agency is in the room, how does the play need to shift to
    speak to their priorities alongside the brand's?
  - Language and vocabulary — are there local terms, frameworks,
    or references that make the play feel native rather than
    imported?
- **Proof point relevance**: Cross-check usps.md and market.md —
  are the proof points in this play actually documented for this
  market? If not, flag it and suggest the rep validate before
  relying on them in the room.

---

### Step 4 — Offer to add to value-story-bank.md

After presenting plays, offer: "Want me to add any of these to your
value story bank? If you've used a version of this story before and
it's landed well, adding it now means it'll be available for future
pursuits with similar buyers or pain points."

If the rep confirms, write the play to value-story-bank.md in the
standard template format. Flag whether it has been tested in a room
or generated and not yet validated.

---

## Asset Types — Reference

Use these to label each play correctly:

**Customer story** — a real client outcome told as a brief narrative.
Situation, what happened, result. Written at a level of abstraction
that doesn't identify the client unless the rep has permission to
name them.

**ROI model** — a framework for quantifying the business case. What
does the rep's solution save, earn, or improve — and what's the
number? Build from usps.md proof points and adapt to the client's
scale.

**TCO / cost of inaction** — what it costs the client to do nothing
or stay with the status quo. Most powerful with economic buyers and
CFO-level conversations.

**Peer benchmark** — "companies like yours are seeing X." Industry
or category-level proof that doesn't require a named client. Useful
when the story bank is thin or when the client is in a market where
naming clients isn't possible.

**Best practice by vertical** — what good looks like for this
industry. Positions the rep as a knowledgeable partner rather than
a vendor. Useful for early-stage conversations before pain is fully
confirmed.

---

## Guardrails

- Never generate generic plays. If deal_context.md doesn't have
  enough confirmed context to make a play specific, flag the gap
  and ask what's missing rather than producing something vague.
- Always flag generated plays as untested. Never present a
  generated play with the same confidence as a proven story.
- Maximum 3 plays per session unless the rep explicitly asks for
  more. In Mode A, maximum 2 talking points.
- Never present plays before checking value-story-bank.md first.
  Proven stories always take priority over generated ones.
- If the right to win assessment in qualify flagged that there is
  no clear right to win yet, say so before building plays. A play
  built on an unclear right to win gives the rep false confidence.
- Always end with the next recommended command — `prep` if the
  meeting is approaching, `recap` after the meeting has happened.
