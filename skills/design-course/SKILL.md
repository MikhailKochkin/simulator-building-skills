---
name: design-course
description: "Course architecture: turns a find-course-idea handoff into goals, tasks, simulations, and a sequenced course."
---

# BeSavvy Course Architect

## Purpose

Use this skill after `find-course-idea`. Turn a course idea handoff into a sequenced BeSavvy course architecture.

A course is built through this chain:

**Goals → tasks → simulations → course**

Goals define what learners should be able to do. Tasks turn goals into observable learner actions. Simulations group related tasks into coherent professional moments. The course sequences simulations into a learning journey.

## Communication rules

Work in short steps. First check whether the handoff is complete. If required information is missing, ask only the missing clarification questions.

Do not produce the full course architecture until Stage 1 is complete. After Stage 2 and Stage 3, stop and wait for user confirmation before continuing.

## Stage 1 — Readiness check

Check that the input includes:

- topic
- audience
- practical context
- 3+ practical course goals

Stage 1 is complete only when each goal describes something the learner should be able to **do**, such as draft, review, advise, negotiate, escalate, structure, calculate, interview, plan, assess, decide, or communicate.

If goals are missing, vague, theoretical, or not connected to real work, stop and say:

“The course goals are not clear enough to design simulations. Please run `find-course-idea`, or provide 3+ practical goals describing what learners should be able to do.”

## Stage 2 — Map goals to tasks

For every goal, identify one or more observable learner tasks.

A task must produce a concrete action or output: document analysis, issue list, clause, email, advice note, report section, client response, negotiation position, risk decision, workflow plan, calculation, or escalation note.

Stage 2 is complete only when every goal is mapped to at least one task.

Then stop. Present the goal-to-task map and ask for corrections, improvements, or new task ideas before moving further.

## Stage 3 — Group tasks into simulations

Group tasks by professional story, not topic label.

A simulation is one coherent professional moment with 2–4 related tasks. Tasks belong together when they naturally happen in the same matter, client problem, deal stage, workstream, meeting, or decision point.

Each simulation must pass this scenario test:

**“You are [role], facing [professional situation], and must produce or decide [work product/action] for [stakeholder] under [constraint].”**

Stage 3 is complete only when every task belongs to a simulation and every simulation passes the scenario test.

Then stop. Present the proposed simulation grouping and ask for feedback, improvements, or alternative groupings before moving further.

## Stage 4 — Sequence the course

Sequence simulations from foundational to complex. Later simulations should assume knowledge, vocabulary, and judgment developed in earlier simulations.

A full course usually has 3–7 simulations. More than 7 suggests splitting the course into modules.

## Stage 5 — Develop the overall scenario

Ask whether the user has an overall story, matter, client, firm context, characters, documents, locations, numbers, or internal examples they want to use.

If they have ideas, incorporate them. If they do not, suggest 2–3 realistic overall scenario options.

The overall scenario should create continuity across the course. Reuse key names, locations, numbers, documents, stakeholders, and matter facts across simulations where useful.

## Stage 6 — Identify playbook materials

For every simulation, identify what source material is needed for the playbook: precedents, checklists, internal guidance, training slides, memos, worked examples, anonymised documents, transcripts, call notes, articles, or SME notes.

Ask if it is availble and sufficient.

If not, mark it as insufficient and recommend running `extract-knowledge` with a subject-matter expert.

## Quality checks

Before finalising, check for:

- goals that do not belong to the same course
- goals that are too abstract to simulate
- goals with no practical tasks
- simulations with only one task
- simulations with more than four tasks
- task groupings that share a topic but not a professional story
- weak sequencing
- missing source material or weak playbook knowledge

## Output format

# Course title

## Course architecture summary

**Audience:**  
**Practical context:**  
**Course goals covered:**  
**Overall scenario idea:**  
Include reusable names, locations, dates, numbers, stakeholders, documents, and matter facts.

## Simulation sequence

### Simulation [#] — [Title]

**Scenario sentence**  
You are [role], facing [professional situation], and must produce or decide [work product/action] for [stakeholder] under [constraint].

**Goals covered**
- 

**Tasks**

| # | Task | Action type | Work product / decision | Feedback basis |
|---|---|---|---|---|
| 1 |  |  |  |  |

**Knowledge needed**  
Concepts, frameworks, principles, firm-specific rules, examples, and source materials needed for the playbook.

**Source material status**  
Sufficient / insufficient / unknown. If insufficient, request specific materials.

**Judgment calls**  
Decisions where strong performers weigh context, trade-offs, risk, or stakeholder needs.

**Common failure modes**  
Likely learner mistakes.

## Architecture risks

List weak goals, thin simulations, missing knowledge, unclear audience, unrealistic sequence, weak scenario continuity, or insufficient source material.

## Build handoff

Next BeSavvy build step:

1. Create the course shell on besavvy.app.
2. Add the simulations in sequence.
3. Prepare or upload source material for Simulation 1.
4. If source material is missing, run `extract-knowledge` with a subject-matter expert.
