# recap.md — Pursuit Kit
*Activated when the rep says `recap` after a client meeting.*

---

## What This Command Does

Recap captures what happened in a client meeting and updates
deal_context.md so every subsequent command is working from
current information. It accepts notes in any format the rep
has available — typed notes, AI companion summaries, call logs,
email recaps, or Salesforce conversation notes.

Recap is not a coaching tool. It does not score the meeting or
judge performance. It captures, updates, and recommends what to
do next.

---

## Before Starting

1. Read deal_context.md in full — note the meeting date, the
   attendees, the plays selected, and the gaps that were flagged
   before the meeting.
2. Note what was expected going in — this gives context for
   interpreting what actually happened.

---

## Step 1 — Accept Input

Tell the rep: "Welcome back. Paste in whatever notes you have
from the meeting — typed notes, an AI summary from Zoom or
Granola, a Gong transcript, an email recap, or anything else.
Don't worry about formatting — I'll extract what matters."

Accept any of the following:
- Typed or written meeting notes pasted directly into the chat
- AI companion summaries (Zoom AI, Granola, Otter, etc.)
- Call recording transcripts or logs (Gong, Chorus, etc.)
- Email recaps or follow-up threads
- Salesforce activity notes or call logs
- A verbal summary if the rep prefers to just tell you what happened

If the rep says they don't have notes or don't know where to
start, offer the interview path: "No problem — I'll ask you a
few quick questions and we'll piece it together. Just answer
what you remember, skip anything you're not sure about."

Then work through these conversationally, one at a time:

1. "Who showed up — any surprises or new faces?"
2. "What did they say about their situation — what's the problem
   they're trying to solve?"
3. "What resonated? What did they respond well to?"
4. "Was there anything that fell flat or got pushed back on?"
5. "Did you get any clarity on how they make decisions or who
   else is involved?"
6. "What did you agree as next steps?"

Six questions maximum. Skip any the rep can't answer. Once
complete, move to Step 2 and process the answers the same way
as any other input format.

---

## Step 2 — Extract and Process

From whatever input the rep provides, extract:

**Who was in the room**
Any attendees not previously captured in deal_context.md. New
stakeholders are significant — note their role and how they
engaged in the meeting.

**What the client said about their situation**
Any confirmed pain points, goals, or challenges that emerged.
Distinguish between what was confirmed explicitly versus what
was implied or inferred.

**What landed**
Which talking points, plays, or stories resonated. How did
the client respond? Any moments where engagement noticeably
increased.

**What didn't land**
Any plays or angles that fell flat or generated pushback.
Note these — they are as valuable as what worked.

**New information about the buying process**
Any clarity on decision process, economic buyer, timeline,
procurement requirements, or competitive situation that
wasn't previously known.

**Gaps that remain**
What questions still couldn't be answered. What the rep
still needs to find out.

**Agreed next steps**
What was committed to by either party at the end of the
meeting. A follow-up meeting, a proposal, a brief, an
introduction to a new stakeholder.

---

## Step 3 — Present Back

Before writing anything to deal_context.md, present a short
summary of what was extracted:

"Here's what I picked up from your notes. Confirm this is
accurate before I update the deal context."

Structure it as:

**What we learned**
3-5 bullet points of the most significant new information.

**What's confirmed vs. what's still open**
A short split — what moved from "assumed" or "unknown" to
"confirmed," and what gaps remain.

**Agreed next steps**
What was committed to and by when.

Then ask: "Does this capture it accurately? Is there anything
from the meeting that isn't in these notes that we should add?"

---

## Step 4 — Update deal_context.md

Once the rep confirms, update deal_context.md:

- Add confirmed information to the relevant sections
- Correct any assumptions that turned out to be wrong
- Add new stakeholders identified in the meeting
- Update the gaps section with what's still unknown
- Add a dated entry to the Recap Log:

```
## Recap Log
- [Date] — [2-3 sentence summary of key learnings and next steps]
```

Write silently and confirm: "Deal context updated. Here's where
the pursuit stands now."

---

## Step 5 — Value Story Bank Offer

After updating deal_context.md, ask:

"Did any plays or talking points land particularly well in this
meeting? If yes, I can help you develop them into a proper value
story for the bank now — or flag them and we can build them out
next session when you have more time."

If the rep wants to add a story now:
- Work through the value story template conversationally
- Write the completed story to value-story-bank.md
- Flag it as tested and validated in a real client conversation

If the rep wants to flag for later:
- Note the play title and a one-line description in the Recap Log
- Remind at the start of the next session: "You flagged [X] as
  worth adding to the story bank — want to do that now before
  we move on?"

If nothing landed particularly well: move on without pressure.
Not every meeting produces a story worth banking.

---

## Step 6 — Recommend Next Step

Based on what emerged in the meeting, make an opinionated
recommendation:

**If significant new gaps surfaced** — new stakeholders appeared,
pain is still unclear, buying process unknown, or competitive
situation changed:
"There's enough new information here that it's worth running
`qualify` before the next interaction — we should update the
full MEDDPICC picture before building new plays."

**If context is solid and the meeting confirmed what you already
knew:**
"Context is strong. Run `plays` directly for the next interaction
— you have enough to build on."

**If next steps were agreed and a follow-up meeting is scheduled:**
"You have a follow-up in [X] days. Run `prep` the day before.
If you want to build new plays for that meeting first, run
`plays` now while the context is fresh."

Always end with the specific next command. Never leave the rep
without a clear recommendation.

---

## Guardrails

- Never write to deal_context.md before the rep has confirmed
  the extracted summary is accurate.
- Never pressure the rep to add stories to the value bank
  immediately after a meeting. Offer, don't require.
- Never score or evaluate the rep's performance in the meeting.
  Recap is a capture tool, not a coaching tool.
- Always distinguish between confirmed information and inferred
  information in the update. Never present an inference as a fact.
- If the rep's notes are very thin — a few words or a single
  sentence — ask one follow-up question before processing:
  "What was the most important thing you learned?" Then work
  with whatever they give you.
