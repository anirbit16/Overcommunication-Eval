# Overcommunication-Eval

**Overcommunication-Eval** is an experimental LLM evaluation project focused on a common conversational failure mode: language models often provide more explanation, caution, qualification, background, or detail than a user's request actually requires.

The project aims to study whether LLMs can better calibrate their response length and tone to the context of a question, while preserving correctness and appropriate safety behavior.

## Motivation

A good response should not simply be as short as possible.

For example, a simple factual question may only require one sentence, while a technical or high-risk question may justify a longer and more careful explanation.

The goal of this project is therefore to measure **contextually unnecessary communication**, rather than verbosity alone.

## Current Evaluation Framework

Responses are manually evaluated using an **Overcommunication Score**:

- **0 — Appropriate**
- **1 — Slight overcommunication**
- **2 — Clear overcommunication**
- **3 — Severe overcommunication**

Responses can also receive one or more failure labels:

- Unnecessary explanation
- Unnecessary examples
- Unnecessary background
- Repetition
- Unnecessary caution
- Unnecessary qualification

## Current Experiments

### Pilot 1 — Simple Questions

The first pilot evaluates responses to simple factual, mathematical, and programming questions where short answers are generally sufficient.

Initial observations suggest that unnecessary explanation is the most common form of overcommunication in this set.

### Pilot 2 — Hyper-Caution and Qualification

The second pilot focuses on ordinary, low-risk questions designed to test whether the model introduces unnecessary caveats, hedging, warnings, or qualification.

## Planned Work

Future stages will include:

- Expanding the benchmark
- Comparing multiple LLMs
- Human and automated evaluation
- Prompt-based tone calibration
- Conversational preference memory
- Embedding-based preference retrieval
- Cosine similarity
- Cohere Embed and Rerank
- Comparing full-context and retrieval-based personalization approaches

## Research Direction

The broader question behind the project is:

> Can an LLM adapt its response style and level of detail to the user's actual conversational needs without becoming under-informative, overly cautious, or unnecessarily verbose?

A later stage of the project will explore whether retrieving only contextually relevant user communication preferences can improve conversational naturalness compared with generic prompting or supplying the entire conversation history.

## Status

This project is currently in the early experimental and benchmark-design stage.
