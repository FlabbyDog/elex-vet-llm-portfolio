# llm-call-extraction-reporting

This repository contains **one version** of my LLM prompt system for veterinary call analytics. It focuses on **call-level extraction, diarization correction, sentiment analysis, and structured reporting** for phone interactions between veterinary staff and clients.

> Important:  
> - This is **just one slice** of a much larger, multi-stage prompt ecosystem.  
> - It does **not** fully represent the overall architecture, automation, or evaluation layers of the full project.

---

## What this version does

This repo showcases how I design complex, multi-step prompts to turn raw (or pre-processed) call transcripts into structured, analysis-ready outputs.

Key capabilities demonstrated:

- **Role-based AI persona design**  
  - Example: `TranscriptSentinel` — a meticulous, emotionally aware assistant that:
    - Corrects speaker diarization and roles (STAFF / CLIENT / SERVICEPROV / AUTOMATED_MESSAGE)  
    - Preserves original wording while fixing attribution and timestamps  
    - Performs granular sentiment scoring (−10 to +10) with confidence scores  
    - Assigns both **colour emojis** (for sentiment) and **face emojis** (for emotional tone)  
    - Builds a **Sentiment & Emotion Flow Grid** to visualize emotional progression

- **Structured multi-task call analysis**
  - Extracts key metadata (call direction, outcome, staff name, client type, URLs, IDs)
  - Generates a fully corrected, line-numbered transcript with embedded sentiment markers
  - Produces summary statistics and performance insights from the emotional flow

- **Weekly performance dataset prompts (Part 1 only)**
  - Uses **pre-extracted call data** (numeric fields, codes, ratings) to build:
    - Call volume and distribution tables  
    - Quality, sentiment, friction, and revenue-impact datasets  
    - Strengths, development opportunities, and missed opportunity datasets  
  - Emphasizes **data integrity**: verify totals, don’t invent data, only use explicitly provided fields

---

## What is *not* in this repo

To keep this portfolio version compact and privacy-safe, this repository **does not** include:

- The full multi-stage pipeline (transcription, QA, aggregation, dashboarding, automation)
- All prompt variants, evaluation harnesses, or tool-calling layers
- Production configs, API orchestration code, or clinic-specific implementation details

Think of this as a **focused showcase** of how I design:

- Complex, stepwise LLM instructions  
- Robust output templates for downstream analytics  
- Human-readable yet machine-parseable report formats

---

## Included artifacts

- `prompts/transcript_sentinel.md`  
  Core persona + stepwise tasks (Tasks 1–7) for single-call transcript correction, sentiment scoring, and emotional flow analysis.

- `prompts/weekly_part1.md`  
  Weekly performance dataset instructions for transforming pre-extracted call metrics into structured, multi-section reports.

- `samples/`  
  Example prompt snippets and (in my portfolio version) selected sample outputs, demonstrating how the prompts behave on real-world-like data. All real client details are redacted/de-identified in actual usage.

---

## Intended usage

These prompts are model-agnostic and can be adapted for:

- OpenAI, Anthropic, or compatible LLM providers  
- Internal analytics tools that take **system + user prompts** and return JSON/markdown  
- Pipelines that chain: transcript → extraction → scoring → reporting → BI dashboards

You’re viewing this repo in the context of my portfolio; it’s meant to illustrate **how I think about LLM system design for structured, high-stakes operations**, not to serve as a drop-in product.
