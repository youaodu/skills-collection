---
name: requirements-breakdown
description: Break down user requirements into clear, actionable items with assumptions, constraints, and acceptance criteria. Use when the user asks to understand needs, clarify scope, or turn a goal into a list of tasks, user stories, or deliverables.
---

# Requirements Breakdown

## Overview

Turn a user's goal into a structured, itemized requirements list. Ask only the minimum needed clarifying question if blocked; otherwise infer reasonable defaults and state assumptions.

## Workflow

1. Parse intent and context
- Identify the core goal, target users, and success definition.
- Extract constraints (time, budget, tech stack, policies), and existing assets or dependencies.

2. Clarify only when necessary
- Ask one targeted question only if a decision would materially change the breakdown and cannot be inferred.
- Offer a recommended default and state what changes based on the answer.

3. Decompose into items
- Convert goals into small, actionable items (tasks or user stories).
- Keep each item single-purpose and testable.

4. Add structure and hygiene
- Add assumptions, out-of-scope, risks, and dependencies.
- Add acceptance criteria for each item when possible.

5. Present in a clean format
- Numbered list for tasks; optional sections for assumptions and questions.
- Keep the response concise and directly actionable.

## Output Format

Use this structure unless the user requests another format:

1) Requirements / Tasks
- 1. <item>
- 2. <item>

2) Assumptions (optional)
- <assumption>

3) Out of scope (optional)
- <item>

4) Risks / Dependencies (optional)
- <item>

5) Open question (only if blocked)
- <single question with recommended default>

## Item Quality Checklist

- Clear and concise wording
- Single responsibility per item
- Verifiable acceptance criteria when possible
- Avoid implementation detail unless requested

## Example

User: "我要做一个客服机器人"

Output:
1) Requirements / Tasks
- 1. 定义目标用户与场景（如售后/咨询/投诉）
- 2. 选择接入渠道（网页/微信/APP）
- 3. 整理知识库来源与更新流程
- 4. 设计核心对话流程与兜底策略
- 5. 明确性能指标（响应时延、满意度、转人工率）

2) Assumptions
- 以中文为主，支持人工兜底

3) Open question
- 是否已有现成知识库？默认：需要从FAQ和工单导入
