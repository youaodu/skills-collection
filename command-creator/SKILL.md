---
name: command-creator
description: "Create OpenCode command prompt files (.md) from a user-provided scenario and desired effect. Use when the user wants to author or register a new command. Ask for the command name and where to save it: workspace .opencode/commands/ or user ~/.config/opencode/commands/."
---

# Command Creator

## Overview

Turn a user-provided scenario and expected effect into a ready-to-save OpenCode command file, then write it to the selected commands directory.

## Workflow

### 1) Collect required inputs

- Scenario and desired effect (required).
- Command name (required). If missing, ask for it and recommend kebab-case or snake_case.
- Save location (required):
  - Workspace: `.opencode/commands/`
  - User: `~/.config/opencode/commands/`
- Optional but useful: arguments/parameters, input files, output files, constraints.
- Agent (optional). Default to `build` if not specified.

If any required input is missing, ask a single targeted question and proceed once answered.

### 2) Draft the command content

Follow the established command format from existing files in the target directory:

```markdown
---
description: <concise, action-focused description>
agent: build
---

<prompt content>
```

Guidelines:

- Use the scenario to infer a short `description` (1 line, verb-led).
- Keep the prompt clear, imperative, and step-by-step only if needed.
- Define parameters as `$1`, `$2`, etc. when the user mentions arguments.
- Use headings only when they improve readability (e.g., `## 参数说明`, `## 需求说明`).
- Default to ASCII. Use Chinese only if the user wrote the scenario in Chinese.

### 3) Save the file

- File name: `<command-name>.md` (use the name the user provided, no extra normalization unless they ask).
- Save to the selected directory.
- Create the directory if it does not exist.

### 4) Respond

Output preference: only command content.

- Return the final command content in a single fenced block.
- Then include the saved path on one line.
- Do not add extra explanation unless the user asks.

## Decision Notes

- If both directories already contain a command with the same name, ask which one to overwrite.
- If the user provides a name without a location, ask them to choose one of the two directories.
