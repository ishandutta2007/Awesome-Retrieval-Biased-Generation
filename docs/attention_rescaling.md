# In-Context Attention Rescaling

Operates inside the Transformer architecture by adjusting attention masking weights to prioritize retrieved document embeddings over general contextual history.

## Architecture & Data Flow

```mermaid
graph TD
    SelfAttention[Self-Attention Layer] --> Masking[Attention Masking]
    Masking --> Amplify[Amplify Retrieved Tokens]
    Amplify --> De-prioritize[De-prioritize Historical Context]
    De-prioritize --> Generation[Generation Step]
```

---

[Back to README](../README.md)
