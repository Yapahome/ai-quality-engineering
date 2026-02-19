# LLM Quality Framework v0.1 (EN)

This document defines a practical, QA-oriented framework for evaluating the quality of LLM (Large Language Model) outputs in product contexts. LLM quality is treated as **behavioral alignment** with user intent and system constraints, not as deterministic correctness.

---

## 1. LLM Defect Taxonomy (Types of Defects)

LLMs are probabilistic systems. Defects are **behavioral deviations** from the expected product behavior, policy, or task intent.

### 1.1 Factual Hallucination
The model produces information that is not supported by reality or verifiable sources.
- Examples: invented facts, fake citations, incorrect dates.

### 1.2 Logical Inconsistency
The output contradicts itself or violates basic reasoning.
- Examples: mutually exclusive claims in the same answer.

### 1.3 Non-deterministic Instability
The same prompt can lead to meaningfully different outputs, structure, or conclusions.
- Note: this is a property of LLMs, but becomes a defect if it violates product expectations.

### 1.4 Context Loss
The model ignores parts of the conversation or forgets constraints and requirements.
- Examples: missing key user constraints, dropping previous instructions.

### 1.5 Format Violation
The model fails to follow an output contract or required structure.
- Examples: invalid JSON, extra text outside the expected format.

### 1.6 Bias / Unfairness
The output shows unwanted bias, unfair generalizations, or discriminatory language.

### 1.7 Over-refusal
The model refuses to answer permissible requests or is overly cautious.

### 1.8 Irrelevance
The output does not answer the user’s question or drifts away from the requested scope.

### 1.9 Error Propagation
Early inaccuracies in multi-step reasoning accumulate and distort the final result.
- Typical in chain-based workflows where intermediate steps influence the final answer.

---

## 2. Quality Criteria for LLM Outputs

LLM output quality is multi-dimensional. A single metric is not sufficient.

### 2.1 Factual Accuracy
How well the output matches verifiable facts (when applicable).

### 2.2 Relevance
How directly the output addresses the user’s request and intent.

### 2.3 Completeness
Whether the answer covers all essential aspects of the question.

### 2.4 Logical Coherence
Whether the reasoning and structure are consistent and understandable.

### 2.5 Consistency
Stability across:
- repeated runs,
- paraphrased prompts,
- multi-turn conversation.

### 2.6 Format Compliance
Adherence to required structure (e.g., JSON schema, table, bullet points).

### 2.7 Safety
Absence of harmful, unsafe, or policy-violating content.

### 2.8 Controllability / Instruction Following
How well the model follows constraints, rules, and formatting requirements.

---

## 3. Practical QA Notes

- Treat model outputs as hypotheses that require validation, especially in factual domains.
- Define expected behavior in terms of **acceptance criteria** and **risk** rather than deterministic expected results.
- Separate evaluation of:
  - model behavior,
  - prompt/instruction design,
  - system integration (UI/API formatting, rate limits, etc.).
