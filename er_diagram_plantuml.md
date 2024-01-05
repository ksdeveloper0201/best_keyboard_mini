@startuml
!define TABLE class
!define PRIMARY_KEY_FIELD "{bg:wheat}"
!define FOREIGN_KEY_FIELD "{bg:lightyellow}"

!define ENTITY_BEGIN class [Entity]
!define ENTITY_END end

!define RELATION_BEGIN class [Relation]
!define RELATION_END end

!define PRIMARY_KEY_FIELD class <<PK>> {bg:wheat}
!define FOREIGN_KEY_FIELD class <<FK>> {bg:lightyellow}

ENTITY_BEGIN users {
user_id INT <<PK>>
email VARCHAR(255)
password_hash VARCHAR(255)
created_at TIMESTAMP
updated_at TIMESTAMP
}
ENTITY_END

ENTITY_BEGIN products {
product_id INT <<PK>>
name VARCHAR(255)
description TEXT
price DECIMAL(10,2)
manufacturer VARCHAR(255)
category VARCHAR(50)
created_at TIMESTAMP
updated_at TIMESTAMP
}
ENTITY_END

ENTITY_BEGIN admins {
admin_id INT <<PK>>
email VARCHAR(255)
password_hash VARCHAR(255)
created_at TIMESTAMP
updated_at TIMESTAMP
}
ENTITY_END

RELATION_BEGIN
users "1" -- "N" products : Writes
RELATION_END

RELATION_BEGIN
admins "1" -- "N" products : Manages
RELATION_END

@enduml
