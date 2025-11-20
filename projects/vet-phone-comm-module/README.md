# Veterinary Phone Reception Communication Module – Multi-Stage Prompt System

> ⚠️ Early system: This module is **one early component** of a larger ecosystem I designed for veterinary phone communication training. It was built when there were **very limited LLM models and tooling**, so much of the orchestration is “hand-built” using prompts and Google Sheets.

This is a **multi-stage content development system** for creating comprehensive, self-directed learning resources on **veterinary phone communication**, with emphasis on **staff–client interactions and their cyclical impacts** (how staff behavior shapes client feelings, thoughts, behaviors, decisions – and how client responses then feed back into staff behavior).

---

## 1. What this project shows (TL;DR)

- Turns a single **phone topic/phase** (e.g., greeting, triage, explaining costs) into a **full mini-module**:
  - structured sections, goals, and questions  
  - pains & challenges + solutions  
  - theory / framework mapping  
  - actionable advice for staff  
  - intro, self-assessment, and skills-gap prompts  
  - deeper draft focused on staff–client interaction cycles
- Built as a **multi-prompt workflow**, not a single “magic” prompt.
- Originally run through a **Google Sheet orchestrator** connected to multiple LLMs; this repo contains:
  - the **prompt templates** (`prompts/`)
  - **example / answer outputs** (`samples/`)
  - a simple **diagram / outline** (`docs/`)

If you only have 30–60 seconds, open:

- `samples/` – to see what the system produces  
- `prompts/` – to see how each stage is structured

---

## 2. How the system works (high level)

You can think of the system as a simple pipeline:

1. **Structure the topic**  
   - Prompts group the topic into **subtopics, sections, goals, questions, and supporting points**.

2. **Add real-world difficulty + theory**  
   - Prompts generate **pains & challenges**, proposed **solutions**, and connect them to **relevant theories/frameworks** (communication, psychology, adult learning, etc.).

3. **Turn into training content**  
   - Prompts convert this into **actionable advice**, **objectives**, an **introduction**, **self-assessment questions**, and a **skills gap analysis** for self-directed learning.

4. **Deepen one key supporting point**  
   - Additional prompts build a **richer theoretical model** and an **expanded teaching draft** for one important supporting point (e.g., verifying understanding, setting emotional tone).

5. **Review for staff–client impact**  
   - Final prompts critique and refine the draft so it more explicitly shows:
     - how staff actions affect **client feelings, thoughts, behaviors, and decisions**
     - the **cyclical nature** of staff–client interactions.

The end result is a **ready-to-use content package** that can be dropped into an LMS, playbook, or workshop.

---

## 3. Google Sheet orchestrator (external)

In practice, the system was run from a **Google Sheet “control panel”**:

- Each column block represents one stage (Supporting Points → Pains & Challenges → Theory → Actionable Advice, etc.).
- Formulas assemble the full prompt from:
  - ROLE / OBJECTIVE / TASK text  
  - the current **Key Topic / Subtopic / Section**  
  - model + temperature selections
- Responses are written back into “ANSWER” cells and then reused by later stages.

**View-only sheet (for visualization):**  
> [https://docs.google.com/spreadsheets/d/1u5GMQQTu_VBhJ4BSSoHZlez8_gaWlqouT6uWjCy_Qls/edit?usp=sharing] 

This repo only includes the **prompt definitions and example outputs**; the live orchestration stays in the sheet.

---

## 4. Repo map

- `prompts/` – cleaned prompt templates for each stage in the workflow  
- `samples/` – redacted/synthetic example outputs (challenge reports, research report, actionable advice, etc.)  
- `docs/` – overview diagram and any additional documentation (e.g., module outline, detailed write-up)

For a deeper, step-by-step explanation of each prompt and how they connect, see:  

- `docs/DETAILED_OVERVIEW.md` (full technical + instructional design breakdown)
