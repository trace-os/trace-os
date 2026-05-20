# TraceOS

**Public architecture surface for regulated evidence-to-decision systems.**

TraceOS is the architecture behind **ApprovalBrief AI**, a proof-pack system for regulated approval decisions.

ApprovalBrief AI is built on a simple control principle:

> **Bounded specialist AI agents prepare proof artifacts.**  
> **Deterministic readiness gates structure the decision state.**  
> **Humans approve, condition, hold, or escalate.**

The first product wedge focuses on workflows where fragmented evidence must become reviewable before a high-stakes decision can move forward:

- payment pilots and controlled rollouts
- vendor / ICT third-party risk approvals
- internal AI tool approvals
- regulated enterprise change gates

```mermaid
flowchart LR
    A[Fragmented enterprise evidence] --> B[Bounded specialist agents]
    B --> C[Proof-pack layer]
    C --> D[Deterministic readiness gates]
    D --> E{Decision state}

    E -->|Blocked| F[Blockers + owners]
    E -->|Conditional| G[Conditions + review notes]
    E -->|Ready| H[Reviewer-ready proof pack]

    F --> I[Rerun after updates]
    G --> I
    I --> C

    H --> J[Human approval boundary]
    J --> K[Traceable decision record]
```

## Public / private boundary

Public repositories contain only public-safe materials: concept notes, synthetic examples, high-level diagrams, and validation framing.

Private repositories contain the product implementation, orchestration logic, evidence mappings, and vertical-specific workflow design.
