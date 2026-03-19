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
>Note: Sources
"Vetted Source" or "Constrained Domain." The goal is to force the AI to cite from a specific .mil domain, an uploaded .pdf of a unclassified GAO report, or a specific .gov press release. 

>Note: TRAINING SCENARIO ONLY. All names, dates, and data are fictitious. In real-world planning, you must ensure any information you input is unclassified and approved for use in this tool. When in doubt, ask your security officer.

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

## Task 2.2 — Catching and Preventing Hallucinations (20 min)

AI hallucinations are responses that sound authoritative but contain fabricated facts — invented statistics, nonexistent agreements, or fictional events. In a DOD environment, an undetected hallucination in a Commander's brief or policy memo can have serious consequences. This task teaches you to trigger, detect, and prevent them.

### Part A: Trigger a Hallucination

Enter this prompt that asks for very specific details about something obscure:

```
What were the specific outcomes and signed agreements from the
U.S.-Tuvalu Joint Security Dialogue held in March 2025? List the
agreement names, signatories, and key provisions.
```

**Examine the response carefully:**
- Does Copilot present specific agreement names and details confidently?
- Click on the source links (if any). Do they actually support the claims?
- Are there any hedging phrases like "reportedly" or "according to sources" that might mask uncertainty?

> **Key insight:** Copilot may generate plausible-sounding agreement names, dates, and provisions that do not exist. The more specific and obscure your question, the higher the hallucination risk.

### Part B: Detect the Hallucination

Now challenge Copilot on its own answer:

```
I need to verify that information before it goes into a briefing.
How confident are you in the specific agreement names and provisions
you listed? Can you confirm each one with a direct source URL?
```

Observe how Copilot responds. It may:
- Acknowledge uncertainty
- Revise or retract specific claims
- Provide sources that don't actually match the details

### Part C: Prevent Hallucinations with Better Prompts

Now rewrite the original prompt using **anti-hallucination techniques**:

**Technique 1 — Constrain to known sources:**
```
Based only on publicly available U.S. Department of State and
Department of Defense press releases, summarize any known U.S.
security cooperation activities with Tuvalu. If there is limited
public information available, say so rather than speculating.
```

**Technique 2 — Demand source attribution inline:**
```
Describe the current state of U.S.-Pacific Island nation security
partnerships. For each claim, include the source name and date
in parentheses. Do not include any information you cannot attribute
to a specific source.
```

**Technique 3 — Upload an authoritative document instead of relying on web grounding:**
```
Using only the attached document, summarize the key bilateral
security agreements discussed. Do not add information from outside
this document.
```
*(You can test this by uploading the file `assets/HADR-After-Action-Report.md` and asking Copilot to summarize only from that file.)*

### Part D: Apply to a Real-World Scenario

You are drafting a briefing slide that states: *"The U.S. has conducted 47 bilateral exercises with the Philippines since 2015."*

Enter this prompt to fact-check:
```
How many bilateral military exercises have the U.S. and Philippines
conducted together since 2015? Provide only information you can
attribute to specific sources. If the exact count is not available
from public sources, state that clearly and give the best available
estimate with your confidence level.
```

> **Rule of thumb for INDOPACOM staff:**
> - **Always check sources** on any specific numbers, dates, names, or quoted statements.
> - **Never put Copilot output directly into a briefing** without verification — treat it as a first draft from a new analyst who needs to be checked.
> - **When accuracy is critical, upload the source document** and constrain Copilot to that document rather than relying on web search.
> - **Add "if you're unsure, say so"** to any prompt where fabricated details would be harmful.

---

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
- Check at least two of the source links.
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

1. In Copilot Chat, select **"See more"** under the initial prompt suggestions.
2. Select the **Prompt Gallery** button at the bottom of the list.
3. Browse and find one prompt in each category you could adapt for INDOPACOM work:
   - **Summarize** — for operations briefs
   - **Create** — for drafting memos
   - **Analyze** — for reviewing exercise data
4. **Save** at least one prompt and **edit** it to tailor for military context.

---

## Checkpoint

Before moving on, confirm you can:

- [ ] Write prompts using all four key elements (Goal, Context, Source, Expectations)
- [ ] Trigger, detect, and prevent AI hallucinations
- [ ] Apply anti-hallucination techniques: source constraining, inline attribution, document upload, and confidence-level requests
- [ ] Iteratively refine Copilot responses through follow-up prompts
- [ ] Identify and fix common prompting mistakes
- [ ] Navigate the Prompt Gallery and save/edit prompts
