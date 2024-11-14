graph TD
    A[Start] --> B[Display Available Routes]
    B --> C{Route Choice}
    C -->|1| D[City Center to Airport]
    C -->|2| E[City Center to Beach]
    C -->|3| F[City Center to University]
    D --> G[Display Time Slots]
    E --> G
    F --> G
    G --> H{Time Slot Choice}
    H -->|1| I[Morning (9:00)]
    H -->|2| J[Noon (12:00) - 10% Premium]
    H -->|3| K[Afternoon (15:00) - 20% Premium]
    H -->|4| L[Evening (18:00) - 15% Premium]
    I --> M[Enter Number of Tickets]
    J --> M
    K --> M
    L --> M
    M --> N[Calculate Total Price]
    N --> O{Is Student?}
    O -->|Yes| P[Apply Student Discount]
    O -->|No| Q[Proceed Without Discount]
    P --> Q
    Q --> R[Payment Process]
    R --> S{Continue Booking?}
    S -->|Yes| B
    S -->|No| T[Generate End of Day Report]
    T --> U[Display Revenue and Statistics]
    U --> V[End]
