  ```mermaid
flowchart TD
    subgraph "User Interface"
        UI[User Interface]
    end
    subgraph "Frontend (EC2)"
        FE[Frontend Server]
    end
    subgraph "Backend"
        BE[Backend Server]
    end
    subgraph "Database"
        DB[Database Server]
    end
    subgraph "External Services"
        CnC[Command and Control Server]
    end
    UI --> FE
    FE --> BE
    BE --> DB
    BE --> CnC