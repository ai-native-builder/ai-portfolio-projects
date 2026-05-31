# Project: B2B Outreach Agent

**Category:** Agent / Automation  
**Company:** Humble Group (Humble Grape + Vivat Bacchus)  

---

## The Brief

A founder-led hospitality business wants to grow its B2B customer base — corporate bookings, private events, local business accounts.

Their current outreach: manual. Someone googles local businesses, copies contact details into a spreadsheet, writes an email, sends it. Slow, inconsistent, unscalable.

From their job posting:

> *"A hyper-personalised outbound outreach agent for local B2B prospecting, scraping Google Maps, enriching leads, verifying emails, and crafting bespoke messages for every recipient."*

They want an agent that does this:
- Finds relevant local businesses
- Enriches each lead with useful context
- Verifies contact details
- Crafts a personalised outreach message for each recipient

That's it. No data provided. No tooling specified. No pipeline defined.

Your job is to figure out what to build and ship something that actually works.

- Company: [humblegrape.co.uk](https://www.humblegrape.co.uk/)
- Job posting: [AI & Automation Lead](https://humblegrape.teamtailor.com/jobs/7622691-ai-automation-lead) (full JD saved in [`job-description.md`](./job-description.md))

---

## Before You Touch Code

**Understand the domain:**
- Who is the actual target for B2B hospitality outreach? What kind of businesses book corporate events or wine tastings?
- What makes an outreach message land vs get ignored?
- What data do you actually need per lead — and what's just noise?
- Where does personalisation add value vs where is it wasted effort?
- What are the legal and ethical boundaries of automated outreach?

**Understand the pipeline:**
This is a multi-step agent. Each step has different requirements:
- Finding leads — what source, what criteria, what volume?
- Enriching leads — what extra context makes the outreach better?
- Verifying contacts — what does verified actually mean here?
- Crafting messages — where does AI add value vs where does it produce generic slop?

Map the full pipeline on paper before writing any code. Every step is a decision point.

---

## Define Your Scope

1. What is your target business type and location? Why?
2. What does your pipeline look like step by step?
3. Which tools are you using at each step and why?
4. Where does AI make decisions vs surface information for a human?
5. What is your success metric — how will you know if this actually works?
6. What are you explicitly not building and why?
7. What are the failure modes at each step?

Write this down. The pipeline map is part of the deliverable.

---

## Build the Prototype

Build a working pipeline that takes zero input and produces a list of enriched, verified leads with personalised outreach messages ready to send.

It should run on a real geography against real businesses — not synthetic data.

---

## Evaluation Criteria

### Discovery
- [ ] Did you identify the right target business type before building?
- [ ] Did you map the full pipeline before writing code?
- [ ] Did you think about legal/ethical boundaries of automated outreach?
- [ ] Did you define what "personalised" actually means vs generic?

### Scoping
- [ ] Is your tool choice at each step clearly reasoned?
- [ ] Did you define a success metric before building?
- [ ] Did you make a deliberate call on where AI sits vs deterministic logic?
- [ ] Could you defend every pipeline decision to a founder who wants ROI?

### Build quality
- [ ] Does the full pipeline run end to end without manual intervention?
- [ ] Did you write tests for the deterministic parts of the pipeline?
- [ ] How does the pipeline handle a step failing — does it crash or degrade gracefully?
- [ ] Is the output actually usable — would you send these messages yourself?

### AI-native process
- [ ] Did you set up a CLAUDE.md before starting? What did you put in it?
- [ ] Did you create any skills or reusable context files?
- [ ] Did you use sub-agents or parallel workstreams? Why or why not?
- [ ] Where did AI output require the most verification?
- [ ] Did your workflow evolve during the build?

---

## Common Mistakes

- Starting with code before mapping the full pipeline
- Scraping data without thinking about what actually makes a lead qualified
- Calling AI-generated copy "personalised" when it's just a template with a name swapped in
- No error handling when a step in the pipeline returns nothing
- Ignoring the legal side of automated outreach entirely
- No success metric — shipping without knowing if it works

---

## Want Feedback?

Self-score first, then post in [r/AINativeBuilder](https://www.reddit.com/r/AINativeBuilder/) with the **Feedback Request** flair.

The review is about your pipeline decisions and your judgment on where AI belongs — not your code.
