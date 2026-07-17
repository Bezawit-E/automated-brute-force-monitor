Linux Automated Threat Detection & Incident Parsing Script

Project Overview
This lightweight, native Linux utility automates the monitoring of authentication logs (`/var/log/auth.log`) to detect and log active SSH brute-force attacks. The script acts as a basic Host Intrusion Detection System (HIDS) by extracting source IPs, triaging thresholds, and auto-generating an incident response report file for security teams.

How It Works (Log Triage Logic)
The script utilizes Linux text processing strings to filter authentication failures:
1. Filters logs using `grep` for authentication failure flags.
2. Isolates the attacker IP addresses using `awk` parsing parameters.
3. Groups, counts, and filters addresses exceeding a customizable limit (Default: >3 attempts).

 Lab Deployment & Output
          Raw Log Input Example:
```text
Jul 17 20:10:05 dubian sshd: Failed password for invalid user fakeadmin from 127.0.0.1 port 54321 ssh2
