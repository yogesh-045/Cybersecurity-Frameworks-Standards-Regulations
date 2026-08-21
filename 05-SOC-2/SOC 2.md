# 🛡️ SOC 2 — Service Organization Control 2

## 📌 Overview

**SOC 2** is an examination and reporting framework developed by the **AICPA (American Institute of Certified Public Accountants)** for evaluating controls at service organizations that are relevant to security and other trust services criteria.

### Simple Definition

> **SOC 2 evaluates whether a service organization's controls are suitably designed and, for certain report types, operating effectively against applicable Trust Services Criteria.**

SOC 2 is especially common among:

* SaaS companies
* Cloud providers
* Technology companies
* Managed service providers
* Data-processing companies
* Third-party service providers

---

# 🧠 What Does SOC Mean?

**SOC = System and Organization Controls**

In modern usage, SOC reports are used to communicate information about controls at service organizations.

Do not confuse:

```text
SOC 2
```

with:

```text
SOC Analyst
Security Operations Center
```

They are completely different concepts.

---

# 🎯 Why SOC 2 Exists

Companies increasingly give sensitive data to third-party service providers.

Example:

```text
Customer
   ↓
SaaS Application
   ↓
Cloud Infrastructure
   ↓
Customer Data
```

The customer wants to know:

> "Does this service provider have appropriate controls to protect my data and systems?"

SOC 2 provides an independent examination/report that can help answer that question.

---

# 🏢 Example

Suppose a company provides a cloud-based HR platform.

The platform handles:

* Employee information
* Payroll information
* Login credentials
* Business data

A customer may ask:

> "How do I know your organization has appropriate security controls?"

The service provider can provide a SOC 2 report describing the relevant controls and examination results.

---

# ⭐ Trust Services Criteria

SOC 2 is based on the **Trust Services Criteria (TSC)**.

There are five categories:

```text
1. Security
2. Availability
3. Processing Integrity
4. Confidentiality
5. Privacy
```

---

# 🟥 1. Security

Security is the **common criteria** that applies to every SOC 2 examination.

It focuses on protecting systems and information against:

* Unauthorized access
* Unauthorized disclosure
* Unauthorized modification
* Unauthorized destruction

Examples of controls:

* Access control
* Authentication
* Network security
* Vulnerability management
* Incident response
* Monitoring
* Change management

---

# 🟦 2. Availability

Availability focuses on whether systems are available for operation and use as committed or agreed.

Examples:

* Disaster recovery
* Backup
* Redundancy
* Capacity management
* Availability monitoring
* Business continuity

Example:

```text
Production Server
      ↓
Failure
      ↓
Redundant System
      ↓
Service Continues
```

---

# 🟩 3. Processing Integrity

Processing integrity focuses on whether system processing is:

* Complete
* Valid
* Accurate
* Timely
* Authorized

### Example

An online payment system receives:

```text
₹1,000
```

The system should not incorrectly process:

```text
₹10,000
```

Processing integrity controls help ensure transactions are processed correctly.

---

# 🟨 4. Confidentiality

Confidentiality focuses on protecting information designated as confidential.

Examples:

* Encryption
* Access control
* Data classification
* DLP
* Secure transmission

```text
Confidential Data
       ↓
Access Control
       +
Encryption
       ↓
Authorized Access
```

---

# 🟪 5. Privacy

Privacy focuses on the collection, use, retention, disclosure, and disposal of personal information in accordance with applicable privacy commitments and criteria.

Examples:

* Privacy policies
* Consent management
* Data retention
* Data deletion
* Access controls
* Privacy incident management

---

# 📊 Trust Services Criteria

| Criteria             | Main Focus                             |
| -------------------- | -------------------------------------- |
| Security             | Protection from unauthorized access    |
| Availability         | System availability                    |
| Processing Integrity | Accurate and complete processing       |
| Confidentiality      | Protection of confidential information |
| Privacy              | Handling of personal information       |

### Important

**Security is the common criterion.**

The other four may be included depending on the scope of the SOC 2 examination.

---

# 🔥 SOC 2 Type I vs Type II

This is one of the most important interview topics.

## SOC 2 Type I

Type I evaluates whether controls are:

> **Suitably designed and implemented at a specific point in time.**

Simple:

```text
Type I
   ↓
Point-in-Time
   ↓
Control Design
```

---

# SOC 2 Type II

Type II evaluates:

> **Whether controls were suitably designed and operated effectively over a specified period of time.**

Simple:

```text
Type II
   ↓
Period of Time
   ↓
Control Design
      +
Operating Effectiveness
```

---

# 🧠 Easy Difference

```text
TYPE I
"What controls exist and are they suitably designed?"

TYPE II
"Do those controls operate effectively over time?"
```

---

# 📊 Type I vs Type II

| Feature                           | Type I        | Type II        |
| --------------------------------- | ------------- | -------------- |
| Evaluation                        | Point in time | Period of time |
| Control design                    | Yes           | Yes            |
| Operating effectiveness over time | No            | Yes            |
| Evidence                          | Point-in-time | Period-based   |
| Assurance depth                   | Lower         | Greater        |

---

# 🔍 What Does "Operating Effectiveness" Mean?

A control may exist on paper but fail in practice.

Example:

### Policy

> "All privileged accounts must use MFA."

Policy exists.

But investigation shows:

```text
10 Privileged Accounts
       ↓
8 use MFA
2 do not
```

The control may not be operating effectively.

This is why Type II examinations are important.

---

# 🧩 SOC 2 Controls

SOC 2 does not prescribe one universal checklist of technical controls for every company.

Controls are designed according to:

* Organization
* Systems
* Risks
* Services
* Commitments
* Trust Services Criteria

Examples:

### Access Management

```text
Employee
   ↓
Identity
   ↓
Authentication
   ↓
Authorization
   ↓
Resource
```

---

### Change Management

```text
Code Change
    ↓
Review
    ↓
Approval
    ↓
Testing
    ↓
Deployment
    ↓
Monitoring
```

---

### Vulnerability Management

```text
Scan
 ↓
Identify
 ↓
Risk Assess
 ↓
Remediate
 ↓
Verify
```

---

### Incident Response

```text
Detection
 ↓
Triage
 ↓
Investigation
 ↓
Containment
 ↓
Eradication
 ↓
Recovery
 ↓
Lessons Learned
```

---

# 📜 SOC 2 Report

A SOC 2 report generally describes things such as:

* Service organization
* System being examined
* Applicable Trust Services Criteria
* Management's description of the system
* Control objectives / controls
* Auditor's procedures and conclusions
* Tests of controls where applicable
* Results / exceptions

---

# 👨‍💼 Auditor's Role

An independent CPA firm performs the SOC examination.

The auditor evaluates relevant controls according to the applicable examination criteria.

### Basic Process

```text
Service Organization
        ↓
Defines System
        ↓
Defines Controls
        ↓
Auditor Examination
        ↓
Evidence / Testing
        ↓
SOC 2 Report
```

---

# 🧪 Evidence

Auditors may examine evidence such as:

* Access reviews
* User provisioning records
* Security logs
* Change tickets
* Vulnerability reports
* Incident records
* Backup testing
* Policies
* Configuration evidence
* Monitoring records

---

# 🔐 SOC 2 and SIEM

SOC 2 can be highly relevant to security monitoring.

Example:

```text
Firewall
   +
Cloud Logs
   +
Endpoint Logs
   +
Authentication Logs
   ↓
SIEM
   ↓
Monitoring
   ↓
Alerts
   ↓
Investigation
```

The existence and operation of such controls may be relevant to the organization's SOC 2 scope.

---

# 🧑‍💻 SOC Analyst Relevance

For a SOC Analyst, important SOC 2 areas include:

* Access control
* Authentication
* Logging
* Monitoring
* Incident response
* Vulnerability management
* Change management
* Endpoint security
* Network security
* Backup
* Security policies

---

# 🚨 Example SOC 2 Incident

Suppose an employee account is compromised.

### Detection

```text
Impossible Travel
      ↓
SIEM Alert
```

### Investigation

SOC checks:

* Login history
* Source IP
* Device
* MFA events
* User activity
* Data access
* Cloud activity

### Response

```text
Compromised Account
       ↓
Disable Session
       ↓
Reset Credentials
       ↓
Investigate
       ↓
Contain
       ↓
Document
```

This operational evidence can become relevant to security-control testing and assurance activities.

---

# 🔗 SOC 2 vs ISO 27001

These are often confused.

| SOC 2                                     | ISO 27001                                     |
| ----------------------------------------- | --------------------------------------------- |
| Examination/reporting framework           | International standard                        |
| Based on Trust Services Criteria          | Based on ISMS requirements                    |
| Independent examination produces a report | Certification audit can produce certification |
| Common in SaaS/cloud companies            | Broad organizational use                      |
| Focuses on controls relevant to TSC       | Focuses on ISMS                               |
| Type I / Type II reports                  | Certification / surveillance model            |

---

# 🔗 SOC 2 vs PCI DSS

| SOC 2                                 | PCI DSS                       |
| ------------------------------------- | ----------------------------- |
| Service-organization controls         | Payment-card security         |
| Trust Services Criteria               | 12 high-level requirements    |
| Broad technology/service environments | Payment account data          |
| Type I / Type II                      | Compliance validation methods |
| Customer assurance                    | Card-data security            |

---

# 🔗 SOC 2 vs HIPAA

| SOC 2                         | HIPAA                                                   |
| ----------------------------- | ------------------------------------------------------- |
| Assurance/reporting framework | U.S. federal law                                        |
| Trust Services Criteria       | Privacy/Security/Breach requirements                    |
| Broad service organizations   | Healthcare-related covered entities/business associates |
| Independent examination       | Regulatory/legal compliance                             |
| Not healthcare-specific       | Healthcare information focus                            |

---

# 🔗 SOC 2 vs NIST CSF

| SOC 2                    | NIST CSF                     |
| ------------------------ | ---------------------------- |
| Examination/reporting    | Cybersecurity framework      |
| Trust Services Criteria  | Cybersecurity risk outcomes  |
| Evidence of controls     | Risk-management guidance     |
| Independent examination  | No certification requirement |
| Often customer assurance | Broad organizational use     |

---

# 🧠 SOC 2 and GRC

SOC 2 is strongly connected with **GRC**.

```text
GRC
│
├── Governance
│
├── Risk
│
└── Compliance
       ↓
     SOC 2
       ↓
Policies
Controls
Evidence
Testing
Audit
```

---

# 📋 Control Example

Suppose the company has:

> "Quarterly review of privileged accounts."

### Control

```text
Privileged Accounts
        ↓
Quarterly Review
        ↓
Manager Approval
        ↓
Remove Unnecessary Access
```

### Evidence

Auditor may review:

* Account list
* Review date
* Reviewer
* Approval
* Removed accounts
* Tickets

---

# ⚠️ Important: SOC 2 Is Not a Certification

A common misconception is:

> "Our company is SOC 2 certified."

This terminology is generally inaccurate.

SOC 2 results in an **examination report**, not an ISO-style certification.

Better terminology:

> "The company completed a SOC 2 examination and received a SOC 2 report."

---

# ⚠️ SOC 2 Does Not Mean Perfect Security

Another misconception:

> "SOC 2 means the company cannot be hacked."

False.

SOC 2 provides assurance about controls within the defined examination scope.

It does not guarantee:

* Zero vulnerabilities
* Zero incidents
* Zero breaches
* Perfect security

---

# 🎯 SOC 2 Interview Questions

## Q1. What is SOC 2?

SOC 2 is an examination and reporting framework for evaluating controls at service organizations against applicable Trust Services Criteria.

---

## Q2. Who developed SOC 2?

SOC 2 is developed by the **AICPA**.

---

## Q3. What are the five Trust Services Criteria?

```text
Security
Availability
Processing Integrity
Confidentiality
Privacy
```

---

## Q4. Which SOC 2 criterion is common to every examination?

**Security.**

---

## Q5. What is SOC 2 Type I?

It evaluates the suitability of control design and implementation at a specified point in time.

---

## Q6. What is SOC 2 Type II?

It evaluates control design and implementation and tests operating effectiveness over a specified period.

---

## Q7. What is the biggest difference between Type I and Type II?

```text
Type I
→ Point in time

Type II
→ Period of time + operating effectiveness
```

---

## Q8. Is SOC 2 a cybersecurity framework?

Not in the same sense as NIST CSF.

It is an examination/reporting framework based on Trust Services Criteria.

---

## Q9. Is SOC 2 certification?

No.

SOC 2 results in an examination report rather than an ISO-style certification.

---

## Q10. Why is SOC 2 important for SaaS companies?

It provides customers and other stakeholders with independent information about relevant controls at the service organization.

---

# 📝 Quick Revision

```text
SOC 2
 ↓
AICPA
 ↓
Trust Services Criteria
 ↓
Controls
 ↓
Independent Examination
 ↓
SOC 2 Report
```

### Five Criteria

```text
Security
Availability
Processing Integrity
Confidentiality
Privacy
```

### Reports

```text
Type I
 ↓
Point in Time
 ↓
Control Design

Type II
 ↓
Period of Time
 ↓
Control Design
+
Operating Effectiveness
```

---

# ⭐ Key Takeaways

* **SOC 2** is an examination/reporting framework developed by the **AICPA**.
* It evaluates controls at service organizations.
* It is especially common in **SaaS, cloud, and technology companies**.
* SOC 2 is based on five **Trust Services Criteria**:

  * Security
  * Availability
  * Processing Integrity
  * Confidentiality
  * Privacy
* **Security** is the common criterion.
* **Type I** = point-in-time evaluation.
* **Type II** = evaluation over a period, including operating effectiveness testing.
* SOC 2 produces a **report**, not an ISO-style certification.
* SOC 2 does not guarantee that a company cannot be breached.
* SOC 2 is highly relevant to **GRC, compliance, auditing, cloud security, security operations, and vendor risk management**.

---

# 📚 Official References

* AICPA — SOC Services: https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services
* AICPA — Trust Services Criteria: https://www.aicpa-cima.com/resources/download/2017-trust-services-criteria
