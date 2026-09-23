\# Cybersecurity Incident Report



\## Project Description

Two incident response investigations conducted as a cybersecurity analyst, each

based on analyzing network traffic logs (via `tcpdump`/Wireshark) to identify the

root cause of a reported outage and determine the type of attack involved.



\## Incident 1: DNS Resolution Failure

\*\*Reported:\*\* Customers received a "destination port unreachable" error when

visiting `yummyrecipesforme.com` at 1:24 p.m.



\*\*Investigation:\*\* Packet sniffing with `tcpdump` showed UDP port 53 (DNS) as

unreachable, with ICMP error responses confirming the DNS server was not

responding to queries. The DNS flags on the outgoing UDP request (`A?` query

type) confirmed this was a DNS resolution attempt, not a routing issue elsewhere.



\*\*Conclusion:\*\* The DNS server was down or traffic to port 53 was being blocked —

likely caused by either a Denial of Service attack or a server misconfiguration.

Next step identified: determine which of the two by checking server status and

firewall rules for port 53.



\## Incident 2: TCP SYN Flood Attack

\*\*Reported:\*\* Website connection timeout errors.



\*\*Investigation:\*\* Logs showed a large volume of TCP SYN requests arriving from a

single unknown IP address (`203.0.113.0`), with no completed handshakes.



\*\*Analysis:\*\* In a normal TCP three-way handshake (SYN → SYN-ACK → ACK), the

server allocates resources after step 2 and waits for the final ACK. By sending SYN

packets without ever completing the handshake, the attacker forced the server to

hold open a large number of half-open connections simultaneously, exhausting its

resources and causing it to crash — a classic \*\*TCP SYN flood (DoS) attack\*\*.



\*\*Conclusion:\*\* The server crash under attack load is what produced the connection

timeout errors customers experienced.



\## What This Demonstrates

Reading and interpreting raw network traffic logs (DNS/ICMP and TCP handshake

behavior) to diagnose the root cause of an incident, distinguish between an

infrastructure failure and an active attack, and communicate findings in a

structured incident report format.



\## Files

\- `docs/Cybersecurity\_incident\_report\_network\_traffic\_analysis.pdf` — DNS failure investigation

\- `docs/Cybersecurity\_incident\_report.pdf` — TCP SYN flood investigation

\- `docs/How\_to\_read\_a\_Wireshark\_TCPHTTP\_log.docx` — reference guide for interpreting the Wireshark log

\- `docs/Wireshark\_TCPHTTP\_Log.xlsx` — raw log data referenced in the SYN flood analysis

