# Exercise 2: Writing Effective Prompts for Military Operations
**Module 2 | Estimated Time: 75 minutes**

---

## Scenario  

As a staff officer at USINDOPACOM, you write and consume dozens of documents each week — briefings, reports, talking points, and analysis. The quality of what Copilot produces depends entirely on the quality of your prompts. In this exercise you will practice the five key prompt elements

- Role
- Goal
- Context
- Source
- Expectations

This exercise will help you learn to detect and prevent AI hallucinations, and use scenarios you encounter regularly.

---
>**Note:** Sources
"Vetted Source" or "Constrained Domain." The goal is to force the AI to cite from a specific .mil domain, an uploaded .pdf of a unclassified GAO report, or a specific .gov press release. 

>**Note:** TRAINING SCENARIO ONLY. All names, dates, and data are fictitious. In real-world planning, you must ensure any information you input is unclassified and approved for use in this tool. When in doubt, ask your security officer.

---

## Task 2.1 — Anatomy of a Good Prompt (15 min)

### Part A: Compare Weak vs. Strong Prompts

Enter this **weak prompt** into Copilot Chat:

```
Tell me about disaster relief.
```

Now enter this **strong prompt** that uses all five elements:

```
I am a J3 operations planner at USINDOPACOM preparing a briefing for
the Deputy Commander. Summarize the key phases of a multinational
humanitarian assistance and disaster relief (HA/DR) operation in the
Pacific region. Focus on coordination between U.S. military forces and
host-nation agencies. Present the response as 4-5 bullet points with
a one-sentence explanation for each phase. Use a formal military tone.
```

**Identify the five elements in the strong prompt:**

| Element | What it is in this prompt |
|---------|--------------------------|
| **Role** | I am a J3 operations planner at USINDOPACOM preparing a briefing for the Deputy Commander |
| **Goal** | Summarize the key phases of a multinational HA/DR operation |
| **Context** | J3 ops planner at INDOPACOM, briefing for Deputy Commander |
| **Source** | Web-based knowledge about Pacific HA/DR operations |
| **Expectations** | 4-5 bullets, one sentence each, formal military tone |

> **Discussion:** How did the quality and relevance of the two responses differ?

### Part B: Build Your Own

Write a prompt that includes all five elements for this scenario:

> You need to prepare talking points for a visiting delegation from a Pacific Island nation about the benefits of participating in a joint military exercise.

Enter your prompt into Copilot Chat and evaluate the response. Refine it at least once.

---

## Task 2.2 — Preventing AI Hallucinations (20–25 min)

AI systems can **overstate certainty, fill in missing data, or infer details that are not supported by sources**. In a DoD environment, this is especially dangerous — responses may *sound correct* while containing subtle inaccuracies that could mislead decision-makers.

This task teaches you **prompting best practices that reduce hallucination risk** and how to verify AI-generated content before using it.

---

### Understanding How Hallucinations Happen

AI hallucinations are not random — they follow predictable patterns. Knowing these patterns helps you write prompts that prevent them:

| Pattern | Example | Why It Happens |
|---------|---------|----------------|
| **Fabricated precision** | Inventing exact dollar figures or statistics | The model fills in plausible-sounding details when real data is unavailable |
| **False attribution** | Paraphrasing presented as a direct quote | The model generates text that *looks like* a quote but is reconstructed from training data |
| **Gap-filling** | Smoothing over missing dates in a timeline | The model prefers complete-looking answers over honest gaps |
| **Assumed causation** | Claiming one event caused another without evidence | The model infers causal links from correlation |
| **Confident uncertainty** | Stating unverified claims without hedging | The model defaults to an authoritative tone regardless of actual confidence |

---

### Part A: Constrain Your Sources (Practice)

The most effective way to prevent hallucinations is to **tell the AI where to get its information** and **what to do when information is unavailable**.

Try this prompt:

```
Act as a defense analyst. Summarize the current status of the
U.S.–Philippines Enhanced Defense Cooperation Agreement (EDCA).
Use only information from official U.S. Department of Defense or
Department of State public releases. If specific details such as
dates or figures cannot be confirmed from these sources, state
that clearly rather than estimating.
```

**Why this works:**
- “Use only information from...” constrains the source domain
- “If specific details cannot be confirmed... state that clearly” gives the model permission to say “I don't know”

> **Tip:** Constraining sources is even more effective when you **upload a document** (PDF, Word, or text) and instruct Copilot to answer only from that document.

---

### Part B: Require Source Attribution (Practice)

When you need factual content, **require the model to cite its sources inline**. This makes unverifiable claims easier to spot.

Try this prompt:

```
I am a J5 strategic planner at USINDOPACOM. List the major
multilateral military exercises the U.S. conducts annually in
the Indo-Pacific region. For each exercise, include the
participating nations and general purpose. After each entry,
note the source of the information. If you are unsure about
any detail, flag it as unverified.
```

**After receiving the response:**
- Check at least two of the cited sources — do they exist and support the claims?
- Did the model flag anything as unverified, or did it present everything with equal confidence?

> **Key insight:** If a model provides no sources or flags nothing as uncertain, treat the entire response with extra scrutiny.

---

### Part C: Allow and Encourage Uncertainty (Practice)

Models default to sounding confident. You can **explicitly invite uncertainty** to get more honest responses.

Try this prompt:

```
What is known from publicly available, unclassified sources about
the number of bilateral military exercises the U.S. conducted with
ASEAN nations between 2020 and 2024? Provide what is well-documented,
note where data is incomplete, and rate your overall confidence
(High / Medium / Low) for each claim.
```

**Compare that to this version without safeguards:**

```
How many bilateral military exercises did the U.S. conduct with
ASEAN nations between 2020 and 2024? Break it down by country
and provide a grand total.
```

> **Discussion:** How do the two responses differ in tone and specificity? Which would be more dangerous to use in a briefing without verification?

---

### Part D: Verify Quotes and Specific Claims (Practice)

Direct quotes and specific statistics are the **highest-risk content** for hallucination. Use this technique to reduce risk:

```
Summarize — do not quote — the key themes from recent U.S.
Department of Defense statements about the Indo-Pacific strategy.
Provide the approximate date and context for each statement.
Do not fabricate direct quotes. If you are paraphrasing, say so.
```

**Why this works:**
- Asking for summaries instead of quotes avoids the most common hallucination type
- “Do not fabricate direct quotes” sets a clear boundary
- “If you are paraphrasing, say so” forces transparency

> **Best practice:** If you need an exact quote, ask the model to find it, then **verify it yourself** before using it in any product.

---

### Part E: Ground Responses in Uploaded Documents

The strongest defense against hallucination is to **provide the source material directly**. When you upload a document, Copilot can answer from it rather than generating from memory.

**Try this workflow:**
1. Find an unclassified public document (e.g., a DoD fact sheet, a press release from defense.gov, or a GAO report summary)
2. Upload it to Copilot Chat
3. Use this prompt pattern:

```
Using only the attached document, summarize the key findings
in 4-5 bullet points. Do not add information from outside
this document. If the document does not address a topic,
state that explicitly.
```

> **This is the gold standard** for reducing hallucinations — the model works from your authoritative source rather than generating from its training data.

---

### Prevention Techniques Summary

Use these techniques in combination for the best results:

| Technique | Prompt Language |
|-----------|----------------|
| **Constrain sources** | *”Use only information from [specific source domain]”* |
| **Require attribution** | *”Cite the source for each claim”* |
| **Allow uncertainty** | *”If unsure, say so and rate your confidence level”* |
| **Avoid exact quotes** | *”Summarize — do not quote directly”* |
| **Ground in documents** | *”Answer only from the attached document”* |
| **Request verification flags** | *”Flag any claims that could not be verified”* |

---

### Operational Guidance

- Treat AI output as a **draft from a junior analyst** — always review before use
- Verify **all numbers, quotes, and timelines** against authoritative sources
- Prefer **partial truth over confident error**
- Require **sources before using content in briefings**
- When possible, **ground AI in uploaded authoritative documents**
- Use **multiple prevention techniques together** for highest-risk content

---

### Key Takeaway

You cannot eliminate AI hallucinations entirely, but you can **dramatically reduce them** through careful prompting. The most effective strategies are:
- **Constraining sources** so the model draws from known, reliable information
- **Requiring attribution** so unverified claims are easy to spot
- **Giving the model permission to say “I don't know”** so it does not fill gaps with assumptions

Your job is to **prompt defensively and verify before trusting**.




## Task 2.3 — Prompting for Intelligence Summaries (15 min)

Practice writing prompts that produce intelligence-style summaries. Enter each prompt and evaluate the output.

**Prompt 1 — Regional Threat Summary:**

```
Act as a defense analyst specializing in the Indo-Pacific region.
Provide a summary of current maritime security challenges in the
South China Sea. Structure the response with three sections:
(1) Key Actors, (2) Recent Incidents, and (3) Implications for
Regional Stability. Limit each section to 3-4 sentences. Cite
recent developments from the past 6 months.
```

**After receiving the response, apply what you learned in Task 2.2:**
- Check at least two of the source links or ask Copilot for them if necessary.
- Are the "recent incidents" actually recent, or is Copilot presenting older events as current?
- If any claims lack sources, flag them.

**Prompt 2 — Country Profile Brief:**

```
Create a one-page country profile brief for the Republic of Palau
suitable for a military commander's pre-visit read-ahead. Include:
geography, government type, population, GDP, military forces,
U.S. bilateral agreements, and key security concerns. Format as
a structured brief with headers and short paragraphs. For each
factual claim, note the source.
```

**Prompt 3 — Refine with Follow-up:**

```
Now reformat the Palau brief as a two-column layout with category
labels on the left and details on the right. Add a section on
climate-related security risks.
```

> **Tip:** When Copilot gives a good-but-not-perfect response, refine it rather than starting over. Iterative prompting saves time.

---

## Task 2.4 — Prompting for Operational Planning (15 min)

### Scenario: Joint Exercise Planning

You are helping plan **Exercise Pacific Sentinel 2026**, a multilateral exercise involving forces from the U.S., Australia, Japan, and the Philippines.

**Step 1 — Research:**

```
What are the most common types of military training events conducted
during multilateral exercises in the Indo-Pacific? List the top 8
event types with a brief description of each. Focus on exercises
involving the U.S., Australia, Japan, and the Philippines.
```

**Step 2 — Draft an Executive Summary:**

```
Using the training events you just described, draft a one-paragraph
executive summary for a fictitious Exercise Pacific Sentinel 2026.
The exercise takes place over 14 days in the Philippine Sea and
involves naval, air, and ground components. The purpose is to improve
interoperability and readiness for regional contingencies. Write in
formal military style suitable for a FRAGO or EXORD summary.
```

**Step 3 — Create a Timeline:**

```
Create a day-by-day schedule for Exercise Pacific Sentinel 2026
across the 14-day period. Organize it as a table with columns for
Day, Date (starting 15 Sep 2026), Phase, and Primary Training Event.
Include Reception/Staging in the first 2 days and an After Action
Review on the final day.
```

**Step 4 — Risk Assessment:**

```
Draft a background paragraph on the geopolitical context of the Philippine Sea for a public affairs document, citing only unclassified State Dept. releases
```

---

## Task 2.5 — Avoiding Common Mistakes (5 min)

Enter each of these **intentionally flawed prompts**, observe the poor results, then fix them.

**Flawed Prompt 1 — Too vague:**
```
Tell me about Pacific exercises.
```
**Fix it:** Add goal, context, source, and expectations.

**Flawed Prompt 2 — Conflicting instructions:**
```
Give me a detailed one-sentence summary of all INDOPACOM operations
since 2020 in bullet format as a single paragraph.
```
**Fix it:** Remove contradictions (detailed vs. one-sentence, bullets vs. paragraph).

**Flawed Prompt 3 — No format guidance:**
```
What should I know about RIMPAC?
```
**Fix it:** Specify your role, what aspect of RIMPAC, and desired format.

---
## Assume Unclassified, Public Data Only

For this training, all prompts assume you are using Copilot in a web-facing, unclassified environment. Do not enter any information that is not approved for public release. If you were using a DOD-specific, secure AI, the rules would be different—ask your security officer.

## Task 2.6 — Explore the Prompt Gallery (5 min)

1. In Copilot Chat, select **New chat**.

2. Select **"See more"** under the initial prompt suggestions.
3. Select the **Prompt Gallery** button at the bottom of the list.
3. Browse and find one prompt in each category you could adapt for INDOPACOM work:
   - **Summarize** — for operations briefs
   - **Create** — for drafting memos
   - **Analyze** — for reviewing exercise data
4. **Save** at least one prompt and **edit** it to tailor for military context.

---

## Checkpoint

Before moving on, confirm you can:

- [ ] Write prompts using all four key elements (Goal, Context, Source, Expectations)
- [ ] Apply prompting best practices to prevent AI hallucinations
- [ ] Use anti-hallucination techniques: source constraining, inline attribution, document upload, and confidence-level requests
- [ ] Iteratively refine Copilot responses through follow-up prompts
- [ ] Identify and fix common prompting mistakes
- [ ] Navigate the Prompt Gallery and save/edit prompts