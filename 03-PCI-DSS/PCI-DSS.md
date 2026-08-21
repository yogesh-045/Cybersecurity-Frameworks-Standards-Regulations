# 💳 PCI DSS — Payment Card Industry Data Security Standard

## 📌 Overview

**PCI DSS = Payment Card Industry Data Security Standard**

PCI DSS is a security standard designed to protect **payment account data** and reduce the risk of payment-card data compromise.

It applies to entities that **store, process, or transmit payment account data**, as well as organizations whose systems can affect the security of that environment.

### Simple Definition

> **PCI DSS is a security standard that defines requirements for protecting payment-card data and securing systems involved in payment-card processing.**

---

# 🧠 Who Maintains PCI DSS?

PCI DSS is maintained by the:

**PCI Security Standards Council (PCI SSC)**

The Council was founded by major payment brands including:

* Visa
* Mastercard
* American Express
* Discover
* JCB

The PCI SSC develops and maintains PCI security standards and supporting programs.

---

# 🎯 Why Does PCI DSS Exist?

Payment-card information is valuable to attackers.

If card data is compromised, attackers may attempt:

* Fraud
* Unauthorized transactions
* Identity-related attacks
* Card cloning
* Account takeover
* Data resale

PCI DSS establishes security requirements intended to reduce these risks.

---

# 💳 What Data Does PCI DSS Protect?

Important concepts include:

## Cardholder Data

Cardholder data can include:

* Primary Account Number (PAN)
* Cardholder name
* Expiration date
* Service code

### PAN

**PAN = Primary Account Number**

It is the payment-card number associated with the account.

Example:

```text
4111 1111 1111 1111
```

This is an example format only, not a real account.

---

# 🔐 Sensitive Authentication Data

PCI DSS also distinguishes **Sensitive Authentication Data (SAD)**.

Examples can include:

* Full track data
* Card verification codes/values
* PINs and PIN blocks

A particularly important concept:

> Sensitive authentication data has stricter handling requirements, especially after authorization.

Do not assume that because data is encrypted, it can automatically be stored indefinitely.

---

# 🏢 Cardholder Data Environment

**CDE = Cardholder Data Environment**

The CDE consists of systems and components involved in storing, processing, or transmitting payment account data, along with components that may affect its security.

Conceptually:

```text
                  Internet
                     ↓
                Web Server
                     ↓
              Payment System
                     ↓
              Cardholder Data
                     ↓
                  CDE
```

Organizations should understand and appropriately define the scope of their cardholder-data environment.

---

# 🎯 PCI DSS Core Objective

The fundamental objective is:

```text
Protect Payment Account Data
            ↓
Reduce Security Risk
            ↓
Reduce Probability / Impact
of Card Data Compromise
```

---

# 📋 PCI DSS Requirements

PCI DSS v4.0.1 contains **12 high-level requirements**.

They are grouped around six broad security goals.

---

# 🟦 Goal 1 — Build and Maintain a Secure Network and Systems

## Requirement 1

### Install and Maintain Network Security Controls

Organizations must establish and maintain appropriate network-security controls.

Examples:

* Firewalls
* Network segmentation
* Traffic filtering
* Security configurations
* Network access restrictions

### Example

```text
Internet
   ↓
Firewall
   ↓
DMZ
   ↓
Payment Application
   ↓
CDE
```

---

## Requirement 2

### Apply Secure Configurations to All System Components

Systems should be securely configured.

Examples:

* Remove unnecessary services
* Change default credentials
* Disable unnecessary protocols
* Harden operating systems
* Secure network devices

### Example

```text
Default Configuration
       ↓
Hardening
       ↓
Secure Baseline
       ↓
Continuous Review
```

---

# 🟩 Goal 2 — Protect Account Data

## Requirement 3

### Protect Stored Account Data

Organizations must protect stored account data according to applicable PCI DSS requirements.

Security mechanisms may include:

* Encryption
* Tokenization
* Truncation
* Strong cryptography
* Data-retention controls

### Important Principle

> **Do not store payment data that you do not need.**

Data minimization reduces the attack surface.

---

## Requirement 4

### Protect Cardholder Data with Strong Cryptography During Transmission Over Open, Public Networks

When payment account data travels across open/public networks, appropriate cryptographic protection is required.

Example:

```text
Customer
   ↓
HTTPS / TLS
   ↓
Payment Server
```

### Important

Encryption in transit protects data while it is being transmitted.

It does not automatically solve:

* Weak authentication
* Excessive privileges
* Malware
* Vulnerable applications
* Poor logging

---

# 🟥 Goal 3 — Maintain a Vulnerability Management Program

## Requirement 5

### Protect All Systems and Networks from Malicious Software

Organizations should protect applicable systems against malware.

Examples:

* Anti-malware
* EDR
* Endpoint security
* Malware detection
* Security monitoring

SOC example:

```text
Malware
   ↓
EDR
   ↓
Detection
   ↓
SIEM
   ↓
SOC Alert
```

---

## Requirement 6

### Develop and Maintain Secure Systems and Software

Security must be incorporated into system and software development.

Examples:

* Secure coding
* Vulnerability remediation
* Patch management
* Code review
* Security testing
* Change management

### Secure Development Lifecycle

```text
Design
  ↓
Development
  ↓
Security Review
  ↓
Testing
  ↓
Deployment
  ↓
Monitoring
```

---

# 🟨 Goal 4 — Implement Strong Access Control Measures

## Requirement 7

### Restrict Access to System Components and Cardholder Data by Business Need to Know

Access should be based on legitimate business requirements.

### Principle

> **Need-to-know + least privilege**

Example:

```text
Employee
   ↓
Business Role
   ↓
Required Access
   ↓
Only Necessary Resources
```

A database administrator may need database access, while a normal employee may not.

---

## Requirement 8

### Identify Users and Authenticate Access to System Components

Organizations need mechanisms to uniquely identify and authenticate users and other entities where applicable.

Examples:

* Unique user IDs
* Passwords
* MFA
* Authentication mechanisms
* Account lifecycle management

### Authentication

```text
Username
   +
Password
   +
MFA
   ↓
Identity Verification
```

---

## Requirement 9

### Restrict Physical Access to Cardholder Data and Systems

Physical security matters too.

Examples:

* Data-center access controls
* Badge systems
* Visitor controls
* Physical monitoring
* Secure media storage
* Secure media destruction

---

# 🟪 Goal 5 — Regularly Monitor and Test Networks

## Requirement 10

### Log and Monitor All Access to System Components and Cardholder Data

This requirement is particularly relevant to SOC Analysts.

Organizations need appropriate:

* Audit logs
* Security logs
* Authentication logs
* Access logs
* Monitoring
* Log review
* Time synchronization
* Incident investigation capabilities

### SOC Architecture

```text
Servers
   ↓
Firewalls
   ↓
Applications
   ↓
Authentication Systems
   ↓
        SIEM
         ↓
    Correlation
         ↓
       Alert
         ↓
        SOC
```

---

# 🔎 What Does a SOC Analyst Look For?

Example:

```text
User: admin
Source IP: unusual
Time: 03:15 AM
Action: Database access
Volume: unusually high
```

SOC investigation:

```text
Unusual Access
      ↓
Check User
      ↓
Check Source IP
      ↓
Check Authentication
      ↓
Check Previous Activity
      ↓
Check Database Logs
      ↓
Determine Legitimacy
      ↓
Escalate if Necessary
```

---

# Requirement 11

### Regularly Test Security Systems and Processes

Organizations should test security mechanisms and processes according to applicable PCI DSS requirements.

Examples include:

* Vulnerability scans
* Penetration testing
* Intrusion-detection/prevention testing
* Wireless testing where applicable
* Security-control testing
* Change verification

### Basic Security Testing Cycle

```text
Test
 ↓
Find Weakness
 ↓
Remediate
 ↓
Retest
 ↓
Verify
```

---

# 🟧 Goal 6 — Maintain an Information Security Policy

## Requirement 12

### Support Information Security with Organizational Policies and Programs

Security needs organizational governance.

Examples:

* Information-security policies
* Acceptable-use policies
* Incident-response plans
* Security awareness
* Risk management
* Roles and responsibilities
* Third-party security management

### Security Is Not Only Technology

```text
People
  +
Process
  +
Technology
  +
Governance
      ↓
Security
```

---

# 📊 PCI DSS 12 Requirements — Quick Table

| #  | Requirement                   | Main Focus           |
| -- | ----------------------------- | -------------------- |
| 1  | Network Security Controls     | Network protection   |
| 2  | Secure Configurations         | Hardening            |
| 3  | Protect Stored Account Data   | Data protection      |
| 4  | Protect Data in Transit       | Cryptography         |
| 5  | Protect Against Malware       | Malware defense      |
| 6  | Secure Systems and Software   | Secure development   |
| 7  | Restrict Access               | Need-to-know         |
| 8  | Identify & Authenticate Users | Authentication       |
| 9  | Restrict Physical Access      | Physical security    |
| 10 | Log & Monitor                 | Logging / monitoring |
| 11 | Test Security Systems         | Security testing     |
| 12 | Information Security Policy   | Governance           |

---

# 🔐 PCI DSS and CIA Triad

PCI DSS supports the traditional security objectives.

## Confidentiality

Protect cardholder information from unauthorized disclosure.

Examples:

* Encryption
* Access control
* Tokenization

## Integrity

Protect systems and data from unauthorized modification.

Examples:

* File integrity monitoring
* Change management
* Logging

## Availability

Maintain availability of payment systems.

Examples:

* Redundancy
* Resilience
* Monitoring
* Incident response

---

# 🧩 Tokenization

**Tokenization** replaces sensitive payment data with a non-sensitive substitute called a token.

Example:

```text
Actual PAN
    ↓
Tokenization
    ↓
Token
```

Example:

```text
PAN:
4111 1111 1111 1111

Token:
tok_8F4K2X...
```

The token is not simply another form of the original card number; its security properties and usage depend on the tokenization system.

---

# 🔒 Encryption vs Tokenization

These are different.

### Encryption

Transforms data using cryptographic techniques.

```text
Plaintext
   ↓
Encryption
   ↓
Ciphertext
```

### Tokenization

Replaces sensitive data with a token.

```text
Sensitive Data
      ↓
Tokenization
      ↓
Token
```

---

# ✂️ Truncation

Truncation means displaying/storing only part of a PAN.

Example:

```text
Original:
4111 1111 1111 1111

Displayed:
************1111
```

The exact permitted representation depends on the applicable PCI DSS requirements.

---

# 🚨 PCI DSS and Incident Response

PCI DSS requires organizations to maintain appropriate incident-response capabilities.

Example:

```text
Card Data Compromise
        ↓
Detection
        ↓
Incident Response
        ↓
Containment
        ↓
Investigation
        ↓
Remediation
        ↓
Recovery
        ↓
Lessons Learned
```

This overlaps heavily with SOC operations.

---

# 🛡️ PCI DSS and SIEM

SIEM can help organizations:

* Centralize logs
* Correlate events
* Detect suspicious activity
* Investigate incidents
* Monitor authentication
* Track privileged activity
* Support audit requirements

### Example

```text
Firewall Logs
      +
Windows Logs
      +
Linux Logs
      +
Database Logs
      +
Application Logs
      ↓
     SIEM
      ↓
Correlation
      ↓
Security Alert
      ↓
SOC Investigation
```

---

# 🧠 Example SOC Investigation

Suppose an attacker compromises an administrator account.

### Observed activity

```text
02:00 → Failed login
02:02 → Successful login
02:03 → Privilege escalation
02:05 → Database access
02:07 → Large data query
02:10 → External connection
```

### SOC investigation

```text
Authentication Logs
        ↓
Privileged Access Logs
        ↓
Database Logs
        ↓
Network Logs
        ↓
SIEM Correlation
        ↓
Incident Investigation
```

The analyst determines whether the activity represents unauthorized access or another security event.

---

# 🏢 PCI DSS Scope

Scope is a critical concept.

The organization should determine which systems, people, processes, and technologies are relevant to payment-account-data security.

### Example

```text
Customer
   ↓
Payment Application
   ↓
Payment Processing
   ↓
Cardholder Data
   ↓
CDE
```

Systems that can affect the security of the CDE may also be relevant to scope.

---

# 🌐 Network Segmentation

Network segmentation can help isolate the CDE from other environments.

Example:

```text
                 Internet
                    ↓
               Firewall
                    ↓
             Public Web Tier
                    ↓
                   DMZ
                    ↓
             Payment Network
                    ↓
                   CDE
```

Segmentation can reduce attack surface and potentially reduce PCI DSS scope, but it does **not automatically remove systems from scope**. Proper validation and assessment are required.

---

# 👥 Third-Party Service Providers

Organizations often use third parties for:

* Payment processing
* Cloud services
* Hosting
* Security services
* Managed infrastructure

Third-party relationships need appropriate security and responsibility management.

### Example

```text
Merchant
   ↓
Payment Service Provider
   ↓
Payment Processing
```

The use of a third party does not automatically eliminate the merchant's PCI DSS responsibilities.

---

# 🧠 PCI DSS Compliance

PCI DSS compliance means meeting the applicable PCI DSS requirements for the organization's environment.

Depending on the entity, validation may involve mechanisms such as:

* Self-Assessment Questionnaires
* Reports on Compliance
* Attestations
* Qualified Security Assessors

The exact validation method depends on the applicable payment-brand/acquirer requirements and transaction environment.

---

# ❗ PCI DSS Is NOT a Law

A common misconception:

> "PCI DSS is a government cybersecurity law."

**Incorrect.**

PCI DSS is an **industry security standard**.

However, contractual obligations, payment-brand rules, acquiring-bank requirements, or applicable laws/regulations may make compliance operationally or legally significant for a particular organization.

---

# 🔗 PCI DSS vs ISO 27001

| PCI DSS                         | ISO/IEC 27001                    |
| ------------------------------- | -------------------------------- |
| Payment-card security           | Information-security management  |
| Focused on payment account data | Broad information-security scope |
| 12 high-level requirements      | ISMS requirements                |
| Industry standard               | International standard           |
| Payment ecosystem               | Any applicable organization      |
| Strong payment-data focus       | Risk-management + ISMS focus     |

---

# 🔗 PCI DSS vs NIST CSF

| PCI DSS                        | NIST CSF                        |
| ------------------------------ | ------------------------------- |
| Payment-card security standard | Cybersecurity risk framework    |
| Specific security requirements | Flexible cybersecurity outcomes |
| Strong compliance focus        | Risk-management focus           |
| 12 requirements                | 6 Functions                     |
| Payment environment            | Broad organizational use        |

---

# 🔗 PCI DSS vs ISO 27002

| PCI DSS                       | ISO 27002                       |
| ----------------------------- | ------------------------------- |
| Payment security requirements | Control guidance                |
| Specific payment-data focus   | General information security    |
| Compliance-oriented           | Control implementation guidance |
| 12 requirements               | 93 controls in 2022 edition     |

---

# 🎯 SOC Analyst Relevance

For a SOC Analyst, the most important PCI DSS areas are:

### 🔥 High Priority

```text
Requirement 1
→ Network Security

Requirement 5
→ Malware Protection

Requirement 6
→ Secure Systems

Requirement 7
→ Access Control

Requirement 8
→ Authentication

Requirement 10
→ Logging & Monitoring

Requirement 11
→ Security Testing

Requirement 12
→ Incident Response / Security Policy
```

---

# 🧪 Practical SOC Scenario

## Scenario

An administrator accesses a payment database from an unusual IP.

### Step 1 — Detect

SIEM generates alert.

```text
Unusual Privileged Login
```

### Step 2 — Investigate

SOC checks:

* Username
* Source IP
* Authentication method
* MFA status
* Device
* Time
* Database activity

### Step 3 — Correlate

```text
Login
 ↓
Privilege
 ↓
Database Access
 ↓
Large Query
 ↓
Network Connection
```

### Step 4 — Respond

If malicious:

* Disable/restrict account
* Contain affected system
* Block malicious infrastructure
* Escalate incident
* Preserve relevant evidence

### Step 5 — Document

Record:

* Timeline
* Indicators
* Affected systems
* Actions
* Findings
* Root cause

---

# 🧠 Interview Questions

## Q1. What is PCI DSS?

PCI DSS is an industry security standard designed to protect payment account data and secure environments involved in payment-card processing.

---

## Q2. What does PCI DSS stand for?

**Payment Card Industry Data Security Standard.**

---

## Q3. Who maintains PCI DSS?

The **PCI Security Standards Council (PCI SSC)**.

---

## Q4. How many high-level requirements does PCI DSS have?

**12 high-level requirements.**

---

## Q5. Which PCI DSS requirement is most relevant to SIEM?

**Requirement 10 — Log and Monitor All Access to System Components and Cardholder Data.**

---

## Q6. Which requirement focuses on authentication?

**Requirement 8 — Identify Users and Authenticate Access to System Components.**

---

## Q7. Which requirement focuses on access control?

**Requirement 7 — Restrict Access to System Components and Cardholder Data by Business Need to Know.**

---

## Q8. What is PAN?

**PAN = Primary Account Number.**

It is the payment-card account number.

---

## Q9. What is CDE?

**CDE = Cardholder Data Environment.**

It refers to the systems and components involved in storing, processing, or transmitting payment account data, together with components that can affect its security.

---

## Q10. Is PCI DSS a law?

**No.**

It is an industry security standard, although contractual and regulatory obligations may make it applicable or enforceable in particular contexts.

---

## Q11. What is tokenization?

Tokenization replaces sensitive payment data with a token that can be used within an appropriately designed payment system.

---

## Q12. What is the difference between encryption and tokenization?

Encryption transforms data cryptographically.

Tokenization substitutes sensitive data with a token.

---

## Q13. Why is logging important in PCI DSS?

Logging and monitoring support detection, investigation, accountability, and security oversight of activity affecting systems and payment account data.

---

# 📝 Quick Revision

```text
PCI DSS
   ↓
Payment Card Security
   ↓
Protect Payment Account Data
   ↓
Secure CDE
   ↓
12 Requirements
```

### Most Important for SOC

```text
R1  → Network Security
R2  → Secure Configuration
R3  → Stored Account Data
R4  → Data in Transit
R5  → Malware Protection
R6  → Secure Development
R7  → Access Control
R8  → Authentication
R9  → Physical Security
R10 → Logging & Monitoring
R11 → Security Testing
R12 → Security Policy
```

---

# ⭐ Key Takeaways

* **PCI DSS = Payment Card Industry Data Security Standard.**
* It protects payment account data.
* PCI DSS is maintained by the **PCI Security Standards Council**.
* PCI DSS v4.0.1 contains **12 high-level requirements**.
* **PAN** means Primary Account Number.
* **CDE** means Cardholder Data Environment.
* Requirement **10** is especially important for SOC analysts because it focuses on logging and monitoring.
* Requirement **7** focuses on access control.
* Requirement **8** focuses on identification and authentication.
* Requirement **11** focuses on testing security systems and processes.
* Requirement **12** focuses on information-security policies and programs.
* Encryption, tokenization, and truncation are different techniques.
* PCI DSS is an **industry standard, not a government law**.
* Compliance does not mean an organization can never be breached.
* PCI DSS should be understood together with network security, IAM, SIEM, vulnerability management, incident response, and secure configuration.

---

# 📚 Official References

* PCI Security Standards Council: https://www.pcisecuritystandards.org/
* PCI DSS: https://www.pcisecuritystandards.org/standards/pci-dss/
