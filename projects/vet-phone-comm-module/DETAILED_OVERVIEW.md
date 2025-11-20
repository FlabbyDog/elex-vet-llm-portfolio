# Veterinary Phone Reception Communication Module – Multi-Stage Prompt System

> ⚠️ Note: This system is **one early component** of a larger ecosystem I designed for veterinary phone communication training.  
> It represents one of my **earliest multi-stage content systems**, built at a time when there were **very limited LLM models and tooling available**, so much of the structure is “hand-built” in prompts and Google Sheets.

---

## 1. What this project is

This is a **multi-stage content development system** for creating comprehensive, self-directed learning resources on **veterinary phone communication**, with a strong emphasis on:

- Staff–client interactions  
- How staff actions affect **client feelings, thoughts, behaviors, and decisions**  
- The **cyclical impact** of these interactions (clients’ responses then shaping staff behavior, and so on)

The system takes a **single phone communication topic or phase** (e.g., “opening a call”, “triaging a sick pet”, “explaining costs”) and progressively transforms it into:

- Structured learning sections  
- Challenge & pain-point analysis  
- Theory & framework mapping  
- Actionable advice  
- Intro, self-assessment, and skills gap analysis  
- An expanded, theory-backed teaching draft focused on staff–client interaction cycles

This repo contains:

- The **prompt system** (`prompts/`)
- **Example / answer outputs** (`samples/`)
- A small **docs area** (`docs/`) for diagrams and outlines  

The **operational orchestration** (multi-LLM wiring, formulas, dashboards) lived in a Google Sheet + external tools and is **not fully represented** here.

---

## 2. Spreadsheet-Orchestrated Version (External)

In practice, this prompt system was driven from a **Google Sheet “control panel”** rather than typed into an LLM one by one.

The Sheet acts as a light-weight **orchestrator and visualizer**:

- Each **column block** represents one stage in the pipeline  
  (e.g., “Supporting Points, Questions, and Goals” → “Pains and Challenges & Solutions” → “Theories/Framework” → “Actionable Advice”).
- Each block contains:
  - The **role / context / task text** for the prompt
  - A **topic snapshot** pulled from the “Sample Topic” area (Key Topic, Subtopic, Section)
  - Dropdowns for **temperature** and **model selection** (e.g., `claude-3.5-sonnet-20240620`, `claude-3-haiku-20240307`)
  - A **formula cell** (e.g., `=JOIN(CHAR(10), …)`) that automatically assembles the full prompt from the role, topic, and parameters
  - An **ANSWER cell** where the LLM output is written back

Across the tabs, the layout roughly follows the prompt system:

- One tab focuses on **Key Topic 1** and runs Prompts **1–4**:
  - Left side: “Sample Topic” with key topic, overview, sections  
  - Center/right: colored blocks for  
    - Supporting Points, Questions, and Goals (Prompt 1)  
    - Pains and Challenges & Solutions (Prompt 2)  
    - Theories/Framework (Prompt 3)  
    - Actionable Advice (Prompt 4)
- Another tab arranges **Introduction + Supporting Points 1–5** in columns:
  - Each column is a subtopic/section “card” that calls the relevant prompt, using the same pattern of  
    **prompt text → model/temperature → formula → answer cell**.
- The lower rows on that tab handle **expansion and refinement for a single supporting point**, corresponding to Prompts **6–9**:
  - Suggestions for Theoretical Framework and Models (Prompt 6)  
  - Enhanced suggestions for Theoretical Framework and Models (second pass)  
  - Suggestions for Content and Depth (Prompt 8)  
  - Enhanced Content and Depth (Prompt 9)

The Sheet was connected to various LLMs via external tooling.  
The formulas:

- Pull the right **topic/section text** from the “Sample Topic” area
- Combine it with the **ROLE / OBJECTIVE / TASK / TEMPLATE** for the chosen prompt
- Send the assembled prompt to the selected model
- Store the **raw answer** in the ANSWER cell for that prompt stage

From there, answers were copied or transformed into downstream resources
(LMS content, PDFs, etc.).  

In this repo, I only include the **prompt definitions** and some **answer examples**.  
The live orchestration remains in the Google Sheet.

**View the orchestration sheet (view-only):**  
> https://docs.google.com/spreadsheets/d/1u5GMQQTu_VBhJ4BSSoHZlez8_gaWlqouT6uWjCy_Qls/edit?usp=sharing


---

## 3. Big Picture – How the System Works

### 3.1 High-level flow

At a conceptual level, the flow looks like this:

1. **Define the Topic**
   - Example: “Start of a veterinary phone interaction: greeting and identity check”

2. **Structure the Content (Prompt 1)**
   - Break the topic into **subtopics, sections, goals, questions, supporting points**

3. **Find Real-World Pains (Prompt 2)**
   - For each section, surface **challenges and pain points**, and propose **solutions**

4. **Anchor in Theory (Prompt 3)**
   - Connect those challenges to **theories, frameworks, and principles**

5. **Turn into Practical Guidance (Prompt 4)**
   - Convert into **step-by-step actionable advice** for staff

6. **Wrap as a Learning Module (Prompt 5)**
   - Create **objectives, introductions, self-assessment, skills gap analysis**

7. **Deepen a Key Idea (Prompt 6 & 7)**
   - Choose one **supporting point** and:
     - Strengthen the **theoretical model** (Prompt 6)
     - Produce an **expanded teaching draft** for that point (Prompt 7)

8. **Refine for Interaction Depth (Prompt 8 & 9)**
   - Analyze and enhance the draft to better show:
     - How staff actions affect **client feelings, thoughts, behaviors, decisions**
     - The **cyclical nature** of staff–client interactions

### 3.2 Visual mental model

You can visualize it as an assembly line:

```text
Topic
  ↓
[Prompt 1] Structure content (sections, goals, questions, points)
  ↓
[Prompt 2] Pains & challenges + solutions
  ↓
[Prompt 3] Theories & frameworks
  ↓
[Prompt 4] Actionable advice
  ↓
[Prompt 5] Objectives, intro, self-assessment, skills gap
  ↓
[Prompt 6] Theoretical upgrade for one key supporting point
  ↓
[Prompt 7] Expanded teaching draft (staff–client focus)
  ↓
[Prompt 8 & 9] Depth & interaction-cycle review
  ↓
Final self-directed learning content
````

---

## 4. What feeds into the system & what comes out

### Inputs

* **Key Topic**:
  e.g., “Phone Topic: Start of Veterinary Phone Interaction”

* **Subtopic & Sections**:
  e.g., “Subtopic: Greeting and Identification”, with sections like:

  * “Setting tone and first impression”
  * “Verifying client and patient identity”

* **Context & constraints**:

  * Veterinary phone setting (no visual exam, emotional clients, time pressure)
  * Focus on staff–client interaction dynamics
  * Desire for **self-directed** learning resources

### Outputs (end-to-end)

By the end of the full prompt chain, you can generate:

* A **structured outline** of the topic (sections, goals, questions, supporting points)
* A **Challenge Analysis & Solutions Report** for each section
* A **Research-style report** linking challenges to theories/frameworks
* A set of **Actionable Advice** sequences for staff
* **Module front matter**:

  * Objectives
  * Introduction
  * Self-assessment
  * Skills gap analysis
* An **expanded, theory-backed teaching draft** for a key supporting point
* **Critique and enhancement suggestions** focusing on:

  * Staff impact on client feelings/thoughts/behaviors/decisions
  * Cyclical nature of staff–client interactions

---

## 5. Detailed Description of Each Prompt

Below is the **intent, input, output, and connection** for each prompt in the chain.

---

### Prompt 1 – Content Structuring

**File:** `prompts/01_content-structuring.md`

**Purpose:**
Turn a Key Topic + Subtopic into a **teaching structure**:

* Sections
* Supporting questions
* Goals
* Supporting points

**Input:**

* Key Topic name & overview
* Subtopic name & overview
* Section titles & short descriptions (if already defined)

**Output:**
For each section, Prompt 1 produces:

* **Supporting Questions** (what learners should think about)
* **Goals** (what they should achieve)
* **Supporting Points** (key ideas, examples, applications)

**Connection:**

* These **sections + points** become the foundation for:

  * The **challenges** in Prompt 2
  * The **learning objectives** in Prompt 5
  * The **supporting point** chosen for deeper work in Prompt 6–7

---

### Prompt 2 – Pains and Challenges & Solutions

**File:** `prompts/02_pains-challenges-solutions.md`

**Purpose:**
Surface **real-world problems** in that section and outline **solutions**, especially where staff–client interaction goes wrong.

**Input:**

* One section from Prompt 1 (title, overview, goals, points)

**Output:**
For each **challenge**:

* Title + explanation of **why it’s a pain**
* Detailed **problem description**
* **3 solutions**, with:

  * How it addresses the challenge
  * “Theory into action” steps / behaviors
* **Follow-up questions** for further exploration

**Connection:**

* These challenges become the **raw material** for:

  * The theories in Prompt 3
  * Actionable advice in Prompt 4
  * Examples & hooks in the Intro and Self-assessment (Prompt 5)

---

### Prompt 3 – Theories / Frameworks (Research Report)

**File:** `prompts/03_theories-frameworks.md`

**Purpose:**
Map practical challenges to **theories, frameworks, and principles** from:

* Communication
* Psychology
* Adult learning
* Healthcare/veterinary domains

**Input:**

* Challenge Analysis & Solutions from Prompt 2
* The same section context from Prompt 1

**Output:**
For each challenge:

* 2–3 **Key conceptual elements / frameworks / theories**:

  * What it is
  * Why it matters to phone interactions
  * How/when it’s applied
  * Who is involved (staff, client, team)
  * Impact on:

    * Staff understanding and behavior
    * Client feelings, thoughts, decisions
* Practical examples and implementation notes

**Connection:**

* This anchors the system in **evidence and theory**, and feeds:

  * Prompt 4 (to justify actionable advice)
  * Prompt 6 (for building a stronger model for one supporting point)
  * Prompt 7 (for a theory-aware teaching narrative)

---

### Prompt 4 – Actionable Advice

**File:** `prompts/04_actionable-advice.md`

**Purpose:**
Translate challenges + theory into **clear, sequential advice** for staff.

**Input:**

* Challenges & solutions (Prompt 2)
* Theories & frameworks (Prompt 3)

**Output:**
For each challenge:

* An **Actionable Advice** block with:

  * A concise description of **what to do**
  * **5 sequential steps** staff can follow
  * Implementation insights and resource ideas
  * Space to suggest **AI applications** (e.g., as a practice coach, template generator)

**Connection:**

* These steps feed directly into:

  * The **module content** used by staff
  * The **Self-assessment** and **Skills Gap** thinking in Prompt 5
  * Concrete examples in Prompt 7

---

### Prompt 5 – Objectives, Introduction, Self-Assessment & Skills Gap Analysis

**File:** `prompts/05_intro-self-assessment.md`

**Purpose:**
Wrap the topic into **front-of-module content** that is ready for learners.

**Input:**

* Goals & supporting questions (Prompt 1)
* Pains and challenges (Prompt 2)
* Actionable advice (Prompt 4)

**Output:**

* **Objectives**

  * What learners should know/do after this section
  * Explicitly includes **client experience** and **team interaction** goals

* **Introduction**

  * Overview of the section
  * Why it matters in real clinics
  * A scenario/hook highlighting a common pain

* **Self-Assessment**

  * 5–7 questions (mix of factual + reflective)
  * Focus on:

    * Knowledge
    * Staff’s own behavior with clients
    * Awareness of client feelings & decisions

* **Skills Gap Analysis**

  * A simple framework/template for:

    * Identifying skills they already have
    * Skills they need to improve
    * Particularly around staff–client dynamics

**Connection:**

* These pieces belong in the **front part of a learning module** (e.g., LMS unit, manual, workbook).

---

### Prompt 6 – Suggestion for Theoretical Framework & Models (Supporting Point)

**File:** `prompts/06_supporting-point-framework.md`

**Purpose:**
Zoom in on **one supporting point** (from Prompt 1) and strengthen the theory beneath it.

**Input:**

* A chosen **supporting point** (e.g., “Confirming client understanding before ending the call”)
* Prior theory & challenges (Prompts 2 & 3)

**Output:**

* Assessment of current theoretical coverage
* Identification of **gaps**
* Suggested **additional theories/models**
* A proposed **comprehensive model**:

  * Staff actions
  * Client responses
  * Team dynamics
* A **skill progression framework** (Novice → Expert)
* Suggestions for **outcome measurement** (e.g., client satisfaction, call quality)

**Connection:**

* Prompt 6 informs how Prompt 7 will **rewrite and expand** that supporting point into a richer teaching piece.

---

### Prompt 7 – Expanded Supporting Point Draft

**File:** `prompts/07_supporting-point-expanded-draft.md`

**Purpose:**
Use the theoretical upgrade (Prompt 6) to write an **expanded, structured teaching draft** for the chosen supporting point.

**Input:**

* Supporting point from Prompt 1
* Theoretical model from Prompt 6
* Challenges, theory, and advice (Prompts 2–4)

**Output:**

A structured draft that includes:

* Hook & Goal
* Explanation of the supporting point
* Frameworks & theories in plain language
* Multiple perspectives (staff, client, team)
* Challenge analysis & common misconceptions
* Solutions & implementation strategies (individual + manager level)
* Reflective prompts & scenarios
* Follow-up questions

**Connection:**

* This is the **core teaching text** that learners would read or watch.
* Prompts 8 and 9 then critique and deepen this draft.

---

### Prompt 8 – Content & Depth Suggestions (First Pass)

**File:** `prompts/08_content-depth-review.md`

**Purpose:**
Act as a **reviewer/editor** for the draft from Prompt 7, focusing on:

* Staff impact on client feelings, thoughts, behaviors, decisions
* The **interaction cycle** between staff and client

**Input:**

* Expanded draft from Prompt 7
* Context of the supporting point

**Output:**

A structured **recommendation document** that:

* Summarizes what the current content covers well
* Identifies gaps (e.g., not explicit enough about emotions or decision-making)
* Suggests:

  * Stronger examples
  * Clearer cause–effect chains
  * More reflective exercises
  * Potential structural changes

**Connection:**

* These recommendations guide further revision of the teaching draft
* Prompt 9 can be seen as a **more integrated/final critique** using all context

---

### Prompt 9 – Content & Depth Suggestions (Final / Integrated Pass)

**File:** `prompts/09_content-depth-review-final.md`

**Purpose:**
A **second, more integrated review pass** that:

* Uses:

  * Challenges (Prompt 2)
  * Theory (Prompt 3)
  * Actionable Advice (Prompt 4)
  * Expanded Draft (Prompt 7)
  * First review (Prompt 8)
* To produce a **sharper, more holistic set of enhancement suggestions**

**Input:**

* All prior context and outputs

**Output:**

A refined **Content & Depth suggestion set** that focuses on:

* Making the impact of staff actions on clients **explicit**
* Highlighting the **cyclical nature** of staff–client interactions
* Proposing **evidence-based** enhancements without losing focus on the specific supporting point

**Connection:**

* This serves as a **final content-critique layer** before locking in module content for that supporting point.

---

## 6. What’s in This Repo vs. Outside

**In this repo:**

* `prompts/`

  * Cleaned prompt templates for each stage of the system
* `samples/`

  * **Answers / example outputs** from the system (redacted/synthetic)
* `docs/`

  * Visual aids (e.g., overview diagram, optional module outline)

**Outside this repo (in the original system):**

* A **Google Sheet** orchestrator:

  * LLM connections (multiple models over time)
  * Formulas to auto-populate inputs/outputs
  * Dashboards and tracking
* Additional downstream processes (e.g., formatting for LMS, PDF handouts, etc.)

This README focuses on the **logic and flow** of the multi-stage content development system, not the entire production pipeline.

---

## 7. What this project demonstrates

This project showcases:

* **Multi-stage LLM prompt system design** for a real, high-stakes domain (veterinary phone calls)
* Integration of:

  * Domain expertise (veterinary medicine & client communication)
  * Instructional design (objectives, self-assessment, skills gap)
  * Theoretical grounding (frameworks, models, progression)
  * Staff–client **interaction dynamics** and their cyclical impacts
* Early-stage engineering of an **automated content pipeline** using:

  * LLMs
  * Google Sheets
  * Structured prompts and templates

Even as an early version, it illustrates how a single topic can be transformed into a **comprehensive, self-directed learning resource** through a series of carefully designed prompt stages.