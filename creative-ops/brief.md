# Project: Creative Operations Platform

**Category:** Automation / Workflow  
**Company:** Anonymised — a social media creative agency  

---

## The Brief

A social media team manages monthly content planning, approvals, and community engagement across multiple platforms.

Their current process:
- Everything lives in a shared Excel file
- Approvals happen over email, copy-pasted back into the sheet manually
- Leadership, PR, and legal teams receive a weekly Excel copy by email
- Feedback from those teams travels back the same way

They need a better system.

Your job is to design and build a working prototype that solves the core operational problem.

---

## Before You Touch Code

**Investigate the domain:**
- Who are the different people involved in this workflow? What does each one actually need?
- What are the different types of content being managed? Are they the same problem?
- What are the different types of approval happening? Are they the same problem?
- Where does the current process break down and why?
- What's the cost of a mistake in each part of this workflow?

Write this down before you build anything.

---

## Define Your Scope

1. What is the core problem you're solving?
2. What are you building and for which users?
3. What are you explicitly not building and why?
4. Where does AI fit — and where should it not?
5. What's the biggest risk in this system if something goes wrong?

---

## Tooling

Build this in **Airtable**. Create a free account if you don't have one.

This is intentional. Many creative ops and marketing teams run on tools like Airtable. Understanding how to build inside a no-code/low-code platform — its constraints, its automation layer, its interface builder — is a real skill.

---

## Build the Prototype

Build a working prototype that a real team could use to plan, review, and approve content.

A sample dataset is provided in `data/creative_operations.xlsx` — use it as the basis for your data model. Don't start from a blank Airtable.

---

## Automation Layer

Build at least one automation. Before you build it, answer in writing:

**Airtable native automations** — triggers, conditions, actions built inside Airtable. Fast to set up, no external dependencies. What are the limits?

**External AI automation** — bringing in Claude API, Make, n8n, or similar. More powerful, more complex, more cost. When does this make sense vs native?

**For every automation you build, document:**
- What does it do?
- Why did you choose this tool for this automation?
- What are its limits?
- What would you replace it with at 10x the scale?

Tool judgment is the skill. Anyone can click "create automation." Few people can explain why.

---

## Evaluation Criteria

### Discovery
- [ ] Can you name every type of user and what they need from the system?
- [ ] Did you identify the different approval types and what makes them different?
- [ ] Did you spot where the current process creates the most friction?
- [ ] Did you think about what a mistake costs in each workflow?

### Scoping
- [ ] Is your scope decision clearly reasoned?
- [ ] Did you write down what you cut and why?
- [ ] Did you make a deliberate decision about where AI helps and where it doesn't?
- [ ] Could you defend your architecture to a technical lead?

### Build quality
- [ ] Does the core workflow actually function end to end?
- [ ] Are the right things automated and the right things human-controlled?
- [ ] Could a non-technical user operate this without breaking it?

### AI-native process
- [ ] Did you set up a CLAUDE.md before starting? What did you put in it?
- [ ] Did you create any skills or reusable context files?
- [ ] Did you use sub-agents or parallel workstreams? Why or why not?
- [ ] Where did AI get things wrong and how did you catch it?
- [ ] Did your workflow evolve during the build?

---

## Common Mistakes

- Treating all approvals as the same type of problem
- Building for one user type and forgetting the others
- Automating the wrong things
- No data model thought through before building
- Beautiful UI, broken workflow logic

---

## Want Feedback?

Self-score first, then post in [r/AINativeBuilder](https://www.reddit.com/r/AINativeBuilder/) with the **Feedback Request** flair.

The review is about your decisions, not your code.
