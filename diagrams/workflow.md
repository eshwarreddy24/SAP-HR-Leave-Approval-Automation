# Proposed HR leave request approval workflow

**Design only:** this diagram is not proof of a configured or tested process. Update it to reflect what actually works in the SAP trial.

```mermaid
flowchart TD
    A[Employee submits leave request] --> B{Required fields provided?}
    B -->|No| C[Return for correction]
    C --> A
    B -->|Yes| D[Manager reviews request]
    D --> E{Approve or reject?}
    E -->|Reject| F[Mark rejected]
    E -->|Approve| G[HR review if implemented]
    G --> H{HR validation passed?}
    H -->|No| I[Return for clarification]
    H -->|Yes| J[Mark approved]
```

If the trial does not support HR review or form validation, simplify the actual implementation to employee form, manager decision and conditional routing. Maintain a clear distinction between **planned** and **implemented** steps.
