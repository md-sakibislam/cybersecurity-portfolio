\# Identifying Vulnerabilities for a Small Business



\## Project Description

A vulnerability assessment of a business's publicly accessible database server,

using \*\*NIST SP 800-30 Rev. 1\*\* as the guiding framework for risk analysis —

identifying threat sources, threat events, and calculating risk scores to prioritize

remediation.



\## System Description

Linux-based server (powerful CPU, 128GB RAM) hosting a MySQL database, with

IPv4 network connectivity and SSL/TLS-encrypted connections.



\## Scope

Assessment of current access controls over a three-month period (June–August),

guided by NIST SP 800-30 Rev. 1 risk analysis methodology.



\## Risk Assessment

Risk scores calculated as \*\*Likelihood × Severity\*\* (each scored 1–3, per NIST SP

800-30's qualitative/quantitative scale):



| Threat Source | Threat Event | Likelihood | Severity | Risk |

|---|---|---|---|---|

| External attacker | Gain unauthorized access to the database | 3 | 3 | \*\*9\*\* |

| Malicious insider | Access or modify sensitive database information | 2 | 3 | \*\*6\*\* |

| Unauthorized user | Steal sensitive data from the database | 2 | 3 | \*\*6\*\* |

| Employee | Accidentally grant excessive access privileges | 2 | 2 | \*\*4\*\* |



The highest risk identified is external unauthorized access to the database,

followed closely by insider threats and data theft by unauthorized users.



\## Remediation Strategy

\- Implement authentication, authorization, and auditing (AAA) controls, including

&nbsp; strong password requirements, role-based access control, and multi-factor

&nbsp; authentication.

\- Replace SSL with TLS for encrypting data in motion.

\- Apply IP allow-listing restricted to corporate offices to block unsolicited

&nbsp; internet-based connection attempts to the database.



\## What This Demonstrates

Applying the NIST SP 800-30 risk assessment methodology to a real system:

identifying human, technological, and environmental threat sources; scoring

likelihood and severity; calculating composite risk scores; and translating

findings into a concrete, prioritized remediation plan.



\## Files

\- `docs/Vulnerability\_assessment\_report.pdf` — the completed assessment and risk table

\- `docs/NIST\_SP\_800-30\_Rev\_\_1.pdf` — reference guide used for the risk methodology

