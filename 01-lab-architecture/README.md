# Lab Architecture

## Overview

This project is built around a hands-on Security Operations Center (SOC), Threat Hunting, Detection Engineering, Incident Response , and Threat Intelligence lab environment.

The objective is to simulate real-world security operations by generating telemetry, conducting investigations, developing detections, performing threat intelligence enrichment, and documenting incident response activities.

---

## Lab Objectives

* Build a realistic SOC environment
* Generate attack telemetry
* Collect endpoint and network logs
* Perform threat hunting investigations
* Conduct IR activities
* Develop detection logic
* Integrate threat intelligence workflows
* Implement security automation concepts

---

## Lab Components

### Splunk Enterprise

Primary SIEM platform used for:

* Log ingestion
* Data analysis
* Threat hunting
* Dashboard creation
* Detection validation

### Windows 7

Primary endpoint used for:

* Sysmon telemetry generation
* Process monitoring
* Attack simulation
* Investigation exercises

### Sysmon

Endpoint telemetry source used for:

* Process creation monitoring
* Network connection monitoring
* File activity monitoring
* Parent-child process analysis

### Kali Linux

Adversary simulation platform used for:

* Reconnaissance
* Enumeration
* Attack simulation
* Security testing

### Nessus

Vulnerability assessment platform used for:

* Vulnerability discovery
* Risk identification
* Security assessment
* Remediation analysis

### MISP

Threat intelligence platform used for:

* IOC enrichment
* Threat intelligence analysis
* Indicator management
* Intelligence-driven investigations

### MITRE ATT&CK

Framework used for:

* Adversary behavior mapping
* Technique identification
* Detection coverage analysis
* Investigation documentation

### BOTSv3 Dataset

Security dataset used for:

* Threat hunting exercises
* Investigation scenarios
* Detection engineering validation
* SOC analyst training

---

## Data Flow

```text
Attack Simulation
        ↓
Windows 11 + Sysmon
        ↓
Splunk Enterprise
        ↓
Threat Hunting
        ↓
Threat Intelligence Enrichment
        ↓
       IR 
        ↓
Detection Engineering
        ↓
SOAR Automation
```

---

## Repository Structure

```text
01-lab-architecture
02-vulnerability-assessment
03-attack-simulation
04-endpoint-telemetry
05-splunk-ingestion
06-threat-hunting
07-mitre-attack-mapping
08-threat-intelligence
09-incident-response
10-soc-investigations
11-detection-engineering-sigma
12-soar-automation
```

---

## Skills Demonstrated

* Splunk Administration
* Threat Hunting
* Incident Response
* Threat Intelligence
* MITRE ATT&CK Mapping
* Vulnerability Management
* Detection Engineering
* Sigma Rule Development
* Security Automation

```
```
