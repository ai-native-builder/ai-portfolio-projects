# Project: Multi-Agent Orchestration Layer

**Category:** Agent / Architecture  
**Company:** Anonymised — an online university platform  

---

## The Brief

An online education platform runs several learner-facing AI agents — an admissions/discovery agent and a Career Advisor agent. They were built independently, sit on different stacks, and don't share context.

A learner asks: *"What program is right for me, and what jobs does it lead to once I graduate?"*

Currently they bounce between two agents that don't know each other exist. Each gives a disconnected answer.

Your job: design and build an orchestration layer that fixes this.

---

## What To Build

Your orchestrator should:
- Route between a discovery/admissions agent and a Career Advisor agent
- Look up the learner's enrolment status from a CRM-style system (HubSpot or a stub that simulates it)
- Return a single, coherent response — not three disconnected ones

Assume ~10,000 learners. Be explicit about how you'd scale from prototype to production.

---

## Before You Touch Code

**Understand the problem:**
- Why do agents built independently fail to share context? What's the root cause?
- What does a learner actually need from this interaction — and in what order?
- What does "coherent response" actually mean? What makes it feel coherent vs stitched together?
- What are the failure modes when agents hand off to each other?
- Where does the CRM lookup fit in the flow — before routing, during, or after?

Map the full architecture on paper before writing any code.

---

## Deliverables

This project has three parts — all required.

### Part 1 — Strategy Memo (max 2 pages)

Write a crisp memo answering:

**Architecture** — what's the right shape: single orchestrator, multi-agent, routing layer, hybrid? Why this and not the alternatives?

**Build vs buy vs partner** — which framework, which model provider, which custom component? Be specific and justify each choice.

**Success metrics** — 2-3 concrete metrics you'd track in production. What does good look like at 30 days, 90 days, and steady state?

**Top 3 risks** — from: cost, latency, hallucination, privacy, integration brittleness. Pick the three you actually worry about and how you'd mitigate them.

**What you'd cut** — what is NOT in v1 and why?

The memo is not a warmup. It is evaluated equally with the code.

### Part 2 — Working Prototype

Build something runnable. Not production — a prototype that proves you can ship code.

Your repo must include:
- Code that runs end to end with a clear README (how to run it, what's stubbed vs real)
- Architecture overview — diagram preferred, README section acceptable
- Evals approach — even minimal. How would you know if the system is getting better or worse?
- One paragraph: what would it take to productionise at 10,000 learner scale?
- A note on which parts you wrote vs used a code assistant for — be honest, it's expected

### Part 3 — Walkthrough Prep

Prepare to present your prototype as if to a CTO. If you book a review session, this is what it will cover:
- Defend every technical choice
- What you'd change with two more weeks
- A curveball extension — you'll be asked to extend it on the spot

---

## Evaluation Criteria

### Thoughtfulness
- [ ] Did you pick the right shape for the architecture?
- [ ] Is your scope decision defensible?
- [ ] Did you write down what you cut and why?
- [ ] Does the memo read like someone who's shipped agents, not just read about them?

### Technical fluency
- [ ] Is the code well-structured and readable?
- [ ] Are framework and model choices justified not just listed?
- [ ] Can you explain every tradeoff you made?
- [ ] Does the prototype actually run end to end?

### Productionisation thinking
- [ ] Did you think about cost and latency at 10k learners?
- [ ] Is there an evals approach, even minimal?
- [ ] Have you addressed privacy and data handling?
- [ ] Is the stub/real boundary clearly documented?

### Communication
- [ ] Is the memo crisp and under 2 pages?
- [ ] Can a non-technical stakeholder understand the value?
- [ ] Can a technical one challenge the choices and get real answers?

### AI-native process
- [ ] Did you set up a CLAUDE.md before starting? What did you put in it?
- [ ] Did you use sub-agents or parallel workstreams? Why or why not?
- [ ] Where did AI get things wrong and how did you catch it?
- [ ] Were you transparent in the repo about how you used code assistants?

---

## Common Mistakes

- Building before writing the memo — the memo forces clarity the code can't
- Stitching three responses together and calling it orchestration
- No CRM integration at all, even a stub
- Evals section missing entirely
- Prototype that runs but can't be explained
- Memo that describes what the system does instead of why it's designed that way

---

## Want Feedback?

Self-score first, then post in [r/AINativeBuilder](https://www.reddit.com/r/AINativeBuilder/) with the **Feedback Request** flair.

The review covers architecture decisions, memo quality, and how you'd perform in the live walkthrough — not just whether the code runs.
