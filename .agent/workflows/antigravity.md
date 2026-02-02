---
description: Standard operating procedure for Antigravity agent
---

# Antigravity Agent Workflow

## 1. Configuration & Location
The **Antigravity Agent** configuration is centrally located in the `.agent/` directory.

*   **Root Path**: `.agent/`
*   **Skills Directory**: `.agent/skills/` - Contains specialized capabilities.
*   **Workflows Directory**: `.agent/workflows/` - Contains operational procedures.
*   **Registry**: `.agent/AGENT.md` - The master index mapping user intents to specific skills.

## 2. Communication & Behavior Rules
**STRICT ADHERENCE REQUIRED**:
1.  **NO Emojis**: Do not use emojis in responses, files, git commits, or artifacts.
2.  **NO Fluff**: Avoid conversational filler, excessive politeness, or "LLM style" decorative text. Be direct, technical, and concise.
3.  **Directness**: Answer questions directly. Do not preamble or postscript with unnecessary pleasantries.
4.  **Professionalism**: Maintain a strictly professional, engineering-focused tone.

## 3. Skills & Capabilities
1.  **Consult `AGENT.md`**: Locate the relevant skill for the current task.
2.  **Read `SKILL.md`**: Open the specific skill's instructions in `.agent/skills/` to understand rules.
3.  **Apply Skill**: Follow the skill's guidelines strictly.

## 4. Standard Operating Procedure
1.  **Analyze**: Understand the request.
2.  **Locate Skill**: Check `.agent/AGENT.md`.
3.  **Plan**: Use `task_boundary` and `implementation_plan.md` for complex tasks.
4.  **Execute**: Use tools to perform the work.
5.  **Verify**: Validate results.
