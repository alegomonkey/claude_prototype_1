# Unhelpful Interaction 02 — Institutional Blindness

**Personas involved:** Advisor, Amara  
**Skills involved:** `session-start` → `goal-excavation` (3 passes, done correctly) → `learning-plan` → `faculty-translation` (fails to check constraints)  
**Failure mode:** Agent proposes an alternative that bypasses an institutional constraint it never checked; plan collapses at the faculty meeting; student is disappointed and trust is damaged

---

## What goes wrong

*Note: The goal-excavation portion of this session goes correctly — all three passes, Amara's real goals are surfaced. The failure happens in `learning-plan` and `faculty-translation`.*

---

**[Goal-excavation completes correctly. Learning snapshot established: community-facing tech, food justice, builds for real people, learns by doing.]*

---

**Agent (learning-plan):**
> Here's the plan for Amara. I'll cover all three of her current courses.

---

> **Systems Programming**
> - Standard objective: OS-level concepts — memory management, concurrency, file I/O; assessed via midterm exam
> - Proposed alternative: **Replace the midterm exam** with a "community code review event" — Amara presents her pantry inventory system to real pantry staff and volunteers, demonstrating her command of the systems concepts through a live application
>
> This is more authentic, more meaningful to Amara, and demonstrates the same OS competencies in a real context.

---

**Advisor:** That sounds amazing. Amara will love this.

**Agent:**
> I think she will. Let me put together the faculty translation for the Systems Programming instructor.

---

**Agent (faculty-translation — skips constraint check):**
> Here's how to frame the midterm alternative for the Systems Programming instructor:
>
> "Amara has been working on a community inventory system for a food pantry. We'd like to propose that she demonstrate her command of the Systems Programming concepts — concurrency, file I/O, memory management — through a live code review with real users rather than a written exam. The learning objectives are identical; the evidence of competency is more authentic and applied."
>
> This is a strong pitch — instructors often respond well to real-world application framing.

---

**Advisor:** This is great. I'll take it to the instructor next week.

*[Advisor brings the proposal to the Systems Programming instructor and the department chair.]*

---

**Department Chair:** I appreciate the creativity here, but Systems Programming is an ABET-accredited course. The midterm exam assesses specific competencies that our accreditation requires us to evaluate in a standardized, individually-proctored format. We can't substitute a community event for that — it would put our program accreditation at risk.

**Instructor:** I'm sorry — I would have loved to say yes. I don't have the authority to change the midterm format even if I wanted to.

---

*[Advisor returns to Amara to explain that the plan won't work as proposed. Amara, who had been excited about the pantry system as her midterm, is visibly disappointed.]*

**Amara:** So the plan isn't actually possible?

**Advisor:** Part of it isn't. The midterm has to stay as a midterm.

**Amara:** [quietly] Then why did we spend all that time on it?

---

## Why this fails

**The agent never ran the constraint check.** The `faculty-translation` skill contains an explicit checklist that must be completed before any alternative is framed as viable. Item 1 on that checklist: "Does this course have accreditation or licensure constraints on assessment format?" The agent skipped it entirely.

**ABET accreditation of CS programs is not obscure.** It's a well-known institutional reality in CS departments. A correctly-functioning `faculty-translation` skill would have flagged this as a likely constraint to verify before building any expectation around changing the midterm format.

**The damage is to Amara, not the advisor.** Amara got excited about a possibility that turned out not to exist. That disappointment is not neutral — it can make a student feel that the advising process is naive or that the institution doesn't actually care about her goals. Trust is harder to rebuild than it is to protect.

**Polished output is not the same as viable output.** The faculty translation sounded compelling. It wasn't wrong about the pedagogical argument. It was wrong about what the institution would allow — and the agent had no idea because it never asked.

---

## Principle violated

> `faculty-translation` must always run the institutional constraint checklist before framing any alternative as viable. An alternative that fails at the faculty meeting is worse than no alternative — it raises and then dashes student expectations. Check constraints first, not after.
