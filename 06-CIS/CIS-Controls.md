# 🛡️ CIS Controls

## 📌 Overview

**CIS Controls = Center for Internet Security Controls**

CIS Controls are a prioritized set of cybersecurity safeguards designed to help organizations defend against common and significant cyber threats.

### Simple Definition

> **CIS Controls are prioritized cybersecurity safeguards that organizations can implement to reduce their exposure to common cyber attacks.**

CIS Controls are developed by the:

**Center for Internet Security (CIS)**

---

# 🎯 Why CIS Controls Exist

Organizations cannot always implement every security control immediately.

CIS Controls provide a prioritized approach:

```text
Identify Assets
      ↓
Understand Risks
      ↓
Prioritize Safeguards
      ↓
Implement Controls
      ↓
Monitor
      ↓
Improve
```

The focus is practical cybersecurity implementation.

---

# 🧠 CIS Controls vs Frameworks

CIS Controls should not be confused with:

* NIST CSF
* ISO 27001
* ISO 27002
* PCI DSS
* HIPAA

They serve different purposes.

| Standard / Framework | Main Purpose                             |
| -------------------- | ---------------------------------------- |
| NIST CSF             | Cybersecurity risk-management framework  |
| ISO 27001            | ISMS requirements                        |
| ISO 27002            | Security-control guidance                |
| PCI DSS              | Payment-card security requirements       |
| HIPAA                | U.S. healthcare privacy/security law     |
| SOC 2                | Service-organization control examination |
| CIS Controls         | Prioritized cybersecurity safeguards     |

---

# 🔢 CIS Controls Version

The current major version is:

**CIS Controls v8.1**

It contains:

> **18 CIS Controls**

---

# 📋 The 18 CIS Controls

```text
01 → Inventory and Control of Enterprise Assets
02 → Inventory and Control of Software Assets
03 → Data Protection
04 → Secure Configuration of Enterprise Assets and Software
05 → Account Management
06 → Access Control Management
07 → Continuous Vulnerability Management
08 → Audit Log Management
09 → Email and Web Browser Protections
10 → Malware Defenses
11 → Data Recovery
12 → Network Infrastructure Management
13 → Network Monitoring and Defense
14 → Security Awareness and Skills Training
15 → Service Provider Management
16 → Application Software Security
17 → Incident Response Management
18 → Penetration Testing
```

---

# 🟦 Control 1 — Inventory and Control of Enterprise Assets

Organizations should know what devices and assets exist in their environment.

Examples:

* Laptops
* Servers
* Workstations
* Network devices
* Cloud resources
* Mobile devices

### Why?

You cannot effectively secure an asset you don't know exists.

```text
Unknown Device
     ↓
No Monitoring
     ↓
Potential Attack Surface
```

### SOC Relevance

Asset inventory helps analysts determine:

* What system generated an alert?
* Who owns it?
* Is it critical?
* Is it authorized?

---

# 🟩 Control 2 — Inventory and Control of Software Assets

Organizations should know what software is installed or running.

Examples:

* Operating systems
* Applications
* Libraries
* Browser extensions
* Packages

### Example

```text
Asset
 ↓
Installed Software
 ↓
Version
 ↓
Known Vulnerabilities
 ↓
Risk
```

Unauthorized software can increase attack surface.

---

# 🟨 Control 3 — Data Protection

Organizations should identify and protect sensitive data.

Examples:

* Classification
* Encryption
* Access control
* Data retention
* Data disposal
* DLP

### Example

```text
Sensitive Data
      ↓
Classification
      ↓
Access Control
      ↓
Encryption
      ↓
Monitoring
```

---

# 🟧 Control 4 — Secure Configuration

Systems should use secure configurations.

Examples:

* Disable unnecessary services
* Remove default accounts
* Disable insecure protocols
* Apply hardening
* Use secure configuration baselines

### Example

```text
Default Server
      ↓
Hardening
      ↓
Secure Baseline
      ↓
Monitoring
```

---

# 🟥 Control 5 — Account Management

Organizations should manage accounts throughout their lifecycle.

```text
Employee Joins
      ↓
Account Created
      ↓
Access Assigned
      ↓
Role Change
      ↓
Access Updated
      ↓
Employee Leaves
      ↓
Account Disabled
```

Important account types:

* User accounts
* Privileged accounts
* Service accounts
* Administrator accounts

---

# 🔐 Control 6 — Access Control Management

Access should be restricted based on business requirements.

Important concepts:

* Least privilege
* Role-based access
* Privileged access
* MFA
* Access reviews

### Example

```text
User
 ↓
Role
 ↓
Required Permissions
 ↓
Minimum Necessary Access
```

---

# 🔥 Control 7 — Continuous Vulnerability Management

Organizations should continuously identify and manage vulnerabilities.

### Process

```text
Discover
   ↓
Scan
   ↓
Identify Vulnerabilities
   ↓
Risk Prioritization
   ↓
Remediation
   ↓
Verification
```

### Important

Do not simply patch vulnerabilities based on CVSS alone.

Consider:

* Asset criticality
* Exploit availability
* Internet exposure
* Business impact
* Existing controls

---

# 📜 Control 8 — Audit Log Management

This is one of the most important controls for a SOC Analyst.

Organizations should collect, manage, and review relevant audit logs.

Examples:

* Authentication logs
* Windows Event Logs
* Linux logs
* Firewall logs
* DNS logs
* VPN logs
* Cloud logs
* Application logs

### SIEM

```text
Windows
   +
Linux
   +
Firewall
   +
Cloud
   +
Endpoint
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

# 🌐 Control 9 — Email and Web Browser Protections

Email and web browsers are common attack vectors.

Threats include:

* Phishing
* Malicious attachments
* Malicious URLs
* Drive-by downloads
* Credential theft

Controls may include:

* Email filtering
* URL filtering
* Browser security
* Attachment scanning
* Anti-phishing controls

---

# 🦠 Control 10 — Malware Defenses

Organizations should protect systems from malware.

Examples:

* Antivirus
* EDR
* Anti-malware
* Application control
* Behavioral detection

### SOC Flow

```text
Malware
   ↓
Endpoint
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

# 💾 Control 11 — Data Recovery

Organizations should be able to recover data and systems after incidents.

Examples:

* Backups
* Recovery procedures
* Backup testing
* Offline/isolated backups
* Recovery validation

### Important

A backup is not enough.

You need to verify that it can actually be restored.

```text
Backup
  ↓
Restore Test
  ↓
Successful?
  ↓
Recovery Confidence
```

---

# 🌐 Control 12 — Network Infrastructure Management

Organizations should securely manage network infrastructure.

Examples:

* Routers
* Switches
* Firewalls
* VPN
* Wireless infrastructure
* Network configurations

Security practices:

* Secure configuration
* Administrative access control
* Firmware updates
* Network segmentation
* Configuration monitoring

---

# 🔎 Control 13 — Network Monitoring and Defense

Organizations should monitor network activity to identify suspicious behavior.

Examples:

* IDS
* IPS
* Network detection
* Traffic analysis
* DNS monitoring
* Firewall monitoring

### SOC Example

```text
Network Traffic
      ↓
NDR / IDS
      ↓
Suspicious Activity
      ↓
SIEM
      ↓
SOC Investigation
```

---

# 🎓 Control 14 — Security Awareness and Skills Training

Employees should understand cybersecurity risks.

Training topics:

* Phishing
* Password security
* MFA
* Social engineering
* Data handling
* Incident reporting

### Example

```text
Employee
   ↓
Security Awareness
   ↓
Recognize Phishing
   ↓
Report Suspicious Email
   ↓
SOC Investigation
```

---

# 🤝 Control 15 — Service Provider Management

Organizations often depend on third parties.

Examples:

* Cloud providers
* SaaS providers
* MSPs
* Security vendors
* Payment providers

Organizations should understand the security risks associated with service providers.

### Example

```text
Organization
     ↓
Cloud Provider
     ↓
Customer Data
```

Third-party risk should be assessed and managed.

---

# 💻 Control 16 — Application Software Security

Applications should be developed and maintained securely.

Important practices:

* Secure SDLC
* Code review
* Dependency management
* Vulnerability testing
* Security testing
* Input validation
* Authentication
* Authorization

### Example

```text
Requirements
     ↓
Secure Design
     ↓
Development
     ↓
Security Testing
     ↓
Deployment
     ↓
Monitoring
```

---

# 🚨 Control 17 — Incident Response Management

Organizations need a defined incident-response capability.

### Basic Process

```text
Preparation
    ↓
Detection
    ↓
Analysis
    ↓
Containment
    ↓
Eradication
    ↓
Recovery
    ↓
Lessons Learned
```

### SOC Connection

SOC Analysts commonly participate in:

* Alert triage
* Investigation
* Escalation
* Containment
* Evidence collection
* Documentation

---

# 🧪 Control 18 — Penetration Testing

Organizations should perform penetration testing according to their risk and applicable requirements.

Purpose:

> Identify weaknesses by simulating realistic attack techniques in an authorized manner.

Examples:

* Web application testing
* Network penetration testing
* External testing
* Internal testing
* Segmentation testing
* Cloud/security testing

### Basic Flow

```text
Scope
 ↓
Reconnaissance
 ↓
Testing
 ↓
Exploitation
 ↓
Evidence
 ↓
Report
 ↓
Remediation
 ↓
Retesting
```

---

# 🧩 Implementation Groups

CIS Controls v8.1 organizes implementation priorities through **Implementation Groups (IGs)**.

There are:

```text
IG1
IG2
IG3
```

---

# 🟢 IG1

**IG1 = Essential Cyber Hygiene**

This represents foundational safeguards for organizations with limited resources and basic security needs.

Focus:

* Asset inventory
* Software inventory
* Basic security configuration
* Account management
* Vulnerability management
* Logging
* Malware defense
* Data recovery

---

# 🟡 IG2

IG2 builds on IG1.

It is intended for organizations with more complex environments and greater security requirements.

Focus expands into:

* More mature security processes
* More extensive monitoring
* Application security
* Third-party management
* More advanced controls

---

# 🔴 IG3

IG3 represents the highest level of implementation.

It is intended for organizations facing sophisticated threats and/or highly sensitive environments.

Examples:

* Critical infrastructure
* High-value targets
* Organizations facing advanced threat actors

IG3 builds upon the safeguards addressed in IG1 and IG2.

---

# 📊 Implementation Groups

| Group | Meaning                 | Focus                 |
| ----- | ----------------------- | --------------------- |
| IG1   | Essential Cyber Hygiene | Basic protection      |
| IG2   | Increased maturity      | Broader controls      |
| IG3   | Advanced protection     | Sophisticated threats |

### Remember

```text
IG1 → Basic
IG2 → Advanced
IG3 → Sophisticated
```

---

# 🔗 CIS Controls and NIST CSF

These frameworks can complement each other.

### Example

NIST CSF:

```text
Identify
Protect
Detect
Respond
Recover
Govern
```

CIS Controls:

```text
Asset Inventory
Access Control
Logging
Vulnerability Management
Incident Response
Recovery
```

They are not identical.

A useful way to think about them:

```text
NIST CSF
"What cybersecurity outcomes should we manage?"

CIS Controls
"What prioritized safeguards can we implement?"
```

---

# 🔗 CIS Controls and ISO 27001

| CIS Controls                   | ISO 27001                    |
| ------------------------------ | ---------------------------- |
| Practical safeguards           | ISMS requirements            |
| Prioritized security actions   | Management system            |
| 18 Controls                    | ISMS + control framework     |
| Technical/operational emphasis | Governance + risk management |
| Implementation-focused         | Certification-oriented       |

---

# 🔗 CIS Controls and ISO 27002

| CIS Controls               | ISO 27002                     |
| -------------------------- | ----------------------------- |
| 18 prioritized controls    | 93 controls                   |
| Practical safeguards       | Control guidance              |
| Prioritized implementation | Broad control guidance        |
| Cyber defense focus        | Information-security controls |

---

# 🔗 CIS Controls and PCI DSS

| CIS Controls           | PCI DSS                 |
| ---------------------- | ----------------------- |
| General cybersecurity  | Payment-card security   |
| 18 controls            | 12 requirements         |
| Prioritized safeguards | Compliance requirements |
| Broad organizations    | Payment environments    |

---

# 🔗 CIS Controls and SOC 2

| CIS Controls             | SOC 2                             |
| ------------------------ | --------------------------------- |
| Cybersecurity safeguards | Control examination               |
| 18 controls              | Trust Services Criteria           |
| Implementation-focused   | Assurance-focused                 |
| Technical + operational  | Governance + operational controls |

---

# 🧑‍💻 SOC Analyst Mapping

Several CIS Controls directly map to daily SOC work.

## Asset Management

```text
CIS 1
CIS 2
```

Know:

* What assets exist?
* What software runs on them?
* Who owns them?

---

## Vulnerability Management

```text
CIS 7
```

SOC can use vulnerability information to prioritize detections and investigations.

---

## Logging

```text
CIS 8
```

Extremely important.

SOC needs visibility.

```text
Logs
 ↓
SIEM
 ↓
Detection
 ↓
Investigation
```

---

## Network Defense

```text
CIS 12
CIS 13
```

Examples:

* Firewall
* IDS/IPS
* NDR
* Network segmentation
* Traffic analysis

---

## Incident Response

```text
CIS 17
```

Directly relevant to SOC operations.

---

# 🔥 Practical SOC Scenario

Suppose an attacker compromises a workstation.

### Detection

EDR detects suspicious PowerShell execution.

```text
PowerShell
    ↓
EDR
    ↓
Detection
    ↓
SIEM
```

### Investigation

SOC checks:

* User
* Host
* Process tree
* Parent process
* Command line
* Network connections
* File hashes
* Authentication activity

### CIS Controls Involved

```text
CIS 1
→ Asset identification

CIS 2
→ Software identification

CIS 5
→ Account management

CIS 8
→ Logging

CIS 10
→ Malware defense

CIS 13
→ Network monitoring

CIS 17
→ Incident response
```

---

# 🧠 Important Concepts

## Attack Surface

> The collection of assets, interfaces, services, applications, and other exposure points that an attacker could potentially target.

CIS Controls reduce attack surface through:

* Asset inventory
* Software inventory
* Secure configuration
* Vulnerability management
* Access control

---

# 🔐 Least Privilege

Users should receive only the permissions required to perform their tasks.

```text
User
 ↓
Role
 ↓
Required Permissions
 ↓
Minimum Access
```

---

# 📜 Security Baseline

A **security baseline** is a defined set of secure configuration settings used as a standard for systems.

Example:

```text
Windows Server
   ↓
Security Baseline
   ↓
Disable Unnecessary Services
   ↓
Configure Logging
   ↓
Secure Authentication
```

---

# 🔎 Continuous Monitoring

Security should not be a one-time activity.

```text
Configure
   ↓
Monitor
   ↓
Detect
   ↓
Investigate
   ↓
Remediate
   ↓
Verify
   ↓
Monitor Again
```

---

# ⚠️ Common Misconceptions

## ❌ "CIS Controls is a certification."

False.

CIS Controls are cybersecurity safeguards, not an ISO-style certification standard.

---

## ❌ "You only need CIS Controls if you're a large company."

False.

IG1 specifically provides a foundation for organizations with limited resources.

---

## ❌ "Implementing CIS Controls guarantees security."

False.

Controls reduce risk; they cannot guarantee zero attacks.

---

## ❌ "CIS Controls and NIST CSF are the same."

False.

They can complement each other but serve different purposes.

---

# 🎯 Interview Questions

## Q1. What are CIS Controls?

CIS Controls are a prioritized set of cybersecurity safeguards developed by the Center for Internet Security to help organizations reduce cyber risk.

---

## Q2. How many CIS Controls are in v8.1?

**18 controls.**

---

## Q3. What is CIS Control 1?

**Inventory and Control of Enterprise Assets.**

---

## Q4. What is CIS Control 2?

**Inventory and Control of Software Assets.**

---

## Q5. Which CIS Control focuses on vulnerability management?

**Control 7 — Continuous Vulnerability Management.**

---

## Q6. Which CIS Control focuses on logging?

**Control 8 — Audit Log Management.**

---

## Q7. Which CIS Control is highly relevant to SOC Analysts?

Several, especially:

* Control 8 — Audit Log Management
* Control 10 — Malware Defenses
* Control 13 — Network Monitoring and Defense
* Control 17 — Incident Response Management

---

## Q8. What are the CIS Implementation Groups?

```text
IG1
IG2
IG3
```

They provide implementation priorities based on organizational needs and risk.

---

## Q9. What is IG1?

IG1 represents **Essential Cyber Hygiene** and foundational safeguards.

---

## Q10. What is the difference between CIS Controls and NIST CSF?

NIST CSF provides a broader cybersecurity risk-management structure, while CIS Controls provide prioritized safeguards that organizations can implement.

---

# 📝 Quick Revision

```text
CIS Controls
      ↓
Center for Internet Security
      ↓
18 Prioritized Controls
      ↓
Cyber Defense
```

### Most Important

```text
01 → Assets
02 → Software
03 → Data
04 → Configuration
05 → Accounts
06 → Access
07 → Vulnerabilities
08 → Logs
09 → Email/Web
10 → Malware
11 → Recovery
12 → Network Infrastructure
13 → Network Monitoring
14 → Awareness
15 → Service Providers
16 → Application Security
17 → Incident Response
18 → Penetration Testing
```

### Implementation Groups

```text
IG1 → Essential Cyber Hygiene
IG2 → Increased Security Maturity
IG3 → Advanced / Sophisticated Protection
```

---

# ⭐ Key Takeaways

* **CIS Controls** are prioritized cybersecurity safeguards.
* They are developed by the **Center for Internet Security**.
* The current major release is **CIS Controls v8.1**.
* v8.1 contains **18 Controls**.
* CIS Controls are implementation-oriented and highly practical.
* **Control 1** = Enterprise Asset Inventory.
* **Control 2** = Software Inventory.
* **Control 7** = Vulnerability Management.
* **Control 8** = Audit Log Management.
* **Control 10** = Malware Defenses.
* **Control 13** = Network Monitoring and Defense.
* **Control 17** = Incident Response.
* **Control 18** = Penetration Testing.
* Implementation Groups are **IG1, IG2, and IG3**.
* CIS Controls can complement NIST CSF, ISO 27001, ISO 27002, PCI DSS, and other security/compliance approaches.
* CIS Controls are **not a certification** and do not guarantee complete security.

---

# 📚 Official Reference

* CIS Controls: https://www.cisecurity.org/controls
