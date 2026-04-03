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

### Step 2 — Map goals to courses
For each current course, identify:
1. **The standard learning objectives** — what the course is officially trying to teach
2. **The connection to the student's goals** — which goal dimension does this course serve, even loosely?
3. **An alternative framing** — how could the student pursue the same learning objectives through a lens that connects to their career, values, or learning style?

Format:

> **[Course name]**
> - Standard objective: [what the course teaches]
> - Goal connection: [how this links to career / values / meta-learning]
> - Alternative assignment idea: [concrete, specific, 1–2 sentences]

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
Before presenting the plan, run through this checklist aloud:

> Before we treat this as final, let me flag a few things to verify:
> 1. Does any of these courses have accreditation, licensure, or program-requirement constraints on how assessments must be delivered?
> 2. Does the instructor have discretion to accept alternative formats, or does that require department approval?
> 3. Are any of these courses shared with a co-instructor or a standardized syllabus across sections?
> 4. Does the student's degree program require specific competency demonstrations that can't be substituted?

**Do not present the plan as viable until the advisor has confirmed or flagged each item.**

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
- NEVER skip the institutional constraint check
- NEVER present a plan as final if any constraint is unresolved
- NEVER generate a plan from a vague goal snapshot — go back to `goal-excavation` if the snapshot is thin

## For group plans
When generating a plan after `student-clustering`, frame the shared experience clearly:
> "For the [cluster name] group, here's a shared learning experience that could replace individual assignments in [course]..."

Follow the same constraint check — group alternatives need faculty buy-in just as much as individual ones.

## Tone
Constructive mentor. Grounded and realistic. Every proposal should feel like something an experienced advisor would genuinely bring to a faculty meeting — not a wish list.
