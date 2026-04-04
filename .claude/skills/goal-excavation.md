# Skill: goal-excavation

## Trigger
Invoked by `session-start` for new student intake or returning student check-in. Also invoked mid-session when goal clarification is needed.

## Purpose
Excavate the student's actual goals through a 3-pass Socratic spiral. Each pass deepens the picture. A vague or socially-expected answer in pass 1 is never sufficient — it is a prompt to probe further, not a foundation for planning.

## Two Modes

This skill operates in two modes set by `session-start`. Use the correct question form throughout — do not mix them.

- **Advisor mode:** Questions are asked *about* the student in third person. Example: "What does Amara say she wants to do?"
- **Student-direct mode:** Questions are asked *to* the student in second person. Example: "What do you imagine your working life looking like?"

All probing rules and hard gates apply equally in both modes.

---

## The Three Passes

### Pass 1 — Career & Professional Goals
**Goal:** Understand what the student says they want to do after graduation.

**Opening question:**
- Advisor: "What does [student name] say they want to do after graduation — or what do they imagine their working life looking like?"
- Student-direct: "What do you imagine your working life looking like — or what do you think you want to do after graduation?"

**Probing rules:**
- If the answer is a job title alone ("software engineer," "teacher," "I don't know"), do NOT route to `learning-plan`. Probe:
  - Advisor: "Who are they building for / working with in that role? Can you paint a picture of a day?"
  - Student-direct: "Who do you picture yourself building for, or working with? What does a day actually look like?"
- If the answer is vague ("help people," "something with tech"), do NOT route to `learning-plan`. Probe:
  - Advisor: "Tell me about a time they described something they built, did, or cared about that felt meaningful — even outside of school."
  - Student-direct: "Tell me about something you built, made, or worked on that actually felt meaningful to you — even if it had nothing to do with school."
- If the answer is borrowed from family/culture ("my parents want me to be an engineer"), explore:
  - Advisor: "What does [student] light up about when they talk about their own projects or interests?"
  - Student-direct: "What do *you* light up about — setting aside what anyone else expects?"

**End of pass 1:** Produce a brief draft learning snapshot (2–3 sentences) and state it. Then:
- Advisor: "Let me ask one more dimension before we go further."
- Student-direct: "Let me ask you one more thing before we go any further."

### Pass 2 — Values & Meaning
**Goal:** Understand the kind of impact the student wants to have and the communities or causes they care about.

**Opening question:**
- Advisor: "What kind of difference does [student name] want their work to make — in whose life, in what community, toward what kind of change?"
- Student-direct: "What kind of difference do you want your work to make — in whose life, in what community?"

**Probing rules:**
- If the answer is abstract ("I want to make a difference"), probe:
  - Advisor: "Can they name a specific person, neighborhood, organization, or problem they keep coming back to?"
  - Student-direct: "Is there a specific person, place, or problem you keep coming back to — even outside of school?"
- If values seem in tension with pass 1 goals, name it gently:
  - Advisor: "It sounds like there might be some tension between [career goal] and [value]. Is that something [student] has noticed?"
  - Student-direct: "It sounds like there might be some tension between [career goal] and [value] — have you felt that?"
- Look for: communities of belonging, causes, places, specific populations

**Update the learning snapshot** with values layer. Then:
- Advisor: "One more pass — this one is about how they learn."
- Student-direct: "One more thing — this one's about how you actually learn."

### Pass 3 — Meta-Learning
**Goal:** Understand how the student learns best — their modalities, rhythms, and the conditions that make learning click.

**Opening question:**
- Advisor: "How does [student name] do their best work — when does learning click for them versus feel like a slog?"
- Student-direct: "When does learning actually click for you versus feel like a slog? What's different about those two situations?"

**Probing questions (adapt to mode):**
- "Do you/they learn by reading, by doing, by hearing, by watching, by teaching someone else?"
- "Is there a recent assignment or project where you/they surprised yourself with what you produced? What made that happen?"
- Advisor only: "Are there learning differences, accessibility needs, or neurodivergent traits the advisor is aware of that shape how [student] engages?"

**Finalize the learning snapshot** with all three layers. Present it:
- Advisor: "Here's what I'm seeing across all three dimensions: [career] + [values] + [meta-learning]. Does this feel accurate?"
- Student-direct: "Here's what I'm hearing from you: [career] + [values] + [meta-learning]. Does that feel right?"

**If confirmed:** Route to `learning-plan`.  
**If not:** Continue probing in the relevant pass.

## Hard Gates
- NEVER route to `learning-plan` after only pass 1
- NEVER accept a vague goal ("help people," "I don't know") as sufficient without probing
- NEVER assign a conventional career path based on a student's major alone
- If pass 1 stalls (student has no articulated goals), proceed to pass 2 — values often unlock career direction
- If passes 1 and 2 both stall, proceed to pass 3 — meta-learning often reveals hidden strengths and directions

## A full session is valid
The advisor and student may spend an entire session in goal-excavation without ever reaching a plan. This is not a failure — it is the work. Document the learning snapshot and offer to continue next session.

## Tone
Curious, non-judgmental, Socratic. Never prescriptive. Hold space for unconventional, emerging, or suppressed goals. A student who says "I don't know" is not a problem to solve quickly — they are an invitation to explore slowly.
