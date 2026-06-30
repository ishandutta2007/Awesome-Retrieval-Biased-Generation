# Sycophancy and Data Contamination Risk

When a model is forced to trust retrieved documents, it risks repeating false information (sycophancy or adversarial attacks). Rule-based semantic filters inspect content before generation.

## Architecture & Data Flow

```mermaid
graph TD
    PoisonedDB[(Poisoned Vector DB)] --> RetValue[Inaccurate Fact Ingestion]
    RetValue --> Guardrails[Factual Guardrail Filter]
    Guardrails --> Check[Validate Semantic Boundaries]
    Check -- Clean --> Generator[Logit Bias Generator]
    Check -- Flagged --> Alert[Fallback/Reject Generation]
```

---

[Back to README](../README.md)
