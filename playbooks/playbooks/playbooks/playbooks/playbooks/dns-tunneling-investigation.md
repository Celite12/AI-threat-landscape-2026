# DNS Tunneling Investigation Playbook

## Purpose

This playbook provides guidance for identifying, investigating, and responding to suspected DNS tunneling activity.

DNS tunneling is commonly used for:

- Data exfiltration
- Command and control (C2)
- Bypassing network controls
- Malware communications

---

# What is DNS Tunneling?

DNS normally translates names like:

google.com → IP addresses.

Attackers abuse DNS by hiding data inside DNS requests and responses.

This allows malicious traffic to blend into normal network activity.

---

# Common Indicators

Potential indicators include:

- Large volumes of DNS traffic
- Long or unusual domain names
- High numbers of TXT record requests
- Communication with unknown domains
- Outbound traffic occurring after business hours
- DNS requests with encoded strings

---

# Initial Investigation Steps

SOC analysts should:

1. Identify affected hosts.
2. Review DNS server logs.
3. Analyze queried domains.
4. Determine whether data exfiltration occurred.
5. Check for related malware activity.

---

# Indicators of Compromise (IOCs)

Examples include:

- Excessive DNS queries from a single endpoint.
- Unusually long domain names.
- Base64-like encoded text.
- Communication with newly registered domains.
- Large outbound traffic on Port 53.

---

# MITRE ATT&CK Mapping

## T1071.004 – Application Layer Protocol: DNS

Attackers use DNS protocols for command and control communications.

---

## T1048 – Exfiltration Over Alternative Protocol

Data is transferred using non-standard methods to avoid detection.

---

# Containment

Recommended actions:

- Block malicious domains.
- Isolate affected systems.
- Restrict external DNS access.
- Force internal DNS resolution.
- Monitor additional endpoints for similar behavior.

---

# Eradication

Security teams should:

- Remove malware.
- Eliminate persistence mechanisms.
- Reset compromised credentials.
- Patch vulnerabilities.
- Update detection rules.

---

# Recovery

Organizations should:

- Restore normal DNS operations.
- Continue monitoring affected systems.
- Conduct threat hunting activities.
- Improve DNS security controls.

---

# Security Controls

Effective protections include:

## DNS Filtering

Blocks known malicious domains.

---

## Network Monitoring

Detects abnormal DNS activity patterns.

---

## SIEM Correlation

Examples:

- Splunk
- Wazuh
- Microsoft Sentinel

---

## Threat Intelligence

Compares domains against known indicators of compromise.

---

# Security+ Concepts Applied

- Data Exfiltration
- Defense in Depth
- Threat Detection
- Security Monitoring
- Incident Response
- Threat Intelligence

---

# Analyst Notes

Large outbound traffic over Port 53 may indicate:

> DNS tunneling and possible data exfiltration.

DNS traffic should always be analyzed in context with:

- Authentication logs
- Endpoint activity
- PowerShell execution
- User behavior

DNS remains one of the most common methods for stealthy command-and-control communications.
