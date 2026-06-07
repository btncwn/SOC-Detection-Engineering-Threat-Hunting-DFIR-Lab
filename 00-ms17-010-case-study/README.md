# MS17-010 (EternalBlue) – Full Adversary Emulation Case Study

## One-Sentence Summary

Discovered MS17-010 via Nessus, exploited it from Kali to Windows 7, captured Sysmon telemetry in Splunk, mapped to MITRE ATT&CK, and produced an incident report—all documented in my existing lab folders.

## Why This Case Study Exists

This folder contains **no new files**. Instead, it provides **symlinks** (shortcuts) to work already present in my main repository. Think of it as a curated tour of my MS17-010 investigation.

## Case Study Narrative

### Phase 1 – Vulnerability Discovery
📁 [01-nessus-scan](./01-nessus-scan)
- Nessus credentialed scan against Windows 7
- Found **MS17-010 (EternalBlue)** – critical SMBv1 RCE

### Phase 2 – Attack Simulation
📁 [02-attack-simulation](./02-attack-simulation)
- SMB enumeration and service discovery from Kali

### Phase 3 – Endpoint Telemetry
📁 [03-sysmon-telemetry](./03-sysmon-telemetry)
- Sysmon deployed on Windows 7
- Captured process creation (EventID 1), network connections (EventID 3)

### Phase 4 – SIEM Detection
📁 [04-splunk-detection](./04-splunk-detection)
- Splunk Enterprise ingesting Sysmon logs

### Phase 5 – MITRE ATT&CK Mapping
📁 [05-mitre-mapping](./05-mitre-mapping)

| TTP | Technique | Detected? |
|-----|-----------|-----------|
| T1210 | Exploitation of Remote Services | ✅ |
| T1059.001 | PowerShell | ✅ |
| T1021.002 | SMB Lateral Movement | ⚠️ (logged, no alert) |

### Phase 6 – Incident Response
📁 [06-incident-response](./06-incident-response)
- Full investigation with 9 screenshots

### Phase 7 – Detection Engineering (Sigma Rule)
📁 [07-sigma-rule](./07-sigma-rule)
- Sigma rule for scheduled task persistence

## Detection Coverage Summary

| Phase | Detected? |
|-------|-----------|
| Vulnerability scan | ✅ |
| SMB enumeration | ⚠️ (manual, no alert) |
| Exploit execution | ✅ |
| Reverse shell | ✅ |
| Lateral movement | ❌ (no Sigma rule yet) |
| Persistence | ✅ |

**Overall Coverage: 66% (4 of 6 phases detected)**

## How to Present This in an Interview

> *"I built a complete MS17-010 emulation chain. I found the vulnerability with Nessus, exploited it with Metasploit, captured Sysmon telemetry in Splunk, mapped everything to MITRE ATT&CK, and wrote an incident report. My detection coverage was 66% – I caught the exploit and reverse shell, but missed SMB enumeration and lateral movement alerts. Those gaps are now in my lab roadmap."*

## Last Updated

2026-06-07
