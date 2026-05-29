# Phishing Investigation Summary

## Alert Overview

A phishing email was detected during analysis in the SIEM dashboard. The email contained a suspicious attachment and an external URL attempting to imitate a legitimate login portal.

The investigation focused on:

* validating sender legitimacy
* extracting indicators of compromise
* identifying endpoint interaction
* determining whether malware execution occurred

---

## Initial Findings

* Sender domain appeared visually similar to a legitimate organization
* SPF validation failed
* Attachment used double file extension naming
* Embedded URL redirected users to an external credential harvesting page
* Domain reputation checks showed newly registered infrastructure

---

## Indicators Identified

### Suspicious Domain

malicious-login-support.com

### Sender Email

[support@security-check-mail.com](mailto:support@security-check-mail.com)

### SHA256 Hash

3f2c4d7a8b9c1e5d6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9

### Suspicious IP

185.220.101.15

---

## Investigation Steps

1. Reviewed email headers
2. Extracted attachment hashes
3. Investigated embedded URLs
4. Checked domain reputation
5. Queried SIEM logs for endpoint interaction
6. Investigated PowerShell activity
7. Reviewed suspicious child processes
8. Mapped findings to MITRE ATT&CK

---

## MITRE ATT&CK Mapping

| Tactic              | Technique                  |
| ------------------- | -------------------------- |
| Initial Access      | Phishing                   |
| Execution           | User Execution             |
| Command and Control | Application Layer Protocol |

---

## Final Assessment

The alert was classified as a true positive phishing attempt.

No evidence of successful malware execution was identified during the investigation window.

The suspicious domain and associated indicators were documented for future detection tuning and blocking activities.
