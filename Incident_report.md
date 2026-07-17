SOC Incident Investigation Report: Unauthorized SSH Enumeration

 1. Incident Overview
  Incident ID: INC-2026-001
  Date/Time of Detection:July 17, 2026
  Severity Level: Medium
  Impacted Asset: Local Linux Workstation (Kali Host)
   Detection Mechanism: Custom Host Intrusion Detection Script (`monitor.sh`)

2. Threat Analysis & Log Evidence
Our automated log-parsing utility flagged an anomalous spike in authentication failures targeting the SSH daemon (`sshd`).

Corrupted Log Excerpt:
```text
Failed password for invalid user fakeadmin from 127.0.0.1 port 54321 ssh2
Failed password for victimuser from 127.0.0.1 port 54322 ssh2
