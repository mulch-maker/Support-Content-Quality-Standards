# Square How-to Article Template

*Source: https://docs.google.com/document/d/1jqw8_kpFcao5nW3ujSspAB_9uSbQwuMJxZdNSpZgB2I/edit*

This documentation serves as a guide and drafting document for a how-to article in the Project Blueprint playbook.

⚠️ **Make a copy to use as drafting document** ⚠️

## Global Guidance

Guidance to support article creation.

### Principles
- **One article, one purpose**
- **Keep it short** (~650 words or less)
- **Headings are critical** — make it easy to scan
- **Be clear about where sellers can complete instructions**
- **Use good hyperlink hygiene**

### Hyperlink Hygiene

Hyperlinks are doorways to related URLs. To support usability, we should follow some guidelines.

#### When linking to another support article
- Sentence case
- Use full title of article when possible
- Preface with the directive "Learn how to"
- **Example:** Learn how to [create and edit items](https://squareup.com/help/article/8335).
- Where not possible to use an article title (like in a list), add link to 1 word, or 1 feature or product name (e.g. "service charges")
- Do not link to text such as 'here' or 'learn more'
- Limit hyperlinks to a few key articles that answer anticipated questions or teach about a related feature

#### When linking to Dashboard
- Use in instruction items only
- Preferably in the first instruction item, which often directs to a surface
- Preface with the directive "Sign in"
- Use proper name of target surface — Square Dashboard
- Link on the ending destination level (like "Item library")
- **Example:** Sign in to your Square Dashboard and go to Items & services (or Items & menus or Items & inventory) > Items > [item library](https://app.squareup.com/dashboard/items/library).

### Callout Hygiene

When adding callouts via the secondary notification fragment, be sparing and discerning in when/how you use them. Use cases include:

- **Blocking actions**
- **Contacting support** - Use a callout box to indicate when they will need to contact support, like if they completed all self-serve troubleshooting steps they can independently
- **Downstream effects** - Warn sellers that an action they take may have downstream effects
- **Actions with impact on payments, data, etc.** - Updating transfer schedule/settings may take a few days to come into effect

## Article Structure

### Typical Outline
This is a typical outline for a how-to article. Scanning the title and headings should represent the full narrative arc of the article.

1. **Title**
2. **Who is this article for**
3. **About (feature overview)**
4. **Before you begin (critical context)**
5. **Option 1 (or Step 1)**
6. **Option 2 (or Step 2)...**
7. **Square for RST POS**
8. **Square Dashboard**
9. **Related articles**

## Content Components

### 1. Title

**Guidance:**
- Describe content
- Always a verb phrase
- Use invisible "how to" in front of title
- Use vertical product name when contextualizing shared feature for a vertical
- **Example:** Schedule your team with Square for Restaurants
- One article, one purpose: title should reflect a single task
- Sentence case

### 2. Who is this article for?

**Purpose:** Explain who, what, why

Use the primary notification fragment with heading to highlight this block. Answer the question "who completes the task?"

**Structure:**
- **Header:** Who is this article for?
- **Body:**
  - **Line 1: Permissions** (Include if needed)
    - Choose appropriate option:
      - Account owners or team members with the [category] permission to [specific permission]. Set permissions in Square Dashboard.
      - Account owners or team members with [category] permissions. Set permissions in Square Dashboard.
      - Only account owners can [task].
      - Only account owners can [task]. Sellers with the [category] permission to [specific permission] can [task]. Set permissions in Square Dashboard.
      - Account owners or team members can [task]. Only account owners can [task].
      - Customers who purchase from Square sellers.
  
  - **Line 2: Legacy subscriptions**
    - [Legacy subscription name] subscribers
    - **Example:** Square for Restaurants Plus and Premium subscribers
  
  - **Line 3: P&P subscriptions and advanced capabilities** (Include if legacy information is included, or if the feature is now behind a SQ1 paywall)
    - P&P is only available in the US. Do not include P&P info on non-US articles.
    - Choose appropriate option:
      - Square Free, Square Plus, and Square Premium subscribers
      - Square Plus and Square Premium subscribers
      - Square Premium subscribers
    - Add advanced capabilities if needed: "... with advanced [restaurants/inventory/bookings] capabilities added. Add capabilities in Square Dashboard."
  
  - **Line 4: Modes** (Only include if referencing a POS task)
    - Include all POS modes they can enable to accomplish the task
    - Modes should be lowercase
    - **Style:** Sellers with [full service/bar/quick service/retail/bookings/services] mode enabled in the Square Point of Sale app.

### 3. About this feature

**Content guidance:**
- Briefly define the feature
- Briefly explain how feature is used (1-2 sentences)
- Address anticipated common questions to promote understanding, such as company terms or multiple instances/tiers of feature
- If a sibling article already has this content, copy it

**Style guidance:**
- Use the h2 About [PRODUCT/FEATURE]
- Don't hyperlink within this section
- Use present tense when possible

### 4. Critical context

Set expectations that prepare sellers to follow instructions.

**Include information around:**
- Surfaces & options to complete tasks
- Other needed hardware
- Prior necessary setup tasks
- Location & time frame contingencies

**Style guidance:**
- Use the h2 Before you begin
- Bulleted lists facilitate easy scanning and sense-making
- Use present tense when possible
- Use a building block approach for body content following this order:

#### Building Block Structure:

**Surfaces and options:**
- If multiple options: "You have # options to complete [task]: option 1 w/ surface, option 2 w/ surface"
- If one option: "You can [task] from your [surface(s)]."

**Other needed hardware:**
- "You also need [other hardware]. Learn how to [related hardware setup article]."

**Prior necessary setup tasks:**
- "You also need to already have [feature/task] [done/set up/enabled]. Learn how to [article w/link]."

**Location & time frame contingencies:**
- "To [task], you need to be [location.]"
- "Avoid/complete [task] during [time of day/location] because [effect]."

### 5. Instruction Lists

A set of steps to complete a task.

**Content guidance:**
- For clarity, aim for 1 level of hierarchy, or a maximum of 2
- Two levels of hierarchy are generally used when instructions can be completed on more than one surface
- Include brief introductory text explaining where the instructions will be completed and any required materials or information to have on hand
- Include brief concluding text that explains what sellers should see, do, or know after completing instruction list

**Style guidance:**
- Headers take sentence case
- Often written as Option 1:... or Step 1:...
- Use h2s for headers in Contentful
- Use present tense when possible

### 6. Instruction Steps

**Content guidance:**
- Describe a single step within an instruction list

**Style guidance:**
- Use ordinal numbers
- Use present tense when possible
- Bold UI text that sellers will interact with
- Begin with verbs

**Mode order (as needed):**
1. Full service
2. Quick service
3. Bar
4. Retail
5. Bookings
6. Services
7. Standard

**For Dashboard instructions:**
- Use: "Sign in to Square Dashboard..."
- List the full path of navigation in step 1
- When linking, make the hypertext the name of the final destination and link to the final destination listed in the step
- **Example:** Sign in to Square Dashboard and go to Appointments > Calendar.

**For app instructions:**
- Use: "Open the [POS app] and tap..."
- List SuperPOS modes first using the mode hierarchy, followed by the legacy apps
- **Style:** "From your Square Point of Sale app in [listed modes] mode or your [related legacy app(s)]: Open your app and select..."

### 7. Instruction Sections

**Content guidance:**
- Create two-level section to give instruction list for two or more surfaces (e.g. Dashboard and POS app)
- Header should follow instruction list guidance
- Use accordion fragment
- Label header in accordion the proper name of the surface

**Style guidance:**
- Use instruction list and step styles inside each accordion section
- Use an introductory sentence to explain the options
- Use present tense when possible

### 8. Related Articles List

Provide additional articles related to this article.

**Guidelines:**
- Use the h2 Related articles
- Choose articles from:
  - The same subtopic of the IA as the primary article
  - Another topic or subtopic if the article is about a task with a prerequisite task in another topic, or about a task that enables a task in another topic
- Use bulleted list

### 9. Related Articles Items

**Guidelines:**
- Provide single link in the text
- Provide only full title of target article
- Hyperlink full title
- Limit items to 5 or less