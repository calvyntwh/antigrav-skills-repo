# Antigravity Skills Repo

This repository serves as a catalog of specialized skills for the Antigravity Agentic System. It includes both core custom skills and a collection of reference skills.

## 🧠 Core Skills

These skills are located in `.agent/skills/` and are designed to enhance the agent's reasoning and operational capabilities.

| Skill | Description |
|-------|-------------|
| **[create_new_skill](.agent/skills/create-new-skill/SKILL.md)** | Specialized skill for creating new Antigravity agent skills. Follows a Research -> Create -> Deploy workflow where the Agent directly creates the necessary files. |
| **[first-principles-thinking](.agent/skills/first-principles-thinking/SKILL.md)** | A mental model for breaking down basic truths to generate original solutions. Use for innovation, novel problems, or when stuck in conventional thinking. |
| **[inversion-thinking](.agent/skills/inversion-thinking/SKILL.md)** | Proactive failure analysis using the Saboteur Method. |
| **[map-vs-territory](.agent/skills/map-vs-territory/SKILL.md)** | Empiricism and Reality Checking. Prioritizing runtime truth over documentation. |
| **[occams-razor](.agent/skills/occams-razor/SKILL.md)** | Complexity Pruning and Simplification using the Subtraction Method. |
| **[pareto-principle](.agent/skills/pareto-principle/SKILL.md)** | Strategic Prioritization using the 80/20 Rule. Optimization of Scope. |
| **[systems-thinking](.agent/skills/systems-thinking/SKILL.md)** | Architectural analysis using Feedback Loops and System Dynamics. |

## 🚀 Usage

To use a skill:
1.  Ensure the `.agent/skills/` directory is accessible to your agent context.
2.  The Antigravity system automatically indexes valid skills found in this directory.
3.  Refer to the specific `SKILL.md` file for instructions on invoking and utilizing each skill.
