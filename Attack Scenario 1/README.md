# Attack 1 Summary: AI Generated External phishing email utilising admin credentials

## Stages of the Attack

### Origins
The attack is initiated by an attacker leveraging a long history of cyber attack techniques. The attacker identifies the Solari Health 360 application as a target due to its sensitive health data and public-facing nature.

### Reconnaissance
The attacker conducts research to identify vulnerabilities in the Solari Health 360 application. This includes gathering information about the application's architecture, technologies used, and potential weaknesses in its security measures.

### Weaponization
Exploit payloads are crafted specifically to target vulnerabilities identified in the Solari Health 360 application. Additionally, the attacker creates sophisticated phishing emails tailored to appear legitimate and enticing to users of the application.

### Delivery
Phishing emails containing malicious links or attachments are sent to users of the Solari Health 360 application. These emails may appear to come from trusted sources or mimic official communication from the application itself, increasing the likelihood of successful exploitation.

### Exploitation
The attacker exploits vulnerabilities in the Solari Health 360 application, such as SQL injection or cross-site scripting (XSS) vulnerabilities, to gain unauthorized access. By exploiting these vulnerabilities, the attacker can execute arbitrary code or extract sensitive information from the application's database.

### Installation
Once access is gained, the attacker establishes a foothold within the Solari Health 360 application's infrastructure. This may involve creating backdoor accounts or implanting malware to maintain persistent access to the system.

### Actions on Objectives
With access to the Solari Health 360 application, the attacker can exfiltrate sensitive health data stored within the application's database. Additionally, the attacker may manipulate patient records, tamper with medical information, or disrupt the application's functionality for malicious purposes.


```mermaid
flowchart LR


    A[GitHub Repos] --> B{CI/CD Pipeline GH Actions}
    A[Reconnaissance] -->|Identify target| B
    B[Reconnaissance] -->|Gather information| B
    B[Weaponization] -->|Craft malicious payload| D
    D[Delivery] -->|Send phishing email| D
    D[Delivery] -->|Trick user to download payload| D
    D[Exploitation] -->|Execute payload| D
    D[Exploitation] -->|Gain access to web server| H
    H[Installation] -->|Install backdoor| H
    H[Installation] -->|Establish persistence| H
    H[Command and Control] -->|Communicate with C&C server| H
    H[Command and Control] -->|Issue commands| L
    H[Actions on Objectives] -->|Steal sensitive data| M

