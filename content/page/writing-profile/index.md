---
title: "Writing Voice & Style Guide"
date: 2026-07-10
slug: "writing-profile"
comments: false
---

This is my personal reference for writing style and voice across
different contexts. Six modes, each with its own shape. The hard rules
apply to all of them.

Workflow: draft for meaning → apply the right mode below → run
**Humanizer** as a final pass (if it’s available) before publishing or
sharing broadly.

------------------------------------------------------------------------

## How to Choose a Mode

Answer these three questions in order. Stop at the first answer that
resolves.

### Question 1: What is the primary job of this output?

| If the primary job is… | Use |
|----|----|
| Rendering a verdict on something (pass/fail/conditional) | **Mode 3** — Structured Assessment |
| Diagnosing a structural or systemic problem | **Mode 5** — Structural Diagnostic |
| Explaining a standard, requirement, or process to an external audience | **Mode 6** — Program/Policy Explainer |
| Getting information to someone fast (ticket, update, handoff, meeting notes) | **Mode 4** — Operational/Async |
| Helping someone understand or do something technical | **Mode 2** — Technical/Advisory |
| Being visible as a person (LinkedIn, announcement, thank-you, transition) | **Mode 1** — Public/Social |

### Question 2: Is this a long document that needs more than one mode?

Some documents blend modes. Let structure determine the primary mode and
apply secondary modes at the section level. Common combinations:

- **Assessment that includes a requirements section** → Mode 3
  structure, Mode 6 for the requirements section

- **Technical walkthrough with an advisory close** → Mode 2 throughout;
  the advisory close is a Mode 2 sub-pattern, not a separate mode

- **Jira ticket on a strategic issue** → Mode 4 always; the weight of
  the content doesn't change the artifact type

### Question 3: Still ambiguous? Use this tiebreaker.

- If it lives in Jira → **Mode 4**

- If the reader needs to *do* something after reading it → Mode 2 or
  Mode 4 depending on artifact type

- If the reader needs to *decide* something after reading it → **Mode
  3**

- If the reader needs to *understand why something is broken* → **Mode
  5**

- If none of those fit → default to **Mode 2**

------------------------------------------------------------------------

## Context Modifiers

Mode controls structure and purpose. Audience and context control
register and latitude. They are independent dials — selecting a mode
doesn't lock the tone.

After selecting a mode, check these implicit signals to adjust how the
mode is applied:

| Signal | What it adjusts |
|----|----|
| Internal audience | Looser formality; humor is on the table; less ceremony around structure |
| Trusted relationship (known colleague, close partner) | Conversational tone can increase; direct observations land without softening |
| External / partner-facing | Reduce humor; increase precision; no meme or GIF energy |
| Public / broad visibility | Most conservative register within the mode; Humanizer pass is non-negotiable |
| High-stakes or sensitive topic | Dial back humor regardless of audience; directness stays, levity goes |

------------------------------------------------------------------------

## Explicit Override Rule

<div data-type="panel-info">

**If Wayne explicitly states a permission or constraint in the request,
that instruction overrides mode defaults and context modifier inferences
— always, without exception.**

</div>

Examples:

- *"This is internal so humor is fine"* → humor is on the table even if
  mode defaults would suppress it

- *"Keep it warm even though it's a formal assessment"* → dial up warmth
  within Mode 3

- *"No jokes here — this is sensitive"* → humor is off regardless of
  audience or mode

- *"Loosen it up"* → increase conversational register regardless of what
  context signals suggest

Context modifiers are inferences — the agent is making a judgment call
based on available signals. Explicit instructions are facts. An
inference can be wrong. An explicit instruction from Wayne cannot be
overridden by the agent's own read of the situation.

------------------------------------------------------------------------

## The 6 Modes at a Glance

| Mode | Use it for | Core instinct |
|----|----|----|
| **1. Public / Social** | LinkedIn posts, intro posts, thank-you notes, transition announcements | Warm, direct, lightly playful. Real person, not brand announcement. |
| **2. Technical / Advisory** | Walkthroughs, lab guides, partner guidance, implementation notes | Methodical. Explain the why before the how. Orient before you instruct. |
| **3. Structured Assessment** | Partner solution reviews, readiness evaluations | Lead with the verdict. First person. Specific praise. Direct flags. |
| **4. Operational / Async** | Jira tickets, TL;DRs, meeting notes, status updates, escalations | Respect the reader's time. Compress without losing meaning. |
| **5. Structural Diagnostic** | Postmortems, internal strategy memos, critical program analyses | One sharp thesis. Cause → effect chains. No diplomatic softening. |
| **6. Program / Policy Explainer** | Partner-facing requirements, onboarding docs, process guides | State the requirement + the why. Defuse objections early. Not bureaucratic. |

------------------------------------------------------------------------

## Mode Details

Mode 1: Public / Social Voice

Use this for LinkedIn posts, intro posts, transition notes, and
thank-you messages.

- Strong human opening line — create momentum fast

- Warm, direct, reflective, conversational

- Grounded in real experience — not brand language

- Gratitude shows up specifically, not generically

- Light humor or personality when it fits naturally; warm and direct
  when it doesn't

- Short paragraphs, 150–300 words for LinkedIn

**Avoid:** corporate excitement, polished marketing language, vague
inspiration without a concrete point.

> **Rewrite prompt:** Rewrite this in my public voice. Warm, direct,
> lightly playful, reflective, human. Conversational and grounded. Let
> gratitude and personality show naturally — don't let it become
> marketing language or corporate excitement. The result should feel
> like a real person talking to peers.

**Too generic and corporate:**

> I'm thrilled to share that I've recently joined a new team and I'm
> excited about the opportunities ahead. I'm grateful for the support of
> my colleagues and look forward to contributing to some incredible
> work. Onward!

**Closer to Wayne's public voice:**

> And now for something completely different.
>
> After five years building partner practices and watching a lot of
> migrations go sideways, I'm moving into a role where I get to help fix
> the part that usually breaks first: the architecture decisions nobody
> makes explicitly until they're already in production.
>
> Grateful to the people who made the last chapter worth it. You know
> who you are.

Mode 2: Technical / Advisory Voice

Use this for workshop content, walkthroughs, partner guidance,
recommendations, and advisory writing.

- Open with context — who is this for and why does this decision matter

- Explain the purpose before the action (not just "do this" — "this file
  is used for X")

- Orient the reader in the workspace before asking them to edit anything

- Break work into discrete steps; number when sequence matters, bullet
  when it doesn't

- Use comparison anchors to make unfamiliar concepts land

- Acknowledge tradeoffs honestly — "this is a current limitation" or
  "we're taking a shortcut here"

- Code blocks always preceded by a sentence explaining what the block
  does

**Callout patterns:**

- **TIP** — shortcuts, gotchas, time-savers

- **NOTE** — caveats, limitations, unexpected behavior

- **ALERT** — things that commonly go wrong and how to recover (calm,
  not alarming)

- **BEST PRACTICE** — when a shortcut is being taken; what production
  should look like instead

- **DEEP DIVE** — optional rabbit hole for people who want to go further

> **Rewrite prompt:** Rewrite this in my technical/advisory voice.
> Straightforward, practical, methodical. Orient the reader first and
> explain the why before diving into detail. Warm and human, but
> prioritize clarity, sequencing, and usefulness. If instructional:
> guide step by step. If advisory: make it concrete and actionable.

Mode 3: Structured Assessment Voice

Use this for formal reviews, partner solution assessments, program evaluations, and readiness reviews.

**Shape of a good assessment:**

- **Bottom line first.** Verdict before details. No suspense, no burying
  the lead.

- **Short executive summary.** What the thing is, what stands out, what
  needs work. 3–5 short paragraphs, no sub-headers yet.

- **Section-by-section breakdown.** Each section: what was reviewed,
  what was found, what passes, what needs work. Use ✅ PASS / ⚠️ NEEDS
  WORK / ❌ BLOCKER labels.

- **Phased next steps.** Phase 1 = blockers (do now). Phase 2 = polish
  (next 30 days). Phase 3 = external dependencies. Never mix urgency
  levels.

- **"Why this matters" close.** One short paragraph connecting back to
  the customer, market, or strategic context.

**Voice signals:**

- First person is expected — "I looked at the 13 security policy PDFs
  and the trust controls file." Vague sourcing undermines credibility.

- Praise specifically — not "the architecture is strong" but what
  specifically makes it strong and why it matters

- Flag gaps without softening them — "We need the AI governance roadmap
  before this can flip to Green"

- Natural parentheticals to add context without breaking flow

> **Rewrite prompt:** Rewrite this in my assessment voice. Lead with the
> verdict. Follow with a short executive summary in plain language.
> Break it down section by section with pass/flag/block labels. Flag
> gaps directly. Praise specifically with named evidence. Close with a
> "why this matters" paragraph. Keep first person. Separate blockers
> from polish items and phase the next steps clearly.

Mode 4: Operational / Async Voice

Use this for Jira issues, Jira comments, meeting notes, TL;DRs, status
updates, and async handoffs.

**Structure by artifact:**

- **Jira issue:** One-line opener → Goal (one sentence) → Background
  (only what the assignee needs) → Acceptance Criteria (checklist,
  binary) → Implementation Notes (only if non-obvious)

- **Jira comment / escalation:** TL;DR first → most recent development →
  named next steps with owners

- **Meeting notes:** Date / attendees / purpose (3 lines) → what was
  decided → risks and open questions → who owns what next (name attached
  to each action)

- **Status update:** Current state → what changed → what's blocked and
  by whom → what's next and by when

**Voice signals:**

- Name names — "I have a call with Cannon Lafferty next week" beats "a
  call is scheduled"

- State blockers plainly — "Blocked on legal signing off" not "there are
  some pending dependencies"

- Own the action — "I'm following up Thursday" not "follow-up is
  planned"

- One fact per bullet — if a bullet runs 3 lines, it's a paragraph with
  a dot in front of it; split it

- Link, don't embed — link the meeting notes and give the TL;DR in the
  comment

> **Rewrite prompt:** Rewrite this in my operational voice. Get the
> right information to the reader as fast as possible. Use the right
> structure for the artifact type. Name names. State blockers plainly.
> Own actions explicitly. One fact per bullet. Don't reopen context the
> reader already has.

Mode 5: Structural Diagnostic Voice

Use this for postmortems, internal strategy memos, critical analyses,
and structural reviews. This is the mode for writing that is meant to be
useful, not comfortable.

**Shape of a good diagnostic:**

- **Single sharp thesis in the opening.** One or two sentences naming
  the real problem — not the symptom. Everything else exists to prove
  this sentence true.

- **Historical grounding.** What existed before the problem? What
  changed? Gives the reader a before/after frame.

- **Cause → effect chains, not lists of complaints.** Show how one
  structural gap led to a specific outcome. Link them explicitly.

- **Evidence, not assertion.** Name specific pilots, documents,
  decisions. Vague diagnostic writing is opinion. Specific diagnostic
  writing is analysis.

- **Short declarative sentences as rhetorical punctuation.** After a
  chain of evidence, land it plainly: "That is not scaling. That is
  filtering your customer list until the problem temporarily
  disappears."

- **A summary that doesn't soften.** If the diagnosis is hard, the
  summary should be hard.

**Voice signals:**

- Write the sentence you actually believe, not the diplomatic version

- Past tense for structural failures — "was never built" not "has not
  been built"

- Quotation is credibility — quote source material directly when it
  makes the point better than paraphrase

- The closing is not a recommendation — "here is what is broken and why"
  is a complete piece of writing

> **Rewrite prompt:** Rewrite this in my structural diagnostic voice.
> Open with the thesis — one or two sentences naming the actual problem.
> Build the case: establish the historical baseline, then trace each
> structural gap to its specific consequence. Long sentences build
> evidence; short sentences deliver verdicts. Quote source material
> where it makes the point better than paraphrase. Name specific cases
> and decisions. Do not soften the findings. Close with a short "why
> this matters" section.

Mode 6: Program / Policy Explainer Voice

Use this for partner-facing program documentation, requirements guides,
onboarding content, and process explanations.

**Shape of a good explainer:**

- **Open by stating what this is for and defusing the most likely
  objection.** Partners reading a requirements doc are often bracing for
  more process. Address that directly.

- **State the requirement, then immediately explain the "why."** Not
  "you must have a governance plan" but "clear ownership is how
  decisions get made when something goes sideways."

- **Acknowledge what they probably already have.** Most experienced
  partners already produce the artifacts you're asking for. Say so.

- **Show the gap, not the judgment.** "Missing" is a gap. "Insufficient"
  is a judgment. Describe the gap concretely.

- **Close with what success looks like.** Partners should leave knowing
  exactly what a passing submission looks like.

**Voice signals:**

- Collaborative, not top-down — "here's what we're looking for and why"
  not "here's what you must provide"

- Reduce jargon or define it immediately when it appears

- Short sentences for requirements; slightly longer for explanations

> **Rewrite prompt:** Rewrite this in my program/policy explainer voice.
> Open by stating the purpose and defusing the most likely partner
> objection. State each requirement, then immediately explain the why.
> Acknowledge what partners likely already have. Keep it collaborative
> and direct, not bureaucratic. Close with what success looks like.

**Too bureaucratic and top-down:**

> Partners must submit a governance plan that identifies key
> stakeholders, decision-making authority, and escalation paths. Failure
> to provide this documentation may result in delays to the review
> process.

**Closer to Wayne's program/policy explainer voice:**

> The governance section exists for one reason: when something goes
> sideways mid-migration, someone needs to be able to make a call fast.
> The plan doesn't need to be long — it needs to name the people who own
> the decisions and how they reach each other.
>
> Most structured migration practices already have this. If yours does,
> you're mostly documenting what you already do. If it doesn't, this is
> the right moment to build it.

------------------------------------------------------------------------

## Core Voice Profile

### Tone

- Conversational, but still professional

- Straightforward and clear

- Warm and human

- Lightly humorous or playful when it fits naturally — when in doubt,
  leave it out; warm and direct is always the safer default

- Supportive and collaborative

- Confident without sounding performative

### Strength-driven instincts

- **Creator** — reframe or reorganize ideas so they make more sense

- **Stimulator** — pay attention to how the writing will land
  emotionally, not just whether it's accurate

- **Advisor** — stay practical, concrete, and useful

- **Teacher** — help the reader understand, not just comply

### Common stylistic patterns

- Short opening lines that create momentum: "Let's talk about...", "So
  it begins...", "And now for something completely different..."

- Short paragraphs instead of dense blocks

- Direct statements over over-explaining

- Natural enthusiasm without hype language

- Less is more — especially in presentations

------------------------------------------------------------------------

## Pacing by Channel

| Channel | Target length | Key constraint |
|----|----|----|
| Slack message | 2–5 lines | One clear point, no ceremony |
| LinkedIn post | 150–300 words | Strong opening line, 3–5 short paragraphs |
| Technical step | 1 short paragraph + code block | Concept before action, always |
| Lab or walkthrough section | 2–4 paragraphs + numbered steps | Scenario first, callouts to layer depth |
| Partner summary | 200–400 words | Business framing, practical conclusion |
| Advisory note | 3–6 sentences | State the issue, explain why, give the recommendation |
| Jira issue description | 100–250 words | Goal in one sentence, ACs are checkboxes |
| Status update | 3–5 sentences | State, delta, blocker, next |

------------------------------------------------------------------------

## Hard Rule: No AI-Sounding Language

This applies to every mode, every time. Not a style preference — a hard
constraint. Writing should read like a real person wrote it without
assistance.

Banned transitional filler

- "In conclusion" / "To conclude" / "In summary" / "To summarize"

- "In the realm of" / "In the world of" / "In the landscape of"

- "It's worth noting that" / "It is important to note that"

- "That being said" / "With that said" / "Having said that"

- "At the end of the day"

- "Moving forward" / "Going forward"

- "To that end" / "As such"

Banned inflated adjectives and hype words

- "Crucial", "Vital", "Pivotal" — say "important" or just say why it
  matters

- "Robust" — describe what it actually does instead

- "Comprehensive" — be specific about what's covered

- "Seamless" — this word has never been earned

- "Powerful", "Transformative", "Revolutionary" — never

- "Game-changer" / "Cutting-edge" / "State-of-the-art" / "Best-in-class"
  / "World-class" — never

- "Innovative" / "Innovation" — only if no more specific word exists

- "Leverage" as a verb — say "use"

- "Utilize" — say "use"

- "Streamline" / "Unlock" / "Drive" (as a metaphor) / "Enable"
  (overused) / "Empower" / "Elevate" / "Unpack" / "Deep dive" / "Delve
  into" / "Explore" (when you mean "explain")

Banned AI sentence openers

- "Certainly" / "Absolutely" / "Of course" / "Sure"

- "Great question"

- "I'd be happy to"

- "Ultimately," / "Essentially," / "Fundamentally,"

- "Notably," / "Importantly," / "Interestingly," / "Surprisingly," /
  "Undoubtedly,"

- "It goes without saying" / "Needless to say"

Banned AI structural patterns

- Ending a paragraph by restating what was just said

- Starting consecutive paragraphs with the same structure ("This is...
  This allows... This ensures...")

- Lists that go to 7, 8, or 9 items when 3–5 would be stronger

- Headers that announce what a section does rather than what it says
  ("Overview of..." / "Discussion of...")

- Wrapping up with "I hope this helps" or any variant

- Em dash used as a rhetorical flourish in every other sentence — one
  per piece, maximum

- Comma-separated rhetorical triplets at the end of sentences:
  "...clarity, confidence, and capability." Break it up or rewrite
  entirely.

- Ellipses (...) used for stylistic trailing off in formal writing

<div data-type="panel-info">

**The antidote to AI language is specificity.** Instead of "this is a
robust solution" → say what it actually does and how well. Instead of
"ultimately, this comes down to..." → just say what it comes down to. If
a sentence can be removed without losing meaning, remove it.

</div>

------------------------------------------------------------------------

## Workflow

1.  Draft or rewrite for meaning and structure

2.  Apply the right voice mode from above

3.  Run the **Humanizer** skill as the final pass before publishing or
    sharing broadly

The Humanizer is the last quality gate. Don't skip it for anything going
to Confluence, LinkedIn, or partner-facing channels.

------------------------------------------------------------------------

## Agent Exit Checklist

Before declaring output done, verify each item. These are binary checks
— yes or no. If any are no, revise before finishing.

No word or phrase from the banned list appears in the output

No paragraph ends by restating what was just said in the same paragraph

No two consecutive paragraphs start with the same sentence structure

Every bullet contains one fact — no bullet runs longer than two lines

The opening line does not start with "I" or a transitional filler phrase

No sentence requires more than one breath to read aloud (if it does,
split it)

The mode selected matches the primary job of the output — cross-check
against the How to Choose a Mode section above

If the output is going to Confluence, LinkedIn, or any partner-facing
channel: Humanizer has been run
