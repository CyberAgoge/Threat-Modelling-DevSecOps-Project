# Summary MITRE ATT&CK Sequence

# Attack Description

The attacker is an APT who has conducted avdanced research on Solaris. The attacker initiates the attack by identifying key personnel who likely had admin credentials to production environments. This way the attacker does not need to bypass a WAF or any other security controls but will instead have direct access to the environments as if an admin.

# Methodology
The attack sequence below utilises the MITRE ATT&CK framework along with the commonly used techniques. 





```mermaid
flowchart TD
    style Reconnaissance fill:#F4D03F,stroke:#000,stroke-width:2px
    style Weaponization fill:#F5B041,stroke:#000,stroke-width:2px
    style Delivery fill:#EB984E,stroke:#000,stroke-width:2px
    style Exploitation fill:#E59866,stroke:#000,stroke-width:2px
    style Installation fill:#DC7633,stroke:#000,stroke-width:2px
    style Command_Control fill:#CA6F1E,stroke:#000,stroke-width:2px
    style Actions_Objectives fill:#BA4A00,stroke:#000,stroke-width:2px
    style MITRE fill:#85C1E9,stroke:#000,stroke-width:2px

    Reconnaissance[Reconnaissance] -->|Attacker searches Linkedin for admin users of Solaris with credentials to AWS| Weaponization[Weaponization]
    Weaponization[Weaponization] -->|Craft exploit for known vulnerabilities| Delivery[Delivery]
    Delivery[Delivery] -->|Deploy phishing campaign targeting app users| Exploitation[Exploitation]
    Exploitation[Exploitation] -->|Trick users into downloading malware| Installation[Installation]
    Installation[Installation] -->|Gain access to app backend| Command_Control[Command and Control]
    Command_Control[Command and Control] -->|Establish communication with C&C server| Actions_Objectives[Actions on Objectives]
    Actions_Objectives[Actions on Objectives] -->|Steal sensitive health data| Actions_Objectives[Actions on Objectives]
    Actions_Objectives[Actions on Objectives] -->|Manipulate patient records| Actions_Objectives[Actions on Objectives]

    subgraph MITRE_Attack[MITRE ATT&CK Techniques]
    style MITRE fill:#85C1E9,stroke:#000,stroke-width:2px
    Delivery -->|T1566.001 - Phishing| MITRE
    Exploitation -->|T1190 - Exploit Public-Facing Application| MITRE
    Exploitation -->|T1059.003 - Command and Scripting Interpreter| MITRE
    Installation -->|T1106 - Execution through API| MITRE
    Command_Control -->|T1102 - Web Service| MITRE
    Command_Control -->|T1105 - Ingress Tool Transfer| MITRE
    Actions_Objectives -->|T1136 - Create Account| MITRE
    Actions_Objectives -->|T1574 - Hijack Execution Flow| MITRE
    Actions_Objectives -->|T1565.001 - Data Manipulation| MITRE
    end
