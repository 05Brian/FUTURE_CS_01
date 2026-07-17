# Vulnerability Assessment Report

**Future Interns — Cyber Security Track**
**Task 01: Vulnerability Assessment Report for a Live Website**
**Author:** Brian Amani Mlenge
**Repository:** `FUTURE_CS_01`

---

## 📌 Overview

This repository documents a vulnerability assessment conducted against **scanme.nmap.org**, a publicly available test host maintained by the Nmap Security Scanner Project. The target explicitly permits scanning and port-testing activity, satisfying the ethical and legal requirements for this task.

The assessment used **passive and low-impact techniques only**. No exploitation, credential attacks, or active attack simulation were performed at any stage.

## 🎯 Objective

- Identify common web and network security weaknesses on the target host.
- Classify each finding by risk level.
- Explain the findings in plain business language.
- Provide clear, actionable remediation steps.

## 🛠️ Tools Used

| Tool | Version | Category | Purpose |
|---|---|---|---|
| Nmap | 7.99 | Network scanner | Port scanning and service/version detection |
| OWASP ZAP | 2.17.0 | Web proxy | Passive HTTP traffic analysis |
| Firefox DevTools | Built-in | Browser utility | Manual response header verification |

## 🔍 Methodology

| Step | Phase | Tool Used | Description |
|---|---|---|---|
| 1 | Network enumeration | Nmap | Identify open ports, running services, and versions |
| 2 | Web application analysis | OWASP ZAP | Passive-mode traffic inspection only — no active attack payloads |
| 3 | Header verification | Firefox DevTools | Manually confirm HTTP response headers reported by ZAP |

## 📊 Summary of Findings

| # | Finding | Category | Risk Level | Evidence |
|---|---|---|---|---|
| 1 | Outdated SSH Service | Network Service | Medium | `nmap-scan-results.png` |
| 2 | Outdated Web Server Software | Network Service | Medium | `nmap-scan-results.png` |
| 3 | Missing Content Security Policy Header | HTTP Header | Medium | `devtools-headers.png` |
| 4 | Missing Anti-Clickjacking Header | HTTP Header | Medium | `devtools-headers.png` |
| 5 | Missing Strict-Transport-Security Header | HTTP Header | Medium | `devtools-headers.png` |
| 6 | Server Version Disclosure | Information Disclosure | Low | `zap-alerts.png` |
| 7 | Missing X-Content-Type-Options Header | HTTP Header | Low | `devtools-headers.png` |
| 8 | Minor Information Disclosures | Information Disclosure | Low / Informational | `zap-alerts.png` |

Full descriptions, evidence, and remediation steps for each finding are documented in the full report.

## 📁 Repository Structure

```
FUTURE_CS_01/
├── README.md
├── report/
│   └── Vulnerability_Assessment_Report.pdf
├── screenshots/
│   ├── nmap-version.png
│   ├── ping-connectivity.png
│   ├── nmap-scan-results.png
│   ├── nmap-traceroute.png
│   ├── zap-alerts.png
│   └── devtools-headers.png
└── scan-output/
    └── scanme_nmap_results.txt
```

## ✅ Scope and Authorization

Testing was limited strictly to `scanme.nmap.org`. The target's homepage explicitly states that scanning is authorized for testing purposes. No production systems, live users, or third-party services were accessed or affected during this assessment.

## 📄 Report

The full report, including detailed findings, evidence, and remediation recommendations, is available here:
[report/Vulnerability_Assessment_Report.pdf](./report/Vulnerability_Assessment_Report.pdf)
