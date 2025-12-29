# RULE SET: HOW TO WRITE THIS HANDBOOK

This file defines a single writing standard for the entire repository, using `02_solution_components/2.5_evals.md` as the reference implementation.

It is written for coding agents (and humans) who will:
1) create new handbook pages, and
2) rewrite existing pages to match a consistent consulting-grade style.

The outcome we want: every page reads like an end-to-end guide that a strategic consulting audience can use to **understand**, **decide**, and **deliver**.

---

# 1. NON-NEGOTIABLES (WHAT MUST ALWAYS BE TRUE)

## 1.1. Audience and voice

- Audience: strategy/tech consultants and enterprise stakeholders (product, architecture, risk/security, delivery).
- Voice: didactic, practical, confident-but-honest. Explain concepts like you are onboarding a smart reader who is new to the topic.
- Goal: enable decisions and delivery, not academic or tehcnical completeness.

## 1.2. Language and tone

- English only.
- Prefer clear, direct sentences. Avoid jargon unless you define it.
- Use consistent terms across the repo (glossary-friendly).

## 1.3. Page is “end-to-end”

Each page must cover the topic from:
- **Why it matters** (enterprise value, risk, adoption)
- **What it is** (definitions, mental models)
- **How it works** (components and flow)
- **How to implement it** (process, roles, artifacts, gates)
- **How to measure and operate it** (metrics, monitoring, escalation)
- **What goes wrong** (pitfalls, failure modes, mitigations)

## 1.4. Bullets vs continuous text (70/30)

- Target: ~70% continuous text, ~30% bullets/numbered lines.
- Bullets are for: lists, checklists, criteria, options, taxonomy, “do/don’t”.
- Continuous text is for: explanation, causality, narrative, trade-offs, reasoning.

## 1.5. Bolding (strategic, not decorative)

Use bold to highlight what a consultant would underline in a review:
- **key claims**, **decision criteria**, **non-negotiables**, **risk language**, **go/no-go rules**, **the one sentence to remember**

Rules:
- Do not bold entire paragraphs.
- Prefer 1–3 bold phrases per paragraph when needed.
- Bold terms on first introduction if they become recurring concepts.

## 1.5 Lenght of the file 
- Aim for <1000 lines in the text. 
- May be a litter higher like 1080
- May be lower like 300, 500 or 700...

## 1.6. Diagrams
Some files use diagrmans to explainf concepts. This is ok, no problem at all. If it is used for a more didactic axplanation, it is great

---

# 2. STRUCTURE CONTRACT (THE REQUIRED SKELETON)

Use this skeleton for every file unless there is a strong reason not to.

## 2.1. Top matter (always present)

At the top of every page:

1) H1 title (topic name), in caps:
```md
# <TOPIC NAME IN CAPS> (<OPTIONAL CLARIFIER>)
```

2) Goal, prerequisites, related (exact labels):
```md
**Goal:** <1–2 lines, outcome-focused>

**Prerequisites:**
- [<link>](<link>) - <why it matters>

**Related:**
- [<link>](<link>) - <why it matters>
```

3) Separator before H1 titles:
```md
---
```

## 2.2. TL;DR and scope blocks (always present)

Immediately after the separator:

```md
# TL;DR (30 SECONDS)

<One short paragraph that can be read aloud in <30 seconds.>

- <3–8 bullets: the “memory hooks”>

---

# WHAT'S IN / WHAT'S OUT

**In:** <1–3 lines>

**Out:** <1–3 lines>

---
```

## 2.3. Main body (numbered H1 sections)

Main sections are numbered and in caps, using:
- H1: `# X. TITLE IN CAPS`
- H2: `## X.X. Title Case`
- H3: `### X.X.X. Title Case`

Rules:
- Numbering must be consistent (H2/H3 must match their parent section).
- Keep the number of H1 main sections reasonable (typically 5–8, excluding TL;DR and WHAT'S IN/OUT).
- 
- Use H2/H3 only when they improve clarity; avoid “heading spam”.

Recommended main-body layout (adapt per topic):

1) `# 1. WHAT IT IS (AND WHAT IT IS NOT)`  
2) `# 2. WHY IT MATTERS IN ENTERPRISE`  
3) `# 3. HOW IT WORKS (SYSTEM VIEW)`  
4) `# 4. HOW TO IMPLEMENT (DELIVERY PLAYBOOK)`  
5) `# 5. HOW TO MEASURE AND OPERATE`  
6) `# 6. PITFALLS AND FAILURE MODES`  
7) `# 7. CASE STUDY: <TOPIC IN ENTERPRISE>` (place right before Next Steps)

## 2.4. Next Steps (always last)

Always end with:
```md
---

# <N>. NEXT STEPS
```

Then:
- 3–6 internal links, each with a short reason.
- 2–4 “starting from scratch” actions (numbered list).

---

# 3. CONTENT RULES (HOW TO WRITE EACH SECTION)

## 3.1. “Why it matters” must include decision language

Include:
- the business value (time, cost, quality, adoption)
- the risk (safety, compliance, reliability, reputational)
- the decision it enables (go/no-go, baseline choice, gating, scaling)

Use a sentence pattern like:
“In enterprise contexts, <topic> matters because <value>, but it creates <risk>, so teams must decide <decision>.”

## 3.2. Define terms before using them as assumptions

When a concept is critical, define it in plain English first, then introduce the technical term.

## 3.3. Prefer system thinking over isolated parts

Consulting readers need:
- end-to-end flow
- where failures happen
- which lever fixes which failure

Add “separation of concerns” language:
- retrieval vs generation
- selection vs execution
- design-time vs run-time
- offline vs online measurement

## 3.4. Always include “how to implement” as a playbook

Implementation guidance should include:
- phases (POC -> pilot -> production)
- roles/ownership (product, eng, SME, security)
- artifacts (rubrics, datasets, run cards, gates, dashboards)
- cadence (weekly loop, incident response)

This is where the page becomes consulting-grade.

## 3.5. Metrics must map to decisions

Do not list metrics without purpose.
Introduce metrics with: “We measure X because it supports decision Y.”

If a topic has a “slice risk”, explicitly say:
- “Overall score is not enough; risk concentrates in slices (high-risk, tool cases, hard cases).”

## 3.6. Use examples that look like enterprise reality

Examples should be realistic:
- policy Q&A with citations (RAG)
- workflow tools (tickets, CRM, account status)
- access control and redaction
- latency and cost trade-offs

## 3.7. Pitfalls must be diagnostic, not generic

For each pitfall, include:
- symptom (what you see)
- root cause (why it happens)
- fix (what to change)
- how to prevent recurrence (turn it into a regression test / gate)

---

# 4. STYLE RULES (MICRO-DECISIONS THAT MATTER)

## 4.1. Paragraph style

- Prefer 2–5 sentence paragraphs.
- First sentence: point. Next sentences: explanation and implication.
- Avoid walls of text; break when the reader would breathe.

## 4.2. Bullets style

- Use bullets for lists; keep bullets short and parallel when possible.
- Prefer 3–8 bullets per list. If you need more, you likely need structure or grouping.
- Use numbered lists only when order matters.

## 4.3. Formatting conventions

- Use plain ASCII quotes (`"`) not smart quotes.
- Use consistent hyphenation: “go/no-go”, “end-to-end”.
- Keep link text short and meaningful; always explain “why this link”.

## 4.4. Do not over-claim

Use cautious language when needed:
- “typically”, “often”, “in most enterprise programs”
- If a claim depends on context, say so.

---

# 5. QUALITY GATES (HOW TO SELF-CHECK BEFORE MERGING)

Before considering a page “done”, verify:

## 5.1. Structure checks

- Has `**Goal:**`, `**Prerequisites:**`, `**Related:**` at the top.
- Has `# TL;DR (30 SECONDS)` and `# WHAT'S IN / WHAT'S OUT`.
- Main section headings follow numbering: H1 `X.`, H2 `X.X.`, H3 `X.X.X.`.
- “Next Steps” exists and is the last section.

## 5.2. Content checks

- Would a consultant be able to explain the topic after reading it once?
- Does the page include at least one concrete implementation playbook?
- Does it include decision criteria and explicit trade-offs?
- Does it include failure modes with symptoms + root causes + fixes?
- If the topic has safety implications, are P0 blockers called out?

## 5.3. Style checks

- Bullet share is roughly 30% (not exact, but clearly not bullet-heavy).
- Bold is used to emphasize key consulting points, not for decoration.
- No “heading spam” (headings are used to improve navigation, not to break every paragraph).

---

# 6. REWRITING EXISTING FILES (MIGRATION PLAYBOOK)

When rewriting an existing page:

1) Keep the original topic scope, but reshape it into the skeleton (Goal -> TL;DR -> In/Out -> main sections -> case study -> Next Steps).
2) Convert “wall-of-bullets” into explanatory text, keeping only the lists that support decisions or checklists.
3) Add missing consulting elements:
   - explicit decisions and trade-offs
   - P0/P1/P2 language if risk exists
   - a realistic case study
   - an operational loop (cadence, ownership, gates)
4) Ensure internal links are correct and helpful.

If you must choose between being shorter and being end-to-end, prefer end-to-end. Add structure rather than adding more bullets.
