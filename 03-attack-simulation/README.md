# Attack Simulation

## Objective

This phase focused on generating realistic endpoint telemetry within a controlled Windows 7 SOC lab environment.

The goal was to produce process, PowerShell, command-line, and service activity that could be collected by Sysmon and analyzed in Splunk.

## Lab Environment

### Attacker Platform

* Kali Linux

### Target System

* Windows 7 SP1 x64
* Sysmon Installed
* Splunk Universal Forwarder Installed

### Monitoring Platform

* Splunk Enterprise

## Activities Performed

The following attack-oriented behaviors were generated and monitored:

* Process creation activity
* Command-line execution activity
* PowerShell execution activity
* Parent-to-child process relationships
* Windows service activity
* Splunk Universal Forwarder telemetry

## Detection Objectives

The generated activity was used to validate:

* Sysmon event collection
* Splunk log ingestion
* Threat hunting searches
* SOC dashboard visualizations
* Process activity monitoring

## Evidence

The generated telemetry was successfully visualized through the SOC Attack Timeline dashboard.

## Outcome

The attack simulation successfully generated Windows endpoint telemetry that was collected by Sysmon, forwarded to Splunk, and used to build detection engineering and threat hunting workflows.

This phase established the foundation for future ATT&CK mapping, DFIR investigations, and incident response exercises.
