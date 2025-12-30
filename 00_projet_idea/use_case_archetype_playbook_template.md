# Use-Case Archetype Playbook Template (for Consulting GenAI Projects)

This template is designed for **strategic consulting audiences**. Each archetype page should read like an end-to-end guide that helps consultants **understand**, **decide**, and **deliver** a GenAI initiative without re-teaching foundations or solution components (those should be linked, not repeated).

---

## How to use this template

- Apply the same structure to every archetype file.
- Keep content operational: pain points, steps, decision criteria, delivery plan, measurement.
- Always include reusable consulting assets: discovery questions, workshop agenda, demo script, acceptance criteria.

---

# Recommended Structure for Each `use_case_archetype` Document

## 0) Header + "Consulting Snapshot" (readable in ~2 minutes)

**Purpose:** allow a consultant to quickly position the archetype in a client conversation.

Include:
- **Archetype name + one-line definition**
- **What it replaces / augments** (current process/tooling)
- **Primary value drivers** (cost, speed, quality, risk)
- **Primary solution pattern** (RAG, tool calling, workflow+AI, agentic)
- **Risk level** (Low/Med/High) and why
- **Typical stakeholders** (Business owner, Ops, IT, Sec/Privacy)
- **MVP timebox** (e.g., 4-6 weeks) and what "done" looks like
- **KPIs** (3-6 metrics max)

**Format recommendation:** a Use-Case Card table + TL;DR bullets.

---

## 1) Business Context and Pain Points (what hurts and why)

**Purpose:** anchor the archetype in a real operational problem, not "GenAI because GenAI".

Include:

### 1.1 Common pain points (MECE list)

- **Symptoms** (what people complain about)
- **Root causes** (why it happens)
- **Impact** (cost, SLA breaches, compliance risk, customer experience)

### 1.2 Current-state workflow (as-is)

- Show the typical steps today (human + systems)
- Identify failure points (handoffs, rework, waiting times)

**Best practice:** represent it as a step table.

---

## 2) Target State and User Journey (what "good" looks like)

**Purpose:** define the to-be experience in operational steps.

### 2.1 To-be workflow (step-by-step)

- The steps the business will run after implementation
- Where GenAI is used (**assist vs automate vs decide**)
- Where humans must approve (**human-in-the-loop**)

### 2.2 Operating rules

- Escalation logic (when to handoff to humans)
- Exception handling (edge cases)
- "No-answer / abstain" policy when evidence is missing

**Best practice:** a to-be step table with controls.

---

## 3) Decision Guide (fit, anti-fit, readiness)

**Purpose:** help consultants decide if the archetype is appropriate and what pattern to use.

### 3.1 Fit criteria (when this archetype is a good choice)

- Data exists and has a reliable **source of truth**
- Integration path is feasible
- Governance can support it
- Business can define success metrics

### 3.2 Anti-fit criteria (when to avoid or delay)

- No data ownership / no access model
- No escalation workflow
- High-risk actions without approvals
- Unstable policies or constantly changing truth without governance

### 3.3 Readiness checklist (minimum viable)

Break into:
- **Data readiness** (quality, freshness, ownership, classification)
- **Integration readiness** (APIs, auth, sandboxes, limits)
- **Governance readiness** (RBAC/ABAC, logging rules, approvals)
- **Operating readiness** (support model, runbooks, training)

### 3.4 Recommended approach (explicitly justify)

- Workflow+AI vs Agentic (and why)
- RAG vs no RAG (and why)
- Tool calling boundaries (allowed actions)

---

## 4) Solution Blueprint (how it works end-to-end, without re-teaching components)

**Purpose:** provide a reference architecture and map it to your solution components.

### 4.1 Architecture diagram (single diagram)

Keep it consistent across archetypes; vary integrations and data sources.

### 4.2 Component mapping (link to solution component pages)

A table:
- Component | Why it matters here | Link

### 4.3 Data and integration design (archetype-specific)

- Systems involved
- Sources of truth
- Identity and permissions
- Data retention + logging boundaries

### 4.4 Guardrails for this archetype

Use-case specific guardrails:
- disallowed intents
- tool allowlist rules
- sensitive data handling
- escalation triggers
- abstain thresholds

---

## 5) Delivery Playbook (how a consulting team executes it)

**Purpose:** make it deliverable, with phases, deliverables, and acceptance gates.

### 5.1 Phase plan (POC/MVP -> Pilot -> Scale)

For each phase:
- Objective
- Scope
- Key deliverables
- Dependencies
- Acceptance criteria ("ready to move on")
- Typical timeline

### 5.2 Roles and cadence (light RACI)

- Who approves what
- Weekly cadence (SME review, security review, eval review)

### 5.3 Backlog starter (MVP backlog)

Group by:
- Data & ingestion
- Core UX
- Guardrails
- Evals
- Observability
- Integrations

---

## 6) Measurement and Acceptance (how you prove it works)

**Purpose:** give consultants a measurement story aligned to business outcomes.

### 6.1 Success metrics (business KPIs)

3-6 max (examples):
- Deflection, AHT, FCR, cycle time, error rate, compliance incidents, escalation quality

### 6.2 System quality metrics (GenAI KPIs)

Examples:
- Citation coverage (if RAG)
- Retrieval precision/recall (if RAG)
- Tool success rate / duplicate action rate (if tools)
- Cost per case (tokens + tool calls)
- Safety refusal accuracy

### 6.3 Acceptance gates

Define go/no-go thresholds per phase.

---

## 7) Pitfalls and How to Avoid Them (consulting value section)

**Purpose:** turn the playbook into battle-tested guidance.

Include 8-12 items:
- what goes wrong
- how you detect it
- how you fix it
- prevention tactic

---

## 8) Appendices (assets consultants reuse)

**Purpose:** make the page immediately usable in delivery.

Include:
- **Discovery questions** (by stakeholder: Business/Ops, IT/Arch, Sec/Privacy)
- **Workshop agenda** (90-120 minutes)
- **Demo script (3-5 minutes)**
- **Templates**:
  - Use-Case Card
  - Risk register starter
  - MVP acceptance criteria
  - Pilot rollout checklist

---

# Canonical "Step Table" (include in every archetype)

Include a canonical step table for both As-Is and To-Be.

## Step Table Template

| Step | Owner | Input | System(s) | GenAI role | Output | Controls/Checks |
|---|---|---|---|---|---|---|
| 1 | ... | ... | ... | ... | ... | ... |
| 2 | ... | ... | ... | ... | ... | ... |
| 3 | ... | ... | ... | ... | ... | ... |

**Tip:** Make Controls/Checks explicit (PII redaction, ABAC filter, audit logging, approval gate, refusal policy).

---

# Minimal, High-Impact Heading Set (copy/paste)

If you want a concise archetype page that most consultants will actually read, use this heading list:

1. **Snapshot (TL;DR + Use-Case Card)**
2. **Pain Points + As-Is Workflow**
3. **To-Be Workflow + Operating Rules**
4. **Decision Guide (Fit / Anti-fit / Readiness)**
5. **Blueprint (Architecture + Component Mapping + Guardrails)**
6. **Delivery Plan (MVP -> Pilot -> Scale)**
7. **Measurement (KPIs + Acceptance Gates)**
8. **Pitfalls + Mitigations**
9. **Appendix (Discovery Questions + Demo Script + Templates)**

---

# Optional: Copy/Paste Archetype Skeleton (fill-in template)

```md
# <Archetype Title>

**Primary pattern:** <RAG / Tool Calling / Workflow+AI / Agentic>  
**Risk level:** <Low/Med/High>  
**MVP timeline:** <4-6 weeks typical>  
**Typical stakeholders:** <...>

## Snapshot (TL;DR)
- **Pain:** ...
- **Value:** ...
- **Approach:** ...
- **Risks:** ...
- **KPIs:** ...

## Use-Case Card
| Item | Summary |
|---|---|
| Primary users | ... |
| Primary decision/task | ... |
| Systems involved | ... |
| Data sources (source of truth) | ... |
| Actions (tools) allowed | ... |
| In-scope | ... |
| Out-of-scope | ... |
| Primary KPIs | ... |
| Constraints | ... |

## Pain Points + As-Is Workflow
### Pain points
- ...

### As-Is step table
| Step | Owner | Input | System(s) | GenAI role | Output | Controls/Checks |
|---|---|---|---|---|---|---|
| 1 | ... | ... | ... | ... | ... | ... |

## To-Be Workflow + Operating Rules
### To-Be step table
| Step | Owner | Input | System(s) | GenAI role | Output | Controls/Checks |
|---|---|---|---|---|---|---|
| 1 | ... | ... | ... | ... | ... | ... |

### Rules (escalation, abstain, exceptions)
- ...

## Decision Guide
### Fit criteria
- ...

### Anti-fit criteria
- ...

### Readiness checklist
- Data: ...
- Integrations: ...
- Governance: ...
- Operations: ...

## Blueprint
- Architecture diagram (Mermaid)
- Component mapping (links)
- Data & integrations
- Guardrails (use-case specific)

## Delivery Plan (MVP -> Pilot -> Scale)
- MVP scope + deliverables + acceptance criteria
- Pilot hardening + rollout
- Scale plan

## Measurement
- Business KPIs
- System metrics
- Acceptance gates

## Pitfalls + Mitigations
- ...

## Appendix
- Discovery questions
- Workshop agenda
- Demo script
- Templates
```

---

## Notes (to keep pages consistent and MECE)

- Do not re-teach RAG/tool calling/agentic fundamentals; link to your foundation/component docs.
- Keep KPIs few and meaningful.
- Prefer tables and checklists when they clarify; keep narrative for reasoning and trade-offs.
- Always define what "done" means (acceptance criteria) per phase.
