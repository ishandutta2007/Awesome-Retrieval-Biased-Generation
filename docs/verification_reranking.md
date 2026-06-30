# Post-Hoc Verification Reranking

After the generator produces several candidate answers, a specialized value network or cross-encoder evaluates and ranks them to select the option most grounded in the retrieved sources.

## Architecture & Data Flow

```mermaid
graph TD
    Prompt[Prompt] --> LLM[LLM Generator]
    LLM --> Candidates[N Candidate Answers]
    Candidates --> Reranker[Cross-Encoder Reranker]
    Reranker --> BestCandidate[Min-Hallucination Response]
```

---

[Back to README](../README.md)
