@startuml

entity "users" {

-   ## user_id : INT
    email : VARCHAR(255)
    password_hash : VARCHAR(255)
    created_at : TIMESTAMP
    updated_at : TIMESTAMP
    }

entity "products" {

-   ## product_id : INT
    name : VARCHAR(255)
    description : TEXT
    price : DECIMAL(10,2)
    manufacturer : VARCHAR(255)
    category : VARCHAR(50)
    created_at : TIMESTAMP
    updated_at : TIMESTAMP
    }

entity "admins" {

-   ## admin_id : INT
    email : VARCHAR(255)
    password_hash : VARCHAR(255)
    created_at : TIMESTAMP
    updated_at : TIMESTAMP
    }

users --|{ products
products --|{ users
admins --|{ products

@enduml
