# Cash App Contentful Quick Text Guide

*Source: https://docs.google.com/document/d/1RKMlmBMzSXqCpZ94qzbbqKiSbjZEb6NGJ1pz-i-VXnI/edit*

**Audience:** Content Operations  
**Applies to:** All Cash App Support channels  
**Last updated:** August 2025

## 🔍 Overview & Purpose

Quick Texts are standardized, pre-written responses used by Cash App Support across all channels to ensure fast, consistent, and accurate communication with customers. Retrieved from CF1 and tailored to each case, QTs help:

- Deliver consistent, policy-compliant messaging
- Reduce drafting time
- Guide support teams with clear, conversational scripts
- Streamline customer actions with embedded links

## ✅ Summary 

When drafting QTs:

- Use the template outlined in this document
- Follow tone and style guidelines
- Replace steps with action links when possible (Chat ONLY)
- Keep everything short, clear, and helpful

**Quick Reference:**

- **Naming format:** Cash App {Product/Workstream - Topic - Subtopic, if needed}
- **Length:** 2-3 sentences, max 100 words (excludes action links)
- **Always start email Quick Texts with:** Hi {!Contact_FirstName},
- **Include:** [Empathy and/or acknowledgement] + [Clear, actionable solution or next step]

💡**Pro-tip:** Use Goose to validate your drafted QT(s) against this template at [go/QTvalidation](http://go/qtvalidation)

## 🧩 Essential Components

### Naming Conventions

Use clear, searchable names. Include relevant category/topic. Use the following format for naming conventions: **Cash App {Product/Channel - Topic - Subtopic}**

**Examples:**
- Cash App {Direct Deposit - Setup}
- Cash App {Messaging - Transfer to Email}
- Cash App {Card - ETA - Lost in Transit}

| Component | Example | Purpose |
|-----------|---------|---------|
| Brand | Cash App | Identifies the product |
| Product/Channel | Direct Deposit | Main category |
| Topic | Setup | Primary issue/action |
| Subtopic (if needed) | | Further specification |

### Format Requirements

**Format:**
- Start with: Hi {!Contact_FirstName},
- Pattern: [Empathy or Acknowledgement] + [Clear, actionable next step or solution]

**Length:**
- 2–3 sentences
- Max 100 words* (excludes action/hyperlinks). This translates to 500-600 characters on average, with our tooling max character limit count as 4,000

*NOTE: Exceptions to the word count limit apply, particularly for content containing mandatory regulatory/compliance information. Use your best judgment and look for opportunities to condense communication where possible. AI tools are available to help optimize content length while maintaining essential information.

### Links 

We have two different QT body types–Email and Chat–and they interact with tooling differently, especially links. Below are all the available options for linking:

#### Action Links–CHAT ONLY 
- Use approved link format: {action: name=LinkName}
- Example: "You can reset your PIN {action: name=ResetPIN} if you've forgotten it."
- Replace multi-step processes with single action links
- Do not add more than 1–2 links per QT
- Embed links naturally in the sentence
- Provide fallback instructions for non-clickable scenarios

💡**Pro-tip:** For a complete guide to all QuickText formatting options, reference [Toolbox Chat QuickText Guide](https://docs.google.com/document/u/0/d/12DPx5yOJLxC-iw8FOc6TeYXCf5Hnu5u1ANcgeaVU0oc/edit) to create more user-friendly Quick Texts. This comprehensive resource covers additional features like:

- Message breaks for splitting content
- Formtext fields for customizable inputs
- Formtoggle sections for optional content
- Placeholder syntax using ZZZZZ markers

#### Hyperlinks
Always use Contentful's native, rich-text hyperlinking functionality for Quick Texts.

**Macro body:** In the macro body, Contentful will apply markdown formatting to hyperlinks. Please do not manually try to replicate markdown formatting.

**Other references:** In all other instances of linking, the rich text editor will hyperlink unique text. When possible, try to embed the link within the sentence versus at the end.

Either way, please ensure that sentence punctuation is not included in the hyperlink, as it can break the link.

**Guidelines:**
- Link using a full title
- Depending on the scenario, this could mean linking the name of an action, product, page, or surface
- On average, hyperlinked text should be between 1-4 words
- Avoid generic terms like "click here"
- Do not list out URLs in full, use unique text
- Links will display as duplicates if plain text URLs are linked instead of proper hyperlinking

**Language codes:** Avoid hyperlinks that include a language code (such as /en-us/ for english), as this forces the article to load in that specific language. Instead, use language neutral hyperlinks. This allows a user's browser to determine the language.

As a best practice ensure language codes are removed from the URL before hyperlinking.

**For Example:**
- ❌ https://cash.app/help/us/en-us/3127-keeping-your-cash-app-secure → Forces the article to load in English
- ✅ https://cash.app/help/us/3127-keeping-your-cash-app-secure → Allows the browser to determine the language

#### SendSafely Links

If you need to include a SendSafely link in a QT, use the following formatting: {!Case.SendSafely_URL_Type}.

- Use [How to Get Code for SendSafely Links](https://docs.google.com/document/d/1IWj-_m9L3sVSXSi66jEZeXQu5HgvA-ER9ti2OTndaXw/edit?tab=t.0) to locate the Sendsafely link type you need
- Reference existing, related QTs for further help with the link you need
- To create a new link, you'll need to work with your project stakeholders and file a [Jira](https://block.atlassian.net/browse/CBS-3359) with CSSE

## ✍️ Writing Guidelines

**Tone & Style:**
- Warm, supportive, calm
- Solution-oriented and clear
- Present tense
- Conversational (avoid overly formal language)
- Avoid technical jargon
- Emotionally appropriate
- Sentence case

### Example with Analysis:

"Hi Kelly, I see your Cash App Card order was approved—cards typically arrive within 14 days. Once it arrives, you'll need to activate it in the app before using it. You can do so here: {action: name=ActivateCard}"

| Standard | Implementation | Example/Notes |
|----------|----------------|---------------|
| **Structure & Format** | ✅ Start with greeting<br>✅ 2-3 sentences (30 words)<br>✅ Uses action link | "Hi Kelly"<br>Clear, concise message<br>{action: name=ActivateCard} |
| **Tone & Style** | ✅ Warm & supportive<br>✅ Present tense<br>✅ No jargon | Friendly acknowledgment<br>"is approved, arrives, need"<br>Plain, clear language |
| **Content Principles** | ✅ Lead with empathy<br>✅ Simplify steps<br>✅ Build trust<br>✅ Clarify next steps | Acknowledges approval<br>Uses action link<br>Clear timeline given<br>Specific activation instruction |

## 🔄 Process & Workflow

### When to Create a QT
- Recurring issue needs consistent responses
- Workflow with multiple steps can be simplified
- New product/policy requires templated support
- Support teams writing similar messages repeatedly

### When to Update a QT
- Product flow or policy has changed
- Tone or structure is outdated
- Action link now replaces steps
- Support teams feedback indicates confusion

### When to Archive a QT
- Feature or product is deprecated 
- Promotion, experiment, or campaign is over 
- Policy updates make it obsolete
- Redundant or superseded by another QT
- Low usage of less than 1,000 times in a year

### Content Operations Responsibilities
- Scope and prioritize QT needs
- Draft and review content
- Coordinate SME and policy input
- Publish and maintain QTs in Contentful
- Audit QTs for usage, accuracy, and compliance

## ✏️ Template

Use this template when drafting new QTs:

### QT: 
Cash App {Product/Workstream - Topic - Subtopic, if needed}

### Status: 
🟡

### Use Case: 
Provide the purpose of this QT

### Email:
Hi {!Contact_FirstName},

[Empathy or acknowledgement] + [Clear, actionable solution or next step]
Length: 2-3 sentences, max 100 words 

### Messaging
Hi {!Contact_FirstName},

[Empathy or acknowledgement] + [Clear, actionable solution or next step]
Length: 2-3 sentences, max 100 words (excludes action links)

### Example:

**QT:** Cash App {Card - ETA}

**Status:** 🟡

**Use Case:** To confirm a successful Cash App Card order and provide ETA for physical card to arrive

**Email:**
Hi Kelly,

I see your Cash App Card order was approved—cards typically arrive within 14 days. Once it arrives, you'll need to activate it in the app before using it.

**Messaging:**
Hi Kelly, I see your Cash App Card order was approved—cards typically arrive within 14 days. Once it arrives, you'll need to activate it in the app before using it. You can do so here: {action: name=ActivateCard}

## 🧠 Additional Best Practices

- Keep it brief—support teams can customize if needed
- Use placeholders for variables (e.g., {!Contact_FirstName})
- Test all action links before with a staging account publishing
- Collaborate with SMEs to validate accuracy
- Track usage to inform updates and deletions

## 📚 Related Resources

- [SD_Content Scoping Template (Make A Copy)_#####](https://docs.google.com/document/d/1w-U6jDHT6zV6nL2nLxNJsKLSrw331A7us-3BA4zXsEM/edit?tab=t.u8j6frnqv9)
- [TKO: Quality](https://docs.google.com/document/u/0/d/1Wb4CnZlvGtCWc6ynwaMWY7c1S_TeemaOBy2qZYUwBkg/edit)
- [Unified Support Content Style Guide](https://docs.google.com/document/u/0/d/1597tA9YdQmYkDEO7YLqJh1HGUGHgJ5gFp4NxYeNs6OY/edit)
- [Toolbox Chat QuickText Guide](https://docs.google.com/document/u/0/d/12DPx5yOJLxC-iw8FOc6TeYXCf5Hnu5u1ANcgeaVU0oc/edit)
- [Messaging Action Buttons (Updated 11.2024)](https://docs.google.com/document/u/0/d/1PdJ7WhNWWtUS6cO3v5MAxCohzfOC4e242LaOTHZdfMg/edit)
- [How to test Chat Quick Texts using Textblaze](https://docs.google.com/document/d/1cIZG6uG50QrxuGt-Xfr7RPrnqpDDr8fDzr4fR1kPLOQ/edit?tab=t.0)