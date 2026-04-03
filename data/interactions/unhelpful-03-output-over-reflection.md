# Unhelpful Interaction 03 — Output Over Reflection

**Personas involved:** Advisor, Amara  
**Skills involved:** `session-start` → `goal-excavation` (pass 1 only) → `learning-plan` (triggered too early, polished output produced)  
**Failure mode:** Agent produces a well-formatted, impressive plan after a single pass; the advisor accepts it; three weeks later Amara says the plan doesn't feel like hers

---

## What goes wrong

**Advisor:** I have Amara again — sophomore CS student. She mentioned wanting to be a software engineer. Can we get her a plan?

**Agent (session-start):**
> Sure — let's build a plan for Amara.

---

**Agent (goal-excavation — pass 1 only):**
> Quick question before we start: what's Amara's career goal?

**Advisor:** Software engineer. She's pre-career, first-gen, parents are from Ghana.

**Agent:**
> Got it. Let me put together a learning plan that sets her up well for a software engineering career.

*[Agent immediately produces a plan without running pass 2 or pass 3.]*

---

**Agent (learning-plan):**
> **Personalized Learning Plan — Amara**
>
> **Goal:** Software engineer at a technology company
>
> ---
>
> **Data Structures**
> Amara should focus on mastering the standard DS topics — linked lists, trees, graphs, hash maps — as these appear directly in technical interviews. Recommend LeetCode practice starting in the spring.
>
> **Systems Programming**
> Strong OS fundamentals are essential for backend engineering roles. Recommend she aim for a high grade in this course and consider systems-focused electives (compilers, networking) next year.
>
> **Technical Writing**
> Clear technical documentation is a valued skill at software companies. Recommend standard completion of this course.
>
> **Recommended concentration:** Systems and Networks, or Software Engineering if available
>
> **3-year roadmap:**
> - Junior year: internship at a tech company, ideally mid-size or startup for broader experience
> - Senior year: capstone project in a systems domain; full-time recruiting in the fall
>
> **LinkedIn summary draft:**
> "Computer Science student at [University] with a focus on systems programming and software engineering. Passionate about building reliable, impactful software. Seeking internships in software development."

---

**Advisor:** [genuinely impressed] This is really thorough. Very professional.

**Agent:**
> Happy to help. This should give Amara a clear path through her CS program.

*[Advisor and Amara meet. Amara reads the plan. It is well-formatted and contains reasonable advice.]*

**Amara:** [looking at the plan] Yeah, this looks... fine.

**Advisor:** Is there anything you'd change?

**Amara:** I don't know. I guess this is what I'm supposed to do.

*[The plan is filed. Amara attends a recruiting workshop the following month. She is not excited about it. Three weeks after the session, the advisor checks in.]*

**Advisor:** How are you feeling about the plan?

**Amara:** Honestly? It just feels like more school. Like I'm doing what I'm supposed to do, not what I actually... I don't know. Never mind.

**Advisor:** What were you going to say?

**Amara:** My aunt's food pantry has this inventory system that's terrible. I've been thinking about building something better for her. But that's not really a software engineering thing, I guess.

---

## Why this fails

**The agent never asked who Amara is.** The plan is technically competent and completely generic. It could have been generated for any CS student with software engineering as a stated goal. There is no Amara in the plan — no community, no food pantry, no aunt, no neighborhood, no first-gen context, no learning style.

**Speed of output is not a quality signal.** The plan was produced quickly. It was polished. The advisor was impressed. None of that means the plan is good for Amara. A plan that reflects who Amara actually is requires passes 2 and 3 — which take time and careful questioning. There is no shortcut.

**The spiral exists for a reason.** Pass 1 gets the expected answer. Pass 2 gets the values. Pass 3 gets the learning style. The food pantry — Amara's real direction — lives in pass 2. It is invisible to a single-pass intake. A plan built on pass 1 alone will always be a generic plan.

**"This is what I'm supposed to do" is a warning sign, not acceptance.** Amara's lack of objection was resignation, not enthusiasm. A student who has genuinely seen themselves in a plan says something different. The agent had no way to know this because it never asked.

**The harm is invisible.** Unlike the institutional blindness failure, this one doesn't collapse dramatically at a faculty meeting. It just... sits there. Amara gets through the semester doing what she's supposed to do, not what she could be doing. The food pantry goes unbuilt. Amara graduates with a resume that looks like everyone else's and a sense that school was never really about her.

---

## Principle violated

> `goal-excavation` must complete at least 2 passes — ideally 3 — before `learning-plan` runs. The purpose of the spiral is not efficiency; it is accuracy. A fast plan built on a single vague answer is worse than no plan, because it forecloses the exploration that would have produced something real. The goal is not to file a document — it is to help the student understand themselves and find a path that's actually theirs.
