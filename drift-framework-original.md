# DRIFT Assessment Framework — v2

## What is DRIFT?

**DRIFT** describes the natural quality degradation that occurs in knowledge base articles over time. The framework evaluates five categories of content quality drift:

1. **Audience Drift** — Content loses focus on its intended users
2. **Governance Drift** — Content violates established rules or content types over time
3. **Topic Drift** — Scope creep as content tries to cover too much
4. **Style Drift** — Writing standards degrade
5. **Template Drift** — Structural consistency breaks down

The framework evaluates knowledge base articles on a **1–10 scale per category** (1 = no drift / best, 10 = severe drift / worst) and produces a **weighted overall score** with a corresponding status.

---

## Pre-Analysis Checklist

Before scoring, perform a structured inventory of the article:

| Dimension | What to Identify |
|---|---|
| **Primary Audience** | Who is this written for? (e.g., Advocates, SAS, sellers, both) |
| **Distinct Tasks** | Count and list the separate jobs/workflows the article covers |
| **FAQ Sections** | Count Q&A pairs embedded in the article |
| **Verbatim Scripts** | Count phrases like "You could say…" or scripted language for agents |
| **Seller-Facing Guidance** | Count sections that explain product behavior to sellers (not agent procedures) |
| **Tools Referenced** | List all internal tools mentioned (e.g., Square Dashboard, Regulator, Jedi Temple) |
| **Geographic Scope** | Identify what market(s) this applies to (e.g., US, CA, AU, Global) |

---

## Category 1: Audience Drift

**Weight: 1.0**

**Question:** Is the article written for one clear audience, or does it blur roles?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Single, clearly defined audience throughout; no role blurring |
| 3–4 | Primarily one audience with minor references to another role |
| 5–6 | Two audiences addressed without clear separation or labeling |
| 7–8 | Multiple roles (advocate, SAS, seller) mixed throughout with no delineation |
| 9–10 | Completely unclear who the article is for; buyer-facing and agent-facing language fully intermingled |

### What to Check

- Are multiple roles (advocate, SAS, seller) addressed without separation?
- Is buyer-facing vs. seller-facing language mixed?
- Does the geographic scope match the title?
- Is there a clear audience statement?
- Is the voice (second person "you") consistently directed at one audience?

---

## Category 2: Governance Drift

**Weight: 1.0**

**Question:** Does the article contain content that violates knowledge base governance rules?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Fully compliant with governance rules; no embedded scripts, FAQs, or mixed content types |
| 3–4 | Minor governance issues (e.g., 1–2 embedded scripts in an otherwise clean article) |
| 5–6 | Moderate issues (e.g., a small FAQ section or several scripts in a reference article) |
| 7–8 | Significant violations (e.g., dedicated scripting tables in a reference article, multiple content types mixed) |
| 9–10 | Article fundamentally violates governance structure; content type is completely wrong for its placement |

### What to Check

- **Verbatim scripts** ("You could say…") embedded in reference/overview articles — these should be in procedure articles only
- **Embedded FAQs** that belong in a separate FAQ article
- **Seller-facing product guidance** mixed with advocate procedures
- **Procedural steps** in what should be a reference/overview article
- **Reference content** in what should be a procedure article

---

## Category 3: Topic Drift

**Weight: 1.0**

**Question:** Does the article try to cover too many distinct tasks?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Single, well-scoped topic with one clear job story |
| 3–4 | One primary topic with 1–2 closely related sub-topics |
| 5–6 | 2–3 distinct workflows bundled together with some logical connection |
| 7–8 | Multiple distinct workflows with different triggers and completion criteria bundled into one article |
| 9–10 | "Umbrella" article covering loosely related or unrelated topics; should be split into 3+ separate articles |

### What to Check

- Multiple distinct workflows bundled into one article
- Multiple job stories with different triggers and completion criteria
- "Umbrella" article covering loosely related topics
- Content that could logically stand alone as its own article
- Whether the article title accurately represents ALL the content within

---

## Category 4: Style Drift

**Weight: 1.0**

**Question:** Does the writing follow style standards?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Fully compliant with style guide; active voice, single-action steps, proper formatting |
| 3–4 | Minor style issues (e.g., occasional passive voice or inconsistent bolding) |
| 5–6 | Moderate issues (e.g., multiple multi-action steps, several passive constructions) |
| 7–8 | Significant style violations throughout; hard to follow due to formatting issues |
| 9–10 | Article ignores style guide entirely; passive voice dominant, no formatting standards followed |

### What to Check

- **Passive voice** where active voice is required (e.g., "Verification is needed" → "You need to verify")
- **Multi-action steps** — each step should contain one action only
- **UI elements not bolded** per style guide (tool names, button labels, menu items)
- **Inconsistent formatting** (headers, lists, tables used inconsistently)
- **Emoji usage** where standard callouts should be used
- **Vague instructions** (e.g., "verify accordingly" without specifying how)

---

## Category 5: Template Drift

**Weight: 0.5**

**Question:** Does the article follow the required structural template?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | All required template elements present and correctly formatted |
| 3–4 | Minor template issues (e.g., one missing optional section or minor formatting inconsistency) |
| 5–6 | Some required sections missing or incorrectly formatted |
| 7–8 | Multiple required sections missing; structure doesn't follow template |
| 9–10 | No recognizable template structure; article is free-form |

### What to Check

- **Geo tags** present and correctly formatted (e.g., [US], [Global])
- **Revisions section** with documented changes (date, author, Jira ID, description)
- **Required sections** present (General Information, About this post, etc.)
- **Links to related articles** where appropriate
- **Duplicate content** (paragraphs or sections repeated)
- **Proper heading hierarchy** (H1 → H2 → H3, not skipping levels)

---

## Overall Score Calculation

### Formula

```
Overall = (Audience × 1.0) + (Governance × 1.0) + (Topic × 1.0) + (Style × 1.0) + (Template × 0.5)
          ─────────────────────────────────────────────────────────────────────────────────────────────
                                    1.0 + 1.0 + 1.0 + 1.0 + 0.5 (= 4.5)
```

Round the result to the **nearest integer**.

---

## Status Determination

| Overall Score | Status | Meaning |
|---|---|---|
| **1–3** | ✅ Compliant | Article meets standards; no action needed |
| **4–5** | ⚠️ Needs Review | Minor issues identified; schedule for review |
| **6–7** | 🔶 Action Required | Significant drift detected; prioritize remediation |
| **8–10** | 🔴 Critical | Severe drift across multiple categories; immediate rewrite needed |

---

## Output Format

A complete DRIFT assessment should include:

1. **Pre-Analysis Checklist** — structured inventory table
2. **5 Category Scores** — each with:
   - Score (1–10)
   - Specific findings (evidence from the article)
   - Actionable fix steps
3. **Overall Score Calculation** — breakdown table showing weights and weighted scores
4. **Final Status** — determination with summary of top issues and priority recommendations

---

## Usage Notes

- **Score honestly** — a score of 1 means truly zero issues in that category
- **Cite evidence** — every finding should reference specific content from the article
- **Make fixes actionable** — don't just identify problems; describe exactly what to change
- **Weight reflects impact** — Template Drift is weighted at 0.5 because structural issues are less impactful to the reader than content/audience/governance issues
- **Context matters** — a reference article has different governance expectations than a procedure article
