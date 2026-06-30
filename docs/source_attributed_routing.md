# Source-Attributed Token Routing

Through Supervised Fine-Tuning, self-attention heads are trained to map generated claims back to specific document coordinates, naturally outputting verification keys during generation.

## Architecture & Data Flow

```mermaid
graph TD
    Query[Query] --> SFTModel[SFT Model with Citations]
    SFTModel --> Track[Self-Attention Maps to Sources]
    Track --> Generate[Generate Text + Markdown Coordinates]
    Generate --> Output[Response with Citations]
```

---

[Back to README](../README.md)
