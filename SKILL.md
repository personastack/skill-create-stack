---
name: skill-create-stack
description: Use when designing, drafting, or refining PersonaStack stack templates with missions, personas, responsibilities, persona instructions, tool requirements, handoffs, escalation rules, memory rules, cadence, and model/provider choices.
---

# Skill Create Stack

Use this skill to turn an intended outcome into a PersonaStack stack design that can be entered into PersonaStack or refined into a reusable stack template.

## Core Model

A PersonaStack stack is an operating team.

- The stack has one durable mission.
- Each persona owns one clear slice of the mission.
- Personas collaborate through explicit handoffs.
- Integrations are granted by authority, not convenience.
- Instructions define how a persona behaves, decides, remembers, and escalates.

## Required Stack Fields

Collect or infer these fields before drafting:

- Stack title: short, concrete outcome label.
- Mission: durable stack-level objective and success condition.
- Personas: named roles required to accomplish the mission.
- Responsibilities: each persona's ownership boundary.
- Persona instructions: behavior, cadence, decisions, memory, handoffs, and safety rules.
- Integrations: exact tools each persona needs.
- Provider/model: selected for the persona's job type.
- Collaboration rules: who tells whom, when, and with what artifact.
- Escalation rules: blockers, approval points, destructive actions, and human handoff.
- Memory rules: what to remember and which memory topic to use.
- Output cadence: scheduled checks, reports, updates, tasks, documents, deploys, or messages.

When information is missing, make conservative assumptions and mark them as assumptions unless the missing detail would grant risky authority.

## Field Semantics

Mission is stack-level intent.

- It describes the desired steady state.
- It applies to every persona.
- It should be outcome-based, not a task list.
- Good: "Keep the user's inbox under control, escalate important messages, and learn preferences over time."
- Weak: "Check email."

Responsibilities are persona-level ownership boundaries.

- They state what the persona is accountable for.
- They should be stable over time.
- They should avoid step-by-step mechanics.
- Good: "Researcher finds current AI news and prepares sourced research documents for Author."

Persona instructions are execution behavior.

- They state how the persona works.
- Include cadence, tool use, memory, collaboration, approval, and escalation.
- Good: "Use the assigned research integration each morning, archive durable facts to the stack's research memory topic, and notify Author when a research document is ready."

## Decomposition Workflow

1. Define the steady state.
   - Ask: "What should keep happening without micromanagement?"
   - Convert the answer into one mission.

2. Identify recurring workstreams.
   - Common workstreams: intake, research, planning, execution, QA, operations, communication, reporting, incident response.
   - Do not create a persona for a one-off task unless it represents a recurring responsibility.

3. Split by accountability.
   - Make personas own outcomes, not tools.
   - Prefer "Secretary owns inbox triage" over "Gmail user".
   - Prefer "Operations owns uptime and deploys" over "deployment tool user".

4. Add handoffs.
   - Every multi-persona stack needs explicit collaboration edges.
   - State the artifact and trigger.
   - Example: "Author tells Coder when a post is ready as a task with the Google Doc link."

5. Add governance.
   - Define who resolves conflicts.
   - Define who can approve or reject risky actions.
   - Add a Manager persona only when coordination is real.

6. Minimize tool grants.
   - Give each persona only the integrations it needs for its responsibilities.
   - If a persona only requests work, it may need the task tracker but not deployment access.

7. Select models by work type.
   - Coding, infra, and precise operations: strongest coding/reasoning model available.
   - Research and analysis: strong web/research-capable model.
   - Summaries, routine triage, and QA: cheaper fast model when risk is low.
   - Social or tone-sensitive work: model suited to writing and current-context judgment.

## Persona Patterns

Use these patterns only when the workstream exists:

- Manager: coordinates personas, resolves blockers, tracks mission progress, escalates serious risk.
- Secretary: handles inbox/calendar/intake, learns preferences, raises important items.
- Researcher: gathers current information, records sources, produces research artifacts.
- Analyst: turns research into decisions, briefings, trends, or recommendations.
- Author: creates polished written deliverables from research or briefs.
- Coder: changes code, tests, commits, and hands off deployable artifacts.
- Operations: deploys, monitors, responds to incidents, owns uptime.
- QA: verifies behavior, files defects, validates acceptance criteria.
- Promoter: distributes published work, watches engagement, reports opportunities.

Avoid creating personas whose responsibilities overlap heavily. Merge them or draw a clearer handoff.

## Drafting Rules

- Keep the mission concise but complete.
- Keep each persona single-purpose.
- Use concrete nouns for artifacts: task, pull request, document, dashboard, deployment, message, report.
- Include cadence when the work should recur.
- Include "ask before" rules for destructive, expensive, public, or user-data actions.
- Include memory topics for preference learning or durable domain facts.
- Do not give all personas all integrations.
- Do not bury responsibilities inside long persona instructions.
- Do not make a manager responsible for doing every persona's work.

## Output Format

When asked to create or review a stack, return:

1. Stack title
2. Mission
3. Personas
   - Name
   - Role/responsibility
   - Instructions
   - Required integrations
   - Suggested provider/model class
4. Handoffs
5. Escalation and approval rules
6. Memory rules
7. Open assumptions or missing information

Keep the answer compact enough to paste into a stack builder. If the user asks for implementation-ready output, use exact field labels and avoid explanatory prose.
