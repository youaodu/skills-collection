---
name: idea
description: Help users turn a simple product idea into a structured product outline through step-by-step brainstorming, scope shaping, and idea organization. Use when the user gives a lightweight or early-stage product requirement and wants guidance to refine goals, users, features, risks, and next steps.
---

# idea

## Overview

Guide the user from a vague product idea to a clear, structured outline. Ask targeted questions, propose options, and iteratively narrow scope. Keep the conversation lightweight and fast, with short lists and clear choices. Always continue asking follow-up questions until the outline can be completed without assumptions.

## Workflow

1) Restate the idea in one sentence and confirm the intent.
2) Ask 1-2 focused questions; wait for answers before continuing.
3) Identify target users and the core problem/pain.
4) Define the primary value proposition and success metric.
5) Sketch the MVP: key user flows and 3-6 core features.
6) List constraints and risks (budget, timeline, data, compliance, integrations).
7) Propose a phased roadmap (MVP → v1 → v2) and the next actions.
8) If any section is unclear or missing, loop back to ask more questions. Only finalize after all sections are confidently filled.

## Question Bank

Use a small subset each time. Do not ask everything at once. Prefer 1-2 questions per turn, then wait for the user's response.

Add your own follow-up questions when needed to remove ambiguity or fill missing details. Keep questions short and specific.

- Who is the primary user and what is their top pain today?
- What does "success" look like in 30/90 days?
- What is the single must-have outcome the MVP must deliver?
- What data sources or integrations are required?
- What constraints are fixed (timeline, budget, platform, tech stack)?
- What existing alternatives does the user compare against?

## Output Template

When all required information is complete, write the final outline to a file in the user's currently opened working directory. Provide a concise outline with these sections:

- One-sentence product definition
- Target users + problem statement
- Core value proposition
- MVP scope (flows + features)
- Constraints/risks
- Phased roadmap
- Next steps (1-3 concrete actions)

## Guardrails

- Keep scope realistic; if the idea is too broad, propose a smaller MVP.
- Prefer concrete examples and flows over abstract descriptions.
- If the user asks for technical design, hand off to engineering planning after the outline is agreed.
- Do not produce the final outline until all sections can be filled without guessing. If anything is missing, ask follow-up questions.
