Introduction to SIEM

Overview

This room introduced Security Information and Event Management (SIEM), explaining how organizations collect, process, correlate, and analyze security logs to detect suspicious activities and generate security alerts.

1. What is SIEM?

SIEM stands for Security Information and Event Management.

It is a security solution that collects logs from different systems and devices in a centralized location. It helps security analysts identify suspicious activities by processing logs, correlating events, and generating alerts.

2. Types of Log Sources

Host-Centric Logs

These logs record activities occurring inside devices and operating systems, such as:

- Login attempts.
- Process creation.
- Windows Registry changes.

Network-Centric Logs

These logs record network communication and traffic activities, such as:

- Web traffic.
- SSH connections.
- VPN connections.

3. Challenges of Log Analysis Without SIEM

Analyzing logs manually can be difficult because:

- Logs are distributed across multiple devices.
- Different systems use different log formats.
- Individual events may not provide enough context.
- The large volume of logs makes manual analysis time-consuming.

4. Core SIEM Functions

Function| Description
Centralized Collection| Collects logs from multiple sources in one location.
Parsing| Extracts useful fields from raw log data, such as usernames, timestamps, and processes.
Normalization| Standardizes log fields and formats across different sources.
Correlation| Connects related events from multiple sources to provide better context.
Alerting| Generates alerts when specific detection conditions are met.
Dashboards and Reporting| Displays events, alerts, and statistics for security monitoring.

5. Log Collection Methods

Logs can be forwarded to a SIEM using different methods:

- Agents or Forwarders.
- Syslog.
- Manual log uploads.
- Sending data to a listening network port.

6. Detection Rules and Alert Investigation

A detection rule is a logical condition used to identify specific patterns in log data.

When the defined conditions are met, the SIEM generates an alert for further investigation.

Lab Detection Rule

The room demonstrated a detection rule based on Windows Event ID 4688, which represents process creation.

The rule searched for process names containing:

- "miner"
- "crypt"

A matching event generated an alert indicating potentially suspicious cryptocurrency-mining activity.

7. Alert Classification

- True Positive: An alert correctly identifies activity that matches the malicious behavior being detected.
- False Positive: An alert is generated, but investigation determines that the activity is not malicious.

Analysts should investigate alerts and validate the available evidence before reaching a conclusion.

8. Practical Lab Findings

The investigation identified the following details:

Field| Finding
Suspicious Process| "cudominer.exe"
User| Chris
Hostname| HR_02
Detection Keyword| "miner"
Alert Classification| True Positive

These findings demonstrate how SIEM detection rules can help analysts identify suspicious process activity and investigate the affected endpoint.

9. Key Takeaways

- SIEM provides centralized security log management.
- Host-centric and network-centric logs provide different types of security information.
- Parsing and normalization prepare logs for effective analysis.
- Correlation connects related events and provides investigation context.
- Detection rules help identify suspicious activity.
- Alerts must be investigated and validated before classification.

Conclusion

This room provided an introduction to SIEM architecture, log collection methods, detection rules, and alert classification. Understanding these concepts is an important step toward performing security monitoring and alert investigation as a SOC Analyst.

---

Training Platform: TryHackMe
Room: Introduction to SIEM
Learning Track: Blue Team / SOC Analyst
Note: This report documents educational lab findings and does not represent professional incident-response experience.
