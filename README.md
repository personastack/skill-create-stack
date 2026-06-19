# skill-create-stack

`skill-create-stack` is an agent skill for designing PersonaStack stack templates for `my.personastack.ai`.

Use it when you want to turn an outcome into a complete stack design with:

- a clear stack mission
- focused personas
- persona responsibilities
- persona instructions
- required integrations
- handoffs between personas
- escalation and approval rules
- memory and cadence guidance

## Install

```sh
npx skills add personastack/skill-create-stack
```

To install the individual skill explicitly:

```sh
npx skills add personastack/skill-create-stack --skill skill-create-stack
```

## Use

Invoke the skill in Codex, Claude Code, or another compatible agent:

```text
Use $skill-create-stack to design a PersonaStack stack for managing my inbox and calendar on my.personastack.ai.
```

The skill is meant to produce stack-builder-ready content: title, mission, personas, responsibilities, instructions, integrations, handoffs, escalation rules, and assumptions.

## Target Platform

This skill is specifically written for creating stacks on `my.personastack.ai`, where a stack is a mission-driven team of personas with tool access, responsibilities, and collaboration rules.
