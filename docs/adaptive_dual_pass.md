# Adaptive Dual-Pass Alignment (Balanced RBG)

Adaptive Dual-Pass Alignment computes two probability distributions simultaneously: one based on standard model weights, and another interleaved with retrieved text. A dynamic bias parameter beta balances creative and factual fidelity.

## Architecture & Data Flow

```mermaid
graph TD
    Query[Query] --> Pass1[Pass 1: Parametric Generation]
    Query --> Pass2[Pass 2: Retrieval-Interleaved Generation]
    Pass1 --> Divergence[Calculate Divergence]
    Pass2 --> Divergence
    Divergence --> Calibration[Apply Retrieval Bias Beta]
    Calibration --> FinalOutput[Balanced Response]
```

---

[Back to README](../README.md)
