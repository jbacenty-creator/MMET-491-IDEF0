# MMET-491-IDEF0

### A-0 Context Diagram

```mermaid
flowchart TD
    A0[Run Autonomous Fleet Printing Operation]

    C1[Controls] --> A0
    C2[Policies & Standards] --> A0

    I1[Inputs] --> A0
    I2[Raw Materials] --> A0

    M1[Mechanisms] --> A0
    M2[Tools & Personnel] --> A0

    A0 --> O1[Outputs]
    A0 --> O2[Finished Product]
```

---

### A0 Decomposition Diagram (6 Activity Blocks)

```mermaid
flowchart LR
    I1[Input 1]
    I2[Input 2]

    C1[Control / Policy 1]
    C2[Control / Standard 2]
    C3[Control / Budget 3]

    M1[Personnel / Team]
    M2[Software / Tools]
    M3[Hardware / Equipment]

    O1[Final Output 1]
    O2[Final Output 2]

    A1[A1: Assess Requirements]
    A2[A2: Design System]
    A3[A3: Develop Components]
    A4[A4: Integrate & Test]
    A5[A5: Deploy Solution]
    A6[A6: Maintain & Audit]

    I1 --> A1
    I2 --> A2

    C1 --> A1
    C1 --> A2
    C2 --> A3
    C2 --> A4
    C3 --> A5
    C3 --> A6

    M1 --> A1
    M1 --> A2
    M2 --> A3
    M2 --> A4
    M3 --> A5
    M3 --> A6

    A1 -->|Requirements Doc| A2
    A2 -->|Architecture Blueprint| A3
    A3 -->|Code Modules| A4
    A4 -->|Tested Build| A5
    A5 -->|Live System| A6

    A5 --> O1
    A6 --> O2
```
