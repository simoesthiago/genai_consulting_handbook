# RULE SET: USE CASE ARCHETYPES (03_USE_CASE_ARCHETYPES)

This file defines the writing standard for all pages under `03_use_case_archetypes/`.

It combines:
- the **content structure** and consulting assets from `00_projet_idea/use_case_archetype_playbook_template.md`, and
- the **style rules** (headings, bolding, 70/30 text vs bullets, tone) from `00_projet_idea/rule_set.md`.

The outcome we want: every archetype page reads like an end-to-end consulting playbook that helps a strategic audience **understand**, **decide**, and **deliver** a GenAI initiative.

---

# 1. NON-NEGOTIABLES (WHAT MUST ALWAYS BE TRUE)

## 1.1. Audience and voice

- Audience: strategy/tech consultants and enterprise stakeholders (business owners, product, architecture, risk/security, delivery).
- Voice: didactic, practical, confident-but-honest. Explain like you are onboarding a smart reader who is new to the archetype.
- Goal: enable decisions and delivery, not academic completeness.

## 1.2. Archetype pages are operational (not essays)

An archetype page must be usable in real delivery. That means it includes:

- a 2-minute "snapshot" (use-case card + TL;DR)
- an **as-is** and **to-be** workflow (step tables)
- explicit fit/anti-fit and readiness criteria
- a blueprint that maps to canonical solution components (links, not repetition)
- a delivery playbook with phase gates and acceptance criteria
- KPIs that map to decisions (go/no-go, scaling, autonomy expansion)
- reusable consulting assets (discovery questions, workshop agenda, demo script, templates)

If a reader cannot use the page to run a workshop or draft a delivery plan, the page is not done.

## 1.3. Keep pages DRY: link to canonical components

Archetype pages should **not** re-teach foundations or solution components. They should link to canonical pages and focus on what is archetype-specific.

Rules:

- Use `01_foundations/` for definitions and basics (what LLMs are, prompt injection, hallucinations).
- Use `02_solution_components/` for reusable building blocks (RAG, tool calling, guardrails, evals, observability, agentic).
- In the archetype, explain *why the component matters here* and *what decisions it changes*, then link.

## 1.4. Bullets vs continuous text (70/30)

- Target: ~70% continuous text, ~30% bullets/numbered lines (tables are allowed and encouraged when they clarify).
- Bullets are for: checklists, criteria, options, taxonomies, "do/don't".
- Continuous text is for: explanation, causality, trade-offs, and reasoning.

## 1.5. Bolding (strategic, not decorative)

Use bold to highlight what a consultant would underline in a review:

- **key claims**, **decision criteria**, **non-negotiables**, **risk language**, **go/no-go rules**, **P0 failures**

Rules:

- Do not bold entire paragraphs.
- Prefer 1-3 bold phrases per paragraph when needed.
- Bold terms on first introduction if they become recurring concepts.

## 1.6. Formatting conventions

- English only.
- Use plain ASCII quotes (`"`) not smart quotes.
- Use consistent hyphenation: "go/no-go", "end-to-end", "as-is", "to-be".
- Headings are numbered and consistent:
  - H1: `# X. TITLE IN CAPS`
  - H2: `## X.X. Title Case`
  - H3: `### X.X.X. Title Case`

---

# 2. STRUCTURE CONTRACT (REQUIRED SKELETON FOR 03_USE_CASE_ARCHETYPES)

Use this skeleton for every archetype page unless there is a strong reason not to.

## 2.1. Top matter (always present)

At the top of every archetype page:

```md
# <ARCHETYPE NAME IN CAPS> (USE CASE ARCHETYPE)

**Goal:** <1-2 lines, outcome-focused>

**Prerequisites:**
- [<link>](<link>) - <why it matters>

**Related:**
- [<link>](<link>) - <why it matters>

---
```

## 2.2. TL;DR and scope blocks (always present)

Immediately after the separator:

```md
# TL;DR (30 SECONDS)

<One short paragraph that can be read aloud in <30 seconds.>

- <3-8 bullets: the memory hooks>

## Use-Case Card (Snapshot)
| Item | Summary |
|---|---|
| Archetype definition | ... |
| What it replaces/augments | ... |
| Primary value drivers | ... |
| Primary solution pattern | RAG / tool calling / workflow+AI / agentic |
| Risk level | Low/Med/High - <why> |
| Typical stakeholders | ... |
| MVP timebox | ... |
| Primary KPIs | ... |

---

# WHAT'S IN / WHAT'S OUT

**In:** <1-3 lines>

**Out:** <1-3 lines>

---
```

Notes:

- The Use-Case Card is mandatory: it is the fastest way to align stakeholders.
- Keep KPIs few (3-6) and decision-relevant.

## 2.3. Main body (numbered H1 sections)

Use this recommended main layout (adapt H2/H3 as needed, but keep H1 stable):

1. `# 1. WHY IT MATTERS IN ENTERPRISE (VALUE AND DECISIONS)`  
2. `# 2. BUSINESS CONTEXT AND PAIN POINTS (AS-IS)`  
3. `# 3. TARGET STATE AND OPERATING RULES (TO-BE)`  
4. `# 4. DECISION GUIDE (FIT, ANTI-FIT, READINESS)`  
5. `# 5. SOLUTION BLUEPRINT (ARCHITECTURE + CONTROLS)`  
6. `# 6. DELIVERY AND ACCEPTANCE (POC -> PILOT -> SCALE)`  
7. `# 7. CASE STUDY: <ARCHETYPE> IN ENTERPRISE`  
8. `# 8. NEXT STEPS`

## 2.4. Canonical tables (mandatory)

Every archetype page must include these tables:

1. As-is step table:

```md
## <X.X>. AS-IS STEP TABLE
| Step | Owner | Input | System(s) | GenAI Role | Output | Controls/Checks |
|---|---|---|---|---|---|---|
| 1 | ... | ... | ... | Assist/Automate/Decide | ... | ... |
```

2. To-be step table:

```md
## <X.X>. TO-BE STEP TABLE
| Step | Owner | Input | System(s) | GenAI Role | Output | Controls/Checks |
|---|---|---|---|---|---|---|
| 1 | ... | ... | ... | Assist/Automate/Decide | ... | ... |
```

3. Component mapping table (in blueprint):

```md
## <X.X>. Component Mapping (Link to Canonical Pages)
| Component | Why it matters here | Link |
|---|---|---|
| Retrieval (RAG) | ... | ../02_solution_components/2.1_rag.md |
```

In the step tables, make `Controls/Checks` explicit (PII redaction, ABAC/RBAC filter, audit logging, approval gate, refusal policy, idempotency).

## 2.5. Next Steps (always last)

Always end with:

```md
---

# 8. NEXT STEPS

- [<internal link>](<internal link>) - <why it matters>

If you are starting from scratch:
1. <action>
2. <action>
3. <action>
4. <action>
```

---

# 3. CONTENT RULES (HOW TO WRITE EACH SECTION)

## 3.1. Section 1: Why it matters must include decision language

Include:

- enterprise value (time, cost, quality, adoption)
- enterprise risk (safety, compliance, reliability, reputational)
- explicit decisions enabled (go/no-go, MVP scope, autonomy level, tool enablement, scaling)

Use a pattern like:

"In enterprise contexts, this archetype matters because <value>, but it creates <risk>, so teams must decide <decision>."

## 3.2. Section 2: As-is must be concrete and diagnostic

As-is should include:

- symptoms, root causes, and impact (MECE)
- where time is lost (handoffs, rework, waiting)
- where risk concentrates (sensitive data, privileged actions)

The as-is step table should show the real workflow, not an idealized one.

## 3.3. Section 3: To-be must specify operating rules and controls

To-be should answer:

- where GenAI helps (assist vs automate vs decide)
- where humans must approve (HITL)
- what happens when evidence is missing ("abstain" and escalation)
- what happens in exceptions and edge cases

The to-be step table must include controls at each step, not only at the end.

## 3.4. Section 4: Decision guide must include fit, anti-fit, and readiness

Decision guide should include:

- Fit criteria (when this archetype is a good choice)
- Anti-fit criteria (when to avoid or delay)
- Readiness checklist split by:
  - data readiness (quality, freshness, ownership, classification)
  - integration readiness (APIs, auth, sandboxes, limits)
  - governance readiness (RBAC/ABAC, logging rules, approvals)
  - operating readiness (support model, runbooks, training)

Then explicitly justify the recommended approach:

- workflow+AI vs agentic (and why)
- RAG vs no RAG (and why)
- tool calling boundaries (allowed actions)

## 3.5. Section 5: Blueprint must map to solution components and controls

Blueprint should include:

- one architecture diagram (keep diagrams consistent across archetypes)
- a component mapping table with links (DRY)
- data and integration design (sources of truth, identity/permissions, retention/logging)
- use-case specific guardrails (disallowed intents, tool allowlist rules, escalation triggers)

## 3.6. Section 6: Delivery must be phased and gated

Delivery should include:

- a phase plan (POC/MVP -> pilot -> scale), with:
  - objective, scope, deliverables, dependencies, acceptance criteria, timeline
- roles and cadence (light RACI; who approves what)
- backlog starter (data & ingestion, UX, guardrails, evals, observability, integrations)
- measurement and acceptance gates (go/no-go thresholds per phase)

This is where the archetype becomes consulting-grade: it turns architecture into deliverable work.

## 3.7. Pitfalls must be diagnostic

For each pitfall:

- symptom (what you see)
- root cause (why it happens)
- fix (what to change)
- prevention (turn it into a regression test / gate)

## 3.8. Reusable assets must be included

Every archetype page should include assets consultants reuse:

- discovery questions by stakeholder (business/ops, IT/arch, security/privacy, SMEs)
- workshop agenda (90-120 minutes)
- demo script (3-5 minutes)
- templates (use-case card, risk register starter, MVP acceptance criteria, pilot rollout checklist)

## 3.9. Case study must be end-to-end and realistic

Case study should include:

- context and risk appetite (including P0 failures)
- architecture choice and why it fits this archetype
- delivery timeline (phases and gates)
- eval plan and evidence used for go/no-go decisions
- observability and incident response
- one realistic incident and how it became a regression gate
- scaling decision and why it is defensible

---

# 4. QUALITY GATES (HOW TO SELF-CHECK)

Before considering an archetype page done, verify:

## 4.1. Structure checks

- Has `**Goal:**`, `**Prerequisites:**`, `**Related:**` at the top.
- Has `# TL;DR (30 SECONDS)` and a Use-Case Card table.
- Has `# WHAT'S IN / WHAT'S OUT`.
- Includes both as-is and to-be step tables.
- Includes a component mapping table with links to `02_solution_components/`.
- Includes a case study before Next Steps.
- Next Steps is the last section.

## 4.2. Content checks

- Would a consultant be able to position the archetype after reading it once?
- Are fit/anti-fit and readiness criteria explicit?
- Are P0 failures defined (and measurable) for this archetype?
- Are phase gates and acceptance criteria explicit?
- Are KPIs few and decision-relevant (3-6)?
- Are reusable assets included (discovery questions, workshop agenda, demo script, templates)?

## 4.3. Style checks

- Bullet share is roughly 30% (not exact, but clearly not bullet-heavy).
- Bold is used strategically.
- No smart quotes; use ASCII quotes.
- Headings are numbered consistently (H1 X., H2 X.X., H3 X.X.X.).

---

# 5. REWRITING EXISTING ARCHETYPES (MIGRATION PLAYBOOK)

When rewriting an existing archetype page:

1. Start from the Use-Case Card (definition, value, pattern, risk, KPIs).
2. Write the as-is and to-be step tables next (these force reality and controls).
3. Add the decision guide (fit/anti-fit/readiness) so the archetype can be chosen defensibly.
4. Map the archetype to solution components via links (keep it DRY).
5. Add delivery phases and acceptance gates (POC -> pilot -> scale).
6. Add pitfalls (diagnostic) and reusable assets (questions, agenda, demo script).
7. Add a realistic case study and ensure Next Steps is last.

If you must choose between being shorter and being deliverable, prefer deliverable. Add structure rather than adding more bullets.
