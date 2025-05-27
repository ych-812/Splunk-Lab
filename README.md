# Splunk Lab Setup and Configuration

## Overview

This repository contains the setup and configuration details for a local Splunk lab designed to simulate a Security Operations Center (SOC) environment. The lab includes:

- Splunk Enterprise server installed locally
- Universal Forwarder installed on a Windows VM
- Configuration to collect Windows Event Logs (Security, System, Application)
- Forwarding logs from the VM to the local Splunk instance for monitoring and analysis

---

## Lab Setup

### Splunk Enterprise Server

- Installed on a local machine (host)
- Configured to receive data on port 9997
- Default index used for incoming logs

### Universal Forwarder (UF) on Windows VM

- Installed Universal Forwarder version X.X.X (specify version)
- Configured inputs to monitor Windows Event Logs:
  - Security
  - System
  - Application
- Configured outputs to forward logs to the Splunk server IP on port 9997

---

## Configuration Files

Located at:
C:\Program Files\SplunkUniversalForwarder\etc\system\local\inputs.conf

### inputs.conf

```ini
[WinEventLog://Security]
disabled = 0

[WinEventLog://System]
disabled = 0

[WinEventLog://Application]
disabled = 0

