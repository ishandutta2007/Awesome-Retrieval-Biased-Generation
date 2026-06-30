# Strict External-Anchored Bias (Zero-Parametric Override)

This configuration enforces absolute compliance by suppressing any generated token that diverges from the retrieved source context. If a parametric hallucination starts to emerge, its logit value is suppressed to zero.

## Architecture & Data Flow

```mermaid
graph TD
    Logits[Un-aligned Token Probabilities] --> Check[Is Token in Context?]
    Check -- No --> Suppress[Suppress Logits to Zero]
    Check -- Yes --> Keep[Keep Probabilities]
    Suppress --> FinalLogits[Final Probabilities]
    Keep --> FinalLogits
    FinalLogits --> Output[Zero-Parametric Output]
```

---

[Back to README](../README.md)
