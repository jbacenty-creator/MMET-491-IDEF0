# MMET-491-IDEF0

```mermaid
flowchart TD
    %% Custom styling to match your template
    classDef mainBox fill:#f4f5f7,stroke:#333,stroke-width:2px,color:#000,font-weight:bold;

    %% --------------------------------------------------
    %% NODES
    %% --------------------------------------------------
    %% Process Box
    A0["Manufacturing Function"]:::mainBox

    %% Control Arrows (Top)
    C1[" "]
    C2[" "]

    %% Input Arrows (Left)
    I1[" "]
    I2[" "]

    %% Output Arrows (Right)
    O1[" "]
    O2[" "]

    %% Mechanism Arrows (Bottom)
    M1[" "]
    M2[" "]

    %% --------------------------------------------------
    %% CONNECTIONS & LABELS
    %% --------------------------------------------------
    %% Controls
    C1 -->|Controls| A0
    C2 --> A0

    %% Inputs
    I1 -->|Inputs| A0
    I2 --> A0

    %% Outputs
    A0 --> O1
    A0 -->|Outputs| O2

    %% Mechanisms
    M1 -->|Mechanisms| A0
    M2 --> A0

flowchart LR
    %% Set default node styling
    classDef process fill:#f9f9f9,stroke:#333,stroke-width:2px;

    %% --------------------------------------------------
    %% INPUTS (Left Side)
    %% --------------------------------------------------
    I1[Input 1]
    I2[Input 2]

    %% --------------------------------------------------
    %% CONTROLS (Top Side)
    %% --------------------------------------------------
    C1[Control / Policy 1]
    C2[Control / Standard 2]
    C3[Control / Budget 3]

    %% --------------------------------------------------
    %% MECHANISMS (Bottom Side)
    %% --------------------------------------------------
    M1[Personnel / Team]
    M2[Software / Tools]
    M3[Hardware / Equipment]

    %% --------------------------------------------------
    %% OUTPUTS (Right Side)
    %% --------------------------------------------------
    O1[Final Output 1]
    O2[Final Output 2]

    %% --------------------------------------------------
    %% 6 IDEF0 ACTIVITY BLOCKS (A1 - A6)
    %% --------------------------------------------------
    A1[A1: Assess Requirements]:::process
    A2[A2: Design System]:::process
    A3[A3: Develop Components]:::process
    A4[A4: Integrate & Test]:::process
    A5[A5: Deploy Solution]:::process
    A6[A6: Maintain & Audit]:::process

    %% --------------------------------------------------
    %% CONNECTIONS (ICOM Flow)
    %% --------------------------------------------------
    
    %% Inputs to Initial Processes
    I1 --> A1
    I2 --> A2

    %% Controls (Top-Down into Nodes)
    C1 --> A1
    C1 --> A2
    C2 --> A3
    C2 --> A4
    C3 --> A5
    C3 --> A6

    %% Mechanisms (Bottom-Up into Nodes)
    M1 --> A1
    M1 --> A2
    M2 --> A3
    M2 --> A4
    M3 --> A5
    M3 --> A6

    %% Sequential Process Flow (Inter-block Feedback/Outputs)
    A1 -->|Requirements Doc| A2
    A2 -->|Architecture Blueprint| A3
    A3 -->|Code Modules| A4
    A4 -->|Tested Build| A5
    A5 -->|Live System| A6

    %% Final Outputs Exiting Process
    A5 --> O1
    A6 --> O2
