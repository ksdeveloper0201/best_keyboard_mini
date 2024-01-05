```mermaid
erDiagram
    User ||..o{ Product : Creates
    User ||--o{ Review : Writes
    Admin ||--o{ Product : Manages

    User {
    int user_id
    varchar email
    varchar password_hash
    timestamp created_at
    timestamp updated_at
    }

    Product {
    int product_id
    varchar name
    text description
    decimal price
    varchar manufacturer
    varchar category
    timestamp created_at
    timestamp updated_at
    }

    Review {
    int review_id
    text content
    int rating
    timestamp created_at
    timestamp updated_at
    }

    Admin {
    int admin_id
    varchar email
    varchar password_hash
    timestamp created_at
    timestamp updated_at
    }

    User }|..|{ Review : "1..*"
    Product }|..|{ Review : "1..*"
    Admin }|..|{ Product : "1..*"
```
