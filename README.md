%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#0d1117', 'primaryBorderColor': '#00ffcc', 'lineColor': '#ff00ff', 'fontFamily': 'JetBrains Mono'}}}%%
graph TD
    classDef silicon fill:#000,stroke:#ff0033,stroke-width:3px,color:#ff0033;
    classDef kernel fill:#0d1117,stroke:#00ffcc,stroke-width:3px,color:#00ffcc;
    classDef math fill:#0d1117,stroke:#ff00ff,stroke-width:3px,color:#ff00ff;
    classDef brain fill:#0d1117,stroke:#00ccff,stroke-width:3px,color:#00ccff;
    classDef live fill:#00ffcc,stroke:#000,stroke-width:3px,color:#000,font-weight:bold;

    subgraph L1 ["💀 LAYER 1: SILICON"]
        A[<b>Market Data</b><br/>Live SPX Feed]:::silicon
        B[<b>CPU / Memory</b><br/>Zero-Copy Mindset]:::silicon
        A ==> B
    end
    subgraph L2 ["⚡ LAYER 2: KERNEL"]
        C{<b>Ring Buffer</b><br/>Lock-Free Concept}:::kernel
        D[<b>Python Async</b><br/>Fast Ingestion]:::kernel
        B ==> C
        B --> D
    end
    subgraph L3 ["🧬 LAYER 3: MATH ENGINES - LIVE NOW"]
        E1([Stochastic<br/>Brownian]):::math
        E2([Theta Decay<br/>Time Model]):::live
        E3([Entropy<br/>Shannon]):::math
        E4([Kalman<br/>Noise Filter]):::math
        E5([Kelly<br/>Position Size]):::live
        E6([VaR 95%<br/>Risk Model]):::live
        C --> E1
        C --> E2
        C --> E3
        C --> E4
        C --> E5
        C --> E6
    end
    subgraph L4 ["🧠 LAYER 4: RISK AGENT - LIVE IN RiskGuard"]
        F((<b>ORCHESTRATOR</b><br/>RiskGuard Engine)):::brain
        G[[<b>RED / YELLOW / GREEN</b><br/>Exit Signal]]:::live
        E2 --> F
        E5 --> F
        E6 --> F
        F ==> G
    end
    subgraph L5 ["⚔️ LAYER 5: EXECUTION"]
        H{{<b>Streamlit Cloud</b><br/>Live Dashboard}}:::live
        G --> H
        H -. Feedback .-> A
    end