**FUTURE_CS_01 — Vulnerability Assessment Report**  
**Future Interns  Cyber Security Track**  
   
 **Task 01: Vulnerability Assessment Report for a Live Website**  
Author: Brian Amani Mlenge  
   
   
**Overview**  
This repository documents a vulnerability assessment conducted against scanme.nmap.org, a publicly available test host maintained by the Nmap Security Scanner Project. The target explicitly permits scanning and port-testing activity, which satisfies the ethical and legal requirements for this task.  
The assessment used passive and low-impact techniques only. No exploitation, credential attacks, or active attack simulation were performed at any stage.  
**Objective**  
Identify common web and network security weaknesses on the target host, classify each by risk level, explain the findings in plain business language, and provide clear remediation steps.  
**Tools Used**  
| | | |  
|-|-|-|  
| **Tool** | **Version** | **Purpose** |   
| Nmap | 7.99 | Port scanning and service/version detection |   
| OWASP ZAP | 2.17.0 | Passive HTTP traffic analysis |   
| Firefox DevTools | Built-in | Manual response header verification |   
   
**Methodology**  
1. Network service enumeration using Nmap  
2. Passive web application analysis using OWASP ZAP (passive mode only)  
3. Manual verification of HTTP response headers using browser DevTools  
**Summary of Findings**  
| | | |  
|-|-|-|  
| **#** | **Finding** | **Risk Level** |   
| 1 | Outdated SSH Service | Medium |   
| 2 | Outdated Web Server Software | Medium |   
| 3 | Missing Content Security Policy Header | Medium |   
| 4 | Missing Anti-Clickjacking Header | Medium |   
| 5 | Missing Strict-Transport-Security Header | Medium |   
| 6 | Server Version Disclosure | Low |   
| 7 | Missing X-Content-Type-Options Header | Low |   
| 8 | Minor Information Disclosures | Low / Informational |   
   
Full descriptions, evidence, and remediation steps for each finding are documented in the report.  
**Repository Structure**  
FUTURE_CS_01/  
 ├── README.md  
 ├── report/  
 │   └── Vulnerability_Assessment_Report.pdf  
 ├── screenshots/  
 │   ├── nmap-version.png  
 │   ├── ping-connectivity.png  
 │   ├── nmap-scan-results.png  
 │   ├── nmap-traceroute.png  
 │   ├── zap-alerts.png  
 │   └── devtools-headers.png  
 └── scan-output/  
     └── scanme_nmap_results.txt  
   
**Scope and Authorization**  
Testing was limited strictly to scanme.nmap.org. The target's homepage explicitly states that scanning is authorized for testing purposes. No production systems, live users, or third-party services were accessed or affected during this assessment.  
**Report**  
The full report, including detailed findings, evidence, and remediation recommendations, is available here: [report/Vulnerability_Assessment_Report.pdf](./report/Vulnerability_Assessment_Report.pdf "./report/Vulnerability_Assessment_Report.pdf")  
