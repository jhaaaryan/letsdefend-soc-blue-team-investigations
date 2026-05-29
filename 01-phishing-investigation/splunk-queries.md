# Splunk Investigation Queries

These are example Splunk searches used during SOC investigation practice and alert triage exercises.

---

# Failed Login Attempts

```spl
index=windows EventCode=4625
| stats count by Account_Name, Source_Network_Address
```

Purpose:
Identify repeated failed login activity that may indicate brute-force attempts.

---

# Successful Logins

```spl
index=windows EventCode=4624
| stats count by Account_Name, Source_Network_Address
```

Purpose:
Compare successful logins against failed authentication attempts.

---

# PowerShell Execution Detection

```spl
index=windows powershell.exe
| stats count by host, user, CommandLine
```

Purpose:
Detect suspicious PowerShell execution and encoded commands.

---

# Suspicious Network Connections

```spl
index=network dest_ip=185.220.101.15
```

Purpose:
Identify outbound communication to suspicious IP addresses.

---

# Possible Persistence Activity

```spl
index=windows registry
| search Run OR RunOnce
```

Purpose:
Check for registry persistence mechanisms.

---

# New Service Installation

```spl
index=windows EventCode=7045
```

Purpose:
Detect newly installed services that may indicate malware persistence.
