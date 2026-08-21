# 🚨 NIST SP 800-61 — Incident Response

## 📌 Overview

**NIST SP 800-61** is a NIST publication that provides guidance for organizations to establish and improve their **Computer Security Incident Response Capability (CSIRC)**.

### Simple Definition

> **NIST SP 800-61 provides guidance for preparing for, detecting, analyzing, responding to, and recovering from cybersecurity incidents.**

It is highly relevant to:

* SOC Analysts
* Incident Responders
* Security Analysts
* Threat Hunters
* Security Engineers

---

# 🧠 What is an Incident?

A **security incident** is an event that actually or potentially threatens the confidentiality, integrity, or availability of information or information systems.

Examples:

* Malware infection
* Ransomware
* Phishing
* Credential compromise
* Unauthorized access
* Data exfiltration
* Privilege escalation
* Denial-of-Service attack
* Suspicious insider activity

---

# ⚠️ Event vs Alert vs Incident

These three terms are commonly confused.

## Event

An observable occurrence in a system.

Example:

```text
User Login
```

A login is an event. It is not automatically malicious.

---

## Alert

A security system identifies activity that may require investigation.

Example:

```text
50 Failed Logins
       ↓
SIEM Rule
       ↓
Security Alert
```

An alert is an indication that something suspicious may have occurred.

---

## Incident

After investigation, the activity is determined to represent an actual or potential security compromise requiring response.

```text
Event
  ↓
Alert
  ↓
Investigation
  ↓
Confirmed Security Incident
```

---

# 🎯 Purpose of Incident Response

Incident response helps an organization:

* Detect incidents quickly
* Analyze incidents accurately
* Limit damage
* Contain threats
* Remove malicious activity
* Restore normal operations
* Preserve evidence
* Learn from incidents
* Improve security controls

---

# 🔄 Incident Response Lifecycle

NIST SP 800-61 Rev. 2 is commonly represented using four major phases:

```text
       PREPARATION
            ↓
   DETECTION & ANALYSIS
            ↓
CONTAINMENT, ERADICATION
       & RECOVERY
            ↓
   POST-INCIDENT ACTIVITY
            ↓
       IMPROVEMENT
```

These activities are not necessarily strictly linear.

An incident responder may move back and forth between analysis, containment, eradication, and recovery as new evidence is discovered.

---

# 1️⃣ Preparation

## Definition

Preparation involves establishing the capabilities, processes, tools, people, and resources required to handle security incidents.

### Preparation includes:

* Incident response policy
* Incident response plan
* Roles and responsibilities
* Contact information
* SIEM
* EDR
* Network monitoring
* Logging
* Backup systems
* Threat intelligence
* Forensic tools
* Communication procedures
* Training
* Incident-response exercises

---

# 🛠️ Example

Before an incident occurs, an organization should have:

```text
SIEM
 ↓
Centralized Logs
 ↓
Alert Rules
 ↓
SOC Analysts
 ↓
Escalation Process
 ↓
Incident Response Team
```

If ransomware occurs, the organization is not starting from zero.

---

# 👥 Incident Response Roles

Depending on the organization, incident response can involve:

* SOC Analyst
* Incident Responder
* Security Engineer
* Threat Hunter
* Digital Forensics Analyst
* Malware Analyst
* Network Engineer
* System Administrator
* IT Team
* Legal Team
* Management
* Communications / PR
* Business Owners

---

# 2️⃣ Detection and Analysis

This is one of the most important phases for a SOC Analyst.

## Detection

Security teams identify possible malicious activity using:

* SIEM
* EDR
* IDS/IPS
* Firewall
* Antivirus
* Cloud security tools
* Authentication logs
* Threat intelligence
* User reports

---

# 🔎 Example

```text
Multiple Failed Logins
        ↓
Successful Login
        ↓
Unusual Source IP
        ↓
SIEM Correlation
        ↓
SOC Alert
```

The SOC analyst now investigates the alert.

---

# 🔍 Analysis

The analyst determines:

* What happened?
* When did it happen?
* Which account was involved?
* Which system was affected?
* What IP address was involved?
* What process executed?
* Was malware involved?
* Was data accessed?
* Is the activity malicious?
* Is the incident still active?

---

# 🧩 Incident Investigation

A basic investigation can follow:

```text
Alert
 ↓
Validate
 ↓
Collect Evidence
 ↓
Analyze Logs
 ↓
Identify Scope
 ↓
Determine Impact
 ↓
Determine Severity
 ↓
Escalate / Respond
```

---

# 📊 Important Investigation Data

SOC analysts may examine:

### Authentication

* Username
* Source IP
* Destination system
* Login time
* Login result
* Authentication method

### Endpoint

* Process
* Parent process
* Command line
* File path
* Hash
* User
* Network connection

### Network

* Source IP
* Destination IP
* Port
* Protocol
* Domain
* URL
* Traffic volume

### Email

* Sender
* Recipient
* Subject
* Attachment
* URL
* Message headers

---

# ⏱️ Establishing a Timeline

Timeline analysis is critical.

Example:

```text
09:00 → Phishing email received
09:05 → User clicked link
09:07 → Credentials submitted
09:10 → Suspicious login
09:12 → PowerShell executed
09:15 → C2 connection established
09:20 → SOC alert generated
```

This helps reconstruct the attack.

---

# 🗺️ Determining Scope

The SOC needs to determine how far the attack spread.

Questions:

* One user or multiple users?
* One endpoint or multiple endpoints?
* One account or several accounts?
* Was lateral movement observed?
* Was data accessed?
* Was data exfiltrated?

Example:

```text
Compromised Laptop
       ↓
Credential Theft
       ↓
Domain Account
       ↓
Domain Controller Access
       ↓
Multiple Systems
```

This is much more serious than a single isolated endpoint infection.

---

# 📈 Incident Prioritization

Incidents should be prioritized based on factors such as:

* Business impact
* Asset criticality
* Data sensitivity
* Scope
* Attacker activity
* Potential damage
* Confidence level

### Example

| Incident                              | Priority    |
| ------------------------------------- | ----------- |
| Single failed login                   | Low         |
| Repeated brute-force attempt          | Medium      |
| Malware on employee endpoint          | Medium/High |
| Domain administrator compromise       | Critical    |
| Active ransomware                     | Critical    |
| Confirmed sensitive-data exfiltration | Critical    |

Actual severity depends on organizational context and incident-response policy.

---

# 3️⃣ Containment

## Definition

**Containment** limits the spread and impact of an incident.

The objective is:

> Stop the attacker from causing further damage while preserving the ability to investigate.

---

# 🟡 Short-Term Containment

Immediate actions.

Examples:

* Isolate endpoint
* Block malicious IP
* Disable compromised account
* Block malicious domain
* Quarantine email
* Disable malicious process

Example:

```text
Compromised Endpoint
       ↓
EDR Isolation
       ↓
Network Access Blocked
```

---

# 🟠 Long-Term Containment

More sustainable temporary measures while remediation continues.

Examples:

* Network segmentation
* Temporary firewall rules
* Restrict privileged access
* Move services to clean infrastructure
* Apply temporary configuration changes

---

# 4️⃣ Eradication

## Definition

**Eradication removes the root cause and malicious artifacts of the incident.**

Examples:

* Remove malware
* Delete malicious accounts
* Remove persistence mechanisms
* Patch exploited vulnerabilities
* Reset compromised credentials
* Remove malicious scheduled tasks
* Remove unauthorized software

---

# 🦠 Example

Suppose malware created a persistence mechanism:

```text
Malware
  ↓
Scheduled Task
  ↓
Persistence
```

Eradication:

```text
Identify Task
      ↓
Remove Task
      ↓
Remove Malware
      ↓
Patch Vulnerability
      ↓
Reset Credentials
```

---

# 5️⃣ Recovery

## Definition

Recovery restores systems and services to normal operation and verifies that the environment is secure.

Activities may include:

* Restore systems
* Restore backups
* Rebuild compromised systems
* Validate security controls
* Monitor restored systems
* Return services to production

---

# 🔄 Example

```text
Ransomware
    ↓
Contain
    ↓
Eradicate
    ↓
Rebuild Systems
    ↓
Restore Clean Backup
    ↓
Validate
    ↓
Enhanced Monitoring
    ↓
Normal Operations
```

---

# 6️⃣ Post-Incident Activity

After the incident is handled, the organization should review what happened.

Questions:

* What happened?
* Why did it happen?
* How was it detected?
* How long did detection take?
* How effective was containment?
* What controls failed?
* What should be improved?

---

# 📝 Lessons Learned

Example:

### Finding

Phishing email bypassed email security controls.

### Root Cause

Malicious domain was not detected.

### Improvement

```text
Email Security
      +
Threat Intelligence
      +
URL Analysis
      +
User Awareness
```

---

# 🔥 Root Cause Analysis

Root cause analysis identifies the underlying reason an incident occurred.

Example:

```text
Ransomware
    ↓
Malicious Execution
    ↓
Phishing Attachment
    ↓
User Opened Attachment
    ↓
Email Security Failed
```

The root cause may involve multiple weaknesses rather than one single failure.

---

# 📊 Incident Response Metrics

Organizations can measure incident-response performance.

Important metrics include:

### MTTD

**Mean Time To Detect**

How long it takes to detect an incident.

```text
Attack
 ↓
Detection
```

---

### MTTR

**Mean Time To Respond/Recover**

Depending on the organization's defined metric, MTTR can refer to the time taken to respond to or recover from an incident.

Always check how the organization defines MTTR.

---

### Example

```text
Attack
  ↓
10 minutes
  ↓
Detection

Detection
  ↓
20 minutes
  ↓
Containment
```

The organization can use these measurements to identify response bottlenecks.

---

# 🧠 Incident Response Example

## Scenario: Phishing Attack

### Step 1 — Preparation

Organization has:

* Email security
* SIEM
* EDR
* Incident-response plan

↓

### Step 2 — Detection

User reports suspicious email.

↓

SOC analyzes:

```text
Sender
URL
Attachment
Headers
Domain
IP
```

↓

### Step 3 — Analysis

SOC discovers:

```text
User clicked malicious URL
       ↓
Credentials submitted
       ↓
Suspicious login detected
```

↓

### Step 4 — Containment

SOC:

* Disables account
* Revokes sessions
* Blocks malicious domain
* Quarantines email

↓

### Step 5 — Eradication

* Remove malicious artifacts
* Reset password
* Investigate endpoint
* Remove persistence if present

↓

### Step 6 — Recovery

* Restore affected system
* Validate endpoint
* Re-enable account when appropriate
* Increase monitoring

↓

### Step 7 — Post-Incident

* Document incident
* Identify root cause
* Improve email filtering
* Update detections
* Conduct awareness training

---

# 🛡️ NIST SP 800-61 and SOC

A SOC commonly interacts with incident response like this:

```text
SIEM
 ↓
Alert
 ↓
SOC L1
 ↓
Triage
 ↓
False Positive?
 ↙       ↘
YES       NO
 ↓         ↓
Close    Investigate
            ↓
        SOC L2 / IR
            ↓
        Containment
            ↓
        Eradication
            ↓
          Recovery
```

---

# 🔗 NIST SP 800-61 and NIST CSF

These are complementary.

### NIST CSF

Broad cybersecurity risk-management framework.

```text
Govern
Identify
Protect
Detect
Respond
Recover
```

### NIST SP 800-61

Detailed incident-response guidance.

```text
Preparation
      ↓
Detection & Analysis
      ↓
Containment
      ↓
Eradication
      ↓
Recovery
      ↓
Post-Incident Activity
```

---

# 🔗 NIST SP 800-61 and NIST SP 800-53

### SP 800-53

Provides security and privacy controls.

### SP 800-61

Provides incident-response guidance.

Example:

```text
SP 800-53
   ↓
AU → Logging
SI → Monitoring / Integrity
IR → Incident Response Controls
   ↓
SP 800-61
   ↓
Use those capabilities during incident response
```

---

# 🚨 SOC Analyst Responsibilities During an Incident

A SOC Analyst may:

### L1

* Monitor alerts
* Validate alerts
* Perform initial triage
* Collect basic evidence
* Enrich IOCs
* Document findings
* Escalate confirmed incidents

### L2

* Perform deeper investigation
* Correlate multiple data sources
* Determine scope
* Hunt for related activity
* Support containment
* Perform detailed analysis

### L3 / Incident Response / Detection Engineering

* Advanced investigation
* Malware analysis
* Forensics
* Detection development
* Root-cause analysis
* Threat hunting
* Long-term remediation

Roles differ by organization.

---

# 🧩 Important IOCs

During incident response, analysts may collect **Indicators of Compromise (IOCs)**.

Examples:

* IP addresses
* Domains
* URLs
* File hashes
* Email addresses
* File names
* Registry keys
* Malware signatures

Example:

```text
Malicious IP
185.x.x.x

Malicious Domain
example-malicious.com

SHA-256
<hash>
```

These indicators can be searched across the environment.

---

# 🧠 IOC vs IOA

### IOC

**Indicator of Compromise**

Evidence that a compromise may have occurred.

Examples:

* Malicious hash
* Known C2 IP
* Malicious domain

### IOA

**Indicator of Attack**

Behavior suggesting an attack is occurring.

Example:

```text
PowerShell
    ↓
Encoded Command
    ↓
Downloads Payload
    ↓
Executes Payload
```

The behavior itself can be suspicious even if the exact malware hash is unknown.

---

# 🔎 Evidence Preservation

Incident response may involve digital evidence.

Important principles:

* Preserve relevant logs
* Record timestamps
* Maintain chain of custody where applicable
* Avoid unnecessary modification of evidence
* Document actions
* Preserve forensic images when required

This becomes particularly important during:

* Legal investigations
* Insider-threat investigations
* Malware investigations
* Data-breach investigations

---

# 📊 Incident Documentation

A good incident record may contain:

```text
Incident ID
Date / Time
Detection Source
Affected Asset
Affected User
Severity
Description
Indicators
Timeline
Analysis
Containment Actions
Eradication Actions
Recovery Actions
Root Cause
Lessons Learned
Recommendations
```

---

# 🎯 Interview Questions

## Q1. What is NIST SP 800-61?

NIST SP 800-61 provides guidance for establishing and improving an organization's computer security incident-response capability.

---

## Q2. What are the major incident-response phases?

For the commonly used NIST SP 800-61 Rev. 2 lifecycle:

```text
Preparation
Detection & Analysis
Containment, Eradication & Recovery
Post-Incident Activity
```

---

## Q3. What is containment?

Containment limits the spread and impact of an incident.

Example:

> Isolating a compromised endpoint from the network.

---

## Q4. What is eradication?

Eradication removes the root cause and malicious artifacts.

Example:

> Removing malware, persistence mechanisms, and patching the exploited vulnerability.

---

## Q5. What is recovery?

Recovery restores affected systems and services to normal operation while validating that they are secure.

---

## Q6. What is the difference between an event and an incident?

An event is an observable occurrence.

An incident is an event or set of events that actually or potentially threatens security and requires response under the organization's criteria.

---

## Q7. What is MTTD?

**Mean Time To Detect** — the average time taken to detect a security incident.

---

## Q8. What is an IOC?

An Indicator of Compromise is observable evidence that may indicate a system or environment has been compromised.

---

## Q9. What is the role of a SOC L1 analyst?

Typical responsibilities include:

* Alert monitoring
* Initial triage
* Basic investigation
* IOC enrichment
* Documentation
* Escalation

---

# 📝 Quick Revision

```text
NIST SP 800-61
        ↓
Incident Response
        ↓
Preparation
        ↓
Detection & Analysis
        ↓
Containment
        ↓
Eradication
        ↓
Recovery
        ↓
Post-Incident Activity
```

### Remember:

```text
Preparation
    = Be Ready

Detection
    = Find It

Analysis
    = Understand It

Containment
    = Stop It From Spreading

Eradication
    = Remove It

Recovery
    = Restore Operations

Post-Incident
    = Learn & Improve
```

---

# ⭐ Key Takeaways

* NIST SP 800-61 focuses on **incident response**.
* It is highly relevant to SOC operations.
* Preparation happens before incidents.
* Detection and analysis identify and understand suspicious activity.
* Containment limits damage and spread.
* Eradication removes malicious artifacts and root causes.
* Recovery restores normal operations.
* Post-incident activity identifies lessons and improvements.
* SOC analysts perform alert triage, investigation, enrichment, documentation, and escalation.
* IOCs help identify possible compromise.
* Incident response should be documented and repeatable.
* NIST SP 800-61 complements NIST CSF and NIST SP 800-53.

---

# 📚 Official Reference

NIST Computer Security Incident Handling Guide:

https://csrc.nist.gov/pubs/sp/800/61/r2/final

NIST Cybersecurity Publications:

https://csrc.nist.gov/publications
