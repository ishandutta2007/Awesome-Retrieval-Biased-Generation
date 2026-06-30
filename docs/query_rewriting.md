# Pre-Inference Query Rewriting

Pre-Inference Query Rewriting transforms unstructured user inputs into optimal search queries, aligning query intent with document storage schemes before the primary generation loop.

## Architecture & Data Flow

```mermaid
graph TD
    RawQuery[Raw User Query] --> Parser[Auxiliary Parser/LLM]
    Parser --> Structured[Structured Keyword Query]
    Structured --> VectorDB[(Vector DB)]
    VectorDB --> Output[Optimized Context Ingestion]
```

---

[Back to README](../README.md)
