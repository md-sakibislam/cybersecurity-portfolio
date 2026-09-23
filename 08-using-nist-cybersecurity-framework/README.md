\# Using the NIST Cybersecurity Framework



\## Project Description

Applying the NIST Cybersecurity Framework's (CSF) five core functions —

\*\*Identify, Protect, Detect, Respond, Recover\*\* — to analyze and respond to a

real-world-style DDoS incident.



\## Incident: ICMP Flood DDoS Attack



\*\*Summary:\*\* All network services became unavailable. Investigation determined

the cause was a distributed denial-of-service (DDoS) attack using a flood of ICMP

packets. The team responded by blocking the attack traffic and shutting down

non-critical network services to preserve capacity for critical operations.



| NIST CSF Function | Applied Response |

|---|---|

| \*\*Identify\*\* | Confirmed an ICMP flood attack affecting the entire internal network; scoped all network resources requiring protection and restoration |

| \*\*Protect\*\* | Implemented a new firewall rule rate-limiting incoming ICMP packets; deployed an IDS/IPS to filter packets with suspicious attributes |

| \*\*Detect\*\* | Configured the firewall to validate source IP addresses and detect spoofing; installed network monitoring tools to flag unusual traffic patterns |

| \*\*Respond\*\* | Established a plan to isolate affected systems, restore critical services, analyze logs for abnormal activity, and report incidents to management/legal authorities as needed |

| \*\*Recover\*\* | Defined a recovery sequence: block future ICMP floods at the firewall, shut down non-critical services to cut internal traffic, restore critical services first, then reactivate non-critical services after packet timeout |



\## What This Demonstrates

Practical application of the NIST CSF's five functions as an end-to-end incident

lifecycle — from identifying what was affected, through protective and detective

controls, to a structured response and recovery sequence — rather than treating

the framework as a theoretical checklist.



\## Files

\- `docs/Incident\_report\_analysis.pdf` — completed NIST CSF incident analysis (ICMP flood/DDoS)

\- `docs/Applying\_the\_NIST\_CSF\_.pdf` — reference guide to the five core functions and their key questions

