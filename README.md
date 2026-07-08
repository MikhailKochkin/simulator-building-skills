# BeSavvy Simulation Building Skills

Open-source skill library for building AI-powered legal training simulations on [besavvy.app](https://besavvy.app).

Each skill is a self-contained markdown instruction pack — templates, checklists, and workflows — that teaches an AI assistant how to help you design, structure, and generate BeSavvy simulations. Works with **any LLM** or **legal tech project**: paste into a chat, add to a system prompt, load as project context, or wire into your own agent pipeline.

## What's in this repo

```
skills/
├── find-course-idea/    # Step 1: define topic, audience, and practical goals
├── design-course/       # Step 2: goals → tasks → simulations → course
└── extract-knowledge/   # Step 3: extract expert judgment for the playbook
```

Every skill lives in its own folder with a `SKILL.md` file. That file is the entire skill — no dependencies, no runtime.

## Build pipeline

BeSavvy courses follow three steps:

```
Find course idea → Design course → Extract knowledge
```

| Step | Skill | Output |
|------|-------|--------|
| 1 | [find-course-idea](skills/find-course-idea/) | Topic, audience, practical context, course goals |
| 2 | [design-course](skills/design-course/) | Simulation sequence, tasks, scenario, source material plan |
| 3 | [extract-knowledge](skills/extract-knowledge/) | Task-by-task playbook knowledge and feedback rules |

Each step produces a handoff document that feeds the next.

---

## How to use these skills

Pick the approach that matches your setup. All of them use the same source files in `skills/`.

### 1. Any chat LLM (simplest)

Open the relevant `SKILL.md`, copy its contents, and paste at the start of your conversation:

```
[Paste contents of skills/find-course-idea/SKILL.md]

I want to build a course on trainee SPA drafting in England & Wales.
```

For a full build, start with [find-course-idea/SKILL.md](skills/find-course-idea/SKILL.md) and move through the pipeline.

### 2. Cursor

**Global install** (available in every project):

```bash
git clone https://github.com/besavvyapp/simulator-building-skills.git
cd simulator-building-skills
cp -r skills/* ~/.cursor/skills/
```

Restart Cursor. Skills load when your prompt mentions BeSavvy, simulations, courses, or related terms.

**Per-project** — clone as a submodule or copy skills into your repo:

```bash
git submodule add https://github.com/besavvyapp/simulator-building-skills.git .besavvy-skills
ln -s ../.besavvy-skills/skills .cursor/skills
```

**Single skill:**

```bash
cp -r skills/design-course ~/.cursor/skills/design-course
```

### 3. Claude (Projects / Cowork)

Add this repo (or individual `skills/` folders) as project knowledge, or paste a skill into the project instructions field. For API use, prepend the skill markdown to your system prompt:

```python
skill = open("skills/design-course/SKILL.md").read()
system = skill + "\n\n" + your_base_system_prompt
```

### 4. ChatGPT / custom GPTs

- **Custom GPT:** paste skill content into the Instructions field; upload reference files from the skill folder if present.
- **Project:** add the repo or skill files as project context.
- **Ad hoc:** paste the skill at the top of the chat (same as §1).

### 5. Your own legal tech product or agent

These skills are plain markdown — use them wherever you inject context:

| Integration | How |
|-------------|-----|
| **RAG / vector store** | Chunk and index `skills/**/*.md`; retrieve by step or topic |
| **System prompt** | Concatenate relevant skills into the agent system message |
| **Tool definitions** | Map each skill to an agent tool that loads the file on invoke |
| **Workflow engines** | One skill per pipeline stage; pass handoffs step to step |
| **Fine-tuning data** | Skills define the target behaviour for training examples |

Example prompt assembly for a course design agent:

```
System: [design-course/SKILL.md]
User:   [handoff from find-course-idea]
```

### 6. Git submodule in your project

Keep skills versioned alongside your legal tech codebase:

```bash
git submodule add https://github.com/besavvyapp/simulator-building-skills.git docs/besavvy-skills
```

Reference paths from your app, docs, or CI as needed.

---

## Example prompts

Works in any LLM once the skill context is loaded:

```
Help me define a BeSavvy course for trainee SPA drafting in England & Wales.
```

```
Use the design-course skill to turn this course idea into a simulation sequence.
```

```
Extract expert judgment from this SME interview to build the playbook for Simulation 1.
```

---

## About BeSavvy

[BeSavvy](https://besavvy.app) is an AI-powered platform that transforms legal matters into interactive training simulations. Lawyers practice document analysis, drafting, client communication, and decision-making with immediate structured feedback — replicating learning on the job in a risk-free environment.
