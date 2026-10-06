# Defensive Security Intro

**Platform:** TryHackMe  
**Room:** Defensive Security Intro  
**Difficulty:** Easy  
**Status:** Completed ✅

This room introduced the fundamentals of defensive cybersecurity and how security teams detect, investigate, and respond to threats.

It provided an overview of defensive security roles and introduced areas such as Security Operations Centres (SOC), digital forensics, incident response, threat intelligence, and malware analysis.

🔗 **Official Room:** https://tryhackme.com/room/defensivesecurityintro

---

## 🎯 Objective

The objective of this room was to understand how organisations defend systems against cyber threats and how defenders investigate suspicious activity.

The room focused on:

- Defensive security fundamentals
- Security Operations Centres (SOC)
- Digital Forensics and Incident Response (DFIR)
- Threat intelligence
- Malware analysis
- Security Information and Event Management (SIEM)
- Defensive security workflows

---

## 🛡️ What Is Defensive Security?

Defensive security focuses on protecting systems, networks, applications, and users from cyber threats.

A simplified defensive workflow is:

```text
Prevent
  ↓
Monitor
  ↓
Detect
  ↓
Investigate
  ↓
Respond
  ↓
Recover
  ↓
Improve
```

The goal is not only to prevent attacks, but also to detect and respond to incidents when prevention fails.

---

## 🏢 Security Operations Centre (SOC)

A **Security Operations Centre (SOC)** is a team or function responsible for monitoring and defending an organisation's environment.

A SOC commonly performs:

- Security monitoring
- Alert triage
- Threat detection
- Incident investigation
- Incident response
- Log analysis
- Threat intelligence
- Security reporting

### Typical SOC workflow

```text
Security Events
      ↓
Log / Telemetry Collection
      ↓
Alert Generation
      ↓
Alert Triage
      ↓
Investigation
      ↓
Incident Response
      ↓
Documentation
```

This introduced me to the general workflow used by defensive security teams.

---

## 🔎 Digital Forensics & Incident Response (DFIR)

DFIR combines two closely related areas:

### Digital Forensics

Digital forensics focuses on collecting and analysing digital evidence.

Examples include investigating:

- Files
- System activity
- Logs
- Network evidence
- Browser artefacts
- Disk images
- Memory

### Incident Response

Incident response focuses on handling security incidents.

A simplified process is:

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

The goal is to understand what happened, limit damage, remove the threat, and improve future security.

---

## 🧠 Threat Intelligence

Threat intelligence involves collecting and analysing information about threats and threat actors.

Useful intelligence can include:

- Malicious IP addresses
- Domains
- URLs
- File hashes
- Malware indicators
- Attack techniques
- Threat actor behaviour

These indicators can help defenders identify suspicious activity and improve detection.

---

## 🦠 Malware Analysis

Malware analysis is the process of examining malicious software to understand its behaviour and capabilities.

Common approaches include:

### Static Analysis

Examining malware without executing it.

Examples:

- File hashes
- Strings
- Metadata
- File structure
- Embedded information

### Dynamic Analysis

Observing malware while it executes in a controlled environment.

Examples:

- Processes created
- Files modified
- Network connections
- Registry changes
- System behaviour

A simplified workflow:

```text
Suspicious File
      ↓
Identify & Hash
      ↓
Static Analysis
      ↓
Controlled Execution
      ↓
Observe Behaviour
      ↓
Extract Indicators
      ↓
Detection / Response
```

---

## 📊 SIEM

A **Security Information and Event Management (SIEM)** system collects and analyses security-related logs and events from different sources.

Typical data sources include:

- Servers
- Endpoints
- Firewalls
- Applications
- Authentication systems
- Network devices

A simplified SIEM workflow:

```text
Multiple Data Sources
        ↓
     Log Collection
        ↓
       SIEM
        ↓
Correlation & Analysis
        ↓
      Alerts
        ↓
   Investigation
```

SIEM technology is particularly important in SOC environments.

---

## 🔧 Skills & Concepts Introduced

| Area | Understanding |
|---|---|
| Defensive Security | ✅ |
| SOC | ✅ |
| Alert Monitoring | ✅ |
| Incident Response | ✅ |
| Digital Forensics | ✅ |
| Threat Intelligence | ✅ |
| Malware Analysis | ✅ |
| SIEM | ✅ |

---

## 🔐 Cybersecurity Relevance

Defensive security complements offensive security.

A security professional benefits from understanding both sides:

```text
OFFENSIVE SECURITY
        ↓
How can systems be attacked?
        │
        ▼
DEFENSIVE SECURITY
        ↓
How can those attacks be detected,
prevented, investigated and contained?
```

The concepts from this room provide a foundation for later learning in:

- SOC analysis
- SIEM
- Log analysis
- Threat hunting
- Incident response
- Digital forensics
- Malware analysis
- Detection engineering
- Blue-team operations

---

## 🧠 Key Takeaways

- Defensive security focuses on protecting and monitoring systems.
- SOC teams continuously monitor security events and investigate alerts.
- DFIR combines digital evidence analysis with incident response.
- Threat intelligence helps defenders understand current and emerging threats.
- Malware analysis helps determine how malicious software behaves.
- SIEM platforms centralise and correlate security logs.
- Effective defense requires detection, investigation, response, and continuous improvement.

---

## 📝 Learning Flow

My learning from this room can be summarised as:

```text
Understand Defensive Security
            ↓
       Learn SOC Role
            ↓
     Understand DFIR
            ↓
   Explore Threat Intelligence
            ↓
     Learn Malware Analysis
            ↓
      Understand SIEM
            ↓
     Build Blue-Team Skills
```

---

## 🚀 What This Room Built Toward

This room gave me an introductory foundation for further defensive-security practice.

Potential next areas include:

- Linux and Windows log analysis
- SIEM investigation
- SOC alert triage
- Network monitoring
- Threat hunting
- Incident response
- Digital forensics
- Malware analysis
- Detection engineering

These topics can be developed further through dedicated labs and practical projects.

---

## ⚖️ Ethical Practice

All practical activity documented here was performed inside the authorised TryHackMe training environment.

The knowledge and techniques are intended for:

- Education
- Defensive security
- Authorized investigations
- Cybersecurity labs
- Responsible security practice

---

**Status: Completed ✅**
