# Project: Legal Contract Review Agent

**Category:** Agent / Automation  
**Company:** Anonymised — a B2B software company  

---

## The Brief

A small in-house legal team reviews a steady stream of low-stakes commercial contracts — mutual NDAs, customer order forms, standard boilerplate. Most are 80% identical. Redlines and amendment requests follow patterns the team has seen dozens of times before.

Every contract still gets read by a person. The queue is always longer than the day. End of quarter is overwhelming.

Show how AI could help.

That's it. No spec. No sample contracts. No defined output format. No told-you-what-to-build.

- Company: [portswigger.net](https://portswigger.net/)
- Job posting: [AI Pioneer](https://apply.workable.com/portswigger/j/58071DA702/) (full JD saved in [`job-description.md`](./job-description.md))

---

## On Ownership

This brief came from a real job application task.

Notice what's missing: no assets provided, no scope defined, no output format specified. That's not an oversight — that's the test.

Most people wait. They ask for sample contracts. They ask what format to submit in. They wait for permission to start.

AI-native builders don't wait. They source what they need, define their own scope, build something real, and ship it. This is what separates you from every other candidate — you are the only person who did everything themselves. No team. No PM. No handoff.

High ownership is not a trait. It's the baseline.

This project exists to train that muscle.

---

## Before You Touch Code

**Understand the domain:**
- What types of contracts are we talking about? What's actually in an NDA vs an order form?
- What does a legal review actually involve? What is the reviewer looking for?
- What are the failure modes? What happens when a contract review goes wrong?
- Where is AI genuinely useful here — and where is it dangerous?
- What does "low-stakes" mean in a legal context? Does that change your approach?

You have no sample contracts. That's intentional. Find or generate realistic ones yourself before writing a line of code.

---

## Define Your Scope

1. What specific part of the contract review workflow are you solving?
2. What is your prototype actually doing — summarising, flagging, redlining, routing?
3. Where does AI make the decision vs surface information for a human to decide?
4. What are you explicitly not building and why?
5. What would break this in production?

Write this down. The scope document is part of the deliverable.

---

## Build the Prototype

Build something a real legal team could interact with — not a demo, not a slide deck.

It should handle a real contract as input and produce a useful output.

---

## Evaluation Criteria

### Discovery
- [ ] Did you source or generate realistic contract samples before building?
- [ ] Can you explain what a legal reviewer actually looks for in each contract type?
- [ ] Did you identify where AI can and cannot be trusted in this workflow?
- [ ] Did you think about what a mistake costs here vs other domains?

### Scoping
- [ ] Is your scope decision clearly reasoned and written down?
- [ ] Did you make a deliberate call on where the human stays in the loop?
- [ ] Did you cut features with clear reasoning, not laziness?
- [ ] Could you defend every decision to a sceptical lawyer?

### Build quality
- [ ] Does it handle a real contract end to end?
- [ ] Did you write tests for any deterministic logic in the pipeline?
- [ ] Did you evaluate your output — does it actually help, and by how much?
- [ ] Is the output something a non-technical legal team member could use?

### AI-native process
- [ ] Did you set up a CLAUDE.md before starting? What did you put in it?
- [ ] Did you create any skills or reusable context files?
- [ ] Did you use sub-agents or parallel workstreams? Why or why not?
- [ ] Where did AI get things wrong and how did you catch it?
- [ ] Did your workflow evolve during the build?

---

## Common Mistakes

- Trusting AI output on legal content without verification
- Building a summariser and calling it a review agent
- Not thinking about who the actual user is — a lawyer, not a developer
- Skipping evals — "it looks right" is not an evaluation
- Waiting for sample contracts instead of sourcing them yourself

---

## Want Feedback?

Self-score first, then post in [r/AINativeBuilder](https://www.reddit.com/r/AINativeBuilder/) with the **Feedback Request** flair.

The review is about your ownership and your judgment — not your code.
