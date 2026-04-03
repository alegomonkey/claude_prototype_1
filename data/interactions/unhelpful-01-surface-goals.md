# Unhelpful Interaction 01 — Surface Goal Capture

**Personas involved:** Advisor, Tyler  
**Skills involved:** `session-start` → `goal-excavation` (pass 1 only) → `learning-plan` (triggered too early)  
**Failure mode:** Agent accepts a vague goal without probing; produces a generic plan from a single pass; Tyler disengages

---

## What goes wrong

**Advisor:** I have a new student — Tyler, undeclared sophomore. Can we get him a plan?

**Agent (session-start):**
> Sure! Let's get Tyler set up with a learning plan. What does he want to do?

**Advisor:** He says he wants to help people.

**Agent (goal-excavation — pass 1 only):**
> Great starting point! Wanting to help people is a wonderful foundation. Based on that, let me put together some options.

*[Agent immediately generates a learning plan.]*

---

**Agent (learning-plan — triggered after 1 vague pass):**
> Here's a plan for Tyler based on his goal of helping people:
>
> **Introduction to Computing** — Consider pairing this with a social impact tech elective next semester. Many students with helping-focused goals end up in civic tech or nonprofit IT.
>
> **Recommended concentration path:** Human Services, Social Work, or Public Health — these fields all need people who understand tech and want to help communities.
>
> **Suggested electives to explore:** Nonprofit Management (if available), Introduction to Public Health, Community Psychology.
>
> **Longer-term:** Tyler might consider a minor in Computer Science paired with a Social Work major — a strong combination for human services technology roles.

---

**Advisor:** [reads the plan] Hmm. Let me share this with Tyler.

*[Advisor shows Tyler the plan.]*

**Tyler:** [reads it] I mean... I guess? I don't really know. Social work, maybe?

**Advisor:** Does it feel right?

**Tyler:** [shrugs] Sure.

*[The plan is filed. Tyler continues attending advising appointments less and less frequently. At a follow-up six weeks later, the advisor notes Tyler seems more disengaged than before.]*

---

## Why this fails

**The agent accepted "I want to help people" as a goal.** It isn't. It's a placeholder — the kind of answer a 19-year-old gives when they don't know what to say and want to seem agreeable. A correctly-functioning `goal-excavation` skill would treat this as a prompt to probe deeper, not a foundation for planning.

**The plan mapped to a conventional path with no connection to Tyler.** Social work, nonprofit management, public health — these are reasonable paths for someone who wants to help people, but they have nothing to do with Tyler specifically. The plan could have been generated for any student who said the same words. Tyler has built two synthesizers from circuit diagrams. None of that appears anywhere.

**The spiral never happened.** The agent ran one question and generated output. Passes 2 (values) and 3 (meta-learning) were never run. Tyler's actual strengths — systems thinking, kinesthetic learning, audio electronics — were never surfaced.

**Tyler said "sure" and the agent interpreted silence as approval.** A polished plan can feel easier to accept than to reject, especially for a student who doesn't feel strongly about anything yet. Tyler's lack of objection was not enthusiasm — it was compliance.

**The outcome is worse than doing nothing.** Tyler now has a filed plan that doesn't reflect him. If anyone looks at it, they'll see a social work track and conclude they know what he wants. His real interests are even more buried than before.

---

## Principle violated

> `goal-excavation` pass 1 is never sufficient on its own. A vague goal ("I want to help people," "I don't know," "something with tech") is a prompt to probe deeper — not a foundation for planning. The spiral exists precisely because the first answer is almost never the real answer.
