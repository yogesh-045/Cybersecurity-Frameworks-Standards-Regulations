# 🛡️ NIST SP 800-53 — Security and Privacy Controls

## 📌 Overview

**NIST SP 800-53** is a NIST publication that provides a catalog of **security and privacy controls** for information systems and organizations.

It helps organizations select and implement controls to protect:

* Information systems
* Organizational information
* Sensitive data
* Privacy
* Users
* Business operations

### Simple Definition

> **NIST SP 800-53 is a catalog of security and privacy controls used to manage and reduce organizational cybersecurity risk.**

---

# 🧠 What Does "Control" Mean?

A **security control** is a safeguard or countermeasure designed to:

* Prevent security incidents
* Detect malicious activity
* Reduce risk
* Protect information
* Respond to incidents
* Support recovery

### Example

Threat:

```text
Stolen Password
      ↓
Unauthorized Account Access
```

Controls:

```text
MFA
+
Strong Authentication
+
Access Control
+
Logging
```

These controls reduce the risk of unauthorized access.

---

# 🎯 Purpose of NIST SP 800-53

NIST SP 800-53 helps organizations:

* Identify appropriate security controls
* Protect information systems
* Protect organizational information
* Manage cybersecurity risks
* Protect privacy
* Support compliance
* Standardize security practices

It is especially relevant to organizations that require formal security-control programs.

---

# 🔗 NIST SP 800-53 and NIST CSF

These two are commonly confused.

## NIST CSF

Focuses on cybersecurity **outcomes and risk management**.

```text
What cybersecurity outcomes should we achieve?
```

## NIST SP 800-53

Provides a catalog of **controls** that can help achieve security and privacy objectives.

```text
What controls can we implement?
```

### Simple Relationship

```text
NIST CSF
    ↓
Cybersecurity Outcomes
    ↓
Security Objectives
    ↓
NIST SP 800-53
    ↓
Security & Privacy Controls
```

---

# 🧩 Control Families

NIST SP 800-53 organizes controls into **control families**.

Important families include:

| Family | Name                                      |
| ------ | ----------------------------------------- |
| AC     | Access Control                            |
| AT     | Awareness and Training                    |
| AU     | Audit and Accountability                  |
| CA     | Assessment, Authorization, and Monitoring |
| CM     | Configuration Management                  |
| CP     | Contingency Planning                      |
| IA     | Identification and Authentication         |
| IR     | Incident Response                         |
| MA     | Maintenance                               |
| MP     | Media Protection                          |
| PE     | Physical and Environmental Protection     |
| PL     | Planning                                  |
| PM     | Program Management                        |
| PS     | Personnel Security                        |
| PT     | PII Processing and Transparency           |
| RA     | Risk Assessment                           |
| SA     | System and Services Acquisition           |
| SC     | System and Communications Protection      |
| SI     | System and Information Integrity          |
| SR     | Supply Chain Risk Management              |

---

# 1️⃣ AC — Access Control

## Definition

Access Control controls who can access systems, applications, networks, and information.

### Examples

* Role-Based Access Control
* Least privilege
* Account restrictions
* Remote access controls
* Privileged access management

### Example

```text
Employee
   ↓
Normal User
   ↓
Limited Permissions
```

An administrator should not automatically give every employee administrative privileges.

### SOC Relevance

SOC analysts investigate:

* Unauthorized access
* Privilege abuse
* Suspicious logins
* Account misuse
* Privilege escalation

---

# 2️⃣ AT — Awareness and Training

Organizations need security-awareness and training programs.

Examples:

* Phishing awareness
* Password security
* Security policies
* Incident reporting
* Security training

### Example

```text
Employee receives phishing email
              ↓
Recognizes phishing
              ↓
Reports email
              ↓
SOC investigates
```

Human awareness can therefore contribute to security detection.

---

# 3️⃣ AU — Audit and Accountability

This family is highly relevant to SOC operations.

It deals with:

* Audit records
* Logging
* Monitoring
* Accountability
* Event analysis

### Example

```text
User Login
     ↓
Authentication Log
     ↓
SIEM
     ↓
Correlation
     ↓
Alert
```

### SOC Relevance

SOC analysts depend heavily on logs.

Common sources:

* Windows Event Logs
* Linux logs
* Firewall logs
* VPN logs
* Authentication logs
* EDR logs
* Application logs
* Cloud logs

---

# 4️⃣ CA — Assessment, Authorization, and Monitoring

This family deals with:

* Security assessments
* Control assessments
* Authorization
* Continuous monitoring

### Simple idea

```text
Implement Controls
       ↓
Assess Controls
       ↓
Identify Weaknesses
       ↓
Improve Controls
       ↓
Monitor Continuously
```

---

# 5️⃣ CM — Configuration Management

Focuses on managing system configurations securely.

Examples:

* Secure baseline
* Configuration changes
* Configuration monitoring
* Software inventory
* System hardening

### Example

```text
Server
  ↓
Secure Baseline
  ↓
Configuration Monitoring
  ↓
Unauthorized Change
  ↓
Alert
```

### SOC Relevance

Unexpected configuration changes can be indicators of compromise or policy violations.

---

# 6️⃣ CP — Contingency Planning

Focuses on preparing for disruptions and recovering systems.

Examples:

* Backup
* Disaster recovery
* Business continuity
* Alternate processing
* Recovery procedures

### Example

```text
Ransomware
    ↓
Systems Unavailable
    ↓
Contain Incident
    ↓
Restore From Backup
    ↓
Resume Operations
```

---

# 7️⃣ IA — Identification and Authentication

Focuses on identifying and authenticating users, devices, and other entities.

Examples:

* Username/password
* MFA
* Certificates
* Biometrics
* Device authentication

### Authentication vs Authorization

**Authentication:**

> Who are you?

**Authorization:**

> What are you allowed to access?

```text
User
 ↓
Authentication
 ↓
Identity Verified
 ↓
Authorization
 ↓
Permissions Granted
```

---

# 8️⃣ IR — Incident Response

This is one of the most important families for SOC Analysts.

It covers:

* Incident response planning
* Incident handling
* Incident monitoring
* Incident reporting
* Incident response assistance

### Example

```text
Alert
 ↓
Analysis
 ↓
Incident Confirmation
 ↓
Containment
 ↓
Eradication
 ↓
Recovery
 ↓
Lessons Learned
```

### SOC Relevance

SOC analysts are directly involved in:

* Alert triage
* Investigation
* Escalation
* Containment support
* Evidence collection
* Incident documentation

---

# 9️⃣ MA — Maintenance

Focuses on secure maintenance of information systems.

Examples:

* System maintenance
* Remote maintenance
* Maintenance personnel
* Maintenance tools

Security teams need to ensure maintenance does not introduce unnecessary risk.

---

# 🔟 MP — Media Protection

Focuses on protecting information stored on media.

Examples:

* Hard drives
* USB drives
* Backup media
* Removable storage

Controls can include:

* Media access restrictions
* Media sanitization
* Encryption
* Secure disposal

---

# 1️⃣1️⃣ PE — Physical and Environmental Protection

Cybersecurity is not only digital.

This family addresses physical security.

Examples:

* Data-center access
* Physical access controls
* Surveillance
* Environmental controls
* Visitor management

### Example

```text
Unauthorized Person
        ↓
Data Center
        ↓
Physical Access Control
        ↓
Access Denied
```

---

# 1️⃣2️⃣ PL — Planning

Focuses on security and privacy planning.

Examples:

* System security plans
* Privacy planning
* Rules of behavior
* Security architecture

---

# 1️⃣3️⃣ PM — Program Management

Focuses on organization-wide security and privacy programs.

Examples:

* Cybersecurity strategy
* Risk management
* Security policies
* Security resources
* Program oversight

---

# 1️⃣4️⃣ PS — Personnel Security

Focuses on security risks related to employees and other personnel.

Examples:

* Background screening
* Personnel termination
* Role changes
* Access removal

### Example

Employee leaves organization:

```text
Employee Resignation
       ↓
Disable Account
       ↓
Revoke Tokens
       ↓
Remove VPN Access
       ↓
Revoke Privileges
```

---

# 1️⃣5️⃣ PT — PII Processing and Transparency

Focuses on personally identifiable information and privacy.

Important concepts:

* PII handling
* Privacy requirements
* Data processing
* Transparency
* Privacy notices

---

# 1️⃣6️⃣ RA — Risk Assessment

Focuses on identifying and evaluating cybersecurity risks.

Basic process:

```text
Asset
 ↓
Threat
 ↓
Vulnerability
 ↓
Likelihood
 ↓
Impact
 ↓
Risk
```

### Example

```text
Critical Database
       +
Unpatched Vulnerability
       +
Known Exploit
       ↓
High Risk
```

---

# 1️⃣7️⃣ SA — System and Services Acquisition

Focuses on security requirements during acquisition and development of systems and services.

Examples:

* Vendor security
* Security requirements
* Software development
* Supply-chain security
* Third-party risk

---

# 1️⃣8️⃣ SC — System and Communications Protection

Focuses on protecting systems and communications.

Examples:

* Encryption
* Network segmentation
* Boundary protection
* Secure protocols
* Network architecture

### Example

```text
Internet
   ↓
Firewall
   ↓
DMZ
   ↓
Internal Network
   ↓
Critical Systems
```

---

# 1️⃣9️⃣ SI — System and Information Integrity

Focuses on identifying and correcting security weaknesses and maintaining system integrity.

Examples:

* Malware protection
* Vulnerability remediation
* Security alerts
* Software updates
* File integrity monitoring

### SOC Example

```text
Malicious File
     ↓
EDR Detection
     ↓
SIEM Alert
     ↓
SOC Investigation
```

---

# 2️⃣0️⃣ SR — Supply Chain Risk Management

Focuses on cybersecurity risks associated with suppliers and third parties.

Examples:

* Cloud providers
* Software vendors
* Hardware suppliers
* Managed security providers
* Third-party applications

### Example

```text
Organization
      ↓
Third-Party Vendor
      ↓
Software Dependency
      ↓
Supply-Chain Vulnerability
      ↓
Organizational Risk
```

Supply-chain security became increasingly important as organizations depend heavily on external software, cloud services, and vendors.

---

# 🧠 Security Control Types

Security controls can also be categorized by their purpose.

## Preventive Controls

Designed to prevent an incident.

Examples:

* Firewall
* MFA
* Access control
* Network segmentation

```text
Attack
 ↓
Firewall
 ↓
Blocked
```

---

## Detective Controls

Designed to detect suspicious activity.

Examples:

* SIEM
* IDS
* EDR
* Security monitoring

```text
Attack
 ↓
SIEM
 ↓
Alert
```

---

## Corrective Controls

Designed to correct or reduce the impact of an incident.

Examples:

* Malware removal
* System restoration
* Patching
* Account reset

```text
Incident
 ↓
Contain
 ↓
Fix
 ↓
Restore
```

---

# 🔐 Example: Protecting a Corporate Laptop

Suppose a company laptop contains sensitive information.

### Preventive Controls

* MFA
* Disk encryption
* Endpoint protection
* Least privilege

### Detective Controls

* EDR
* Windows Event Logs
* SIEM
* File integrity monitoring

### Corrective Controls

* Endpoint isolation
* Malware removal
* Credential reset
* System restoration

---

# 🔥 NIST SP 800-53 and SOC Operations

SOC analysts interact with multiple control families.

### Example

A suspicious login occurs.

**IA**

Authentication information is analyzed.

↓

**AC**

Access permissions are reviewed.

↓

**AU**

Authentication logs are investigated.

↓

**SI**

Suspicious system activity is analyzed.

↓

**IR**

Incident-response procedures are initiated.

↓

**CA**

Security controls may later be assessed.

This shows how security controls support SOC operations.

---

# 🧩 Control Baselines

NIST SP 800-53 can be used with **control baselines**.

A baseline is a defined starting set of controls selected according to factors such as:

* System type
* Risk
* Impact
* Organizational requirements

Different environments may require different levels of security controls.

### Simple Example

```text
Low-Impact System
       ↓
Lower Baseline

High-Impact System
       ↓
Stronger Baseline
```

The exact baseline selection should be based on the applicable NIST guidance and organizational risk requirements.

---

# 📊 NIST SP 800-53 vs NIST CSF

| NIST CSF                                | NIST SP 800-53                     |
| --------------------------------------- | ---------------------------------- |
| Cybersecurity risk-management framework | Security & privacy control catalog |
| High-level outcomes                     | Detailed controls                  |
| Helps communicate risk                  | Helps select/implement controls    |
| Functions & Categories                  | Control Families & Controls        |
| Broad organizational use                | Detailed control implementation    |

---

# 📊 NIST SP 800-53 vs ISO 27001

| NIST SP 800-53                      | ISO/IEC 27001                             |
| ----------------------------------- | ----------------------------------------- |
| Control catalog                     | ISMS standard                             |
| Security & privacy controls         | ISMS requirements                         |
| Detailed control families           | Management-system approach                |
| NIST publication                    | International standard                    |
| Strong control implementation focus | Risk + management + continual improvement |

---

# 🎯 SOC Analyst Interview Questions

## Q1. What is NIST SP 800-53?

NIST SP 800-53 is a catalog of security and privacy controls designed to help organizations protect information systems and manage security and privacy risks.

---

## Q2. What is a security control?

A security control is a safeguard or countermeasure designed to reduce security risk.

---

## Q3. Which NIST 800-53 family is related to logging?

**AU — Audit and Accountability**

---

## Q4. Which family deals with incident response?

**IR — Incident Response**

---

## Q5. Which family deals with authentication?

**IA — Identification and Authentication**

---

## Q6. Which family deals with access permissions?

**AC — Access Control**

---

## Q7. Which family deals with system integrity and vulnerabilities?

**SI — System and Information Integrity**

---

## Q8. Which family deals with network protection?

**SC — System and Communications Protection**

---

## Q9. Which family deals with risk assessment?

**RA — Risk Assessment**

---

## Q10. Which family deals with supply-chain risk?

**SR — Supply Chain Risk Management**

---

# 📝 Quick Revision

```text
NIST SP 800-53
       ↓
Security + Privacy Controls
       ↓
Control Families
       ↓
AC → Access Control
AT → Awareness & Training
AU → Audit & Accountability
CA → Assessment & Authorization
CM → Configuration Management
CP → Contingency Planning
IA → Identification & Authentication
IR → Incident Response
MA → Maintenance
MP → Media Protection
PE → Physical Protection
PL → Planning
PM → Program Management
PS → Personnel Security
PT → PII Processing & Transparency
RA → Risk Assessment
SA → System & Services Acquisition
SC → Communications Protection
SI → System & Information Integrity
SR → Supply Chain Risk Management
```

---

# 🧠 Easy Memory for SOC

For SOC Analyst preparation, remember these first:

```text
AU → Logs
IA → Authentication
AC → Access
SI → Integrity / Vulnerabilities
SC → Network / Communications
IR → Incidents
RA → Risk
CM → Configuration
SR → Supply Chain
```

---

# ⭐ Key Takeaways

* NIST SP 800-53 is a **security and privacy control catalog**.
* It is different from NIST CSF.
* NIST CSF focuses on **cybersecurity outcomes and risk management**.
* SP 800-53 provides **detailed security and privacy controls**.
* Controls are organized into **control families**.
* **AU** is highly relevant to logging and accountability.
* **IA** covers identification and authentication.
* **AC** covers access control.
* **IR** covers incident response.
* **SI** covers system and information integrity.
* **SC** covers system and communications protection.
* **RA** covers risk assessment.
* **SR** covers supply-chain risk management.
* SOC analysts interact with multiple control families during monitoring and incident response.

---

# 📚 Official Reference

NIST Special Publication 800-53:

https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final

NIST Computer Security Resource Center:

https://csrc.nist.gov/
