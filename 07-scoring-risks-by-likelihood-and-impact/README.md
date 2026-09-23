\# Scoring Risks by Likelihood and Impact



\## Project Description

A risk register built for a fictional bank, scoring identified risks using a

\*\*Likelihood × Severity\*\* matrix to prioritize which risks need to be addressed

first. The exercise applies a standard 1–3 risk-matrix scale (Rare/Likely/Certain ×

Low/Moderate/Catastrophic) to real organizational context.



\## Operational Context

A coastal bank in a low-crime area, with 100 on-premise and 20 remote employees,

serving 2,000 individual and 200 commercial accounts. Subject to strict financial

regulations, including maintaining sufficient daily cash reserves to meet Federal

Reserve requirements.



\## Risk Register



| Asset | Risk | Description | Likelihood | Severity | Priority |

|---|---|---|---|---|---|

| Funds | Business email compromise | Employee tricked into sharing confidential information | 2 | 2 | 4 |

| Compromised user database | Poor encryption | Customer data is poorly encrypted | 2 | 3 | 6 |

| Financial records | Data leak | Backup database server is publicly accessible | 3 | 3 | \*\*9\*\* |

| Theft | Unlocked safe | The bank's physical safe is left unlocked | 1 | 3 | 3 |

| Supply chain | Disruption | Delivery delays due to natural disasters | 1 | 2 | 2 |



\*\*Highest priority:\*\* the publicly accessible backup database server (risk score 9)

— both highly likely to be discovered and catastrophic in impact if exploited,

since it exposes financial records.



\## What This Demonstrates

Building a risk register from operational context: identifying assets and their

associated risks, scoring each on likelihood and severity using a standard risk

matrix, calculating a combined priority score, and using that score to determine

which risks require immediate remediation versus lower-priority monitoring.



\## Files

\- `docs/Risk\_register.pdf` — completed risk register with likelihood/severity scoring and sample risk matrix reference

