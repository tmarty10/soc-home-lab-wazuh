# Alert Simulations Overview

This section contains simulated security scenarios used to test custom Wazuh detection rules. These simulations were designed to replicate common attack behaviors and validate alert generation, log ingestion, and investigation workflows within a SOC environment.

## Custom Detection Rules

Although Wazuh already has its own rules for the following scenarious, custom Wazuh rules were created for practice and to better understand how log-based alerts are generated and correlated.

The rules cover the following scenarios:

- Multiple failed login attempts (brute force detection)
- New user account creation/User added to Administrators group (privilege escalation)
- Suspicious service creation (persistence technique)
- Sensitive file modification (file integrity monitoring)
- Suspicious PowerShell activity (command execution / obfuscation)

These rules leverage existing Wazuh rule IDs (`if_matched_sid`) and Windows Event IDs to ensure accurate detection while maintaining compatibility with built-in alerts.

## Custom Rules Configuration

Below is a snippet of the custom rules configured on the Wazuh manager:

![Custom Rules](../screenshots/custom-rules.png)

## Simulation Files

Each simulation is documented in its own file:

- `failed_logins.md`
- `new_user.md`
- `service_creation.md`
- `sensitive_file.md`
- `sus_powershell.md`

Each file includes:
- Simulation steps
- Log evidence
- Alert validation
