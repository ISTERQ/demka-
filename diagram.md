```mermaid
erDiagram
    PRODUCTS {
        int product_id PK
        string name
        string description
        string style
        string material
        decimal price
    }
    WORKSHOPS {
        int workshop_id PK
        string name
        string location
    }
    PRODUCT_WORKSHOPS {
        int product_id PK, FK
        int workshop_id PK, FK
    }
    PRODUCTS ||--o{ PRODUCT_WORKSHOPS : produces
    WORKSHOPS ||--o{ PRODUCT_WORKSHOPS : contains
```
