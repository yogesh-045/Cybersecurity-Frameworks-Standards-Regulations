# Cybersecurity-Frameworks-Standards-Regulations
# 🔐 Cybersecurity Frameworks, Standards & Regulations

A structured collection of cybersecurity frameworks, standards, regulations, governance models, security controls, and threat intelligence frameworks.

This repository is created for **cybersecurity learning, SOC Analyst preparation, security interviews, compliance awareness, and practical security operations**.

---

## 📚 What This Repository Covers

This repository explains the purpose, terminology, structure, use cases, and cybersecurity relevance of major frameworks, standards, regulations, and security models.

### 🟦 Cybersecurity Frameworks

* NIST Cybersecurity Framework (CSF)
* CIS Controls

### 🟩 Information Security Standards

* ISO/IEC 27001
* ISO/IEC 27002
* PCI DSS
* CIS Benchmarks

### 🟥 Regulations & Laws

* HIPAA
* GDPR
* SOX
* FISMA

### 🟨 Compliance & Assurance

* SOC 2
* HITRUST CSF
* FedRAMP

### 🟪 IT Governance

* COBIT

### 🟧 Application Security

* OWASP Top 10

### 🟫 Threat & Attack Frameworks

* MITRE ATT&CK
* Cyber Kill Chain

---

# 🗂️ Repository Structure

```text
Cybersecurity-Frameworks-Standards-Regulations/
│
├── README.md
│
├── 01-NIST/
│   ├── README.md
│   ├── NIST-CSF-2.0.md
│   ├── NIST-SP-800-53.md
│   └── NIST-SP-800-61.md
│
├── 02-ISO-27001/
│   ├── README.md
│   ├── ISO-27001.md
│   └── ISO-27002.md
│
├── 03-PCI-DSS/
│   └── PCI-DSS.md
│
├── 04-HIPAA/
│   └── HIPAA.md
│
├── 05-GDPR/
│   └── GDPR.md
│
├── 06-SOC-2/
│   └── SOC-2.md
│
├── 07-CIS/
│   ├── CIS-Controls.md
│   └── CIS-Benchmarks.md
│
├── 08-COBIT/
│   └── COBIT.md
│
├── 09-SOX/
│   └── SOX.md
│
├── 10-FISMA/
│   └── FISMA.md
│
├── 11-FedRAMP/
│   └── FedRAMP.md
│
├── 12-HITRUST/
│   └── HITRUST-CSF.md
│
├── 13-OWASP/
│   └── OWASP-Top-10.md
│
├── 14-MITRE-ATTACK/
│   └── MITRE-ATTACK.md
│
├── 15-Cyber-Kill-Chain/
│   └── Cyber-Kill-Chain.md
│
└── comparisons/
    ├── Framework-vs-Standard-vs-Regulation.md
    ├── NIST-vs-ISO-27001.md
    └── Security-Framework-Comparison.md
```

---

# 🎯 Purpose

The purpose of this repository is to understand how cybersecurity is managed at an organizational level.

It covers:

* Cybersecurity risk management
* Information security management
* Security controls
* Compliance requirements
* Privacy and data protection
* IT governance
* Application security
* Incident response
* Threat detection
* Adversary behavior
* Security monitoring

---

# 🧠 Framework vs Standard vs Regulation

One of the most important concepts is understanding that these terms are **not interchangeable**.

| Category             | Examples                | Primary Purpose                         |
| -------------------- | ----------------------- | --------------------------------------- |
| Framework            | NIST CSF, CIS Controls  | Security risk management and safeguards |
| Standard             | ISO/IEC 27001, PCI DSS  | Defined security requirements/practices |
| Regulation / Law     | HIPAA, GDPR, SOX, FISMA | Legal or regulatory obligations         |
| Assurance            | SOC 2                   | Assessment of organizational controls   |
| Governance           | COBIT                   | IT governance and management            |
| Threat Framework     | MITRE ATT&CK            | Understanding adversary behavior        |
| Application Security | OWASP                   | Application security risks              |

---

# 🔐 CIA Triad

Most information-security frameworks ultimately support the three fundamental security objectives:

```text
                CIA TRIAD

           Confidentiality
                 /\
                /  \
               /    \
              /      \
             /        \
        Integrity ---- Availability
```

### Confidentiality

Ensuring that information is accessible only to authorized individuals or systems.

Examples:

* Access control
* Encryption
* Authentication

### Integrity

Ensuring that information remains accurate and is not improperly modified.

Examples:

* Hashing
* File integrity monitoring
* Change management

### Availability

Ensuring that systems and information are available when required.

Examples:

* Backups
* Redundancy
* Disaster recovery
* High availability

---

# 🛡️ Major Frameworks & Standards

## 1. NIST

**National Institute of Standards and Technology**

NIST publishes cybersecurity standards, frameworks, and guidance used to help organizations manage cybersecurity and technology risks.

### Important NIST resources

* NIST Cybersecurity Framework (CSF)
* NIST SP 800-53
* NIST SP 800-61
* NIST SP 800-171
* NIST SP 800-30

### NIST CSF 2.0

The current NIST Cybersecurity Framework is **CSF 2.0**.

Its six core functions are:

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

NIST describes CSF 2.0 as a flexible framework for helping organizations understand, assess, prioritize, and communicate cybersecurity risks.

➡️ Detailed notes: [`01-NIST/`](01-NIST/)

---

# 2. ISO/IEC 27001

ISO/IEC 27001 is an international standard for establishing, implementing, maintaining, and continually improving an **Information Security Management System (ISMS)**.

### Key concept

```text
ISO/IEC 27001
       ↓
     ISMS
       ↓
Risk Management
       ↓
Security Controls
       ↓
Continuous Improvement
```

The current published edition is **ISO/IEC 27001:2022**.

➡️ Detailed notes: [`02-ISO-27001/`](02-ISO-27001/)

---

# 3. PCI DSS

**Payment Card Industry Data Security Standard**

Purpose:

> Protect payment card data and the systems that handle it.

Relevant to organizations involved in payment-card environments.

Important areas include:

* Access control
* Secure configurations
* Vulnerability management
* Encryption
* Logging
* Monitoring
* Security testing

➡️ Detailed notes: [`03-PCI-DSS/`](03-PCI-DSS/)

---

# 4. HIPAA

**Health Insurance Portability and Accountability Act**

A U.S. federal law containing requirements concerning protected health information.

Important concept:

**PHI = Protected Health Information**

Security concepts include:

* Administrative safeguards
* Physical safeguards
* Technical safeguards
* Access control
* Audit controls
* Authentication
* Incident response

➡️ Detailed notes: [`04-HIPAA/`](04-HIPAA/)

---

# 5. GDPR

**General Data Protection Regulation**

A major European data-protection regulation focused on the processing and protection of personal data.

Important concepts:

* Personal data
* Privacy
* Lawful processing
* Data minimization
* Data subject rights
* Data protection
* Breach response

➡️ Detailed notes: [`05-GDPR/`](05-GDPR/)

---

# 6. SOC 2

**Service Organization Control 2**

SOC 2 focuses on controls related to the Trust Services Criteria.

Major categories:

* Security
* Availability
* Processing Integrity
* Confidentiality
* Privacy

### SOC 2 Type I

Evaluates control design at a specific point in time.

### SOC 2 Type II

Evaluates control design and operating effectiveness over a period of time.

➡️ Detailed notes: [`06-SOC-2/`](06-SOC-2/)

---

# 7. CIS Controls

**Center for Internet Security Controls**

CIS Controls provide prioritized cybersecurity safeguards that organizations can implement to reduce common cyber risks.

Examples:

* Asset management
* Account management
* Vulnerability management
* Secure configuration
* Audit logging
* Malware defenses
* Data protection

➡️ Detailed notes: [`07-CIS/CIS-Controls.md`](07-CIS/CIS-Controls.md)

---

# 8. CIS Benchmarks

CIS Benchmarks provide secure configuration recommendations for operating systems, applications, cloud platforms, and other technologies.

Example:

```text
Windows Server
      ↓
Secure Configuration
      ↓
Disable unnecessary services
      ↓
Configure logging
      ↓
Harden authentication
      ↓
Reduce attack surface
```

➡️ Detailed notes: [`07-CIS/CIS-Benchmarks.md`](07-CIS/CIS-Benchmarks.md)

---

# 9. COBIT

**Control Objectives for Information and Related Technologies**

COBIT is primarily focused on **IT governance and management**.

It connects:

```text
Business Objectives
        ↓
IT Governance
        ↓
Risk Management
        ↓
Controls
        ↓
Performance
```

➡️ Detailed notes: [`08-COBIT/`](08-COBIT/)

---

# 10. SOX

**Sarbanes-Oxley Act**

A U.S. law associated with financial reporting, corporate governance, and internal controls.

Cybersecurity-related areas may include:

* Access control
* Audit trails
* Change management
* Separation of duties
* Financial-system security

➡️ Detailed notes: [`09-SOX/`](09-SOX/)

---

# 11. FISMA

**Federal Information Security Modernization Act**

U.S. federal information-security legislation focused on protecting federal information and information systems.

Important concepts:

* Risk management
* Security controls
* Security assessments
* Continuous monitoring
* Authorization

➡️ Detailed notes: [`10-FISMA/`](10-FISMA/)

---

# 12. FedRAMP

**Federal Risk and Authorization Management Program**

FedRAMP provides a standardized approach for security assessment and authorization of cloud services used by U.S. federal agencies.

➡️ Detailed notes: [`11-FedRAMP/`](11-FedRAMP/)

---

# 13. HITRUST CSF

**HITRUST Common Security Framework**

A security and privacy control framework that brings together requirements from multiple sources.

It is particularly relevant in healthcare and other regulated environments.

➡️ Detailed notes: [`12-HITRUST/`](12-HITRUST/)

---

# 14. OWASP Top 10

OWASP focuses on application and web security.

Important risks include:

* Broken Access Control
* Cryptographic Failures
* Injection
* Security Misconfiguration
* Vulnerable and Outdated Components
* Identification and Authentication Failures

➡️ Detailed notes: [`13-OWASP/`](13-OWASP/)

---

# 15. MITRE ATT&CK

MITRE ATT&CK is a knowledge base describing real-world adversary tactics and techniques.

Example attack progression:

```text
Initial Access
      ↓
Execution
      ↓
Persistence
      ↓
Privilege Escalation
      ↓
Defense Evasion
      ↓
Credential Access
      ↓
Discovery
      ↓
Lateral Movement
      ↓
Collection
      ↓
Command & Control
      ↓
Exfiltration / Impact
```

MITRE ATT&CK is especially useful for:

* SOC Analysts
* Threat Hunters
* Detection Engineers
* Incident Responders
* Red Teams

➡️ Detailed notes: [`14-MITRE-ATTACK/`](14-MITRE-ATTACK/)

---

# 16. Cyber Kill Chain

The Cyber Kill Chain describes an attack as a sequence of stages.

```text
Reconnaissance
      ↓
Weaponization
      ↓
Delivery
      ↓
Exploitation
      ↓
Installation
      ↓
Command & Control
      ↓
Actions on Objectives
```

It helps security teams understand where an attack can be detected or disrupted.

➡️ Detailed notes: [`15-Cyber-Kill-Chain/`](15-Cyber-Kill-Chain/)

---

# 🔎 SOC Analyst Relevance

These frameworks are not just theoretical.

A SOC Analyst may use them while:

* Investigating alerts
* Classifying incidents
* Mapping attacker behavior
* Assessing security controls
* Supporting compliance
* Reviewing logs
* Performing threat hunting
* Documenting incidents
* Improving detection rules

### Example

Suppose a suspicious PowerShell command is detected.

```text
SIEM Alert
     ↓
Investigate PowerShell Activity
     ↓
Identify Attacker Behavior
     ↓
Map to MITRE ATT&CK
     ↓
Determine Incident Severity
     ↓
Contain / Escalate
     ↓
Document Findings
```

The organization may additionally use NIST guidance for incident-response processes and security frameworks for broader risk/control management.

---

# 📊 Quick Comparison

| Framework / Standard | Primary Focus                        |
| -------------------- | ------------------------------------ |
| NIST CSF             | Cybersecurity risk management        |
| NIST SP 800-53       | Security & privacy controls          |
| NIST SP 800-61       | Incident response                    |
| ISO/IEC 27001        | ISMS                                 |
| ISO/IEC 27002        | Control guidance                     |
| PCI DSS              | Payment card security                |
| HIPAA                | Protected health information         |
| GDPR                 | Personal-data protection             |
| SOC 2                | Service organization controls        |
| CIS Controls         | Prioritized security safeguards      |
| CIS Benchmarks       | Secure configurations                |
| COBIT                | IT governance                        |
| SOX                  | Financial controls/reporting         |
| FISMA                | U.S. federal information security    |
| FedRAMP              | Federal cloud security authorization |
| HITRUST CSF          | Security/privacy controls            |
| OWASP                | Application security                 |
| MITRE ATT&CK         | Adversary tactics & techniques       |
| Cyber Kill Chain     | Attack lifecycle                     |

---

# 🎯 SOC Analyst Priority

If your goal is SOC Analyst / Security Analyst preparation, prioritize these first:

### High Priority

1. NIST CSF
2. NIST SP 800-61
3. MITRE ATT&CK
4. ISO/IEC 27001
5. CIS Controls
6. PCI DSS
7. OWASP Top 10
8. GDPR
9. HIPAA
10. SOC 2

### Secondary

* CIS Benchmarks
* COBIT
* SOX
* FISMA
* FedRAMP
* HITRUST CSF
* Cyber Kill Chain

---

# 🧩 Important Terminology

| Term          | Meaning                                            |
| ------------- | -------------------------------------------------- |
| Framework     | Structured guidance for managing a particular area |
| Standard      | Defined requirements or practices                  |
| Regulation    | Legal/regulatory requirement                       |
| Control       | Safeguard used to reduce risk                      |
| Compliance    | Meeting applicable requirements                    |
| Risk          | Potential impact from uncertainty/threat           |
| Threat        | Potential cause of harm                            |
| Vulnerability | Weakness that can be exploited                     |
| Asset         | Something valuable that needs protection           |
| ISMS          | Information Security Management System             |
| PHI           | Protected Health Information                       |
| PII           | Personally Identifiable Information                |
| SIEM          | Security Information and Event Management          |
| SOC           | Security Operations Center                         |

---

# 🚀 Learning Path

Recommended order:

```text
01 → NIST CSF
        ↓
02 → ISO/IEC 27001
        ↓
03 → CIS Controls
        ↓
04 → PCI DSS
        ↓
05 → HIPAA
        ↓
06 → GDPR
        ↓
07 → SOC 2
        ↓
08 → OWASP
        ↓
09 → MITRE ATT&CK
        ↓
10 → Cyber Kill Chain
        ↓
11 → Governance & Compliance
        ↓
12 → Framework Comparisons
```

---

# 📌 Disclaimer

This repository is intended for **educational and cybersecurity interview-preparation purposes**.

It does not constitute legal, regulatory, audit, compliance, or professional security advice.

For compliance decisions, organizations should consult the applicable official standards, regulations, contractual requirements, and qualified professionals.

---

# 📚 Official References

* [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
* [NIST CSF 2.0](https://www.nist.gov/publications/nist-cybersecurity-framework-csf-20)
* [ISO/IEC 27001](https://www.iso.org/standard/27001.html)

---

## ⭐ Repository Goal

Build a practical understanding of:

```text
Cybersecurity
      ↓
Risk Management
      ↓
Security Controls
      ↓
Compliance
      ↓
Threat Detection
      ↓
Incident Response
      ↓
Continuous Improvement
```

**Learning cybersecurity is not only about knowing how attacks work — it is also about understanding how organizations manage, reduce, monitor, and govern security risk.**
