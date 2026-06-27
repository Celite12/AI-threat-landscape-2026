# Brute Force Detection Playbook

## Purpose

This playbook provides guidance for identifying, investigating, containing, and recovering from brute force attacks.

These attacks attempt to gain unauthorized access through repeated authentication attempts.

---

# What is a Brute Force Attack?

A brute force attack occurs when attackers repeatedly try passwords until one succeeds.

Common variants include:

- Traditional brute force
- Password spraying
- Credential stuffing
- Dictionary attacks

---

# Common Indicators

Potential indicators include:

- Multiple failed login attempts
- Account lockouts
- Successful logins after numerous failures
- Authentication attempts outside business hours
- Geographic anomalies
- Repeated access to privileged accounts

---

# Initial Investigation Steps

SOC analysts should:

1. Identify affected accounts.
2. Determine source IP addresses.
3. Review authentication logs.
4. Check for successful logins.
5. Identify privilege escalation attempts.

---

# Indicators of Compromise (IOCs)

Examples include:

- Hundreds of failed login attempts.
- Successful authentication after repeated failures.
- New administrator accounts.
- Unusual RDP activity.
- Geographic impossibilities.
- Multiple accounts targeted simultaneously.

---

# Attack Variants

## Traditional Brute Force

Many passwords are attempted against a single account.

Example:

```text
admin
password1
password2
password3
```

---

## Password Spraying

A single common password is attempted across many accounts.

Example:

```text
Summer2026!
```

against:

- jsmith
- jdoe
- bwilliams
- cwhite

This technique reduces account lockouts.

---

## Credential Stuffing

Previously stolen credentials are reused on other systems.

Attackers exploit password reuse habits.

---

# MITRE ATT&CK Mapping

## T1110 – Brute Force

Sub-techniques include:

- T1110.001 Password Guessing
- T1110.003 Password Spraying
- T1110.004 Credential Stuffing

---

# Containment

Recommended actions:

- Disable affected accounts.
- Block malicious IP addresses.
- Force password resets.
- Terminate active sessions.
- Enable additional monitoring.

---

# Recovery

Organizations should:

- Re-enable accounts safely.
- Require strong passwords.
- Review access privileges.
- Monitor for persistence.
- Conduct user awareness training.

---

# Security Controls

## Multi-Factor Authentication (MFA)

MFA remains one of the strongest protections against brute force attacks.

Even if attackers discover passwords, additional authentication factors reduce risk.

---

## Account Lockout Policies

Organizations should define:

- Failed login thresholds
- Lockout durations
- Administrative review procedures

---

## Strong Password Policies

Recommended practices include:

- Long passphrases
- Password managers
- Unique credentials
- Regular security training

---

## Network Segmentation

Administrative services should never be directly exposed to the public internet.

Examples:

- RDP (3389)
- SSH (22)
- Administrative web portals

---

# Security+ Concepts Applied

- Authentication
- Access Control
- MFA
- Least Privilege
- Defense in Depth
- Incident Response
- Threat Detection

---

# Analyst Notes

Multiple failed logins followed by a successful authentication commonly indicate:

> A successful brute force attack.

Exposed RDP services increase organizational risk and are frequently targeted by ransomware operators.

MFA significantly reduces the effectiveness of password-based attacks.
