# MITRE ATT&CK Mapping

## Overview

This section maps adversary behaviours observed throughout the lab environment to the MITRE ATT&CK framework.

The objective is to understand attacker tactics, techniques, and procedures (TTPs), improve detection coverage, and align investigations with industry-standard threat modelling practices.

Mappings are derived from vulnerability assessments, attack simulations, threat hunting activities, incident response investigations, and threat intelligence analysis performed throughout the lab.


## Assessment Scope

MITRE ATT&CK mappings were developed using evidence collected from:

* Nessus Vulnerability Assessments
* SMB Enumeration Activities
* Sysmon Endpoint Telemetry
* Splunk Threat Hunting Investigations
* Threat Intelligence Analysis
* PowerShell Investigations
* Persistence Investigations
* Lateral Movement Investigations
* Data Exfiltration Simulations
* Fileless Malware Investigations

---

## ATT&CK Technique Mapping

| Tactic              | Technique ID | Technique                              |
| ------------------- | ------------ | -------------------------------------- |
| Discovery           | T1046        | Network Service Discovery              |
| Discovery           | T1018        | Remote System Discovery                |
| Execution           | T1059.001    | PowerShell                             |
| Execution           | T1059.003    | Windows Command Shell                  |
| Persistence         | T1547.001    | Registry Run Keys / Startup Folder     |
| Defense Evasion     | T1027        | Obfuscated Files or Information        |
| Lateral Movement    | T1021.002    | SMB / Windows Admin Shares             |
| Lateral Movement    | T1047        | Windows Management Instrumentation     |
| Command and Control | T1071.001    | Application Layer Protocol             |
| Exfiltration        | T1048        | Exfiltration Over Alternative Protocol |
| Exploitation        | T1210        | Exploitation of Remote Services        |

---

## Technique Analysis

### Discovery

#### T1046 – Network Service Discovery

Observed during SMB enumeration activities conducted from the Kali Linux attacker platform.

Evidence:

* SMB Enumeration
* Service Discovery
* TCP/445 Identification
* Nessus Validation

#### T1018 – Remote System Discovery

The Windows endpoint was identified and profiled through reconnaissance activities.

Evidence:

* Host Identification
* Operating System Discovery
* SMB Banner Enumeration


### Execution

#### T1059.001 – PowerShell

PowerShell activity was observed across multiple investigations and attack simulations.

Evidence:

* PowerShell Execution Monitoring
* Event ID 4104 Analysis
* Sysmon Process Creation Events
* Fileless PowerShell Beacon Investigation

#### T1059.003 – Windows Command Shell

Command-line execution activity was captured through endpoint telemetry.

Evidence:

* cmd.exe Execution
* Sysmon Event ID 1
* Splunk Process Analysis


### Persistence

#### T1547.001 – Registry Run Keys / Startup Folder

Persistence was simulated using Atomic Red Team and validated through registry analysis.

Evidence:

* Registry Run Key Creation
* Atomic Red Team Simulation
* PowerShell Event ID 4104
* Persistence Hunting Investigation


### Defense Evasion

#### T1027 – Obfuscated Files or Information

Observed during fileless PowerShell beacon simulations using dynamically generated payloads.

Evidence:

* Encoded PowerShell Commands
* Variable Randomisation
* Polymorphic Payload Generation


### Lateral Movement

#### T1021.002 – SMB / Windows Admin Shares

SMB services were identified and evaluated during attack simulation activities.

Evidence:

* SMBv1 Enabled
* SMB Signing Disabled
* Accessible SMB Service

#### T1047 – Windows Management Instrumentation

WMI activity was validated during lateral movement investigations.

Evidence:

* Remote Command Execution
* WMI Commands
* Event ID 4688 Analysis


### Command and Control

#### T1071.001 – Application Layer Protocol

Command and control activity was simulated using PowerShell-based beaconing.

Evidence:

* HTTP Beacon Traffic
* PowerShell Beacon Investigation
* Event ID 4104 Analysis



### Exfiltration

#### T1048 – Exfiltration Over Alternative Protocol

Low and slow UDP-based data exfiltration was simulated and investigated.

Evidence:

* UDP Traffic Analysis
* Wireshark Packet Validation
* PowerShell Exfiltration Activity

### Exploitation

#### T1210 – Exploitation of Remote Services

The Windows 7 endpoint was identified as vulnerable to MS17-010 (EternalBlue).

Evidence:

* SMBv1 Exposure
* Missing Security Patches
* Nessus Vulnerability Findings
* Remote Code Execution Risk


## Detection Coverage

The following telemetry sources provided visibility into mapped ATT&CK techniques:

* Sysmon Event ID 1 – Process Creation
* Sysmon Event ID 3 – Network Connections
* Sysmon Event ID 5 – Process Termination
* PowerShell Event ID 4104 – ScriptBlock Logging
* Windows Event ID 4688 – Process Creation
* Splunk Threat Hunting Queries
* SOC Dashboard Visualisations
* Threat Intelligence Enrichment


## Outcome

The lab successfully mapped observed attacker behaviours to multiple MITRE ATT&CK tactics and techniques across the attack lifecycle.

This process improved understanding of adversary methodology, strengthened detection coverage, and validated the effectiveness of endpoint telemetry, threat hunting workflows, and incident response investigations.
