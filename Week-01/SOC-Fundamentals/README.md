SOC Fundamentals – TryHackMe

Author: Mohamed Assem
Learning Path: SOC Analyst L1
Platform: TryHackMe
Room: SOC Fundamentals
Category: Blue Team / Security Operations
Status: Completed

1. Introduction

A Security Operations Center (SOC) is a dedicated team responsible for continuously monitoring an organization's systems and networks, detecting suspicious activities, investigating security alerts, and responding to security incidents.

2. Key SOC Concepts

The Three Pillars of SOC

- People: Security analysts, engineers, and managers.
- Process: Alert triage, investigation, escalation, and incident response.
- Technology: SIEM, EDR, firewalls, and monitoring tools.

SOC Analyst Levels

- L1: Initial alert monitoring, triage, documentation, and escalation.
- L2: Advanced investigation and correlation of security events.
- L3: Advanced threat analysis and incident response.

Other SOC Roles

- Security Engineer
- Detection Engineer
- SOC Manager

3. Alert Triage – The Five Questions

During an investigation, analysts should establish:

1. What? What happened?
2. When? When did it happen?
3. Where? Where did it happen?
4. Who? Which user or device was involved?
5. Why? Why did it happen, and what was the possible cause?

4. Essential Security Technologies

Technology| Main Function
SIEM| Collects and correlates logs from multiple sources.
EDR| Monitors endpoint activities and supports investigation and response.
Firewall| Controls incoming and outgoing network traffic.

5. Practical Lab – Port Scanning Investigation

Scenario: Investigating a port scanning alert.

Observed Information

Field| Value
Source IP| 10.0.0.8
Source Host| NESSUS
Destination IP| 10.0.0.3
Destination Host| JOE PC
Activity| Port Scanning
Classification| Intended

Investigation Findings

The scanning activity originated from the NESSUS machine, which was identified in the lab scenario as the vulnerability assessment team's device.

The activity was classified as intended based on the provided lab context.

The logs also showed a connection from the destination host back to the scanner on port 22.

Analyst Note: In a real SOC environment, an analyst must verify authorization, scan scope, source identity, and timing before classifying similar activity as legitimate.

6. Skills Practiced

- Understanding SOC operations.
- Security alert triage.
- Basic security log analysis.
- Understanding SIEM, EDR, and Firewall.
- Identifying potentially authorized network scanning.
- Documenting investigation findings.

7. Key Takeaways

This room introduced the SOC environment, analyst responsibilities, alert investigation workflow, and essential defensive security technologies.

It also demonstrated how contextual information helps analysts distinguish authorized security testing from suspicious activity.

8. Training Source

TryHackMe – SOC Fundamentals
https://tryhackme.com/room/socfundamentals

Disclaimer: This document records educational lab work and is not evidence of professional SOC employment experience.
