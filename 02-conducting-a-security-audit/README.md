\# Conducting a Security Audit



\## Project Description

A security audit of \*\*Botium Toys\*\*, a fictional company, scoped across their entire

security program — assets, internal processes, and adherence to controls and

compliance best practices. The audit identifies existing gaps and recommends

improvements to strengthen the company's overall security posture.



\## Scope and Goals

\*\*Scope:\*\* The entire security program at Botium Toys — all assets, internal

processes, and procedures related to control implementation and compliance.



\*\*Goals:\*\* Assess existing assets and complete a controls/compliance checklist to

determine what needs to be implemented to improve the security posture.



\## Assets in Scope

On-premises equipment, employee devices, storefront/warehouse inventory,

core business systems (accounting, telecom, database, security, e-commerce,

inventory management), internet and internal network infrastructure, data

retention/storage, and legacy systems requiring manual monitoring.



\## Risk Assessment

\*\*Risk score: 8/10\*\* — driven primarily by missing controls and weak compliance

adherence.



Key findings:

\- All employees have access to internally stored data, including cardholder

&nbsp; data and customer PII/SPII — no least privilege or separation of duties in place.

\- No encryption on stored/transmitted credit card data.

\- No intrusion detection system (IDS); no disaster recovery plan or backups.

\- Password policy exists but doesn't meet modern complexity requirements, and

&nbsp; there's no centralized password management system.

\- Firewall and antivirus are in place and functioning.

\- Physical security (locks, CCTV, fire detection) is adequate.

\- GDPR breach-notification plan (72-hour) and data-handling policies are in place,

&nbsp; but PCI DSS and NIST CSF are not being followed properly.



\## Controls and Compliance Checklist

Assessed controls against three categories — \*\*Administrative/Managerial\*\*,

\*\*Technical\*\*, and \*\*Physical/Operational\*\* — and against three compliance

frameworks: \*\*PCI DSS\*\*, \*\*GDPR\*\*, and \*\*SOC (Type 1/2)\*\*.



Result: defense-in-depth is weak across the board. Preventative controls (least

privilege, separation of duties, password management) are largely missing, and

PCI DSS in particular is not maintained despite the company processing online

payments.



\## Recommendations

\- Implement PCI DSS compliance given the company's use of online payment processing.

\- Properly align with NIST CSF across all three control categories.

\- Deploy an IDS and consider a SIEM for continuous monitoring.

\- Enforce least privilege to limit customer data exposure across departments.

\- Apply OWASP principles to account lifecycle management.

\- Formalize policies/procedures and reinforce them with regular security

&nbsp; awareness training for employees.



\## What This Demonstrates

Structuring a full-scope security audit: mapping assets, assessing controls across

administrative, technical, and physical categories, scoring risk, checking compliance

against PCI DSS/GDPR/SOC, and translating findings into prioritized, actionable

recommendations.



\## Files

\- `docs/Scope\_\_goals\_\_and\_risk\_assessment\_report\_\_Botium\_Toys\_.pdf` — full scope, asset inventory, and risk assessment

\- `docs/Control\_Categories.pdf` — reference: control types and categories used in the assessment

\- `docs/Controls\_and\_compliance\_checklist.pdf` — completed checklist and findings

