# The Rigid Prompt-Engineering Era (~2023–2024)

During this era, engineers attempted to force models to adhere to external context using natural language constraints (e.g., 'Answer strictly using the provided context...'). While simple to implement, it was fragile, especially with long contexts where models suffered from the 'Lost in the Middle' phenomenon.

## Architecture & Data Flow

```mermaid
graph TD
    UserQuery[User Query] --> SystemPrompt[Explicit System Instructions]
    Context[Retrieved Context] --> SystemPrompt
    SystemPrompt --> LLM[LLM In-Context Learning]
    LLM --> Output[Strictly Anchored Output]
    style SystemPrompt fill:#f9f,stroke:#333,stroke-width:2px
```

---

[Back to README](../README.md)
