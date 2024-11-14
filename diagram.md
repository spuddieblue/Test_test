```mermaid
graph TD
    A[Start] --> B[Display Available Routes]
    B --> C{Route Choice}
    C --> D[City Center to Airport]
    C --> E[City Center to Beach]
    C --> F[City Center to University]
    D --> G[Display Time Slots]
    E --> G
    F --> G
    G --> H{Time Slot Choice}
    H --> I[Morning (9:00)]
    H --> J[Noon (12:00) - 10% Premium]
    H --> K[Afternoon (15:00) - 20% Premium]
    H --> L[Evening (18:00) - 15% Premium]
    I --> M[Enter Number of Tickets]
    J --> M
    K --> M
    L --> M
    M --> N[Calculate Total Price]
    N --> O{Is Student?}
    O --> P[Apply Student Discount]
    O --> Q[Proceed Without Discount]
    P --> Q
    Q --> R[Payment Process]
    R --> S{Continue Booking?}
    S --> B
    S --> T[Generate End of Day Report]
    T --> U[Display Revenue and Statistics]
    U --> V[End]
