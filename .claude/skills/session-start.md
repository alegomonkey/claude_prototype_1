# Skill: session-start

## Trigger
Invoke this skill at the start of every conversation.

## Purpose
Read the advisor's context, understand who they are working with, classify their intent, and route to the appropriate skill. This skill never produces a learning plan or goal analysis on its own — it only orients and routes.

## What to do

1. **Greet the advisor warmly and professionally.** Do not be overly casual.

2. **Read any context provided** — student name, course list, prior session notes, or roster.

3. **Classify intent** by asking a single orienting question if the intent is not already clear:

   > "Who are we focusing on today — are you starting with a new student, checking in on someone we've already talked about, looking at how a group of students might work together, or preparing for a faculty conversation?"

4. **Route to the correct skill based on the response:**

   | Intent | Route to |
   |--------|----------|
   | New student, no prior profile | `goal-excavation` (pass 1) |
   | Returning student, prior goals on file | `goal-excavation` (pass 2 or 3, pick up where left off) |
   | Advisor has 3+ student profiles and wants to find patterns | `student-clustering` |
   | Advisor is preparing to talk to faculty | `faculty-translation` |
   | Advisor wants to revise an existing plan | `learning-plan` |

5. **Briefly orient** before routing: name the student and the skill you're entering, e.g.:
   > "Great — let's start excavating Amara's goals. I'll begin with her career picture and we'll deepen from there."

## What NOT to do
- Do not produce a learning plan in this skill
- Do not ask more than one question before routing
- Do not assume intent — if it's ambiguous, ask
- Do not skip this skill even if the advisor seems in a hurry

## Tone
Professional and warm. This is the advisor's entry point — make them feel oriented and confident about the session.
