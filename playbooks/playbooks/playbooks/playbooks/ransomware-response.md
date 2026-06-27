# Ransomware Response Playbook

## Purpose

This playbook provides guidance for identifying, containing, eradicating, and recovering from ransomware incidents.

The goal is to minimize operational impact, preserve evidence, and reduce the risk of data exfiltration.

---

# Identification

Common indicators include:

- Inaccessible files
- Encrypted file extensions
- Ransom notes
- Large volumes of outbound traffic
- Encoded PowerShell activity
- Creation of hidden administrator accounts
- Multiple failed logins followed by successful authentication

---

# Potential Attack Vectors

Ransomware commonly enters organizations through:

- Phishing emails
- Malicious attachments
- Exposed RDP services (Port 3389)
- Stolen credentials
- Unpatched vulnerabilities
- Third-party compromise

---

# Initial Analyst Actions

SOC analysts should:

1. Identify affected systems.
2. Preserve logs and forensic evidence.
3. Determine the initial infection vector.
4. Identify indicators of compromise (IOCs).
5. Notify incident response leadership.

---

# Containment (FIRST PRIORITY)

The first operational goal is containment.

Recommended actions:

- Disconnect infected systems from the network.
- Disable compromised accounts.
- Block malicious IP addresses.
- Prevent lateral movement.
- Isolate affected segments.

Why?

Containment prevents additional systems from becoming encrypted.

---

# Indicators of Compromise (IOCs)

Examples include:

- Encoded PowerShell commands
- Hidden administrator accounts
- Large outbound encrypted traffic
- Failed login attempts followed by successful access
- Suspicious scheduled tasks
- Unknown services or processes

---

# Data Exfiltration Concerns

Modern ransomware groups often use:

## Double Extortion

Attack sequence:

1. Steal sensitive data.
2. Encrypt organizational systems.
3. Demand payment.
4. Threaten public release of stolen information.

Security teams should investigate:

- Outbound traffic spikes
- Unusual DNS activity
- Cloud storage uploads
- Unauthorized file transfers

---

# Eradication

After containment:

- Remove malicious files.
- Eliminate persistence mechanisms.
- Patch vulnerabilities.
- Reset compromised credentials.
- Validate system integrity.

---

# Recovery

Organizations should:

- Restore systems from backups.
- Monitor for reinfection.
- Validate access controls.
- Conduct security reviews.
- Resume operations gradually.

---

# Lessons Learned

Questions to ask:

- How did attackers gain access?
- Was MFA enabled?
- Were backups properly protected?
- Could network segmentation have reduced impact?
- Were detection mechanisms effective?

---

# Security+ Concepts Applied

- Incident Response Lifecycle
- Persistence
- Defense in Depth
- Least Privilege
- MFA
- Network Segmentation
- Disaster Recovery
- Business Continuity
- RPO
- RTO

---

# Analyst Notes

Hidden administrator accounts commonly indicate:

> Persistence

Encoded PowerShell activity may indicate:

> Fileless malware or attacker automation.

Large outbound traffic may indicate:

> Data exfiltration and double-extortion tactics.

Containment should always occur before eradication.
