# DRIFT Assessment Framework — Block Support Knowledge Model Edition

**Status:** Draft v0.1  
**Date:** 2025-01-27  
**Owner:** Derek Mulch
**Companion:** This framework assesses quality drift in the Block Support Knowledge Model defined in [`content-model-architecture.md`](./content-model-architecture.md)

---

## 1. Purpose

The DRIFT Assessment Framework evaluates quality degradation in modular content blocks within the Block Support Knowledge Model. It measures how individual blocks and their compositions drift from established standards across five categories, ensuring content maintains quality as it scales through reuse and recombination.

**DRIFT** describes the natural quality degradation that occurs in modular content over time:
- **Audience Drift** — Blocks lose focus on their intended users
- **Governance Drift** — Blocks violate approved taxonomy and composition rules  
- **Topic Drift** — Blocks try to cover too many distinct purposes
- **Style Drift** — Writing standards degrade within block types
- **Template Drift** — Structural consistency breaks down at the block level

The framework evaluates content on a **1–10 scale per category** (1 = no drift / best, 10 = severe drift / worst) and produces a **weighted overall score** with corresponding remediation status.

---

## 2. Key Terms

- **Block** — the smallest reusable unit of support content with exactly one content type
- **Issue Card** — the canonical definition of a customer problem, governing which blocks resolve it
- **Surface** — the assembled output a reader sees (Internal Task Flow, Agent View, How-To, etc.)
- **Composition** — how blocks combine through reference patterns (block-to-block, Issue Card-to-blocks, Reference Data single-source)
- **Content Type** — one of eight atomic block types organized by role in support content
- **Taxonomic Spine** — hierarchical classification (Business Unit → Product → Topic → Issue)

---

## 3. Pre-Assessment Block Inventory

Before scoring, perform a structured inventory using the Block Support Knowledge Model structure:

### 3.1 Block Discovery
| Dimension | What to Identify |
|---|---|
| **Block Types Present** | Count blocks by type: Task, Education, Policy, Glossary, Reference Data, Approved Response, Required Script, Conversation Guidance |
| **Block IDs** | Verify kebab-case slugs with correct prefixes (`task-`, `edu-`, `policy-`, etc.) |
| **Content Type Compliance** | Confirm each block has exactly one content type from approved taxonomy |
| **Taxonomic Placement** | Map blocks to Business Unit → Product → Topic → Issue hierarchy |
| **Composition Patterns** | Identify block-to-block references, Issue Card relationships, Reference Data dependencies |

### 3.2 Surface Analysis
| Dimension | What to Identify |
|---|---|
| **Surface Templates** | List surfaces using blocks: Internal Task Flow, Agent View, How-To, Education Article, Training Module, etc. |
| **Component Mapping** | Verify blocks fill appropriate surface components (Task blocks in "Steps", Policy blocks in "Before You Begin") |
| **Cross-Surface Reuse** | Track which blocks appear in multiple surfaces |
| **Template Compliance** | Check surfaces follow prescribed component structure |

### 3.3 Metadata Validation
| Dimension | What to Identify |
|---|---|
| **Common Base Fields** | Verify required fields: brand, userType, audience, channel, supportStage, riskRating |
| **Type-Specific Extras** | Check type-specific fields (educationSubtype, tone, macroName, etc.) |
| **Reference Integrity** | Validate all block references resolve correctly |
| **Attribute Consistency** | Ensure blocks with similar purposes have consistent metadata |

---

## 4. Category 1: Audience Drift

**Weight: 1.0**

**Question:** Do blocks maintain clear audience focus consistent with their metadata, and do surface compositions serve coherent user needs?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Each block's audience metadata matches content; surfaces compose blocks for consistent user types |
| 3–4 | Most blocks have clear audience alignment with minor metadata inconsistencies |
| 5–6 | Some blocks address multiple audiences without clear separation; surface compositions create minor user confusion |
| 7–8 | Blocks with conflicting audience metadata are composed inappropriately in surfaces |
| 9–10 | Block audience metadata is completely inconsistent with content; surfaces mix incompatible user types |

### What to Check

- **Audience metadata alignment**: Does `audience` field (Public/Advocate/Both) match block content?
- **User type consistency**: Does `userType` (Personal/Business/Teen/All) align with content language and examples?
- **Surface audience coherence**: Do surfaces compose blocks with compatible audience metadata?
- **Channel appropriateness**: Does `channel` (Help Center/Agent Assist/Both) match content tone and detail level?
- **Cross-surface reuse**: When blocks appear in multiple surfaces, do audience assumptions remain consistent?

---

## 5. Category 2: Governance Drift

**Weight: 1.0**

**Question:** Do blocks conform to the approved content type taxonomy and composition rules defined in the Block Support Knowledge Model?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | All blocks use approved content types; composition follows model rules; metadata schema compliance |
| 3–4 | Minor deviations from approved types or composition patterns (1-2 blocks) |
| 5–6 | Some blocks violate content type definitions or inappropriate composition patterns |
| 7–8 | Multiple blocks deviate from approved taxonomy; significant composition rule violations |
| 9–10 | Fundamental violations of content model; unauthorized block types or composition patterns |

### What to Check

#### Content Type Compliance
- **Approved taxonomy**: Are blocks using only the 8 approved types (Task, Education, Policy, etc.)?
- **Type definition adherence**: Do blocks match their content type's purpose and shape?
- **Hybrid detection**: Are blocks trying to combine multiple content types inappropriately?
- **Schema compliance**: Do blocks include required common base fields and appropriate type-specific extras?

#### Composition Rule Compliance  
- **Reference patterns**: Are block-to-block, Issue Card-to-blocks, and Reference Data single-source patterns followed correctly?
- **Surface component rules**: Are blocks filling appropriate surface components (Task blocks in "Steps", not "Definitions")?
- **Issue Card governance**: Do Issue Cards properly govern block relationships through typed fields?
- **Reference Data integrity**: Is single-source principle maintained for Reference Data blocks?

#### Metadata Schema Compliance
- **Required fields**: Are all common base fields present with valid enum values?
- **Type-specific extras**: Are type-specific fields used appropriately (tone on Conversation Guidance, not Task)?
- **ID conventions**: Do block IDs follow kebab-case with correct prefixes?

---

## 6. Category 3: Topic Drift

**Weight: 1.0**

**Question:** Do blocks maintain single, clear purposes aligned with their taxonomic spine placement, and do surface compositions address coherent customer issues?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Each block serves one clear purpose; surfaces compose blocks to address single customer issues coherently |
| 3–4 | Most blocks are focused with minor scope creep in 1-2 blocks |
| 5–6 | Some blocks try to cover multiple purposes; surface compositions address 2-3 related issues |
| 7–8 | Multiple blocks have scope creep; surfaces combine blocks addressing distinct, loosely related issues |
| 9–10 | Blocks are unfocused and cover unrelated purposes; surface compositions are incoherent |

### What to Check

#### Block-Level Topic Focus
- **Single purpose**: Does each block do one job well within its content type definition?
- **Taxonomic alignment**: Does block content match its Business Unit → Product → Topic → Issue placement?
- **Content type boundaries**: Are blocks staying within their type's role (Procedural, Knowledge & Reference, Communication)?
- **Modularity range**: Do blocks fit the prescribed word count/complexity ranges for their type?

#### Surface-Level Topic Coherence
- **Issue Card alignment**: Do surfaces serve the customer issue defined in their Issue Card?
- **Component logic**: Do surface components build toward resolving a single customer problem?
- **Cross-surface consistency**: When blocks are reused across surfaces, do they maintain topic relevance?
- **CIT mapping confidence**: Is the Issue Card's CIT mapping confidence rating (high/medium/low) accurate?

---

## 7. Category 4: Style Drift

**Weight: 1.0**

**Question:** Do blocks follow prescribed style standards for their content type, maintaining consistency within type categories?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Each block type follows its prescribed style standards; consistent voice/tone within content type categories |
| 3–4 | Most blocks follow style standards with minor deviations in 1-2 blocks |
| 5–6 | Some blocks drift from prescribed style; inconsistent voice within content type categories |
| 7–8 | Multiple blocks violate style standards for their type; inconsistent formatting across similar blocks |
| 9–10 | Blocks ignore prescribed style standards entirely; no consistency within content type categories |

### Content Type-Specific Style Standards

#### Procedural Category
| Block Type | Voice/Tone | Language Patterns | Formatting Requirements |
|---|---|---|---|
| **Task** | Imperative, active | Single action verbs, direct commands | Tool + action + result format; numbered lists for multi-step |

#### Knowledge & Reference Category  
| Block Type | Voice/Tone | Language Patterns | Formatting Requirements |
|---|---|---|---|
| **Education** | Explanatory, instructional | Concept-focused, benefit-driven | Overview → details → application |
| **Policy** | Authoritative, definitive | Clear rule statements, no ambiguity | Rule → scope → exceptions |
| **Glossary** | Precise, concise | Term + definition format | 15-30 words, one sentence definition |
| **Reference Data** | Structured, factual | Data-driven, consistent units | Table/list format, clear headers |

#### Communication Category
| Block Type | Voice/Tone | Language Patterns | Formatting Requirements |
|---|---|---|---|
| **Approved Response** | Customer-appropriate, clear | Macro-ready language | 1-2 sentences, channel-variant aware |
| **Required Script** | Verbatim, compliant | Exact regulatory/legal language | Quoted format, compliance metadata |
| **Conversation Guidance** | Tone-appropriate, adaptable | Second-person, never scripted | Situation-based, tone metadata aligned |

### What to Check
- **Content type consistency**: Do all blocks of the same type follow the same style patterns?
- **Tone metadata alignment**: Does content match declared tone (for Conversation Guidance blocks)?
- **Channel variant appropriateness**: Do Approved Response blocks match their channel variant metadata?
- **Cross-surface style consistency**: When blocks appear in multiple surfaces, does style remain appropriate?

---

## 8. Category 5: Template Drift

**Weight: 0.5**

**Question:** Do blocks follow prescribed structural templates for their content type, and do surfaces follow component structure rules?

### Scoring Criteria

| Score | Description |
|---|---|
| 1–2 | Each block follows its prescribed template perfectly; surfaces follow component structure rules |
| 3–4 | Most blocks follow templates with minor structural deviations in 1-2 blocks |
| 5–6 | Some blocks missing required template elements or surface components incorrectly structured |
| 7–8 | Multiple blocks don't follow prescribed templates; surface structure violations |
| 9–10 | Blocks have no recognizable template structure; surfaces ignore component rules |

### Content Type Template Requirements

#### Procedural Category
| Block Type | Required Structure | Mandatory Elements |
|---|---|---|
| **Task** | Action → Object → Expected Result | Action verb, target object/system, success criteria |

#### Knowledge & Reference Category
| Block Type | Required Structure | Mandatory Elements |
|---|---|---|
| **Education** | Concept → Explanation → Context | Core concept, detailed explanation, usage context |
| **Policy** | Rule Statement → Scope → Exceptions | Policy rule, applicability, exception conditions |
| **Glossary** | Term → Definition | Term, concise definition (15-30 words) |
| **Reference Data** | Structure → Data → Metadata | Data format, actual data, update frequency/effective dates |

#### Communication Category
| Block Type | Required Structure | Mandatory Elements |
|---|---|---|
| **Approved Response** | Message → Context | Customer message, usage context |
| **Required Script** | Script → Compliance Info | Verbatim text, legal/compliance metadata |
| **Conversation Guidance** | Situation → Guidance → Tone | Context setup, guidance content, tone specification |

### Surface Template Compliance
Check that surfaces follow their prescribed component structures:

- **Internal Task Flow**: Trigger → Steps → Resolution components filled by appropriate block types
- **Agent View**: Context-driven components populated with eligible blocks based on metadata
- **How-To**: Introduction (Education) → Steps (Task) → Important to Know (Policy) structure
- **Education Article**: Overview (Education) → Body (Education) → Key Details (Policy) structure
- **Training Module**: Objectives → Key Concepts (Education/Glossary) → Guided Walkthrough (Task) structure

---

## 9. Overall Score Calculation

### Formula

```
Overall = (Audience × 1.0) + (Governance × 1.0) + (Topic × 1.0) + (Style × 1.0) + (Template × 0.5)
          ─────────────────────────────────────────────────────────────────────────────────────────────
                                    1.0 + 1.0 + 1.0 + 1.0 + 0.5 (= 4.5)
```

Round the result to the **nearest integer**.

---

## 10. Status Determination

| Overall Score | Status | Meaning |
|---|---|---|
| **1–3** | ✅ Compliant | Blocks meet Block Support Knowledge Model standards; no action needed |
| **4–5** | ⚠️ Needs Review | Minor drift identified; schedule for block review and metadata correction |
| **6–7** | 🔶 Action Required | Significant drift detected; prioritize block remediation and composition review |
| **8–10** | 🔴 Critical | Severe drift across multiple categories; immediate block rewrite and governance review needed |

---

## 11. Assessment Output Format

A complete DRIFT assessment for the Block Support Knowledge Model should include:

### 11.1 Block Model Inventory Report
- **Content Type Distribution**: Count of blocks by type (Task, Education, Policy, etc.)
- **Taxonomic Spine Mapping**: Blocks organized by Business Unit → Product → Topic → Issue
- **Surface Template Usage**: Which templates are using which blocks
- **Composition Pattern Analysis**: Reference relationships and dependencies
- **Metadata Compliance Summary**: Common base field and type-specific extra validation

### 11.2 Individual Block Assessments
For each block:
- **Block Identification**: ID, content type, taxonomic placement
- **5 Category Scores** (1–10 each) with specific findings
- **Metadata Validation**: Common base and type-specific field compliance
- **Reference Integrity**: Validation of all block references
- **Reuse Impact Analysis**: How many surfaces use this block
- **Block-Specific Recommendations**: Targeted remediation steps

### 11.3 Surface Composition Analysis
For each surface template:
- **Component Structure Review**: Template compliance assessment
- **Block-Component Fit**: Appropriateness of blocks filling components
- **User Journey Coherence**: Does the surface serve its intended audience effectively?
- **Issue Card Alignment**: Does the surface resolve the customer issue it claims to address?
- **Cross-Surface Consistency**: Style and tone consistency across surfaces using the same blocks

### 11.4 Governance Compliance Report
- **Content Type Taxonomy Violations**: Unauthorized or hybrid block types
- **Composition Rule Violations**: Improper reference patterns or surface component usage
- **Metadata Schema Violations**: Missing or invalid common base fields and type-specific extras
- **ID Convention Violations**: Blocks not following kebab-case prefix standards
- **Reference Data Single-Source Violations**: Duplicated data that should be centralized

### 11.5 Remediation Roadmap
- **Critical Path Fixes**: Blocks affecting multiple surfaces that need immediate attention
- **Governance Actions**: Steps to bring blocks into content model compliance
- **Metadata Standardization**: Common base field and type-specific extra corrections
- **Composition Improvements**: Reference pattern and surface component optimizations
- **Quality Assurance Process**: Ongoing monitoring aligned with Block Support Knowledge Model standards

---

## 12. Usage Guidelines

### 12.1 Assessment Principles
- **Model-first approach**: Assess compliance with Block Support Knowledge Model before evaluating quality
- **Taxonomy validation**: Verify governance compliance using approved content types and composition rules
- **Metadata integrity**: Ensure common base fields and type-specific extras are correctly implemented
- **Reuse impact consideration**: Understand how block changes affect multiple surfaces and Issue Cards
- **Evidence-based scoring**: Cite specific content and metadata for every finding

### 12.2 Implementation Workflow
1. **Block Discovery**: Inventory all blocks using content type taxonomy
2. **Taxonomic Mapping**: Place blocks on Business Unit → Product → Topic → Issue spine
3. **Governance Validation**: Verify content model compliance before quality assessment
4. **Individual Block Assessment**: Score each block across all drift categories
5. **Surface Composition Analysis**: Evaluate how blocks work together in surfaces
6. **Issue Card Governance Review**: Ensure Issue Cards properly govern block relationships
7. **Impact Mapping**: Understand remediation implications across reuse instances
8. **Remediation Planning**: Prioritize fixes based on drift severity, reuse impact, and model compliance

### 12.3 Quality Maintenance
- **Regular Assessment Cycles**: Quarterly block quality reviews aligned with content model evolution
- **New Block Validation**: Governance and quality checks for new blocks entering the taxonomy
- **Surface Template Monitoring**: Track how template changes affect block composition
- **Metadata Schema Evolution**: Update assessment criteria as Block Support Knowledge Model evolves
- **Reference Integrity Monitoring**: Ongoing validation of block-to-block and Issue Card relationships

---

## 13. Integration with Block Support Knowledge Model

This DRIFT framework is designed to work seamlessly with the Block Support Knowledge Model's five-layer architecture:

### Layer Integration
- **Layer 1 (Content Types)**: Governance Drift validates the eight atomic block types
- **Layer 2 (Taxonomic Spine)**: Topic Drift ensures blocks align with Business Unit → Product → Topic → Issue hierarchy  
- **Layer 3 (Attributes)**: Audience Drift validates metadata consistency across common base fields and type-specific extras
- **Layer 4 (Composition)**: Governance Drift validates reference patterns and Issue Card relationships
- **Layer 5 (Surfaces)**: Template Drift ensures surface components are filled by appropriate block types

### Model Evolution Support
As the Block Support Knowledge Model evolves, this DRIFT framework can adapt by:
- **Adding new content types** to the approved taxonomy in Governance Drift criteria
- **Updating surface templates** in Template Drift component structure requirements
- **Expanding metadata fields** in Audience Drift metadata validation checks
- **Refining composition rules** in Governance Drift reference pattern validation
- **Adjusting style standards** as content type definitions mature

The framework's fundamental commitment aligns with the model's: **one definition, many surfaces**. Quality drift assessment ensures that as blocks are reused and recombined across surfaces, they maintain the standards that make the modular system reliable and effective.
