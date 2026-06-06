[Home](index.md) | [About](about.md) | [Certifications](certifications.md) | [Projects](projects.md) | [Contact](contact.md)

## SOC Analyst | Threat Hunter | Detection Engineering | IR

Welcome to my cybersecurity portfolio. 

This portfolio documents a hands-on SOC, Incident Response, Threat Hunting, Detection Engineering, Threat Intelligence, and SOAR Automation lab. 

This website documents hands-on security projects focused on:

* Threat Hunting
* Detection Engineering
* Threat Intelligence
* Splunk Enterprise
* Sysmon
* MISP
* Sigma
* PySigma
* SOAR Automation


## Current Lab

### SOC Detection Engineering, Threat Hunting and DFIR Lab

A hands-on SOC lab focused on vulnerability assessment, attack simulation, endpoint telemetry, Splunk ingestion, threat hunting, MITRE ATT&CK mapping, threat intelligence, IR, detection engineering, and SOAR automation.


## Portfolio Sections

* Lab Architecture
* Vulnerability Assessment
* Attack Simulation
* Endpoint Telemetry
* Splunk Ingestion
* Threat Hunting
* MITRE ATT&CK Mapping
* Threat Intelligence
* SOC Investigations
* Detection Engineering with Sigma
* SOAR Automation


## Key Achievements

✅ Built an end-to-end SOC lab covering Telemetry → Detection → Threat Hunting → Incident Response → Threat Intelligence → SOAR Automation

✅ Deployed and integrated Splunk Enterprise, Sysmon, MISP, Nessus, Docker, and Windows endpoints within a single security monitoring environment

✅ Created and validated Sigma detection rules using PySigma and Splunk

✅ Mapped observed attacker behaviours to MITRE ATT&CK techniques and tactics

✅ Performed Threat Intelligence investigations using MISP and IOC enrichment workflows

✅ Conducted Incident Response investigations including persistence, lateral movement, command and control, and data exfiltration scenarios

✅ Developed SOAR playbooks and security automation workflows using Python and threat intelligence enrichment processes

✅ Produced 30+ technical project write-ups supported by 49+ screenshots, validation artefacts, and investigation evidence



## Project Journey

Designed and built a complete SOC Detection Engineering, Threat Hunting, Threat Intelligence, and Incident Response lab from the ground up using Splunk Enterprise, Sysmon, Nessus Essentials, MISP, Sigma, and the BOTSv3 dataset.

During the project, multiple technical challenges were encountered and resolved. Initial attempts to forward Windows event logs from a Windows 11 UTM virtual machine to a Splunk Enterprise instance running on macOS were unsuccessful, requiring redesign of the lab architecture. To overcome compatibility and telemetry collection issues, the environment was rebuilt using a dedicated Windows 7 endpoint and a Kali Linux attacker system.

Successfully deployed and configured Sysmon and Splunk Universal Forwarder on legacy Windows infrastructure, generated endpoint telemetry, and validated successful ingestion into Splunk Enterprise for security monitoring and threat hunting activities.

Conducted vulnerability assessments using Nessus Essentials, identified a critical MS17-010 (EternalBlue) exposure, validated the findings through SMB enumeration activities, and analyzed resulting telemetry through Splunk-based investigations.

Developed structured threat hunting investigations covering malicious domains, malware hashes, suspicious PowerShell activity, attacker behaviour analysis, detection engineering, threat intelligence enrichment, and incident response workflows.

The project demonstrates the ability to design, build, troubleshoot, document, and operate an end-to-end SOC environment using real telemetry and industry-standard security technologies.

## Featured Investigations

### Investigation 03 – Suspicious hdoor.exe Activity

Analysis of PowerShell execution, process creation telemetry, SHA256 extraction, internal network enumeration, service discovery activity, and MITRE ATT&CK mapping.

### Investigation 04 – MISP Threat Intelligence Enrichment

IOC enrichment using MISP, CIRCL OSINT Feed, Botvrij.eu Feed, and threat intelligence validation workflows.

### Detection Engineering 04 – Scheduled Task Persistence

Sigma-based detection for suspicious PowerShell-driven scheduled task creation involving `schtasks.exe`, SYSTEM execution, hidden PowerShell activity, and Splunk validation.

### Detection Engineering 05 – Threat Intelligence Driven Detection

Transformation of Space Pirates and PlugX RAT threat intelligence into behavioral Sigma detections using MITRE ATT&CK mapping, PySigma conversion, and Splunk validation.

---

## Key Portfolio Message

This portfolio demonstrates the full SOC workflow:

Threat Hunting
      ↓
Threat Intelligence
      ↓
Detection Engineering
      ↓
Sigma Rule Development
      ↓
PySigma Conversion
      ↓
Splunk Validation
      ↓
SOC Investigation
      ↓


Core lesson:

> Hashes change. IPs change. Domains change. Behaviors persist.


