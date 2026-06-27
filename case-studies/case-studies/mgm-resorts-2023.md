# MGM Resorts Social Engineering Attack (2023)

## Overview

In September 2023, MGM Resorts experienced a major cybersecurity incident that disrupted hotel operations, payment systems, and customer services.

Attackers reportedly used social engineering techniques to gain unauthorized access to internal systems.

---

# Attack Vector

The attackers allegedly contacted the IT help desk and impersonated employees.

Using publicly available information, they convinced support personnel to reset credentials and provide access.

This demonstrates that people can sometimes become the weakest link in security.

---

# MITRE ATT&CK Techniques

Potential techniques involved:

- T1566: Phishing / Social Engineering
- T1078: Valid Accounts
- T1136: Create Account
- T1486: Data Encryption for Impact

---

# Indicators of Compromise (IOCs)

Examples include:

- Unusual login activity
- Account resets outside normal procedures
- Privileged account changes
- Unauthorized access attempts
- Large volumes of outbound traffic

---

# Security Controls That Could Help

## Multi-Factor Authentication (MFA)

MFA reduces risks associated with stolen credentials.

---

## Zero Trust Architecture

Trust should never be granted solely because someone claims to be an employee.

---

## Security Awareness Training

Employees should verify identities through approved procedures.

---

## Least Privilege

Users should only possess the permissions necessary for their duties.

---

# Lessons Learned

Organizations should:

- Verify identities using multiple methods.
- Monitor privileged account activity.
- Implement strong incident response plans.
- Conduct regular social engineering exercises.
- Practice defense in depth.

---

# Personal Analysis

This incident demonstrates that cybersecurity is not only a technical problem.

Human behavior, processes, and verification procedures are equally important.

Security awareness, Zero Trust principles, and strong authentication controls remain critical defenses against modern attacks.
