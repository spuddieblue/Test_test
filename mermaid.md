flowchart TD
    A[Start Program] --> B[Initialize Variables]
    B --> C[Generate Random Numbers for n1 and n2]
    C --> D[Check n1: Is it 10, 11, or 12?]
    D -->|Yes| E[Set n1 = 10]
    D -->|No| F[Check n1: Is it 14?]
    F -->|Yes| G[Prompt User: Ace 1 or 11?]
    G -->|Valid Input| H[Set n1 = Choice]
    G -->|Invalid Input| I[Display Error]
    F -->|No| J[Continue]

    C --> K[Check n2: Is it 10, 11, or 12?]
    K -->|Yes| L[Set n2 = 10]
    K -->|No| M[Check n2: Is it 14?]
    M -->|Yes| N[Prompt User: Ace 1 or 11?]
    N -->|Valid Input| O[Set n2 = Choice]
    N -->|Invalid Input| P[Display Error]
    M -->|No| Q[Continue]

    J --> R[Calculate Total = n1 + n2]
    Q --> R

    R --> S[Display Cards and Total]
    S --> T[Prompt User: Hit or Stand?]
    T -->|Hit| U[Generate Random Card n3]
    U --> V[Check n3: Is it 10, 11, or 12?]
    V -->|Yes| W[Set n3 = 10]
    V -->|No| X[Check n3: Is it 14?]
    X -->|Yes| Y[Prompt User: Ace 1 or 11?]
    Y -->|Valid Input| Z[Set n3 = Choice]
    Y -->|Invalid Input| AA[Display Error]
    X -->|No| AB[Continue]

    W --> AC[Add n3 to Total]
    Z --> AC
    AB --> AC
    AC --> AD[Check Total: > 21?]
    AD -->|Yes| AE[Display Bust Message]
    AD -->|No| T

    T -->|Stand| AF[Display Final Total]
    AE --> AG[End Program]
    AF --> AG
