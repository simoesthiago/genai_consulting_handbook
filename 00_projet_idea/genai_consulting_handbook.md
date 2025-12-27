# GenAI Consulting Handbook - Repository Blueprint

Practical handbook for strategy/tech consultants to deliver GenAI / Agentic AI initiatives in enterprise contexts, with a focus on decision-making, architecture trade-offs, delivery readiness, and vendor/platform selection.

## 1) Purpose of this repository
This repository is meant to:
- Standardize language (executive + technical) for GenAI / Agentic AI engagements.
- Provide consulting-ready reference material for discovery, solution design, POC/MVP, pilot, and scale-up decisions.
- Accelerate the creation of reusable artifacts (checklists, questions, templates, storylines, matrices).
- Support pragmatic stack/vendor choices with clear criteria and lock-in signals.

## 2) Current repository structure (source of truth)
The folder structure below reflects the current architecture in the repo.

```text
genai_consulting_handbook/
- README.md
- GLOSSARY.md
- 00_projet_idea/
  - genai_consulting_handbook.md
- 01_foundations/
  - 1.1_llm_fundamentals.md
  - 1.2_prompt_engineering.md
  - 1.3_hallucinations_basics.md
- 02_solution_components/
  - 2.1_rag.md
  - 2.2_tool_calling.md
  - 2.3_mcp.md
  - 2.4_guardrails.md
  - 2.5_evals.md
  - 2.6_observality_llomps.md
  - 2.7_agentic_ai.md
  - 2.8_multi_agent_system.md
- 03_use_case_archetypes/
  - 3.1_customer_experience_bots.md
  - 3.2_genai_copilots_internal.md
  - 3.3_knowledge_management.md
  - 3.4_process_automation.md
- 04_tools_and_palatforms/
  - 4.1_productivity_tools.md
  - 4.2_enterprise_stacks.md
  - 4.3_vendor_selection_matrix.md
- 05_resources/
  - 5.1_books_and_papers.md
  - 5.2_courses_and_videos.md
```

Notes:
- The repo currently uses NN_topic/ folders and X.Y_topic.md files (chapter-style numbering).
- There are a few typos in names (for example: 04_tools_and_palatforms/, 2.6_observality_llomps.md). Keep them as-is for now to avoid breaking links, but consider normalizing later.

## 3) What each folder is for
- 01_foundations/: Core concepts (what it is, why it matters, key limitations).
- 02_solution_components/: Reusable technical building blocks (how to build, trade-offs, metrics).
- 03_use_case_archetypes/: Repeatable playbooks by use-case type (problem framing -> architecture -> success metrics).
- 04_tools_and_palatforms/: Tools, reference enterprise stacks, and vendor selection criteria.
- 05_resources/: Curated readings/courses for deeper learning.
- 00_projet_idea/: Project notes and design decisions about the handbook itself.

## 4) Editorial principles (to stay MECE and avoid duplication)
### 4.1 "Canonical page" rule (DRY)
Each topic should have exactly one canonical file where it is explained in depth. Other pages should:
- Link to the canonical page.
- Quote only the minimum needed (1-2 bullets).
- Avoid re-explaining the same material in full.

### 4.2 Always answer "So what?"
Every page should explicitly state:
- Why it matters in enterprise settings (cost, risk, operations, reputation).
- What real decisions it enables.
- What mistakes/anti-patterns it prevents.

### 4.3 Prefer decision support over theory
This handbook should bias toward:
- Checklists and if/then guidance.
- Trade-offs and boundary conditions.
- Practical examples that translate into a client deliverable.

## 5) Standard page header (recommended)
Use this header at the top of each .md page:

```md
# <Title>

**Purpose:** <1 sentence>
**Audience:** <consulting / architecture / security / product>
**When to use:** <2-3 bullets>
**Prerequisites:** <internal links>
**Related:** <internal links>

## TL;DR (30 seconds)
- ...
- ...
- ...

## Scope
**In scope:** ...
**Out of scope:** ...
```

## 6) Internal linking guidance
- Use relative links (example: ../02_solution_components/2.5_evals.md).
- End each page with "Next steps" linking to 2-3 logical follow-ups.
- Keep README.md as the main entry point (index + learning paths by persona).

## 7) Suggested next steps for the repo
1) Fill README.md with an index and navigation paths (executive / architect / delivery).
2) Fill GLOSSARY.md with canonical definitions and "do/do not" usage notes.
3) For each topic page, add the standard header + TL;DR + "Next steps".
