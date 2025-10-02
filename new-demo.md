```mermaid
graph TD
    A[Root<br/>MAX<br/>α=12 β=∞] --> B{L-MIN<br/>val=12};
    A --> C{R-MIN<br/>α=12 β=2<br/>(Pruning occurs here)};

    B --> B1[MAX<br/>val=17];
    B --> B2[MAX<br/>val=12];
    B1 --> B11((3));
    B1 --> B12((17));
    B2 --> B21((2));
    B2 --> B22((12));

    C --> C1[MAX<br/>val=25];
    C --> C2[MAX<br/>val=2];
    C1 --> C11((15));
    C1 --> C12((25));
    C2 --> C21((0));
    C2 --> C22((2));

    subgraph Legend
        direction LR
        L1[MAX Node]
        L2{MIN Node}
        L3((Terminal Value))
    end

    style C fill:#f99,stroke:#333,stroke-width:2px
    linkStyle 2 stroke-width:2px,stroke:red,fill:none;
```
