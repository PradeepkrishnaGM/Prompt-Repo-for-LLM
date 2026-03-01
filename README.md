# Prompt-Repo-for-LLM (v0.1.0)

Domain-specific prompt library with structured output contracts, test cases, rubrics, and benchmark reports.

## What this repo contains (v0.1.0)
- **Prompt specs** (YAML): reusable prompt templates with clear input/output contracts
- **Output schemas** (JSON Schema): standard, machine-checkable outputs
- **Test cases** (JSONL): inputs + expected outcomes
- **Rubrics** (YAML): scoring guidance
- **Failure galleries** (Markdown): documented failure modes and mitigations
- **Benchmarks** (Markdown): manual benchmark reports across models

## Current domain
- `customer_support`

## Current prompt
- `cs.classify_ticket` — ticket classification into category/priority/sentiment/escalation

## How to use (manual, v0.1.0)
1. Open: `prompts/customer_support/classify_ticket/prompt.yaml`
2. Pick a testcase from: `prompts/customer_support/classify_ticket/tests.jsonl`
3. Paste into your LLM UI (ChatGPT / Claude / Gemini / DeepSeek)
4. Verify output matches schema: `schemas/classify_ticket.output.schema.json`

## Licensing
- **Code** (anything under `src/` and tooling files): Apache-2.0 — see `LICENSE-CODE`
- **Content** (prompts, tests, benchmark data, docs examples): CC0-1.0 — see `LICENSE-CONTENT`

## Roadmap
- Add 2 more customer support prompts (summarize + draft response)
- Add minimal Python loader/validator package
- Expand test suites and automate schema validation
- Add multimodal attachments via file references
