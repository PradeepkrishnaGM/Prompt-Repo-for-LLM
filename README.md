# Prompt-Repo-for-LLM (v1.0.0)

A domain-specific Python 3.11+ prompt library with structured output contracts, test cases, and benchmark reports.

It provides:

- A **prompt registry** that loads prompts from disk (YAML + Jinja2 templates) and selects by id/version plus optional filters.
- **Typed inputs** via Pydantic models (one model per prompt).
- **Output contracts** (JSON contracts and/or markdown contracts) plus deterministic **validation**.
- An optional **repair flow** that generates a “fix your output” instruction when validation fails.
- A provider-agnostic **evaluation harness** with a `ModelBackend` protocol and a deterministic `MockBackend`.
- A **CLI** and Python API.
- A manual benchmarking workflow for ChatGPT/Claude/Gemini/Grok UIs (no keys, no integrations).

## Install (editable)

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e .[dev]

## Licensing

This repository uses two licenses:

- **Code** (Python source, CLI, evaluation runner, tests, examples): **Apache-2.0** — see `LICENSE-CODE`.
- **Content** (prompt templates, prompt metadata YAML, evaluation case files, benchmark artifacts): **CC0-1.0** — see `LICENSE-CONTENT`.

Suggested mapping (adjust if you want):
- Code: `prl/**/*.py`, `tests/**/*.py`, `examples/**/*.py`, `pyproject.toml`
- Content: `prl/prompts/**`, `eval_cases/**`, `eval_results/**` (records you commit)

## Roadmap
- Add 2 more customer support prompts (summarize + draft response)
- Add minimal Python loader/validator package
- Expand test suites and automate schema validation
- Add multimodal attachments via file references
