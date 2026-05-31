# Project: Ember Coach Hire — Self-Serve Booking Prototype

**Category:** Product / Booking  
**Company:** Ember (real company — investigate before you build)  
**Difficulty:** Medium  

---

## The Brief

Ember is a tech-first electric bus operator in the UK. They run scheduled routes but also offer coach hire — currently handled manually by their team.

- Company: [ember.to](https://www.ember.to/)
- Job posting: [Builder – AI Native](https://ember.recruitee.com/o/builder-ai-native) (full JD saved in [`job-description.md`](./job-description.md))

From their job posting:

> *"Developing a self-serve checkout for coach hire bookings, letting customers design and update their own journeys and stops."*

That's it. One sentence. No spec. No wireframes. No defined scope.

Your job is to figure out what to build and why — then build a prototype.

---

## Before You Touch Code

This is the most important part. Real AI-native builders do discovery first.

**Investigate Ember:**
- What does Ember actually do? What makes them different from a traditional coach company?
- Visit their live site. Find the coach hire flow. What happens today?
- What trip types do they offer? (hint: there are multiple — figure them out)
- What business logic is involved? (pricing, distance, stops, duration, vehicle type?)
- What constraints does an electric coach introduce that a diesel one doesn't?
- Who is the actual customer for coach hire? B2C? B2B? Both?

Write down everything you find before opening your code editor.

---

## Define Your Scope

Based on your investigation, answer these questions in writing:

1. What is the core problem you're solving with a prototype?
2. What trip type are you focusing on and why?
3. What are you explicitly NOT building? Why?
4. What assumptions are you making that a real product would need to validate?
5. What's the biggest uncertainty in this problem?

**There is no right answer.** There are well-reasoned answers and poorly-reasoned answers.

---

## Build the Prototype

Build a working prototype of the self-serve booking flow you defined above.

It should be something a real customer could interact with — not a static mockup.

---

## Evaluation Criteria

Score yourself honestly before asking for feedback.

### Discovery (did you understand the problem?)
- [ ] Can you explain Ember's business in 3 sentences without looking it up?
- [ ] Did you identify the different trip types and their distinct logic?
- [ ] Did you spot the electric vehicle constraints that affect the product?
- [ ] Did you identify who the actual customer is?

### Scoping (did you make good decisions about what to build?)
- [ ] Is your scope decision clearly reasoned, not arbitrary?
- [ ] Did you write down what you cut and why?
- [ ] Does your prototype solve a real part of the problem, not just look like it does?
- [ ] Could you defend every scope decision to a CTO?

### Build quality (is it shippable?)
- [ ] Does the core flow actually work end to end?
- [ ] Did you write unit tests for the business logic? (pricing calculation, stop validation, distance/duration logic)
- [ ] Did you handle the obvious edge cases for your chosen scope?
- [ ] Is there any basic validation / error handling?
- [ ] Could a real customer use this without breaking it?

### AI-native process (how did you work?)
- [ ] Did you set up a CLAUDE.md before starting? What did you put in it?
- [ ] Did you create any skills or reusable context files?
- [ ] Did you use sub-agents / parallel workstreams, or did you work linearly? Why?
- [ ] Where did AI get things wrong and how did you catch it?
- [ ] Did your workflow evolve during the build, or did you stick to your first approach?

---

## Common Mistakes

- Building a generic booking form without understanding Ember's actual business
- Trying to build everything (all trip types, battery optimisation, design system) in v1
- No discovery — just reading the brief and coding immediately
- Beautiful UI, broken logic
- Ignoring the electric vehicle constraint entirely

---

## Want Feedback?

Self-score first, then post in [r/AINativeBuilder](https://www.reddit.com/r/AINativeBuilder/) with the **Feedback Request** flair.

The review isn't about the code. It's about your thinking.
