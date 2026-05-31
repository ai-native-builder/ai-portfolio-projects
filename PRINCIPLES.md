# Principles for AI-Native Builders

Read this before starting any project. Come back to it when you're stuck.

These principles exist to help you make scope decisions, not to make them for you. Every project is different. Use these as a checklist, not a formula.

---

## 1. Via Negativa
**Remove before you add.**

The best scope decision is usually subtraction. Before adding a feature, ask: what can I remove and still solve the core problem?

Most prototypes fail not because they lack features but because they have too many. Every feature is a surface for failure, a thing to maintain, a decision the user has to make.

**Before you build, ask:**
- What is the smallest thing that solves the real problem?
- Which features am I adding because they're easy, not because they're needed?
- If I ship without this, does the core still work?

---

## 2. Antifragile Design
**Let failures make the system stronger.**

A fragile system breaks under stress and stays broken. An antifragile system breaks, logs why, and comes back tighter.

This means: build in logging from day one. When something goes wrong — wrong output, edge case, user confusion — that failure should automatically make the system better. Auto-log misses. Tighten prompts from real incidents. Don't patch and forget.

**Before you build, ask:**
- How will I know when this fails?
- What happens to that failure information — does it disappear or feed back in?
- Am I building a system that learns from production, or one I have to manually fix every time?

---

## 3. Skin in the Game
**Risky actions need explicit approval and a paper trail.**

If your system takes an action that's hard to reverse — sends an email, modifies a record, approves a contract, charges a customer — someone must explicitly approve it and that approval must be traceable.

Don't automate the irreversible. Automate the reversible, surface the irreversible for human judgment.

**Before you build, ask:**
- What are the irreversible actions in this system?
- Who approves them and how is that recorded?
- If something goes wrong, can I trace exactly what happened and who signed off?

---

## 4. Barbell Strategy
**Stable core. Isolated experiments.**

Keep your core agent or workflow small, simple, and reliable. Put experimental features — new models, new tools, new approaches — in isolated channels where they can fail without taking everything down.

Don't mix your stable production logic with your experiments. They have different risk profiles and should be treated differently.

**Before you build, ask:**
- What is the stable core that must always work?
- What is experimental and should be isolated?
- If my experimental feature fails completely, does the core still run?

---

## 5. Black Swan Readiness
**Assume unknown failures. Build for them anyway.**

You cannot predict every failure mode. That's the point. What you can do is build circuit breakers, rate limits, and safe fallbacks so that when something unexpected happens, the system degrades gracefully rather than catastrophically.

The failure you haven't thought of is more dangerous than the one you have.

**Before you build, ask:**
- What does graceful degradation look like for this system?
- Where are the circuit breakers — points where the system stops rather than does something harmful?
- What is the safe fallback when the AI gets it wrong?

---

## 6. Optionality
**Prefer reversible over irreversible. Small experiments, easy rollback.**

A config change is better than a code fork. A feature flag is better than a deployment. A prompt edit is better than a new agent. The more reversible your decision, the cheaper it is to be wrong.

This applies to scope too. Scope decisions that are hard to undo should require more justification than ones that are easy to reverse.

**Before you build, ask:**
- Is this decision reversible if I'm wrong?
- Am I making a permanent architectural choice when a temporary one would do?
- Can I test this with a small experiment before committing?

---

## 7. Robustness Over Optimisation
**Simple rules that degrade gracefully beat perfect logic that breaks.**

Brittle systems are often over-engineered. The "perfect" routing logic that handles every edge case is also the thing that fails in ways nobody predicted. A simple rule that handles 80% of cases and fails safely on the other 20% is often better.

Don't optimise before you've validated. Don't add complexity to handle edge cases you haven't seen in production yet.

**Before you build, ask:**
- Am I over-engineering for edge cases I've imagined but not seen?
- What does this system do when it hits something it wasn't built for?
- Is there a simpler rule that gets me 80% of the way with half the complexity?

---

## The Scope Checklist

Run your prototype idea through these before writing code:

| Principle | Question | Your Answer |
|-----------|----------|-------------|
| Via Negativa | What can I remove and still solve the problem? | |
| Antifragile | How will failures feed back into improvements? | |
| Skin in the Game | What are the irreversible actions and who approves them? | |
| Barbell | What is the stable core vs the experimental layer? | |
| Black Swan | What is the safe fallback when something unexpected happens? | |
| Optionality | Is this decision reversible? | |
| Robustness | Am I over-engineering for edge cases I haven't seen yet? | |

You don't need perfect answers. You need honest ones.

---

## When to Come Back Here

- You're adding a feature and not sure if it belongs in v1 → **Via Negativa**
- Your prototype works but you're not sure how to handle errors → **Antifragile + Black Swan**
- Your agent is taking actions and you're not sure who's accountable → **Skin in the Game**
- You're mixing stable logic with experimental ideas → **Barbell**
- You've made an architectural decision that's hard to undo → **Optionality**
- Your routing or classification logic is getting complicated → **Robustness**

---

These principles won't tell you what to build. They'll tell you when to stop adding, when to simplify, and when to slow down before committing to something irreversible.

That judgment is the skill.
