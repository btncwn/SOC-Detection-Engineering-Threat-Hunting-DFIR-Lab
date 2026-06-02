# Investigation 05 – Threat Intelligence Driven Hunting

## Overview

This investigation demonstrates a threat intelligence driven hunting methodology.

Unlike traditional alert-driven investigations, threat hunting begins with a hypothesis derived from threat intelligence, adversary behavior, or observed indicators.

The objective is to use intelligence collected during previous investigations to proactively search Splunk telemetry for evidence of suspicious activity.

---

## Investigation Hypothesis

Threat intelligence indicators and behavioral findings collected during previous investigations may reveal additional evidence of attacker activity within the environment.

The investigation focuses on identifying:

* Encoded PowerShell execution
* Suspicious process creation
* Internal network discovery activity
* Host enumeration behavior
* Related attacker techniques

---

## Data Sources

* Splunk Enterprise
* Sysmon Telemetry
* BOTSv3 Dataset
* MISP Threat Intelligence Platform

---

## Investigation Workflow

Threat Intelligence Indicator

↓

Threat Hunting Hypothesis

↓

Splunk Search

↓

Telemetry Analysis

↓

Behavior Validation

↓

Investigation Outcome

---

## Investigation Outcome

Threat hunting activities identified behavior consistent with host discovery and internal network reconnaissance.

The investigation successfully demonstrated how threat intelligence findings can be used to guide proactive hunting activities within Splunk.

No additional threat intelligence attribution was established; however, behavioral evidence supported further investigative analysis.

---

## MITRE ATT&CK Mapping

| Tactic    | Technique                         |
| --------- | --------------------------------- |
| Discovery | T1087 - Account Discovery         |
| Discovery | T1018 - Remote System Discovery   |
| Discovery | T1046 - Network Service Discovery |
| Execution | T1059.001 - PowerShell            |

---

## Related Investigations

* Investigation 03 – Malware Hash Investigation
* Investigation 04 – MISP Threat Intelligence Enrichment
