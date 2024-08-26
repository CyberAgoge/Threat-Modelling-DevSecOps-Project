  This is a an example of an attacker flow using mermaid.
  
  ```mermaid
  sequenceDiagram
    participant Attacker
    participant SolariHealthApp
    participant CnCServer
    participant BackendServer
    participant User

    activate Attacker
    Attacker->>SolariHealthApp: Identify Solari Health 360 app
    SolariHealthApp->>Attacker: Application identified
    deactivate Attacker

    activate Attacker
    Attacker->>SolariHealthApp: Craft exploit for known vulnerabilities
    SolariHealthApp->>Attacker: Exploit crafted
    deactivate Attacker

    activate Attacker
    Attacker->>SolariHealthApp: Deploy phishing campaign targeting app users
    SolariHealthApp->>User: Phishing email sent
    activate User
    User->>SolariHealthApp: Clicks on malicious link/download attachment
    SolariHealthApp->>User: Malware downloaded
    deactivate User
    deactivate Attacker

    activate Attacker
    Attacker->>SolariHealthApp: Trick users into downloading malware
    SolariHealthApp->>BackendServer: Malicious payload executed
    BackendServer->>CnCServer: Communication established
    CnCServer->>BackendServer: Commands issued
    BackendServer->>CnCServer: Actions performed
    deactivate Attacker
