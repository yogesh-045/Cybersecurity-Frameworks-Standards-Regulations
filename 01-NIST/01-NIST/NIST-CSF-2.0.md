# 🛡️ NIST Cybersecurity Framework (CSF) 2.0

## 📌 Overview

The **NIST Cybersecurity Framework (CSF)** is a cybersecurity risk-management framework developed by the **National Institute of Standards and Technology (NIST)**.

NIST CSF 2.0 provides a common structure that organizations can use to:

* Understand cybersecurity risks
* Assess cybersecurity risks
* Prioritize security activities
* Communicate cybersecurity priorities
* Improve cybersecurity risk management

CSF 2.0 is designed for organizations of different sizes, sectors, and levels of cybersecurity maturity. It does not prescribe one specific technology or security product. Instead, it describes desired cybersecurity outcomes and provides references to practices and controls that can help achieve them.

---

# 🧠 What is NIST?

**NIST = National Institute of Standards and Technology**

NIST is a U.S. government agency that develops standards, measurements, guidelines, and technical publications.

In cybersecurity, NIST publishes resources such as:

* NIST Cybersecurity Framework
* NIST Special Publications
* Security and privacy controls
* Risk-management guidance
* Incident-response guidance
* Cybersecurity and privacy guidance

---

# 📜 NIST CSF History

### CSF 1.0

The original Cybersecurity Framework was published in **2014** and was initially focused on critical infrastructure cybersecurity.

### CSF 1.1

NIST released CSF 1.1 in **2018**.

### CSF 2.0

NIST released **CSF 2.0 on February 26, 2024**.

The major update expanded the framework beyond its original critical-infrastructure focus and placed greater emphasis on **governance** and **cybersecurity supply-chain risk management**.

---

# 🎯 Purpose of NIST CSF

The primary purpose of the CSF is to help organizations manage cybersecurity risk.

It helps answer questions such as:

```text
What assets do we have?
        ↓
What risks do they face?
        ↓
What security controls do we need?
        ↓
Can we detect attacks?
        ↓
How do we respond?
        ↓
How do we recover?
```

---

# ⭐ NIST CSF 2.0 Core

The CSF Core is the central part of the framework.

It provides a taxonomy of high-level cybersecurity outcomes.

The Core is organized into:

```text
Functions
    ↓
Categories
    ↓
Subcategories
```

### Example

```text
Function
   ↓
Identify
   ↓
Asset Management
   ↓
Specific cybersecurity outcome
```

The Core is intended to provide a common language for discussing cybersecurity risk.

---

# 🔵 Six Functions of NIST CSF 2.0

NIST CSF 2.0 has six Functions:

```text
        GOVERN
           ↓
        IDENTIFY
           ↓
        PROTECT
           ↓
         DETECT
           ↓
        RESPOND
           ↓
        RECOVER
```

These Functions should not be treated as a strict one-way process.

Organizations may perform activities across multiple Functions simultaneously.

---

# 1️⃣ GOVERN

## Definition

**Govern** establishes and monitors the organization's cybersecurity risk-management strategy, expectations, and policy.

This is the major addition/emphasis in CSF 2.0.

### Main idea

> How should cybersecurity risk be governed?

Governance includes:

* Cybersecurity strategy
* Organizational policies
* Roles and responsibilities
* Risk management strategy
* Oversight
* Legal and regulatory requirements
* Supply-chain risk
* Risk appetite

### Example

A company decides:

> "Critical production systems must have centralized logging and continuous monitoring."

This becomes part of its cybersecurity governance and security expectations.

### SOC relevance

SOC analysts may work under policies and risk priorities established through governance.

---

# 2️⃣ IDENTIFY

## Definition

**Identify** helps the organization understand its current cybersecurity risks.

The organization needs to know:

* What assets exist?
* What data exists?
* Which systems are critical?
* What vulnerabilities exist?
* What threats exist?
* What business processes depend on these systems?

### Examples

Asset inventory:

```text
Web Server
Database Server
Employee Laptop
Domain Controller
Cloud Storage
Network Devices
```

Risk identification:

```text
Critical Database
      ↓
Contains sensitive information
      ↓
High-value target
      ↓
Higher security priority
```

### SOC relevance

SOC analysts need context about:

* Critical servers
* Important applications
* Users
* Network infrastructure
* Data
* Cloud resources

Without asset context, alert prioritization becomes difficult.

---

# 3️⃣ PROTECT

## Definition

**Protect** focuses on implementing appropriate safeguards to reduce cybersecurity risk.

Examples:

* Identity and access management
* Authentication
* MFA
* Security awareness
* Data security
* Protective technology
* Secure configuration

### Example

Risk:

```text
Stolen password
      ↓
Unauthorized account access
```

Protection:

```text
Strong Password
      +
MFA
      +
Conditional Access
```

This reduces the likelihood and impact of unauthorized access.

### SOC relevance

SOC analysts monitor whether protective controls are being bypassed or abused.

---

# 4️⃣ DETECT

## Definition

**Detect** focuses on finding and analyzing possible cybersecurity attacks or compromises.

This Function is highly relevant to SOC operations.

Examples:

* SIEM monitoring
* Log analysis
* IDS/IPS
* EDR
* Threat intelligence
* Anomaly detection
* Security alerts

### Example

```text
Failed Login
      ↓
Multiple Attempts
      ↓
Unusual Source IP
      ↓
SIEM Alert
      ↓
SOC Investigation
```

### SOC analyst activities

```text
Monitor
   ↓
Analyze
   ↓
Correlate
   ↓
Validate
   ↓
Escalate
```

---

# 5️⃣ RESPOND

## Definition

**Respond** focuses on taking action after a cybersecurity incident has been detected.

Typical activities include:

* Incident management
* Incident analysis
* Incident reporting
* Response planning
* Containment
* Mitigation
* Communication

### Example

Detected:

```text
Compromised Endpoint
        ↓
SOC Investigation
        ↓
Confirm Incident
        ↓
Isolate Endpoint
        ↓
Block Malicious IP
        ↓
Reset Credentials
```

### SOC relevance

This is directly related to incident response.

---

# 6️⃣ RECOVER

## Definition

**Recover** focuses on restoring affected systems and operations after a cybersecurity incident.

Activities include:

* Recovery planning
* System restoration
* Backup restoration
* Recovery communication
* Lessons learned
* Improvements

### Example

Ransomware:

```text
Ransomware Attack
       ↓
Containment
       ↓
Malware Removal
       ↓
Restore From Backup
       ↓
Validate Systems
       ↓
Return To Normal Operations
```

---

# 🔄 Complete NIST CSF Example

Imagine a company has a web application.

### Govern

Company establishes:

> Customer data must be protected.

↓

### Identify

Security team identifies:

* Web server
* Database
* Customer information
* API
* Cloud infrastructure

↓

### Protect

Controls implemented:

* MFA
* Encryption
* Access control
* Secure configuration
* Network segmentation

↓

### Detect

SOC detects:

```text
Suspicious API requests
       ↓
WAF Alert
       ↓
SIEM Correlation
```

↓

### Respond

SOC:

* Investigates
* Blocks malicious traffic
* Contains affected systems
* Escalates incident

↓

### Recover

Security team:

* Restores affected services
* Validates systems
* Reviews root cause
* Improves controls

---

# 🧩 CSF Categories

Each Function contains **Categories**.

Categories provide more specific groups of cybersecurity outcomes.

Conceptually:

```text
GOVERN
├── Organizational Context
├── Risk Management Strategy
├── Roles, Responsibilities & Authorities
└── Cybersecurity Supply Chain Risk Management

IDENTIFY
├── Asset Management
├── Risk Assessment
└── Improvement

PROTECT
├── Identity Management
├── Authentication & Access Control
├── Awareness & Training
└── Data Security

DETECT
├── Continuous Monitoring
└── Adverse Event Analysis

RESPOND
├── Incident Management
├── Incident Analysis
├── Incident Response Reporting
└── Incident Response Communication

RECOVER
├── Incident Recovery Plan Execution
├── Incident Recovery Communication
└── Incident Recovery Improvements
```

The exact CSF 2.0 Core should be consulted when implementing or mapping controls because the Framework is structured around specific outcomes and references.

---

# 👤 Organizational Profiles

A **CSF Organizational Profile** describes an organization's cybersecurity posture using CSF outcomes.

There are two important concepts:

### Current Profile

Describes:

> Where are we now?

### Target Profile

Describes:

> Where do we want to be?

### Example

```text
CURRENT PROFILE
Weak MFA
Limited logging
Incomplete asset inventory

        ↓
       GAP
        ↓

TARGET PROFILE
MFA everywhere
Centralized logging
Complete asset inventory
```

The organization can then create a plan to close the gap.

---

# 📊 Current vs Target Profile

```text
Current State
      ↓
Identify Gaps
      ↓
Prioritize Improvements
      ↓
Implement Controls
      ↓
Target State
```

This is extremely useful for cybersecurity maturity improvement.

---

# 📈 CSF Tiers

CSF Tiers characterize how an organization views and manages cybersecurity risk.

The four Tiers are:

```text
Tier 1 → Partial

Tier 2 → Risk Informed

Tier 3 → Repeatable

Tier 4 → Adaptive
```

---

# 🟢 Tier 1 — Partial

Characteristics:

* Limited awareness
* Ad hoc security practices
* Inconsistent risk management
* Limited organizational processes

Example:

> Security controls are implemented only when problems occur.

---

# 🟡 Tier 2 — Risk Informed

The organization understands cybersecurity risks but risk management may not be organization-wide or consistently applied.

Example:

> Management understands cyber risk, but security practices vary between departments.

---

# 🟠 Tier 3 — Repeatable

The organization has formalized and repeatable cybersecurity practices.

Characteristics:

* Formal policies
* Consistent processes
* Regular risk management
* Organization-wide security practices

Example:

```text
Alert
 ↓
Investigation Process
 ↓
Incident Classification
 ↓
Escalation
 ↓
Documentation
```

The same process is consistently followed.

---

# 🔴 Tier 4 — Adaptive

The organization continuously adapts cybersecurity practices based on:

* Threat intelligence
* Lessons learned
* Changing technologies
* Emerging threats
* Continuous improvement

Example:

```text
New Threat
    ↓
Threat Intelligence
    ↓
Detection Improvement
    ↓
New Security Control
    ↓
Monitoring
    ↓
Continuous Improvement
```

---

# 🔥 NIST CSF and SOC

For a SOC Analyst, the most relevant Functions are:

### DETECT

You monitor:

* SIEM
* EDR
* IDS
* Firewall
* Authentication logs
* Endpoint logs
* Network traffic

### RESPOND

You:

* Investigate
* Contain
* Escalate
* Document

### RECOVER

You support:

* Restoration
* Validation
* Post-incident improvement

But a SOC does not operate only within Detect/Respond. Asset context, access controls, governance, risk, and recovery requirements affect how SOC alerts are prioritized and handled.

---

# 🖥️ Practical SOC Example

## Scenario

An employee account shows:

```text
50 failed logins
       ↓
Successful login
       ↓
Unusual country
       ↓
PowerShell execution
       ↓
Suspicious outbound connection
```

### NIST mapping

**Identify**

Understand:

* User
* Device
* Application
* Criticality

↓

**Protect**

Check:

* MFA
* Access controls
* Endpoint protection

↓

**Detect**

SIEM detects:

* Failed logins
* Successful login
* PowerShell
* Network activity

↓

**Respond**

SOC:

* Investigates
* Disables account if required
* Isolates endpoint
* Blocks malicious infrastructure

↓

**Recover**

* Restore affected systems
* Reset credentials
* Validate environment
* Improve detections

---

# 🔗 NIST CSF vs NIST SP 800-53

These are often confused.

### NIST CSF

Focuses on:

> **What cybersecurity outcomes should the organization achieve?**

### NIST SP 800-53

Provides:

> **A catalog of security and privacy controls that can be used to achieve security objectives.**

Simple:

```text
NIST CSF
    ↓
Cybersecurity Outcomes
    ↓
What should we achieve?

NIST SP 800-53
    ↓
Security & Privacy Controls
    ↓
What controls can help us achieve it?
```

---

# 🔗 NIST CSF vs NIST SP 800-61

### NIST CSF

Broad cybersecurity risk-management framework.

### NIST SP 800-61

Focused specifically on **incident response**.

```text
NIST CSF
   ↓
Overall Cybersecurity Risk Management

NIST SP 800-61
   ↓
Incident Response
```

---

# 🔗 NIST CSF vs ISO 27001

| NIST CSF                                   | ISO/IEC 27001                                     |
| ------------------------------------------ | ------------------------------------------------- |
| Cybersecurity risk-management framework    | ISMS standard                                     |
| Flexible cybersecurity outcomes            | Requirements for an ISMS                          |
| Not a certification standard               | Certification is possible                         |
| Functions, Categories, Subcategories       | ISMS requirements and controls                    |
| Strong cybersecurity risk-management focus | Organization-wide information-security management |

---

# 🧠 Important Interview Questions

## Q1. What is NIST CSF?

NIST CSF is a cybersecurity risk-management framework that helps organizations understand, assess, prioritize, and communicate cybersecurity risks.

---

## Q2. What are the six Functions of NIST CSF 2.0?

```text
Govern
Identify
Protect
Detect
Respond
Recover
```

---

## Q3. Which Function was added in CSF 2.0?

**Govern**

It emphasizes cybersecurity risk governance, organizational context, risk strategy, roles and responsibilities, and supply-chain risk management.

---

## Q4. Is NIST CSF a law?

**No.**

It is a cybersecurity framework/guidance resource.

---

## Q5. Is NIST CSF mandatory for every organization?

**No.**

CSF is designed as flexible guidance and can be used by organizations across sectors and sizes.

---

## Q6. What is a CSF Profile?

A representation of an organization's cybersecurity posture using CSF outcomes.

Profiles can represent:

* Current state
* Target state

---

## Q7. What are CSF Tiers?

CSF Tiers characterize the organization's approach to cybersecurity risk governance and management:

```text
Tier 1 → Partial
Tier 2 → Risk Informed
Tier 3 → Repeatable
Tier 4 → Adaptive
```

---

## Q8. Which NIST CSF Function is most relevant to a SOC?

**Detect and Respond** are particularly relevant, although SOC operations can support and depend on activities across all six Functions.

---

# 📝 Quick Revision

```text
NIST
 ↓
Cybersecurity Risk Management
 ↓
CSF 2.0
 ↓
6 Functions
 ↓
Govern
Identify
Protect
Detect
Respond
Recover
```

### Remember:

```text
G → Governance
I → Know your environment
P → Protect it
D → Detect attacks
R → Respond to incidents
R → Recover operations
```

---

# 🎯 One-Line Memory Trick

> **Govern the risk → Identify the assets → Protect the environment → Detect threats → Respond to incidents → Recover operations.**

---

# 📚 Official References

* NIST Cybersecurity Framework: https://www.nist.gov/cyberframework
* NIST CSF 2.0: https://www.nist.gov/publications/nist-cybersecurity-framework-csf-20
* NIST CSF 2.0 Publication: https://doi.org/10.6028/NIST.CSWP.29

---

# ✅ Key Takeaways

* NIST CSF is a **cybersecurity risk-management framework**.
* Current major version is **CSF 2.0**.
* CSF 2.0 was published on **February 26, 2024**.
* CSF 2.0 has **six Functions**.
* **Govern** is the new Function introduced with CSF 2.0.
* CSF contains **Functions → Categories → Subcategories**.
* Organizations can use **Current and Target Profiles**.
* CSF Tiers range from **Partial → Risk Informed → Repeatable → Adaptive**.
* NIST CSF is **not a law**.
* NIST CSF is **not the same thing as NIST SP 800-53**.
* NIST CSF is highly relevant to **SOC, incident response, risk management, and security operations**.
