# Phishing Investigation Playbook

## Purpose

This playbook provides guidance for investigating suspected phishing incidents.

---

# Identification

Common indicators include:

- Unexpected email attachments
- Requests for credentials
- Urgent financial requests
- Misspelled domains
- Suspicious hyperlinks

---

# Initial Actions

SOC analysts should:

1. Preserve the email.
2. Collect headers.
3. Identify affected users.
4. Determine whether links were clicked.
5. Determine whether attachments were opened.

---

# Indicators of Compromise (IOCs)

Examples include:

- Unknown sender domains
- Newly created external accounts
- Suspicious PowerShell activity
- Credential harvesting pages
- Large outbound connections

---

# Containment

Recommended actions:

- Isolate affected systems.
- Disable compromised accounts.
- Block malicious domains.
- Reset credentials.
- Revoke active sessions.

---

# Eradication

Security teams should:

- Remove malware.
- Patch affected systems.
- Scan endpoints.
- Validate account integrity.

---

# Recovery

Organizations should:

- Restore systems.
- Monitor for persistence.
- Re-enable accounts safely.
- Conduct post-incident reviews.

---

# Lessons Learned

Questions to ask:

- How did the email bypass protections?
- Was MFA enabled?
- Were users properly trained?
- Can detection rules be improved?

---

# Security+ Concepts Applied

- Defense in Depth
- MFA
- Least Privilege
- Incident Response
- User Awareness Training
- Zero Trust
