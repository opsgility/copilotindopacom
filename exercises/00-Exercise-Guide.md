# USINDOPACOM Microsoft 365 Copilot Chat — Hands-On Exercise Guide

**Course:** Transform Ideas into Action with Copilot Chat (MS-4023)
**Duration:** 4 Hours
**Classification:** UNCLASSIFIED
**Date:** April 2025

---

## Overview

This exercise guide accompanies the MS-4023 slide deck and provides hands-on, scenario-based exercises tailored for USINDOPACOM personnel. All exercises use fictitious but realistic military scenarios relevant to Indo-Pacific operations.

> **Important:** All data in these exercises is UNCLASSIFIED and fictitious. Do not enter classified or sensitive information into Copilot Chat.

### GCC High Environment Notes

These exercises are designed for **GCC High** environments. The following features referenced in the standard MS-4023 course are **not available** in GCC High and have been removed or adjusted:

| Feature | Status in GCC High | Exercise Impact |
|---------|-------------------|-----------------|
| Copilot in Edge sidebar | Not available | Removed from Exercise 1 access points |
| Web grounding | Not enabled by default (admin must enable) | Instructor note added to Exercise 1 |
| Copilot in PowerPoint (slide generation, speaker notes, summaries) | Not available | Exercise 3 uses Copilot Chat to generate content, then manual PowerPoint build |
| Copilot Agents (Researcher, Analyst, custom agents) | Not available | Removed from exercises |
| Teams Meeting Copilot | Not available | Removed from exercises |
| Copilot in Teams chat/channels | Not available | Removed from exercises |
| Schedule with Copilot (Outlook) | Not available | Not exercised |
| Clean Data with Copilot (Excel) | Not available | Not exercised |
| Copilot in Excel with Python | Not available | Not exercised |

---

## Schedule

| Time Block | Duration | Activity | Slide Reference |
|-----------|----------|----------|-----------------|
| 0800-0830 | 30 min | **Module 1 Lecture** — Get started with Copilot Chat | Slides 2-12 |
| 0830-0900 | 30 min | **Exercise 1** — Getting Started | Slide 12 |
| 0900-0915 | 15 min | Break | |
| 0915-1000 | 45 min | **Module 2 Lecture** — Write effective prompts + Hallucinations & Reliability | Slides 13-23 |
| 1000-1115 | 75 min | **Exercise 2** — Writing Effective Prompts for Military Operations (includes hallucination detection) | Slide 23 |
| 1115-1130 | 15 min | Break | |
| 1130-1200 | 30 min | **Module 3 Lecture** — Work smarter with Copilot Chat | Slides 24-38 |
| 1200-1400 | 120 min | **Exercise 3** — Plan a Joint Readiness Review | Slide 35 |
| 1400-1415 | 15 min | **Wrap-up and Q&A** | |

**Total instruction + exercise time:** ~4 hours (with 45 min of breaks)

---

## Exercise Summary

### Exercise 1: Getting Started with Copilot Chat (30 min)
**File:** `Exercise-1-Getting-Started.md`
**Module:** 1 — Get started with Microsoft 365 Copilot Chat
**Topics covered:**
- Accessing Copilot Chat from multiple entry points
- Navigating the interface
- Entering prompts, checking sources, refining responses
- Enterprise Data Protection awareness

### Exercise 2: Writing Effective Prompts for Military Operations (75 min)
**File:** `Exercise-2-Effective-Prompts.md`
**Module:** 2 — Write effective prompts to achieve optimal results
**Topics covered:**
- The four prompt elements: Goal, Context, Source, Expectations
- **Catching and preventing AI hallucinations** (Task 2.2 — 20 min dedicated)
  - Triggering a hallucination with an obscure military query
  - Detecting fabricated facts by challenging Copilot and checking sources
  - Anti-hallucination techniques: source constraining, inline attribution, document upload, confidence requests
  - Applying verification to real-world briefing scenarios
- Writing prompts for intelligence summaries and country profiles
- Prompts for joint exercise planning (Pacific Sentinel 2026)
- Identifying and fixing common prompting mistakes
- Using and customizing the Prompt Gallery

### Exercise 3: Work Smarter — Plan a Joint Readiness Review (120 min)
**File:** `Exercise-3-Work-Smarter.md`
**Module:** 3 — Work smarter with Copilot Chat
**Topics covered:**
- Research and brainstorming with Copilot Chat
- Drafting formal military documents in Word
- Analyzing budget data in Excel
- Drafting correspondence in Outlook
- Generating briefing content via Copilot Chat for manual PowerPoint build
- Collaborating with Copilot Pages

---

## Required Assets

The following files are provided in the `assets/` folder:

| File | Used In | Description |
|------|---------|-------------|
| `JRR-Budget-Data.csv` | Exercise 3, Task 3.3 | INDOPACOM directorate budget data for Excel analysis |
| `HADR-After-Action-Report.md` | Exercise 2, Task 2.2 / Exercise 3 | Fictitious HA/DR AAR for summarization and anti-hallucination practice |
| `Theater-Security-Cooperation-Activities.csv` | Exercise 2 (bonus) / Exercise 3 | 2026 theater exercise schedule for analysis and planning |

---

## Prerequisites

- Microsoft 365 work account with Copilot Chat access (GCC High: M365 F1/F3/G3/G5 or Office 365 F1/F3/G3/G5)
- Web browser (Microsoft Edge recommended)
- Access to Microsoft Teams, Word, Excel, Outlook, and PowerPoint
- Web grounding enabled by admin (GCC High: "Allow web search in Copilot" policy must be turned on)
- These exercise files (printed or available digitally)

---

## Tips for Participants

1. **Do not enter classified information** into Copilot Chat. All exercises use unclassified fictitious data.
2. **Experiment freely.** The best way to learn is to try different prompts and see what works.
3. **Iterate.** If the first response isn't perfect, refine your prompt rather than starting over.
4. **Verify before you trust.** Always check Copilot's sources — especially for specific numbers, dates, names, and quoted statements. Treat Copilot output as a first draft, not a finished product.
5. **Save good prompts.** When you write a prompt that works well, save it to the Prompt Gallery for future use.
6. **Collaborate.** Share what you learn with the person next to you. Discuss what worked and what didn't.
