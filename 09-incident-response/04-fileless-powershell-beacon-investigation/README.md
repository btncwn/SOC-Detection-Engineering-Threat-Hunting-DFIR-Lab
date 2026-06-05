# Incident Response Investigation 04 – Fileless PowerShell Beacon Detection

## Overview

This investigation documents the execution and detection of a fileless PowerShell beacon operating entirely in memory.

The objective was to simulate attacker techniques that avoid writing files to disk while maintaining periodic communication with a remote system.

The investigation focuses on PowerShell execution, beacon validation, PowerShell ScriptBlock Logging, and incident response analysis.

---

## Scenario

A polymorphic PowerShell beacon was generated using a Python script and executed directly from memory.

The beacon:

* Executed without creating a `.ps1` file on disk
* Generated randomized variable and function names
* Sent periodic HTTP requests to a Kali Linux listener
* Operated at 30-second intervals to simulate low and slow command-and-control activity

The activity was monitored using PowerShell ScriptBlock Logging (Event ID 4104).

---

## Investigation Workflow

```text
Python Payload Generated
            ↓
Fileless PowerShell Execution
            ↓
Beacon Communication Established
            ↓
Kali Listener Validation
            ↓
Event ID 4104 Detection
            ↓
Evidence Collection
            ↓
Incident Response Assessment
```

---

## Evidence Collected

| Screenshot                         | Description                                  |
| ---------------------------------- | -------------------------------------------- |
| 01-kali-beacon-listener.png        | Kali Linux listener receiving beacon traffic |
| 02-powershell-beacon-execution.png | PowerShell beacon execution activity         |
| 03-eventid-4104-detection.png      | Event ID 4104 PowerShell ScriptBlock Logging |

---

## Beacon Execution Analysis

A Python-based payload generator was used to create a polymorphic PowerShell beacon.

The generated payload executed entirely in memory and did not require a PowerShell script file to be written to disk.

The beacon transmitted periodic HTTP requests to a remote listener while using randomized variable names and function names.

### PowerShell Execution Evidence

![PowerShell Beacon Execution](screenshots/02-powershell-beacon-execution.png)

The activity generated recurring outbound communications every 30 seconds.

---

## Command and Control Validation

A Kali Linux listener was configured to receive inbound beacon communications.

The listener successfully recorded periodic requests from the Windows endpoint.

### Listener Evidence

![Kali Beacon Listener](screenshots/01-kali-beacon-listener.png)

This validated successful communication between the Windows endpoint and the remote system.

---

## PowerShell Detection Analysis

PowerShell ScriptBlock Logging was enabled to capture executed script content.

Event ID 4104 recorded the PowerShell activity and provided visibility into the executed commands.

### Event ID 4104 Evidence

![Event ID 4104 Detection](screenshots/03-eventid-4104-detection.png)

The logged activity contained evidence of PowerShell network communication and beacon execution behavior.

---

## Key Findings

### Fileless Execution

The beacon executed entirely in memory without creating a PowerShell script file on disk.

### Polymorphic Behaviour

Variable names and function names changed during payload generation, reducing the effectiveness of static signatures.

### Beacon Communication

The Windows endpoint successfully communicated with the Kali Linux listener at regular intervals.

### Detection Visibility

PowerShell ScriptBlock Logging successfully captured execution details despite the absence of a file on disk.

---

## MITRE ATT&CK Mapping

| Tactic              | Technique                       | ID        |
| ------------------- | ------------------------------- | --------- |
| Execution           | PowerShell                      | T1059.001 |
| Command and Control | Application Layer Protocol      | T1071.001 |
| Defense Evasion     | Obfuscated Files or Information | T1027     |

---

## Incident Response Assessment

The investigation confirmed successful execution of a fileless PowerShell beacon and validated communication with a remote listener.

Although the beacon avoided creating files on disk, PowerShell ScriptBlock Logging provided sufficient visibility to identify and investigate the activity.

The investigation demonstrated the importance of PowerShell logging when monitoring fileless attack techniques.

---

## Skills Demonstrated

* Incident Response
* PowerShell Analysis
* Fileless Malware Investigation
* Command and Control Analysis
* Event ID 4104 Analysis
* Evidence Collection
* MITRE ATT&CK Mapping
* Security Monitoring

---

## Key Lesson

> Fileless activity may evade traditional file-based detection methods, but endpoint telemetry and PowerShell logging can still provide valuable investigative evidence.

This investigation demonstrated how PowerShell ScriptBlock Logging can be used to identify and analyse fileless command-and-control activity.
