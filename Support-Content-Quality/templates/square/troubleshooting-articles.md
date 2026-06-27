# Square Troubleshooting Article Template

*Source: https://docs.google.com/document/d/17zdvfXneswISC3aK_77dWpxlDGC52QhC32mVg6mkwyQ/edit*

This documentation serves as a guide and drafting document for a troubleshooting article in the Project Blueprint playbook.

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

#### When linking to a related article
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

## Article Structure

### Typical Outline
This is a typical outline for a troubleshooting article. Scanning the title and headings should represent the full narrative arc of the article.

1. **Title**
2. **Feature overview**
3. **Before you begin**
4. **Option 1 (or Step 1)**
5. **Option 2 (or Step 2)...**
6. **Square POS apps**
7. **Square Dashboard**

## Content Components

### 1. Title

**Guidance:**
- Describe content
- Always begin with "Troubleshoot"
- Use plain language to describe the issue
- One article, one purpose: title should reflect a single task
- **Example:** Troubleshoot Missing Orders with Square KDS

### 2. Issue Overview

**Purpose:** Identify issue for the seller

**Guidelines:**
- Limit to single paragraph; 1-3 sentences
- Use present tense when possible

**Example:**
"If your orders placed on Square Point of Sale or Square for Restaurants are not appearing on your Square KDS, it can be a stressful experience for both your customers and staff."

### 3. Article Purpose

**Purpose:** Explain who, what, why

**Guidelines:**
- Link to any related concepts that are likely to answer anticipated questions
- When possible, provide reassurance to seller that issue can be resolved
- For urgent information or blocking action, call out in a secondary notification without heading
- Use present tense when possible

**Example:**
"This article provides advanced troubleshooting for your point of sale and Square KDS. Most issues can be resolved with the suggested troubleshooting steps below — to avoid hiccups in service and get you back to business.

This article is about missing orders. If your issue is duplicate orders appearing on your KDS, contact Square support."

### 4. Before You Begin

**Purpose:** Set expectations that prepare sellers to follow instructions

**Guidelines:**
- Use header "Before you begin"
- Explain any requirements or constraints; permissions should be addressed in purpose section
- Address anticipated questions about the troubleshooting process such as timing and data loss
- Limit paragraphs to 1-2 sentences

**Style guidance:**
- If using headers, use noun phrases and sentence case; avoid header text that is constructed as a question
- Bulleted lists facilitate easy scanning and sense-making
- For urgent information or blocking action, call out in a secondary notification without heading
- Use present tense when possible

**Example sections:**

#### When to troubleshoot
"If at all possible, try to troubleshoot your Square KDS and points of sale during after hours. If you must troubleshoot during the workday, try to avoid peak busy hours so your customers will experience few delays."

#### Multiple Points of Sale and Square KDS stations
"If you are missing orders on multiple stations, you'll need to troubleshoot each Point of Sale device connected to a Square KDS separately."

#### Saving data while troubleshooting
"It depends on whether your payments have been captured or not. If you are using Offline Mode, be sure to connect your offline devices to the internet to capture any unsettled payments."

### 5. Instruction Section

**Purpose:** Create two-level section to give instruction lists for 3 or more steps

**Guidelines:**
- If only two steps, consider instruction lists without section
- Construct header for section with relevant troubleshooting action verbs
- Use introductory paragraph to set context for steps and promote understanding
- Order steps from least invasive to most invasive

**Style guidance:**
- Use accordion fragment
- Header should use "Step #:" followed by verb phrase
- Use present tense when possible

### 6. Instruction Items

**Purpose:** Describe a single step within an instruction list

**Style guidelines:**
- Use ordinal numbers
- Begin with verbs
- Bold UI text that sellers will interact with
- Use present tense when possible

**For Dashboard instructions:**
- Use: "Sign in to Square Dashboard and go to..."
- List the full path of navigation in step 1
- When linking, make the hypertext the name of the final destination and link to the final destination listed in the step
- **Example:** Sign in to Square Dashboard and go to Appointments > Calendar.
- For paths that start at the Items & services or Orders & payments L1, use the standard name with the vertical specific names in parentheses
- **Example:** Sign in to Square Dashboard and go to Items & services (or Items & menus or Items & inventory) > Inventory > Items.

**For point of sale app instructions:**
- List SuperPOS modes first using the mode hierarchy, followed by the legacy apps
- **Style:** "From your Square Point of Sale app in [listed modes] mode or your [related legacy app(s)]: Open your app and select..."
- If two sets of instructions take place within a single kramdown, don't repeat the surface link within the kramdown
- If all modes and legacy apps use the same steps, use "Point of sale app" for the accordion header and do not specify modes or legacy names in the instructions

## Example Troubleshooting Structure

### Troubleshoot missing orders

The steps below are listed in order of least to most time intensive. If the first step solves the issue, there is no need to continue troubleshooting. If the issue is not resolved, follow the instructions in sequential order.

#### Step 1: Validate Your Device Codes
Check your device codes to make sure you are signed in to the correct location on your POS/Square KDS with the matching device code and nickname you previously set up on your Square Dashboard for that device.

#### Step 2: Confirm your Square KDS Settings are configured correctly
If you have created categories for your items, check that: A) your items are assigned to the correct category and B) categories are assigned to route orders to your preferred expo (KDS) station.

#### Step 3: Restart your KDS and POS devices
Restarting all of your devices and updating software may require your POS or expo (KDS) stations to be unavailable for taking orders. Using written paper tickets can make troubleshooting less stressful while your staff serves your customers in the meantime.

**Note:** Restarting your device will not erase your settings or open orders.

#### Step 4: Update your KDS and POS devices with the latest software
To make sure the Square app runs smoothly and to access the newest features and fixes, update to the latest version of software available for your device.

#### Step 5: Test the POS connection to your KDS
Take a trial order to double check that your KDS is properly receiving orders from the Point of Sale (either Square Point of Sale or Square for Restaurants POS).

### 7. Related Articles List

**Guidelines:**
- Use the h2 Related articles
- Choose articles from:
  - The same subtopic of the IA as the primary article
  - Another topic or subtopic if the article is about a task with a prerequisite task in another topic, or about a task that enables a task in another topic
- Use bulleted list

### 8. Related Articles Items

**Guidelines:**
- Provide single link in the text
- Provide only full title of target article
- Hyperlink full title
- Limit items to 5 or less