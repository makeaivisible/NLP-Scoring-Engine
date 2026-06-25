# NLP Scoring Engine

Behavioral scoring pipeline for anonymized AI conversations.

This repository owns the MVP scoring layer that turns anonymized conversations into research-friendly indicators. The first version should be transparent, auditable, and easy to compare against expert labels before any automated claims are trusted.

## MVP Scope

- Consume anonymized conversation records.
- Score conversations across the Make AI Visible behavioral dimensions.
- Return structured scores, confidence, evidence snippets, and model/rubric version metadata.
- Support both transparent rubric baselines and future model-backed scoring.
- Provide an evaluation harness for agreement with human reviewers.

## Privacy Boundary

This engine should never receive raw, non-anonymized submissions. Tests and examples must use synthetic or already anonymized content.

## Suggested Stack

- Python package with a small CLI.
- Pydantic schemas for scoring input/output.
- Pytest evaluation fixtures.
- Baseline rubric implementation before LLM/model integration.

## First Milestone

Implement a deterministic baseline scorer with fixtures, schema validation, and a report comparing output against hand-labeled examples.
