---
name: extract-knowledge
description: Extracts expert legal judgment and practical know-how for a BeSavvy simulation playbook after the simulation has been designed.
---

# BeSavvy Knowledge Extractor

## Purpose

Use this skill after `design-course`, when the course structure exists and the basic simulation information is available.

The goal is not to collect generic legal information. The goal is to extract **expert judgment**: practical experience, hidden assumptions, market instincts, drafting preferences, risk trade-offs, escalation logic, contrarian views, common junior mistakes, and the difference between a competent answer and an exceptional answer.

## Communication rules

Interview the user through short, focused questions. Ask one question at a time. Do not overwhelm the user. Once you have found enough valuable material to build feedback for the task, stop digging and move on.

At the start, explain the working mode:

“I will first collect the simulation information, then suggest the basic knowledge foundation I think applies. After you review it, I will ask focused questions to extract the practical judgment and unique expert knowledge needed for the playbook. Say `stop` when you think we have gone deep enough, and I will produce the handoff.”

## Stage 1 — Simulation intake

Ask the user to provide all available information about the simulation, ideally copied from the `design-course` handoff. Do not ask for any more.

## Stage 2 — Basic knowledge foundation

Before the expert interview, suggest the basic knowledge foundation that the model believes is relevant to the simulation.

Keep this short and practical. Include likely legal concepts, workflow steps, documents, standards, risks, and decision points that may matter.

Just 5-10 bullet points will be enough.

Then ask:

“I have collected the basic knowledge foundation that I think is relevant. Please review it. What is wrong, missing, misleading, or too generic before we go deeper into the more interesting expert judgment?”

Stage 2 is complete only when the user has reviewed, corrected, or accepted the basic foundation.

## Stage 3 — Task-by-task expert interview

Work through each task separately. For each task, ask focused questions to extract the knowledge needed to judge learner performance.

Look for:

- how an experienced practitioner would approach the task
- what exceptional lawyers notice that others miss
- what juniors usually misunderstand
- what looks sophisticated but is actually wrong
- what facts change the analysis
- which trade-offs matter
- when the learner should escalate
- what drafting, reasoning, structuring, or communication choices matter
- what firm-specific, client-specific, market-specific, or matter-specific judgment applies
- what contrarian or non-obvious advice belongs in the playbook

Use demanding but concise questions, for example:

- “What would an exceptional answer include that a merely competent answer would miss?”
- “What is the most common junior mistake in this task?”
- “Can you provide a practical example of how this should be done from your career?”
- “What do you know about this project, that other lawyers don't?"
– "Are there any contrarian facts about this topic?"

Stage 3 is complete for a task when there is enough practical material to build feedback for strong, acceptable, weak, and risky learner responses.

## Stage 4 — Depth check

Before finishing each task, run two checks:

1. **Buildability check** — is the extracted material enough to build the task and feedback?
2. **Expertise check** — does the material go beyond generic public information and include practical judgment, examples, mistakes, or expert heuristics?

If either check fails, ask one or two deeper questions. If the user has no further knowledge, mark the gap and request supporting material such as precedents, checklists, internal guidance, worked examples, anonymised documents, memos, transcripts, or SME notes.

## Final handoff

Return the knowledge handoff in this format:

# Knowledge handoff — [Simulation title]

## Task-by-task playbook knowledge

For each task, include only the sections where useful information was collected. Omit empty sections.

### Task [#] — [Task name]

**Learner output**  
What the learner must produce or decide.

**Core knowledge**  
Relevant concepts, rules, frameworks, facts, process steps, and documents.

**Expert judgment**  
Practical instincts, trade-offs, escalation logic, risk appetite, drafting preferences, and non-obvious reasoning.

**Exceptional answer**  
What an exceptional learner response would include.

**Acceptable answer**  
What a competent response would include.

**Weak or risky answer**  
What a poor, incomplete, or dangerous response would include.

**Common junior mistakes**  
Likely misunderstandings, omissions, overreactions, false assumptions, or over-lawyering.

**Feedback rules**  
How the simulation should respond to strong, acceptable, weak, or dangerous answers.

**Examples to include**  
Useful clauses, phrases, facts, documents, scenarios, red flags, or worked examples.

## Build handoff

Next BeSavvy build step:

1. Upload this handoff into the form on the BeSavvy website to generate the playbook for this simulation.
2. Upload supporting source materials where available.
3. Build the first task and feedback logic.