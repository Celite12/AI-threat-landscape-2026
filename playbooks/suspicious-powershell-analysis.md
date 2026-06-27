# Suspicious PowerShell Analysis Playbook

## Purpose

This playbook helps SOC analysts investigate suspicious PowerShell activity.

---

# Common Indicators

Examples include:

- Encoded PowerShell commands
- Base64 strings
- Hidden execution windows
- Downloaded scripts
- Network connections to unknown hosts

---

# Potential Threats

PowerShell abuse may indicate:

- Fileless malware
- Ransomware
- Credential theft
- Persistence mechanisms
- Data exfiltration

---

# Initial Investigation Steps

1. Preserve logs.
2. Identify the user account involved.
3. Review command history.
4. Determine network activity.
5. Check for privilege escalation.

---

# Indicators of Compromise (IOCs)

Examples:

- Encoded commands
- New administrator accounts
- Failed logins followed by success
- Large outbound traffic
- Scheduled task creation

---

# Containment

Recommended actions:

- Isolate affected systems.
- Disable compromised accounts.
- Block malicious connections.
- Preserve forensic evidence.

---

# Recovery

- Remove malicious scripts.
- Review persistence mechanisms.
- Patch vulnerabilities.
- Reset credentials.

---

# Security+ Concepts Applied

- Persistence
- Incident Response
- Least Privilege
- Defense in Depth
- Threat Detection
- Security Monitoring

---

# Analyst Notes

Hidden administrator accounts frequently indicate:

> Persistence

Encoded PowerShell commands often suggest:

> Fileless malware or advanced attack techniques.

Large outbound traffic may indicate:

> Data exfiltration or double-extortion ransomware activity.
