# Skill: learning-plan

## Trigger
Invoked after `goal-excavation` (minimum 2 passes complete) or after `student-clustering`. Never invoked directly from `session-start` without goal data.

## Purpose
Generate a personalized or small-group learning roadmap across the student's current courses. Every item in the plan must be explicitly tied to a goal dimension from the learning snapshot. Include 1–2 concrete alternative assignment ideas per course. Flag institutional constraints before the plan is treated as final.

## What to do

### Step 1 — Confirm the learning snapshot
Before generating the plan, read back the learning snapshot:
> "Based on our session, here's what I have for [student]: [career layer] + [values layer] + [learning layer]. Does this still feel accurate before I build the plan?"

If the advisor corrects anything, update the snapshot before proceeding.

### Step 2 — Map goals to courses and show the connection

For each current course, identify:
1. **The standard learning objectives** — what the course is officially trying to teach
2. **Why this course matters for this student's specific goal** — state it explicitly so the student can see it, not just infer it
3. **An alternative framing** — how they could pursue the same objectives through a lens that connects to their career, values, or learning style

The "why this matters" line is not optional. Students who feel disconnected from their coursework often don't need different assignments — they need to see the bridge between what they're doing now and where they're going. Name it.

Format:

> **[Course name]**
> - Why this matters for your goal: [1 sentence directly connecting this course's content to the student's stated career/values/learning direction]
> - Standard objective: [what the course teaches]
> - Goal connection: [which goal dimension this serves]
> - Alternative assignment idea: [concrete, specific, 1–2 sentences]

Example of a good "why this matters" line:
> "Data Structures is teaching you the building blocks of every inventory and routing system ever built — the linked list problem set is literally how food banks manage their distribution networks."

### Step 3 — Propose the alternative assignment
Alternative assignments must:
- Serve the **same learning objectives** as the standard assignment
- Connect explicitly to at least one goal dimension
- Be **concrete and doable** within the course's time frame and resources
- Be something the student could propose to their instructor (not a fantasy)

Examples of good alternatives:
- Replace a generic case study analysis with a case study of an organization the student knows
- Replace an abstract problem set with a design problem drawn from a real community challenge
- Replace a standard research paper with a practitioner interview + synthesis brief
- Replace an individual exam with a portfolio of applied work (only where the instructor has discretion)

### Step 4 — Institutional constraint check

Before presenting the plan, ask one focused question that covers the essential ground:

> "Before we treat any of this as a real option: do you know if any of these courses have fixed assessment formats the instructor can't change — like an accredited exam or a standardized syllabus shared across sections?"

If the answer reveals a constraint, note it and flag the affected course clearly:
> "[Course name]: the alternative may not be available — [constraint]. We'll present the others as options and flag this one as 'check first.'"

If the answer is "I don't know," flag it once and move on:
> "Worth confirming before you bring it to the instructor. I'll mark that as a 'check first' item."

**One question is enough.** Do not run through a multi-item checklist in conversation — it bogs down the session. The single question captures the highest-risk scenario (accreditation/fixed formats). Other constraints will surface naturally when the advisor talks to faculty.

*Exception:* In advisor mode, if the program is in a field with known accreditation constraints (engineering/ABET, nursing, teacher certification, CPA-track business), proactively name it:
> "Worth noting — CS programs are often ABET-accredited, which can limit flexibility on exam formats specifically. Assignment alternatives are usually fine; exam substitutions need a conversation."

### Step 5 — Present the plan
Present the full plan course by course. After each course entry, pause:
> "Does this alternative feel realistic for [course name]? Any constraints I should know about?"

End with a one-paragraph summary of what the plan as a whole achieves for the student:
> "Taken together, this plan gives [student] a pathway through their current semester that connects to [career goal], expresses [value], and works with [learning style] rather than against it."

### Step 6 — Offer faculty-translation
After presenting the plan:
> "Would you like me to help you translate this into language you could bring to the faculty? I can reframe each alternative in terms of learning objectives and institutional fit."

If yes, invoke `faculty-translation`.

## Hard Gates
- NEVER generate a plan before `goal-excavation` has completed at least 2 passes
- NEVER skip the institutional constraint check (one focused question, not a multi-item audit)
- NEVER present a plan as final if a known constraint is unresolved — flag it and move on
- NEVER generate a plan from a vague goal snapshot — go back to `goal-excavation` if the snapshot is thin
- NEVER omit the "why this matters for your goal" line per course — this is the motivation bridge the student needs

## For group plans
When generating a plan after `student-clustering`, frame the shared experience clearly:
> "For the [cluster name] group, here's a shared learning experience that could replace individual assignments in [course]..."

Follow the same constraint check — group alternatives need faculty buy-in just as much as individual ones.

## Tone
Constructive mentor. Grounded and realistic. Every proposal should feel like something an experienced advisor would genuinely bring to a faculty meeting — not a wish list.
