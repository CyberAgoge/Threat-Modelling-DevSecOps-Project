# Project Summary

This project is a new and revolutionary approach to Threat Modelling as a template that you can use. I have worked across a plethora of different industries in cyber security for over ten years and I have yet to find a suitable method to run threat modelling. I have therefore created this template for you to use either in your future DevSecOps role or for you to create a project to help you show on your CV/in interviews when asked about threat modelling. 

Threat modelling diagrams/models should also reside within the repos of the projects. This approach ensures teams underestand the threats to the applications and continue to own it.

To access the code for this repo please visit the following website for the full video and code to create your first threat modelling project: (https://cyberagoge.thinkific.com/courses/take/devsecops-bootcamp/texts/55130887-part-1-introduction-to-the-course) Sigg up and click free preview and visit project 4 for the code and video. 

Customise all of the below to a chosen application - this can be make believe or a running application you have created for your project as created during the bootcamp or a live, real application for your organisation. If the application is live and real I recommned you keep the repo private.

# Threat Modelling Workshop Summary

## Introduction
A 3 Hour threat modelling workshop took place to detail the runbook scenario of multiple AI attacks against the web-facing health care application Solaris Care Connect 360.

## Attendess
Care Connect Eng team, Product Managers, DevEx Engineers and the DevSecOps Team.

## Scope
4 Scenarios were run covering: (1) AI Generated External phishing email utilising admin credentials, (2) Attack against Machine Processes and the data lake, (3) SQL Injection attack and (4) Insider attack taking Quant algorithms.

## Methodology
All scenarios were run against the cyber attack killchain, utilising the Mitre Att&ack framework and STRIDE for control gap assessments. Culminating in identified risks. 

## Conclusion
A total of 4 high risks and 1 medium risks were found during the threat modelling workshop.

## Controls Required

- Regular security audits using ASVS specifically targeting the Solaris Health 360 application to detect vulnerabilities and weaknesses in its security measures.
- Patch management to ensure the Solari Health 360 application and its underlying technologies are up-to-date and protected against known vulnerabilities.
- Comprehensive employee training on phishing awareness to educate users of the Solaris Health 360 application about the risks of phishing attacks and how to identify and report suspicious emails.
- Implementation of a Web Application Firewall (WAF) tailored to the Solari Health 360 application's traffic to monitor and filter incoming requests for malicious activity.
- Deployment of Multi-factor Authentication (MFA) to enhance authentication security and prevent unauthorized access to the Solari Health 360 application.
- Continuous network traffic monitoring to detect and respond to suspicious activity within the Solari Health 360 application's infrastructure.
- Implementation of Role-based Access Control (RBAC) within the Solari Health 360 application to limit access to sensitive health data and functionalities based on user roles and permissions.

# Threat Modelling Process Summary

```mermaid
mindmap
  root((Attack Begins))
    STRIDE/MITRE ATT&CK/Kill Chain
      Conduct Inherent Risk Assesment
      ::icon(fa fa-book)
      Create Critical Asset List
        Schedule and Scope Threat Modelling Workshop
    Controls Required
      Risks<br/>Mitigations
      Risk Summary
        Redmeiation workflow
            Slack
            JIRA 
    Attack Scenarios
      Attack 1
      Attack 2
      Attack 3
      Attack 4

