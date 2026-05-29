# MITRE ATT&CK Mapping Notes

These mappings were created during SOC alert investigations and malware analysis exercises.

| Technique           | ID        | Description                               |
| ------------------- | --------- | ----------------------------------------- |
| Phishing            | T1566     | Initial access through malicious email    |
| PowerShell          | T1059.001 | Command execution using PowerShell        |
| Scheduled Task      | T1053     | Persistence using scheduled tasks         |
| Command and Control | T1071     | Communication over common protocols       |
| Credential Dumping  | T1003     | Attempt to access stored credentials      |
| Registry Run Keys   | T1547.001 | Persistence through registry modification |

---

# Common Tactics Observed

* Initial Access
* Execution
* Persistence
* Discovery
* Command and Control

---

# Notes

Most investigations involved phishing delivery, suspicious PowerShell execution, or outbound HTTP communication.

MITRE ATT&CK mapping helped connect alerts to attacker behavior patterns instead of focusing only on isolated events.
