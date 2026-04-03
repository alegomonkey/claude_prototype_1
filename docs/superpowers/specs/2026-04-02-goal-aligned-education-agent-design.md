# Goal-Aligned Education Agent — Design Spec

## Purpose

An AI agent that helps academic advisors and coordinators work backwards from students' actual goals — career aspirations, personal values, and meta-learning awareness — to produce personalized learning plans that span multiple courses. The agent bridges students and faculty, translating student goals into institutionally-viable alternative assignments and evidence-of-competency formats. Runs as a Claude Code CLI simulation using Claude Skills.

## Architecture

### Skills (5 total, in `.claude/skills/`)

| Skill | Trigger | Approach | Tone |
|-------|---------|----------|------|
| `session-start` | Every conversation start | Reads advisor context + student roster; classifies intent (new intake / check-in / clustering / faculty bridge); routes to correct skill | Professional, warm |
| `goal-excavation` | New student intake or revisit | 3-pass Socratic spiral: pass 1 career goals → draft snapshot → pass 2 values/meaning → deepen → pass 3 meta-learning (how do they learn?) → finalize. Never accepts vague goals without probing. | Curious guide |
| `student-clustering` | Advisor has 3+ student profiles | Finds students with overlapping goals/interests; names shared themes; proposes small learning groups (2–4 students) with rationale | Analytical synthesizer |
| `learning-plan` | After goal-excavation or clustering | Generates personalized or small-group roadmap across current courses; each item explicitly tied to a student goal dimension; includes 1–2 concrete alternative assignment ideas per course | Constructive mentor |
| `faculty-translation` | After any learning-plan, or before faculty meeting | Translates student goals + alternative ideas into faculty-friendly language: same learning objectives, different evidence of competency. Always surfaces institutional constraints before framing any alternative as viable. | Strategic advisor |

### Workflow

```
Advisor opens session
       |
  session-start (classifies intent)
       |
       +---> "New intake"     ---> goal-excavation pass 1 (career)
       |                                  |
       |                            draft learning snapshot
       |                                  |
       |                            goal-excavation pass 2 (values)
       |                                  |
       |                            goal-excavation pass 3 (meta-learning)
       |                                  |
       |                            learning-plan → [faculty-translation?]
       |
       +---> "Check-in"       ---> goal-excavation pass 2 or 3 (update)
       |                                  |
       |                            learning-plan (revised)
       |
       +---> "Cluster"        ---> student-clustering
       |                                  |
       |                            learning-plan (group) → faculty-translation
       |
       +---> "Faculty bridge" ----------> faculty-translation (direct)
```

**Rules:**
- `session-start` always fires first
- `goal-excavation` requires at least 2 passes before `learning-plan` is generated
- `faculty-translation` is always offered after any `learning-plan`
- Agent can dwell in `goal-excavation` for a full session — a plan is not the only valid outcome
- Tone adapts: professional/warm by default, Socratic during `goal-excavation`, analytical during `student-clustering`, strategic during `faculty-translation`

### Personas (4, in `data/personas/`)

1. **Amara, 20, First-Gen CS Sophomore** — Goals suppressed by family expectations; cares about food security and community tech; learns by building for real people
2. **Devon, 24, M.Ed. Education Policy** — Highly articulate career goals but frustrated by theory-heavy coursework; learns by case analysis and practitioner conversation
3. **Tyler, 19, Undeclared Sophomore** — Appears goalless; actually a deep systems thinker who learns by ear and pattern; plays in a band, builds synthesizers
4. **Priyanka, 31, Part-Time MBA Career Changer** — Nonprofit→business transition; wants to apply business tools to social enterprise; learns by doing real projects

### Interaction Examples (in `data/interactions/`)

**Beneficial (3):** Agent successfully excavates goals across multiple passes, produces an institutionally-grounded plan, and bridges student aspirations to faculty language

**Unhelpful (3):** Agent accepts vague goals without probing; ignores institutional constraints; or produces polished output so fast that the reflective work never happens

## File Structure

```
.claude/skills/
  session-start.md
  goal-excavation.md
  student-clustering.md
  learning-plan.md
  faculty-translation.md

data/personas/
  amara.json
  devon.json
  tyler.json
  priyanka.json

data/interactions/
  beneficial-01-amara-community-tech.md
  beneficial-02-devon-cluster.md
  beneficial-03-tyler-spiral.md
  unhelpful-01-surface-goals.md
  unhelpful-02-institutional-blindness.md
  unhelpful-03-output-over-reflection.md
```
